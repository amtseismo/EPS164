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
- Section 5.5: Three-dimensional Velocity Inversion

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

---

## The Geophysical Forward Problem versus the Geophysical Inverse Problem

Often in geophysics, we have to solve the **inverse problem**. The inverse problem is the estimations of parameters of a **model** of the Earth system from **data** or observations. The inverse problem is different from the forward problem.


👉 **The Forward Problem** aka the direct problem or the forward model

Given a model **m**, the forward problem computes the data **d** that would be observed.

$$ 
\mathbf{d} = F(\mathbf{m})
$$

where F maps from the model to data space as shown below:

```{figure} ../figures/05_forward_problem.png
---
name: Forward Problem
width: 400px
---
Visualization of the Forward Problem.
```

The forward problem has a solution that:

1. exists.
2. is unique.
3. is stable (i.e. a small model change $\delta m$ gives a small data change $\delta d$).

An example of the forward problem is calculting arrival times for seismic waves given a seismic velocity model. Forward problems are phyiscal problems that occur in nature. Inverse problems are mathematical.

👉 **The Inverse Problem** 

Given an observed set of data **d**, determine what model parameters **m** gave rise to that data.

$$ 
\mathbf{m} = F^{-1}(\mathbf{d})
$$

where $F^{-1}$ maps from the model to data space as shown below:

```{figure} ../figures/05_inverse_problem.png
---
name: Inverse Problem
width: 400px
---
Visualization of the Inverse Problem.
```

The inverse problem has a solution that:

1. may or may not exist.
2. is generally non-unique (i.e. an infinite number of acceptable models can be found to fit the data).
3. is often unstable (i.e. a small change to the data $\delta d$ such as **noise** gives a large model change $\delta m$).

An example of the inverse problem is solving for the Earth velocity structure, given an observed set of seismic arrival times.

---

## Three-dimensional Velocity Inversion

Observed seismic travel times (**data**) are often different from predicted seismic travel times (**model**). We can compare the two using the **travel time *residual***.

$$ 
t_{resid} = t_{obs} - t_{pred}
$$

- If $t_{resid} < 0$, the velocity model we are using is too slow.
- If $t_{resid} > 0$, the velocity model we are using is too fast.

Residuals are often plotted on histograms showing that there is natural scatter in our tavel time data. 

- If the average residual is zero, the data is well modeled using a 1D velocity model.
- If the average residual is nonzero, as in the example below, we must reevaluate the velocity model and a 2D or 3D velocity model may become necessary to resolve lateral velocity perturbations. This process is called ***seismic tomography***.


```{figure} ../figures/05_residuals.png
---
name: Travel time residuals.
width: 400px
---
Residuals with a nonzero average residual, indicating the need to consider 2D or 3D lateral velocity perturbations.
```

___

## Setting up the Tomography Problem

In the tomographic problem we parameterize the velocity model as a number of blocks of uniform velocity perturbations. Rays travel through the velocity model from a source point to and end point.


```{figure} ../figures/05_2D_tomo_problem.png
---
name: Ray Path and 2D Tomography Problem.
width: 400px
---
An example ray path and cell numbering for a simple 2D tomography problem.
```

When you know the geometry of the seismic ray, the reference travel time through each block in the velocity model can be given by:

$$
\Delta t_0 = \Delta x u_0
$$

where $\Delta x$ is the ray path distance through the block and $u_0$ is the local reference slowness (model).

Our observed travel time for this block is slightly different than the predicted travel time. We assume a slight perturbation to our velocity model such that the observed slowness of the block, $u$, is given by 

$$
u = u_0 (1+s)
$$ 

or the modeled slowness ($u_0$) plus some small fractional slowness perturbation, $s$. The contribution of this slowness perturbation to the travel time residual is therefore:

$$
\Delta r = \Delta t - \Delta t_0 = \Delta x u_0 (1+s) - \Delta x u_0 = \Delta t_0 s
$$

If we sum all slowness perturbations along the entire ray path, the total travel time residual is:

$$
r = \sum_k b_k s_k 
$$

where $b_k$ is the ray travel time in the *k*th block and $s_k$ is the fractional slowness perturbation in *k*th block.

If we now consider the solution for many rays where the ray number is $i$, we get:

$$
r_i = \sum_{j=1}^m b_{ij} s_{j}
$$

where $m$ is the total number of model blocks. If a ray does not enter a block, we set that equal to 0. In this case, $s_k$ values are fractional related to the starting model i.e. an $s_k$ value of -0.01 means the solution is 1% slower than the starting model. 

If we have $n$ number of residuals, this becomes a matrix problem:

$$
\begin{bmatrix}
r_1 \\
r_2 \\
... \\
r_n
\end{bmatrix}
= 
\begin{bmatrix}
b_{11} & b_{12} & ... \\
b_{21} & b_{22} & ... \\
... & ... & b_{nm} 
\end{bmatrix}
\begin{bmatrix}
s_1 \\
s_2 \\
... \\
s_m
\end{bmatrix}
$$

