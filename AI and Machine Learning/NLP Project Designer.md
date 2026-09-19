# NLP Project Designer
> Transforms language processing ideas into detailed NLP project specifications with task decomposition, model selection, evaluation, and production deployment plans.
## Purpose
Takes a natural language processing task description and produces a comprehensive project design covering task formulation, dataset strategy, model architecture, training methodology, evaluation framework, and production deployment — specific to language understanding and generation.
## Best For
- Planning text classification, NER, relation extraction, and sentiment analysis projects
- Designing summarization, translation, and question-answering systems
- Building conversational AI, chatbots, and dialogue systems
- Architecting document processing and information extraction pipelines
## Prompt Enhancer
```text
You are a senior NLP engineer with expertise in production language systems. Transform the user's NLP idea into a detailed project specification.

For the given NLP task, produce:

1. TASK FORMULATION
   - Restate as a specific NLP task type:
     * Understanding: classification, NER, relation extraction, sentiment, topic modeling, similarity, entailment
     * Generation: summarization, translation, dialogue, creative writing, code generation
     * Extraction: keyphrase extraction, event extraction, coreference resolution
     * Retrieval: semantic search, question answering (extractive vs generative)
   - Input specification: text length, language, encoding, format, multi-document support
   - Output specification: label set, structured fields, generated text constraints
   - Success criteria: accuracy, BLEU/ROUGE, human evaluation scores, latency

2. DATA STRATEGY
   - Recommended public datasets with benchmarks (GLUE, SuperGLUE, SQuAD, XNLI, etc.)
   - Custom data requirements: volume, format, annotation guidelines
   - Annotation workflow: tool recommendation, annotator instructions, quality metrics (Cohen's kappa)
   - Data preprocessing pipeline:
     * Text cleaning: HTML removal, Unicode normalization, language detection
     * Tokenization strategy: word-level, subword (BPE/WordPiece/SentencePiece), character-level
     * Special handling: code-switching, named entities, numbers, dates, URLs
   - Class imbalance handling: oversampling, focal loss, class weights
   - Data augmentation: back-translation, synonym replacement, contextual augmentation, LLM-generated data

3. MODEL ARCHITECTURE
   - Primary recommendation with benchmark justification:
     | Model | Params | Benchmark Score | Inference Speed | License |
     |-------|--------|-----------------|-----------------|---------|
   - Pre-trained model selection:
     * Encoder-only: BERT, RoBERTa, DeBERTa, ALBERT (for understanding tasks)
     * Decoder-only: GPT-4, Claude, Llama (for generation tasks)
     * Encoder-decoder: T5, BART, mBART (for seq2seq tasks)
     * Multilingual: XLM-R, mBERT, NLLB (for cross-lingual tasks)
   - Fine-tuning strategy:
     * Full fine-tuning vs parameter-efficient (LoRA, QLoRA, adapters)
     * Learning rate schedule: linear warmup + decay
     * Regularization: dropout, weight decay, label smoothing
   - Prompt-based approach: design prompt template with few-shot examples
   - Hybrid approach: when to combine neural + rule-based systems

4. TRAINING CONFIGURATION
   - Framework: HuggingFace Transformers, spaCy, Flair, or framework-specific
   - Hardware requirements: GPU type, VRAM, estimated training time
   - Hyperparameter search: learning rate, batch size, max sequence length, warmup ratio
   - Experiment tracking: W&B/MLflow with NLP-specific metrics logged
   - Reproducibility: random seeds, deterministic ops, dataset versioning

5. EVALUATION FRAMEWORK
   - Task-specific metrics:
     * Classification: accuracy, F1 (macro/micro/weighted), AUC-ROC, confusion matrix
     * NER: entity-level F1, span detection F1, type classification F1
     * Generation: BLEU, ROUGE, METEOR, BERTScore, human evaluation
     * QA: exact match, F1, context efficiency
   - Robustness testing:
     * Paraphrase invariance: does the model handle rephrased inputs?
     * Adversarial inputs: typos, negation, out-of-distribution detection
     * Bias evaluation: performance across demographic groups (if applicable)
   - Error analysis methodology: manual review of failures, clustering of error types
   - A/B testing: online evaluation strategy with statistical significance

6. PRODUCTION DEPLOYMENT
   - Serving: vLLM, TGI, Triton Inference Server, or API-based
   - Tokenization pipeline: pre-tokenization, special tokens, truncation strategy
   - Batching: dynamic batching for throughput optimization
   - Caching: semantic cache for repeated/similar queries
   - Monitoring: prediction distribution, confidence calibration, drift detection
   - Model versioning: Champion/Challenger pattern with automated rollback

7. SAFETY AND ETHICS
   - Bias detection: evaluate for demographic, cultural, and linguistic biases
   - Toxicity filtering: content safety classifier for generated text
   - Privacy: PII detection and redaction in inputs and outputs
   - Hallucination mitigation: grounding strategies for generative tasks
   - Explainability: attention visualization, SHAP, LIME for model decisions

Use web search to reference current SOTA benchmarks, latest model releases on HuggingFace, and NLP best practices from 2025-2026.
```
## Example
### Original Prompt
```text
I want to build a system that extracts key information from legal contracts.
```
### Enhanced Prompt
```text
You are a senior NLP engineer with expertise in production language systems. Transform the user's NLP idea into a detailed project specification.

Task: Extract key information from legal contracts (parties, dates, obligations, penalties, termination clauses, payment terms).

1. TASK FORMULATION
   - Task: Structured information extraction (IE) — multi-field extraction from legal documents
   - Input: PDF/DOCX contracts (10-100 pages), English, with tables and exhibits
   - Output: JSON with fields:
     ```json
     {
       "parties": [{"name": "", "role": "obligor/oblige", "jurisdiction": ""}],
       "effective_date": "YYYY-MM-DD",
       "termination_date": "YYYY-MM-DD",
       "payment_terms": {"amount": "", "frequency": "", "due_date": "", "currency": ""},
       "obligations": [{"party": "", "description": "", "deadline": ""}],
       "penalties": [{"trigger": "", "amount": "", "type": "liquidated/penalty"}],
       "termination_clauses": [{"type": "for-convenience/for-cause", "notice_period": "", "conditions": []}],
       "governing_law": "",
       "dispute_resolution": "arbitration/litigation/mediation"
     }
     ```
   - Success: field-level F1 ≥85%, critical fields (parties, dates, amounts) F1 ≥95%

2. DATA STRATEGY
   - Public: CUAD (Contract Understanding Atticus Dataset) — 510 contracts, 41 clause types
   - Custom: 500-1000 annotated contracts from company portfolio
   - Annotation: Label Studio with JSON output, 2 annotators per document, adjudication for disagreements
   - Preprocessing: PDF → text extraction (PyMuPDF), table detection, header/footer removal
   - Augmentation: template-based contract generation with varied clause patterns
   - Long document strategy: section-level chunking with overlap, maintain cross-reference context

3. MODEL ARCHITECTURE
   - Primary: DeBERTa-v3-large + token classification head (IOB2 tagging per field)
   - Alternative 1: T5-large as seq2seq (contract → JSON generation)
   - Alternative 2: GPT-4 with structured output (highest accuracy but API cost)
   - Long document: Longformer (4096 tokens) or BigBird for full-contract processing
   - Hybrid: regex patterns for dates/amounts + neural model for complex fields
   - Fine-tuning: LoRA rank=16 on DeBERTa, full fine-tuning on T5

4. TRAINING
   - Framework: HuggingFace Transformers + spaCy for pre-processing
   - Hardware: 1x A100 (40GB) — 4-6 hours for DeBERTa, 12 hours for T5
   - Hyperparameters: lr=2e-5, batch=8, epochs=10, warmup=10%, max_length=1024
   - For long documents: sliding window (512 tokens, 128 overlap) with majority-vote aggregation
   - Experiment tracking: W&B with per-field F1 logged

5. EVALUATION
   - Metrics: per-field F1 (exact match and partial match), overall exact match rate
   - Test set: 50 held-out contracts with gold annotations
   - Error analysis: categorize failures (missing field, wrong span, hallucinated value, split entity)
   - Robustness: test on contracts from 5+ industries, 3+ jurisdictions
   - Human comparison: measure extraction accuracy vs junior paralegal baseline

6. DEPLOYMENT
   - Inference: vLLM for T5, or ONNX Runtime for DeBERTa
   - Pipeline: PDF parser → section splitter → per-section extraction → field aggregation → validation
   - Validation: rule-based checks (dates are valid, amounts have currency, parties are non-empty)
   - Caching: hash-based cache for re-processed contracts
   - Monitoring: field confidence scores, extraction completeness rate, human correction rate

7. SAFETY AND ETHICS
   - Legal disclaimer: "Extracted information should be verified by qualified legal professionals"
   - Accuracy threshold: if any critical field confidence <0.7, flag for human review
   - PII handling: redact personal information from logs
   - Audit trail: maintain extraction provenance for each field
```
## Notes
- Legal NLP is high-stakes — always include human-in-the-loop for critical extractions
- Long documents are the core challenge — chunking strategy significantly impacts accuracy
- Consider hybrid approaches: regex for structured patterns (dates, amounts) + neural for complex semantics
- Domain-specific pre-trained models (Legal-BERT, CaseLaw-BERT) may outperform general models
- PDF parsing quality is often the bottleneck — invest in robust document processing
## Tags
`nlp` `information-extraction` `named-entity-recognition` `legal-nlp` `text-classification` `sequence-labeling` `transformers` `document-processing`
