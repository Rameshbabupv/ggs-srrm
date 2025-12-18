# NLP Project: Student Team Feasibility & Budget Analysis

> **Note:** Please refer to [[Project-Disclaimer]] for project context, expectations, and collaboration guidelines.
> **Related:** [[Resource-Analysis]] | [[4-Month-Roadmap-Analysis]]

---

## Key Constraints

| Factor | Details |
|--------|---------|
| **Duration** | 4 months (16 weeks) |
| **Student Level** | 3rd Year B.Tech |
| **Stipend Budget** | Rs. 10-15K per student |
| **Faculty Stipend** | Rs. 10-15K per month |
| **Misc Budget** | Rs. 10-15K per month |

---

## 1. Learning Curve Reality Check

Based on the Resource Analysis document, students need:

| Skill | Learning Time | Priority |
|-------|---------------|----------|
| PyTorch / Hugging Face | 2-3 weeks | High |
| IndicTrans2 / NLLB-200 | 1-2 weeks | High |
| spaCy / NER | 1-2 weeks | Medium |
| FastAPI | 1 week | High |
| GCP Vertex AI | 1-2 weeks | High |
| PostgreSQL | 1 week | Medium |
| React/Vue (UI) | 1-2 weeks | Medium |

**Reality:** Students need **4-6 weeks** to learn core ML/NLP skills. With 4 months available, **10-12 weeks** remain for development — more realistic than the 3D project.

---

## 2. Feasibility Assessment

### Is 4 months realistic? **Yes — for core scope**

| Scenario | Feasibility | Notes |
|----------|-------------|-------|
| Full scope (all 5 languages + all features) | **Challenging** | Aggressive but possible |
| Core scope (2-3 languages first) | **Yes** | Recommended approach |
| MVP (2 languages + basic pipeline) | **High confidence** | Safe baseline |

---

## 3. Proposed Student Team Structure

Based on the work breakdown:

| Role/Team | Students Needed | Key Skills | Responsibilities |
|-----------|-----------------|------------|------------------|
| **NLP/ML Team** | 4-5 | PyTorch, Hugging Face, NLP | Model fine-tuning, NER integration, evaluation |
| **Backend Team** | 2 | Python, FastAPI, PostgreSQL | API, pipeline integration, database |
| **Frontend Team** | 1-2 | React/Vue | Web UI for upload & review |
| **DevOps/MLOps** | 1-2 | GCP, Vertex AI, Docker | Cloud setup, CI/CD, deployment |
| **QA/Testing** | 1 | General | Testing, validation, UAT support |

**Total Students: 10-12**

**Faculty Role:** Technical lead, ML architecture guidance, code review, GGS coordination

---

## 4. Budget Estimate (SRM Institution Side)

| Item | Calculation | Low Estimate | High Estimate |
|------|-------------|--------------|---------------|
| Students (10-12) | 10 × Rs.10K to 12 × Rs.15K | Rs. 1,00,000 | Rs. 1,80,000 |
| Faculty Stipend | Rs. 10-15K × 4 months | Rs. 40,000 | Rs. 60,000 |
| Misc Expenses | Rs. 10-15K × 4 months | Rs. 40,000 | Rs. 60,000 |
| **Total (SRM Side)** | | **Rs. 1,80,000** | **Rs. 3,00,000** |

---

## 5. Client/Vendor (GGS) Responsibilities

The following costs and resources are to be provided by **GGS Information Services**:

### 5.1 Infrastructure (Cloud - GCP)

| Item | Specification | Purpose |
|------|---------------|---------|
| GPU Instances | A100 or V100 | Model training & fine-tuning |
| Vertex AI | Standard tier | Model serving & inference |
| Cloud SQL | PostgreSQL | Glossary, translation memory, logs |
| Cloud Storage | 500GB-1TB | Documents, models, datasets |
| Compute Engine | n2-standard-4 | API hosting |

### 5.2 Software & Tools

| Item | Type | Purpose |
|------|------|---------|
| GCP Credits | Cloud budget | Training, inference, storage |
| Annotation Tools | If needed | Data labeling platform access |
| Evaluation Tools | BLEU, COMET | Translation quality scoring |

### 5.3 Project Data & Assets

| Item | Details |
|------|---------|
| Parallel Corpora | 5-10 years of translated automotive documents |
| Domain Glossaries | Automotive terminology in target languages |
| Named Entity Lists | Part numbers, model names, brand names |
| Sample Documents | XML, PDF manuals for testing |
| Translation Memory | Previously approved translations |

