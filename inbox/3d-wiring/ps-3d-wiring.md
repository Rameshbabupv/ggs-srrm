# Problem Statement: 3D Wiring Power Flow Automation Tool

## For Automobile Domain Technical Documentation

**Document Version:** 1.0
**Date:** 16 December 2025
**Project Domain:** 3D Wiring Power Flow Automation – Authoring Tool
**Target Industry:** Automotive Aftermarket / Commercial Vehicles
**Project Owner:** D. Ravi, 9500017732, ravi.dharmarajan@ggsinc.com
## 1. Objective

The primary objective of 3D wiring flow is to automate the end-to-end 3D wiring routing inside the truck chassis based on real electrical power flow and sensor/control signal distribution, ensuring accurate wiring paths through engine, transmission, cabin, chassis frame, and dashboard, displayed in 360-degree view.

The process of generating metadata for electric circuit 3D flow visualizations is highly manual, time-consuming, error-prone, and dependent on subject matter experts. There is no unified system that automatically reads engineering data (2D schematics, CAD, DTC logs) and converts it into structured metadata for animation engines.

### 1.1 Specific Objectives

1. To create an Automated 3D Wiring Routing based on diagnostic procedure.
2. The complete wiring path (highlighted in yellow in the 3D harness) from ECU/connector → sensors → actuators across the entire truck chassis.
3. Exact routing of harnesses based on CAD geometry with hotspots.

### 1.2 Purpose

The purpose of the system is to provide 3D visualization based on real-world electrical power/signal flow from main connectors to truck sensors and actuators. Automate routing of wiring inside the truck chassis structure. Highlight faulty paths → affected harness → connected components automatically. Provide real-time diagnostic visualization based on troubleshooting procedure/error code. When a diagnostic trouble code (DTC) is selected, the system will automatically trace the wiring path and show power flow direction with highlighted faulty segments inside the truck.

### 1.3 Existing Problems in 3D Wiring Power Flow

- Engineers interpret circuit and flow diagrams manually
- 2D electrical diagrams and 3D CAD wiring models are isolated
- Metadata like "start node → end node → animation colour → timing" is created manually
- Current, voltage, and signal propagation paths must be manually defined
- 3D Animation power flow created manually
- No automation for DTC/Error cases

## 2. Proposed System

Replace manual animation creation with metadata-driven automation.

### 2.1 Expected Automation Capabilities

1. **Extract circuit metadata from 2D drawings**
   - OCR/shape detection for components
   - Auto-identify connections & signal directions
   - Convert into structured JSON/XML metadata

2. **Generate 3D wiring metadata**
   - Auto-map logical nodes to physical CAD points
   - Auto-generate flow paths over 3D harness
   - Define animation timing and colour rules

3. **Support multiple flow types**
   - Power flow
   - Grounding flow
   - Fault flow
   - Reverse flow
   - Sequential component activation

4. **Generate metadata for animation engines**
   - Unity
   - WebGL
   - SCORM-based HTML5 animation
   - Web/AR/VR/MR

### 2.2 Key Features of Proposed System

1. **Automated Error-Code Driven Circuit Mapping**
   - Auto-reads diagnostic error codes (DTCs)
   - Automatically maps DTC → component → wiring circuit → 3D model
   - Generates the affected path tree instantly without manual tracing

2. **Dynamic Wiring Data Integration**
   - Auto-sync connector IDs, pin mapping, wire specs, harness IDs, circuit metadata
   - Ensures 3D model and wiring database remain aligned

3. **Automated Power Flow Animation Generation**
   - Auto-create power-flow highlights and path animations
   - Fault point blink
   - Blockage/break animation
   - Fuse blow/relay click
   - Sensor location view

4. **Interactive Authoring Tool Interface**
   - Drag-and-drop circuit selection
   - Timeline editor with auto-populated steps
   - CAD Component browser linked to error codes
   - One-click preview of generated animation
   - Allows minor manual refinements if needed

5. **Real-Time Data Validation and Error Checking**
   - Detects missing metadata or broken circuit paths
   - Validates consistency between CAD and wiring data
   - Provides auto-generated error logs
   - Ensures animation logic is correct before export

