# System Design Specification

## Overview

Activated narrow-beam overhead LED coordinated with existing RRFB installation. Solar-powered, push-button or passive detection triggered, 15-20 second hold with pedestrian clearing detection.

## Optical Design

### Primary Fixture
- **Type**: Narrow-beam LED spot, 15-25° beam spread
- **Color temp**: 4000K recommended (see CCT justification below); 3000K fallback if variance not granted
- **Output**: 4,000-5,000 lumens (~50W LED equivalent)
- **Target**: 20 lux vertical at 1.5m above crossing surface (per IES RP-8-22; verify target unchanged in RP-8-25)
- **Mounting**: Pole-mounted at 20-25ft, approach side of crossing
- **Optics**: House-side shield, cutoff fixture to prevent driver glare
- **Aim**: 5-10° tilt from vertical toward approaching traffic. Pure straight-down aim maximizes horizontal illuminance but produces poor vertical illuminance at 1.5m (the IES RP-8-25 measurement height). Slight tilt directs beam center toward the pedestrian's vertical plane while keeping the fixture well below the driver's sight line. Exact tilt angle to be determined by photometric modeling with selected fixture's .ies file.

### CCT Justification: Why 4000K for Pedestrian Safety

Nashville's dark sky ordinance (BL2020-535) caps outdoor CCT at 3000K. However, there is a strong, research-backed safety case for 4000K at activated crosswalk locations, and multiple paths to authorization.

**The science:**

At nighttime ambient light levels, human vision shifts from photopic (cone-dominated, daytime) to mesopic (mixed rod-and-cone). In mesopic conditions, the eye's peak sensitivity shifts toward shorter (bluer) wavelengths — the Purkinje shift. Higher CCT light sources (4000K) provide more energy in the wavelengths where the mesopic eye is most sensitive.

- **FHWA-HRT-15-047** (2015): Found that in low-speed pedestrian environments, "lighting levels can be scaled based on the light source spectrum." Study compared 6000K vs 3500K LEDs and found significant detection improvements with higher CCT.
- **Terry & Gibbons (Virginia Tech Transportation Institute)**: 6000K LED outperformed 3500K LED by ~30% in pedestrian clothing color recognition distance. The performance difference is largest for dark clothing — exactly the worst case.
- **IES TM-12-12**: Establishes that mesopic multipliers apply to exterior environments at speeds <25 mph. Pedestrian crossings on arterials are exactly this environment — the approaching driver is (or should be) decelerating to well under 25 mph.
- **FHWA-HRT-08-053**: White-light sources improved detection of pedestrians in dark clothing at midblock crosswalks. Associates broad-spectrum light with better crosswalk detection performance.
- **2025 ScienceDirect study**: Visual performance stable across 1800K-4000K, with deficit at 5000K. Supports 4000K as the optimal ceiling — maximum safety benefit with no documented health or ecological downside.

**The practical difference:** At 3000K, achieving the same pedestrian detection performance as 4000K requires approximately 30-40% more lumen output — meaning a bigger fixture, more power, more battery, and more cost. 4000K delivers the safety target at lower wattage.

**Paths to 4000K authorization:**

1. **Jurisdictional argument**: TDOT state-route installations may be outside Nashville's municipal ordinance scope. The dark sky ordinance applies to new construction reviewed under Metro building codes. TDOT installations on state ROW follow TDOT standards, not Metro zoning.

2. **Variance via BL2022-1088**: Nashville's 2022 amendment authorizes the Board of Fire and Building Code Appeals to grant variances when strict enforcement would cause "manifest injustice" or contradict the "spirit and purposes" or public interest. A safety-critical application with FHWA research backing is a strong case.

3. **Legislative precedent**: Maine's LD 1934 (effective Sept 2026) — the most comprehensive US dark sky law — explicitly exempts DOT and pedestrian safety lighting from the CCT cap. This demonstrates that the exemption is recognized as appropriate even in the most restrictive dark sky jurisdictions.

4. **IPWEA (Australia)**: Formally recommends 4000K for main roads and pedestrian crossings, citing ~20% safety improvement. International practice supports the exception.

