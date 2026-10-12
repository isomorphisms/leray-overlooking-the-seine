# FluidX3D — lattice-Boltzmann cross-check

**Source:** [ProjectPhysX/FluidX3D](https://github.com/ProjectPhysX/FluidX3D)

**Numerics.** C++/OpenCL GPU-oriented lattice Boltzmann method (LBM), generally using voxelized solid boundaries rather than the finite-volume Navier–Stokes discretizations of the other codes. A potentially useful distinct numerical formulation for unsteady wakes.

**Why riff on it.** If the proposed denticle-induced vortices appear even with a substantially different discrete fluid model, they are less likely to be artifacts of a single pressure-projection or finite-volume implementation. GPU computation may make visually rich comparisons practical.

**Concrete first experiment.** Resolve one denticle on a flat plate with a systematic voxel-size sweep. Plot the downstream cross-plane streamwise vorticity, wake separation, and integrated force, matching Reynolds number and wall conditions with an independent solver. Only then examine a denticle row on an airfoil.

**Risk.** Voxelization may staircase or eliminate tiny ridge tips, and LBM wall/boundary accuracy and stability at the chosen Reynolds number need separate checks. Do not infer microstructure effects when geometry is represented by only a handful of voxels. GPU speed cannot replace refinement.

**License:** **source-available but not OSI open source**. Upstream allows non-commercial research/education and restricts commercial use; check the actual license before any reuse or distribution. Its code is C++/OpenCL; it is not being proposed as a project dependency.

**Borrow:** alternate kinetic discretization, memory/layout ideas, GPU wake visualization. **Decision:** optional cross-check, with license restrictions clearly separated from open-source options.
