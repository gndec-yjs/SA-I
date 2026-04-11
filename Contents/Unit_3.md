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
- [Cable Subjected to Concentrated Loads](#cable-subjected-to-concentrated-loads)
- [Cable Subjected to a Uniformly Distributed Load](#cable-subjected-to-a-uniformly-distributed-load)
- [Cable with Ends at Different Levels](#cable-with-ends-at-different-levels)
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

1) Determine slopes of each segment  
2) Apply equilibrium at load points:

$$
\sum F_x = 0, \quad \sum F_y = 0
$$

3) Compute forces in segments:

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

## Cable Subjected to a Uniformly Distributed Load

Consider a cable of length $L$ supported at points $A$ and $B$ at the same level, separated by a horizontal distance $l$. The cable carries a **uniformly distributed load $w$ per unit horizontal length**.

<img width="693" height="327" alt="image" src="https://github.com/user-attachments/assets/4a0fd897-8fa8-4fac-8f62-6d7d0e8b277b" />

*Figure: Cable subjected to UDL*

<img width="603" height="309" alt="image" src="https://github.com/user-attachments/assets/60235324-e65a-42af-854e-f8dc6529e1c2" />

*Figure: Free body diagram of Cable*

## Support Reactions

By symmetry,

$$
V_A = V_B = \frac{w l}{2}
$$

## Horizontal Thrust

Taking moments about the lowest (central) point of the cable and using the condition that **bending moment in a cable is zero**, we obtain:

$$
Hh - \frac{w l}{2}\cdot\frac{l}{2} - \frac{w l}{2}\cdot\frac{l}{4} = 0
$$

Therefore,

$$
\boxed{H = \frac{w l^2}{8h}}
$$

where $h$ is the central sag of the cable.

## Shear and Tension in Cable

At any section $X\!-\!X$ at a distance $x$ from support $A$:

$$
T = \sqrt{V^2 + H^2}
$$

Maximum shear occurs at supports:

$$
V_{\max} = \frac{w l}{2}
$$

Maximum tension:

$$
T_{\max} = \sqrt{\left(\frac{w l}{2}\right)^2 + \left(\frac{w l^2}{8 h}\right)^2}
$$

Minimum shear occurs at centre:

$$
V_{\min} = 0
$$

Minimum tension:

$$
T_{\min} = H
$$

## Equilibrium at Section

At any section:

$$
\sum H = 0 \Rightarrow T \cos \theta = H
$$

$$
\sum V = 0 \Rightarrow T \sin \theta = V_A - wx = \frac{w l}{2} - wx
$$

Therefore,

$$
\tan \theta = \frac{\frac{w l}{2} - wx}{H}
$$

## Equation of Cable Profile

Since,

$$
\frac{dy}{dx} = \tan \theta
$$

$$
\frac{dy}{dx} = \left(\frac{w l}{2} - wx\right)\frac{1}{H}
$$

Integrating:

$$
y = \left[\frac{w l}{2}x - \frac{w x^2}{2}\right]\frac{1}{H}
$$

$$
y = \frac{w x (l - x)}{2H}
$$

Substituting $H = \dfrac{w l^2}{8h}$:

$$
y = \frac{w x (l - x)}{2} \cdot \frac{8h}{w l^2}
$$

$$
\boxed{y = \frac{4h x (l - x)}{l^2}}
$$

## Shape of Cable

> The above equation represents a **parabola**.

Hence, a cable subjected to **UDL per horizontal length assumes a parabolic shape**.


## Length of Cable

For any curve:

$$
\frac{ds}{dx} = \sqrt{1 + \left(\frac{dy}{dx}\right)^2}
$$

Using approximation:

$$
\frac{ds}{dx} \approx 1 + \frac{1}{2}\left(\frac{dy}{dx}\right)^2
$$

Substituting slope expression and integrating:

$$
L = \int_0^l ds
$$

$$
L = l + \frac{8h^2}{3l}
$$

## Important Results Summary

$$
H = \frac{w l^2}{8h}
$$

$$
y = \frac{4h x (l - x)}{l^2}
$$

$$
T_{\max} = \sqrt{\left(\frac{w l}{2}\right)^2 + \left(\frac{w l^2}{8 h}\right)^2}
$$

$$
T_{\min} = H
$$

## Key Insight

> A cable under **UDL per horizontal length behaves like a parabola**, and its analysis can be directly linked to the **bending moment diagram of an equivalent simply supported beam**.

---

