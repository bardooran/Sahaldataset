# Reviewed data

This area is for human-reviewed Somali data and annotations.

Reviewed data may include words, sentences, morphology, grammar, language labels, or other linguistic judgments. Each collection must document its purpose, provenance, review method, and license/usage status.

## Reviewed evidence v1

Use `EVIDENCE_FORMAT.md` and `evidence_record.schema.json` when turning a source observation into a SahalDataset linguistic judgment.

The basic rule is:

```text
source evidence → precise locator → human/source review → recorded judgment → explicit usage split
```

External dictionaries and other reference works remain external sources. A reviewed record should capture the specific supported fact and provenance rather than copying the whole source into SahalDataset.

A reviewed record may be `approved`, `uncertain`, or `rejected`. Uncertainty is preserved when evidence is weak or sources disagree.

A review example can be used for development only if its usage fields permit that use. Do not silently move frozen evaluation answers into training or development.

Do not create empty topic folders in advance. Add a reviewed collection only when real reviewed records are ready for it.
