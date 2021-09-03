# Next-word-prediction-Sentence-Generation
### About 
The model predicts the next word by analyzing the previous words.The model is also capable of generating a sentence of arbitrary length based on given words.
### Dataset
I have used news headlines dataset to train the model.However,the model isn't that robust because of the dataset I have used,these headlines are from abc news which is quite old dataset.I downloaded the dataset from kaggle in csv format.There were about one million records in the dataset but since I was using google colab with 12gb of ram, it can't load the complete dataset for categorical conversion at once, so I had to take a sample of datapoints.
### Preprocessing and visulaization
The news headlines were full of unnecessary symbols and characters, so I cleaned the text by first tokenizing all words,converting them into lowercase and then removing punctuations,unwanted space and finally lemmatizing the words.<br>
I also used word cloud to visualize the most repeated words in the headlines which is shown below.<br>
<img src='https://github.com/nilay121/Next-word-predictor-model/blob/main/wd.png' height=300 width=400>
<br>
After some more preprocessing steps, I One hot encoded the text data using tokenizer class of the tensorflow library, and then passed the generated array through the <b>Embedding Layer</b>.

### Model Creation
I have used two Bi directional LSTM layers with 100 neurons each and then added a dense layer containing 100 neurons.In the last dense layer the number of neurons will be equal to the vocabulary size we have defined.I have trained the model for 30 epochs with optimiser as Adam and the loss function as Categorical Cross Entropy

### Prediction

<img src='https://github.com/nilay121/Next-word-predictor-model/blob/main/pred..png' height=350 width=600>
<br>
<img src ="https://github.com/nilay121/Next-word-prediction-Sentence-Geneartion/blob/main/word_prediction_and_Sentence_generation.ipynb%20-%20Colaboratory%20%E2%80%94%20Mozilla%20Firefox%2003-09-2021%2019_19_27.png" height=350 width=600>
