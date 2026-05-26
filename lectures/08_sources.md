# Chapter 9: Beachballs, Focal Mechanisms, and Moment Tensors

## Purpose

In previous chapters, we focused primarily on seismic wave propagation through the Earth. In this chapter, we shift our attention to the **earthquake source itself** and how fault motion generates seismic waves.

In this chapter, we will:

- describe earthquake fault geometry and slip
- develop the double-couple model of earthquake sources
- examine P- and S-wave radiation patterns
- learn how focal mechanisms and beachball diagrams are used to infer fault motion
- introduce moment tensors as a mathematical description of earthquake sources

---

## Reading

Shearer Chapter 9: Earthquakes and Source Theory

- Section 9.2: Earthquake faults
- Section 9.3: Radiation Patterns and Beachballs
- Section 9.1: Green's functions and the Moment Tensor

---
# Earthquake Faults

## Earthquake Fault Geometry

Earthquakes are modeled as slip across a fault plane.

Fault orientation is described by:
- **Strike** ($\phi$): direction of the fault trace on the surface
- **Dip** ($\delta$): angle of the fault relative to horizontal
- **Rake** ($\lambda$): direction of slip measured within the fault plane from the strike direction.
  - $\lambda = 0^\circ$ → left-lateral strike slip
  - $\lambda = 180^\circ$ → right-lateral strike slip
  - $\lambda = 90^\circ$ → reverse faulting
  - $\lambda = -90^\circ$ (or $270^\circ$) → normal faulting

```{figure} ../figures/08_fault_geometry.png
---
name: Fault Geometry
alt: Fault Geometry defined by strike, rake, and dip.
width: 400px
---
A planar fault is defined by the strike and dip of the fault surface and the direction of the slip vector.
```

Common fault types:

- **Normal fault**
  - hanging wall moves downward
  - associated with extension

- **Reverse / thrust fault**
  - hanging wall moves upward
  - associated with compression

- **Strike-slip fault**
  - horizontal motion along the fault
  - right-lateral or left-lateral

👉 Fault geometry controls the earthquake radiation pattern and moment tensor.

---

## Beachball Diagrams

Fault motion is commonly displayed using lower-hemisphere projections called **beachball diagrams**.

```{figure} ../figures/09_beachballs.jpg
---
name: Focal mechanisms
width: 600px
alt: Examples of strike-slip, normal, and reverse fault focal mechanisms. 
---
Examples of focal spheres and their corresponding fault geometries. The lower half of the focal sphere is plotted to the left, with the compressional quadrants shaded. The block diagrams on the right show the two fault geometries (the primary and auxiliary fault planes) that could have produced the observed radiation pattern.
```

Interpretation:
- Black = compressional first motions
- White = dilatational first motions
- Normal faults → white center
- Reverse faults → black center
- Strike-slip faults → four-quadrant pattern



---

# Radiation Patterns

## Far-Field P-Wave Radiation

Far from the earthquake source, the observed seismic waves are dominated by the **far-field radiation**:

For a double-couple earthquake source:

- P-wave amplitudes decay approximately as:

$$
u^P \propto \frac{1}{r}
$$

- Radiation depends strongly on direction relative to the fault geometry
- Some directions produce compressional first motions
- Other directions produce dilatational first motions
- Certain directions produce no P-wave motion at all (nodal planes)

For a double-couple source, P-wave amplitude depends strongly on takeoff direction and azimuth relative to the fault.

👉 Earthquakes radiate seismic energy directionally rather than equally in all directions.

```{figure} ../figures/08_focal_springs.mp4
---
width: 600px
---
Ground motion visualization for P-wave radiation.
```

---

## P-Wave Radiation Pattern

```{figure} ../figures/09_p_radiation.png
---
name: P-wave radiation pattern
width: 500px
alt: P-wave radiation pattern for a double-couple source. 
---
The far-field radiation pattern for P-waves (top) for a double-couple source. The orientation of the small arrows shows the direction of first motion; their length is proportional to the wave amplitude. The primary and auxiliary fault planes are shown as heavy lines; the compressional quadrants are shaded. P-wave first motions are outward in the compressional quadrant and inward in the dilatational quadrant with nodal lines in between. Because of the ambiguity between the primary and auxiliary fault planes, the positions of the slip and fault normal vectors could be reversed.
```

Features:
- Four quadrants of alternating polarity
- Fault plane and auxiliary plane are nodal planes
- Outward motion = compressional quadrant
- Inward motion = dilatational quadrant

