# KBS — Kurdish Benchmark System · Deliverables D0 + D1

> **Generated from:** `KLB_v3.md` v3.1 · **Mode:** `staged` (§18) · **Date:** 2026-10-08
> **Parameters:** all §0 defaults applied. `YEAR1_VOLUME` and `BUDGET_ENVELOPE` are estimated below as `[ASSUMPTION]`.
> **Status:** ✅ All defaults (DN-01…DN-22) **accepted** by owner on 2026-10-08. Formalised in D2 §0.

---

## D0 — Assumptions, decisions needed, open questions

### D0.1 Working assumptions

| ID | Assumption | Basis / reasoning | What would change it |
|---|---|---|---|
| A-01 | **Year-1 volume: ~2,500 candidates (range 1,500–4,000).** About 70 % Sorani (`ckb`), 22 % Kurmanji Arabic script (`kmr-Arab`, mostly Duhok), 8 % Kurmanji Latin (`kmr-Latn`, mostly diaspora). | Capacity: 3 KRI centres × ~24 CBT seats + 1 diaspora centre × ~16 seats = **~88 seats**. 2 sessions/day × 6 test days/month × 10 months gives ~10,000 seat-sittings. Year-1 demand will be well below capacity until recognition exists, so utilisation is assumed at 20–40 %. `[ASSUMPTION]` | A ministry or employer mandate (e.g. a civil-service language requirement) could multiply demand 5–10×. |
| A-02 | **Live volume alone cannot calibrate `kmr-Latn`, and only barely `kmr-Arab`.** Calibration therefore relies on **paid pilot cohorts** recruited through universities and community organisations, not on live candidates. | Stable Rasch difficulties need roughly 100–150 responses per item (Linacre's rule of thumb `[VERIFY]`). At ~200 `kmr-Latn` candidates per year, a live-only design would take years. | Large diaspora uptake, e.g. via a European mother-tongue programme. |
| A-03 | Peak load: **~90 concurrent test seats** (all offline-capable), plus **~500 concurrent web users** at results release. | Derived from A-01 and the seat count. | — |
| A-04 | **Order-of-magnitude budget (to be built bottom-up in D10):** Phase 0 ≈ USD 0.4–0.9 M; Phase 1 ≈ USD 1.5–3.5 M, including platform MVP, item development for 3 variety-script tracks, pilots and standard setting, 4 centres, and series MVP (10 books + Hub v1). | Ranges only; driven by staffing (largest line), panel and pilot costs, and illustration/audio. **No vendor prices assumed.** `[ASSUMPTION]` | The actual funding envelope; whether KRG ministries provide premises and staff in kind. |
| A-05 | Kurdish psychometric expertise is scarce. Phase 0–1 needs an **international psychometric partner** (university or testing body) under a capacity-transfer agreement. | §17 risk "key-person dependency". | A qualified in-house lead is hired early. |
| A-06 | Existing open Kurdish corpora (web, news, Wikipedia, academic corpora) are enough to **start** the RLD, but are skewed toward written, news and Sorani text. Spoken and Kurmanji-Arabic-script data must be collected. | §6.3. Corpus licences: `[VERIFY]` each. | — |
| A-07 | Candidates and learners in Turkey, Iran and Syria may face risk if identifiable as Kurdish-language candidates (§3.3). **No candidate data flows to any government by default.** | §3.3. | — |
| A-08 | The legal status of the institute and recognition by the KRG need an act, decree or MoU. The route and timing are unknown. | `[VERIFY]` KRI legal routes. | — |
| A-09 | DK's EFE structure (Levels 1–4 ≈ A1–B2, Course + Practice Books, audio app) is treated as stated in §16 until a physical style audit confirms it. | `[VERIFY against DK's stated mapping]` | Style audit in D16. |

### D0.2 Decisions needed — each with a recommended default

"Accept defaults" adopts every **Recommended** column. Each decision is formally recorded under the listed AD/ADR ID in the deliverable shown.

#### Institute & brand

| ID | Decision | Options | **Recommended default** | Would change my mind | Record |
|---|---|---|---|---|---|
| DN-01 | Programme brand | KLB · KBS · other | **KBS (Kurdish Benchmark System)** in English. Kurdish names to be set by the Standards Committee `[VERIFY]`. Retire "KLB" everywhere before anything is published. | A Kurdish-first brand tests better with candidates. | D9 |
| DN-02 | `INSTITUTE_NAME` | — | Working name: **Kurdish Language Assessment Institute (KLAI)**. It must not carry any party, ministry or person's name. `[TBD]` | — | D9 |
| DN-03 | Legal form (§15) | Public body · university-hosted unit · foundation/NGO · PPP | **Independent non-profit foundation** with (a) a hosting MoU with one KRI university for premises and academic legitimacy, (b) recognition MoUs with both KRG ministries, (c) a charter with a multi-party board, term limits, a public conflict-of-interest register, and an academic advisory board holding a veto on standards. | KRI law makes foundations unable to certify, or recognition only possible for a public body `[VERIFY]`. In that case, start as a university-hosted unit with a charter that guarantees independence. | D9 |

#### Assessment

| ID | Decision | Options | **Recommended default** | Would change my mind | Record |
|---|---|---|---|---|---|
| DN-04 | Variety policy (§6.4) | A separate tests · B variety-of-choice + cross-variety component · C single standard | **A for MVP.** Separate Sorani and Kurmanji tests, each linked to the CEFR independently. Add **B's cross-variety comprehension as an optional endorsement in Phase 3**, alongside the Sorani ↔ Kurmanji Bridge book. **Reject C:** there is no agreed written standard, it would disadvantage both communities, and it is politically non-neutral. | Recognition bodies demand one "Kurdish" result. Answer: a single certificate format, not a single test. | AD-001 (D2) |
| DN-05 | Script policy (§6.5) | Latin only for Kurmanji · both scripts | **Both scripts at MVP for Kurmanji**, because Duhok is a launch site and uses Badînî Arabic script. Items are authored once, transliterated, then human-reviewed. Script-DIF is run on identical content. Writing is accepted in the script chosen at booking. The certificate records the script. **Sorani is Arabic script only** at MVP. | Pilot shows `kmr-Arab` demand < 50 candidates/year. Then defer it to Phase 2 and give Duhok candidates `kmr-Latn` or `ckb`. | AD-002 (D2) |
| DN-06 | Level range of KBS General | One A1–C2 form · two tiers · MST | **Two tiers:** *KBS General Foundation* (A1–B1) and *KBS General Advanced* (B1–C2), overlapping at B1 for linking. A **free online placement test** (M15) routes candidates. MST replaces tiers in Phase 3. | Pilot shows a single 3-hour form keeps acceptable reliability across the whole range. | AD-003 (D2) |
| DN-07 | Speaking mode (§7) | Semi-direct · face-to-face · hybrid | **Hybrid, separating interlocutor from rater:** computer-delivered monologue and picture tasks, plus an 8–10 min **examiner-led interaction** (in centre, or by video for the diaspora). Everything is recorded. **Scoring is done blind from recordings** by certified raters of the candidate's variety; the interlocutor never scores. | Rater supply for Kurmanji proves too thin. Fallback: semi-direct only, with the missing interaction construct disclosed in the handbook. | AD-004 (D2) |
| DN-08 | Reporting scale (§7) | CEFR labels only · 0–100 · bands 1–9 · custom | **Per-skill CEFR level + a KBS scale score of 0–120.** Each CEFR level spans 20 points (Pre-A1 0–19 · A1 20–39 · A2 40–59 · B1 60–79 · B2 80–99 · C1 100–109 · C2 110–120 `[ASSUMPTION — C-band split set at standard setting]`), using a piecewise-linear transform of Rasch θ so cut scores land on round numbers. **Overall** = mean of the four skills, rounded half-up. **No minimum-per-skill rule** on the certificate; receiving institutions may set their own. SEM is reported as ± points per skill. 0–100 is avoided because it reads as a percentage. | Recognition bodies insist on an IELTS-like 1–9. A concordance can still be published later. | AD-005 (D6) |
| DN-09 | "General academic competencies" (§4) | Separate module · exclude | **Exclude it from KBS.** It is a different construct with a different validity argument. Revisit as a separate product only if a university partner funds and validates it. | A ministry formally requires it for admission. | AD-006 (D2) |
| DN-10 | Certificate validity (§12) | Permanent + recency recommendation · fixed expiry | **Permanent certificate**, with a published **recommended recency of 2 years** that receiving institutions apply. | A major recognition body requires a printed expiry. | AD-007 (D6) |
| DN-11 | Arabic on certificate (§12) | No · optional · always | **Default bilingual:** candidate's variety/script + English. An **Arabic-language page is available on request** for Iraqi federal bodies. | Federal ministries require Arabic on all certificates `[VERIFY]`. | AD-008 (D6) |

#### Platform

| ID | Decision | Options | **Recommended default** | Would change my mind | Record |
|---|---|---|---|---|---|
| DN-12 | Hosting and data residency | KRI on-prem · international cloud · split | **One portable stack (containers, open-source DB, S3-compatible storage)**, primary in an **EU-jurisdiction region** with institute-held encryption keys. Centre servers in KRI hold only session-scoped encrypted data and purge after sync. Rationale: GDPR and stronger rule of law for diaspora candidates; lowers compelled-access risk (§3.3). | KRI/Iraqi law requires in-country residency for KRI residents' data `[VERIFY current law]`. Then go dual-region: KRI residents in-region, diaspora in EU. | ADR-009 (D5) |
| DN-13 | Remote proctoring | MVP · later | **Not in MVP.** Pilot in Phase 3 for lower-stakes uses only, always with an in-centre alternative and human review of every flag. | — | AD-009 (D2) |
| DN-14 | Payments | — | **Local wallets/bank apps through a licensed aggregator** (candidates named in §11 M3 `[VERIFY]`), **cash at centre**, **institutional vouchers**, and **international cards through one PSP** for the diaspora. Equity: fee waiver quota (e.g. 10 % of seats `[ASSUMPTION]`). | — | D3 |

#### Learning Series

| ID | Decision | Options | **Recommended default** | Would change my mind | Record |
|---|---|---|---|---|---|
| DN-15 | `SERIES_NAME` | — | Working title **"Pêngav / پێنگاو" ("step")** with an English subtitle such as "Kurdish, step by step". It works across both varieties and avoids the "… for Everyone" pattern. `[VERIFY with Standards Committee + trademark search]` | Kurmanji or Sorani speakers reject the form. Alternative: variety-specific names under one series mark. | D16 |
| DN-16 | `DK_LICENCE` (§16) | Path A: emulate, new content · Path B: licensed co-edition | **Path A as the plan of record.** In parallel, send DK an **exploratory co-edition enquiry in Phase 0**: it costs little, and a "yes" would save illustration cost and remove trade-dress risk. **Get a legal look-and-feel opinion before the first design brief.** Pending that opinion, emulate formats, page logic and illustration style closely, but keep **cover, logo and primary brand colours distinct**. | DK grants a licence (switch to Path B). Legal advice says close page-design emulation is unsafe (increase differentiation). | ADR-010 (D5) / D16 |
| DN-17 | Instruction language (§16.3) | A Kurdish-only · B bilingual editions · C Kurdish core + glossary companions | **Per market:** KRI and Kurdish-schooled learners → **A** (Kurdish-only, visual-first, closest to EFE). Diaspora, heritage and L2 → **C** (Kurdish core + glossary companions; **English first**, then Arabic, Persian, Turkish, German, Swedish as demand shows). **B is rejected:** it multiplies editions and dilutes immersion. | Strong institutional demand for one language pair (e.g. a German school authority). | D15 |
| DN-18 | Romanization scaffold (§16.3) | None · Hawar-based · ad hoc | For **Sorani editions**, use a **Hawar-based Kurdish Latin transliteration** (with agreed forms for ڵ, ڕ, ح, ع, e.g. `ll`/`rr` or `ł`/`ř` `[VERIFY Standards Committee]`). It appears in the Script & Literacy Starter and in L1 U1–U6, fades through L1, and is **withdrawn from L2**. It doubles as preparation for Kurmanji Latin. **Kurmanji Arabic-script editions** mirror this with Latin support. | Pilot shows learners become dependent on the scaffold. Then withdraw it earlier. | D16 |
| DN-19 | EPUB format | Fixed-layout · reflowable | **Fixed-layout** for Course and Practice Books, which are spread-designed. **Reflowable** for the Grammar Guide and Teacher's Guides. The **Hub (M15)** is the primary accessible and interactive channel. | Accessibility audit shows fixed-layout EPUB fails essential needs. Then the Hub becomes the accessible edition of record. | ADR-010 (D5) |
| DN-20 | Pricing and equity | — | **Tiered.** Subsidised KRI print price; **free Hub audio and answer keys** for all buyers; **free or bulk-licensed access for public programmes** (KRG schools, diaspora mother-tongue schools, refugee programmes); diaspora retail at market price. | Funder grant covers free distribution. | D10 |
| DN-21 | Content licence | Institute copyright · open licence · split | **Split.** Course books stay under institute copyright (revenue + quality control). **Open licence (CC BY 4.0)** for the descriptors, RLD core lists, rubrics and sample tests, to build legitimacy and adoption. | Funder requires open licensing of all outputs. | D16 |
| DN-22 | Firewall cooling-off (§16.1) | — | **12 months** between authoring live/pretest items and book authoring (in either direction), plus a conflict-of-interest register. | Staff shortage makes 12 months unworkable. Floor: 6 months + exposure audit. | D16 |

### D0.3 Tensions flagged in the parameters

1. **Kurmanji Arabic script: test vs books.** DN-05 puts `kmr-Arab` testing in the MVP (Duhok). §17 puts Kurmanji Arabic-script *book editions* in Phase 2. Duhok learners therefore get a test before a matching coursebook. Mitigation: provide a Hub-only Arabic-script rendition of the L1 Practice content in Phase 1 (`[DECISION NEEDED]`; default **accept the gap**, use the Hub stopgap).
2. **Close emulation vs IP risk.** v3.1 asks for close emulation of page design and colour system. That is where trade-dress claims attach. DN-16 keeps emulation but adds a legal gate and a distinct brand layer.
3. **One level range vs reliability.** An A1–C2 single form is long or unreliable at the extremes, hence the two tiers in DN-06.
4. **Diaspora centre vs data safety.** The diaspora centre location affects which privacy law applies and which candidate populations attend. It is open in OQ-03.

### D0.4 Open questions (answers sharpen later deliverables; none block D2)

| ID | Question | Affects |
|---|---|---|
| OQ-01 | Is there a known first "anchor user", such as a ministry, employer or university that will accept KBS in Year 1? | A-01, recognition plan (D9) |
| OQ-02 | Is there an actual budget envelope or a named funder? | D10 |
| OQ-03 | Where will the diaspora centre be (Germany, Sweden, UK …)? | Privacy law (D7), series support language (DN-17) |
| OQ-04 | Is there existing staff or a partner university for psychometrics? | A-05, staffing (D10) |
| OQ-05 | Does the Kurdish Academy (KRI) or another body have orthography standards the Standards Committee should adopt as a starting point? `[VERIFY]` | §6.6, series orthography (D16) |
| OQ-06 | Are any Kurdish speech or text corpora available under licence through partners? | RLD (§6.3), ASR research track |
| OQ-07 | Has DK been contacted already? | DN-16 |
| OQ-08 | Are there contacts in diaspora mother-tongue education authorities (e.g. German or Swedish municipalities) for pilots? | Recognition, series pilots |

---

## D1 — Executive summary (≤ 1 page)

**Mission (≤ 50 words).** KBS gives every Kurdish speaker and learner, in Kurdistan or the diaspora, a fair, trusted and safe way to prove their Kurdish. It does this through rigorous CEFR-linked certification in their own variety and script, and through a learning series that shares the same standards.

**3-year vision.** By 2029, KBS General runs in Sorani and Kurmanji (both scripts) at KRI and diaspora centres. It is recognised by both KRG education ministries and at least three employers or universities outside the KRI. It is on the path to ALTE membership and publishes an annual technical report. Pêngav Levels 1–4 are in print and on the Hub, with measured learning outcomes.

**What we are building.**
- **The Institute:** an independent foundation (DN-03) that owns the standards, item bank, rating quality and certificates. A Standards Committee per variety governs acceptable variation.
- **The Platform:** a portable, open-source **modular monolith** with offline-first centre delivery. A power cut costs no data and no time. Signed PDF + QR certificates at MVP, W3C Verifiable Credentials from Phase 2. Minimal data, no ethnic, political or religious fields, and an alternative ID pathway for stateless candidates.
- **The Learning Series ("Pêngav"):** adult studybooks emulating DK *English for Everyone*'s format, wording style, exercises, artwork style and page logic, with **all content newly written and illustrated**. They share the CEFR descriptors and Kurdish RLD with KBS, behind a firewall that keeps test items out of the books.

**Key choices (defaults).** Separate Sorani and Kurmanji tests (AD-001). Kurmanji in Latin and Arabic script (AD-002). Two-tier General test (AD-003). Hybrid speaking, scored blind from recordings (AD-004). Per-skill CEFR + 0–120 scale, with per-skill results as the primary result (AD-005). Fixed linear forms and human rating at MVP; MST, CAT and automated scoring only behind numerical readiness gates.

**Biggest risks.** (1) **Recognition**: a certificate nobody accepts. Mitigation: anchor users before launch. (2) **Small calibration samples** for Kurmanji. Mitigation: paid pilot cohorts plus an international psychometric partner. (3) **Candidate safety** for diaspora candidates. Mitigation: data minimisation and residency (ADR-009). (4) **Orthography politics**. Mitigation: per-variety committees and an acceptable-variation policy. (5) **Trade-dress claims** from close EFE emulation. Mitigation: legal gate and DK enquiry (DN-16).

**Timeline and cost (ranges, `[ASSUMPTION]`).** Phase 0 (9–12 months, USD 0.4–0.9 M) → Phase 1 MVP/pilot (12–18 months, USD 1.5–3.5 M) → first live window about 20–28 months from start.

### D1.2 Phase 1 MVP scope (MoSCoW)

**Must have**
| Area | Scope |
|---|---|
| Institute | Legal entity; Board; Standards Committees (Sorani, Kurmanji); DPIA; candidate handbook; acceptable-variation policy v1; malpractice and appeals procedures |
| Assessment | KBS General Foundation + Advanced in `ckb`, `kmr-Latn`, `kmr-Arab`; L/R/W/S; fixed linear forms (≥ 2 parallel forms per tier per track); Rasch calibration from pilots; CEFR standard setting per variety (CoE 2009 Manual); MFRM rater monitoring (offline analysis acceptable); reliability and DIF report before first live release |
| Delivery | Centre CBT at Erbil, Sulaimani, Duhok + 1 diaspora centre; local delivery server with full offline session; per-response autosave and exact-time resume; paper-based fallback with scanning; Kurdish keyboards + on-screen keyboard + practice period |
| Platform | M1 public site (`ckb`, `kmr-Latn`, `kmr-Arab`, `en`); M2 candidate portal incl. alternative ID pathway; M3 payments (local wallet aggregator, cash, vouchers, cards); M4 delivery client; M5 item bank with normalization layer; M6 manual form assembly + encrypted package publishing; M7 operations console; M8 rating portal (blind allocation, double rating, seeding); M9 results & signed PDF certificates with QR; M10 basic verification via candidate share codes; M14 IAM/MFA/audit log |
| Security & privacy | Data minimisation review per field; encryption at rest, in transit and in packages; signing keys in HSM/KMS; no public name search; pen test before go-live |
| Series | Script & Literacy Starter + Level 1–2 Course & Practice Books in Sorani and Kurmanji (Latin) (10 books); EFE style audit → house style; content model (single source); M15 Learning Hub v1: audio + offline packs, transcripts, answer keys, free placement test |

**Should have**
- Arabic certificate page on request (DN-11).
- SMS/WhatsApp notifications.
- Psychometrics workbench exports to R/Python (M12, basic).
- Support helpdesk (M13).
- Teacher pilot materials for L1.
- Hub-only `kmr-Arab` rendition of L1 Practice (D0.3 #1).
- Free sample tests per track.

**Could have**
- Interactive book exercises on the Hub.
- Kurdish-calendar display.
- Institutional portal for bulk registration (M11 light).
- Webhooks for verifiers.

**Won't have (this phase)**
- KBS Academic, Professional, Junior.
- MST and CAT.
- Automated scoring of writing or speaking (research track only).
- Remote proctoring.
- Verifiable Credentials (Phase 2).
- Blockchain anchoring.
- Varieties beyond Sorani and Kurmanji.
- Series Levels 3–4, Grammar Guide, Vocabulary Builder, Kurmanji Arabic-script print editions.
- General academic competencies module.

---

### Changes to prior deliverables
None. This is the first deliverable. IDs reserved: AD-001…AD-009, ADR-009, ADR-010, DN-01…DN-22, A-01…A-09, OQ-01…OQ-08. ADR-001…ADR-008 are reserved, in §14 order, for D5.

### §19 self-check
- ✅ Varieties, scripts and offline delivery addressed (DN-04/05/12, MVP delivery). Candidate safety drives hosting (DN-12) and the minimisation items.
- ✅ Every `[DECISION NEEDED]` has a recommended default with "would change my mind". Data-hungry features (CAT, MST, automated scoring, remote proctoring) are deferred behind gates, to be quantified in D2/D8.
- ✅ No invented laws, prices or partner commitments. Budget figures are labelled ranges; legal, vendor and DK facts are tagged `[VERIFY]`.
- ⏳ FR/NFR IDs and acceptance criteria start in D3. Curriculum ↔ descriptor traceability starts in D14/D13.
- ✅ Series plan keeps EFE emulation with newly created content and a legal gate (DN-16).

**Next deliverable: D2 — Assessment framework & test specifications (§4–§8).**
