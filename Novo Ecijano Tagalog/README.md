#  NOVO ECIJANO TAGALOG LEXICON


## A. Group Members

* IVAN ALBARIDA
* RENUEL JEREMI BALOGO
* AU BUMANGLAG
* MACKENZHIE DANNIEL CABUTE
* KYLE ANDREW DUMIPNAS
* JOVV NEIU ESMILLA
* NATHAN MIKHAIL EUGENIO
* EMIL JOHN GAPUZ

---

## B. Metadata

- **Dataset Name:** Novo Ecijano Tagalog Lexicon
- **Description:** A structured lexicon of Novo Ecijano Tagalog words with definitions, parts of speech, and sample sentences.
- **Language:** Novo Ecijano / Tagalog
- **Format:** CSV (Comma-Separated Values)
- **Number of Records:** 125 entries
- **Intended Use:** Linguistic research, education, and NLP applications

---

## C. Fields of the Lexicon

| Field Name        | Description                                      |
|-------------------|--------------------------------------------------|
| Word              | The Novo Ecijano / Tagalog lexical entry         | 
| Part of Speech    | Grammatical category of the word                 | 
| Definition        | Meaning or translation of the word               | 
| Sample Sentence   | Example sentence demonstrating usage             | 


---

## D. How to Use the Lexicon

### 1. General Use
You can open the file using:
- Microsoft Excel
- Google Sheets
- LibreOffice Calc


---

### 2. Use with Python (Pandas)

```python
import pandas as pd

# Load the dataset
df = pd.read_csv("Novo Ecijano Tagalog Lexicon.csv")

# Word you want to locate
word_to_find = "äakas"

# Access the word
entry = df[df["Word"] == word_to_find]
```
---




