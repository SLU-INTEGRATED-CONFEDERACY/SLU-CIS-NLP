# Ibaloi NLP Lexicon System: Preserving Ibaloi through Natural Language Processing and LLM

**A digital platform designed to support the preservation, study, and modernization of the Ibaloi language through Natural Language Processing (NLP).**

## 🔗 Quick Links
* **Live Website:** [https://ibaloinlp.vercel.app/](https://ibaloinlp.vercel.app/)
* **Repository:** [https://github.com/nlp-mors3/Morse_RASA](https://github.com/nlp-mors3/Morse_RASA)
* **Paper:** [https://ibaloinlp.vercel.app/research-paper](https://github.com/nlp-mors3/Morse_RASA)


---

## 📖 About the Project

The Cordillera Administrative Region (CAR) is home to rich ethnolinguistic groups, yet languages like **Ibaloi** remain underrepresented in modern technological applications. While traditional dictionaries exist, they often lack the structure required for computational processing.

**The Ibaloi NLP Lexicon System** bridges this gap. It is an academic initiative designed to create a structured, machine-readable lexicon dataset compatible with NLP processes. The system aims to support future applications such as machine translation, chatbots, and digital cultural preservation.

![Web-agent IMG Preview](web-preview.png)

### Key Objectives
* **Construct a Digital Lexicon:** A structured database of Ibaloi vocabulary with English translations, POS tagging, and phonetic respelling.
* **Crowdsource Language Data:** Utilize a "Sentence Builder" to gather authentic sentence examples from the community.
* **Demonstrate NLP Capabilities:** Implement an **LLM-based** translation tool that combines lexicon matching with generative AI context injection.

---

## Key Features

### 1. Digital Lexicon
A searchable database containing over **1,500+ entries**. It serves as the core linguistic resource for the project.

![Lexicon IMG Preview](lexicon.png)

* **Structured Data:** Includes variants, simplified pronunciation (adapted from Google/Oxford conventions), part of speech (POS), and synonyms.
* **Search Interface:** Allows users to filter by Ibaloi word, English translation, or spelling variants.

### 2. Sentence Builder (Crowdsourcing Tool)
To address the scarcity of digital Ibaloi resources, we developed a custom data collection module.
* **Workflow:** Users select a "Main Word" provided by our API and construct an Ibaloi sentence around it, providing an English translation.
* **Backend:** Data is processed via a Node.js API and stored in a structured sheet for validation.

### 3. LLM Translator (Lexicon lookup + Generative AI Translation)
A demonstration of low-resource language modeling using a hybrid approach.
* **Lexicon Matching:** Identifies and highlights known terms from the database.
* **Context Injection:** Uses a Generative AI / LLM pipeline to infer context and generate sentence predictions even when exact matches are missing.
* **Bidirectional:** Supports both English-to-Ibaloi and Ibaloi-to-English translation.

### 4. Research Paper Viewer
An integrated document viewer that presents our full study, *"Constructing a Structured Ibaloi Lexicon through Digital Resource Collection,"* making the methodology accessible to all users.

---

## 🛠️ Technology Stack

* **Frontend:** Tailwind
* **Backend/API:** Flask, Google Scripts
* **NLP Framework:** Lexicon, Gemini 2.5 Open Source Framework
* **Deployment:** Vercel

---

## Message to Future Researchers & Contributors

To the students, developers, and linguists who may inherit or fork this repository:

**This project is a starting point, not a finish line.**
We created this system because we recognized that Ibaloi was falling behind in the digital age due to a lack of machine-readable datasets. We have laid the groundwork by scraping dictionaries, standardizing orthography, and building the initial collection infrastructure.

**Where you can take this next:**
1.  **Expand the Dataset:** The *Sentence Builder* is fully functional. Use it to launch wider community campaigns to gather more complex sentence structures. The more data you collect, the better the model becomes.
2.  **Refine the Model:** Our translaton model uses a hybrid approach. Future work could focus on fine-tuning specific Large Language Models (LLMs) specifically on the Ibaloi dataset we've started.
3.  **Audio Integration:** We structured the lexicon with pronunciation guides. A logical next step is integrating Text-to-Speech (TTS) or Speech-to-Text (STT) to support oral preservation.

Please treat the data with respect to the culture it represents. Ensure that any major changes to orthography align with the *DepEd Ibaloi Orthography* standards we followed.

*Agmapteng! (Padayon!)*

---

## 👥 The Team (NLP Team Mors3)

**Saint Louis University** - School of Computing and Information Sciences

![TEAM IMG Preview](team.png)

---

*© 2025 NLP Team Mors3. Saint Louis University. All rights reserved.*
