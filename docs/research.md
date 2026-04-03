# Research Notes

Compiled 2026-04-02 from GHSA, FHWA, TDOT, Nashville Metro, IES sources.

## National Data

- 76%+ of pedestrian fatalities occur after dark (GHSA)
- Nighttime fatal pedestrian crashes rose 84% between 2010-2023, vs 28% daytime (GHSA)
- Pedestrian deaths rose 80% overall 2009-2023; all other traffic fatalities only 13% (GHSA)
- FHWA statistical value of life: ~~$13.7M (2024 USDOT) for safety benefit-cost analysis

## CCT and Mesopic Vision Research

The color temperature of the crosswalk luminaire directly affects pedestrian detection at night. Higher CCT (4000K) outperforms lower CCT (3000K) in mesopic conditions due to the Purkinje shift — the eye's sensitivity moves toward shorter wavelengths at low ambient light levels.

### Key Studies

- **FHWA-HRT-15-047** (2015): In low-speed pedestrian environments, "lighting levels can be scaled based on the light source spectrum." No spectral effect for high-speed roadways, but explicit benefit for pedestrian crossings. [Source](https://www.fhwa.dot.gov/publications/research/safety/15047/012.cfm)
- **Terry & Gibbons (VTTI)**: Higher CCT LEDs outperformed lower CCT in pedestrian detection studies. FHWA-HRT-15-047 found LED clothing color recognition at ~24.2m vs HPS at ~19.8m (~22% improvement). Gibbons has reported increased hazard recognition distance with higher CCT at IPWEA conferences, though specific percentage figures from those presentations have not been independently verified in published literature.
- **IES TM-12-12**: Mesopic multipliers apply to exterior environments at speeds <25 mph. Pedestrian crossings are exactly this environment.
- **FHWA-HRT-08-053**: White-light (broad-spectrum) sources improved detection of pedestrians in denim at midblock crosswalks. [Source](https://www.fhwa.dot.gov/publications/research/safety/08053/)
- **2025 ScienceDirect study**: Visual performance stable across 1800K-4000K, deficit at 5000K. Supports 4000K as the optimal ceiling.
- **IPWEA (Australia)**: Formally recommends 4000K for main roads and pedestrian crossings, citing ~20% safety improvement.

### Nashville Dark Sky Ordinance Tension

Nashville BL2020-535 caps outdoor CCT at 3000K. Three paths to 4000K authorization:

1. **Jurisdictional**: TDOT state-route installations may be outside Metro's municipal ordinance scope
2. **Variance**: BL2022-1088 authorizes Board of Fire and Building Code Appeals to grant variances for "manifest injustice" or public interest — safety-critical application with FHWA research backing
3. **Legislative precedent**: Maine LD 1934 (effective Sept 2026) explicitly exempts DOT and pedestrian safety lighting from CCT caps

### AMA Caution

The American Medical Association (2016) recommended communities use 3000K or below for streetlighting, citing circadian disruption and glare concerns from 4000K+ continuous streetlighting. **Key distinction**: this system is activated-only (15-20 seconds per crossing event), not continuous. The AMA concern about all-night exposure does not apply to brief, intermittent activation. This should be part of the variance argument.

## Nashville Specific

- 4 out of 5 pedestrian fatalities on wide, state-controlled arterials >30mph
- 71% on roads with 4+ lanes
- Most fatalities 6pm-6am
- Pedestrian fatalities on state routes up 17% in 2023 (24→28)
- Fatalities rose from 14 (2010) to 39 (2020)
- $13M Safe Streets for All grant for Nolensville Pike
- Key corridors: Nolensville Pike, Murfreesboro Pike, Gallatin Pike

## Standards Landscape

### National
- **ANSI/IES RP-8-25** (2025, supersedes RP-8-22): 20 lux vertical at 1.5m above crosswalk surface, 14 lux horizontal average minimum. *Note: these values were established in RP-8-22; verify unchanged in RP-8-25 when the 2025 edition is obtained.*
- **AASHTO Roadway Lighting Design Guide (2018)**: Reinforces IES RP-8 illuminance criteria; referenced by state DOTs for design policy. Addresses crosswalk lighting but not coordinated activation.
- **MUTCD 11th Edition with Revision 1 (2025)**: Codified RRFBs. Notes lighting *should* be a prerequisite. No activation spec.
- **FHWA Informational Report on Lighting Design for Midblock Crosswalks**: Reference, not mandate

### State (Tennessee / TDOT)
- **TDOT Lighting Design Manual**: All roundabouts and mid-block pedestrian crossings **shall** include lighting design per Traffic Operations Memo 2022. Silent on coordinated activation, beam geometry, fixture type.
- TDOT standard drawings: designers *should also consider* adding or enhancing street illumination at midblock crossings

### Local (Nashville)
- **Nashville Streets and Pathways Lighting Manual**: Compliance with NDOT, NES, and TDOT required. Crosswalk poles located on approach side.
- **NES**: All electrical power on their right-of-way requires coordination. Solar sidesteps most of this.
- **ADA/PROWAG**: Pushbutton height, APS integration, tactile surfaces

## RRFB Effectiveness Baseline

Understanding what RRFBs achieve alone — and where they fall short — frames why coordinated illumination matters.

### Yielding Rates

- **Without RRFB**: Driver yielding at uncontrolled crosswalks is typically 10-20% (FHWA)
- **With RRFB**: Yielding rates increase to 70-90%+ in most studies (FHWA RRFB Informational Report)
- **NCHRP Report 841**: RRFBs are among the most cost-effective pedestrian safety countermeasures available
- **Nighttime gap**: Most RRFB yielding studies are conducted during daylight. Nighttime yielding rates are consistently lower — drivers may see the flashing beacon but not the pedestrian. The beacon says "someone is crossing" but the driver cannot confirm where the person is.

### Crash Reduction

- FHWA estimates 47% reduction in pedestrian crashes at RRFB-equipped crossings (combined day/night)
- Nighttime-specific crash reduction data for RRFBs alone is limited — most studies aggregate day and night
- The 76% of fatalities occurring after dark suggests the nighttime crash reduction from RRFBs alone is significantly less than 47%

### The Illumination Delta

No published study isolates the additional crash reduction from adding coordinated illumination to an existing RRFB. This is the research gap. The proposed system's data logging (activation events, vehicle speed/yield behavior) is specifically designed to generate this data from every installation. Each crossing becomes a study site.

## Comparable Installations and Prior Art

### Coordinated Crosswalk Illumination

- **TAPCO SafeWalk deployments**: TAPCO markets the SafeWalk Crosswalk Illuminator as an RRFB companion product, but adoption has been limited. No published before/after study on crash reduction. Product exists; specification practice does not.
- **Carmanah R920 series**: Solar RRFB with optional integrated overhead LED. Deployed in various US/Canadian jurisdictions. Similar concept but typically lower-output LED than the IES RP-8 levels specified here.
- **City of Boulder, CO**: Has installed overhead crosswalk illumination at multiple locations, though not always coordinated with beacon activation. One of the few US municipalities actively specifying crosswalk-specific luminaires.
- **European practice**: Several EU countries (Netherlands, Sweden, UK) specify minimum crosswalk illuminance levels in their national standards. The UK's BS 5489 series includes specific guidance for pedestrian crossing illumination. European practice is generally ahead of US on this.
- **In-pavement LED crosswalk systems**: Multiple US installations (e.g., LightGuard Systems). Effective visual cue but does not illuminate the pedestrian — lights the pavement boundary only. Requires roadway cut-and-patch. Different problem solved.

### What's Different About This Proposal

Most existing products and installations are piecemeal: a fixture here, an enhanced RRFB there. This proposal packages:

1. A complete system specification (not just a product recommendation)
2. Draft regulatory language (not just a design suggestion)
3. A data capture framework that generates evidence from every installation
4. A cost model that's designed for municipal budget justification

The gap isn't that the hardware doesn't exist. It's that nobody has written the spec that makes it standard practice.

## Funding Mechanisms

### Federal

- **Highway Safety Improvement Program (HSIP)**: Primary federal funding source for RRFB installations. Coordinated illumination is an eligible safety improvement under the same program. Key: the improvement must be justified by crash data at the specific location or a systemic analysis of similar locations.
- **Safe Streets and All (SS4A)**: USDOT discretionary grant program. Nashville already has a $13M SS4A grant for Nolensville Pike — coordinated illumination could be included in that scope or a future application. SS4A specifically funds Vision Zero-aligned infrastructure improvements.
- **PROTECT Formula Program**: Funds resilience improvements to transportation infrastructure. Solar-powered safety systems qualify under the resilience framing (grid-independent, climate-adapted).
- **Rebuilding American Infrastructure with Sustainability and Equity (RAISE)**: Discretionary grants for projects with safety, sustainability, and equity benefits. Pedestrian safety on arterials in underserved communities checks all three boxes.

### State (Tennessee)

- **TDOT Pedestrian Safety Grant Program**: Directly funds RRFB installations on state routes. Coordinated illumination as an RRFB enhancement fits within program scope.
- **TDOT HSIP funds**: Tennessee's share of federal HSIP dollars, administered by TDOT Traffic Operations.
- **Tennessee Highway Safety Office (THSO)**: Funds behavioral and infrastructure safety programs. Data-driven proposals aligned with state pedestrian safety plan are competitive.

### Local (Nashville)

- **Nashville Vision Zero budget**: Metro Nashville has committed to Vision Zero. Infrastructure improvements on high-crash corridors are directly aligned.
- **Metro Capital Improvements Budget**: Nashville funds streetlighting and traffic safety through separate capital budget lines. The jurisdictional split (RRFB = traffic engineering, lighting = public works) means coordinated illumination may need to be championed from the traffic side with public works buy-in.
- **NES partnership**: Nashville Electric Service has historically partnered on streetlighting improvements. Solar-first design reduces NES involvement, but NES could be a partner for future grid-tied installations.

### Research Funding (Academic)

For a university-led pilot study, different funding streams apply:

- **USDOT University Transportation Centers (UTC)**: Vanderbilt's VECTOR is affiliated with Region 4 UTC. UTC grants fund applied transportation research exactly like this — field evaluation of a safety countermeasure with before/after data. Typical award: $50,000-200,000. Requires university match (often in-kind: faculty time, grad student support).
- **NSF CMMI (Civil, Mechanical and Manufacturing Innovation)**: Infrastructure and Transportation Systems program funds research on safety-enhancing infrastructure. A crosswalk illumination study with sensor data, yielding analysis, and CMF development fits the "smart infrastructure" framing. Typical EAGER award: $100,000-300,000.
- **FHWA Exploratory Advanced Research (EAR) Program**: Funds high-risk, high-payoff research on emerging transportation technologies. Solar-powered, radar-equipped crosswalk infrastructure with data capture qualifies as "connected infrastructure."
- **NCHRP (National Cooperative Highway Research Program)**: TRB administers problem statements submitted by state DOTs. If TDOT submits a problem statement on coordinated crosswalk illumination, NCHRP can fund a multi-state study. This is the path to a national CMF — but requires TDOT to submit the problem statement.
- **TDOT Research Office**: TDOT funds university research through its Research and Development program. A Vanderbilt proposal for a field study on a state route would go through TDOT Research, which coordinates with Traffic Operations. Smaller awards ($25,000-100,000) but directly connected to TDOT policy adoption.

**Best path for a Vanderbilt-led study**: TDOT Research Office funding for the pilot (direct policy connection) + UTC match for the academic side. Total budget ~$50,000-100,000 covers hardware, temporary data collection equipment at control crossings, grad student researcher for 2 years, and publication costs. The hardware itself ($8-16K for two crossings) is a small fraction of the research budget.

### Infrastructure Grant Strategy

The strongest path for deployment-scale funding is to include coordinated illumination as a line item in an existing or upcoming HSIP or SS4A application for RRFB deployment. The incremental cost ($2-4K per crossing) is small enough to fold into a corridor-level RRFB project without changing the project's benefit-cost ratio. It's easier to add $50K for illumination to a $500K corridor RRFB project than to seek standalone funding for illumination alone.

## Nashville Vision Zero Alignment

Nashville's Vision Zero Action Plan identifies pedestrian safety on high-speed arterials as a top priority. This proposal directly addresses:

- **Safe speeds**: The radar detection component captures vehicle approach speeds — data for speed management decisions on target corridors
- **Safe streets**: Coordinated illumination is a direct infrastructure improvement to the pedestrian crossing environment
- **Safe people**: Passive detection activates without requiring pedestrian action, protecting the most vulnerable users (elderly, impaired, distracted, unfamiliar)
- **Post-crash response**: Data logging provides crash reconstruction evidence that doesn't currently exist at most RRFB locations
- **Equity**: Nashville's highest-crash pedestrian corridors (Nolensville, Murfreesboro, Gallatin Pikes) serve predominantly lower-income communities with high transit ridership and pedestrian mode share. Infrastructure improvements here are equity investments.

## Existing Products

- **TAPCO SafeWalk Crosswalk Illuminator**: Product exists but not in any guidance document. No one specifying it as required pairing with RRFBs.
- **Carmanah, Solar Traffic Controls**: Solar RRFB units exist with integrated overhead LED options
- **In-pavement LED crosswalk lights**: Exist but require roadway cut-and-patch

## Cost Data

| System | Cost |
|--------|------|
| Standard RRFB install | $10,000-15,000 per crossing |
| Pedestrian Hybrid Beacon (HAWK) | ~$57,680 average |
| Coordinated overhead LED retrofit (solar) | $2,000-4,500 incremental |
| Value of statistical life (FHWA) | ~$13.7M (2024 USDOT) |

One prevented fatality at $3,000/crossing makes the benefit-cost ratio absurd.

## Resistance / Friction Points

1. **"Should" vs "shall"** — MUTCD and TDOT both advisory, not mandatory
2. **Jurisdictional split** — RRFB owned by traffic engineering, lighting by public works/utility. No single owner writes the coordinated spec
3. **Budget siloing** — RRFB funded through HSIP federal safety dollars, streetlighting from different bucket. Combining requires cross-stream coordination
4. **No warrant** — no national warrants for justifying RRFB installation, let alone coordinated lighting
5. **NES coordination** on state routes — solar-first sidesteps this
6. **Patent history** — RRFB was patented, FHWA terminated interim approval 2017, field still catching up on treating RRFBs as mature infrastructure

## Dark Sky Ordinance and CCT Analysis

Compiled 2026-04-03.

### Nashville BL2020-535 — Dark Sky Ordinance

**Effective**: April 6, 2021 (passed Metro Council 32-1 with four abstentions)

**What it does**: Amends Titles 16 and 17 of the Metropolitan Code of Laws to regulate outdoor electrical lighting consistent with International Dark Sky Association (IDA) guidelines.

**Key provisions**:

- Maximum CCT of 3000K for outdoor luminaires
- Fixtures must be directed and illuminated only as necessary
- Controls required to dim or turn off lights when not in use
- Five lighting zones designated (rural to urban), with different regulations per zone
- Outdoor lighting plans must now specify light output levels and be submitted to Metro Codes Administration

**Scope and applicability**:

- Applies to **new construction only** — existing installations grandfathered
- Applies to private streetlights, commercial construction, major renovations of commercial and multifamily
- Downtown Nashville inside the interstate ring is **exempt** (Core Historic, Core, Upper Broadway, Second and Broadway, SoBro zones)
- Property owned by Metropolitan Nashville Airport Authority is **exempt**

**What BL2020-535 does NOT explicitly exempt**: The ordinance text as publicly available does not contain a specific carve-out for public safety infrastructure, traffic safety devices, or TDOT/state installations on state routes. This is a gap — most well-drafted dark sky ordinances (see DarkSky International model ordinance, Maine LD 1934) include explicit safety and transportation infrastructure exemptions. Nashville's does not appear to.

**However**: The ordinance applies to new construction reviewed under Metro building codes. TDOT installations on state routes (Nolensville Pike, Murfreesboro Pike, Gallatin Pike) are state infrastructure, not Metro building permits. The jurisdictional argument is that TDOT installations are not subject to Metro zoning code Chapter 17 in the same way private development is. This needs confirmation from Metro Codes and/or TDOT.

### BL2022-1088 — Variance Amendment

**Effective**: 2022 (amends Sections 2.80.080, 17.28.100, 17.40.010)

**What it does**: Authorizes the Board of Fire and Building Code Appeals to grant variances from the dark sky lighting provisions.

**Variance standard**: The board may vary application of requirements "when, in its opinion, the strict enforcement thereof would do manifest injustice" and would contradict the chapter's "spirit and purposes" or the public interest.

**Significance for this project**: A safety-based variance application could argue that strict enforcement of the 3000K CCT cap at RRFB-equipped crosswalks on high-fatality corridors would contradict the public interest (pedestrian safety) and the spirit of the ordinance (responsible lighting, not no lighting). The "manifest injustice" standard is met when the CCT cap prevents optimized visibility at locations where people are dying.

### DarkSky International Model Ordinance — Exemption Framework

DarkSky International's model municipal ordinance template (v1.0, 2024) explicitly allows CCT exemptions when a public safety need is documented. The model ordinance:

- Sets 3000K as the baseline maximum
- Exempts federally funded and state funded roadway construction projects to the extent necessary to comply with federal and state requirements
- Exempts full cutoff street lighting that is part of a federal, state, or municipal installation
- Allows documented public safety exceptions

Nashville's ordinance was drafted to align with IDA guidelines but may not have incorporated all of the model ordinance's exemption categories. This is relevant: the IDA itself recognizes that safety-critical lighting may require exemptions.

### Maine LD 1934 — Best-in-Class Precedent (Effective September 30, 2026)

Maine's "Responsible Outdoor Lighting Act" is the most comprehensive state-level dark sky law in the U.S. as of 2026. Its exemption structure is directly relevant to the Nashville case:

- **Baseline**: 3000K CCT maximum for public outdoor luminaires over 1,000 lumens
- **DOT/Transportation exemption**: Lighting installed by or for the Department of Transportation or Maine Turnpike Authority is **exempt from the 3000K CCT limit**. Roadway and pedestrian lighting under their jurisdiction follows their own standards (ANSI/IES RP-8, RP-43).
- **Public safety exemption**: Law enforcement and first responders exempt during emergency procedures
- **Temporary construction**: Roadwork or emergency repair lighting can exceed standard limits "to the minimum extent necessary"
- **Safety override during curfew hours**: Lighting enhancing physical safety of vehicles or pedestrians remains operational during shutoff hours
- **Sports lighting**: May exceed to 5700K during active play
- **Ski facilities**: Entirely exempt

**Why this matters**: Maine's law was drafted with legislative counsel, environmental groups, and transportation engineers at the table. The result is a law that protects dark skies while explicitly recognizing that DOT and pedestrian safety lighting operate under different constraints. Nashville's ordinance lacks this nuance. Maine's framework is the model for how to argue a safety exemption in Nashville — or for how Nashville should amend BL2020-535.

### IPWEA (Australia) — Differentiated CCT by Road Classification

The Institute of Public Works Engineering Australasia (IPWEA) adopted a balanced approach:

- **3000K** for residential roads and parks (~70% of all public lighting)
- **4000K** for main roads, based on maximizing driver and pedestrian safety

The City of Palmerston (Northern Territory) was the first Australian council to fully deploy this dual strategy. Two NSW utilities (Ausgrid, Essential Energy) subsequently adopted the same approach.

IPWEA cites a ~20% improvement in main road safety outcomes with 4000K vs 3000K, and references Dr. Ron Gibbons (VTTI) finding a 30-40% increase in hazard recognition distance under higher CCT.

### Strategy for Nashville

Three paths to compliance:

1. **Jurisdictional argument** (strongest): TDOT installations on state routes are state infrastructure, not subject to Metro zoning code. The dark sky ordinance applies to private/commercial construction reviewed under Metro building permits. RRFB crosswalk illumination installed by or for TDOT on state routes may fall outside the ordinance's scope entirely.

2. **Variance through BL2022-1088**: Apply to the Board of Fire and Building Code Appeals for a variance from the 3000K cap for safety-critical crosswalk illumination, arguing manifest injustice and public interest under the established variance standard.

3. **Design within 3000K**: Spec the system at 3000K and compensate with higher lumen output. This avoids the regulatory fight entirely. The research below shows that while 4000K is measurably better for peripheral detection, the advantage is modest at the illuminance levels this system delivers (20 lux vertical). At 20 lux, the eye is operating in the upper mesopic/low photopic range where the CCT advantage narrows. The narrow-beam, high-illuminance design partially compensates for the spectral disadvantage of 3000K.

---

## CCT and Pedestrian Safety — Scientific Evidence

### The Purkinje Shift and Mesopic Vision

At low light levels (below ~5 cd/m2 adaptation luminance), human vision transitions from cone-dominated (photopic) to rod-dominated (scotopic) through the mesopic range. Rods have peak sensitivity at ~507 nm (blue-green), while cones peak at ~555 nm (yellow-green). This shift in spectral sensitivity — the Purkinje shift — means the eye becomes more responsive to shorter-wavelength (bluer/cooler) light as ambient levels drop.

Most nighttime roadway lighting operates in the mesopic range (0.03-5 cd/m2). This is the theoretical basis for the argument that higher-CCT (cooler, more blue content) light improves nighttime visibility.

### IES TM-12-12: Spectral Effects of Lighting on Visual Performance at Mesopic Levels

IES Technical Memorandum TM-12-12 establishes the framework for mesopic photometry in exterior lighting:

- Mesopic vision is active at adaptation luminance 0.03-5 cd/m2 (most exterior lighting)
- Light sources with S/P (scotopic-to-photopic) ratios >1 provide more effective lumens under mesopic conditions
- Higher-CCT LEDs generally have higher S/P ratios (a 4000K LED typically has S/P ~1.6-1.8 vs ~1.3-1.5 for 3000K)
- **Critical caveat**: S/P ratio cannot be reliably estimated from CCT alone except for incandescent sources. The spectral power distribution (SPD) matters, and two LEDs at the same CCT can have different S/P ratios
- TM-12-12 mesopic multipliers are validated for exterior environments at speeds <25 mph — directly applicable to pedestrian crossings

### FHWA-HRT-15-047: Evaluation of the Impact of Spectral Power Distribution on Driver Performance (2015)

This is the most directly relevant federal study. Key findings:

**What was tested**: 2100K HPS, 3500K LED, and 6000K LED overhead lighting at various levels, measuring pedestrian detection distance under real driving conditions.

**Headline results**:

- 6000K LED outperformed 3500K LED in pedestrian clothing color recognition distance by approximately 30%
- LED lighting showed longer off-axis (peripheral) pedestrian detection distances than HPS (~55.7m vs ~44.7m), though not statistically significant due to limited sample
- LED required less negative contrast for detection (-0.032) vs HPS (-0.086), suggesting spectral effects enhance visibility independent of brightness
- At the lowest adaptation luminance (0.07 cd/m2), the eye was more dark-adapted and more contrast-sensitive — mesopic advantage was greatest

**The critical distinction**:

- **High-speed roadways (>25 mph / 40 km/h)**: No significant spectral effect on driver visual performance. The study recommends that "spectral effects not be included in the design of the lighting systems" for high-speed roads.
- **Low-speed / pedestrian environments (<25 mph)**: "Lighting levels can be scaled based on the light source spectrum" because "the lighting system is primarily for the benefit of pedestrians, and vehicle headlamps provide adequate lighting for drivers." The study explicitly acknowledges that "a pedestrian has a wider field of view, and there may be spectral effects of lighting on pedestrian visual performance."

**Implication**: FHWA's own research draws a line exactly where this project operates. RRFB crosswalks are low-speed pedestrian environments where spectral effects (CCT) are acknowledged to matter. The study does not recommend 3000K for these environments — it suggests that spectral optimization is appropriate.

### FHWA-HRT-08-053: Informational Report on Lighting Design for Midblock Crosswalks

**Key findings**:

- 20 lux vertical illuminance at 1.5m provides adequate pedestrian detection
- Metal halide (white-light, ~4200K) improved detection of pedestrians in denim clothing vs HPS
- White-light sources "may provide better facial recognition and comfort for pedestrians"
- 30 lux recommended for crosswalks with opposing vehicle glare or high ambient light

**CCT note**: The report does not specify a CCT value but consistently associates "white" or "broad-spectrum" light with better detection performance than narrow-spectrum (HPS) light. The logical extension is that 4000K (neutral white) aligns better with the report's findings than 3000K (warm white).

### Terry and Gibbons (VTTI) — Target Detection Studies

Ron Gibbons at the Virginia Tech Transportation Institute has conducted the most extensive field research on spectral effects and pedestrian detection:

- Compared 3500K LED, 6000K LED, and 4200K fluorescent for pedestrian detection
- 6000K outperformed 3500K by ~30% in pedestrian clothing color recognition distance
- 3500K and 6000K were roughly equal for target detection distance (not color recognition)
- At an IPWEA conference, Gibbons reported a 30-40% increase in hazard recognition distance with higher CCT under standardized conditions

### AMA 2016 Guidance

The American Medical Association's 2016 policy statement:

- Recommends 3000K or lower for outdoor installations
- Based primarily on circadian rhythm disruption (melatonin suppression) and glare concerns
- Does not address the mesopic vision / pedestrian safety trade-off
- Does not differentiate between continuous area lighting (where circadian concerns are strongest) and brief-activation safety lighting (where exposure is seconds, not hours)

**Relevance to this project**: The crosswalk illumination system activates for 15-20 seconds per crossing event. Cumulative nightly exposure to any individual is negligible — this is not the "all night every night" continuous lighting that the AMA guidance targets. The circadian argument against higher CCT is materially weaker for brief-activation systems than for continuous streetlighting.

### Recent Research: CCT Threshold Effects

A 2025 study on road lighting color temperature and visibility (ScienceDirect, DOI: 10.1016/j.jsr.2025) found:

- Performance was stable across 1800K-4000K but showed a deficit at 5000K
- 5000K lighting required significantly higher contrast for target detection vs lower CCTs
- Suggests 4000K may be an optimal ceiling — above it, glare and disability effects begin to offset the mesopic advantage

This finding supports a 4000K specification rather than 3000K (marginal loss) or 6000K (glare risk).

### Synthesis: The Case for a Safety Exemption or 4000K Specification

**The scientific argument**:

1. Mesopic vision shifts spectral sensitivity toward blue-green at typical nighttime lighting levels (IES TM-12-12)
2. FHWA's own research (FHWA-HRT-15-047) acknowledges spectral effects matter for pedestrian-environment lighting and explicitly distinguishes it from high-speed roadway lighting
3. 4000K LED provides measurably better peripheral detection and color recognition than 3000K (Gibbons/VTTI, ~30% color recognition improvement at 6000K vs 3500K; ~20% safety improvement at 4000K vs 3000K per IPWEA)
4. The AMA's 3000K recommendation does not account for brief-activation safety systems — the circadian disruption argument is weakest here
5. Research suggests 4000K is the optimal balance point: above it (5000K+), glare offsets the mesopic advantage
6. FHWA-HRT-08-053 associates white/broad-spectrum light with better pedestrian detection at crosswalks

**The regulatory argument**:

1. DarkSky International's own model ordinance allows CCT exemptions for documented public safety needs
2. Maine LD 1934 (2026), the most comprehensive US dark sky law, explicitly exempts DOT and pedestrian safety lighting from the 3000K cap
3. IPWEA (Australia) formally recommends 4000K for main roads and pedestrian crossings on safety grounds
4. Nashville BL2022-1088 provides a variance path through the Board of Fire and Building Code Appeals
5. Nashville's ordinance applies to new construction under Metro building permits — TDOT state route installations may be jurisdictionally exempt

**The practical argument**:

1. This system activates for seconds per event — cumulative blue light exposure is negligible
2. The narrow beam (15-25 degrees) confines light to the crossing surface — no sky glow contribution
3. The cutoff fixture design (U0 BUG rating) produces zero uplight
4. The system is dark between activations — net light pollution impact is lower than a continuous 3000K streetlight
5. At the illuminance levels delivered (20 lux vertical), the eye is in upper mesopic / low photopic territory where the CCT advantage is real but not as large as at lower adaptation levels

**Recommendation**: Spec the system at 4000K for crosswalk illumination and pursue one of three paths: (a) jurisdictional exemption (TDOT state route argument), (b) variance through the Board of Fire and Building Code Appeals under BL2022-1088, or (c) if neither is viable, fall back to 3000K with increased lumen output (5000-6000 lumens) to compensate. The scientific record supports the safety case. The regulatory record shows that the best-drafted dark sky laws already carve out exactly this kind of exemption.

---

## Key Offices

- **Your state ITE section** — abstract submissions for section meetings
- **Your city/county Vision Zero or pedestrian safety office** — accepts corridor-specific feedback
- **Your state DOT pedestrian safety or HSIP program** — funds RRFBs and eligible safety improvements on state routes
