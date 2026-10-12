# RPI AI CFD Scientist

**Earlier comparator, not an adoption of OpenAI's September result.** Sources reviewed on **12 October 2026**.

Shaowu Pan's group at Rensselaer Polytechnic Institute introduced AI CFD Scientist in **May 2026**. It connects literature reading, experiment design, OpenFOAM execution through Foam-Agent, model changes, numerical comparisons and report writing.

## What is automated

The system can generate and compile physical-model changes, run parameter studies and revise hypotheses against reference data. Its checks include mesh refinement and inspection of computed flow images. This extends beyond preparing input files for an unchanged solver.

## What was demonstrated

The paper evaluates five tasks using GPT-5.5. On a periodic-hill benchmark at Reynolds number **5600**, a Spalart–Allmaras turbulence-model correction reduced **lower-wall skin-friction RMSE by 7.89%** against direct numerical simulation. A separate check detected **14 of 16** planted failures missed by solver-level checks.

These are bounded benchmark results. They do not establish a general improvement to turbulence modelling.

## Why include it here

It supplies a concrete example of an automated CFD research process. Applying that process productively to OpenAI's later construction remains untested in the sources reviewed.

## Sources

- [Paper and author list](https://arxiv.org/abs/2605.06607)
- [Code, prompts and research artifacts](https://github.com/csml-rpi/cfd-scientist)
- [Foam-Agent](https://github.com/csml-rpi/Foam-Agent)

[Back to post OAI](README.md)
