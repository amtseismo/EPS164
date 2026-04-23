# Chapter 4: Ray Theory and Seismic Rays

```{figure} ../figures/qrcode_47.png
---
name: 4/14 Quiz QR Code
alt: 4/14 Quiz QR Code
---
```

## Purpose

Seismic waves are governed by the wave equation, but solving it exactly is often complicated.  Ray theory provides a simpler description by treating seismic energy as traveling along **paths (rays)**.

In this framework:
- wavefronts are locally planar  
- propagation is governed by **geometry** rather than full wave physics  

This approach is widely used in:
- earthquake location  
- travel-time analysis  
- imaging Earth structure  

---

## Learning Objectives

By the end of this lecture, you should be able to:
- Describe the relationship between wavefronts and rays
- Define slowness and the ray parameter, and explain their physical meaning
- Apply Snell’s Law to predict how rays bend across velocity contrasts
- Explain how velocity structure controls ray paths and turning depth
- Interpret travel-time curves in terms of ray geometry and Earth structure

---

## M5.7 Nevada Earthquake (April 13, 2026)

At 6:29 PM local time, a magnitude 5.7 earthquake struck western Nevada near Silver Springs.

- Shallow earthquake (~5–9 km depth) → **strong local shaking**  
- Maximum intensity: **VI–VII (strong to very strong)**  
- Felt widely across Nevada and Northern California  
- Shaking lasted ~10–20 seconds near the epicenter  

More than 6,000 people reported feeling the earthquake, with descriptions emphasizing the **duration and rolling motion** of the shaking. 

```{figure} ../figures/04_nevada_eq_map.jpg
---
name: Nevada Earthquake
width: 500px
---
Nevada Earthquake location and aftershocks.
```

---

## Seismic Record Section of Nevada EQ

A **record section** shows many seismograms plotted as a function of distance from the source.

- Each trace = one station  
- Time on x-axis, distance on y-axis  
- Reveals how waves move across a network  

```{figure} ../figures/04_nevada_eq.png
---
name: Nevada Earthquake Record Section
width: 500px
---
Record section of Nevada Earthquake.
```
Using data like this, we can construct a **travel-time curve**:

- Distance ($X$) on the x-axis  
- Arrival time ($T$) on the y-axis  

These curves contain information about the **structure of the Earth**, since wave speeds depend on material properties at depth.

---

## What is a Ray?

To interpret travel-time curves we need to introduce the concept of a **ray**.  Consider a plane seismic wave propagating through a homogeneous medium.  Wavefronts are surfaces of constant phase, and **rays are normal to wavefronts**.  They represent the path along which seismic energy travels.

Instead of tracking the full wavefield, we:
- follow the motion of wavefronts  
- approximate propagation using **straight or curved paths**  

Ray theory is a **high-frequency approximation**, valid when wavelengths are small compared to Earth structure. It describes where energy travels, not how waveforms interfere. Despite its limitations, it underpins:

- Earthquake location
- 1-D and 3-D travel-time tomography
- Phase identification at local and global scales

---

## Ray Geometry

```{figure} ../figures/04_figure_4.1.png
---
name: plane_wave
width: 500px
---
A plane wave incident on a horizontal surface.  The ray angle from vertical is termed the incidence angle $\theta$. From simple geometry, we find:
```

Assume two wavefronts are separated in time by $\Delta t$ and in distance by $\Delta s$ and that the wavefront is traveling at **incidence angle $\theta$**, defined as the angle between the direction of wave propagation and the vertical.  Under these circumstances, the horizontal distance the wave travels at the surface is $\Delta x$.  $\Delta x$ can be related $\Delta s$ by   

$$
\Delta s = v \Delta t = \Delta x \sin \theta
$$

Rewriting this we can see that 

$$
\frac{\Delta t}{\Delta x} = \frac{\sin \theta}{v} = u \sin \theta = p
$$

Where:
- $v$ = velocity  
- $u = 1/v$ = **slowness**

---

## Ray Parameter

This quantity, $p$, is called the **ray parameter**. It has an important interpretation:

- it is the **horizontal slowness** 
- it can be measured from arrival times (it is the slope of the travel time curve)  
- it remains **constant along a ray path** (in laterally homogeneous media)