### 5.4 Human Resources

| Item | Details |
|------|---------|
| Domain Expert Access | Weekly calls with GGS SME for terminology clarification |
| Human Reviewers | For translation QA and feedback loop |
| Technical POC | Single point of contact for technical queries |
| Technical Review | Bi-weekly review of deliverables |

### 5.5 Technical Support

| Item | Details |
|------|---------|
| Acceptance Criteria | Clear definition of quality targets (BLEU scores, accuracy) |
| Language Priority | Confirmation of which languages to prioritize |
| Data Format Specs | XML/DITA structure requirements |

---

## 6. Risk Factors

| Risk | Impact | Mitigation |
|------|--------|------------|
| Parallel corpora insufficient | High | Early data audit in Week 1-2 |
| GPU availability/cost overrun | High | GGS to pre-allocate budget |
| Model quality below target | Medium | Start with 2 languages, iterate |
| Student ML skill gap | Medium | Front-load ML bootcamp (2 weeks) |
| Student academic conflicts | Medium | Plan around exam schedule |
| Terminology inconsistency | Medium | Build glossary first (Month 1) |
| Scope creep (more languages) | Medium | Document Phase 1 languages clearly |

---

## 7. Recommended Approach

### Option A: Conservative (Recommended)

- **10 students** + 1 faculty
- **Focus:** Hindi + Tamil first, then expand
- **SRM Budget:** ~Rs. 1.8-2.2L
- **Deliverable:** Working translation system for 2 languages with 85%+ accuracy

### Option B: Ambitious

- **12 students** + 1 faculty
- **Focus:** All 4 languages (Hindi, Tamil, Telugu, Malayalam)
- **SRM Budget:** ~Rs. 2.4-3.0L
- **Risk:** Quality may suffer if spread too thin

### Option C: Phased Approach (Best Balance)

- **10-12 students** + 1 faculty
- **Month 1-2:** Hindi + Tamil (core pipeline)
- **Month 3-4:** Add Telugu + Malayalam (if on track)
- **SRM Budget:** ~Rs. 2.0-2.5L
- **Benefit:** De-risks delivery while allowing expansion

---

## 8. Critical Questions to Resolve with GGS

1. **Does GGS have sufficient parallel corpora?** (50K+ sentence pairs per language needed)
2. **Which 2 languages should be prioritized for Phase 1?** (Hindi + Tamil recommended)
3. **What is the acceptable accuracy threshold?** (90% target vs 85% realistic)
4. **Will GGS provide human reviewers for translation QA?**
5. **What is the GCP budget allocation for training?** (A100 GPUs are expensive)
6. **Who is the GGS technical POC for weekly syncs?**
7. **What document formats are priority?** (XML, PDF, Excel)
8. **Is there flexibility on the 4-month timeline?**

---

## 9. Summary: Cost Responsibility Matrix

| Category | SRM Responsibility | GGS Responsibility |
|----------|-------------------|-------------------|
| Student Stipends | Rs. 1.0L - 1.8L | |
| Faculty Stipend (4 months) | Rs. 40K - 60K | |
| Misc Expenses (4 months) | Rs. 40K - 60K | |
| **SRM Total** | **Rs. 1.8L - 3.0L** | |
| GCP Infrastructure (GPU, Vertex AI) | | ✓ |
| Cloud Storage & Database | | ✓ |
| Parallel Corpora & Glossaries | | ✓ |
| Human Reviewers for QA | | ✓ |
| Domain Expert Support | | ✓ |
| Annotation Tools (if needed) | | ✓ |

---

## 10. Comparison with 3D Wiring Project

| Factor | NLP Project | 3D Wiring Project |
|--------|-------------|-------------------|
| Duration | 4 months | 2 months |
| Team Size | 10-12 students | 8-10 students |
| SRM Budget | Rs. 1.8L - 3.0L | Rs. 1.2L - 2.1L |
| Technical Complexity | High (ML/NLP) | High (3D/CAD) |
| Learning Curve | Steeper (ML) | Steep (3D tools) |
| Schedule Risk | Medium | High |
| Data Dependency | High (corpora) | High (CAD files) |

---

*Document Created: December 2024*
*Status: Draft for Review*
*Version: 1.0*
