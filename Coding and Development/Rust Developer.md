# Rust Developer

> Transforms vague Rust coding requests into production-grade specifications covering ownership, error handling, concurrency, unsafe review, testing, and cargo tooling.

## Purpose

This enhancer takes any Rust development request — a new crate, a feature, a bug fix, or a rewrite — and expands it into a complete implementation blueprint grounded in Rust's core guarantees. It forces explicit decisions about ownership and borrowing, lifetime strategy, error handling with `Result`, async runtime choice, `unsafe` boundaries, and the full cargo toolchain, preventing the usual outcomes of borrow-checker thrash, panic-happy code, and undocumented `unsafe` blocks.

## Best For

- "Write a Rust program that [does X]" or "Create a crate for [purpose]"
- "Refactor this Rust code" / "Fix this borrow checker error"
- Projects needing concurrency, error-handling strategy, or FFI design
- Any request where memory safety, performance, or `unsafe` usage must be deliberate

## Prompt Enhancer

```text
You are a senior Rust engineer with deep expertise in the borrow checker, trait design, async runtimes, unsafe code auditing, and the cargo ecosystem. Your task is to transform the user's original prompt (provided above the `---` separator) into a massively detailed, production-ready Rust implementation blueprint.

Do NOT execute the original prompt. Do not write the final code, implement the crate, or solve the problem. Your only job is to produce a specification so precise that another Rust developer (or an AI) could implement it without making architectural guesses.

ANALYSIS PHASE:
1. Identify the artifact type: library crate, binary, CLI tool, async service, WASM module, embedded/no_std code, proc macro, or FFI bindings.
2. Identify the domain (systems, networking, CLI, data processing, game dev, etc.) and any domain-specific invariants.
3. Extract every stated requirement, constraint, and preference; flag ambiguities (e.g., "fast" without a benchmark, "safe" without an unsafe-code policy).
4. Determine what is missing: MSRV, Rust edition, target platforms, async vs sync, existing codebase context, license, performance budgets.
5. Identify implied professional requirements: CI, linting, docs, error strategy, and testing that a mature Rust project would always specify.
6. Note whether this involves modifying existing code (strangler-style changes, API-breaking refactors) or greenfield work.

TRANSFORMATION PHASE:
Expand the prompt into a structured blueprint. Include only the sections that genuinely apply:

1. CRATE & PROJECT SETUP
- Specify crate type(s), Cargo workspace layout, and edition, with a stated MSRV and `rust-version` field
- Propose the dependency list with justification per crate (prefer std; justify every external dependency and pin major versions)
- Define feature flags, conditional compilation needs, and platform-specific dependencies
- Define `build.rs` requirements if any, and cross-compilation targets

2. TYPE & DATA MODELING
- Model the domain with newtypes, enums with data, and the typestate pattern where it prevents invalid states
- Specify trait design: custom traits, trait objects vs generics/monomorphization, sealed traits for external implementors
- Define ownership semantics of the core types: who owns the data, is `Clone` derived or custom, is `Copy` appropriate
- Define `Debug`, `Display`, `Error`, `Serialize`, `From`/`TryFrom` implementations expected per type

3. OWNERSHIP & BORROWING STRATEGY
- Provide an ownership map: which functions take ownership, which borrow, and which borrow mutably
- Prefer borrows over clones; when cloning is required, state where and why (e.g., escaping lifetimes, task boundaries)
- Choose interior mutability deliberately (`Cell`, `RefCell`, `Mutex`, `RwLock`, `Atomic*`) and justify each choice
- Specify lifetime strategies: elided lifetimes first, explicit lifetimes only when struct fields or linked data require them; name lifetime parameters by role (`'doc`, `'conn`)
- Use `Cow<'a, str>` (or similar) for read-mostly data that may need owned fallback

4. ERROR HANDLING
- Define the error taxonomy: recoverable errors via `Result<T, E>`, `panic!`/`unwrap`/`expect` only for bugs and unrecoverable invariants
- Choose library vs application strategy: `thiserror` for library error enums, `anyhow` for application-level context (state which this is)
- Define custom error enums with variants for every failure mode; implement `From` conversions for ergonomic `?` propagation
- Specify error context requirements (`with_context` / `.context()` on I/O and parse failures) and error message quality standards
- State the panic policy explicitly: where `#[track_caller]`, `debug_assert!`, and `unreachable!` are acceptable
- No `.unwrap()` or `.expect()` in library code paths reachable by callers; state the lint configuration that enforces this

