# Oncology-Data-Literacy — TASKS.md

> Status: Draft · Version: 0.1.0 · Last updated: 2026-06-28 · Owner: TBD (maintainer) · Lane: donated

Backlog for **Oncology-Data-Literacy** (slug: `oncology-data-literacy`): three short, open,
expert-reviewed courses that teach people to read cancer statistics correctly — **Reading Rates**,
**Reading Survival**, **Reading Screening Evidence**. See `PLAN.md` for full context.

**Binding cancer guardrails for every task:** open-access / **aggregate / de-identified** statistics
**only** (controlled-access and identifiable patient data are out of scope; no registry, no patient
data store); **per-source license verification** before any figure/datum is used; **no medical
advice** — patient-facing content is education-only, carries a persistent "not medical advice" frame,
and is **oncologist + patient-advocate reviewed (riskTier high)**; **provenance on every statistical
assertion**. The **editorial guardrail rubric is the first build item**. No partner, requestor, or
expert reviewer is yet secured, so delivery- and review-dependent tasks carry `requestor: TO BE
SECURED` and `verifiedNeed: false`.

## How these tasks map to Elyos

Each task below becomes an Elyos **Task JSON** validated against `packages/schema/src/schemas.ts`.
Field mapping:

- **id** — stable slug `oncology-data-literacy-<area>-NNN` (e.g. `oncology-data-literacy-editorial-001`).
- **title** — the task title in the milestone table.
- **project** — `oncology-data-literacy`.
- **type** — one of `code | research | writing | data | design-spec | maintenance`.
- **lane** — `donated` (default; no funded tasks planned. Any `funded` task must add
  `fundedBudgetUsd` with a hard cap).
- **priority** — `high | medium | low`.
- **domain** — array, e.g. `["cancer","statistics","education","health-literacy"]`.
- **riskTier** — `low | medium | high`. **Statistical content is `medium`**; **patient-facing
  survival/screening content is `high`** (per the cancer guardrails — oncologist + advocate sign-off);
  pure tooling/platform/a11y is `low`.
- **urgent** — boolean (no urgent tasks at cold-start).
- **deliverable** — `pr | dataset | document | translation`.
- **tokenEstimate** — `small | medium | large` (maps to the Size column).
- **status** — `open | in-progress | review | delivered | done` (all start `open`).
- **context / objective / acceptanceCriteria[] / resources[] / output** — per task.
- **requestor** — partner/steward/expert; `TO BE SECURED` where unknown.
- **verifiedNeed** — `true` only once a specific partner/need is confirmed; currently `false`
  everywhere (no partner/reviewer secured).
- **outputLicense** — content/datasets/docs: **`CC-BY-4.0`**; code/tooling: **`MIT`**.

Size legend: small ≈ tokenEstimate `small`, med ≈ `medium`, large ≈ `large`.
Reviewer shorthand: **Stats reviewer** = biostatistician / cancer epidemiologist (medium-tier stats
gate); **Clinical reviewer** = oncologist (HIGH-tier patient-facing); **Advocate reviewer** =
patient advocate (HIGH-tier patient-facing); **Maintainer** = engineering/editorial. All expert
reviewers are **TO BE SECURED**.

---

## Milestone M0 — Foundations, editorial guardrails & reviewer recruitment (cold-start)

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| oncology-data-literacy-editorial-001 | Editorial guardrail rubric (no-statistic-without-a-source, correct-endpoint, absolute-before-relative, no-medical-advice/no-recommendation, refuse-and-reframe) | design-spec | medium | medium | document | — | Stats reviewer + Maintainer |
| oncology-data-literacy-curriculum-002 | Curriculum map + learning objectives + named misconception inventory (3 courses) | design-spec | small | medium | document | 001 | Stats reviewer + Maintainer |
| oncology-data-literacy-licensing-003 | Source-licensing & provenance policy + register schema (CC-BY-compatibility verdicts, dataVintage) | data | small | medium | document | — | Maintainer |
| oncology-data-literacy-platform-004 | OER repo + static build + portable/LMS export + CI (lint, link-check, citation-coverage scaffold) | code | small | low | pr | — | Maintainer |
| oncology-data-literacy-reviewers-005 | Recruit + secure expert reviewers (biostatistician/epidemiologist, oncologist, patient advocate) | research | small | medium | document | — | Maintainer |
| oncology-data-literacy-pilot-006 | Pilot "reading a cancer headline" module (method proof; 1 worked example end-to-end) | writing | small | medium | document | 001, 002, 003 | Stats reviewer + Maintainer |

