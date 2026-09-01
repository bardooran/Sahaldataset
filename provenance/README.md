# Provenance

This area records where SahalDataset material came from and what rights or restrictions apply.

Useful fields include source identifier, source type, URL/location, retrieval date, license/terms, transformation history, and review status.

Do not invent missing provenance or licensing. Unknown values should remain explicitly unknown until resolved.

## External reference sources

Sahal may register a useful language source here even when the source content itself must **not** be committed to SahalDataset.

A source marked `reference_only` or `reference_only_pending_rights_review` is evidence/reference material, not Sahal-owned training data.

For these sources:

- keep the full restricted or rights-unclear extract out of `reviewed/`, `training/`, `validation/`, and `evaluation/`;
- do not apply a Sahal open-data license to upstream content unless the upstream rights actually allow it;
- record whether redistribution, training, validation, and evaluation use are approved;
- treat machine-parsed dictionary entries as unreviewed until their entry boundaries and linguistic fields are checked;
- when a linguistic fact is promoted into a reviewed Sahal record, retain the source identifier and human-review status;
- preserve uncertainty when the source, parsing, meaning, grammar, or rights are unclear.

This lets Sahal use external books and dictionaries as **evidence** without confusing them with SahalDataset-owned or freely reusable data.
