# Kankanaey Lexicon and Machine Translation Model

## Group Members

- **DELA CRUZ,** Christpaul George B.
- **DORIA,** Realinda S.
- **LAPUS,** Christine Angela A.
- **PALANGDAN,** Joanalyn Mae S.
- **TI,** Kailey L.
- **YU,** Oliver T.

## About the Lexicon

The Kankanaey Lexicon is a structured collection of Kankanaey words and phrases with their English translations, example sentences, and linguistic annotations. It provides a foundation for understanding and working with the Kankanaey language. The lexicon is saved in the Kankanaey.csv file.

### Metadata

- **Total Entries**: 2,880 words/phrases
- **Entries with Sentence Pairs**: 661 (used for training translation models)
- **Language**: Kankanaey (Northern Luzon, Philippines)
- **Target Language**: English
- **Format**: CSV (Comma-Separated Values)
- **Encoding**: UTF-8

## KankanaeyLexicon.csv Fields

The lexicon CSV file contains the following fields:

1. **Word**
2. **English Translation / Meaning**
3. **Sentence / Phrase (Kankanaey)**
4. **Sentence / Phrase (English)**
5. **POS**

### Lexicon Field Descriptions

- **Word**: The Kankanaey word or phrase entry. This is the primary lexical item being documented.
- **English Translation / Meaning**: The direct English translation or meaning of the Kankanaey word.
- **Sentence / Phrase (Kankanaey)**: Example sentence or phrase in Kankanaey showing the word in context.
- **Sentence / Phrase (English)**: The corresponding English translation of the example sentence/phrase.
- **POS**: Part of Speech tag indicating the grammatical category through spaCy's universal POS tagging(e.g., NOUN, VERB, ADJ, ADV, PRON, SCONJ, etc.)

## How to Use the Lexicon

### Loading the Lexicon

To work with the lexicon, the CSV file can be loaded using any data processing tool that supports CSV format. Using Python with the Pandas library, the file can be loaded by specifying the filename `KankanaeyLexicon.csv`. Once loaded, the structure of the data can be viewed to see the column headers and first few entries.

### Searching / Filtering the Lexicon

The lexicon can be searched in multiple ways to find specific entries. A Kankanaey word can be searched by filtering entries where the "Word" column contains the search term (case-insensitive search is recommended). Similarly, the English meaning/translation can be searched by filtering the "English Translation / Meaning" column. For example, searching for "anap" will find entries containing that Kankanaey word, while searching for "find" in the English column will return entries with that English meaning. Entries can also be filtered through the part of speech by matching the "POS" field to specific tags like "VERB", "NOUN", "ADJ", etc. This allows the creation of subsets of the lexicon focused on particular grammatical categories. Additionally, filtered subsets of the lexicon can be exported to separate CSV files for specialized use cases, such as creating a nouns-only lexicon or a lexicon containing only entries with sample sentences.

## Additional Resources: Translation Model

### About the Translation Model

A neural machine translation model was trained using this lexicon to provide automated Kankanaey-to-English translation. The model is based on Facebook's NLLB-200-distilled-600M and was fine-tuned on the sentence pairs from this lexicon.

**Model Metadata:**

- **Model Base**: `facebook/nllb-200-distilled-600M`
- **Surrogate Source Language**: `ilo_Latn` (Ilocano Latin script, used as surrogate for Kankanaey)
- **Target Language**: `eng_Latn` (English)
- **Training Data**: 661 sentence pairs from this lexicon
- **Training Split**:
  - Training: 528 samples (80%)
  - Validation: 66 samples (10%)
  - Test: 67 samples (10%)
- **Model Performance**:
  - Test BLEU Score: 34.83
  - Test chrF Score: 46.03
- **Link to Drive**:
  -https://drive.google.com/drive/folders/1vVTKh3dnsyxMtAsHEKqKhPILJZNUXIXL?usp=sharing

### Using the Translation Model

The trained model is under `/nllb_kke_model` directory in the Google Drive link provided. To use the model, both the tokenizer and the model is loaded using the Hugging Face Transformers library. The tokenizer handles the conversion of text into tokens that the model can process, while the model performs the actual translation.

To translate Kankanaey text to English, the input text is first tokenized, setting appropriate parameters for maximum length and padding. The model then generates the translation using beam search with configurable parameters such as maximum output length and number of beams. The generated tokens are decoded back into readable English text. For example, when translating the Kankanaey word "anap", the model processes it through tokenization, generation, and decoding to produce the English translation, "find".

## Google Colab Usage (for Translation Model)

### Setup

To use the translation model in Google Colab:

1. Mount your Google Drive to access the saved model files when opting to use Google drive directly. This allows Colab to access files stored in the Drive.
2. Install the required packages including the Transformers library, datasets, accelerate, sentencepiece, sacrebleu, and evaluate. These packages provide the necessary functionality for loading and using the model.
3. Verify that Colab runtime is set to use a GPU by going to Runtime → Change runtime type and selecting GPU (T4 or better is recommended), as normal runtime may not be able to handle the process. The notebook can automatically detect and use the GPU if available, which significantly speeds up model inference.

### Running Inference from the Notebook (Sample Google Colab Script)

The training notebook (`Kankanaey-EnglishTranslation.ipynb`) contains a ready-to-use inference example for the translation model. This script demonstrates how to load the model and tokenizer from the specific Google Drive path where the trained model is stored. It includes a translation function that handles the complete process from tokenization through generation to decoding. The example shows how to translate a Kankanaey word like "anap" and display both the input and the model's translation output. This section serves as a practical reference for using the trained model for inference tasks.

## Translation Model Training Details

### Training Process

The model was trained using:

- **Framework**: Hugging Face Transformers
- **Training Strategy**: Fine-tuning with early stopping
- **Evaluation Metrics**: BLEU and chrF scores
- **Optimization**: AdamW optimizer with learning rate 3e-5
- **Regularization**: Weight decay 0.01

### Key Training Parameters

- **Batch Size**: 4 per device
- **Gradient Accumulation**: 1 step
- **Learning Rate**: 3e-5
- **Max Epochs**: 15
- **Early Stopping Patience**: 3 epochs
- **Evaluation Strategy**: After each epoch
- **Best Model Selection**: Based on BLEU score

### Performance Metrics

- **Test BLEU**: 34.83 - The BLEU (Bilingual Evaluation Understudy) score indicates good translation quality and the model is considered to have strong performance.
- **Test chrF**: 46.03 - The chrF (character F-score) indicates high character-level similarity between the predicted texts and the reference texts.
- **Test Loss**: 0.187 - the low test loss indicates good generalization, corresponding to higher confidence for the translations.

## Lexicon Notes

1. **Data Quality**: The lexicon contains 2,880 entries, with 661 entries having complete sentence pairs. Some entries may have missing fields (e.g., missing example sentences).

2. **Part of Speech Tags**: The POS field uses standard linguistic abbreviations (NOUN, VERB, ADJ, ADV, etc.) utilizing spaCy's universal POS tagging. Some entries may have empty or missing POS tags.

3. **Language Coverage**: The lexicon focuses on common Kankanaey words and phrases with their English translations and example usage. The Lexicon did not consider the different Kankanaey dialects in different areas of the community.

4. **Usage**: The lexicon can be used for:
   - Language learning and reference
   - Computational linguistics research
   - Building translation systems
   - Creating language learning applications
   - Linguistic analysis and documentation

## Translation Model Limitations

_Note: These limitations apply to the translation model, not the lexicon itself._

1. **Surrogate Language**: The model uses Ilocano (`ilo_Latn`) as a surrogate source language since Kankanaey is not directly supported by NLLB-200. This is a common approach for low-resource languages.

2. **Dataset Size**: The training dataset is relatively small (661 sentence pairs), which may limit the model's generalization capabilities.

3. **Domain**: The model is trained on lexicon data, which may perform better on vocabulary and short phrases rather than long, complex sentences.

4. **GPU Memory**: If you encounter out-of-memory errors when using the model:

   - Reduce `per_device_train_batch_size`
   - Increase `gradient_accumulation_steps`
   - Use `torch.float16` for model loading

5. **Model Memory Size**: The trained model is relatively large and requires substantial memory resources, which limits its deployment on resource-constrained systems.

## File Structure

The project contains several key files and directories. The main resource is the `KankanaeyLexicon.csv` file, which contains the complete lexicon dataset. The `README.md` file provides documentation and usage instructions. Additionally, there is a trained translation model which can be accessed through the link provided, which contains model configuration files (config.json), the model weights (pytorch_model.bin), tokenizer configuration (tokenizer_config.json), and other supporting files. A Google Colab script is also provided for reference when to use the trained model.

```
.
├── README.md
├── KankanaeyLexicon.csv          # The main lexicon dataset (PRIMARY RESOURCE)
└── Kankanaey-EnglishTranslation.ipnyb 
```

## Dependencies

### For Using the Lexicon

- **Python 3.8+** (for data processing)
- **Pandas** (for CSV manipulation and analysis)

### For Using the Translation Model (Optional)

- Python 3.8+
- PyTorch
- Transformers 4.57.2+
- Datasets 4.0.0+
- NumPy
- scikit-learn
- evaluate
- sacrebleu

## Acknowledgments

- **Primary**: The Kankanaey language community and contributors who helped compile this lexicon
- **Translation Model**: Facebook AI Research for the NLLB-200 model
- **Translation Model**: Hugging Face for the Transformers library
- Saint Louis University
