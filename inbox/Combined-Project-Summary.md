# GGS-SRM Collaborative Projects: Combined Summary

> **Note:** Please refer to [[Project-Disclaimer]] for project context, expectations, and collaboration guidelines.

---

## Executive Summary

| Project | Duration | Students | SRM Budget | Feasibility | Schedule Risk |
|---------|----------|----------|------------|-------------|---------------|
| **NLP Translation** | 4 months | 10-12 | Rs. 1.8L - 3.0L | High | Medium |
| **3D Wiring** | 2 months | 8-10 | Rs. 1.2L - 2.1L | Medium | High |
| **Combined Total** | - | 18-22 | **Rs. 3.0L - 5.1L** | - | - |

---

## 1. Project Overview

### 1.1 NLP Multilingual Machine Translation System

| Attribute | Details |
|-----------|---------|
| **Objective** | Translate automotive technical docs (English → Indian languages) |
| **Target Languages** | Hindi, Tamil, Telugu, Malayalam, Kannada |
| **Key Deliverables** | Fine-tuned NMT model, Translation API, Web UI, Quality estimation |
| **Tech Stack** | IndicTrans2/NLLB-200, PyTorch, Hugging Face, FastAPI, GCP Vertex AI |
| **Project Owner** | Dr Karthikeyan Saminathan (GGS) |

### 1.2 3D Wiring Power Flow Automation Tool

| Attribute | Details |
|-----------|---------|
| **Objective** | Automate 3D wiring visualization for truck diagnostics |
| **Key Features** | DTC-driven routing, Power flow animation, Fault visualization |
| **Key Deliverables** | CAD pipeline, 3D routing engine, Authoring tool UI, MP4/WebGL export |
| **Tech Stack** | Blender, Pixyz, Unity, Three.js, FastAPI, GCP |
| **Project Owner** | D. Ravi (GGS) |

---

## 2. Timeline Comparison

```
NLP Project (4 months)
├── Month 1: Data Collection & Preparation
├── Month 2: Model Development & Fine-tuning
├── Month 3: System Integration & API
└── Month 4: Testing & Deployment

3D Wiring Project (2 months)
├── Month 1: Data Preparation & Framework
└── Month 2: 3D Engine & UI Development
```

| Factor | NLP Project | 3D Wiring Project |
|--------|-------------|-------------------|
| Total Duration | 4 months (16 weeks) | 2 months (8 weeks) |
| Training Buffer | 2-3 weeks (implicit) | 2-3 weeks (implicit) |
| Development Time | 10-12 weeks | 5-6 weeks |
| Testing Phase | 4 weeks (dedicated) | None (concurrent) |
| Timeline Pressure | **Moderate** | **High** |

---

## 3. Student Team Comparison

### 3.1 Team Size & Structure

| Role | NLP Project | 3D Wiring Project |
|------|-------------|-------------------|
| ML/NLP Engineers | 4-5 | - |
| 3D/CAD Developers | - | 3-4 |
| Backend Developers | 2 | 2 |
| Frontend Developers | 1-2 | 2 |
| DevOps/MLOps | 1-2 | 1 |
| QA/Testing | 1 | 1-2 |
| **Total Students** | **10-12** | **8-10** |
| Faculty Lead | 1 | 1 |

### 3.2 Skills Required

| Skill Area | NLP Project | 3D Wiring Project |
|------------|-------------|-------------------|
| **Primary Skills** | PyTorch, Hugging Face, NLP | Blender, Unity, Three.js |
| **Backend** | FastAPI, PostgreSQL | FastAPI, PostgreSQL |
| **Cloud** | GCP Vertex AI, MLOps | GCP Compute, Cloud Storage |
| **Learning Curve** | Steeper (ML concepts) | Steep (3D tools) |
| **Training Needed** | 3-4 weeks | 2-3 weeks |

---

## 4. Budget Comparison (SRM Side)

### 4.1 Detailed Budget Breakdown

| Item | NLP Project | 3D Wiring Project |
|------|-------------|-------------------|
| | Low / High | Low / High |
| **Students** | Rs. 1,00,000 / Rs. 1,80,000 | Rs. 80,000 / Rs. 1,50,000 |
| **Faculty** (per month) | Rs. 10-15K × 4 = Rs. 40-60K | Rs. 10-15K × 2 = Rs. 20-30K |
| **Misc** (per month) | Rs. 10-15K × 4 = Rs. 40-60K | Rs. 10-15K × 2 = Rs. 20-30K |
| **Total** | **Rs. 1,80,000 / Rs. 3,00,000** | **Rs. 1,20,000 / Rs. 2,10,000** |

### 4.2 Budget Summary

