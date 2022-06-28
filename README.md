# About this Repository
This project contains the code that I saved while practicing LSTM Model.

# Used Data (Train Data)
AI Hub data - Emotional communication/sentiment corpus (74000 sentences)

# Text Preprocessing
+ drop duplicate sentences
+ Get rid of things that are not Korean (Noise Canceling)
+ Stopword processing
+ Check rare words and remove 

# Text Vectorize
+ Tokenizing use rare word counts
+ switch text to sequences
+ pad sequences for making all sentences length same
+ if using machine learning model as LogisticRegression, LightGBM we do TF-IDF Vectorization

# Model
+ LightGBM
+ LogisticRegression
+ LSTM

# Result
|Model|Vectorization|Accuracy|
|------|---|---|
|LogisticRegression|TF-IDF|86.8%|
|LogisticRegression|CountVectorize|86.6%|
|LogisticRegression(liblinear)|TF-IDF|86.7%|
|LightGBM|TF-IDF|87.5%|
|LSTM|Tokenizer|80.1%|

This is a result of model accuracy when the number of labels is 3. LSTM is the lowest one, but LSTM bias is lower than any other one. 
Also, actual label was six, but I made it three. So this accuracy cannot be determined unconditionally. 
If, the class label is six, LSTM Model is highest and accuracy difference(LSTM and other) gets higher.


