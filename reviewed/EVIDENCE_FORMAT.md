# Reviewed evidence format v1

This format turns a useful linguistic observation into a traceable SahalDataset judgment without copying an entire external source into the repository.

## Purpose

A reviewed evidence record should answer four questions:

1. **What is being claimed?**
2. **What source supports it?**
3. **How was it reviewed?**
4. **Where is the judgment allowed to be used?**

## Workflow

```text
external/reference source
        ↓
precise source locator
        ↓
review of one linguistic claim
        ↓
approved / uncertain / rejected judgment
        ↓
explicit development/training/validation/evaluation permission
```

The external source itself does not automatically become Sahal training data.

## Required fields

- `record_id` — stable SahalDataset identifier.
- `language` — currently `so` for Somali.
- `subject` — the form or construction being reviewed.
- `claim_type` — spelling, POS, noun gender, meaning, morphology, usage, grammar, language status, or other.
- `claim` — the exact judgment. Do not make the claim broader than the evidence supports.
- `evidence` — one or more provenance records plus precise locators.
- `review` — approved, uncertain, or rejected, together with the review method.
- `usage` — explicit permission flags for development, training, validation, and evaluation.

## Important rules

- A dictionary entry is evidence, not automatically project truth.
- Do not copy large copyrighted passages into reviewed records. Store a precise locator and a short evidence note instead.
- If a parsed JSON entry looks broken, check the underlying source before approving a claim.
- Native-speaker review can confirm natural usage, but important project facts must still be recorded here with evidence and review status.
- Disagreement between sources should remain visible. Use `uncertain` rather than forcing a single answer.
- A record reserved for frozen evaluation must have `development: false` and `training: false`.
- Do not use an evaluation answer to improve SahalNLP and continue calling that example unseen.

## File organization

Reviewed collections should be grouped by purpose rather than creating many files at the repository root. For example, future collections may live under paths such as:

```text
reviewed/lexicon/
reviewed/morphology/
reviewed/grammar/
```

Only create a collection when we have real reviewed records to put in it.

The machine-readable contract is `reviewed/evidence_record.schema.json`.