| Scenario | NLP | 3D Wiring | Combined |
|----------|-----|-----------|----------|
| **Conservative** | Rs. 1,80,000 | Rs. 1,20,000 | **Rs. 3,00,000** |
| **Moderate** | Rs. 2,40,000 | Rs. 1,65,000 | **Rs. 4,05,000** |
| **Ambitious** | Rs. 3,00,000 | Rs. 2,10,000 | **Rs. 5,10,000** |

### 4.3 Cost Per Month Analysis

| Project | Duration | Total Budget (Moderate) | Cost/Month |
|---------|----------|------------------------|------------|
| NLP | 4 months | Rs. 2,40,000 | Rs. 60,000 |
| 3D Wiring | 2 months | Rs. 1,65,000 | Rs. 82,500 |

> **Insight:** 3D Wiring has higher monthly burn rate due to compressed timeline.

---

## 5. GGS Responsibilities (Both Projects)

### 5.1 Infrastructure (GGS to Provide)

| Resource | NLP Project | 3D Wiring Project |
|----------|-------------|-------------------|
| **GPU Instances** | A100/V100 (training) | n2-highcpu-8 (rendering) |
| **Cloud Storage** | 500GB-1TB | 500GB-1TB |
| **Database** | Cloud SQL (PostgreSQL) | Cloud SQL (PostgreSQL) |
| **Specialized** | Vertex AI | Cloud CDN |

### 5.2 Software Licenses (GGS to Provide)

| Project | Required Licenses |
|---------|-------------------|
| NLP | GCP credits, Annotation tools (if needed) |
| 3D Wiring | **Pixyz** (Commercial - Critical), Unity Pro (if needed) |

### 5.3 Data & Assets (GGS to Provide)

| Project | Critical Data Needed |
|---------|---------------------|
| **NLP** | Parallel corpora (50K+ sentence pairs/language), Automotive glossary, Named entity lists |
| **3D Wiring** | CAD files (.JT, .FBX, .STEP), DTC database, Component metadata |

### 5.4 Human Resources (GGS to Provide)

| Resource | NLP Project | 3D Wiring Project |
|----------|-------------|-------------------|
| Technical POC | Required | Required |
| Domain Expert | Weekly calls | Weekly calls |
| Human Reviewers | Month 3-4 (translation QA) | Not required |
| Technical Review | Bi-weekly | Bi-weekly |

---

## 6. Feasibility Comparison

### 6.1 Feasibility Matrix

| Dimension | NLP Project | 3D Wiring Project |
|-----------|-------------|-------------------|
| Technical | **Feasible** | **Feasible** |
| Operational | **Feasible** (with training) | **Feasible** (with training) |
| Schedule | **Medium Risk** | **High Risk** |
| Resource | **Feasible** (pending data) | **Feasible** (pending CAD) |
| **Overall** | **Higher Confidence** | **Lower Confidence** |

### 6.2 Success Probability

| Scope | NLP Project | 3D Wiring Project |
|-------|-------------|-------------------|
| Full Scope | 50-60% | 30-40% |
| MVP Scope | 70-80% | 55-65% |
| PoC Only | 85-90% | 75-80% |

### 6.3 Why NLP Has Higher Feasibility

| Factor | NLP Advantage |
|--------|---------------|
| Timeline | 4 months vs 2 months (2x more time) |
| Pre-trained Models | IndicTrans2, NLLB-200 available |
| Testing Phase | Dedicated Month 4 for UAT |
| Iteration Buffer | Can start with 2 languages, expand |

---

## 7. Risk Comparison

### 7.1 Critical Risks

| Risk | NLP Impact | 3D Wiring Impact |
|------|------------|------------------|
| Data delay from GGS | **Critical** | **Critical** |
| Student learning curve | High | High |
| Scope creep | Medium | High |
| Timeline pressure | Medium | **Critical** |
| Quality targets not met | Medium | Medium |

### 7.2 Risk Mitigation Summary

| Mitigation | NLP | 3D Wiring |
|------------|-----|-----------|
| Pre-project bootcamp | 2-3 weeks ML training | 2-3 weeks 3D tools |
| Phased delivery | 2 languages → 4 languages | 1 vehicle, 15-20 DTCs |
| Weekly GGS syncs | Yes | Yes |
| Early data access | Week 1-2 | Week 1 |
| Scope documentation | MVP sign-off required | MVP sign-off required |

---

## 8. Go/No-Go Prerequisites

### 8.1 GGS Prerequisites (Both Projects)

| # | Prerequisite | NLP | 3D Wiring |
|---|--------------|-----|-----------|
| 1 | Technical POC assigned | Required | Required |
| 2 | Data/assets provided by Week 1 | Parallel corpora | CAD files + DTC data |
| 3 | Infrastructure access confirmed | GPU instances | Compute + Pixyz license |
| 4 | MVP scope signed off | Required | Required |
| 5 | Weekly sync commitment | Required | Required |

