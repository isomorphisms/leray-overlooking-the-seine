# CFD solvers: shark-denticle lift

Research notes for [Leray overlooking the Seine](../README.md). These are **candidate methods to inspect and compare**, not installed dependencies or claims that simulations have been run.

## The actual phenomenon

The motivating experiment is Domel et al. (2018), [*Shark skin-inspired designs that improve aerodynamic performance*](https://doi.org/10.1098/rsif.2017.0828), with [supplementary data](https://doi.org/10.6084/m9.figshare.c.3986802.v3). Its NACA0012 airfoil carried three-dimensional, shark-denticle-inspired protrusions on the suction side. Some arrangements increased lift and reduced drag. The headline **up to 323% improvement** refers to **lift-to-drag ratio**, **not** a 323% increase in lift, and only to selected conditions.

The paper proposes two coupled mechanisms:

1. A short separation bubble downstream of a denticle changes surface pressure, enhancing suction and thus lift.
2. Streamwise vortices redistribute higher-momentum outer fluid toward the near-wall layer, potentially postponing separation and reducing drag.

These are evidence-backed proposed explanations, not an unexplained violation of fluid mechanics. Crucially, *shark-like riblets* (longitudinal microgrooves studied mainly for skin-friction reduction) are not the same shape or mechanism as discrete, tilted *denticles* acting as vortex generators. Keep the experimental geometries separate.

## What to model

Start with the [common experimental and numerical protocol](shark-denticle-lift.md). In particular, contrast a smooth foil, a two-dimensional bump with matched chordwise profile, and an actual three-dimensional denticle arrangement. The bump is an essential counterexample: a purely two-dimensional model cannot generate the claimed pair of streamwise vortices.

| Solver | Numerical family | First useful question | Principal obstacle |
| --- | --- | --- | --- |
| [Basilisk](Basilisk.md) | Adaptive finite volume, embedded boundaries | Does resolving local wake/suction change the lift? | Fine near-wall three-dimensional geometry |
| [Xcompact3d](Xcompact3d.md) | High-order finite differences, immersed boundary | Do coherent streamwise vortices survive better-resolved flow? | Large structured-grid DNS/LES |
| [WaterLily](WaterLily.md) | Cartesian incompressible, immersed boundary | Can we visualize and vary individual denticle wakes quickly? | Small features demand many cells |
| [Nek5000](Nek5000.md) | High-order spectral elements | Does a high-order reference reproduce wake and wall stresses? | Curved conforming meshes |
| [Dedalus](Dedalus.md) | Spectral PDE framework | Which simplified instability/pressure mechanisms are plausible? | Not a turnkey complex-airfoil mesher |
| [Code_Saturne](Code_Saturne.md) | Industrial unstructured finite volume | Can an independent 3D RANS/LES setup replicate force trends? | Near-wall mesh and model dependence |
| [SU2](SU2.md) | Finite-volume aerodynamics and optimization | What geometry/placement shifts the lift–drag polar? | C++ dependency; RANS may hide small vortices |
| [OpenFOAM](OpenFOAM.md) | Finite volume with surface meshing | Can we build a documented 3D comparison to the published CFX model? | Tiny protrusions and boundary layers |
| [JAX-CFD](JAX-CFD.md) | Differentiable periodic-grid CFD | Can a reduced flow model distinguish rival hypotheses? | Unmaintained; no direct wall/airfoil case |
| [FluidX3D](FluidX3D.md) | GPU lattice Boltzmann | Does a second numerical formulation show comparable vortical structures? | Voxel resolution, licensing restrictions |

## Order of attack

1. Reproduce or digitize **published** quantities and geometry, including the paper's ANSYS CFX/SST single-denticle case; record what is extracted versus reconstructed.
2. Begin a **3D single-denticle flat-plate** calculation; compare separation region and streamwise-vorticity cross-section.
3. Establish a **smooth NACA0012** lift/drag baseline near the paper's Reynolds number, including span and support/finite-wing caveats.
4. Compare the **2D bump** and the **3D denticle row** at identical flow conditions, wall treatment, and reference area.
5. Require convergence and agreement between at least two genuinely independent discretizations before assigning causal significance to a predicted lift gain.

A small implementation can use Basilisk/WaterLily for experiments, Xcompact3d/Nek5000 for high-fidelity checks, and OpenFOAM/Code_Saturne/SU2 as independent practical baselines. These are **alternatives**, not ten packages to integrate. The C++ implementations are research references only; nothing in this folder imposes C++ on Leray or the wider build system.

**Reproducibility rule:** report a negative result just as prominently as a positive one. Never transfer a rough-wall skin-friction result into an airfoil-lift claim without actually simulating the airfoil.

## Contact and symplectic geometry

A companion [contact and symplectic collection](../contact-symplectic/README.md) follows the geometry of motion, ideal-fluid topology, and numerical structure. Start with [geometry and CFD](../contact-symplectic/geometry-to-cfd.md) for variational fluids, compatible exterior calculus, helicity, and QuFlow, or the [proposed experiments](../contact-symplectic/questions-and-experiments.md) for exact reference fields and pressure-error comparisons.

## Video companion: Physics of Life

[Scott Turner's videos and course guide](../notes/scott-turner-physics-of-life.md) provide experiments and biological examples for Reynolds number, boundary layers, drag and vortex shedding, including the cylinder-and-dye flume demonstration.
