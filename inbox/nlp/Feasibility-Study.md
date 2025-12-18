# NLP Project: Feasibility Study

> **Note:** Please refer to [[Project-Disclaimer]] for project context, expectations, and collaboration guidelines.
> **Related:** [[Student-Team-Budget-Analysis]] | [[Resource-Analysis]] | [[4-Month-Roadmap-Analysis]]

---

## Executive Summary

| Aspect | Assessment | Confidence |
|--------|------------|------------|
| **Technical Feasibility** | Feasible | High |
| **Operational Feasibility** | Feasible with training | Medium-High |
| **Schedule Feasibility** | Feasible for phased approach | Medium |
| **Resource Feasibility** | Feasible if GGS provides data | Medium |
| **Overall Recommendation** | **Proceed with phased language rollout** | - |

---

## 1. Technical Feasibility

### 1.1 Technology Stack Assessment

| Technology | Maturity | Student Familiarity | Risk |
|------------|----------|---------------------|------|
| **IndicTrans2** | Recent, Well-documented | None | Medium |
| **NLLB-200** | Mature (Meta) | None | Low |
| **PyTorch** | Mature, Industry Standard | Low-Medium | Low |
| **Hugging Face** | Mature, Excellent docs | Low | Low |
| **spaCy / NER** | Mature | Low | Low |
| **FastAPI** | Mature | Medium | Low |
| **GCP Vertex AI** | Mature | None | Medium |
| **PostgreSQL** | Mature | Medium | Low |

### 1.2 Technical Complexity Analysis

| Component | Complexity | Reason |
|-----------|------------|--------|
| Data Collection & Cleaning | **Medium** | Depends on GGS data quality |
| Parallel Corpus Curation | **Medium-High** | Sentence alignment, quality filtering |
| Model Fine-tuning | **High** | GPU resources, hyperparameter tuning |
| NER Integration | **Medium** | Pre-trained models available |
| Terminology Enforcement | **Medium** | Glossary lookup + post-processing |
| Quality Estimation (COMET) | **Medium** | Pre-built tools available |
| Backend API | **Low-Medium** | Standard REST patterns |
| Web UI | **Low-Medium** | File upload + review interface |
| MLOps / Deployment | **Medium-High** | Vertex AI learning curve |

### 1.3 Model Selection Analysis

| Model | Pros | Cons | Recommendation |
|-------|------|------|----------------|
| **IndicTrans2** | Best for Indian languages, open-source | Newer, less community support | **Primary choice** |
| **NLLB-200** | 200 languages, Meta-backed, robust | Generic, may need more fine-tuning | Fallback option |
| **mBART** | Good multilingual base | Older architecture | Not recommended |

### 1.4 Technical Feasibility Verdict

| Question | Answer |
|----------|--------|
| Can this be built with available technology? | **Yes** |
| Are pre-trained models available? | **Yes (IndicTrans2, NLLB-200)** |
| Can 3rd-year B.Tech students learn the stack? | **Yes, with 2-3 week ML bootcamp** |
| Can it achieve 85%+ accuracy? | **Yes, with sufficient training data** |
| Can it achieve 90%+ accuracy? | **Maybe — depends on data quality** |

**Technical Feasibility: FEASIBLE**

---

## 2. Operational Feasibility

### 2.1 Team Capability Assessment

| Role | Availability | Skill Gap | Training Needed |
|------|--------------|-----------|-----------------|
| Faculty Lead | 1 available | ML/NLP depth | GGS domain onboarding |
| NLP/ML Students | Need to recruit 4-5 | High | 3-4 weeks |
| Backend Students | Need to recruit 2 | Low-Medium | 1 week |
| Frontend Students | Need to recruit 1-2 | Medium | 1-2 weeks |
| DevOps/MLOps Students | Need to recruit 1-2 | High | 2 weeks |
| QA Students | Need to recruit 1 | Low | 1 week |

### 2.2 Operational Constraints

