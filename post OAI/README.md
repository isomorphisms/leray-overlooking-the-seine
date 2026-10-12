# post OAI

Summaries of numerical and automated CFD work connected with OpenAI's September 2026 Navier–Stokes result. Sources reviewed on **12 October 2026**.

OpenAI's [published construction](https://openai.com/index/navier-stokes-solution/) describes a specially forced, three-dimensional incompressible flow whose speed becomes unbounded in finite time while its kinetic energy remains bounded. The projects below explore different ways to turn mathematical work into computations.

## Projects

| Note | Relationship | What to learn from it |
|---|---|---|
| [Ramani Duraiswami: swirl-collapse](Duraiswami.md) | Direct numerical follow-up | Human-directed AI implementation of selected flow profiles |
| [James: ns-blowup and Singularity Observatory](ns-blowup.md) | Direct component translation | Executable formulas, numerical diagnostics and implementation gaps |
| [Xavier Callens: MechanicaFluidorum](MechanicaFluidorum.md) | Direct numerical and physical investigation | Tests of different fluid models; further automation remains proposed |
| [RPI: AI CFD Scientist](AI-CFD-Scientist.md) | Earlier comparator, published before the OpenAI result | An automated process connecting papers, model changes, simulations and reports |

Each note links its primary sources and distinguishes implemented calculations from proposed work. None of these sources demonstrates a complete automatic translation of the OpenAI construction into an established improvement for engineering CFD.

## Connection with the Leray project

These examples suggest several routes worth keeping distinct: computing pieces of a mathematical construction, making test cases for numerical methods, comparing physical models, and automating experiments with existing solvers. Their usefulness for near-wall flow, drag control or shark-denticle lift remains an open application question.

See also the [CFD solver notes](../CFD%20solvers/README.md). This folder records the follow-up work; it does not select a solver or settle the construction's practical implications.
