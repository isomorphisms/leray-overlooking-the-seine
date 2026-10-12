# WaterLily — rapid moving-geometry flow experiments

**Source:** [WaterLily.jl](https://github.com/WaterLily-jl/WaterLily.jl) · [documentation](https://waterlily-jl.github.io/WaterLily.jl/stable/)

**Numerics.** Julia implementation of unsteady incompressible 2D/3D Navier–Stokes on Cartesian grids, geometric-multigrid pressure solution, and Boundary Data Immersion Method for solid shapes; serial CPU, multithreaded CPU, and GPU backends.

**Why riff on it.** Its simple geometry description and immersed solid machinery make it a useful visual laboratory for changing denticle height, lean, location, and spacing. Geometry variation can reveal which shapes actually create coherent wakes before committing to difficult airfoil meshing.

**Concrete first experiment.** Model a denticle profile over a moving-flow rectangular box. Vary ridge height while holding Reynolds number and domain dimensions fixed. Export time-dependent streamline fields, pressure near the wake, 3D vorticity slices, and integrated forces on the solid. Then place one row on the suction side of a simple foil and compare with the same foil without protrusions.

**Risk.** A fast visualization at low grid resolution can give the wrong wall stress, effective curvature, or separation bubble. A 2D profile can illustrate suction, but cannot resolve the spanwise vortex hypothesis; 3D and grid convergence are mandatory. GPU speed does not automatically imply accuracy.

**Borrow:** compact experiment structure, immersed-body representation, geometry animation/visualization, CPU/GPU comparative runs.

**Decision:** fast exploratory prototype and visual check, not primary evidence for the published lift-to-drag improvement.
