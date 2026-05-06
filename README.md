# PanelEngine
Revit panel fabrication tool (demo)
# PanelEngine

**Revit Panel Fabrication Tool (Demo Build)**

---

## Overview

PanelEngine is a Revit add-in that generates fabrication-ready panel families with controlled geometry and a stable constraint system.

This tool demonstrates a workflow that bridges **design → fabrication**, allowing panels to be:

* Generated parametrically
* Flattened for fabrication
* Exported as CNC-ready geometry

---

## Key Features

✔ Generate triangle and rectangle panels as Revit families
✔ Automatic family naming and loading into the project
✔ Flange system with fabrication-aware offsets
✔ Flatten toggle for panel layout (fabrication view)
✔ CNC export (DXF) from flattened geometry

---

## Demo Workflow

1. Open Revit

2. Go to:
   **Add-Ins → External Tools → PanelEngine**

3. Create a panel:

   * Enter panel name
   * Define dimensions
   * Set flange depth

4. Place the panel in the model

5. Toggle:

   * `Flattened = TRUE` → view flat pattern

6. Click:

   * **Export CNC** → generates DXF file

---

## Installation

### Step 1

Download the latest demo build from **Releases**

---

### Step 2

Extract the folder to:

```text
C:\PanelEngine\
```

---

### Step 3

Copy the file:

```text
PanelEngine.addin
```

to:

```text
C:\ProgramData\Autodesk\Revit\Addins\2027\
```

---

### Step 4

Open Revit and launch:

```text
Add-Ins → External Tools → PanelEngine
```

---

## Notes

* This is a **demo version** focused on workflow validation
* Panels are created as **Generic Model families**
* Flattening simulates fabrication layout (not full bend allowance yet)
* Geometry is structured to avoid common Revit constraint failures

---

## Technical Approach

PanelEngine uses a controlled geometry hierarchy:

```text
Panel (triangle/rectangle)
    ↓
Reference edges
    ↓
Offset reference lines (fabrication spacing)
    ↓
Flanges (dependent geometry)
```

This prevents:

* circular constraints
* geometry conflicts
* instability during edits

---

## Future Development

Planned extensions include:

* True bend allowance (K-factor support)
* Automated nesting for sheet layouts
* Expanded panel library system
* Direct fabrication integration

---

## Author

Developed as part of an exploration into improving fabrication workflows within Revit.

---

## Demo

*(Optional: add screenshot or short video here)*

---

## Summary

PanelEngine demonstrates how Revit can move beyond modeling and begin supporting **fabrication-ready workflows with controlled, reliable geometry**.
