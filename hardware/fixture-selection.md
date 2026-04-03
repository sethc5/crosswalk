# Fixture Selection Notes

## Requirements

From the system design spec — the fixture must:

1. **Narrow beam**: 15-25° spread to confine light pool to crossing surface
2. **Cutoff rated**: No light above 90° from nadir (prevents driver glare)
3. **House-side shield**: Blocks spill toward approaching traffic
4. **Roadway rated**: IP65+ wet location, vibration resistant
5. **Mounting**: Slotted arm compatible, tool-free fixture access
6. **Color temperature**: 4000K recommended for mesopic pedestrian detection performance (see spec CCT justification); 3000K fallback if dark sky variance not granted. Fixture should support field-swappable LED module or tunable-white driver for either CCT.
7. **Output**: 4,000-5,000 lumens minimum to hit 20 lux vertical at 20-25ft mounting height

## Candidates

### TAPCO SafeWalk Crosswalk Illuminator

- **Status**: Only purpose-built crosswalk activation luminaire on the market
- **Pro**: Designed for this exact use case; mounts on RRFB pole assembly
- **Con**: Not widely specified; limited independent photometric data published; single-source vendor risk
- **Action**: Request IES photometric file (.ies) from TAPCO for modeling

### Standard Roadway LED (Lithonia DSX0, RAB ALED, similar)

- **Status**: Mature product lines with published photometrics
- **Pro**: Multiple vendors, competitive pricing, field-proven, full IES data available
- **Con**: Requires careful distribution selection — most roadway fixtures are wider than 25°; need Type I or narrow flood
- **Action**: Pull .ies files for narrow distributions; model in AGi32 or similar to verify 20 lux at mounting height

### Framing Projector (ETC Source Four, Altman PHX, similar)

- **Status**: Theatrical lighting adapted for architectural/infrastructure use
- **Pro**: Projects exact crosswalk rectangle with hard edges; maximum visual impact
- **Con**: Higher cost ($800-1,500), less weather-hardened, more complex aiming, not standard in traffic infrastructure
- **Action**: Worth evaluating for a demonstration/prototype unit; probably not the volume spec

## Photometric Modeling Needed

Before final fixture selection, model the following in lighting design software:

- Verify 20 lux vertical at 1.5m above surface with selected fixture at 20-25ft mounting height
- Confirm light spill does not exceed crosswalk boundaries by more than 1 lane width
- Validate cutoff angle eliminates direct glare for drivers at 200ft+ approach distance
- Check uniformity ratio across crossing width (IES RP-8 recommends max 4:1)
