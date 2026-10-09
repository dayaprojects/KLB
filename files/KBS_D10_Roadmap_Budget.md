# KBS — D10 · Roadmap, Budget & Staffing

> **Covers:** `KLB_v3.md` §17 (roadmap, budget, staffing) · **Depends on:** D1 (MVP scope), D2–D9
> **All money figures are `[ASSUMPTION]` ranges in USD.** They are built from stated unit assumptions, not vendor quotes. **No partner or funder commitments are assumed.** Unit-cost assumptions are listed in §3.1 so they can be replaced with local quotes.

---

## 1. Roadmap

```mermaid
gantt
    title KBS roadmap (indicative; months from start)
    dateFormat X
    axisFormat M%s
    section Phase 0 Foundations
    Legal entity, governance, MoUs            :p0a, 0, 9
    Construct & variety decisions, descriptors :p0b, 0, 8
    RLD v0.5                                  :p0c, 0, 11
    DPIA, policies                            :p0d, 3, 10
    Architecture + client spike (ADR-005)     :p0e, 4, 9
    Series: style audit, ordinance, sample units :p0f, 3, 11
    section Phase 1 MVP / Pilot
    Platform MVP build                        :p1a, 9, 20
    Item development + cognitive labs         :p1b, 8, 13
    Pilot + calibration + standard setting    :p1c, 12, 20
    Centres accredited (4)                    :p1d, 14, 20
    Series MVP (10 books) + Hub v1            :p1e, 10, 24
    First live window                         :milestone, m1, 22, 22
    section Phase 2 Limited release
    More centres incl. diaspora               :p2a, 24, 40
    VCs, institutional portal, MFRM live      :p2b, 24, 36
    Series L3–L4, Grammar, Vocab, kmr-Arab ed. :p2c, 24, 46
    section Phase 3 Scale
    KBS Academic, MST, research tracks        :p3a, 46, 70
    section Phase 4 Broad
    CAT (if gated), new varieties, Junior/Professional :p4a, 70, 96
```

### 1.1 Phase definitions

| Phase | Duration | Scope | Go / no-go exit criteria | Team (avg FTE) | Phase KPIs (D12) |
|---|---|---|---|---|---|
| **0 Foundations** | 9–12 months | Legal entity + charter (D9); Board and committees seated; DN decisions ratified; descriptors adapted (S-02); RLD v0.5; DPIA; ministry MoUs (D9 §4); architecture + client spike; EFE style audit → house style (D16); one sample unit per variety (D17) piloted with ≥ 20 learners | (1) Entity registered with certification capacity confirmed `[VERIFY]`; (2) ≥ 1 ministry MoU signed; (3) funding for Phase 1 secured at ≥ 80 % of low-case budget; (4) client spike passes (shaping + power-pull); (5) Standards Committees approve AVP v1 draft and Series orthography v1 | 12–16 | — (set baselines) |
| **1 MVP / Pilot** | 12–18 months | D1 §1.2 Must-haves: KBS General F/A in `ckb`, `kmr-Latn`, `kmr-Arab`; fixed forms; centre CBT + paper; human rating; signed PDF + QR; 4 launch sites; pilot, calibration, standard setting. Series: Script & Literacy Starter + L1–L2 Course & Practice (Sorani, Kurmanji Latin) + Hub v1. | (1) Quality targets met in pilot (D2 §5.7) for ≥ 2 tracks, with a plan for the third; (2) standard setting completed for each variety; (3) pen test + red team: no open high or critical findings; (4) all 4 centres pass the offline dry run; (5) ≥ 2 anchor users (D9 §4) agree to accept results; (6) Series L1 pilot: ≥ 70 % of completers reach A1 on the placement test | 35–45 | KPI-001…012, KPI-023, KPI-024 |
| **2 Limited release** | 18–24 months | More centres (2–4 KRI + 1–2 diaspora); institutional portal; VCs (ADR-008 Ph2); MFRM monitoring live; first formal recognitions; standard-setting replication; bilingual comparability study (S-12). Series: L3–L4, Grammar Guides, Vocabulary Builder, Kurmanji Arabic-script editions, Teacher's Guides, Heritage Fast-Track. | (1) ≥ 5 recognising bodies (KPI-013); (2) quality targets met in ≥ 4 consecutive windows; (3) cost recovery ≥ 25 % (KPI-029); (4) no unresolved I-4 security incidents; (5) annual technical report published | 50–65 | All KPIs |
| **3 Scale** | ~24 months | KBS Academic; MST (if gated); remote-proctoring pilot; automated scoring as a research second rater; ALTE full membership + Q-mark preparation; ISO 27001 certification. Series: Kurdish for Work, Sorani ↔ Kurmanji Bridge, Level 5 / Academic Kurdish. | Gates in D2 §5.6 and D8 §8 per feature; cost recovery ≥ 40 % | 60–80 | — |
| **4 Broad** | Open-ended | CAT if gated; additional varieties (Southern Kurdish, Hawrami; Zazaki subject to policy); KBS Junior and Professional; Junior series | Per-feature gates | — | — |

