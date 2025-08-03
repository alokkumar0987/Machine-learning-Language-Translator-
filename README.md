# Machine-learning-Language-Translator-

# 🧠 Neural Machine Translation with Seq2Seq LSTM using Keras

This project demonstrates a **Neural Machine Translation (NMT)** system using an **Encoder-Decoder architecture** built with **Keras** and **LSTM layers**. It translates sentences from one language to another using **sequence-to-sequence learning**.

## 📚 Overview

The project includes the full pipeline:
- Vectorization of input/output sentences
- Training a Seq2Seq model using LSTM layers
- Implementing separate encoder and decoder models for inference
- Deploying the translation model using a **Streamlit web app**

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

This setup allows the model to **translate unseen sentences** at test time.

---

## 🚀 Streamlit Web App

A lightweight **Streamlit interface** is provided:
- Input a sentence
- Get the translated output in real-time

To run:

```bash
streamlit run streamlit_app.py
Neural-Machine-Translation---LSTM/NeuralMachineTranslator_French to English.ipynb at master · khatrideepti/Neural-Machine-Translation---LSTM https://share.google/ESNbaOew9W3yQH4uc
