# Coordinated Crosswalk Illumination at RRFB-Equipped Midblock Crossings

## Overview

This package contains a complete system specification, research compilation, study design, and regulatory analysis for solar-powered, radar-activated overhead LED illumination coordinated with existing RRFB installations at midblock pedestrian crosswalks.

The work originated from direct observation of nighttime pedestrian conditions on Nashville arterials: RRFBs alert drivers to a crossing's existence, but the crossing surface remains dark. The pedestrian is invisible. The infrastructure gap is specific and well-documented — and no Crash Modification Factor exists for coordinated crosswalk illumination.

## The Research Opportunity

**No CMF exists.** FHWA's CMF Clearinghouse has no entry for the effect of coordinated activated illumination at RRFB crossings. RRFB-only CMFs are well-established (yielding rate increases from ~10-20% to 70-90%), but nighttime-specific crash reduction data is sparse, and no study isolates the incremental effect of adding coordinated illumination to an existing RRFB.

This package provides everything needed to design and execute that study:

- A field-ready system specification with BOM ($2,000-4,500 per crossing)
- A built-in data capture framework (radar activation logs, vehicle speed/yield, crossing demand, near-miss detection) that generates research data from every installation without additional instrumentation
- A complete study design with hypotheses, variables, power analysis, analysis plan, and publication targets
- Nashville-specific site candidates with before/after control design
- Regulatory clearance documentation (50+ applicable codes catalogued)

## Reading Order

**Start here:**

1. **This document** — overview and reading order (you're here)
2. **[study-design.md](study-design.md)** — Full study design: research questions, hypotheses, variables, data collection, sample size, analysis plan, IRB considerations, publication targets, and connection to ongoing Vanderbilt pedestrian safety research

**The system:**

3. **[system-design.md](../spec/system-design.md)** — Complete technical specification: optical design with multi-lane coverage geometry, 48V DC electrical architecture, environmental durability, CCT justification (4000K for mesopic pedestrian detection), radar detection, communications, maintenance lifecycle, safety/human factors analysis, draft TDOT supplemental specification language
4. **[bom.md](../hardware/bom.md)** — Bill of materials with fixture options and cost breakdown
5. **[fixture-selection.md](../hardware/fixture-selection.md)** — Fixture candidates and photometric modeling requirements
6. **[installation-notes.md](../hardware/installation-notes.md)** — Retrofit sequence, pole loading, tamper resistance

**The evidence base:**

7. **[research.md](research.md)** — National and Nashville crash data, RRFB effectiveness baseline, CCT/mesopic vision research, comparable installations, standards landscape, research and infrastructure funding pathways
8. **[legal-and-codes.md](legal-and-codes.md)** — Complete regulatory framework: 50+ instruments from federal statute to Nashville municipal ordinance, catalogued by jurisdiction and applicability

**Implementation:**

9. **[implementation-plan.md](implementation-plan.md)** — Pilot site selection criteria and candidates (including university corridors), stakeholder map, approval pathway, evaluation methodology, budget, timeline

## Key Numbers

| | |
|---|---|
| Nighttime pedestrian fatalities (national trend, 2010-2023) | +84% (GHSA) |
| Nashville pedestrian fatalities on arterials >30 mph | 4 out of 5 |
| RRFB yielding rate improvement (day, FHWA) | 10-20% to 70-90% |
| RRFB nighttime-specific yielding improvement | Unknown (research gap) |
| CMF for coordinated crosswalk illumination | Does not exist |
| Pedestrian detection improvement at 4000K vs 3000K | 30-40% (FHWA-HRT-15-047) |
| System cost per crossing (solar retrofit) | $2,000-4,500 |
| Pilot budget (2 crossings + data collection + contingency) | $13,000-29,000 |
| FHWA statistical value of life | $11-12 million |

## Connection to Vanderbilt Pedestrian Safety Research

This system design complements the ongoing campus pedestrian safety study using wearable physiological sensors (smartwatch heart rate variability) to identify high-stress pedestrian locations.

**Two complementary data streams:**

| | Smartwatch Study | This System |
|---|---|---|
| Measures | Pedestrian physiological stress response | Driver yielding, approach speed, near-miss events |
| Perspective | Pedestrian experience (subjective safety) | Infrastructure performance (objective safety) |
| Coverage | Campus and campus-adjacent crossings | Same crossings + arterial corridors |
| Data type | Heart rate variability, GPS location, time | Radar activation, vehicle speed, event timestamps |

**Combined analysis**: Linking pedestrian stress data with driver behavior data at the same crossings, before and after illumination retrofit, creates a uniquely comprehensive evaluation. A joint publication pairing "pedestrian perceived safety" with "objective safety metrics" would be novel in the transportation safety literature.

**Gresham Smith**: The existing Vanderbilt-Gresham Smith partnership provides photometric modeling capability (AGi32) to verify illuminance targets for specific crossing geometries — a gap between the current spec-level calculations and field-verified design.

## What This Package Is Not

- This is not a product pitch. No vendor relationship exists. The spec is performance-based and vendor-neutral.
- This is not a grant application. It's the technical foundation for one.
- This is not a completed study. It's the intervention design and study framework for a study that hasn't been run.

## Contact

Questions or interest in collaboration — open an issue on this repository or reach out via the channels listed in the repo profile.
