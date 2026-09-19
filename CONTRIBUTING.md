# Contributing to AI Prompts Vault

<p align="center">
  <strong>This project is open for contributions!</strong><br>
  <em>If you have a Prompt Enhancer idea, we want it.</em>
</p>

---

## The Short Version

```
Fork → Branch → Add Enhancer → Pull Request
```

1. **Fork** this repository
2. **Create a branch** for your enhancer
3. **Add your enhancer** as a `.md` file in the right category
4. **Open a Pull Request**

That's it. If your enhancer is high-quality and useful, it gets merged.

---

## What We're Looking For

We want **Prompt Enhancers** — detailed, expert-level instruction prompts that transform simple user prompts into dramatically more detailed and structured versions.

### What Makes a Good Enhancer

- **Detailed and specific** — not "make it better" but a comprehensive transformation methodology
- **Domain-aware** — understands the specific field and what matters in it
- **Actually transforms** — instructs the AI to improve the prompt, not execute it
- **Well-documented** — includes a clear before/after example
- **Useful** — someone should be able to copy it and get a better prompt immediately

### What We Don't Accept

- Weak enhancers like "improve this prompt" or "add more details"
- Enhancers that execute the task instead of transforming the prompt
- Duplicate enhancers that already exist in the library
- Placeholder content with no real substance

---

## Step-by-Step Guide

### 1. Fork the Repository

Click the **Fork** button on the GitHub page to create your own copy.

### 2. Clone Your Fork

```bash
git clone https://github.com/YOUR-USERNAME/AI-Prompt-Engineer.git
cd AI-Prompt-Engineer
```

### 3. Create a Branch

```bash
git checkout -b add-my-enhancer-name
```

Use a descriptive branch name like:
- `add-python-testing-enhancer`
- `add-seo-blog-writer`
- `add-medical-research-analyst`

### 4. Choose the Right Category

Place your enhancer in the appropriate folder under `AI PROMPT ENHANCER/`.

| Category | For Enhancers About |
|----------|-------------------|
| `Universal/` | Cross-domain enhancers that work anywhere |
| `Coding and Development/` | Programming, APIs, DevOps, databases |
| `Writing and Content/` | Blog posts, copywriting, technical writing |
| `Research and Analysis/` | Market research, literature reviews, analysis |
| `Image Generation and Creative/` | AI image prompts, digital art, design |
| `Business and Strategy/` | Business plans, pitch decks, strategy |
| `Education and Learning/` | Courses, tutoring, assessments |
| `Productivity and Planning/` | Projects, goals, workflows, sprints |
| `Technical and Engineering/` | Systems, cloud, IoT, infrastructure |
| `Data and Analytics/` | Pipelines, dashboards, SQL, ETL |
| `AI and Machine Learning/` | ML models, LLM apps, MLOps |
| `Health and Science/` | Clinical research, medical writing |
| `Marketing and SEO/` | SEO, ad copy, email marketing |
| `Legal and Compliance/` | Contracts, compliance, privacy |

**No fitting category?** Create a new one. Make sure the name is specific and useful.

### 5. Create Your Enhancer

Create a new `.md` file with the required format:

```markdown
# Enhancer Name

> One-sentence explanation of what this enhancer does.

## Purpose

Explain the enhancer's purpose and what makes it unique.

## Best For

Explain what kinds of prompts it works with.

## Prompt Enhancer

```text
[YOUR COMPLETE, DETAILED ENHANCER HERE]
```

## Example

### Original Prompt

```text
[A simple example prompt]
```

### Enhanced Prompt

```text
[The dramatically improved version the enhancer produces]
```

## Notes

Brief practical notes about when and how to use this enhancer.

## Tags

`tag1` `tag2` `tag3`
```

### The `## Prompt Enhancer` Section Is Everything

This is the part users will copy and paste. It must be:

**Detailed** — Provide comprehensive transformation instructions, not vague directions.

**Domain-specific** — Understand what matters in the specific field.

**Actionable** — The AI should know exactly how to transform the prompt.

