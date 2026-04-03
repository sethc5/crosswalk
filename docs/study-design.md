# Research Study Design

Coordinated Crosswalk Illumination at RRFB-Equipped Midblock Crossings: A Before-After Field Study with Comparison Group

## Research Questions

1. Does coordinated activated illumination at RRFB-equipped crosswalks increase nighttime driver yielding rates compared to RRFB-only crosswalks?
2. Does coordinated illumination reduce vehicle approach speeds during active crossing events?
3. Does coordinated illumination reduce near-miss frequency (defined as vehicles failing to decelerate below a threshold speed during active crossing events)?
4. What is the interaction between illumination and pedestrian push-button compliance — does passive radar activation change the proportion of crossings that trigger the system compared to push-button-only RRFB operation?

## Hypotheses

- **H1**: Nighttime driver yielding rate at treatment crossings will be significantly higher than at matched control crossings after illumination retrofit (one-tailed, alpha = 0.05).
- **H2**: Mean vehicle approach speed during active crossing events will be significantly lower at treatment crossings post-retrofit.
- **H3**: Near-miss event rate (vehicles exceeding speed threshold during active crossing) will be significantly lower at treatment crossings post-retrofit.
- **H4**: Total system activation rate (push-button + radar) at treatment crossings will be significantly higher than push-button-only activation rate at control crossings, indicating radar detection captures crossings that push-button compliance misses.

## Study Design

**Type**: Before-after with comparison group (BA/CG) — the standard FHWA-recommended methodology for evaluating traffic safety countermeasures when randomized controlled trials are not feasible.

**Sites**: Minimum 2 crossings per corridor, 1 treatment + 1 control.

- **Treatment**: Existing RRFB crossing retrofitted with coordinated illumination system
- **Control**: Matched existing RRFB crossing, no modification

**Matching criteria**: Road width (number of lanes), posted speed limit, AADT, pedestrian crossing volume, adjacent land use, existing lighting conditions, RRFB model/configuration, baseline pedestrian crash rate (5-year), and baseline RRFB activation rate.

**Minimum separation**: Treatment and control crossings should be at least 0.5 miles apart on the same corridor to minimize spillover/contamination effects (drivers who experience the illuminated crossing may change behavior at the nearby control).

**Recommended corridors** (Nashville):
- Nolensville Pike (SR 11A) — active SS4A grant, high crash history, TDOT jurisdiction
- Wedgewood Ave near Belmont University — high pedestrian volume, university funding potential
- West End Ave (US 70S) near Vanderbilt — state route, high pedestrian volume, research institution adjacency

**Expansion**: Additional treatment-control pairs on Murfreesboro Pike, Gallatin Pike, and university corridors strengthen statistical power and generalizability. 4-6 treatment crossings across multiple corridors is ideal.

## Variables

### Independent Variables
- **Primary**: Presence/absence of coordinated illumination system (binary: treatment vs control)
- **Secondary**: Time period (before vs after retrofit), time of day (day/night/dusk/dawn), CCT (if testing 3000K vs 4000K at different sites)

### Dependent Variables
- **Yielding rate**: Proportion of approaching vehicles that yield to pedestrians during active crossing events (video-coded)
- **Approach speed**: Vehicle speed at 200ft and 100ft from crossing during active events (radar-measured)
- **Near-miss rate**: Proportion of active crossing events where any vehicle exceeds threshold speed (e.g., 15 mph) within the crosswalk zone (radar-measured)
- **Activation count**: Total system activations per hour by source (push-button, radar, both)
- **Crossing volume**: Pedestrian crossings per hour by time of day (radar-measured)
- **Push-button compliance rate**: Proportion of crossings where pedestrian uses push-button (comparison between radar-detected crossings and button presses)

### Covariates
- Ambient light level (measured by photocell, logged continuously)
- Weather conditions (clear/rain/fog — logged or sourced from NWS)
- Day of week, season
- Pedestrian clothing color/reflectivity (video-coded subsample)
- Pedestrian demographics where observable (age group, mobility aid use — video-coded subsample)

## Data Collection

### Automated (continuous, full study period)
All collected by the illumination system's onboard instrumentation at treatment crossings:
- Activation events with timestamp, duration, and trigger source
- Vehicle approach speeds (radar)
- Pedestrian detection events (radar)
- Battery state, solar production, system health
- Ambient light level

