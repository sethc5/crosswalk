# Closing the Dark Crossing Gap

**Coordinated Activated Illumination for RRFB-Equipped Midblock Crosswalks**

---

## The Problem

RRFBs tell drivers a crossing exists. They don't light the person in it.

- 76% of pedestrian fatalities nationally occur after dark (GHSA)
- Nighttime pedestrian fatalities rose **84%** between 2010 and 2023 (GHSA)
- In Nashville, 4 out of 5 pedestrian fatalities occur on wide, state-controlled arterials above 30 mph — predominantly between 6 PM and 6 AM
- Pedestrian fatalities on Tennessee state routes increased 17% in 2023 alone (24 to 28)
- 71% of Nashville pedestrian fatalities occur on roads with 4 or more lanes

The corridors are known: Nolensville Pike, Murfreesboro Pike, Gallatin Pike. The times are known. The mechanism is known — the pedestrian is a shadow in the roadway.

RRFBs increase driver yielding from ~10-20% to 70-90% (FHWA). But most yielding studies are conducted during daylight. At night, drivers may see the flashing beacon but cannot see the person. The beacon says "someone is crossing." The driver cannot confirm where.

## The Standards Gap

TDOT Traffic Operations Memo 2022 already requires that mid-block pedestrian crossings **shall** include lighting design. The mandate exists.

What doesn't exist is any specification for how that lighting should work at an RRFB crossing:

- No requirement for coordinated activation with the beacon
- No beam geometry spec to light the crossing without blinding drivers
- No illuminance target at the crossing surface (vs general area lighting)
- No clearing integration to keep the light on until the pedestrian is across

The MUTCD 11th Edition with Revision 1 (2025) says lighting *should* be a prerequisite for RRFB installation — advisory, not mandatory — and provides no activation specification at all. AASHTO's Roadway Lighting Design Guide reinforces IES RP-8 illuminance criteria but does not address coordinated activation.

A standard cobra-head streetlight near the crossing technically satisfies the current "shall." It does not solve the problem.

## The Fix

A narrow-beam overhead LED, solar-powered, activated by the same trigger as the RRFB.

- **Cutoff fixture, 15-25° beam**: Light pool confined to crossing surface. Driver sees an illuminated pedestrian, not a light source. Eliminates the glare objection that has historically blocked crosswalk lighting proposals.
- **4000K color temperature**: FHWA research (HRT-15-047) documents significant improvement in pedestrian detection with higher CCT in nighttime conditions (~20% at 4000K vs 3000K per IPWEA; 30-40% at wider CCT gaps per VTTI). Nashville's dark sky ordinance caps at 3000K, but TDOT state-route installations may be jurisdictionally exempt, and a variance path exists for safety-critical applications. The AMA's concerns about 4000K streetlighting address continuous all-night exposure — this system activates for 15-20 seconds per event.
- **20 lux vertical at 1.5m**: Meets ANSI/IES RP-8-25 — the actual standard for crosswalk illuminance.
- **Multi-fixture for wide roads**: A single narrow-beam fixture covers ~11ft at 25ft mounting height. Nashville's 4-5 lane arterials need 2-3 fixtures per crossing — one per direction of travel, optional median fixture. Fixtures share a single controller and solar/battery system.
- **Radar detection**: Triggers automatically (no reliance on push-button compliance), confirms crossing is clear before ramp-down, and captures demand and yield data that most RRFB locations currently lack.
- **Solar-first**: Sidesteps NES utility coordination on state routes. 48V DC bus with LiFePO4 battery, sized for 72 hours without solar charge at December insolation. Conduit stubbed for future hardwire.
- **Failsafe**: Mechanical timer relay — if the controller fails, push-button still triggers a 20-second illumination hold. System degrades gracefully, never goes dark silently.
- **Built for Nashville weather**: Rated for -10°F to 105°F, surge protection for 50-60 thunderstorm days/year, ice load tolerant, ASCE 7 wind rated.

## The Cost

| | Per Crossing |
|---|---|
| Coordinated illumination retrofit (solar, 2-fixture) | **$2,000–4,500** |
| Standard RRFB installation it augments | $10,000–15,000 |
| Pedestrian Hybrid Beacon alternative | ~$57,680 |
| FHWA statistical value of one life | $11–12 million |

The retrofit is 15–30% of the RRFB cost it improves. One prevented fatality pays for over 2,500 crossings.

### Maintenance is minimal

Battery replacement every 10-15 years is the primary recurring cost (shallow daily cycling extends LiFePO4 life far beyond rated cycles). LED fixtures at this duty cycle last effectively forever. Solar panel cleaning aligns with existing RRFB inspection schedules. Remote monitoring via cellular/LoRa flags faults before they require a truck roll.

## The Data Story

Every installation generates data that doesn't exist today for most RRFB locations:

- **Crossing demand**: Pedestrian volume by time of day — justifies infrastructure investment
- **Vehicle yield behavior**: Approach speed and deceleration on activation — measures actual safety impact
- **Near-miss detection**: Vehicles that don't slow during active crossings — identifies highest-risk locations
- **System health**: Battery state, solar production, activation counts — proactive maintenance
- **Crash reconstruction**: Timestamped activation records show whether the system was active during an incident

This data is the path to establishing a Crash Modification Factor (CMF) for coordinated crosswalk illumination — which doesn't exist today. Once a CMF exists, any jurisdiction in the country can use it to justify the improvement in benefit-cost analyses for federal funding.

## The Path Forward

### Pilot: Nolensville Pike (Fall 2026 – Spring 2027)

