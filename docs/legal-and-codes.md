# Legal and Codes Reference

Complete regulatory framework for solar-powered LED illumination at RRFB-equipped pedestrian crosswalks. Covers every code, standard, law, and regulation that applies — from federal statute down to Nashville municipal ordinance.

**Status key:**
- **HARD** = Mandatory (shall/must language, legally binding)
- **ADVISORY** = Recommended practice (should/may, non-binding guidance)
- **CONDITIONAL** = Hard requirement only if specific conditions are met (e.g., federal funding, historic district, floodplain)

---

## Part 1: Nashville-Specific (Local)

Everything in this section applies to installations within Nashville / Davidson County, in addition to the state and federal requirements in Parts 2 and 3.

### Traffic and Lighting

**Nashville Streets and Pathways Lighting Manual (2024)**
- Authority: Nashville Dept. of Transportation (NDOT)
- Governs: Pole types, locations, photometric requirements for Nashville street lighting. Crosswalk poles located on approach side. Any lighting installation in Nashville ROW must conform.
- Status: **HARD**

**NES Lighting Guidelines (Version 6, 2023)**
- Authority: Nashville Electric Service
- Governs: NES-approved light pole selection, documentation and design requirements, inspection and power connection procedures. NES controls streetlight infrastructure in Nashville.
- Status: **HARD** for grid-connected installations; **ADVISORY** for solar-only (coordination still recommended)
- Note: Solar-first design sidesteps most NES involvement. If ever grid-tied, full NES coordination required.

**NES Pole Attachment Guidelines**
- Authority: Nashville Electric Service
- Governs: If mounting on existing NES-owned poles, an Infrastructure Use Agreement is required. Attachments must meet NESC standards and NES design standards. Application through NES Attachments Group. $100/pole application fee.
- Status: **HARD** if using NES poles; N/A if installing independent poles

### Encroachment and Right-of-Way

**Metro Nashville Code Title 13, Chapter 13.08 — Streets, Alleys and Sidewalks**
- Authority: Metro Nashville
- Governs: Prohibits temporary or permanent encroachment in public ROW without permit. Construction manner subject to approval of Director of Public Works.
- Status: **HARD**

**Metro Nashville Code Title 13, Chapter 13.16 — Private Installations in Public Ways**
- Authority: Metro Nashville
- Governs: Any private installation on, over, or under public ways requires permit, insurance (amount per Metro Attorney), and indemnification of Metro Government. Underground encroachments require ordinance approval (three readings before Metro Council).
- Status: **HARD**

**Metro Nashville Code Title 13, Chapter 13.20 — Excavation and Obstruction Permits**
- Authority: Metro Nashville
- Governs: Permit fees and requirements for excavation in ROW for pole foundation installation. Fee schedule at 13.20.030.
- Status: **HARD**

**NDOT Encroachment Permit**
- Authority: Nashville Dept. of Transportation
- Governs: Any work in Nashville's public ROW requires encroachment permit from NDOT. Covers pole installation, foundation excavation, conduit placement.
- Contact: NDOT Right-of-Way Permits Office, 615-862-8782
- Status: **HARD**

### Building and Electrical

**Metro Nashville Code Title 16 — Buildings and Construction**
- Authority: Metro Nashville Dept. of Codes and Building Safety
- Governs: Building permit requirements. Chapter 16.08 adopts building codes. Chapter 16.28 governs permit applications. A CAEP (Electrical Photovoltaic) permit required for the solar installation. Must be installed by a licensed and registered electrical contractor.
- Status: **HARD**

**Nashville NEC 2023 Adoption (effective July 15, 2025)**
- Authority: Metro Nashville
- Governs: Nashville adopted NEC 2023, superseding the state's NEC 2017 for work within Nashville/Davidson County. All NEC 2023 provisions for PV (Art. 690), ESS (Art. 706), and general wiring apply.
- Design impact: NEC 2023 Art. 690.12 rapid shutdown requires controlled conductors reduced to 80V within 30 seconds within 1-foot boundary of PV array.
- Status: **HARD**

