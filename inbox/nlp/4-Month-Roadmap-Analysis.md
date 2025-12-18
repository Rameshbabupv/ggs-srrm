# NLP Project: 4-Month Roadmap Analysis

## Scope vs Timeline Reality Check

---

## Phase 1: Data Collection & Preparation (Month 1)

### What's Needed
- Gather 5-10 years parallel English-Indian language docs from GGS
- Curate 50K+ sentence pairs per language (4 languages = ~200K pairs total)
- Build automotive terminology glossary (ECU, ABS, torque specs, etc.)
- Create NER lexicon for part numbers, model names

> **Reality Check:** Month 1 is tight if data isn't already organized. Assumes GGS has existing translated materials.

---

## Phase 2: Model Development (Month 2)

### What's Needed
- Select base model (IndicTrans2 or NLLB-200)
- Fine-tune on automotive corpus for 4 languages
- Integrate NER component (spaCy/BERT)
- Target: BLEU score > 40

> **Reality Check:** Standard NMT fine-tuning takes 2-3 weeks per language. 4 languages in 1 month = aggressive but doable with parallel GPU training.

---

## Phase 3: System Integration (Month 3)

### What's Needed
- Pre/post-processor pipeline
- Quality estimator (COMET-QE confidence scoring)
- FastAPI endpoints (batch + real-time)
- PostgreSQL glossary + translation memory setup
- Web UI for upload & review

> **Reality Check:** Core pipeline can be built in 3-4 weeks. UI refinement is often the bottleneck.

---

## Phase 4: Testing & Deployment (Month 4)

### What's Needed
- Manual QA review (10% sample)
- Performance testing (target: 60 sec/doc)
- GCP Vertex AI deployment
- Documentation + UAT with stakeholders

> **Reality Check:** Testing is compressed. Real UAT typically needs 2-3 weeks minimum.

---

## Scope vs Timeline Assessment

### Tight Spots

1. **Language Coverage:** 4 languages at launch = acceptable, but means less time per language
2. **Quality Targets:** 90% accuracy is ambitious for Month 2 fine-tuning—may need Month 3 refinement
3. **Testing Window:** Only 1 month for UAT + optimization is compressed
4. **Continuous Learning:** Active learning loop may not mature fully by Month 4

### What Fits

- Core NMT pipeline (4 languages)
- Terminology enforcement layer
- Quality estimation + confidence scoring
- FastAPI + GCP deployment
- Basic UI for document upload

### What's At Risk

- Real-time translation mode (may slip to post-launch)
- Multi-format output options (prioritize XML/PDF first)
- Advanced continuous learning loop (basic version only)
- Comprehensive documentation

---

## Recommendation

**To fit 4 months, prioritize:**

1. **Month 1:** Focus on Hindi + Tamil (higher demand). Skip Telugu/Malayalam for Phase 1.
2. **Month 2:** Achieve 85%+ accuracy for 2 languages (lower bar than 90%).
3. **Month 3:** Expand to Telugu/Malayalam if time allows.
4. **Month 4:** Deploy with 2-3 languages; Phase 2 adds remaining languages.

**Alternative:** Keep all 4 languages but reduce quality targets to 85% across the board.
