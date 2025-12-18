# NLP Project - Resource Analysis

*Focus on team structure and infrastructure needs*

---

## 1. Team Resources

| Role | Count | Responsibility |
|------|-------|----------------|
| NLP/ML Engineer (Senior) | 1 | Model architecture, fine-tuning strategy |
| NLP/ML Engineer (Mid) | 2 | Training, NER integration, evaluation |
| Backend Developer | 1 | FastAPI, database, pipeline integration |
| Frontend Developer | 1 | Web UI for upload & review |
| DevOps/MLOps | 1 | GCP setup, CI/CD, deployment |
| QA Engineer | 1 | Testing, validation, UAT support |
| Project Manager | 1 (part-time) | Coordination, stakeholder management |
| **Total Team** | **8** | |

---

## 2. Infrastructure Requirements (GCP)

| Resource | Specification | Purpose |
|----------|--------------|---------|
| GPU Instances | A100 or V100 | Model training & fine-tuning |
| Vertex AI | Standard tier | Model serving & inference |
| Cloud SQL | PostgreSQL | Glossary, translation memory, logs |
| Cloud Storage | 500GB-1TB | Documents, models, datasets |
| Compute Engine | n2-standard-4 | API hosting |

---

## 3. Data & Tools

| Item | Purpose |
|------|---------|
| Data Annotation | Parallel corpus curation (if gaps exist) |
| Human Reviewers | Translation QA, feedback loop |
| Evaluation Tools | BLEU, COMET scoring |

---

## 4. Resource Allocation by Phase

| Phase | Duration | Key Resources |
|-------|----------|---------------|
| **Month 1** - Data Prep | 4 weeks | 2 ML Engineers + PM |
| **Month 2** - Model Dev | 4 weeks | Full ML team + Heavy GPU |
| **Month 3** - Integration | 4 weeks | Backend + Frontend + DevOps |
| **Month 4** - Testing | 4 weeks | QA + DevOps + PM |

---

## 5. Skills Matrix

| Skill | Priority | Phase Needed |
|-------|----------|--------------|
| IndicTrans2 / NLLB-200 | High | Month 2 |
| PyTorch / Hugging Face | High | Month 2-3 |
| spaCy / NER | Medium | Month 2 |
| FastAPI | High | Month 3 |
| GCP Vertex AI | High | Month 3-4 |
| PostgreSQL | Medium | Month 3 |
| React/Vue (UI) | Medium | Month 3 |
