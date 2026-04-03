# System Design Specification

## Overview

Activated narrow-beam overhead LED coordinated with existing RRFB installation. Solar-powered, push-button or passive detection triggered, 15-20 second hold with pedestrian clearing detection.

## Optical Design

### Primary Fixture
- **Type**: Narrow-beam LED spot, 15-25° beam spread
- **Color temp**: 3000-4000K (neutral to warm white)
- **Output**: 4,000-5,000 lumens (~50W LED equivalent)
- **Target**: 20 lux vertical at 1.5m above crossing surface (IES RP-8)
- **Mounting**: Pole-mounted at 20-25ft, approach side of crossing
- **Optics**: House-side shield, cutoff fixture to prevent driver glare
- **Aim**: Straight down at crossing centerline

### Why Narrow Beam
- Eliminates glare objection (standard pushback on crosswalk lighting)
- Defined pool of light on crossing surface only
- Pedestrian lit from above — driver sees illuminated person, not light source
- Minimal light pollution / spill into adjacent properties

### Enhanced Options
- **Retroreflective crosswalk markings**: Cheap force multiplier — pop hard under the narrow beam
- **Framing projector**: Theatrical-grade, projects exact rectangle matching crosswalk striping. Higher cost but precision is unmatched.
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
| **Total per crossing** | **$2,030-3,950** |

## Compliance Checklist

- [ ] ANSI/IES RP-8-22 — 20 lux vertical at 1.5m, 14 lux horizontal
- [ ] MUTCD 11th Edition Chapter 4L — RRFB device standards
- [ ] TDOT Lighting Design Manual — mandatory lighting on mid-block crossings
- [ ] Nashville Streets and Pathways Lighting Manual
- [ ] TDOT/NDOT approval for state route installations
- [ ] NES coordination (if hardwired; solar largely exempt)
- [ ] ADA/PROWAG — pushbutton height, APS integration
- [ ] NFPA 70 (NEC) — electrical installation
- [ ] IES/IESNA dark sky compliance (narrow beam minimizes upward spill)