## Cable with Ends at Different Levels

Consider a cable supported at two points **A** and **B**, which are at different heights above the lowest point **C**.  
The cable carries a **uniformly distributed load $w$ per unit horizontal length** over the entire span $l$.

- Horizontal distance:
  - $AC = l_1$
  - $CB = l_2$
- Vertical distances:
  - $AC = h_1$
  - $BC = h_2$

The **horizontal reaction** at both supports is:

$$
H = \text{constant}
$$

Since a cable can resist **only axial tension**, it cannot resist bending moment or shear force.  
At the lowest point $C$:

- Vertical force = 0  
- Tension = $H$  

<img width="732" height="445" alt="image" src="https://github.com/user-attachments/assets/76bfe94a-71e3-481b-81f2-fd2870a04b18" />
**Figure:** Cable with supports at different levels  

<img width="696" height="291" alt="image" src="https://github.com/user-attachments/assets/7e68c4d6-9948-4dad-93e0-25408eb2e754" />
**Figure:** Free body diagram of cable

### Equilibrium of Cable Segment

Let $D$ be any point on the cable where the slope is $\theta$.  
Taking point $C$ as origin and considering equilibrium of segment $CD$:

$$
T \cos \theta = H
$$

$$
T \sin \theta = wx
$$

Dividing,

$$
\tan \theta = \frac{wx}{H}
$$

Since,

$$
\tan \theta = \frac{dy}{dx}
$$

we get:

$$
\frac{dy}{dx} = \frac{wx}{H}
$$

### Equation of Cable Shape

Integrating,

$$
y = \frac{w x^2}{2H} + C_1
$$

At lowest point $C$:

$$
x = 0, \quad y = 0
$$

Therefore,

$$
C_1 = 0
$$

Hence,

$$
\boxed{y = \frac{w x^2}{2H}}
$$

This represents a **parabola**, hence the cable takes a **parabolic shape**.

### Relations at Supports

Applying the equation at supports:

$$
h_1 = \frac{w l_1^2}{2H}, \quad h_2 = \frac{w l_2^2}{2H}
$$

Taking ratio:

$$
\frac{h_1}{h_2} = \frac{l_1^2}{l_2^2}
$$

$$
\frac{\sqrt{h_1}}{\sqrt{h_2}} = \frac{l_1}{l_2}
$$

Hence,

$$
\frac{l_1}{l} = \frac{\sqrt{h_1}}{\sqrt{h_1} + \sqrt{h_2}}
$$

$$
\boxed{
l_1 = l \left( \frac{\sqrt{h_1}}{\sqrt{h_1} + \sqrt{h_2}} \right)
}
$$

$$
\boxed{
l_2 = l \left( \frac{\sqrt{h_2}}{\sqrt{h_1} + \sqrt{h_2}} \right)
}
$$

### Determination of Horizontal Thrust $H$

Taking moments about point $C$:

#### From left side:

$$
V_A l_1 - H h_1 - \frac{w l_1^2}{2} = 0
$$

$$
V_A = \frac{w l_1}{2} + \left(\frac{h_1}{l_1}\right) H \quad ...(i)
$$

#### From right side:

$$
V_B l_2 - H h_2 - \frac{w l_2^2}{2} = 0
$$

$$
V_B = \frac{w l_2}{2} + \left(\frac{h_2}{l_2}\right) H \quad ...(ii)
$$

Adding:

$$
V_A + V_B = \frac{w}{2}(l_1 + l_2) + \left(\frac{h_1}{l_1} + \frac{h_2}{l_2}\right)H
$$

But total load:

$$
V_A + V_B = wl
$$

Therefore,

$$
\frac{wl}{2} = \left(\frac{h_1}{l_1} + \frac{h_2}{l_2}\right)H
$$

Substituting values of $l_1$ and $l_2$:

$$
\boxed{
H = \frac{w l^2}{2(\sqrt{h_1} + \sqrt{h_2})^2}
}
$$

### Length of Cable

Total cable length:

$$
L = l + \frac{2}{3}\frac{h_1^2}{l_1} + \frac{2}{3}\frac{h_2^2}{l_2}
$$

### Key Takeaways

- Cable assumes a **parabolic shape under UDL**
- Lowest point carries **only horizontal tension**
- Horizontal thrust depends on **span and support heights**
- Unequal support levels shift lowest point away from center

### Exam Tip

> In cables with different support levels, always take the **lowest point as origin** — it simplifies equations significantly.

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