Definitions:
- **T-axis** = center of compressional quadrant
- **P-axis** = center of dilatational quadrant

---

## Far-Field S-Wave Radiation

S-wave radiation from a double-couple source is also directional.

Key features:
- S-wave amplitudes decay approximately as:

$$
u^S \propto \frac{1}{r}
$$

- S-wave radiation patterns differ from P-wave patterns
- S waves have nodal points rather than nodal planes
- S-wave particle motion is transverse to propagation direction

For a double-couple source, the angular dependence of S-wave radiation is more complicated than for P waves and depends on both:
- takeoff direction
- polarization direction

👉 Radiation patterns control which stations record strong or weak S-wave amplitudes.

---

## S-Wave Radiation Pattern

```{figure} ../figures/09_s_radiation.png
---
name: S-wave radiation pattern
width: 500px
alt: S-wave radiation pattern for a double-couple source. 
---
The far-field radiation pattern for S-waves for a double-couple source. The orientation of the small arrows shows the direction of first motion; their length is proportional to the wave amplitude. The primary and auxiliary fault planes are shown as heavy lines; the compressional quadrants are shaded. S-wave first motions are generally away from the pressure axis and toward the tension axis; there are 6 nodal points and no nodal lines in S. 
```

Features:
- More complicated than P-wave radiation
- No nodal planes
- Radiation strongest away from nodal directions
- Polarization depends on observation direction

👉 Radiation patterns control which stations record large or small amplitudes.

---

# Determining Focal Mechanisms from Seismic Observations

## Earthquake Focal Mechanisms

P-wave first motions can be used to determine earthquake focal mechanisms and represented graphically with beachballs.

Step 1: Determine whether first motion is upward or downward

```{figure} ../figures/09_up_down.png
---
width: 800px
---
Example showing up and down first motions.
```

Step 2: Make polarity measurements on many stations

```{figure} ../figures/09_polarity_observations.png
---
width: 600px
---
Polarity observations on many stations.
```

Step 3: Project rays back to the source and plot takeoff angles on the focal sphere

```{figure} ../figures/09_takeoff_angles.png
---
width: 300px
---
Polarity observations on the focal sphere.
````

Step 4: Find two orthogonal nodal planes separating compressional and dilatational quadrants

```{figure} ../figures/09_focal_mechanism.png
---
width: 600px
---
Fitting a focal mechanism.
````

👉 The focal mechanism provides strike, dip, and rake information.

---

## Applications in Seismotectonics

Focal mechanisms are useful for:

- Mapping tectonic stress regimes
- Distinguishing crustal vs. subduction-zone deformation
- Understanding earthquake sequences and fault interactions
- Improving seismic hazard assessment

```{figure} ../figures/09_mendo_fms.jpg
---
width: 600px
---
Focal mechanisms of the Mendocino Transform Fault from Dengler et al. (1994)
````

```{figure} ../figures/09_ridgecrest.png
---
width: 800px
---
Focal mechanisms of the Ridgecrest aftershock sequence from Atterholt et al. (2025)
````

---

## Stress and Focal Mechanisms

The P and T axes are related to the stress field, but a single focal mechanism does not uniquely determine the stress tensor.

Why?

- The true fault plane is ambiguous
- Faults do not always occur on planes of maximum shear stress

Many focal mechanisms together within a common stress field can be used to estimate principal stress orientations.  This approach is widely used in tectonics and earthquake seismology.

___

# Seismic Moment

## Scalar Seismic Moment

The overall size of an earthquake is described by the:

> **Scalar seismic moment**
$$
M_0 = \mu D A
$$

where:
- $\mu$ = shear modulus
- $D$ = average slip
- $A$ = rupture area

```{figure} ../figures/09_seismogenic_zone.gif
---
name: Rupture length, width, and slip
alt: Fault Geometry defined by strike, rake, and dip.
width: 500px
---
Rupture length, width, and slip.
```

Larger earthquakes result from:
- larger rupture area
- larger fault slip
- or stronger rocks

👉 Seismic moment is the fundamental physical measure of earthquake size.  It is the physical basis for the moment magnitude scale.

---

## Moment Magnitude

> **Moment Magnitude** is defined as 
$$
M_w = 2/3 log(M_0)-10.7
$$

where:

