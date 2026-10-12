# Eva Miranda: contact geometry, singular structures, and fluid computation

Miranda and collaborators supply several threads: the geometry of stationary ideal fluids; the Reeb–Beltrami correspondence; controlled singular geometry near hypersurfaces; and the computational complexity of particle trajectories.

Start with the contact-mirror overview below. Then compare the three-dimensional construction with the later Euclidean result: changing the metric, domain, or resource bound changes what is proved.

## Looking at Euler flows through a contact mirror: Universality and undecidability

**Robert Cardona, Eva Miranda, Daniel Peralta-Salas.** Preprint 2021; EMS Press chapter 2023. [Paper](https://arxiv.org/abs/2107.09471) · [Publisher chapter](https://ems.press/books/standalone/262/5205).

A panoramic entry into the program, with additional undecidability results. Contact geometry turns certain Beltrami-flow questions into Reeb dynamics, allowing geometric constructions to control particle paths. The paper includes flows for which determining whether the orbit of an explicitly encoded initial point is periodic is undecidable.

This can coexist with a theorem guaranteeing some periodic orbit: existence and deciding every specified initial point's fate are different questions. For an experiment, specify a finite observation interval and what a computed trajectory can establish.

## Constructing Turing complete Euler flows in dimension 3

**Robert Cardona, Eva Miranda, Daniel Peralta-Salas, Francisco Presas (2021).** *PNAS* 118(19), e2026818118. [Paper](https://arxiv.org/abs/2012.12828) · [DOI](https://doi.org/10.1073/pnas.2026818118).

The authors construct a smooth stationary incompressible Euler flow on S³ that simulates a universal Turing machine. An area-preserving disk map is realized as a Reeb return map, and the Reeb–Beltrami correspondence supplies an adapted metric. The metric is part of the construction, rather than a prescribed Euclidean metric.

Section 6B also examines a special viscous evolution using the Hodge Laplacian on the constructed Riemannian manifold. For fixed positive viscosity and initial amplitude, decay permits only a finite amount of the original particle-path time to be traversed. The Euler universality theorem should therefore be kept separate from that finite-step Navier–Stokes construction.

## Computability and Beltrami fields in Euclidean space

**Robert Cardona, Eva Miranda, Daniel Peralta-Salas (2023).** *Journal de Mathématiques Pures et Appliquées* 169, 50–81. [Paper](https://arxiv.org/abs/2111.03559) · [DOI](https://doi.org/10.1016/j.matpur.2022.11.007).

This reaches the prescribed Euclidean metric on ℝ³. The universal Beltrami field has infinite energy, and its encoding uses noncompactness. On the standard flat three-torus, the authors instead prove robust simulation of arbitrary tape-bounded Turing machines and quantify a cost in terms of field norms.

The paper therefore separates unrestricted universal computation from arbitrarily complex finite-resource computation. It also constructs Turing-complete dynamics on S² with zero topological entropy, showing that these notions of complexity need not coincide. The finite-resource periodic-domain result is a promising reading route toward bounded numerical examples.

## Universality of Euler flows and flexibility of Reeb embeddings

**Robert Cardona, Eva Miranda, Daniel Peralta-Salas, Francisco Presas (2023).** *Advances in Mathematics* 428, 109142; preprint first posted 2019. [Paper](https://arxiv.org/abs/1911.01963) · [DOI](https://doi.org/10.1016/j.aim.2023.109142).

A nonautonomous flow on a compact manifold can be embedded in a smooth stationary Euler flow on a suitable Riemannian manifold, possibly of higher dimension. Flexibility of Reeb embeddings is a central ingredient; the resulting stationary flows can contain universal computation.

The striking mathematical point is that a velocity field can be time-independent while its particles execute very complicated motion. Ambient dimension and metric are construction data. Realizing the same dynamics in a specified physical fluid domain remains a separate question.

## Euler flows and singular geometric structures

**Robert Cardona, Eva Miranda, Daniel Peralta-Salas (2019).** *Philosophical Transactions of the Royal Society A* 377, 20190034. [Paper](https://arxiv.org/abs/1902.00039) · [DOI](https://doi.org/10.1098/rsta.2019.0034).

For analytic stationary Euler flows on a compact analytic three-manifold, tangent to the boundary when present, the paper revisits Arnold's structure theorem for nonconstant Bernoulli function. Away from an analytic exceptional set, the flow is organized into invariant tori or cylinders. Under additional Morse–Bott assumptions, some singular Bernoulli levels admit b-symplectic descriptions after resolving their topological singularities.

On three-dimensional b-manifolds, it also relates rotational Beltrami fields that are nonvanishing as b-tangent sections to rescaled Reeb fields. Here rotational requires the proportionality factor in curl u = f u to be nowhere zero. The converse chooses an appropriate b-metric and volume form. Cylindrical ends motivate this geometry. Applying it to a wall model would require identifying the actual asymptotic regime and coordinate transformation.

## Symplectic and Poisson geometry on b-manifolds

**Victor Guillemin, Eva Miranda, Ana Rita Pires (2014).** *Advances in Mathematics* 264, 864–896. [Paper](https://arxiv.org/abs/1206.2020) · [DOI](https://doi.org/10.1016/j.aim.2014.07.032).

A b-Poisson bivector has a top exterior power that vanishes transversely along a hypersurface. Its inverse is naturally described using controlled singular forms, locally including a term like dz/z. The paper develops local structure, cohomology, and geometric invariants.

The useful idea is that a prescribed type of degeneracy can admit its own coherent geometry. This provides a foundation for the singular Euler paper. Such a geometric singularity is not automatically a finite-time singularity of a fluid solution.

## Contact structures with singularities: From local to global

**Eva Miranda and Cédric Oms (2023).** *Journal of Geometry and Physics* 192, 104957; preprint first posted 2018. [Paper](https://arxiv.org/abs/1806.05638) · [DOI](https://doi.org/10.1016/j.geomphys.2023.104957).

This develops singular contact structures, especially bᵐ-contact forms, with prescribed behavior along a hypersurface. Contact nondegeneracy is expressed in an adapted bundle. The authors establish local models, study the induced structure on the critical hypersurface, and relate these objects to smooth or folded structures by desingularization.

Read it alongside the b-Poisson paper to compare the even- and odd-dimensional stories. A vector field vanishing in ordinary coordinates can behave differently as a section of an adapted tangent bundle; interpreting that difference physically requires additional work.

## Questions that remain open here

- Can an explicit return map furnish a particle-tracking benchmark with known return times and locations?
- Which parts of a tape-bounded construction survive finite spatial resolution and perturbations?
- How does the exact viscous decay of a Beltrami eigenfield change its particle paths?
- Which physical end or boundary geometries actually justify the b-geometric model?

[The proposed experiments](questions-and-experiments.md) begin with a simple flat-torus Beltrami field. They are exploratory calculations, not implementations or validations of the universality constructions.