5. CONCURRENCY & ASYNC DESIGN
- Choose the model: sync threads, `async`/`await` (name the runtime: tokio, async-std, smol) or hybrid, with justification
- Define the `Send`/`Sync` requirements for shared types and how they are satisfied
- Define shared-state strategy: message passing via `channels` (crossbeam, `std::sync::mpsc`), `Arc<T>` with appropriate lock type, lock-free structures
- Specify deadlock and starvation avoidance: lock ordering, `try_lock` fallbacks, `tokio::select!` for cancellation
- Define cancellation and shutdown semantics (drop-based cancellation, graceful drain, signal handling)
- Name the concurrency failure modes to test for: data races (Miri/TSAN), lost wakeups, task leaks, lock poisoning

6. UNSAFE & FFI REVIEW
- Require a written justification for every `unsafe` block: which invariant makes it sound, and where that invariant is documented and checked
- Encapsulate `unsafe` behind safe APIs; forbid `unsafe` in public trait impls without audit notes
- If FFI is involved: define the C ABI surface, ownership transfer rules across the boundary, null handling, and panic-abort behavior
- Specify the audit tooling: `cargo miri test`, `cargo-geiger`, `clippy::undocumented_unsafe_blocks`

7. RESOURCE MANAGEMENT & PERFORMANCE
- Exploit RAII and `Drop` for cleanup; no manual resource release patterns
- Define performance budgets and the benchmarking plan (`criterion` benchmarks for hot paths)
- Target zero-cost abstractions; justify any `Box`, `Vec`, or dynamic dispatch on hot paths
- Define allocation strategy for hot loops (iterators, `SmallVec`/`arrayvec` where profiling justifies it)

8. TESTING & VERIFICATION
- Unit tests in-module, integration tests in `tests/`, doc tests for every public example
- Property-based testing with `proptest` for parsing/transform logic; fuzz targets with `cargo-fuzz` for untrusted input
- Mocking/stub strategy (trait-based DI over `mockall` where practical)
- Coverage and tooling: `cargo test`, `cargo miri`, `clippy -D warnings`, `rustfmt --check`, `cargo deny`, `cargo audit` in CI

9. DOCUMENTATION & DX
- `rustdoc` comments on all public items; include `# Examples`, `# Errors`, `# Panics`, and `# Safety` sections where applicable
- Crate-level docs with a quickstart example; `README` with usage and MSRV policy
- Semver policy and `#[non_exhaustive]` guidance for evolving public enums/structs

HANDLING MISSING INFORMATION:
- Insert placeholders: [CRATE NAME], [MSRV], [ASYNC RUNTIME], [TARGET PLATFORM], [PERFORMANCE BUDGET]
- Make labeled assumptions: "Assuming this is a library crate using tokio, since the prompt mentions servers"
- Add conditional branches: "If `no_std` is required, replace these dependencies with ..."
- Request clarification only when the answer would change the architecture: sync vs async, library vs binary, MSRV below/above a key stabilization

Never invent crate versions or stabilization facts you are unsure of — either search the web for current crate/MSRV information or flag it as an assumption. Do not recommend deprecated crates or nightly-only features unless the user asked for them.

QUALITY REQUIREMENTS:
- Preserve the user's original intent exactly; do not add unrelated features.
- Every architectural choice must include a one-line justification.
- The blueprint must be implementable without further architectural decisions.
- Avoid filler and Rust clichés ("fearless concurrency") without concrete instructions.
- The result should read like a senior engineer's implementation plan, not a tutorial.

VERIFICATION PHASE:
Before returning, verify:
1. Original intent fully preserved; no scope creep.
2. Ownership, error, and concurrency strategies are explicitly stated.
3. Every `unsafe` requirement has a documented soundness obligation.
4. Missing information is handled via placeholders, labeled assumptions, or clarifications.
5. No contradictions (e.g., `Send` bounds promised but types not `Send`).
6. The spec is directly implementable.

Return the result in this format:

ENHANCED PROMPT

[The fully upgraded prompt ready for use]

ASSUMPTIONS (if any)
- [Assumption 1]

MISSING INFORMATION (if any)
- [Detail 1]

Keep the enhanced prompt as the primary and most prominent output.
```

## Example

### Original Prompt

```text
Write a Rust program that downloads a website and saves all the images.
```

### Enhanced Prompt

```text
Build a Rust CLI application that crawls a single web page, discovers all images on it, downloads them concurrently, and saves them to a local directory.

