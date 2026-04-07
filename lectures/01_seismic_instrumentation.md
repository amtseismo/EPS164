# Chapter 11 Lecture: Seismometers and Seismographs

## Purpose

In this course, we describe seismic waves using the displacement field:

$$
\mathbf{u}(\mathbf{x}, t)
$$

However, seismic data are not direct measurements of this quantity.  They are shaped by the instruments used to record ground motion.

**This raises a fundamental question:**  How do seismometers measure Earth motion, and how does instrument response influence what we observe?

In this chapter, we introduce the basic physics of seismic instrumentation and show how recorded signals relate to true ground motion. Understanding instrument response is essential for interpreting seismic data throughout the course.

---

## Learning Objectives

By the end of this lecture, you should be able to:

- Explain how seismometers measure ground motion  
- Describe the behavior of a seismometer as a damped oscillator  
- Understand how instrument response depends on frequency  
- Distinguish between short-period and long-period observations  
- Recognize why instrument response matters for interpreting data  

---

## Seismometers and Seismographs

A **seismometer** is the sensor that detects ground motion, while a **seismograph** refers to the complete system, including the recording electronics.

Modern instruments record data digitally and often transmit it in real time. Regardless of the specific design, all instruments share an important feature:

**Seismometers do not record ground motion directly—they record a filtered version of it.**

Understanding this filtering is essential for interpreting seismic data.

---

## Inertial Seismometers

Most seismometers are based on a simple physical idea: **inertia**.  A mass is suspended inside the instrument. When the ground moves, the instrument case moves with it, but the mass tends to remain stationary. The instrument measures the motion of the mass relative to the case.

This relative motion can be recorded in different ways—displacement, velocity, or acceleration—and this choice strongly affects the instrument response.

---

## Equation of Motion

```{figure} ../figures/11_simple_inertial_seismometer.png
---
name: Schematic of a simple inertial seismometer.
alt: Schematic of a simple inertial seismometer.
---

Schematic of a simple inertial seismometer
```

We can describe the motion of the suspended mass using Newton’s second law. If $ u(t) $ is the ground displacement and $ z(t) $ is the displacement of the mass relative to the ground, the system behaves as a **damped harmonic oscillator**:

$$
\ddot{z} + 2\epsilon \dot{z} + \omega_0^2 z = -\ddot{u}
$$

This equation shows that the instrument is driven by **ground acceleration**, even if it records displacement.  $ \omega_0^2 = k/m $ and $ \omega_0 $ is the resonant angular frequency.  The damping parameter, $ \epsilon $ is defined such that $ 2\epsilon = D/m $.  

---

## Frequency Response and Damping

To understand how a seismometer modifies signals, it is useful to work in the frequency domain. The response can be written as

$$
\Zeta(\omega) = A(\omega)e^{i\phi(\omega)}
$$

where:
- $ A(\omega) $ describes how amplitudes are scaled  
- $ \phi(\omega) $ describes phase shifts  

**The key point is that both amplitude and phase depend on frequency**, so a seismometer acts as a **filter** that modifies ground motion in a predictable way.

Assuming harmonic motion,

$$
u(t) = U(\omega)e^{-i\omega t}, \quad z(t) = Z(\omega)e^{-i\omega t}
$$

the frequency response can be written as

$$
\frac{Z(\omega)}{U(\omega)}
=
\frac{\omega^2}{\omega_0^2 - \omega^2 - 2ih\omega_0\omega}
$$

where the dimensionless damping parameter is

$$
h = \frac{\epsilon}{\omega_0}
$$

The parameter $ h $ controls the damping:

- $ h < 1 $: **underdamped** (resonance and ringing)  
- $ h = 1 $: **critically damped** (stable, optimal response)  
- $ h > 1 $: **overdamped** (sluggish response)  

At high frequencies ($ \omega \gg \omega_0 $), the mass remains nearly stationary and the instrument tracks ground motion well. At low frequencies ($ \omega \ll \omega_0 $), the response decreases and the instrument becomes less sensitive. In practice, seismometers record only a limited frequency band.

