# Chapter 2 Lecture: Stress and Strain

## Purpose

To describe how the Earth deforms and how forces are transmitted through it, we need a framework for:

- **Forces inside materials** → **stress**
- **Deformation of materials** → **strain**

These two quantities are linked through **constitutive relationships**, which ultimately control:
- Seismic wave propagation  
- Faulting and earthquakes  
- Rock deformation  

In this chapter, we build that framework.

---

## Learning Objectives

By the end of this lecture, you should be able to:

- Explain how **stress** describes internal forces in the Earth and how it acts on planes of arbitrary orientation.

- Describe the **stress tensor** as a mathematical representation of internal forces and interpret its physical meaning.

- Understand the concept of **principal stresses** and why they provide a natural coordinate system for analyzing stress.

- Distinguish between **hydrostatic** and **deviatoric stress**, and explain their roles in deformation and faulting.

- Explain how **strain** describes deformation and how it is derived from spatial variations in displacement.

- Distinguish between **deformation** and **rigid-body rotation**, and interpret the physical meaning of strain components.

- Understand how **stress and strain are related through elasticity**, and recognize the assumptions of linear elastic behavior.

- Relate elastic properties of materials to **seismic wave propagation**, including the origin of P- and S-wave speeds.

---


## 1. The Stress Tensor

### 1.1 Traction

Imagine cutting an infinitesimal plane inside a material. Forces act across that plane.

The **force per unit area** is called the **traction**:

$$
\mathbf{t}(\hat{\mathbf{n}}) = (t_x, t_y, t_z)
$$

where $\hat{\mathbf{n}}$ is the unit normal to the plane.

We can always decompose traction into:
- **Normal stress** → perpendicular to the plane  
- **Shear stress** → parallel to the plane  

Key symmetry:
$$
\mathbf{t}(-\hat{\mathbf{n}}) = -\mathbf{t}(\hat{\mathbf{n}})
$$

👉 This just says: flip the plane, and the force reverses.

**Special case (fluids):**

Fluids cannot support shear stress, so:
$$
\mathbf{t} = -P \hat{\mathbf{n}}
$$

Only normal forces (pressure) exist.

---

### 1.2 Stress Tensor

Instead of describing traction separately for every possible plane, we define a single object:

The **stress tensor**:

$$
\boldsymbol{\tau} =
\begin{bmatrix}
\tau_{xx} & \tau_{xy} & \tau_{xz} \\
\tau_{yx} & \tau_{yy} & \tau_{yz} \\
\tau_{zx} & \tau_{zy} & \tau_{zz}
\end{bmatrix}
$$

Interpretation:
- $\tau_{ij}$ = force in direction $i$ acting on a plane normal to $j$

The key idea is:

$$
\mathbf{t}(\hat{\mathbf{n}}) = \boldsymbol{\tau} \hat{\mathbf{n}}
$$

👉 The stress tensor maps **plane orientation → traction**.

---

### 1.3 Why is Stress Symmetric?

Physics requires that a tiny volume cannot spontaneously rotate.

This leads to:
$$
\tau_{ij} = \tau_{ji}
$$

So:
- Only **6 independent components**
- Not 9

👉 This is a *big simplification*.

---

### 1.4 Principal Stresses

There exist special directions where traction has **no shear component**:

$$
\boldsymbol{\tau} \hat{\mathbf{n}} = \lambda \hat{\mathbf{n}}
$$

This is an eigenvalue problem:
$$
(\boldsymbol{\tau} - \lambda I)\hat{\mathbf{n}} = 0
$$

- $\lambda$ → **principal stresses**  
- $\hat{\mathbf{n}}$ → **principal directions**

👉 In these directions, stress is purely normal.

---

### 1.5 Principal Coordinate System

If we rotate into the principal directions:

$$
\boldsymbol{\tau}_R =
\begin{bmatrix}
\tau_1 & 0 & 0 \\
0 & \tau_2 & 0 \\
0 & 0 & \tau_3
\end{bmatrix}
$$

👉 No shear stresses remain.

This is often the **most physically meaningful coordinate system**.

---