**Nashville Electrical Contractor Registration**
- Authority: Metro Nashville Dept. of Codes
- Governs: Contractors must hold State CE, CE-B, or CE-H classification AND register locally with Nashville. Minimum $300,000 general liability insurance required for Nashville registration.
- Status: **HARD**

### Zoning, Dark Sky, and Overlays

**Nashville Dark Sky Ordinance (BL2020-535, effective April 6, 2021)**
- Authority: Metro Nashville
- Governs: Outdoor lighting design and operation for light pollution reduction, consistent with DarkSky International guidelines.
- Key requirements:
  - Maximum color temperature: **3000K** (specification recommends 4000K with 3000K fallback; see CCT justification)
  - Controls to dim or turn off when not in use (activated-only design complies)
  - Five lighting zones from rural to urban with different limits
  - Requires BUG ratings per IES TM-15
  - Exemptions: Downtown districts (Core Historic, Core, Upper Broadway, SoBro, etc.) and MNAA property
- Design impact: Spec recommends 4000K for pedestrian safety (mesopic vision research, ~20% detection improvement per IPWEA). Pursuing TDOT jurisdictional argument and/or BL2022-1088 variance. 3000K fallback with increased lumen output if variance denied. See system design spec CCT justification for full research package.
- Status: **HARD** (except in exempt downtown zones)

**Nashville Historic Zoning Overlay Districts**
- Authority: Metro Nashville Historic Zoning Commission
- Governs: Exterior improvements within historic overlay districts require preservation permit before building permit. Commission reviews appropriateness of exterior design. Pole design, height, finish, and fixture appearance may require HZC approval.
- Design impact: Site-specific screening needed per crossing location.
- Status: **CONDITIONAL** (applies only in designated historic overlay districts)

**Nashville Tree Canopy Protection Ordinance (BL2022-1409, effective March 15, 2023)**
- Authority: Metro Nashville / Urban Forestry Division
- Governs: Tree protection in ROW. Tree protection zones (minimum 10 ft around retained trees) must be maintained during construction. If pole foundation excavation is within critical root zone of a protected tree, mitigation or alternative placement required.
- Status: **CONDITIONAL** (applies if protected trees in work area)

### Stormwater and Floodplain

**Metro Nashville Stormwater Management Manual (2021) / Metro Code Title 15, Chapter 15.64**
- Authority: Metro Water Services
- Governs: Grading permit required for land disturbance >10,000 sq ft. Public utility installation exempt from grading permit but must comply with erosion and sediment control. Single-pole foundations are de minimis.
- Status: **CONDITIONAL** (generally exempt for single pole; applies if part of larger grading activity)

**Nashville Floodplain Overlay District / FEMA SFHA Regulations**
- Authority: Metro Water Services / FEMA
- Governs: If crosswalk is in Special Flood Hazard Area (SFHA), any development including pole installation requires local floodplain development permit. Electrical equipment must be elevated above base flood elevation + 4 ft (Nashville standard).
- Design impact: Nashville arterial corridors cross creeks. **Each crosswalk location needs floodplain screening before design.** Nolensville, Murfreesboro, and Gallatin Pikes all have creek crossings with adjacent floodplain.
- Status: **CONDITIONAL** (applies only at locations within SFHA; **HARD** when triggered)

---

## Part 2: Tennessee State

### Traffic and Roadway

**TDOT Traffic Operations Memo 2022**
- Authority: TDOT Traffic Operations
- Governs: Requires lighting design at midblock crossings and roundabouts. Establishes the "shall" requirement this proposal builds upon.
- Status: **HARD**

**TDOT Lighting Design Manual**
- Authority: TDOT
- Governs: All roundabouts and mid-block pedestrian crossings **shall** include lighting design per Traffic Operations Memo 2022. Silent on coordinated activation, beam geometry, fixture type.
- Status: **HARD** for the lighting mandate; silent on implementation detail (the gap this specification addresses)