| Constraint | Impact | Mitigation |
|------------|--------|------------|
| Student ML knowledge gap | High initially | Front-load 2-week ML bootcamp |
| Academic schedule | Medium | Plan around exam calendar |
| GPU access coordination | Medium | GGS to provide dedicated instances |
| Part-time availability | Medium | Realistic sprint planning |
| Domain terminology learning | Medium | GGS glossary + domain sessions |

### 2.3 Operational Feasibility Verdict

| Question | Answer |
|----------|--------|
| Can SRM assemble the required team? | **Yes** |
| Can students learn NLP/ML in time? | **Yes, with structured bootcamp** |
| Can faculty guide ML project? | **Yes, if ML-experienced faculty assigned** |
| Can team coordinate with GGS effectively? | **Yes, with clear POC and weekly syncs** |

**Operational Feasibility: FEASIBLE (with structured training)**

---

## 3. Schedule Feasibility

### 3.1 Timeline Analysis (4 Months)

| Phase | Allocated | Realistic Need | Gap |
|-------|-----------|----------------|-----|
| ML Bootcamp (implicit) | 0 weeks | 2-3 weeks | **-2 to -3 weeks** |
| Month 1: Data Preparation | 4 weeks | 4-5 weeks | **-1 week** |
| Month 2: Model Development | 4 weeks | 5-6 weeks | **-1 to -2 weeks** |
| Month 3: System Integration | 4 weeks | 4 weeks | On track |
| Month 4: Testing & Deployment | 4 weeks | 3-4 weeks | On track |
| **Total Gap** | | | **-4 to -6 weeks** |

### 3.2 Schedule Risk Assessment

| Milestone | Risk Level | Dependency |
|-----------|------------|------------|
| Parallel corpora received from GGS | **Critical** | Blocks all training |
| Glossary/terminology database ready | **High** | Blocks post-processing |
| GPU instances available | **High** | Blocks model training |
| Model achieves target BLEU score | **Medium** | May need iteration |
| NER integration complete | **Medium** | Depends on entity lists |
| API + UI integration | **Low** | Standard development |
| UAT with GGS | **Medium** | Depends on reviewer availability |

### 3.3 Schedule Feasibility Verdict

| Question | Answer |
|----------|--------|
| Can full scope (4 languages) be delivered in 4 months? | **Risky** |
| Can core scope (2 languages) be delivered in 4 months? | **Yes** |
| Can phased approach (2 → 4 languages) work? | **Yes — recommended** |

**Schedule Feasibility: FEASIBLE (with phased approach)**

### 3.4 Recommended Phased Timeline

| Phase | Duration | Languages | Deliverable |
|-------|----------|-----------|-------------|
| **Month 1** | Weeks 1-4 | - | Data prep, glossary, corpus for Hindi + Tamil |
| **Month 2** | Weeks 5-8 | Hindi, Tamil | Fine-tuned models, NER integration |
| **Month 3** | Weeks 9-12 | Hindi, Tamil + start Telugu, Malayalam | API, UI, pipeline integration |
| **Month 4** | Weeks 13-16 | All 4 | Testing, deployment, UAT |

---

## 4. Resource Feasibility

### 4.1 SRM Resources Required

| Resource | Required | Available | Status |
|----------|----------|-----------|--------|
| Faculty Lead (ML-experienced) | 1 | TBD | To be assigned |
| B.Tech Students | 10-12 | TBD | To be recruited |
| Budget (Rs.) | 1.8L - 3.0L | TBD | To be approved |
| Lab/Workspace | Yes | TBD | To be confirmed |
| Local GPU (optional) | Nice to have | TBD | Not critical if GCP available |

### 4.2 GGS Resources Required (Dependencies)

