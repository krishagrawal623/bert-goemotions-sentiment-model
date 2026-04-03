# 🧠 Emotion2Sentiment BERT Model

A sentiment analysis model built using **BERT (bert-base-uncased)** and fine-tuned on the **GoEmotions dataset**.  
This project converts 27 emotion labels into **3 simple sentiment classes**:

👉 Positive 😊 | Negative 😡 | Neutral 😐

---

## 🚀 Overview

Understanding human emotions in text is complex. The GoEmotions dataset provides 27 fine-grained emotion labels, but in real-world applications, simpler sentiment categories are often more useful.

This project simplifies emotion detection into **Positive, Negative, and Neutral sentiment classification**, making it more practical for applications like chatbots, feedback analysis, and social media monitoring.

---

## 📊 Dataset

- **GoEmotions Dataset (Google Research)**
- ~58k Reddit comments
- Original labels: 27 emotions + neutral

### 🔄 Label Mapping

- **Positive** → joy, love, excitement, gratitude, etc.  
- **Negative** → anger, sadness, fear, disgust, etc.  
- **Neutral** → neutral statements  

---

## ⚙️ Model Details

- **Model:** bert-base-uncased  
- **Architecture:** Transformer (BERT)  
- **Framework:** Hugging Face Transformers + PyTorch  
- **Task:** Text Classification  
- **Classes:** 3 (Positive, Negative, Neutral)

---

## 🧠 Methodology

1. Load GoEmotions dataset  
2. Map 27 emotions → 3 sentiment classes  
3. Preprocess text (cleaning + tokenization)  
4. Fine-tune BERT model  
5. Evaluate using accuracy and F1-score  

---

## 📈 Results

- Accuracy: ~90% *(update with your result)*  
- F1 Score: ~0.85  

---

## ▶️ Usage

```python
from transformers import pipeline

classifier = pipeline("text-classification", model="your-username/emotion2sentiment-bert")

result = classifier("This is the best day ever!")
print(result)