- $M_0$ must be in units of dyne-cm (1 dyne-cm=$10^{-7}$ N-m)
- Moment magnitude ($M_w$) is based upon the scalar seismic moment, and represents a kind of bridge between the seismological and geological views of an earthquake.
- $M_w$ is a more consistent measure of big earthquakes and relates magnitude to physical quantities
- Moment magnitude doesn’t suﬀer from the saturation issues that other magnitude scales

---

## Example: Computing Scalar Seismic Moment

Assume an earthquake occurs with length 100 km, depth 12 km, average slip of 6 m and that the shear modulus is 30 Gpa. What is the scalar seismic moment of such an event? What are the units?

The scalar seismic moment is

$$
M_0 = \mu D A
$$

where:
- $\mu = 30 \,\text{GPa} = 30 \times 10^9 \,\text{Pa}$
- $D = 6 \,\text{m}$
- $A = LW$

The rupture area is:

$$
A = (100\,\text{km})(12\,\text{km})
$$

Converting to meters:

$$
A = (1.0\times10^5\,\text{m})(1.2\times10^4\,\text{m})
=1.2\times10^9\,\text{m}^2
$$

Thus,

$$
M_0
=
(30\times10^9\,\text{Pa})
(6\,\text{m})
(1.2\times10^9\,\text{m}^2)
$$

$$
M_0 = 2.16\times10^{20}\,\text{N}\cdot\text{m}
$$

The units of scalar seismic moment are:

$$
\boxed{\text{N}\cdot\text{m}}
$$

What is the moment magnitude of the previous earthquake? 

Moment magnitude is related to scalar seismic moment by:

$$
M_w = \frac{2}{3}\log_{10}(M_0) - 10.7
$$

where:
- $M_0$ must be in units of dyne-cm

Using:

$$
M_0 = 2.16\times10^{27}\,\text{dyne-cm}
$$

First compute the logarithm:

$$
\log_{10}(2.16\times10^{27})
=
27.33
$$

Then:

$$
M_w
=
\frac{2}{3}(27.33)-10.7
$$

$$
\boxed{M_w \approx 7.5}
$$


How do the moment and magnitude change if we increase slip to 8 m?

---

# Green's Functions and the Moment Tensor

## The Forward Problem in Seismology

One of the central goals of seismology is the **forward problem**:

> Given an earthquake source and Earth structure, how do we predict the seismic waves recorded at a station?

Seismic wave propagation in an elastic medium is governed by the elastic wave equation:

$$
\rho \frac{\partial^2 u_i}{\partial t^2}
=
\partial_j \tau_{ij} + f_i
$$

where:
- $\rho$ = density
- $u_i$ = displacement
- $\tau_{ij}$ = stress tensor
- $f_i$ = body force

Physically:
- stress gradients accelerate the medium
- forces generate seismic motion
- wave propagation depends on Earth structure and source properties

👉 Solving this equation directly for a realistic earthquake rupture is generally very difficult.

---

## Why We Need Green’s Functions

Instead of solving the elastic wave equation separately for every earthquake, we first solve a much simpler problem:

> How does the Earth respond to a very simple source?

The simplest possible source is a unit impulsive force applied at a point in space and time.

The displacement observed at a receiver location $\mathbf{x}$ is:

$$
u_i(\mathbf{x},t)
=
G_{ij}(\mathbf{x},t;\mathbf{x}_0,t_0)\,f_j
$$

where:
- $u_i$ = displacement at the receiver
- $f_j$ = force applied at the source
- $G_{ij}$ = elastodynamic Green’s function

The **Green’s function** describes the Earth’s response to a unit point force and contains all information about:
- wave propagation
- Earth structure
- reflections and refractions
- boundary conditions

👉 Green’s functions are the impulse responses of the Earth.

Because the elastic wave equation is linear:

👉 Complicated earthquake sources can be constructed by summing many simple point-force solutions.

---

## Why a Point Force Is Not a Real Earthquake

Although a point force is mathematically convenient, it is not a realistic earthquake source.

Why?

### Problem 1: Conservation of Momentum

A single internal force would accelerate the Earth in one direction and produce net linear momentum.

Real earthquakes do not do this.

### Problem 2: Earthquakes Are Slip, Not External Pushes

Earthquakes occur because two sides of a fault slide past one another.

There is no external hammer striking the Earth.

👉 Real earthquake sources must involve opposing forces.

To represent this mathematically, we introduce a **force couple**:
- two equal and opposite forces
- separated by a small distance

A force couple conserves linear momentum and provides a much better representation of fault slip.

---

## Force Couples and Double Couples

A single force couple still produces a net torque, which would rotate the Earth.

