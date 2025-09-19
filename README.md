
# 🎮 Sentiment Analysis on Video Game Reviews

The goal of this project is to **build and train a deep learning model** that can accurately predict the sentiment of a video game review based on its text.

The workflow involves:

1. Creating a suitable dataset from raw Amazon review data.
2. Training a **Bidirectional LSTM** sentiment analysis model.

---

## 💾 Dataset

* Source: [Amazon "Video Games" 5-core dataset](https://nijianmo.github.io/amazon/index.html)
* Size: **497,000+ reviews** in JSON format.

Two CSV files are created from the raw dataset:

* **`small_corpus.csv`** → undersampled dataset for **quick testing & prototyping**.
* **`big_corpus.csv`** → larger, weighted corpus for **training the final model**.

📓 Notebook: `creating_dataset.ipynb`

* Handles raw JSON processing.
* Generates the CSV files for downstream tasks.

---

## 🤖 Model

The model is a **Bidirectional LSTM (Long Short-Term Memory)** network with the following architecture:

* **Embedding Layer**
* **2 × Bidirectional LSTM Layers**
* **Dropout Layers** (for regularization)
* **Dense Layers**
* **Final Dense Layer** → Softmax activation for **3 sentiment categories**

📊 **Performance**: Achieves **\~73.76% test accuracy**.

📓 Notebook: `Sentiment_Analysis.ipynb`

* Covers data preprocessing
* Model building & training
* Evaluation

---




