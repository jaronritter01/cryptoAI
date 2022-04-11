Research Notes

Long Short-Term Memory Neural Network (LSTM) 
============================================ 
- Data from:
    - https://www.researchgate.net/profile/Murtaza-Roondiwala/publication/327967988_Predicting_Stock_Prices_Using_LSTM/links/5bafbe6692851ca9ed30ceb9/Predicting-Stock-Prices-Using-LSTM.pdf
    
* seems very popular
* Features Extracted
    * Date
    * Open
    * Close
    * High
    * Low
    * Close
    * Volume

* Their method had 5 stages 
* These models are able to effectively associate memories and imput over time
* Testing data should only be 5-10% of all the collected data

Neural Network with Keras
=========================
    
``` python:
model = Sequential()
model.add(LSTM(128, input_shape=(layers[1], layers[0]), return_sequences=True))
model.add(LSTM(64, input_shape=(layers[1], layers[0]), return_sequences=False))
model.add(Dense(16,init='uniform',activation='relu'))
model.add(Dense(1,init='uniform',activation='linear'))
```

* seems that around 500 epochs is a good number for incorperating all the mentioned parameters