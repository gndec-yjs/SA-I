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

📌 **Image Placeholder:**  
`![Classification of Loads](images/load_classification_placeholder.png)`  
*Fig: Classification of Loads commonly acting on structures*

### Load Idealization (For Analysis)

Loads are converted into simplified forms for mathematical analysis:

- **Point Load (P)**
- **Uniformly Distributed Load (w)**
- **Uniformly Varying Load (UVL)**
- **Moment (M)**

📌 **Image Placeholder:**  
`![Load Idealization](images/load_idealization_placeholder.png)`  
*Fig: Load idealization formats used in analysis*

### Load Combination (Example per IS codes)

For Limit State Design:

$$ 1.5(DL + LL), \quad 1.2(DL + LL + WL) $$

### Quick Summary Table

| Parameter | Dead Load | Live Load |
|---|---|---|
| Variation | Constant | Variable |
| Duration | Permanent | Temporary |
| Source | Material self-weight | Occupancy |
| Code Reference | IS 875 Part 1 | IS 875 Part 2 |

## Types of Supports

Supports provide constraints against motion, causing reaction forces.

### Support Types & Reaction Characteristics

| Type of Support | Restrained DoF | Reactions Generated | Notes |
|---|---|---|---|
| **Fixed** | $u_x, u_y, \theta$ | $R_x, R_y, M$ | No movement or rotation |
| **Pinned/Hinged** | $u_x, u_y$ | $R_x, R_y$ | Rotation free |
| **Roller** | $u_y$ | $R_y$ | Allows expansion |
| **Link Support** | Along link axis | Single reaction | Used in trusses |

📌 **Image Placeholder:**  
`![Support Types](images/support_types_placeholder.png)`  
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

### Comparison Table

| Feature | Determinate Structure | Indeterminate Structure |
|---|---|---|
| Solved by | Equilibrium only | Equilibrium + Compatibility |
| Reaction Dependence on Material | No | Yes |
| Effect of Temp./Settlement | No internal force | Induces internal forces |
| Stiffness Influence | No | Yes |
| Safety under Overloads | Less | More (redundancy) |

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



### ➤ Back to Top
[Go to Index](#index)

