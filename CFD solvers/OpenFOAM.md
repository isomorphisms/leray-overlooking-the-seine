# OpenFOAM — geometry-resolved finite-volume reproduction

**Source:** [OpenFOAM development tree](https://github.com/OpenFOAM/OpenFOAM-dev) · [snappyHexMesh geometry/mesh guide](https://doc.openfoam.com/2606/tools/pre-processing/mesh/generation/snappyhexmesh/)

**Numerics.** C++ open-source finite-volume framework with incompressible solvers, steady and unsteady turbulence closures, and tools for surface-conforming mesh generation. snappyHexMesh can read triangulated shapes and insert near-wall prismatic layers.

**Why riff on it.** The most direct way to approximate the published single-denticle CFX study in an auditable nonproprietary workflow: import the exact 3D denticle geometry, build a boundary-layer mesh, and evaluate the wake separation and streamwise vortices under an SST-family closure.

**Concrete first experiment.** (1) Mesh smooth flat plate, validate wall flow. (2) Add one digitized denticle, mesh-tip refinement and prism layers. (3) Run a transient comparison, export ωₓ cross-sections and separation length. (4) Repeat with smooth foil, 2D bump foil and row-of-denticles foil; report C_L, C_D and L/D versus angle.

**Risk.** Automated meshing may round off the ridges or collapse prism layers in tight valleys, producing a different *physical* denticle. Wall-function approximations can suppress the microstructure even if it appears in a 3D mesh. Grid count can explode if all small features are resolved across an entire wing. This implementation is C++: no requirement to import C++ into Leray.

**Borrow:** mesh reproducibility, force/post-processing workflow, SST/LES comparisons, unstructured boundary-layer meshing.

**Decision:** strong first attempt at a realistic 3D reproduction and a cross-check of the original CFX analysis.
