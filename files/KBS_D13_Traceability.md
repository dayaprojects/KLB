# KBS — D13 · Traceability Matrix

> **Covers:** `KLB_v3.md` §18 D13. Two chains:
> 1. **requirement → design → test → KPI**;
> 2. **curriculum item → book unit → KBS descriptor**.
>
> **Depends on:** D0–D12. D14–D15 use the curriculum IDs fixed here (`CUR-*`, `L1-U##`).
> The authoritative matrix lives as data in the requirements tool (exported from M12 and the Series content model). This document is the **Phase 1 baseline**. Gaps are listed honestly in §7.

---

## 1. Test catalogue (IDs used below)

| Test ID | Test | Method source |
|---|---|---|
| TST-001 | Power-pull rig (50 hard cuts per build) | D4 §6 NFR-RES-001/002 |
| TST-002 | Full offline session dry run (WAN unplugged) | D4 §6 NFR-AVAIL-002 |
| TST-003 | Sync fault injection (duplicate, reorder, truncate, broken chain) | D4 §6 NFR-RES-003 |
| TST-004 | Session close recording-integrity report | D4 §6 NFR-RES-004 |
| TST-005 | DR restore drill | D4 §6 NFR-RES-005 |
| TST-006 | Load tests (booking, notifications, ×10 headroom) | D4 §6 NFR-PERF-004/005, SCAL-001 |
| TST-007 | Throttled Lighthouse CI + RUM | D4 §6 NFR-PERF-003 |
| TST-008 | ASVS checklist + external pen test | D7 CTL-028 |
| TST-009 | Centre red-team exercise | D7 CTL-018 |
| TST-010 | Schema lint: data inventory + prohibited fields | D4 DR-001/002 |
| TST-011 | NORM-v1 golden corpus | D4 §4.7 |
| TST-012 | Bidi visual regression | D4 §6 NFR-L10N-002 |
| TST-013 | String-catalogue completeness | NFR-L10N-001 |
| TST-014 | Glyph test string (UI + PDF) | FR-L10N-005 |
| TST-015 | Accessibility audit (automated + manual) | NFR-A11Y-001 |
| TST-016 | **Acceptance tests generated from Given/When/Then** (one scenario per FR: `ATS-<FR-ID>`) | D3, D4 §7 |
| TST-017 | Architecture boundary tests (module isolation) | ADR-001 |
| TST-018 | Delivery-client spike acceptance (shaping, durability, audio) | ADR-005 |
| TST-019 | Dual computation of operational scores | AD-032 |
| TST-020 | Results QA sample (50 + all near-cut) | D8 §5.6 |
| TST-021 | Post-administration key check | D6 §1.2 |
| TST-022 | Notification template lint | FR-NOTIF-002 |
| TST-023 | Residency query | NFR-PRIV-004 |
| TST-024 | Series ↔ item-bank similarity check | DR-030 |
| TST-025 | Retention job audit | NFR-PRIV-002 |
| TST-026 | Psychometric quality report vs D2 §5.7 targets | D8 §3 |
| TST-027 | Standard-setting procedural audit | D2 §5.5 |
| TST-028 | IDML ↔ source round-trip text check | ADR-010 |

---

## 2. Decisions → requirements → design → test → KPI

