# Questions and experiments

These are proposed investigations. None has been run for this folder. Each starts with a bounded question so the mathematical idea and numerical evidence can be compared.

## 1. A contact/Beltrami field with an exact viscous solution

Work on a flat periodic box with coordinates x, y, z modulo 2π. Choose nondimensional units and

**u₀(x,y,z) = (sin z, cos z, 0).**

This field has zero divergence, curl u₀ = u₀, |u₀| = 1, and Δu₀ = −u₀. Its velocity-dual one-form is

**α = sin z dx + cos z dy.**

A direct calculation gives α ∧ dα = dx ∧ dy ∧ dz, so it is contact everywhere. The Reeb field is u₀ itself. This supplies a particularly simple example of the [Etnyre–Ghrist correspondence](etnyre-ghrist.md).

Because u₀ has no z-component and depends only on z, its convective acceleration vanishes. With no forcing, constant pressure, and kinematic viscosity ν ≥ 0, the exact Navier–Stokes solution is

**u(t) = exp(−νt) u₀.**

Energy and helicity therefore both scale by exp(−2νt). These formulas are derived here from the displayed field; they are proposed reference values, not measured results.

Compare ν = 0 with positive ν. Record velocity error, divergence, energy, helicity, and particle locations while refining space and time separately. Physical decay has a known value, so extra loss or growth can be identified as numerical error.

For ν > 0, a particle moves along its original straight-line direction by an accumulated factor (1 − exp(−νt)) ÷ ν. Even an arbitrarily long observation covers only finite distance in the covering space. This provides a simple way to think about the finite-time reparametrization in [Miranda's viscous discussion](eva-miranda.md), without claiming this elementary field is computationally universal.

## 2. Does invariant drift change long-time vortices?

Use the **same finite matrix approximation** of spherical Euler flow for two time integrators: the geometric scheme associated with [Modin–Viviani/QuFlow](geometry-to-cfd.md) and a conventional comparison.

Fix initial data and spatial resolution; refine the time step independently. Record energy, angular momentum, several independent matrix Casimirs, and the organization of large vortices.

The question is whether time-integration error changes the observed organization. Changing the spatial discretization at the same time would obscure that comparison. At any fixed matrix size, only finitely many independent discrete invariants are being preserved.

## 3. Can a pressure gradient create a false velocity?

Choose a bounded incompressible problem with specified velocity on the boundary and a known solution. Add a forcing term ∇ψ, changing the pressure to p + ψ. The continuous velocity remains unchanged because the added force is canceled by the added pressure gradient.

Compare a compatible FEEC formulation with another mixed formulation across mesh sizes and viscosities. Measure the resulting change in velocity, divergence error, and kinetic energy. Keep boundary data consistent; a prescribed traction boundary would need its own corresponding adjustment.

This gives a direct test of the [pressure-robustness thread](geometry-to-cfd.md). It can be understood before introducing a complicated surface.

## 4. What do geometric diagnostics add to the denticle experiment?

Use the [existing shark-denticle protocol](../CFD%20solvers/shark-denticle-lift.md): compare the smooth foil, matched two-dimensional bump, and three-dimensional denticle arrangement under the same physical conditions.

Retain pressure distribution, lift, drag, separation, and mesh convergence as the principal observations. Then add:

- Signed helicity density u · ω, where ω = curl u.
- Velocity–vorticity alignment (u · ω) ÷ (|u| |ω|), only where both vectors are nonzero.
- A Beltrami-alignment residual |u × ω| ÷ (|u| |ω|), under the same nonzero condition.
- Separate traces of instantaneous streamlines, vorticity lines, and time-dependent particle paths.
- Energy and momentum budgets including viscosity and boundary fluxes.

Mark undefined alignment values at zeros rather than manufacturing an angle. At a stationary no-slip wall the velocity-dual contact form degenerates, so inspect the off-wall region explicitly.

The exploratory question is whether these diagnostics reveal a repeatable structural change associated with the measured pressure and forces. An interesting helicity plot alone does not establish a cause of lift. Longitudinal riblets can be a separate geometry study; they should not replace the protruding denticles in the existing comparison.

## 5. A numerical-looking problem entirely inside symplectic topology

[Hutchings and McDuff–Schlenk](symplectic-topology.md) make ellipsoid capacities accessible through ordered action sequences.

For an ellipsoid with capacity parameters 1 and 2, list all m + 2n for nonnegative integers m and n, retaining multiplicities:

**0, 1, 2, 2, 3, 3, 4, 4, 4, …**

For a ball with capacity parameter c, the corresponding list begins:

**0, c, c, 2c, 2c, 2c, …**

A symplectic embedding requires termwise capacity inequalities. The entry at index 2, counting the first zero as index 0, already forces c ≥ 2, stronger than the volume condition c ≥ √2.

This is a hand-computable starting point for the Fibonacci-staircase reading. A finite list supplies necessary lower bounds; it does not alone construct an embedding or prove the full optimal capacity function.

## Further questions

- Can a manageable Reeb return map become a benchmark for section crossings and return-time error?
- Which singular-end coordinate changes in b-geometry correspond to a physically meaningful domain?
- How do open boundaries change the useful interpretation of helicity?
- Which qualitative flow features survive changes in both discretization and diagnostic definition?

These threads can proceed independently. A mathematical obstruction, a useful numerical method, and an explanation of a measured force are different possible outcomes.
