# Phase 1: Data Collection & Preparation (Month 1)

## In Simple Terms - What Are We Doing?

We're gathering "learning material" for the translation model. Just like a student needs textbooks, our AI needs examples to learn from.

---

## The 4 Tasks

| Task | What It Means | Old Way (Manual) | New Way (LLM-Assisted) |
|------|---------------|------------------|------------------------|
| **Parallel Corpus** | English sentence + Indian language translation pairs | Humans manually align documents line-by-line | LLM auto-aligns sentences, humans verify |
| **Sentence Pairs** | 50K matched sentences per language | Manual copy-paste from old translations | LLM extracts & matches from PDFs/docs automatically |
| **Glossary** | List of technical terms (ECU = ECU, ABS = ABS) | SME manually creates term list | LLM scans documents, extracts technical terms, humans approve |
| **NER Lexicon** | Part numbers, model names to protect | Manual identification from manuals | LLM identifies patterns (part numbers, codes) automatically |

---

## Before vs After LLM

| Activity | Before (Weeks) | After LLM (Weeks) |
|----------|----------------|-------------------|
| Document alignment | 3-4 weeks | 1 week |
| Term extraction | 2-3 weeks | 3-5 days |
| NER tagging | 2 weeks | 1 week |
| **Total** | **7-9 weeks** | **2-3 weeks** |

---

## What LLM Does in Phase 1

1. **Reads PDFs/Docs** - Extracts text automatically
2. **Aligns Sentences** - Matches English <-> Indian language pairs
3. **Finds Technical Terms** - Identifies ECU, ABS, torque specs
4. **Tags Entities** - Marks part numbers, model names
5. **Flags Gaps** - Shows where data is missing

---

## What Humans Still Do

- Verify LLM's alignment is correct
- Approve glossary terms
- Fill data gaps
- Quality check

---

## Bottom Line

> **Phase 1** = Feeding the AI its textbooks
> **LLM** = The assistant that organizes the library
> **Humans** = The librarian who approves the catalog

---

## Deep Dive: What → How → Why → Next

### Task 1: Parallel Corpus Collection

| Question | Answer |
|----------|--------|
| **WHAT** | Paired documents (English + Indian language version of same content) |
| **HOW** | Extract from GGS's existing translated manuals, service docs, bulletins |
| **WHY** | AI learns by seeing "this English = this Hindi" - needs thousands of examples |
| **NEXT (Phase 2)** | Becomes the "textbook" for model fine-tuning. No corpus = no training. |

---

### Task 2: Sentence Pair Curation (50K per language)

| Question | Answer |
|----------|--------|
| **WHAT** | Clean, aligned sentence-by-sentence pairs from the corpus |
| **HOW** | LLM splits documents → matches sentences → humans verify alignment |
| **WHY** | Model learns at sentence level, not document level. Garbage in = garbage out. |
| **NEXT (Phase 2)** | Direct input to fine-tuning. Quality here = accuracy later. |

---

### Task 3: Automotive Glossary

| Question | Answer |
|----------|--------|
| **WHAT** | Dictionary: English term → Approved Indian language translation |
| **HOW** | LLM scans corpus → extracts technical terms → SMEs approve translations |
| **WHY** | "ECU" must translate consistently every time, not randomly |
| **NEXT (Phase 2)** | Terminology Enforcement Layer uses this during training + inference |

---

### Task 4: NER Lexicon

| Question | Answer |
|----------|--------|
| **WHAT** | List of entities to PROTECT (part numbers, model names, codes) |
| **HOW** | LLM finds patterns (e.g., "P0301", "XYZ-1234") → humans validate |
| **WHY** | Part number "P0301" should stay "P0301" - never translated |
| **NEXT (Phase 2)** | NER module tags these BEFORE translation, protects them during process |

---

## The Flow: Phase 1 → Phase 2

```
Phase 1 Output              →    Phase 2 Input
─────────────────────────────────────────────────
Parallel Corpus             →    Training Dataset
Sentence Pairs (50K x 4)    →    Fine-tuning Examples
Glossary                    →    Terminology Enforcement
NER Lexicon                 →    Entity Protection Layer
```

---

## Key Insight

> **Phase 1 is the FOUNDATION.**
> If data is poor → model is poor → output is poor.
>
> Phase 2 cannot fix bad Phase 1 work.