### Automated at control crossings
Requires temporary equipment installation:
- Portable radar speed unit (vehicle approach speeds)
- Pneumatic tube counter or video (pedestrian crossing volume)
- RRFB activation logger (records push-button events)

### Manual (periodic sampling)
- Video recording for yielding rate coding (minimum 40 hours per crossing per period: 20 daytime, 20 nighttime, split across weekday/weekend). Use traffic-camera-style equipment to minimize Hawthorne effect — visible research-style setups may alter driver behavior.
- Pedestrian behavior coding from video (push-button use, crossing path, wait time)
- Illuminance measurements at crossing surface (handheld meter, quarterly verification)
- **Inter-rater reliability**: Yielding rate coding must be performed by at least 2 independent coders. Report Cohen's kappa with minimum threshold of κ > 0.80 for inclusion in analysis.

### Concurrent Change Documentation
Maintain a log of any infrastructure, regulatory, or land use changes at or near either crossing throughout the study period (signal timing changes, new development, speed limit modifications, road diet, adjacent construction). The comparison group controls for corridor-wide changes but not crossing-specific confounders.

## Timeline

| Phase | Duration | Activity |
|-------|----------|----------|
| Baseline (before) | 6 months minimum | Data collection at both treatment and control crossings with no modifications |
| Installation | 1-2 weeks | Retrofit treatment crossing(s); no changes to control |
| Burn-in | 30 days | System operational, data collected but excluded from analysis (novelty effects) |
| After period | 12 months minimum | Data collection at both crossings under operational conditions |
| Extended monitoring | 12+ months optional | Long-term performance, seasonal variation, maintenance data |

**Total minimum study duration**: ~20 months (6 before + 1 install/burn-in + 12 after + 1 analysis)

**Seasonal coverage**: Both before and after periods must span summer and winter to control for daylight variation. A 6-month before period starting in spring captures spring-summer-fall; the 12-month after period captures a full annual cycle.

## Sample Size and Statistical Power

### Yielding rate (primary outcome)
- Baseline nighttime yielding at RRFB crossings: estimated 60-75% (daytime is 70-90%; nighttime is lower)
- Minimum detectable effect: 10 percentage point increase (e.g., 65% to 75%)
- At alpha = 0.05 and power = 0.80, a two-proportion z-test requires ~300 crossing events per group
- At 20 crossings/night, 300 events = ~15 nights of observation per period
- Video sampling at 40 hours/period easily exceeds this

### Speed (secondary outcome)
- Baseline mean approach speed: estimated 30-35 mph (posted 35-40, with some deceleration)
- Minimum detectable effect: 3 mph reduction
- At estimated SD of 8 mph, alpha = 0.05, power = 0.80: ~112 events per group
- Radar data is continuous — sample size is not a constraint for speed

### Near-miss rate
- Baseline rate unknown (this is part of what the study establishes)
- Exploratory analysis; will report effect size and confidence interval regardless of significance

## Analysis Plan

1. **Primary analysis**: Chi-square / Fisher exact test comparing nighttime yielding rates at treatment vs control crossings in the after period, controlling for before-period rates. Odds ratio with 95% CI.

2. **Before-after comparison**: Mixed-effects logistic regression with crossing (treatment/control) and period (before/after) as fixed effects, and site as random effect. Interaction term (crossing x period) is the treatment effect.

3. **Speed analysis**: Two-sample t-test or Mann-Whitney U comparing approach speeds at treatment vs control during active nighttime crossing events. Mixed-effects linear model for longitudinal analysis.

4. **Near-miss analysis**: Poisson or negative binomial regression comparing near-miss rates per active crossing event.

5. **CMF calculation**: Crash Modification Factor using empirical Bayes before-after method if sufficient crash data accumulates (requires 3-5 years). In the interim, report surrogate safety measures (yielding rate, speed, near-miss rate) as Crash Modification Function inputs per FHWA CMF Clearinghouse methodology.

6. **Subgroup analyses**: Day vs night, clear vs adverse weather, high-visibility vs dark clothing (video-coded subsample), push-button vs radar-triggered activations.

