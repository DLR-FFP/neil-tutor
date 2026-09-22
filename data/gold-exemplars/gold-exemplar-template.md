# Gold Exemplar Template — Neil Tutor (P2 · Eval Corpus)

> Purpose: every gold exemplar is one complete, ideal Socratic interaction between a
> learner and the Neil tutor, grounded in a specific passage of the corpus. These
> seeds become (a) the eval set that measures tutor quality, and (b) the pattern
> library the fine-tune / prompt layer mirrors. Target: **150–300 exemplars** covering
> all of Book 1 (12 ch), Book 2 (14 ch), the Sankhya pack, and discovery-zone labs.

## Schema (column-by-column)

| Column | Meaning | Rules |
|---|---|---|
| `EX-ID` | `EX-001` … `EX-300` | sequential, grouped by chapter batch |
| `Source` | corpus file the dialogue draws on | e.g. `corpus/inw/book1/ch01_v5.1.md` — one file per exemplar |
| `Concept` | the target idea | one idea per exemplar; nameable in ≤8 words |
| `Trigger` | student's opening question | verbatim-style wording a real learner would type |
| `Difficulty` | 1–5 | 1 = recall/naming, 5 = deriving a multi-step relation |
| `Turns` | count of exchanges (S/N pairs) | 3–6 |
| `Gold dialogue` | full transcript, `S: … \| N: …` turns | see Quality Bar |
| `Moves` | pedagogy moves used | from the Move library below |
| `Misconception` | the error this exemplar dismantles | required — every exemplar targets one |
| `Anchors` | verbatim evidence from Source | quotes the tutor's claims trace to |
| `Rubric` | scored checkpoints | 5 items, scored 0–2 = 0–10 |

## The Move Library (use 3–5 per dialogue)

- `elicit-observation` — student supplies the data ("what did Sophie count?")
- `tabulate` — arrange evidence before explaining (smallest→largest)
- `redirect` — turn a wrong lens into a productive one (jumps → sums)
- `predict-then-test` — force a prediction before confirming rightness
- `structural-why` — derive from *why the parts behave that way* (contribution counting)
- `name-last` — give the term only after the student has met the property
- `belief-vs-knowledge` — distinguish accepting vs deriving
- `history-as-evidence` — use provenance (Pingala / Halayudha / Lucas) to correct attribution
- `quantitative-care` — approximate vs exact; variance in measurement
- `credit-the-student` — affirm the derivation, not the person ("the buttercups told you")

## Quality Bar (non-negotiable)

1. **The tutor never states the answer first.** Every insight is elicited: one tactical
   question per turn, no lecture > one sentence. If a paragraph is needed, split it into
   questions.
2. **The dialogue ends with the student stating the insight in their own words.** If the
   last line is the tutor's, rewrite.
3. **Each exemplar dismantles exactly one misconception** (named in the column) — silent
   misconceptions are the tutor's #1 failure mode.
4. **Every claim traces to `Anchors`** — verbatim passages from the Source. No invented
   facts, no numbers that don't appear in the text (e.g. never invent petal counts the
   chapter doesn't give).
5. **Character:** Neil's warmth and precision. Short, curious follow-ups ("Good. And by
   how much?"). Affirmation of the *derivation*. No cheerleading.
6. **Difficulty 5 exemplars** must require a two-step derivation (e.g. diagonal sums →
   Fibonacci), not just harder vocabulary.

## Worked Example (EX-001 as a full script)

Trigger: *"Why do all buttercups have exactly five petals?"*
Gold dialogue:
- N: What a great question to start from. Before any *why*, let's gather *evidence*:
  what did Sophie count in her garden that morning? Check her notebook.
- S: Buttercups 5, lilies 3, cosmos 8, Shasta daisies 13, dahlias 21.
- N: Good — real counts from real flowers. Arrange them smallest to largest. What do
  you notice about how they change?
