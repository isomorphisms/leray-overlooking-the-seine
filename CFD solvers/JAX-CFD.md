# JAX-CFD — differentiable reduced experiments

**Source:** [google/jax-cfd](https://github.com/google/jax-cfd) (its own README explicitly says the repository is **no longer maintained**).

**Numerics.** Python/JAX research package with staggered-grid finite-volume/difference and pseudospectral incompressible methods, automatic differentiation, and accelerated numerical kernels. The upstream README describes its core supported boundary conditions as **periodic**.

**Why riff on it.** Differentiation through a *simplified flow model* can explore which parameters are influential: perturbation amplitude, spanwise periodicity, applied vortex forcing, or pressure sensitivity. Its structure is interesting for learned corrections and numerical sensitivity, independently of a physical airfoil.

**Concrete first experiment.** Implement a well-defined periodic test in which localized forcing represents a stylized near-wall momentum disturbance. Compare predicted streamwise-vorticity statistics and the sensitivity of a proxy pressure quantity to spanwise wavelength. Label all proxies; verify derivatives against finite perturbations.

**Risk.** With only periodic boundary conditions in the documented core, upstream JAX-CFD cannot directly resolve a physical no-slip denticle on an airfoil. It is **not** an honest substitute for the published lift/drag case without substantial boundary and geometry extensions. Automatic differentiation of an under-resolved or incorrectly modeled flow is still differentiation of the wrong model.

**Borrow:** differentiable program structure, parameter sweeps, carefully bounded data-driven closure experiments.

**Decision:** secondary hypothesis laboratory only; do not put it in the main aerodynamic validation chain.