| Resource | Required | Status | Blocker if Missing? |
|----------|----------|--------|---------------------|
| Parallel Corpora (50K+ pairs/language) | Week 1-2 | **Pending** | **Yes — Critical** |
| Automotive Glossary | Week 1-2 | **Pending** | **Yes — Critical** |
| Named Entity Lists | Week 2-3 | **Pending** | Yes |
| GCP GPU Access (A100/V100) | Week 3+ | **Pending** | **Yes — Critical** |
| Sample Documents (XML, PDF) | Week 1 | **Pending** | Yes |
| Human Reviewers | Month 3-4 | **Pending** | Yes (for QA loop) |
| Technical POC | Ongoing | **Pending** | Yes |
| Domain Expert (weekly) | Ongoing | **Pending** | Yes |

### 4.3 Data Requirements Deep Dive

| Language | Min Sentence Pairs | Ideal | GGS Status |
|----------|-------------------|-------|------------|
| Hindi | 50,000 | 100,000+ | TBD |
| Tamil | 50,000 | 100,000+ | TBD |
| Telugu | 50,000 | 100,000+ | TBD |
| Malayalam | 50,000 | 100,000+ | TBD |
| **Total** | **200,000** | **400,000+** | **TBD** |

### 4.4 Resource Feasibility Verdict

| Question | Answer |
|----------|--------|
| Are SRM resources sufficient? | **Yes, if budget approved** |
| Is data availability confirmed? | **No — critical action needed** |
| Is GPU access confirmed? | **No — action needed** |

**Resource Feasibility: FEASIBLE (pending GGS data confirmation)**

---

## 5. Risk Assessment Matrix

| Risk ID | Risk Description | Probability | Impact | Risk Score | Mitigation |
|---------|------------------|-------------|--------|------------|------------|
| R1 | Insufficient parallel corpora | Medium | Critical | **High** | Audit data in Week 1; adjust language count |
| R2 | GPU budget overrun | Medium | High | **High** | GGS to pre-allocate; use spot instances |
| R3 | Model quality below 85% | Medium | High | **Medium** | Start with 2 languages; iterate |
| R4 | Student ML learning curve | High | Medium | **Medium** | 2-week ML bootcamp before start |
| R5 | Terminology inconsistency | Medium | Medium | **Medium** | Build glossary first; enforce in pipeline |
| R6 | Scope creep (more languages) | Medium | Medium | **Medium** | Document Phase 1 scope formally |
| R7 | Human reviewer unavailability | Medium | Medium | **Medium** | Schedule reviewers early |
| R8 | Academic conflicts (exams) | High | Low | **Low** | Plan around exam schedule |
| R9 | Faculty ML expertise gap | Low | High | **Medium** | Assign ML-experienced faculty |
| R10 | GCP/Vertex AI learning curve | Medium | Medium | **Medium** | Dedicated MLOps student(s) |

---

## 6. Go/No-Go Criteria

### 6.1 Prerequisites for Project Start

| # | Prerequisite | Owner | Status |
|---|--------------|-------|--------|
| 1 | GGS confirms parallel corpora availability (min 50K/language) | GGS | Pending |
| 2 | GGS provides automotive glossary/terminology | GGS | Pending |
| 3 | GGS confirms GCP GPU budget allocation | GGS | Pending |
| 4 | GGS assigns technical POC | GGS | Pending |
| 5 | GGS confirms human reviewers for Month 3-4 | GGS | Pending |
| 6 | SRM budget approved | SRM | Pending |
| 7 | ML-experienced faculty lead assigned | SRM | Pending |
| 8 | Students recruited (min 10) | SRM | Pending |
| 9 | Phase 1 language scope agreed (2 languages) | Both | Pending |
| 10 | Quality targets agreed (BLEU, accuracy thresholds) | Both | Pending |

### 6.2 Go/No-Go Decision

| Condition | Decision |
|-----------|----------|
| All 10 prerequisites met | **GO** |
| Prerequisites 1-5 (GGS) not met | **NO-GO** |
| Prerequisites 6-8 (SRM) not met | **DELAY** |
| Prerequisites 9-10 not met | **NO-GO** |

