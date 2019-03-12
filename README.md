# This program is meant to classify, inquiry type. Program will be given an input, and it'll output the type of question.

Program has been trained with around 1400 different kind of sentences. In which 20% of which were kept as validation dataset. 


### Following feature engineering was done on dataset:
  1. Use a lambda function, to convert all inquiry question in the data to lower and to remove all unwanted characters in the given dataset with space.  
  2. Secondly, I've used tokenizer from keras.preprocessing to split the sentences in the given inquiry dataset to tokens, and convert those tokens subsequently to integers. Afterall, these word integers will be feeded into the LSTM units.
  3. I have changed outputs of Y, which is target variable, into some specific labels. We can in time use the outputs from our model to perform inverse label and get our desired output
  4. I've made embedding vector, from the glove 6 billion, 100 dimensional word vector. I've used these embeddings to convert the word into word vector


### Structure of Model used:
I'm using *Unidirectional LSTM of around 200 units with 1 layers*, as it makes sense to use an algorithm with constantly changing weights, will learn quite well, and increase in accuracy was also observed. So no reason why it shouldn't be used
I'm also using droputouts, of around 0.2. It should prevent overfitting, and it does quite well as we see validation accuracy of around 0.9

### How to run this program


After extracting the glove embeddings in the same folder as jupyter notebook, place any sentence you want in the last line of the cell. and press ctrl+enter. It'll print output