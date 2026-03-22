# Project Title : Quora Question Classification using Deep Learning

## 📌 Project Overview
This project focuses on building a **Deep Learning model** to classify Quora questions as **sincere (0)** or **insincere/toxic (1)** using Natural Language Processing (NLP) techniques.

The goal is to automatically detect harmful or misleading questions to improve content quality on platforms like Quora.
## 📊 Dataset
- Source: Quora Insincere Questions Classification Dataset
- Total training samples: ~1.3 million
- Features:
  - `question_text` → Input text
  - `target` → Label (0 = sincere, 1 = insincere)
 
## 🚀 Notebook
👉 Google Colab: (https://colab.research.google.com/drive/1t2cDY7zbhAJSecsT6Oi6TNpEHuGgJII5?authuser=1#scrollTo=Kf5lSC9_dTL8)

## ⚙️ Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn
- PyTorch
- NLTK (for text preprocessing)
- Matplotlib (for visualization)
- 
## 🔍 Data Preprocessing
- Tokenization using NLTK
- Stopword removal
- Stemming using Snowball Stemmer
- TF-IDF Vectorization (max_features = 1000)

## 🧠 Model Architecture
A fully connected neural network built using PyTorch:

- Input Layer → 1000 features (TF-IDF)
- Hidden Layers:
  - 512 neurons
  - 256 neurons
  - 128 neurons
- Output Layer → 1 neuron (Binary Classification)

Activation: ReLU  
Output: Sigmoid

## 🚀 Training Details
- Loss Function: Binary Cross Entropy (with class weighting)
- Optimizer: Adam
- Batch Size: 128
- Epochs: 5

## 📈 Model Performance
- Accuracy: ~94.4%
- F1 Score: ~0.41

## 📊 Visualizations
- Loss vs Epochs
- Accuracy vs Epochs
- F1 Score vs Epochs

(Plots included in notebook)

## 🔮 Predictions
Example:

```python
predict_text("Why can't liberals realize that they're stupid?")
# Output: 1 (Insincere)
