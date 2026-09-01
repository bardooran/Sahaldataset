# Frozen Language Benchmark v1

Purpose: measure SahalNLP's Somali-first language analysis on externally sourced text that was selected before the analyzer was run.

## Scope

This benchmark contains 60 monolingual records:

- 20 Somali positives
- 20 English negatives
- 20 Swedish negatives

English and Swedish are counterexamples for Somali detection. They are not new language targets for SahalNLP.

## Selection rule

The records are aligned NTREX-128 sentences at source line positions:

`1-5, 501-505, 1001-1005, 1501-1505`

The same positions are used for Somali, English, and Swedish. This rule was fixed before measuring SahalNLP, so examples were not selected based on analyzer success or failure.

## Primary scoring

`expected_somali` is the frozen target:

- `true`: SahalNLP should recognize the record as Somali.
- `false`: SahalNLP must not claim the record is Somali.

For negative records, `non_somali` and `uncertain` are both safe for the primary Somali-detection metric. A secondary metric may report how often clear negatives are resolved as `non_somali` instead of remaining `uncertain`.

This keeps the benchmark Somali-first and does not turn English or Swedish into full NLP targets.

## Freeze rules

- Do not edit `benchmark.jsonl` after results are inspected.
- Corrections or new examples require a new benchmark version.
- Once benchmark answers influence SahalNLP implementation, v1 remains a frozen regression benchmark and must not be described as unseen for later versions.
- Never move these records into training or development data.

## Provenance

All benchmark text is a fixed subset of MicrosoftTranslator/NTREX, NTREX-128, pinned to source commit `468c6b69c7f6a75d31d4743d9daba2af566cc18d`.

NTREX-128 is released under CC BY-SA 4.0. See `../../provenance/ntrex_128.json` for source paths and attribution.

## Integrity

SHA-256 of the UTF-8 `benchmark.jsonl` file:

`31ca351801e9fbbebc467b9fc2f8f6515f2fd5e3fbe44dd8f733391d75b61e6c`