Real earthquakes also conserve angular momentum, so a second complementary force couple is required.

The **double-couple** model is the fundamental representation of earthquake fault slip.

```{figure} ../figures/08_force_couples.png
---
name: Force Couple and Double Couple
alt: Force Couple and Double Couple
width: 300px
---
Force couples are opposing point forces separated by a small distance. A double couple is a pair of complementary couples that produce no net torque.
```

👉 The double-couple source produces the characteristic four-quadrant radiation pattern observed in earthquake focal mechanisms.

---

## The Moment Tensor

Rather than tracking many individual force couples separately, we collect them into a single mathematical object called the **Moment tensor**.

A force couple $M_{ij}$ represents forces acting in the $i$-direction separated in the $j$-direction.

The full moment tensor is:

$$
\mathbf{M} =
\begin{bmatrix}
M_{11} & M_{12} & M_{13} \\
M_{21} & M_{22} & M_{23} \\
M_{31} & M_{32} & M_{33}
\end{bmatrix}
$$

The moment tensor compactly describes the geometry and strength of an earthquake source.

The tensor components have physical meaning:
- diagonal terms represent expansion or contraction
- off-diagonal terms represent shear force couples

Conservation of angular momentum requires:

$$
M_{ij}=M_{ji}
$$

so the moment tensor is symmetric and has only six independent components.

👉 The moment tensor is the mathematical foundation of focal mechanisms and seismic source inversion.

```{figure} ../figures/08_moment_tensor_components.png
---
name: The nine force couples
alt: The nine force couples
width: 600px
---
The nine different force couples that make up the components of the moment tensor.
```

---

## Scalar Moment and the Moment Tensor

The scalar seismic moment introduced earlier:

$$
M_0 = \mu D A
$$

is directly related to the moment tensor representation of the earthquake source.

For any moment tensor:

$$
M_0 =
\left(
\frac12 M_{ij}M_{ij}
\right)^{1/2}
$$

where:
- $M_{ij}$ are the moment tensor components
- repeated indices imply summation

This relationship is fundamental because it connects fault properties slip, rupture area, and rock rigidity to the mathematical source representation used to model seismic waves.

👉 Moment tensors provide a compact mathematical description of real earthquake rupture.

---

## Moment Tensors and Seismograms

The displacement from a force couple can be written as

```{math}
u_i(\mathbf{x},t)
=
\frac{\partial G_{ij}}{\partial (x_0)_k}
\,M_{jk}
```

where:
- $G_{ij}$ = Green’s function
- $M_{jk}$ = moment tensor
- $\partial G_{ij}/\partial (x_0)_k$ = spatial derivative of the Green’s function

This equation shows that seismograms depend linearly on the moment tensor.

If the Earth structure and Green’s functions are known, we can:
- predict synthetic seismograms from a source model
- or invert observed seismograms to determine the moment tensor

```{figure} ../figures/09_mt_inversion.png
---
name: Yellowstone MT Inversion
alt: Yellowstone MT Inversion
width: 600px
---
Focal mechanism determined by moment tensor analysis on an M4.4 event in Yellowstone National Park in 2017
```

---

## Big Picture: Earthquake Source Theory

Earthquake fault slip  
↓  
Equivalent double-couple source  
↓  
Moment tensor representation  
↓  
Green’s functions propagate seismic waves  
↓  
Synthetic seismograms  
↓  
Invert observations for earthquake source parameters

---

## The Global CMT Catalog

The **Global Centroid Moment Tensor (CMT) Catalog** provides moment tensor solutions for large earthquakes recorded globally.

Moment tensors are determined by computing synthetic seismograms using Green’s functions and inverting observed long-period seismic waveforms.

The Global CMT catalog is one of the most widely used earthquake source databases in seismology: https://www.globalcmt.org/

Modern global earthquake catalogs routinely determine moment tensors from seismic data (e.g., the Global CMT catalog).

```{figure} ../figures/08_global_red.gif
---
name: The Global CMT Catalog
alt: The nine force couples
width: 800px
---
The Global CMT Catalog of shallow earthquakes 1976-2005
```

---

# Moment Tensor Interpretation

## Fault Plane Ambiguity

The double-couple model provides an excellent representation of earthquake fault slip.  Because two different fault planes produce the same far-field seismic radiation pattern.

These are:
- the **primary fault plane** (the actual fault)
- the **auxiliary fault plane**

