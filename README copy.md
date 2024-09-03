## Working with the Codebase
---
---

### Code Files Description
---

Under the code folder you will find several files each containing the following: 

1. **read_data.py**: A file containing utility functions that we used to read our data as well as other functions
that we used when downsampling our language datasets. We also had to write a custom functions 
that ensure that we can shuffle our datasets while maintaining a 1-1 mapping between the input and the target. 
We also use a custom split function to ensure that splitting also keeps a 1-1 mapping. 
These functions are later imported in the language_translation jupyter notebook. 


2. **language_translation.ipynb**: a jupyter notebook with code to our entire ML Pipeline. 
See below on how to use the pipeline.

### Running the Pipeline
---

There are four stages involved with our pipeline. Each one of them is described below:

1. Reading and Processing the Data:
Our model works with language data and there are two accepted ways of providing the data.
    - Data can be provided as two files: one for inputs and one for target values. 
    - Data can also be provided as one file: where input sentences appear on the left and target sentences appear on the right separated by a tab. 
Two separate functions are available to read each type of 
data representation. 
* If using the first option, use the read_data function. 
* If using the second option, use the read_tsv_data.

2. After reading the data, proceed with tokenizing and padding the dataset. Both these 
steps are wrapped in one function: data_preprocessing. The data_preprocessing function returns the tokenized 
and padded dataset as a numpy array. If you need to split data into train and test sets,
consider using our custom function, split_data. The default split_ratio is set to 0.40, but can be adjusted 
with the parameter split_ratio.

3. Building, training, and evaluating the models. 
We wanted to explore the perfomance of three models: Simple RNN, Gated Recurrent Unit(GRU), and Long Short Term Memory(LSTM). 
All these models used embedding layers trained from scratch, a time distributed layer, a dropout layer to prevent overfiting, and 
softmax activation function at the output nodes. You can experiment with these models by adding different layers 
and reiterating or add other models and compare all performances.The models are trained and 
tested with our preprocessed datatset. The train model function that takes the train/test data and the number 
of epochs(default is 20, but can be adjusted to preference) to train the models. The function also fits the train data, 
plots validation graphs and evaluates the accuracy on the test data. You can also adjust the 
validation split ratio which is set at 0.4

4. BLEU Score
High accuracies reported in phase 3 did not reflect manually sampled predictions. The CalculateBleuStats function calculates 
the BLEU scores for all prediction and provides another validation metric.

After all modifications are made, run all cells to run the pipeline.