**TDOT Traffic Design Manual — Chapter 15 (Roadway and Intersection Lighting)**
- Authority: TDOT
- Governs: Design procedures for highway lighting on state routes. References AASHTO, IES RP-8, and AASHTO LTS-6. Covers pole placement, mounting height, spacing, photometric design, electrical design.
- Status: **HARD** for state route installations

**TDOT 2021 Standard Specifications for Road and Bridge Construction — Section 714 (Roadway and Structure Lighting)**
- Authority: TDOT
- Governs: Material specifications, construction methods, and acceptance criteria for highway lighting installations on TDOT projects. Specifies fixture types, conductor sizes, conduit, grounding, testing.
- Status: **HARD** for TDOT contract work

**TDOT Standard Drawings**
- Authority: TDOT
- Governs: Standard details for pole foundations, wiring, conduit routing, mounting configurations. Notes designers "should also consider" adding or enhancing street illumination at midblock crossings.
- Status: **HARD** for construction details; **ADVISORY** for the illumination recommendation

**TDOT Utility Accommodation Policy — Tenn. Comp. R. & Regs. 1680-06-01**
- Authority: TDOT
- Governs: Any installation within state highway ROW requires a Use & Occupancy Permit. Specifies location and alignment criteria (no installations in median except extreme hardship), depth, materials, installation methods. TDOT inspector must be notified 3 days before work begins.
- Design impact: **Even solar-powered, off-grid installations in TDOT ROW require this permit.**
- Status: **HARD**

**Tennessee Code Annotated, Title 54 — Highways, Bridges and Ferries**
- Authority: Tennessee Legislature
- Governs: Statutory authority for TDOT over state highways. TCA 54-5-136 authorizes TDOT to remove unauthorized encroachments at owner's expense with 10 days' notice (or immediately if danger).
- Status: **HARD**

### Electrical, Building, and Fire

**Tennessee Electrical Code — NEC 2017 (State level)**
- Authority: TN Dept. of Commerce & Insurance
- Governs: Minimum electrical code statewide. Nashville supersedes with NEC 2023. State NEC 2017 applies in unincorporated areas not covered by Nashville's adoption.
- Status: **HARD**

**Tennessee State Fire Marshal — IFC 2021 (effective August 2025 per TN State Fire Marshal adoption schedule)**
- Authority: TN Dept. of Commerce & Insurance, Division of Fire Prevention
- Governs: Fire code for energy storage systems, electrical equipment. References NFPA 855 for ESS installations. Chapter 0780-02-02 contains Tennessee-specific amendments.
- Status: **HARD**

**Tennessee Board for Licensing Contractors — TCA 62-6-101 et seq.**
- Authority: TN Dept. of Commerce & Insurance
- Governs: Contractor licensing. Electrical work valued at $25,000+ requires state Contractor's license with CE (electrical) classification. Below that threshold, Nashville still requires local registration.
- Status: **HARD**

### Procurement

**Tennessee Procurement Act — TCA Title 12, Chapters 3 and 4**
- Authority: Tennessee Legislature
- Governs: Competitive bidding for public works. Formal bidding required for purchases $2,500+. Construction contracts $10,000-$1,000,000 require public advertisement and competitive bid. Professional services (engineering design) exempt from price bidding per TCA 12-4-106.
- Status: **HARD** for publicly funded installations

**TCA 12-4-903 — Prohibited Provisions in Bid Specifications**
- Authority: Tennessee Legislature
- Governs: Bid specs cannot specify a single brand or proprietary product without allowing "or equal" alternatives.
- Design impact: The system spec must be **performance-based, not brand-specific**. Cannot require "TAPCO SafeWalk" — must specify lumens, beam angle, mounting, and allow equivalent products.
- Status: **HARD** for publicly bid projects

### Environmental

