# Chapter 5: Inversion of Travel Time Data

```{figure} ../figures/qrcode_47.png
---
name: 4/28 Quiz QR Code
alt: 4/28 Quiz QR Code
---
```

## Purpose

In previous chapters, we used a known velocity structure to predict how seismic waves travel.  We generally do not know the velocity structure in advance and it is something we want to determine.  Going from observed travel times to the subsurface velocity structure requires solving an inverse problem, which is more complex and often non-unique.

In this chapter, we develop a framework for:

- Inferring a 1-D average velocity structure from travel-time data
- Defining and interpreting travel-time residuals
- Linearizing the inverse problem for small velocity perturbations
- Formulating the problem as a system of equations
- Understanding the role of damping, smoothing, and resolution in tomographic inversion

---

## Learning Objectives

By the end of this lecture, you should be able to:
- XXXX
- XXXX
- XXXX

---

## Reading

Shearer Chapter 5:
- Section 5.1: One dimensional velocity inversion theory
- Section 5.2: Straight Line Fitting
- Section 5.3: $\tau (p)$ (not 5.3.2 or 5.3.3)

---

## One-Dimensional Velocity Inversion

We now consider the inverse problem where we have travel times and want to determine the velocity structure.  We can approach this problem if we assume 1-D Earth ($v = v(z)$), no triplications, and no low-velocity zones.

Each point on the travel-time curve has a slope:

$$
\frac{dT}{dX} = p
$$

This gives slowness at the turning point but not the **depth** where it occurs.

Conceptually:
- we know the velocities, can compute $X(p)$ and $T(p)$    
- we must determine **where they occur in depth**  
- equivalent to assigning a depth to each point on $T(X)$
- need to know $V$ at every point above the depth in question so work our way down.
- at the origin we know both the depth (zero) and the velocity (the slope of the T(X) curve).
- for nearby point on the $T(X)$ curve, compute the velocity, and find the depth at which the predicted travel time curve would pass through the observed point

>Invert using the **Herglotz–Wiechert formula**:
$$
z(u) = \frac{1}{\pi} \int_0^{X(u)} \frac{dX}{\sqrt{u^2 - p^2}}
$$

---

## Formal Solution and Reality

In theory:
- a complete $T(X)$ → unique $v(z)$  

In practice:
- data are discrete and noisy  
- multiple models fit the data  
- low-velocity zones → non-unique solutions  

👉 Inversion becomes:
**finding the “best” model that fits imperfect data**

---

## Straight-Line Fitting

One of the simplest inversion approaches is simply fitting the travel-time curve with **straight line segments**.  This approach was widely used in marine refraction experiments (1950s–60s) before computers were available.

This led to the classic **“layer cake” model**

Each line has a slope $\frac{dT}{dX} = p = u$.

Thus:
- each segment → one velocity  
- corresponds to a **homogeneous layer**

---

## From Lines to Layers

Each line segment defines:
- slowness: $u_i = p_i$

>Recall $\tau(p)$:
$$
\tau(p) = 2 \sum_i \sqrt{u_i^2 - p^2}\, z_i
$$

Layer thicknesses are obtained sequentially:

- first layer: from $\tau_2$, $u_1$, $u_2$  
- second layer: from $\tau_3$, $u_2$, $u_3$  
- etc.  

→ build model from **top down**

---

## Example: Solving for a Layer-Cake Model

```{figure} ../figures/05_line_fitting_example.png
---
name: Line Fitting Example
width: 400px
---
Example travel time curve.
```

Given a travel-time curve with three straight-line segments:

1. Find the slope of each segment  
2. Convert slopes to ray parameters  
3. Use ray parameters as layer slownesses  

Because the plot uses a **6 km/s reduction velocity**, the slopes give $p_1 = 0.417 \ \text{s/km}$, $p_2 = 0.267 \ \text{s/km}$, $p_3 = 0.167 \ \text{s/km}$.

Thus:

$$
u_1 = p_1, \quad u_2 = p_2, \quad u_3 = p_3
$$

and

