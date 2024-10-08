### About
* During 80's and 90's, RNN's and LSTM's were popular architectures for ANN's
* Nowadays, we use [[Building LLM Powered Applications/Architecture/Transformers|Transformers]]
### RNN's 
* Recurrent neural networks 
* Designed to handle sequential data 
* Have recurrent connections
	* allows data to be persistent 
* Problem: can't capture long-range dependencies due to vanishing/exploding gradient problem 
### Gradient
* measurement of how performance will improve if we adjust the weights 
* RNN's try to minimize difference between output and expected value by adjusting weights based on the gradient of the loss function 
#### Vanishing gradient
* Problem occurs during training
* When the gradient becomes very small
	* RNN learns very slowly 
	* Fails to capture long-term patterns in the data
#### Exploding Gradient
* Problem occurs during training 
* When the gradient is too big
	* leading to unstable training
	* Model can't find a good solution
	* 
### LSTM 
* Long short term memory 
* A variant of RNN's 
* Address vanishing gradient problem