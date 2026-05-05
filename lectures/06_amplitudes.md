# Chapter 6: Amplitudes

```{figure} ../figures/qrcode_47.png
---
name: 4/28 Quiz QR Code
alt: 4/28 Quiz QR Code
---
```

## Purpose

In previous chapters, XXXX

In this chapter, we XXX:

- XXX
- XXX
- XXX

---

## Learning Objectives

By the end of this lecture, you should be able to:
- XXXX
- XXXX
- XXXX

---

## Reading

Shearer Chapter 6:
- Section 6.1: Energy in Seismic Waves
- Section 6.3: Reflection and Transmission Coefficients
- Section 6.6: Attenuation

---

## What Controls Seismic Amplitude?

- Why do amplitudes decrease with distance?
- Why do some stations record stronger shaking than others?
- Why does strong shaking occur far from the source in some areas?

👉 What factors might control seismic amplitude?

```{figure} ../figures/06_ridgecrest_shakemap.jpg
---
name: Ridgecrest Shakemap
alt: Ridgecrest Shakemap
width: 600px
---
Shakemap for the M7.1 Ridgecrest earthquake showing the spatial distribution of peak shaking.
```
```{figure} ../figures/06_ridgecrest_record.png
---
name: Ridgecrest Seismic Record
alt: Ridgecrest Seismic Record
width: 800px
---
Seismic record section for the M7.1 Ridgecrest earthquake sorted with increasing distance.
```

---

## Factors Affecting Seismic Wave Amplitudes

Observed amplitudes depend on:

- **Geometrical spreading**
  - energy spreads over larger area  
  - body waves: $A \propto 1/r$
  - surface waves: $A \propto 1/\sqrt{r}$

- **Structure / interfaces**
  - reflection and transmission at boundaries  
  - impedance contrasts ($\rho c$)
  
- **Attenuation (Q)**
  - energy loss due to intrinsic absorption and scattering  
  - stronger at higher frequencies 
  
- **Source effects**
  - earthquake size (moment)
  - radiation pattern (directionality)

---

👉 Amplitude = source × path × structure

---

## Energy in a Ray

To understand how seismic amplitudes change, we consider how **energy propagates along a ray**.  If we define $E_K$ = **kinetic energy** and $E_W$ = **strain (potential) energy**.  The total energy density in a seismic wave is $E = E_K + E_W$

The **kinetic energy density* is:

$$
E_K = \frac{1}{2} \rho \dot{u}^2
$$

The strain energy density is:

$$
E_W = \frac{1}{2} \tau_{ij} e_{ij}
$$

---

## Average Energy of a Harmonic Plane Wave

Consider a harmonic wave:

$$
u = A \sin(\omega t - kx), \dot{u} = A \omega \cos(\omega t - kx)
$$


Averaging over time (note $\overline{\cos^2}=1/2$):

$$
E_K = E_W = \frac{1}{4} \rho A^2 \omega^2
$$

>Total energy density:
$$
E = \frac{1}{2} \rho A^2 \omega^2
$$

Energy scales with:
- amplitude squared ($A^2$)  
- frequency squared ($\omega^2$)

👉 Higher-frequency waves carry more energy for the same amplitude  

---

## Energy Flux and Rays

Energy density is energy per unit volume.  Energy flux is energy per unit area per unit time.  In time $\Delta t$, energy travels a distance $c \Delta t$ so the flux = energy density × speed.

$$
E_{\text{flux}} = \frac{1}{2} c \rho A^2 \omega^2
$$

Consider a small patch of wavefront area $dS$.  As the wave propagates $dS$ the patch expands or contracts but energy flux through the ray tube must remain constant:

$$
E_{\text{flux}} \cdot dS = \text{constant}
$$

---

## Geometric Spreading

For constant $c$, $\omega$, and $\rho$ along a ray

$$
\frac{A_2}{A_1}=\sqrt\frac{dS_1}{dS_2}
$$

- As wavefront area increases → amplitude decreases  
- As wavefront area decreases → amplitude increases  

👉 Amplitude is controlled by **ray geometry**

---

## Connection to Seismic Waves

**Body waves (3D spreading)**
- Wavefront is approximately **spherical**  
- Surface area increases as:

$$
\frac{dS_2}{dS_1} = \left(\frac{r_2}{r_1}\right)^2
$$

Thus:

$$
\frac{A_2}{A_1} = \sqrt{\frac{r_1^2}{r_2^2}} = \frac{r_1}{r_2}
$$