$$
p = \frac{dT}{dX}
$$

---

## Refraction at Interfaces

When a wave crosses a horizontal interface separating layers with different seismic wavespeeds, the wave will be transmitted to the lower layer.  The incidence angle of the ray must change to preserve the timing of wavefronts across the interface.


```{figure} ../figures/04_snell_timing_continuity.png
---
name: fig-snell-timing
width: 600px
alt: Wavefronts crossing an interface between two layers with different velocities
---
Snell's law as timing continuity. Wavefronts (colored by time progression from early to late) bend across the interface, preserving arrival time continuity. The ray parameter p = u sin θ remains constant across the boundary.
```

$$
p = u_1 \sin \theta_1 = u_2 \sin \theta_2
$$

This means:
- the ray bends as velocity changes  
- the ray parameter remains **constant**

Direction of bending:
- faster layer → bends **away from vertical**  
- slower layer → bends **toward vertical**

Note that this is just the seismic version of Snell's law in optics...

## Ray Paths for Laterally Homogenous Models

In the Earth, both $ V_P $ and $ V_S $ generally **increase with depth**.  This leads to curved ray paths because as velocity increases, slowness decreases and the ray bends away from vertical.  

Because $ p = u \sin\theta $ is constant:
- As $ u $ decreases with depth
- $ \sin\theta $ must increase
- Rays bend **away from vertical**

Eventually, the ray becomes horizontal. This defines the **turning point** which is the deepest point the ray reaches. At the turning point, $\theta = 90$ and $\sin \theta = 1$, so $p = u(t_p)$.

This means:
- **Steep rays** (small $ p $) turn deeper
- **Shallow rays** (large $ p $) turn near the surface
- Far-offset arrivals sample **deeper Earth structure**

This single idea explains why travel-time curves encode depth information.

```{figure} ../figures/04_curved_rays_turning.png
---
name: fig-curved-rays
width: 600 px
alt: Curved ray paths in a velocity model increasing with depth
---
Ray paths in a model with velocity increasing with depth. Rays with different takeoff angles (different ray parameters p) turn at different depths. Steeper rays (smaller p) penetrate deeper before returning to the surface.
```

Note that $p=constant$ only for layers that are horizontally homogeneous.  If lateral velocity gradients or dipping layers are present, p will change along the ray path.

---

## Ray parameter and travel-time curves

Each observed arrival at distance $ X $ corresponds to **one ray** with a specific $ p $.

Plotting first-arrival time versus distance produces a **travel-time curve**:

$$ T(X)$$

The slope at any point is:

$$ \frac{dT}{dX} = p$$

Note that: 
- Observations: $ T(X) $
- Slopes give: $ p(X) $
- Ray parameter varies along the curve (each arrival has different $p$)

This is the foundation of **travel-time inversion** which is how we understand the structure of the Earth's interior

```{figure} ../figures/04_traveltime_tangent_p.png
---
name: fig-traveltime-tangent
alt: Travel-time curve with tangent line showing ray parameter
---
Travel-time curve T(X) and ray parameter. The slope of the tangent line at any point equals the ray parameter: p = dT/dX. This geometric relationship connects observable travel times to ray paths.
```

---

## Slowness and Ray Geometry

The **slowness vector** $\mathbf{s}$ has magnitude $|\mathbf{s}| = u$.  This can be geometrically decomposed into components.  The horizontal slowness $s_x = p$ and the vertical slowness $\eta = u \cos \theta = \sqrt{u^2 - p^2}$.

Note:
- $p$ is constant along a ray (in layered media)
- $\eta$ controls how the ray propagates vertically

```{figure} ../figures/04_ray_geometry.png
---
name: fig-ray-geometry
width: 600 px
alt: Geometric breakdown of slowness into horizontal and vertical slowness
---
Geometric breakdown of slowness into horizontal and vertical components.
```

---

## Distance and Travel Time Along a Ray

We want to compute distance, $X(p)$, along a ray.  From geometry:

$$
\frac{dx}{ds} = \frac{p}{u}, \quad
\frac{dz}{ds} = \sqrt{1 - \frac{p^2}{u^2}}, \quad
\frac{dx}{dz} = \frac{p}{\sqrt{u^2 - p^2}}
$$

