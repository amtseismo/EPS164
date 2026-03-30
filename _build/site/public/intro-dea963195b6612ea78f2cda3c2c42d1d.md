# EPS 164: Introduction to Seismology

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Deploy Book](https://github.com/amtseismo/EPS164/actions/workflows/deploy.yml/badge.svg)](https://github.com/amtseismo/EPS164/actions/workflows/deploy.yml)

Lecture notes, notebooks, and other course content for **EPS 164** Seismology at the University of California, Davis by Amanda Thomas. Materials supplement Peter Shearer's *Introduction to Seismology 3rd Edition* with hands-on Python exercises using real seismic data.

**📖 Course site:** <https://amtseismo.github.io/EPS164/>

```{figure} 3_toppled_train.png
:scale: 100 %
:alt: A Narrow Gauge train on the North Shore Railroad toppled on its side at Point Reyes Station, California, during the 1906 San Francisco earthquake on April 18. The 5:15 a.m. locomotive,, which was on a siding for fueling, was overturned by intense ground shaking. 

A train thrown down by the earthquake at Point Reyes Station. The train was standing on a siding. Beyond are the buildings of the Point Reyes Hotel and, on the extreme right, the ruin of a stone store which was shaken down.

```

## Course Schedule

| Module | Lecture | Labs | Topics |
|--------|---------|------|--------|
| 1 — Data Foundations | — | 01 | FDSN data access, ObsPy, Fourier analysis, filtering |
| 2 — Stress & Strain | [Stress & Strain](lectures/02_Stress_Strain_Lecture.md) | 02 | Elastic constants, stress/strain tensors, Hooke's Law |
| 3 — Body Waves | [Ray Theory](lectures/ray-theory.md) | 03a–c | P/S polarization, ray tracing (PyKonal), global phases (TauP) |
| 4 — Reflection | — | 04a–b | Reflection/transmission coefficients, CMP, NMO, migration |
| 5 — Surface Waves | [Surface Waves](lectures/surface-waves.md) | 05a–d | Rayleigh & Love waves, dispersion, ambient noise |
| 6 — Earthquake Sources | [Inverse Problem](lectures/earthquake-location.md) | 06a | Earthquake location methods & uncertainties |
| 7 — Moment Tensors & Magnitudes | [Moment Tensors](lectures/moment-tensor.md), [Radiation Patterns](lectures/07b-radiation-patterns.md), [Magnitudes](lectures/07c-magnitudes.md) | 07a–d | Moment tensor decomposition, radiation patterns, magnitude scales |
| Optional | [Tomography](lectures/tomography-lecture-whiteboard.md) | — | Travel-time tomography, surface wave inversion |

Each notebook includes a Colab badge — click it to run in Google Colab with no local setup.

## Acknowledgments

- Course lectures and notes include some material from ESS 412/512 taught by Marine Denolle at the University of Washington (thanks Marine!)
- Course structure based on Peter Shearer's *Introduction to Seismology* (Cambridge University Press)
- Built with [ObsPy](https://obspy.org/), [Jupyter Book](https://jupyterbook.org/), and [sphinxcontrib-bibtex](https://sphinxcontrib-bibtex.readthedocs.io/)
- Seismic data from [Earthscope Consortium](https://www.earthscope.org/) via FDSN web services

## License

MIT — see [LICENSE](LICENSE).

## Contact

**Instructor**: Amanda M. Thomas, University of California, Davis <br>
**Email**: amthom@ucdavis.edu <br>
**Website**: [amtseismo.github.io](https://amtseismo.github.io/) <br>
**Repo**: <https://github.com/amtseismo/EPS164>
