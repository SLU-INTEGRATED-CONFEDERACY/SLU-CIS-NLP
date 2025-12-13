# Kapampangan Lexicon

## Overview

This repository contains a structured Kapampangan lexicon encoded in JSON format. The lexicon is designed for linguistic research, language documentation, educational use, and natural language processing (NLP) tasks such as tokenization, part-of-speech tagging, lemmatization, and bilingual lexicon alignment.

Kapampangan (also known as Pampango) is a major Philippine language spoken primarily in Central Luzon. This lexicon aims to preserve lexical knowledge while making it computationally accessible.

---

## What This Lexicon Is About

The lexicon is a **word-level resource** that maps Kapampangan entries to:

- their canonical forms (lemmas),
- grammatical categories,
- English and Filipino (Tagalog) translations,
- short semantic descriptions,
- example sentences in Kapampangan, and
- bibliographic or digital sources.

It combines data from multiple dictionaries, academic works, online lexical databases, and cultural texts. Because of this, the lexicon reflects **real language use**, including traditional vocabulary, modern terms, cultural concepts, and occasional orthographic variation.

Some entries are fully annotated, while others are partial. This reflects the ongoing and incremental nature of lexicon building.

---

## File Structure

### `kapampangan_lexicon.json`

The main file is a JSON array. Each element in the array represents **one lexical entry**.

```json
[
  { "word": "abu", "lemma": "abu", ... },
  { "word": "abung", "lemma": "abung", ... }
]
```

Each entry follows a consistent schema described below.

---

## Lexical Entry Schema

Each lexical entry contains the following fields:

### 1. `word`

- **Type:** string
- **Description:** The surface form as it commonly appears in Kapampangan text.
- **Example:** `"abul"`, `"adwang dalan"`

This may include multi-word expressions, hyphenated forms, or diacritics.

---

### 2. `lemma`

- **Type:** string or `"None"`
- **Description:** The canonical or dictionary form of the word.

For inflected or derived forms, this field links the entry to its base form. If the lemma is unknown or not yet annotated, it is set to `"None"`.

---

### 3. `variants`

- **Type:** string or `"None"`
- **Description:** Alternative spellings or closely related forms.

This accounts for orthographic variation across sources and dialectal usage.

---

### 4. `pos` (Part of Speech)

- **Type:** string
- **Description:** The grammatical category of the word.

Common values include:

- `NOUN`
- `VERB`
- `ADJ`
- `ADV`
- `PRON`
- `DET`
- `NUM`

If the part of speech is not yet identified, the field may be empty.

---

### 5. `en_translation`

- **Type:** string
- **Description:** English gloss or translation of the word.

This is intended for bilingual alignment and cross-linguistic comparison.

---

### 6. `tl_translation`

- **Type:** string or `"None"`
- **Description:** Filipino (Tagalog) equivalent.

This supports local language education and comparative Philippine linguistics.

---

### 7. `meaning`

- **Type:** string or `"None"`
- **Description:** A short semantic definition written in plain English.

This goes beyond simple translation and clarifies usage or sense distinctions.

---

### 8. `example_sentence`

- **Type:** string or `"None"`
- **Description:** A sample sentence showing the word in natural Kapampangan usage.

These examples help illustrate syntax, semantics, and pragmatic context.

---

### 9. `source`

- **Type:** object

```json
"source": {
  "source_id": "dict_006",
  "link": "https://..."
}
```

- **`source_id`:** Internal identifier for the reference
- **`link`:** URL pointing to the original dictionary, paper, or text

This ensures transparency, traceability, and academic credibility.

---

## Data Characteristics and Notes

- Some entries are **incomplete** (e.g., missing lemma, POS, or examples).
- Orthography may vary due to differences across historical and modern sources.
- Diacritics are preserved when available.
- Multi-word expressions are treated as single lexical items when they function semantically as one unit.

Think of this lexicon like a **growing dictionary card catalog**: some cards are fully detailed, others are placeholders waiting to be completed.

---

## Intended Use Cases

- Linguistic analysis of Kapampangan
- NLP tasks (lexicon lookup, POS tagging, NER support)
- Educational materials and language learning tools
- Cross-lingual studies (Kapampangan–Filipino–English)
- Cultural and lexical preservation

---

## Pros

- Structured and machine-readable
- Bilingual and partially trilingual
- Source-attributed entries
- Suitable for both human and computational use

## Cons

- Not yet exhaustive
- Inconsistent annotation completeness
- No sense disambiguation IDs for polysemous words
- No frequency or usage metadata

---

## Future Directions

Possible extensions include:

- Sense-level IDs for polysemous entries
- Morphological features (affixes, aspect, voice)
- Frequency counts from corpora
- Kulitan script representations
- Validation and normalization of incomplete entries

---

## Summary of Key Takeaways

- This is a **structured Kapampangan lexical database** in JSON format.
- Each entry captures form, meaning, grammar, usage, and source.
- The lexicon supports both **language preservation** and **computational processing**.
- Incompleteness reflects an evolving, research-oriented resource rather than a finished dictionary.
