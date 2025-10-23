# Generative AI Triage Demo

**Automated Text Categorization, Summarization, and Routing using Generative AI**

This project simulates an intelligent triage system for text-based public requests. It automatically classifies, summarizes, and routes incoming text using transformer-based language models running on GPU.

---

## Project Overview

This notebook demonstrates how Generative AI can be applied to automate the intake and processing of text-based requests, similar to a public record or helpdesk system.

It performs the following tasks:

1. **Categorization:** Predicts which category or department a request belongs to using zero-shot classification.  
2. **Summarization:** Condenses long text inputs into short, meaningful summaries.  
3. **Routing:** Uses classification confidence scores to suggest the appropriate routing destination.

The system is implemented using Hugging Face transformer models and runs efficiently on GPU.

---

## Models Used

- **Text Classification:** `facebook/bart-large-mnli`  
  Utilized for zero-shot text classification based on natural language inference (NLI).

- **Summarization:** `sshleifer/distilbart-cnn-12-6`  
  Used for abstractive summarization of long text inputs into concise summaries.

---

## Dataset

The project uses the **20 Newsgroups dataset** as a stand-in for real-world public request data.  
Each text entry represents a user query or request, which is then automatically categorized and summarized.

---

## Environment Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/ManishKanuri/generative-ai-triage.git
   cd generative-ai-triage
2. Install the dependencies:
pip install torch transformers accelerate tqdm matplotlib pandas
3.(Optional) Enable GPU acceleration in Google Colab:
Runtime → Change runtime type → GPU
4.(Optional) Enable GPU acceleration in Google Colab:
Runtime → Change runtime type → GPU
## Output Files

demo_predictions_with_summaries_and_routing.csv
Contains classified request texts, their summaries, predicted categories, and confidence scores.

## Key Features

Automated zero-shot text categorization

Abstractive text summarization

GPU-accelerated inference (T4 preferred)

Visualization of predicted category distribution

CSV export of results for further analysis

## Example Output

The notebook produces:

1.A category distribution bar chart showing predicted labels

2.A summary table with:
  .Request text
  
  .Predicted category
  
  .Confidence score
  
  .Generated summary
