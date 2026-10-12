# Experimental target and falsifiable CFD protocol

## Primary observations

Domel, Saadat, Weaver, Haj-Hariri, Bertoldi & Lauder, [2018, *J. Royal Society Interface* 15, 20170828](https://doi.org/10.1098/rsif.2017.0828), [supplementary material](https://doi.org/10.6084/m9.figshare.c.3986802.v3).

- A symmetric **NACA0012** airfoil; chord **68 mm**, span/chord **2.8**, tested in **water** at **0.58 m/s**, with kinematic viscosity approximately **10⁻⁶ m²/s**: chord Reynolds number approximately **4 × 10⁴**.
- Angles of attack **0–24° in 2° increments**.
- Twenty geometrical arrangements of denticles were examined. For the best-performing arrangement discussed in the paper: one row at **26% chord**, approximately **2 mm × 2 mm footprint** per denticle, **0.7 mm middle-ridge height**, **1 mm spanwise gap**. These few numbers **do not uniquely specify** the denticle. Reconstruct the ridges, tilt, and other dimensions from the paper and supplementary material rather than replacing the geometry with arbitrary bumps.
- The original authors used a water-flow experiment, particle-image velocimetry, and **ANSYS CFX**, with an unsteady implicit coupled flow solver and **SST turbulence model**, for an individual denticle on a flat plate. Their proposed mechanisms are local pressure changes from wake separation and streamwise vortices from the denticle's spanwise structure.

The headline **323%** concerns the **relative lift-to-drag ratio improvement for selected cases**, not raw lift, not all angles, and not all 20 designs. Reproducing only that percentage is not a validation.

## Cases: separate mechanisms before combining them

| Case | Shape | Question | Minimum observable |
| --- | --- | --- | --- |
| A | Smooth airfoil, no denticles | Is baseline flow and polar credible? | Lift, drag, pressure, separation |
| B | Matched **2D chordwise bump** | Is pressure/suction change enough for low-angle lift gain? | Chordwise pressure and integrated lift |
| C | **Single 3D denticle on flat plate** | Does a pair/pattern of streamwise vortices emerge? | Cross-plane ωₓ, wake bubble, wall shear |
| D | **3D denticle row on airfoil** | Do the two effects combine under matched conditions? | Lift/drag polar, Cp, ωₓ, reattachment |
| E | Streamwise micro-riblets on wall | Is conventional riblet drag reduction distinct? | Skin friction; do **not** call it airfoil lift |

Case B cannot test vortex generation by spanwise curvature: it has no such curvature. Case C on a flat plate cannot alone demonstrate net airfoil lift. Only Case D measures the proposed aerodynamic effect directly.

## Governing equations and quantities

For a constant-density incompressible Newtonian fluid:

∂ₜu + (u · ∇)u = −∇p/ρ + ν∇²u, and ∇ · u = 0.

Use a consistent airfoil planform reference area **A** for 3D lift and drag; for a 2D section, report forces per unit span and define the reference convention. 

- **C_L = L / (½ρU∞²A)**; **C_D = D / (½ρU∞²A)**. Integrate **both pressure and viscous stress** on the surface. Report changes in each contribution separately.
- **C_p = (p − p∞) / (½ρU∞²)** along the foil, and the location and extent of any separation/reattachment bubble.
- **ωₓ = ∂u_z/∂y − ∂u_y/∂z** for x streamwise, y wall-normal, z spanwise. Inspect a cross-plane downstream of a denticle; define coordinates and handedness explicitly.
- Wall shear, near-wall momentum, velocity profiles, time history, and vortical structures. Be careful: a colored vorticity plot by itself does not establish improved force.
- Report **C_L/C_D**, but also the absolute **C_L** and **C_D**, particularly near zero angle where ratios can mislead.

## Verification and validation

1. Record solver revision, dimensional units, exact mesh geometry, free-stream Reynolds number, angle, density, viscosity, finite wing-span/boundaries, boundary conditions, and turbulence model.
2. Run at least three mesh densities with **local** measures: cells across denticle height, around tip/ridge, through the wake and viscous sublayer; report achieved wall resolution and any unresolved feature. Merely refining the far field does not count.
3. Reduce timestep and record forces/pressure/vorticity after transient settling; distinguish steady means from instantaneous fields. Check mass conservation and force integration.
4. Compare to the smooth-foil polar and the reported experiment **before** choosing a best denticle. Include measurement uncertainty when available and finite-span/end effects, transition and support effects where relevant.
5. Isolate geometry from turbulence-model choices: laminar / transient resolved computation if feasible, then SST RANS/URANS and LES with explicit caveats. Do not treat all agreement between two SST runs as independent physics validation.
6. State whether source results are **reported in the paper**, **reconstructed from figures**, **predicted by our solver**, or merely **planned**. Store numeric input/output and scripts; no fabricated simulation results.

## Interpretation / competing hypotheses

- **H₁ (local suction):** the leading/trailing curvature of a raised element establishes a pressure deficit; a matched 2D bump should produce much of the low-angle effect.
- **H₂ (vortex energization):** three-dimensional denticle ridges generate streamwise vortices whose entrainment delays near-wall momentum loss and separation; Case D should outperform B in regimes where H₂ dominates.
- **H₃ (geometry-dependent drag penalty):** at other placements/heights/angles, added form drag or premature separation erases any benefit. Positive results are contingent, not universal.
- **H₄ (numerical artifact):** a claimed effect disappears on mesh/time refinement, geometry reconstruction, changed wall treatment, or independent method.

Do not mistake the unproven existence of a generic *shark skin lift* law for the specific measured lift change in this study. The natural continuation is controlled, falsifiable comparison.

Related reading: [2023 multi-fidelity modelling of shark denticle flows](https://doi.org/10.1098/rsos.220684), which contrasts numerical fidelity for denticle-related drag mechanisms.
