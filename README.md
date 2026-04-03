# Crosswalk Illumination Project

Coordinated overhead lighting for RRFB-equipped pedestrian crossings. The beacon tells drivers a crossing exists. The light lets them see the person in it.

## The Problem

76% of pedestrian fatalities happen after dark. Nighttime pedestrian deaths rose 84% from 2010-2023. Nashville: 4 out of 5 pedestrian fatalities occur on wide arterials with speeds above 30mph, mostly between 6pm-6am.

RRFBs (Rectangular Rapid Flash Beacons) draw driver attention to the *sign*. The crossing surface itself remains dark. The pedestrian is a shadow.

## The Gap in Standards

The MUTCD 11th Edition (2023) says lighting *should* accompany RRFBs. TDOT's manual says mid-block crossings *shall* include lighting design. But neither specifies:
- Coordinated activation with the beacon
- Beam geometry to light the crossing without blinding drivers
- Lux targets specific to activated crosswalk illumination
- Timer integration for pedestrian clearing

The word "should" instead of "shall" is the gap. Advisory, not mandatory.

## The Proposal

A narrow-beam overhead LED, solar-powered, activated by the same trigger as the RRFB. 15-20 second hold. Lights the crossing surface to IES RP-8 standards (20 lux vertical at 1.5m). Cuts off before reaching driver eye level. $2,000-4,500 incremental cost per crossing on a retrofit.

## What's Here

- `docs/` — research, data, standards analysis
- `spec/` — technical specification and electrical design
- `hardware/` — BOM, fixture selection, installation notes
- TSITE abstract for Tennessee Section ITE presentation
