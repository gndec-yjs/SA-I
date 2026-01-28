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

<img src="images/internal_forces_placeholder.png" width="650" />

*Fig: Internal actions at a beam section (Axial force, Shear force, Bending moment)*

## Sign Conventions

A clear sign convention is essential for correct SFD/BMD and for avoiding sign errors in calculations.

### Sign Convention Used in This Course

- **Shear Force:** Clockwise $(+)$, Anticlockwise $(-)$  
- **Bending Moment:** Sagging $(+)$, Hogging $(-)$  

<img src="images/sign_convention_placeholder.png" width="650" />

*Fig: Sign convention for shear force and bending moment*

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

<img src="images/sfd_bmd_shapes_placeholder.png" width="700" />

*Fig: Typical SFD and BMD shapes for common loadings*

## Standard SFD/BMD Results (Quick Reference)

*(Useful for exam and fast checking of answers. Assume span $L$.)*

### Simply Supported Beam (SSB)

| Case | Maximum Shear | Maximum Bending Moment | Location of $M_{max}$ |
|---|---:|---:|---|
| Central point load $P$ | $V_{max} = P/2$ | $M_{max} = \frac{PL}{4}$ | Midspan |
| Eccentric point load $P$ at $a$ from left ($b=L-a$) | $V_{max} = \max(R_A, R_B)$ | $M_{max} = R_A a = R_B b$ | Under the load |
| UDL over entire span $w$ | $V_{max} = \frac{wL}{2}$ | $M_{max} = \frac{wL^2}{8}$ | Midspan |
| Triangular UVL (0 to $w$ over $L$) | depends on reactions | $M_{max}$ by $dM/dx=0$ | within span |

> For UVL and partial UDL cases, write $V(x)$ and $M(x)$ piecewise and locate maximum moment using $V(x)=0$.

### Cantilever Beam (Fixed at one end, free at other)

| Case | Shear at Fixed End | BM at Fixed End (Maximum) |
|---|---:|---:|
| Point load $P$ at free end | $V_{max}=P$ | $M_{max}=PL$ |
| UDL $w$ over full span | $V_{max}=wL$ | $M_{max}=\frac{wL^2}{2}$ |
| Triangular UVL (0 at free to $w$ at fixed) | $V_{max}=\frac{wL}{2}$ | $M_{max}=\frac{wL^2}{6}$ |
| End moment $M$ at free end | $V=0$ | $M_{max}=M$ |

<img src="images/standard_cases_placeholder.png" width="700" />

*Fig: Standard beam cases for quick reference*

## Overhang Beams (Introduction)

An **overhanging beam** is a beam which extends beyond one or both supports.  
Such beams commonly exhibit **negative bending moments near supports**, and may develop a **point of contraflexure**.

<img src="images/overhang_beam_placeholder.png" width="650" />

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

For a straight prismatic beam undergoing **small deflection**, the **differential equation of the elastic curve** (Euler–Bernoulli beam theory) is:

$$ EI\,\frac{d^2y}{dx^2}=M(x) $$

where  
$y$ = deflection at a distance $x$ from the reference origin,  
$E$ = modulus of elasticity,  
$I$ = second moment of area,  
$EI$ = flexural rigidity.

### Curvature–Slope–Deflection Relation

The curvature of the elastic curve is defined as:

$$ \kappa=\frac{1}{R} $$

For small slopes $(\theta \ll 1)$, the curvature is approximately:

$$ \kappa=\frac{d^2y}{dx^2} $$

and slope is:

$$ \theta=\frac{dy}{dx} $$

## Relations Between Load, Shear, Moment, Slope, Curvature and Deflection

<div style="border:1px solid #000; padding:12px; border-radius:6px;">

**(1) Rate of Loading → Shear**

$$ \boxed{\frac{dV}{dx}=-w(x)} $$

**(2) Shear → Moment**

$$ \boxed{\frac{dM}{dx}=V(x)} $$

**(3) Moment → Curvature**

$$ \boxed{\kappa=\frac{1}{R}=\frac{M(x)}{EI}} $$

**(4) Curvature → Slope**

$$ \boxed{\frac{d\theta}{dx}=\kappa=\frac{M(x)}{EI}} $$

**(5) Slope → Deflection**

$$ \boxed{\theta=\frac{dy}{dx}} $$

**(6) Combined Beam Differential Equation (Deflection Form)**

$$ \boxed{EI\,\frac{d^2y}{dx^2}=M(x)} $$

**(7) Higher-Order Form Linking Load to Deflection**

$$ \boxed{EI\,\frac{d^3y}{dx^3}=V(x)} $$
$$ \boxed{EI\,\frac{d^4y}{dx^4}=-w(x)} $$

</div>

### Sign Note (Common Convention)

If $w(x)$ is taken positive downward, then:

- $\dfrac{dV}{dx}=-w(x)$  
- $\dfrac{dM}{dx}=V(x)$  

(Keep the sign convention consistent throughout the problem.)

## Methods of Computing Deflections

Deflection of determinate beams can be computed using the following methods:

- **Direct Integration Method**
- **Moment–Area Method**
- **Conjugate Beam Method**
- **Energy Methods** (e.g., strain energy, Castigliano’s theorem, unit load method)

### Quick Comparison of Methods

| Method | Best Used For | Key Idea | Output |
|---|---|---|---|
| Direct integration | Simple beams with piecewise $M(x)$ | Integrate $M/EI$ to get $y$ | Slope & deflection |
| Moment–area | Beams with known $M/EI$ diagram | Areas and moments of $M/EI$ diagram | Change in slope & deflection |
| Conjugate beam | Beams with multiple segments | Convert deflection problem into shear/moment problem | Slope & deflection |
| Energy methods | Trusses/frames/beams; complex loads | Work–energy / strain energy | Deflection at a point |

<img src="images/deflection_methods_placeholder.png" width="700" />

*Fig: Overview of deflection calculation methods*

## Direct Integration Method

The governing equation:

$$ EI\frac{d^2y}{dx^2} = M(x) $$

Steps:
1. Write $M(x)$ for the beam (piecewise if needed).  
2. Integrate twice to obtain $\theta(x)=dy/dx$ and $y(x)$.  
3. Apply boundary conditions (supports/fixity) to evaluate constants.  

## Moment–Area Method

Two theorems:

1. **Change in slope** between two points equals the **area** under $M/EI$ between those points.  
2. **Deflection of a point** relative to tangent at another point equals the **moment of area** of $M/EI$ between the points.

## Conjugate Beam Method

A fictitious **conjugate beam** is formed such that:

- Load on conjugate beam $= M/EI$ of real beam  
- Shear in conjugate beam corresponds to slope in real beam  
- Moment in conjugate beam corresponds to deflection in real beam  

Support conditions change accordingly (fixed ↔ free, etc.)

## Energy Methods

Energy methods are powerful for deflection at a specific point.

Key idea:
- Strain energy stored in bending, axial and shear is used.
- Unit load method / Castigliano’s theorem are widely used.


[➤ Go to Index](#index)