| Decision | Requirements | Design | Tests | KPI |
|---|---|---|---|---|
| AD-001 separate varieties | FR-CAND-005, FR-RATE-002, FR-IAM-001 | BC2, BC7; Track enum (D5 §7) | ATS-FR-CAND-005, ATS-FR-RATE-002, TST-027 | KPI-001 (per track), KPI-013 |
| AD-002 Kurmanji both scripts | FR-ITEM-007, FR-DEL-009, FR-RATE-002 | TRANSLIT-kmr-v1 (D4 §4.8); BC3 | ATS-FR-ITEM-007, TST-012 | KPI-004 (script DIF) |
| AD-003 two tiers + placement | FR-CAND-005, FR-HUB-003 | BC2, BC13 | ATS-FR-HUB-003 | KPI-005 |
| AD-004 hybrid speaking | FR-DEL-007/008/015, FR-OPS-009 | ADR-003, ADR-015 | ATS-FR-DEL-008, TST-004 | KPI-003, KPI-010 |
| AD-005 scale & reporting | FR-RES-001, FR-CAND-011 | BC8; conversion tables (D6 §3) | TST-019, TST-020 | KPI-002, KPI-005 |
| AD-006 no academic competencies | — (scope exclusion) | — | Handbook review | — |
| AD-007 permanent certificate | FR-RES-005 | ADR-008 | ATS-FR-RES-005 | — |
| AD-008 Arabic page on request | FR-RES-005 | D6 §5.6 | TST-014 | — |
| AD-009 no remote proctoring Ph1 | FR-PROC-* (W) | — | — | — |
| AD-010 Rasch/MFRM | FR-PSY-001/002 | BC10 | TST-019, TST-026 | KPI-001, KPI-003 |
| AD-011 single Kurmanji bank (conditional) | FR-PSY-006 | BC10 | TST-026 (script-DIF) | KPI-004 |
| AD-012 CINEG equating | FR-ASM-001, FR-PSY-005 | BC4, BC10 | ATS-FR-ASM-001, TST-019 | KPI-006 |
| AD-013 standard-setting methods | — (procedure) | D8 S-10 | TST-027 | KPI-005 |
| AD-014 play-count | FR-DEL-006 | ADR-005 client | ATS-FR-DEL-006, TST-001 | KPI-011 |
| AD-015 no read-aloud | — (blueprint) | D2 §4.5 | Form QA (D8 §5.2) | — |
| AD-016 DIF procedure | FR-PSY-004 | BC10 | TST-026 | KPI-004, KPI-016 |
| AD-017 mediation deferred | — | — | — | — |
| AD-018 NORM-v1 | FR-DEL-018, FR-ITEM-006, FR-L10N-002 | D4 §4.7; `kbs-norm` library (D5 §10) | TST-011 | KPI-001 (indirect) |
| AD-019 age 16 + guardian | FR-CAND-014 | BC1 | ATS-FR-CAND-014 | — |
| AD-020 scheduling policy | FR-SCHED-001, FR-CAND-007/008, FR-PAY-007 | BC2 | ATS-FR-CAND-007/008 | KPI-007 |
| AD-021 incident classes | FR-OPS-005, FR-INC-001 | BC6 | ATS-FR-OPS-005 | KPI-008 |
| AD-022 alternative ID pathway | FR-CAND-004 | BC1 | ATS-FR-CAND-004, TST-010 | KPI-017 (access) |
| AD-023 MFRM fair measures | FR-RES-001 | BC7, BC10 | TST-019 | KPI-003 |
| AD-024 no score adjustment | FR-RES-003 | BC8 | Results QA | — |
| AD-025 re-mark up or down | FR-RES-006 | BC8 | ATS-FR-RES-006 | KPI-021 |
| AD-026 double-rating gate | FR-RATE-005 | BC7 | TST-026 | KPI-003 |
| AD-027 release SLA | FR-RES-004 | BC8 | ATS-FR-RES-004 | KPI-009 |
| AD-028 jurisdiction policy | — (policy) | ADR-009 | CTL-002 review | KPI-022 |
| AD-029 statistics ≠ misconduct | — (procedure) | D7 §5 | Case audit (CTL-023) | KPI-020, KPI-021 |
| AD-030 human face comparison | FR-OPS-004 | No biometric template stores | Architecture review (CTL-022) | — |
| AD-031 transparency report | — | — | CTL-031 | — |
| AD-032 R + dual computation | FR-PSY-001 | D8 §4 | TST-019 | KPI-001…006 |
| AD-033 PRB | FR-RES-004 (release gate) | D8 §1 | PRB minutes | KPI-009 |
| AD-034 cognitive labs | — | D8 S-03 | Study report | — |
| AD-035/036/037 governance | — | D9 | Board audit | KPI-013 |
| DN-12 / ADR-009 hosting | NFR-PORT-001, NFR-PRIV-004 | D5 §4, DR-004 | TST-023 | KPI-022 |
| DN-22 firewall | FR-ITEM-011, FR-HUB-003 | CON-015, DR-030 | TST-024 | — |
| ADR-011 laptops | FR-DEL-003/004 | D4 §5.3 | TST-001 | KPI-011 |
| ADR-012 separate Hub identity | FR-HUB-009 | ADR-006 realms | ATS-FR-HUB-009 | KPI-027 |

---

