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