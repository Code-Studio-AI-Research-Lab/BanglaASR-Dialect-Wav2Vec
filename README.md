# BanglaASR-Dial: Automatic Speech Recognition for Regional Bangla Dialects Using Wav2Vec 2.0 Fine-Tuning

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Framework: PyTorch](https://img.shields.io/badge/Framework-PyTorch-orange.svg)](https://pytorch.org/)
[![Model: Wav2Vec 2.0](https://img.shields.io/badge/Model-Wav2Vec%202.0-blue.svg)](https://huggingface.co/meta-llama)
[![Domain: Speech & NLP](https://img.shields.io/badge/Domain-Speech%20%26%20NLP-green.svg)]()

This repository hosts the official research and implementation of **BanglaASR-Dial**, an Automatic Speech Recognition (ASR) framework optimized specifically for regional Bangla dialects (e.g., Chittagonian, Sylheti, Noakhailla, etc.). By leveraging and fine-tuning Meta's self-supervised **Wav2Vec 2.0** architecture, this project addresses the steep challenge of transcribing highly diverse, phonetically complex, and low-resource regional spoken dialects into standardized written Bangla text.

---

## 📌 Research Vision & Core Concept
While standard Bangla ASR models perform adequately on formal speech (such as news broadcasts), they fail drastically when exposed to regional dialects due to vocabulary shifts, phonetic mutations, and lack of annotated speech corpora. 
* **Self-Supervised Pre-training:** Utilizing raw audio wave representations learned by foundational Wav2Vec 2.0 architectures.
* **Dialectal Fine-Tuning:** Fine-tuning the acoustic model using Connectionist Temporal Classification (CTC) loss over a curated dataset of regional Bangla dialects.
* **Language Model Integration:** Post-processing raw acoustic outputs with an n-gram or neural Bangla language model to maximize grammatical and context-aware accuracy.



---

## 🛠️ Key Features & Methodology
1. **Audio Audio-Augmentation Pipeline:** Built-in scripts for noise injection, pitch shifting, and speed perturbation to handle diverse real-world recording conditions.
2. **CTC Loss Optimization:** Fine-tuning transformer layers using Hugging Face's `Trainer` API optimized for CTC decoding.
3. **Robust Metrics Evaluation:** Evaluates transcription quality using standard **Word Error Rate (WER)** and **Character Error Rate (CER)** across separate dialect clusters.
4. **Hugging Face Hub Integration:** Ready-to-export configurations to deploy fine-tuned checkpoints seamlessly onto the Hugging Face Hub.

---

## 📂 Repository Structure
```text
├── src/
│   ├── audio_processing/   # Audio cleaning, resampling (16kHz), and augmentation scripts
│   ├── models/             # Wav2Vec2ForCTC configuration and fine-tuning wrappers
│   ├── decoding/           # CTC Beam Search decoders and Language Model (LM) integrations
│   └── evaluation/         # Word Error Rate (WER) and Character Error Rate (CER) evaluators
├── data/                   # Manifest file generators and dataset split maps (Train/Val/Test)
├── configs/                # Hyperparameters for learning rate, batch size, and freeze-layers
├── notebooks/              # Spectrogram visualizations and error analysis
├── Literature_Review/      # Team research matrices and BibTeX reference files
└── README.md
