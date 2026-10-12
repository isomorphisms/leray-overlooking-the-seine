# Leray bibliography continuation: cascades, generalized flows, and variational existence

Research date: 2026-10-12. Source IDs L164–L175 continue the earlier L001–L163 register. This pass follows all six leads named at the end of [the stochastic-Lagrangian continuation](stochastic-lagrangian-spider-continuation.md), then selected descendants. It is not an exhaustive recursive crawl.

**Scope:** 12 new source records; 7 inspected in selected full-text sections, 3 at their own publisher abstract, 1 through an institutional reproduction of the original abstract, and 1 retained at metadata/partial-abstract level. The accompanying [relationship register](../bibliography/cascades-generalized-flows-edges.json) distinguishes located citations from editorial comparisons. No simulations were run, proofs independently verified, or FP/AICI acceptance receipts produced. This remains source-review work on draft PR #4, not merge authorization.

## What this pass changes

### 1. Probability is doing several different jobs

The starting papers should not be merged into one generic stochastic solver:

| Construction | Random or optimized object | What the construction supplies |
|---|---|---|
| Chorin, L165 | Random displacement in a numerical vorticity method | A two-dimensional viscous-flow approximation |
| Le Jan–Sznitman, L166; Dascaliuc–Pham–Thomann, L170 | Branching trees in Fourier space, with vector-valued evaluations | A representation and estimates for a nonlinear integral equation |
| Brenier, L167; Benamou–Carlier–Nenna, L172 | Probability measures on complete particle paths | A relaxed, endpoint-constrained least-action problem |
| Eyink, L169/L174 | Noisy trajectory maps and transported surfaces | Stochastic magnetic-flux conservation and related hydromagnetic descriptions |
| Gomes, L168 | Stochastic-control variations | A critical-point characterization assuming smoothness |
| Ortiz–Schmidt–Stefanelli, L175 | Parameter-dependent functionals of whole velocity histories | A variational construction converging to a Leray–Hopf weak solution |

Each row has different data, constraints and approximation errors. Connecting the rows is an exploratory comparison, not a claim that their stochastic objects are interchangeable.

### 2. Generalized flows preserve more than two density pictures

In the formulation inspected in L172, let Q be a probability measure on continuous paths γ in a domain Ω over [0,T]. Let eₜ(γ)=γ(t), let m be normalized volume, and let π₀,T be the prescribed joint distribution of starting and finishing positions. The constraints are

    (eₜ)₊Q = m                       for every time t,
    (e₀,eT)₊Q = π₀,T.

Here ₊ denotes pushforward of a measure. The objective is the average kinetic action

    minimize  𝔼Q[½ ∫₀ᵀ |γ̇(t)|² dt].

This notation restates L172 equations (1.3)–(1.6). Incompressibility fixes every intermediate position marginal. The endpoint coupling records which starting locations connect to which finishing locations. Merely giving uniform density at both endpoints discards that association. This last observation is a deduction from the displayed constraints.

Time discretization turns the problem into multi-marginal optimal transport. Entropy regularization makes the optimization strictly convex and brings in Sinkhorn scaling. The paper also compares this construction with a Brownian-reference entropic interpolation problem on the torus. **That connection does not identify an arbitrary numerical entropy parameter with physical viscosity, or turn endpoint reconstruction into a Navier–Stokes initial-value solver.** See L172 §§1–5.

### 3. Two qualifications matter when reading the optimal-transport branch

**Uniqueness:** L171's preprint conclusion uses an unrestricted uniqueness phrase for generalized minimizers. Do not inherit it as a general theorem. L172 §2 explicitly states that the unregularized problems need not have unique solutions. Its entropy-regularized problem is different. Existence, uniqueness under additional hypotheses, and uniqueness after regularization require separate labels.

**Long reconstruction intervals:** L171 reports artificial statistical behavior when its two-end reconstruction interval exceeds the relevant turnover-time threshold. Its useful short-interval examples are numerical reconstruction results, not a general proof that long-time physical motion minimizes the endpoint action.

### 4. A genuine existence construction appears beyond smooth critical-point formulas

Following the Gomes bibliography forward reaches L175. For an unforced three-dimensional fluid in a bounded container, with homogeneous Dirichlet boundary conditions, Ortiz–Schmidt–Stefanelli minimize stabilized, exponentially time-weighted functionals. Theorem 3.2 assumes stabilization σ > 1/8 and obtains a subsequential limit satisfying Navier–Stokes and an energy inequality. The limit is a Leray–Hopf weak solution.

