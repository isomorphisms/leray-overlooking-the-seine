# Etnyre and Ghrist: contact topology and hydrodynamics

A contact form carries a Reeb field. A suitably nonvanishing Beltrami field can be translated into that language, so contact topology can answer questions about its trajectories. The [plain-language guide](geometry-in-plain-words.md) derives the correspondence and explains where the metric enters.

## I. Beltrami fields and the Seifert conjecture

**John Etnyre and Robert Ghrist (2000), “Contact topology and hydrodynamics: I. Beltrami fields and the Seifert conjecture.”** *Nonlinearity* 13, 441–458. [Author page](https://etnyre.math.gatech.edu/preprints/hydro.html) · [Paper](https://arxiv.org/abs/dg-ga/9708011) · [DOI](https://doi.org/10.1088/0951-7715/13/2/306).

The paper establishes the relationship between nonsingular rotational Beltrami fields and Reeb-like fields. It obtains closed-orbit results on the three-sphere and conditions for periodic orbits on the three-torus.

Two levels of hypotheses should remain distinct: the Beltrami correspondence is smooth, while the general steady-Euler result uses real analyticity. The converse realization allows a suitable Riemannian metric.

**“Seifert” here means the Seifert conjecture about periodic orbits.** It does not identify the paper as a theorem specifically about Seifert-fibered contact manifolds. For the related circle-bundle construction, see the Geiges entry in [Foundations](foundations.md).

## II. Solid tori

**John Etnyre and Robert Ghrist (2002), “Contact topology and hydrodynamics II: solid tori.”** *Ergodic Theory and Dynamical Systems* 22(3), 819–833. [Author page](https://etnyre.math.gatech.edu/preprints/tubes.html) · [Paper](https://arxiv.org/abs/math/9907112) · [DOI](https://doi.org/10.1017/S0143385702000408).

A steady, nonsingular, real-analytic Euler flow on a Riemannian solid torus, leaving its boundary invariant, has a closed flowline. The proof uses contact structures and a solid-torus version of the Weinstein conjecture.

The solid torus is an entire three-dimensional domain. An arbitrarily chosen tubular region around a numerical streamline need not have an invariant boundary, so it does not automatically meet the theorem's hypotheses.

## III. Knotted orbits

**John Etnyre and Robert Ghrist (2000), “Contact topology and hydrodynamics III: knotted orbits.”** *Transactions of the American Mathematical Society* 352, 5781–5794. [Author page](https://etnyre.math.gatech.edu/preprints/hydroIII.html) · [Paper](https://arxiv.org/abs/math-ph/9906021) · [DOI](https://doi.org/10.1090/S0002-9947-00-02651-9).

The authors construct a single steady, nonsingular, real-analytic Euler flow on a Riemannian three-sphere with periodic trajectories of every knot and link type. Contact constructions and dynamical templates control the topology. The Riemannian metric changes as part of the construction.

This motivates knotted-flow visualizations and trajectory classification. It does not by itself construct those knots in a prescribed Euclidean wing domain.

## Bibliographic details

The sequence was published **I: 2000; II: 2002; III: 2000**. The first preprint was titled simply *Contact Topology and Hydrodynamics*. The third preprint uses *knotted flowlines* where the published article uses *knotted orbits*. The [bibliography](references.bib) records the published titles and the preprint links.

## What to investigate

The first practical calculation is the velocity-dual contact condition:

**α ∧ dα = (u · curl u) vol.**

Away from zeros, examine velocity–vorticity alignment, closed trajectories, and changes in helicity. At a no-slip wall u = 0, so this particular contact form degenerates. The [CFD notes](geometry-to-cfd.md) treat these as candidate diagnostics; the [experiments](questions-and-experiments.md) keep pressure and forces as separate measured quantities.
