# Datasheet — YUA-ES Communicative Contexts Corpus v1.0

Following *Datasheets for Datasets* (Gebru et al., 2021).

## Motivation
- **Purpose.** Provide an open, aligned Yucatec Maya–Spanish phrase corpus to support machine translation, language technology, and documentation for a low-resource indigenous language, and to contribute to recognition of Yucatán's linguistic heritage.
- **Created by.** CentroGeo, part of the Secretaría de Ciencia, Humanidades, Tecnología e Innovación (Secihti, México), and SEDECULTA, under agreement SEDECULTA-CDC-253-05-2024.
- **Funding / support.** Institutional collaboration between the two parties; see the agreement.

## Composition
- **Instances.** 14,332 parallel phrase pairs (YUA, ES), each tagged with one of 31 communicative contexts.
- **Granularity.** Short, everyday phrases (mean length ~5.3 tokens per side).
- **Language variety.** Yucatec Maya (Glottolog `yuca1254`); Spanish as spoken/written in Yucatán.
- **Labels.** `Communicative_Context` (a `COMMC####` code) links each pair to a communicative domain; see `contexts.tsv`.
- **Splits.** None predefined. Users should create train/dev/test splits; note that some near-duplicate variants exist and exact duplicates have already been removed to limit leakage.
- **Sensitive content.** Everyday, non-sensitive topics (greetings, household, market, family, etc.). No personal data about identifiable private individuals is intended.

## Collection process
- Phrases were authored, translated, and aligned by a team of Maya-speaking professionals, linguists, NLP practitioners, and volunteers, starting from material first produced in 2022 and continued 2022–2024.
-

## Preprocessing / cleaning
- UTF-8 normalization; CRLF→LF; whitespace trimming and collapse.
- Exact (YUA, ES) duplicates removed (72), logged in `duplicates_removed.tsv`.
- Linguistic content otherwise unmodified; regional Spanish spellings preserved.
- Sequential re-indexing to `YUAES#######`.

## Uses
- **Suitable for.** MT (YUA↔ES), bilingual lexicon induction, educational tools, corpus linguistics, language documentation.
- **Out of scope / caution.** Not a balanced or exhaustive sample of the language; uneven context coverage; short register only. Should not be treated as authoritative orthographic reference.

## Distribution
- Released openly under CC-BY-4.0 via Zenodo (DOI) and GitHub.

## Maintenance
- Maintained by Alejandro Molina-Villegas (CentroGeo). Issues and contributions via the GitHub repository. Future versions may add more phrases, more contexts, morphological/POS annotation and expand contexts.
