# Judicial Opinion Labeling Project

## Project Overview
The goal of this project is to develop a model that automates the labeling of text present in the "paragraph" column of a given dataset. The dataset contains 10 different labels/classes, and the objective is to accurately label judicial opinions based on these categories.

## Approach
To tackle this problem, two distinct techniques were employed:

### 1. Mistral-OpenOrca (LLM) Model
- Utilized the Mistral-OpenOrca model hosted on the Ollama server (locally).
- Created a prompt specifying the 10 different classes for the LLM to label the text accordingly.
- No training of the model was performed in this approach.
- Evaluated the model's performance based on contextual similarity between its predictions and the original labels.

### 2. DistilBERT-base-uncased Model
- Employed the DistilBERT-base-uncased model for task-specific fine-tuning.
- Selected the two most frequently occurring classes for fine-tuning, addressing the highly imbalanced nature of the dataset.
- Evaluated the performance of the fine-tuned model using a lightweight model due to computational limitations and a very limited number of data points.

## Requirements & Installation

### Installing Ollama
For detailed installation instructions, please visit: [Ollama Installation](https://ollama.com/download/windows).

### Pulling the Mistral-OpenOrca Model
After installation, you can pull the Mistral-OpenOrca model by running the following command in your terminal:
```bash
ollama pull mistral-openorca:latest
