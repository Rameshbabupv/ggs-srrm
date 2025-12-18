# Phase 3: System Integration (Month 3)

## In Simple Terms - What Are We Doing?

Building the factory around the brain. Phase 2 gave us a smart translator - now we wrap it in a usable system with inputs, outputs, quality checks, and a user interface.

---

## The 5 Core Tasks

| Task | What | How | Why | Next (Phase 4) |
|------|------|-----|-----|----------------|
| **Pre-processor** | Clean & prepare input docs | Parse PDF/XML, segment sentences, tag entities | Garbage in = garbage out | Ready for testing |
| **Post-processor** | Polish translated output | Terminology check, format preservation, entity verification | Ensure consistency | QA validation |
| **Quality Estimator** | Score translation confidence | COMET-QE scoring per sentence | Flag bad translations for human review | UAT metrics |
| **API Layer** | Expose translation service | FastAPI endpoints (batch + real-time) | Enable integration with other systems | Load testing |
| **Web UI** | User-friendly interface | Upload docs, view translations, review flagged items | Non-technical users can use the system | User testing |

---

## Suggestions & Alternatives

### 1. Pre-processor Options

| Approach | Tools | Pros | Cons |
|----------|-------|------|------|
| **Custom Pipeline** | Python + lxml + PDFPlumber | Full control | More dev time |
| **Apache Tika** | Pre-built document parser | Fast setup | Less customization |
| **LangChain Loaders** | LLM-native document loading | Modern, flexible | Newer, less tested |

> **Recommendation:** **Custom Pipeline** - automotive docs need precise handling.

---

### 2. Quality Estimation Options

| Approach | Tool | Pros | Cons |
|----------|------|------|------|
| **COMET-QE** | Reference-free scoring | No need for gold translations | Compute heavy |
| **BLEU-based** | Compare to reference | Simple | Needs reference translations |
| **LLM-as-Judge** | GPT/Claude evaluates | Flexible, contextual | Cost per call |

> **Recommendation:** **COMET-QE** for automated scoring + **LLM-as-Judge** for edge cases.

---

### 3. API Architecture

| Approach | Description | Pros | Cons |
|----------|-------------|------|------|
| **Sync API** | Request → Wait → Response | Simple | Slow for large docs |
| **Async + Queue** | Submit → Job ID → Poll results | Scalable, handles large docs | More complex |
| **Hybrid** | Sync for small, Async for large | Best of both | Two code paths |

> **Recommendation:** **Hybrid** - real-time for single pages, async for batch.

---

### 4. UI Options

| Approach | Tech | Pros | Cons |
|----------|------|------|------|
| **React SPA** | React + Tailwind | Modern, fast | Heavier dev |
| **Streamlit** | Python-native | Fast to build, ML-friendly | Less polished |
| **Gradio** | ML demo UI | Fastest MVP | Limited customization |

> **Recommendation:** **Streamlit** for MVP → **React** for production.

---

## Suggested Phase 3 Flow

```
Week 1: Pre-processor + Post-processor Pipeline
        ↓
Week 2: Quality Estimator Integration (COMET-QE)
        ↓
Week 3: FastAPI Endpoints (Batch + Real-time)
        ↓
Week 4: Web UI + Database Setup (PostgreSQL)
```

---

## System Architecture

```
┌─────────────┐     ┌──────────────┐     ┌─────────────┐
│   Web UI    │────▶│   FastAPI    │────▶│  Database   │
└─────────────┘     └──────────────┘     │ (PostgreSQL)│
                           │              └─────────────┘
                           ▼
                    ┌──────────────┐
                    │ Pre-processor│
                    │  - PDF Parse │
                    │  - NER Tag   │
                    └──────────────┘
                           │
                           ▼
                    ┌──────────────┐
                    │  Translation │
                    │   Engine     │
                    │ (Phase 2)    │
                    └──────────────┘
                           │
                           ▼
                    ┌──────────────┐
                    │Post-processor│
                    │  - Term Check│
                    │  - Format    │
                    └──────────────┘
                           │
                           ▼
                    ┌──────────────┐
                    │   Quality    │
                    │  Estimator   │
                    │  (COMET-QE)  │
                    └──────────────┘
                           │
                           ▼
                    ┌──────────────┐
                    │   Output     │
                    │ + Confidence │
                    └──────────────┘
```

---

## Deep Dive: What → How → Why → Next

### Task 1: Pre-processor

| Question | Answer |
|----------|--------|
| **WHAT** | Ingestion layer - cleans and prepares documents for translation |
| **HOW** | PDF/XML parsing → Sentence segmentation → NER tagging → Glossary lookup |
| **WHY** | Model expects clean, tagged sentences - not raw messy documents |
| **NEXT (Phase 4)** | Test with real GGS documents, measure parsing accuracy |

---

### Task 2: Post-processor

| Question | Answer |
|----------|--------|
| **WHAT** | Output layer - polishes and validates translations |
| **HOW** | Terminology consistency check → Entity verification → Format reconstruction |
| **WHY** | Ensure ECU translated same way everywhere, part numbers intact |
| **NEXT (Phase 4)** | Validate 95% terminology consistency target |

---

### Task 3: Quality Estimator

| Question | Answer |
|----------|--------|
| **WHAT** | Confidence scoring for each translated sentence |
| **HOW** | COMET-QE model scores 0-100, flag below 75 for human review |
| **WHY** | Catch bad translations before they reach users |
| **NEXT (Phase 4)** | Calibrate thresholds based on UAT feedback |

---

### Task 4: API Layer

| Question | Answer |
|----------|--------|
| **WHAT** | REST endpoints for translation service |
| **HOW** | FastAPI with /translate (sync), /batch (async), /status (polling) |
| **WHY** | Enable integration with GGS systems, future automation |
| **NEXT (Phase 4)** | Load testing - target 60 sec/doc |

---

### Task 5: Web UI

| Question | Answer |
|----------|--------|
| **WHAT** | User interface for non-technical users |
| **HOW** | Upload document → Select language → View translation → Review flagged |
| **WHY** | Technicians and managers need simple interface |
| **NEXT (Phase 4)** | User acceptance testing with GGS team |

---

## The Flow: Phase 3 → Phase 4

```
Phase 3 Output              →    Phase 4 Input
─────────────────────────────────────────────────
Complete Pipeline           →    End-to-end Testing
API Endpoints               →    Load & Performance Testing
Quality Estimator           →    Threshold Calibration
Web UI                      →    User Acceptance Testing
Database                    →    Data Migration & Backup
```

---

## Key Risks & Mitigation

| Risk | Impact | Mitigation |
|------|--------|------------|
| PDF parsing failures | Broken input | Test with diverse GGS doc samples early |
| Slow API response | Poor UX | Async queue for large docs |
| UI not user-friendly | Low adoption | Involve GGS users in design |
| Quality scores inaccurate | Bad translations slip through | Calibrate with human feedback |

---

## Key Insight

> **Phase 3 is the BODY.**
> Phase 1 = Textbooks. Phase 2 = Brain. Phase 3 = Hands, eyes, mouth.
>
> Without integration, the smart model sits useless.