This is stronger than merely showing that already-smooth solutions are stationary points of an action. It does not establish uniqueness of the three-dimensional weak limit, smoothness for arbitrary time, or a performance result for a discretized optimizer. The paper itself leaves the unstabilized σ=0 convergence question open in the inspected version. See L175 §§1, 3 and Theorem 3.2; compare its discussion of L168/L173.

### 5. Explosion of a branching representation is not automatically explosion of velocity

L170 incorporates stochastic-tree explosion into a minimal-cascade construction and relates it to Picard iteration. Its finite-time blowup and nonuniqueness application concerns the **Montgomery–Smith toy equation**. Navier–Stokes retains a vector product encoding incompressibility and cancellations that the toy comparison does not preserve.

An implementation should therefore distinguish tree depth, probability of explosion, integrability of its vector-valued evaluation, and norms of the reconstructed velocity. Treating those as four different diagnostics is an editorial proposal grounded in L170 §§1–3, not a tested algorithm.

### 6. A numerical reset count is representation-dependent

L164 introduces a time-dimensioned parameter τ in generalized Weber–Clebsch equations. For its Taylor–Green calculation at Reynolds number 800, Table I reports **29 resets at τ=0 and 13 at τ=1** during the reported interval t=0 to t=12. These are numbers from the paper, not new computations. Figure 7, Table I, the conclusion and Appendix A were visually checked in the original PDF.

The physical equations being represented remain Navier–Stokes while the auxiliary description changes. A reset counter alone is consequently not an invariant measure of physical singularity or reconnection. The authors also report high-wavenumber errors; fewer resets are not, by themselves, an accuracy certificate.

### 7. A concrete link among curves, surfaces and fluid motion

L169 Proposition II.2 writes magnetic flux through a present surface as an expectation of initial fluxes through stochastic preimage surfaces. Its general-Prandtl formulation still requires the momentum equation separately. The stronger pair of stochastic conservation laws in Proposition II.1 assumes unit magnetic Prandtl number, ν=λ, as well as smoothness and the stated domain conditions.

For the project's original dimensional question, this is an explicit interaction of loop/flux formulas, transported surfaces, and three-dimensional velocity fields. Organizing such compatible observations by sheaves is a possible additional construction; neither L169 nor L174 proves that a sheaf solver results automatically. L174 follows the magnetic-flux question into rough-flow limits and dynamo numerics. Its turbulent-limit arguments must not be confused with its finite-resistivity identities.

## Source register

Inspection labels: **F** = selected full-text scientific sections inspected, not an independent proof check; **A** = own abstract and bibliographic record inspected; **A-mirror** = original abstract reproduced by an identified scholarly archive; **M** = metadata/partial abstract only.

### L164 — Generalized Eulerian-Lagrangian description of Navier-Stokes dynamics

Carlos Cartes, Miguel D. Bustamante and Marc E. Brachet. *Physics of Fluids* 19, 077101 (2007). DOI: `10.1063/1.2748447`.