```{figure} ../figures/11_response_functions.png
---
name: Example response functions
alt: Amplitude and phase response functions for a seismometer with different damping values h
width: 500px
---

Amplitude and phase response functions for a seismometer with a 1 Hz natural frequency. The damping parameter $h$ controls the sharpness and stability of the response.
```

---

## What Do Seismometers Measure?

Instruments may record displacement, velocity, or acceleration. In the frequency domain, each time derivative introduces a factor of $\omega$, so:

- Acceleration emphasizes high frequencies  
- Displacement emphasizes low frequencies  

At very long periods, even a displacement sensor effectively responds to **ground acceleration**.

---

## What Makes a Good Seismometer?

In practice, we would like a seismometer to record ground motion **faithfully**, without distorting the signal. This corresponds to having a **flat response** over a broad frequency band.

- A **flat amplitude response** means all frequencies are recorded with equal sensitivity  
- A **linear phase response** means the waveform shape is preserved  

If the response is not flat, the instrument will:

- amplify some frequencies (e.g., near resonance)  
- suppress others (e.g., long-period signals)  
- introduce phase shifts that distort waveforms  

This is why real seismometers are designed to operate over a specific **frequency band** where the response is approximately flat.

While, in principle, ground motion can be recovered from any well-characterized instrument via deconvolution, in practice nonlinear effects (clipping), noise amplification, and imperfect knowledge of the response make such inversion unstable—motivating the design of broadband, well-damped instruments with flat, robust responses.

```{figure} ../figures/clipped_data.jpg
---
name: Example clipped data
alt: Seismograms of the magnitude 4.8 earthquake that occurred in Yellowstone on March 30, 2014 with the top record being clipped and the bottom showing undistored waveforms
width: 800px
---

Seismograms of the magnitude 4.8 earthquake that occurred in Yellowstone on March 30, 2014, as recorded by seismometers at station YNR near Norris Geyser Basin.  Top: Seismogram recorded on the accelerometer, which stayed on scale during the shaking.  Bottom: “Clipped” seismogram recorded on the broadband seismometer, which went off scale during the shaking.  Credit USGS.
```

---

## Modern Seismographs

Modern instruments are designed to record signals over a wide range of amplitudes and frequencies.  Modern broadband seismometers use **force-feedback systems** to extend the flat portion of the response far beyond what is possible with simple mechanical designs.

- **Short-period instruments** (higher $ \omega_0 $) are sensitive to high-frequency body waves  
- **Long-period instruments** (lower $ \omega_0 $) are sensitive to low-frequency signals like surface waves  
- **Broadband instruments** are designed to have a flat response over a wide range of frequencies  

A key concept is **dynamic range**, which describes the range between the smallest and largest signals that can be recorded. Instruments must be sensitive enough to detect weak signals, while avoiding clipping during strong ground motion.

To achieve this, many instruments use **force-feedback designs**, where the mass is held nearly fixed and the recorded signal is proportional to the force required to keep it in place. This improves both linearity and bandwidth.

Digital recording systems (typically 24-bit) now provide very large dynamic ranges, allowing a single instrument to capture both small and large signals.

In regions of strong shaking, specialized **strong-motion instruments** (accelerometers) are used to avoid clipping and to record large ground accelerations.

---

## Instrument Response

Seismographs record **digital counts**, not ground motion directly. To interpret the data, we must know how the instrument modifies the signal.

This is described by the **instrument response function**, which specifies how amplitude and phase vary with frequency.

A seismogram is only meaningful if the instrument response is known.

---

## Short- vs Long-Period Seismology

Seismic observations are often divided into two bands, separated by the **microseism noise peak** near periods of 6–8 seconds.

- **Short-period (high frequency)** data are dominated by body waves and are used for earthquake location and arrival-time analysis.
- **Long-period (low frequency)** data emphasize surface waves and are particularly useful for studying earthquake sources and modeling waveforms.


---

## Summary

Seismometers are physical systems that respond to ground motion according to well-defined equations. They act as frequency-dependent filters, and their design determines what parts of the seismic signal are recorded most clearly.

Understanding instrument response is essential for:
- Interpreting seismic data  
- Comparing observations across stations  
- Recovering true ground motion  