**Acceptance criteria — key tasks**

- **oncology-data-literacy-editorial-001** (editorial guardrail rubric)
  - Encodes, as checkable rules: **no statistical assertion without a cited source**; the
    **correct-endpoint** rule (mortality — not 5-year survival or incidence — is the yardstick for
    screening/early-detection benefit; observed vs relative/net survival distinguished);
    **absolute-before-relative** risk and **natural-frequency** framing required; the
    **no-medical-advice / no-recommendation** rule plus the persistent "Education only — not medical
    advice" frame on every module; the **uncertainty** rule (CIs, small-number instability, data
    vintage shown); and the **refuse-and-reframe** rule for advice-shaped or personal-risk-calculator
    requests.
  - Defines the **misconception-targeting method**: each learning objective must name the
    misconception it corrects and cite evidence it is a real, common error.
  - Specifies the riskTier split (statistical = medium → stats reviewer; patient-facing survival/
    screening = high → oncologist + advocate) and the per-content sign-off gate.
  - Reviewed and signed off by the statistical reviewer (recorded in the reviewers ledger).

- **oncology-data-literacy-licensing-003** (source-licensing & provenance register)
  - Defines the register entry shape: `{ name, publisher, table/figure id, dataVintage,
    retrievalDate, url, legalStatus, ccByCompatible, reviewBy }`.
  - States the **public-domain-first** sourcing rule and the **NC/ND-incompatible →
    redraw-from-public-domain-or-cite-only** rule for CC-BY output.
  - A figure/datum may not be used in courseware without a register entry whose `ccByCompatible`
    verdict is true (or an explicit cite-only marker).

- **oncology-data-literacy-platform-004** (OER repo + CI)
  - pnpm + TypeScript/ESM repo; static OER build; **portable exports** (HTML, print PDF, and an
    OER-package/Common-Cartridge or SCORM export for LMS partners).
  - CI runs lint, link-check, and the **citation-coverage scaffold** (fails on an uncited statistic);
    no secrets/PII in the repo; build green.

- **oncology-data-literacy-reviewers-005** (secure expert reviewers)
  - Secures (or documents the dated pipeline toward) a **biostatistician/epidemiologist**, an
    **oncologist**, and a **patient advocate**, with credentials + consent recorded and COI disclosed.
  - **Gate:** until the reviewers are secured, content authoring (M2+) does not start (PLAN decision
    rule); `verifiedNeed` stays `false` until confirmed.

**M0 Definition of Done:** editorial guardrail rubric (stats-reviewed) + curriculum map +
misconception inventory merged; source-licensing/provenance register schema + policy defined; OER
repo + static build + portable/LMS export + CI (lint, link-check, citation-coverage scaffold) green;
pilot "reading a cancer headline" module proves the method end-to-end; **expert reviewers secured (or
a dated pipeline recorded)** so content authoring can begin.

---

## Milestone M1 — Source vetting, provenance & teaching datasets

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| oncology-data-literacy-sources-007 | Vet + record each launch source's license + data vintage in the register (SEER/CDC/USPSTF/GLOBOCAN/OWID) | data | medium | medium | dataset | 003 | Stats reviewer + Maintainer |
| oncology-data-literacy-datasets-008 | Aggregate teaching datasets + data dictionaries (published rate/survival/screening tables, aggregate-only) | data | medium | medium | dataset | 007 | Stats reviewer + Maintainer |
| oncology-data-literacy-citations-009 | Citation/provenance tooling: citation-coverage + license-compatibility + staleness checks in CI | code | small | low | pr | 004, 007 | Maintainer |

**Acceptance criteria — key tasks**

- **oncology-data-literacy-sources-007** (source vetting)
  - Each launch source has a register entry with a **verified license/legal status**, **data
    vintage**, retrieval date, URL, and a **CC-BY-compatibility verdict**.
  - **Controlled-access / record-level data is rejected**; only aggregate, published statistics are
    admitted. **GLOBOCAN/IARC reuse terms resolved** (embed-derivative vs cite-only).
  - Any NC/ND source is marked cite-only (no embedding); public-domain US-gov sources preferred for
    embedded figures. Stats-reviewer audit recorded.

