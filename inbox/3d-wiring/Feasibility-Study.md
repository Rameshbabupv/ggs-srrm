# 3D Wiring Project: Feasibility Study

> **Note:** Please refer to [[Project-Disclaimer]] for project context, expectations, and collaboration guidelines.
> **Related:** [[Student-Team-Budget-Analysis]] | [[Resource-Analysis]] | [[2-Month-Roadmap-Analysis]]

---

## Executive Summary

| Aspect | Assessment | Confidence |
|--------|------------|------------|
| **Technical Feasibility** | Feasible with constraints | Medium |
| **Operational Feasibility** | Feasible for MVP only | Medium |
| **Schedule Feasibility** | High Risk | Low |
| **Resource Feasibility** | Feasible if GGS provides dependencies | Medium |
| **Overall Recommendation** | **Proceed with MVP scope** | - |

---

## 1. Technical Feasibility

### 1.1 Technology Stack Assessment

| Technology | Maturity | Student Familiarity | Risk |
|------------|----------|---------------------|------|
| **Blender** | Mature, Open Source | Low (needs training) | Medium |
| **Unity 3D** | Mature, Industry Standard | Low-Medium | Medium |
| **Three.js** | Mature, Well-documented | Low | Medium |
| **FastAPI** | Mature, Python-based | Medium | Low |
| **PostgreSQL** | Mature | Medium | Low |
| **Pixyz** | Commercial, Specialized | None | High |
| **CAD Formats (.JT, .FBX, .STEP)** | Industry Standard | None | High |

### 1.2 Technical Complexity Analysis

| Component | Complexity | Reason |
|-----------|------------|--------|
| CAD Import Pipeline | **High** | Multiple formats, large files, optimization needed |
| DTC-to-Wiring Mapping | **Medium** | Database design + logic mapping |
| 3D Routing Engine | **High** | Auto-trace paths through 3D geometry |
| Animation Generation | **Medium-High** | Power flow, fault blink effects |
| Web UI (React + Three.js) | **Medium** | 3D viewer integration |
| Backend API | **Low-Medium** | Standard REST patterns |
| Export (MP4, WebGL) | **Medium** | Rendering pipeline |

### 1.3 Technical Feasibility Verdict

| Question | Answer |
|----------|--------|
| Can this be built with available technology? | **Yes** |
| Can 3rd-year B.Tech students learn the stack? | **Yes, with training** |
| Can it be built to production quality in 2 months? | **No — MVP only** |

**Technical Feasibility: FEASIBLE (for MVP scope)**

---

## 2. Operational Feasibility

### 2.1 Team Capability Assessment

| Role | Availability | Skill Gap | Training Needed |
|------|--------------|-----------|-----------------|
| Faculty Lead | 1 available | Domain knowledge | GGS onboarding |
| 3D/CAD Students | Need to recruit 3-4 | High | 2-3 weeks |
| Backend Students | Need to recruit 2 | Low-Medium | 1 week |
| Frontend Students | Need to recruit 2 | Medium | 1-2 weeks |
| QA/Integration | Need to recruit 1-2 | Low | 1 week |

### 2.2 Operational Constraints

| Constraint | Impact | Mitigation |
|------------|--------|------------|
| Student academic schedule | May lose productivity during exams | Plan around exam calendar |
| Part-time availability | Students may have 4-6 hrs/day max | Adjust expectations |
| No prior CAD experience | Slower initial progress | Front-load training |
| Remote collaboration | Communication overhead | Daily standups, shared tools |

### 2.3 Operational Feasibility Verdict

| Question | Answer |
|----------|--------|
| Can SRM assemble the required team? | **Yes** |
| Can students work effectively on this? | **Yes, with mentorship** |
| Can faculty manage the project? | **Yes, if single POC from GGS** |

**Operational Feasibility: FEASIBLE (with structured mentorship)**

---

## 3. Schedule Feasibility

### 3.1 Timeline Analysis

| Phase | Allocated | Realistic Need | Gap |
|-------|-----------|----------------|-----|
| Training/Onboarding | 0 weeks (implicit) | 2-3 weeks | **-2 to -3 weeks** |
| Month 1: Data & Framework | 4 weeks | 4-5 weeks | **-1 week** |
| Month 2: 3D Engine & UI | 4 weeks | 6-8 weeks | **-2 to -4 weeks** |
| Testing & QA | 0 weeks (implicit) | 2 weeks | **-2 weeks** |
| **Total Gap** | | | **-7 to -10 weeks** |

### 3.2 Schedule Risk Assessment

| Milestone | Risk Level | Dependency |
|-----------|------------|------------|
| CAD files received from GGS | **Critical** | Blocks all 3D work |
| Pixyz license available | **Critical** | Blocks CAD conversion |
| DTC data received | **High** | Blocks mapping logic |
| Student training complete | **High** | Blocks productive work |
| MVP feature complete | **High** | Compressed timeline |
| Testing complete | **Medium** | No dedicated phase |

### 3.3 Schedule Feasibility Verdict

| Question | Answer |
|----------|--------|
| Can full scope be delivered in 2 months? | **No** |
| Can MVP be delivered in 2 months? | **Maybe — high risk** |
| Can PoC be delivered in 2 months? | **Yes — with focus** |

**Schedule Feasibility: HIGH RISK**

### 3.4 Schedule Recommendation

| Option | Scope | Confidence |
|--------|-------|------------|
| **Option 1:** Extend to 3 months | Full MVP | High |
| **Option 2:** Keep 2 months | Reduced MVP (PoC+) | Medium |
| **Option 3:** Keep 2 months | Proof of Concept only | High |

