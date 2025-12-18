# 3D Wiring - Phase 2: 3D Development & Authoring Tool (Month 2)

> **Note:** Please refer to [[Project-Disclaimer]] for project context, expectations, and collaboration guidelines.

---

## In Simple Terms - What Are We Doing?

Building the "engine" that turns Phase 1 data into magic. We take the CAD models, DTC mappings, and wiring data — and create a system that automatically generates 3D animations showing power flow and faults.

---

## The 4 Core Tasks

| Task | What | How | Why | Next (Post-Launch) |
|------|------|-----|-----|-------------------|
| **3D Routing Engine** | Auto-trace wiring paths in 3D | Algorithm maps circuit data to CAD geometry | No manual path drawing | Continuous refinement |
| **Animation Generator** | Create power flow visuals | Rule-based animation: flow, blink, highlight | Visual troubleshooting | Add more animation types |
| **Authoring Tool UI** | Full editing interface | Drag-drop, timeline, preview, export | Users create content easily | Feature enhancements |
| **Output Exporter** | Multi-format delivery | MP4, WebGL, GLB, AR-ready packages | Content reaches end users | Add more formats |

---

## Animation Types to Support

| Type | Visual Effect | Use Case |
|------|---------------|----------|
| **Power Flow** | Yellow/green pulse along wire | Show current path |
| **Fault Flow** | Red blink at failure point | Identify problem location |
| **Grounding Flow** | Blue flow to ground | Trace ground connections |
| **Blockage Animation** | X mark, stopped flow | Show broken circuit |
| **Fuse Blow** | Flash + break visual | Indicate fuse failure |
| **Sequential Activation** | Step-by-step highlight | Training/learning mode |

---

## Authoring Tool Features

| Feature | Description | Priority |
|---------|-------------|----------|
| **DTC Selector** | Dropdown to pick error code | Must Have |
| **3D Viewport** | Interactive model viewer (rotate, zoom) | Must Have |
| **Path Highlighter** | Click component → see wiring path | Must Have |
| **Timeline Editor** | Control animation sequence | Should Have |
| **Preview Mode** | Play animation before export | Must Have |
| **Export Options** | Choose output format | Must Have |
| **Manual Override** | Tweak auto-generated paths | Nice to Have |

---

## Technology Choices

| Component | Options | Recommendation |
|-----------|---------|----------------|
| **3D Viewer** | Unity / Three.js / Babylon.js | **Unity** for AR/VR, **Three.js** for web-only |
| **Animation Engine** | Unity Animator / Custom scripts | **Unity Animator** + custom triggers |
| **UI Framework** | React / Vue + WebGL | **React** + Three.js for web authoring |
| **Backend** | FastAPI / Flask | **FastAPI** (async, fast) |
| **Export Pipeline** | Blender scripts / Unity export | **Unity** for .glb, **FFmpeg** for MP4 |

---

## Deep Dive: What → How → Why → Post-Launch

### Task 1: 3D Routing Engine

| Question | Answer |
|----------|--------|
| **WHAT** | Algorithm that auto-traces wiring in 3D space |
| **HOW** | Phase 1 graph data + CAD coordinates → pathfinding algorithm |
| **WHY** | Manual tracing takes weeks; auto-trace takes seconds |
| **POST-LAUNCH** | Improve accuracy, handle edge cases |

---

### Task 2: Animation Generator

| Question | Answer |
|----------|--------|
| **WHAT** | System that creates visual effects along wiring paths |
| **HOW** | Rule engine: DTC type → animation style → timing → render |
| **WHY** | Technicians need visual cues to understand problems |
| **POST-LAUNCH** | Add more animation styles, custom effects |

---

### Task 3: Authoring Tool UI

| Question | Answer |
|----------|--------|
| **WHAT** | Web interface for creating/editing 3D content |
| **HOW** | React frontend + 3D viewport + timeline + export panel |
| **WHY** | Non-technical users need intuitive interface |
| **POST-LAUNCH** | User feedback → UI improvements |

---

### Task 4: Output Exporter

| Question | Answer |
|----------|--------|
| **WHAT** | Multi-format export pipeline |
| **HOW** | Unity exports .glb → FFmpeg renders MP4 → WebGL packages |
| **WHY** | Different users need different formats (web, mobile, AR) |
| **POST-LAUNCH** | Add SCORM, more AR formats |

---

## Suggested Phase 2 Flow

```
Week 1: 3D Routing Engine (pathfinding + CAD integration)
        ↓
Week 2: Animation Generator (power flow, fault blink)
        ↓
Week 3: Authoring Tool UI (full interface, preview)
        ↓
Week 4: Output Exporter + Testing (MP4, WebGL, GLB)
```

---

## System Architecture

```
┌─────────────────────────────────────────────────────┐
│                  Authoring Tool UI                   │
│  ┌─────────┐  ┌─────────┐  ┌─────────┐  ┌────────┐ │
│  │   DTC   │  │   3D    │  │Timeline │  │ Export │ │
│  │Selector │  │Viewport │  │ Editor  │  │ Panel  │ │
│  └─────────┘  └─────────┘  └─────────┘  └────────┘ │
└─────────────────────────────────────────────────────┘
                         │
                         ▼
┌─────────────────────────────────────────────────────┐
│                   Backend (FastAPI)                  │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐ │
│  │   Routing   │  │  Animation  │  │   Export    │ │
│  │   Engine    │  │  Generator  │  │  Pipeline   │ │
│  └─────────────┘  └─────────────┘  └─────────────┘ │
└─────────────────────────────────────────────────────┘
                         │
                         ▼
┌─────────────────────────────────────────────────────┐
│                    Data Layer                        │
│  ┌─────────┐  ┌─────────┐  ┌─────────┐  ┌────────┐ │
│  │   CAD   │  │   DTC   │  │ Wiring  │  │ Output │ │
│  │ Models  │  │Metadata │  │  Graph  │  │ Files  │ │
│  └─────────┘  └─────────┘  └─────────┘  └────────┘ │
└─────────────────────────────────────────────────────┘
```

---

## Output Formats

| Format | Use Case | Delivery |
|--------|----------|----------|
| **MP4** | Embedded in manuals, offline viewing | Download/embed |
| **WebGL/HTML5** | Interactive web modules | Browser-based |
| **GLB/FBX** | 3D packages for further editing | 3D software |
| **AR-Ready** | Mobile AR experience | ARCore/ARKit |

---

## Key Risks & Mitigation

| Risk | Impact | Mitigation |
|------|--------|------------|
| Complex CAD geometry | Slow rendering | Aggressive poly reduction |
| Animation performance | Laggy preview | Optimize shaders, LOD |
| Export quality issues | Bad output | Test early, iterate |
| Students new to Unity | Learning curve | Tutorials, pair programming |

---

## Success Criteria

| Metric | Target |
|--------|--------|
| Auto-routing accuracy | ≥ 90% correct paths |
| Animation render time | ≤ 30 seconds |
| UI usability | Complete task without help |
| Export success rate | 100% valid files |

---

## Key Insight

> **Phase 2 is the ENGINE.**
> Phase 1 gave the fuel (data). Phase 2 builds the machine that runs on it.
>
> Input: DTC code → Output: Ready-to-use 3D animation
