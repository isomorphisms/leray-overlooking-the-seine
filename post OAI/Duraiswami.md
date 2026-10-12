# Ramani Duraiswami and swirl-collapse

**Direct follow-up.** Sources reviewed on **12 October 2026**.

Duraiswami's **15 September 2026** preprint asks whether parts of OpenAI's construction can be computed and related to a possible fluid experiment. It connects the leading swirl profile with his earlier work on flow between porous cylinders.

## What was automated

Claude Fable 5.1 wrote and tested the solver and analysis code, ran computations, kept the research log and drafted the paper. Duraiswami chose the questions, supplied the earlier mathematics, checked derivations and made the scientific judgments.

## What was computed

The study solves selected flow profiles, follows solution branches as parameters change, and examines the central flow and matching conditions. It uses Chebyshev collocation and continuation, with numerical checks described in the paper.

## What remains open

The complete blowup flow was not reproduced. Some stability calculations failed to converge as resolution increased. Duraiswami calls the **12–15 September** study finished and leaves explicit questions for others to pursue. The proposed experiment has not established an engineering CFD improvement.

## Sources

- [Paper: Self-similar swirl between contracting porous walls](https://arxiv.org/abs/2609.17642)
- [Full text, including the AI contribution statement and open questions](https://arxiv.org/html/2609.17642v1)
- [Code, tests and research log](https://gitlab.umiacs.umd.edu/ramanid/swirl-collapse)

[Back to post OAI](README.md)
