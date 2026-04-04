# Fixture Selection Notes

## Requirements

From the system design spec — the luminaire or luminaire array must:

1. **Narrow beam**: 15-25° spread per emitter to confine light to crossing zone
2. **Cutoff rated**: No direct light above 80° from nadir (prevents driver glare; matches supplemental specification requirement)
3. **Glare control**: House-side shield (single fixture) or inherent low-output-per-emitter glare management (array)
4. **Roadway rated**: IP65+ wet location, vibration resistant
5. **Mounting**: Arm-compatible at 25-30ft. Single fixture: slotted arm, tool-free access. Array: linear bracket with individual emitter aim adjustment.
6. **Color temperature**: 4000K recommended for mesopic pedestrian detection performance (see spec CCT justification); 3000K fallback if dark sky variance not granted. Fixture should support field-swappable LED module or tunable-white driver for either CCT.
7. **Output**: 4,000-5,000 lumens total to hit 20 lux vertical at 25-30ft mounting height with 20-30ft pole offset

## Approach A: Single Fixture

For crossings where the pole is directly above or within 10-15ft of the crosswalk, or for 2-lane roads where a single fixture provides adequate coverage.

### TAPCO SafeWalk Crosswalk Illuminator

- **Status**: Only purpose-built crosswalk activation luminaire on the market
- **Pro**: Designed for this exact use case; mounts on RRFB pole assembly
- **Con**: Not widely specified; limited independent photometric data published; single-source vendor risk
- **Action**: Request IES photometric file (.ies) from TAPCO for modeling

### Standard Roadway LED (Lithonia DSX0, RAB ALED, similar)

- **Status**: Mature product lines with published photometrics
- **Pro**: Multiple vendors, competitive pricing, field-proven, full IES data available
- **Con**: Requires careful distribution selection — most roadway fixtures are wider than 25°; need Type I or narrow flood
- **Action**: Pull .ies files for narrow distributions; model in AGi32 or similar to verify 20 lux at mounting height and offset distance

### Framing Projector (ETC Source Four, Altman PHX, similar)

- **Status**: Theatrical lighting adapted for architectural/infrastructure use
- **Pro**: Projects exact crosswalk rectangle with hard edges; maximum visual impact
- **Con**: Higher cost ($800-1,500), less weather-hardened, more complex aiming, not standard in traffic infrastructure
- **Action**: Worth evaluating for a demonstration/prototype unit; probably not the volume spec

## Approach B: Multi-Emitter Linear Array

Recommended for the typical real-world case: existing RRFB pole 20-30ft ahead of the crosswalk, 4+ lane road. The array configuration shapes the illuminated area to the crosswalk rectangle from an offset position that a single fixture cannot cover.

### Array Design Parameters

- 15-30 individual LED emitters, 3-5W each, 15-25° beam per emitter
- Total output: 4,000-5,000 lumens across the array
- IP65+ per emitter or sealed array housing
- Individual emitter aim adjustment for dual-zone targeting:
  - **Zone A** (lower emitters): aimed at crossing pavement — horizontal illuminance, bright-pool driver cue
  - **Zone B** (upper emitters): aimed at 3-6ft above crossing surface — pedestrian body illumination, vertical illuminance
- Array mounted on single linear bracket, field-replaceable emitter modules

### Array Component Candidates

- **Commodity narrow-beam LED modules**: Cree, Bridgelux, Lumileds — 3-5W modules with integrated optics in the 15-25° range. Widely available, low cost per unit ($5-20 each).
- **Array housing**: Custom bracket or adapted from existing linear LED wallwasher housings. Must be roadway-rated (IP65+, vibration resistant, UV-stable).
- **Estimated array cost**: $200-500 for emitter modules + $100-300 for housing/bracket. Comparable to or less than a single roadway-rated fixture, with superior coverage and graceful degradation.

### Array Advantages

| | Single Fixture | LED Array |
|---|---|---|
| Light shape | Circular pool | Rectangular, matching crosswalk |
| Failure mode | Total loss | Graceful — lose 2 of 20, 90% coverage remains |
| Glare | One bright source, needs shield | Many low-output points, no single bright source |
| Vertical illuminance | Requires tilt or offset | Dual-zone targeting covers full body |
| Replacement | Swap entire fixture | Swap individual emitter modules |
| Coverage on wide roads | ~19ft per FHWA | Adjustable per emitter aim |

## Photometric Modeling Needed

Before final selection (either approach), model the following in AGi32 or equivalent:

- Verify 20 lux vertical at 1.5m above surface across 100% of crosswalk width at 25-30ft mounting height **and** at the actual pole-to-crosswalk offset distance (not just directly below)
- For arrays: model Zone A and Zone B coverage independently, then combined
- Confirm light spill does not exceed crosswalk boundaries by more than 1 lane width
- Validate glare control — no direct source visibility for drivers at 200ft+ approach distance
- Check uniformity ratio across crossing width (IES RP-8-25 max 4:1)
- Model both single-side and two-sided configurations for the target crossing width
