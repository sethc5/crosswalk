# Coordinated Crosswalk Illumination for RRFB-Equipped Pedestrian Crossings

An open specification for solar-powered, radar-activated overhead LED illumination coordinated with Rectangular Rapid Flash Beacons (RRFBs) at midblock crosswalks.

The beacon tells drivers a crossing exists. The light lets them see the person in it.

**License**: [CC-BY-4.0](LICENSE) — use it, adapt it, put your jurisdiction's name on it.

---

## The Problem

- 76% of pedestrian fatalities in the US occur after dark (GHSA)
- Nighttime pedestrian fatalities rose **84%** from 2010-2023
- RRFBs increase daytime yielding to 70-90%, but nighttime-specific data is sparse — the beacon says "someone is crossing" while the pedestrian remains invisible
- No Crash Modification Factor exists for coordinated crosswalk illumination

The MUTCD 11th Edition with Revision 1 (2025) says lighting *should* accompany RRFBs. Multiple state DOTs require lighting at midblock crossings. But no standard specifies coordinated activation, beam geometry, illuminance targets, or clearing integration.

The hardware exists. The standards gap is the problem. Nobody has written the spec that makes coordinated illumination standard practice.

## What's Here

A complete, field-ready package — not a product pitch, not a concept paper. Developed using Nashville, TN as the primary case study (data, codes, corridors), but written to be adapted to any US jurisdiction.

### For Researchers

Start with **[academic-summary.md](docs/academic-summary.md)** — overview, reading order, connection to existing pedestrian safety research, key numbers.

- [study-design.md](docs/study-design.md) — Full study design: hypotheses, variables, power analysis, analysis plan, IRB considerations, publication targets, CMF pathway
- Research funding pathways (UTC, NSF CMMI, FHWA EAR, state DOT research offices) in [research.md](docs/research.md)

### For DOTs and Traffic Engineers

Start with **[executive-summary.md](docs/executive-summary.md)** — problem, gap, fix, cost, political framing.

- [system-design.md](spec/system-design.md) — Complete technical spec with draft supplemental specification language (7 requirements, written for state DOT Traffic Operations Memo adoption)
- [tsite-abstract-draft.md](docs/tsite-abstract-draft.md) — 250-word abstract adaptable for any ITE section meeting

### For Anyone

- [system-design.md](spec/system-design.md) — Full technical spec: optics, multi-lane beam geometry, 48V DC electrical, radar detection, comms, environmental durability, CCT justification (4000K for mesopic pedestrian detection), maintenance lifecycle, safety/liability analysis
- [hardware/](hardware/) — BOM ($2,000-4,500/crossing), fixture candidates, installation sequence, tamper resistance
- [research.md](docs/research.md) — Crash data, RRFB effectiveness baseline, CCT/mesopic vision research, comparable installations, funding mechanisms
- [legal-and-codes.md](docs/legal-and-codes.md) — 50+ applicable codes and regulations catalogued by jurisdiction and enforceability (Nashville-specific, but the federal/national sections apply everywhere)
- [implementation-plan.md](docs/implementation-plan.md) — Pilot site selection, stakeholder mapping, approval pathway, evaluation methodology, budget, timeline

### Audit and review scaffolds

- [audit/](audit/) — Photometric verification, study design self-audit against FHWA CMF Clearinghouse, electrical PE review checklist, structural review checklist, site-specific screening template, Buy America compliance matrix, legal review template, IRB exemption draft

## Key Numbers

| | |
|---|---|
| System cost per crossing (solar retrofit) | $2,000-4,500 |
| Standard RRFB installation it augments | $10,000-15,000 |
| FHWA statistical value of one life | ~$13.7 million (2024) |
| Pedestrian detection improvement at 4000K vs 3000K | ~20% (IPWEA); higher at wider CCT gaps (VTTI, unverified) |
| Pilot budget (2 crossings + evaluation) | $13,000-29,000 |

One prevented fatality pays for over 3,000 crossings.

## Adapting for Your Jurisdiction

This spec is Nashville-first because that's where the observation and data originated. To adapt it:

1. **Swap the local codes** — [legal-and-codes.md](docs/legal-and-codes.md) is organized in three tiers: Nashville-specific (Part 1), Tennessee state (Part 2), and federal/national (Part 3). Part 3 applies everywhere. Replace Parts 1-2 with your state and local codes.
2. **Swap the corridors** — the [implementation plan](docs/implementation-plan.md) identifies Nashville corridors and universities. Replace with your high-crash pedestrian corridors and institutions.
3. **Adjust climate specs** — the environmental durability section in [system-design.md](spec/system-design.md) is designed for Nashville (hot, humid, ice storms, 115 mph wind). Adjust temperature range, solar insolation, and wind speed for your location.
4. **Check dark sky rules** — Nashville caps outdoor CCT at 3000K; the spec includes a safety variance argument for 4000K. Your jurisdiction may have different or no CCT restrictions.
5. **Use the draft language** — the supplemental specification in the system design is written to plug into any state DOT's existing lighting manual. Change the memo reference to your state's equivalent.

## Contributing

- **Adapt it** for your jurisdiction — the whole point of CC-BY-4.0
- **Build on it** — the study design is ready for a PI to pick up and fund
- **Use the language** — the draft supplemental specification is written to be adopted as a memo addendum by any state DOT
- **File issues** if you find errors, gaps, or improvements
- **Fork it** and run a pilot

## Origin

This work originated from direct observation of nighttime pedestrian conditions on urban arterials: RRFBs flash to alert drivers, but the crossing itself is dark. The pedestrian is invisible. The spec was written to close that gap — anywhere.
