# Oncology-Data-Literacy — PLAN.md

> Status: Draft · Version: 0.1.0 · Last updated: 2026-06-28 · Owner: TBD (maintainer) · Lane: donated

A set of **short, open, self-contained courses that teach people to read cancer statistics
correctly** — incidence and mortality **rates**, **survival** statistics, and **screening**
evidence — so that patients, families, patient advocates, health journalists, students, and the
general public are not misled by the numbers that dominate cancer headlines and well-meaning
advice. The output is **open educational resources (OER)**, not a clinical tool: it explains *how
to interpret* a statistic, never *what an individual should do about their cancer*.

The single most important design fact is that **this project lives or dies on statistical and
clinical correctness**. A statistics-literacy course that is itself subtly wrong — that conflates
survival with mortality, mistakes lead-time bias for benefit, or implies a screening
recommendation — actively *manufactures* the misconception it claims to cure, and does so with the
authority of an "educational resource." Correctness is therefore not a quality nicety; it is the
safety-critical core, and it is gated by **independent expert review** (a biostatistician/cancer
epidemiologist for statistical accuracy, an oncologist for clinical framing, and a patient advocate
for plain-language safety) before anything ships.

---

## Executive summary

Cancer statistics are among the most widely cited and most widely misunderstood numbers in public
life. "Five-year survival has doubled" is routinely read as "screening saves lives" when it can be
fully explained by lead-time bias and overdiagnosis. "1 in 2 people will get cancer" is read as a
personal coin-flip rather than a lifetime, age-driven population figure. A relative-risk headline
("doubles your risk!") hides a tiny absolute change. A screening test "99% accurate" is mistaken
for "99% of positives have cancer." These are not edge cases; they are the *default* way cancer
numbers are misread, and the errors change real decisions and real anxiety.

Oncology-Data-Literacy delivers three short, free, openly-licensed courses — **Reading Rates**,
**Reading Survival**, and **Reading Screening Evidence** — each built around the specific, named
misconceptions that recur in cancer coverage, taught with worked examples drawn **only from
open-access, aggregate, published cancer statistics** (e.g., NCI SEER\*Explorer, CDC US Cancer
Statistics, IARC Global Cancer Observatory — each with its reuse terms verified before use). Every
statistical assertion in the courseware carries a **citation with its data vintage and provenance**;
nothing is asserted that a learner could not trace back to a verifiable, licensed source.

**This project handles no patient data.** It uses only aggregate, de-identified, published
statistics; controlled-access databases (the individual-level SEER research file under DUA, dbGaP,
EGA, biobanks) and any identifiable patient data are **out of scope by design**. There is no
registry, no data store of people, and no individualized risk calculator.

The project is **medium risk-tier overall** for statistical-accuracy reasons, but its
**patient-facing survival and screening content is treated as HIGH risk-tier**: per the Elyos
cancer guardrails, patient-facing material is education-only, carries a persistent "not medical
advice" frame, and ships only with **oncologist and patient-advocate sign-off**. The screening
course in particular is engineered to teach people *how to weigh screening evidence and have a
shared-decision conversation* — it must **never** tell an individual whether to be screened.

Honesty note: **no delivery partner, educator, or requesting organization is yet secured.** Every
delivery-dependent task is marked `TO BE SECURED` with `verifiedNeed: false` until a real
educator/advocacy organization/library adopts the courses with real learners. The project is **not
"shipped" on merge**; it is shipped only when a real cohort of learners completes a course and we
can measure a reduction in the targeted statistical misconceptions, with all content
expert-signed-off.

