# Competitive & Improvement Analysis — `oncology-data-literacy`

> Analyst pass against PLAN.md v0.1.0 (2026-06-28). Web-researched competitive landscape.
> Scope: short, open OER courses teaching correct reading of cancer statistics (rates, survival,
> screening) for patients, advocates, journalists, students. Medium-tier overall, HIGH-tier on
> patient-facing survival/screening content.

---

## 1. Correctness & completeness review of PLAN.md

The plan is unusually strong: it correctly identifies its own failure mode (a stats-literacy course
that is itself wrong "manufactures the misconception it claims to cure") and makes correctness a
release gate, not a review nicety. The statistical-concept coverage is accurate and canon-aligned.
Specific findings:

**Statistical concepts — accurate and well-chosen.**
- The **correct-endpoint rule** (mortality, not 5-year survival, is the yardstick for early-
  detection/screening benefit) is the single most important idea in this field and the plan makes
  it a first-class editorial rule (Architecture component 1, M3, M4). This matches Welch's canonical
  result that *survival always rises with early detection even if no one is helped* — correct.
- **Lead-time bias, length-time bias, overdiagnosis, stage migration (Will Rogers)** are all named
  in M3 and correctly distinguished. Good: many lay treatments conflate lead-time and overdiagnosis;
  the plan keeps them separate.
- **Base-rate fallacy / sensitivity vs PPV via natural frequencies** (M4) is exactly the Gigerenzer
  prescription (the mammography "9 of 10 positives have cancer" error). Correct and the right
  pedagogy (natural frequencies over conditional probabilities).
- **Absolute-before-relative** and **crude vs age-standardized**, **rates vs risk**, **lifetime risk
  ≠ personal probability**, **CIs / small-number instability** (M2) — all correct and complete for a
  foundational rates course.

**Two most important correctness findings (gaps/risks):**
1. **"Net/relative survival" needs a sharper internal definition or it will trip the course itself.**
   The plan lists "observed vs relative/net survival" (M3) but does not flag that *relative survival*
   is itself a frequently-misread construct (it is a ratio to an age/sex-matched general population,
   not a probability of not dying of cancer, and can exceed expectations or behave oddly with
   competing risks and at long horizons). This is precisely the kind of second-order subtlety where a
   stats-literacy course most easily becomes subtly wrong. Recommend an explicit editorial sub-rule +
   a biostatistician-authored canonical definition fixture in the accuracy-regression set.
2. **The "is the statistic itself misleading?" framing needs nuance the plan does not yet carry.**
   The Beral/Peto vs Crouch BMJ debate ("UK cancer survival statistics are misleading": simulation
   study, BMJ 2011) shows that *survival* can be misleading for cross-country/temporal comparison yet
   *not* an artifact in the way naive critics claim. The course must teach "survival is the wrong
   endpoint for screening benefit" **without** sliding into "survival statistics are fake/useless"
   (an over-correction that is itself a misconception). This boundary is not currently called out and
   should be an explicit editorial guard + a worked example.

**Audience targeting.** Strong and explicitly multi-audience (patients/families, advocates,
journalists, students, educators/librarians), with journalists correctly identified as the
high-leverage *upstream* audience. Minor risk: one reading level cannot serve a newly-diagnosed
patient and a journalism student equally; the plan acknowledges reading-level tension in Open
Questions but does not yet commit to audience-segmented tracks. Recommend explicit
patient-track vs practitioner-track variants of the same module sharing one citation base.

