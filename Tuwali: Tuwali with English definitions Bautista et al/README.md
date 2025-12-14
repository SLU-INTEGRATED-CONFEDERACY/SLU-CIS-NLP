# Tuwali Ifugao Electronic Lexicon
**A structured digital lexicon for preserving and learning the Tuwali language of Ifugao, Philippines**

This project provides a comprehensive bilingual lexicon documenting the Tuwali language, an indigenous language of the Ifugao province. The lexicon is designed for language preservation, educational purposes, and future NLP applications, offering structured entries with English definitions, Tagalog explanations, sample sentences, and grammatical information.

---

## a. Project Team
- **Bautista, Mary Antoinnette**
- **Bustria, Jazper Louie Ysmael**
- **Del Rosario, Edward Nathan**
- **Laguerta, Harold**
- **Palacay, Abigail**
- **Riboroso, Rhotre Matthieu**
- **Urbiztondo, Karl Jasper**

*4th Year Computer Science Students, Saint Louis University (SLU), Baguio City*  
*Course: CSE30 - Natural Language Processing, Year: 2025*

---

## b. Dataset Metadata
| Field | Description |
|-------|-------------|
| **Dataset Name** | `tuwali_lexicon.xlsx` |
| **Language(s)** | Tuwali (Ifugao), English, Tagalog |
| **Source** | Webonary (Tuwali Dictionary), Omniglot (Tuwali Numbers) |
| **Format** | Excel (.xlsx) |
| **Encoding** | UTF-8 |
| **Number of Entries** | 5,343 |
| **Academic Context** | NLP Lexicon Project, Computer Science Department |
| **Instructor** | CSE30 NLP Instructor |
| **Purpose** | Language learning, NLP research, and language preservation |

---

## c. Lexicon Structure
The Excel file contains the following columns:

| Column Name | Description | Example |
|-------------|-------------|---------|
| **word** | Tuwali headword | `aaa` |
| **part_of_speech** | Grammatical category (e.g., adj, comm, trans, intrans, sta, proc, adv, interj, det, prop, neg) | `trans` |
| **definitions** | English definitions of the word | `to run` |
| **examples** | Sample sentences demonstrating usage (multiple examples separated by `|`) | `Nagpapatakder siya iti balay | Agkakabsat da iti eskwela` |
| **tag_definition** | Tagalog meaning or paraphrased explanation | `tumakbo` |

---

## d. How to Use This Lexicon

### 1. For Language Learners
- Look up Tuwali words and find English and Tagalog equivalents  
- Study usage through example sentences  
- Filter or browse by **Part of Speech** to focus on grammatical categories  

### 2. For Researchers
- Analyze language structure and morphology  
- Study semantic relationships across Tuwali, English, and Tagalog  
- Support research in linguistic preservation and NLP applications  

### 3. For Developers
- Load the Excel file into Python, R, or JavaScript:
```python
import pandas as pd
df = pd.read_excel("tuwali_lexicon.xlsx")
# Example lookup
df[df['word'] == 'aaa']
