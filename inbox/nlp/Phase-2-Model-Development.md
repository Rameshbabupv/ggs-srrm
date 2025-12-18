# Phase 2: Model Development (Month 2)

## In Simple Terms - What Are We Doing?

Teaching the AI to translate using the textbooks from Phase 1. Like training a new employee with company-specific knowledge.

---

## The 3 Core Tasks

| Task | What | How | Why | Next (Phase 3) |
|------|------|-----|-----|----------------|
| **Base Model Selection** | Pick the starting AI brain | Evaluate IndicTrans2 vs NLLB-200 | Don't start from scratch - leverage existing knowledge | Foundation for fine-tuning |
| **Fine-Tuning** | Teach automotive domain | Feed 50K sentence pairs per language | Generic model → Domain expert | Core engine for pipeline |
| **NER Integration** | Protect entities during translation | Tag part numbers before translation | "P0301" stays "P0301" | Feeds into post-processor |

---

## Suggestions & Alternatives

### 1. Base Model Choice

| Option | Pros | Cons | Recommendation |
|--------|------|------|----------------|
| **IndicTrans2** | Built for Indian languages, open-source | Smaller community | Best for Phase 1 (Hindi, Tamil) |
| **NLLB-200** | 200 languages, Meta-backed | Generic, needs more fine-tuning | Backup option |
| **Google Gemma** | Modern, efficient | Less tested for Indic | Future consideration |

> **Recommendation:** Start with **IndicTrans2** - purpose-built for Indian languages.

---

### 2. Fine-Tuning Approach

| Approach | Description | Benefit |
|----------|-------------|---------|
| **Full Fine-Tuning** | Train all parameters | Heavy GPU, slow, expensive |
| **LoRA/PEFT** | Train only small adapters | 70% less compute, faster, cheaper |
| **QLoRA** | LoRA + quantization | Even cheaper, minimal quality loss |

> **Recommendation:** Use **LoRA** - same quality, 70% less cost, faster iterations.

---

### 3. Training Strategy

| Strategy | Description | Pros | Cons |
|----------|-------------|------|------|
| **Sequential** | Train Hindi → Tamil → Telugu → Malayalam | Focused, easier debugging | Slower, 4x time |
| **Parallel** | Train all 4 together (multilingual) | Faster, shared learning | Needs more GPU |
| **Hybrid** | Hindi+Tamil together, then Telugu+Malayalam | Balanced | Medium complexity |

> **Recommendation:** **Hybrid** - Group by script similarity (Hindi+Tamil first).

---

### 4. NER Integration Timing

| Approach | When | Pros | Cons |
|----------|------|------|------|
| **Pre-Translation** | Tag entities BEFORE translation | Clean, entities protected | Extra processing step |
| **Post-Translation** | Fix entities AFTER translation | Simpler pipeline | May miss some |
| **Dual** | Tag before + verify after | Most accurate | Slower |

> **Recommendation:** **Pre-Translation** - protect entities upfront, cleaner results.

---

## Suggested Phase 2 Flow

```
Week 1: Model Selection & Setup
        ↓
Week 2: Fine-tune Hindi + Tamil (LoRA)
        ↓
Week 3: Fine-tune Telugu + Malayalam (LoRA)
        ↓
Week 4: NER Integration + Evaluation (BLEU > 40)
```

---

## Key Risks & Mitigation

| Risk | Impact | Mitigation |
|------|--------|------------|
| Low BLEU scores | Poor translation | More training data, adjust hyperparameters |
| GPU shortage | Delays | Use spot instances, LoRA reduces need |
| Language imbalance | Some languages worse | Prioritize Hindi/Tamil, others in Phase 2 |

---

## What Changes From Original Plan?

| Original | Suggested | Why |
|----------|-----------|-----|
| Full fine-tuning | LoRA/PEFT | Cost & speed |
| All 4 languages equal | Prioritize Hindi+Tamil | Higher demand, faster delivery |
| NER as separate step | Integrated in training | Cleaner pipeline |

---

## Deep Dive: What → How → Why → Next

### Task 1: Base Model Selection

| Question | Answer |
|----------|--------|
| **WHAT** | Choose pre-trained translation model as starting point |
| **HOW** | Benchmark IndicTrans2 vs NLLB-200 on sample automotive text |
| **WHY** | Starting from scratch = years of work. Pre-trained = weeks. |
| **NEXT (Phase 3)** | Selected model becomes core of translation pipeline |

---

### Task 2: Fine-Tuning on Automotive Domain

| Question | Answer |
|----------|--------|
| **WHAT** | Train model on GGS-specific automotive sentence pairs |
| **HOW** | LoRA fine-tuning with 50K pairs per language on GPU |
| **WHY** | Generic model doesn't know "torque converter" - now it will |
| **NEXT (Phase 3)** | Fine-tuned model deployed as translation engine |

---

### Task 3: NER Integration

| Question | Answer |
|----------|--------|
| **WHAT** | Connect entity recognition to protect part numbers, codes |
| **HOW** | spaCy/BERT NER trained on Phase 1 lexicon, tags before translation |
| **WHY** | "P0301" must stay "P0301" - not translated to gibberish |
| **NEXT (Phase 3)** | NER feeds into pre-processor, output verified in post-processor |

---

## The Flow: Phase 2 → Phase 3

```
Phase 2 Output              →    Phase 3 Input
─────────────────────────────────────────────────
Fine-tuned Model            →    Translation Engine
NER Component               →    Pre-processor Module
BLEU Benchmarks             →    Quality Baseline
Training Logs               →    MLOps Pipeline
```

---

## Key Insight

> **Phase 2 is the BRAIN.**
> Phase 1 gave the textbooks. Phase 2 creates the expert.
>
> Quality of fine-tuning = Quality of translations forever.