- **oncology-data-literacy-datasets-008** (aggregate teaching datasets)
  - Datasets are **aggregate-only** (no individual-level data), each with a data dictionary and a
    provenance/register link and data vintage.
  - Suitable for the worked examples named in the curriculum (e.g., crude vs age-standardized rate
    pairs; a relative-survival-by-stage table; a screening trial summary).

- **oncology-data-literacy-citations-009** (provenance tooling)
  - CI **fails** on any statistical assertion not keyed to a register entry; **fails** on any
    embedded source whose `ccByCompatible` is false; and **flags** any source past its `reviewBy`
    (staleness) for refresh + re-sign-off.

**M1 Definition of Done:** launch source set vetted + recorded with license verdicts and data
vintages (GLOBOCAN terms resolved); aggregate teaching datasets + dictionaries committed; citation
coverage + license compatibility + staleness checks live in CI and green on the pilot module.

---

## Milestone M2 — Course 1: Reading Rates (statistical, medium tier)

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| oncology-data-literacy-rates-010 | Course 1 content: incidence/mortality/prevalence, crude vs age-standardized, rates vs risk, absolute vs relative, CIs, reading trends | writing | large | medium | document | 002, 006, 008, 009 | Stats reviewer + Maintainer |
| oncology-data-literacy-rates-011 | Course 1 worked examples + exercises + self-check from aggregate data | writing | medium | medium | document | 010 | Stats reviewer + Maintainer |

**Acceptance criteria — key tasks**

- **oncology-data-literacy-rates-010** (Reading Rates content)
  - Covers: incidence vs mortality vs prevalence; **crude vs age-standardized** rates (why age
    structure matters; standard populations); **rates vs risk** (lifetime "1 in N" is a population,
    age-driven figure, not a personal probability); **absolute vs relative** risk (relative-risk
    headline inflation); **confidence intervals / small-number instability / suppression**; reading
    **trends** (changes in detection/coding vs real change; correlation ≠ causation).
  - Each learning objective is tied to a named misconception from the inventory; **every statistic is
    cited** (citation coverage 100%) with its data vintage; "not medical advice" frame present.
  - **Biostatistician/epidemiologist sign-off recorded** (version-scoped) before ship.

**M2 Definition of Done:** Reading Rates content + worked examples + exercises drafted entirely from
cited aggregate data; citation coverage 100% and license/staleness checks green; every objective maps
to a named misconception; **stats reviewer sign-off recorded**.

---

## Milestone M3 — Course 2: Reading Survival (patient-facing, HIGH tier)

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| oncology-data-literacy-survival-012 | Course 2 content: observed vs relative/net survival, survival≠mortality, lead-time/length-time bias, overdiagnosis, stage migration, KM/censoring basics | writing | large | high | document | 002, 006, 008, 009 | Stats reviewer + Clinical reviewer + Advocate reviewer |
| oncology-data-literacy-survival-013 | Course 2 worked examples + exercises + self-check (lead-time/overdiagnosis demonstrations from aggregate data) | writing | medium | high | document | 012 | Stats reviewer + Clinical reviewer + Advocate reviewer |

**Acceptance criteria — key tasks**

