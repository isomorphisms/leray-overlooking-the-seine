# Stochastic-Lagrangian bibliography continuation

Checked 2026-10-12. **10 new records (L154–L163), 5 updated records, 26 located citation links.** Continues the unfinished references in [the Arnold–Khesin note](arnold-khesin-spider-continuation.md). Inspection levels distinguish selected full-text reading from abstracts and metadata. No simulations or independent proof verification occurred.

## 1. A failed description is not necessarily a failed fluid

[Ohkitani–Constantin (L152)](https://doi.org/10.1063/1.1608009) studies a deterministic diffusive back-to-labels map that can lose invertibility and require resetting. [Cartes and collaborators (L156)](https://arxiv.org/html/0804.3602v1) connect changes in generalized Weber–Clebsch potentials and resetting with reconnection in selected Navier–Stokes and resistive-MHD computations. Neither turns every reset into a velocity-singularity certificate.

Keep three events distinct: loss of regularity of the fluid velocity; failure of an auxiliary coordinate description; and breakdown introduced by a finite approximation. [Iyer–Novikov (L160)](https://doi.org/10.1214/10-AOP586) gives a concrete example of the third: a finite-ensemble Burgers system can develop shocks for certain data. Its frequent-resetting theorem provides high-probability regularity on a prescribed finite interval under stated assumptions, not unconditional all-time regularity. The periodic resetting theorem and the unreset shock example on the line have different domain/data hypotheses.

## 2. Viscosity through noisy paths, without random physical forcing

[Constantin–Iyer (L157)](https://arxiv.org/html/math/0511067v4), Theorem 2.2, represents deterministic incompressible Navier–Stokes velocity using stochastic flow maps:

```text
dXₜ(a) = u(Xₜ(a),t) dt + √(2ν) dWₜ
Aₜ = Xₜ⁻¹
uₜ = 𝔼 ℙ[(∇Aₜ)ᵀ (u₀ ∘ Aₜ)]
```

Here ν is viscosity; W is Brownian motion, spatially uniform within each realization; A is the spatial inverse map; 𝔼 averages realizations; ℙ projects onto divergence-free fields. The unknown velocity u both drives X and results from the expectation. This is still a nonlinear fixed-point problem. The displayed unforced representation assumes periodicity or decay at infinity and the paper’s regularity hypotheses. Individual stochastic inverse maps are not the deterministic diffusive map in L154.

## 3. Finite-time convergence does not settle long-time dissipation

[Iyer–Mattingly (L159)](https://arxiv.org/html/0803.1222v3) averages N entire stochastic flows of diffeomorphisms, not merely N moving points. It proves two-dimensional convergence on fixed finite time intervals. However, for fixed N, Theorem 5.2 gives a positive long-time limsup lower bound on the expected squared velocity-gradient norm. Do not replace that statement with a universal exact kinetic-energy fraction, or silently promote the conditional three-dimensional discussion to a global theorem.

Research question: does increasing the ensemble size remove a persistent simulated structure, or only delay its appearance? This is a proposed diagnostic, not a computation performed here.

## 4. Walls and action principles

The [boundary extension (L158)](https://arxiv.org/html/1003.2461v4) exposes an implicit, nonlocal dependence of interior velocity on boundary vorticity. Simply stopping paths at a wall does not justify transplanting the boundary-free formula. This is relevant to comparing periodic mathematical examples with flow around solid objects; no engineering geometry has been validated here.

[Eyink (L161)](https://arxiv.org/html/0810.0817v1) relates stochastic action, particle-relabelling symmetry and a stochastic Kelvin law. His introduction explicitly identifies the variational calculation as formal and leaves functional-analytic details for further work. Preserve that qualification.

## 5. The five previous bibliography-only leads

L125 now has its own publisher abstract; L150 selected full-text inspection; L151 and L152 their own abstracts and bibliographies. L153 remains **metadata-only**: its publisher currently lists pages 169–177, whereas the previously inspected later bibliography gives 169–189. Without the original article’s pages, record the disagreement rather than declaring it settled.

The stability branch also needs precise scope. Ponce et al. studies perturbations of suitable existing global strong solutions. Chemin–Gallagher permits selected large data under a nonlinear smallness condition. Koch–Tataru supplies small-data BMO⁻¹ theory. None means global regularity for every large initial velocity.

## Source register

F = selected full-text sections, not an entire proof audit. A = own abstract, with metadata/references as specified. M = publisher metadata only. Ten records received F inspection, four A, one M.

| ID | Source and publication | Inspection and qualification |
|---|---|---|
| L125, updated | Zeitlin, [Finite-mode analogs of 2D ideal hydrodynamics](https://www.sciencedirect.com/science/article/pii/016727899190152Y), Physica D 49, 353–362 (1991) | A. O(N) integrals for O(N²) modes; canonical-variable and su(3) discussion. Article text identifies V. Zeitlin; automated page-author metadata incorrectly picked up a cited author. |
| L150, updated | Chemin–Gallagher, [Wellposedness and stability results for the Navier–Stokes equations in R³](https://www.numdam.org/articles/10.1016/j.anihpc.2007.05.008/), AIHP C 26(2), 599–624 (2009) | F. Abstract, introduction, selected statements and bibliography. Nonlinear smallness and structured stability, not arbitrary large data. [Full text](https://www.numdam.org/article/AIHPC_2009__26_2_599_0.pdf). |
| L151, updated | Ponce–Racke–Sideris–Titi, [Global stability of large solutions to the 3D Navier–Stokes equations](https://link.springer.com/article/10.1007/BF02102642), CMP 159, 329–341 (1994) | A. Publisher abstract and references. Stability around suitably decaying global strong solutions, including approximately symmetric data. |
| L152, updated | Ohkitani–Constantin, [Numerical study of the Eulerian–Lagrangian formulation of the Navier–Stokes equations](https://doi.org/10.1063/1.1608009), Physics of Fluids 15, 3251–3254 (2003) | A. Publisher abstract and references; later retrieval attempts were unreliable. Original full paper not read. Auxiliary-map invertibility and resetting. |
| L153, updated | Kida–Takaoka, [Vortex Reconnection](https://www.annualreviews.org/content/journals/10.1146/annurev.fl.26.010194.001125), Annual Review of Fluid Mechanics 26 (1994) | M. Publisher 169–177 versus later bibliography 169–189; printed pagination and scientific contents remain unchecked. |
| L154, new | Constantin, [An Eulerian–Lagrangian Approach to the Navier–Stokes Equations](https://doi.org/10.1007/s002200000349), CMP 216, 663–686 (2001) | F. [Author manuscript](https://web.math.princeton.edu/~const/xlnsF.pdf) introduction and references; publisher metadata. Deterministic diffusive labels and virtual velocity. Manuscript dated 2000. |
| L155, new | Constantin, [An Eulerian–Lagrangian approach for incompressible fluids: Local theory](https://arxiv.org/abs/math/0004059), JAMS 14(2), 263–278 (2001) | A. Own abstract; journal locator cross-checked in L158/L159 bibliographies. Local Euler theory, not viscous global regularity. Preprint 2000. |
| L156, new | Cartes–Bustamante–Pouquet–Brachet, [Generalized Eulerian-Lagrangian description of Navier-Stokes and resistive MHD dynamics](https://arxiv.org/abs/0804.3602), Fluid Dynamics Research 41, 011404 (2009), DOI 10.1088/0169-5983/41/1/011404 | F. Formulation, conclusions and references in [v1](https://arxiv.org/html/0804.3602v1). Reconnection/resetting correlations in particular flows; preprint 2008. No numerical reproduction. |
| L157, new | Constantin–Iyer, [A stochastic Lagrangian representation of the three-dimensional incompressible Navier–Stokes equations](https://arxiv.org/abs/math/0511067), CPAM 61(3), 330–345 (2008), DOI 10.1002/cpa.20192 | F. Introduction, Theorem 2.2, local-existence statement, comparison with diffusive labels, bibliography. First preprint 2005; inspected v4 dated 2006. |
| L158, new | Constantin–Iyer, [A stochastic-Lagrangian approach to the Navier–Stokes equations in domains with boundary](https://arxiv.org/abs/1003.2461), Annals of Applied Probability 21(4), 1466–1492 (2011), DOI 10.1214/10-AAP731 | F. Introduction, boundary formulation, selected vorticity/circulation discussion and bibliography in [v4](https://arxiv.org/html/1003.2461v4). Nonlocal wall-vorticity dependence. |
| L159, new | Iyer–Mattingly, [A stochastic-Lagrangian particle system for the Navier–Stokes equations](https://arxiv.org/abs/0803.1222), Nonlinearity 21(11), 2537–2553 (2008), DOI 10.1088/0951-7715/21/11/004 | F. Formulation, Theorems 3.5/4.1/5.2, Proposition 5.1 and bibliography in [v3](https://arxiv.org/html/0803.1222v3). Full flows, finite-ensemble long-time limitation. |
| L160, new | Iyer–Novikov, [The regularizing effects of resetting in a particle system for the Burgers equation](https://www.math.cmu.edu/~gautam/sj/research/papers/200811-resetting.pdf), Annals of Probability 39(4), 1468–1501 (2011), DOI 10.1214/10-AOP586 | F. Introduction, Theorem 2.3 including page-image check, shock example and references. Finite-horizon high-probability resetting result; not an unconditional all-time claim. |
| L161, new | Eyink, [Stochastic least-action principle for the incompressible Navier–Stokes equation](https://arxiv.org/abs/0810.0817), Physica D 239, 1236–1240 (2010) | F. Introduction, action and circulation formulations, explicit qualifications and bibliography in [v1](https://arxiv.org/html/0810.0817v1). Preprint 2008; journal locator checked in L158 [16]. |
| L162, new | Koch–Tataru, [Well-posedness for the Navier–Stokes equations](https://doi.org/10.1006/aima.2000.1937), Advances in Mathematics 157(1), 22–35 (2001) | F. [Author manuscript](https://math.berkeley.edu/~tataru/papers/nas.pdf) introduction and Theorems 2–3; publisher metadata. Small BMO⁻¹ global theory and localized criterion; hosted manuscript date differs from journal year. |
| L163, new | Chemin–Gallagher, [On the global wellposedness of the 3-D Navier–Stokes equations with large initial data](https://www.numdam.org/articles/10.1016/j.ansens.2006.07.002/), Annales scientifiques de l’ENS 39(4), 679–698 (2006) | F. [Published text](https://www.numdam.org/article/ASENS_2006_4_39_4_679_0.pdf) introduction/main statement and bibliography. Structured periodic data large in a critical Besov norm. |

## Located citation graph

Each row is an actual `cites` relation, directed citing → cited. Reference numbers belong to the explicitly identified version; not every preprint uses journal numbering.

| Citing | Cited | Location in source above |
|---|---|---|
| L152 | L154 | Publisher references [1] |
| L152 | L155 | Publisher references [2] |
| L154 | L155 | Author manuscript [4], PDF p.31 |
| L154 | L018 | Author manuscript [6], PDF p.31 |
| L156 | L155 | v1 references [1] |
| L156 | L154 | v1 references [2] |
| L156 | L152 | v1 references [3] |
| L157 | L155 | v4 references [9] |
| L157 | L154 | v4 references [10] |
| L157 | L015 | v4 references [1] |
| L158 | L157 | v4 references [11] |
| L158 | L155 | v4 references [7] |
| L158 | L018 | v4 references [10] |
| L158 | L161 | v4 references [16] |
| L159 | L157 | v3 references [6], earlier to-appear version |
| L159 | L155 | v3 references [7] |
| L159 | L018 | v3 references [5] |
| L160 | L157 | Published references [3], p.1500 / PDF p.33 |
| L160 | L159 | Published references [9], p.1500 / PDF p.33 |
| L161 | L157 | v1 references [1] |
| L150 | L163 | Published references [8] |
| L150 | L162 | Published references [18] |
| L150 | L020 | Published references [10] |
| L150 | L022 | Published references [17] |
| L163 | L162 | Published references [10], not author-preprint [8] |
| L151 | L018 | Publisher references [1] |

Inherited anchors, not independently re-audited: L015 = Beale–Kato–Majda (1984); L018 = Constantin–Foias (1988); L020 = Fujita–Kato (1964); L022 = Kato (1984).

## Located but not followed in this pass

Six bibliography-only leads, excluded from the new-record count: Cartes–Bustamante–Brachet (2007), L156 [4]; Chorin’s random-vortex computation (1973), L157 [6] and L159 [4]; Le Jan–Sznitman stochastic cascades (1997), L157 [20] and L158 [26]; Brenier’s generalized flows (1989), L161 [14]; Gomes’s variational Navier–Stokes formulation (2005), L161 [10]; and Eyink’s non-ideal hydromagnetic line-motion paper, L158 [17], arXiv:0812.0153.

## Validation and boundaries

Local catalogue checks: 15 distinct reviewed record IDs; new range L154–L163 has no collision with the inherited bundles; all 26 unique edge endpoints resolve against those records or four named anchors; every edge has a referring-source locator. These are catalogue consistency checks, not independent mathematical verification or live-link uptime guarantees.

The older note remains historical. Only the inspection statuses and qualifications stated here supersede L125 and L150–L153. No solver was installed or run, no proofs were independently verified, and no OpenAI manuscript claims were re-audited. Existing unrelated files and other pull requests are unchanged by this addition.

Remain draft for source review and normal FP/AICI acceptance. This pass supplies no FP/AICI acceptance receipts and does not authorize merging.
