# Abacus.AI terms verification (P1 · Legal & Land)

Verified against Abacus.AI's published Customer Terms of Service and Privacy
Policy on 2026-09-18. These are the standard (click-through) terms — no bespoke
agreement required for the Neil prototype.

## REG-01 — Customer owns the IP in Customer Data and the Application/Project — ToS §4

> "As between the parties, Customer owns all Intellectual Property Rights in
> Customer Data and the Application or Project (if applicable), and Abacus.AI
> owns all Intellectual Property Rights in the Services and Software."
Source: https://abacus.ai/customer-terms-of-service
Status: **Verified.**

## REG-02 — Termination for convenience + data deletion — ToS §6.3, §6.4

> §6.3: "Customer may terminate this Agreement for its convenience at any time
> on prior written notice and upon termination, must cease use of the applicable
> Services."
> §6.4: "If the Agreement is terminated, then … (ii) Abacus.AI will delete all
> Customer data for all storage devices; … (iv) upon request, each party will use
> commercially reasonable efforts to return or destroy all Confidential
> Information of the other party."
Source: https://abacus.ai/customer-terms-of-service
Status: **Verified.**

## REG-03 — No training on customer content — Privacy Policy

> "We do not use any personal information, Google user data, or customer-provided
> content (including prompts, uploads, or API data) to develop, improve, or train
> any generalized or proprietary AI or ML models."
> "Abacus.AI maintains a zero data retention agreement with all foundation and
> third-party AI models integrated into our product. Any data exchanged with such
> models occurs only for real-time inference and is never stored, logged, or
> reused by the model provider for training or product improvement."
Source: https://abacus.ai/privacy
Status: **Verified (standard terms).** Written confirmation for *this account*
still pending — support ticket filed (see REG-04 ticket).

## REG-04 — LoRA / fine-tuned weight export (product capability)

Not a legal clause — a product-capability question. Requires confirmation that a
fine-tuned LoRA adapter trained on SuperComputer can be downloaded as files
(e.g., safetensors + config).
Status: **Pending** — support ticket filed.

## Open items (evidence to close)

- [ ] Written confirmation from Abacus support that the no-training /
      zero-retention commitments apply to *this account* — support ticket filed.
- [ ] Product verification: can a fine-tuned LoRA adapter trained on
      SuperComputer be downloaded as files (e.g., safetensors + config)?
- [ ] Internal: release & publishing path for open artifacts (regardless of
      weight custody).