Nolensville Pike is the natural first site: active $13M SS4A grant, existing RRFB locations, high pedestrian crash history, TDOT already at the table. Retrofit 1-2 crossings with coordinated illumination, pair with a matched control crossing for evaluation.

**Pilot cost: $13,000-29,000** — including temporary data collection equipment and contingency. Less than 0.25% of the existing Nolensville Pike SS4A grant.

### Evaluation: 12-18 Months of Data (2027-2028)

Before/after comparison of nighttime yielding rates, vehicle speeds, and near-miss events at treatment vs control crossings. Results published through TSITE, ITE Journal, and submitted to FHWA CMF Clearinghouse.

### Specification Adoption (2028)

TDOT adopts supplemental specification as Traffic Operations Memo addendum. All future RRFB installations on state routes include coordinated illumination by default.

### University Corridors (Parallel Track)

Nashville's universities create a separate, potentially faster path. Belmont, Vanderbilt, TSU, Fisk, and Lipscomb all have campus-adjacent arterial crossings with high pedestrian volume. Universities bring:

- **Institutional funding** that moves faster than municipal budgets (Vanderbilt endowment: ~$10.9B)
- **Liability pressure** — a student fatality on a campus-adjacent crossing generates institutional, legal, and national media consequences
- **Political leverage** — parents from across the country send money to Nashville. That creates attention municipal corridors don't get.
- **Research partnership** — Vanderbilt Civil Engineering could co-author the evaluation study, adding academic rigor and publication credibility

Vanderbilt's Civil & Environmental Engineering department is already running a pedestrian safety study on campus using smartwatch data — students specifically flagged the need for better crossing illumination. That research is the justification; this system is the intervention.

University pilots can run in parallel with state-route pilots. Different funding, different approval chains, different pressure. If one stalls, the other moves.

### Scaling (2028+)

Corridor-wide deployment on Nashville's high-crash arterials and university perimeters. Nashville NDOT adopts for local roads. TSITE recommends to ITE nationally. Other state DOTs reference Tennessee's specification.

Tennessee writes the standard. Everyone else follows.

## Why This Works Politically

- **Supplements, doesn't replace.** TDOT already said "shall." This adds the "how."
- **No new mandate required.** It's implementation detail for an existing requirement.
- **Solves the jurisdictional split.** RRFBs are traffic engineering; lighting is public works. This spec ties them together at the trigger level.
- **Budget-friendly.** Solar-first avoids utility coordination costs. Incremental cost folds into existing HSIP or SS4A project budgets without changing benefit-cost ratios.
- **Multiple funding paths.** HSIP, Safe Streets for All, TDOT Pedestrian Safety Grants, RAISE, PROTECT — the improvement qualifies under all of them.
- **Data story.** The radar layer captures crossing demand and vehicle yield behavior — data TDOT and Nashville don't currently have. That alone justifies a pilot.
- **Vision Zero aligned.** Addresses Nashville's highest-priority safety gap (nighttime pedestrian fatalities on arterials) on its highest-crash corridors, in communities with the greatest equity need.
- **Liability favors action.** TDOT's own memo says "shall." Not specifying what that means creates more exposure than installing and maintaining a well-designed system with failsafes and data logging.

## What's in This Package

Everything needed to move this forward without additional research or development:

1. **Draft supplemental specification** — 7 requirements for TDOT Traffic Operations Memo addendum, covering illuminance, coordinated activation, optical control, clearing hold, power resilience, failsafe, and data capture. Written to be adoptable by TDOT and portable to ITE nationally.

2. **Full technical spec** — Optical design with multi-lane coverage geometry, 48V DC electrical architecture, detection options, communications, environmental durability for Nashville climate, surge protection, dimming protocol, time-of-night intelligence.

3. **Safety and human factors analysis** — Liability assessment, driver behavior impact, pedestrian behavior considerations, emergency vehicle interaction.

4. **Maintenance lifecycle** — Component lifespan analysis, maintenance schedule aligned with existing RRFB inspection cycles, cost projections.

5. **Hardware evaluation** — Fixture candidates (TAPCO SafeWalk, standard roadway LEDs, framing projectors) with selection criteria, photometric modeling requirements, BOM with volume pricing notes.

6. **Installation guide** — Retrofit sequence, pole loading analysis, vandalism/tamper resistance, NES coordination notes.

7. **Research compilation** — National and Nashville-specific crash data, complete standards landscape (IES RP-8, AASHTO, MUTCD, TDOT, Nashville), RRFB effectiveness baseline, comparable installations, cost comparisons.

8. **Funding strategy** — Federal (HSIP, SS4A, PROTECT, RAISE), state (TDOT Pedestrian Safety, THSO), and local (Vision Zero, Metro capital) funding mechanisms with recommended grant integration approach.

9. **Implementation plan** — Pilot site selection criteria and candidates, stakeholder map, approval pathway, evaluation methodology with study design, scaling timeline through 2028+.

10. **Complete legal and codes reference** — Every applicable code, standard, law, and regulation from federal statute to Nashville municipal ordinance. 50+ regulatory instruments catalogued with jurisdiction, applicability, and hard/advisory/conditional status. Includes design flags (CCT cap, MASH breakaway base, rapid shutdown, UL listings, Buy America) and site-specific screening requirements (floodplain, historic overlay, tree canopy, clear zone).

11. **University corridor analysis** — Belmont, Vanderbilt, TSU, Fisk, Lipscomb campus-adjacent crossings with institutional funding paths, liability analysis, and parallel pilot track.

12. **CCT and mesopic vision research** — FHWA, IES, and VTTI studies supporting 4000K for pedestrian safety, with dark sky variance pathway documentation.

13. **TSITE abstract** — 250 words, ready for submission.

---

*Nashville, TN — April 2026*
