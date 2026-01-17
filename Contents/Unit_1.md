<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    tex2jax: {
      inlineMath: [ ['$','$'], ["\\(","\\)"] ],
      processEscapes: true
    }
  });
</script>
    
<script type="text/javascript"
        src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>

## Unit 1: Introduction to Structural Systems

### Index
- [Load – Types and Their Assessment](#load--types-and-their-assessment)
- [Types of Supports](#types-of-supports)
- [Concept and Types of Structures](#concept-and-types-of-structures)
- [Statical Determinacy](#statical-determinacy)
- [Identification of Determinate and Indeterminate Structures based on degree of redundancy (DoR)](#identification-of-determinate-and-indeterminate-structures-based-on-degree-of-redundancy-dor)

## Load – Types and Their Assessment

A *load* is any external action causing internal forces, deformation, or displacement in a structure.

Loads must be properly identified and assessed for safe design as per relevant IS codes.

### Classification of Loads

| Load Type | Description | Examples | Assessment Basis |
|---|---|---|---|
| **Dead Load (DL)** | Permanent, due to self-weight (Material density × volume) | RCC slab, walls, finishes | IS 875 Part 1 |
| **Live Load (LL)** | Movable and occupancy-related | People, furniture | IS 875 Part 2 |
| **Wind Load (WL)** | Pressure due to wind action | Wind on buildings | IS 875 Part 3 |
| **Snow Load (SL)** | Weight of snow deposition | Himalayan structures | IS 875 Part 4 |
| **Seismic Load (EL)** | Inertial load due to earthquakes | Base shear | IS 1893 |
| **Thermal Load** | Due to temperature variations | Expansion/Contraction | $\sigma_t = E\,\alpha\,\Delta T$ |
| **Impact / Dynamic Load** | Sudden or shock loads | Crane loads, traffic | Impact factor |


<img width="659" height="406" alt="image" src="https://github.com/user-attachments/assets/1887507b-3563-480e-bb9e-d6e69b39da12" />

*Fig: Classification of Loads commonly acting on structures*


### Load Idealization (For Analysis)

Loads acting on physical structures are idealized into mathematically convenient forms to facilitate structural analysis. Idealization permits the conversion of actual distributed, concentrated, or dynamic actions into simpler equivalent load systems without significantly altering their analytical effect.

Common idealized load forms include:

* **Concentrated Load / Point Load (P)**
  Represents a load applied over a very small area idealized as acting at a single point. Used to model wheel loads, machine loads, or localized forces.

* **Uniformly Distributed Load (UDL or w)**
  Load uniformly spread over a length, having constant intensity (e.g., floor loads, self-weight of beams).

* **Uniformly Varying Load (UVL or Linearly Varying Load)**
  Load varying linearly along the span, commonly triangular or trapezoidal in nature (e.g., soil pressure on retaining walls, wind pressure on tapered elements).

* **Triangular Load** (Special case of UVL)
  Zero at one end and maximum at the other; equivalent point load acts at one-third the base from the larger intensity end.

* **Trapezoidal Load**
  Combination of two triangular components; arises in cases such as wind pressure with height.

* **Moment Load (M)**
  Represents a couple applied to a member creating pure rotational effect (seen at fixed ends or due to applied torques).

* **Combined Load Systems**
  Real structures may experience a combination of point loads + UDL + UVL. Superposition is applied to handle such cases in analysis.


#### Comparison Table of Load Idealization Forms

| Idealization    | Shape              | Equivalent Point Load         | Point of Action from Larger End |
| --------------- | ------------------ | ----------------------------- | ------------------------------- |
| UDL             | Constant rectangle | $wL$                          | $L/2$                           |
| Triangular UVL  | Linear wedge       | $\frac{1}{2}w_{max}L$         | $L/3$                           |
| Trapezoidal UVL | Frustum shape      | Sum of rectangle + triangular | Depends on components           |
| Point Load      | Single spike       | —                             | At point of application         |
| Pure Moment     | Couple             | —                             | Causes rotation only            |

<img width="526" height="517" alt="image" src="https://github.com/user-attachments/assets/65e34136-581e-48c9-abc7-a22c9ed8c362" />

*Fig: Load idealization formats used in analysis*

### Load Combinations (as per IS codes)

In structural analysis, different types of loads may act simultaneously. Therefore, appropriate **load combinations** are considered while evaluating structural response. IS 875 (Part 5) provides recommended combinations for gravity and lateral loads.

Typical combinations include:

* ( DL + LL )
* ( DL + WL )
* ( DL + LL + WL )
* ( DL + EL )
* ( DL + LL + EL )

> **Note:** Wind Load (WL) and Earthquake Load (EL) are treated as independent lateral load cases and are **not combined together** for conventional building design, as both represent rare extreme events.

### Summary Table

| Load Type                | Variation   | Duration       | Source                | Code Reference   |
| ------------------------ | ----------- | -------------- | --------------------- | ---------------- |
| **Dead Load (DL)**       | Constant    | Permanent      | Self-weight, finishes | IS 875 Part 1    |
| **Live Load (LL)**       | Variable    | Temporary      | Occupancy, usage      | IS 875 Part 2    |
| **Wind Load (WL)**       | Directional | Short-duration | Atmospheric action    | IS 875 Part 3    |
| **Earthquake Load (EL)** | Dynamic     | Instantaneous  | Ground motion         | IS 1893 (Part 1) |

## Types of Supports

Supports provide constraints against motion, causing reaction forces.

### Support Types & Reaction Characteristics

| Type of Support | Restrained DoF | Reactions Generated | Notes |
|---|---|---|---|
| **Fixed** | $u_x, u_y, \theta$ | $R_x, R_y, M$ | No movement or rotation |
| **Pinned/Hinged** | $u_x, u_y$ | $R_x, R_y$ | Rotation free |
| **Roller** | $u_y$ | $R_y$ | Allows expansion |
| **Link Support** | Along link axis | Single reaction | Used in trusses |

<img width="591" height="357" alt="image" src="https://github.com/user-attachments/assets/5eb2cd79-4edf-414d-9a26-49e576fd2e81" />

*Fig: Common support symbols used in analysis*

## Concept and Types of Structures

A *structure* is a connected system designed to resist loads safely without excessive deformation.

### Classification Based on Form and Force Mechanism

| Structural Form | Load Carrying Mechanism | Internal Forces | Examples |
|---|---|---|---|
| **Cable** | Pure tension | Tension only | Suspension bridges |
| **Truss** | Axial actions | Tension/Compression | Roof trusses |
| **Beam** | Bending action | Bending + Shear | Floors, girders |
| **Arch** | Compression thrust | Compression + Thrust | Masonry arches |
| **Frame** | Combined action | Axial + Shear + Bending | Buildings, portals |

📌 **Image Placeholder:**  
`![Structural Forms](images/structural_forms_placeholder.png)`  
*Fig: Different structural systems based on load transfer*

## Statical Determinacy

A structure is **statically determinate** if all unknown reactions and internal forces can be obtained using only the **equilibrium equations**.

For a 2D system, available equilibrium equations are:

$$ \sum F_x = 0, \quad \sum F_y = 0, \quad \sum M = 0 $$

If more unknowns exist than available equations, structure is **statically indeterminate**.

### **Difference Between Statically Determinate and Statically Indeterminate Structures**

| **Statically Determinate Structure**                                                        | **Statically Indeterminate Structure**                                                                   |
| ------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| Forces and reactions can be determined using **equilibrium equations alone**                | Forces and reactions require **equilibrium + compatibility conditions** and force–displacement relations |
| Number of unknown reactions/internal forces is **equal to** number of equilibrium equations | Number of unknowns is **greater than** the number of equilibrium equations                               |
| Internal forces and reactions are **independent of material properties** (E, I, A)          | Internal forces and reactions **depend on stiffness and material properties** (E, I, A)                  |
| **No additional internal forces** develop due to support settlements or temperature changes | **Secondary internal forces** develop due to support settlements and thermal strains                     |
| **No structural redundancy**; failure of one member may lead to mechanism                   | **Has redundancy**, offering alternative load paths and enhanced safety                                  |
| Less realistic representation of actual stiffness behavior                                  | More accurate representation of actual structural behavior                                               |
| **Less ductile** and less safe against overloads; limited redistribution                    | **More ductile** and safer against overloads due to force redistribution                                 |
| Easy to compute; **suitable for hand calculations**                                         | Requires **advanced analysis methods** like slope-deflection, moment distribution, or matrix methods     |
| Less sensitive to fabrication and erection tolerances                                       | More sensitive; misfits introduce additional internal stresses                                           |
| Examples: Simply supported beam, Cantilever, 3-hinged arch, Perfect truss                   | Examples: Continuous beam, Fixed beam, Rigid frame, Multi-span systems                                   |


## Identification of Determinate and Indeterminate Structures based on degree of redundancy (DoR)

### Degree of Redundancy (DoR)

**Degree of Redundancy (DoR)** or **Degree of Static Indeterminacy (DSI)** is defined as:

> *The number of excess unknown reactions or internal forces over available equilibrium equations.*


### 1. **External Static Indeterminacy**

For a **2D rigid structure**:

$$ DSI_{ext} = r - 3 $$

Where:  
$r =$ number of external reaction components


### 2. **Internal Static Indeterminacy**

For **pin-jointed trusses**:

$$ DSI_{int} = m - (2j - 3) $$

Where:  
$m =$ members, $j =$ joints

### 3. **Combined Indeterminacy (General 2D Frame)**

$$ DSI = (r + m) - 3j $$

### Example Summary Table

| Structure | Reactions (r) | DSI | Classification |
|---|---|---|---|
| Simply Supported Beam | 3 | $3-3=0$ | Determinate |
| Cantilever | 3 | $3-3=0$ | Determinate |
| Propped Cantilever | 4 | $4-3=1$ | Indeterminate |
| Fixed Beam | 6 | $6-3=3$ | Indeterminate |
| Two-Span Continuous Beam | 4 | $4-3=1$ | Indeterminate |

📌 **Image Placeholder:**  
`![Determinate vs Indeterminate](images/determinacy_placeholder.png)`  
*Fig: Examples of determinate and indeterminate beams*

### Quick Definitions

- **Statically Determinate Structure:**  
  A structure whose reactions and internal forces can be obtained using only equilibrium equations.

- **Statically Indeterminate Structure:**  
  A structure where number of unknowns > number of equilibrium equations.

- **Degree of Redundancy (DoR) / DSI:**  
  Number of additional unknown forces beyond equilibrium requirements.

- **External Indeterminacy:**  
  Excess support reactions.

- **Internal Indeterminacy:**  
  Excess internal member forces (common in frames & trusses).

[➤ Go to Index](#index)

