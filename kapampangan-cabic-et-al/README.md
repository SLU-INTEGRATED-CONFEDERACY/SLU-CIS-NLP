# Kapampangan Language Datasets

## Overview

This repository contains two complementary datasets for the Kapampangan language: a comprehensive dictionary and a collection of real-world phrases. Together, these datasets provide both lexical resources and authentic language usage examples to facilitate linguistic research, language learning applications, and natural language processing tasks for the Kapampangan language.

## Files Description

This repository contains two CSV files:
- `dictionary.csv` - Lexical entries from a formal dictionary
- `phrases.csv` - Real-world phrase examples from online communities

## Dataset 1: Dictionary (`dictionary.csv`)

### Structure

The dataset contains the following columns:

| Column | Description |
|--------|-------------|
| `word` | The Kapampangan word entry from the dictionary |
| `syllables` | International Phonetic Alphabet (IPA) representation of the word's pronunciation |
| `meaning` | The dictionary definition of the word in English |
| `tag` | Part of speech tag (e.g., noun, verb, adjective, etc.) |
| `english` | English equivalent or translation of the Kapampangan word |
| `filipino` | Filipino (Tagalog) translation of the English equivalent via Google Translate |

### Data Source

- **Primary Source:** Michael L. Forman's Kapampangan Dictionary
- **Translation Method:** English to Filipino translations were generated using Google Translate

### Example Entry

```csv
word,syllables,meaning,tag,english,filipino
alaga,a.la.ga,to care for; to take care of,verb,care,pag-aalaga
```

---

## Dataset 2: Phrases (`phrases.csv`)

### Structure

The phrases dataset contains the following columns:

| Column | Description |
|--------|-------------|
| `phrase` | The Kapampangan phrase as used in real-world contexts |
| `meaning` | The meaning of the sentence, consulted with a native Kapampangan speaker |
| `tag` | Part of speech tagset for each word in the phrase |
| `english` | English translation consulted with a native speaker |
| `filipino` | Filipino (Tagalog) translation consulted with a native speaker |
| `context` | The use case or situational context for the phrase |

### Data Source

- **Primary Source:** Reddit's r/Kapampangan community
- **Validation Method:** Meanings, translations, and context verified by consultation with native Kapampangan speakers
- **Collection Method:** Phrases extracted from community posts and discussions

### Example Entry

```csv
phrase,meaning,tag,english,filipino,context
"Mayap a abak","Good morning",ADJ PART NOUN,"Good morning","Magandang umaga","Greeting used in the morning"
```

---

## Combined Usage

These datasets can be used together for:
- **Dictionary (`dictionary.csv`):** Word-level analysis, vocabulary building, pronunciation guides
- **Phrases (`phrases.csv`):** Sentence-level understanding, conversational patterns, contextual usage
- **Combined:** Comprehensive language learning systems, NLP model training with both lexical and contextual data

Specific applications include:
- Kapampangan language learning and education
- Linguistic analysis and research
- Development of language learning applications
- Natural language processing and machine learning models
- Cross-linguistic studies between Kapampangan, English, and Filipino
- Syntax and grammar analysis using tagged phrases
- Conversational AI and chatbot development

## Format

- **File Type:** CSV (Comma-Separated Values)
- **Encoding:** UTF-8 (recommended)
- **Delimiter:** Comma (`,`)

## Example Entry

```csv
word,syllables,meaning,tag,english,filipino
alaga,a.la.ga,to care for; to take care of,verb,care,pag-aalaga
```

## Citation

```
Michael L. Forman. 1971. Kapampangan Dictionary. University of Hawai‘i Press, Honolulu, HI. PALI Language Texts—Philippines. ISBN 9780824881139. https://manifold.uhpress.hawaii.edu/projects/kapampangan-dictionary
```

## Acknowledgments

- **Dictionary data:** Derived from Michael L. Forman's Kapampangan Dictionary. Filipino translations were generated using Google Translate and may require human verification for accuracy.
- **Phrase data:** Collected from Reddit's r/Kapampangan community with translations and meanings validated by native Kapampangan speakers. Special thanks to the community members and native speakers who contributed their expertise.