```{figure} ../figures/08_ambiguity.png
---
name: Fault plane ambiguity
alt: Demonstration of the fault plane ambiguity.
width: 500px
---
Owing to the symmetry of the moment tensor, these right-lateral and left-lateral faults have the same moment tensor represention and the same seismic radiation pattern.
```

Seismic observations alone generally cannot distinguish which plane actually slipped. Additional information is needed, such as aftershock locations, mapped surface rupture, or finite-fault rupture models.

---

## Principal Axes of the Moment Tensor

Because the moment tensor is symmetric $M_{ij} = M_{ji}$ it can be diagonalized by rotating into its principal-axis coordinate system.

For a double-couple source, the rotated moment tensor becomes:

$$
\mathbf{M} =
\begin{bmatrix}
M_0 & 0 & 0 \\
0 & -M_0 & 0 \\
0 & 0 & 0
\end{bmatrix}
$$

The principal axes are:
- **T-axis** = tension axis
- **P-axis** = pressure axis

```{figure} ../figures/08_PT_axes.png
---
name: Pressure and Tension axes
alt: Diagram showing the pressure and tension axes from a double couple source.
width: 500px
---
 The douple-couple pair on the left is represented by the off-diagonal terms in the moment tensor, M12 and M21. By rotating the coordinate system to align with the P and T axes, the moment tensor in the new coordinate system is diagonal with opposing M11 and M22 terms.
```

👉 Different force-couple representations can produce the same seismic radiation pattern and moment tensor.

---

## Beyond Double-Couple Sources

Double-couple earthquake sources produced by shear faulting have zero trace and zero determinant and therefore involve no net volume change.

However, more general moment tensors are possible.  For an isotropic source (e.g., an explosion):

$$
\mathbf{M} =
\begin{bmatrix}
M_{11} & 0 & 0 \\
0 & M_{22} & 0 \\
0 & 0 & M_{33}
\end{bmatrix}
$$

with

$$
M_{11}=M_{22}=M_{33}
$$

This represents:
- equal expansion in all directions
- a net volume increase

👉 Explosions, implosions, and some volcanic processes can produce non-double-couple moment tensors.

---

## Advanced: Decomposition of the Moment Tensor

A general moment tensor can contain:
- isotropic components
- double-couple components
- other non-double-couple terms

The isotropic part is:

$$
\mathbf{M}^{\text{iso}}
=
\frac13 (\mathrm{tr}\,\mathbf{M})\mathbf{I}
$$

The full moment tensor can be decomposed into:

$$
\mathbf{M}
=
\mathbf{M}^{\text{iso}}
+
\mathbf{M}^{\text{dev}}
$$

where the deviatoric tensor satisfies:

$$
\mathrm{tr}\,\mathbf{M}^{\text{dev}} = 0
$$

After diagonalizing the deviatoric tensor:

$$
\mathbf{M}^{\text{dev}}
=
\begin{bmatrix}
\sigma_1 & 0 & 0 \\
0 & \sigma_2 & 0 \\
0 & 0 & \sigma_3
\end{bmatrix}
$$

with

$$
\sigma_1 + \sigma_2 + \sigma_3 = 0
$$

The deviatoric tensor can be separated into:
- a **double-couple (DC)** component
- a **compensated linear vector dipole (CLVD)** component

For a pure double-couple source:

$$
\sigma_2 = 0,
\qquad
\sigma_3 = -\sigma_1
$$

For a pure CLVD source:

$$
\sigma_1 = \sigma_2 = -\frac12 \sigma_3
$$

or equivalently

$$
\sigma_3 = -2\sigma_1
$$

👉 Most tectonic earthquakes are dominated by the double-couple term, while explosions and volcanic sources may contain significant isotropic or CLVD components.

---

## Advanced: Non-Double-Couple Earthquakes

Most tectonic earthquakes are well described by:
- pure double-couple (DC) sources
- corresponding to shear slip on faults

A useful measure of departure from a pure DC source is:

$$
\epsilon
=
\frac{\sigma_2}
{\max(|\sigma_1|,|\sigma_3|)}
$$

where:
- $\epsilon = 0$ → pure double couple
- $\epsilon = \pm 0.5$ → pure CLVD source

Non-double-couple components can arise from slip on curved faults, simultaneous rupture on multiple fault planes, volcanic or magmatic processes, explosions or collapses.

Examples include caldera collapse earthquakes, magma intrusion events, landslides, and glacial sliding (“glacial earthquakes”).

👉 These sources may require isotropic, CLVD, or even single-force source models beyond the standard double-couple approximation.

---