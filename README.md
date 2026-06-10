# YUA-ES Communicative Contexts Corpus

**A parallel corpus of everyday Yucatec Maya–Spanish phrases for NLP and computational linguistics research.**

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-blue.svg)](https://creativecommons.org/licenses/by/4.0/)
<!-- [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](https://doi.org/10.5281/zenodo.XXXXXXX) -->

---

## Resumen (ES)

Corpus paralelo de **14,332 pares de frases alineadas maya yucateco (YUA) – español (ES)**, organizado en **31 contextos comunicativos** de la vida cotidiana. Fue creado mediante la colaboración institucional entre el **Centro de Investigación en Ciencias de Información Geoespacial (CentroGeo)** y la **Secretaría de la Cultura y las Artes de Yucatán (SEDECULTA)**, bajo la dirección de **Alejandro Molina Villegas**, en el marco del convenio **SEDECULTA-CDC-253-05-2024**, con el fin de incentivar proyectos encaminados a la generación de herramientas tecnológicas en lengua maya y contribuir al reconocimiento del patrimonio lingüístico del estado.

## Overview (EN)

This dataset contains **14,332 aligned phrase pairs** in Yucatec Maya (YUA) and Spanish (ES), organized around **31 communicative contexts** drawn from everyday life. It is intended for:

- Machine translation (Maya ↔ Spanish), especially low-resource MT
- Linguistic annotation and corpus studies
- Development of educational and documentation tools for Yucatec Maya
- Language preservation and revitalization efforts

| | |
|---|---|
| **Version** | 1.0 (June 2026) |
| **Language pair** | Yucatec Maya (YUA, Glottolog `yuca1254`) — Spanish (ES) |
| **Pairs** | 14,332 |
| **Communicative contexts** | 31 |
| **Unique YUA tokens** | 3,103 |
| **Unique ES tokens** | 2,548 |
| **License** | CC-BY-4.0 |
| **Format** | UTF-8 TSV |

---

## What's included

| File | Description |
|------|-------------|
| `YUA_ES_communicative_contexts_corpus_v1.tsv` | Main parallel corpus (14,332 rows) |
| `contexts.tsv` | Metadata for the 31 communicative contexts |
| `CITATION.cff` | Citation metadata |
| `LICENSE` | CC-BY-4.0 license and attribution terms |
| `DATASHEET.md` | Dataset documentation (Datasheets for Datasets, Gebru et al. 2021) |
| `README.md` | This file |

---

## Data format

### Main corpus — `YUA_ES_communicative_contexts_corpus_v1.tsv`

| Column | Type | Description |
|--------|------|-------------|
| `Phrase_ID` | string | Unique, sequential identifier: `YUAES` + 7 digits |
| `YUA` | string | Yucatec Maya phrase |
| `ES` | string | Spanish translation |
| `Communicative_Context` | string | Communicative-context code `COMMC####` (foreign key; joins to `contexts.tsv` → `Context_ID`) |

Example:

```
Phrase_ID	YUA	ES	Communicative_Context
YUAES0000001	Táan in bin koonol tu k'íiwikil koonol	Estoy yendo a vender al mercado	COMMC0001
YUAES0000002	Táan a bin koonol tu k'íiwikil koonol	Estás yendo a vender al mercado	COMMC0001
```

### Contexts — `contexts.tsv`

| Column | Type | Description |
|--------|------|-------------|
| `Context_ID` | string | Generic context code: `COMMC0001`–`COMMC0031` (primary key) |
| `Communicative_Context` | string | Readable label combining the Maya tag and Spanish name (e.g. `kiiwikil-Mercado`) |
| `n_phrases` | integer | Number of phrases in this context |

Example:

```
Context_ID	Communicative_Context	n_phrases
COMMC0001	kiiwikil-Mercado	488
COMMC0002	paarkee-Parque	464
```

The 31 contexts cover greetings and farewells, market, park, house, cornfield (*milpa*), homestead (*solar*), school, weather, courtesy, family, work, place and origin, location, daily culinary customs, physical description, shopping, travel, pets, local fauna, and personal-information domains (name, age, birthplace, marital status, residence), among others. See `contexts.tsv` for the full list with counts.

---

## Credits & authorship

This dataset is the product of an institutional collaboration between:

- **Centro de Investigación en Ciencias de Información Geoespacial (CentroGeo)** — Secretaría de Ciencia, Humanidades, Tecnología e Innovación (Secihti, México)
- **Secretaría de la Cultura y las Artes de Yucatán (SEDECULTA)** — Gobierno del Estado de Yucatán, México

Carried out under agreement **SEDECULTA-CDC-253-05-2024**.

**Data authors** (direct contributors to data creation, annotation, and validation):

1. **Alejandro Molina-Villegas** — CentroGeo (Secihti, México) — Technical lead / Responsable Técnico
2. **María Elisa Chavarrea Chim** — SEDECULTA — Linguistic supervision
3. **Samuel Canul Yah** — SEDECULTA — Maya language specialist
4. **Sary Lorena Hau Ucán** — SEDECULTA — Maya language specialist
5. **Daniela Esther Cano Chan** — SEDECULTA (fellow) — Annotation
6. **Alejandra del Rocío Moo Batun** — SEDECULTA (fellow) — Annotation
7. **Gregorio Hau Caamal** — SEDECULTA (fellow) — Annotation

The data was elaborated, supervised, and curated by a team of Maya-speaking collaborators.

---

## Use in the AmericasNLP 2024 Shared Task

**A subset of this corpus was used in the AmericasNLP 2024 Shared Task 2: Creation of Educational Materials for Indigenous Languages**, in the Yucatec Maya (`yuca1254`) portion.

This shared task asks NLP systems to **automatically generate language-learning exercises**: given a base sentence and a target property, a system transforms the sentence by changing that single property (for example, negation or tense). Its motivation is urgent and practical — many Indigenous languages of the Americas are vulnerable or endangered, community revitalization efforts depend on teaching materials that are costly and slow to produce by hand, and most of these languages are severely low-resource and exhibit linguistic properties uncommon in mainstream NLP. The task exists to motivate researchers to build systems that can support the teaching and diffusion of these languages.

That a subset of these Maya–Spanish phrases fed such a task reflects the corpus's purpose: data built to power educational and language technology for Yucatec Maya, in a low-resource setting where every well-curated, openly licensed pair matters.

> **If you use these data for any AmericasNLP task, you must cite this corpus (see _How to cite_).**

---

## How to cite

See `CITATION.cff`. Example BibTeX:

```bibtex
@dataset{molina_villegas_2026_yua_es,
  title     = {{YUA-ES Communicative Contexts Corpus}},
  author    = {Molina-Villegas, Alejandro and Chavarrea Chim, Mar{\'i}a Elisa
               and Canul Yah, Samuel and Hau Uc{\'a}n, Sary Lorena
               and Cano Chan, Daniela Esther and Moo Batun, Alejandra del Roc{\'i}o
               and Hau Caamal, Gregorio},
  year      = {2026},
  version   = {1.0},
  publisher = {Zenodo},
  doi       = {10.5281/zenodo.XXXXXXX},
  license   = {CC-BY-4.0}
}
```

---

## Known limitations

- Phrase length is short and everyday-register by design (originally aimed at educational materials).
- Coverage across contexts is uneven (from ~53 to ~2,472 pairs); see `contexts.tsv`.
- Some Spanish strings depart from standard orthography or phrasing. This is **intentional and preserved**: these renderings reflect how a local Maya–Spanish bilingual would naturally translate, and keeping them lets technologies reproduce the naturalness of contemporary speakers rather than a normalized, non-native standard.
- Context names in `contexts.tsv` are editorial interpretations of the Maya table labels and may be refined by the authors.

---

## License

Released under the **Creative Commons Attribution 4.0 International (CC-BY-4.0)** license. You may share and adapt the material, including commercially, provided you give appropriate credit to the data authors and the institutional collaboration (see `CITATION.cff` and `LICENSE`). Full text: https://creativecommons.org/licenses/by/4.0/

---

## Positioning

We release this corpus to support the view that the path forward for technology in indigenous languages is quality data in the open commons, with transparent authorship and shared credit for the speaker communities and professionals who create it.