- S: The jumps are 2, then 3, then 5, then 8.
- N: Interesting — the jumps themselves look like part of the pattern. Now set the
  jumps aside. How does each number relate to the *two before it*?
- S: …3+5=8, 5+8=13, 8+13=21. Each number is the two before it, added!
- N: You just re-derived the Fibonacci sequence — the same rule the flowers follow.
  You didn't need me to tell you. The buttercups told you.
Moves: `elicit-observation`, `tabulate`, `redirect`, `name-last`, `credit-the-student`.
Misconception: reading the pattern as intervals (differences) instead of generation (sums).
Anchors: "3 + 5 = 8! … Each number is made by adding the two numbers before it!"
Rubric: (1) student supplies data from the chapter; (2) jump→sum redirect via question;
(3) student states the rule in own words; (4) no over-length tutor turns; (5) closing names
the sequence only after derivation, with credit.

## Scaling path 10 → 300

1. **Book 1 (ch01–ch12): 60** — 5/chapter at difficulties 1–5, one per chapter family.
2. **Book 2 (ch01–ch14): 70** — add Sankhya vocabulary, adversarial questions ("what if
   the rule broke?").
3. **Sankhya pack (5 PDFs): 40** — concepts in the reference guide + bridge paper; verify
   phrasing against the extracted .txt under `data/sankhya-text/`.
4. **Discovery zone (5 collections + sims index): 30** — lab-led questions; ground each in
   `data/discovery-zone-text/*.txt`.
5. **Cross-chapter synthesis: 100** — trigger questions that require joining ch01+ch06,
   Book 1+Book 2, Sankhya→phenomena.
Review: every batch is read against the Quality Bar by a second pass before seeding evals.

## Seed inventory (this file's sibling CSV)

`gold-exemplars-seeds.csv` — 280 exemplars, Books 1–2 + Sankhya pack + discovery zone + cross-chapter synthesis + Book 1 deep-dive + Sankhya RG deep-dive + Book 2 depth pass + Book 2 synthesis joins + RG Axiomatic Foundation (Think Axiomatically) + Book1↔Book2↔RG triple-synthesis: EX-001…EX-270 (Book 1 — ch01: EX-001–010 · ch02: EX-011–015 · ch03: EX-016–020 · ch04: EX-021–025 · ch05: EX-026–030 · ch06: EX-031–035 · ch07: EX-036–040 · ch08: EX-041–045 · ch09: EX-046–050 · ch10: EX-051–055 · ch11: EX-056–060 · ch12: EX-061–065 · Book 2 — ch01: EX-066–067 · ch02: EX-068 · ch03: EX-069–070 · ch04: EX-071–072 · ch05: EX-086–087 · ch06: EX-073 · ch07: EX-074 · ch08: EX-088–089 · ch09: EX-075–076 · ch10: EX-077 · ch11: EX-078–079 · ch12: EX-080–081 · ch13: EX-082–083 · ch14: EX-084–085 · Sankhya pack — reference guide v2.4: EX-090–101 · bridge v2.8: EX-102–105 · discovery zone: EX-106–111 · cross-chapter synthesis: EX-112–125 · Book 1 deep-dive — gauge, sound dials, atom as spherical standing wave, Sankhya survival-by-verse, laser coherence, Siddhi as direct knowing, ratio figures as bean numbers: EX-126–132 · Sankhya RG deep-dive — Sutra 1/68 loop, Aathyantha, Atho matrix, Guna Equation S.1, holographic space, Planck mass as oscillator, Planck constant derived, iron PHO, Guna algebra, Moolaprakriti, Prakriti/Vikrithi, Linga/Bhava, Abhiman/Ahankar, photon as Vrithi, self-similar vs scale-invariant, k and Si, the 6-step non-empty argument, the four-question compass: EX-133–150 · Book 2 depth pass — vacuum not nothing (ch01), the medium must match its contents (ch01), the packed continuum and its stress fates (ch02), one-stuff moolaprakriti + Purusha as state (ch02), the 3D seesaw atom (ch03), entropy as downhill flow (ch03), three ways of knowing (ch04), the holodeck generation (ch04), the breathing mode (ch05), count-merging (ch05), reality-first math-second + transcendence as indicator (ch06), the 28/72 dark split predicted (ch06), the two ways to count (ch07), Guna decoded to ten states (ch07), Quantum Aggregates (ch09), synchronisation degrees mass/charge/light (ch09), spin as broken synchronisation (ch10), pi as inward-gathering (ch10), the heartbeat Rs (ch13), the 1/7 carousel (ch13), nested spherical shells (ch14), k as the sequential journey (ch14), x algebraic not transcendental (ch12), the dimension detective (ch01): EX-151–175 · Book 2 synthesis joins — the structure-carrier union (176), state-not-thing vs reality-first (177), seesaw-aggregate one picture (178), the self-projecting holodeck (179), breathing and the k-journey (180), two self-feeding loops (181), reality-first entropy (182), thickness as count (183), x by necessity (184), constants generated (185), the atom as stored stress (186), ways-of-knowing sorted (187), the 28/72 in aggregates (188), spin as a status (189), flow with a heartbeat (190), evidence and structure agree (191), one stuff and moolaprakriti (192), the 7-frame in arithmetic (193), numbers sorted by role (194), three ways into the balance (195), dark as a nickname (196), rows meet shells (197), the shell as dimension filter (198), observer and activities as states (199), the evidence-to-balance arc (200): EX-176–200 · RG Axiomatic Foundation — the single axiom 1+1=2 (201), axiom discovered not chosen (202), one as a real whole (203), half as maximum change (204), the 1/n ladder (205), nature selects the balance (206), axioms protect causality (207), time as the single variable (208), derived vs measured constants (209), the vacuum conundrum (210), counting is certain (211), one field not four forces (212), patterns mathematically inevitable (213), PHO is no violation (214), redshift without expansion (215), derive don't believe (216), empower don't lecture (217), no mysticism (218), follow the ladder (219), same ratio everywhere (220), invisible is not unreal (221), the two light speeds (222), Planck derived as 7·Ne (223), the fine-structure source (224), one axiom to the engine (225): EX-201–225 · Book1↔Book2↔RG triple-synthesis — the thunderclap pair at every scale (226), doubling in three spellings (227), the driftwood medium (228), the gap never empty (229), the wave made by a joining eye (230), dynamic stillness (231), one stress sequence at three scales (232), one lossless exchange (233), oneness granted by coherence (234), rate as nature's one dial (235), the drainless exception (236), counting certain measuring fitful (237), the checkable claim (238), order on a schedule (239), closing as synchronisation (240), pi in three rooms (241), digits as rungs (242), the medium's quarter-note (243), what a photon is (244), coherence as quantity (245), confinement not force (246), three fates of stress (247), time the single dial (248), x in three homes (249), the three witnesses capstone (250): EX-226–250).
Each covers the chapter's core ideas end-to-end (petal-count derivation, the jumps
trap, the Pingala/Fibonacci/Lucas history, prediction-and-test, ratio convergence,
body-ratio measurement care, Meru Prastara doubling, diagonal Fibonacci, dimensional
diagonals, sunflower packing, sphere as the coherence limit, duhkha as the stress triad, the balance equation 1/x = 1 + x, the two light speeds, the hidden coherent mass, the electron boundary state, Michelson–Morley isotropy, Hubble's redshift, uncertainty as transition artifact, EPR unity, the C-power ladder, Siddhi as lawful resonance, standing-wave selection, cross-chapter joins: flower counts to the ten-count cycle, cube coherence to the orchestra, the sutra's seed to the six numbers, dark matter's two thresholds, light as stress transmigration, PHO as nature's balance, the ladder's doublings, the porous pot's 21 minutes, counting as the axiom). Field-copy an EX row into the schema above and expand
`Gold dialogue` into 3–6 full turns to grow the set.

