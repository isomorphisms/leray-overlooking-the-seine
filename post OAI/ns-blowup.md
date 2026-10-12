# James and ns-blowup

**Direct component translation.** Sources reviewed on **12 October 2026**.

James, GitHub user **james-coder**, combines numerical evaluators for parts of OpenAI's construction with a JAX library for two- and three-dimensional periodic incompressible flow. The Singularity Observatory aims to examine how numerical methods lose accuracy near a known singularity.

## What works

The project implements similarity coordinates, viscosity rescaling, heat-exterior integrals, a periodic spectral solver and numerical checks. Its research notes describe replacing a noncomputable coordinate choice in Lean with an iterative calculation.

## What is automated

The repository preserves a ChatGPT design conversation and supports automated simulations, diagnostics and differentiation through the solver. This does not establish unattended conversion of an entire proof into CFD.

## What remains missing

The complete smooth blowup field and its parameter selection remain unimplemented, including inner profiles, matching, pulses, corrections and localization. The preview lacks walls and obstacles, so it cannot directly represent a wing surface. Checking the upstream Lean proof does not certify the numerical translation.

## Sources

- [Repository and implementation status](https://github.com/james-coder/navier-stokes-blowup)
- [Research notes](https://github.com/james-coder/navier-stokes-blowup/blob/main/docs/research.md)
- [Changelog](https://github.com/james-coder/navier-stokes-blowup/blob/main/CHANGELOG.md)

[Back to post OAI](README.md)
