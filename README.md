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
- For detailed installation instructions, please visit: [Ollama Installation](https://ollama.com/download/windows).

### Pulling the Mistral-OpenOrca Model
- After installation, you can pull the Mistral-OpenOrca model by running the following command in your terminal:
ollama pull mistral-openorca:latest


## Dependencies
A requirements.txt file is included with the necessary dependencies for this project. Ensure to install all required packages listed in this file.

## Observations
Noticed overfitting in the case of fine-tuning.
Comments have been added in the code to enhance understanding.

## Conclusion
This project presents a promising and feasible solution for automating the labeling of judicial opinions through the innovative application of state-of-the-art machine learning techniques. By leveraging the strengths of both Large Language Models (LLMs) and fine-tuned models, we effectively tackle the complexities inherent in this task while addressing the challenges posed by dataset imbalances. The methodologies implemented not only enhance the accuracy of the labeling process but also pave the way for future advancements in legal technology. With the groundwork laid out, this project is not only achievable but also holds significant potential for improving efficiency and reducing the manual effort involved in analyzing judicial texts. We are optimistic about the prospects of further refinement and scalability, making this a highly doable and impactful initiative in the field.