---

## 7. Recommendations

### 7.1 For SRM

| # | Recommendation | Priority |
|---|----------------|----------|
| 1 | Assign ML-experienced faculty lead | Critical |
| 2 | Begin student recruitment (prioritize ML/CS students) | High |
| 3 | Plan 2-week ML/NLP bootcamp before project start | High |
| 4 | Confirm budget approval (Rs. 1.8L - 3.0L) | High |
| 5 | Check student exam schedules for conflicts | Medium |
| 6 | Identify students with prior PyTorch/ML exposure | Medium |

### 7.2 For GGS

| # | Recommendation | Priority |
|---|----------------|----------|
| 1 | Audit and confirm parallel corpora availability | Critical |
| 2 | Provide automotive glossary in structured format | Critical |
| 3 | Confirm GCP GPU budget (A100 instances are expensive) | Critical |
| 4 | Assign dedicated technical POC | High |
| 5 | Confirm human reviewer availability for Month 3-4 | High |
| 6 | Prioritize 2 languages for Phase 1 (recommend Hindi + Tamil) | High |
| 7 | Define acceptable BLEU/accuracy thresholds | High |
| 8 | Provide sample XML/PDF documents for testing | Medium |

### 7.3 Joint Recommendations

| # | Recommendation | Priority |
|---|----------------|----------|
| 1 | Conduct data audit meeting in Week 1 | Critical |
| 2 | Sign off on Phase 1 scope (2 languages) | High |
| 3 | Establish weekly sync cadence | High |
| 4 | Define quality metrics and acceptance criteria | High |
| 5 | Plan for continuous feedback loop with human reviewers | Medium |

---

## 8. Comparison: NLP vs 3D Wiring Project

| Factor | NLP Project | 3D Wiring Project |
|--------|-------------|-------------------|
| Duration | 4 months | 2 months |
| Team Size | 10-12 students | 8-10 students |
| SRM Budget | Rs. 1.8L - 3.0L | Rs. 1.2L - 2.1L |
| Technical Complexity | High (ML/NLP) | High (3D/CAD) |
| Learning Curve | Steeper (ML concepts) | Steep (3D tools) |
| Schedule Risk | **Medium** | **High** |
| Data Dependency | High (parallel corpora) | High (CAD files) |
| Pre-trained Models | Yes (IndicTrans2, NLLB) | No |
| Infrastructure Cost | Higher (GPU) | Lower (CPU-focused) |
| Overall Feasibility | **Higher** | **Lower** |

---

## 9. Conclusion

| Feasibility Dimension | Assessment | Notes |
|-----------------------|------------|-------|
| Technical | **Feasible** | Pre-trained models available, proven tech stack |
| Operational | **Feasible** | Team can be assembled; ML bootcamp needed |
| Schedule | **Feasible** | 4 months adequate for phased approach |
| Resource | **Feasible** | Pending GGS data and GPU confirmation |
| **Overall** | **Feasible** | Better positioned than 3D project |

### Final Recommendation

**PROCEED** with the project under the following conditions:

1. **Phased language rollout:** Hindi + Tamil first (Month 1-2), then Telugu + Malayalam (Month 3-4)
2. **GGS confirms parallel corpora availability** (min 50K sentence pairs per language)
3. **GGS confirms GPU budget allocation** for training
4. **2-week ML/NLP bootcamp** for students before project start
5. **Weekly sync meetings** with GGS technical POC
6. **Formal sign-off on Phase 1 scope and quality targets**
7. **Human reviewers scheduled** for Month 3-4 UAT

### Risk-Adjusted Success Probability

| Scope | Success Probability |
|-------|---------------------|
| 2 languages (Hindi + Tamil) at 85% accuracy | **75-80%** |
| 4 languages at 85% accuracy | **60-65%** |
| 4 languages at 90% accuracy | **40-50%** |

---

*Document Created: December 2024*
*Status: Draft for Review*
*Version: 1.0*