## Inventory - batch 14 (2026-09-21)

- **Total: 270 rows, EX-001-EX-270.** Batch 14 = EX-251-270 (20 seeds) - first batch grounded in the
  G. Srinivasan treatise layer via the section-chunk store (sos-section-chunks.jsonl): SoS1 Axiomatic
  Concepts (4), Axiomatic Definitions (5), Axiomatic Basis for Physics: Pho State (3), Axiomatic Universe
  is Eternally Dynamic (2); SoS2 The Missing Count (4), Power House Of The Universe (2).
  Excluded per user ruling: SoS1 Abstract/Introduction (OCR-mangled region); weak Book2 chapters
  (ch03/04/06/10/11/12/13) as sources; withdrawn canon 28/72 absent (machine-scanned).
  Concepts: axiom indefeasibility / measuring costs work / merged counts gravitation / latent heat as
  hidden time / sequential vs simultaneous counting / ten claps phase-zero / two series meet at 55 /
  Kx from Catalan / mass-charge-radiation constraint orders / PHO rate two + RS 100/98 / one law of
  forces / h = BtpC threshold / hydrogen spectrum derived / photon life 6.4-25 Gyr and Karma /
  recounted-cube periodicity / Einstein stationary-field scope / 18 vs 6 quark levels / space absorbs
  counts / St = Mps/tp elasticity / zero-empirical-input capstone.