**Sourcing.** Excellent and conservative: public-domain-first (SEER, CDC, USPSTF, NCI), explicit
CC-BY compatibility gate, NC/ND exclusion, redraw-or-cite-only rule, per-source register with data
vintage + reviewBy + staleness check. This is best-in-class for an OER and directly addresses the
single biggest legal trap (see §2: the closest canonical resource, *Know Your Chances*, is CC-BY-
**NC-ND** and therefore non-embeddable — the plan's instinct is correct).

**Not-advice boundary.** Well-handled: persistent "education only — not medical advice" frame,
explicit no-for/against-screening rule, refuse-and-reframe rule, shared-decision-making framing,
oncologist + advocate sign-off on HIGH-tier content. This is more rigorous than most real-world
competitors (most blogs carry a one-line disclaimer at best).

**Assessment of learning.** Strong: validated pre/post misconception instrument, M5 kill-gate (no
movement → rework before delivery), accuracy-regression fixtures. This is a genuine differentiator —
almost no competitor *measures* misconception reduction. One gap: the plan should specify it will
test for **iatrogenic learning** (did the course accidentally teach a new wrong belief, e.g.
"screening is bad") not just net items-correct.

**Accessibility.** WCAG 2.2 AA + plain-language + translation-readiness with per-language expert
review — comprehensive and ahead of competitors.

**Avoiding being itself misleading.** This is the plan's central organizing principle and it is
handled better than any competitor reviewed. The residual risks are the two second-order ones above
(relative-survival definition; survival-isn't-fake over-correction), plus the generic risk that
worked examples drift out of date (mitigated by the staleness/reviewBy machinery).

**Completeness verdict:** No blocking gaps. Add (a) a relative/net-survival canonical-definition
rule + fixture, (b) an explicit "don't over-correct survival into worthless" guard, (c)
iatrogenic-misconception checking in the eval, (d) audience-segmented reading tracks.

---

## 2. Competitive landscape

This space is rich but **fragmented**: the authoritative material is either (a) clinician/academic-
facing, (b) not cancer-specific, (c) not openly licensed for derivative reuse, or (d) a reference
artifact (fact box, blog, book) rather than a *taught, assessed course*. No incumbent occupies the
exact "open + cancer-specific + plain-language + assessed course" niche.

**Tier 1 — the canonical risk-literacy authorities (concepts/method).**

- **Harding Center for Risk Literacy (Gigerenzer / Wegwarth / McDowell).** The gold standard for
  *method*: fact boxes for breast, prostate, colon, ovarian cancer screening; natural-frequency
  pedagogy; the mammography PPV result. Strength: rigorous, peer-reviewed, clinician-validated
  formats (McDowell et al., *Med Decis Making* 2019, RCT on fact-box formats). Weakness for our
  purposes: it is a *reference tool* (fact boxes + papers), German/EU-centric, not a sequenced
  taught-and-assessed course, and reuse licensing is bespoke (cite-don't-embed). https://www.hardingcenter.de/en
  · fact boxes: https://www.harding-center.mpg.de/en/fact-boxes · format RCT: https://journals.sagepub.com/doi/10.1177/0272989X18818166
- **Winton Centre for Risk and Evidence Communication (Cambridge; Spiegelhalter).** Best-in-class on
  *how to communicate numbers fairly* (icon arrays, Predict breast/prostate tools, NHS shared-
  decision tools), endowed by the same Harding Foundation. Strength: research-grade, NHS-deployed,
  trusted. Weakness: tools and research outputs, not an open self-serve patient course on *reading*
  cancer stats; cancer content is treatment-decision tools (Predict), not statistics literacy.
  https://wintoncentre.maths.cam.ac.uk/ · resources: https://wintoncentre.maths.cam.ac.uk/resources/
- **H. Gilbert Welch / Woloshin / Schwartz canon.** The intellectual core of this entire project.
  *Know Your Chances: Understanding Health Statistics* (Woloshin, Schwartz, Welch; UC Press 2008) is
  the closest single existing artifact — and it is **free to read on NCBI Bookshelf but licensed
  CC-BY-NC-ND 3.0**, i.e. *non-commercial, no-derivatives* → **cannot be embedded or adapted into a
  CC-BY course**; teach-the-concept/cite-only only. This is both the strongest validation of the
  project's thesis and a concrete licensing constraint. https://www.ncbi.nlm.nih.gov/books/NBK115435/
  Welch's overdiagnosis/lead-time work (e.g. NEJM 2016 breast tumor-size study
  https://www.nejm.org/doi/full/10.1056/NEJMoa1600249) is copyrighted, cite-only.

**Tier 2 — adjacent literacy/evidence resources.**

- **theNNT.com (NNT Group).** Color-coded NNT/NNH summaries for interventions incl. some cancer
  screening; intuitive absolute-benefit framing. Strength: makes baseline-risk-aware benefit
  tangible. Weakness: clinician-oriented, not a teaching course, not cancer-focused, site blocks
  automated reuse; concept overlaps our "number needed to screen." (CEBM NNT explainer:
  https://www.cebm.ox.ac.uk/resources/ebm-tools/number-needed-to-treat-nnt)
- **Testing Treatments interactive (testingtreatments.org).** Free, plain-language explainers of
  lead-time bias and overdiagnosis bias — directly overlapping content, well-written. Strength: open,
  accessible, exactly on-topic conceptually. Weakness: general (not cancer-data-specific), not a
  sequenced assessed course, no real-cancer worked examples. https://en.testingtreatments.org/lead-time-bias/
  · https://en.testingtreatments.org/overdiagnosis-bias/
- **Our World in Data — Cancer.** The one major **CC-BY** cancer-statistics source (charts on
  incidence/mortality, age-standardized rates). Strength: openly licensed, embeddable, high quality —
  a *source/ally*, not a competitor. Weakness: presents data, does not teach how to read it or warn
  about biases. https://ourworldindata.org/cancer
- **Cancer Research UK.** Excellent plain-language explainers (e.g. "Absolute vs relative risk —
  making sense of media stories," 2013; statistics hub) and a science blog. Strength: trusted,
  readable, on-topic. Weakness: charity statistics are typically **CC-BY-NC-SA/bespoke → NC,
  non-embeddable** in CC-BY output (the plan flags this correctly); not a course; UK-centric.
  https://news.cancerresearchuk.org/2013/03/15/absolute-versus-relative-risk-making-sense-of-media-stories/
  · https://www.cancerresearchuk.org/health-professional/cancer-statistics-for-the-uk

**Tier 3 — generic stats education & journalism guides.**

- **Khan Academy — Statistics & Probability.** Free, huge reach, strong on mechanics. Weakness: zero
  cancer/medical-risk specificity, nothing on lead-time/overdiagnosis/screening. https://www.khanacademy.org/math/statistics-probability
- **Sense About Science — "Making Sense of Statistics."** Free PDF guide for journalists/public.
  Strength: plain-language, trusted, audience-matched (journalists). Weakness: general statistics,
  not cancer-specific, a guide not a course. https://senseaboutscience.org/activities/making-sense-of-statistics/
  (PDF: https://senseaboutscience.org/wp-content/uploads/2016/11/Makingsenseofstatistics.pdf)
- **Health journalism guides (HealthNewsReview legacy, USC Center for Health Journalism, Poynter,
  GIJN).** Strong on absolute-vs-relative-risk and mismatched framing for reporters. Strength:
  audience-matched, practical. Weakness: HealthNewsReview is no longer actively publishing; guides
  are not cancer-specific courses. https://www.healthnewsreview.org/toolkit/tips-for-understanding-studies/absolute-vs-relative-risk/
  · https://centerforhealthjournalism.org/our-work/insights/reporting-findings-absolute-vs-relative-risk
- **OER hosts (OERC/MERLOT cancer community, OER Commons).** Distribution channels / pivot targets,
  not competitors. https://oerc.merlot.org/

**Landscape verdict:** The authority exists (Harding, Winton, Welch/Woloshin/Schwartz) but is
locked in non-derivative licenses, clinician framing, or reference (not course) form. The open,
general material (Khan, Sense About Science, OWID) lacks cancer specificity and bias-aware framing.
**No one ships an open, CC-BY, cancer-specific, plain-language, assessed course that targets the
named misconceptions with real aggregate cancer data.** That is the seam.

---

## 3. Gaps we can fill

1. **Open + cancer-specific + derivative-licensed.** The best material (*Know Your Chances*, CRUK,
   Harding figures) is NC/ND or bespoke — *unforkable*. A genuinely CC-BY-4.0 course built on
   public-domain SEER/CDC/USPSTF data is rare-to-nonexistent and is reusable/translatable by anyone.
2. **Taught + sequenced + assessed, not a reference.** Fact boxes, blog posts, and a book exist; a
   structured course with learning objectives mapped to named misconceptions *and a validated pre/post
   instrument that proves misconception reduction* does not exist for cancer stats.
3. **Misconception-first design with real cancer worked examples.** Competitors teach concepts
   abstractly (Khan) or via single examples (Harding mammography). A misconception inventory driving
   every objective, each cured by a worked example from real aggregate cancer data, is a gap.
4. **Survival-specific literacy for patients.** The survival-statistics traps (5-yr survival, lead/
   length-time, Will Rogers, relative vs observed survival) are the highest-misconception area and the
   thinnest in *open patient-facing* material — most coverage is academic or clinician-facing.
5. **Multi-audience plain-language + accessibility + translation-ready.** WCAG 2.2 AA + readability-
   scored + i18n-structured cancer-stats literacy with per-language expert review is unserved.
6. **A reusable provenance/citation discipline as an artifact.** "No statistic without a sourced,
   vintaged, license-verdicted citation, enforced in CI" is itself a transferable public good no
   competitor publishes as reusable tooling.

---

## 4. Differentiators to win

- **Correctness as a CI-enforced release gate** (citation-coverage build-fail + accuracy-regression
  fixtures + tri-expert sign-off) — competitors rely on author authority; we *prove* it and prevent
  regressions.
- **Provably effective, not just published** — validated pre/post misconception instrument + M5
  kill-gate; the success object is *corrected understanding in real learners*, which no incumbent
  measures.
- **Truly open (CC-BY-4.0) and forkable/translatable** where the authorities are NC/ND-locked — the
  one thing the Welch/Harding/CRUK canon *cannot* offer.
- **Cancer-specific with real public-domain data worked examples** vs. generic stats (Khan) or
  single-topic fact boxes (Harding).
- **Misconception-inventory-as-curriculum-contract** — built to cure named, evidenced errors and
  assessed against exactly those.
- **Rigorous not-advice / shared-decision framing with oncologist + advocate veto** — safer than any
  blog/guide competitor.
- **Single strongest differentiator:** an **open, forkable, cancer-specific course whose
  effectiveness at reducing named misconceptions is measured and gated** — uniting open license +
  cancer specificity + proven learning outcome, none of which any single incumbent combines.

---

## 5. Claude API leverage (and the hard limits)

**Where Claude is high-leverage (human-verified):**
- **Draft lessons, worked examples, and "why the headline is wrong" callouts** from a curated set of
  authoritative public-domain inputs (SEER tables, USPSTF evidence) — Claude is excellent at turning
  a sourced statistic into a plain-language explanation and a natural-frequency reframing.
- **Generate quiz/assessment items mapped to the misconception inventory** — distractors that encode
  the *specific* wrong belief (e.g. "survival↑ ⇒ screening works"), then expert-validated. Strong fit
  for building the pre/post instrument's item bank.
- **Plain-language / readability passes and audience-retargeting** (same sourced content rewritten
  for a newly-diagnosed patient vs. a journalist) at a target reading level — high-volume, low-risk
  rewriting where the underlying claims are already locked and cited.
- Supporting: i18n string extraction + first-pass translation drafts (then per-language expert
  review), accessibility alt-text drafting, generating accuracy-regression "tricky claim" fixtures
  for review, and refuse-and-reframe exemplars for the editorial rubric.

**Where Claude must NOT decide (hard boundaries, enforced by gates):**
- **Statistical/clinical accuracy is verified by the biostatistician/oncologist, never by the model.**
  An LLM can fluently state a subtly-wrong survival/relative-survival claim — the exact failure this
  project must prevent. Claude drafts; experts adjudicate truth.
- **No fabricated or unsourced statistics, ever.** Every number must trace to a register entry;
  Claude may *format/explain* a sourced statistic but may not *supply* one from memory (hallucinated
  vintages/values are a critical risk). The citation-coverage CI check is the backstop.
- **No medical advice, prognosis, or for/against-screening recommendation** — Claude must not author
  anything that reads as individualized advice; refuse-and-reframe is enforced editorially, not left
  to model discretion.
- **No final sign-off, no shipping decision** — model output is always a draft entering the expert/
  CI/maintainer gate, never the gate itself.

---

## 6. Ten concrete optimizations

1. **Add a canonical relative/net-survival definition rule + accuracy-regression fixture** (the
   highest second-order trip-hazard; see §1 finding 1).
2. **Add an explicit "don't over-correct" editorial guard + worked example** so the course teaches
   "survival is the wrong *screening* endpoint" without implying "survival statistics are fake"
   (the BMJ "misleading?" debate boundary; §1 finding 2).
3. **Test for iatrogenic misconceptions in the eval**, not just net items-correct (did learners pick
   up a *new* wrong belief, e.g. "screening is harmful"?). Add such items to the pre/post instrument.
4. **License-map the canon up front:** record that *Know Your Chances* (CC-BY-NC-ND) and CRUK/Harding
   figures are cite-only/non-embeddable, and pre-plan public-domain redraws (SEER/CDC) for each
   concept that needs a figure — turns the §2 licensing trap into a checklist.
5. **Ship native fact-box / icon-array templates** (the Harding/Winton evidence-based formats) as
   reusable CC-BY components — adopt the *format* the literature shows works, not just prose.
6. **Audience-segmented reading tracks** (patient vs. journalist/student) sharing one citation base,
   resolving the reading-level tension the plan flags only as an open question.
7. **Co-develop the instrument with an existing validated base** (e.g. Berlin Numeracy / screening-
   statistics-knowledge scales, licensing checked) rather than fully bespoke — faster validation,
   comparability; the plan lists this as open, make it a decision with a default.
8. **Publish a "10 cancer-stat traps for journalists" quick-reference** as an upstream, high-reach,
   low-cost lead artifact (matches the Sense About Science / health-journalism-guide niche but
   cancer-specific and CC-BY) to seed adoption while the full courses are in expert review.
9. **Build a small "headline → correct reading" corpus** of real (de-identified, cited) cancer
   headlines as recurring worked examples and as living accuracy-regression material.
10. **Engineer a per-statistic "provenance card" UI** (value + vintage + source + license verdict +
    reviewBy) rendered inline — makes the no-statistic-without-a-source rule visible to learners and
    doubles as a trust/teaching device and the staleness surface.

---

## 7. Parallel & perpendicular spin-offs

- **Reusable risk-literacy course engine (perpendicular, high value).** The editorial rubric +
  source/provenance register + citation-coverage CI + misconception-inventory + pre/post-instrument
  harness is *domain-general*. Extract it as a **risk-literacy course engine** usable for vaccines,
  cardiovascular risk, nutrition-epidemiology headlines — Elyos's reusable OER substrate.
- **MCP server: "cancer-stat-provenance / fact-box server."** An MCP server exposing the vetted
  source register + the natural-frequency/fact-box transforms (input: a sourced aggregate statistic →
  output: natural-frequency reframing, icon-array spec, absolute-vs-relative pairing, citation card),
  with hard refuse-and-reframe on advice-shaped requests. Lets any Elyos agent (or external tool)
  reuse the verified provenance + correct-format machinery without re-implementing the guardrails.
- **`incidence-explorers` (parallel).** SEER/GLOBOCAN dashboards — natural *data/example source* for
  Reading Rates; share the source register and the crude-vs-age-standardized teaching.
- **`screening-coverage-trends` (parallel).** Screening-uptake data; feeds Reading Screening Evidence
  worked examples and the number-needed-to-screen lessons.
- **`stats-for-clinicians` (parallel sibling).** Shares the survival/hazard-ratio *math* but a
  clinician audience and framing — share fixtures and the accuracy-regression set, differ in reading
  level and the not-advice boundary.
- **`media-literacy-curriculum` (perpendicular).** The "headline → correct reading" corpus and the
  journalist quick-reference (#8) plug directly into a broader media-literacy module.
- **`patient-advocate-research-primer` (parallel, natural downstream partner).** Advocates who relay
  research are both an audience and a delivery channel; co-design the advocate track and the
  instrument.
- **`cancer-dataset-datasheets` (parallel).** Mirror its provenance/datasheet discipline; the source
  register and datasheet practice are the same muscle.

---

## 8. Open questions

1. **Relative/net-survival treatment depth** — how far to go on competing risks and long-horizon
   relative-survival oddities for a *patient* audience without becoming the thing it warns against?
   (Needs biostatistician decision.)
2. **Assessment instrument:** adapt a validated risk-literacy scale (license-checked) vs. bespoke
   misconception inventory — and how to validate within a donated-lane budget? (Plan flags; needs a
   default + decision.)
3. **GLOBOCAN/IARC reuse terms** — embeddable derivative figures vs. cite-only + public-domain
   redraw? (M1 register; unresolved.)
4. **Audience-segmentation cost** — does shipping patient *and* journalist tracks per module fit the
   donated-lane effort, or pick one launch audience first?
5. **Which 3–5 cancer examples** maximize pedagogical clarity (a documented-overdiagnosis screen-
   detected cancer e.g. thyroid/prostate; a real mortality-reducing screen; a rare cancer for small-
   number/CI lessons)? (Needs clinical + stats reviewer confirmation.)
6. **Fact-box/icon-array format adoption** — license-clean reimplementation of the Harding/Winton
   evidence-based formats vs. our own; any IP/attribution constraints on the *format*?
7. **Reusable-engine extraction timing** — generalize the rubric/register/eval into a shared engine
   now (more upfront cost, multi-project payoff) or after the first course ships?
8. **Standing reviewer capacity** — the tri-expert gate + per-version re-sign-off + per-language
   translation review is the true throughput constraint; is a future funded lane (hard budget cap)
   needed for reviewer/translation hours without compromising independence?

---

## Summary (for the requester)

**Top 3 competitors.** (1) **Harding Center for Risk Literacy** (Gigerenzer/Wegwarth) — gold-standard
cancer-screening fact boxes and natural-frequency method, but a reference tool, EU-centric, and not
openly forkable. (2) **Welch / Woloshin / Schwartz canon**, esp. *Know Your Chances* — the
intellectual core and closest single artifact, but it is CC-BY-**NC-ND** (free to read, *not*
adaptable/embeddable) and book-not-course. (3) **Winton Centre (Cambridge)** — best-in-class fair-
numbers communication and NHS tools, but research/tools, not an open assessed course on *reading*
cancer stats. Adjacent: Cancer Research UK (NC-licensed, UK-centric), Khan Academy (no cancer
specificity), Sense About Science / health-journalism guides (general), Our World in Data (a CC-BY
data *ally*, not a competitor).

**Single strongest differentiator.** An **open (CC-BY-4.0), forkable, cancer-specific course whose
effectiveness at reducing *named* misconceptions is measured and CI-gated** — uniting open license +
cancer specificity + proven learning outcome, a combination no incumbent offers (the authorities are
license-locked or reference-only; the open material isn't cancer-specific).

**Top 3 Claude-API ideas.** (1) Draft plain-language lessons and "why the headline is wrong" worked
examples *from curated sourced statistics* (expert-verified). (2) Generate misconception-mapped
quiz/instrument items with distractors encoding the specific wrong belief. (3) Plain-language/
readability and audience-retargeting rewrites (patient vs. journalist) over already-cited content.
Hard limits: Claude never supplies/validates a statistic from memory, never adjudicates statistical/
clinical accuracy, never authors advice or a screening recommendation, and never signs off.

**Two most important plan-correctness findings.** (1) **Relative/net survival** needs an explicit
canonical-definition rule + accuracy-regression fixture — it is the most likely place the course
itself becomes subtly wrong (it is a population-ratio, not "chance of not dying of cancer," and
misbehaves with competing risks / long horizons). (2) The course must teach "survival is the wrong
endpoint for *screening* benefit" **without over-correcting into "survival statistics are fake"** —
the BMJ "are UK survival statistics misleading?" boundary — which the plan does not yet guard
explicitly. Both are cheap to fix and central to the project's safety-critical core. Also flagged:
test for *iatrogenic* misconceptions in the eval, and license-map the NC/ND canon (Know Your
Chances, CRUK figures) to public-domain redraws up front.
