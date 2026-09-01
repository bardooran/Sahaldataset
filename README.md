# SahalDataset

**Reviewed and traceable data for the Sahal Somali-first AI ecosystem.**

SahalDataset holds data. It does not contain the SahalNLP processing engine or the Sahal AI product.

## Simple ecosystem map

- **SahalNLP = tools** — cleaning, Somali detection, deduplication, quality checks, corpus processing, tokenization and evaluation tools.
- **SahalDataset = data** — reviewed corpus data, training data, validation data and frozen evaluation data.
- **Sahal AI = intelligence/product** — the Somali language engine, assistant, APIs and future model integration.

## Repository layout

```text
SahalDataset/
├── reviewed/     # human-reviewed linguistic/data examples
├── corpus/       # corpus releases and corpus manifests
├── training/     # data permitted for model/rule development
├── validation/   # development validation data
├── evaluation/   # frozen evaluation data kept out of training
├── provenance/   # source and licensing records
└── docs/         # data policy and review rules
```

## Core rules

1. Somali is the main language focus.
2. Every dataset should preserve source/provenance and licensing information when known.
3. Training and frozen evaluation data must remain separate.
4. Human review must be recorded instead of existing only in chat.
5. Uncertain labels stay uncertain until evidence supports a stronger decision.
6. Do not place SahalNLP implementation code or Sahal AI product code in this repository.
7. Do not claim a benchmark is unseen after its answers have been used to improve a system.

## Current status

**Foundation v1.** The repository structure and data policy are being established before reviewed datasets and frozen benchmarks are added.

## License

No repository-wide dataset license has been selected. Individual source data may have different licenses, so licensing must be recorded per dataset/source before reuse.
