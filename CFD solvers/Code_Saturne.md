# Code_Saturne — independent industrial finite-volume check

**Source:** [code_saturne](https://github.com/code-saturne/code_saturne)

**Numerics.** EDF's C/Fortran computational fluid dynamics system, with cell-centered finite volumes on unstructured meshes (including polyhedra), incompressible or weakly/compressibly varying fluid models, turbulence modeling, and parallel MPI execution.

**Why riff on it.** The original shark-denticle authors used ANSYS CFX and an SST turbulence model for a single denticle on a plate. Code_Saturne offers a separate, inspectable industrial-style implementation for testing how sensitive that predicted wake is to discretization and closure.

**Concrete first experiment.** Mesh the published single denticle on a flat plate. Start with an SST-style RANS/URANS comparison where supported, extracting the separation bubble and downstream ωₓ slice. Then reconstruct the smooth NACA0012 baseline before introducing the denticle row. Preserve inlet turbulence parameters and wall resolution in the comparison.

**Risk.** A matching turbulence-model name does **not** make two simulations independent validations of physics. Small protrusions need local surface fidelity, wall-normal inflation layers, and geometry convergence. Defaults for wall functions, transition, and mesh quality can dominate the signal.

**Borrow:** unstructured finite-volume geometry handling, conservative flux bookkeeping, industrial turbulence/force reporting, cross-code benchmarking.

**Decision:** practical independent numerical baseline, especially for comparison to the published CFX setup.
