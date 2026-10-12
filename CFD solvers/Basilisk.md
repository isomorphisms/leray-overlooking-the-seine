# Basilisk — adaptive finite volume and embedded surfaces

**Source:** [basilisk.fr](https://basilisk.fr/) · [incompressible centered solver](https://basilisk.fr/src/navier-stokes/centered.h) · [embedded boundaries](https://basilisk.fr/src/embed.h)

**Numerics.** Incompressible Navier–Stokes with cell-centered velocities, pressure projection, finite-volume-style conservative transport, and adaptive Cartesian tree grids. Embedded boundaries permit solids without requiring a body-fitted grid. Its source is an extended C dialect with a special preprocessing/compiler path, not a plain stock-C library.

**Why riff on it.** Refine only near the denticle ridge, downstream bubble, high-vorticity tubes, and the suction-side boundary layer. First compare a smooth flat plate, 2D bump, and 3D isolated denticle. Then ask whether the same local mechanisms appear on an airfoil.

**Concrete first experiment.** In a low-Reynolds-number flat-plate flow, implement one parametrized denticle solid; output cross-plane streamwise vorticity, separation/reattachment, pressure traction, and a sequence of increasingly fine adaptive meshes. Add the 2D bump control, holding maximum height and chordwise station constant.

**Risk.** Adaptive cells still need enough **physical resolution across** the sub-millimetre ridges and at no-slip cut cells; low numerical cost is not guaranteed. Test embedded-boundary geometric accuracy and forces near cut-cell surfaces. The centered solver does not by itself validate a turbulence closure or the full 3D finite-wing experiment.

**Borrow:** readable event-based experiments, adaptive error indicators, finite-volume pressure/velocity coupling, geometry fractions. **Do not assume:** a 2D run proves 3D streamwise-vortex effects.

**Decision:** excellent experimental geometry/projection workbench; compare against a body-fitted or high-order solution before making lift claims.
