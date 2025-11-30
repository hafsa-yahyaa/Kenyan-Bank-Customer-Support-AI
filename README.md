# 🇰🇪 Localized AI: Kenyan Customer Support Classifier

A Natural Language Processing (NLP) project that fine-tunes a Large Language Model (DistilBERT) to understand Kenyan code-mixed text (Swahili, English, and Sheng).

## Project Overview
Global AI models often struggle with local context. If a user says *"Luku imeisha"* (Power tokens are finished), a standard US-trained model might confuse it for a general statement.

This project solves that by fine-tuning **DistilBERT** on a custom dataset of Kenyan customer support queries to classify them into actionable intents.

## Objectives
1.  **Create a Local Dataset:** Curated 100+ samples mixed with Swahili/Sheng.
2.  **Fine-Tune an LLM:** retrained `distilbert-base-uncased` for classification.
3.  **Demonstrate Local Adaptation:** Prove the model understands terms like *M-Pesa, Sambaza, and Bundles*.

## Project Structure
* `fine_tune_bert.ipynb`: The Google Colab notebook containing the training pipeline.
* `customer_support_data.csv`: The custom dataset with 4 categories of intent.
* `train_model.py`: Python script version of the training loop.

## Categories & Performance
The model classifies text into 4 categories:
* **Billing Issue** (e.g., "Tokens zangu hazija reflect")
* **Transaction Reversal** (e.g., "Wrong number, reverse please")
* **Network Issue** (e.g., "Netiko iko down")
* **General Inquiry** (e.g., "Mnafungua saa ngapi?")

**Results:**
* **Accuracy:** ~65% (on a small dataset of 100 samples)
* **Baseline Comparison:** significantly outperforms random guessing (25%)

## How to Run
1.  Open `fine_tune_bert.ipynb` in Google Colab.
2.  Upload `customer_support_data.csv` to the session storage.
3.  Run all cells to fine-tune the model.

## Author
**Hafsa Yahya Mohamud 169440**
*Bachelor of Science in Statistics and Data Science*