# **Unit 1 — Introduction to Structural Systems**

- [Load – types and their assessment](#1-load-types--assessment)
- [Types of supports](#2-types-of-supports)
- [Concept and types of structures – cables, trusses, beams, arches, frames](#3-concept--types-of-structures)
- [Statical determinacy](#4-statical-determinacy)
- [Identification of determinate & indeterminate structures (Degree of Redundancy)](#5-determinacy-via-degree-of-redundancy)

<a id="1-load-types--assessment"></a>
## **1. Load — Types & Assessment**

Loads are external forces applied to a structure that produce internal stresses & deformations.

### **1.1 Classification of Loads**

| Type | Description | Typical Symbol | Assessment Basis |
|---|---|---|---|
| **Dead Load (DL)** | Permanent self-weight of structure & non-removable fixtures | \( W_d \) | Unit weight × Volume |
| **Live Load (LL)** | Occupancy & usage loads | \( W_l \) | IS 875 Part 2 provisions |
| **Wind Load (WL)** | Pressure due to wind actions | \( W_w \) | IS 875 Part 3 calculations |
| **Snow Load (SL)** | Accumulated snow weight | \( W_s \) | IS 875 Part 4 |
| **Seismic Load (EL)** | Earthquake-induced inertia forces | \( W_e \) | IS 1893 spectral method |
| **Impact Load** | Sudden or shock loading | — | Impact coefficients |
| **Temperature Load** | Thermal expansion/contraction | — | \( \Delta T \), restraint condition based |

📌 *Image Placeholder:* *Load types (DL, LL, WL, EL)*  
`![Load Types Diagram](images/load_types_placeholder.png)`

### **1.2 Load Assessment (as per IS)**
Assessment involves:
- **Magnitude estimation** (unit weight, density)
- **Distribution** (point load, UDL, UVL, moment)
- **Load combinations** (as per IS 456 / IS 875)

Example: **Design Load = DL + LL × Load Factor**

<a id="2-types-of-supports"></a>
## **2. Types of Supports**

Supports resist external loads by providing reaction forces.

### **2.1 Classification**

| Support Type | Restraints Provided | Reactions | Example |
|---|---|---|---|
| **Pinned/Hinged** | Resists translation but **not rotation** | \( R_x, R_y \) | Beam ends, frames |
| **Roller** | Resists **one direction translation** only | \( R_y \) | Expansion joints |
| **Fixed** | Resists translation & rotation | \( R_x, R_y, M \) | Encased column |

📌 *Image Placeholder:* *Support symbols*  
`![Support Types Diagram](images/support_types_placeholder.png)`

<a id="3-concept--types-of-structures"></a>
## **3. Concept & Types of Structures**

A **structure** is a system designed to resist applied loads safely.

### **3.1 Classification by Form**

| Structural Form | Behavior | Usage |
|---|---|---|
| **Cables** | Pure tension | Suspension bridges |
| **Trusses** | Axial forces only | Roof trusses, bridges |
| **Beams** | Bending & shear | Floors, girders |
| **Arches** | Compression dominant | Masonry bridges |
| **Frames** | Axial + Bending + Shear | Multi-storey buildings |

📌 *Image Placeholder:* *Structural forms overview*  
`![Structural Forms Diagram](images/forms_placeholder.png)`

<a id="4-statical-determinacy"></a>
## **4. Statical Determinacy**

A structure is **statically determinate** if internal forces & reactions can be found by **equilibrium equations alone**.

### **4.1 Equilibrium Conditions**
For 2D:
\[
\sum F_x = 0,\quad \sum F_y = 0,\quad \sum M = 0
\]

<a id="5-determinacy-via-degree-of-redundancy"></a>
## **5. Determinacy via Degree of Redundancy (DoR)**

### **5.1 Rule for Determinacy**
Degree of Static Indeterminacy (DSI):

For **beams/frames (2D):**
\[
DSI = r + m - 3j
\]

Where:  
`r = external reactions`, `m = internal members`, `j = joints`

### **5.2 Comparison**

| Characteristic | Determinate | Indeterminate |
|---|---|---|
| Unknowns ≤ Equations | ✔ | ✖ |
| Solved by equilibrium only | ✔ | ✖ (needs compatibility) |
| Analysis methods | Simple | Matrix/energy methods |
| Effect of temp./support settlement | No internal force | Causes internal forces |
| Stiffness influence | No | Yes |
| Safety | Predictable | Ductile |

[⮝ Go to Top](#-unit-1-—-introduction-to-structural-systems)