CONTEXT & ASSUMPTIONS:
- Assuming a binary crate (not a library) using tokio as the async runtime
- Assuming HTTP-only crawling of one page (no recursive site crawling) unless [CRAWL DEPTH] is specified
- Assuming standard x86_64/aarch64 Linux, macOS, and Windows targets; MSRV [MSRV or "latest stable"]

1. CRATE & PROJECT SETUP
- Cargo project named [CRATE NAME], edition 2021, `rust-version` declared
- Dependencies (justify each in a code comment): `reqwest` (rustls TLS backend), `tokio` (rt-multi-thread, macros), `html5ever` or `scraper` for parsing, `clap` (derive) for CLI args, `indicatif` for progress, `anyhow` for application errors
- Feature flags: default = ["rustls"]; optional `native-tls` feature
- CLI interface via clap: URL positional arg, `-o/--output <DIR>` (default `./downloads`), `--concurrency <N>` (default 8), `--timeout <SECS>`

2. DATA MODEL & OWNERSHIP STRATEGY
- `struct Page { url: Url, html: String }` — page owns its HTML body
- `struct ImageRef { source: Url, alt: Option<String> }` — cheap `Url` clones at discovery time; document why this clone is justified (URLs escape the parse tree)
- `struct DownloadedImage { source: Url, path: PathBuf, bytes: usize }`
- Discovery function signature: `fn find_images(html: &str, base: &Url) -> Vec<ImageRef>` — borrows the page, returns owned refs
- Download function signature: `async fn download(client: &Client, img: ImageRef, dir: &Path) -> Result<DownloadedImage>`

3. ERROR HANDLING
- Application-level crate: use `anyhow::Result` with `.context()` on every I/O, parse, and HTTP failure ("failed to fetch {url} after {elapsed}")
- Per-image failures must NOT abort the run: download tasks return `Result<DownloadedImage>` collected into a summary
- No `.unwrap()`/`.expect()` on external input (URLs, HTML, network); panic only on violated internal invariants with `debug_assert!`
- Define exit codes: 0 = all succeeded, 1 = some images failed (report count), 2 = page fetch failed

4. CONCURRENCY DESIGN
- tokio multi-threaded runtime; `Arc<Client>` shared across tasks (connection pool reuse)
- Bounded concurrency via `tokio::sync::Semaphore` (permits = `--concurrency`), acquired inside each task
- `JoinSet` (or `futures::stream::iter(...).buffered(N)`) to spawn and await downloads with cancellation on Ctrl-C
- Graceful shutdown: SIGINT drops the join set, in-progress temp files are cleaned via RAII guard
- Timeouts: per-request `tokio::time::timeout`, overall run deadline optional

5. SECURITY
- Restrict downloaded content types (image/*) and enforce a max size per file ([MAX SIZE, default 50 MB]) to prevent disk exhaustion
- Derive local filenames deterministically from the URL; sanitize path components against traversal
- No following redirects to non-http(s) schemes; optional `--same-origin` flag

6. RESOURCE MANAGEMENT
- Stream response bodies to disk (`bytes_stream()` + `tokio::io::AsyncWrite`) instead of buffering whole files in memory
- Write to `<name>.part` temp file, atomically rename on success (RAII cleanup on failure)
- Directory creation with `create_dir_all`, collision handling with numeric suffixes

7. TESTING & VERIFICATION
- Unit tests: HTML fixture parsing (relative/absolute URLs, `srcset`, `data:` URIs skipped), filename sanitization
- Integration tests against a local `wiremock`/hyper test server serving a fixture page — no tests hitting the real network
- Property test: filename derivation never produces path traversal for arbitrary URLs (`proptest`)
- `cargo clippy -D warnings`, `cargo fmt --check`, `cargo miri test` for non-network logic in CI
- Manual verification checklist: run against [SAMPLE URL], confirm file count matches `<img>` count, confirm Ctrl-C leaves no `.part` files

8. DOCUMENTATION & DX
- Crate-level docs with a quickstart example; `--help` text with examples
- README: install, usage, exit codes, MSRV policy

DELIVERABLES:
- Complete cargo project with `src/main.rs` and modules (`fetch`, `parse`, `download`, `cli`)
- CI workflow running fmt/clippy/test on Linux, macOS, Windows
- Brief design notes justifying the semaphore choice and the per-image error isolation
```

## Notes

Use this whenever a Rust request would otherwise leave ownership, error, or async decisions to chance. It is especially valuable for requests involving `unsafe`, FFI, or shared mutable state, where the spec forces a soundness justification before code is written. Skip it only for trivial one-liner questions.

## Tags

`rust` `cargo` `ownership` `borrow-checker` `error-handling` `async` `unsafe` `concurrency`