- **oncology-data-literacy-survival-012** (Reading Survival content)
  - Covers: **observed vs relative/net (cause-specific)** survival; **why 5-year survival ≠
    mortality**, and why rising survival can occur with **no mortality benefit**; **lead-time bias**;
    **length-time bias**; **overdiagnosis**; **stage migration / Will Rogers phenomenon**;
    median/conditional survival; Kaplan–Meier and **censoring** basics.
  - **HIGH-tier framing:** persistent "Education only — not medical advice"; presents no individual
    prognosis and no "what this means for you" answer; routes individual questions to the learner's
    clinician.
  - Each objective tied to a named misconception (esp. "survival↑ ⇒ early detection/treatment saves
    lives"); every statistic cited with data vintage.
  - **Biostatistician + oncologist + patient-advocate sign-off recorded** (version-scoped) before ship.

- **oncology-data-literacy-survival-013** (worked examples)
  - Demonstrates lead-time bias and overdiagnosis with concrete worked examples built from cited
    aggregate data; exercises let learners distinguish a real mortality benefit from a survival
    artifact.
  - Plain-language and dignity reviewed by the advocate reviewer (no fear-mongering, no false
    reassurance).

**M3 Definition of Done:** Reading Survival content + worked examples drafted; "not medical advice"
frame and no-individual-prognosis upheld; citation coverage 100% with data vintages;
**biostatistician + oncologist + patient-advocate sign-off recorded**.

---

## Milestone M4 — Course 3: Reading Screening Evidence (patient-facing, HIGH tier)

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| oncology-data-literacy-screening-014 | Course 3 content: correct endpoint (mortality), sens/spec/PPV via natural frequencies, NNS, false positives/overdiagnosis/overtreatment, RCT vs observational, shared-decision framing | writing | large | high | document | 002, 006, 008, 009, 012 | Stats reviewer + Clinical reviewer + Advocate reviewer |
| oncology-data-literacy-screening-015 | Course 3 worked examples + illustrative-only natural-frequency widget (static teaching numbers; no personal estimate) | code | medium | high | pr | 014 | Stats reviewer + Clinical reviewer + Maintainer |

**Acceptance criteria — key tasks**

- **oncology-data-literacy-screening-014** (Reading Screening content)
  - Covers: the **correct endpoint** (mortality reduction — not survival, incidence, or 5-year
    survival — is the test of screening benefit); **sensitivity/specificity/PPV/NPV** and **base-rate
    dependence** taught via **natural frequencies**; **number needed to screen/invite**; **false
    positives, overdiagnosis, overtreatment** as real harms; **RCT vs observational** evidence; and
    **shared-decision-making** framing.
  - **Hard no-recommendation rule:** the course teaches *how to weigh screening evidence and prepare a
    clinician conversation* and **never** tells an individual whether to be screened; `refuse-and-
    reframe` verified on "should I get screened / at what age" style prompts.
  - Persistent "Education only — not medical advice" frame; every statistic cited with data vintage.
  - **Biostatistician + oncologist + patient-advocate sign-off recorded** before ship.

- **oncology-data-literacy-screening-015** (worked examples + widget)
  - The natural-frequency widget runs **client-side on static teaching numbers**, computes **no
    personal risk estimate**, stores/transmits nothing, and is labeled illustrative/teaching-only.
  - Worked examples convert a "99% accurate test" into natural frequencies to expose the base-rate
    fallacy; stats + clinical sign-off recorded.

**M4 Definition of Done:** Reading Screening content + worked examples + illustrative-only widget
drafted; correct-endpoint and **no-recommendation/shared-decision** rules upheld and verified;
citation coverage 100% with data vintages; **biostatistician + oncologist + patient-advocate sign-off
recorded**.

---

## Milestone M5 — Assessment, accessibility, eval & translation-readiness

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| oncology-data-literacy-assessment-016 | Validated pre/post misconception instrument (items mapped to the inventory) | writing | medium | medium | document | 010, 012, 014 | Stats reviewer + Maintainer |
| oncology-data-literacy-eval-017 | Learning-outcome eval (misconception reduction) + accuracy-regression fixtures in CI | code | medium | medium | pr | 016 | Stats reviewer + Maintainer |
| oncology-data-literacy-a11y-018 | Accessibility (WCAG 2.2 AA) + plain-language pass + translation-readiness extraction | code | medium | low | pr | 010, 012, 014 | Maintainer + Advocate reviewer |

**Acceptance criteria — key tasks**

- **oncology-data-literacy-assessment-016** (misconception instrument)
  - Pre/post items map one-to-one to the misconception inventory (incl. the "survival↑ ⇒ screening
    saves lives" and base-rate items); either adapts a validated risk-literacy instrument (per its
    license) or builds + lightly validates a bespoke one.
  - Items reviewed by the stats reviewer for correctness; scoring + interpretation documented.

- **oncology-data-literacy-eval-017** (eval + accuracy regression)
  - Scores misconception reduction (pre→post) for a cohort; reports the per-item delta.
  - **Accuracy-regression fixtures**: a set of "tricky" claims the courseware must get right; CI
    fails if an edit reintroduces a known error.
  - **M5 kill-gate:** a dry-run of the instrument on a small test group must show movement on the
    core misconception items, or content is reworked before partner delivery.

**M5 Definition of Done:** validated pre/post instrument + eval + accuracy-regression fixtures green;
WCAG 2.2 AA + plain-language + translation-readiness done; the **kill-gate** (instrument shows
misconception movement on a dry-run) passes before partner delivery.

---

## Milestone M6 — Partner adoption & delivery (the deed)

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| oncology-data-literacy-partner-019 | Secure delivery partner + steward; final expert sign-off of all shipped courses; confirm license/provenance | research | medium | high | document | 011, 013, 015, 017, 018 | Steward + Stats + Clinical + Advocate reviewer |
| oncology-data-literacy-delivery-020 | Real-learner cohort completes a course; misconception reduction recorded (the closed loop) | maintenance | medium | high | document | 019 | Steward + Stats reviewer |

**Acceptance criteria — key tasks**

- **oncology-data-literacy-partner-019** (secure partner + final sign-off)
  - A real educator/advocacy org/library/OER host is secured as delivery partner; steward assigned;
    `verifiedNeed` flips to `true`.
  - **All** statistical content has recorded biostatistician sign-off; **all** patient-facing content
    has recorded oncologist + advocate sign-off; every statistic is sourced + provenance-tracked
    under a CC-BY-compatible license.
  - Driven by the **dated partner plan** (≥ 3 in conversation by 2026-08-31; partner by 2026-10-31).
    If no partner is secured by **~2027-01-31**, apply the **build-vs-mothball/pivot rule** (PLAN exec
    summary): donate the courseware to an OER host with **measured reuse** outcomes, or mothball to
    maintenance-only — recorded in governance — rather than ship to no one.

- **oncology-data-literacy-delivery-020** (closed loop — the deed)
  - A real learner cohort completes a course; the pre/post instrument shows a **measurable reduction
    in the targeted misconceptions**, recorded with the partner's attestation.
  - "Not medical advice" frame upheld throughout; outcomes recorded as the success object (not page
    views).

**M6 Definition of Done:** project-level **Definition of Shipped** met — a real cohort completes a
course and shows measurable misconception reduction (or the OER-host pivot with measured reuse), all
content expert-signed-off, every statistic sourced + provenance-tracked, "not medical advice" upheld.
*(Gated on a secured partner — TO BE SECURED.)*

---

## Milestone M7 — Sustain & maintain (post-delivery)

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| oncology-data-literacy-ops-021 | Maintenance rotation + data-vintage review cadence (refresh + re-sign-off) + outcomes record + contribution/expansion process | maintenance | small | medium | document | 020 | Maintainer + Stats reviewer |

**Acceptance criteria — oncology-data-literacy-ops-021**
- Named maintenance rotation; **data-vintage review cadence** refreshes statistics as new SEER/CDC/
  GLOBOCAN releases land, with **re-sign-off** by the relevant expert (staleness check enforces it).
- Outcomes record tracks cohorts taught, misconception reduction, and third-party reuse/translations
  (not DAU/page views).
- Documented, **expert-gated** process for adding a new course/cancer-type case study or a
  translation.

**M7 Definition of Done:** courseware sustainably maintained — statistics kept current with
re-sign-off, outcomes tracked, a rotation owning it, and an expert-gated expansion/contribution
process.

---

## Backlog / future

| ID | Title | Type | Size | Risk | Deliverable | Notes |
|---|---|---|---|---|---|---|
| oncology-data-literacy-i18n-022 | Community translations of the courses (per-language) | translation | large | high | translation | Each language **expert-reviewed** (mistranslated stat = clinical risk); HIGH-tier for patient-facing |
| oncology-data-literacy-cases-023 | Additional cancer-type worked-example case studies | writing | medium | high | document | Pick for pedagogy (overdiagnosed screen-detected cancer; real mortality-reducing screen; rare cancer for small-number/CI) |
| oncology-data-literacy-journalism-024 | Newsroom/health-reporter edition (deadline-friendly checklists) | writing | medium | medium | document | Upstream audience; reuses core content |
| oncology-data-literacy-educator-025 | Educator facilitation guide + slide deck + lesson plan | writing | medium | medium | document | Lowers adoption cost for libraries/colleges |
| oncology-data-literacy-hazard-026 | Hazard-ratio / forest-plot reading mini-module | writing | small | medium | document | Coordinate with `stats-for-clinicians` to avoid duplication |
| oncology-data-literacy-notebook-027 | Optional interactive notebook versions of worked examples (aggregate data) | code | medium | low | pr | Data-science learners; aggregate teaching data only |

---

## Example task JSON

Complete, schema-valid Task JSON for the first M0 task (`oncology-data-literacy-editorial-001`),
validated against `packages/schema/src/schemas.ts`:

```json
{
  "id": "oncology-data-literacy-editorial-001",
  "title": "Editorial guardrail rubric (no-statistic-without-a-source, correct-endpoint, absolute-before-relative, no-medical-advice/no-recommendation, refuse-and-reframe)",
  "project": "oncology-data-literacy",
  "type": "design-spec",
  "lane": "donated",
  "priority": "high",
  "domain": ["cancer", "statistics", "health-literacy", "education"],
  "riskTier": "medium",
  "urgent": false,
  "deliverable": "document",
  "tokenEstimate": "medium",
  "status": "open",
  "context": "Oncology-Data-Literacy publishes three short, open, expert-reviewed courses that teach people to read cancer statistics correctly (rates, survival, screening). The project's safety-critical core is statistical and clinical CORRECTNESS: a statistics-literacy course that is itself subtly wrong manufactures the very misconception it claims to cure, with the authority of an 'educational resource'. Per the binding Elyos cancer guardrails, only open-access/aggregate/de-identified statistics are used (no controlled-access or identifiable patient data; no registry; no patient data store), every assertion carries provenance, and patient-facing content is education-only with a 'not medical advice' frame and oncologist + patient-advocate review. This cold-start task writes the editorial guardrail rubric that every later module is authored and reviewed against, BEFORE any course content exists. No partner or expert reviewer is yet secured.",
  "objective": "Write the authoritative editorial guardrail rubric that all course content must implement and be tested against: the no-statistic-without-a-source rule, the correct-endpoint rule (mortality not 5-year survival for screening/early-detection benefit; observed vs relative/net survival), the absolute-before-relative and natural-frequency requirement, the no-medical-advice / no-recommendation rule and persistent 'Education only - not medical advice' frame, the uncertainty rule (confidence intervals, small-number instability, data vintage shown), the refuse-and-reframe rule for advice-shaped or personal-risk-calculator requests, the misconception-targeting method (each objective names the error it corrects and cites that it is common), and the riskTier split with the per-content expert sign-off gate.",
  "acceptanceCriteria": [
    "Encodes as checkable rules: no statistical assertion without a cited source (data vintage + provenance), the correct-endpoint rule (mortality - not 5-year survival or incidence - is the yardstick for screening/early-detection benefit; observed vs relative/net survival distinguished), absolute-before-relative risk with natural-frequency framing, and the uncertainty rule (CIs, small-number instability, data vintage shown)",
    "States the no-medical-advice / no-recommendation rule and the persistent 'Education only - not medical advice' frame required on every module, and the screening shared-decision-making (never for/against) constraint",
    "Defines the refuse-and-reframe rule for out-of-scope contributions (individualized advice, prognosis, screening recommendation, personal-risk calculator, vendor/charity promotion, controlled-access or identifiable patient data, NC/ND-incompatible figure embedding)",
    "Defines the misconception-targeting method: each learning objective names the specific misconception it corrects and cites evidence the error is real and common",
    "Specifies the riskTier split (statistical content = medium -> biostatistician/epidemiologist; patient-facing survival/screening = high -> oncologist + patient-advocate) and the per-content sign-off gate before ship",
    "Reviewed and signed off by the statistical (biostatistician/epidemiologist) reviewer and recorded, version-scoped, in the reviewers ledger"
  ],
  "resources": [
    "planning/projects/oncology-data-literacy/PLAN.md",
    "CLAUDE.md",
    "docs/good-deed-definition.md",
    "packages/schema/src/schemas.ts",
    "planning/ROADMAP.md"
  ],
  "output": "A reviewed editorial-guardrail rubric document (the project's correctness + no-medical-advice charter) defining the no-statistic-without-a-source, correct-endpoint, absolute-before-relative/natural-frequency, no-medical-advice/no-recommendation, uncertainty, and refuse-and-reframe rules, the misconception-targeting method, and the riskTier/sign-off gates - the contract that the curriculum (oncology-data-literacy-curriculum-002), the provenance tooling (oncology-data-literacy-citations-009), and every course content task implement and are reviewed against.",
  "requestor": "TO BE SECURED",
  "verifiedNeed": false,
  "outputLicense": "CC-BY-4.0"
}
```
