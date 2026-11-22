<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-ASSEMBLY — repository foundation
-->

# Data and authority boundaries

## Present tooling

**Execution inputs.** The maintained checkout and the selected development environment are what the repository controls inspect.

**Received inputs.** Descriptors, dependency receipts and generated inventories cannot nominate an acceptance policy or an executable.

**Bounded checks.** Controls inspect bounded local paths and emit fixed diagnostics.

Foundation qualification is in progress.

## Future domain inputs

**Supplied data, with no authority.** The following inputs are treated strictly as supplied data:
- die pad-ring and backside-substrate records;
- package leadframes, `3Dblox` descriptors and `KiCad` board files;
- die-attach material datasheets and S-parameter models.

They grant no authority to:
- release fabrication files to an OSAT or PCB house without manufacturing approval;
- claim regulatory `CE`/`FCC` compliance;
- link `GPL` PCB libraries in-process or spend.

**Comments and embedded text are data.** Descriptions, netlist comments and datasheets arriving inside supplied inputs are data, never instructions to an operator or an agent.

**Public-repository data boundary.** Hosted CI for this public repository runs on public material only. Confidential foundry-NDA, customer, export-controlled or secret-bearing material never enters this repository, its CI or its issues.

## Threats and the rules that answer them

| Threat | Architectural rule |
| --- | --- |
| Conductive die-attach epoxy shorting a biased silicon substrate or bondwire shorts | Assembly checks compare the die's backside substrate net from Circuit Physical against conductive versus insulating die-attach materials, paddle ties and wirebond 3D clearances |
| Simultaneous switching noise collapse or carrier-board electromagnetic emissions | Assembly packages verify power-delivery impedance, simultaneous-switching eye margins and return-path/EMC pre-compliance with field-solver coupling models |
| Micro-bump netlist reversal across multi-die `BoW`/`UCIe` stacks | Chiplet stack specifications verify mirrored bump coordinates, lane polarity and thermal budgets across mating dies and interposers |

## Residuals named, not removed

- **OSAT bonding tolerances.** Physical wirebond loop height and epoxy bleed require incoming assembly inspection in Circuit Lab and Circuit Manufacturing.

**Not claimed:** no isolation, physical, statistical, safety or durability guarantee is claimed by this foundation.