**Surface waves (2D spreading)**
- Energy confined near the surface  
- Wavefront expands cylindrically:

$$
\frac{dS_2}{dS_1} = \frac{r_2}{r_1}
$$

Thus:

$$
\frac{A_2}{A_1} = \sqrt{\frac{r_1}{r_2}}
$$

>Body waves: amplitude decays as $1/r$  
>Surface waves: amplitude decays as $1/\sqrt{r}$ (larger amplitudes at distance)

---

## Effect of Material Properties

If density and velocity vary but no geometric spreading (i.e. $dS_1=dS_2$)

$$
\frac{A_2}{A_1}=\sqrt\frac{\rho_1 c_1}{\rho_2 c_2}
$$

where:
- $\rho c$ = **impedance**

- Lower impedance → larger amplitudes  
- Higher impedance → smaller amplitudes  

👉 Waves amplify in **slower, less dense materials**

---

## Reflection and Transmission at Interfaces

What happens to wave amplitudes when there is a **velocity discontinuity**?

At an interface waves we call the incoming waves **incident** and the outgoing waves **scattered**. Waves that are **reflected** bounce off the interface.  Waves that are **transmitted** propgate into the next layer.

```{figure} ../figures/06_reflection_transmission.png
---
name: Reflected and Transmitted Waves
alt: Ridgecrest Seismic Record
width: 300px
---
Reflected and transmitted waves at an interface.
```

---

## Plane Waves in a Layered Medium

Recall that a general plane wave can be written as $u(\mathbf{x}, t) = f(t - \mathbf{s} \cdot \mathbf{x})$ where $\mathbf{s}$ is the slowness vector and $\mathbf{x} = (x, y, z)$ is the position

Downgoing wave:

$$
u = f(t - px - \eta z)
$$

Upgoing wave:

$$
u = f(t - px + \eta z)
$$

In layered media, wave equation separates into two types of solutions:

- **P–SV system**
  - motion in the vertical plane  
  - P and SV waves can **couple at interfaces**

- **SH system**
  - motion perpendicular to the plane  
  - SH waves **do not couple**

👉 SH waves are simpler → good starting point

---

## SH-Wave Reflection and Transmission

Consider a downgoing SH-wave incident on a horizontal interface separating two layers with different properties  

At the interface:
- one wave is **reflected upward**
- one wave is **transmitted downward**

At a solid–solid interface:

1. **Displacement must be continuous**
2. **Traction must be continuous**

---

## SH Reflection and Transmission Coefficients

>Reflection coefficient:
$$
R = \frac{\rho_1 \beta_1 \cos \theta_1 - \rho_2 \beta_2 \cos \theta_2}
{\rho_1 \beta_1 \cos \theta_1 + \rho_2 \beta_2 \cos \theta_2}
$$

If sign of $R$ is
- positive → same polarity  
- negative → polarity flip  

>Transmission coefficient:
$$
T = \frac{2 \rho_1 \beta_1 \cos \theta_1}
{\rho_1 \beta_1 \cos \theta_1 + \rho_2 \beta_2 \cos \theta_2}
$$

Note: These coefficients depend on **velocity**, **density**, and **angle of incidence** (note this is the **impedance** $\rho \beta$).

Unlike travel times:

- travel times → depend only on **velocity**
- amplitudes → depend on **velocity + density**

👉 Reflection data can constrain **density structure**

---

## Example: SH Reflection and Transmission

A downgoing SH-wave with $p = 0.2 \,\text{s/km}$ strikes a horizontal interface between:

| Layer | $\beta$ (km/s) | $\rho$ (Mg/m³) | $u = 1/\beta$ (s/km) |
|------|---------------------|---------------------|--------------------------|
| 1    | 3.2                 | 2.6                 | 0.3125                   |
| 2    | 3.9                 | 2.9                 | 0.2564                   |

Using $p = u \sin\theta$:

$\theta_1 = 39.8^\circ, \quad \theta_2 = 51.3^\circ$

Reflection coefficient:

$$
R = \frac{\rho_1 \beta_1 \cos\theta_1 - \rho_2 \beta_2 \cos\theta_2}
{\rho_1 \beta_1 \cos\theta_1 + \rho_2 \beta_2 \cos\theta_2}
= -0.05
$$

Transmission coefficient:

$$
T = \frac{2 \rho_1 \beta_1 \cos\theta_1}
{\rho_1 \beta_1 \cos\theta_1 + \rho_2 \beta_2 \cos\theta_2}
= 0.95
$$

