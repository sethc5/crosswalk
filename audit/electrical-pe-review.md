# Electrical PE Review Checklist

Items requiring review by a licensed Professional Engineer (Electrical) before procurement or installation. Reference NEC edition: 2023 (Nashville adoption effective July 15, 2025).

## NEC Article 690 — Solar Photovoltaic Systems

- [ ] **690.12 Rapid Shutdown**: Controlled conductors within 1-foot boundary of PV array reduced to 80V within 30 seconds of initiating rapid shutdown. Verify charge controller serves as rapid shutdown initiator for standalone pole-mounted system. Does the selected charge controller meet 690.12 requirements?
- [ ] **690.8 Circuit Sizing**: PV source circuit conductors sized per 690.8(A). Maximum current = Isc × 1.25. Verify wire gauge for distance from panel to charge controller.
- [ ] **690.9 Overcurrent Protection**: Overcurrent device rating for PV source circuit. Fuse or breaker sizing.
- [ ] **690.13 PV Disconnecting Means**: Disconnecting means for PV source circuit accessible and clearly labeled. Location on pole or enclosure.
- [ ] **690.41 Grounding**: System grounding configuration (ungrounded or grounded). Equipment grounding per 690.43.
- [ ] **690.47 Grounding Electrode System**: Ground rod at pole. Bonding to grounding electrode system per 250.

## NEC Article 706 — Energy Storage Systems

- [ ] **706.7 Disconnecting Means**: ESS disconnecting means rated for maximum circuit current and voltage. Accessible, lockable, clearly labeled.
- [ ] **706.10 Location**: Battery installation location meets clearance and ventilation requirements. Verify NEMA 4X enclosure rating is adequate for LiFePO4 chemistry.
- [ ] **706.30 Overcurrent Protection**: Overcurrent device sizing for battery circuit. Coordination with charge controller protection.
- [ ] **706.31 System Capacity**: Verify battery capacity labeling requirements. Nameplate with kWh rating, chemistry, voltage, and manufacturer.

## NEC Article 250 — Grounding and Bonding

- [ ] **250.52 Grounding Electrodes**: Driven ground rod per 250.52(A)(5). Length and installation method. Supplemental electrode if resistance >25 ohms per 250.53(A).
- [ ] **250.64 Grounding Electrode Conductor**: Size per Table 250.66 for the PV system.
- [ ] **250.110 Equipment Grounding**: All exposed non-current-carrying metal parts grounded. Pole, fixture housing, enclosure, mounting hardware.

## NEC Article 300 — Wiring Methods

- [ ] **300.5 Underground Installations**: If any underground conduit run (e.g., conduit stub for future hardwire), depth per Table 300.5.
- [ ] **300.9 Raceways in Wet Locations**: Above-grade raceways suitable for wet locations. Interior drainage per 300.9.
- [ ] **Conductor type**: Outdoor, wet-location rated insulation (THWN-2, XHHW-2, or equivalent) for all exposed wiring.

## NEC Article 725 — Class 1/2/3 Circuits

- [ ] **Detection wiring classification**: Radar sensor and push-button interface wiring — Class 1, 2, or 3? Power-limited or non-power-limited? Determines wiring method and separation requirements.
- [ ] **725.136 Separation**: If Class 2/3 circuits in same enclosure as power circuits, separation per 725.136.

## Surge Protection

- [ ] MOV surge suppressor at solar panel junction box — rated for 48V DC, verify kA rating adequate for Nashville lightning exposure
- [ ] TVS diodes on controller signal inputs — verify clamping voltage compatible with controller input range
- [ ] Fusing coordination — verify fuse ratings on PV circuit, battery circuit, and load circuit are coordinated to isolate faults without nuisance tripping

## LED Driver

- [ ] Constant-current driver rated for outdoor temperature range (-10°F to 105°F / -23°C to 41°C)
- [ ] 48V DC input compatible
- [ ] 0-10V or PWM dimming input for time-of-night and ramp-up control
- [ ] UL 8750 listed as component of luminaire assembly

## UL Listings Required

- [ ] LED luminaire assembly: UL 1598 + UL 8750, wet location listed
- [ ] Solar panel mounting system: UL 2703
- [ ] Energy storage system (battery + charge controller): UL 9540
- [ ] All components: UL or equivalent NRTL listing suitable for NEC AHJ approval

## System-Level

- [ ] Total system one-line diagram with all circuit breakers, fuses, disconnects, and grounding
- [ ] Arc flash hazard analysis (48V DC is below typical arc flash threshold, but verify for battery short-circuit current)
- [ ] Labeling plan per NEC requirements (PV, ESS, disconnect, grounding)
- [ ] Conduit fill calculation for 2-inch conduit stub (future wiring capacity)
