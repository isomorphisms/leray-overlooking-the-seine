# William L. Burke: forms, flow, and physical geometry

**Working identification:** the requested “Burke” is provisionally taken to mean William L. Burke, author of *Applied Differential Geometry*.

## Applied Differential Geometry

**William L. Burke (1985).** Cambridge University Press. [Publisher and contents](https://www.cambridge.org/us/universitypress/subjects/mathematics/geometry-and-topology/applied-differential-geometry) · [DOI](https://doi.org/10.1017/CBO9781139171786).

Burke introduces differential geometry through physical quantities and geometric reasoning. The book develops differential forms, twisted forms, the Hodge star, exterior differential systems, and symplectic geometry through applications. The useful starting points are chapters 4–5 on exterior calculus and applications, followed by chapter 7 on particle and field dynamics.

The distinction to keep visible is what a quantity measures. Circulation accumulates along a curve; flux crosses a surface; mass occupies a volume. Forms organize these quantities by the objects over which they can be integrated. Turning one kind of object into another can require a metric. This makes the Hodge star worth examining separately from exterior differentiation.

## Div, Grad, Curl Are Dead

**William L. Burke (1995).** Preliminary manuscript, version 2.0, October 1995. [Author's contents](https://www.ucolick.org/~burke/forms/dgcad.html) · [UCSC-hosted scan](https://people.ucsc.edu/~rmont/papers/Burke_DivGradCurl.pdf).

The relevant contents cover gradients, flow in two and three dimensions, and density; ordinary and twisted forms, integration, Stokes' theorem, the star operator, and Lie derivatives; then Hamiltonian mechanics, Lagrangian mechanics, fluid mechanics, and water waves. Those later subjects are verified contents entries: the completeness of every listed section has not been checked.

## Questions to carry into a solver

These are proposed connections, rather than numerical results attributed to Burke:

- Which stored quantities represent circulation, surface flux, and volume density?
- Which discrete identities depend only on how vertices, edges, faces, and cells meet?
- Which operations require metric information or material coefficients?
- Does the solver preserve these distinctions as the mesh changes?

Follow this strand into [compatible discretization](geometry-to-cfd.md). Follow the mechanics strand into [Singer](stephanie-frank-singer.md).
