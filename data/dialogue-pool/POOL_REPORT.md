# POOL_REPORT — synthetic dialogue pool (2026-09-19, post batch 2)

## Pool size and funnel
- Pool: 200 rows (PL-001..PL-200) = batch 1 (60) + batch 2 (140).
- Funnel: auto-validated=190, needs-mentor=8, rejected-structural=2.
- By difficulty (cumulative): { 1: 13, 2: 77, 3: 62, 4: 27, 5: 21 }.
- Non-validated rows (all pre-existing batch-1): PL-006, PL-009, PL-019, PL-039, PL-043, PL-048, PL-052, PL-053, PL-058, PL-070.

## Batch 2 provenance
- Seeds: 65 previously-unused clean-grounding seeds + 23 reuse (variation pairs — distinct trigger, dialogue, difficulty), drawn from an 88-seed clean set.
- Seed-grounding scan (strict single-quote regex, same logic as pool_validate): 88/250 gold anchors parse clean; 162 dirty — no quoted spans (formula-style anchors, e.g. EX-013) or paraphrase anchors (e.g. EX-001). Validator kept strict; dirty seeds excluded from new rows. Seed-data variance, NOT a validator bug.
- Batch-2 rows inherit their seed's gold rubric (Rubric=None -> seed rubric): checkpoints are the gold-verified ones for that concept.

## Funnel enforcement this round
- 4 batch-2 authoring errors caught and fixed same-turn: PL-158, PL-162, PL-152 (6-pair overruns -> trimmed to 5 pairs), PL-176 (6-pair overrun + credit-close wording). Post-fix: PL-152 auto-validated score 10; PL-176 auto-validated score 10. 0 unresolved batch-2 flags.

## Gate
- Heuristic status is TRIAGE. Human mentor review is the final gate before any row is promoted toward Dataset v1.
- mentor-review-queue.csv: all 200 rows in review order (needs-mentor by score asc, then auto-validated by score asc, rejects last).

## P2 exit status (honest)
- Dataset v1 target: >=1,500 reviewed dialogues in repo. Pool now holds 200 triaged drafts; 0 mentor-reviewed yet (queue just created).
- Revalidate: python3 build_pool.py && python3 pool_validate.py
