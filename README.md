# NLP_nextwords
My simple implementation of predicting next words using Keras LSTM. 

[//]: # (Image References)
[Graph.png]: ./logs/Graph.png

### How to run the code
```
python3 prednextwords.py --mode 'train' --data_path 'datasets/simple-examples/data'
```

### key takeaways
* Here I used word to integer as id, However it is normally suggested to use word2vec. But since keras provide Embedding layer, so it is convenient here. 
* Create dict = (word, id) and reverse dict = (id, word)
* `num_steps=30` indicates we use 30 words to predict next word
* `skip_steps=30` indicates we skip 30 words to take next batch
* `hidden_size=500` indicates the word embedding layer will have vector size 500 to represent the word. 
* rest of keras Sequential model setup is very normal. 


### reference
https://keras.io/layers/recurrent/
http://adventuresinmachinelearning.com/keras-lstm-tutorial/

### model graph
![alt text][Graph.png]
