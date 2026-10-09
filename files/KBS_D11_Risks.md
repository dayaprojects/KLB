# KBS — D11 · Risk Register

> **Covers:** `KLB_v3.md` §17 (risk register) · **Depends on:** D0–D10
> **Scales:**
> - **Likelihood (L):** 1 rare · 2 unlikely · 3 possible · 4 likely · 5 almost certain.
> - **Impact (I):** 1 minor · 2 moderate · 3 serious · 4 major · 5 critical.
> - **Score = L × I**. ≥ 15 = red (Board attention every quarter); 8–14 = amber (Audit & Risk Committee); ≤ 7 = green (owner).
>
> **Owner:** the accountable role (D9). **Trigger:** the observable signal that activates the contingency.

## 1. Register

| ID | Risk | L | I | Score | Owner | Mitigation (preventive → contingency) | Trigger |
|---|---|---|---|---|---|---|---|
| RISK-001 | **Recognition failure:** certificates not accepted by ministries, universities or employers | 3 | 5 | **15** | Head of Recognition | Anchor users before launch (D9 §4); recognition dossier; ministry observers on committees; score-use statements (D2 §1.3) → re-target anchor users (employers, NGOs, diaspora authorities); delay go-live | < 2 anchor users signed at Phase 1 gate |
| RISK-002 | **Dialect and orthography politics:** accusations of favouring one variety, sub-variety or orthography | 4 | 4 | **16** | Chairs, Standards Committees | Separate tracks (AD-001); equal-standing committees; AVP based on internal consistency; neutrality rule (AD-036); transparent decisions → independent review by the International Academic Advisory Board; public consultation | Public campaign or formal complaint by a recognised body |
| RISK-003 | **Small calibration samples**, esp. `kmr-Latn` and `kmr-Arab` | 4 | 4 | **16** | Head of Psychometrics | Paid pilots (D2 §5.3); single Kurmanji bank (AD-011); Rasch; pooling across windows → extend the pilot; delay `kmr-Latn` launch; report wider SEMs | Pilot n < 200 per tier for a track |
| RISK-004 | **Item leaks** (Telegram, social channels, test-prep) | 4 | 4 | **16** | Integrity officer | Exposure caps, form rotation, watermarking, leak monitoring, kiosk lockdown (D7 §3) → breach playbook; invalidate and retake (AD-029) | Fingerprint match found; anomalous facility jump |
| RISK-005 | **Power or connectivity failure** during sessions | 5 | 2 | **10** | Head of Operations | Laptops (ADR-011), UPS, offline S2, autosave, exact-time resume, paper fallback (D3, D4) → void + free retake | Outage > UPS duration; I-3 rate > 2 per 100 sessions |
| RISK-006 | **Candidate data exposure** (breach or compelled access), with harm to at-risk candidates | 2 | 5 | **10** | DPO | Minimisation, EU hosting, AD-028, encryption, region partitioning, transparency report → breach response (D7 §6.7); candidate safety notices | Security incident involving C3; government data request |
| RISK-007 | **Key-person dependency** on scarce Kurdish psychometric expertise | 4 | 4 | **16** | Executive Director | International partner with capacity transfer (A-05); dual computation (AD-032); documented pipelines; train 2 local analysts → partner surge contract | Departure of the Head of Psychometrics or a partner exit |
| RISK-008 | **Vendor lock-in** | 2 | 3 | 6 | CTO | Open-source stack; containers; S3-compatible storage; IDML exit path for InDesign (ADR-010) → migrate using portability tests (NFR-PORT-001) | Price or licence change by a critical vendor |
| RISK-009 | **Automated-scoring bias** against varieties, sub-varieties or groups (Phase 3+) | 3 | 4 | 12 | Head of Psychometrics | Gates (D6 §7); second-rater use only; subgroup fairness monitoring → suspend automated scoring | Subgroup SMD > 0.10 in monitoring |
| RISK-010 | **Funding sustainability**: fee income cannot cover fixed costs (D10 §3.7) | 4 | 5 | **20** | Executive Director + Board | Seek a public mandate; multi-year grants; institutional contracts; cost-recovery gates; AD-035 funding cap → scale back to core tracks and fewer centres; Series cross-subsidy for the Hub | Cost recovery below gate (25 % Ph2, 40 % Ph3); runway < 9 months |
| RISK-011 | **IP / trade-dress claim** from close emulation of DK *English for Everyone* | 3 | 4 | 12 | Head of Legal | New content only; originality checks; legal look-and-feel opinion before the design brief; distinct cover, brand and primary colours (DN-16); exploratory DK licence enquiry → redesign affected elements; licence negotiation | Legal opinion flags risk; DK contact; cease-and-desist |
| RISK-012 | **Orthography disputes in printed books** (e.g., ە/ه, ڵ, Kurmanji Arabic-script conventions) | 4 | 3 | 12 | Series editor + Standards Committees | Committee-approved orthography standard per edition (D16); two native proofreaders; pilot feedback → errata; corrected reprints; digital edition updated first | Errata rate > threshold; public complaints |
| RISK-013 | **Test-prep leakage through Series content** (books aligned to items, not the construct) | 2 | 4 | 8 | Executive Director | Firewall (DN-22); separate systems (CON-015); 12-month cooling-off; n-gram similarity check (D4 §4.6); placement test uses only retired items → withdraw affected content; retire exposed items | Similarity check hit; item facility rise linked to Series content |
| RISK-014 | **Shortage of experienced Kurdish materials writers** | 4 | 3 | 12 | Series editor | Author training (D9 §6); paired authoring (senior + junior); staggered title schedule; diaspora writers → reduce the Phase 1 title list (Starter + L1 first) | Units behind schedule > 20 % |
| RISK-015 | **Legal status uncertainty:** foundation cannot certify, or recognition needs a public body | 3 | 5 | **15** | Head of Legal | Early legal opinion (Phase 0); fallback to a university-hosted unit with an independence charter (DN-03) | Registration or MoU blocked |
| RISK-016 | **Political interference** in governance, results or committee appointments | 3 | 4 | 12 | Board chair | AD-036 neutrality; open appointments; IAAB suspensive veto; pressure-reporting channel → public statement; escalate to the funders' governance clause | Reported pressure; irregular appointment attempt |
| RISK-017 | **Delivery-client spike fails** (WebKitGTK Kurdish shaping or durability) | 2 | 3 | 6 | CTO | 2-week spike (ADR-005) → Electron fallback with the same local store | Spike acceptance tests fail |
| RISK-018 | **Rater shortage**, esp. certified Kurmanji Arabic-script raters | 3 | 4 | 12 | Rating quality manager | Early recruitment in Duhok; diaspora raters (remote); training pipeline; MFRM to manage severity → extend release SLA for affected tracks | Pool < 1.5× required capacity before a window |
| RISK-019 | **Low `kmr-Arab` demand** makes the track uneconomic | 3 | 2 | 6 | Head of Assessment | DN-05 threshold (< 50 candidates/year → defer to Phase 2) → candidates offered `kmr-Latn` or `ckb` | Pilot interest < threshold |
| RISK-020 | **Centre staff collusion** with candidates | 3 | 4 | 12 | Head of Operations | Two invigilators; random inspections; CCTV where lawful; statistical monitoring; de-accreditation policy → hold results; investigate (D7 §5) | Statistical anomaly by centre; tip-off |
| RISK-021 | **Hostile-state targeting** of candidates, staff or systems (TA-7) | 2 | 5 | 10 | Security lead | AD-028; minimisation; EU hosting; staff security training; coercion channel → incident response; candidate notification; legal support | Intrusion attempt; targeted phishing; staff report |
| RISK-022 | **Series name / trademark conflict** ("Pêngav") | 2 | 3 | 6 | Head of Legal | Trademark search before branding (DN-15) → alternative name list ready | Search returns a conflicting mark |
| RISK-023 | **Accessibility gaps** (Kurdish TTS and screen readers immature) excluding disabled candidates | 3 | 3 | 9 | Candidate Services | Human readers; accessible paper; Phase 2 accessibility study; published policy (D2 §4.9) → individual arrangements | Accommodation requests unmet; complaints |
| RISK-024 | **Diaspora pilot recruitment shortfall** (safety concerns deter participation) | 3 | 3 | 9 | Head of Recognition | Community partners; safety-first messaging (data minimisation, EU hosting); honoraria → extend the pilot window; add a second diaspora location | < 60 % of target recruited by mid-pilot |
| RISK-025 | **Standard-setting validity challenge** (panel composition or method criticised) | 2 | 4 | 8 | Head of Psychometrics | CoE Manual process; balanced panels; cross-moderators; replication (D2 §5.5) → independent re-run | External critique; replication difference > 2 SE |
| RISK-026 | **Demand for a single "standard Kurdish" test** from a powerful stakeholder | 3 | 3 | 9 | Executive Director | Variety rationale published (AD-001); a single certificate format across tracks; Bridge endorsement in Phase 3 → stakeholder engagement; keep tracks | Formal request from a ministry |
| RISK-027 | **Currency and inflation volatility** (IQD) erodes fee value | 3 | 2 | 6 | Finance | Annual price review; USD-indexed price policy `[DECISION NEEDED]` → interim fee adjustment | IQD/USD move > 10 % |
| RISK-028 | **Payment rail disruption** (wallet provider outage or regulatory change) | 3 | 2 | 6 | Finance | Multiple rails + cash + vouchers (FR-PAY) → extend seat holds; cash at centre | Provider outage > 24 h near booking close |
| RISK-029 | **Washback harm:** narrow test preparation; heritage learners discouraged by literacy-weak results | 3 | 3 | 9 | Head of Assessment | Per-skill reporting with positive "what you can do" statements (D6 §6); Heritage Fast-Track; teacher training → communication campaign; review task types | Survey shows test-prep narrowing; heritage drop-off |
| RISK-030 | **Insider leak** of C4 content by staff or committee members | 2 | 5 | 10 | Security lead | Least privilege, SoD, export dual control, watermark tracing, background checks → disciplinary and legal action; content replacement | Watermark trace to an internal variant |