## 3. Functional requirements (Musts) → design → test → KPI

| Module | Must FRs | Bounded context / ADR | Tests | KPI |
|---|---|---|---|---|
| M1 Public site | FR-PUB-001/002/003/004/006/007 | BC11 (content), ADR-014 | ATS-*, TST-007, TST-012, TST-013, TST-015 | KPI-023 |
| M2 Candidate portal | FR-CAND-001…009, 011, 012, 013 | BC1, BC2, BC9; ADR-006 | ATS-*, TST-010, TST-015 | KPI-017, KPI-023 |
| M3 Payments | FR-PAY-001…004, 006, 007, 008 | BC2; IF-001/002 | ATS-*, TST-006 | KPI-028 |
| M4 Delivery | FR-DEL-001…013, 016…020 | BC5; ADR-004/005/016; DR-020/021/022 | ATS-*, TST-001…004, TST-009, TST-018 | KPI-007, 010, 011 |
| M5 Item bank | FR-ITEM-001…011 | BC3 (C4 zone) | ATS-*, TST-011, TST-017 | KPI-004 |
| M6 Assembly | FR-ASM-001…005 | BC4; IF-012/013 | ATS-*, TST-009 | KPI-006, KPI-019 |
| M7 Operations | FR-OPS-001…006, 008, 009 | BC5, BC6 | ATS-*, TST-002 | KPI-007, KPI-008 |
| M8 Rating | FR-RATE-001…006, 008, 009 | BC7; ADR-003 | ATS-*, TST-026 | KPI-003 |
| M9 Results | FR-RES-001…008 | BC8; ADR-008 | ATS-*, TST-019, TST-020, TST-021 | KPI-002, 005, 009 |
| M10 Verification | FR-VER-001/002/003/006 | BC9 | ATS-*, TST-008 | KPI-022 |
| M12 Psychometrics | FR-PSY-001/002/005/006 | BC10 | TST-019, TST-026 | KPI-001…006 |
| M13 Support | FR-SUP-002 | BC1 | ATS-FR-SUP-002 | KPI-023 |
| M14 IAM & audit | FR-IAM-001…004, 006 | BC12; ADR-006 | ATS-*, TST-008 | KPI-022 |
| M15 Hub | FR-HUB-001…005, 009 | BC13; ADR-010/012 | ATS-*, TST-024 | KPI-024, KPI-027 |
| Cross-cutting | FR-NOTIF-001/002, FR-SCHED-001, FR-INC-001, FR-L10N-001/002/004/005 | BC11; `kbs-norm` | TST-011…014, TST-022 | — |

## 4. NFRs → design → test → KPI

| NFR | Design | Test | KPI |
|---|---|---|---|
| NFR-SCAL-001 | ADR-001, ADR-017 | TST-006 | KPI-014 |
| NFR-PERF-001/002 | ADR-005 (local SQLCipher), IF-011 | TST-001, centre lab benchmark | KPI-011 |
| NFR-PERF-003 | ADR-014 (htmx, JS budget) | TST-007 | KPI-023 |
| NFR-PERF-004/005 | ADR-002, ADR-007 | TST-006 | KPI-009 |
| NFR-AVAIL-001 | D5 §4, §11 | Probes | KPI-012 |
| NFR-AVAIL-002 | ADR-004, ADR-016 | TST-002 | KPI-007 |
| NFR-RES-001/002 | ADR-005, DR-020 timer model | TST-001 | KPI-011 |
| NFR-RES-003 | ADR-004, DR-021 | TST-003 | KPI-010 |
| NFR-RES-004 | ADR-003, FR-DEL-008 | TST-004 | KPI-010 |
| NFR-RES-005 | D5 §11 | TST-005 | — |
| NFR-SEC-001…005 | D7 §7, ADR-008, IF-007 | TST-008, TST-009 | KPI-019, KPI-022 |
| NFR-PRIV-001…004 | DR-001…004, DR-024, ADR-009 | TST-010, TST-023, TST-025 | KPI-022 |
| NFR-A11Y-001 | ADR-014 design system | TST-015 | KPI-017 |
| NFR-L10N-001…003 | D5 §10 | TST-011…014 | — |
| NFR-OBS-001 | IF-022 | Log scanner | — |
| NFR-PORT-001 | ADR-017, CON-001 | Two-environment deploy | — |

