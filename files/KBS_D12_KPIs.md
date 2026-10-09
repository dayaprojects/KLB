# KBS — D12 · KPI Framework

> **Covers:** `KLB_v3.md` §17 (KPIs) · **Depends on:** D2 (quality targets), D3/D4 (NFRs), D6, D8, D10 (phase gates), D11 (risk triggers)
> Targets are for **Phase 2** unless noted. Phase 1 targets apply from the first live window. **Baselines** are measured in Phase 0–1 where no target can be justified yet (marked `baseline`).
> All KPIs are reported **per track** (`ckb`, `kmr-Latn`, `kmr-Arab`) where relevant. Public reporting suppresses cells with n < 10.

## 1. KPI catalogue

### Psychometric

| ID | KPI | Definition | Formula | Target | Data source | Owner | Freq. |
|---|---|---|---|---|---|---|---|
| KPI-001 | Reliability per skill | Internal consistency (receptive) or G-coefficient (productive) per skill, tier and track | Rasch person reliability or α; G = σ²p / (σ²p + σ²δ) | ≥ 0.85 (F) / ≥ 0.88 (A) receptive; ≥ 0.80 productive; composite ≥ 0.92 | M12 window analysis | Head of Psychometrics | Per window |
| KPI-002 | SEM | Median CSEM in scale points per skill | median(CSEMᵢ) | ≤ 5 points | M9 results | Head of Psychometrics | Per window |
| KPI-003 | Rater agreement | Agreement between two independent ratings per criterion | Exact %, exact+adjacent %, QWK | Exact ≥ 60 %; ±1 ≥ 95 %; QWK ≥ 0.75 (target 0.80) | M8 | Rating quality manager | Per window |
| KPI-004 | DIF rate | Share of scored items flagged ETS class C or Rasch large DIF, any group | C-flagged items / scored items | ≤ 2 %, with 100 % reviewed within the window | M12 DIF runs | Head of Psychometrics | Per window |
| KPI-005 | Classification accuracy | Probability a candidate is classified at the correct CEFR level at each cut | Rudner / Livingston–Lewis | ≥ 0.85 at every reported cut | M12 | Head of Psychometrics | Per window |
| KPI-006 | Linking error | SE of linking per window | Bootstrap or anchor-based SE | ≤ 0.10 logits | Equating record | Head of Psychometrics | Per window |

### Operational

| ID | KPI | Definition | Formula | Target | Data source | Owner | Freq. |
|---|---|---|---|---|---|---|---|
| KPI-007 | Session completion | Sessions completed as scheduled, without void | completed sessions / scheduled sessions | ≥ 99 % | M7 | Head of Operations | Monthly |
| KPI-008 | Session incident rate | I-3 incidents per 100 sessions | I-3 count × 100 / sessions | ≤ 2 | M7 incidents | Head of Operations | Monthly |
| KPI-009 | Results turnaround | Working days from session to release | median and P95 | Median ≤ 12, P95 ≤ 15 (CBT, Ph1); P95 ≤ 10 (Ph2) | M9 | Results officer | Per window |
| KPI-010 | Sync and recording integrity | Recordings checksum-verified before close; data at core within 24 h | verified / total; synced ≤ 24 h / total | 100 %; ≥ 99.9 % | S2 reports | CTO | Per session |
| KPI-011 | Data loss on power events | Responses lost in power or device incidents | lost responses (> 1 s old) | 0 | Incident reports + event logs | CTO | Per incident |
| KPI-012 | Core availability | Monthly uptime of S1 | uptime / time | ≥ 99.5 % (99.9 % key days) | Probes | CTO | Monthly |

### Adoption

| ID | KPI | Definition | Formula | Target | Data source | Owner | Freq. |
|---|---|---|---|---|---|---|---|
| KPI-013 | Recognising bodies | Organisations formally accepting KBS results for a defined use | count (by category) | Ph1 exit ≥ 2 anchor users; Ph2 exit ≥ 5 | Recognition register | Head of Recognition | Quarterly |
| KPI-014 | Candidate volume | Candidates tested | count per track and tier | Year 1: baseline (assumption 2,500); Year 2: +50 % | M9 | Executive Director | Quarterly |
| KPI-015 | Diaspora share | Share of candidates tested outside Iraq | diaspora / total | baseline Year 1; ≥ 15 % by Year 3 | M2/M7 | Head of Recognition | Quarterly |

### Equity

| ID | KPI | Definition | Formula | Target | Data source | Owner | Freq. |
|---|---|---|---|---|---|---|---|
| KPI-016 | Subgroup gaps explained | Share of mean-score gaps > 0.2 SD between fairness groups (D2 §5.8) with a documented explanation (construct-relevant, e.g., literacy) or a mitigation plan | explained gaps / gaps > 0.2 SD | 100 % within 2 windows | M12 + PRB minutes | Head of Psychometrics | Per window |
| KPI-017 | Accommodations fulfilled | Approved accommodations delivered as approved | delivered / approved | 100 % | M2 + M7 | Candidate Services | Per window |
| KPI-018 | Fee waiver use | Waiver seats used / quota | used / quota | 70–100 % (shows reach) | M3 | Finance | Per window |

