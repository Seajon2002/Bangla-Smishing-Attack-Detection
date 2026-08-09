# Bangla Smishing Attack Detection Using a Hybrid Deep Learning Model

A hybrid deep learning-based system for detecting **smishing (SMS phishing) attacks** in Bangla SMS messages. The proposed model combines transformer-based language representations with handcrafted text and URL-based security features to classify messages as **Spam (Smishing)** or **Ham (Legitimate)**.

---

## 📌 Project Overview

Smishing is a form of phishing that uses SMS messages to deceive users into revealing sensitive information, clicking malicious links, or interacting with fraudulent content.

This research proposes a hybrid deep learning architecture that combines:

- **XLM-RoBERTa** for multilingual contextual representation
- **BanglaBERT** for Bangla-specific language representation
- **Attention Pooling** for extracting important contextual information
- **Text-based meta features**
- **URL-based phishing features**
- **Feature Fusion**
- **Deep Neural Classifier**

The final system performs binary classification:

- **Spam** → Smishing / phishing-related SMS
- **Ham** → Legitimate SMS

---

## 🎯 Research Objective

The main objective of this research is to develop an effective deep learning-based approach for detecting smishing attacks in Bangla SMS messages.

The system aims to:

1. Detect suspicious SMS messages automatically.
2. Capture contextual information from Bangla and multilingual text.
3. Identify phishing-related URL characteristics.
4. Combine semantic and handcrafted security features.
5. Improve the detection performance of traditional SMS classification approaches.

---

## 🧠 Proposed Hybrid Architecture

The proposed architecture consists of three major feature-processing branches.

```text
                         SMS Input
                            │
                    Text Cleaning
                            │
          ┌─────────────────┼─────────────────┐
          │                 │                 │
          ▼                 ▼                 ▼
     XLM-RoBERTa         BanglaBERT       Meta Feature
          │                 │              Extraction
          ▼                 ▼                 │
   Attention Pooling  Attention Pooling    │
          │                 │                 │
          └────────────┬────┴─────────────────┘
                       ▼
                 Feature Fusion
                       │
                       ▼
              Deep Neural Classifier
                       │
                       ▼
                Spam / Ham Prediction
