# Chapter 4 Lecture 1: Ray Theory and Seismic Rays

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

- Explain what a seismic ray represents  
- Understand how wave propagation can be approximated geometrically  
- Derive and interpret **Snell’s Law**  
- Define **slowness** and the **ray parameter**  
- Describe how rays propagate in layered and depth-dependent media  

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
- Geometry + physics link $ p $ to turning depth

This is the foundation of **travel-time inversion** which is how we understand the structure of the Earth's interior

```{figure} ../figures/04_traveltime_tangent_p.png
---
name: fig-traveltime-tangent
alt: Travel-time curve with tangent line showing ray parameter
---
Travel-time curve T(X) and ray parameter. The slope of the tangent line at any point equals the ray parameter: p = dT/dX. This geometric relationship connects observable travel times to ray paths.
```

---

## Looking ahead
Next, we will:
- Turn these ideas into **numerical ray tracing**
- Explore when ray theory **fails** (LVZs, triplications)
