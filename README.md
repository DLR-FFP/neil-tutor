# neil-tutor — open home for the Neil project

Neil is an AI Socratic tutor for math & science (holds back answers, scaffolds with
questions). This repository is the **open, portable home for every Neil artifact**:
datasets, prompts, configs, eval logs, methods, and results — regardless of the
platform used to produce them.

## Portability rule
Everything here is disposable or replatformable by design. Nothing irreplaceable
lives solely on any single vendor platform; the winning configuration can be
re-run on open infrastructure (e.g., Prime Intellect credits).

## Repository layout
    compliance/                     compliance register, terms verification, licenses
    data/                           corpus inventory, rights log, datasets, eval logs
    corpus/                         the curated learner corpus (Book 1/2, outlines, Sankhya, Discovery Zone)
    gate/                           (L3 enforcement gate — our deterministic code, plain and inspectable)
    evals/                          I-score harness, robustness probes, preregistration
    docs/                           open write-up, educator one-pager, build notes

## Status labels
Items are marked as they progress: `proposed` (not executed), `in conversation`,
`draft`, `verified`, `cleared`, `blocked`. Nothing in this repo claims executed
status until it is evidenced.

## Provenance
All corpus items are logged in `data/corpus-inventory.csv` with rights-holder,
license, and rights status. The compliance register (`compliance/`) tracks every
obligation to a piece of evidence.
