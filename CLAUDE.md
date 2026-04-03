# Crosswalk — Project Instructions

## What this is

Open specification for coordinated overhead lighting on RRFB-equipped pedestrian crossings. Not a software project — an infrastructure safety specification with research, regulatory analysis, study design, and implementation plan.

## Structure

- `docs/` — Research, executive summaries, study design, legal/codes reference, implementation plan
- `spec/` — Full system design specification
- `hardware/` — BOM, fixture selection, installation notes
- `internal/` — Non-public strategy docs (gitignored)

## Key conventions

- Nashville-specific data and codes are primary, but the spec is written to be portable to any US jurisdiction
- All costs are 2026 estimates for single-unit procurement
- "Shall" vs "should" language is deliberate — matches MUTCD/TDOT memo conventions
- CCT spec is 4000K recommended with 3000K fallback (see CCT justification in system-design.md)
- Performance-based specification — no single-brand requirements (Tennessee procurement law TCA 12-4-903)

## Editing guidelines

- Keep research citations traceable — include source names, not just claims
- Maintain the two-audience structure: academic-summary.md for researchers, executive-summary.md for policy/DOT audience
- internal/ directory is gitignored — keep strategy, contacts, and personal details there
- This is CC-BY-4.0 licensed — anyone can adapt and use with attribution