**Partner-acquisition plan (dated) and build-vs-mothball/pivot decision rule.** Outreach is
time-boxed against the build, not left as an open `TBD`: by **2026-08-31** ≥ 3 candidate delivery
partners (a patient-advocacy organization, a public-library/adult-education program, a community
college or journalism-school health unit, or a patient-advocate research-primer program) are in
active conversation and the **expert reviewers are secured** (the M0 gate); by **2026-10-31** a
named delivery partner + steward is secured (the M6 gate). **Decision rule:** if no expert reviewer
is secured by the M0 exit date, content authoring (M2+) does **not** begin and the project holds at
M1 (sources + provenance infrastructure). If no delivery partner is secured by **2027-01-31**
(≈ M5 completion), the project does **not** ship to no one: it either **(a) pivots** the last-mile
beneficiary — e.g., donate the courseware to an existing OER library (such as a national cancer
charity's education hub, a university health-comms program, or OER Commons) as a maintained
reference resource with measured *download/reuse* outcomes — or **(b) mothballs** to
maintenance-only, archived, no further HIGH-tier content, with the decision recorded in governance.
The expert-reviewed courseware remains a valuable public good in either case.

---

## Problem & beneficiaries

**Who is helped (directly):**

- **Patients and families** trying to make sense of a diagnosis, a prognosis number, or a screening
  letter, who are routinely handed (or find online) statistics they have no framework to interpret —
  and who are vulnerable to both false reassurance and unnecessary fear.
- **Patient advocates and peer-support volunteers** who relay and translate research and statistics
  to communities and need to do so accurately (pairs with the sibling `patient-advocate-research-primer`).
- **Health journalists, science communicators, and students** (public health, nursing, journalism,
  data science) who *produce* the coverage that misleads the public when statistics are mishandled —
  a high-leverage upstream audience.
- **Educators and librarians** running adult-education, health-literacy, or media-literacy programs
  who lack a vetted, ready-to-teach module on cancer statistics specifically.

**Who is helped (ultimately):** the **general public**, who receive more accurate cancer
information because the people who relay it — clinicians' patients, advocates, and journalists — can
read the numbers correctly and resist the predictable misreadings.

**The need.** The specific misconceptions are well-documented in the medical-decision-making and
risk-communication literature (e.g., Gigerenzer and Wegwarth on screening statistics; Welch on
overdiagnosis; the SEER and USPSTF communications guidance): people systematically (1) read rising
**5-year survival** as proof that earlier detection or treatment saves lives, when lead-time bias,
length-time bias, and overdiagnosis can produce exactly that pattern with **no mortality benefit**;
(2) confuse **relative** and **absolute** risk; (3) confuse a test's **sensitivity** with its
**positive predictive value** (the base-rate fallacy); (4) read **crude** rates as if age structure
did not matter; and (5) treat a population **lifetime risk** as a personal probability. Accurate,
plain-language, openly-licensed teaching material that targets *these specific errors* with *real
cancer data* is scarce; what exists is often paywalled, buried in textbooks, or aimed at clinicians
rather than patients and the public.

**Verified need / partner: TO BE SECURED.** No specific educator, advocacy organization, library,
or requesting body has yet agreed to adopt or co-develop the courses. Target partner profiles to
pursue: a national or disease-specific **cancer charity / patient-advocacy organization** with an
education arm; a **public-library or adult-education** health-literacy program; a **community
college or journalism school** health-reporting unit; or an existing **OER platform** (OER Commons,
a university OpenCourseWare) willing to host and route learners. Until one is secured, the project
builds the curriculum, the vetted-source/provenance infrastructure, and the three expert-reviewed
courses, and marks all delivery/adoption work `TO BE SECURED` with `verifiedNeed: false`. Outreach
is **dated, not open-ended** (see the partner-acquisition plan above), and a **build-vs-mothball/
pivot decision rule** governs what happens if the dates slip — pivot the last-mile beneficiary to an
existing OER host, or mothball to maintenance-only, rather than declare victory on merge.

---

## Goals and non-goals

**Goals**

- Publish three short, free, openly-licensed (**CC-BY-4.0**) courses — **Reading Rates**, **Reading
  Survival**, **Reading Screening Evidence** — each built around a named inventory of the specific
  misconceptions it cures.
- Teach every concept with **worked examples drawn only from open-access, aggregate, published
  cancer statistics**, each carrying a citation, **data vintage**, and provenance.
- Achieve and *prove* **statistical and clinical correctness** via independent expert sign-off
  (biostatistician/epidemiologist + oncologist + patient advocate) before any course ships.
- Frame all patient-facing material as **education only, not medical advice**, with screening
  content explicitly supporting *shared decision-making* rather than recommending for/against
  screening.
- Demonstrate a **measurable reduction in the targeted misconceptions** in a real learner cohort
  (pre/post instrument), not just publication.
- Make the courses **accessible (WCAG 2.2 AA), plain-language, and translation-ready** so the
  benefit reaches non-expert and non-English audiences (translations themselves expert-reviewed
  per language).

**Non-goals**

- **Not medical advice, not a clinical decision aid, not an individualized risk calculator.** It
  never tells a person their prognosis, whether to be screened, or what treatment to choose.
- **Not a data store, registry, or patient database.** It collects no patient data and operates over
  aggregate/published statistics only.
- **Not original epidemiological research or reanalysis** of patient-level data (that is the remit of
  sibling projects like `ewing-expression-reanalysis` / `incidence-explorers`, which use their own
  vetted aggregate data). This project *teaches reading*, it does not generate new findings.
- **Not a comprehensive oncology curriculum** — it covers statistical literacy for cancer numbers,
  not biology, diagnosis, or treatment.
- **Not exhaustive across all cancer types at launch** — depth and correctness on the cross-cutting
  statistical concepts first, using a few well-chosen cancer examples; per-cancer breadth is backlog.
- **Not a vehicle for any screening program's, vendor's, charity's, or pharma's promotion** — it is
  source-neutral and refuses content that primarily serves a for-profit or advocacy agenda over the
  learner's understanding.

---

## Success metrics (outcomes)

Outcome-centric and learner-first. Page views, sign-ups, and "modules published" are explicitly
**not** success — the success object is *corrected understanding in real people*, ethically and
accurately delivered.

| Metric | Baseline | Target | How measured |
|---|---|---|---|
| Misconception reduction in a real learner cohort | pre-test score | statistically meaningful pre→post improvement on the targeted-misconception instrument (e.g., median items-correct rises, and the "survival↑ ⇒ screening saves lives" item flips for a majority) | Validated pre/post instrument administered to a pilot cohort |
| Statistical claims traceable to a licensed source | n/a | **100%** of statistical assertions in shipped courseware carry a citation + **data vintage** + verified license | Citation-coverage check (CI) + reviewer audit |
| Expert sign-off before patient-facing content ships | n/a | **100%** of survival/screening (HIGH-tier) content has recorded oncologist **and** patient-advocate sign-off; **100%** of statistical content has biostatistician/epidemiologist sign-off | Reviewers ledger / governance log |
| "Not medical advice" + no-recommendation compliance | n/a | **0** instances of individualized advice or a for/against-screening recommendation in shipped content; persistent disclaimer present on every module | Editorial-rubric checklist + reviewer audit + red-flag scan |
| Source-license compliance | n/a | **0** reused figures/data under a license incompatible with CC-BY output (e.g., NC/ND sources) without relicensing or redraw-from-public-domain | Source-licensing register + reviewer audit |
| Data-vintage freshness | n/a | **0** statistics served past their `reviewBy` date without an auto-flag and refresh/re-sign-off | Staleness check against `dataVintage`/`reviewBy` |
| Accessibility | n/a | Core courseware meets **WCAG 2.2 AA**; readability targets met for plain-language tracks | Automated a11y checks + manual audit + readability scoring |
| Real adoption (the deed) | 0 | ≥ 1 educator/advocacy org/library delivers a course to a real cohort, OR (pivot) an OER host adopts it with measured reuse | Partner attestation / host adoption record |
| Independent reuse / translation | 0 | ≥ 1 third-party reuse or community translation (post-delivery) | Repository/host telemetry + translation PRs |

The **defining success outcome** (Definition of Shipped): a real learner cohort completes a course
and shows a measurable reduction in the targeted statistical misconceptions, with all content
expert-signed-off, every statistic sourced and provenance-tracked, and the "not medical advice"
frame upheld throughout.

---

## Scope

**In scope**

- An **editorial guardrail rubric** (statistical-accuracy rules, "no statistic without a source,"
  "no medical advice / no recommendation," correct-endpoint rule) — built **first** and applied to
  every module.
- A **curriculum map** with explicit learning objectives and a named **misconception inventory** per
  course.
- A **source-licensing & provenance register** that verifies and records each statistical source's
  reuse terms before any figure or datum is used.
- A small set of **aggregate teaching datasets** (published SEER\*Explorer / CDC US Cancer Statistics
  / IARC GCO tables and the like), each with a data dictionary and provenance.
- Three courses — **Reading Rates**, **Reading Survival**, **Reading Screening Evidence** — each with
  explanatory content, **worked examples from real aggregate data**, exercises, and a self-check.
- **Illustrative-only** natural-frequency / base-rate widgets (e.g., a "translate this test
  accuracy into natural frequencies" teaching calculator) that operate on *published/teaching*
  numbers and explicitly **do not** produce a personal risk estimate.
- A **validated pre/post misconception instrument** and a **learning-outcome eval** measuring
  misconception reduction, plus an **accuracy regression** that flags any drift in shipped claims.
- **Accessibility, plain-language, and translation-readiness** passes.
- A **delivery/handoff** to a real partner and the outcome measurement that constitutes shipping.

**Out of scope (explicitly will NOT do)**

- **Any individual-level, identifiable, or controlled-access patient data** — the SEER research file
  under DUA, dbGaP, EGA, biobanks, hospital records, or anything requiring authorized access/IRB.
  Aggregate, de-identified, published statistics **only**.
- **Any medical advice, prognosis, diagnosis, or screening recommendation** for an individual; any
  "should I get screened / tested / treated" answer. The courses teach *how to read the evidence and
  prepare for a shared-decision conversation*, full stop.
- **Building a registry, cohort, or patient data store.** (Where the Elyos cancer guardrails discuss
  registries — consent-first, deceased/aggregate-only, governance-schema-not-a-data-store — they are
  **N/A here because no registry is built**; this is stated so the boundary is explicit, not assumed.)
- **Original research, reanalysis, or new epidemiological estimates.** The project teaches
  interpretation of *already-published* statistics; it does not compute new ones (beyond trivially
  re-deriving textbook quantities from published aggregate inputs for worked examples).
- **Cancer-type-specific clinical guidance** (staging, treatment, biomarker interpretation as advice).
- **Reusing non-commercial (NC) or no-derivatives (ND) licensed material** inside the CC-BY output
  without relicensing permission or redrawing the figure from a public-domain source.
- **Disease/charity/vendor promotion**, fundraising, or partisan framing.

When a request or contribution drifts into the refused set (e.g., "add a calculator that tells a
user their personal cancer risk," or "tell readers they should get screened at 40"), the editorial
rubric requires it be **refused and reframed** into the in-scope teaching equivalent (how to read a
risk model's output and its uncertainty; how to weigh screening evidence and talk to a clinician).

---

## Solution approach & architecture

This is a **content/curriculum pipeline**, not an application; the "architecture" is the authoring,
sourcing, review, build, and delivery pipeline plus the lightweight tooling that enforces the
guardrails.

**Formats & stack.** Source content authored in **Markdown/MDX** in a pnpm-managed repository
(TypeScript/ESM for the small amount of tooling and any interactive widgets), built into a static
OER site (e.g., an Astro/Docusaurus-class static generator — chosen in M0) and exported to
**portable formats** (HTML, print-ready PDF, and an OER-package/SCORM-or-Common-Cartridge export so
LMS-based partners can import it). Interactive teaching widgets (natural-frequency visualizers) are
small client-side TypeScript components operating on static teaching numbers — **no backend, no user
data, no patient data**. Code license **MIT**; content/datasets/docs **CC-BY-4.0**.

**Pipeline components**

1. **Editorial guardrail rubric (`/editorial`) — built first.** The safety-critical spec every
   module is authored and reviewed against. It encodes: the **no-statistic-without-a-source** rule;
   the **correct-endpoint** rule (mortality, not 5-year survival, is the right yardstick for
   screening/early-detection benefit; net/relative survival vs observed survival distinctions);
   the **absolute-before-relative** rule (always give absolute risks and natural frequencies, not
   bare relative risks); the **no-medical-advice / no-recommendation** rule and the persistent
   disclaimer; the **uncertainty** rule (confidence intervals, small-number instability, data
   vintage shown); and the **refuse-and-reframe** rule for out-of-scope requests. It also defines the
   misconception-targeting method: each learning objective names the misconception it corrects and
   the evidence that it is a real, common error.

2. **Curriculum map & misconception inventory (`/curriculum`).** Learning objectives for the three
   courses, sequenced, each tied to a named misconception and a worked example. This is the contract
   the content tasks fulfil and the assessment instrument tests against.

3. **Source-licensing & provenance register (`/sources`).** A machine-readable register: for each
   source, its name, publisher, the specific table/figure/series used, **data vintage** (e.g., "SEER
   incidence 2017–2021, 2024 submission"), retrieval date, URL, **license/legal status** (public
   domain US-gov work vs CC-BY vs NC/restricted), and a **CC-BY-compatibility verdict**. A figure or
   datum may not be used in courseware until it has a register entry with a compatible verdict.

4. **Aggregate teaching datasets (`/data`).** Small, well-documented, **aggregate-only** extracts
   (published rate tables, survival tables, screening trial summary statistics) with a data
   dictionary, used to build worked examples. No individual-level data, ever.

5. **Course content (`/courses/{rates,survival,screening}`).** MDX modules: concept explanation →
   worked example from real aggregate data → common-misconception callout ("Why the headline is
   wrong") → exercise → self-check. Every statistical claim carries an inline citation keyed to the
   source register.

6. **Provenance/citation tooling (`/tools/cite`).** A build-time check that (a) every statistical
   assertion is keyed to a register entry (**no source → build fails**), (b) every cited source has a
   `dataVintage` and a `reviewBy`, and (c) no source flagged NC/ND/incompatible is used. A
   **staleness check** flags any statistic past its `reviewBy` for refresh + re-sign-off.

7. **Assessment & eval (`/assessment`, `/tools/eval`).** A validated pre/post **misconception
   instrument** (items mapped to the inventory) and an eval harness that (a) scores misconception
   reduction in a cohort and (b) runs an **accuracy regression** — a fixture set of "tricky" claims
   the courseware must get right — so edits cannot silently reintroduce an error.

8. **Accessibility, plain-language & i18n (`/a11y`, `/i18n`).** WCAG 2.2 AA checks, readability
   scoring/plain-language pass, and string/structure extraction so courses are translation-ready;
   translations are expert-reviewed per language.

**Key decisions**

- **Correctness is a release gate, not a review nicety:** no course ships without the relevant expert
  sign-off, and the accuracy regression + citation-coverage checks run in CI.
- **Sourcing is conservative and public-domain-first:** prefer US-government public-domain statistics
  (SEER, CDC, USPSTF, NCI) for any reused figure/datum so CC-BY output is unencumbered; cite — never
  copy — copyrighted or NC sources.
- **No patient data, no backend, no registry:** the threat surface for privacy is removed by
  construction, not mitigated after the fact.
- **Screening content is shared-decision-making, not recommendation:** enforced by the editorial
  rubric and the oncologist + advocate review.

---

## Data, licensing & compliance

**This section leads with the binding Elyos cancer guardrails and is deliberately conservative.**

**Cancer data guardrails (binding).**

- **Open-access / aggregate / de-identified data ONLY.** Every datum used in the courseware is a
  published, aggregate statistic. **Controlled-access and identifiable patient data are OUT OF
  SCOPE** — the individual-level SEER research database (DUA), dbGaP, EGA, biobanks, and any
  record-level patient data are never accessed or stored. The project keeps no patient data of any
  kind.
- **No medical advice.** All content is **education only**; every module carries a persistent
  **"Education only — not medical advice; talk to your clinician about your situation"** frame.
  Patient-facing content (survival, screening) is **riskTier high** and ships only with **oncologist
  and patient-advocate review**.
- **Registries:** none is built. The guardrail principles for registries (consent-first;
  deceased/aggregate only; the governance/schema is not a data store) are **N/A here** and noted
  only to make explicit that this project does not collect or store people's data.
- **Provenance on every assertion.** Every statistical claim is traceable to a licensed source with
  its data vintage; "no statistic without a source" is enforced in CI.

**Candidate sources and their reuse terms (each verified and recorded before use).** Licenses below
are the *starting hypothesis to verify per source/figure in the M1 register* — not a final ruling:

| Source | Use | Reuse status (to verify) | Notes / CC-BY compatibility |
|---|---|---|---|
| **NCI SEER / SEER\*Explorer** (aggregate stats) | Incidence/mortality/survival rate tables, trends, stage distribution | US-gov work → generally **public domain** | Preferred reuse source; aggregate published tables only — **not** the DUA research file |
| **CDC US Cancer Statistics / WONDER** | Incidence/mortality, screening rates | US-gov work → generally **public domain** | Aggregate query results; record vintage + suppression rules |
| **USPSTF** recommendations & evidence | Screening evidence framing, endpoints | US-gov → **public domain** | Cite for *how evidence is weighed*; never restate as a personal recommendation |
| **IARC Global Cancer Observatory (GLOBOCAN)** | Global incidence/mortality, intl comparisons | IARC **terms of use** — verify reuse/derivative + attribution | May restrict commercial/derivative use — **verify before reuse**; attribute precisely |
| **Our World in Data** (cancer) | Trends, visual explanations | **CC-BY-4.0** | CC-BY-compatible; attribute |
| **Cancer Research UK / other charity statistics** | Plain-language stats, figures | Often **CC-BY-NC-SA** or bespoke — verify | **NC is INCOMPATIBLE** with CC-BY output — do **not** embed; redraw equivalent from public-domain data or cite-only |
| **Cochrane / academic papers** (e.g., screening RCTs, Gigerenzer/Welch on bias) | Concepts, named biases, methods | **Copyrighted** | **Cite-don't-copy**; teach the concept, reproduce no protected figures/text |

**The headline license gate:** the output is **CC-BY-4.0**, so any **embedded** figure or dataset
must be **public-domain or CC-BY-compatible**. Attractive sources (some charity figures, possibly
GLOBOCAN derivatives) may be **NC/ND or restricted**; the rule is **redraw the equivalent from
public-domain US-gov aggregate data, or cite-without-embedding** — never silently embed incompatible
material. This is enforced by the source register's compatibility verdict and a reviewer audit.

**Provenance model.** Each statistical assertion is keyed to a `Source` register entry: `{ name,
publisher, table/figure id, dataVintage, retrievalDate, url, legalStatus, ccByCompatible,
reviewBy }`. The citation-coverage check fails the build on any uncited statistic; the staleness
check flags any entry past `reviewBy` (cancer statistics are reissued — e.g., annual SEER
submissions — so a stale figure is a real, recurring failure mode, handled as a visible gated event,
not a silent error).

**Privacy / PII stance.** **The project collects no personal data and has no backend.** The only
human data it may touch is **assessment responses** from the optional pre/post instrument; these are
collected by the *delivery partner* under their own consent/privacy terms, and the project's
reference implementation keeps them **anonymous and aggregate** (no names, no identifiers; opt-in;
deletable), used solely to measure misconception reduction. No secrets, tokens, or PII are written
to logs or committed files (Elyos rule).

**Attribution.** Courseware attributes every source per its license (CC-BY/public-domain notices);
redistribution preserves attribution per CC-BY-4.0. Expert reviewers are credited (with consent,
version-scoped) in a reviewers ledger.

---

## Quality, review & risk gates

**Risk tier: MEDIUM overall, with HIGH-tier patient-facing content.** Statistical-accuracy content
(rates, methods, the general survival/screening *math*) is **medium** and requires a
biostatistician/epidemiologist reviewer. **Patient-facing survival and screening content is HIGH**
(per the Elyos cancer guardrails: patient-facing cancer material requires credentialed clinical
review and a "not medical advice" frame) and requires **oncologist + patient-advocate** sign-off in
addition. Pure tooling/platform/a11y tasks are low–medium.

**Required reviews before a deed is "done":**

- **Statistical/epidemiological review** — a biostatistician or cancer epidemiologist verifies every
  statistical claim, worked example, and the correct-endpoint/absolute-risk/uncertainty framing.
  **No stats sign-off, no ship** for any course.
- **Clinical (oncologist) review** — for survival and screening (HIGH-tier) content: clinical
  accuracy, safe framing, and confirmation that nothing reads as individualized advice or a
  screening recommendation.
- **Patient-advocate review** — for all patient-facing content: plain-language clarity, dignity,
  harm-avoidance (e.g., no fear-mongering, no false reassurance), and lived-experience sanity check.
- **Maintainer review** — editorial-rubric compliance, citation coverage + license compatibility +
  staleness checks green, accessibility, no PII/secrets, build/CI green.

**Every patient-facing surface is labeled "Education only — not medical advice"** and routes
individual questions to the learner's own clinician / shared decision-making, never to an answer.

**Definition of Shipped (project):** a real learner cohort completes a course and demonstrates a
measurable reduction in the targeted misconceptions, with **all** statistical content
biostatistician-signed-off, **all** patient-facing content oncologist- and advocate-signed-off,
every statistic sourced + provenance-tracked under a CC-BY-compatible license, the "not medical
advice" frame upheld, and accessibility met. Merge alone is not shipped.

---

## Roadmap & milestones

Phased: editorial guardrails + curriculum + sourcing infrastructure first; expert-reviewed content
next, one statistical domain at a time; assessment/eval; partner delivery last and gated on a
secured partner; then sustain.

- **M0 — Foundations, editorial guardrails & reviewer recruitment (cold-start).**
  *Goal:* the correctness-critical scaffolding exists before any course content is authored.
  *Exit:* editorial guardrail rubric (no-statistic-without-a-source, correct-endpoint,
  absolute-before-relative, no-medical-advice/no-recommendation, refuse-and-reframe) merged;
  curriculum map + misconception inventory for the three courses merged; OER repo + static-build +
  CI (lint + link-check + citation-coverage scaffold) green; a one-page **pilot "reading a cancer
  headline" module** drafted as a method proof. **Expert reviewers secured** (biostatistician/
  epidemiologist, oncologist, patient advocate) — the gate that unblocks content authoring.

- **M1 — Source vetting, provenance & teaching datasets.**
  *Goal:* a verified, licensed, provenance-tracked source base before claims are written on top of it.
  *Exit:* source-licensing & provenance register populated with CC-BY-compatibility verdicts and
  data vintages for the launch source set; aggregate teaching datasets + data dictionaries committed
  (aggregate-only, license-cleared); citation-coverage + license-compatibility + staleness checks
  wired into CI and passing on the pilot module.

- **M2 — Course 1: Reading Rates (statistical, medium tier).**
  *Goal:* the foundational rates course, fully sourced and stats-reviewed.
  *Exit:* incidence/mortality/prevalence, crude vs **age-standardized**, **rates vs risk**,
  **absolute vs relative** risk, confidence intervals/small numbers, and trend-reading content drafted
  with worked examples from aggregate data; citation coverage 100%; **biostatistician sign-off**
  recorded.

- **M3 — Course 2: Reading Survival (patient-facing, HIGH tier).**
  *Goal:* the survival course — the highest-misconception area — correct and safely framed.
  *Exit:* observed vs **relative/net** survival, **survival ≠ mortality**, **lead-time bias**,
  **length-time bias**, **overdiagnosis**, stage migration (Will Rogers), median/conditional survival,
  Kaplan–Meier/censoring basics drafted with worked examples; "not medical advice" frame present;
  **biostatistician + oncologist + patient-advocate sign-off** recorded.

- **M4 — Course 3: Reading Screening Evidence (patient-facing, HIGH tier).**
  *Goal:* the screening course that teaches *how to weigh screening evidence*, never whether to screen.
  *Exit:* correct-endpoint (mortality) framing; **sensitivity/specificity/PPV** + **base-rate** via
  **natural frequencies**; **number needed to screen**; **false positives/overdiagnosis/overtreatment**
  as harms; RCT vs observational evidence; **shared-decision-making** framing (explicitly no for/against
  recommendation) drafted with worked examples and the illustrative-only natural-frequency widget;
  **biostatistician + oncologist + patient-advocate sign-off** recorded; refuse-and-reframe verified
  on "should I get screened" style prompts.

- **M5 — Assessment, accessibility, eval & translation-readiness.**
  *Goal:* prove the courses *work* and reach everyone.
  *Exit:* validated pre/post misconception instrument; learning-outcome eval + accuracy-regression
  fixtures green; WCAG 2.2 AA + plain-language pass; translation-ready extraction done. **Kill-gate:**
  if a dry-run of the instrument on a small test group shows **no** movement on the core misconception
  items, the content is reworked before partner delivery rather than shipping an ineffective course.

- **M6 — Partner adoption & delivery (the deed).**
  *Goal:* a real cohort learns from it.
  *Exit (Definition of Shipped):* a secured educator/advocacy org/library delivers a course to a real
  learner cohort (or, per the pivot rule, an OER host adopts it with measured reuse); misconception
  reduction recorded; final expert sign-off of all shipped content confirmed. *(Gated on a secured
  partner — TO BE SECURED.)*

- **M7 — Sustain & maintain (post-delivery).**
  *Goal:* keep the statistics current and the courses healthy.
  *Exit:* maintenance rotation + **data-vintage review cadence** (refresh statistics as new SEER/CDC/
  GLOBOCAN releases land, with re-sign-off) + outcomes record; documented process for adding a new
  course/cancer-type case study or a translation, each expert-gated.

Dependencies flow M0 → M1 → M2 → M3 → M4 → M5 → M6 → M7. The **reviewer-recruitment decision is made
in M0 and gates M2–M6** (no expert, no content authoring). M3/M4 (HIGH-tier patient-facing) block on
both M1 sources and the secured oncologist + advocate reviewers; M6 blocks on a secured delivery
partner.

---

## Work breakdown

The itemized, schema-mapped backlog lives in **`TASKS.md`**: ~21 tasks across milestones M0–M7 plus
a future backlog, each mapped to the Elyos Task JSON schema, with per-task acceptance criteria for
the most important items, milestone Definitions of Done, and a complete example Task JSON for the
first M0 task (the editorial guardrail rubric). The first build item is the **editorial guardrail
rubric** (correctness + no-medical-advice), reflecting that statistical/clinical correctness is the
project's safety-critical core; **reviewer recruitment** and **source vetting** are sequenced before
content authoring so no course is written against an unvetted source or without a reviewer to sign it
off.

---

## Governance, roles & stakeholders

- **Maintainer (Owner): TBD.** Owns the curriculum architecture, the editorial rubric, the build/CI
  checks (citation coverage, license compatibility, staleness, a11y), and merge quality.
- **Reviewers / rotation:** at least one engineering/editorial reviewer for tooling and rubric
  compliance, plus the credentialed expert reviewers below.
- **Credentialed expert reviewers (gate): TO BE SECURED.**
  - **Statistical reviewer** — a biostatistician or cancer epidemiologist; signs off statistical
    correctness on **every** course (medium-tier gate).
  - **Clinical reviewer** — an oncologist; signs off the HIGH-tier patient-facing survival and
    screening content for clinical accuracy and safe framing.
  - **Patient-advocate reviewer** — a cancer patient advocate; signs off plain-language clarity,
    dignity, and harm-avoidance on all patient-facing content.
  - Tracked in a reviewers ledger with credentials and consent. **Sign-off is version-scoped** (it
    attaches to a specific content version + citation set + data vintage and does **not** carry
    forward through later edits, which require re-sign-off — dovetailing with the `reviewBy`
    staleness model). **Name-use limits:** a reviewer's name may appear only for the versions they
    approved, with consent, and may not imply endorsement of content they did not review.
    **Independence/COI:** a reviewer discloses and recuses from any material conflict (e.g., financial
    ties to a screening vendor or program). **Disagreement fallback:** any one expert holds a **veto
    on whether their domain's content is safe/correct to ship**; a maintainer cannot override a "do
    not ship" on substance — the content does not ship, the disagreement is logged and escalated to
    Elyos governance / a second reviewer for a tie-break; for contested HIGH-tier content the project
    prefers a **second reviewer** over shipping on one contested opinion.
- **Steward (last-mile owner): TO BE SECURED** — owns the delivery-partner relationship and the
  cohort delivery + outcome measurement that constitutes shipping.
- **Partner / requestor: TO BE SECURED** — the educator/advocacy org/library/OER host that adopts and
  delivers the courses.
- **Community / board:** the output-license choice (CC-BY-4.0 confirmed) and any edge cases
  (e.g., whether a borderline source is reusable) go through Elyos governance.

---

## Dependencies & integrations

- **External sources (data):** NCI SEER / SEER\*Explorer (aggregate), CDC US Cancer Statistics /
  WONDER, USPSTF evidence, IARC Global Cancer Observatory (GLOBOCAN — reuse terms to verify), Our
  World in Data (CC-BY) — each entered in the source register with a verified verdict and data
  vintage. **No controlled-access databases.**
- **Reference literature (cite-only, copyrighted):** risk-communication and overdiagnosis literature
  (e.g., Gigerenzer & Wegwarth on screening statistics; Welch on overdiagnosis), screening RCT
  reports, Cochrane reviews — taught as concepts, never copied.
- **Tooling:** pnpm + TypeScript/ESM, a static OER generator (chosen in M0), an OER-package export
  (Common Cartridge/SCORM) for LMS partners, automated a11y + readability tooling, CI (citation
  coverage, license compatibility, staleness, link check).
- **Elyos pieces:** `packages/schema` (Task JSON), `CLAUDE.md` work rules + refusal guardrails,
  `docs/good-deed-definition.md` (risk tiers), Elyos governance for license/edge-case decisions.
- **Sibling Elyos projects (coordinate, don't duplicate):** `stats-for-clinicians` (hazard-ratio /
  survival explainers for a clinician audience — share the survival math, differ in audience),
  `patient-advocate-research-primer` (advocates reading the science — natural downstream partner),
  `incidence-explorers` (SEER/GLOBOCAN dashboards — a potential data/example source),
  `cancer-dataset-datasheets` (provenance practice to mirror).
- **Human/decision dependencies (critical path):** the **secured expert reviewers** (made in M0;
  gates all content authoring M2–M6) and a **secured delivery partner/steward** (gates M6).

---

## Risks & mitigations

| Risk | Likelihood | Impact | Mitigation | Owner |
|---|---|---|---|---|
| Course is itself statistically wrong (teaches the misconception it claims to cure) | Medium | Critical | Editorial rubric built first; biostatistician sign-off gate on every course; accuracy-regression fixtures in CI; worked examples re-derived from cited aggregate data | Stats reviewer / Maintainer |
| Content reads as medical advice or a screening recommendation | Medium | Critical | "Not medical advice" frame on every module; **no-recommendation** rule for screening (shared-decision framing only); oncologist + advocate sign-off; refuse-and-reframe of advice-shaped contributions | Clinical/Advocate reviewer |
| Use of controlled-access or identifiable patient data | Low | Critical | Hard scope rule: aggregate/published only; no backend, no registry, no patient data; source register rejects record-level data; reviewer audit | Maintainer |
| Embedding NC/ND/incompatibly-licensed figures in CC-BY output | Medium | High | Source register CC-BY-compatibility verdict required before use; public-domain-first sourcing; redraw-or-cite-only rule; license check in CI; reviewer audit | Maintainer / Stats reviewer |
| Statistics go stale (new SEER/CDC/GLOBOCAN release) | High | Medium | `dataVintage` + `reviewBy` on every source; runtime/staleness flag; data-vintage review cadence with re-sign-off (M7) | Maintainer |
| No expert reviewer secured → content blocked | Medium | High | Dated recruitment (reviewers by 2026-08-31); recruit via epidemiology/biostat departments, oncology societies, advocacy orgs; **do not author HIGH-tier content without sign-off** (hard gate); hold at M1 | Maintainer |
| No delivery partner secured → cannot reach Definition of Shipped | High | High | Honest `TO BE SECURED` / `verifiedNeed:false`; dated partner plan (partner by 2026-10-31) + **build-vs-mothball/pivot rule** at ~2027-01-31 (donate to an OER host with measured reuse, or mothball) — never ship to no one | Steward / Maintainer |
| Course is accurate but ineffective (no misconception movement) | Medium | High | Misconception inventory drives objectives; pre/post instrument; **M5 kill-gate** dry-run before partner delivery; rework content if no movement | Maintainer / Stats reviewer |
| Source promotes a vendor/charity/program agenda over learner understanding | Low | Medium | Source-neutral editorial rule; refuse promotional framing; COI disclosure for reviewers and sources | Maintainer |
| Translation introduces statistical/clinical error | Medium | High | Per-language expert review of translations (treated as HIGH-tier for patient-facing content); translation-readiness keeps claims structured + cited | Stats/Clinical reviewer |
| Learner assessment data mishandled by a partner | Low | High | Reference implementation anonymous/aggregate/opt-in/deletable; partner uses their own consent/privacy terms; no PII in the repo | Steward / Maintainer |

---

## Security & privacy

**Threat surface.** This project's threat surface is unusually small **by construction**: no
backend, no accounts, no patient data, no registry. The principal risks are **content-integrity**
risks (a wrong statistic, an advice-shaped sentence, an incompatibly-licensed figure slipping into
CC-BY output) rather than classic security risks. Secondary surfaces: the build/CI supply chain
(dependencies for the static site and widgets) and the optional learner-assessment data collected by
a *partner*.

**Controls.**
- **Content integrity as the top control:** editorial rubric + expert sign-off gates +
  citation-coverage/license/staleness checks + accuracy-regression fixtures in CI; a wrong or
  unsourced claim fails the build or fails review.
- **No patient data by design:** aggregate/published statistics only; no record-level data ingested
  or stored; no registry; the source register rejects controlled-access data.
- **Minimal-data assessment:** the reference pre/post instrument is **anonymous, opt-in, aggregate,
  and deletable**; no names/identifiers; partners administer it under their own consent/privacy
  terms; nothing personal is committed to the repo.
- **No secrets/PII in logs or committed files** (Elyos rule); the static build needs no secrets at
  runtime.
- **Supply chain:** dependency + license scanning in CI; pin and review the small dependency set for
  the static generator and widgets.
- **Widgets are inert:** natural-frequency/base-rate widgets run client-side on static teaching
  numbers, compute no personal estimate, and transmit nothing.

**Abuse/misuse prevention.** The refused set — individualized advice, prognosis, a screening
recommendation, a personal-risk calculator, vendor/charity promotion, reuse of incompatible-licensed
material, or any use of identifiable patient data — is enforced by the editorial rubric and the
review gates, not merely documented. Contributions that drift into it are refused and reframed into
the in-scope teaching equivalent.

---

## Sustainability & maintenance

After delivery, a named **maintenance rotation** owns the courseware and tooling; the **steward**
owns the partner relationship and outcome tracking. The defining maintenance burden is **data
vintage**: cancer statistics are reissued regularly (e.g., annual SEER submissions, periodic
GLOBOCAN), so each source carries `dataVintage` + `reviewBy`, the staleness check flags figures past
their window, and a **review cadence** refreshes them with **re-sign-off** by the relevant expert —
stale statistics cannot silently keep serving as current. Outcomes (cohorts taught, misconception
reduction, third-party reuse/translations) are tracked as the success record — **not** page views.
Adding a new course, a cancer-type case study, or a translation follows a documented, expert-gated
process, only after the first courses are stable. The misconception inventory and accuracy-regression
fixtures are living artifacts, expanded as new common errors are observed in the wild.

---

## Open questions

- **Which delivery partner / audience first?** Patient-advocacy education arm vs. public-library/
  adult-education vs. journalism/health-reporting unit vs. OER host. Decided against the dated
  partner plan (≥ 3 in conversation by 2026-08-31; named partner by 2026-10-31). The choice shapes
  reading level, examples, and the assessment instrument.
- **GLOBOCAN / IARC reuse terms** — do they permit embedding derivative figures in a CC-BY work, or
  must we cite-only and redraw from public-domain US-gov data? (Resolve in the M1 source register.)
- **Scope of cancer examples at launch** — which 3–5 cancer types make the clearest worked examples
  (e.g., a screen-detected cancer with documented overdiagnosis like thyroid or prostate; a cancer
  with a real mortality-reducing screen; a rare cancer for small-number/CI lessons)? Confirm with the
  clinical + stats reviewers.
- **Assessment instrument validation depth** — adapt an existing validated risk-literacy instrument
  (e.g., a Berlin-Numeracy-style or screening-statistics-knowledge instrument, used per its license)
  vs. build and lightly validate a bespoke misconception inventory? Licensing of any borrowed
  instrument must be checked.
- **Translation prioritization** — which languages first, and how is per-language expert review
  resourced (volunteer vs. a future funded lane with a hard budget cap)?
- **Lane** — donated by default; is there a future funded lane for reviewer hours or translation,
  with a hard per-task budget cap, without compromising reviewer independence?

---

## References

- Proposal: `governance/proposals/oncology-data-literacy.md` *(TO BE WRITTEN — not yet drafted)*
- Roadmap entry: `planning/ROADMAP.md` → Track 8b, `oncology-data-literacy` (⚪ selected, med)
- Elyos work rules & refusal guardrails: `CLAUDE.md`
- Good-deed definition & risk tiers: `docs/good-deed-definition.md`
- Task JSON schema: `packages/schema/src/schemas.ts`
- House-style sibling plans: `planning/projects/public-official-guide/{PLAN,TASKS}.md`,
  `planning/projects/beacon-game/{PLAN,TASKS}.md`
- Sibling cancer projects to coordinate with: `stats-for-clinicians`,
  `patient-advocate-research-primer`, `incidence-explorers`, `cancer-dataset-datasheets`
- Candidate data sources (verify per source in the M1 register): NCI SEER / SEER\*Explorer, CDC US
  Cancer Statistics / WONDER, USPSTF, IARC Global Cancer Observatory (GLOBOCAN), Our World in Data
- Risk-communication literature (cite-only): Gigerenzer & Wegwarth on screening statistics; Welch on
  overdiagnosis; SEER/USPSTF statistical-communication guidance

---

## Appendix A — Improvements applied

The following **25 specific improvements** were identified during drafting and are **already applied
in the body above** (not deferred). Each is concrete to this project.

1. **Risk-tier split made explicit.** Rather than accept the roadmap's flat "medium," the plan
   separates **medium** statistical content from **HIGH** patient-facing survival/screening content,
   and ties each to the specific reviewer required — matching the binding cancer guardrail that
   patient-facing material needs clinical review. (*Exec summary, Quality gates.*)
2. **"No-statistic-without-a-source" promoted to a CI-enforced rule**, not a guideline — the
   citation-coverage check fails the build on any uncited statistic. (*Architecture, Quality gates,
   Metrics.*)
3. **Correct-endpoint rule encoded** (mortality, not 5-year survival, is the yardstick for
   early-detection/screening benefit) as a first-class editorial rule, because that exact confusion
   is the project's headline misconception. (*Architecture component 1, Survival/Screening
   milestones.*)
4. **Absolute-before-relative rule** and **natural-frequency framing** baked into the rubric, so the
   courses never present a bare relative risk or a conditional probability that invites the base-rate
   fallacy. (*Architecture, M4.*)
5. **Headline license gate written out** with a per-source table and the CC-BY-compatibility verdict,
   including the explicit **NC/ND incompatibility** and the **redraw-from-public-domain-or-cite-only**
   rule. (*Data, licensing & compliance.*)
6. **Public-domain-first sourcing decision** (prefer SEER/CDC/USPSTF/NCI US-gov public-domain data
   for any embedded figure) to keep the CC-BY output unencumbered. (*Key decisions.*)
7. **Data-vintage staleness fail-safe** (`dataVintage` + `reviewBy` + a staleness check + re-sign-off)
   added because cancer statistics are reissued annually — a real, recurring failure mode the
   exemplar's "staleness as fail-safe" pattern handles. (*Provenance model, Sustainability, Risks.*)
8. **No-patient-data-by-construction** stated as an architecture decision that *removes* the privacy
   threat surface rather than mitigating it, with controlled-access databases named and excluded.
   (*Exec summary, Scope, Security & privacy.*)
9. **Registry guardrail explicitly marked N/A** (no registry is built) so the boundary is stated, not
   assumed — directly addressing the binding registry guardrail. (*Scope, Data & compliance.*)
10. **Refuse-and-reframe rule** for advice-shaped or personal-risk-calculator contributions, mirroring
    the exemplar's "refuse + offer the lawful alternative" pattern, adapted to "refuse advice + offer
    the teaching equivalent." (*Scope, Architecture, Security.*)
11. **Shared-decision-making framing for screening** made a hard rule (the course teaches how to weigh
    evidence and prepare a clinician conversation; it never recommends for/against screening),
    enforced by oncologist + advocate review. (*Goals, M4, Risks.*)
12. **Dated partner-acquisition plan + build-vs-mothball/pivot decision rule** added (reviewers by
    2026-08-31, partner by 2026-10-31, pivot/mothball decision ~2027-01-31), replacing an open-ended
    `TBD` — adopted from the exemplar's honesty mechanism. (*Exec summary, Problem, Risks.*)
13. **Outcome-based success metrics** centered on **misconception reduction in real learners**, with
    page views/sign-ups/"modules published" explicitly named as *not* success. (*Success metrics.*)
14. **M5 kill-gate** (dry-run the instrument before partner delivery; rework if no misconception
    movement) so an accurate-but-ineffective course is caught before it reaches a cohort. (*Roadmap,
    Risks.*)
15. **Accuracy-regression fixtures** — a CI fixture set of "tricky" claims the courseware must get
    right — so edits cannot silently reintroduce a corrected error. (*Architecture, Security, M5.*)
16. **Version-scoped expert sign-off + name-use limits + COI/recusal + disagreement-veto fallback**
    governance, adapted from the exemplar so a single reviewer is not a silent single point of
    failure and reviewers aren't misrepresented. (*Governance.*)
17. **Three distinct reviewer roles named** (biostatistician/epidemiologist, oncologist, patient
    advocate) with which content each gates — not a vague "expert review." (*Governance, Quality
    gates.*)
18. **Sibling-project coordination** called out (`stats-for-clinicians`, `patient-advocate-research-
    primer`, `incidence-explorers`, `cancer-dataset-datasheets`) to avoid duplication and reuse
    provenance practice. (*Dependencies.*)
19. **Misconception inventory as the curriculum contract** — each learning objective names the
    specific error it corrects and the evidence it is common — so content is built to *cure named
    misconceptions*, and the assessment tests exactly those. (*Architecture, Curriculum, M5.*)
20. **Illustrative-only widget constraint** — natural-frequency/base-rate widgets run client-side on
    static teaching numbers, compute no personal estimate, transmit nothing — closing the "did you
    build a risk calculator?" misuse path. (*Scope, Architecture, Security.*)
21. **Portable/exportable formats** (HTML + print PDF + OER-package/Common-Cartridge/SCORM) so
    library/community-college/LMS partners can actually adopt it — adoption is a delivery requirement,
    not an afterthought. (*Architecture, Dependencies.*)
22. **Assessment-data privacy** specified (anonymous, opt-in, aggregate, deletable; administered under
    the partner's consent terms; nothing personal in the repo) even though the project itself stores
    no patient data. (*Privacy stance, Security.*)
23. **Pivot target made concrete** (donate to an OER host — OER Commons / a university health-comms
    program / a charity education hub — with measured *reuse* outcomes) so "pivot" is a real plan, not
    a hand-wave. (*Exec summary, Risks.*)
24. **Cancer-example selection turned into an open question with criteria** (a documented-overdiagnosis
    screen-detected cancer; a real mortality-reducing screen; a rare cancer for small-number/CI
    lessons) so examples are chosen for pedagogical power and reviewed. (*Open questions.*)
25. **Translation treated as HIGH-tier with per-language expert review**, since a mistranslated
    statistic in patient-facing content reintroduces clinical risk — translation-readiness keeps
    claims structured and cited to make that review tractable. (*Goals, M5, Risks, Backlog.*)

---

## Review sign-off

A completeness + correctness pass was run against the PLAN_SPEC 17-section structure, the Elyos
cancer guardrails, the good-deed definition, and the Task JSON schema. Findings and fixes:

- **Completeness:** all 17 required H2 sections are present and ordered per the spec; `Data,
  licensing & compliance` leads with the binding cancer guardrails as instructed. ✔
- **Cancer-guardrail coverage (re-verified):** open-access/aggregate/de-identified-only ✔;
  controlled-access + identifiable data out of scope ✔; per-source license verification ✔; no
  medical advice + "not medical advice" frame + oncologist/advocate review at riskTier high ✔;
  registry guardrail addressed (N/A, no registry built — stated explicitly) ✔; provenance on every
  assertion ✔.
- **Correctness fix applied:** the roadmap lists this project at flat "med," but patient-facing
  survival/screening content is escalated to **HIGH** per the guardrails — the plan states the split
  explicitly so the medium/high boundary is unambiguous and the right reviewer gates each milestone.
- **Honesty fix applied:** no partner/reviewers are secured, so `verifiedNeed:false` and `TO BE
  SECURED` are used throughout, backed by a *dated* acquisition plan and an explicit pivot/mothball
  rule — the project cannot "ship on merge."
- **License-gate correctness:** confirmed the output is CC-BY-4.0 and that NC/ND sources (e.g., some
  charity statistics) are **incompatible** for embedding; the redraw-or-cite-only rule and the source
  register's compatibility verdict enforce this. The GLOBOCAN reuse terms remain a flagged M1 item.
- **Schema alignment:** TASKS.md fields and the example Task JSON were checked field-by-field against
  `packages/schema/src/schemas.ts` (all `required` fields present; enum values valid;
  `verifiedNeed:false`; no `funded` tasks so no `fundedBudgetUsd` required).
- **Needs a human decision (surfaced, not hidden):** (1) secure the three expert reviewers (gates all
  content); (2) secure a delivery partner or commit to the OER-host pivot; (3) resolve GLOBOCAN/IARC
  reuse terms; (4) confirm the launch cancer examples and the assessment-instrument approach.

Status: **Draft ready for maintainer + governance review.** No blocking inconsistencies remain; the
open items above are decisions for humans, not gaps in the plan.
