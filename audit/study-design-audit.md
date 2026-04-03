# Study Design Self-Audit

Checking the study design in docs/study-design.md against FHWA CMF Clearinghouse standards and common peer review objections.

## FHWA CMF Clearinghouse Compatibility

The CMF Clearinghouse uses a 5-star quality rating system. To achieve a high rating, a study needs:

### Study Design Quality

- [x] **Comparison group**: Design includes matched control crossings. ✓
- [x] **Before-after design**: 6 months before, 12 months after. ✓
- [x] **Proper matching**: Criteria specified (road width, speed, volume, land use, lighting, RRFB model). ✓
- [ ] **Sample size**: Power analysis included, but based on yielding rate (surrogate measure), not crashes. **For a crash-based CMF, the Clearinghouse expects crash data.** The study correctly notes this requires 3-5 years, and proposes surrogate safety measures as interim. This is acceptable for an initial submission but the CMF will carry a lower star rating without crash data.
- [x] **Empirical Bayes method**: Mentioned for CMF calculation when crash data is available. ✓
- [ ] **Multiple sites**: Study design recommends 4-6 treatment crossings for statistical power. The minimum (1 treatment, 1 control) is underpowered for a crash-based CMF. **Recommend explicitly stating that the pilot is Phase 1, with the expectation that additional sites will strengthen the evidence.**
- [x] **Time period**: Before and after periods span seasonal variation. ✓

### Variables and Confounders

- [x] **Independent variable clearly defined**: Presence/absence of coordinated illumination. ✓
- [x] **Dependent variables measurable and relevant**: Yielding rate, approach speed, near-miss rate. ✓
- [x] **Covariates identified**: Weather, time of day, season, ambient light, clothing color. ✓
- [ ] **Regression to the mean (RTM)**: If treatment crossings are selected BECAUSE of high crash history, the before-after comparison may show improvement due to RTM, not the treatment. **The study design should mention RTM and how the comparison group controls for it.** The EB method handles this for crash-based CMFs, but for surrogate measures, RTM should be explicitly addressed.
- [ ] **Spillover effects**: If treatment and control crossings are on the same corridor (recommended for matching), drivers who experience the illuminated crossing may change behavior at the control crossing (awareness priming). **Study design should acknowledge this potential bias and discuss mitigation (e.g., minimum distance between treatment and control crossings).**

### Data Quality

- [x] **Automated data collection**: Radar data continuous at treatment crossing. ✓
- [x] **Manual verification**: Video coding for yielding rates. ✓
- [ ] **Inter-rater reliability**: Video coding of yielding events should be done by at least 2 independent coders with reliability metric (Cohen's kappa). **Not mentioned in study design — add.**
- [x] **Data retention**: Addressed in IRB section. ✓

## Common Peer Review Objections

### "Selection bias in site choice"

If the treatment crossing is selected because it has worst crash history or highest pedestrian volume, the comparison is biased. **Mitigation**: Match treatment and control on baseline crash rate and volume, not just road geometry. The study design mentions matching criteria but doesn't explicitly include baseline crash rate.

**Recommendation**: Add "baseline pedestrian crash rate (5-year)" and "baseline RRFB activation rate" to matching criteria.

### "Novelty effect"

Driver behavior may change immediately after installation due to novelty (the new light), not because the light actually improves visibility. **Mitigation**: The 30-day burn-in exclusion period is included. ✓ But consider extending to 60-90 days or analyzing for temporal decay in the after period.

### "Hawthorne effect"

If drivers or pedestrians know they're being studied (visible video cameras), behavior changes. **Mitigation**: Use traffic-camera-style equipment, not obviously research-oriented setups. **Not mentioned in study design — add a note on equipment concealment.**

### "Confounding from other changes"

During the 20-month study period, other things may change on the corridor (new development, speed limit change, signal timing change, road diet). **Mitigation**: The comparison group controls for corridor-wide changes that affect both crossings equally. Changes that affect only the treatment or only the control crossing are a threat. **Study design should include a protocol for documenting any concurrent changes at either crossing during the study period.**

### "Surrogate measures aren't crashes"

The CMF Clearinghouse and FHWA Safety Office ultimately want crash data, not yielding rates. Surrogate safety measures are increasingly accepted (FHWA Surrogate Safety Assessment Model) but carry lower evidentiary weight. **The study design correctly acknowledges this and proposes both surrogate and crash-based analysis.** ✓

## Specific Additions Recommended for study-design.md

1. **Add regression to the mean (RTM) discussion** — how the comparison group design and EB method control for RTM
2. **Add spillover/contamination distance** — minimum distance between treatment and control crossings (recommend 0.5+ miles)
3. **Add inter-rater reliability** — Cohen's kappa for video coding of yielding events, with minimum threshold (κ > 0.80)
4. **Add concurrent change documentation protocol** — log any infrastructure, regulatory, or land use changes at either crossing during the study
5. **Add equipment concealment note** — minimize Hawthorne effect from visible research equipment
6. **Add baseline crash rate to matching criteria** — 5-year pedestrian crash rate at both crossings
7. **Clarify phase structure** — this pilot is Phase 1; Phase 2 would expand to additional sites for crash-based CMF with adequate statistical power