6. **Multi-Format Output Generation**
   - MP4 rendered videos
   - WebGL/HTML5 interactive modules
   - GLB/FBX 3D packages

7. **Complete Version Control & Data Sync**
   - Tracks changes in wiring metadata or CAD models
   - Maintains historical versions for audit purposes

8. **High Performance & Scalability**
   - Handles large CAD models efficiently
   - Optimised runtime pipeline for fast regeneration
   - Supports multiple vehicle variants and platforms
### 2.3 Use Case

- Generate metadata for the overall diagnostic workflow
- Structure data based on model selection and corresponding DTC codes
- Map CAD harness, sensors, ECU, relays, and other components to their respective part numbers
- Extract and build a step-by-step troubleshooting procedure for both DTC and Non-DTC scenarios
- Organize technical content according to the troubleshooting flow, including images, circuit diagrams, and activities
- Automatically identify the error or defect location
- Automatically generate the 3D wiring flow
- Display the complete troubleshooting sequence integrated with the 3D wiring flow
- Solution deployable on web/AR platforms

## 3. Expected Results

### 3.1 Input Specifications

| Input Type       | Description                                                        |
| ---------------- | ------------------------------------------------------------------ |
| Source Documents | PDF manuals, Text documents, Images                                |
| CAD File         | .JT, .FBX, .STL, .STEP                                             |
| Domain Lexicons  | 3D Wiring Power Flow Automation – Authoring Tool (Web Application) |
| Excel Document   | DTC error codes, aggregates, probable causes, etc.                 |

### 3.2 Expected Output & Project KPIs

A complete set of authoring tools or platforms capable of developing a 3D Wiring Flow Automation solution.

The solution should support the full workflow described in the DTC troubleshooting process—including:
- CAD import
- Automatic routing
- Sensor hotspots
- Rule-based wiring
- DTC validation
- Output generation
## 4. Tentative Technology Stack

| Category | Technology | Purpose |
|----------|-----------|---------|
| Blender | .JT, .FBX, STL, .STEP | CAD Validation |
| Pixyz | JT, .FBX, STL, .STEP | Poly count optimization and file conversion |
| Maya / Blender | .FBX / .STEP | To creating the 3D power flow for routing and mounting |
| Unity | .glb | 3D Viewer / Front end |
| Backend API | FastAPI / Flask | Data full & push API service |
| Cloud Platform | Google Cloud Platform (Vertex AI) | Model training, deployment, MLOps |
| Data Storage | PostgreSQL / Cloud SQL | 3D content and technical content |
![[Pasted image 20251217133602.png]]
![[Pasted image 20251217133621.png]]
## 5. Project Timeline

The project is planned across two phases over a 2-month duration:

| Phase | Duration | Key Deliverables |
|-------|----------|------------------|
| Phase 1 | Month 1 | Data Collection & Preparation: Metadata creation, authoring tool framework |
| Phase 2 | Month 2 | 3D Wiring Power Flow Development: Base model selection, automotive domain fine-tuning |

## 6. Conclusion

The proposed 3D Wiring Power Flow & Diagnostic Automation Authoring Tool delivers a unified, intelligent, and scalable framework for modern vehicle diagnostics, harness visualization, and automated troubleshooting. By integrating CAD data, DTC logic, component metadata, wiring rules, and real-time error localization into a single automated pipeline, the system transforms traditionally manual and time-consuming diagnostic processes into a fully automated, rule-driven, and visually interactive workflow.

The architecture ensures that every stage—from data ingestion to 3D wiring flow generation—operates with high accuracy and consistency. Using advanced metadata generation, CAD–part number mapping, and rule-based routing, the system automatically creates clear, technician-friendly step-by-step procedures enriched with 3D animations, circuit diagrams, and AR/Web visualizations. This drastically reduces human effort, eliminates interpretation errors, and enhances diagnostic precision.

---

**Prepared By:** Ravi D
**Date:** _______________

**Approved By:**
**Date:** _______________