## Correction — COR-001 rewrite (PR #21, 2026-09-21)
- COR-001 "28/72 harmonic split" WITHDRAWN (user ruling 2026-09-20): 8 gold exemplars rewritten via the documented rewrite loop — register queue EX-184, EX-187, EX-188, EX-193, EX-196, EX-226, EX-250 plus EX-161 (found by the spelled-out paraphrase scan; register extended). Row count unchanged: **270** (EX-001–EX-270).
- Replacement canon: the balance six with master identity (e·Rs·7)/(π·x·10) = 1 (DZ Constant Explorer); ch05 nickname-vs-nature; ch14 cube 8 − 1 = 7; ch13 1/7 cycle. Draft ch06 material not used as source in any rewritten row.
- EX-079's 25/7 = 100/28 = 3.571428… (PHO mnemonic, gate v0.7 Gm family) is canon and untouched.
- Mentor re-review of the 8 rewritten rows pending.

## Inventory - batch 15 (2026-09-22)

- **Total: 280 rows, EX-001-EX-280.** Batch 15 = EX-271-280 (10 seeds) - first batch grounded in the
  Sankhya-Modern Physics Bridge v2.8 (August 2026 comparative assessment report, supporting canon),
  via its 31 concept chunks in the base retrieval index (chunks.jsonl, ids
  `sankhya:modern_physics_bridge_v2.8:*`). Focus per user ask: grounding the young STEM learner's
  perspective.
- Concepts: criteria for a correct theory / aether-to-quantum-vacuum / Michelson-Morley resolved /
  speed of light defined-vs-derived (C = 296,575,967, x = 0.618034, Fc ~ 1.010845) / Planck constant
  as threshold (CONCEPT ONLY - open item 10, no derivation value asserted) / G measured-vs-derived
  scale invariance (Cavendish 1798, 6.674e-11 measured) / quark confinement as simultaneous coherent
  state / wave-particle duality as two phases / uncertainty as simultaneity-boundary artifact /
  being-taught vs discovering-truth.
- Mix: difficulty 2->2, 3->4, 4->4; turns 3->9, 4->1. Withdrawn scan (8 COR-001 classes) CLEAN;
  anchors machine-verified verbatim in claimed chunk AND bridge txt. Pool batch 3 (PL-201-210)
  derives one draft per seed.
