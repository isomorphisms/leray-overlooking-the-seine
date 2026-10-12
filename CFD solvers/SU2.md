# SU2 — airfoil polars and geometry optimization

**Source:** [SU2](https://github.com/su2code/SU2) · [governing equations / turbulence models](https://github.com/su2code/su2code.github.io/blob/master/_docs_v7/Theory.md)

**Numerics.** C++-based CFD and PDE-constrained design toolkit with compressible/incompressible flow solvers, finite-volume discretization, RANS closures (including SA/SST variants), adjoints, and design optimization.

**Why riff on it.** Unlike local flat-plate solvers, SU2 is set up to ask aerodynamic questions: what changes the **lift–drag polar**, at which angle, and with what geometric placement? Adjoint/sensitivity tools may eventually help vary a parametrized denticle or chordwise row position.

**Concrete first experiment.** Reproduce a smooth NACA0012 polar at the paper's chord Reynolds number with a documented 3D finite-span geometry (or label a 2D sectional approximation honestly). Add a matched 2D bump to test local suction. Only then mesh the 3D denticle row and compare forces, pressure, and wall shear over an angle sweep. Check external-force reference area and sign conventions carefully.

**Risk.** The optimization capability does not make the turbulence and wall treatments correct at sub-millimetre protrusions. RANS may not reproduce unsteady vortex structures accurately. A 2D optimization might prefer a bump with no relevance to 3D vortex generation. The source is C++; treat it as a research reference rather than a mandated project dependency.

**Borrow:** standard polar/force reporting, adjoint design ideas, validation against airfoil data, parameter studies.

**Decision:** best suited to the *aerodynamic performance* question, after a geometry-resolved flow baseline exists.