This can be written in the form:

$$
\mathbf{d} = \mathbf{G} \mathbf{m}
$$

where $\mathbf{d}$ is our data vector (i.e. our travel time residuals), $\mathbf{m}$ is our model vector (i.e. our slowness perturbations), and $\mathbf{G}$ is a linear operator (holding the travel times of each ray in each block) that predicts the model from the data. 

___

## Least-Squares Inversion

Most rays will travel through a limited number of blocks. Typically, $\mathbf{G}$ will hold mostly zeros. If the number of travel time observations is greater than the number of model blocks ($n>m$) and our problem is over-determined, then we can solve using the *least squares solution*:

$$
\mathbf{m} = (\mathbf{G}^T\mathbf{G})^{-1} \mathbf{G}^T \mathbf{d}
$$

For most tomographic problems, $\mathbf{G}^T\mathbf{G}$ is invariably singular or ill-conditioned. This can be due to:
- Near identical ray paths,
- Blocks being oversampled or not sampled at all,
- Or having a model so large that we cannnot solve using direct matrix inversion.

---

## Regularization

---

## Damping

A common approach to ill-conditioned least squares inversion is to use regularization using *damped least squares inversion*.  We therefore solve:

$$
\begin{bmatrix}
\mathbf{d} \\
0
\end{bmatrix}
= 
\begin{bmatrix}
\mathbf{G} \\
\lambda \mathbf{I}
\end{bmatrix}
\mathbf{m}
$$

where $\mathbf{I}$ is the identity matrix and $\lambda$ is a weighting parameter that controls damping. The solution to this equation minimizes the function:

$$
|| \mathbf{G}\mathbf{m} - \mathbf{d} ||^2 + \lambda^2 ||\mathbf{m}||^2
$$

where the first term is the misfit to the data and the second term is the variance of the model. $\lambda$ controls the trade-off between misfit and model variance. 


Increasing damping will add stability to the solution. However, a damped least squares solution will not increase model smoothness. Model perturbations in adjacent blocks can still be quite significant.

---

## Smoothing

Commonly, to measure model roughness we compute a *Laplacian operator* $\nabla^2$. This is a difference operator over 2D or 3D block geometries. To minimize roughness, we solve for:

$$
\begin{bmatrix}
\mathbf{d} \\
0
\end{bmatrix}
= 
\begin{bmatrix}
\mathbf{G} \\
\lambda \mathbf{L}
\end{bmatrix}
\mathbf{m}
$$

where $\mathbf{L}$ is a finite difference approximation of the Lapacian over all model blocks. For example in 2D, the Laplacian of the *j*th block becomes:

$$
\nabla_j^2 \simeq 0.25 (m_{left} + m_{right} + m_{up} + m_{down}) - m_j
$$

where $m_{left}, m_{right}, m_{up}, m_{down}$ are the cells directly adjacent to cell $m_j$. This Lapacian minimizes:

$$
|| \mathbf{G}\mathbf{m} - \mathbf{d} ||^2 + \lambda^2 ||L\mathbf{m}||^2
$$

Where $\lambda$ therefore controls the trade-off between misfit and model roughness. A model can therefore be selected that is smooth but does not minimize variance. Blocks are not sampled directly by ray paths but rather interpolated from nearby cells. Typically, $\lambda$ is selected to miminimize the L-curve:

```{figure} ../figures/05_L_curve.png
---
name: L Curve.
width: 400px
---
The L-Curve is the statistical model used to select the $\lambda$ value such that you minimize both misfit and model variance.
```

If we select a very smooth model, we don't care about fitting the data. Inversely, mimimizing data misfit might cause huge increases to model roughness. It is typically pointless to try to fit data perfectly, because all data has inherent error or noise.
___

The ideal type of regularization, whether damping or smoothing, will depend on the exact inversion problem. Both methods have advantages and disadvantages.

For example, one should distrust a damped least-squares solution when there is significant fine velocity structure at the scale-length of the block dimensions.  Minimum roughness models are suspect when there are large-amplitude anomalies in regions with little data.

---

## Limitations of the Tomography Problem

1. Approximating the travel time residual as a sum of the slowness perturbations, $s$, in each block is only valid if the slowness perturbations are small i.e $s<<1$.
2. Conventional linear algebra methods break down for large models where $m$ is very large. This is particularly true for 3D problems. Sparse matrix calculations are therefore necessary for large problems.
3. Seimsic tomography works best for a large number of ray geometries in each cells with varied ray paths. This is not often the case. Tomography models are highly biased by ray coverage. Typically rays in a problem will appear at only some geometries, covering only a small percentage of the model blocks. This leads to biases in the solution along these ray paths:

```{figure} ../figures/05_ray_geometry.png
---
name: Ray Angle Biases.
width: 400px
---
Ray angles in tomographic problems are typically limited. Therefore, resolution in of velocity anomalies is limited parallel to the ray path.
```