**Recommendation**: Spec the system at 4000K. Pursue the TDOT jurisdictional argument first (lowest friction). If Nashville claims jurisdiction, file for variance under BL2022-1088 with the FHWA research package. If variance denied, fall back to 3000K with increased lumen output to compensate. The fixture should be capable of either CCT via field-swappable LED module or tunable-white driver.

### Why Narrow Beam
- Eliminates glare objection (standard pushback on crosswalk lighting)
- Defined pool of light on crossing surface only
- Pedestrian lit from above — driver sees illuminated person, not light source
- Minimal light pollution / spill into adjacent properties

### Coverage Geometry

The beam math matters — Nashville's fatal corridors are 4+ lane roads (48-64ft curb-to-curb). A single fixture must cover the full crossing width or the design needs multiple fixtures.

**Single fixture coverage at mounting heights:**

| Mounting Height | 15° Beam Diameter | 25° Beam Diameter |
|-----------------|-------------------|-------------------|
| 20 ft | 5.3 ft | 8.9 ft |
| 25 ft | 6.6 ft | 11.1 ft |
| 30 ft | 7.9 ft | 13.3 ft |
| 35 ft | 9.3 ft | 15.5 ft |

*(Beam diameter = 2 × height × tan(beam angle / 2))*

A single 25° fixture at 25ft covers ~11ft — roughly one travel lane. A standard 4-lane crossing is 48ft minimum. **One fixture does not cover a wide road.**

**Multi-fixture configurations:**

| Road Width | Lanes | Fixtures Required | Configuration |
|------------|-------|-------------------|---------------|
| 24-30 ft | 2 | 1-2 | Single fixture on approach side, or one per direction |
| 36-48 ft | 3-4 | 2 | One fixture each side, aimed at near half of crossing |
| 48-64 ft | 4-5 + median | 2-3 | One each side + optional median-mounted fixture |
| 64+ ft | 5+ | 3+ | Median fixture mandatory; consider staged crossing |

**For Nashville's target corridors** (Nolensville, Murfreesboro, Gallatin Pikes — typically 4-5 lanes with center turn lane):
- Minimum 2 fixtures: one approach-side per direction of travel
- Each fixture covers its near 2 lanes
- Median-mounted third fixture recommended where median refuge island exists (common on these corridors)
- Each fixture aimed at crossing centerline within its coverage zone

**BOM impact**: Multi-fixture configurations multiply the fixture cost but share solar/battery/controller infrastructure. A 2-fixture 4-lane crossing adds ~$300-600 for the second fixture and arm, not a full system duplication. Controller drives both fixtures from one activation signal.

**Uniformity**: Multiple overlapping fixtures actually improve uniformity ratio across the crossing width — easier to meet the IES RP-8-25 max 4:1 uniformity requirement than with a single wide-beam fixture.

### Pole Offset Reality — Angled Array Configuration

In most real-world RRFB installations, the sign/beacon pole is mounted 20-30 feet ahead of the crosswalk on the approach side — not directly above it. This means any fixture mounted on the existing pole must aim backward and downward toward the crossing at a significant angle (30-45° from vertical, depending on setback and mounting height).

This offset geometry actually benefits the design:

1. **Vertical illuminance is inherent**: Light arriving at 30-45° from vertical illuminates the pedestrian's front — the face the approaching driver sees. This naturally produces the vertical illuminance that IES RP-8-25 measures at 1.5m, without the fixture tilt workaround needed for a directly-overhead mount.

2. **Linear LED array configuration**: Rather than a single large fixture, mount a bank of 15-30 small, tightly focused LED emitters in a linear array on the pole arm. Each emitter covers a slice of the crosswalk. The array shapes the illuminated area to match the crosswalk rectangle — not a circular pool. This is analogous to front-of-house PAR arrays in stage lighting, aimed from a distance to precisely illuminate a performance area.

**Array advantages over single fixture:**

