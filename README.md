# Machine-learning-Language-Translator-

#  Machine Translation with Seq2Seq LSTM using Keras

This project demonstrates a **Machine Translation (MT)** system using an **Encoder-Decoder architecture** built with **Keras** and **LSTM layers**. It translates sentences from one language to another using **sequence-to-sequence learning**.

## 📚 Overview

The project includes the full pipeline:
- Vectorization of input/output sentences
- Training a Seq2Seq model using LSTM layers
- Implementing separate encoder and decoder models for inference


---

## 🎯 Key Concepts Covered

### 🧾 Vectorization

Before training, all sentences are converted into **one-hot encoded NumPy arrays**:

- `encoder_input_data`: One-hot vectorized English sentences (input to encoder)
- `decoder_input_data`: One-hot vectorized French sentences (input to decoder)
- `decoder_target_data`: Same as `decoder_input_data`, but **offset by one timestep**, so the model learns to predict the next character.

### 🧠 Model Training

A **Seq2Seq model** using **LSTM layers** is trained using a technique called **teacher forcing**.  
- It learns to predict the target sequence based on the encoder and decoder inputs.
- Loss is calculated by comparing `decoder_target_data` with predictions.

### 🔁 Decoding / Inference

Once trained:
- We define **two separate models**:
  - **Encoder model**: Produces context states from the input sentence.
  - **Decoder model**: Uses those states to predict one token at a time.


## 📚 Key Reference

*Sequence to Sequence Learning with Neural Networks*  
Ilya Sutskever, Oriol Vinyals & Quoc V. Le (2014)  
Introduced the foundational encoder–decoder architecture using LSTM networks for mapping variable-length input to output sequences—with minimal assumptions about sequence structure. Achieved a BLEU score of about 34.8 on WMT‑14 English→French translation, surpassing strong SMT baselines, and improved further to ~36.5 via reranking. Reversing the order of source sentences significantly boosted performance 1.  
[View on arXiv](https://arxiv.org/abs/1409.3215)






![Alt Text](IMG20250803171654.jpg)