### 1.6 Maximum Shear Stress

The largest shear stress occurs on planes at **45°** to the principal axes:

$$
\tau_{\max} = \frac{\tau_1 - \tau_3}{2}
$$

👉 This is directly related to **failure and faulting**.

---

### 1.7 Hydrostatic vs Deviatoric Stress

We can split stress into:

### Hydrostatic (mean) stress:
$$
\tau_m = \frac{\tau_1 + \tau_2 + \tau_3}{3}
$$

- Causes **volume change only**

### Deviatoric stress:
$$
\boldsymbol{\tau}_D = \boldsymbol{\tau} - \tau_m I
$$

- Causes **shape change**

---

**Key takeaway:**

> Earthquakes are driven by **deviatoric stress**, not hydrostatic pressure.

---

## 2. The Strain Tensor

### 2.1 Displacement Field

We describe motion using displacement:

$$
\mathbf{u}(\mathbf{r}_0, t) = \mathbf{r} - \mathbf{r}_0
$$

- Tracks how points move
- This is a **Lagrangian description**

---

### 2.2 From Displacement → Strain

Strain describes how displacement **varies in space**:

$$
J = \nabla \mathbf{u}
$$

This is the **displacement gradient tensor**.

---

### 2.3 Strain Tensor

We split deformation into:

$$
J = \mathbf{e} + \boldsymbol{\omega}
$$

- $\mathbf{e}$ → **strain (deformation)**  
- $\boldsymbol{\omega}$ → **rotation (rigid motion)**  

Strain is:

$$
e_{ij} = \frac{1}{2}
\left(
\frac{\partial u_i}{\partial x_j} +
\frac{\partial u_j}{\partial x_i}
\right)
$$

👉 Only the symmetric part changes shape.

---

### 2.4 Physical Meaning

- Diagonal terms → stretching or compression  
- Off-diagonal terms → shear  

👉 Strain tells you **how the material deforms**, not where it moves.

---

### 2.5 Volume Change (Dilatation)

$$
\Delta = \nabla \cdot \mathbf{u} = \text{tr}(\mathbf{e})
$$

- $\Delta > 0$ → expansion  
- $\Delta < 0$ → compression  

---

### 2.6 Principal Strains

Strain behaves just like stress:

$$
\mathbf{e} \hat{\mathbf{n}} = \lambda \hat{\mathbf{n}}
$$

👉 There are directions with **pure extension/compression** and no shear.

---

### 2.7 Connection to Seismic Waves

- **P-waves**:
  - Produce **volume change**
  - $\nabla \cdot \mathbf{u} \neq 0$

- **S-waves**:
  - Produce **shear deformation**
  - No volume change

---

### 2.8 Typical Strain Magnitudes

$$
\sim 10^{-6}
$$

👉 Very small → justifies **linear elasticity**.

---

## 3. Stress–Strain Relationship (Elasticity)

To connect forces and deformation, we need a **constitutive law**.

---

### 3.1 General Linear Form

$$
\tau_{ij} = c_{ijkl} e_{kl}
$$

- Maps strain → stress  
- Fully general (anisotropic materials)

---

### 3.2 Isotropic Case

For most Earth materials (first approximation):

$$
\tau_{ij} = \lambda \delta_{ij} e_{kk} + 2\mu e_{ij}
$$

Only **two parameters**:
- $\lambda$
- $\mu$ (shear modulus)

---

### 3.3 Physical Interpretation

- $\lambda$ → controls **volume response**  
- $\mu$ → controls **shear resistance**

👉 $\mu$ is especially important—it controls whether S-waves exist.

---

### 3.4 Seismic Velocities

Elasticity directly determines wave speeds:

$$
\alpha = \sqrt{\frac{\lambda + 2\mu}{\rho}}, \quad
\beta = \sqrt{\frac{\mu}{\rho}}
$$

- P-waves depend on compression + shear  
- S-waves depend only on shear  

---

## Summary

- **Stress** describes internal forces  
- **Strain** describes deformation  
- **Elasticity links the two**

> This framework underpins everything we do in seismology: wave propagation, earthquake mechanics, and Earth structure.