# A Non-Corrective Poetry Editor for Marking Ambiguous Fragments in Creative Writing

This repository contains a short ACM-style project paper about a prototype of a non-corrective poetry editor.

The main idea of the project is simple: a creative text editor should not automatically decide whether an unusual word, line break, or rhythm shift is wrong. Instead, it should mark such places as ambiguous fragments and let the author decide what they mean.

## Paper

Title: A Non-Corrective Poetry Editor for Marking Ambiguous Fragments in Creative Writing  
Author: Dmitry Neledva  
Year: 2026  
Format: ACM-style short paper  
PDF: paper.pdf  
LaTeX source: main.tex

## Project idea

Standard text editors are usually designed to correct mistakes. This works well for ordinary texts, but creative writing often includes intentional deviations: unusual words, broken rhythm, strange punctuation, or non-standard line breaks.

In poetry and other creative texts, the same fragment can be either:

- a real mistake;
- an authorial word;
- a stylistic device;
- a rhythm shift;
- a fragment that should be reviewed later.

The proposed editor does not automatically correct such fragments. It marks them and allows the author to classify each case manually.

## Main features described in the paper

- Detection of ambiguous fragments in creative texts
- Comment-based revision workflow
- Manual authorial decisions
- Personal user dictionary for authorial words
- Local authorial corpus
- Line-level rhythm map based on syllabic structure

## Authorial decision model

The editor treats detected fragments not as final errors, but as places that require an authorial decision.

Possible decisions:

| Decision | Meaning |
|---|---|
| Correct | The author accepts the fragment as a mistake |
| Keep | The fragment is intentional |
| Ignore | The comment is not relevant |
| Later | The author postpones the decision |
| Dictionary | The word is added to the personal dictionary |

## Repository structure

```text
.
├── main.tex                  # LaTeX source of the paper
├── paper.pdf                 # Compiled ACM-style PDF
├── README.md                 # Project description
├── examples/
│   ├── author_corpus_sample.json
│   └── user_dictionary_sample.json
└── survey/
    └── questionnaire.md
```

## Example data

The prototype uses simple local JSON files.

### Author corpus

```json
{
  "id": "2026-05-13T11-04-18",
  "title": "Example poem",
  "created_at": "2026-05-13T11:04:18",
  "text": "...",
  "notes": ""
}
```

### User dictionary

```json
{
  "words": [
    "neologism",
    "authorialword",
    "nonstandardform"
  ]
}
```

## Current status

This is an independent project and portfolio paper.  
The current version presents the design logic and prototype workflow. It does not claim to provide a full literary analysis or prove that the editor improves creative writing.

## Limitations

- The editor does not understand the meaning of the poem.
- The rhythm map is based on a simple syllabic profile.
- The system does not decide whether a fragment is good or bad.
- The current version does not include a user study.
- The corpus is stored locally and has a simple structure.

## Future work

Possible future improvements:

- version history for texts;
- export of annotated texts;
- improved storage of authorial decisions;
- search through comments and corpus entries;
- statistics about repeated authorial devices;
- optional AI-assisted suggestions without automatic correction.

## Links

- Project website: https://neledva.poet.ru
- Paper PDF: paper.pdf
- Demo: add demo link here
- DOI / archive link: add Zenodo or OSF link here
## Citation

If you want to cite this project, use:

```bibtex
@misc{neledva2026poetryeditor,
  author = {Neledva, Dmitry},
  title = {A Non-Corrective Poetry Editor for Marking Ambiguous Fragments in Creative Writing},
  year = {2026},
  howpublished = {Independent project paper},
  url = {https://neledva.poet.ru}
}
```

## License

This repository is published for portfolio and research demonstration purposes.  
Code, text, and data license should be specified before reuse.