Interpretation:
- Reflected wave amplitude: **−0.05**
- Transmitted wave amplitude: **0.95**

---

## SH vs P–SV Reflection and Transmission

At a velocity interface, waves are reflected and transmitted.

- SH waves produce only two scattered waves: a reflected SH wave and a transmitted SH wave  
- No mode conversion occurs → amplitudes are relatively simple to compute  
- The P–SV system produces four scattered waves: reflected P and SV waves, and transmitted P and SV waves  
- Mode conversion occurs at interfaces → a P-wave can generate both P and SV waves   

The algebra for P–SV reflection and transmission coefficients is significantly more complex.  In practice, these coefficients are typically computed numerically and can be found in Appendix D of Shearer. 

---

## Dependence on Ray Angle

Reflection and transmission coefficients depend on **angle of incidence**.  Consider an SH-wave incident on the Moho so that velocity and density increase across the boundary and there is an impedance contrast $\approx$ 30%.  

Near-vertical incidence ($\theta \approx 0^\circ$)

- reflected amplitude is small  
- transmitted amplitude is large  
- reflected wave undergoes **polarity reversal**  

👉 Vertical incidence behavior is controlled mainly by **impedance contrast**

```{figure} ../figures/06_ray_angle.png
---
name: Ray Angle
alt: Ray Angles
width: 600px
---
Reflection and transmission coefficients versus ray angle for a downgoing SH-wave incident on the Moho. In the top plots, the real part of the reflection coefficient is shown with a thin solid line, the imaginary part with a dashed line, and the magnitude with a heavy line. The lower plots show the change in the phase angle for a harmonic wave. The sign of the imaginary part of the reflection coefficients plotted here assumes that a phase shift of −90$\circ$ represents a $\pi$/2 phase advance.
```

---

## Behavior at Increasing Angles

As ray angle increases transmitted amplitude **increases** reflected amplitude **decreases**. 

At a specific angle ($\approx49^\circ $ in this example) reflected amplitude = 0 and transmitted amplitude = 1. No reflection despite impedance contrast.  

- near-horizontal rays carry less **vertical energy flux**  
- amplitudes must increase to conserve energy  

👉 Geometry (ray angle) strongly controls amplitude

---

## Critical Angle and Beyond

At the critical angle ($\approx60^\circ $ in this example):
- transmitted ray becomes **horizontal**  
- transmitted amplitude is large  
- reflected amplitude ≈ 1  

Beyond the Critical Angle:
- no transmitted energy into lower layer  
- total internal reflection occurs   

---

## Attenuation

So far, we have considered amplitude changes due to geometrical spreading, reflection, and transmission  

A third factor is **attenuation** loss of energy due to **internal friction** energy is converted to heat  

Types of attenuation:
- **Intrinsic attenuation** reflects true energy loss  
- **Scattering attenuation** reflects energy redistribution  

In this section, attenuation refers to **intrinsic attenuation**

---

## The Quality Factor (Q)

The strength of attenuation is described by 

> Quality factor
$$
\frac{1}{Q(\omega)} = -\frac{\Delta E}{2\pi E}
$$

where:
- $E$ = stored energy  
- $\Delta E$ = energy lost per cycle  

Note:
- high $Q$ → weak attenuation  
- low $Q$ → strong attenuation  

Even small energy losses per cycle → large amplitude reduction over distance

---

## Amplitude Decay with Distance

For harmonic waves $A(x) = A_0 e^{-\omega x / (2cQ)}$

Note:
- higher frequency → stronger attenuation  
- longer distance → more decay  
- lower $Q$ → more attenuation  

---

## Example: Computing Intrinsic Attenuation 

A wave propagates for 50 km through a material with velocity 6 km/s and $Q = 100$. What is the amplitude reduction for a wave at 1 Hz and at 10 Hz? 

Using $A(x) = A_0 e^{-\omega x / (2cQ)}, \quad \omega = 2\pi f$


For
- $f = 1 \,\text{Hz}$:

$$
A = A_0 e^{-2\pi \cdot 50 / (2 \cdot 6 \cdot 100)} \approx 0.77\, A_0
$$

- $f = 10 \,\text{Hz}$:

$$
A = A_0 e^{-20\pi \cdot 50 / (2 \cdot 6 \cdot 100)} \approx 0.073\, A_0
$$

Note:
- 1 Hz → retains **77%** of amplitude  
- 10 Hz → retains **7.3%** of amplitude  

👉 High-frequency waves attenuate much more rapidly

