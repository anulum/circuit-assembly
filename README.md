<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-ASSEMBLY — repository foundation
-->

# Circuit Assembly

Circuit Assembly is being built to design and verify die-to-package bondwire and flip-chip maps, `3Dblox`/`BoW`/`UCIe` multi-die chiplet stacks, wafer probe cards, automated-test-equipment load boards and carrier printed circuit boards — cross-checking die-backside substrate potential against conductive or insulating die-attach materials, simultaneous switching noise and electromagnetic compatibility pre-compliance — completely deterministically without AI. This checkout contains repository validation tooling and documentation only. Full foundation qualification is in progress. There is no installed package verifier, chiplet-stack planner, carrier-PCB checker or qualified record schema.

**What does not exist yet:**
- a package/PCB checker, chiplet stack planner or wirebond/substrate verifier;
- a registered runtime record schema;
- any migrated chiplet-partitioning module or fabrication Gerber/ODB++ archive.

## Boundary

**What this project owns:**

| Record | Scope |
|---|---|
| Assembly view | Pad-ring coordinates, die-backside electrical net, wirebond/bump geometry, package leadframe/substrate netlist, probe-card map and carrier-PCB stackup |
| Assembly package | Fabrication-ready package/PCB deliverables, decoupling network impedance, simultaneous-switching-noise (`SSN`/`SSO`) eye-opening bounds and electromagnetic compatibility pre-compliance budget |
| Chiplet and 3D stack specification | `3Dblox`, Bunch-of-Wires (`BoW`) or `UCIe` multi-die partition, micro-bump/hybrid-bond map, interposer routing, fibre-array alignment and cross-die thermal/power budgets |

**Static imports:** only Circuit Core and Circuit Technology.

**Records read without importing domain code:**

| Source | Records consumed |
|---|---|
| Circuit Core and Circuit Technology | entity references, design views, operation profiles, approvals, system budgets, technology profiles and board profiles |
| Circuit Physical | post-fill die pad-ring/substrate results and shuttle top-harness specifications |
| Circuit Fields and Circuit Photonics | 3D electromagnetic/thermal results and optical coupler alignments |
| Circuit Prototyping | inter-FPGA interconnect plans |
| Circuit Manufacturing, Circuit Flow and Circuit Learning | wafer-sort maps, hardware BOM provenance, learning records and circuit graph contracts |

**Capability registration and handoffs:** Registers the assembly tool-profile manifest with Circuit Core, feeds chiplet/package outputs to Circuit Physical, Circuit Fields, Circuit Digital, Circuit Mixed-Signal, Circuit Prototyping, Circuit Lab, Circuit Manufacturing, Circuit Acceptance and AER Link Witness, and receives generic chiplet partitioning split from SC-NeuroCore.

**Explicit non-claims and operating boundaries:**
- Every package, chiplet-stack and board verification step works deterministically without machine learning.
- `KiCad` (`GPL-3.0`) executes strictly as a separate child process over file boundaries.
- Pre-compliance electromagnetic compatibility simulations and bench checks never substitute for accredited external `CE` or `FCC` testing.

## Current tooling

Repository controls inspect:
- metadata and source attribution;
- workflows and dependency alignment;
- native documentation and repository inventory;
- preflight orchestration.

Metadata declares architecture-only maturity with empty implemented domain capability and claim inventories.

- Use the exact environment in [Contributing](CONTRIBUTING.md).
- Full CI and preflight belong in CI or in an explicitly admitted pre-push environment.
- See [Validation](VALIDATION.md) for the maintained validation scope.

## Intended evidence

Every future domain artefact will carry the platform's common provenance envelope, its source and environment digests, its confidentiality compartment and its explicit verification boundary. None of the planned record schemas is registered or qualified by this foundation.

## Documentation and support

Read [Architecture](ARCHITECTURE.md), [support](SUPPORT.md), [security reporting](SECURITY.md) and [citation metadata](CITATION.cff).

**Not claimed:**
- a hosted service, released package or DOI;
- a public CI status;
- a performed simulation, hardware measurement or sign-off verdict.

## Licence

Source is licensed under [AGPL-3.0-or-later](LICENSE). A commercial licence is available through the contact in [NOTICE](NOTICE.md).

![ANULUM](docs/assets/anulum_logo_company.jpg)

![Fortis Studio](docs/assets/fortis_studio_logo.jpg)

## Text and data mining reservation
The rightsholder, Miroslav Šotek (ANULUM), expressly reserves the use of the
works in this repository for text and data mining, including the collection of
this content for, and its use in, training, fine-tuning or evaluating machine
learning and artificial intelligence models, in accordance with Article 4(3) of
Directive (EU) 2019/790 and the national provisions transposing it.

No permission for such use has been granted beyond what the licence in
`LICENSE` grants. This reservation does not change that licence: uses the
licence permits remain permitted on its terms, including its attribution and
share-alike conditions.

Reservation made on 2026-11-22. Requests for permission: contact the
rightsholder through the contact listed in this repository.
