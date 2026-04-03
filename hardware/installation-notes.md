# Installation Notes

## Typical Retrofit Sequence

Assumes existing RRFB pole and push-button already installed.

1. **Site survey**: Confirm pole capacity for additional fixture + solar panel weight. Verify mounting height (20-25ft target). Document existing conduit and wiring.

2. **Mounting**: Install slotted arm mount on existing pole (approach side of crossing). If pole capacity is insufficient, new dedicated pole on approach side.

3. **Fixture**: Mount LED fixture on slotted arm. Aim straight down at crossing centerline. Install house-side shield.

4. **Solar**: Mount panel on pole above fixture. Orient south (Nashville ~36°N latitude, optimal tilt ~30-35°). Confirm no shading from adjacent structures or trees.

5. **Battery + controller**: Mount NEMA 4X enclosure at pole base or on pole. Install LiFePO4 battery bank, MPPT charge controller, microcontroller. Wire solar panel → charge controller → battery → fixture.

6. **Detection tie-in**: Connect to existing RRFB push-button circuit as activation trigger. If adding radar, mount radar sensor on pole at 10-15ft facing crossing zone.

7. **Failsafe relay**: Wire mechanical timer relay in parallel with microcontroller output. If controller fails, relay provides fixed 20-second hold on push-button activation.

8. **Conduit stub**: Install 2" conduit with pull string from enclosure to nearest accessible point for future hardwire or fiber.

9. **Commissioning**: Verify activation timing, clearing detection (if radar equipped), light levels at crossing surface, data backhaul.

## Pole Loading

Key consideration for retrofit: existing RRFB poles may not be rated for additional wind load from solar panel + fixture. Check:

- Pole material and rating (breakaway vs structural)
- Wind load calculation with added fixture area + solar panel
- Foundation adequacy

If pole can't take the load, a separate short pole (15-20ft) on the approach side is an alternative. Adds cost but avoids structural questions.

## Vandalism and Tamper Resistance

Solar panels and batteries on roadside poles are theft/damage targets. Design accordingly:

### Physical Security

- **Battery enclosure**: NEMA 4X steel or aluminum enclosure with tamper-resistant fasteners (Torx pin, pentalobe, or security hex). Mounted at pole base or 8-10ft on pole — low enough for maintenance access, high enough to deter casual tampering.
- **Solar panel**: Stainless steel security bolts on mounting hardware. Panel theft requires tools and a ladder — opportunistic theft is unlikely, but panels on lower poles in high-crime areas should use security fasteners.
- **Fixture**: Mounted at 20-25ft — effectively out of reach. Slotted arm mount uses standard bolts (maintenance priority over security at this height).
- **Controller enclosure**: Same tamper-resistant fasteners as battery enclosure. Padlock hasp as secondary lock option for agencies that prefer keyed access.
- **Conduit**: Metal conduit (not PVC) for the first 8ft above ground to resist impact and cutting.

### Electrical Anti-Tamper

- **Battery disconnect**: If enclosure is opened without disabling a magnetic tamper switch, controller logs the event and sends alert via cellular/LoRa. Does not disable system — just logs and alerts.
- **No exposed terminals**: All connections inside sealed enclosures. No junction boxes at accessible height with live conductors.
- **Fusing**: If someone cuts a wire or shorts a connection, fuses blow and isolate the fault. System logs the event. Prevents fire or damage to other components.

### Replacement vs Hardening

The system is designed to be replaceable, not indestructible. At $2,000-4,000 per crossing, it's cheaper to replace a vandalized unit than to over-engineer hardening. The real protection is:

1. Remote monitoring — know immediately when something fails or is tampered with
2. Commodity components — nothing is custom or hard to source
3. Fast reinstall — 1-day installation means 1-day replacement

This is the same philosophy as RRFB maintenance: keep spares, monitor remotely, replace quickly.

## NES / Utility Coordination

- **Solar-only**: Minimal NES involvement — no utility power connection, no metering, no right-of-way electrical work
- **Future grid tie**: Conduit stub allows later connection; will require NES coordination, meter, and possibly interconnection agreement at that time
- **State routes**: TDOT approval required regardless of power source
