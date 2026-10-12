# Geometry and CFD: places where the connection is concrete

Geometry can help specify what a discretization should represent or preserve. To assess a proposed method, name the quantity, the discrete object carrying it, the assumptions under which it is conserved, and the error being measured.

[Arnold–Khesin](foundations.md) provides the ideal-fluid setting. The following papers develop actual numerical formulations.

## Pavlov and colleagues: derive a discrete fluid from geometry

**Dmitry Pavlov, Patrick Mullen, Yiying Tong, Eva Kanso, Jerrold E. Marsden, Mathieu Desbrun (2011), “Structure-preserving discretization of incompressible fluids.”** *Physica D* 240(6), 443–458. [Paper](https://arxiv.org/abs/0912.3989) · [DOI](https://doi.org/10.1016/j.physd.2010.10.012).

The method approximates the volume-preserving diffeomorphism group by a finite-dimensional Lie group. Discrete Euler equations follow from a variational principle with nonholonomic constraints. The resulting scheme has an exact discrete Kelvin circulation theorem and good long-term energy behavior.

This is a direct route from the geometry of fluid-particle relabeling to a numerical method. Good energy behavior should not be relabeled exact energy conservation. Viscosity and the chosen wall conditions require their own treatment.

## Gawlik and colleagues: include transported quantities

**Evan S. Gawlik, Patrick Mullen, Dmitry Pavlov, Jerrold E. Marsden, Mathieu Desbrun (2011), “Geometric, Variational Discretization of Continuum Theories.”** *Physica D* 240(21), 1724–1760. [Paper](https://arxiv.org/abs/1010.4851) · [DOI](https://doi.org/10.1016/j.physd.2011.07.011).

Euler–Poincaré equations with advection extend the geometric framework to ideal fluids, magnetohydrodynamics, and complex fluids. The paper derives and tests methods in which velocity and transported quantities participate in a common variational description. Reported properties include symmetry-related momentum preservation, solenoidal constraints, and good long-term energy behavior.

A possible extension for this repository is to inspect how a transported scalar or director is coupled without losing the intended geometric relations.

## Rebholz: helicity enters a Navier–Stokes scheme

**Leo G. Rebholz (2007), “An Energy- and Helicity-Conserving Finite Element Scheme for the Navier–Stokes Equations.”** *SIAM Journal on Numerical Analysis* 45(4), 1622–1638. [Publisher abstract and DOI](https://epubs.siam.org/doi/10.1137/060651227).

The scheme combines forms of the nonlinearity, solves for velocity and projected vorticity, and uses trapezoidal time stepping. The stated exact conservation of energy and helicity is **in the absence of viscosity and external forcing**. Stability and convergence are also established.

The publisher abstract was checked; the full article's boundary assumptions remain a reading item. Begin any comparison with a periodic benchmark, and inspect the full formulation before transferring the result to another boundary class.

## Carlier, Campos Pinto, and Fambri: compatible exterior calculus

**Valentin Carlier, Martin Campos Pinto, Francesco Fambri, “Mass, momentum and energy preserving FEEC and broken-FEEC schemes for the incompressible Navier–Stokes equations.”** Preprint 2023. [Manuscript](https://arxiv.org/abs/2306.13778) · [Journal version DOI](https://doi.org/10.1093/imanum/drae047).

**Finite-element exterior calculus**, or FEEC, organizes discrete spaces so that differential operators fit together as they do in the de Rham sequence. Here the formulation also uses an explicitly skew-symmetric advection operator. The conforming and broken formulations address discrete incompressibility, pressure robustness, and energy behavior; the broken method permits controlled stabilization.

The inspected manuscript develops and tests the two-dimensional case and discusses extension and boundary treatment. Read its balance laws with viscosity and boundary terms present. “Energy preserving” in a title does not require suppressing physical viscous loss.

**Pressure robustness** has a concrete meaning to test: a force that is a pure gradient can be balanced by changing pressure, without changing the exact incompressible velocity. The experiment below asks whether a discretization respects that.

## Modin and Viviani, with QuFlow

**Klas Modin and Milo Viviani (2020), “A Casimir preserving scheme for long-time simulation of spherical ideal hydrodynamics.”** *Journal of Fluid Mechanics* 884, A22. [Paper](https://arxiv.org/abs/1812.11055) · [DOI](https://doi.org/10.1017/jfm.2019.944) · [Official QuFlow repository](https://github.com/klasmodin/quflow).

The method approximates two-dimensional incompressible Euler flow on a sphere through geometric quantization and Lie–Poisson integration. Its finite-dimensional dynamics preserve discrete **Casimirs**: quantities fixed by the underlying Poisson geometry. The number of independent discrete invariants grows with spatial resolution.

QuFlow supplies an inspectable implementation of quantized vorticity flows. Its official repository identifies a Python implementation and an MIT license. It is a research reference here; no installation or run was performed. Its spherical ideal-flow setting does not supply a wall-resolved airfoil case.

## A working map

| Idea | Fluid or discrete object | Proposed use |
| --- | --- | --- |
| Kelvin circulation | Velocity integral around an advected material loop | Measure circulation drift in an ideal-flow experiment |
| Lie–Poisson geometry | Reduced fluid state and its bracket | Study whether the spatial model and time integrator preserve the same structure |
| Helicity | Integral of u · curl u | Compare a known inviscid invariant or a viscous/boundary balance |
| Contact/Reeb geometry | Nonsingular rotational Beltrami trajectories | Exact fields, closed-orbit tracing, and return maps |
| de Rham sequence | Compatible gradient, curl, and divergence maps | Examine discrete incompressibility and pressure robustness |
| Geometric quantization | Spherical functions approximated by matrices | Compare discrete Casimirs and long-time vortex organization |

A symplectic time integrator alone does not supply a compatible spatial discretization. A compatible spatial complex alone does not supply a turbulence model or all conservation laws. The [questions and experiments](questions-and-experiments.md) specify small ways to separate these effects.

For the existing [CFD solvers](../CFD%20solvers/README.md), these are candidate methods and diagnostics to investigate. The individual solver's documentation and equations must establish which property it actually implements.
