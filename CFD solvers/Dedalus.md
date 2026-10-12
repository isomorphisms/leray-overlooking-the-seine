# Dedalus — spectral PDE mechanisms, not a full denticle mesher

**Source:** [Dedalus](https://github.com/DedalusProject/dedalus) · [project methods](https://dedalus-project.org/about/)

**Numerics.** Python symbolic equation specifications translated to spectral discretizations, with Fourier and other bases, sparse linear operators, and tau boundary enforcement. Useful for well-structured domains and instability/eigenvalue analysis.

**Why riff on it.** It is suited to studying **why** shear layers, small surface undulations, and streamwise perturbations might amplify or decay. A reduced model can distinguish local pressure response from momentum transfer without confusing that with a fitted 3D airfoil result.

**Concrete first experiment.** Define a simple periodic-spanwise shear-flow model with a prescribed wall perturbation or equivalent forcing. Sweep spanwise wavelength and Reynolds number; observe perturbation growth, pressure response, and kinetic-energy budgets. Record exactly how any effective boundary model approximates a denticle.

**Risk.** Actual tilted, separated, sharp-edged denticles on a finite airfoil are **not** naturally represented by its standard global spectral domains. A transformed-coordinate or immersed treatment would be a substantial separate implementation. Reduced models can test plausibility, not reproduce lift/drag coefficients without geometry and wall physics.

**Borrow:** symbolic PDE entry, spectral derivatives, modal/eigenvalue analysis, linearization against a base flow.

**Decision:** mathematical companion to CFD, not a substitute for a resolved 3D denticle/airfoil simulation.