| | Single Fixture | LED Array (15-30 emitters) |
|---|---|---|
| Light shape | Circular pool | Rectangular, matching crosswalk striping |
| Failure mode | Total loss on fixture failure | Graceful degradation — lose 2 of 20, still 90% coverage |
| Glare | One bright source requires cutoff shield | Many low-output sources, no single bright point |
| Wind load | One large housing | Distributed small emitters, lower total sail area |
| Vertical illuminance | Poor if straight-down; requires tilt | Inherent from angled throw |
| Replacement | Swap entire fixture | Swap individual emitter modules |
| Cost | $300-600 for roadway-rated fixture | TBD — commodity LED emitters are cheap, custom array housing adds cost |
| Precision | Limited by single beam pattern | Each emitter independently aimable |

**Design considerations for array configuration:**

- Individual emitters: 3-5W each, 15-25° beam, 3000K or 4000K, IP65+ rated
- Total array output equivalent to single-fixture spec (4,000-5,000 lumens total)
- Array mounted on a single arm bracket with individual emitter aim adjustment
- Controller drives entire array from single activation signal
- Each emitter module field-replaceable without tools or replacing the array housing

**Vertical coverage on wide roads**: A single array on a pole 25ft ahead and 20ft high lights a pedestrian's full body at the near edge of the crosswalk (39° angle) but only legs-to-waist at 50ft (22°) and knees at 70ft (16°). On a 4-5 lane road, a single-side array cannot illuminate a pedestrian's upper body at the far edge. Solutions:

