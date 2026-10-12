# Leray, fluid mechanics, and useful theory before and after observation

These notes follow a set of 2018–2025 social-media screenshots on Jean Leray, mathematical mechanics, drag reduction, and the relation between research and industrial practice. The screenshots are **research leads**, not independent evidence that a scientific or historical claim is true. The reading links below lead to primary papers or identifiable institutional sources.

## Leray's two settings

- **Fluid dynamics, 1934:** Leray's work on the three-dimensional Navier–Stokes equations established the global existence of weak solutions, along with important results on strong solutions and possible singularities. Ożański and Pooley reconstruct those arguments, including weak–strong uniqueness and the singular-time set: [arXiv:1708.09787](https://arxiv.org/abs/1708.09787).
- **Oflag XVIIA, 1940–1945:** While imprisoned, Leray redirected his work from mechanics toward algebraic topology and developed ideas leading to sheaves, sheaf cohomology, and spectral sequences. Haynes Miller's history is [Leray in Oflag XVIIA](https://math.mit.edu/~hrm/papers/ss.pdf). This is not Oflag XVIIIA.

One passage in the screenshot states a fact worth keeping precise: **in a Hilbert space** (in particular $L^2$), weak convergence $u_n \rightharpoonup u$ *together with* $\|u_n\|\to\|u\|$ implies strong convergence. Indeed,

$$
\|u_n-u\|^2=\|u_n\|^2+\|u\|^2-2\langle u_n,u\rangle\to0.
$$

It is not an unrestricted theorem for every normed space. This kind of compactness/weak-solution argument matters to Leray's work.

## The wing-waggling episode: what was observed, proposed, and understood

1. **2005 — modelling streaks.** Lockerby, Carpenter, and Davies, *Control of sub-layer streaks using microjet actuators*, [AIAA Journal](https://doi.org/10.2514/1.14443). Numerical models study how microjets interact with near-wall structures in boundary layers; this is already a theory-driven investigation.
2. **2007 — a potential difficulty.** The same authors, *Is Helmholtz resonance a problem for micro-jet actuators?*, [Flow, Turbulence and Combustion](https://doi.org/10.1007/s10494-006-9056-0). In some model conditions, nominally inactive actuators become strong sources of disturbances. The mechanism that is intended to help may also create instabilities.
3. **2009 — the public announcement.** The EPSRC/Airbus-funded work led by Duncan Lockerby was described in [*Wings That Waggle Could Cut Aircraft Emissions By 20%*](https://www.sciencedaily.com/releases/2009/05/090521084721.htm). Lockerby described a wind-tunnel observation when a *piece of wing* was moved side to side. The proposed practical implementation involved **small oscillating air jets**, potentially using Helmholtz-resonant cavities to force air sideways near the surface. **Up to 40% reduction in skin-friction drag** and **20% fuel savings** were proposals/projections in this 2009 account, **not established full-scale aircraft results**. The story called the work *concept stage*.
4. **2012 — follow-up modelling.** Duque-Daza, Baig, Lockerby, Chernyshenko, and Davies, *Modelling turbulent skin-friction control using linearized Navier–Stokes equations*, [Journal of Fluid Mechanics](https://doi.org/10.1017/jfm.2012.189) ([full paper](https://orca.cardiff.ac.uk/id/eprint/25034/1/Duque-Daza%202012.pdf)). They correlate changes in calculated near-wall streak amplification with published direct numerical simulations of drag reduction under spanwise wall forcing. This **helps explain a related control mechanism**; it is not a proof of a commercial microjet wing's performance. See also [Chernyshenko's explanation](https://www.imperial.ac.uk/aeronautics/fluiddynamics/ChernyshenkoResearch/drag-reduction.php).

The **shark-denticle airfoils** studied by Domel *et al.* (2018), already referenced in this repository, are **another design**. The 2009 EPSRC article also mentions shark-like riblets; that does not make the two experiments identical.

## A separate Lockerby paper: non-equilibrium gas flow

**D. A. Lockerby and J. M. Reese (2008), [*On the modelling of isothermal gas flows at the microscale*](https://wrap.warwick.ac.uk/id/eprint/863/)**, *Journal of Fluid Mechanics* 604, 235–261 ([PDF](https://wrap.warwick.ac.uk/id/eprint/863/1/WRAP_Lockerby_modelling_isothermal.pdf)).

The 2023 screenshot characterizes the R13 model as arbitrarily chosen. The paper says something more definite: it constructs a time-varying standing shear-wave benchmark without solid-wall boundary conditions and **compares several extended hydrodynamic models**, finding the **regularized 13-moment (R13)** equations performed best *in that benchmark*. That is comparative model evidence, not a general proof that R13 is exact. The issue here is microscale **rarefaction/non-equilibrium** and the limitations of conventional continuum models, **not** the same issue as turbulent skin friction on aircraft wings.

These two Lockerby strands—rarefied-gas models and turbulent drag control—should remain distinct even though the same researcher appears in both.

## Other leads visible in the screenshots

- **Andrew N. Norris, Rutgers:** [publication index](https://coewww.rutgers.edu/~norris/papers.html). The screenshot's `.../papers...` link does **not** identify which paper was intended. Do not assign a title without recovering the complete URL.
- **J. Scott Turner, SUNY College of Environmental Science and Forestry (Syracuse):** an animal/biophysics lecture was linked as [this YouTube video](https://youtu.be/KajHpHdZoAM) in a December 2025 post. Its full title/content has not been independently checked; his work on termites and flows is illustrated by [this interview](https://www.loe.org/shows/segments.html?programID=09-P13-00042&segmentID=8).
- **Margaret Byron:** [Penn State research](https://news.engr.psu.edu/2021/byron-margaret-bio-fluid-structure-interaction.aspx) on biological fluid mechanics. The screenshot's characterization of her status as a mechanical engineer is an opinion, not an adequate description of her qualifications; [a 2020 seminar biography](https://sites.google.com/view/frontiersmes/) records a Princeton B.S.E. in Mechanical and Aerospace Engineering and Berkeley graduate degrees in Civil and Environmental Engineering.
- **Engineering education and funding priorities:** the GVSU factory-floor/controls-course quotes and a 2020 criticism of NSF graduate fellowship priorities concern the sociology of research, not evidence about fluid motion. The latter source can be identified as [Peter Woit, *Funding Priorities* (August 2020)](https://www.math.columbia.edu/~woit/wordpress/?p=11961); the exact GVSU article URL is truncated in the screenshots and remains to be recovered.

## Questions worth testing, not assuming

- Which effects of spanwise forcing are reproduced by linearized Navier–Stokes, and which require nonlinear DNS or experiments?
- Does passive Helmholtz-resonant actuation give a *net* benefit after power, weight, and instability effects are counted? Do not substitute 2009 aspirations for field trials.
- How does an R13 approximation compare with kinetic or particle-based reference solutions **outside** its selected standing-shear-wave benchmark?
- Which arguments in Leray's 1934 paper use (L^2) weak convergence and compactness, and where is strong convergence actually needed?

**Boundary of this collection:** original screenshots/posts motivate the reading questions; citations and empirical conclusions come from the identifiable papers and institutional sources above.