## 5. Risks → controls → KPI

| Risk | Main controls / requirements | KPI |
|---|---|---|
| RISK-001 recognition | D9 §4; U-01…U-05 | KPI-013 |
| RISK-002 variety politics | AD-001, AD-036, AVP | KPI-016 |
| RISK-003 small samples | AD-011, D8 S-04 | KPI-001, 002, 006 |
| RISK-004 leaks | CTL-016…020 | KPI-019 |
| RISK-005 power | ADR-011, NFR-RES-* | KPI-008, 011 |
| RISK-006 data exposure | CTL-001…011, ADR-009 | KPI-022 |
| RISK-007 key person | AD-032, A-05 | — (HR) |
| RISK-010 funding | D10 §3.7 | KPI-028…030 |
| RISK-011 IP / trade dress | DN-16; D16 IP rules | — (legal opinion) |
| RISK-012 orthography in print | D16 orthography; two proofreaders | Errata rate (D16 quality gate) |
| RISK-013 test-prep leakage via Series | DN-22, CON-015, TST-024 | KPI-019 |
| RISK-014 writer shortage | D9 §6 author training | KPI-024 (delivery) |

---

## 6. Curriculum item → book unit → KBS descriptor (Level 1 / A1)

**ID scheme:**
- **Curriculum item:** `CUR-<Level>-<Strand>-<nn>`. Strands: FN functions · GR grammar · VO vocabulary set · PR pronunciation · SC script & orthography · SO sociocultural.
- **Units:** `L1-U01…L1-U40`. Every 5th unit (U05, U10 … U40) is a review unit; U40 also holds the level checkpoint.
- **Descriptor:** the `-01` anchors come from D2 §3.3. `-02` onward are draft descriptors introduced in D14 §2, for the descriptor working group to validate (S-02).

### 6.1 Functions (all units are delivered in both the Sorani and the Kurmanji Latin edition)

| Curriculum item | Can-do (learner outcome) | Units | Review units | KBS descriptor(s) |
|---|---|---|---|---|
| CUR-L1-FN-01 | Greet, introduce yourself, say goodbye | U01 | U05 | DESC-S-A1-01, DESC-L-A1-02 |
| CUR-L1-FN-02 | Ask and say where someone is from | U02 | U05 | DESC-S-A1-01 |
| CUR-L1-FN-03 | Talk about jobs | U03 | U05 | DESC-S-A1-01, DESC-R-A1-01 |
| CUR-L1-FN-04 | Use numbers 0–20; phone numbers | U04 | U05 | DESC-L-A1-01 |
| CUR-L1-FN-05 | Talk about your family | U06 | U10 | DESC-S-A1-02 |
| CUR-L1-FN-06 | Identify and describe things and people | U07, U08, U09 | U10 | DESC-S-A1-03, DESC-R-A1-01 |
| CUR-L1-FN-07 | Describe your home; say where things are | U11, U12 | U15 | DESC-S-A1-03, DESC-L-A1-03 |
| CUR-L1-FN-08 | Ask prices; buy things at the bazaar | U13, U14 | U15 | DESC-L-A1-01, DESC-S-A1-04 |
| CUR-L1-FN-09 | Talk about daily routine and time | U16, U17, U18 | U20 | DESC-S-A1-02, DESC-L-A1-01 |
| CUR-L1-FN-10 | Say what food and drink you like | U19 | U20 | DESC-S-A1-02 |
| CUR-L1-FN-11 | Ask simple questions | U21 | U25 | DESC-S-A1-01 |
| CUR-L1-FN-12 | Order food and drink; make simple requests | U22 | U25 | DESC-S-A1-04 |
| CUR-L1-FN-13 | Ask for and follow simple directions | U23 | U25 | DESC-L-A1-03 |
| CUR-L1-FN-14 | Talk about the weather and seasons | U24 | U25 | DESC-S-A1-02 |
| CUR-L1-FN-15 | Say how you feel; simple health problems | U26 | U30 | DESC-S-A1-04 |
| CUR-L1-FN-16 | Talk about clothes and colours | U27 | U30 | DESC-S-A1-03 |
| CUR-L1-FN-17 | Talk about free time and abilities (fixed phrases) | U28 | U30 | DESC-S-A1-02 |
| CUR-L1-FN-18 | Offer, accept and decline hospitality politely | U29 | U30 | DESC-S-A1-04, SO items |
| CUR-L1-FN-19 | Talk about what you have | U31 | U35 | DESC-S-A1-02 |
| CUR-L1-FN-20 | Fill in a form; write short personal details | U32 | U35 | DESC-W-A1-01 |
| CUR-L1-FN-21 | Name places in town; say where they are | U33 | U35 | DESC-R-A1-01, DESC-L-A1-03 |
| CUR-L1-FN-22 | Understand and write short messages; simple phone calls | U34 | U35 | DESC-W-A1-02, DESC-L-A1-02 |
| CUR-L1-FN-23 | Talk about Newroz and festivals (simple) | U36 | U40 | DESC-R-A1-02 |
| CUR-L1-FN-24 | Describe your town or village | U37 | U40 | DESC-S-A1-03, DESC-W-A1-02 |
| CUR-L1-FN-25 | Say where you were (past of "be") | U38 | U40 | DESC-S-A1-02 |
| CUR-L1-FN-26 | Give a short personal presentation (spoken and written) | U39 | U40 | DESC-S-A1-01, DESC-W-A1-02 |

