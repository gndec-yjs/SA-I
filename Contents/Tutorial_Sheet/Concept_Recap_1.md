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

## **Concept Recap (TUTORIAL SHEET – 1)**

### **Beam**

A beam is a structural member predominantly subjected to transverse loading. Such loadings induce:

- **Shear Force (SF):** Internal force tangential to beam cross-section.
- **Bending Moment (BM):** Internal moment causing bending/rotation.

### **Shear Force (SF)**
At a given section of a beam, the **shear force** is the **algebraic sum of all vertical forces** acting on either side of the section.

Units: **kN**

Mathematically, at a section $x$ from the left:
$$ V(x) = \sum F_y $$

### **Bending Moment (BM)**
At a given section of a beam, the **bending moment** is the **algebraic sum of moments** of all forces on either side of the section about that point.

Units: **kN·m**

Mathematically:
$$ M(x) = \sum (F \times \text{lever arm}) $$

### **Sign Conventions (For Analysis)**

- **Shear Force (SF):**
  - Clockwise rotation of left segment → **Positive (+)**
  - Anticlockwise rotation of left segment → **Negative (−)**

- **Bending Moment (BM):**
  - Sagging (concave up) → **Positive (+)**
  - Hogging (concave down) → **Negative (−)**

## **2. Typical Loading Types in Beams**

| Loading Type | Notation | Remarks |
|---|---|---|
| Point Load | $P$ | Acts at a point |
| UDL | $w$ (kN/m) | Constant intensity |
| UVL (Triangular) | varies 0→$w$ | Equivalent load = $\frac{1}{2} wL$ |
| Pure Moment | $M$ | Causes rotation |
| Combinations | — | Multiple loads applied |

- **Point Load:** $P$ (kN)
- **Uniformly Distributed Load (UDL):** $w$ (kN/m)
- **Uniformly Varying Load (UVL):** triangular loads
- **Applied External Moment:** $M$ (kNm)

## **3. Common Cases**

### **(A) Simply Supported Beam (SSB)** — Span $L$

| Loading | Reaction(s) | SF at Mid | Max BM |
|---|---|---|---|
| Point load $P$ at mid | $R_A = R_B = \frac{P}{2}$ | changes sign | $M_{max} = \frac{PL}{4}$ |
| UDL $w$ over whole span | $R_A = R_B = \frac{wL}{2}$ | linear variation | $M_{max} = \frac{wL^2}{8}$ |
| Moment $M$ at mid | $R_A = -R_B = \frac{M}{L}$ | discontinuity | — |

### **(B) Cantilever Beam** — Fixed at A, free at B

| Loading | SF at Fixed End | BM at Fixed End |
|---|---|---|
| Point load $P$ at free end | $V = -P$ | $M = -PL$ |
| UDL $w$ over length $L$ | $V = -wL$ | $M = -\frac{wL^2}{2}$ |
| UVL (0→$w$) | $V = -\frac{wL}{2}$ | $M = -\frac{wL^2}{6}$ |
| Moment $M$ at free end | $V=0$ | $M=-M$ at fixed |

## **4. General Expressions (Symbolic Form)**

Students should derive using a beam of span $L$ under general loads:

### **(i) SSB with UDL $w$**
Reactions:
$$ R_A = R_B = \frac{wL}{2} $$

Shear Force at section $x$:
$$ V(x) = R_A - wx $$

Bending Moment at section $x$:
$$ M(x) = R_A x - \frac{wx^2}{2} $$

### **(ii) Cantilever with UDL $w$**
Shear:
$$ V(x) = -w(L-x) $$

Moment:
$$ M(x) = -w\frac{(L-x)^2}{2} $$

### **5. Point of Contraflexure (POC)**

A **Point of Contraflexure** is a location where:
$$ M(x) = 0 $$
but the bending moment **changes sign**.

Occurs usually in:
- Overhanging beams
- Frames
- Continuous beams

**Significance:**
- Indicates change in curvature from **sagging to hogging**
- Important for **reinforcement detailing** in RCC design

## **6. Worked Example (Illustrative)**

**Problem:** A cantilever beam of length $L$ carries point load $P$ at free end.

**SF Diagram:**
- Constant shear: $V = -P$

**BM Diagram:**
- Linear from $0$ at free end to $-PL$ at fixed end