**TDEC NPDES Construction General Permit (TNR100000)**
- Authority: Tennessee Dept. of Environment & Conservation
- Governs: Stormwater discharge from construction sites disturbing 1+ acres. Requires NOI filing 30 days before construction and active SWPPP.
- Status: **CONDITIONAL** (likely exempt for individual crossings; **HARD** if corridor-scale project disturbs 1+ acres)

**TCA 67-6-346 — Green Energy Production Facility Sales Tax Exemption**
- Authority: Tennessee Legislature / Dept. of Revenue
- Governs: Solar equipment (panels, inverters, batteries, racking) exempt from state sales tax when certified by TDEC.
- Design impact: Could reduce procurement costs for public agencies. Requires application.
- Status: **ADVISORY** (optional tax benefit)

**Tennessee Nongame and Endangered or Threatened Wildlife Species Conservation Act of 1974 (TCA 70-8-101 et seq.)**
- Authority: Tennessee Wildlife Resources Agency
- Governs: State-level protection for listed species. Applies regardless of federal funding. Minimal ground disturbance for pole installation unlikely to trigger.
- Status: **HARD** (but unlikely to be implicated)

### Occupational Safety

**TOSHA — Tennessee Occupational Safety and Health Act (TCA 50-3-101 et seq.)**
- Authority: TN Dept. of Labor & Workforce Development
- Governs: Workplace safety during installation. Tennessee operates a state OSHA plan covering private sector and state/local government workers. Adopts federal OSHA standards for construction (29 CFR 1926) including electrical safety, fall protection for pole work. MUTCD Part 6 governs temporary traffic control during installation.
- Status: **HARD**

### Liability

**Tennessee Governmental Tort Liability Act (TCA 29-20-101 et seq.)**
- Authority: Tennessee Legislature
- Governs: Limits liability of state and local government for discretionary acts (including design decisions). Installation of a safety improvement is a discretionary act protected by sovereign immunity. However, duty to maintain once installed creates ongoing obligation.
- Design impact: Protective of the installing agency. Failsafe design and data logging further reduce liability exposure. See safety analysis in system design spec.
- Status: **HARD** (shapes legal framework; favorable to this project)

---

## Part 3: Federal / National

### Traffic Engineering and Roadway Design

**MUTCD 11th Edition with Revision 1 (2025) — Chapter 4L**
- Authority: FHWA
- Governs: RRFB device standards, placement, flash pattern, sign requirements. Notes lighting "should" be a prerequisite for RRFB installation. No coordinated activation spec.
- Status: **HARD** for RRFB device compliance; **ADVISORY** for lighting as prerequisite

**23 CFR Part 655, Subpart F — Traffic Control Devices on Federal-Aid Highways**
- Authority: FHWA
- Governs: All traffic control devices on public roads must conform to the MUTCD. States must adopt in "substantial conformance" within 2 years of issuance.
- Status: **HARD**

**23 CFR Part 625 — Design Standards for Highways**
- Authority: FHWA
- Governs: NHS projects must conform to AASHTO design standards including AASHTO LTS-6 for structural supports.
- Status: **HARD** for NHS projects; **CONDITIONAL** for others with federal-aid funds

**FHWA Interim Approval IA-21 — Rectangular Rapid-Flashing Beacons**
- Authority: FHWA
- Governs: Technical requirements for RRFB installation. Now superseded by MUTCD 11th Ed. codification, but conditions remain reference standard. The illumination system must not modify or interfere with RRFB operation.
- Status: **HARD**

**FHWA Informational Report on Lighting Design for Midblock Crosswalks (FHWA-HRT-08-053)**
- Authority: FHWA
- Governs: Design guidance for crosswalk illumination. Establishes 28ft (8.5m) as optimal mounting height for crosswalk luminaires, 10-20ft offset from crosswalk, and 20 lux vertical at 1.5m as the illuminance target. Also establishes that pedestrian-area luminaire heights (10-25ft per FHWA general guidance, 10-15ft per TDOT) apply to walkway/decorative fixtures, not crosswalk activation luminaires.
- Status: **ADVISORY**

