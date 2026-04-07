# Chapter 3 Lecture: The Seismic Wave Equation and Wave Properties

## Purpose

In previous lectures, we described seismic waves using the displacement field:

$$
\mathbf{u}(\mathbf{x}, t)
$$

But what governs how this displacement evolves in space and time?

**The answer is the wave equation.**

In this lecture, we introduce the seismic wave equation and show how it leads naturally to two fundamental types of motion: **P waves** and **S waves**. We then develop a simple description of wave propagation using **plane waves** and introduce key diagnostic quantities such as **velocity**, **wavelength**, and **slowness**.

---

## Learning Objectives

By the end of this lecture, you should be able to:

- Describe the physical meaning of the seismic wave equation  
- Explain why elastic media support both P and S waves  
- Distinguish between compressional and shear motion  
- Define plane waves and their key properties  
- Understand and interpret the slowness vector  
- Relate mathematical descriptions of waves to observable quantities  

---

## The Wave Equation

A simple example of wave behavior is given by the 1D wave equation:

$$
\frac{\partial^2 u}{\partial t^2} = c^2 \frac{\partial^2 u}{\partial x^2}
$$

This equation describes waves that:

- propagate at a constant speed $c$  
- maintain their shape as they move  
- can travel in both directions  

The key idea is that **acceleration is proportional to curvature**: regions where the displacement is curved experience restoring forces that drive wave motion.

---

## The Seismic Wave Equation

In an elastic solid, the displacement field satisfies:

$$
\rho \ddot{\mathbf{u}} =
(\lambda + 2\mu)\nabla(\nabla \cdot \mathbf{u})
- \mu \nabla \times \nabla \times \mathbf{u}
$$

Each term has a clear physical meaning:

- $\rho \ddot{\mathbf{u}}$: inertia (mass × acceleration)  
- $\nabla(\nabla \cdot \mathbf{u})$: compressional deformation  
- $\nabla \times \nabla \times \mathbf{u}$: shear deformation  

**Key insight:**

- The equation naturally separates into two types of motion:
  - **Compression (volume change)**  
  - **Shear (shape change)**  

---

## P and S Waves

These two types of motion correspond to two fundamental seismic waves.

### P Waves (Compressional)

- Motion is **parallel** to the direction of propagation  
- Involve **volume change** (compression and dilation)  

$$
\alpha = \sqrt{\frac{\lambda + 2\mu}{\rho}}
$$

---

### S Waves (Shear)

- Motion is **perpendicular** to the direction of propagation  
- Involve **shear deformation only** (no volume change)  

$$
\beta = \sqrt{\frac{\mu}{\rho}}
$$

---

### Key Observations

- $\alpha > \beta$: P waves travel faster than S waves  
- S waves depend on $\mu$, so they **do not propagate in fluids**  
- P waves depend on both $\lambda$ and $\mu$

---

## Plane Waves

To describe wave propagation, we consider a simple solution: a **plane wave**.

A harmonic plane wave can be written as:

$$
\mathbf{u}(\mathbf{x}, t) = \mathbf{A} e^{i(\mathbf{k}\cdot\mathbf{x} - \omega t)}
$$

where:

- $\mathbf{A}$: amplitude  
- $\mathbf{k}$: wavenumber vector  
- $\omega$: angular frequency  

---

### Interpretation

- $\mathbf{k}$ points in the **direction of propagation**  
- $\omega$ controls how fast the wave oscillates in time  
- The wave varies sinusoidally in both space and time  

Surfaces of constant phase are planes perpendicular to $\mathbf{k}$.

---

## Wave Properties

$$
\omega = 2\pi f, \quad
\lambda = \frac{c}{f}, \quad
k = \frac{2\pi}{\lambda} = \frac{\omega}{c}
$$

- **Frequency** $f$: oscillations per second  
- **Wavelength** $\lambda$: spatial scale of the wave  
- **Velocity** $c$: links time and space variation  

---

## Slowness

It is often useful to define the **slowness vector**:

$$
\mathbf{s} = \frac{\mathbf{k}}{\omega}
$$

- Direction: same as propagation direction  
- Magnitude:
$
|\mathbf{s}| = \frac{1}{c}
$

---

### Interpretation

The dot product:

\[
\mathbf{s} \cdot \mathbf{x}
\]

represents **travel time** from the origin.

👉 This makes slowness especially useful for:
- describing wave propagation  
- interpreting travel times  
- connecting to ray theory  

---

## Particle Motion

The direction of motion distinguishes P and S waves:

- **P waves**: motion is parallel to propagation  
- **S waves**: motion is perpendicular to propagation  

S waves can have different polarizations:

- **SV waves**: motion in the vertical plane  
- **SH waves**: motion perpendicular to that plane  

---

## Big Picture

The seismic wave equation provides a unified framework for understanding wave propagation:

- It describes how displacement evolves in space and time  
- It predicts two fundamental types of waves (P and S)  
- It links physical properties of Earth to observable wave behavior  

Using simple solutions like plane waves, we can define key quantities—such as velocity, wavelength, and slowness—that form the foundation of seismic analysis.