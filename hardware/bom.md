# Bill of Materials — Per Crossing (Solar Retrofit)

Extracted from system design spec. Costs are 2026 estimates for single-unit procurement; volume pricing would reduce.

## LED Fixture

| Option | Beam | Lumens | Wattage | Est. Cost | Notes |
|--------|------|--------|---------|-----------|-------|
| TAPCO SafeWalk Crosswalk Illuminator | 20° | 5,000 | 50W | $400-600 | Purpose-built for crosswalk activation; mounts on existing RRFB pole |
| Lithonia DSX0 LED Area Light (narrow distribution) | 15-25° | 4,000-6,000 | 40-60W | $300-500 | Roadway-rated, cutoff, multiple distributions available |
| RAB Lighting ALED (narrow flood) | 20° | 4,500 | 50W | $250-400 | Compact, tool-free access, house-side shield option |
| Framing projector (theatrical) | Custom rectangle | Variable | 50-100W | $800-1,500 | Projects exact crosswalk rectangle; highest precision, highest cost |

**Selection criteria**: Cutoff rating, narrow beam (15-25°), house-side shield available, roadway/wet-rated (IP65+), tool-free fixture access, slotted arm compatible.

## Solar + Storage

| Component | Specification | Est. Cost |
|-----------|--------------|-----------|
| Solar panel | 100-200W monocrystalline, aluminum frame | $150-300 |
| LiFePO4 battery bank | 48V, 50Ah (2.4 kWh), BMS integrated | $400-800 |
| MPPT charge controller | 48V compatible, 10-20A | $100-200 |

**Sizing note**: Panel and battery sized for Nashville worst-case winter (December ~3.5 peak sun hours). 50Ah at 48V provides ~3 days autonomy at 50W draw with 15-20 second activation cycles.

## Controls + Detection

| Component | Specification | Est. Cost |
|-----------|--------------|-----------|
| Radar sensor (primary detection) | Vehicle + pedestrian, speed capture | $200-400 |
| Microcontroller + enclosure | Embedded Linux, NEMA 4X enclosure | $100-200 |
| Timer relay (failsafe) | Mechanical backup, fixed 20s hold | $30-50 |
| Cellular/LoRa modem | Data backhaul for activation logs | $50-150 |

## Mounting + Wiring

| Component | Specification | Est. Cost |
|-----------|--------------|-----------|
| Slotted arm mount | Fits existing RRFB pole or new pole | $50-100 |
| House-side shield/visor | Glare control for approach traffic | $30-50 |
| Wiring, connectors, conduit stub | 2" conduit with pull string for future | $50-100 |

## Summary

| | Low | High |
|---|-----|------|
| Hardware subtotal (single fixture) | $1,230 | $2,450 |
| Installation labor (1-2 electricians, 1 day) | $800 | $1,500 |
| **Total per crossing (2-lane, single fixture)** | **$2,030** | **$3,950** |
| Additional fixture for 4+ lane crossing | $300 | $600 |
| **Total per crossing (4+ lane, multi-fixture)** | **$2,330** | **$4,550** |

Note: Most Nashville target corridors (Nolensville, Murfreesboro, Gallatin Pikes) are 4-5 lanes and require multi-fixture configurations. The $2,000-4,500 range used elsewhere in this package reflects the full spectrum from 2-lane single-fixture to 4+ lane multi-fixture installations.