$$
x(z_1, z_2, p) = p \int_{z_1}^{z_2} \frac{dz}{\sqrt{u^2(z) - p^2}}
$$

While the above is a general expression between two depths, for a surface source that turns at $z_p$:

>Surface to surface range: 
$$X(p) = 2p \int_{0}^{z_p} \frac{dz}{\sqrt{u^2(z) - p^2}}$$

---

## Travel Time

The travel time, $T(X)$, can be computed in a similar way.  See Shearers Section 4.2 for details.

>Surface to surface travel time: 
$$T(p) = 2 \int_{0}^{z_p} \frac{u^2(z)}{\sqrt{u^2(z) - p^2}}$$

---

## Layered Velocity Model

For a stack of **homogeneous layers**, integrals become summations and the equations above reduce to 
$$
X(p) = 2p \sum_i \frac{\Delta z_i}{\sqrt{u_i^2 - p^2}}, \quad u_i > p
$$ 
and 
$$T(p) = 2 \sum_i \frac{u_i^2 \, \Delta z_i}{\sqrt{u_i^2 - p^2}}, \quad u_i > p.$$

Note:
- Sum over layers **from the top downward**
- Stop when $u_i \le p$ otherwise $\sqrt{u_i^2 - p^2}$ becomes imaginary 
- Physically this means there is no propagation into that layer

---

## Example: Computing $X(p)$ and $T(p)$

Consider a homogeneous three-layer model with 3 km layer thicknesses and velocities 4, 6 and 8 km/s for the top, middle and bottom layers, respectively. What is the surface-to-surface distance and travel time for a ray with p= 0.15 s/km?

### Model Summary

| Layer | Depth Range (km) | Thickness (km) | Velocity (km/s) | Slowness $u$ (s/km) | $u_i > p$? |
|------|------------------|----------------|------------------|----------------------|-------------|
| 1    | 0–3              | 3              | 4                | 0.25                 | Yes         |
| 2    | 3–6              | 3              | 6                | 0.167                | Yes         |
| 3    | 6–9              | 3              | 8                | 0.125                | No          |

Note that Ray **turns above layer 3**.

---

### Computing surface-to-surface distance

We use:

$$
X(p) = 2p \sum_i \frac{\Delta z_i}{\sqrt{u_i^2 - p^2}}, \quad u_i > p
$$

Only layers 1 and 2 satisfy $u_i > p$, so:

$$
X(p) = 2p \left( \frac{z_1}{\sqrt{u_1^2 - p^2}} + \frac{z_2}{\sqrt{u_2^2 - p^2}} \right)
$$

Substituting values

$$
p = 0.15, \quad z_1 = z_2 = 3, \quad u_1 = 0.25, \quad u_2 = 0.167
$$

$$
X(p) = 2(0.15)\left(
\frac{3}{\sqrt{0.25^2 - 0.15^2}} +
\frac{3}{\sqrt{0.167^2 - 0.15^2}}
\right)
$$

$$
X(p) = 0.30 \left(
\frac{3}{\sqrt{0.040}} +
\frac{3}{\sqrt{0.0054}}
\right)
$$

$$
X(p) \approx 16.9 \ \text{km}
$$

### Computing surface-to-surface travel time

We use:

$$
T(p) = 2 \sum_i \frac{u_i^2 \, \Delta z_i}{\sqrt{u_i^2 - p^2}}, \quad u_i > p
$$

Only layers 1 and 2 satisfy $u_i > p$, so:

$$
T(p) = 2 \left( \frac{u_1^2 z_1}{\sqrt{u_1^2 - p^2}} + \frac{u_2^2 z_2}{\sqrt{u_2^2 - p^2}} \right)
$$

Substituting values

$$
p = 0.15, \quad z_1 = z_2 = 3, \quad u_1 = 0.25, \quad u_2 = 0.167
$$

$$
T(p) = 2 \left(
\frac{0.25^2 \cdot 3}{\sqrt{0.25^2 - 0.15^2}} +
\frac{0.167^2 \cdot 3}{\sqrt{0.167^2 - 0.15^2}}
\right)
$$

