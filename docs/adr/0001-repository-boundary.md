<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-ASSEMBLY — repository foundation
-->

# Decision: unify die-attach, wirebond, chiplet-stack, probe/load-board and carrier-PCB design in Circuit Assembly

## Context

A silicon die that passes on-chip DRC/LVS still fails immediately if conductive silver epoxy shorts its substrate bias to a grounded paddle, if `BoW`/`UCIe` bump maps mirror-flip, or if carrier-PCB ground return paths collapse high-speed eyes.

## Decision

**What Circuit Assembly owns:**
- assembly view;
- assembly package;
- chiplet and 3d stack specification;

**What it imports:** only Circuit Core and Circuit Technology.

**Owned elsewhere:**

| Responsibility | Owner |
|---|---|
| on-die layout and pad ring | Circuit Physical |
| 3D electromagnetic and thermal solving | Circuit Fields |
| optical waveguide design | Circuit Photonics |
| OSAT/PCB supplier handoff and assembly genealogy | Circuit Manufacturing |
| sign-off and external EMC certificate tracking | Circuit Acceptance |

## Consequences

**What can be qualified now:** repository governance and validation tooling, before domain code exists.

**What it cannot qualify:** unimplemented schemas, solvers, hardware or sign-off verdicts.

**Architectural consequences:**
- Circuit Assembly owns package, carrier-PCB, probe/load-board and chiplet-stack records between Circuit Physical and Circuit Manufacturing;
- `KiCad` runs strictly in a separate process and 3D field solving stays in Circuit Fields.
