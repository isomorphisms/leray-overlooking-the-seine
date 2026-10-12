# Duncan Lockerby — citation spider (2001–2025)

**Seed:** [EPSRC, “Wings That Waggle Could Cut Aircraft Emissions By 20%” (22 May 2009)](https://www.sciencedaily.com/releases/2009/05/090521084721.htm).  
**Primary author index:** [University of Warwick/WRAP: Duncan A. Lockerby (93 records, including duplicates and data)](https://wrap.warwick.ac.uk/view/author_id/9408.type.html).  
**Research profile:** [University of Warwick](https://warwick.ac.uk/fac/sci/eng/people/duncan_lockerby/).  
**Traversal date:** 2026-10-12. This is an *annotated, scoped spider*, not a claim to have exhaustively fetched or read every paper or every citation. See the [complete 20-item backward bibliography of the 2012 paper](duncan-lockerby-2012-backreferences.md) and [references.bib](../references.bib).

## 0. Resolve the original social-media lead

The 2009 **EPSRC press announcement** attributes an initially surprising wind-tunnel observation to Duncan Lockerby: transverse “waggling” of a wing section appeared to reduce **friction drag**; researchers did not yet know precisely why. The concept proposed forcing spanwise motion with tiny oscillating air jets using Helmholtz resonant cavities. It was at **concept stage**.

- “Up to 40%” refers to **proposed skin-friction drag reduction** and “20%” to **projected fuel/emissions benefits**; they are *not measured lift* and not established in-flight fuel savings.
- The same announcement mentions passive *shark-like riblets* (roughly 5% drag improvement) **as a comparison**. Riblets are **not** the proposed resonant microjet mechanism.
- The [2018 Domel et al. denticle airfoil paper](https://doi.org/10.1098/rsif.2017.0828) is a **different experiment**, with an up-to-323% improvement reported in lift/drag *ratio* in selected water-tunnel configurations.
- We have identified the original **article**, but not the exact social-media permalink that surfaced it.

**Evidence hierarchy:** 2009 press claims ≠ calibrated flight measurements; a linearized stability correlation ≠ full nonlinear explanation; drag ≠ lift; a citation relationship ≠ independent experimental replication.

## 1. Branch A: MEMS actuators → turbulent boundary-layer control

A chronological, **thematic** path follows. Arrows here mean “next relevant work in this research programme,” **not** that every item directly cites its predecessor.

1. **Lockerby (2001)**, [*Numerical simulation of boundary-layer control using MEMS actuation*](https://wrap.warwick.ac.uk/id/eprint/3076/), Warwick PhD thesis. Jet and synthetic-jet actuators, from piezoelectric input to exit velocity; three-dimensional boundary-layer disturbances solved using a velocity–vorticity form of Navier–Stokes. [Archive record; 15 MB thesis PDF accessible there.]
2. **Lockerby, Carpenter & Davies (2002)**, [*Numerical Simulation of the Interaction of Microactuators and Boundary Layers*](https://doi.org/10.2514/2.1615), *AIAA Journal* 40(1):67–73. Numerical actuator/laminar-layer interaction.
3. **Lockerby & Carpenter (2004)**, [*Modeling and Design of Microjet Actuators*](https://doi.org/10.2514/1.9091), *AIAA Journal* 42(2):220–227. Coupled diaphragm, cavity-pressure and orifice model; synthetic jets and pulse jets; actuator design.
4. **Lockerby, Carpenter & Davies (2005)**, [*Control of Sub-layer Streaks Using Microjet Actuators*](https://doi.org/10.2514/1.14443), *AIAA Journal* 43(9):1878–1886. Near-wall streak *model* perturbed with microjets, drawing on optimal-response/Klebanoff-mode ideas. It is not a measured full aircraft fuel saving. [Cardiff abstract](https://orca.cardiff.ac.uk/id/eprint/25028/).
5. **Lockerby, Carpenter & Davies (2007)**, [*Is Helmholtz Resonance a Problem for Micro-jet Actuators?*](https://doi.org/10.1007/s10494-006-9056-0), *Flow, Turbulence and Combustion* 78:205–222. Important counterpoint: resonance can make even nominally inactive actuators amplify incoming boundary-layer disturbances. Passive resonance is not automatically beneficial. [Cardiff abstract](https://orca.cardiff.ac.uk/id/eprint/25020/). A distinct 2008 IUTAM proceedings version also exists ([DOI](https://doi.org/10.1007/978-1-4020-6858-4_10)); do not count it as an independent experiment.
6. **EPSRC + Airbus (2009)**, [original public announcement](https://www.sciencedaily.com/releases/2009/05/090521084721.htm). Proposed resonant spanwise microjet strategy; qualitative wind-tunnel observation; ambitious, unverified savings projections. The university's [project list](https://warwick.ac.uk/fac/sci/eng/people/duncan_lockerby/) identifies SWIFT, passive drag-reduction work and the **July 2009–June 2012** EPSRC/EADS/Airbus wall-forcing project **EP/G060215/1**.
7. **Duque-Daza, Baig, Lockerby, Chernyshenko & Davies (2011 conference; 2012 journal)**, [*Modelling turbulent skin-friction control using linearized Navier–Stokes equations*](https://doi.org/10.1017/jfm.2012.189), *Journal of Fluid Mechanics* 702:403–414 ([author-hosted PDF](https://orca.cardiff.ac.uk/id/eprint/25034/1/Duque-Daza%202012.pdf)). Linearized streak amplification under streamwise-travelling waves of spanwise wall velocity correlates with published DNS drag-reduction predictions; the generalized Stokes layer provides a simple correlated characteristic. This assesses a related **wall-forcing mechanism**, **not direct simulation/validation of the proposed Helmholtz microjet wing**. [2011 conference version DOI](https://doi.org/10.1088/1742-6596/318/4/042026).
8. **Pearce, Denissenko & Lockerby (2013)**, [*An experimental study into the effects of streamwise and spanwise acceleration in a turbulent boundary layer*](https://doi.org/10.1007/s00348-012-1414-1), *Experiments in Fluids* 54:1414. Water-channel boundary-layer measurements under streamwise and spanwise pressure gradients. **Related experiments, different actuation and geometry**: not proof of aircraft microjet feasibility.

**Falsifiable questions:** Does the forcing reduce wall shear in a given Reynolds-number and actuation regime? Does reduced wall shear persist after actuation power, mass, drag elsewhere and passive-actuator instability are included? Does the wall-normal/spanwise structure seen in DNS match the linearized streak-amplification prediction? At high Reynolds numbers, does the optimal forcing shift?

## 2. Spider backward from the 2012 linearized Navier–Stokes paper

The [2012 JFM reference list](https://www.cambridge.org/core/journals/journal-of-fluid-mechanics/article/abs/modelling-turbulent-skinfriction-control-using-linearized-navierstokes-equations/D0F50AD15111C37D0A976FE9610508E8) supplies **20 explicitly cited antecedents**, transcribed in [the companion bibliography](duncan-lockerby-2012-backreferences.md). Particularly productive branches:

- **How streaks form:** [Butler & Farrell (1992–93)](duncan-lockerby-2012-backreferences.md); [Chernyshenko & Baig (2005)](https://doi.org/10.1017/S0022112005006506) describe growth/spacing and a mean-shear/lift-up-based alternative to vortex-imposed pattern explanations. [Kline et al. (1967)](duncan-lockerby-2012-backreferences.md) establish the observed near-wall turbulent structures.
- **Why forcing matters:** [Jung, Mangiavacchi & Akhavan (1992)](duncan-lockerby-2012-backreferences.md), [Quadrio, Ricco & Viotti (2009)](https://doi.org/10.1017/S0022112009006077), and [Auteri et al. (2010)](https://doi.org/10.1063/1.3491203) explore simulated and experimental spanwise forcing. Unlike a fixed drag-reduction claim, travelling-wave effects depend on forcing speed and direction; some parameters **increase** drag.
- **Reduced mechanism:** [Quadrio & Ricco (2011)](https://doi.org/10.1017/S0022112010004398) derive the generalized Stokes layer (using the Airy function). The 2012 paper relates its characteristics to drag reduction predicted by DNS.
- **Discretization/formulation:** [Davies & Carpenter (2001)](duncan-lockerby-2012-backreferences.md) give a velocity–vorticity formulation; [Lockerby's 2001 thesis](https://wrap.warwick.ac.uk/id/eprint/3076/) gives actuator coupling and numerical validation. For implementation, distinguish velocity/vorticity evolution, prescribed spanwise wall-speed boundary conditions, and orifice/cavity coupling.

**Citation statement:** The 2012 JFM paper *cites* these 20 works; the graph does not claim that each paper independently replicates an aircraft-scale effect.

## 3. Traverse forward (selected, verified)

- **Blesbois, Chernyshenko, Touber & Leschziner (2013)**, [*Pattern prediction by linear analysis of turbulent flow with drag reduction by wall oscillation*](https://doi.org/10.1017/jfm.2013.165), *JFM* 724:607–641. **Direct backward reference verified:** its printed bibliography explicitly cites Duque-Daza et al. (2012). It compares optimal perturbation/streak shape with DNS.
- **Gatti & Quadrio (2013)**, [*Performance losses of drag-reducing spanwise forcing at moderate values of the Reynolds number*](https://doi.org/10.1063/1.4849537), *Physics of Fluids* 25:125109. Listed among 2012 paper's citing works by the Cambridge publisher's index; DNS to friction Reynolds number Reτ = 2100 studies shifting optimum and Reynolds-number dependence. **Publisher-index citation; source bibliography not individually inspected.**
- **Ricco, Skote & Leschziner (2021)**, [*A review of turbulent skin-friction drag reduction by near-wall transverse forcing*](https://doi.org/10.1016/j.paerosci.2021.100713), *Progress in Aerospace Sciences* 123:100713 ([preprint](https://arxiv.org/abs/2103.04719)). **Topical synthesis**, not asserted to be a direct citation of Lockerby. Surveys wall oscillations, moving discs, plasma forcing, energy accounting, Reynolds-number scaling and practical barriers.

The 2012 paper's publisher landing page exposes an incomplete/variable “cited by” pane. This spider **does not** claim to enumerate every forward citation. Continue forward citation verification from Crossref/OpenAlex or individual reference lists if needed.

## 4. Branch B: rarefied gases → continuum/particle hybrid CFD

This is a **distinct physical regime** (mean free path, Knudsen effects, kinetic non-equilibrium), not an explanation of high-Reynolds-number turbulent aircraft drag.

1. **Lockerby & Reese (2003)**, [*High-resolution Burnett simulations of micro Couette flow and heat transfer*](https://doi.org/10.1016/S0021-9991(03)00162-1), *J. Computational Physics* 188:333–347. Higher-order continuum constitutive equations and their numerical limitations.
2. **Lockerby & Reese (2008)**, [*On the modelling of isothermal gas flows at the microscale*](https://doi.org/10.1017/S0022112008001158), *JFM* 604:235–261 ([Warwick](https://wrap.warwick.ac.uk/id/eprint/863/)). Benchmarks, including standing shear waves, for extended hydrodynamics and R13.
3. **Lockerby, Reese & Struchtrup (2009)**, [*Switching criteria for hybrid rarefied gas flow solvers*](https://doi.org/10.1098/rspa.2008.0497), *Proc. R. Soc. A* 465:1581–1598 ([author manuscript](https://strathprints.strath.ac.uk/7833/)). A kinetic/continuum boundary is chosen using mismatch of stress and heat flux, with R13 as a higher-order predictor; an illustrative hybrid method is compared with a kinetic reference solution.
4. **Lockerby, Duque-Daza, Borg & Reese (2013)**, [*Time-step coupling for hybrid simulations of multiscale flows*](https://doi.org/10.1016/j.jcp.2012.11.032), *JCP* 237:344–365. Time-scale coupling, not spanwise wall forcing.
5. **Lockerby, Patronis, Borg & Reese (2014 online / 2015 volume)**, [*Asynchronous coupling of hybrid models for efficient simulation of multiscale systems*](https://doi.org/10.1016/j.jcp.2014.12.035), *JCP* 284:261–272. Different simulation regions need not march in exact temporal lockstep.
6. **Lockerby & Collyer (2016)**, [*Fundamental solutions to moment equations for the simulation of microscale gas flows*](https://doi.org/10.1017/jfm.2016.606), *JFM* 806:413–436. Fundamental-solution route for moment systems.
7. **Claydon, Shrestha, Rana, Sprittles & Lockerby (2017)**, [*Fundamental solutions to the regularised 13-moment equations*](https://doi.org/10.1017/jfm.2017.763), *JFM* 833:R4. Three-dimensional kinetic effects without full kinetic simulation in every region.
8. **Longshaw et al. (2018)**, [*mdFoam+: Advanced molecular dynamics in OpenFOAM*](https://doi.org/10.1016/j.cpc.2017.09.029), *Computer Physics Communications* 224:1–21 ([Warwick open paper](https://wrap.warwick.ac.uk/id/eprint/93436/)). **Actual open-source MPI molecular-dynamics solver**, within OpenFOAM's **C++** framework. Reference for algorithms and tests; *no C++ implementation is being imported into this repository*. Separate [OPENFOAM-2.4.0-MNF-1.0.1 dataset](https://wrap.warwick.ac.uk/id/eprint/135330/) is an archived software package, not a wing microjet trial.
9. **Stephenson, Kermode & Lockerby (2018)**, [*Accelerating multiscale modelling of fluids with on-the-fly Gaussian process regression*](https://doi.org/10.1007/s10404-018-2164-z), *Microfluidics and Nanofluidics* 22:139 ([full text](https://pmc.ncbi.nlm.nih.gov/articles/PMC6404643/)). Surrogate uncertainty triggers additional expensive molecular simulations, avoiding repeated redundant atomistic calls.
10. **Tatsios et al. (2025)**, [*A DSMC-CFD coupling method using surrogate modelling for low-speed rarefied gas flows*](https://doi.org/10.1016/j.jcp.2024.113500), *JCP* 520:113500 ([open manuscript](https://arxiv.org/abs/2311.14140)). Bayesian corrections learned from DSMC address particle noise; validated on canonical low-speed rarefied parallel-plate flow, **not a wing**.
11. **Lockerby (2025)**, [*First-order analysis of slip flow for micro and nanoscale applications*](https://doi.org/10.1017/flo.2024.34), *Flow* 5:E3. Reciprocal theorem produces first-order slip corrections from no-slip Stokes-flow solutions.
12. **Lockerby (2025)**, [*A correction tensor for approximating drag on slow-moving particles of arbitrary shape and Knudsen number*](https://doi.org/10.1017/jfm.2025.10776), *JFM* 1022:R1. Cunningham/Stokes/Knudsen particle drag, compared with kinetic-theory references; **not turbulent aircraft skin friction**.

## 5. Researchers, projects and methods to follow

| Branch | Collaborators / connections | Why follow |
|---|---|---|
| MEMS jet actuation | Peter W. Carpenter; Christopher Davies | Coupled piezo-driven cavity/orifice model; velocity-vorticity boundary-layer solver |
| Streak formation | Sergei I. Chernyshenko; M. F. Baig; Carlos A. Duque-Daza | Linear growth, generalized Stokes layer, DNS comparisons |
| Experimental forcing | N. F. Pearce; Petr Denissenko | Streamwise/spanwise acceleration in measured boundary layers |
| Transverse-wall-force literature | Maurizio Quadrio; Pierre Ricco; Claudio Viotti; Michael Leschziner | DNS parameter maps, experimental support, energy/scale limitations |
| Higher-order gas models | Jason M. Reese; Henning Struchtrup; Rory Claydon | Burnett, R13, hybrid switching and fundamental solutions |
| Hybrid computational methods | Matthew K. Borg; Alexander Patronis; James R. Kermode; David Stephenson | Time coupling, molecular/continuum handoff, surrogate modeling |
| Fluctuating nanoscale flows | James E. Sprittles; Chengxi Zhao; Yixin Zhang | Thermal noise, nanodrops and thin-film instabilities; a **third** physical branch |

[Warwick's project/grant list](https://warwick.ac.uk/fac/sci/eng/people/duncan_lockerby/) is the anchor for the 2007–2012 Airbus/EADS/EPSRC sequence. See also [Lockerby's comprehensive Warwick publication index](https://wrap.warwick.ac.uk/view/author_id/9408.type.html), which includes research outside the above two lines (e.g. biological fluid mechanics, car-surface contamination and capillary-wave studies). Do **not** infer that every publication studies aerodynamics.

## 6. Concrete work for Leray / CFD solvers

**Physics comparison, not a solved millennium problem:** Leray weak Navier–Stokes theory gives existence/control frameworks for idealised viscous fluids. These engineering papers require *specific boundary data*, turbulent stresses, transitions, rarefaction corrections or molecular coupling. They neither prove 3D Navier–Stokes regularity nor disprove it.

**Three model/benchmark packets, in increasing fidelity:**

A. **Streak/forced-wall control:** plane channel at prescribed wall speed; compare unforced, time-periodic spanwise oscillation and streamwise-travelling spanwise waves. Store forcing amplitude, frequency, phase speed, Reynolds number, measured/derived wall shear, forcing power and net power. Compare linearized optimal transient growth to DNS; reproduce **parameter-dependent increases as well as decreases** in drag.

B. **Resonant microjet safety:** prescribe cavity pressure/volume, resonant frequency, orifice dimensions and wall-pressure forcing. Simulate **active and nominally inactive** actuators with incoming disturbances. Check whether passive resonance causes unintended strong three-dimensional disturbances. Do not credit a 40% aircraft-wide gain merely from an illustrative boundary layer.

C. **Hybrid rarefied solver:** canonical micro-Couette/Poiseuille or standing shear wave, varying Knudsen number. Compare NS + slip, R13/moment, DSMC and a hybrid method with switching/coupling. Report wall flux, non-equilibrium stress, noise and runtime. The [2025 surrogate article](https://doi.org/10.1016/j.jcp.2024.113500) and [2009 switching paper](https://doi.org/10.1098/rspa.2008.0497) give independent baselines.

**Adjacent repository:** [CFD solvers](../CFD%20solvers/README.md). Use it for numerical method comparisons and code-level tests; these notes define scientific provenance. No solver or code has been run by this citation spider.

## 7. Audit limits

- Verified: 2009 original article and wording/context; Warwick author-index metadata; publishers' abstracts and the 20 direct references printed in 2012 JFM; Blesbois (2013) citing 2012; independently identifiable follow-up papers, DOI/archives and grants.
- Not verified: original social-media URL; actual full-aircraft trials or 20% fuel benefit; a complete all-years forward-citation export; source/code artifacts for every paper; line-by-line validation of all scientific derivations.
- The complete author index carries duplicated records and non-journal items; “93 records” is **not** “93 separate peer-reviewed papers.”
