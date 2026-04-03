# Buy America Compliance Matrix

Required only if federal highway funds (HSIP, SS4A, RAISE, PROTECT) are used. Per 23 USC 313 / 23 CFR 635.410 and Build America, Buy America Act (BABA).

## Applicability

- **Applies?**: Only if federal highway funds used for procurement
- **Effective dates**: Final assembly in US required as of Oct 1, 2025. Manufactured products >55% domestic components by cost as of Oct 1, 2026.
- **Waiver process**: FHWA can grant project-specific waivers if domestic product is unavailable, unreasonable cost, or inconsistent with public interest. Waiver requests go through the state DOT to FHWA Division.

## Component-by-Component Compliance

| Component | Category | Domestic Sourcing Status | Compliance Notes |
|-----------|----------|-------------------------|------------------|
| LED luminaire (roadway-rated) | Manufactured product | [ ] Verified  [ ] Needs check | Lithonia (Acuity Brands — US manufactured), RAB (US assembled). TAPCO (US manufactured). Verify specific model. |
| Solar panel (100-200W mono) | Manufactured product | [ ] Verified  [ ] Needs check | Many panels assembled in US from imported cells. Verify final assembly location AND component origin percentage. US-made panels exist (Mission Solar, Silfab, First Solar thin-film) but may not make the size/type needed. |
| LiFePO4 battery (48V, 50Ah) | Manufactured product | [ ] Verified  [ ] Needs check | Most LiFePO4 cells manufactured in China. US-assembled battery packs exist (e.g., Battle Born, Relion, SimpliPhi). Verify cell origin vs pack assembly — BABA may require cell-level domestic content after Oct 2026. **Highest risk component for Buy America.** |
| MPPT charge controller | Manufactured product | [ ] Verified  [ ] Needs check | Morningstar (US-designed, verify assembly location), Midnite Solar (US). Many MPPT controllers manufactured overseas. |
| Microcontroller + enclosure | Manufactured product | [ ] Verified  [ ] Needs check | NEMA 4X enclosures widely available from US manufacturers (Hoffman, Saginaw, Hammond). Microcontroller boards (Raspberry Pi, etc.) typically manufactured overseas. Custom controller assembly in US would comply. |
| Timer relay (failsafe) | Manufactured product | [ ] Verified  [ ] Needs check | Widely available from US manufacturers (Intermatic, Ametek, Leviton). Low risk. |
| Radar sensor | Manufactured product | [ ] Verified  [ ] Needs check | Houston Radar (US manufactured). Some models from European/Asian manufacturers. Verify specific model. |
| Cellular/LoRa modem | Manufactured product | [ ] Verified  [ ] Needs check | MultiTech (US manufactured LoRa gateways). Cellular modems vary. |
| Pole (if new) | Steel/iron product | [ ] Verified  [ ] Needs check | Steel poles domestically manufactured (Valmont, Hapco, Shakespeare). Steel/iron products have stricter BA requirements — must be melted and manufactured in US. Low risk for standard poles. |
| Mounting arm + hardware | Steel/iron product | [ ] Verified  [ ] Needs check | Standard galvanized steel arms — widely US-manufactured. Low risk. |
| Wiring, connectors, conduit | Manufactured product | [ ] Verified  [ ] Needs check | Southwire (US), generic conduit widely US-made. Low risk. |

## Risk Assessment

| Risk Level | Components |
|------------|-----------|
| **High** | LiFePO4 battery (cell-level content), solar panel (cell vs assembly), microcontroller |
| **Medium** | MPPT charge controller, radar sensor, cellular/LoRa modem |
| **Low** | LED luminaire, pole, mounting hardware, timer relay, wiring, conduit, enclosure |

## Recommended Approach

1. **Spec procurement as "Buy America compliant" from the start** — don't select components and then check compliance afterward
2. **Get written manufacturer certifications** of domestic content percentage for each component before purchase order
3. **LiFePO4 battery is the highest-risk item** — may need a FHWA waiver or selection of a US-manufactured pack with domestic cells (if available at the required capacity/voltage)
4. **For the pilot**: If the pilot is funded through university research dollars (UTC, NSF) rather than federal highway funds, Buy America does not apply. This may be another reason to structure the pilot as a research project rather than an infrastructure project.
