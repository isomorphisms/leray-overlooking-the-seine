# Contact and symplectic geometry

A growing collection for [Leray overlooking the Seine](../README.md), beginning with **Eva Miranda, William L. Burke, and Stephanie Frank Singer**. The aim is to follow several mathematical threads: how motion acquires geometric structure, what topology can force a flow to do, and how numerical approximations can retain some of that structure.

“Burke” is provisionally identified as **William L. Burke**, author of *Applied Differential Geometry*. The surname alone did not settle the identification.

## Where to begin

| Reading thread | What to look for |
| --- | --- |
| [Geometry in plain words](geometry-in-plain-words.md) | Forms, symplectic structure, contact planes, Reeb fields, and the actual Beltrami correspondence |
| [William L. Burke](william-burke.md) | Circulation, flux, differential forms, and the metric hidden in vector calculus |
| [Stephanie Frank Singer](stephanie-frank-singer.md) | Mechanics through symmetry, momentum maps, and reduction |
| [Eva Miranda and collaborators](eva-miranda.md) | Singular geometry, Euler flows, Reeb embeddings, and computation inside trajectories |
| [Etnyre and Ghrist](etnyre-ghrist.md) | Contact topology and hydrodynamics I–III; periodic and knotted trajectories |
| [Foundations](foundations.md) | Arnold–Khesin, Marsden–Ratiu, Marsden–Weinstein, Cannas da Silva, and Geiges |
| [Wider symplectic topology](symplectic-topology.md) | Gromov, Taubes, Hutchings, McDuff–Schlenk; holomorphic curves, periodic orbits, and embedding obstructions |
| [Geometry and CFD](geometry-to-cfd.md) | Variational fluids, compatible discretization, helicity, and QuFlow |
| [Questions and experiments](questions-and-experiments.md) | Small calculations and open-ended threads that can connect these readings |
| [Bibliographic records](references.bib) | Sources collected for this folder |

A short route is **Burke → Singer → Etnyre–Ghrist → Miranda**. A numerical route is **forms → Arnold's fluid viewpoint → variational/compatible discretization**. The topology reading can also be pursued independently.

## Four settings worth keeping visible

| Setting | Typical object | What a result concerns |
| --- | --- | --- |
| Finite-dimensional mechanics | Positions and momenta | Symplectic forms, conserved quantities, reduction |
| Ideal incompressible fluid | Smooth Euler velocity and advected particles/vorticity | Geodesic or Lie–Poisson descriptions, circulation, helicity |
| Contact dynamics | Contact form and its Reeb field | Periodic orbits, knotting, return maps, computational complexity |
| Viscous numerical flow | Mesh, time step, viscosity, boundary conditions | Discrete balances, convergence, pressure and force errors |

These settings have specific bridges, explained in the linked notes. In particular, a Reeb realization can require a chosen metric; an ideal-flow invariant can acquire viscous and boundary terms; and contact nondegeneracy can fail at a no-slip wall.

## Connections already in this repository

- [CFD solver notes](../CFD%20solvers/README.md) and the [shark-denticle experiment](../CFD%20solvers/shark-denticle-lift.md).
- [Leray, experiments, and flow control](../notes/theory-experiment-and-flow-control.md).
- [Numerical work following the OpenAI papers](../post%20OAI/README.md).

The present collection adds mathematical routes into those discussions. Its proposed experiments have not been run. Source checking on 12 October 2026 covered primary publisher/archive records and accessible abstracts, introductions, selected theorem statements, and book contents; it was not a complete reading of every proof. Papers remain linked at their sources.

The bibliography is local to this folder so the collection can grow alongside the repository's other citation work.
