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
- [Identification of Determinate and Indeterminate Structures based on Degree of Redundancy (DoR)](#identification-of-determinate-and-indeterminate-structures-based-on-degree-of-redundancy-dor)

## Load – Types and Their Assessment

A **load** is any external action applied to a structure that produces internal forces, stresses, and deformations.  
Correct identification and assessment of loads form the foundation of structural analysis and design.

### Classification of Loads

| Load Type | Description | Examples | Code Reference |
|---|---|---|---|
| **Dead Load (DL)** | Permanent load due to self-weight of structural and non-structural components | Slabs, beams, walls, finishes | IS 875 Part 1 |
| **Live Load (LL)** | Movable or occupancy-related loads | People, furniture, vehicles | IS 875 Part 2 |
| **Wind Load (WL)** | Lateral pressure caused by wind action | High-rise buildings, towers | IS 875 Part 3 |
| **Snow Load (SL)** | Weight of accumulated snow | Hill-region roofs | IS 875 Part 4 |
| **Seismic Load (EL)** | Inertial forces induced by earthquakes | Base shear on buildings | IS 1893 |
| **Thermal Load** | Stresses due to temperature change | Expansion / contraction | $\sigma_t = E \alpha \Delta T$ |
| **Impact / Dynamic Load** | Sudden or shock loading | Crane, moving vehicles | Impact factor |

<img width="659" height="406" alt="image" src="https://github.com/user-attachments/assets/1887507b-3563-480e-bb9e-d6e69b39da12" />

*Fig: Classification of loads acting on structures*

### Load Idealization (For Structural Analysis)

Actual load distributions are converted into **idealized mathematical forms** to simplify analysis while preserving equivalent structural effects.

**Common idealized load forms:**

- **Point Load (P):** Concentrated force acting at a single point.
- **Uniformly Distributed Load (UDL – w):** Constant load intensity over a length.
- **Uniformly Varying Load (UVL):** Linearly varying load (triangular or trapezoidal).
- **Moment Load (M):** Pure couple causing rotational effect.
- **Combined Loads:** Superposition of point loads, UDL, UVL and moments.

#### Comparison of Idealized Load Forms

| Idealization | Shape | Equivalent Resultant Load | Line of Action |
|---|---|---|---|
| UDL | Rectangle | $wL$ | At $L/2$ |
| Triangular UVL | Wedge | $\frac{1}{2}w_{max}L$ | At $L/3$ from larger end |
| Trapezoidal UVL | Rectangle + Triangle | Combined resultant | From component centroids |
| Point Load | Single force | — | At point of application |
| Pure Moment | Couple | — | Produces rotation only |

<img width="526" height="517" alt="image" src="https://github.com/user-attachments/assets/65e34136-581e-48c9-abc7-a22c9ed8c362" />

*Fig: Load idealization in structural analysis*

### Load Combinations (as per IS Codes)

In analysis, multiple loads may act simultaneously. Therefore, standard **load combinations** are considered to evaluate realistic structural response.

Typical combinations:

- (DL + LL)  
- (DL + WL)  
- (DL + LL + WL)  
- (DL + EL)  
- (DL + LL + EL)

> **Note:** Wind Load (WL) and Earthquake Load (EL) are **not combined together**, since both represent rare extreme lateral events.

#### Summary Table

| Load Type | Variation | Duration | Source | Code Reference |
|---|---|---|---|---|
| Dead Load | Constant | Permanent | Self-weight | IS 875-1 |
| Live Load | Variable | Temporary | Occupancy | IS 875-2 |
| Wind Load | Directional | Short duration | Atmospheric | IS 875-3 |
| Earthquake Load | Dynamic | Instantaneous | Ground motion | IS 1893 |

## Types of Supports

Supports provide constraints against displacement and rotation, thereby generating reaction forces.

### Support Types & Reactions

| Support Type | Restrained Degrees of Freedom | Reactions Generated | Remarks |
|---|---|---|---|
| **Fixed** | $u_x, u_y, \theta$ | $R_x, R_y, M$ | Prevents translation and rotation |
| **Pinned / Hinged** | $u_x, u_y$ | $R_x, R_y$ | Rotation free |
| **Roller** | $u_y$ | $R_y$ | Allows horizontal movement |
| **Link** | Along link axis | Single reaction | Used in trusses |

<img width="591" height="357" alt="image" src="https://github.com/user-attachments/assets/5eb2cd79-4edf-414d-9a26-49e576fd2e81" />

*Fig: Standard support symbols*

## Concept and Types of Structures

A **structure** is an assemblage of connected members designed to safely transmit loads to supports.

### Classification Based on Structural Form

| Structural Form | Load Transfer Mechanism | Dominant Internal Forces | Examples |
|---|---|---|---|
| Cable | Tension | Axial tension | Suspension bridges |
| Truss | Axial action | Tension / Compression | Roof trusses |
| Beam | Flexure | Shear + Bending | Floor systems |
| Arch | Compression thrust | Axial compression + bending | Masonry arches |
| Frame | Combined action | Axial + Shear + Bending | Multi-storey buildings |


## **Basic Tenets of Structural Analysis**

For a complete and accurate analysis, a structure must satisfy:

- **Equilibrium:** internal forces must equilibrate external loads  
- **Kinematics:** displacements and strains must be compatible  
- **Stress–strain relation:** stresses must follow material law ($\sigma \propto \varepsilon$)

## Statical Determinacy

A structure is said to satisfy **static equilibrium** when the external loads are balanced by the reactions and internal forces.

For a **2D structure**, the independent equilibrium equations are:

$$ \sum H = 0,\quad \sum V = 0,\quad \sum M = 0 $$

For a **3D structure**, the independent equilibrium equations are:

$$ \sum F_x=0,\; \sum F_y=0,\; \sum F_z=0,\quad \sum M_x=0,\; \sum M_y=0,\; \sum M_z=0 $$

### **Statically Determinate Structures**

A structure is **statically determinate** if the reactions and member forces can be found by **equilibrium equations alone**, i.e.

> **Number of unknown forces = Number of independent equilibrium equations**

Such structures do **not** require compatibility equations for analysis.

### **Statically Indeterminate (Redundant / Hyperstatic) Structures**

A structure is **statically indeterminate** if the reactions and/or member forces **cannot** be found by equilibrium alone, i.e.

> **Number of unknown forces > Number of independent equilibrium equations**

In such cases, equilibrium equations must be supplemented by:

- **Compatibility of deformation (kinematic conditions)**  
- **Force–displacement relations** (depends on $E,\;A,\;I$ etc.)

### **Degree of Static Indeterminacy / Degree of Redundancy**

The **degree of static indeterminacy** (also called **degree of redundancy**) is the number of **additional unknown forces** beyond equilibrium requirements, i.e.

$$ D_s = (\text{No. of unknown forces}) - (\text{No. of independent equilibrium equations}) $$

A statically indeterminate structure may be:
- **Externally indeterminate** (due to supports)  
- **Internally indeterminate** (due to member arrangement / loops)

## **Difference Between Determinate and Indeterminate Structures (Exam Form)**

| **Statically Determinate Structures** | **Statically Indeterminate Structures** |
|---|---|
| Solved using **equilibrium equations alone** | Require **equilibrium + compatibility + force–displacement relations** |
| **Unknowns = equilibrium equations** | **Unknowns > equilibrium equations** |
| Member forces and reactions are **independent of $E, A, I$** | Member forces and reactions **depend on stiffness ($E, A, I$)** |
| Support settlement / temperature change does **not** induce secondary forces | Settlement / temperature restraint **induces secondary forces** |
| No redundancy → failure of one member may be critical | Redundancy → alternative load paths, improved safety |
| Simpler analysis (hand methods) | Advanced methods needed (flexibility/matrix methods, etc.) |

## Identification of Determinate and Indeterminate Structures based on Degree of Redundancy (DoR)

### **External Indeterminacy (Related to Supports)**

If the reactions cannot be obtained by equilibrium alone, the structure is **externally indeterminate**.

For **plane structures**:
$$ D_{se} = r - 3 $$

For **space structures**:
$$ D_{se} = r - 6 $$

where $r$ = number of **independent external reaction components**.

### **Internal Indeterminacy (Related to Members / Configuration)**

If the member forces cannot be obtained by equilibrium alone (even when support reactions are determinate), the structure is **internally indeterminate**.

### **Total Static Indeterminacy**

$$ D_s = D_{se} + D_{si} $$

where  
$D_s$ = total degree of static indeterminacy  
$D_{se}$ = degree of external indeterminacy  
$D_{si}$ = degree of internal indeterminacy  

## **Formulas (Plane vs Space, Pin vs Rigid)**

### **A) Degree of Static Indeterminacy (Direct Formula: Unknowns − Equations)**

| Structure Type | Plane (2D) | Space (3D) |
|---|---|---|
| **Pin-jointed frame / truss** | $$D_s=(m+r)-2j$$ | $$D_s=(m+r)-3j$$ |
| **Rigid-jointed frame** | $$D_s=(3m+r)-3j$$ | $$D_s=(6m+r)-6j$$ |

**Where:**  
$m$ = number of members  
$j$ = number of joints  
$r$ = number of unknown external reactions

> **Note:** The expression $(m+r)-2j$ is valid for **pin-jointed plane frames/trusses**, not for rigid-jointed frames.

### **B) Degree of External Indeterminacy**

| Type | Plane (2D) | Space (3D) |
|---|---|---|
| **External indeterminacy** | $$D_{se}=r-3$$ | $$D_{se}=r-6$$ |

### **C) Degree of Internal Indeterminacy**

#### **(i) Pin-Jointed Frames (Trusses)**

| Type | Plane (2D) | Space (3D) |
|---|---|---|
| **Internal indeterminacy** | $$D_{si}=m-(2j-3)$$ | $$D_{si}=m-(3j-6)$$ |

**Perfect (internally determinate) condition:**
- Plane: $m=2j-3$  
- Space: $m=3j-6$

#### **(ii) Rigid-Jointed Frames (Using Cuts / Loops)**

A rigid-jointed frame is internally determinate only when it forms an **open configuration** (tree-type), i.e., **no closed loops/cells**.

If loops exist, the structure can be made open by introducing **cuts**.  
Each cut releases:

- **Plane (2D):** 3 components (two forces + one moment)  
- **Space (3D):** 6 components (three forces + three moments)

Hence,

| Type | Plane (2D) | Space (3D) |
|---|---|---|
| **Rigid-jointed internal indeterminacy** | $$D_{si}=3c$$ | $$D_{si}=6c$$ |

where $c$ = number of cuts required to obtain an open configuration.

#### **(iii) Hybrid Structures (Some Joints Pin, Others Rigid)**

Skeletal structures having both pin and rigid joints are **hybrid**.  
To compute internal indeterminacy, pin joints may be replaced by rigid joints.

For a **plane hybrid frame**:

$$ D_{si}=3c-\sum (m_i-1) $$

For a **space hybrid frame**:

$$ D_{si}=6c-\sum 3(m_i-1) $$

where $m_i$ = number of members meeting at the $i^{th}$ pin joint.

## **Stability Check for Pin-Jointed Frames (Quick Test)**

### **Pin-Jointed Plane Frames**

| Condition | Interpretation |
|---|---|
| $m < (2j-3)$ | Internally unstable |
| $m = (2j-3)$ | Stable and internally determinate* |
| $m > (2j-3)$ | Overstiff and internally indeterminate |

### **Pin-Jointed Space Frames**

| Condition | Interpretation |
|---|---|
| $m < (3j-6)$ | Internally unstable |
| $m = (3j-6)$ | Stable and internally determinate* |
| $m > (3j-6)$ | Overstiff and internally indeterminate |

\* **Important note (exam point):** Even if $m=2j-3$, the truss may still be unstable/indeterminate if **any panel** is over-stiff or under-braced. The condition must hold not only for the whole truss but also for its individual panels.

### **Quick Definitions**

- **Statically Determinate Structure:**  
  Reactions and member forces are obtained by equilibrium alone, i.e. **unknowns = equilibrium equations**.

- **Statically Indeterminate Structure:**  
  Unknowns exceed equilibrium equations, i.e. **unknowns > equilibrium equations**; compatibility must be used.

- **Degree of Static Indeterminacy / Redundancy ($D_s$):**  
  Excess unknown forces beyond equilibrium, i.e. $$D_s = \text{unknowns} - \text{equations}$$

- **External Indeterminacy ($D_{se}$):**  
  Excess support reactions beyond equilibrium.

- **Internal Indeterminacy ($D_{si}$):**  
  Excess member forces / loops beyond equilibrium.

### **SUMMARY OF DEGREE OF STATIC INDETERMINACY (Ds)**

| TYPE OF JOINT | TYPE OF FRAME | DEGREE OF STATIC INDETERMINACY ($D_s$) |
|---|---|---|
| **PIN-JOINTED STRUCTURE** | Plane Frame | $D_s = (m+r) - 2j$ |
|  | Space Frame | $D_s = (m+r) - 3j$ |
| **RIGID-JOINTED STRUCTURE** | Plane Frame | $D_s = (3m+r) - 3j$ |
|  | Space Frame | $D_s = (6m+r) - 6j$ |

### **DEGREE OF EXTERNAL INDETERMINACY (Dse)**

| TYPE OF STRUCTURE | Degree of External Indeterminacy ($D_{se}$) |
|---|---|
| Plane Structure | $D_{se} = (r - 3)$ |
| Space Structure | $D_{se} = (r - 6)$ |

### **DEGREE OF INTERNAL INDETERMINACY (Dsi)**

| TYPE OF JOINT | TYPE OF FRAME | DEGREE OF INTERNAL INDETERMINACY ($D_{si}$) |
|---|---|---|
| **PIN-JOINTED STRUCTURE** | Plane Frame | $D_{si} = m - (2j - 3)$ |
|  | Space Frame | $D_{si} = m - (3j - 6)$ |
| **RIGID-JOINTED STRUCTURE** | Plane Frame | $D_{si} = 3c$ or $D_{si} = 3m - (3j - 3)$ |
|  | Space Frame | $D_{si} = 6c$ or or $D_{si} = 6m - (6j - 6)$ |
| **HYBRID STRUCTURE** | Plane Frame | $D_{si} = 3c - \sum(m - 1)$ |
|  | Space Frame | $D_{si} = 6c - \sum 3(m - 1)$ |

---

[➤ Go to Index](#index)

