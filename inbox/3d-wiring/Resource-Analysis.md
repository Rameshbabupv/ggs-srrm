# 3D Wiring Project - Resource Analysis

> **Note:** Please refer to [[Project-Disclaimer]] for project context, expectations, and collaboration guidelines.

*Focus on team structure and infrastructure needs*

---
## 1. Team Resources

| **Role**              | **Count**     | **Responsibility**                                 |
| --------------------- | ------------- | -------------------------------------------------- |
| 3D Developer (Senior) | 1             | Architecture, CAD pipeline, Unity/Blender strategy |
| 3D Developer (Mid)    | 2             | Modeling, animation, routing engine                |
| Backend Developer     | 1             | FastAPI, database, metadata engine                 |
| Frontend Developer    | 1             | Authoring tool UI (React + Three.js)               |
| DevOps                | 1             | GCP setup, CI/CD, deployment                       |
| QA Engineer           | 1 (part-time) | Testing, validation                                |
| Project Manager       | 1 (part-time) | Coordination, stakeholder management               |
| **Total Team**        | **8**         |                                                    |

---

## 2. Infrastructure Requirements (GCP)

| Resource | Specification | Purpose |
|----------|--------------|---------|
| Compute Engine | n2-highcpu-8 | CAD processing, rendering |
| Cloud Storage | 500GB-1TB | CAD files, 3D models, exports |
| Cloud SQL | PostgreSQL | DTC metadata, component mappings |
| Cloud Run | Standard | API hosting, backend services |
| Cloud CDN | Standard | Serve WebGL/video content |

---

## 3. Software & Tools

| Tool | Purpose | License |
|------|---------|---------|
| Blender | CAD import, poly reduction | Free/Open Source |
| Pixyz | CAD optimization (.JT/.STEP) | Commercial |
| Unity | 3D viewer, animation, export | Free tier available |
| Three.js | Web-based 3D viewer | Free/Open Source |
| FFmpeg | Video rendering (MP4) | Free/Open Source |
| FastAPI | Backend API | Free/Open Source |

---

## 4. Resource Allocation by Phase

| Phase | Duration | Key Resources |
|-------|----------|---------------|
| **Month 1** - Data & Framework | 4 weeks | 2 3D Devs + Backend + PM |
| **Month 2** - 3D Engine & UI | 4 weeks | Full team (3D + Frontend + DevOps) |

---

## 5. Skills Matrix

| Skill | Priority | Phase Needed |
|-------|----------|--------------|
| Blender / Maya | High | Month 1-2 |
| Unity 3D | High | Month 2 |
| Three.js / WebGL | High | Month 2 |
| CAD formats (.JT, .FBX, .STEP) | High | Month 1 |
| Python scripting | Medium | Month 1-2 |
| FastAPI | High | Month 1-2 |
| React | Medium | Month 2 |
| PostgreSQL | Medium | Month 1 |
| FFmpeg | Low | Month 2 |

---

## 6. Student Learning Requirements

| Skill Gap | Learning Resource | Time Needed |
|-----------|-------------------|-------------|
| Blender basics | Blender Guru tutorials | 1-2 weeks |
| Unity fundamentals | Unity Learn platform | 1-2 weeks |
| Three.js | Three.js Journey course | 1 week |
| CAD file handling | Pixyz documentation | 3-5 days |

---

## 7. Hardware Recommendations (Local Dev)

| Component | Minimum | Recommended |
|-----------|---------|-------------|
| RAM | 16 GB | 32 GB |
| GPU | GTX 1660 | RTX 3060+ |
| Storage | 256 GB SSD | 512 GB SSD |
| CPU | i5 / Ryzen 5 | i7 / Ryzen 7 |