### 8.2 SRM Prerequisites (Both Projects)

| # | Prerequisite | NLP | 3D Wiring |
|---|--------------|-----|-----------|
| 1 | Budget approved | Rs. 1.8-3.0L | Rs. 1.2-2.1L |
| 2 | Faculty lead assigned | ML-experienced | 3D/Graphics-experienced |
| 3 | Students recruited | 10-12 | 8-10 |
| 4 | Pre-project bootcamp planned | 2-3 weeks | 2-3 weeks |

---

## 9. Recommendations

### 9.1 Project Prioritization

| Recommendation | Rationale |
|----------------|-----------|
| **Start NLP first** | Higher feasibility, longer runway, more buffer |
| **Stagger start dates** | Avoid resource competition |
| **Share backend students** | FastAPI/PostgreSQL skills overlap |

### 9.2 Recommended Approach by Project

| Project | Recommended Scope | Students | Budget |
|---------|-------------------|----------|--------|
| **NLP** | Phased: Hindi+Tamil first, then expand | 10-12 | Rs. 2.0-2.5L |
| **3D Wiring** | MVP: 1 vehicle, 15-20 DTCs, 2 animation types | 8-10 | Rs. 1.4-1.8L |

### 9.3 Combined Recommendations

| # | Recommendation | Priority |
|---|----------------|----------|
| 1 | Confirm GGS data availability before committing | **Critical** |
| 2 | Plan pre-project bootcamps for both teams | High |
| 3 | Assign ML-experienced faculty to NLP project | High |
| 4 | Request timeline extension for 3D Wiring (2 → 3 months) | High |
| 5 | Document MVP scope formally for both projects | High |
| 6 | Establish single GGS POC per project | High |
| 7 | Plan around student exam schedules | Medium |
| 8 | Consider shared backend team if timelines overlap | Medium |

---

## 10. Summary Dashboard

```
┌─────────────────────────────────────────────────────────────────┐
│                  GGS-SRM PROJECTS DASHBOARD                     │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  NLP TRANSLATION PROJECT                                        │
│  ════════════════════════                                       │
│  Duration:     ████████████████ 4 months                        │
│  Team:         ██████████████ 10-12 students                    │
│  Budget:       Rs. 1.8L - 3.0L                                  │
│  Feasibility:  ████████░░ HIGH                                  │
│  Risk:         ████░░░░░░ MEDIUM                                │
│                                                                 │
│  3D WIRING PROJECT                                              │
│  ═════════════════                                              │
│  Duration:     ████████ 2 months                                │
│  Team:         ██████████ 8-10 students                         │
│  Budget:       Rs. 1.2L - 2.1L                                  │
│  Feasibility:  ██████░░░░ MEDIUM                                │
│  Risk:         ████████░░ HIGH                                  │
│                                                                 │
│  COMBINED TOTALS                                                │
│  ═══════════════                                                │
│  Total Students:    18-22                                       │
│  Total Budget:      Rs. 3.0L - 5.1L                             │
│  Faculty Required:  2 (1 per project)                           │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

---

## 11. Next Steps

| # | Action Item | Owner | Timeline |
|---|-------------|-------|----------|
| 1 | Schedule kick-off meeting with GGS | SRM | This week |
| 2 | Confirm data availability (corpora, CAD files) | GGS | Before start |
| 3 | Get budget approval | SRM | Before start |
| 4 | Assign faculty leads | SRM | Before start |
| 5 | Begin student recruitment | SRM | Immediately |
| 6 | Plan bootcamp curriculum | SRM + Faculty | 2 weeks before start |
| 7 | Sign off on MVP scope documents | Both | Before start |
| 8 | Set up weekly sync schedule | Both | Week 1 |

---

## Related Documents

### NLP Project
- [[nlp/ps-nlp|Problem Statement]]
- [[nlp/Resource-Analysis|Resource Analysis]]
- [[nlp/4-Month-Roadmap-Analysis|Roadmap Analysis]]
- [[nlp/Student-Team-Budget-Analysis|Budget Analysis]]
- [[nlp/Feasibility-Study|Feasibility Study]]

### 3D Wiring Project
- [[3d-wiring/ps-3d-wiring|Problem Statement]]
- [[3d-wiring/Resource-Analysis|Resource Analysis]]
- [[3d-wiring/2-Month-Roadmap-Analysis|Roadmap Analysis]]
- [[3d-wiring/Student-Team-Budget-Analysis|Budget Analysis]]
- [[3d-wiring/Feasibility-Study|Feasibility Study]]

---

*Document Created: December 2024*
*Status: Draft for Review*
*Version: 1.0*
