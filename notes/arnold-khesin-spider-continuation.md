# Arnold–Khesin spider continuation

Checked 2026-10-12. Continuation of the screenshot-led Leray bibliography, with **30 additional records (L124–L153)** and **49 relationships**, including 41 explicitly located citation edges. The inspection levels below distinguish reading selected full-text sections from checking an abstract or transcribing a bibliography. No fluid simulations, software installations, benchmarks or independent proof verification were performed.

## Starting source

Boris Khesin's **Recent Developments in Topological Hydrodynamics**, in the expanded 2021 edition of *Topological Methods in Hydrodynamics*, has **265 numbered bibliography entries**. Some entries combine several works; 265 is not a count of individually verified papers.

[Publisher back matter, including the complete supplementary survey and bibliography](https://link.springer.com/content/pdf/bbm%3A978-3-030-74278-2/1). The survey starts on printed page 393, PDF page 28. Its numbered bibliography occupies printed pages 435–448, PDF pages 69–82. The earlier alphabetic bibliography in the same PDF is a separate list.

This pass follows selected branches. It does not claim to have recursively inspected all 265 entries. It leaves the earlier OpenAI manuscript crawl and its proof assessment unchanged.

## 1. Geometry that changes the solver

**Khesin reference 189 → Modin–Viviani (L124) → Zeitlin, McLachlan and isospectral integrators (L125–L128).** Instead of merely interpreting an ordinary solver geometrically, these methods discretize the underlying algebra.

```text
vorticity function on S²       → skew-Hermitian matrix W
Poisson bracket of functions  → scaled matrix commutator
integrated vorticity powers   → discrete trace invariants
inviscid transport            → isospectral matrix evolution
```

The finite-dimensional method preserves its discrete Casimirs; this is not exact preservation of every continuum observable at finite resolution. The isospectral time integrator generally nearly conserves energy, rather than conserving it exactly. Viscosity and forcing require their own balance laws.

Sources: [spherical method](https://arxiv.org/html/1812.11055v4), [isospectral methods](https://doi.org/10.1007/s10208-019-09428-w), [forced turbulence](https://arxiv.org/abs/2204.11794).

The later [matrix-hydrodynamics introduction](https://arxiv.org/html/2508.07088v2) contains a worked **quflow** example and discusses finite-resolution noise. The [software README](https://github.com/klasmodin/quflow) was inspected, not the execution of the software. Its implementation is Python; this crawl does not propose translating it.

A different route, **Khesin reference 207 → Pavlov et al. (L134) → Bauer–Gay-Balmaz (L135)**, derives discrete equations variationally and preserves a discrete Kelvin circulation theorem. The atmospheric extension concerns anelastic and pseudo-incompressible models, not arbitrary compressible Navier–Stokes flow.

### Carry the correction with the original

The isospectral-method paper has a [correction](https://doi.org/10.1007/s10208-024-09661-y), online in July 2024 and in a 2025 journal volume. A proof had implicitly assumed that time-dependent matrices commute. The authors reformulate Proposition 1 and supply a corrected proof. It is not enough to cite the old theorem without this qualification.

## 2. Topology change is not the same as blowup

**Khesin reference 65 → Enciso–Lucà–Peralta-Salas (L139)** constructs smooth Navier–Stokes flows on the three-torus whose vortex topology changes. Viscosity permits reconnection without loss of velocity regularity. The paper separates structurally stable reconnection from instantaneous but non-robust destruction. [Full text and bibliography](https://arxiv.org/html/1606.06176v2).

**Ciampa–Lucà (L140)** moves to R³ using localized Beltrami fields and the number of hyperbolic critical points, rather than torus homotopy. The global-smoothness construction concerns specially structured large data, not arbitrary large data. [Full text](https://arxiv.org/html/2311.01369v3).

The latter paper explicitly cites Leray, Fujita–Kato, Kato, Chemin–Gallagher, Albritton–Brué–Colombo and Buckmaster–Vicol. This connects the topology branch back to the weak-solution/stability branch through actual bibliography entries.

## 3. An experimental disagreement worth retaining

[Kleckner–Irvine](https://doi.org/10.1038/nphys2560) create vortex knots and links with shaped hydrofoils. [Scheeler and collaborators](https://arxiv.org/abs/1404.6513) report transfer of geometric helicity across length scales during reconnection. [Kerr](https://arxiv.org/abs/1509.03142) compares trefoil simulations with those experiments and reports helicity depletion, discussing reconnection timing and the meaning of the measured quantity.

Do not turn this into a universal claim that viscous reconnection always conserves or always destroys helicity. A useful comparison would distinguish geometric proxies from the volume integral, vortex-core definitions, viscosity and the interval called reconnection.

[Yao–Hussain](https://doi.org/10.1017/jfm.2020.58) use DNS to test a reduced vortex-ring model and find core deformation inconsistent with simplifying assumptions. That tests a model; it does not prove general global regularity. Their [2022 review](https://doi.org/10.1146/annurev-fluid-030121-125143) has 117 literature entries, a further frontier rather than 117 papers read here.

## 4. The local-to-global question has concrete neighboring methods

[Finite element exterior calculus](https://doi.org/10.1017/S0962492906210018) uses differential forms, complexes and commuting projections to design compatible numerical spaces. Its Arnold is **Douglas N. Arnold**, not Vladimir I. Arnold. FEEC is not itself a sheaf-based Navier–Stokes solver.

[Gawlik–Gay-Balmaz's Euler method](https://arxiv.org/abs/1910.05707) and [their ideal-MHD method](https://arxiv.org/abs/2012.04122) provide nearby finite-element examples with explicit conservation and divergence constraints. These are related-method links, not claimed citations from Khesin's survey.

**Exploratory question, not a result of these papers:** could local solution/measurement spaces and restriction maps organize interfaces, a compatible complex control divergence, and a separately specified time integrator control conservation or dissipation? Such a prototype must demonstrate those properties rather than merely rename mesh data as a sheaf.

## 5. Contact geometry and groupoids

**Khesin reference 44 → Cardona–Miranda–Peralta-Salas–Presas (L147)** develops Reeb/Beltrami universality on suitable Riemannian manifolds, potentially in higher dimension. It does not automatically imply the same realization in an ordinary Euclidean tank. [Paper](https://arxiv.org/abs/1911.01963).

[Izosimov–Khesin (L148)](https://arxiv.org/abs/2206.01434) treats generalized flows, multiphase fluids and vortex sheets through groupoids and a Poisson structure on a dual Lie algebroid. This is a geometric interface framework, not an engineering closure model.

## Source register

Inspection: **F** = selected full-text sections; **A** = own abstract/publisher metadata; **R** = software README; **B** = citing bibliography only; **AB** = own abstract plus bibliography. None means an entire proof was verified.

| ID | Source | Year/version | Inspection and route |
|---|---|---|---|
| L124 | Modin–Viviani, [A Casimir preserving scheme for long-time simulation of spherical ideal hydrodynamics](https://arxiv.org/abs/1812.11055) | JFM 884 A22, 2020 | F; Khesin [189] |
| L125 | Zeitlin, Finite-mode analogs of 2D ideal hydrodynamics: coadjoint orbits and local canonical structure | Physica D 49, 353–362, 1991 | B; L124 bibliography, Zeitlin (1991) |
| L126 | Zeitlin, [Self-Consistent Finite-Mode Approximations for the Hydrodynamics of an Incompressible Fluid on Nonrotating and Rotating Spheres](https://doi.org/10.1103/PhysRevLett.93.264501) | PRL 93, 264501, 2004 | A; L124 bibliography |
| L127 | McLachlan, [Explicit Lie-Poisson integration and the Euler equations](https://doi.org/10.1103/PhysRevLett.71.3043) | PRL 71, 3043–3046, 1993 | A; L124 bibliography |
| L128 | Modin–Viviani, [Lie–Poisson Methods for Isospectral Flows](https://doi.org/10.1007/s10208-019-09428-w) | FoCM 20, 889–921, 2020; online 2019 | F; L124 bibliography |
| L129 | Modin–Viviani, [Correction to L128](https://doi.org/10.1007/s10208-024-09661-y) | FoCM 25, 1085–1086, 2025; online 2024 | F; publisher correction link |
| L130 | Qi–Marston, [Hyperviscosity and statistical equilibria of Euler turbulence on the torus and the sphere](https://arxiv.org/abs/1312.2553) | JSTAT P07020, 2014 | A; L124 bibliography |
| L131 | Cifani et al., [Casimir preserving spectrum of two-dimensional turbulence](https://arxiv.org/abs/2204.11794) | PR Fluids 7 L082601, 2022 | A; L132 [11] |
| L132 | Modin–Viviani, [A brief introduction to matrix hydrodynamics](https://arxiv.org/abs/2508.07088) | arXiv v2, December 2025; linked JCD DOI 2026 | F; forward matrix-hydrodynamics trail |
| L133 | [quflow](https://github.com/klasmodin/quflow) | README checked 2026-10-12 | R; L132 section 4 |
| L134 | Pavlov et al., [Structure-Preserving Discretization of Incompressible Fluids](https://arxiv.org/abs/0912.3989) | Physica D 240, 443–458, 2011 | A; Khesin [207] |
| L135 | Bauer–Gay-Balmaz, [Variational integrators for anelastic and pseudo-incompressible flows](https://arxiv.org/abs/1701.06448) | 2019; DOI 10.3934/jgm.2019025 | F; explicitly cites L134 as [14] |
| L136 | D. Arnold–Falk–Winther, [Finite element exterior calculus, homological techniques, and applications](https://doi.org/10.1017/S0962492906210018) | Acta Numerica 15, 1–155, 2006 | A; related-method search |
| L137 | Gawlik–Gay-Balmaz, [A Conservative Finite Element Method for the Incompressible Euler Equations with Variable Density](https://arxiv.org/abs/1910.05707) | JCP article 109439, 2020 | A; related-method search |
| L138 | Gawlik–Gay-Balmaz, [A Finite Element Method for MHD that Preserves Energy, Cross-Helicity, Magnetic Helicity, Incompressibility, and div B = 0](https://arxiv.org/abs/2012.04122) | 2020 preprint | A; related-method continuation |
| L139 | Enciso–Lucà–Peralta-Salas, [Vortex reconnection in the three dimensional Navier–Stokes equations](https://arxiv.org/abs/1606.06176) | Adv. Math. 309, 452–486, 2017 | F; Khesin [65] |
| L140 | Ciampa–Lucà, [Localization of Beltrami fields: global smooth solutions and vortex reconnection for the Navier-Stokes equations](https://arxiv.org/abs/2311.01369) | JFA 287, 110610, 2024 | F; explicitly cites L139 as [13] |
| L141 | Caro–Ciampa–Lucà, [Magnetic Reconnection in Magnetohydrodynamics](https://arxiv.org/abs/2209.09600) | RMI 41(2), 461–508, 2025; preprint 2022 | A; L140 [7] |
| L142 | Kleckner–Irvine, [Creation and dynamics of knotted vortices](https://doi.org/10.1038/nphys2560) | Nature Physics 9, 253–258, 2013 | A; Khesin [148], L139 [14] |
| L143 | Scheeler et al., [Helicity conservation by flow across scales in reconnecting vortex links and knots](https://arxiv.org/abs/1404.6513) | PNAS 111, 15350–15355, 2014 | A; L139 [10] |
| L144 | Kerr, [Simulated Navier-Stokes trefoil reconnection](https://arxiv.org/abs/1509.03142) | 2015 preprint | A; L139 [11] |
| L145 | Yao–Hussain, [On singularity formation via viscous vortex reconnection](https://doi.org/10.1017/jfm.2020.58) | JFM 888 R2, 2020 | A; related reconnection branch |
| L146 | Yao–Hussain, [Vortex Reconnection and Turbulence Cascade](https://doi.org/10.1146/annurev-fluid-030121-125143) | Annual Review of Fluid Mechanics 54, 2022 | AB; forward review |
| L147 | Cardona et al., [Universality of Euler flows and flexibility of Reeb embeddings](https://arxiv.org/abs/1911.01963) | Adv. Math. 428, 109142, 2023 | A; Khesin [44], then a 2019 preprint |
| L148 | Izosimov–Khesin, [Geometry of generalized fluid flows](https://arxiv.org/abs/2206.01434) | 2023 version; DOI 10.1007/s00526-023-02612-5 | A; author bibliography and vortex-sheet continuation |
| L149 | Enciso–Peralta-Salas, [Knots and links in steady solutions of the Euler equation](https://annals.math.princeton.edu/2012/175-1/p09) | Annals 175, 345–367, 2012 | A; L139 [4], L140 [15] |
| L150 | Chemin–Gallagher, Wellposedness and stability results for the Navier-Stokes equations in R³ | AIHP AN 26, 599–624, 2009 | B; L140 [10] |
| L151 | Ponce–Racke–Sideris–Titi, Global stability of large solutions to the 3D Navier-Stokes equations | CMP 159, 329–341, 1994 | B; L139 [17] |
| L152 | Ohkitani–Constantin, Numerical study of the Eulerian–Lagrangian formulation of the Navier–Stokes equations | Physics of Fluids 15, 3251–3254, 2003 | B; L139 [16] |
| L153 | Kida–Takaoka, Vortex reconnection | Annual Review of Fluid Mechanics 26, 1994 | B; L139 [13]; page-range discrepancy remains unresolved |

## Graph and audit

The [relationship graph](../bibliography/arnold-khesin-edges.csv) uses `cites`, `corrects`, `implements`, `documents_software`, `compares_with`, `related_method` and `author_followup` separately. Only `cites` asserts an inspected bibliography edge. Existing IDs are defined in the accompanying anchor register below.

Two corrections found while following references: Zeitlin's 2004 article number is **264501**, not the page range 353–362 reproduced in L124's bibliography. L128's final title and journal year differ from its earlier bibliography entry. The 2024/2025 correction is a separate linked record. L153 has conflicting page ranges in later bibliographies and remains a lead until the original metadata is checked.

The five bibliography-only records are L125 and L150–L153. The other 25 were checked at their own abstract, publisher, selected full-text sections or software README. No claim of full-text reading for all 25.

### Inherited graph anchors

| ID | Work |
|---|---|
| L001 | Leray (1934), Sur le mouvement d'un liquide visqueux emplissant l'espace |
| L020 | Fujita–Kato (1964), On the Navier–Stokes initial value problem I |
| L022 | Kato (1984), Strong Lp-solutions of Navier–Stokes equations in Rm |
| L032 | Majda–Bertozzi, Vorticity and Incompressible Flow |
| L041 | Albritton–Brué–Colombo (2022), Nonuniqueness of Leray solutions of forced Navier–Stokes |
| L044 | Buckmaster–Vicol (2019), Nonuniqueness of weak solutions to Navier–Stokes |
| L090 | Arnold–Khesin expanded edition (2021), including Khesin's supplementary survey |
| L091 | Etnyre–Ghrist I, Beltrami fields and the Seifert conjecture |
| L094 | Enciso–Peralta-Salas (2015), Existence of knotted vortex tubes in steady Euler flows |
| L096 | Enciso–Peralta-Salas–Torres de Lizaur (2017), Knotted structures in high-energy Beltrami fields on the torus and sphere |
| L097 | Khesin–Kuksin–Peralta-Salas (2014), KAM theory and the 3D Euler equation |
| L099 | Izosimov–Khesin, Vortex sheets and diffeomorphism groupoids |

These anchor labels connect to the previous 123-record crawl; their earlier annotations were not re-audited here. This documentation remains draft pending review; no merge or FP/AICI acceptance is asserted.
