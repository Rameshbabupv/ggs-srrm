# 3D Wiring Project: 2-Month Roadmap Analysis

> **Note:** Please refer to [[Project-Disclaimer]] for project context, expectations, and collaboration guidelines.

---

## Scope vs Timeline Reality Check

---

## Phase 1: Data Preparation & Framework (Month 1)

### What's Needed
- Set up CAD pipeline (Blender/Pixyz for .JT/.FBX/.STEP)
- Extract DTC metadata from service manuals
- Build component-to-wiring mapping database
- Create authoring tool framework (UI skeleton)

> **Reality Check:** Month 1 is achievable if GGS provides sample CAD files and DTC data early. CAD format compatibility is the biggest unknown.

---

## Phase 2: 3D Development & Authoring Tool (Month 2)

### What's Needed
- Build 3D routing engine (auto-trace wiring paths)
- Develop animation generator (power flow, fault blink)
- Complete authoring tool UI (drag-drop, preview, export)
- Multi-format export (MP4, WebGL, GLB)

> **Reality Check:** Month 2 is aggressive. Full authoring tool + animation engine in 4 weeks requires focused scope. May need to prioritize core features only.

---

## Scope vs Timeline Assessment

### Tight Spots

1. **CAD Complexity:** Large truck models = heavy files, slow processing
2. **Animation Types:** Supporting all 6 animation types in Month 2 is ambitious
3. **UI Polish:** Full drag-drop + timeline editor needs significant effort
4. **Testing Window:** No dedicated testing phase — must test as we build
5. **Student Learning:** Unity/Blender learning curve for new students

### What Fits<br><br>- CAD import pipeline (1-2 vehicle models)<br>- Basic DTC → wiring path mapping<br>- 2-3 animation types (power flow, fault blink)<br>- Simple authoring UI (select DTC, preview, export)<br>- MP4 + WebGL export

### What's At Risk

- Full timeline editor (may slip to post-launch)
- AR/VR export (prioritize web first)
- Multiple vehicle variants (start with 1)
- Advanced manual override features
- Complete testing coverage

---

## Timeline Fit Summary

| Phase       | Duration         | Risk Level                            |
| ----------- | ---------------- | ------------------------------------- |
| **Month 1** | Data + Framework | Medium - depends on data availability |
| **Month 2** | 3D Engine + UI   | High - aggressive feature set         |

---

## Recommendation

**To fit 2 months, prioritize:**

1. **Month 1 Week 1-2:** CAD pipeline with ONE sample vehicle model
2. **Month 1 Week 3-4:** DTC extraction for top 20 common error codes only
3. **Month 2 Week 1-2:** Routing engine + 2 animation types (power flow, fault)
4. **Month 2 Week 3-4:** Basic UI + MP4/WebGL export

**What to Defer:**
- Timeline editor → v2
- AR/VR export → v2
- Multiple vehicle models → v2
- Advanced animation types → v2

---

## MVP Definition

| Feature | In MVP | Deferred |
|---------|--------|----------|
| CAD import (1 model) | Yes | |
| DTC mapping (top 20) | Yes | |
| Power flow animation | Yes | |
| Fault blink animation | Yes | |
| Basic UI (select + preview) | Yes | |
| MP4 export | Yes | |
| WebGL export | Yes | |
| Timeline editor | | v2 |
| AR/VR export | | v2 |
| Multiple vehicles | | v2 |
| All animation types | | v2 |

---

## Key Insight

> **2 months = MVP only.**
> Focus on proving the concept works. Polish and scale come later.
>
> A working demo with 1 vehicle + 20 DTCs is better than an incomplete system with everything.