[Author-hosted paper](https://www.phys.ens.psl.eu/~brachet/files/Publications_%26_Reprints_files/PhysFluids_19_077101.pdf)

**F:** abstract, introduction, conclusion, Appendix A, references; PDF pp. 6–7 visually inspected, including Figure 7 and Table I. Located through L156 reference [4]. Generalized potentials use a Moore–Penrose construction; τ→0 recovers the earlier formulation. References [2] and [3] return to L154 and L152. Preserve the distinction between the minimum-norm construction and the simplified practical equation discussed after (A10).

### L165 — Numerical study of slightly viscous flow

Alexandre Joel Chorin. *Journal of Fluid Mechanics* 57(4), 785–796 (1973). DOI: `10.1017/S0022112073002016`.

[Publisher record and abstract](https://www.cambridge.org/core/journals/journal-of-fluid-mechanics/article/numerical-study-of-slightly-viscous-flow/4E4FE6AE32F826FFFD6F46E3E86F330A)

**A:** own abstract and displayed bibliography. Located through L157 [6] and L159 [4]. Random numbers approximate vorticity generation and dispersal in a two-dimensional viscous-flow method, illustrated with a cylinder. **1973 is the journal year; 2006 is the publisher's online-publication date.** No convergence theorem was inferred from this abstract.

### L166 — Stochastic cascades and 3-dimensional Navier–Stokes equations

Yves Le Jan and Alain-Sol Sznitman. *Probability Theory and Related Fields* 109, 343–366 (1997). DOI: `10.1007/s004400050135`.

[Publisher record and summary](https://link.springer.com/article/10.1007/s004400050135)

**A:** original summary and metadata. Located through L157 [20] and L158 [26]. The nonlinear Fourier-space integral equation is represented through branching and composition along trees. The summary claims existence and uniqueness in specified new classes, not for arbitrary initial data. Full original proofs were not retrieved; L170 supplies an independently inspected later treatment.

### L167 — The least action principle and the related concept of generalized flows for incompressible perfect fluids

Yann Brenier. *Journal of the American Mathematical Society* 2(2), 225–255 (1989). DOI: `10.1090/S0894-0347-1989-0969419-8`.

[AMS-derived Géodesic record, abstract and bibliography](https://geodesic.mathdoc.fr/articles/10.1090/S0894-0347-1989-0969419-8/) · [DOI](https://doi.org/10.1090/S0894-0347-1989-0969419-8)

**A-mirror:** the institutional record explicitly identifies AMS as its source. The original PDF was not successfully retrieved. Located through L161 [14]. Probability measures on whole paths relax the classical least-action problem. Later mathematical formulations were checked directly in L172 rather than attributed to an unread original theorem.

### L168 — A Variational Formulation for the Navier-Stokes Equation

Diogo Aguiar Gomes. *Communications in Mathematical Physics* 257, 227–234 (2005). DOI: `10.1007/s00220-004-1263-8`.

[Publisher abstract and references](https://link.springer.com/article/10.1007/s00220-004-1263-8)

**A:** own abstract and 16 displayed references. Located through L161 [10]. Smooth solutions enter a stochastic-control critical-point formulation on the area-preserving group. References [6], [8], [9] lead respectively to L165, L155, L154. Stationarity is not synonymous with global minimality or an existence theorem; compare L175's explicit discussion.

### L169 — Stochastic Line-Motion and Stochastic Conservation Laws for Non-Ideal Hydromagnetic Models. I. Incompressible Fluids and Isotropic Transport Coefficients

Gregory L. Eyink. arXiv:0812.0153v1 (submitted 2008).

[Versioned full text](https://arxiv.org/html/0812.0153v1) · [Submission record](https://arxiv.org/abs/0812.0153)

**F:** introduction, Propositions II.1–II.2, discussion and bibliography. Located through L158 [17]. The unit/general magnetic-Prandtl distinction and finite smoothness interval are retained above. References [9] and [14] return to L157 and L161. The listed Part II was only 'in preparation' in this version; this pass does not assert its later publication.

### L170 — On Le Jan-Sznitman's stochastic approach to the Navier-Stokes equations

Radu Dascaliuc, Tuan N. Pham and Enrique Thomann. Inspected version: arXiv:1910.05500v7 (2021; first submitted 2019). Published: *Transactions of the American Mathematical Society* 377(4), 2335–2365 (2024), DOI `10.1090/tran/8974`.

[Inspected preprint](https://arxiv.org/html/1910.05500v7) · [Publisher paper record](https://www.ams.org/journals/tran/2024-377-04/S0002-9947-2024-08974-2/)

**F:** introduction, cascade definitions, minimal-solution discussion and bibliography; no full proof audit. **Reference numbers in this continuation belong to v7, not the published edition.** Its [19] is L166; [16] is L022. Its [8]–[9] lead to the two Yule-cascade papers, retained below as the next frontier.

### L171 — Turbulence of generalised flows in two dimensions

Simon Thalabard and Jérémie Bec. *Journal of Fluid Mechanics* 883, A49 (2020). DOI: `10.1017/jfm.2019.892`. Inspected manuscript: arXiv:1812.02167v2 (2019).

[Full text](https://arxiv.org/html/1812.02167v2) · [Publisher](https://www.cambridge.org/core/journals/journal-of-fluid-mechanics/article/turbulence-of-generalised-flows-in-two-dimensions/4524DDA60B8FF4C1397B445F14BB822A)

**F:** formulation, introductory interpretation, concluding discussion and named bibliography entries. Published metadata checked separately. The long-interval and uniqueness qualifications appear above. Citations to Brenier (1989) and Benamou–Carlier–Nenna (2017) locate L167 and L172. No figures from this paper were independently analyzed here.

### L172 — Generalized incompressible flows, multi-marginal transport and Sinkhorn algorithm

Jean-David Benamou, Guillaume Carlier and Luca Nenna. Inspected version: arXiv:1710.08234v2 (2018; first submitted 2017).

[Full text](https://arxiv.org/html/1710.08234v2) · [Submission record](https://arxiv.org/abs/1710.08234)

**F:** §§1–5 formulations, entropy constraints, algorithm description, and references. The unregularized and regularized uniqueness statements are explicitly separated. Reference [6] is L167; [1] is the Bredinger/entropic-interpolation lead. Journal metadata is not assigned from an unverified match. Numerical figure panels were not audited.

### L173 — On a variational principle for the Navier-Stokes equation

Diogo Aguiar Gomes. In *Mathematical Analysis of Random Phenomena*, World Scientific (2007), pp. 93–100. DOI: `10.1142/9789812770547_0008`.

[Publisher chapter](https://www.worldscientific.com/doi/abs/10.1142/9789812770547_0008)

**M:** publisher-indexed metadata and partial abstract only; full chapter access failed. L175 reference [25] confirms the bibliographic entry and explicitly discusses it alongside L168. The publisher snippet mentions clarifying boundary conditions, but the exact conditions have not been inspected. No theorem-level claim is made from that snippet.

### L174 — Stochastic flux freezing and magnetic dynamo

Gregory L. Eyink. *Physical Review E* 83, 056405 (2011). DOI: `10.1103/PhysRevE.83.056405`. Inspected preprint: arXiv:1008.4959v1 (2010).

[Preprint](https://arxiv.org/html/1008.4959v1) · [Publisher](https://link.aps.org/doi/10.1103/PhysRevE.83.056405)

**F:** abstract, introductory discussion, path-integral/flux-freezing discussion, selected concluding material and references. Publisher metadata separately checked. A 2026 date printed by the regenerated HTML is not its publication date. Its connection to L169 is stored as a thematic continuation, not as a numbered citation verified in this pass.

### L175 — A variational approach to Navier-Stokes

Michael Ortiz, Bernd Schmidt and Ulisse Stefanelli. Inspected version: arXiv:1802.06606v2 (2018).

[Full text](https://arxiv.org/html/1802.06606v2) · [Submission record](https://arxiv.org/abs/1802.06606)

**F:** introduction, admissible-space definitions, Theorem 3.2 and bibliography. The key assumptions and weak-limit conclusion are stated above. References [24]–[25] locate L168/L173; [22] leads to Gigli–Mosconi's variational time-discretization method. No numerical implementation was executed.

## Six-lead coverage and remaining frontier

All six previously named leads now have records: Cartes 2007 → L164; Chorin 1973 → L165; Le Jan–Sznitman 1997 → L166; Brenier 1989 → L167; Gomes 2005 → L168; Eyink 0812.0153 → L169. Following a lead does not imply full-text access: the inspection labels above are part of the result.

The next selected bibliography targets are not counted as newly inspected papers:

1. Goodman, *Convergence of the random vortex method* (1987), DOI `10.1002/cpa.3160400204`, and Long, *Convergence of the random vortex method in two dimensions* (1988), DOI `10.1090/S0894-0347-1988-0958446-1`: L157 references [12], [21]. Publisher metadata found; convergence assumptions still need direct inspection.
2. Dascaliuc–Pham–Thomann–Waymire, *Doubly Stochastic Yule Cascades*, Parts I and II: arXiv:2103.06912 and 2107.13182, L170 v7 [8], [9]. Also Bhattacharya and collaborators, *Majorizing kernels and stochastic cascades* (2003), L170 [2].
3. Arnaudon–Cruzeiro–Léonard–Zambrini, *An entropic interpolation problem for incompressible viscid fluids*, arXiv:1704.02126: L172 [1]. Determine exactly which velocity and pressure equations the entropy minimizer satisfies before identifying it with viscous flow.
4. Gigli–Mosconi, *A variational approach to the Navier–Stokes equations* (2012): L175 [22]. Compare its time-stepping construction with whole-history WIDE minimization.
5. Recover the full original L167 and full chapter L173 before upgrading their inspection labels. Trace the magnetic branch's cited stochastic-flow and dynamo models separately from ordinary hydrodynamic vortex reconnection.

## Integrity notes

No claim in the inherited OpenAI-manuscript branch was re-audited here. Existing parallel Lockerby, CFD-solver, contact-topology and sheaf-implementation files were not changed. Inherited anchors used by the graph are L022 (Kato 1984), L152 (Ohkitani–Constantin 2003), L154/L155 (Constantin 2001), L156 (Cartes et al. 2009), L157/L158 (Constantin–Iyer), L159 (Iyer–Mattingly), and L161 (Eyink least action). Graph arrows mean **citing source → cited source** unless the relation is explicitly editorial.
