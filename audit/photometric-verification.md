# Photometric Verification

Hand calculations to verify the spec's illuminance claims. These do NOT replace AGi32 modeling with actual .ies files — they confirm the spec is in the right ballpark.

## Claim to Verify

20 lux vertical illuminance at 1.5m above crossing surface, from a 4,000-5,000 lumen fixture at 20-25ft mounting height with 15-25° beam spread.

## Method: Inverse Square Law with Beam Factor

For a narrow-beam downlight aimed straight down, the illuminance at a point on the crossing surface can be estimated using:

```
E = (I × cos(θ)) / d²
```

Where:
- E = illuminance (lux) at the target point
- I = peak luminous intensity (candela) at beam center
- θ = angle from beam axis to target point (0° for directly below)
- d = distance from fixture to target point (meters)

### Step 1: Estimate Peak Candela from Lumens

For a narrow-beam fixture, peak intensity is related to total lumens by the beam solid angle:

```
I_peak = Φ / Ω
```

Where:
- Φ = total luminous flux (lumens)
- Ω = solid angle of the beam cone (steradians)

Solid angle of a cone with half-angle α:
```
Ω = 2π(1 - cos(α))
```

| Beam Spread (full angle) | Half-Angle (α) | Solid Angle (Ω) sr |
|--------------------------|-----------------|---------------------|
| 15° | 7.5° | 0.0538 |
| 20° | 10° | 0.0955 |
| 25° | 12.5° | 0.149 |

Peak candela estimates:

| Lumens | 15° Beam (cd) | 20° Beam (cd) | 25° Beam (cd) |
|--------|---------------|---------------|---------------|
| 4,000 | 74,350 | 41,880 | 26,850 |
| 5,000 | 92,940 | 52,360 | 33,560 |

### Step 2: Calculate Illuminance at Crossing Surface (Directly Below)

Mounting height 20ft = 6.1m, 25ft = 7.6m. For the point directly below the fixture (θ = 0, cos(θ) = 1):

```
E = I / d²
```

| Config | Lumens | Beam | Height | Peak cd | E (lux) |
|--------|--------|------|--------|---------|---------|
| Min spec | 4,000 | 25° | 25ft (7.6m) | 26,850 | **465** |
| Min spec | 4,000 | 25° | 20ft (6.1m) | 26,850 | **722** |
| Mid spec | 4,500 | 20° | 25ft (7.6m) | 47,120 | **816** |
| Max spec | 5,000 | 15° | 25ft (7.6m) | 92,940 | **1,610** |

### Step 3: Reality Check

The peak illuminance numbers are extremely high (465-1,610 lux directly below). The IES RP-8 target is 20 lux vertical at 1.5m above the surface — measured on a vertical plane facing the approaching driver, not on the horizontal ground plane.

**Key distinction**: Vertical illuminance ≠ horizontal illuminance.

For a downlight aimed straight down:
- Horizontal illuminance (on the ground) is maximized directly below
- Vertical illuminance (on a pedestrian facing the driver) is ZERO directly below, because the light is coming from straight above

Vertical illuminance from an overhead downlight peaks at some lateral offset, where the fixture-to-pedestrian angle creates a component on the vertical plane.

### Step 4: Vertical Illuminance Calculation

For a pedestrian at position offset from directly below the fixture, with the fixture at height h:

```
E_v = (I(θ) × cos(α)) / d²
```

Where:
- θ = angle from fixture nadir to pedestrian (the beam angle)
- α = angle between the light ray and the normal to the vertical measurement plane
- d = actual distance from fixture to measurement point (1.5m above ground)

For a fixture at height H (to crossing surface) and a measurement plane at 1.5m above surface:
- Effective height = H - 1.5m
- At lateral offset x from directly below:
  - d = sqrt(x² + (H-1.5)²)
  - θ = arctan(x / (H-1.5))  [angle from nadir]
  - The vertical illuminance component depends on fixture aim and lateral position

**At 25ft (7.6m) mounting, measurement at 1.5m above surface:**
- Effective height above measurement point: 7.6 - 1.5 = 6.1m
- At x = 3m lateral offset (roughly one lane width from below fixture):
  - d = sqrt(9 + 37.2) = sqrt(46.2) = 6.8m
  - θ = arctan(3/6.1) = 26.2° from nadir
  - sin(θ) = 0.441 (component on vertical plane)
  - For a 25° beam fixture, 26.2° is at the beam edge — intensity drops significantly

**This reveals the real design challenge**: A narrow-beam fixture aimed straight down maximizes horizontal illuminance but delivers poor vertical illuminance. The IES RP-8 vertical illuminance target (20 lux at 1.5m) requires either:

1. **Fixture tilt** — aim the fixture slightly off-vertical toward the approaching traffic direction, so the beam center creates a vertical component on the pedestrian
2. **Wider beam than specified** — a 25° beam at 25ft creates a ground spot of ~11ft diameter, but the vertical illuminance is only significant at the beam edges
3. **Multiple fixtures from different angles** — the multi-fixture configuration for wide roads partially addresses this, as fixtures on opposite sides illuminate pedestrians from different lateral angles

### Assessment

**The spec's lumen output (4,000-5,000) is more than adequate for horizontal illuminance.** Even at the widest beam (25°) and highest mounting (25ft), horizontal illuminance directly below is ~465 lux — 33x the IES RP-8 horizontal target of 14 lux.

**Vertical illuminance at 1.5m is the constraint.** A straight-down aim with a narrow beam does not efficiently produce vertical illuminance. The spec should either:

1. Specify a small fixture tilt (5-10° toward approaching traffic) — this would direct the beam center toward the measurement plane and dramatically improve vertical illuminance while still keeping the light source out of the driver's direct line of sight
2. Acknowledge that the IES RP-8 vertical illuminance target is met by the combination of direct and reflected light (the bright crossing surface reflects upward onto the pedestrian)
3. Note that photometric modeling with actual .ies files is required to verify the vertical illuminance target — the hand calc confirms the energy budget is more than sufficient, but the distribution matters

**Recommendation**: Add a note to the spec that fixture aim may require 5-10° tilt from vertical toward approaching traffic, and that photometric modeling must verify vertical illuminance at 1.5m, not just horizontal illuminance at the surface.

## Status

- [x] Hand calculation completed
- [x] Horizontal illuminance: verified far exceeds 14 lux target
- [ ] Vertical illuminance: **requires fixture tilt or modeling — spec should note this**
- [ ] AGi32 modeling with actual .ies files: requires fixture procurement or manufacturer data
