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
- [Equilibrium of Cable](#equilibrium_of_cable)
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

Cables are widely used in engineering structures both as **temporary supporting elements** and as **permanent load-carrying members**. During construction, cables act as **guys** to stabilize structures such as masts, towers, and erection systems. In many practical situations—such as circus tents or temporary shelters—guy cables are commonly used to provide stability and maintain structural form.

In permanent structures, cables play a crucial role in systems like **suspension bridges**, where they support the primary load of the structure. Towers are used to support these cables, and the load is transferred through **suspenders** to the roadway or deck.

<img width="809" height="362" alt="image" src="https://github.com/user-attachments/assets/169e6411-53b2-4532-8b9d-3c5eb08bcc83" />

*Figure: Typical suspension bridge showing cable, towers, suspenders, and roadway*

A suspension bridge consists of a main cable passing over towers, with the roadway suspended below using vertical members called **suspenders**. This arrangement significantly reduces bending in the system, making it structurally efficient for long spans. The central dip or **sag** of the cable is an important design parameter and generally varies between **one-tenth to one-fifth of the span**.

To further reduce bending effects in towers and improve stability, **anchor cables (or anchor guys)** are provided at the ends. These help in balancing horizontal forces developed due to cable tension.

Depending on support conditions, cables may pass over towers through:

- **Guided pulley supports**, or  
- **Roller supports**

<img width="1312" height="456" alt="image" src="https://github.com/user-attachments/assets/abcc5bc1-3c2b-422d-84fe-f5d2e85827a1" />

*Figure: Types of cable supports – Guided Pulley and Saddle on Rollers/Smooth Rollers support*

**Conceptually:**

A cable passing over a tower must be able to adjust its position and tension as loads change. Different support types allow this in different ways.

- **Roller / Pulley Support**

In roller or pulley supports, the cable:

physically moves/rolls over the support
reduces friction
allows free adjustment of tension on both sides

_Think of it like a rope passing over a smooth wheel._

**Effect:**

Tension on both sides of the tower tends to be equal (or nearly equal)
Used in idealized analysis

- **Saddle Support (Real Practice)**

A saddle is what is actually used in real suspension bridges.

It is a curved seating (grooved block) placed on top of the tower
The cable rests on it, not freely rolling like a pulley
May allow limited movement, but not full rolling

_Think of it like a shaped support where the cable sits and slightly slides._

- **Key Differences**

| Feature          | Roller/Pulley           | Saddle                |
| ---------------- | ----------------------- | --------------------- |
| Movement         | Free rolling            | Limited sliding       |
| Friction         | Very low (idealized)    | Some friction present |
| Tension equality | Nearly equal both sides | May differ slightly   |
| Usage            | Theoretical problems    | Real bridges          |

In bridges carrying pedestrian or vehicular loads, a **stiffening girder** is often provided below the roadway. This helps in distributing loads more uniformly and reduces excessive deformation of the cable.

<img width="808" height="386" alt="image" src="https://github.com/user-attachments/assets/91a488e3-9abd-4cb0-bcdd-7252bb71690d" />

*Figure: Stiffening girder in a suspension bridge system*

Since the number of suspenders in a suspension bridge is generally large, the load transferred to the cable can be **idealized as a uniformly distributed load**. Cables are highly flexible and can resist **only tensile forces**, not bending or compression. This makes **steel** the most suitable material for cables due to its high tensile strength and efficiency.

Because of these advantages, suspension bridges are highly economical for **long spans**, typically ranging from **200 m to 300 m or more**.

Well-known examples of suspension bridges include structures like **Laxman Jhula at Rishikesh** and the **Howrah Bridge**, which demonstrate the practical application and efficiency of cable-supported systems.

##### Q: Define Cable. Give suitable examples. 

**Ans:** A **cable** is a flexible structural element that can carry **tension only** and has negligible resistance to bending or compression.

_Examples:_
- Suspension bridges  
- Transmission lines  
- Cable roofs  

When subjected to loads, a cable assumes a shape such that it remains entirely in **tension**.

## Equilibrium of Cable

A **cable** is a flexible structural element which **cannot resist bending moment**. When subjected to loads, it adjusts its shape such that the **bending moment at every point is zero**. This condition is achieved by the development of a **horizontal thrust** at the supports, along with corresponding vertical reactions, resulting in an appropriate cable profile.

<img width="872" height="363" alt="image" src="https://github.com/user-attachments/assets/11a81fb3-da19-4aba-8535-131dcd568ea6" />

*Figure: Equilibrium of a cable under concentrated loads*

Consider a cable subjected to a system of loads. Let:

- $H$ = horizontal component of cable tension (constant throughout)  
- $V_A$, $V_B$ = vertical reactions at supports $A$ and $B$  
- At a section $X - X$, let the vertical deflection (ordinate) be $y$  

Using the analogy of a **simply supported beam**, the bending moment at section $X - X$ can be written as:

$$
M_x = V_A x - W_1(x - a_1) - W_2(x - a_2) - H y
$$

Since the cable is perfectly flexible,

$$
M_x = 0
$$

Therefore,

$$
H_y = V_A x - W_1(x - a_1) - W_2(x - a_2) = Beam Moment
$$

> Considering any segment of cable and using the above equation alone with usual equations, a loaded cable can be analyzed. This equation relates the **shape of the cable** (through $y$) to the applied loads and support reactions.

#### Key Concept

> The equilibrium of a cable can be analysed by treating it as an **equivalent simply supported beam**, where:

- The **bending moment in beam** = $H \cdot y$ in cable  
- The **shear force in beam** = slope of cable  

#### General Approach for Cable Analysis

1. Determine **support reactions** using equilibrium:
   $$
   \sum V = 0,\quad \sum M = 0
   $$

2. Write the **beam moment equation** at a section.

3. Use the condition:
   $$
   M = 0 \quad \Rightarrow \quad Hy = \text{beam moment}
   $$

4. Obtain the **equation of cable profile**.

#### Important Note

> A loaded cable is always analysed using:
- **Equilibrium equations**, and  
- **Beam analogy (moment relationship)**  

This simplifies the analysis of cables under different loading conditions.

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

## Cable Subjected to Concentrated Loads

Consider a cable of length $L$ spanning over a horizontal distance $l$, subjected to a system of **concentrated loads** as shown in the figure.

<img width="830" height="386" alt="image" src="https://github.com/user-attachments/assets/3b057771-59a2-4179-8793-c3177dad2d59" />

*Figure: Cable subjected to concentrated loads*

Let:
- $V_A$, $V_B$ = vertical reactions at supports $A$ and $B$  
- $H$ = horizontal component of cable tension (constant)  

### Fundamental Relation

From equilibrium of the cable:

$$
H y = M_{\text{beam}} \quad \text{or} \quad y = \frac{M_{\text{beam}}}{H}
$$

#### Key Interpretation

> The **shape of the cable** under concentrated loads is **similar to the bending moment diagram** of a simply supported beam carrying the same loads.

### Deflection at Load Points

If:
- $M_1$, $M_2$, $M_3$ = bending moments at load points (from equivalent beam)  

Then corresponding cable deflections are:

$$
y_1 = \frac{M_1}{H}, \quad
y_2 = \frac{M_2}{H}, \quad
y_3 = \frac{M_3}{H}
$$

### Description of Cable System

The cable is supported at points $A$ and $B$ with:

- Horizontal reaction: $H$  
- Vertical reactions: $V_A$, $V_B$  

The cable is divided into multiple straight segments due to concentrated loads:

- Segment tensions: $T_1$, $T_2$, $T_3$, $T_4$  

Intermediate points:

- Point 1: Load $W_1$, deflection $y_1$  
- Point 2: Load $W_2$, deflection $y_2$  
- Point 3: Load $W_3$, deflection $y_3$  

### Determination of Cable Shape

If either:

- Horizontal thrust $H$ is known, **or**  
- Deflection at any one point is known  

then:

- Deflections at all other points can be calculated  
- Complete **cable profile (shape)** can be obtained  

### Length of Cable

The actual length of the cable is obtained as:

> Sum of lengths of individual straight segments between load points.

### Determination of Tension in Cable Segments

After finding deflections:

1. Determine slopes of each segment  
2. Apply equilibrium at load points:

$$
\sum F_x = 0, \quad \sum F_y = 0
$$

3. Compute forces in segments:

$$
T_1,\; T_2,\; T_3,\; T_4
$$

### Important Insight

> A cable subjected to concentrated loads forms a **polygonal shape**, unlike smooth curves seen in UDL cases.

### Note

> Always:
- First analyze the **equivalent beam**  
- Then use $y = \dfrac{M}{H}$ to get cable profile  
- Finally compute **tensions using joint equilibrium**

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
