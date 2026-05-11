# Chapter 7: Surface Waves

```{figure} ../figures/qrcode_47.png
---
name: 4/28 Quiz QR Code
alt: 4/28 Quiz QR Code
---
```

## Purpose

In previous chapters, we focused primarily on body waves traveling through the Earth interior. In this chapter, we introduce **surface waves**, which propagate along the Earth's surface and are strongly controlled by near-surface structure.

Surface waves are especially important because they:
- often dominate long-period seismic shaking
- are highly dispersive
- provide strong constraints on crust and upper mantle structure

In this chapter, we will:

- distinguish between Love and Rayleigh waves
- understand why surface waves are dispersive
- introduce phase and group velocity
- relate surface-wave dispersion to Earth structure and seismic hazard

---

## Learning Objectives

By the end of this lecture, you should be able to:

- describe the particle motions of Love and Rayleigh waves
- explain why surface waves are dispersive
- distinguish between phase velocity and group velocity
- explain why different surface-wave frequencies sample different depths
- interpret basic surface-wave dispersion curves

---

## Reading

Shearer Chapter 8:

- Section 8.3: Dispersion
- Section 8.1: Love Waves
- Section 8.4: Global Surface Waves
- Section 8.5: Observing Surface Waves

---

# What Are Surface Waves?

Surface waves:

- propagate near the Earth's surface
- decay exponentially with depth
- generally travel slower than body waves
- often have the largest amplitudes at long periods

Surface waves are important because they dominate long-period shaking, they can travel very large distances and often are the highest amplitude seismic waves, and they are strongly affected by crustal structure.

Applications:

- seismic hazard
- crustal thickness
- tomography
- ambient noise interferometry

---

## Love Waves

Love waves can be thought of as:

- trapped SH waves
- repeatedly reflecting within a low-velocity layer

Most reflected SH waves interfere destructively.

At specific frequencies:

- reflected waves interfere constructively
- energy becomes trapped near the surface

These trapped SH waves form Love waves

---

## Rayleigh Waves

Rayleigh waves involve:

- coupled P-SV motion
- elliptical particle motion

Near the surface:

- motion is retrograde
- particles move both vertically and horizontally

Rayleigh waves decay exponentially with depth and typically travel slightly slower than Love waves.

---

## Surface Wave Particle Motion

Love Waves:

- transverse horizontal motion  
- motion is perpendicular to propagation direction  
- no vertical displacement  
- SH polarized  
- often produce strong side-to-side shaking

Rayleigh Waves:

- elliptical rolling motion  
- particles move in elliptical paths  
- retrograde motion near the surface  
- coupled P-SV motion  
- motion resembles ocean waves

```{figure} ../figures/08_seismic_waves.jpg
---
width: 800px
---
Particle motions of the different types of seismic waves.
```

---

# Dispersion

When different frequencies travel at different phase velocities, wave packets become **dispersed** as the frequencies gradually separate.

Consider two waves with slightly different frequencies and wavenumbers:

$$
u(x,t)
=
\cos(\omega_1 t-k_1x)
+
\cos(\omega_2 t-k_2x)
$$

Define:

$$
\omega_1=\omega-\delta\omega,
\qquad
\omega_2=\omega+\delta\omega
$$

$$
k_1=k-\delta k,
\qquad
k_2=k+\delta k
$$

Substituting:

$$
u(x,t)
=
2\cos(\omega t-kx)
\cos(\delta kx-\delta\omega t)
$$

The resulting waveform consists of:

- a rapidly oscillating carrier wave
- modulated by a slowly varying envelope
- called "beating" in acoustics

```{figure} ../figures/08_beating.gif
---
width: 400px
---
When adding two waves with close frequencies (and wavenumbers), the resulting wave exhibits beats. The red bullet (on a node of the beat envelope) is propagating with the group velocity. The yellow bullet (starting at the same position than the red one) is propagating with the phase velocity. Here the phase velocity is faster than the group one (and motions are in the same direction).
```

```{figure} ../figures/08_group_demo.gif
---
width: 800px
---
The red square moves with the phase velocity, and the green circles propagate with the group velocity. Here the phase velocity is twice the group velocity. The red square overtakes two green circles when moving from the left to the right of the figure.
```

---

## Phase Velocity

The short-period oscillations move with the 

>**Phase velocity**
$$
c=\frac{\omega}{k}
$$

## Group Velocity

The envelope moves with the 

>**Group velocity**
$$
U=\frac{\delta\omega}{\delta k}=c+k\frac{dc}{dk}=c\left(1-k\frac{dc}{d\omega} \right)^{-1}
$$

👉 Group velocity emerges from interference between nearby frequencies and describes the propagation of energy in a dispersive wave packet.


---

# Love-Wave Generation

Love waves can be thought of as trapped SH waves undergoing repeated reflections within a low-velocity surface layer e.g. SSS, SSSS, and SSSSS.

Most reflected SH waves interfere destructively. Love waves form only at frequencies where the reflected waves interfere constructively.

```{figure} ../figures/08_reflections.png
---
width: 500px
---
Repeated SH reflections forming a Love wave.
```

Consider a monochromatic SH plane wave with ray parameter $p$.

- The wave turns at depth where:

$$
\beta = \frac{1}{p}
$$

- The horizontal slowness along the surface is also $p$

If adjacent surface bounce points are separated by distance $X(p)$ there are **two important travel times**.

### Horizontal phase propagation

The phase delay along the surface is:

$$
\omega pX(p)
$$

since:
- $p$ = horizontal slowness
- $X(p)$ = horizontal distance

---

### Actual ray-path propagation

The phase delay along the bouncing ray path is:

$$
\omega T(p) - \frac{\pi}{2}
$$

where:
- $T(p)$ = total ray travel time
- $-\pi/2$ = turning-point phase shift 

---

### Constructive Interference Condition

For the wave to reinforce itself after one bounce cycle:

$$
\omega pX(p)
=
\omega T(p)
-
\frac{\pi}{2}
-
2\pi n
$$

where:
- $n$ = integer mode number
- $n$ = 0, fundamental mode
- $n \ge $ 1, higher modes

>**Love Wave Dispersion Curve**:
$$
\omega
=
\frac{2\pi n + \pi/2}
{T(p)-pX(p)}
=
\frac{2\pi n + \pi/2}
{\tau(p)}
$$

This relationship gives the allowed frequencies for each ray parameter $p$; since $c=1/p$, it implicitly defines the Love-wave dispersion relation $c(\omega)$.

Note that only specific frequencies satisfy the constructive interference condition.

---

# Surface-Wave Dispersion

**Dispersion** is when the **phase velocity**, or the speed at which peaks and troughs in the waveform move across the surface, depends on the frequency.

Different frequencies sample different depths.

Short periods:

- shallow sensitivity
- strongly affected by low-velocity near-surface materials

Long periods:

- penetrate deeper
- sample faster lower crust and upper mantle

Since Earth velocity generally increases with depth short-period waves travel slower and long-period waves travel faster so the surface-wave velocity depends on period.

---

## Phase Velocity vs Group Velocity in Seismology

A single sinusoidal wave extends infinitely in space and does not represent a localized signal or pulse.  Real seismic waves are instead composed of many nearby frequencies that interfere to form a **wave packet**.  The small oscillations within the packet move with the **phase velocity** The overall envelope of the packet moves with the **group velocity**

The **phase velocity** is:

- velocity of individual peaks and troughs  
- depends on frequency for dispersive surface waves  

The **group velocity** is:

- velocity of the wave packet / energy propagation  
- energy travels along the actual ray paths

For dispersive waves, phase and group velocity are different.

```{figure} ../figures/08_dispersion_curve.png
---
width: 600px
---
Dispersion curves for the fundamental mode Love wave (n = 0) and higher modes (n > 0) in a simple crustal model, consisting of a uniform 40-km-thick layer over a half-space. The phase velocity decreases with frequency, starting at the shear velocity, β2, of the bottom layer and then asymptotically approaching the shear velocity, β1,ofthe toplayer.
```

---

## What Do Dispersion Curves Tell Us?

Surface-wave velocity depends on period because different periods sample different depths.

**Short periods:**
- shallow sensitivity
- strongly affected by sediments and low-velocity near-surface structure
- slower velocities

**Long periods:**
- deeper penetration
- sample faster lower crust and upper mantle
- faster velocities

```{figure} ../figures/08_love_rayleigh_dispersion.png
---
width: 800px
---
Fundamental Love and Rayleigh dispersion curves computed from the isotropic PREM model.
```

Surface waves are sensitive to:
- crustal thickness
- sedimentary basins
- lithospheric structure
- low-velocity zones

---

# Global Surface Waves

Love and Rayleigh waves propagate along great-circle paths on the Earth's surface.

Because they are confined to the surface of a sphere:

- geometrical spreading is weaker than for body waves
- amplitudes remain large at long distances

```{figure} ../figures/08_kamchatka_surface_waves.mp4
---
width: 800px
---
Ground motion visualization for Mw 8.8 off east coast of Kamchatka
```

---

## Multiple Surface-Wave Orbits

The first arrival travels along the shorter great-circle path:

- Love wave → $G_1$
- Rayleigh wave → $R_1$

A later arrival travels the long way around Earth through the antipode:

- Love wave → $G_2$
- Rayleigh wave → $R_2$

```{figure} ../figures/08_surface_wave_orbits.png
---
width: 300px
---
Minor-arc and major-arc surface-wave propagation.  Ray paths for the first three Rayleigh Waves.
```

---

## Surface Waves Continue Orbiting Earth

```{figure} ../figures/08_r1_r2.png
---
width: 800px
---
Globe-circling Rayleigh (R) and Love (G) surface waves recorded at the three-component broad-band seismic station YMG and the well water level site 140341 over 12 hr after the Tohoku M w 9 earthquake. The seismograms have been corrected for instrument response by deconvolution. Both seismograms and water level records were filtered by a Butterworth bandpass filter from 2 to 5 mHz. 
```

Surface waves continue traveling around the globe after passing the receiver:

- $R_1, R_3, R_5$: minor-arc direction
- $R_2, R_4, R_6$: major-arc direction

👉 Large earthquakes can generate surface-wave arrivals for many hours.

```{figure} ../figures/08_sumatra_poster.png
---
width: 800px
---
Sumatra Earthquake Poster showing R1, R2, etc.
```

---

## Surface-Wave Tomography

Surface-wave travel times can be inverted for:

shear-wave velocity structure
crust and upper mantle heterogeneity

Applications:

continental structure
basin imaging
tectonics

---

## Surface Waves and Seismic Hazard

Surface waves often dominate:

long-duration shaking
basin amplification

Examples:

Mexico City
Los Angeles basin

Long-period surface waves strongly affect:

tall buildings
bridges
large infrastructure