$$
T(p) = 2 \left(
\frac{0.0625 \cdot 3}{\sqrt{0.040}} +
\frac{0.0279 \cdot 3}{\sqrt{0.0054}}
\right)
$$

$$
T(p) \approx 4.17 \ \text{s}
$$

## Prograde and Retrograde

In the Earth, **range $X(p)$ generally increases as slowness $p$ decreases**.  Smaller takeoff angle → larger distance.

Prograde branch:
- $\frac{dX}{dp} < 0$
- Rays spread outward with decreasing $p$
- Most common behavior in smoothly varying velocity structures

```{figure} ../figures/04_prograde_tt_curve.png
---
name: prograde-tt-curve
width: 600 px
alt: Prograde travel time curve
---
Prograde travel time curve.
```

Retrograde branch:
- $\frac{dX}{dp} > 0$
- Rays **turn back on themselves**
- Caused by **rapid velocity increases with depth**

```{figure} ../figures/04_retrograde_tt_curve.png
---
name: retrograde-tt-curve
width: 650 px
alt: Retrograde travel time curve
---
Retrograde travel time curve.
```

## Travel time curve complexities

**Triplications** in Travel-Time Curves occur when there is a transition from **prograde → retrograde → prograde**

**Caustics** occur at the endpoints of the triplication and are defined by $\frac{dX}{dp} = 0$.  Rays with different takeoff angles arrive at the **same distance**.  This means that energy becomes focused.  Geometrical ray theory predicts **infinite amplitude** at caustics.

```{figure} ../figures/04_triplication.png
---
name: triplication
width: 700 px
alt: Triplications and caustics in travel time curves.
---
Triplications and caustics in travel time curves.
```

## Reduced Velocity

Travel times can be plotted using a **reduction velocity** $v_r$.  The reduced time $T_{\text{red}} = T - \frac{X}{v_r}$.  In this space, waves with velocity $v_r$ plot as horizontal lines and velocity reduction has the advantage of expanding the time scale to highlight structure.

```{figure} ../figures/04_reduced_velocity.png
---
name: reduced velocity
width: 500 px
alt: Travel time curve with reduced velocity.
---
Travel time curve with reduced velocity.
```

## Decomposing Travel Time

```{figure} ../figures/04_tt_decomp.png
---
name: travel time decomposition
width: 400 px
alt: Travel time decomposition.
---
The travel time along a ray segment can be decomposed into the sum of the horizontal slowness times the horizontal offset (time to travel from A to B) and the vertical slowness times the vertical offset (time to travel from B to C)..
```

For a small ray segment $dt = p\,dx + \eta\,dz$

- $p = u \sin\theta$ → **horizontal slowness**
- $\eta = u \cos\theta = \sqrt{u^2 - p^2}$  → **vertical slowness**
- $p\,dx$ → time from horizontal propagation  
- $\eta\,dz$ → time from vertical propagation

The total travel time is the sum of horizontal and vertical contributions.

## Defining $\tau(p)$

Integrating along the ray:

>Total travel time: 
$$T(p) = pX(p) + \tau(p)$$
Delay time:
$$\tau(p) = 2 \int_0^{z_p} \sqrt{u^2(z) - p^2} \, dz= 2 \int_0^{z_p} \eta(z)\, dz$$

Physical meaning
- $pX(p)$ → horizontal contribution  
- $\tau(p)$ → depth-integrated vertical contribution  

For a layered medium:

$$
\tau(p) = 2 \sum_i \sqrt{u_i^2 - p^2}\, z_i
\quad (u_i > p)
$$

## Geometry and Properties of $\tau(p)$

```{figure} ../figures/04_delay_time_geometry.png
---
name: Delay time geometry
width: 400 px
alt: Delay time geometry.
---
The delay time, $\tau(p) = T − pX$, is given by the intercept of the tangent to the travel time curve.
```

So the travel time curve has
- slope = $p$  
- intercept = $\tau(p)$  

---

## Key properties of $\tau(p)$

