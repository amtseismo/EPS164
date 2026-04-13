# Chapter 3 Lecture: The Seismic Wave Equation and Wave Properties

```{figure} ../figures/qrcode_47.png
---
name: 4/14 Quiz QR Code
alt: 4/14 Quiz QR Code
---
```

## Purpose

Using the framework of **stress** and **strain**, we now derive the equation that governs how seismic waves propagate through the Earth.

This leads to the **seismic wave equation**, which describes how displacement evolves in space and time.

Two fundamental wave types emerge:

- **P waves** → compressional (volume change)  
- **S waves** → shear (shape change)  

Their velocities depend on material properties $\lambda, \mu, \rho$

---

## Learning Objectives

By the end of this lecture, you should be able to:

- Explain how Newton’s laws lead to the equation of motion for a continuum
- Interpret the divergence of stress as a force per unit volume
- Understand how the*wave equation emerges from elasticity
- Distinguish between P and S waves physically and mathematically
- Interpret plane waves and slowness
- Describe particle motion (polarization)

---

## Equation of Motion

To describe wave propagation, we apply **Newton’s second law** to a continuous medium:

$$
F = ma
$$

Consider an infinitesimal cube of material. Forces act on its faces due to **stress**, and throughout its volume due to **body forces**.

The key result is:

$$
F_i = \partial_j \tau_{ij} \, dV
$$

where

$$
\partial_j \tau_{ij}
$$

is the **divergence of the stress tensor**.  This represents **net force per unit volume**.  

Including body forces and inertia:

$$
\rho \frac{\partial^2 u_i}{\partial t^2}
=
\partial_j \tau_{ij} + f_i
$$

This is the **equation of motion** (momentum equation).

- $\rho \ddot{u}_i$ → inertia  
- $\partial_j \tau_{ij}$ → internal forces from stress gradients  
- $f_i$ → body forces  

Note that stress itself does not cause motion—spatial variations in stress do. Seismic waves arise when stress gradients accelerate the medium.

### Special Case (Wave Propagation)

Away from sources:

$$
\rho \ddot{u}_i = \partial_j \tau_{ij}
$$

---

## The Seismic Wave Equation

To solve this, we relate stress to deformation using elasticity:

$$
\tau_{ij} = \lambda \delta_{ij} e_{kk} + 2\mu e_{ij}
$$

$$
e_{ij} = \frac{1}{2}(\partial_i u_j + \partial_j u_i)
$$

Substituting into the equation of motion, and assuming the medium is homogenous (i.e. gradients in Lame parameters are zero) gives:

$$
\rho \ddot{\mathbf{u}} =
(\lambda + 2\mu)\nabla(\nabla \cdot \mathbf{u})
- \mu \nabla \times \nabla \times \mathbf{u}
$$

There are two ways to deform a material, changing volume or changing shape.

These appear directly in the equation:

- $\nabla(\nabla \cdot \mathbf{u})$ → compressional motion  
- $\nabla \times \nabla \times \mathbf{u}$ → shear motion  

---

## P and S Waves

The wave equation naturally separates into two independent wave types.

**P waves:** have motion parallel to propagation and involve volume change  
**S waves:** have motion perpendicular to propagation and involve purely shear  

We can isolate the P-wave in the wave equation by taking the divergence:

$$
\frac{\partial^2}{\partial t^2}(\nabla\cdot\mathbf{u})
=
\alpha^2 \nabla^2(\nabla\cdot\mathbf{u})
$$

$$
\alpha = \sqrt{\frac{\lambda+2\mu}{\rho}}
$$

Volume changes propagate as waves → **P waves**

Alternatively we can isolate the S-wave contribution by taking the curl:

$$
\frac{\partial^2 (\nabla \times \mathbf{u})}{\partial t^2}
=
\beta^2 \nabla^2 (\nabla \times \mathbf{u})
$$

$$
\beta = \sqrt{\frac{\mu}{\rho}}
$$

Shear disturbances propagate → **S waves**

---

## Plane Waves and Slowness

A plane wave is a solution of the wave equation in which the displacement varies only in the direction of wave propagation:

$$
\mathbf{u}(x, t) = \mathbf{f}\left(t \pm \frac{x}{c}\right)
$$

$c$ is the velocity of the wave, $\mathbf{f}$ is any arbitrary function, and the wave is propagating in either the $+x$ or the $-x$ direction.  Displacement doenst vary with $y$ or $z$.

### Slowness

More generally, displacement at position vector x for a plane wave propagating in the unit direction $\hat{\mathbf{s}}$ may be expressed as $\mathbf{s} = \frac{\hat{\mathbf{s}}}{c}$ where $\mathbf{s}$ is the **slowness vector**.

