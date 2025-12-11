# Gaddang E-Dictionary Project

## Overview
This repository contains a cleaned and structured dataset for a Gaddang-English-Filipino trilingual electronic dictionary. The dataset includes over 500 lexical entries, complete with definitions, parts of speech, and usage examples, aggregated from various linguistic resources.

## A. Group Members
*   **Calera, Earl Daniele**
*   **De Leon, Earl Macy**
*   **De Leon, Tomie**
*   **Grabador, Ramil**
*   **Modelo, Alexx**
*   **Ordonio, Adrian James**
*   **Pascual, Bryan**

## B. Metadata
*   **Dataset Name:** Gaddang E-Dictionary - Cleaned Data
*   **Language(s):** 
    *   **Source Language:** Gaddang
    *   **Target Languages:** English, Filipino (Tagalog)
*   **Total Entries:** 503
*   **File Format:** Comma-Separated Values (CSV)
*   **Encoding:** UTF-8
*   **Date Created:** December 2025
*   **Primary Sources:** 
    *   *A Gaddang Vocabulary* by Yukihiro Yamada
    *   *Austronesian Basic Vocabulary Database*
    *   *Construal of selected Gaddang lexicon and their cultural implications* (Research & Reviews: Journal of Linguistics)
    *   *Gaddang language resources* (Verbix)

## C. Data Fields (Lexicon Structure)
The dataset is organized into columns separated by commas. Below is the description of each field found in the header:

| Field Name | Description |
| :--- | :--- |
| **[Index/ID]** | Unique numerical identifier for the entry (column 1). |
| **Word (Gaddang)** | The headword in the Gaddang language. |
| **Word (English)** | The direct translation of the headword into English. |
| **Word (Filipino)** | The direct translation of the headword into Filipino. |
| **Meaning** | A detailed definition or description of the word (typically in English). |
| **Gaddang Example Sentence** | A sentence demonstrating how the word is used in context (if available). |
| **English Example Sentence** | The English translation of the Gaddang example sentence (if available). |
| **POS (Parts of Speech)** | The grammatical category of the word (e.g., Noun, Verb, Adjective). |
| **Source** | The specific reference material or citation from which the entry was obtained. |

## D. How to Use the Lexicon

### 1. Opening the Data
*   **Spreadsheet Software:** You can open the file directly in Microsoft Excel, Google Sheets, or LibreOffice Calc. 
    *   *Note:* If opening in Excel, ensure you select "Comma" as the delimiter to separate the columns correctly.
*   **Text Editors:** You can view the raw data using Notepad, Notepad++, VS Code, or Sublime Text.

### 2. Searching for Words
*   Use `Ctrl + F` (or `Cmd + F` on Mac) in your viewer of choice to find specific translations.
*   **Example:** To find the Gaddang word for "House", search for "house" in the English column or look for "balay" in the Gaddang column.

### 3. Usage for Developers (Python Example)
If you wish to use this dataset in a Python application (e.g., for a search tool or NLP project), you can use the `pandas` library:

```python
import pandas as pd

# Load the dataset
# Ensure the file name matches your local file
df = pd.read_csv('Gaddang E-Dictionary - Cleaned Data.txt')

# 1. View the first 5 entries
print(df.head())

# 2. Search for a specific Gaddang word (e.g., 'balay')
search_word = 'balay'
result = df[df['Word (Gaddang)'] == search_word]
print(result)

# 3. Filter by Part of Speech (e.g., Nouns)
nouns = df[df['POS (Parts of Speech)'] == 'Noun']
print(f"Total Nouns: {len(nouns)}")

```

### 4. Citation

When using this dataset for research or academic purposes, please ensure you cite the original sources listed in the "Source" column of the dataset, as well as acknowledging the compilation work done by the group members listed in Section A.