### AASHTO Standards

**AASHTO Roadway Lighting Design Guide (2018)**
- Authority: AASHTO (referenced by FHWA)
- Governs: Reinforces IES RP-8 illuminance criteria. Referenced by state DOTs for design policy. Addresses crosswalk lighting but not coordinated activation.
- Status: **ADVISORY** (becomes **HARD** when referenced in state design manuals or federal-aid project requirements)

**AASHTO LTS-6 — Standard Specifications for Structural Supports for Highway Signs, Luminaires, and Traffic Signals (6th Ed.)**
- Authority: AASHTO (referenced in 23 CFR 625)
- Governs: Structural design of luminaire poles — wind loading, fatigue, foundation, material specs, fabrication. Any pole supporting a fixture in highway ROW must comply.
- Status: **HARD** for federal-aid NHS projects; **ADVISORY** otherwise but universally referenced by TDOT

**AASHTO Roadside Design Guide — Clear Zone Requirements**
- Authority: AASHTO
- Governs: Pole placement lateral offset from traveled way. Clear zone width based on speed, volume, slope. Poles within clear zone must be breakaway-compliant. On curbed urban roads (Nashville arterials), minimum 1.5 ft lateral offset from face of curb.
- Status: **HARD** for federal-aid projects; standard practice otherwise

**AASHTO MASH — Manual for Assessing Safety Hardware (2016)**
- Authority: AASHTO/FHWA
- Governs: Crash-testing criteria for roadside hardware including luminaire pole bases. All new luminaire supports on the NHS must have FHWA eligibility letters demonstrating MASH compliance. Breakaway or yielding base design required for poles within the clear zone.
- Design impact: Pole base selection must be MASH-tested with FHWA eligibility letter.
- Status: **HARD** for new installations on NHS with federal aid

### Illumination Standards

**ANSI/IES RP-8-25 — Roadway and Intersection Lighting**
- Authority: ANSI/IES
- Governs: 20 lux vertical at 1.5m above crosswalk surface; 14 lux horizontal average maintained minimum; max 4:1 uniformity ratio. The definitive standard for crosswalk illumination.
- Status: **ADVISORY** standalone; **HARD** when referenced by TDOT or local design manuals

**IES TM-15-20 — Luminaire Classification System (BUG Ratings)**
- Authority: IES
- Governs: Backlight, Uplight, and Glare rating system for outdoor luminaires. Replaces deprecated cutoff/semi-cutoff classification. Required by Nashville dark sky ordinance for characterizing fixture performance.
- Status: **ADVISORY** standalone; **HARD** when Nashville dark sky ordinance references it

**FHWA Lighting Handbook (2012)**
- Authority: FHWA
- Governs: Design guidance for roadway and intersection lighting including luminaire selection using IES TM-15 BUG system.
- Status: **ADVISORY**

### Electrical and Fire Codes

**NFPA 70 (NEC) — National Electrical Code**
- Authority: NFPA (adopted by Tennessee and Nashville)
- Governs: All electrical installation. Key articles for this project:
  - **Art. 690** — Solar PV: Rapid shutdown (690.12), disconnecting means, wiring, grounding, overcurrent protection
  - **Art. 706** — Energy Storage Systems: Installation, disconnecting means, overcurrent protection for LiFePO4 battery
  - **Art. 411** — Low-Voltage Lighting (48V DC circuits)
  - **Art. 250** — Grounding and Bonding
  - **Art. 300** — Wiring Methods (outdoor, wet location)
  - **Art. 725** — Class 1/2/3 Remote Control, Signaling, Power-Limited Circuits (detection/control wiring)
- Status: **HARD**