### Security and integrity

| ID | KPI | Definition | Formula | Target | Data source | Owner | Freq. |
|---|---|---|---|---|---|---|---|
| KPI-019 | Content compromise | Live items confirmed leaked | count; % of live items | 0 confirmed; any leak triggers the playbook | Leak monitoring | Integrity officer | Monthly |
| KPI-020 | Malpractice detection | Confirmed malpractice cases per 1,000 candidates, and time to decision | cases × 1,000 / candidates; median days | baseline Ph1; decision ≤ 40 working days | Case management | Integrity officer | Quarterly |
| KPI-021 | Appeal outcomes | Share of appeals upheld (fully or partly) | upheld / decided | baseline; > 20 % triggers a process review | Appeals register | Board secretary | Annual |
| KPI-022 | Privacy incidents | Personal-data incidents by severity; notifiable breaches | count | 0 notifiable | DPO log | DPO | Quarterly |

### Experience

| ID | KPI | Definition | Formula | Target | Data source | Owner | Freq. |
|---|---|---|---|---|---|---|---|
| KPI-023 | Candidate satisfaction (CSAT) | Post-test survey score (1–5), by track and centre | mean; % 4–5 | ≥ 4.2; ≥ 80 % satisfied | Survey (anonymous, optional) | Candidate Services | Per window |

### Learning outcomes and Series

| ID | KPI | Definition | Formula | Target | Data source | Owner | Freq. |
|---|---|---|---|---|---|---|---|
| KPI-024 | Series completers reaching target level | Learners completing Level N who reach the target CEFR on the Hub placement test (or KBS) | reached / completers measured | ≥ 70 % (L1, Ph1 pilot); ≥ 75 % (Ph2) | Hub (opt-in) + pilot studies | Series editor | Per cohort |
| KPI-025 | Level gain per guided hour | Scale-score gain on the placement measure per 10 guided learning hours | Δscale / (GLH/10) | baseline Ph1; target set after pilots | Pilot studies | Series editor + Psychometrics | Per cohort |
| KPI-026 | Programmes using the series | Schools, programmes and organisations using the series in class | count | Ph2: ≥ 20 programmes | Teacher registrations, sales | Head of Recognition | Annual |
| KPI-027 | Active Hub learners | Distinct devices or accounts using Hub content in 30 days (privacy-preserving, cookieless count) | count | baseline Ph1 | Hub analytics (self-hosted) | Series editor | Monthly |

### Financial

| ID | KPI | Definition | Formula | Target | Data source | Owner | Freq. |
|---|---|---|---|---|---|---|---|
| KPI-028 | Cost per test | Total testing cost per candidate (fixed + variable) | testing costs / candidates | Trend down; variable ≤ USD 60 (Ph2) | Finance | Finance | Quarterly |
| KPI-029 | Cost recovery (testing) | Fee and contract income / testing costs | income / costs | ≥ 25 % Ph2; ≥ 40 % Ph3 | Finance | Executive Director | Quarterly |
| KPI-030 | Series cost recovery | Series income / Series costs (production + Hub) | income / costs | ≥ 50 % by Ph3 | Finance | Series editor | Annual |

## 2. KPI → phase gates and risks

| Gate / risk | KPIs watched |
|---|---|
| Phase 1 exit (D10 §1.1) | KPI-001, 003, 005, 007, 010, 011, 013, 024 |
| Phase 2 exit | KPI-001…006, 009, 013, 016, 019, 029 |
| RISK-001 recognition | KPI-013 |
| RISK-003 small samples | KPI-001, 002, 006 (per track) |
| RISK-004 / 030 leaks | KPI-019 |
| RISK-005 power | KPI-008, 011 |
| RISK-006 / 021 data exposure | KPI-022 |
| RISK-010 funding | KPI-028, 029, 030 |
| RISK-029 washback | KPI-016, 023, 024 |

## 3. Data and privacy rules for KPIs
- KPIs use **aggregate** data. Fairness KPIs use the pseudonymised store (DR-003).
- Learning-outcome KPIs use **opt-in** Hub data or consented pilot studies only. No learner tracking without consent (FR-HUB-005).
- Every KPI definition is versioned. A change of formula resets the trend line, and the change is noted in reports.

## Changes to prior deliverables
- **D10:** its KPI references (phase table, §3.7) were aligned to this catalogue's IDs in the same build (KPI-013 recognition, KPI-023 CSAT, KPI-024 Series completers, KPI-029 cost recovery).

## §19 self-check
- ✅ Every KPI has a definition, formula, target or baseline, source and owner. KPIs are reported per track; candidate safety is covered by aggregate-only data and suppression of cells with n < 10.
- ✅ The KPI families listed in §17 are all covered: psychometric, operational, adoption, equity, security, experience, learning outcomes, series adoption, financial.
- ⚠️ Several adoption and learning targets are `baseline` by design. Setting them before pilot data would be invented numbers.

**Next deliverable: D13 — Traceability matrix.**
