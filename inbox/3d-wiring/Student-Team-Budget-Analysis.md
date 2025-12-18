# 3D Wiring Project: Student Team Feasibility & Budget Analysis

> **Note:** Please refer to [[Project-Disclaimer]] for project context, expectations, and collaboration guidelines.

---

## Key Constraints

| Factor | Details |
|--------|---------|
| **Duration** | 2 months (8 weeks) |
| **Student Level** | 3rd Year B.Tech |
| **Stipend Budget** | Rs. 10-15K per student |
| **Faculty Stipend** | Rs. 10-15K per month |
| **Misc Budget** | Rs. 10-15K per month |

---

## 1. Learning Curve Reality Check

From the Resource Analysis document, students need:

| Skill | Learning Time | Priority |
|-------|---------------|----------|
| Blender basics | 1-2 weeks | High |
| Unity fundamentals | 1-2 weeks | High |
| Three.js | 1 week | High |
| CAD file handling (Pixyz) | 3-5 days | High |
| FastAPI | 1 week | High |
| React | 1 week | Medium |

**Problem:** If students need **3-4 weeks** to learn basics, only **4-5 weeks** remain for actual development.

---

## 2. Feasibility Assessment

### Is 2 months realistic? **Conditionally Yes — but only for MVP**

| Scenario | Feasibility | Notes |
|----------|-------------|-------|
| Full scope (all features) | **No** | Even professionals rated this "High Risk" |
| MVP scope (1 vehicle, 20 DTCs) | **Maybe** | Tight, needs parallel workstreams |
| Proof of Concept | **Yes** | Demonstrate core flow works |

---

## 3. Proposed Student Team Structure

Based on the work breakdown:

| Role/Team | Students Needed | Key Skills | Responsibilities |
|-----------|-----------------|------------|------------------|
| **3D/CAD Team** | 3-4 | Blender, Unity | CAD import, 3D routing, animation |
| **Backend Team** | 2 | Python, FastAPI, PostgreSQL | API, DTC metadata, database |
| **Frontend Team** | 2 | React, Three.js | Web UI, 3D viewer integration |
| **Integration/QA** | 1-2 | General | Testing, documentation, deployment |

**Total Students: 8-10**

**Faculty Role:** Technical lead, architecture decisions, unblocking students, code review

---

## 4. Budget Estimate (SRM Institution Side)

| Item | Calculation | Low Estimate | High Estimate |
|------|-------------|--------------|---------------|
| Students (8-10) | 8 × Rs.10K to 10 × Rs.15K | Rs. 80,000 | Rs. 1,50,000 |
| Faculty Stipend | Rs. 10-15K × 2 months | Rs. 20,000 | Rs. 30,000 |
| Misc Expenses | Rs. 10-15K × 2 months | Rs. 20,000 | Rs. 30,000 |
| **Total (SRM Side)** | | **Rs. 1,20,000** | **Rs. 2,10,000** |

---

## 5. Client/Vendor (GGS) Responsibilities

The following costs and resources are to be provided by **GGS Information Services**:

### 5.1 Infrastructure (Cloud)

| Item | Specification | Purpose |
|------|---------------|---------|
| GCP Compute Engine | n2-highcpu-8 | CAD processing, rendering |
| Cloud Storage | 500GB-1TB | CAD files, 3D models, exports |
| Cloud SQL | PostgreSQL | DTC metadata, component mappings |
| Cloud Run | Standard | API hosting, backend services |
| Cloud CDN | Standard | Serve WebGL/video content |

### 5.2 Software Licenses

| Software | Type | Purpose |
|----------|------|---------|
| **Pixyz** | Commercial License | CAD optimization (.JT/.STEP conversion) |
| Unity Pro (if needed) | Commercial License | Advanced 3D features |
| Any proprietary tools | As required | Per project needs |

### 5.3 Hardware & Development Environment

| Item | Specification | Purpose |
|------|---------------|---------|
| Development Workstations | 32GB RAM, RTX 3060+ GPU | If students lack capable machines |
| OR Cloud Dev Environments | GPU-enabled VMs | Remote development option |

### 5.4 Project Data & Assets

| Item | Details |
|------|---------|
| Sample CAD Files | .JT, .FBX, .STEP files for 1 vehicle model |
| DTC Database | Error codes, descriptions, wiring mappings |
| Service Manual Excerpts | Reference documentation for troubleshooting flows |
| Component Metadata | Part numbers, connector IDs, pin mappings |

### 5.5 Technical Support

| Item | Details |
|------|---------|
| Domain Expert Access | Weekly calls with GGS SME for clarifications |
| Technical Review | Bi-weekly review of deliverables |
| Acceptance Criteria | Clear definition of MVP acceptance |

---

## 6. Risk Factors

| Risk | Impact | Mitigation |
|------|--------|------------|
| Learning curve too steep | High | Pre-training bootcamp (1 week before project starts) |
| Student academic conflicts | Medium | Buffer time, exam-aware scheduling |
| CAD data delay from GGS | High | Get sample files in Week 1 |
| Scope creep | High | Stick strictly to MVP definition |
| Communication gaps | Medium | Weekly sync calls with GGS |

---

## 7. Recommended Approach

### Option A: Conservative (Recommended)

- **8 students** + 1 faculty
- **Focus:** Proof of Concept — 1 vehicle, 10-15 DTCs, 2 animation types
- **SRM Budget:** ~Rs. 1.2-1.4L
- **Deliverable:** Working demo that proves the concept

### Option B: Ambitious

- **10-12 students** + 1 faculty
- **Focus:** Full MVP — 1 vehicle, 20 DTCs, all basic features
- **SRM Budget:** ~Rs. 1.7-2.1L
- **Risk:** Higher chance of incomplete delivery

---

## 8. Critical Questions to Resolve with GGS

1. **Will GGS provide Pixyz license access?** (Critical for CAD conversion)
2. **Will GGS provide sample CAD files by Week 1?** (Blocks all 3D work)
3. **Will GGS provide cloud dev environments?** (If students lack hardware)
4. **Who is the GGS technical POC for weekly syncs?**
5. **What are the exact acceptance criteria for MVP?**
6. **Is there flexibility on the 2-month timeline?** (Even 1-2 week buffer helps)

---

## 9. Summary: Cost Responsibility Matrix

| Category | SRM Responsibility | GGS Responsibility |
|----------|-------------------|-------------------|
| Student Stipends | Rs. 80K-1.5L | |
| Faculty Stipend (2 months) | Rs. 20-30K | |
| Misc Expenses (2 months) | Rs. 20-30K | |
| **SRM Total** | **Rs. 1.2L - 2.1L** | |
| GCP Infrastructure | | ✓ |
| Software Licenses (Pixyz, Unity) | | ✓ |
| Hardware/Dev Machines | | ✓ |
| CAD Files & Data | | ✓ |
| Domain Expert Support | | ✓ |

---

*Document Created: December 2024*
*Status: Draft for Review*
