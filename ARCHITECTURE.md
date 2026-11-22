<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-ASSEMBLY — repository foundation
-->

# Architecture

## Current executable surface

The checkout contains:
- repository validation tooling;
- dedicated tests;
- workflow definitions;
- native documentation.

No domain component of Circuit Assembly is implemented yet. The metadata keeps domain capabilities, claims and qualified record formats empty.

## Intended data flow

1. **Chiplet and stack specification** defines multi-die bump maps, `BoW`/`UCIe` link lanes and package envelopes from technology profiles.
2. **Die-to-package and board co-design** checks die-backside substrate bias against die-attach conductivity, wirebond geometry, probe-card/load-board pinouts and `KiCad` PCB rules.
3. **Signal, power and EMC pre-compliance** combines field-solver S-parameters and thermal maps to verify simultaneous-switching eye margins and radiated/conducted pre-compliance.

## Ownership

**This project owns** the planned Circuit Assembly records and boundary rules.

**Owned elsewhere:**

| Responsibility | Owner |
|---|---|
| on-die layout and pad ring | Circuit Physical |
| 3D electromagnetic and thermal solving | Circuit Fields |
| optical waveguide design | Circuit Photonics |
| OSAT/PCB supplier handoff and assembly genealogy | Circuit Manufacturing |
| sign-off and external EMC certificate tracking | Circuit Acceptance |

## Interpretation

- **Pre-compliance.** Simulated emissions and impedance checks do not replace accredited EMC chamber testing.

Read [the documentation architecture](docs/ARCHITECTURE.md) for the planned records, domain rules and schema identifiers.
