# Crosswalk — Claude Code instructions

## What this is

Design spec and TSITE abstract for coordinated overhead lighting on RRFB-equipped pedestrian crossings. Not a software project — an infrastructure safety proposal with an engineering spec.

## Origin

Seth observed the problem driving Nashville arterials at night: RRFBs flash to alert drivers, but the crossing itself is dark. The pedestrian is invisible. The gap exists in every standard — MUTCD, TDOT, Nashville — as "should" not "shall."

## Current state

- Research compiled: national data (GHSA), Nashville-specific (crash records, corridors), standards analysis (IES RP-8, MUTCD, TDOT manual, Nashville manual)
- System design spec: narrow-beam LED, solar, 48V DC, radar detection, data capture, BOM $2K-4K/crossing
- TSITE abstract drafted for submission to Bryan Bartnik (Bryan.Bartnik@tn.gov)
- No code — this is a spec/policy project

## What's next

1. Review and polish the abstract
2. Submit to TSITE for spring/annual meeting
3. Optionally: prototype one unit for demonstration
4. Optionally: submit corridor-specific feedback to Nashville Vision Zero / TDOT

## Key files

- `docs/research.md` — all data, standards, contacts, cost estimates
- `spec/system-design.md` — full technical spec with BOM
- `docs/tsite-abstract-draft.md` — 250-word abstract ready for submission
