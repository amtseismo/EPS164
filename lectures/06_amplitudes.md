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
