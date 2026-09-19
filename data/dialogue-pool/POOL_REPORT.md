# Dialogue Pool - Batch 1 funnel report (2026-09-18)

- **Pool rows:** 60 (PL-001..PL-060), negatives: 12 (NG-001..NG-012)
- **Funnel outcome:** {"auto-validated": 51, "needs-mentor": 7, "rejected-structural": 2}
- **By difficulty:** {"2": 33, "3": 25, "5": 2}
- **Mean heuristic score:** 8.88/10
- **Negative failure modes:** answer-too-early, ends-student-side, flattery-no-probe, leading-the-witness, lecture-dump, misconception-ignored, missing-credit, moves-mislabel, over-length-tutor-turn, premature-name, vague-anchorless, wrong-canon-number

## Method
- Drafts inherit Source/Concept/Misconception/Anchors from their gold seed (Seed-EX);
  anchors are gold-verified verbatim quotes, so grounding is mechanical.
- New content per row: trigger, dialogue, moves mix, difficulty, rubric checkpoints.
- Turns field is computed from the dialogue (pairs count), not hand-declared.
- Funnel: structural validation (starts S:, alternation, Turns==pairs, ends tutor-side
  N: with Sophie + credit, Moves 3-5 unique incl. credit-the-student), grounding check
  (anchor quotes located in cited source, normalized), heuristic /10 (credit close,
  question density, no-lecture length, student articulation, grounding).
  Status: >=8 auto-validated | 5-7 needs-mentor | <5 rejected; structural flags override.
- Heuristic scores are TRIAGE; human mentor review is the final gate before promotion.

## Convention note (discrepancy documented)
gold-exemplar-template.md Quality Bar 2 says dialogues end student-side; the enforced
convention (batch skill rules + strict validator + gold data) is a tutor-side close:
final N: turn with the student's name and a credit phrase. The pool follows the ENFORCED
convention. The template file is untouched (frozen md5 a519ae5f...).

## Status vs the P2 exit criterion
Dataset v1 target: >=1,500 reviewed dialogues in repo. Batch 1 puts 60 triaged drafts
in the pool (~4% of target). Continuation: batch 2 (~140 rows, incl. d1/d4
spread) + first mentor-review pass over auto-validated rows.
