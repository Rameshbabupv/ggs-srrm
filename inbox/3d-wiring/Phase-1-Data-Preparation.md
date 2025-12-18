# 3D Wiring - Phase 1: Data Preparation & Framework (Month 1)

> **Note:** Please refer to [[Project-Disclaimer]] for project context, expectations, and collaboration guidelines.

---

## In Simple Terms - What Are We Doing?

Building the "knowledge base" for the system. Before we can auto-generate 3D animations, we need to teach the system:
- What components exist
- How they connect (wiring paths)
- What each error code means
- Where everything sits in the 3D model

---

## The 4 Core Tasks

| Task | What | How | Why | Next (Phase 2) |
|------|------|-----|-----|----------------|
| **CAD Pipeline Setup** | Import & process 3D models | Blender/Pixyz ingests .JT/.FBX/.STEP | Foundation for all 3D work | 3D routing uses these models |
| **DTC Metadata Collection** | Map error codes to components | Extract from service manuals, Excel sheets | System needs to know "P0301 = Cylinder 1 Misfire" | Drives auto-tracing logic |
| **Component Mapping** | Link parts to wiring paths | Build: DTC → Component → Circuit → 3D location | Core intelligence of the system | Enables auto-animation |
| **Authoring Tool Framework** | Basic UI skeleton | Web app structure, drag-drop foundation | Users need interface to interact | Full UI in Phase 2 |

---

## The Data We Need

| Data Type | Source | Format | Purpose |
|-----------|--------|--------|---------|
| CAD Models | GGS/OEM | .JT, .FBX, .STEP | 3D visualization base |
| DTC Codes | Service manuals | Excel/PDF | Error → component mapping |
| Wiring Diagrams | 2D schematics | PDF/Images | Circuit path extraction |
| Component List | Parts catalog | Excel/CSV | Part numbers, locations |
| Connector/Pin Data | Wiring specs | Excel | Pin mapping, wire IDs |

---

## Before vs After Automation

| Activity | Manual (Weeks) | Automated (Days) |
|----------|----------------|------------------|
| CAD file conversion | 2-3 weeks | 2-3 days |
| DTC extraction from PDFs | 3-4 weeks | 1 week |
| Component mapping | 4-6 weeks | 1-2 weeks |
| Wiring path tracing | 2-3 weeks | 3-5 days |

---

## What LLM/AI Can Do in Phase 1

| Task | AI Role | Human Role |
|------|---------|------------|
| **DTC Extraction** | Read PDFs, extract error codes & descriptions | Verify accuracy |
| **Component Identification** | Parse manuals, identify parts & relationships | Validate mappings |
| **Wiring Path Parsing** | OCR 2D diagrams, extract node connections | Review & correct |
| **Metadata Generation** | Auto-create JSON/XML structure | Approve format |

---

## Deep Dive: What → How → Why → Next

### Task 1: CAD Pipeline Setup

| Question | Answer |
|----------|--------|
| **WHAT** | System to import, optimize, and prepare 3D models |
| **HOW** | Blender/Pixyz imports → poly reduction → Unity-ready export (.glb) |
| **WHY** | Raw CAD files too heavy, wrong format for web/AR |
| **NEXT (Phase 2)** | Optimized models feed into 3D routing engine |

---

### Task 2: DTC Metadata Collection

| Question | Answer |
|----------|--------|
| **WHAT** | Database of all error codes with component links |
| **HOW** | LLM extracts from service manuals → structured JSON → human review |
| **WHY** | "P0301" means nothing to system without context |
| **NEXT (Phase 2)** | DTC triggers auto-trace of affected circuit |

---

### Task 3: Component Mapping

| Question | Answer |
|----------|--------|
| **WHAT** | Relationship database: DTC → Component → Circuit → 3D Location |
| **HOW** | Parse wiring diagrams + parts catalog → build graph structure |
| **WHY** | This IS the brain - connects error to visual |
| **NEXT (Phase 2)** | Mapping drives animation generation |

---

### Task 4: Authoring Tool Framework

| Question | Answer |
|----------|--------|
| **WHAT** | Web-based UI skeleton for content creators |
| **HOW** | React/Vue frontend + FastAPI backend scaffold |
| **WHY** | Users need interface, not command line |
| **NEXT (Phase 2)** | Full drag-drop, preview, export features |

---

## Suggested Phase 1 Flow

```
Week 1: CAD Pipeline (Blender/Pixyz setup, test imports)
        ↓
Week 2: DTC Extraction (LLM parses service docs)
        ↓
Week 3: Component Mapping (Build relationship graph)
        ↓
Week 4: Authoring Framework (Basic UI + API scaffold)
```

---

## The Flow: Phase 1 → Phase 2

```
Phase 1 Output              →    Phase 2 Input
─────────────────────────────────────────────────
Optimized CAD Models        →    3D Routing Engine
DTC Metadata Database       →    Auto-Trace Logic
Component-Wiring Graph      →    Animation Generator
UI Framework                →    Full Authoring Tool
```

---

## Key Risks & Mitigation

| Risk | Impact | Mitigation |
|------|--------|------------|
| CAD files incompatible | Delays | Test with sample files early |
| DTC docs poorly structured | Bad extraction | Manual backup for critical codes |
| Wiring data incomplete | Gaps in mapping | Flag gaps, prioritize common circuits |
| Students new to 3D tools | Learning curve | Blender tutorials, mentor support |

---

## Key Insight

> **Phase 1 is the KNOWLEDGE BASE.**
> No data = No automation. Garbage data = Garbage animations.
>
> Phase 2 builds the engine, but Phase 1 provides the fuel.