**NFPA 855 — Standard for Installation of Stationary Energy Storage Systems**
- Authority: NFPA
- Governs: Fire safety for the LiFePO4 battery bank. Spacing, ventilation, thermal runaway protection, detection. 2026 edition introduces TRPP requirements.
- Status: **HARD** where adopted (Tennessee IFC 2021 references it)

**International Fire Code (IFC) 2021**
- Authority: ICC (adopted by Tennessee)
- Governs: Fire safety for energy storage systems, electrical equipment. References NFPA 855 for ESS installations.
- Status: **HARD**

### Accessibility

**ADA — Americans with Disabilities Act (42 USC 12101 et seq.)**
- Authority: Federal
- Governs: Installation must not create barriers to pedestrian access. Pole placement must maintain minimum clear sidewalk width. Any new pedestrian interface must be ADA-compliant.
- Status: **HARD**

**PROWAG — Public Right-of-Way Accessibility Guidelines (Final Rule, effective Sept 7, 2023)**
- Authority: US Access Board (adopted by USDOT Dec 2024)
- Governs: Accessibility for sidewalks, crosswalks, curb ramps, pedestrian signals in public ROW. Pole placement must not reduce pedestrian access route below minimum width. Pushbutton height and reach range requirements.
- Status: **HARD** for new construction/alterations with federal funding; increasingly standard of care regardless

### Environmental

**NEPA — National Environmental Policy Act (42 USC 4321 et seq.) / 23 CFR 771**
- Authority: FHWA/CEQ
- Governs: Environmental review for federally funded transportation projects. Pedestrian safety improvements typically qualify for **Categorical Exclusion (CE)** under 23 CFR 771.117(c)(3) and (c)(28) — no EA or EIS required.
- Status: **CONDITIONAL** (applies only with federal funding; likely CE, not a barrier)

**Section 106 — National Historic Preservation Act (54 USC 306108 / 36 CFR Part 800)**
- Authority: Advisory Council on Historic Preservation / SHPO
- Governs: Effects on historic properties for federally funded/permitted projects. If installing near a property on the National Register, SHPO consultation required. Tennessee Historical Commission is the SHPO.
- Status: **CONDITIONAL** (federal funds AND near historic properties)

**Section 4(f) — USDOT Act of 1966 (49 USC 303)**
- Authority: USDOT/FHWA
- Governs: Restricts use of land from publicly owned parks, recreation areas, wildlife refuges, or historic sites. Pole installation adjacent to a park or historic property could trigger review. De minimis finding likely for a single pole.
- Status: **CONDITIONAL** (federal funding AND protected property)

**Endangered Species Act — Section 7 (16 USC 1536)**
- Authority: USFWS
- Governs: Federal agencies must consult when actions may affect listed species. Nashville area has listed species (Indiana bat, etc.). Programmatic or informal consultation typically sufficient for pole installation.
- Status: **CONDITIONAL** (federal nexus only; likely resolved through programmatic agreement)

### Procurement

**Buy America Act / Build America, Buy America (BABA) — 23 USC 313 / 23 CFR 635.410**
- Authority: FHWA
- Governs: If federal highway funds used, all steel, iron, and manufactured products must be domestically produced. As of Oct 1, 2025, final assembly in US. As of Oct 1, 2026, manufactured products must have >55% domestic components by cost. Applies to LED fixtures, poles, solar panels, battery enclosures, controllers.
- Design impact: Fixture and component sourcing must verify domestic manufacturing compliance if federal funds are used.
- Status: **CONDITIONAL** (applies only with federal funds; **HARD** when triggered)

### Communications and Electronics

**FCC 47 CFR Part 15 — Radio Frequency Devices**
- Authority: FCC
- Governs: Any device that radiates RF energy — LED drivers, microcontrollers, LoRaWAN/cellular modem. LED drivers are unintentional radiators requiring Part 15 compliance. All equipment must be FCC certified or verified.
- Status: **HARD**

