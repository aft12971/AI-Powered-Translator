# AI Translator
An AI-powered toolkit for efficient language translation, combining data preprocessing and RNN models in a user-friendly package for NLP development

## RNN Perfomance Analysis in Machine Translation

The project explores the application and comparative performance of different Recurrent Neural Network (RNN) architectures - Simple RNN, Gated Recurrent Unit (GRU), and Long Short-Term Memory (LSTM) - in the field of machine translation. The focus is on evaluating how these models translate from English to French, assessed through accuracy and BLEU scores. The findings highlight LSTM as the most effective model, with the highest accuracy and BLEU scores, challenging initial expectations about the capabilities of these neural network architectures.


## Project Overview

This repository contains all the necessary components for replicating and understanding the RNN Performance Analysis in Machine Translation project. 

## Contents

- `read_data.py`: Script for reading and preprocessing the data.
- `language_translation.ipynb`: Jupyter notebook containing the model training and evaluation process.
- `paper.tex`: LaTeX source file for the research paper.
- `paper.pdf`: Compiled research paper detailing our findings.
- `icml2014.sty` and `icml2014.bst`: Style and bibliography files for LaTeX formatting.
- `Makefile`: Contains commands to compile the LaTeX document.
- `references.bib`: Bibliography file for citing references in the paper.
- `README.md`: This file, containing documentation for the repository.

## Installation

No installation is required for reading the paper. To run the Python scripts and Jupyter notebooks, ensure you have Python 3.x installed along with the following packages:
- numpy
- pandas
- tensorflow
- matplotlib

You can install them using pip:
```bash
pip install numpy pandas tensorflow matplotlib
