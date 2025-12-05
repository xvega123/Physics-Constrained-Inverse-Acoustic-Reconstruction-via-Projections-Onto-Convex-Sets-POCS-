# Physics-Constrained Inverse Acoustic Reconstruction via Projections Onto Convex Sets (POCS)

Implementation of a **physics-constrained inverse solver** based on **Projections Onto Convex Sets (POCS)** for reconstructing coherent acoustic fields from sparse, irregular, or occluded sensor measurements.

---

## Overview
Conventional interpolation methods (e.g., Kriging, IDW) rely on smoothness priors that often suppress oscillatory wave physics, failing to capture diffraction patterns in measurement gaps. 

This project introduces a **training-free iterative solver** that enforces the **Acoustic Dispersion Relation** as a physical constraint. By iterating between data consistency (physical domain) and physics consistency (spectral domain), the algorithm successfully recovers complex topological features like interference fringes and spiral arms within large shadow zones.

**Paper Reference:**
> **C. Park**, Y. Kwak, S. Choi, "Physics-Constrained Inverse Acoustic Reconstruction via Projections Onto Convex Sets (POCS)," *Advances in Engineering Software* (Submitted), 2025.

---

## Key Features
* **Physics-Constrained Solver:** Uses a "Resonant Tapered Filter" in the spectral domain to enforce the Helmholtz equation without needing training data.
* **Superior Structural Fidelity:** Outperforms standard interpolants in Structural Similarity Index (SSIM) across various scenarios (e.g., Doppler sources, rotating quadrupoles).
* **Gap Filling & Extrapolation:** Capable of reconstructing fields in large shadow zones and extrapolating wave propagation beyond sparse sensor arrays.

---

## Performance Benchmarks
The proposed method was benchmarked against Linear Interpolation, IDW, and Kriging across five canonical scenarios.

| Benchmark Case | Normalized $L_2$ Error (Lower is Better) | SSIM (Higher is Better) |
| :--- | :---: | :---: |
| **Translating Dipole** | **14.6%** (vs >80%) | **84.6%** (vs <57%) |
| **Doppler Source** ($M=0.5$) | **38.8%** (vs >70%) | **80.2%** (vs <60%) |
| **Rotating Quadrupole** | **26.0%** (vs >30%) | **78.1%** (vs <63%) |
| **Cylinder Scattering** | **84.7%** (Best) | **79.3%** (Best) |

*[Note: See the 'Codes' branch for the scripts to reproduce these results.]*

---

## Code Availability
The source code for this project is available upon request. Please contact the author via email for access.

## Contact
For any inquiries regarding the code or research, please contact:
**Chanho Park** xvegaasd@gm.gist.ac.kr