7. **Regression to the mean (RTM) control**: If treatment crossings are selected partly because of high crash history, apparent improvement in the after period may reflect RTM rather than treatment effect. The comparison group design controls for RTM by providing a matched baseline — any RTM effect should appear equally at both crossings. For crash-based CMF calculation, the empirical Bayes method explicitly adjusts for RTM using expected crash frequency from the reference population. For surrogate measures (yielding rate, speed), RTM is less of a concern because these are behavioral measures with high event counts, not rare-event counts subject to Poisson variation.

## Phase Structure

This pilot is **Phase 1** of a multi-phase research program:

- **Phase 1 (this study)**: 1-3 treatment crossings + matched controls. Generates surrogate safety measures (yielding rate, speed, near-miss rate) and establishes the data capture methodology. Sufficient for initial CMF Clearinghouse submission with surrogate measures. Duration: ~20 months.

- **Phase 2 (expansion)**: 4-10 additional treatment crossings across multiple corridors and road types. Strengthens statistical power, tests generalizability beyond initial sites, begins accumulating crash data. Duration: 2-3 years.

- **Phase 3 (crash-based CMF)**: With 3-5 years of crash data across 10+ treatment crossings, calculate a crash-based CMF using empirical Bayes method. This is the gold standard for the FHWA CMF Clearinghouse and the threshold for high star-rating. Duration: 3-5 years from Phase 1 start.

## IRB Considerations

- **Human subjects**: The study observes pedestrian and driver behavior in public spaces. No intervention on human participants — the intervention is on the infrastructure.
- **Classification**: Likely qualifies for IRB exemption under 45 CFR 46.104(d)(2) — research involving observation of public behavior where subjects cannot be identified.
- **If linking to smartwatch data** (e.g., Vanderbilt pedestrian stress study): The physiological data IS human subjects research and already operates under Vanderbilt IRB approval. Linking the two datasets would require IRB amendment to the existing protocol.
- **Video data**: Video recordings of public roadways for traffic analysis are standard practice in transportation research. No consent required for observation in public spaces. Video should be retained for coding only, not published with identifiable individuals.

## Publication Targets

### Primary (peer-reviewed journals)
1. **Transportation Research Record (TRR)** — TRB's journal, directly relevant, high visibility in the field. Paper: "Effect of Coordinated Activated Illumination on Nighttime Driver Yielding at RRFB Crosswalks."
2. **Accident Analysis & Prevention** — Top safety journal. Paper: "Surrogate Safety Measures for Coordinated Crosswalk Illumination: A Before-After Study with Comparison Group."
3. **Journal of Safety Research** — Broader safety audience. Paper: "Closing the Dark Crossing Gap: Field Evaluation of Activated Overhead Illumination at Midblock Crosswalks."

### Secondary
4. **ITE Journal** — Practitioner audience. Shorter format, implementation-focused.
5. **FHWA CMF Clearinghouse submission** — Not a publication but establishes the Crash Modification Factor in the national database. This is the single most impactful long-term output.

### Conference presentations
6. **TRB Annual Meeting** — January, Washington DC. Abstract due August. The premier transportation research venue.
7. **TSITE Annual Meeting** — Tennessee section ITE. State-level audience, policy impact.

## Connection to Existing Research

This study design complements and extends Vanderbilt's ongoing campus pedestrian safety research (2023-present), which uses wearable physiological sensors (smartwatch heart rate variability) to identify high-stress pedestrian locations on and adjacent to campus.

**Complementary data streams:**
- **Vanderbilt smartwatch study**: Physiological stress response of pedestrians at crossing locations — identifies WHERE pedestrians feel unsafe and WHEN stress peaks during the crossing event
- **This study**: Infrastructure performance data — measures WHETHER drivers yield, HOW FAST they approach, and HOW OFTEN near-misses occur at the same locations

**Combined analysis potential**: Linking physiological stress data (pedestrian experience) with yielding/speed/near-miss data (driver behavior) at the same crossings, before and after illumination retrofit, creates a uniquely comprehensive evaluation that neither dataset achieves alone. A joint publication pairing "pedestrian perceived safety" with "objective safety metrics" would be novel in the field.

**Gresham Smith partnership**: The existing collaboration between Vanderbilt CEE and Gresham Smith provides photometric modeling and engineering design capability that complements the system specification in this package. Gresham Smith can provide AGi32 lighting models to verify the spec's illuminance targets for specific crossing geometries.