### 6.2 Grammar (variety-specific delivery shown; details in D14 §3)

| Curriculum item | Sorani (`ckb`) | Kurmanji (`kmr-Latn`) | Units | Descriptor link |
|---|---|---|---|---|
| CUR-L1-GR-01 Sound–letter mapping | Arabic-based alphabet (Starter + script panels U01–U04) | Hawar Latin alphabet (Starter + panels U01–U04) | Starter, U01–U04 | DESC-R-A1-01, DESC-W-A1-01 |
| CUR-L1-GR-02 Personal pronouns | من، تۆ، ئەو، ئێمە، ئێوە، ئەوان | ez, tu, ew, em, hûn, ew + oblique min, te, wî/wê … | U01, U02 | DESC-S-A1-01 |
| CUR-L1-GR-03 Present copula + negation | ـم، ـیت، ـە/ـیە، ـین، ـن; نیم، نیت، نییە… | -im/-me, -î/-yî, -e/-ye, -in/-ne; ne … | U02, U03 | DESC-S-A1-01 |
| CUR-L1-GR-04 Ezafe basics | ـی (ناوی من) | -ê (m.), -a (f.), -ên (pl.) (navê min) | U01, U06, U09 | DESC-S-A1-02 |
| CUR-L1-GR-05 Possession | Pronominal clitics (ناوم، ماڵت) | Ezafe + oblique pronoun (navê min, mala te) | U01, U06 | DESC-S-A1-02 |
| CUR-L1-GR-06 Demonstratives | ئەم … ە / ئەو … ە | ev / ew; oblique vê/vî, wê/wî | U07 | DESC-S-A1-03 |
| CUR-L1-GR-07 Definiteness | ـەکە (definite), ـێک (indefinite) | -ek (indefinite); no definite article | U07, U08 | DESC-R-A1-01 |
| CUR-L1-GR-08 Plural | ـان، ـەکان | Plural ezafe -ên; oblique plural -an | U08 | DESC-R-A1-01 |
| CUR-L1-GR-09 Grammatical gender (kmr only) | — | Masculine/feminine via ezafe and oblique | U06, U09, U12 | DESC-W-A1-01-kmr |
| CUR-L1-GR-10 Oblique case basics (kmr only) | — | After prepositions and in possession | U06, U12 | DESC-W-A1-01-kmr |
| CUR-L1-GR-11 There is / isn't | هەیە / نییە | heye / tune | U11 | DESC-S-A1-03 |
| CUR-L1-GR-12 Prepositions and circumpositions | لە … دا، بۆ، لەگەڵ، لە … ەوە | li … (ê), ji … re, bi … re, di … de | U12, U23, U33 | DESC-L-A1-03 |
| CUR-L1-GR-13 Numbers, time, dates | Cardinal/ordinal; Kurdish month names (variants) | Same | U04, U13, U17, U18 | DESC-L-A1-01 |
| CUR-L1-GR-14 Present tense | دە-/ئە- + present stem + personal endings | di- + present stem + personal endings | U16 | DESC-S-A1-02 |
| CUR-L1-GR-15 Liking | حەزم لە … ە | ji … hez dikim | U19 | DESC-S-A1-02 |
| CUR-L1-GR-16 Question words | کێ، چی، کوێ، کەی، چۆن، بۆچی، چەند | kî, çi, ku, kengî, çawa, çima, çend | U21 | DESC-S-A1-01 |
| CUR-L1-GR-17 Imperative | بـ + stem (بڕۆ، وەرە) | bi- + stem (here, were) | U22, U23 | DESC-L-A1-03 |
| CUR-L1-GR-18 Experiencer (pain) | سەرم دێشێت | serê min diêşe | U26 | DESC-S-A1-04 |
| CUR-L1-GR-19 Ability as chunks | دەتوانم … (fixed phrases) | dikarim … (fixed phrases) | U28 | DESC-S-A1-02 |
| CUR-L1-GR-20 Have | clitic + هەیە (ئۆتۆمبێلێکم هەیە) | min … heye (otomobîleke min heye) | U31 | DESC-S-A1-02 |
| CUR-L1-GR-21 Past of "be" | بووم، بوویت، بوو … | bûm, bûyî, bû … | U38 | DESC-S-A1-02 |