### 1.2 Critical path and dependencies
1. **Entity + certification capacity → recognition MoUs → anchor users.** Without these, the pilot has no purpose (RISK-001).
2. **Descriptors + RLD v0.5 → item writing → cognitive labs → pilot → calibration → standard setting → first live window.** This is the longest chain, about 22 months.
3. **Client spike (ADR-005) → delivery client build → centre dry runs.** A failed spike costs about 2 months (Electron fallback).
4. **House style (D16) + orthography v1 → Series authoring → pilot → print.** The Series does not block testing.

---

## 2. Staffing (roles × phase × FTE ranges)

| Unit / role | Ph 0 | Ph 1 | Ph 2 | Ph 3 | Notes |
|---|---|---|---|---|---|
| Executive Director | 1 | 1 | 1 | 1 | |
| Finance & administration | 1–2 | 2 | 2–3 | 3 | |
| Head of Assessment | 1 | 1 | 1 | 1 | |
| Head of Psychometrics | 0.5 (partner) | 1 | 1 | 1 | International partner covers gaps (A-05) |
| Psychometricians / data analysts | 0–1 | 2 | 2–3 | 3–4 | Dual computation (AD-032) needs ≥ 2 |
| Item development manager | 0.5 | 1 | 1 | 1–2 | |
| Item writers (contract, FTE equiv.) | 1–2 | 6–8 | 4–6 | 6–8 | Split across `ckb` and `kmr` |
| Reviewers (contract, FTE equiv.) | 0.5 | 2–3 | 2 | 3 | Linguistic, bias, script |
| Standards Committees (honoraria, FTE equiv.) | 1 | 1 | 1 | 1.5 | 14 members part-time |
| Rating quality manager | — | 1 | 1 | 1–2 | |
| Raters (sessional, FTE equiv.) | — | 2–4 | 4–8 | 8–15 | Scales with volume |
| Operations head + centre coordinators | 0.5 | 3–5 | 5–7 | 7–9 | |
| Candidate Services / support | — | 2–3 | 3–5 | 5–7 | Multilingual |
| CTO | 1 | 1 | 1 | 1 | |
| Backend engineers (Python/Django) | 1 | 3–4 | 3–4 | 4–5 | |
| Frontend engineers (htmx + React/TS) | 0.5 | 2 | 2 | 2–3 | |
| Client engineer (Rust/Tauri) | 0.5 (spike) | 1 | 1 | 1 | Scarce locally; partner backup |
| DevOps / SRE | 0.5 | 1 | 1–2 | 2 | |
| Security lead | 0.5 | 1 | 1 | 1 | |
| QA / test engineers | — | 1–2 | 2 | 2 | Centre lab |
| DPO / privacy | 0.5 | 0.5–1 | 1 | 1 | |
| Integrity officer | — | 0.5 | 1 | 1 | |
| Legal (retainer, FTE equiv.) | 0.3 | 0.3 | 0.5 | 0.5 | |
| Recognition & partnerships | 1 | 1 | 2 | 2 | |
| Communications | 0.5 | 1 | 1 | 1–2 | |
| **Series editor-in-chief** | 0.5–1 | 1 | 1 | 1 | |
| Series authors (contract, FTE equiv.) | 1 | 4–6 | 6–8 | 4–6 | Per variety |
| Designers / layout | 0.5 | 2 | 2–3 | 2 | ADR-010 |
| Illustrators (contract, FTE equiv.) | 0.3 | 2–3 | 2–3 | 1–2 | |
| Audio producer (+ voice talent sessional) | — | 1 | 1 | 1 | |
| Proofreaders (contract) | — | 1 | 1–2 | 1 | Two per edition (D16) |
| **Total (approx.)** | **12–16** | **35–45** | **50–65** | **60–80** | |