Then:

$$
\mathbf{u}(\mathbf{x}, t) = f(t - \mathbf{s} \cdot \mathbf{x})
$$

$\mathbf{s} \cdot \mathbf{x}$ represents **travel time**.

### Harmonic Waves

## Harmonic Waves

Far from the source, the wavefront becomes nearly flat, and we can often approximate the seismic waves as a **plane wave**.  To simplify things further, we often consider waves of a single frequency. These are called **harmonic waves**, and can be written as:

$$
\mathbf{u}(\mathbf{x}, t) = \mathbf{A}(\omega) \, e^{-i\omega (t - \mathbf{s} \cdot \mathbf{x})} = \mathbf{A}(\omega) \, e^{-i(\omega t - \mathbf{k} \cdot \mathbf{x})}
$$

The wavenumber vector is related to wave speed by $\mathbf{k} = \omega\mathbf{s} = \frac{\omega}{c}\,\hat{\mathbf{s}}$ and the key wave properties are related in ways shown in the table below.

**Key idea:** harmonic plane waves are the simplest solutions to the wave equation, and more complex seismic waves can be built by combining many of them.

| Quantity            | Symbol | Definition / Relationship                          | Units            |
|--------------------|--------|----------------------------------------------------|------------------|
| Angular frequency  | $\omega$ | $\omega = 2\pi f = \dfrac{2\pi}{T}$              | s$^{-1}$         |
| Frequency          | $f$      | $f = \dfrac{1}{T} = \dfrac{\omega}{2\pi}$        | s$^{-1}$ (Hz)    |
| Period             | $T$      | $T = \dfrac{1}{f} = \dfrac{2\pi}{\omega}$        | s                |
| Velocity           | $c$      | $c = \dfrac{\omega}{k} = f\lambda$               | m/s              |
| Wavelength         | $\lambda$ | $\lambda = \dfrac{c}{f} = cT = \dfrac{2\pi}{k}$ | m                |
| Wavenumber         | $k$      | $k = \dfrac{2\pi}{\lambda} = \dfrac{\omega}{c}$  | m$^{-1}$         |
| Slowness           | $s$      | $s = \dfrac{1}{c}$                                | s/m              |

---

## Polarization

The **polarization** of a seismic wave describes the direction of particle motion relative to the direction of propagation.

For a **P wave** traveling in the $x$-direction, displacement is given by $\mathbf{u} = \nabla \phi$ where $\phi$ is called a scalar potential.

Because a plane wave varies only in the direction of propagation, we have $\partial_y = \partial_z = 0$ so the displacement becomes $u_x = \frac{\partial \phi}{\partial x}, \quad u_y = 0, \quad u_z = 0$.

**Key idea:** motion is entirely in the direction of propagation.

- Motion is **parallel** to propagation  
- Called **longitudinal waves**  
- $\nabla \cdot \mathbf{u} \neq 0$ → volume change  
- $\nabla \times \mathbf{u} = 0$ → no rotation  

P waves involve compression and dilation of the material. Although often described as purely compressional, they also involve some shear deformation, which is why their speed depends on both $\lambda$ and $\mu$.

For an **S wave** traveling in the $x$-direction, displacement is given by $\mathbf{u} = \nabla \times \boldsymbol{\psi}$ where $\psi$ is called a scalar potential.

Again assuming a plane wave ($\partial_y = \partial_z = 0$), this gives

$$
u_x = 0, \quad
u_y = -\frac{\partial \psi_z}{\partial x}, \quad
u_z = \frac{\partial \psi_y}{\partial x}.
$$

**Key idea:** motion is entirely perpendicular to propagation.

- Motion is **perpendicular** to propagation  
- Called **transverse waves**  
- $\nabla \cdot \mathbf{u} = 0$ → no volume change  
- Pure **shear deformation**  

S-wave motion can occur in any direction perpendicular to propagation.

Two common polarizations are:

- **SV waves**: motion in the vertical plane containing the propagation direction  
- **SH waves**: motion perpendicular to that plane  

---

## Summary

Seismic waves arise from the balance between **inertia** and **stress gradients** in an elastic medium.

The **seismic wave equation** shows that motion separates into two fundamental types:

- **P waves**: compressional (volume change)  
- **S waves**: shear (shape change)  

Plane waves provide simple solutions that describe how waves propagate through space and time, with **slowness** linking propagation to travel time.

**Key idea:** seismic wavefields can be understood as combinations of P and S waves governed by the wave equation.