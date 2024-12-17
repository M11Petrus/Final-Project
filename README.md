This code analyzes movie reviews and determines whether they are positive or negative. The following models were used in the code:

BERT (Bidirectional Encoder Representations from Transformers):
The base pre-trained model bert-base-uncased from the Hugging Face Transformers library. It was used for classifying text into positive and negative reviews. 

LoRA (Low-Rank Adaptation):
This method was applied for additional fine-tuning of the BERT model. LoRA optimizes training by adding adaptive layers with fewer parameters, which reduces resource consumption. Thus, the foundation is BERT, fine-tuned and optimized using LoRA to improve accuracy and efficiency.

Key Components:

Data Preprocessing What was done: The IMDB dataset with movie reviews, including text and labels (positive/negative), was used. The texts were tokenized (converted into numerical format), truncated, and padded to ensure uniform length.
Why its important: Tokenization prepares the data for input into a neural network model, preserving its structure and context.

Transformers, Trained from Scratch and LoRA What was done: The BERT model was fine-tuned for the text sentiment classification task. The LoRA (Low-Rank Adaptation) method was used to optimize training and reduce computational resource requirements.
Why its important: Training a model from scratch is expensive and requires a lot of data. Using a pre-trained model (BERT) with additional fine-tuning via LoRA achieves high accuracy with minimal computational costs.

A/B Testing, Fine-Tuning, and Model Comparison What was done: The BERT model was fine-tuned using LoRA on a reduced training dataset. The resulting model was compared to the baseline BERT model (without fine-tuning).
Result: The LoRA model demonstrated significantly higher accuracy compared to the baseline model.

Why its important: A/B testing validates the effectiveness of fine-tuning and optimization, which is critical for selecting a solution for real-world use.

Python API What was done: An API was created using FastAPI that accepts input text and returns the models sentiment prediction. The API allows HTTP requests, making the model accessible for integration into web applications, bots, and other systems.