---

## 3. Budget

### 3.1 Unit-cost assumptions `[ASSUMPTION — replace with local quotes]`

| Item | Assumption |
|---|---|
| Local senior professional (fully loaded, KRI) | USD 24–42 k/yr |
| Local mid-level professional | USD 14–26 k/yr |
| Diaspora-based staff (EU) | USD 60–95 k/yr |
| International expert days | USD 600–1,000/day |
| Item commissioning incl. reviews | USD 60–150 per receptive item; 150–300 per productive prompt |
| Rater time | USD 10–20/h (KRI); 35–50/h (EU) |
| Pilot participant honorarium | USD 20–40 |
| Laptop (spec D4 §5.3) | USD 700–1,000 |
| Centre server + UPS + network + scanner | USD 8–14 k per centre |
| Book illustration | USD 40–120 per illustration (shared across editions where culturally suitable) |
| Finished audio hour (studio, talent, edit) | USD 500–1,200 |
| Print unit cost (full colour, 150–250 pp) | USD 3–7 at 2–5 k copies |

### 3.2 Phase 0 (≈ 12 months)

| Line | USD k (low–high) |
|---|---|
| Staff (12–16 FTE) | 260–440 |
| International psychometric partner + experts | 60–120 |
| RLD corpus work (licensing, transcription start) | 25–60 |
| Legal, governance, DPIA | 25–50 |
| Series style audit, ordinance, sample units + mini-pilot | 25–50 |
| Architecture, client spike, prototypes | 30–60 |
| Office, admin, travel | 25–50 |
| Contingency 10 % | 45–83 |
| **Total Phase 0** | **≈ 495–913** |

### 3.3 Phase 1 (≈ 18 months)

| Line | USD k (low–high) |
|---|---|
| Staff (35–45 FTE avg, incl. contractors) | 1,100–1,900 |
| Item development (≈ 1,000–1,500 items + prompts + listening audio) | 90–250 |
| Cognitive labs + pilot (1,200 participants + logistics) | 40–100 |
| Standard setting (2 varieties + cross-variety exercise) | 30–70 |
| Hosting, HSM/KMS, software licences (incl. Winsteps/Facets, InDesign) | 40–100 |
| Centre equipment (4 centres; ~88 seats) | 100–180 |
| Pen test + red team | 40–90 |
| **Series MVP**: illustration 40–110; design/layout contract 60–150; audio 20–50; editorial/proofing 30–70; IP/legal review 15–40; first print run (10 books × 2–5 k) 60–250 | 225–670 |
| Recognition, communications, travel | 40–90 |
| Office, admin, insurance | 60–120 |
| Contingency 12 % | 212–428 |
| **Total Phase 1** | **≈ 1,980–3,998** |

**Levers to reduce Phase 1 cost:**
- Print-on-demand or a smaller first run (−50 to −200 k).
- Premises and centres provided in kind by the host university and ministries (−50 to −150 k).
- Defer `kmr-Arab` testing if pilot demand is below the DN-05 threshold (−60 to −120 k).
- With these levers the range is ≈ **USD 1.7–3.4 M**.

### 3.4 Phase 2 and steady-state OPEX

