# Question Answering with Flan-T5 and the SQuAD v2 Dataset

This project demonstrates how to perform **Question Answering** using the pre-trained **Flan-T5 model** fine-tuned on the **SQuAD v2 dataset**.

## Overview

In this project, we leverage the **Flan-T5** model, which is a fine-tuned version of Google's T5 (Text-to-Text Transfer Transformer), to answer questions based on the SQuAD v2 dataset. The SQuAD v2 dataset consists of questions based on Wikipedia articles, where some questions have no answer, and the model must predict the appropriate answers or indicate that no answer is available.

## Requirements

Make sure you have the following Python packages installed:

- **transformers**: For working with pre-trained models and tokenizers.
- **datasets**: For accessing the SQuAD v2 dataset from Hugging Face.
- **tensorflow**: For training and evaluation of the model.
- **rouge-score**: For calculating ROUGE scores to evaluate the model's performance.
- **nltk**: For computing BLEU scores (optional).

## Model Training Details

- The **Flan-T5** model is fine-tuned using the **SQuAD v2 dataset**.
- The first 3 layers of the model are frozen during training to focus on fine-tuning the head layers.
- The model is trained for **3 epochs** and can be saved after the training process.

## Evaluation

After training, the model is evaluated on the **validation set** using **ROUGE** and **BLEU** scores to measure the performance of the question answering task.

## Results

- The model predicts answers to the questions based on the given context from the **SQuAD v2 dataset**.
- Performance is measured using metrics like **ROUGE-1**, **ROUGE-2**, and **ROUGE-L** for textual similarity.

## License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.