1. **Two-sided installation** (already specified for 4+ lane roads): Each side's array covers its near half. The pedestrian is always within ~30ft of at least one array regardless of position in the crosswalk.
2. **Split aim within the array**: Not all emitters aim at the ground plane. Divide the array into zones — lower emitters aimed at the pavement (horizontal illuminance, crosswalk visibility), upper emitters aimed at 1.5m height at mid-crossing and far edge (vertical illuminance on pedestrian's torso and face). This provides upper-body illumination across the full crossing width even from one side.
3. **Both**: Two-sided installation with split-aim arrays provides redundant full-body coverage. Each array's high-aim emitters cover the far half that the other array's low-aim emitters miss.

**Photometric modeling note**: The angled throw from 20-30ft offset changes the illuminance calculation significantly from the straight-down model in the photometric verification (audit/photometric-verification.md). The inverse-square-law distance is longer (hypotenuse, not just height), but the angle of incidence creates far better vertical illuminance at the near edge. Modeling must verify coverage across the full crossing width at both ground level and 1.5m height, not just at the near edge. This is the critical modeling task for array design.

### Enhanced Options
- **Retroreflective crosswalk markings**: Cheap force multiplier — pop hard under the directed beam array
- **Framing projector**: Theatrical-grade, projects exact rectangle matching crosswalk striping. Higher cost but precision is unmatched. The LED array approach achieves a similar result with commodity hardware.
- **Ground-projected warning**: "STOP" or warning symbol on approach lane surface

## Electrical Design

### Power Architecture
- **Bus**: 48V DC (emerging standard for distributed solar/battery, smaller wire gauge, less loss)
- **Storage**: Lithium iron phosphate (LiFePO4) — long cycle life, stable in TN heat, no thermal runaway
- **Sizing**: 3x current load for future expandability
- **Solar**: Panel sized for worst-case winter (Nashville: ~3.5 peak sun hours December)
- **Charge controller**: MPPT, 48V compatible

### Activation Circuit
- **Input**: Existing RRFB push-button or passive IR/radar detection
- **Controller**: Onboard microcontroller (embedded Linux or similar)
- **Timer**: 15-20 second hold, software-configurable
- **Clearing detection**: Radar or IR confirms crossing is clear before ramp-down
- **Failsafe**: If comms/controller fail, reverts to basic push-button + fixed timer relay

### Grid Readiness
- Bidirectional inverter-ready for future grid tie
- Conduit stub for future hardwire (sleeve it at install, costs nothing)
- Hybrid solar/grid is where municipal infrastructure is heading

## Communications

- **Data backhaul**: Cellular or LoRaWAN (Nashville has municipal LoRa infrastructure)
- **Protocol**: NTCIP-compliant where possible (standard traffic infrastructure comms)
- **Conduit**: 2-inch with pull string for future fiber/ethernet
- **Data captured**:
  - Activation events (timestamp, duration, source)
  - Battery state, solar production
  - Fault alerts
  - Pedestrian demand data (crossing volume by time of day)
  - Near-miss detection via radar (vehicles that don't slow on activation)

## Environmental Durability

### Nashville Climate Design Conditions

- **Temperature range**: -20°F to 110°F (-29°C to 43°C). Nashville records: -17°F (Jan 1985) and 109°F (Jun 2012). Design range adds margin beyond recorded extremes. LiFePO4 chemistry handles this without active thermal management — unlike NMC lithium cells. Controller and LED driver must be rated for full range.
- **Humidity**: Nashville averages ~70% relative humidity annually (monthly range ~51-78%, highest in winter). All electronics in sealed NEMA 4X enclosures. Conformal coating on circuit boards. Desiccant packs in controller enclosure.
- **Ice storms**: Middle Tennessee experiences significant ice events roughly every few years, with minor icing more frequent. ASCE 7-22 ice loading for Nashville (~0.5-0.75 inch radial ice) adds ~5 lb/sq ft to exposed surfaces. Mounting hardware must accommodate this load. Panel tilt (30-35°) helps shed ice. Fixture lens is warm during operation — ice clears on activation.
- **Wind**: ASCE 7 basic wind speed for Nashville is 115 mph (Risk Category II). Pole and mounting arm must be designed for this. Solar panel is the largest wind sail — flush-mount or low-profile reduces effective area.
- **Tornado**: Central TN is in tornado alley. Breakaway pole design (standard for roadside infrastructure) limits damage — system is replaceable, not hardened against direct tornado strike. This is consistent with how RRFBs and traffic signals are treated.
- **UV degradation**: Solar panel frames are anodized aluminum (inherently UV stable). Fixture housing is die-cast aluminum with powder coat. Polycarbonate lens must be UV-stabilized — specify UV-resistant grade or glass lens.

### Surge Protection

Nashville averages 50-60 thunderstorm days per year. Solar systems on poles are lightning targets.

- **Panel side**: Metal oxide varistor (MOV) surge suppressor at panel junction box, rated for 48V DC
- **Controller side**: Transient voltage suppressor (TVS) diodes on all signal and power inputs
- **Ground**: Equipment grounding conductor from pole to ground rod per NEC 250. Pole itself provides path but dedicated ground rod is cheap insurance.
- **Fusing**: Inline fuses on battery and panel circuits — isolate faulted components without taking down entire system
- **Cost**: Surge protection adds ~$50-100 to BOM. Not optional in Nashville.

### Dimming Protocol

The time-of-night intelligence requires controllable LED output:

- **Protocol**: 0-10V dimming (simplest, most robust for outdoor single-fixture control) or PWM via microcontroller GPIO
- **Levels**: Full (100%), reduced (40-60% for dusk/dawn), standby (0% — off between activations)
- **Ramp**: 0.5 second ramp-up to full output on activation (instant-on is disorienting to drivers; half-second ramp approximates theatrical "bump" — fast enough to be immediate, slow enough to not startle)
- **LED driver**: Constant-current driver with dimming input, 48V DC compatible, rated for outdoor temperature range

## Detection Options

| Method | Pros | Cons |
|--------|------|------|
| Push-button (existing) | Cheapest, already installed | Compliance problem — many don't use it |
| Passive IR | Auto-triggers, no user action | Limited range, weather sensitive |
| Radar | Auto-triggers, all-weather, speed data | Higher cost, more complex install |
| PIR + radar | Redundant detection, most robust | Most expensive |

Recommendation: Radar primary (also captures vehicle speed data for near-miss detection), push-button as manual override.

## Mounting

- Slotted arm mount (swap fixture without replacing arm)
- Tool-free fixture access for maintenance
- Conduit capacity for future additions

## Time-of-Night Intelligence

- Full intensity: sunset to sunrise
- Reduced intensity: dusk/dawn when ambient light is higher
- Extends battery life, reduces light pollution during partial-dark hours

## Maintenance Lifecycle

### Component Lifespan

| Component | Expected Life | Replacement Trigger | Est. Replacement Cost |
|-----------|--------------|--------------------|-----------------------|
| LED fixture | 50,000-100,000 hrs (L70) | Lumen depreciation below 70% of initial output | $300-600 |
| LiFePO4 battery | 3,000-5,000 cycles | Capacity below 80% of rated Ah | $400-800 |
| Solar panel | 25-30 years | Output below 80% of rated watts | $150-300 |
| MPPT charge controller | 10-15 years | Failure or efficiency drop | $100-200 |
| Microcontroller | 10-15 years | Firmware no longer updatable or hardware failure | $100-200 |
| Radar sensor | 10+ years | Detection reliability drops | $200-400 |

### Practical Lifespan Estimates

**LED fixture**: At 50W and 20 activations/night averaging 20 seconds each, the fixture runs ~6-7 minutes/night at full output, plus dusk/dawn reduced output. Annual operating hours are extremely low — maybe 200-400 hours/year including dusk/dawn. At that rate, LED L70 life is effectively 100+ years. The fixture housing or lens will fail before the LEDs do.

**Battery**: This is the maintenance-critical component. At 20 activations/night, each drawing 50W for 20 seconds, daily energy consumption is ~0.006 kWh from activation alone. Dusk/dawn ambient mode adds more. Realistic daily draw is 0.1-0.3 kWh. A 2.4 kWh bank cycles less than 15% depth of discharge daily. At that shallow cycling, LiFePO4 batteries should last 10-15 years before hitting 80% capacity. **Battery replacement is the primary recurring maintenance cost.**

**Solar panel**: Degradation is ~0.5%/year for monocrystalline. After 25 years, output is still ~87% of rated. Cleaning is the real maintenance task — Nashville tree pollen (March-May) and dust reduce output. Quarterly cleaning recommended, alignable with existing RRFB inspection schedules.

### Maintenance Schedule

| Interval | Task |
|----------|------|
| Quarterly | Visual inspection, solar panel cleaning, verify activation function |
| Annually | Battery state of health check (logged automatically), firmware update if available, verify lux levels at crossing surface |
| 5 years | Replace desiccant packs in controller enclosure, inspect all connections and surge protection devices |
| 10-15 years | Battery replacement (primary recurring cost) |
| As needed | Fixture lens replacement if UV-degraded or damaged, radar recalibration |

### Maintenance Integration

These units should be on the same inspection cycle as the RRFB they augment. TDOT and Nashville already inspect RRFBs — adding "verify illumination activation" to the existing checklist is a single line item, not a new maintenance program. Remote monitoring via cellular/LoRa backhaul flags faults before they require a truck roll.

## Safety and Human Factors

### Liability — The Raised Expectation Question

The most common objection to activated crosswalk lighting: "If we install it and it fails, are we more liable than if we never installed it?"

This concern is real but well-addressed in traffic engineering case law:

- **Sovereign immunity** protects TDOT and Nashville from most tort claims for discretionary design decisions. Installing a safety improvement is a discretionary act.
- **The duty to maintain** does apply — once installed, the agency has an obligation to keep it functional. This is no different from the obligation to maintain the RRFB itself, the crosswalk markings, or the sign.
- **The alternative is worse**: *not* installing illumination at a crossing where TDOT's own memo says lighting "shall" be included creates a clearer liability exposure than installing it and having it occasionally fail.
- **Failsafe design directly addresses this**: the mechanical timer relay means even total controller failure still provides basic illumination on push-button activation. The system degrades gracefully rather than going dark silently.
- **Data logging is protective**: timestamped activation records demonstrate the system was functioning. If a crash occurs, the log shows whether the system activated or not — this is better legal footing than having no system and no data.

**Net assessment**: The liability risk of installing and maintaining coordinated illumination is lower than the liability risk of not installing it at locations where the existing "shall" mandate applies.

### Driver Behavior

- **Positive contrast**: The narrow beam creates a bright pool on the crossing surface. The pedestrian appears as a dark figure against a bright background (positive contrast). This is the same visual principle as theatrical stage lighting — the eye is drawn to the lit area and immediately identifies objects within it.
- **Activation as cue**: The sudden appearance of a lit crossing zone is itself an alerting stimulus, reinforcing the RRFB flash. Drivers get two signals: flashing beacon (peripheral vision) and illuminated crossing (direct ahead). Different sensory channels.
- **Glare elimination**: The cutoff fixture means drivers never see the light source — they see the result (lit pavement, lit pedestrian). This is the key design decision that avoids the historical objection to crosswalk lighting.
- **0.5s ramp-up**: Prevents startle response. The light appears quickly but not instantaneously — drivers perceive it as "the crossing lit up" rather than "a flash in my eyes."
- **Adaptation concern**: On corridors with many RRFBs (e.g., Nolensville Pike), drivers could become habituated. The illumination system helps here — even a habituated driver who ignores the beacon flash will see a bright pool of light appear in the roadway ahead. Harder to ignore than flashing yellow alone.

### Pedestrian Behavior

- **False security risk**: Could a pedestrian assume that because the crossing is lit, drivers will stop? This is the same concern raised about RRFBs themselves — and the data shows RRFBs increase yielding rates from ~10-20% to 70-90% without measurably increasing risky pedestrian behavior.
- **Visibility is not protection**: The illumination makes the pedestrian visible. It does not make them invulnerable. But the alternative — an invisible pedestrian in a dark crossing — is strictly worse.
- **Passive detection benefit**: Radar-triggered activation means the system works for pedestrians who don't use the push-button. These are disproportionately the same population at highest risk (impaired, elderly, distracted, unfamiliar with the crossing).

### Emergency Vehicle Interaction

- **No conflict**: The illumination system does not affect signal timing, traffic control, or right-of-way. It lights a crossing surface. Emergency vehicles equipped with optical preemption (Opticom/GPS) interact with traffic signals, not with RRFB/lighting systems.
- **Potential benefit**: If an emergency occurs at or near a crossing, an activated illumination system improves scene visibility for responding units.
- **No preemption needed**: The system activates on pedestrian presence, not on traffic control logic. There is no scenario where an emergency vehicle needs the crosswalk light to turn off — it's not a signal.

## BOM Estimate (per crossing, solar retrofit)

| Component | Est. Cost |
|-----------|-----------|
| LED narrow-beam fixture (roadway-rated) | $300-600 |
| Solar panel (100-200W) | $150-300 |
| LiFePO4 battery bank (48V, 50Ah) | $400-800 |
| MPPT charge controller | $100-200 |
| Microcontroller + enclosure | $100-200 |
| Timer relay (failsafe backup) | $30-50 |
| Mounting hardware + shield | $100-200 |
| Wiring, connectors, conduit stub | $50-100 |
| **Hardware subtotal** | **$1,230-2,450** |
| Installation labor (1-2 electricians, 1 day) | $800-1,500 |
| **Total per crossing (single fixture, 2-lane road)** | **$2,030-3,950** |
| Additional fixture for multi-lane (4+ lane) crossing | $300-600 |
| **Total per crossing (multi-fixture, 4+ lane road)** | **$2,330-4,550** |

## Compliance Checklist

- [x] ANSI/IES RP-8-25 — 20 lux vertical at 1.5m, 14 lux horizontal *(met by optical design: 4-5K lumen narrow beam at 20-25ft mounting height)*
- [x] MUTCD 11th Edition Chapter 4L — RRFB device standards *(system augments, does not modify RRFB operation)*
- [ ] TDOT Lighting Design Manual — mandatory lighting on mid-block crossings *(requires TDOT review of fixture and placement)*
- [ ] Nashville Streets and Pathways Lighting Manual *(requires NDOT review for local installations)*
- [ ] TDOT/NDOT approval for state route installations *(field verification required per corridor)*
- [x] NES coordination (if hardwired; solar largely exempt) *(solar-first design avoids NES right-of-way requirements)*
- [x] ADA/PROWAG — pushbutton height, APS integration *(uses existing RRFB pushbutton; no new pedestrian interface)*
- [ ] NFPA 70 (NEC) — electrical installation *(field verification at install)*
- [x] IES/IESNA dark sky compliance (narrow beam minimizes upward spill) *(cutoff fixture with house-side shield, 15-25° beam)*

## TDOT "Shall" Language — Existing and Proposed

### What Already Exists

TDOT Traffic Operations Memo 2022 requires that all roundabouts and mid-block pedestrian crossings **shall** include lighting design. The mandate for lighting is established. What the memo does not address is how that lighting should function at RRFB-equipped crossings — specifically, coordinated activation, beam geometry, illuminance targets at the crossing surface, and clearing integration.

The result is that the "shall" is satisfied by a standard cobra-head streetlight near the crossing — continuous, unfocused illumination that does not respond to the RRFB activation and may not deliver adequate vertical illuminance on the pedestrian.

### Proposed Supplemental Language

The following is proposed as supplemental specification to the existing TDOT lighting design requirement for RRFB-equipped crossings. It is written to be adoptable by TDOT as a Traffic Operations Memo addendum, referenced by local agencies (e.g., Nashville NDOT), and structured for potential adoption by ITE at the national level.

> **Coordinated Illumination at RRFB-Equipped Crosswalks — Supplemental Specification**
>
> Where a Rectangular Rapid Flash Beacon (RRFB) is installed at a midblock or uncontrolled crosswalk, the lighting design required by [Traffic Operations Memo 2022 / TDOT Lighting Design Manual] **shall** include a dedicated crosswalk luminaire meeting the following:
>
> 1. **Illuminance**: Minimum 20 lux vertical at 1.5 meters above the crossing surface and 14 lux average maintained horizontal illuminance across the marked crosswalk, per ANSI/IES RP-8-25 and consistent with AASHTO Roadway Lighting Design Guide recommendations.
>
> 2. **Coordinated activation**: The crosswalk luminaire **shall** activate simultaneously with the RRFB upon any triggering event (push-button, passive detection, or both) and **shall** remain at full output for the duration of the pedestrian crossing interval.
>
> 3. **Clearing hold**: Following the crossing interval, the luminaire **shall** maintain illumination for a clearing buffer of no less than 5 seconds, or until passive detection confirms the crossing is clear, whichever is longer.
>
> 4. **Optical control**: The luminaire **shall** be a cutoff-rated fixture with a maximum beam spread of 25°. A house-side shield or equivalent optical control **shall** prevent direct light above 80° from nadir toward approaching traffic. Light distribution **shall** be substantially confined to the crosswalk surface.
>
> 5. **Power and resilience**: Solar-powered systems **shall** be acceptable. Where solar is used, battery storage **shall** be sized to maintain full operation through a minimum of 72 hours without solar charge at December insolation levels for the installation latitude. Conduit **shall** be stubbed for future hardwire connection regardless of initial power source.
>
> 6. **Failsafe**: If the primary controller fails, the system **shall** revert to a fixed-timer relay mode providing illumination for a minimum of 20 seconds upon push-button activation.
>
> 7. **Data capture**: Systems **shall** log all activation events with timestamps. Where radar or equivalent detection is installed, systems **should** log pedestrian demand volume and vehicle approach speed for yielding compliance analysis.
>
> **Applicability**: This specification applies to all new RRFB installations and **should** be applied to existing RRFB locations as part of scheduled maintenance or retrofit programs. Existing continuous roadway lighting at or near the crossing does not satisfy this coordinated illumination requirement.

### Notes on Framing

- The language anchors to TDOT's existing "shall" — it supplements, not replaces. This avoids the political problem of proposing a new mandate.
- Numbered requirements are specific enough to be enforceable but leave fixture vendor and detection method to the designer.
- "Should" is used deliberately for data capture and retrofit applicability — these are harder to mandate immediately but establish direction.
- The structure mirrors MUTCD and TDOT memo formatting so it reads as native to the standards ecosystem.
- This language is written to be portable: TDOT can adopt it as a memo addendum, ITE could reference it in recommended practice, and local agencies can incorporate it into their own manuals.
