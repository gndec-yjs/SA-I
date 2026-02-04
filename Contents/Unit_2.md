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

## Unit 2: Internal Forces, SFD–BMD and Deflection of Determinate Structures

### Index
- [Internal Forces in Determinate Structures](#internal-forces-in-determinate-structures)
- [Sign Conventions](#sign-conventions)
- [Shear Force and Bending Moment Diagrams (SFD & BMD)](#shear-force-and-bending-moment-diagrams-sfd--bmd)
- [Point of Contraflexure (POC)](#point-of-contraflexure-poc)
- [Displacements: Deflection and Rotation](#displacements-deflection-and-rotation)
- [Methods of Computing Deflections](#methods-of-computing-deflections)
- [Double Integration Method](#double-integration-method)
- [Moment Area Method](#moment-area-method)

## Internal Forces in Determinate Structures

When a structure is subjected to external loads, **internal forces** develop within its members to maintain equilibrium.  
For beams and frames in the plane, the primary internal actions at a section are:

- **Axial Force ($N$):** internal force along the axis of the member (tension/compression)  
- **Shear Force ($V$):** transverse internal force at the section  
- **Bending Moment ($M$):** internal couple causing bending of the member  

### Classification of Internal Actions

| Internal Action | Symbol | Cause | Typical Effect |
|---|---|---|---|
| Axial force | $N$ | Loads along member axis | Change in length (tension/compression) |
| Shear force | $V$ | Transverse loads | Sliding tendency between sections |
| Bending moment | $M$ | Transverse loads / moments | Curvature (bending) |

<img width="500" height="372" alt="image" src="https://github.com/user-attachments/assets/de71c387-a6a2-4d89-aa98-c082f9102208" />

*Fig: Internal actions at a beam section (Axial force, Shear force, Bending moment)*

## Sign Conventions

A clear sign convention is essential for correct SFD/BMD and for avoiding sign errors in calculations.

### Sign Convention Used in This Course

- **Axial Force:** Tension $(+)$, Compression $(-)$ 
- **Shear Force:** Clockwise $(+)$, Anticlockwise $(-)$  
- **Bending Moment:** Sagging $(+)$, Hogging $(-)$  

<img width="907" height="363" alt="image" src="https://github.com/user-attachments/assets/c6cde39f-c688-4595-b656-bdf059fb1e04" />

*Fig: Sign convention for axial force, shear force and bending moment*

#### Axial Force

An axial force is regarded as positive if it tends to tier the member at the section under consideration. Such a force is regarded as tensile, while the member is said to be subjected to axial tension. On the other hand, an axial force is considered negative if it tends to crush the member at the section being considered. Such force is regarded as compressive, while the member is said to be in axial compression.

#### Shear Force

A shear force that tends to move the left of the section upward or the right side of the section downward will be regarded as positive. Similarly, a shear force that has the tendency to move the left side of the section downward or the right side upward will be considered a negative shear force (see Figure 4.2c and Figure 4.2d).

#### Bending Moment

A bending moment is considered positive if it tends to cause concavity upward (sagging). If the bending moment tends to cause concavity downward (hogging), it will be considered a negative bending moment

> **Note:** Different textbooks may adopt different sign conventions. Always remain consistent within a problem.

## Shear Force and Bending Moment Diagrams (SFD & BMD)

### Definitions

- **Shear Force at a section:** algebraic sum of transverse forces on either side of the section.  
- **Bending Moment at a section:** algebraic sum of moments of forces about the section on either side.

Mathematically, for a beam with coordinate $x$:

- $V(x)$ represents the shear force function  
- $M(x)$ represents the bending moment function  

### Fundamental Relationships

For a loaded beam:

$$ \frac{dV}{dx} = -w(x) $$
$$ \frac{dM}{dx} = V(x) $$

where $w(x)$ is the load intensity (positive downward as per common convention).

### General Rules (Very Important for Quick Drawing)

| Loading / Action | Effect on Shear Force (SFD) | Effect on Bending Moment (BMD) |
|---|---|---|
| Point load $P$ | Sudden jump by $P$ | Linear variation between loads |
| UDL $w$ | Linear variation | Parabolic variation |
| UVL (triangular/trapezoidal) | Parabolic variation | Cubic variation |
| Applied moment $M$ | No change in shear | Sudden jump in BM by $M$ |

<img width="512" height="640" alt="image" src="https://github.com/user-attachments/assets/829f998d-37a4-4f07-9752-7193781cbefc" />

*Fig: Typical SFD and BMD shapes for common loadings*

## Standard SFD/BMD Results (Quick Reference)

### Simply Supported Beam (SSB)

<img width="582" height="169" alt="image" src="https://github.com/user-attachments/assets/fdc75e83-2284-4af0-8879-b9688b378ffa" />

| Case | Maximum Shear | Maximum Bending Moment | Location of $M_{max}$ |
|---|---:|---:|---|
| Central point load $P$ | $V_{max} = P/2$ | $M_{max} = \frac{PL}{4}$ | Midspan |
| Eccentric point load $P$ at $a$ from left ($b=L-a$) | $V_{max} = \max(R_A, R_B)$ | $M_{max} = R_A a = R_B b$ | Under the load |
| UDL over entire span $w$ | $V_{max} = \frac{wL}{2}$ | $M_{max} = \frac{wL^2}{8}$ | Midspan |
| Triangular UVL (0 to $w$ over $L$) | depends on reactions | $M_{max}$ by $dM/dx=0$ | within span |

> For UVL and partial UDL cases, write $V(x)$ and $M(x)$ piecewise and locate maximum moment using $V(x)=0$.

### Cantilever Beam (Fixed at one end, free at other)

<img width="582" height="172" alt="image" src="https://github.com/user-attachments/assets/116e9fbb-19c0-4f89-8ca5-c90f75c26d80" />


| Case | Shear at Fixed End | BM at Fixed End (Maximum) |
|---|---:|---:|
| Point load $P$ at free end | $V_{max}=P$ | $M_{max}=PL$ |
| UDL $w$ over full span | $V_{max}=wL$ | $M_{max}=\frac{wL^2}{2}$ |
| Triangular UVL (0 at free to $w$ at fixed) | $V_{max}=\frac{wL}{2}$ | $M_{max}=\frac{wL^2}{6}$ |
| End moment $M$ at free end | $V=0$ | $M_{max}=M$ |

## Overhang Beams (Introduction)

An **overhanging beam** is a beam which extends beyond one or both supports.  
Such beams commonly exhibit **negative bending moments near supports**, and may develop a **point of contraflexure**.

<img width="558" height="308" alt="image" src="https://github.com/user-attachments/assets/78b0f58a-3403-4b3a-8f68-f4692a8ddcb0" />

*Fig: Typical overhanging beam*

## Point of Contraflexure (POC)

The **point of contraflexure** is the point on a beam where the **bending moment changes sign**, i.e.

$$ M(x)=0 \;\; \text{within the span (not at a support)} $$

At this point, curvature reverses from sagging to hogging (or vice-versa).

### Significance of POC

- Indicates change in curvature of elastic curve  
- Useful in approximate analysis of continuous beams and frames  
- Important for design detailing (regions of tension shift from one face to the other)

## Displacements: Deflection and Rotation

When a beam is loaded, it bends and develops:

- **Deflection ($y$):** transverse displacement of a point on the beam  
- **Slope / Rotation ($\theta$):** rotation of the tangent to the elastic curve  

## Elastic Curve Relations (Differential Equation of Deflection)

### **Bending Equation**

From bending theory,

$$ \frac{M}{I} = \frac{E}{R} $$

Since curvature $\dfrac{1}{R} = \dfrac{d^2y}{dx^2}$ for small deflections,

$$ M = EI\,\frac{d^2y}{dx^2} $$

This is the **fundamental differential equation of the elastic curve** of a straight beam.

### **Differential Equation of Deflection**

\[
\boxed{EI\,\frac{d^2y}{dx^2} = M(x)}
\]

where  
$y$ = deflection at distance $x$  
$E$ = modulus of elasticity  
$I$ = moment of inertia  
$EI$ = flexural rigidity  

### **Relation Between Shear Force and Deflection**

Differentiating bending equation w.r.t. $x$:

$$ \frac{dM}{dx} = EI\,\frac{d^3y}{dx^3} $$

But,

$$ \frac{dM}{dx} = V(x) $$

Therefore,

$$
\boxed{V(x) = EI\,\frac{d^3y}{dx^3}}
$$


### **Relation Between Load Intensity and Deflection**

Differentiating shear force w.r.t. $x$:

$$ \frac{dV}{dx} = EI\,\frac{d^4y}{dx^4} $$

But,

$$ \frac{dV}{dx} = w(x) $$

Therefore,

$$
\boxed{w(x) = EI\,\frac{d^4y}{dx^4}}
$$

### **Complete Relationship Chain**

\[
\boxed{
\begin{aligned}
\text{Deflection:} &\quad y \\
\text{Slope:} &\quad \theta = \frac{dy}{dx} \\
\text{Curvature:} &\quad \frac{1}{R} = \frac{d^2y}{dx^2} \\
\text{Bending Moment:} &\quad M = EI\,\frac{d^2y}{dx^2} \\
\text{Shear Force:} &\quad V = EI\,\frac{d^3y}{dx^3} \\
\text{Rate of Loading:} &\quad w = EI\,\frac{d^4y}{dx^4}
\end{aligned}
}
\]

</div>

### **Important Exam Note**

> The beam deflection problem is solved by integrating  
> $$ EI\,\frac{d^4y}{dx^4} = w(x) $$  
> and applying appropriate **boundary conditions** on deflection and slope.

### **Sign Convention Note**

If downward load $w(x)$ is taken positive, then:

$$
\frac{dV}{dx} = w(x), \quad \frac{dM}{dx} = V(x)
$$

(Keep sign convention consistent throughout analysis.)

## Methods of Computing Structural Deflections

Determination of structural displacements (deflection and rotation) is an essential part of structural analysis.  
Depending on the type of structure and loading, deflections can be computed using **geometric methods** or **energy methods**.

## **A) Geometric Methods**

These methods use the **elastic curve relations** directly and are best suited for **determinate beams**.

### **Methods included in syllabus (highlighted):**

- **Direct Integration Method** 
 
- **Moment–Area Method**

- **Conjugate Beam Method**

### Other geometric approaches:
- Macaulay’s Method (for discontinuous loads)

### **1. Direct Integration Method (Double Integration & Macaulay’s Method)**

Based on the fundamental relation:

$$ EI\,\frac{d^2y}{dx^2}=M(x) $$

By integrating twice and applying boundary conditions, slope and deflection are obtained.  
Macaulay’s method is a convenient extension to handle multiple discontinuous loads in a single equation.

### **2. Moment–Area Method**

Uses areas and first moments of the $M/EI$ diagram.

**Theorems:**

1. Change in slope between two points = Area under $M/EI$ diagram  
2. Deflection at a point = Moment of $M/EI$ area about that point

Efficient for beams with piecewise loading.

### **3. Conjugate Beam Method**

An imaginary **conjugate beam** is created where:

- Load on conjugate beam = $M/EI$ diagram of real beam  
- Shear in conjugate beam = slope in real beam  
- Moment in conjugate beam = deflection in real beam

Very useful for beams with multiple segments.

## **B) Energy Methods**

Energy methods are particularly effective for **trusses, frames, and complex loading systems**, where geometric methods become lengthy.

### **Different Energy Methods**

- Strain Energy Method 
- Castigliano’s Theorem  
- Unit Load Method 
- Virtual Work Principle  
- Maxwell–Betti Reciprocal Theorem  

### **1. Strain Energy Method**

Deflection is obtained by differentiating total strain energy $U$ with respect to applied load.

### **2. Castigliano’s Theorem**

For linearly elastic structures:

$$ \delta = \frac{\partial U}{\partial P} $$

where  
$\delta$ = deflection at load point  
$P$ = applied load  

### **3. Unit Load Method**

A virtual unit load is applied at the point of desired displacement.  
Deflection is computed using internal force work relations.

### **4. Maxwell–Betti Reciprocal Theorem**

States that the deflection at point A due to load at B equals deflection at B due to same load at A.

## **Quick Comparison of Deflection Methods**

| Method | Best Used For | Key Idea | Output |
|---|---|---|---|
| **Direct Integration** | Simple determinate beams | Integrate $M/EI$ | Slope & deflection |
| **Moment–Area** | Beams with known $M/EI$ diagram | Area & centroid of $M/EI$ | Change in slope & deflection |
| **Conjugate Beam** | Multi-segment beams | Convert deflection → shear/moment problem | Slope & deflection |
| **Energy Methods** | Trusses, frames, complex beams | Work–energy relations | Deflection at a point |

### **Exam Tip**

> **Geometric methods** are preferred for **determinate beams**,  
> while **energy methods** are preferred for **frames and trusses**.

## **Double Integration Method**

## Direct Integration Method – Fundamental Relations

From bending theory, the **bending moment at any section** of a beam is related to deflection by the differential equation:

$$ M = EI\,\frac{d^2y}{dx^2} $$

or

$$ \frac{d^2y}{dx^2} = \frac{M(x)}{EI} $$

This is the **basic differential equation of the elastic curve**.

### **First Integration — Slope Equation**

Integrating once with respect to $x$:

$$ \frac{dy}{dx} = \int \frac{M(x)}{EI}\,dx + C_1 $$

where  
$\dfrac{dy}{dx} = \theta$ = **slope of the elastic curve**,  
$C_1$ = constant of integration determined from boundary conditions.

### **Second Integration — Deflection Equation**

Integrating again:

$$ y = \int\!\!\int \frac{M(x)}{EI}\,dx\,dx + C_1 x + C_2 $$

where  
$y$ = **deflection of the beam**,  
$C_1,\;C_2$ = constants obtained from support boundary conditions.

### **Summary (Direct Integration Method)**

$$
\boxed{
\begin{aligned}
M(x) &= EI\,\frac{d^2y}{dx^2} \\[6pt]
\theta(x) &= \frac{dy}{dx} = \int \frac{M(x)}{EI}\,dx \\[6pt]
y(x) &= \int\!\!\int \frac{M(x)}{EI}\,dx\,dx
\end{aligned}
}
$$

### **Note**

> In the **Direct Integration Method**, integrate $M/EI$ **once** to obtain **slope**, integrate **twice** to obtain **deflection**, then apply boundary conditions to evaluate constants.

## Simply Supported Beam with Central Point Load — Double Integration Method

Consider a simply supported beam $AB$ of span $l$ carrying a **central point load** $W$ at midspan $C$.

<img width="1088" height="385" alt="image" src="https://github.com/user-attachments/assets/0c54217e-56f4-456a-aa2c-90611778524f" />

*Fig: Simply supported beam with a central point load*

### Step 1: Support Reactions

By symmetry,

$$ R_A = R_B = \frac{W}{2} $$

### Step 2: Bending Moment Expression

Take a section at a distance $x$ from the **left support $A$**.

For $0 \le x \le \frac{l}{2}$ (left half):

$$ M(x) = R_A x = \frac{W}{2}x $$

By symmetry, the same form applies for the right half, but for derivation we proceed with $0\le x\le l/2$ and use symmetry.

### Step 3: Differential Equation of Elastic Curve

Using the bending equation,

$$ EI\,\frac{d^2y}{dx^2} = M(x) $$

Substitute $M(x)=\dfrac{W}{2}x$:

$$ EI\,\frac{d^2y}{dx^2} = \frac{W}{2}x \qquad (1) $$

### Step 4: First Integration (Slope)

Integrate Eq. (1) w.r.t. $x$:

$$ EI\,\frac{dy}{dx} = \frac{W}{4}x^2 + C_1 \qquad (2) $$

At the centre $C$, slope is zero due to symmetry:

$$ x=\frac{l}{2},\;\; \frac{dy}{dx}=0 $$

Substitute in Eq. (2):

$$ 0 = \frac{W}{4}\left(\frac{l}{2}\right)^2 + C_1
= \frac{Wl^2}{16} + C_1 $$

Hence,

$$ C_1 = -\frac{Wl^2}{16} $$

Substitute $C_1$ in Eq. (2):

$$ EI\,\frac{dy}{dx} = \frac{W}{4}x^2 - \frac{Wl^2}{16} \qquad (3) $$

Therefore the slope equation is:

$$ \theta(x)=\frac{dy}{dx}=\frac{1}{EI}\left(\frac{W}{4}x^2-\frac{Wl^2}{16}\right) $$

### Maximum Slope (at Supports)

At $A$: $x=0$

$$ EI\,\theta_A = 0-\frac{Wl^2}{16} $$

$$ \boxed{\theta_A = -\frac{Wl^2}{16EI}} $$

At $B$ (by symmetry):

$$ \boxed{\theta_B = +\frac{Wl^2}{16EI}} $$

(negative sign indicates rotation in opposite sense as per sign convention.)

### Step 5: Second Integration (Deflection)

Integrate Eq. (3) w.r.t. $x$:

$$ EI\,y = \frac{W}{12}x^3 - \frac{Wl^2}{16}x + C_2 \qquad (4) $$

At support $A$: $x=0$, deflection $y=0$:

$$ 0 = 0 - 0 + C_2 \Rightarrow C_2 = 0 $$

Hence,

$$ EI\,y = \frac{W}{12}x^3 - \frac{Wl^2}{16}x \qquad (5) $$

So the deflection equation is:

$$ y(x)=\frac{1}{EI}\left(\frac{W}{12}x^3-\frac{Wl^2}{16}x\right) $$

### Maximum Deflection (at Midspan)

At centre $C$: $x=\dfrac{l}{2}$

$$ EI\,y_C = \frac{W}{12}\left(\frac{l}{2}\right)^3 - \frac{Wl^2}{16}\left(\frac{l}{2}\right) $$

$$ EI\,y_C = \frac{Wl^3}{96} - \frac{Wl^3}{32}
= \frac{Wl^3}{96} - \frac{3Wl^3}{96}
= -\frac{2Wl^3}{96}
= -\frac{Wl^3}{48} $$

Therefore,

$$ \boxed{y_C = -\frac{Wl^3}{48EI}} $$

Magnitude of maximum deflection:

$$ \boxed{|y_{max}|=\frac{Wl^3}{48EI}} $$

(Negative sign indicates downward deflection.)

## Final Results (For Quick Use)

$$
\boxed{
\begin{aligned}
R_A &= R_B = \frac{W}{2} \\[6pt]
\theta_A &= -\frac{Wl^2}{16EI},\qquad \theta_B = +\frac{Wl^2}{16EI} \\[6pt]
y_{max} &= y_C = -\frac{Wl^3}{48EI}
\end{aligned}}
$$

## Example Problem — Simply Supported Beam with Central Point Load

### Problem Statement

A simply supported beam of span **3 m** is subjected to a **central point load of 10 kN**.  
Find:

1. **Maximum slope** of the beam  
2. **Maximum deflection** of the beam  

**Given Data:**

- Span, $l = 3\,\text{m} = 3000\,\text{mm}$  
- Central load, $W = 10\,\text{kN} = 10,000\,\text{N}$  
- Moment of inertia, $I = 12 \times 10^6 \,\text{mm}^4$  
- Modulus of elasticity, $E = 200\,\text{GPa} = 200 \times 10^3 \,\text{N/mm}^2$

### Solution:

For a simply supported beam with a central point load:

**Maximum slope (at supports):**

$$ \theta_{max} = \frac{Wl^2}{16EI} $$

**Maximum deflection (at midspan):**

$$ y_{max} = \frac{Wl^3}{48EI} $$

#### (1) Maximum Slope

$$
\theta_A = \frac{Wl^2}{16EI}
= \frac{10,000 \times (3000)^2}
{16 \times 200\times10^3 \times 12\times10^6}
$$

$$
\boxed{\theta_A = 0.0023 \text{ radians}}
$$

By symmetry:

$$ \theta_B = 0.0023 \text{ radians} $$

#### (2) Maximum Deflection

$$
y_C = \frac{Wl^3}{48EI}
= \frac{10,000 \times (3000)^3}
{48 \times 200\times10^3 \times 12\times10^6}
$$

$$
\boxed{y_C = 2.34 \text{ mm}}
$$

### Answers

$$
\boxed{
\begin{aligned}
\theta_{max} &= 0.0023 \text{ radians} \\
y_{max} &= 2.34 \text{ mm (downward)}
\end{aligned}
}
$$

### Exam Tip

> Always convert all quantities to **consistent units** before substitution.  
> Maximum slope occurs at **supports**, and maximum deflection occurs at **midspan** for a centrally loaded simply supported beam.

## Example Problem — Load Required for Given Central Deflection

### Problem Statement

A wooden beam **140 mm wide** and **240 mm deep** has a span of **4 m**.  
Determine the **load $W$** that must be applied at the **centre** to cause a **deflection of 10 mm** at the centre of the beam.  

Take **$E = 6$ GPa**.

### Given Data

- Width, $b = 140 \text{ mm}$  
- Depth, $d = 240 \text{ mm}$  
- Span, $l = 4 \text{ m} = 4000 \text{ mm}$  
- Central deflection, $y_C = 10 \text{ mm}$  
- Modulus of elasticity,  
  $E = 6 \text{ GPa} = 6000 \text{ N/mm}^2$

### Step 1: Moment of Inertia of Beam Section

For a rectangular section,

$$ I = \frac{bd^3}{12} $$

Substituting,

$$
I = \frac{140 \times (240)^3}{12}
= 1.613 \times 10^8 \text{ mm}^4
$$

### Step 2: Deflection Formula

For a simply supported beam with a **central point load**,

$$ y_C = \frac{Wl^3}{48EI} $$

Given $y_C = 10$ mm. Substituting values:

$$
10 = \frac{W(4000)^3}
{48 \times 6000 \times 1.613\times10^8}
$$

### Step 3: Solve for Load $W$

$$
W = \frac{10 \times 48 \times 6000 \times 1.613\times10^8}
{(4000)^3}
$$

$$
\boxed{W = 7258.5 \text{ N}}
$$

or

$$
\boxed{W \approx 7.25 \text{ kN}}
$$

## Moment Area Method

The **Moment–Area Method** is a geometric method used to determine **slopes and deflections** in beams.  
It is based on two fundamental theorems which relate the **area and moment of the $M/EI$ diagram** to slope and deflection of the elastic curve.

## Moment–Area Theorems (or Mohr's Theorems)

### **Theorem 1 — Change in Slope**

**Statement:**  
The **change in slope** between any two points on a beam is equal to the **area of the $M/EI$ diagram** between those two points.

Let $C$ and $D$ be two points on a beam under flexure. Then,

$$
\theta_{CD} = \int_C^D \frac{M(x)}{EI}\,dx
$$

**Where:**

- $M(x)$ = Bending moment at section  
- $E$ = Young’s modulus  
- $I$ = Moment of inertia  
- $EI$ = Flexural rigidity  
- $\theta_{CD}$ = Change in slope between points $C$ and $D$

**Interpretation:**  
The **area under the $M/EI$ curve** between two points gives the **change in slope**.

### **Theorem 2 — Deflection**

**Statement:**  
The **deflection at a point** on a beam (measured from the tangent drawn at another point) is equal to the **moment of the $M/EI$ diagram** between the two points about the point where deflection is required.

If deflection at point $C$ is measured from the tangent at point $D$:

$$
\Delta_C = \int_C^D x \frac{M(x)}{EI}\,dx
$$

**Where:**

- $x$ = Distance of elemental area from the reference point  
- $\Delta_C$ = Deflection at point $C$

**Interpretation:**  
The **first moment of area** of the $M/EI$ diagram gives the **deflection**.

<img width="693" height="726" alt="image" src="https://github.com/user-attachments/assets/443a484e-7565-4803-9112-161f062cc8fa" />

*Fig: Elastic curve of a beam and corresponding $M/EI$ diagram for Moment–Area Method*

## Derivation of Moment–Area Theorems

From the **flexure formula**:

$$
\frac{M}{I} = \frac{E}{R}
$$

Rearranging:

$$
\frac{1}{R} = \frac{M}{EI}
$$

<img width="1168" height="520" alt="image" src="https://github.com/user-attachments/assets/ab3d45df-5a46-42e3-9769-f6ece2552418" />

For small deflections:

$$
d\theta = \frac{dx}{R}
$$

Substituting:

$$
d\theta = \frac{M}{EI} dx
$$

Integrating between $C$ and $D$:

$$
\theta_{CD} = \int_C^D \frac{M(x)}{EI} dx
$$

Hence, **Theorem 1 is proved.**

Now, elemental deflection is:

$$
d\Delta = x\,d\theta
$$

Substituting $d\theta$:

$$
d\Delta = x \frac{M}{EI} dx
$$

Integrating:

$$
\Delta_C = \int_C^D x \frac{M(x)}{EI} dx
$$

Hence, **Theorem 2 is proved.**

## Key Relations Summary

$$
\boxed{\theta = \int \frac{M}{EI} dx}
$$

$$
\boxed{\Delta = \int x \frac{M}{EI} dx}
$$

## Important Notes

- Method is **purely geometric**
- Requires known **bending moment diagram**
- Best suited for **statically determinate beams**
- Avoids solving differential equations directly

## Example — Cantilever Beam with Point Load at Free End (Moment–Area Method)

### Problem Statement

Determine the **rotation** and **deflection** at the **free end** of a cantilever beam of span $L$, subjected to a **point load $W$** at the free end.

### Solution: (Using Area $A$ and First Moment $A\bar{x}$)


### Beam and Bending Moment Diagram

<img width="555" height="156" alt="image" src="https://github.com/user-attachments/assets/c3a2e376-6ac0-4bc0-8325-796532d21cd8" />

*Fig: Cantilever beam with point load $W$ at free end*

<img width="543" height="206" alt="image" src="https://github.com/user-attachments/assets/f374bf7d-d987-45d5-ab37-b9e07af7c70a" />

*Fig: Bending moment diagram for cantilever with end point load*

In Moment–Area Method, we can avoid integration by using:

- **Theorem 1:** Change in slope = **Area** of $M/EI$ diagram  
  $$ \theta = A $$
- **Theorem 2:** Deflection = **First moment of area** of $M/EI$ diagram about the point where deflection is measured  
  $$ \Delta = A\bar{x} $$

## Step 1: $M/EI$ Diagram

For a cantilever with point load $W$ at free end, taking $x$ from the **free end**:

$$
M(x)=Wx
$$

Hence $M/EI$ diagram is a **triangle** of base $L$ with maximum ordinate at fixed end:

$$
h=\left(\frac{M}{EI}\right)_{\max}=\frac{WL}{EI}
$$

## Rotation at Free End ($\theta_B$)

Slope at fixed end is zero:

$$
\theta_A = 0
$$

So rotation at free end:

$$
\theta_B = \theta_{BA} = \text{Area of } \left(\frac{M}{EI}\right)\text{ diagram}
$$

Area of triangular $M/EI$ diagram:

$$
A = \frac{1}{2}\times (\text{base}) \times (\text{height})
= \frac{1}{2}\times L \times \frac{WL}{EI}
$$

$$
\boxed{\theta_B = \frac{WL^2}{2EI}}
$$

Direction: **clockwise**.

## Deflection at Free End ($\Delta_B$)

Deflection of free end $B$ with respect to tangent at fixed end $A$:

$$
\Delta_B = A\bar{x}
$$

For a triangular area, centroid lies at:

- $\bar{x}=\frac{L}{3}$ from the **larger ordinate end** (fixed end), or  
- $\bar{x}=\frac{2L}{3}$ from the **zero ordinate end** (free end)

Since we need moment about the **fixed end** (larger ordinate end), use:

$$
\bar{x}=\frac{L}{3}
$$

Hence,

$$
\Delta_B = A\bar{x}
= \left(\frac{1}{2}L\cdot\frac{WL}{EI}\right)\left(\frac{L}{3}\right)
$$

$$
\boxed{\Delta_B = \frac{WL^3}{3EI}}
$$

Direction: **downward**.

## Final Results

$$
\boxed{
\begin{aligned}
\theta_B &= \frac{WL^2}{2EI} \quad \text{(clockwise)} \\[6pt]
\Delta_B &= \frac{WL^3}{3EI} \quad \text{(downward)}
\end{aligned}}
$$

</div>

## Note (Triangle $M/EI$ Diagram)

For a triangular $M/EI$ diagram of base $L$ and maximum ordinate $h$:

- Area: $$A=\frac{1}{2}Lh$$
- Centroid location: $$\bar{x}=\frac{L}{3}\text{ from larger ordinate end}$$  
  or $$\bar{x}=\frac{2L}{3}\text{ from zero end}$$

This is the quickest way to apply Moment–Area Method without integration.

---

## OR

---

### Alternative Solution: (Using Integration)

### Step 1: Bending Moment Expression

Take $x$ measured from the **free end**.

At a section at distance $x$ from the free end:

$$
M(x) = Wx
$$

Hence, the $M/EI$ diagram is **triangular** with maximum ordinate at the fixed end equal to:

$$
\left(\frac{M}{EI}\right)_{\max} = \frac{WL}{EI}
$$

## Rotation at the Free End

Slope at the fixed end is zero:

$$
\theta_A = 0
$$

From **Moment–Area Theorem 1**:

$$
\theta_B = \int_0^L \frac{M(x)}{EI}\,dx
$$

Substitute $M(x)=Wx$:

$$
\theta_B = \int_0^L \frac{Wx}{EI}\,dx
= \frac{W}{EI}\int_0^L x\,dx
$$

$$
\theta_B = \frac{W}{EI}\left[\frac{x^2}{2}\right]_0^L
= \frac{WL^2}{2EI}
$$

**Rotation direction:** Clockwise at free end.

## Deflection at the Free End

From **Moment–Area Theorem 2**:

$$
\Delta_B = \int_0^L x\,\frac{M(x)}{EI}\,dx
$$

Substitute $M(x)=Wx$:

$$
\Delta_B = \int_0^L x\frac{Wx}{EI}\,dx
= \frac{W}{EI}\int_0^L x^2\,dx
$$

$$
\Delta_B = \frac{W}{EI}\left[\frac{x^3}{3}\right]_0^L
= \frac{WL^3}{3EI}
$$

**Deflection direction:** Downward at free end.

$$
\boxed{
\begin{aligned}
\theta_B &= \frac{WL^2}{2EI} \quad \text{(rotation at free end)} \\[6pt]
\Delta_B &= \frac{WL^3}{3EI} \quad \text{(deflection at free end)}
\end{aligned}
}
$$

</div>

## Note: (Triangle $M/EI$ Diagram)

For a triangular diagram of base $L$ and maximum ordinate $h$:

- Area = $\frac{1}{2}Lh$
- Centroid lies at $L/3$ from the larger ordinate end  
  (or $2L/3$ from the zero end)

This provides a quick shortcut for moment–area calculations.

### Note:

> Always remember fixed-end slope = **zero boundary condition**.


## Example — Cantilever Beam with Full UDL (Moment–Area Method)

### Problem Statement

Determine the **rotation** and **deflection** at the **free end** of a cantilever beam of span $L$, subjected to a **uniformly distributed load $w$** over the entire length.

### Solution: (Using Area $A$ and First Moment $A\bar{x}$)

### Beam and Bending Moment Diagram

<img width="706" height="227" alt="image" src="https://github.com/user-attachments/assets/fe668056-a03e-4fab-91aa-32fa7cc3f32e" />

*Fig: Cantilever beam with UDL over entire span*

<img width="706" height="227" alt="image" src="https://github.com/user-attachments/assets/31f538c4-54d7-41a1-b12b-db67b507eabe" />

*Fig: Parabolic bending moment diagram for cantilever with full UDL*

Moment–Area Theorems:

- **Theorem 1:** Change in slope = **Area** of $M/EI$ diagram  
  $$\theta = A$$
- **Theorem 2:** Deflection = **First moment of area** of $M/EI$ diagram about the point where deflection is required  
  $$\Delta = A\bar{x}$$

## Step 1: $M/EI$ Diagram

For a cantilever with UDL $w$ over entire span, taking $x$ from the **free end**:

$$
M(x)=\frac{wx^2}{2}
$$

Maximum bending moment occurs at the fixed end ($x=L$):

$$
M_{\max}=\frac{wL^2}{2}
$$

Hence, maximum ordinate of $M/EI$ diagram is:

$$
h=\left(\frac{M}{EI}\right)_{\max}=\frac{wL^2}{2EI}
$$

The $M/EI$ diagram is a **parabola** (opening upward) from 0 at free end to $h$ at fixed end.

## Rotation at Free End ($\theta_B$)

Slope at fixed end is zero:

$$
\theta_A=0
$$

So, rotation at free end:

$$
\theta_B = \text{Area of } \left(\frac{M}{EI}\right)\text{ diagram}
$$

For a parabolic diagram of base $L$ and end ordinate $h$ (zero at one end):

$$
A=\frac{1}{3}Lh
$$

Substitute $h=\dfrac{wL^2}{2EI}$:

$$
\theta_B=\frac{1}{3}L\left(\frac{wL^2}{2EI}\right)
$$

$$
\boxed{\theta_B=\frac{wL^3}{6EI}}
$$

Direction: **clockwise**.

## Deflection at Free End ($\Delta_B$)

Deflection of $B$ with respect to tangent at $A$:

$$
\Delta_B = A\bar{x}
$$

For a parabolic area (zero at free end, max at fixed end), centroid lies at:

$$
\bar{x}=\frac{3L}{4}
$$

measured from the **zero ordinate end** (free end).  
Therefore, from the **fixed end**, centroid distance is:

$$
\bar{x}_{A}=L-\frac{3L}{4}=\frac{L}{4}
$$

Since we need the **moment about the fixed end**, use $\bar{x}_A = \dfrac{L}{4}$:

$$
\Delta_B = A\left(\frac{L}{4}\right)
$$

Substitute $A=\dfrac{1}{3}Lh$ and $h=\dfrac{wL^2}{2EI}$:

$$
\Delta_B=\left(\frac{1}{3}L\cdot\frac{wL^2}{2EI}\right)\left(\frac{L}{4}\right)
$$

$$
\boxed{\Delta_B=\frac{wL^4}{8EI}}
$$

Direction: **downward**.

$$
\boxed{
\begin{aligned}
\theta_B &= \frac{wL^3}{6EI} \quad \text{(clockwise)} \\[6pt]
\Delta_B &= \frac{wL^4}{8EI} \quad \text{(downward)}
\end{aligned}}
$$

</div>

## Note (Parabolic $M/EI$ Diagram Quick Geometry)

For a parabolic $M/EI$ diagram with:

- base $=L$
- zero ordinate at one end
- maximum ordinate $=h$ at the other end

Then:

$$
A=\frac{1}{3}Lh
$$

Centroid location:

- $\bar{x}=\frac{3L}{4}$ from the **zero ordinate end**
- $\bar{x}=\frac{L}{4}$ from the **maximum ordinate end**

---

## OR

---

### Alternative Solution (Using Integration)

### Step 1: Bending Moment Expression

Taking $x$ measured from the **free end**:

$$
M(x) = \frac{w x^2}{2}
$$

## Rotation at the Free End

Let $A$ be the fixed end and $B$ the free end.

Since slope at the fixed end is zero:

$$
\theta_A = 0
$$

From **Moment–Area Theorem 1**:

$$
\theta_B = \int_0^L \frac{M(x)}{EI} dx
$$

Substitute $M(x)$:

$$
\theta_B = \int_0^L \frac{w x^2}{2EI} dx
$$

$$
\theta_B = \frac{w}{2EI} \int_0^L x^2 dx
$$

$$
\theta_B = \frac{w}{2EI}\left[\frac{x^3}{3}\right]_0^L
$$

$$
\theta_B = \frac{wL^3}{6EI}
$$

**Rotation direction:** Clockwise at free end.

## Deflection at the Free End

From **Moment–Area Theorem 2**:

$$
\Delta_B = \int_0^L x \frac{M(x)}{EI} dx
$$

Substitute $M(x)$:

$$
\Delta_B = \int_0^L x \frac{w x^2}{2EI} dx
$$

$$
\Delta_B = \frac{w}{2EI} \int_0^L x^3 dx
$$

$$
\Delta_B = \frac{w}{2EI}\left[\frac{x^4}{4}\right]_0^L
$$

$$
\Delta_B = \frac{wL^4}{8EI}
$$

**Deflection direction:** Downward at free end.

$$
\boxed{
\begin{aligned}
\theta_B &= \frac{wL^3}{6EI} \quad \text{(rotation at free end)} \\[6pt]
\Delta_B &= \frac{wL^4}{8EI} \quad \text{(deflection at free end)}
\end{aligned}
}
$$

</div>

## Note: (From Geometry of Parabolic $M/EI$ Diagram)

For a **parabolic $M/EI$ diagram**:

- **Area** = $\frac{1}{3} \times (\text{base}) \times (\text{maximum ordinate})$
- **Centroid** lies at **$3L/4$** from the end where ordinate is zero

This simplifies manual calculations in moment–area problems.

## Example — Simply Supported Beam with Central Point Load (Moment–Area Method)

### Problem Statement

A simply supported beam $AB$ of span $L$ carries a **central point load $W$** at midspan $C$.  
Determine:

- Slopes at the supports: $\theta_A$ and $\theta_B$  
- Deflection at midspan: $\Delta_C$

### Solution:

### Beam and Bending Moment Diagram

<img width="575" height="935" alt="image" src="https://github.com/user-attachments/assets/a07e5256-b18e-44f0-83d9-6227125a0c80" />

*Fig: Simply supported beam with central point load $W$ at $C$, M/EI diagram, and elastic curve*

### Problem Statement

Determine the **slopes at supports** and **deflection at midspan** for a **simply supported beam** $AB$ of span $L$, subjected to a **central point load $W$** at midspan $C$, using the **Moment–Area Method**.

### Solution:

### Beam and Bending Moment Diagram

<img src="images/ssb_central_load_placeholder.png" width="700"/>

*Fig: Simply supported beam with central point load*

<img src="images/ssb_central_load_bmd_placeholder.png" width="700"/>

*Fig: Triangular bending moment diagram*

### Step 1: Reactions at Supports

Due to symmetry,

$$
R_A = R_B = \frac{W}{2}
$$

Maximum bending moment occurs at midspan:

$$
M_{max} = \frac{WL}{4}
$$

The bending moment diagram is triangular on each half.

### Step 2: Area of $M/EI$ Diagram

Consider only half span ($B$ to $C$).

The $M/EI$ diagram is triangular with:

- Base = $\frac{L}{2}$
- Height = $\frac{WL}{4EI}$

Area of triangle:

$$
A = \frac{1}{2} \times \frac{L}{2} \times \frac{WL}{4EI}
= \frac{WL^2}{16EI}
$$


## Slope at Supports

From **Moment–Area Theorem 1**,

Change in slope between $B$ and $C$ equals area of $M/EI$ diagram.

At midspan,

$$
\theta_C = 0
$$

Hence,

$$
\theta_B = A
$$

Therefore,

$$
\boxed{
\theta_B = \frac{WL^2}{16EI}
}
$$

By symmetry,

$$
\boxed{
\theta_A = \frac{WL^2}{16EI}
}
$$

Rotation directions are opposite at the two supports.

## Deflection at Midspan

Using **Moment–Area Theorem 2**, deflection of $C$ with respect to tangent at $B$ equals moment of $M/EI$ area between $B$ and $C$ about point $B$.

Centroid of triangle lies at:

$$
\frac{1}{3} \times \frac{L}{2} = \frac{L}{6}
$$

from the larger ordinate end (midspan).

Distance of centroid from $B$:

$$
\frac{L}{2} - \frac{L}{6} = \frac{L}{3}
$$

Hence,

$$
\Delta_C = A \times \bar{x}
$$

$$
\Delta_C = \frac{WL^2}{16EI} \times \frac{L}{3}
$$

$$
\boxed{
\Delta_C = \frac{WL^3}{48EI}
}
$$

Deflection is downward.

$$
\boxed{
\begin{aligned}
\theta_A &= \theta_B = \frac{WL^2}{16EI} \\
\Delta_C &= \frac{WL^3}{48EI}
\end{aligned}
}
$$




[➤ Go to Index](#index)
