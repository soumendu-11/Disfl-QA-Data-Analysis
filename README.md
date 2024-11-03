Assignment Summary & Outcomes
Objective
The goal of this project is to develop a model that automates the labeling of text present in the "paragraph" column of a given dataset. The dataset contains 10 different labels/classes, and the objective is to accurately label judicial opinions based on these categories.

Approach
To tackle this problem, I employed two distinct techniques:

Mistral-OpenOrca (LLM) Model:

I utilized the Mistral-OpenOrca model hosted on the Ollama server (locally).
A prompt specifying the 10 different classes was created, and the LLM was tasked with labeling the text accordingly.
No training of the model was performed in this approach.
The performance of the model was evaluated based on the contextual similarity between its predictions and the original labels.

DistilBERT-base-uncased Model:

For task-specific fine-tuning, I employed the DistilBERT-base-uncased model.
Given the highly imbalanced nature of the dataset, I selected the two most frequently occurring classes for fine-tuning.
I evaluated the performance of the fine-tuned model.
Due to computational limitations, I opted for a lightweight model and utilized a very limited number of data points.
Requirements & observations
To run the project, please follow these instructions:


Installing Ollama:

For detailed installation instructions, please visit: Ollama Installation.
Pulling the Mistral-OpenOrca Model:

After installation, you can pull the Mistral-OpenOrca model by running the following command in your terminal:
Copy code
ollama pull mistral-openorca:latest
Dependencies:

A requirements.txt file is attached with the necessary dependencies for this project. Ensure to install all required packages listed in this file.
Conclusion
This project aims to provide an effective solution for automating the labeling of judicial opinions using state-of-the-art machine learning techniques. The combination of LLM and fine-tuned models addresses the complexity of the task while accounting for dataset imbalances.

For further information, please refer to the attached documentation and the requirements file.

I noticed overfitting in the case of fine-tuning. 
I added comments in the code to help understand it better. 
