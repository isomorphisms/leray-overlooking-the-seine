# Xcompact3d — high-order turbulence and immersed solids

**Source:** [Xcompact3d / Incompact3d](https://github.com/xcompact3d/Incompact3d) · [methodology](https://xcompact3d.readthedocs.io/en/latest/pages/methodology.html)

**Numerics.** Fortran, sixth-order compact finite differences on a Cartesian grid, pressure Poisson solution using FFTs, and immersed-boundary forcing for solids. Designed for direct numerical simulation (DNS) and large-eddy simulation (LES), including wall-bounded flow.

**Why riff on it.** If the hypothesis is that a denticle makes **streamwise vortex pairs** that move momentum toward the wall, their three-dimensional wake structure and time evolution matter more than a single lift number. High-order discretization reduces ambiguity from numerically smeared vortices.

**Concrete first experiment.** Begin from the project's channel-flow or smooth-cylinder validation examples. Introduce an isolated denticle on a flat plate, use periodic spanwise boundaries only when physically defensible, and compare the cross-plane ωₓ field with the original paper's single-denticle CFX figure. Examine vortex persistence, wall shear, and sensitivity to denticle span/tilt.

**Risk.** The whole grid is structurally expensive at the small feature scales, and immersed-boundary interpolation can modify the effective ridge shape and wall stress. A periodic span may change the apparent interaction between neighboring vortices. High-order DNS at full experimental wing scale may be prohibitively expensive; LES closure choices remain consequential.

**Borrow:** pencil-decomposed high-order operations, pressure projection, immersed-boundary validation, spectral-like derivative accuracy, DNS/LES methodology.

**Decision:** preferred high-fidelity *vortex mechanism* check; first target a local 3D patch, not the entire airfoil.
