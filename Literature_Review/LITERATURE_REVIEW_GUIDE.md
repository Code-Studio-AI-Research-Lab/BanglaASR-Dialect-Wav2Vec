# 🎙️ Onboarding Guide: Literature Review Workflow for Bangla Dialect ASR

Welcome to the **Code Studio AI Research Lab**. This guide establishes the mandatory workflow for conducting the Literature Review for our project: **"BanglaASR-Dial: Automatic Speech Recognition for Regional Bangla Dialects Using Wav2Vec 2.0 Fine-Tuning"**.

---

## 🔍 1. Where to Find High-Impact Papers
Speech processing is a specialized field. Focus your searches entirely on these elite AI, Speech, and NLP venues:
* **Top Speech Conferences:** **Interspeech**, **ICASSP** (IEEE International Conference on Acoustics, Speech and Signal Processing).
* **Top NLP Venues:** **ACL**, **EMNLP**, **EACL**.
* **Open Repositories:** Google Scholar and arXiv (Look under `cs.SD` - Sound/Audio and `cs.CL` - Computation and Language).

---

## 🛠️ 2. Search Strategy & Keywords
Do not search blindly. Use precise scientific strings:
* **Query 1:** `"Automatic Speech Recognition" AND "Wav2Vec 2.0" AND "Dialect"`
* **Query 2:** `"Bangla ASR" OR "Bengali Speech to Text" AND "Low-resource"`
* **Query 3:** `"Connectionist Temporal Classification" AND "Speech" AND "Cross-lingual transfer"`

---

## 📖 3. How to Read & Critically Evaluate an ASR Paper
1. **Analyze the Dataset:** Where did they get the audio? How many hours of speech did they have? Is it clean studio audio or noisy crowdsourced phone recordings?
2. **Examine the Baseline Model:** Did they train a model from scratch or did they fine-tune a pre-trained foundational model (like Wav2Vec2-Large, XLS-R, or Whisper)?
3. **The Dialectal Flaw:** Check their **Limitations**. Did they bundle all regional speakers into one bucket, or did they design specific tokens for different dialects? *Our edge is dialect-specific fine-tuning.*

---

## 📂 4. GitHub Directory Management Rules
```text
BanglaASR-Dialect-Wav2Vec/
└── Literature_Review/
    ├── PDFs/                 # Store paper PDFs (Format: FirstAuthor_Year.pdf, e.g., Islam_2024.pdf)
    ├── BibTeX/               # Append raw BibTeX blocks to `citations.bib`
    └── Research_Matrix.md    # Update the markdown matrix table
