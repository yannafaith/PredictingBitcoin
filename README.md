# Bitcoin closing price prediction 

### Links to online notebooks (in case unable to load in Github):

- https://nbviewer.jupyter.org/github/yannafaith/PredictingBitcoin/blob/master/BitcoinWithSentiment.ipynb
This notebook expands upon the most succesful model from the notebook below, by including bitcoin's total volume and a sentiment indicator (with value indicators ranging from extreme fear to extreme greed).

- https://nbviewer.jupyter.org/github/yannafaith/PredictingBitcoin/blob/master/BitcoinPrediction.ipynb
This notebook explores three different (simple and un-optimized) ML models for predicting bitcoin's closing price, given 
historical closing prices from Jan 01 2018 to Feb 19, 2019.

### Summary/Ranking of Models

##### Multivariate LSTM 
- Training set was 365 days, and the test set was the rest.
- had 3 input vars/features, looked at the data one timestep back, output a predicted closing price. 
- used 200 epochs.
- Had a RMSE of 96.75. 

For the rest of the models, the training set was 66% of the dataset.

##### LSTM (Long Short-Term Memory Model)
- had one input neuron, four neurons in a hidden layer, and one output neuron.
- looked back 3 days
- used 200 epochs and a batch size of five. 
- Had a RMSE of 110.88. 

##### AIRMA (AutoRegressive Integrated Moving Average)
- Had a RMSE of 157.71. 

##### Baseline model was a "naive" persistance model. 
- At timestep t it outputs (t-1). 
- This had a RMSE of about 160.54 

##### MLP (Multi-Layer Perceptron Model) 
- had one input neuron, five neurons in a hidden layer, and one output neuron.
- used 50 epochs and a batch size of one. 
- Had a RMSE of 160.56.