---

## 4. Resource Feasibility

### 4.1 SRM Resources Required

| Resource | Required | Available | Status |
|----------|----------|-----------|--------|
| Faculty Lead | 1 | TBD | To be assigned |
| B.Tech Students | 8-10 | TBD | To be recruited |
| Budget (Rs.) | 1.2L - 2.1L | TBD | To be approved |
| Lab/Workspace | Yes | TBD | To be confirmed |

### 4.2 GGS Resources Required (Dependencies)

| Resource | Required | Status | Blocker if Missing? |
|----------|----------|--------|---------------------|
| CAD Files (1 vehicle) | Week 1 | **Pending** | **Yes — Critical** |
| DTC Database | Week 1 | **Pending** | **Yes — Critical** |
| Pixyz License | Week 1 | **Pending** | **Yes — Critical** |
| GCP Access | Week 2 | **Pending** | Yes |
| Technical POC | Ongoing | **Pending** | Yes |
| Domain Expert (weekly) | Ongoing | **Pending** | Yes |

### 4.3 Resource Feasibility Verdict

| Question | Answer |
|----------|--------|
| Are SRM resources sufficient? | **Yes, if budget approved** |
| Are GGS dependencies clearly defined? | **Yes** |
| Are GGS dependencies confirmed? | **No — action needed** |

**Resource Feasibility: FEASIBLE (pending GGS confirmations)**

---

## 5. Risk Assessment Matrix

| Risk ID | Risk Description | Probability | Impact | Risk Score | Mitigation |
|---------|------------------|-------------|--------|------------|------------|
| R1 | CAD data delayed from GGS | Medium | Critical | **High** | Get commitment for Week 1 delivery |
| R2 | Pixyz license not available | Medium | Critical | **High** | Confirm before project start |
| R3 | Student learning curve longer than expected | High | High | **High** | Add 1-week bootcamp before start |
| R4 | Scope creep from GGS | Medium | High | **Medium** | Document MVP scope formally |
| R5 | Student dropouts mid-project | Low | Medium | **Low** | Recruit 1-2 buffer students |
| R6 | Faculty unavailable | Low | Critical | **Medium** | Identify backup faculty |
| R7 | Academic conflicts (exams) | High | Medium | **Medium** | Plan around exam schedule |
| R8 | Technical blockers in 3D routing | Medium | High | **Medium** | Weekly GGS technical reviews |

---

## 6. Go/No-Go Criteria

### 6.1 Prerequisites for Project Start

| # | Prerequisite | Owner | Status |
|---|--------------|-------|--------|
| 1 | GGS provides sample CAD files | GGS | Pending |
| 2 | GGS provides DTC database | GGS | Pending |
| 3 | GGS confirms Pixyz license access | GGS | Pending |
| 4 | GGS assigns technical POC | GGS | Pending |
| 5 | SRM budget approved | SRM | Pending |
| 6 | Faculty lead assigned | SRM | Pending |
| 7 | Students recruited (min 8) | SRM | Pending |
| 8 | MVP scope documented and signed off | Both | Pending |

### 6.2 Go/No-Go Decision

| Condition | Decision |
|-----------|----------|
| All 8 prerequisites met | **GO** |
| Prerequisites 1-4 (GGS) not met | **NO-GO** |
| Prerequisites 5-7 (SRM) not met | **DELAY** |
| Prerequisite 8 not met | **NO-GO** |

---

## 7. Recommendations

### 7.1 For SRM

| # | Recommendation | Priority |
|---|----------------|----------|
| 1 | Begin student recruitment immediately | High |
| 2 | Identify and assign faculty lead | High |
| 3 | Plan 1-week pre-project bootcamp | High |
| 4 | Confirm budget approval | High |
| 5 | Check student exam schedules for conflicts | Medium |

### 7.2 For GGS

| # | Recommendation | Priority |
|---|----------------|----------|
| 1 | Provide sample CAD files before project start | Critical |
| 2 | Confirm Pixyz license access | Critical |
| 3 | Provide DTC database extract | Critical |
| 4 | Assign dedicated technical POC | High |
| 5 | Document and agree on MVP acceptance criteria | High |
| 6 | Consider timeline extension to 10-12 weeks | Medium |

### 7.3 Joint Recommendations

| # | Recommendation | Priority |
|---|----------------|----------|
| 1 | Conduct kick-off meeting with all stakeholders | High |
| 2 | Sign off on MVP scope document | High |
| 3 | Establish weekly sync cadence | High |
| 4 | Define clear escalation path | Medium |

---

## 8. Conclusion

| Feasibility Dimension | Assessment | Notes |
|-----------------------|------------|-------|
| Technical | **Feasible** | Technology exists, skills can be learned |
| Operational | **Feasible** | Team can be assembled with training |
| Schedule | **High Risk** | 2 months is aggressive; MVP only |
| Resource | **Feasible** | Pending GGS confirmations |
| **Overall** | **Conditionally Feasible** | Proceed with MVP scope + risk mitigation |

### Final Recommendation

**PROCEED** with the project under the following conditions:

1. **Scope limited to MVP/PoC** (1 vehicle, 15-20 DTCs, 2 animation types)
2. **GGS provides all dependencies by Week 1**
3. **1-week pre-project bootcamp** for students
4. **Weekly sync meetings** with GGS technical POC
5. **Formal MVP sign-off** before work begins

---

*Document Created: December 2024*
*Status: Draft for Review*
*Version: 1.0*