| | Phase 2 (24 months) | Steady state (per year, Phase 3) |
|---|---|---|
| Staff | 2,600–4,400 | 1,500–2,600 |
| Item development + standard setting replication + studies | 250–550 | 150–300 |
| Technology (hosting, licences, security testing) | 150–300 | 100–200 |
| Centres (new equipment + operations) | 150–350 | 100–250 |
| Series (L3–L4, Grammar, Vocab, kmr-Arab editions, Teacher's Guides, Heritage Fast-Track) | 450–1,100 | 150–400 |
| Recognition, ALTE, ISO, travel | 80–180 | 60–120 |
| Contingency 10 % | 368–688 | 206–387 |
| **Total** | **≈ 4,050–7,570** | **≈ 2,270–4,260** |

### 3.5 Cost per candidate (variable)

| Component | USD per candidate |
|---|---|
| Rating (W+S, 100 % double, ~1.5 rater-hours + ~10 % third ratings) | 18–35 |
| Centre delivery (staff, venue, power) | 10–20 |
| Interlocutor (speaking part) | 4–8 |
| Payments (2–4 % of fee), SMS/WhatsApp, certificate signing | 3–7 |
| Support | 3–5 |
| **Variable total** | **≈ 38–75** |

After the double-rating reduction (AD-026), rating drops to about 10–20, and the variable total to ≈ 30–60.

### 3.6 Fee model with equity tiers `[ASSUMPTION — Board to set]`

| Tier | Fee (indicative) | Notes |
|---|---|---|
| KRI resident | USD 60–90 equivalent, charged in IQD | Price list in IQD (FR-PAY-006) |
| Iraq (other) | Same as KRI | — |
| Diaspora / international (EU, UK) | EUR 160–220 | Local market comparators `[VERIFY]` |
| Institutional bulk (≥ 20 candidates) | −10 to −20 % | Vouchers (FR-PAY-004) |
| **Fee waivers** | 0 | ≤ 10 % of seats per window (AD-020): refugees, low income |
| Re-mark (E2) / clerical (E1) | ~40 % / ~10 % of the fee | Refunded if result changes (D6 §4.4) |
| Series books (KRI) | USD 6–10 subsidised | Free Hub audio and keys (DN-20) |
| Series books (diaspora retail) | EUR 20–30 | — |

### 3.7 Break-even scenarios (testing only; steady-state fixed cost USD 2.0 M/yr)

Blended fee assumes 75 % KRI at USD 75 and 25 % diaspora at USD 190, with 8 % waivers → ≈ USD 96 per candidate. Variable cost ≈ USD 50 → contribution ≈ **USD 46**.

| Annual volume | Revenue (k) | Variable (k) | Contribution (k) | Cost recovery of total (fixed + variable) |
|---|---|---|---|---|
| 2,500 (Year-1 base, A-01) | 240 | 125 | 115 | ≈ 11 % |
| 10,000 | 960 | 500 | 460 | ≈ 38 % |
| 25,000 (e.g., civil-service or teacher screening mandate) | 2,400 | 1,250 | 1,150 | ≈ 74 % |
| 45,000 | 4,320 | 2,250 | 2,070 | ≈ 101 % (break-even) |

**Conclusion:**
- At realistic early volumes, **KBS cannot be fee-funded**.
- Sustainability depends on (a) a **public mandate** that creates volume, such as KRG civil-service or teacher language screening; (b) multi-year **grant or public funding** for fixed costs; and (c) **institutional contracts**.
- Series revenue can cross-subsidise Hub costs, not the testing.
- The phase gates track cost recovery (KPI-029): ≥ 25 % in Phase 2 and ≥ 40 % in Phase 3.

### 3.8 Funding sources (none assumed committed)

| Source | Fit | Status |
|---|---|---|
| KRG budget lines (MoE, MoHESR) | Fixed costs; recognition linkage | `[VERIFY]`; must respect AD-035 after Phase 2 |
| Host university (in kind) | Premises, research ethics, staff secondment | To negotiate (D9) |
| International donors and cultural foundations | Phase 0–1 grants; Series; minority-language programmes | `[VERIFY eligibility]` |
| Research grants (e.g., EU programmes via partner universities) | RLD, corpora, ASR research | `[VERIFY]` |
| Diaspora philanthropy | Waiver fund; Series for mother-tongue schools | — |
| Fees and institutional contracts | Variable costs, then contribution | Per §3.7 |
| Series sales and licences | Series production and Hub | Per DN-20, DN-21 |

---

## Changes to prior deliverables
- **D0 A-04 / D1 budget:** Phase 0 is refined to **≈ USD 0.50–0.91 M** (within the original range). Phase 1 is refined to **≈ USD 1.98–4.0 M**, above D0's USD 1.5–3.5 M, because of centre hardware and the Series first print run. With the §3.3 levers it is ≈ USD 1.7–3.4 M.
- **D1 timeline:** the first live window is at about month 22 (within D1's 20–28-month range).
- KPI-### and RISK-### IDs referenced here are defined in D12 and D11.

## §19 self-check
- ✅ Varieties and scripts are costed per track (items, raters, editions); the `kmr-Arab` deferral lever is explicit. Offline: centre equipment (laptops, UPS) budgeted.
- ✅ Phase gates are measurable and tied to KPIs and quality targets. Data-hungry features stay in Phase 3–4 behind gates.
- ✅ No invented prices: all figures are labelled assumptions with a unit-cost basis; no funder commitments.
- ⚠️ The break-even analysis shows a structural funding gap. This is a strategic risk (RISK-010 in D11) that needs an owner decision on the mandate and funding strategy.

**Next deliverable: D11 — Risk register.**
