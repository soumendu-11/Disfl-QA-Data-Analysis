# Correct Questions Pipeline

This project processes noisy or disfluent questions, corrects them to generate coherent versions, and evaluates the contextual similarity between the original and corrected questions. The pipeline is implemented in Python and utilizes a language model to correct and evaluate the questions.

# Steps Involved

#### `Question Correction:`

The function correctQuestions() is used to correct disfluent questions by sending a prompt to a pre-trained language model (e.g., mistral-openorca:latest).
The disfluent question is corrected to be coherent, grammatically accurate, and contextually aligned with the intended meaning.
Processing DataFrame for Question Correction:

The df2CorrectQuestions() function takes a pandas DataFrame with a column disfluent containing noisy questions.
It generates a new column correct_question with the corrected questions by applying the correction function to each row.
Contextual Evaluation:

The evaluateQuestions() function compares the original question and the corrected question using the same language model to determine if they are contextually similar.
The function returns 1 if the questions are contextually similar and 0 otherwise.
Saving the Results:

The corrected questions and their evaluation results are saved in a CSV file (corrected_questions_with_evaluation.csv) in the local directory.
The output is saved with the | delimiter for easier parsing.
Functions
correctQuestions(prompt: str, model="mistral-openorca:latest"): Sends a prompt to a language model to correct a disfluent question and returns the corrected version.

df2CorrectQuestions(dataframe: pd.DataFrame, model=None): Takes a DataFrame with a disfluent column, generates corrected questions, and returns a DataFrame with a new correct_question column.

evaluateQuestions(dataframe: pd.DataFrame, model="mistral-openorca:latest"): Compares the original and corrected questions for contextual similarity, adding a new column evaluation with the results (1 for similar, 0 for not similar).

CSV Output Format
The output CSV will contain the following columns:
disfluent: The original noisy/disfluent question.
original: The original intended question.
correct_question: The corrected version of the disfluent question.
evaluation: The context similarity score (1 for similar, 0 for not similar).
Usage
Prepare a DataFrame with columns disfluent and original.
Run the correction and evaluation pipeline.
Check the output in the CSV file corrected_questions_with_evaluation.csv.
