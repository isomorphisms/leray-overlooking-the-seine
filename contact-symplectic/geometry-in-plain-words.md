# Geometry in plain words

Start with three things one can do to a moving fluid: follow a particle, measure circulation around a loop, and measure flux through a surface. Those operations use different mathematical objects, even when ordinary vector notation makes them look alike. [Burke's notes](william-burke.md) and [Arnold–Khesin](foundations.md) provide complementary routes into this distinction.

## Forms remember what is being measured

A **one-form** accepts a direction and returns a number; integrating it along a curve adds those directional measurements. A **two-form** accepts an oriented pair of directions; integrating it over a surface measures an oriented surface quantity.

For a velocity field u in an oriented three-dimensional Riemannian domain:

- Its metric-dual one-form α is defined by α(v) = g(u,v), where g is the metric and v is a direction. Integrating α around a loop measures circulation.
- Contracting the volume form with u gives a flux two-form. Integrating it over a surface measures volume flux.
- The exterior derivative dα is the vorticity two-form. The metric and orientation identify it with the usual curl u.

Thus circulation, flux, and curl have related but distinct roles. The exterior derivative d belongs to the differential-form calculus; the metric enters through the duality and Hodge star. That distinction matters when transferring equations to a mesh. See [Burke](william-burke.md) and [the numerical notes](geometry-to-cfd.md).

## Symplectic geometry: a pairing preserved by motion

For a mechanical particle, position alone does not specify the instantaneous state: momentum matters too. The space of position–momentum pairs is its **phase space**.

A symplectic form ω assigns a signed area to each pair of infinitesimal directions. It is closed, dω = 0, and nondegenerate: every nonzero direction pairs nontrivially with some other direction. Nondegeneracy forces the dimension to be even.

For one degree of freedom, a standard model is ω = d(position) ∧ d(momentum). Hamiltonian evolution preserves this form. An ideal harmonic oscillator provides a concrete picture: after a suitable choice of units, its phase points rotate around circles. Small phase-space areas retain their area.

In higher dimensions, preserving ω is more restrictive than preserving total volume; [Gromov's non-squeezing theorem](symplectic-topology.md) makes that difference global. [Singer](stephanie-frank-singer.md) develops the mechanical meaning, while [Cannas da Silva](foundations.md) develops the geometry.

## Contact geometry: a twisting family of planes

In three dimensions, a contact form α selects a plane at each point: the directions v for which α(v) = 0. The condition α ∧ dα ≠ 0 says that these planes twist in a way that prevents them from fitting together into local surfaces everywhere.

An explicit local example is α = dz − y dx. Its derivative is dα = dx ∧ dy, and α ∧ dα = dz ∧ dx ∧ dy, which never vanishes.

The **Reeb field** R associated with α is determined by two conditions:

- α(R) = 1 fixes its speed relative to the chosen form.
- dα(R,v) = 0 for every direction v fixes its direction.

For the displayed local example, R = ∂/∂z. The plane field alone does not fix this particular Reeb motion: changing the contact form by a positive factor preserves its kernel but can change the Reeb dynamics. [Geiges](foundations.md) supplies the general theory.

## The exact fluid bridge

Suppose a smooth divergence-free field u satisfies curl u = f u, and both u and the scalar f are nowhere zero. Such a field is called a nonvanishing rotational **Beltrami field**: velocity and vorticity point along the same line.

For its velocity-dual form α, a direct calculation gives

**α ∧ dα = (u · curl u) vol = f |u|² vol.**

This never vanishes, so α is contact. Its Reeb field is

**R = u ÷ |u|².**

The paths are the same, with a different time parametrization. Conversely, a Reeb field can be realized as a rotational Beltrami field for a suitable metric and volume form. The chosen metric is part of that converse. This is the bridge established in [Etnyre–Ghrist I](https://arxiv.org/abs/dg-ga/9708011) and reviewed in [Cardona–Miranda–Peralta-Salas–Presas](https://arxiv.org/abs/2012.12828).

Nonzero u · curl u by itself makes the velocity-dual form contact; it does **not** by itself identify its Reeb field with the original fluid velocity. The Beltrami alignment supplies that extra condition.

## What changes in a fluid with walls?

At a no-slip stationary wall, u = 0. The displayed velocity-dual contact form therefore degenerates there. This follows directly from the formula above; a simulation should not declare contact structure throughout its domain merely because a vortex picture looks twisted.

The state space of an ideal fluid is also much larger than its three-dimensional physical domain. Its Hamiltonian formulation generally uses a **Poisson** structure, which may be degenerate; appropriate symplectic leaves sit inside that state space. A three-dimensional divergence-free field is not automatically a finite-dimensional Hamiltonian system in its spatial coordinates. [Arnold–Khesin and Marsden–Ratiu](foundations.md) explain that distinction.
