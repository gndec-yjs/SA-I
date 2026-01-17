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

# CE-SA-I: Structural Analysis I

## Unit 1: Introduction to Structural Systems

- [Load – Types and Their Assessment](#load--types-and-their-assessment)
- [Types of Supports](#types-of-supports)
- [Concept and Types of Structures](#concept-and-types-of-structures)
- [Statical Determinacy](#statical-determinacy)
- [Identification of Determinate and Indeterminate Structures (DoR)](#identification-of-determinate-and-indeterminate-structures-dor)

---

## Load – Types and Their Assessment

A **load** is any external force or action applied on a structural system that causes stresses, deformation, or displacement.

### Classification of Loads

| Load Type | Description | Examples |
|---|---|---|
| **Dead Load (DL)** | Permanent, time-invariant loads | Self-weight, walls, finishes |
| **Live Load (LL)** | Movable, variable loads | Occupants, furniture |
| **Environmental Loads** | Climatic or natural effects | Wind, snow, earthquake |
| **Dynamic Loads** | Time-dependent with inertia | Machinery, vehicles |
| **Thermal Loads** | Due to temperature variation | Expansion / Contraction |

### Basic Load Assessment Concepts

- **Dead Load**  
  $DL = \gamma \times \text{Volume}$

- **Live Load**  
  As per IS 875 Part 2 (varies with building use)

- **Wind Load**  
  Depends on basic wind speed and exposure (IS 875 Part 3)

- **Earthquake Load**  
  Equivalent static base shear approach:  
  $V_b = A_h \times W$

---

## Types of Supports

Supports restrain movement and provide **reaction forces**.

| Support Type | Restrained Movements | Reactions |
|---|---|---|
| **Fixed Support** | Rotation + Translation | $R_x, R_y, M$ |
| **Pinned Support** | Translation | $R_x, R_y$ |
| **Roller Support** | One Translation | $R_y$ or $R_x$ |

(Images can be added later as needed)

---

## Concept and Types of Structures

Structures transfer loads safely to the supports.

Common structural systems:

| System | Behavior | Examples |
|---|---|---|
| **Cables** | Tension only | Suspension bridges |
| **Trusses** | Axial forces (Tension/Compression) | Roof trusses |
| **Beams** | Bending + Shear | Floor beams |
| **Arches** | Compression with horizontal thrust | Stone bridges |
| **Frames** | Axial + Flexural | RC building frames |

---

## Statical Determinacy

A structure is **statically determinate** if all reactions and internal forces can be found using only **equilibrium equations**.

For 2D systems:

$$ \sum F_x = 0,\quad \sum F_y = 0,\quad \sum M = 0 $$

---

## Identification of Determinate and Indeterminate Structures (DoR)

### Degree of Redundancy (DoR)

For 2D structures:

$$ DoR = r - 3 $$

Where:  
- $r =$ Number of unknown support reactions  
- $3 =$ Number of independent equilibrium equations in 2D

### Examples

- **Simply Supported Beam**  
  $r = 3$ → $DoR = 3 - 3 = 0$ → Determinate

- **Propped Cantilever**  
  $r = 4$ → $DoR = 4 - 3 = 1$ → Indeterminate

### Summary Table

| Type | Condition | Example |
|---|---|---|
| **Determinate** | $DoR = 0$ | Simply supported beam |
| **Indeterminate** | $DoR > 0$ | Fixed beams, continuous beams |

