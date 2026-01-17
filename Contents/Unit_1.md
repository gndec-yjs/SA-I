<!-- MathJax Configuration for HTML Rendering -->
<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    tex2jax: {
      inlineMath: [ ['$','$'], ["\\(","\\)"] ],
      processEscapes: true
    }
  });
</script>

<script type="text/javascript"
        src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>

<a id="top"></a>

# **Unit 1 — Introduction to Structural Systems**

## 📌 **Syllabus Content (Anchored)**  
Load – types and their assessment; Types of supports; Concept and types of structure – cables, trusses, beams, arches, frames; Statical determinacy; Identification of determinate and indeterminate structures based on Degree of Redundancy (DoR)

---

## **1. Load — Types and Their Assessment**

Loads are actions applied to structures that produce internal forces and deformations.

Common load categories include:

| Load Type | Description | Example |
|---|---|---|
| Dead Load | Permanent, self-weight | Weight of beams, slabs |
| Live Load | Movable, time-dependent | People, furniture |
| Environmental Load | From natural effects | Wind, temperature |
| Dynamic Load | Time-varying inertial effects | Seismic, machinery |

Mathematically, loads may be expressed as:

- Point Load: $P$ (in Newtons)
- Uniformly Distributed Load: $w$ (in $kN/m$)
- Uniformly Varying Load: $w(x)$

**Assessment parameters include:**

- Magnitude
- Direction
- Distribution
- Duration
- Point of application

📷 *[Load diagram placeholder]*

---

## **2. Types of Supports**

Supports resist structural movements and produce reactions.

| Support Type | Restraints | Reactions | Symbol |
|---|---|---|---|
| Roller | One translation | $R_y$ | 🔵 |
| Pin | Two translations | $R_x, R_y$ | ⚫ |
| Fixed | All translations + rotation | $R_x, R_y, M$ | ⛔ |

📷 *[Support diagram placeholder]*

---

## **3. Concepts & Types of Structures**

Based on geometry & force transfer:

| Structure | Description | Example |
|---|---|---|
| Cables | Carry tension only | Suspension bridges |
| Trusses | Two-force members | Roof trusses |
| Beams | Bending dominant | Floor beams |
| Frames | Axial + shear + bending | Building frames |
| Arches | Compression dominant | Stone bridges |

📷 *[Structure-type diagram placeholder]*

---

## **4. Statical Determinacy**

A structure is **statically determinate** if equilibrium equations alone determine internal forces & reactions.

For planar structures:

$$
\sum F_x = 0,\ \sum F_y = 0,\ \sum M = 0
$$

Total equations available = 3

---

## **5. Determinate vs. Indeterminate Structures**

| Feature | Determinate | Indeterminate |
|---|---|---|
| Equilibrium suffices | ✔️ | ❌ Requires compatibility |
| Redundancy (DoR) | 0 | ≥ 1 |
| Analysis | Simple | Complex |
| Example | Simply supported beam | Fixed beam |

---

## **6. Degree of Redundancy (DoR)**

DoR quantifies excess reactions / internal forces beyond equilibrium.

For planar structures:

$$
DoR = R - 3
$$

Where:  
- $R =$ number of reaction components  
- `3` = available equilibrium equations ($\sum F_x, \sum F_y, \sum M$)

**Examples:**

- Simply Supported Beam → $R = 3 → DoR = 0$ (Determinate)
- Fixed Beam → $R = 4 → DoR = 1$ (Indeterminate)

📷 *[DoR illustration placeholder]*

---

### 🔗 **Back to Top**
[⬆ Go to Top](#top)