**FCC 47 CFR Part 15.247 — Spread Spectrum / Digital Modulation (902-928 MHz)**
- Authority: FCC
- Governs: Specifically governs the LoRaWAN radio module (915 MHz ISM band). No duty cycle limit in US. Max 1W transmit power. No individual license required but equipment must bear FCC ID.
- Status: **HARD**

### Product Safety Certification

**UL 1598 — Standard for Luminaires**
- Authority: UL/ANSI
- Governs: Safety certification for LED luminaire assembly. Wiring, grounding, spacing, temperature, enclosure, wet location suitability. NEC requires listed equipment.
- Status: **HARD**

**UL 8750 — Standard for LED Equipment for Use in Lighting Products**
- Authority: UL
- Governs: Safety of LED modules, arrays, controllers, drivers within the luminaire. Required as component of UL 1598 listing.
- Status: **HARD**

**UL 2703 — Standard for Mounting Systems for Solar PV Modules**
- Authority: UL
- Governs: Structural integrity, electrical grounding, bonding of solar panel mounting system. NEC requires PV mounting tested and listed to UL 2703.
- Status: **HARD**

**UL 9540 — Standard for Energy Storage Systems and Equipment (3rd Ed. 2023)**
- Authority: UL
- Governs: System-level safety for LiFePO4 battery bank plus charge controller as ESS. Referenced by NFPA 855 and IFC.
- Status: **HARD** where NFPA 855 or IFC enforced (Nashville)

**UL 9540A — Test Method for Evaluating Thermal Runaway Fire Propagation in Battery ESS**
- Authority: UL
- Governs: Thermal runaway propagation test for lithium battery systems. Referenced by NFPA 855 (2026) for spacing and fire protection requirements.
- Status: **CONDITIONAL** (required by NFPA 855 for certain ESS sizes/configurations)

### Structural

**ASCE 7-22 — Minimum Design Loads for Buildings and Other Structures**
- Authority: ASCE (referenced by IBC and AASHTO)
- Governs: Wind loads (Nashville: 115 mph basic wind speed, Risk Category II), ice loads, seismic loads for pole and mounting arm. Chapter 29 covers wind loads on poles.
- Status: **HARD**

**IBC 2021 — Section 1807.3 (Pole Foundations)**
- Authority: ICC (adopted by Tennessee/Nashville)
- Governs: Foundation design for poles embedded in earth or concrete footings. Lateral bearing pressures, depth requirements.
- Status: **HARD**

### Electrical Safety (Field Installation)

**NESC — National Electrical Safety Code (ANSI C2)**
- Authority: IEEE
- Governs: Clearance requirements for pole-mounted electrical equipment over roadways and near utility lines. If mounting on or adjacent to NES utility poles, NESC clearances apply. Governs worker safety during installation.
- Status: **HARD** (NES requires NESC compliance for anything near their infrastructure)

### Communications Protocol

**NTCIP 1213 v03 — Object Definitions for Electrical and Lighting Management Systems (ELMS)**
- Authority: NEMA/USDOT ITS Standards
- Governs: Communications protocol for remote monitoring/control of roadway lighting. Defines data objects and commands if system connects to municipal traffic management center.
- Status: **ADVISORY** (good practice; not required unless specified in procurement)

### Energy Efficiency Qualification

**DLC (DesignLights Consortium) — Qualified Products List / LUNA Program**
- Authority: DLC
- Governs: Energy efficiency and performance qualification for LED outdoor luminaires. DLC SSL V6.0 requires 14% higher efficacy than V5.1. CCT capped at 5000K. LUNA V2.0 adds responsible outdoor lighting criteria. Many utility rebate programs and procurement specs require DLC listing.
- Status: **ADVISORY** (increasingly required in municipal procurement and for utility incentive eligibility)

### Enclosure Ratings

**NEMA 250 — Enclosures for Electrical Equipment**
- Authority: NEMA
- Governs: NEMA 4X rating required for outdoor controller and battery enclosures (watertight, dust-tight, corrosion-resistant, ice-resistant).
- Status: **HARD** (NEC requires suitable enclosures; NEMA 4X is the appropriate rating for this application)

