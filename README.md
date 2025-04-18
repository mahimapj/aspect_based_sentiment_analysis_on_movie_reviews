# Aspect-Based Sentiment Analysis (ABSA) on IMDB Movie Reviews
This project implements a fast and optimized Aspect-Based Sentiment Analysis (ABSA) system for movie reviews using Natural Language Processing (NLP) techniques. It analyzes specific aspects of a movie (like acting, direction, etc.) from user reviews and classifies the sentiment for each using BERT, a transformer-based language model, and a user-friendly Gradio interface.

# About this Project
🔹 1. Text Preprocessing & Tokenization - using BERT Tokenizer
🔹 2. Aspect Extraction - using NLP methods like dependency parsing and named entity recognition (NER).
🔹 3. Multi-Label Sentiment Classification - using pretrained  BERT(Bidirectional Encoder Representations from Transformers)
🔹 4. Sentiment Scoring - Sigmoid activation converts raw logits from BERT into probabilities per aspect which in turn are interpreted as confidence scores for each sentiment prediction.

 # Features
  - Multi-aspect sentiment detection (acting, dialogues, storyline, etc.)
  - Built with advanced transformer-based NLP models (BERT)
  - Fast training on a subset of IMDB data
  - Confidence-based visualization using Matplotlib
  - Gradio interface for real-time user interaction

# Installation
<pre> ##  ```bash pip install transformers[torch] gradio pandas matplotlib --quiet ``` </pre>

* Dataset - Uses a sample of 2,000 reviews from the IMDB Movie Review Dataset .
Each review is annotated with binary indicators for aspects based on keyword presence.

* Training Parameters
Parameter	Value
Model	BERT-base
Max Sequence Len	128
Batch Size	16
Epochs	2
Learning Rate	4e-5
Loss Type	Multi-label Binary CrossEntropy
Mixed Precision	✅ Enabled with AMP

## 🔍 Run the Project

You can run the full project in **Google Colab** or **locally** (preferably with GPU).  
The interface will launch a Gradio app:

```python
iface.launch()
```

# Project Structure

```bash
├── absa_fast.py           # Main Python script
├── IMDB Dataset.csv       # Dataset sample
├── temp_plot.png          # Visualization output
├── README.md              # Project documentation
```

- Accepts a free-text review from the user
- Returns aspect sentiment breakdown
- Displays a bar graph for visual feedback
  
# Language
Python

# License
MIT License

# Acknowledgements
* Huggingface Transformers
* Gradio
* PyTorch
* IMDB Sentiment Dataset