Working with $\tau(p)$ is advantageous for a number of reasons:
- $\frac{d\tau}{dp} = -X(p)$
- Because X is always positive, $\tau(p)$ is always decreasing
- $\frac{d^2\tau}{dp^2} = -\frac{dX}{dp}$ so concave up → prograde and concave down → retrograde 
- $T(X)$ → **multivalued** (triplications) whereas $X(p)$, $T(p)$, $\tau(p)$ → **single-valued**
- Makes it possible to "unravel" triplications in travel time curves

```{figure} ../figures/04_tau_p.png
---
name: Delay time geometry
width: 600 px
alt: Delay time geometry.
---
The $\tau(p)$ function “unravels” triplications in travel time curves. Prograde branches have concave upward $\tau(p)$ curves; retrograde branches have concave downward τ(p) curves.
```

---

## Why use $\tau(p)$?

- Simpler mathematical behavior  
- Useful for ray tracing (TauP methods)  
- Ideal for velocity inversion problems

## Example: Computing $\tau(p)$

Consider the same three-layer model with 3 km layer thicknesses and velocities 4, 6 and 8 km/s for the top, middle and bottom layers, respectively. What is the delay time for a ray with $p = 0.15$ s/km?

### Model Summary

| Layer | Depth Range (km) | Thickness (km) | Velocity (km/s) | Slowness $u$ (s/km) | $u_i > p$? |
|------|------------------|----------------|------------------|----------------------|-------------|
| 1    | 0–3              | 3              | 4                | 0.25                 | Yes         |
| 2    | 3–6              | 3              | 6                | 0.167                | Yes         |
| 3    | 6–9              | 3              | 8                | 0.125                | No          |

Note that Ray **turns above layer 3**.

### Computing delay time

We use:

$$
\tau(p) = 2 \sum_i \sqrt{u_i^2 - p^2}\, \Delta z_i, \quad u_i > p
$$

Only layers 1 and 2 satisfy $u_i > p$, so:

$$
\tau(p) = 2 \left( z_1 \sqrt{u_1^2 - p^2} + z_2 \sqrt{u_2^2 - p^2} \right)
$$

Substituting values

$$
p = 0.15, \quad z_1 = z_2 = 3, \quad u_1 = 0.25, \quad u_2 = 0.167
$$

$$
\tau(p) = 2 \left(
3\sqrt{0.25^2 - 0.15^2} +
3\sqrt{0.167^2 - 0.15^2}
\right)
$$

$$
\tau(p) = 2 \left(
3\sqrt{0.040} +
3\sqrt{0.0054}
\right)
$$

$$
\tau(p) \approx 1.64 \ \text{s}
$$

### Verification

We use:

$$
\tau(p) = T(p) - pX(p)
$$

Substituting values from the previous example:

$$
T(p) = 4.17 \ \text{s}, \quad X(p) = 16.9 \ \text{km}
$$

$$
\tau(p) = 4.17 - 0.15 \cdot 16.9
$$

$$
\tau(p) \approx 1.64 \ \text{s}
$$

## Low-Velocity Zones (LVZ): Ray Behavior

In most of the Earth velocity **increases with depth**.  In low-velocity zones, velocity **decreases with depth**.  From $p = u \sin \theta$, as $u$ increases with depth, $\sin\theta$ decreases, rays bend **downward (toward vertical)**.

Key implications:
- rays from the surface **do not turn within the LVZ**
- large $p$ rays turn **above** the LVZ
- only small $p$ rays penetrate and turn **below**

---

## LVZs: Shadow Zones and Waveguides

LVZs produce **shadow zones** which are gaps in ray coverage at the surface.  Observationally they manifest as missing arrivals in $T(X)$ and gaps in $\tau(p)$.

Consequence is that LVZ structure is **difficult to constrain**...travel-time data alone may be insufficient.

If waves originate within an LVZ, rays bend back toward the velocity minimum and energy becomes **trapped**.  LVZ acts as a **waveguide** allows long-distance propagation.

```{figure} ../figures/04_lvz.png
---
name: Low velocity zone
width: 600 px
alt: Low velocity zone.
---
 A low-velocity zone (LVZ) results from a velocity decrease with depth. Rays curve downward as the velocity decreases, creating a shadow zone on the surface and gaps in the $T(X)$ and $\tau(p)$ curves.
```
