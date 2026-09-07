---
license: cc-by-4.0
language: [en, fr, pt, de, es]
task_categories: [text-classification, text-generation]
pretty_name: Sagius Philosopher Quotes
tags: [philosophy, quotes, multilingual, stoicism]
repository: https://github.com/gmalmeida/philosopher-quotes
---

# Sagius Philosopher Quotes

3613 English quotations from 160 public-domain
philosophers (author died in or before 1955, i.e. life+70 already
elapsed on Jan 1 of the current year), with parallel translations in
French, Portuguese, German and Spanish. Row counts: en 3613, fr 3594, pt 3597, de 3595, es 3593.
Source catalog: [Sagius](https://sagius.app).

**Public URL:** https://github.com/gmalmeida/philosopher-quotes

## What's inside

One JSONL file per language under `data/`. Each row:

```json
{"id": 115100, "lang": "en", "text": "...", "author": "Marcus Aurelius",
  "author_slug": "marcusaurelius", "school": "stoic", "category": "wisdom",
  "author_death_year": 180}
```

`id` is stable across languages — join on it for a parallel multilingual corpus.

## Load it

```python
from datasets import load_dataset
ds = load_dataset("json", data_files={
    "en": "https://raw.githubusercontent.com/gmalmeida/philosopher-quotes/main/data/quotes-en.jsonl",
    "fr": "https://raw.githubusercontent.com/gmalmeida/philosopher-quotes/main/data/quotes-fr.jsonl",
    "pt": "https://raw.githubusercontent.com/gmalmeida/philosopher-quotes/main/data/quotes-pt.jsonl",
    "de": "https://raw.githubusercontent.com/gmalmeida/philosopher-quotes/main/data/quotes-de.jsonl",
    "es": "https://raw.githubusercontent.com/gmalmeida/philosopher-quotes/main/data/quotes-es.jsonl",
})
```

Or clone: `git clone https://github.com/gmalmeida/philosopher-quotes.git`

## Licensing

- The original quote texts are in the **public domain** (every included author
  died 70+ years ago; authors not provably public-domain were excluded).
- The **curation, metadata and translations** are released under
  **CC-BY 4.0**. Attribution: "Sagius (https://sagius.app)".

## Provenance & honesty

Quotes come from the curated catalog that ships inside the Sagius app.
Attributions were reviewed against the catalog's philosopher registry
(238 thinkers with sourced lifespans and Wikipedia links). No AI-generated
text is included in this dataset — only the quotes themselves.
