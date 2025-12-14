# LexiLoko: Constructing an Electronic Iloko Lexicon from Phased-out DepEd-Pangasinan Mother Tongue-Based Learning Resources for Neural Machine Translation

In today’s digital world, many minority languages face marginalization as global communication 
increasingly favors international languages. The absence of linguistic resources for these languages 
hinders their preservation and representation online. Although Iloko is among the most spoken languages
in the Philippines, it lacks structured corpora to support Natural Language Processing (NLP) and Neural
Machine Translation (NMT) development. This study presents LexiLoko, an electronic Iloko lexicon
constructed by repurposing phased-out Iloko Mother Tongue-Based Multilingual Education (MTB-MLE)
modules from Pangasinan. The lexicon offers a scalable, machine-readable resource documenting Iloko 
words and sentences paired with English equivalents, forming the basis for a parallel corpus. Findings
show that LexiLoko mitigates corpus scarcity and high out-of-vocabulary rates while providing a 
comprehensive digital repository. The study concludes that reusing discontinued educational materials is 
an effective approach to fostering inclusivity, supporting e-governance, and preserving the Iloko language 
in the digital age.

## Authors:
* Stephen M. Coloma
* Sanchie Earl M. Guzman
* Leonhard T. Leung
* Marius Glenn M. Nonato
* Hannah T. Ragudos
* Jerwin Kyle R. Ramos

## Dataset
The LexiLoko dataset is composed of two primary resources: a **lexicon** and a **parallel corpus**, both
derived from phased-out Iloko MTB-MLE learning modules. These resources are designed to support linguistic
analysis and computational applications, particularly in **Natural Language Processing (NLP)** and
**Neural Machine Translation (NMT)** for the Iloko language.

### Lexicon
The lexicon consists of **4,065 Iloko lexical entries**, each paired with its corresponding **English equivalent**.
Entries include commonly used vocabulary extracted from educational texts and represent a range of everyday language use.
This component serves as a foundational bilingual reference and may be utilized for tasks such as vocabulary lookup,
lexical alignment, and lexicon-based NMT enhancement.

### Parallel Corpus
The parallel corpus contains **1,833 aligned Iloko-English sentence pairs**. These sentence-level translations
provide contextualized language data suitable for training, evaluating, and fine-tuning machine translation models. The corpus
also supports other NLP tasks such as sentence alignment, syntactic analysis, and semantic modeling.

### Dataset Summary

| Component       | Description                                | Entries | Language Pair | Intended Use                        |
| --------------- | ------------------------------------------ | ------- | ------------- | ----------------------------------- |
| Lexicon         | Word-level Iloko–English lexical mappings  | 4,065   | Ilo–En        | Vocabulary lookup, NLP, NMT support |
| Parallel Corpus | Sentence-level Iloko–English aligned pairs | 1,833   | Ilo–En        | NMT training, evaluation, alignment |


## Technical Specifications
This section outlines the structure and format of the dataset files included in the repository

### Lexicon
| Field                 | Description / Value                                 |
| --------------------- | --------------------------------------------------- |
| Dataset Type          | Bilingual Lexicon                                   |
| Source                | Phased-out Iloko MTB-MLE modules (DepEd Pangasinan) |
| Number of Entries     | 4,065                                               |
| Unit of Annotation    | Word / Lexical item                                 |
| Language              | Iloko                                               |
| Target Language       | English                                             |
| Format                | *CSV*                                               |
| Encoding              | *UTF-8*                                             |
| Intended Applications | NLP, NMT, dictionary systems                        |
| Annotation Method     | Manual extraction and organization                  |

### Parallel Corpus
| Field                    | Description / Value                                 |
| ------------------------ | --------------------------------------------------- |
| Dataset Type             | Parallel Corpus                                     |
| Source                   | Phased-out Iloko MTB-MLE modules (DepEd Pangasinan) |
| Number of Sentence Pairs | 1,833                                               |
| Unit of Annotation       | Sentence                                            |
| Language Pair            | Iloko–English                                       |
| Alignment Level          | Sentence-level                                      |
| Format                   | *CSV*                                               |
| Encoding                 | *UTF-8*                                             |
| Intended Applications    | NMT, NLP experiments, alignment tasks               |
| Annotation Method        | Manual translation alignment                        |

## How to use
### 1. Accessing the Files
* Clone or download the repository
  
``` console
git clone https://github.com/SLU-INTEGRATED-CONFEDERACY/SLU-CIS-NLP.git
```
       
* Locate the dataset files in the corresponding folders:
  * `SLU-CIS-NLP/Iloko - Coloma et al/iloko_lexicon.csv`
  * `SLU-CIS-NLP/Iloko - Coloma et al/iloko_parallel.csv`

### 2. Using the Lexicon
* The lexicon can be loaded in Python using **pandas**:

``` python
import pandas as pd

lexicon = pd.read_csv("iloko_lexicon.csv")
print(lexicon.head())
```

### 3. Using the Parallel Corpus
* Load the parallel corpus for NLP or machine translation experiments:

``` python
import pandas as pd

corpus = pd.read_csv("iloko_parallel.csv")
print(lexicon.head())
```

## Recommendations for Future Use
Future researchers are encouraged to expand the lexicon by incorporating additional
sources such as **songs**, **stories**, **fables**, and **legends** to capture a wider
range of Iloko language use. LexiLoko may also be utilized in developing NLP applications,
including **bilingual dictionary tools**, **spell and grammar checkers**, **educational platforms**,
**chatbots**, and **voice-enabled assistants**.