## 2. Heat map (current scores)

| Impact ↓ / Likelihood → | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| **5** | | 006, 021, 030 | 001, 015 | 010 | |
| **4** | | 013, 025 | 009, 011, 016, 018, 020 | 002, 003, 004, 007 | |
| **3** | | 008, 017, 022 | 023, 024, 026, 029 | 012, 014 | |
| **2** | | | 019, 027, 028 | | 005 |

**Red (≥ 15):** RISK-010 (20), RISK-002, RISK-003, RISK-004, RISK-007 (16), RISK-001, RISK-015 (15).

## 3. Governance of the register
- **Review:** owners update monthly; the Audit & Risk Committee reviews quarterly; the Board reviews red risks quarterly.
- **New risks:** any staff member can raise one. The integrity, privacy and security teams add risks from incidents automatically.
- **Linkage:** each mitigation maps to a requirement, decision or control ID (D13). Each red risk has a KPI watch (D12).

## Changes to prior deliverables
- **D10 §3.7 / RISK-010:** funding sustainability is the top-scored risk. The owner decision on mandate and funding strategy is `[DECISION NEEDED]` before the Phase 0 gate.
- **RISK-027:** new `[DECISION NEEDED]` on whether to index fees to USD.

## §19 self-check
- ✅ Every risk named in §17 is included (001–004, 005, 006, 007, 008, 009, 010, 011, 012, 013, 014), plus 16 project-specific risks.
- ✅ Varieties and scripts (002, 003, 012, 018, 019, 026); offline (005); candidate safety (006, 021, 024).
- ✅ Mitigations reference concrete decisions and controls; triggers are observable.

**Next deliverable: D12 — KPI framework.**
