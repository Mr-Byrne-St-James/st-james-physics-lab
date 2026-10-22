# quickCheck — style and production guide
Version 1.0 · 22 October 2026

## Brand and naming
- Always write **quickCheck**: lowercase q, uppercase C, no space. Never “Quick Check” or “QuickCheck” in UI or documentation.
- App page title: **[Unit] — quickCheck** (e.g. “Energy 1 — quickCheck”).
- Use the compact, navy-and-gold quickCheck wordmark with clipboard/checklist motif.
- Use the **St James Physics Lab** school logo separately at the top left as a working hyperlink to the [main app homepage](https://mr-byrne-st-james.github.io/st-james-physics-lab/).
- Keep the header compact on iPads; preserve a clear teacher-mode control at the right.
- Use a dark navy app background, accessible off-white text, sky-blue primary controls, green “secure” and amber “review” controls. Do not use the older red/yellow oversized quickCheck banner.
- Version number in document title, code comment and filename. Avoid multiple version entries in the home menu: use the site's highest-version filename convention (e.g. _v1.html, _v2.html); archive or supersede an earlier version in the same naming family.

## Student experience
1. Landing panel shows unit, brief self-assessment explanation, new-version action, reproducible seed code and **Start quickCheck**.
2. Present **one question at a time**; no answers visible until the learner clicks **Reveal model answer**.
3. The student checks their own response and selects **✓ I got this right** or **✗ I need to review this**. Never claim automatic marking.
4. A standard attempt has **20 questions**, with a curriculum-weighted blueprint that covers every taught lesson.
5. Results report self-assessed secure count out of 20 and group gaps by OneNote lesson and objective; allow review of flagged questions and another attempt.
6. Teacher mode exposes all bank questions by lesson, shows model answers, supports search and individual-question preview.
7. Include printable/PDF-friendly output where supported; printed model answers must be clearly identified.
8. Must run on an iPad and desktop without external JavaScript libraries; buttons should be large enough to tap.

## Question bank and AFL
- Initial topic-specific bank: **80 original questions**, expandable to 160; track ID, lesson, type, marks, question, answer and checklist objective.
- Prefer assessment-for-learning questions that students can use to diagnose an actionable gap. Do not merely reproduce specification wording.
- For introductory topics (e.g. Energy 1), emphasise recall, units, correct terms and simple calculations. Graphics are optional, not mandatory.
- Keep questions short, unambiguous and fully self-contained. Provide required values (e.g. g=10 N/kg) explicitly.
- **Mandatory model-answer formula layout:** For every calculation or formula question, the **first line** of the model answer must show the **full standard equation in its original form** (e.g. `P = E/t`), even when no rearrangement is needed. If rearrangement is required, put the **rearranged equation on the next line** (e.g. `E = Pt`), followed by substitution, the numerical answer and the correct unit on subsequent lines. Never begin with the rearranged formula or substituted numbers.
- Include useful units and working in calculation model answers. Check every numerical template and unit conversion.
- Vary question *selection* and selected *numbers*, not the underlying assessed skill. Never randomise into implausible data or accidental arithmetic traps.
- Seeded pseudo-randomness must be deterministic: entering/reusing the same seed yields the same question IDs and numerical variants.
- Use a **lesson blueprint** to prevent a random attempt missing entire lessons. As bank grows, monitor skill coverage as well as lesson coverage.
- Avoid repeat question IDs within a single standard attempt.
- Retain student ownership of self-assessment; the app must not pretend to verify a typed answer.

## OneNote integration
- Lesson numbers must match the current OneNote hierarchy and the unit's AfL checklists.
- Waves 1: lessons 01–07, pre-test 08, quickCheck 08.1.
- Energy 1: lessons 01–07, pre-test 08, quickCheck 08.1.
- Display lesson references on questions and in the review summary.

## File and release conventions
- Preferred file: `KS4_PHYSICS_[TOPIC]_[descriptive_name]_vN.html`.
- GitHub repository: `Mr-Byrne-St-James/st-james-physics-lab`; site root: `https://mr-byrne-st-james.github.io/st-james-physics-lab/`.
- Maintain only the latest version on the menu using the homepage's version selection; ensure earlier file naming conventions actually match its parser.
- Test: correct school hyperlink, layout at mobile/tablet widths, 20 unique selections, coverage by lesson, seeded repeatability, each answer-reveal/self-rating flow, results and flagged review, teacher mode, search, and print/PDF if offered.
- Never remove the question bank, model answers or existing student features during a cosmetic update.