Vocabulary sets (CUR-L1-VO-01…13), pronunciation (CUR-L1-PR-01…06), script and orthography (CUR-L1-SC-01…05) and sociocultural items (CUR-L1-SO-01…06) are mapped to units in D14 §3–§4.

### 6.3 Level 2 (A2) and beyond
- The L2 chain uses the same scheme (`CUR-L2-*` → `L2-U01…U40` → A2 descriptors). Its mapping table is in D14 §5 and the unit list in D15.
- L3–L4 mappings are produced with those titles in Phase 2.

### 6.4 Descriptor → test task link (closing the loop)

| Descriptor family | Taught in (L1) | Assessed in KBS General Foundation |
|---|---|---|
| DESC-L-A1-* | FN-01, 04, 08, 09, 13, 21, 22 | Listening L1 (picture MCQ), L2 (announcements) |
| DESC-R-A1-* | FN-03, 06, 21, 23 | Reading R1 (signs, notices) |
| DESC-W-A1-* | FN-20, 22, 24, 26 | Writing W1 (form / short message) |
| DESC-S-A1-* | most FN items | Speaking S1 (personal questions), S2 (picture description) |

**Firewall check:** this table links **descriptors**, never items. No Series exercise is derived from a test item (DN-22, TST-024).

---

## 7. Coverage summary and known gaps

| Check | Status |
|---|---|
| Every AD/ADR has ≥ 1 requirement or explicit "scope/procedure" | ✅ (§2) |
| Every Must FR has an acceptance test (ATS) | ✅ Generated from D3 GWT + D4 §7 |
| Every NFR has a test and a design element | ✅ (§4) |
| Every red risk has a control and a KPI | ✅ except RISK-007 (HR measure; add "succession coverage" in Phase 1 HR plan) |
| Every L1 curriculum item maps to ≥ 1 unit and ≥ 1 descriptor | ✅ (§6) |
| Every L1 teaching unit has ≥ 1 curriculum item | ✅ U01–U04, U06–U09, U11–U14, U16–U19, U21–U24, U26–U29, U31–U34, U36–U39 |
| **Gaps** | (1) Descriptors `-02` onward are **drafts** until study S-02 validates them. (2) Should/Could FRs have acceptance tests but no KPI link (acceptable). (3) L3–L4 curriculum chain is pending (Phase 2). (4) FR-PROC-* and FR-RES-009 (VC) are Phase 2–3 and untested. |

## Changes to prior deliverables
- **D2 §3.3:** draft descriptor IDs `-02`…`-04` are referenced (they are defined in D14 §2). The D2 seed set is unchanged.
- New IDs: TST-001…TST-028, ATS-<FR-ID> convention, CUR-L1-*, L1-U01…U40.

## §19 self-check
- ✅ Variety and script: grammar items split by variety; Kurmanji-only items (GR-09/10) flagged; per-track KPIs.
- ✅ Every minimum-curriculum item at L1 maps to a book unit and a KBS descriptor. The full L2 table is in D14.
- ✅ Requirements trace to design, test and KPI. Gaps are listed honestly.

**Next deliverable: D14 — Curriculum framework.**
