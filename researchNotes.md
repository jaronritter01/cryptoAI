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

* Have a 3D input requirement
* in the form of (batch_size, time_steps, units)
* ![pic for image](input.jpg)

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

- Another Link
    - Need IEEE access to view
    - https://ieeexplore.ieee.org/abstract/document/7966019

* Data does not only flow in one direction
* Neurons can pass data into a previous layer or the same layer

- Here is a good link with code examples
    - https://colab.research.google.com/drive/18WiSw1K0BW3jOKO56vxn11Fo9IyOuRjh#scrollTo=VU6ve06iDV5Q

- Helpful Explanations
    - https://colah.github.io/posts/2015-08-Understanding-LSTMs/
    