**Safe** — Prevent hallucination, handle missing information, preserve intent.

Here's what a strong enhancer looks like internally:

```text
You are an expert prompt engineer specializing in [DOMAIN].

The user's original prompt appears above the `---` separator.

Your task is NOT to answer or execute that prompt.
Your sole objective is to transform it into a substantially more
detailed and professionally engineered prompt that another AI can
use to perform the requested task.

ANALYSIS:
1. Determine the user's actual objective and preserve it
2. Extract every explicit requirement
3. Identify ambiguity and missing information
4. Consider domain-specific requirements...

TRANSFORMATION:
Based on your analysis, expand the prompt with relevant information:
- [Domain-specific dimension 1]
- [Domain-specific dimension 2]
- [Domain-specific dimension 3]
...

QUALITY:
- Preserve the user's original intent
- Do not add unrelated goals
- Use placeholders for missing information
- Do not fabricate facts
...

Return the enhanced prompt in a clean, copyable format.
```

**Do NOT create weak enhancers** like:

```text
Make this prompt better by adding more details.
```

These are too vague to be useful.

### 6. Test Your Enhancer

Before submitting, mentally walk through the workflow:

1. Imagine a user writes a simple prompt
2. They paste your enhancer below the `---` separator
3. Does the AI understand exactly how to transform the prompt?
4. Does the result actually improve the prompt meaningfully?
5. Is the enhanced prompt more detailed, structured, and useful?

### 7. Commit and Push

```bash
git add .
git commit -m "Add [enhancer name] to [category]"
git push origin add-my-enhancer-name
```

### 8. Open a Pull Request

Go to your fork on GitHub and click **New Pull Request**.

In your PR description, include:
- **What your enhancer does** — one sentence
- **Which category** it belongs to
- **Why it is distinct** from existing enhancers

---

## Quality Standards

### Must Have

- [ ] A detailed `## Prompt Enhancer` section (the core of your contribution)
- [ ] At least one before/after example
- [ ] At least 3 relevant tags
- [ ] A clear purpose and use case
- [ ] Proper Markdown formatting

### Should Have

- [ ] Domain-specific guidance within the enhancer
- [ ] Web research instructions where relevant
- [ ] Missing information handling (placeholders, assumptions)
- [ ] Intent preservation instructions
- [ ] Clear output format instructions

### Must Not Have

- [ ] Vague or generic "improve this" instructions
- [ ] Filler content or meaningless verbosity
- [ ] Duplicated content from other enhancers
- [ ] Instructions that execute the task instead of transforming the prompt

---

## Naming Conventions

- Use **Title Case** for file names
- Be descriptive: `Python Backend Developer.md`, not `Python.md`
- Avoid abbreviations unless universally understood
- Good examples:
  - `Full Stack Developer.md`
  - `SEO Blog Writer.md`
  - `Medical Research Analyst.md`
  - `Pitch Deck Creator.md`
  - `Database Designer.md`

---

## Creating New Categories

If no existing category fits:

1. Choose a name that is specific, clear, and useful
2. Create the folder under `AI PROMPT ENHANCER/`
3. Add the category to the README.md table
4. Ensure it does not overlap significantly with an existing category

---

## Review Process

All contributions are reviewed for:

1. **Quality** — Is the enhancer detailed and well-engineered?
2. **Usefulness** — Does it actually transform prompts meaningfully?
3. **Uniqueness** — Is it distinct from existing enhancers?
4. **Accuracy** — Are domain-specific considerations handled correctly?
5. **Formatting** — Does it follow the required file structure?

We aim to review PRs within **7 days**.

---

## Questions?

If you have questions about contributing, open a GitHub Issue with the label `question`.

---

## Code of Conduct

- Be respectful
- Be constructive
- Be helpful
- We are building a resource that helps everyone get better results from AI

---

## Thank You

Every contribution makes this library more useful for everyone.

**Have a Prompt Enhancer idea? Open a Pull Request.**

---

*Created by [Kritagya Dubey](https://github.com/kritagyadubey) — [@kritagyadubey](https://github.com/kritagyadubey)*
