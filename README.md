# **Binary Sentiment Classification with Hugging Face Transformer Model**
**Binary sentiment classification** represents a fundamental Natural Language Processing (NLP) task, wherein the objective is to categorize a piece of text, often a sentence or document, into one of two primary categories: positive or negative sentiment.

Recently, I've been assigned to an exciting project that involves classifying the sentiment of customer reviews. This project aligns perfectly with my current learning journey in **PyTorch and Hugging Face**. Given the constraints of not being able to share actual customer reviews, I thought it would be great to demonstrate my approach to sentiment classification tasks by undertaking a project to classify the sentiment of IMDB movie reviews.

For this project, I'm going to fine-tune [a pretrained BERT uncased model](https://huggingface.co/bert-base-uncased) shared on the Hugging Face Hub with [IMDB movie reviews data](https://huggingface.co/datasets/imdb) and use the fine-tuned mdoel to classify the sentiment of movie reviews. Final results are saved in a CSV file, facilitating easy reference and analysis.

**Without any fine-tuning**, the pretrained BERT uncased model can correctly classify the sentiment of **48%** of movie reviews in the testing data. **After fine-tuning** the model with only 500 movie reviews, it can correctly classify the sentiment of almost **80%** of movie reviews in the same data.

A substantial portion of the functions employed throughout this project are sourced from the **Hugging Face Transformers library**. The deep learning framework used is **PyTorch**.

---

# **Table of Contents**
## **Section 1: Download the IMDB movie reviews dataset and process the data**
- 1.1 Download the dataset from the Hugging Face Hub
- 1.2 Process data
    - 1.2.1 Tokenize text
    - 1.2.2 Dynamic padding

## **Section 2: Prepare for modeling**
- 2.1 Process tokenized dataset
- 2.2 Prepare DataLoaders
- 2.3 Set up optimizer 

## **Section 3: Modeling**
- 3.1 Baseline model
- 3.2 Fine-tune the pretrained BERT uncased model

## **Section 4: Use the fine-tuned BERT uncased model for sentiment classification**
- 4.1 Process data and prepare DataLoaders
- 4.2 Classify sentiment of movie reviews
- 4.3 Export results to a CSV file

--- 

# **Summary**
**Sentiment analysis**, encompassing tasks like binary sentiment classification, is now more accessible and efficient than ever, thanks to the **Hugging Face Transformers library**. Many pretrained models shared on the Hub can be downloaded effortlessly. Based on the fine-tuned BERT uncased model's performance, often requiring just a small amount of domain-specific data, these pretrained models can deliver exceptional performance in sentiment classification tasks.
