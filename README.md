# Prompt Injection Detection — Assignment 4

Research topic: Development of a Prompt Injection Attack Detection
System for Large Language Models Using Machine Learning and
Rule-Based Analysis

Author: Zhibek Mussakulova

## Investigation

This experiment compares three prompt-injection detectors:
- Rule-based detection using regular expressions.
- Machine-learning detection using TF-IDF and Logistic Regression.
- Combined detection using an OR decision rule.

## Dataset

Dataset: deepset/prompt-injections
https://huggingface.co/datasets/deepset/prompt-injections

Training subset: 436 prompts.
Validation subset: 110 prompts.
Official test set: 116 prompts.
Random seed for the training/validation split: 42.

## Files

- small_thesis.ipynb: implementation and saved experiment outputs.
- final_results.csv: test-set performance metrics.
- test_predictions.csv: reference labels and detector predictions.
- final_confusion_matrices.png: test-set confusion matrices.

## Running the experiment

Open small_thesis.ipynb in Google Colab and run the cells in order.
The first cell installs the required packages.
The notebook loads the dataset from Hugging Face.

## Results

Test-set injection-class F1-scores:
- Rule-based: 0.261
- Machine learning: 0.852
- Combined: 0.862

The combined detector identified one additional injection compared
with machine learning alone, with the same number of false positives.
This is a small observed improvement on one test set, not evidence
of general superiority.