$$
v_1 = 2.4 \ \text{km/s}, \quad
v_2 = 3.75 \ \text{km/s}, \quad
v_3 = 6.0 \ \text{km/s}
$$

---

## Solving for Layer Thicknesses

Use the delay times:

$$
\tau_1 = 0, \quad \tau_2 = 0.6 \ \text{s}, \quad \tau_3 = 1.6 \ \text{s}
$$

For the first layer:

$$
\tau_2 = 2\sqrt{u_1^2 - p_2^2}z_1
$$

$$
0.6 = 2\sqrt{0.417^2 - 0.267^2}z_1
$$

$$
z_1 = 0.937 \ \text{km}
$$

For the second layer:

$$
\tau_3 =
2\sqrt{u_1^2 - p_3^2}z_1
+
2\sqrt{u_2^2 - p_3^2}z_2
$$

$$
z_2 = 2.12 \ \text{km}
$$

Resulting model:

- Layer 1: $v = 2.4$ km/s, thickness = 0.937 km  
- Layer 2: $v = 3.75$ km/s, thickness = 2.12 km  
- Layer 3: $v = 6.0$ km/s, thickness unconstrained  

---

## Limitations

Layered models predict triplications, secondary arrivals around each corner, and many different models produce the **same first arrivals**.  Without secondary phases the models are **non-unique**.

👉 Straight-line fitting works best when:
- structure is approximately layered  
- supported by independent constraints  

```{figure} ../figures/05_secondary_branches.png
---
name: Secondary Branches
width: 400px
---
Each of the velocity models on the left produces identical first arrivals; the differences only appear in the secondary branches of the travel time curve.
```

---

## τ(p) Inversion

Working in the **$\tau(p)$ domain** allows us to use **linear inversion**.


Starting point:

$$
\tau(p) = 2 \int_0^{z_p} \sqrt{u^2(z) - p^2}\, dz
$$

Change variables from $z \rightarrow u$:

$$
\tau(p) = 2 \int_{u_0}^{p} \frac{z(u)}{\sqrt{u^2 - p^2}} \, du
$$

Since $\tau(p)$ depends **linearly** on $z(u)$ this enables use of linear inverse theory.

---

## Discretizing the Model

Assume:
- known slownesses $u_i$  
- unknown layer thicknesses $h_i$

Then:

$$
\tau(p_j) = 2 \sum_i h_i \sqrt{u_i^2 - p_j^2}
$$

Matrix form:

$$
\boldsymbol{\tau} = \mathbf{G}\mathbf{h}
$$

Solve for $h$ using:
- least squares (overdetermined)  
- regularization (underdetermined)  

---

## Example: Layer Cake Model

Given:

$$
u_1 = 0.417,\quad u_2 = 0.267,\quad u_3 = 0.167 \ \text{s/km}
$$

$$
\tau_2 = 0.6,\quad \tau_3 = 1.6 \ \text{s}
$$

We write the system:

$$
\begin{bmatrix}
\tau(p_2) \\
\tau(p_3)
\end{bmatrix}
=
\begin{bmatrix}
2\sqrt{u_1^2 - p_2^2} & 0 \\
2\sqrt{u_1^2 - p_3^2} & 2\sqrt{u_2^2 - p_3^2}
\end{bmatrix}
\begin{bmatrix}
h_1 \\
h_2
\end{bmatrix}
$$

Substitute values:

$$
\begin{bmatrix}
0.6 \\
1.6
\end{bmatrix}
=
\begin{bmatrix}
2\sqrt{0.417^2 - 0.267^2} & 0 \\
2\sqrt{0.417^2 - 0.167^2} & 2\sqrt{0.267^2 - 0.167^2}
\end{bmatrix}
\begin{bmatrix}
h_1 \\
h_2
\end{bmatrix}
$$

Solve:

- $h_1 = 0.937$ km  
- $h_2 = 2.12$ km 

---

## Why Work in τ(p)?

- linear relationship → easier inversion  
- works with noisy, discrete data  
- avoids issues in $T(X)$  
- triplications are **unraveled**  

👉 foundation for modern inversion methods
