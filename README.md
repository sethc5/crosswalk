# Coordinated Crosswalk Illumination for RRFB-Equipped Pedestrian Crossings

An open specification for solar-powered, radar-activated overhead LED illumination coordinated with Rectangular Rapid Flash Beacons (RRFBs) at midblock crosswalks.

The beacon tells drivers a crossing exists. The light lets them see the person in it.

**License**: [CC-BY-4.0](LICENSE) — use it, adapt it, put your jurisdiction's name on it.

---

## The Problem

- 76% of pedestrian fatalities occur after dark (GHSA)
- Nighttime pedestrian fatalities rose **84%** from 2010-2023
- RRFBs increase daytime yielding to 70-90%, but nighttime-specific data is sparse
- No Crash Modification Factor exists for coordinated crosswalk illumination
- TDOT already says "shall" for midblock crossing lighting — but no spec says *how*

The hardware exists. The standards gap is the problem. Nobody has written the spec that makes coordinated illumination standard practice.

## What's Here

A complete, field-ready package — not a product pitch, not a concept paper:

### For Researchers

Start with **[academic-summary.md](docs/academic-summary.md)** — overview, reading order, connection to existing pedestrian safety research, key numbers.

- [study-design.md](docs/study-design.md) — Full study design: hypotheses, variables, power analysis, analysis plan, IRB considerations, publication targets, CMF pathway
- Research funding pathways (UTC, NSF CMMI, FHWA EAR, TDOT Research Office) in [research.md](docs/research.md)

### For DOTs and Traffic Engineers

Start with **[executive-summary.md](docs/executive-summary.md)** — problem, gap, fix, cost, political framing.

- [system-design.md](spec/system-design.md) — Complete technical spec with draft TDOT supplemental language (7 requirements, ready for Traffic Operations Memo adoption)
- [tsite-abstract-draft.md](docs/tsite-abstract-draft.md) — 250-word abstract for ITE section meeting submission

### For Anyone

- [system-design.md](spec/system-design.md) — Full technical spec: optics, multi-lane beam geometry, 48V DC electrical, radar detection, comms, environmental durability, CCT justification (4000K for mesopic pedestrian detection), maintenance lifecycle, safety/liability analysis
- [hardware/](hardware/) — BOM ($2,000-4,500/crossing), fixture candidates, installation sequence, tamper resistance
- [research.md](docs/research.md) — Crash data, RRFB effectiveness baseline, CCT/mesopic vision research, comparable installations, funding mechanisms
- [legal-and-codes.md](docs/legal-and-codes.md) — 50+ applicable codes and regulations (federal, state, local) catalogued by jurisdiction and enforceability
- [implementation-plan.md](docs/implementation-plan.md) — Pilot site selection, stakeholder map, approval pathway, evaluation methodology, budget, timeline

## Key Numbers

| | |
|---|---|
| System cost per crossing (solar retrofit) | $2,000-4,500 |
| Standard RRFB installation it augments | $10,000-15,000 |
| FHWA statistical value of one life | $11-12 million |
| Pedestrian detection improvement at 4000K vs 3000K | 30-40% |
| Pilot budget (2 crossings + evaluation) | $13,000-29,000 |

One prevented fatality pays for over 2,500 crossings.

## Contributing

This is an open specification. If you're a traffic engineer, researcher, DOT staffer, or practitioner:

- **Adapt it** for your jurisdiction — swap Nashville codes for yours, adjust climate specs, identify your corridors
- **Build on it** — the study design is ready for a PI to pick up and fund
- **Use the language** — the draft TDOT supplemental specification is written to be adopted as a memo addendum by any state DOT
- **File issues** if you find errors, gaps, or improvements
- **Fork it** and run a pilot. That's the point.

## Origin

This work originated from direct observation of nighttime pedestrian conditions on Nashville arterials: RRFBs flash to alert drivers, but the crossing itself is dark. The pedestrian is invisible. The spec was written to close that gap — first in Tennessee, then anywhere.
