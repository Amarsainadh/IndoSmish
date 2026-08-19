# Smishing Detection Beyond English Benchmarks

A research-oriented study on **SMS phishing (smishing) detection beyond traditional English benchmarks**, focusing on code-mixed and Romanized Indic languages, dataset leakage, language models, adversarial robustness, and resource-efficient on-device inference.

## Overview

Smishing is a form of phishing delivered through SMS, where attackers use deceptive messages to encourage users to click malicious links, reveal credentials, make payments, call numbers, or perform other unsafe actions.

Most existing SMS detection research relies heavily on older English benchmarks. This creates a gap between benchmark performance and real-world deployment scenarios, particularly for Indian-language communication where messages may combine English with Indic languages and frequently use Romanized scripts.

This project investigates that gap by connecting four major research areas:

- SMS spam and smishing detection
- Code-mixed and low-resource Indic NLP
- Language-model-based threat detection
- Resource-efficient and on-device inference

The study is designed to understand how these areas can be combined into a reliable benchmark for future Indian-language smishing detection.

---

## Key Research Questions

The study investigates five major questions:

1. How have SMS spam and smishing detection methods evolved from rule-based systems to modern language models?
2. What evidence exists for code-mixed, Romanized, and low-resource Indic text?
3. How can language models be compressed for privacy-sensitive on-device inference?
4. Which datasets and evaluation protocols provide reliable comparisons?
5. What components are required for a deployable code-mixed Indian-language smishing detector?

---

## Research Framework

The project organizes existing research into four evidence areas:

### 1. SMS / Smishing Detection

Covers:

- Rule-based detection
- Classical machine learning
- Deep learning
- Transformer / PLM-based detection
- Hybrid content + URL analysis
- LLM-based detection

### 2. Code-Mixed Indic NLP

Focuses on:

- Romanized Indic text
- Code-switching
- Transliteration
- Language identification
- Indic language encoders
- MuRIL
- IndicBERT
- XLM-R

### 3. LLM-Based Threat Detection

Investigates:

- Zero-shot classification
- Few-shot prompting
- Fine-tuned language models
- Small language models
- Parameter-efficient fine-tuning
- LoRA / QLoRA
- Explainable LLM-based detection

### 4. Resource-Efficient On-Device AI

Explores:

- Model compression
- Quantization
- Knowledge distillation
- Parameter-efficient adaptation
- Mobile inference
- Latency
- Memory usage
- Energy consumption

---

## Literature Review

The review contains an evidence base of **169 records** and an eligibility-filtered comparison set of **48 direct SMS detector studies**.

The 48 direct studies are categorized as:

- 18 Classical ML
- 13 Deep Learning
- 9 Pre-trained Language Models
- 8 Decoder-based LLM approaches

The review deliberately separates direct SMS evidence from transfer and contextual evidence instead of combining results from different tasks and datasets. 

---

## Dataset and Leakage Analysis

A major focus of the project is understanding how dataset reuse and near-duplicate messages can produce overly optimistic evaluation results.

### English Dataset

The preliminary validation starts with:

- 5,971 English rows
- 5,797 independent-label records after conflict quarantine and exact deduplication

### Bangla Dataset

The validation includes:

- 2,772 Bangla rows
- 1,204 records after cleaning and deduplication

The evaluation uses five fixed random seeds and compares naive row-level splitting against group-aware splitting based on near-duplicate components.

---

## Evaluation Methodology

The preliminary validation uses:

### Models

- Word-level TF-IDF + Linear SVM
- Character-level TF-IDF + Linear SVM

### Splitting

- 70% Training
- 15% Validation
- 15% Testing

Five fixed seeds are used:

13
29
47
71
97