**IEC 60529 — Ingress Protection (IP) Ratings**
- Authority: IEC (referenced domestically)
- Governs: IP66 minimum for outdoor electrical enclosures. Approximately equivalent to NEMA 4X but without corrosion/ice testing.
- Status: **ADVISORY** (NEMA rating is primary in US; IP rating useful for sourcing international components)

---

## Part 4: Design Flags

Items discovered during codes review that require design changes or site-specific screening:

### Design Changes Required

1. **CCT — pursuing 4000K** — Nashville dark sky ordinance BL2020-535 caps at 3000K, but Research supports improved pedestrian detection at higher CCT (~20% at 4000K vs 3000K per IPWEA). Three paths to authorization: (a) TDOT state-route jurisdictional argument, (b) BL2022-1088 variance for safety, (c) legislative precedent (Maine LD 1934). Fallback to 3000K with increased lumen output. Fixture spec includes tunable-white/swappable module. **(IN PROGRESS)**

2. **MASH-compliant breakaway base** — Any pole within the clear zone on a federal-aid NHS road must have a MASH-tested breakaway or yielding base with FHWA eligibility letter. Must be specified in pole procurement.

3. **NEC 2023 rapid shutdown (Art. 690.12)** — Solar PV array must have rapid shutdown system. Charge controller typically serves as rapid shutdown initiator for standalone pole-mounted systems. Must be specified in electrical design.

4. **UL listings required** — All major components must be listed: luminaire (UL 1598 + UL 8750), solar mounting (UL 2703), ESS (UL 9540). Must be specified in procurement.

5. **Performance-based specification** — TCA 12-4-903 prohibits single-brand specs on publicly bid projects. Cannot require "TAPCO SafeWalk" — must specify lumens, beam angle, mounting, and allow "or equal" alternatives.

6. **Buy America compliance** — If federal funds used, all manufactured products must meet domestic content requirements. Must verify domestic manufacturing for fixture, solar panel, battery, controller.

7. **TDOT encroachment permit** — Even solar-powered, off-grid installations in TDOT ROW require a Use & Occupancy Permit per Tenn. Comp. R. & Regs. 1680-06-01. Required even for solar-powered, off-grid installations.

### Site-Specific Screening Required (Per Crossing)

8. **Floodplain check** — Nashville arterials cross creeks. Each crossing location must be screened against FEMA SFHA maps. If in floodplain, electrical equipment must be elevated above BFE + 4 ft.

9. **Historic overlay check** — Several corridors pass through or near historic overlay districts. If in overlay, pole design/appearance may require Historic Zoning Commission approval.

10. **Tree canopy check** — If pole foundation excavation is within critical root zone (10 ft) of a protected tree, mitigation or alternative placement required per BL2022-1409.

11. **NES pole proximity check** — If mounting near existing NES infrastructure, NESC clearances apply and NES coordination required regardless of solar power source.

12. **Clear zone analysis** — Pole lateral offset from traveled way must meet AASHTO Roadside Design Guide requirements for the road's speed and volume classification.

---

## Part 5: Non-Regulatory but Implementation-Critical

These are not codes or laws but affect whether and how installations happen:

- **Nashville Vision Zero Action Plan** — Policy direction supporting this project. Creates institutional alignment for funding and prioritization.
- **TDOT HSIP / SS4A Program Guidance** — Federal grant eligibility and documentation requirements for funded projects.
- **Metro Nashville Capital Improvements Budget Process** — Internal budget allocation. Jurisdictional split (traffic engineering vs public works) requires cross-department champion.
- **ITE Recommended Practice / ITE Journal Publications** — Professional society guidance that establishes standard of care and influences design defensibility.
- **FHWA CMF Clearinghouse** — No Crash Modification Factor exists for coordinated crosswalk illumination. Establishing one through pilot evaluation data is the path to national adoption.
