# Wider symplectic topology

This thread asks what global shapes and trajectories are possible when a geometric structure must be preserved. It belongs here both for its connections with Reeb dynamics and as an independent mathematical exploration.

## Gromov: holomorphic curves reveal global obstructions

**Mikhail Gromov (1985), “Pseudo holomorphic curves in symplectic manifolds.”** *Inventiones mathematicae* 82, 307–347. [Author-hosted paper](https://www.ihes.fr/~gromov/wp-content/uploads/2018/08/945.pdf).

Gromov studies surfaces whose tangent maps respect an almost complex structure, using a compatible symplectic form to control their area. These surfaces can detect constraints on embeddings that volume cannot see.

A central example is **non-squeezing**: a standard symplectic ball of radius r cannot fit symplectically into a cylinder whose disk in a conjugate coordinate plane has radius smaller than r, however much room the other directions provide. The cylinder can have infinite volume. Read the introduction and §0.3.A before following the analytic machinery.

Question: what information does preserving a two-form retain that preserving only the top-dimensional volume loses?

## Taubes: some periodic motion must exist

**Clifford Henry Taubes (2007), “The Seiberg–Witten equations and the Weinstein conjecture.”** *Geometry & Topology* 11, 2117–2202. [Paper](https://arxiv.org/abs/math/0611007) · [DOI](https://doi.org/10.2140/gt.2007.11.2117).

On a closed oriented three-manifold, every contact form has a Reeb field with a periodic orbit. “Closed” here means compact without boundary. The proof uses Seiberg–Witten Floer theory to obtain closed Reeb trajectories.

This belongs beside [Etnyre–Ghrist](etnyre-ghrist.md): it supplies an existence statement for Reeb motion. It also belongs beside [Miranda's undecidability thread](eva-miranda.md): existence of some periodic orbit and an algorithm deciding every specified trajectory's fate are different questions. An airfoil exterior with walls and inflow/outflow does not meet the stated closed-manifold hypotheses.

## Hutchings: assemble closed trajectories into algebra

**Michael Hutchings, “Lecture notes on embedded contact homology.”** Preprint 2013, revised 2014. [Archive](https://arxiv.org/abs/1303.5789) · [Author's full notes](https://math.berkeley.edu/~hutching/pub/bn-draft.pdf).

**Embedded contact homology**, or ECH, starts with collections of closed Reeb orbits on a contact three-manifold. Its differential counts suitable holomorphic curves in a related four-dimensional symplectic space. The resulting homology connects dynamics to topology.

The introduction offers a concrete route through ellipsoids and symplectic embeddings. Later sections explain the holomorphic-curve counts, the ECH index, and the differential. This is a place to examine chain complexes built from actual geometric trajectories.

**Michael Hutchings, “Quantitative embedded contact homology.”** Preprint 2010. [Paper](https://arxiv.org/abs/1005.2260).

This paper extracts **ECH capacities**, a sequence of numbers measuring symplectic embedding constraints. For a four-dimensional Liouville domain, the construction uses the contact dynamics of its boundary; a Liouville domain is a compact exact symplectic manifold with contact-type boundary. The capacities are monotone under symplectic embeddings. Start with ellipsoids and polydisks, where computations become explicit.

These are phase-space geometric quantities. A use as an observable in a particular fluid discretization would need a separately established symplectic model.

## McDuff–Schlenk: a Fibonacci staircase in an embedding problem

**Dusa McDuff and Felix Schlenk (2012), “The embedding capacity of 4-dimensional symplectic ellipsoids.”** *Annals of Mathematics* 175, 1191–1282. [Publisher and abstract](https://annals.math.princeton.edu/2012/175-3/p05) · [DOI](https://doi.org/10.4007/annals.2012.175.3.5).

How large must a symplectic ball be to contain an image of a given four-dimensional ellipsoid? The answer is richer than the volume bound: over an initial interval, the optimal size follows an infinite staircase related to Fibonacci numbers. The paper connects exceptional curves in blown-up projective planes, embedding constraints, and lattice-point counts.

This provides a manageable computational reading project: generate the ellipsoid action sequences and inspect a few embedding obstructions before studying the full staircase proof. It connects contact topology, symplectic four-manifolds, arithmetic patterns, and geometry without requiring a claimed CFD application.

## Threads to follow outward

| Thread | Next question | Entry already in this folder |
| --- | --- | --- |
| Symplectic rigidity | Which embeddings are forbidden despite sufficient volume? | Gromov; McDuff–Schlenk |
| Periodic motion | What topology forces a closed orbit? | Taubes; Etnyre–Ghrist |
| Holomorphic curves | How does counting surfaces detect dynamics? | Hutchings |
| Reduction | What remains after symmetry is removed? | [Singer and Marsden–Weinstein](foundations.md) |
| Singular structures | What survives along a hypersurface where the ordinary description becomes singular? | [Miranda–Oms; Guillemin–Miranda–Pires](eva-miranda.md) |
| Flexibility and computation | Which prescribed dynamics can a Reeb/Euler flow contain? | [Cardona–Miranda–Peralta-Salas–Presas](eva-miranda.md) |

A later expansion could add Lagrangian Floer theory, Legendrian knots, open books, and symplectic fillings. Those remain a reading frontier rather than a claim of coverage in this first collection.
