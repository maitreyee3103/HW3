# Question Answering Models Implementation

This repository contains implementations of three different transformer-based models for Question Answering tasks using the SQuAD dataset.

## Models Implemented

### 1. AlBERTa Model
- Uses `AlbertForQuestionAnswering` architecture
- Parameter sharing to reduce model size
- Learning rate: 2e-6
- Batch size: 16
- Epochs: 10
- F1 Score: 0.168

### 2. BERT Model
- 12 transformer layers
- 768 hidden dimensions
- 12 attention heads
- Learning rate: 2e-4
- Batch size: 16
- Epochs: 6
- F1 Score: 37.038

### 3. DistilBERT Model
- 40% smaller and 60% faster than BERT
- 6 transformer layers
- 768 hidden dimensions
- Learning rate: 2e-6
- Batch size: 16
- Epochs: 10
- F1 Score: 38.267

## Dataset

The models are trained and evaluated on the SQuAD (Stanford Question Answering Dataset) which consists of:
- Wikipedia articles
- Question-answer pairs
- Context paragraphs
- Answers that span within the context text

## Performance Evaluation

Models are evaluated using Exact Match and F1 Score metrics. The evaluation process includes:
- Text normalization (removing articles and punctuation)
- Case normalization (converting to lowercase)
- Comparison between predicted and ground truth answers

### Results Summary
1. DistilBERT: 38.267 F1 Score (Best performing model)
2. BERT: 37.038 F1 Score
3. ALBERTa: 0.168 F1 Score

## Training Details

All models use:
- AdamW optimizer
- `loss.backward()` for gradient computation
- `optim.step()` for parameter updates

### Training Observations
- BERT: Training loss decreased from 2.13 to 0.444
- AlBERTa: Training loss decreased from 1.36 to 0.166
- DistilBERT: Training loss remained constant during training

## Installation and Usage

[Add installation instructions and usage examples here]

## Requirements

[Add required packages and dependencies here]

## Author
Maitreyee Narkhede

## Course Information
CPSC:8430 - Deep Learning
Homework 3

## Repository
GitHub Link: https://github.com/maitreyee3103/HW3
