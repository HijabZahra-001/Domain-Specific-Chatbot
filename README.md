#  Q&A Chatbot using TF-IDF + Cosine Similarity

A retrieval-based chatbot that answers domain-specific questions by finding the most relevant match from a predefined dataset.

---

##  Overview

This chatbot uses **TF-IDF Vectorization** and **Cosine Similarity** to match user queries with the most similar question in the dataset and returns the corresponding answer.

### Key Features
-  TF-IDF with n-grams (unigrams + bigrams)
-  Cosine Similarity for matching
-  Text preprocessing (cleaning, normalization)
-  Interactive chatbot loop
-  Multi-domain dataset (Tech, Health, Education, General)
-  Similarity threshold with fallback responses
-  Confidence scores for transparency
-  CSV dataset export

---

##  Quick Start

### Installation
```bash
pip install pandas scikit-learn numpy
```

### Run
```bash
python chatbot.py
```

### Usage
- Type your question and get the best matching answer
- Type `exit` or `quit` to end
- Type `info` to see available topics

### Example
```
You: what is AI
Bot: AI (Artificial Intelligence) is the simulation of human intelligence 
     in machines. (Confidence: 92.45%)

You: how to reduce stress
Bot: Reduce stress through exercise, meditation, and mindfulness. 
     (Confidence: 88.32%)

You: explain Python
Bot: Python is a high-level programming language used in AI and data science. 
     (Confidence: 94.78%)
```

---

##  Dataset

Contains **40+ Q&A pairs** across 4 domains:
- **Technology**: AI, ML, Python, Data Science, NLP
- **Health**: Diet, Stress, Exercise, Sleep, Meditation
- **Education**: Study tips, Critical thinking, Leadership
- **General**: Geography, Science, Environment, History

---

##  How It Works

1. **Preprocess** text (lowercase, remove special characters)
2. **Vectorize** using TF-IDF with n-grams
3. **Calculate** cosine similarity with all questions
4. **Return** answer if confidence ≥ threshold (0.2)
5. **Suggest** alternatives if confidence is too low

---

##  Important Limitations

-  **Does NOT generate** new answers - only retrieves from dataset
-  **Cannot handle** questions outside the dataset
-  **No conversation memory** - each query is independent
-  **No learning capability** - static dataset only

---

##  Files

```
QA_Chatbot/
├── chatbot.py          # Main application (single file)
├── qa_dataset.csv      # Auto-generated dataset
└── README.md           # This file
```

---

## Technologies

- Python 3.7+
- pandas
- scikit-learn (TF-IDF, Cosine Similarity)
- NumPy
- re (regex)

---

##  Use Cases

-  FAQ systems for websites
-  Customer support automation
-  Educational tutoring
-  Knowledge base search

---

##  License

MIT License

---

##  Author
Hijab Zahra

---

## Future Improvements

- Add web interface (Streamlit)
- Support larger datasets
- Add fuzzy matching
- Implement sentence transformers
