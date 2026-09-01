# SahalDataset data policy

SahalDataset is the data layer of the Sahal ecosystem.

## Responsibilities

SahalDataset may hold reviewed Somali examples, corpus manifests/releases, training data, validation data, frozen evaluation data, and provenance/licensing records.

It should not become the home for NLP implementation code. Processing and evaluation tools belong in SahalNLP. User-facing intelligence belongs in Sahal AI.

## Data separation

### Reviewed
Human-reviewed material. A review record should say what was reviewed and, when useful, who or what evidence supported the decision.

### Corpus
Cleaned or prepared corpus material plus enough metadata to understand its source and processing history.

### Training
Data that may influence rules, tokenizers, models, thresholds, prompts, or other development decisions.

### Validation
Development data used to compare choices while building. Validation data is not a final unseen benchmark if developers repeatedly inspect its answers.

### Evaluation
Frozen data used to measure a system. Evaluation examples must not be silently copied into training/development data.

If evaluation answers are inspected and then used to change a system, that benchmark remains useful for regression testing but must no longer be described as unseen.

## Provenance and licensing

For each meaningful data source, record when known:

- source name or identifier;
- source type;
- original URL or location;
- collection/retrieval date;
- license or usage terms;
- transformation history;
- review status.

Unknown licensing is not permission. Data with unclear rights should be kept out of distributable/training releases until resolved.

## Somali review

Native-speaker review is valuable, but important corrections should become documented records, tests, or reviewed examples rather than remaining only in conversation history.

Do not force uncertain Somali morphology, grammar, meaning, gender, dialect, or natural usage into a confident label when evidence is weak.
