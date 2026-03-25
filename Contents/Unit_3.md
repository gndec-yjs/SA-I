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

## Unit 3: Cables and Trusses (Determinate Structures)

### Index
- [Cables – Introduction](#cables--introduction)
- [General Cable Theorem](#general-cable-theorem)
- [Shape of Cable](#shape-of-cable)
- [Tension in Cables](#tension-in-cables)
- [Elastic Stretch of Cable](#elastic-stretch-of-cable)
- [Back-Stays and Support Reactions](#back-stays-and-support-reactions)
- [Pressure on Supporting Towers](#pressure-on-supporting-towers)
- [Trusses – Introduction](#trusses--introduction)
- [Assumptions in Truss Analysis](#assumptions-in-truss-analysis)
- [Method of Joints](#method-of-joints)
- [Method of Sections](#method-of-sections)
- [Tension Coefficient Method](#tension-coefficient-method)
- [Deflection of Trusses (Energy Method)](#deflection-of-trusses-energy-method)

## Cables – Introduction

## Cables – Introduction

Cables are widely used in engineering structures both as **temporary supporting elements** and as **permanent load-carrying members**. During construction, cables act as **guys** to stabilize structures such as masts, towers, and erection systems. In many practical situations—such as circus tents or temporary shelters—guy cables are commonly used to provide stability and maintain structural form.

In permanent structures, cables play a crucial role in systems like **suspension bridges**, where they support the primary load of the structure. Towers are used to support these cables, and the load is transferred through **suspenders** to the roadway or deck.

<img width="932" height="450" alt="image" src="https://github.com/user-attachments/assets/c5ea796f-f66f-46f6-a6b7-b00abbb523d3" />

*Figure: Typical suspension bridge showing cable, towers, suspenders, and roadway*

A suspension bridge consists of a main cable passing over towers, with the roadway suspended below using vertical members called **suspenders**. This arrangement significantly reduces bending in the system, making it structurally efficient for long spans. The central dip or **sag** of the cable is an important design parameter and generally varies between **one-tenth to one-fifth of the span**.

To further reduce bending effects in towers and improve stability, **anchor cables (or anchor guys)** are provided at the ends. These help in balancing horizontal forces developed due to cable tension.

Depending on support conditions, cables may pass over towers through:

- **Guided pulley supports**, or  
- **Roller supports**

<img width="1518" height="533" alt="image" src="https://github.com/user-attachments/assets/f34339c7-d325-44b6-a17e-60ff32763cd2" />

*Figure: Types of cable supports – Guided Pulley and Saddle on Rollers/Smooth Rollers support*

In bridges carrying pedestrian or vehicular loads, a **stiffening girder** is often provided below the roadway. This helps in distributing loads more uniformly and reduces excessive deformation of the cable.

<img width="813" height="419" alt="image" src="https://github.com/user-attachments/assets/ed2cfd11-1c0f-4af5-80a1-3b94e0404ca4" />

*Figure: Stiffening girder in a suspension bridge system*

Since the number of suspenders in a suspension bridge is generally large, the load transferred to the cable can be **idealized as a uniformly distributed load**. Cables are highly flexible and can resist **only tensile forces**, not bending or compression. This makes **steel** the most suitable material for cables due to its high tensile strength and efficiency.

Because of these advantages, suspension bridges are highly economical for **long spans**, typically ranging from **200 m to 300 m or more**.

Well-known examples of suspension bridges include structures like **Laxman Jhula at Rishikesh** and the **Howrah Bridge**, which demonstrate the practical application and efficiency of cable-supported systems.

Q: Define Cable. Give suitable examples.
A: A **cable** is a flexible structural element that can carry **tension only** and has negligible resistance to bending or compression.

Examples:
- Suspension bridges  
- Transmission lines  
- Cable roofs  

When subjected to loads, a cable assumes a shape such that it remains entirely in **tension**.

---

## General Cable Theorem

The **general cable theorem** states:

> *At any point on a cable, the horizontal component of tension is constant and the slope of the cable at that point is proportional to the shear force at the corresponding point in an equivalent simply supported beam.*

Mathematically,

$$
\frac{dy}{dx} = \frac{V}{H}
$$

where:  
$V$ = shear force at corresponding section of beam  
$H$ = horizontal component of cable tension (constant)

Also,

$$
M = H \cdot y
$$

where $M$ is the bending moment in the corresponding beam and $y$ is the vertical ordinate of the cable.

---

## Shape of Cable

The shape of a cable depends on the type of loading:

### 1. Cable under Uniform Load (UDL per horizontal length)

- Shape: **Parabola**
- Equation:

$$
y = \frac{w x^2}{2H}
$$

### 2. Cable under Uniform Load (UDL per cable length)

- Shape: **Catenary**
- Equation:

$$
y = \frac{H}{w}\left[\cosh\left(\frac{wx}{H}\right)-1\right]
$$

### 3. Cable under Point Loads

- Shape: **Polygonal**

---

## Tension in Cables

At any point in the cable, total tension $T$ is given by:

$$
T = \sqrt{H^2 + V^2}
$$

where:
- $H$ = horizontal tension (constant)
- $V$ = vertical component at the section

### Maximum Tension

Maximum tension occurs at **supports**:

$$
T_{max} = \sqrt{H^2 + V_{support}^2}
$$

---

## Elastic Stretch of Cable

When a cable is subjected to load, it undergoes **elongation** due to axial tension.

Total extension:

$$
\Delta L = \sum \frac{T \cdot L}{AE}
$$

where:
- $A$ = cross-sectional area  
- $E$ = modulus of elasticity  
- $T$ = tension in segment  

---

## Back-Stays and Support Reactions

**Back-stays** are inclined cables provided at supports to resist horizontal forces.

- They reduce horizontal thrust on towers  
- Improve overall stability  

Horizontal component:

$$
H = T \cos \theta
$$

Vertical component:

$$
V = T \sin \theta
$$

---

## Pressure on Supporting Towers

Supporting towers are subjected to:

- Vertical loads from cable reactions  
- Horizontal thrust due to cable tension  

Resultant force on tower:

$$
R = \sqrt{H^2 + V^2}
$$

---

## Trusses – Introduction

A **truss** is a structure composed of **straight members connected at joints**, forming a stable framework.

Characteristics:
- Members carry **axial forces only**
- Joints are assumed to be **pin-connected**

---

## Assumptions in Truss Analysis

- Loads act only at joints  
- Members are straight and prismatic  
- Self-weight is negligible or lumped at joints  
- Joints are frictionless pins  

---

## Method of Joints

Based on **equilibrium of joints**:

At each joint,

$$
\sum F_x = 0, \quad \sum F_y = 0
$$

Procedure:
1. Start with a joint having ≤ 2 unknowns  
2. Assume all unknown forces as tension  
3. Solve using equilibrium equations  

---

## Method of Sections

Used to find forces in specific members directly.

Steps:
1. Pass a section cutting through desired members  
2. Consider equilibrium of one part  
3. Apply:

$$
\sum F_x = 0,\quad \sum F_y = 0,\quad \sum M = 0
$$

---

## Tension Coefficient Method

Used for **systematic analysis of trusses**.

Define tension coefficient:

$$
t = \frac{T}{L}
$$

where:
- $T$ = force in member  
- $L$ = length of member  

Equilibrium equations are written in terms of **coordinates of joints**.

---

## Deflection of Trusses (Energy Method)

Deflection at a joint is computed using **unit load method**:

$$
\delta = \sum \frac{F \cdot f \cdot L}{AE}
$$

where:
- $F$ = member force due to actual load  
- $f$ = member force due to unit load  
- $L$ = length of member  

---

## Key Comparison: Cables vs Trusses

| Feature | Cable | Truss |
|--------|------|------|
| Force Type | Tension only | Tension & Compression |
| Shape | Flexible | Rigid |
| Analysis | Based on geometry | Based on equilibrium |
| Applications | Bridges, cables | Roofs, towers |

---

## Exam Tips

> Use **general cable theorem** to convert cable problems into beam problems.  

> Always check **determinacy condition** before solving trusses:
$$
m = 2j - 3
$$

> Use:
- **Method of joints** → full analysis  
- **Method of sections** → specific members  
- **Energy method** → deflection  

---

[➤ Go to Index](#index)
