<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-ASSEMBLY — repository foundation
-->

# Repository architecture

## Current executable tooling

**What it contains:** the repository's metadata, source-provenance, workflow, dependency-alignment, documentation, inventory and preflight controls.

**What each control does:** it inspects its fixed, declared local scope.

**What received metadata cannot do:** select another acceptance policy or grant domain authority.

Foundation qualification is in progress.

## Intended domain boundaries

| Record | Responsibility | Required evidence |
| --- | --- | --- |
| Assembly view | Pad-ring coordinates, die-backside electrical net, wirebond/bump geometry, package leadframe/substrate netlist, probe-card map and carrier-PCB stackup | Cross-check of die-backside potential against conductive versus insulating die-attach epoxy and wirebond loop/crossing clearances |
| Assembly package | Fabrication-ready package/PCB deliverables, decoupling network impedance, simultaneous-switching-noise (`SSN`/`SSO`) eye-opening bounds and electromagnetic compatibility pre-compliance budget | Verified power-delivery target impedance, return-path continuity and bill-of-materials provenance alignment |
| Chiplet and 3D stack specification | `3Dblox`, Bunch-of-Wires (`BoW`) or `UCIe` multi-die partition, micro-bump/hybrid-bond map, interposer routing, fibre-array alignment and cross-die thermal/power budgets | Consistent bump netlists, link lane budgets and thermal coupling handoff to Circuit Fields and Circuit Physical |

## Licence isolation

- **Separate-process PCB tools.** `KiCad` (`GPL-3.0`, command-line DRC/ERC/export) runs strictly in a separate process; permissive geometry and netlist checkers run in-process.

## Planned record schemas

- `circuit_assembly.assembly_view.v1`
- `circuit_assembly.assembly_package.v1`
- `circuit_assembly.chiplet_and_3d_stack_spec.v1`

These are planned identifiers. None of them is registered or qualified here.

Read [validation tooling](validation-tooling.md) for the executable repository interfaces.
