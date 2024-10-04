### RNN's 
* Recurrent neural networks 
* Designed to handle sequential data 
* Have recurrent connections
	* allows data to be persistent 
* Problem: can't capture long-range dependencies due to vanishing/exploding gradient problem 
* Gradient:
	* measurement of how performance will improve if we adjust the weights 
	* RNN's try to minimize difference between output and expected value by adjusting weights based on the gradient of the loss function 
* Vanishing gradient:
	* When the gradient becomes very small, RNN learns very slowly 
	* exploding is when gradient is too big -> leading to unstable training 
### LSTM 
* Long short term memory 
* A variant of RNN's 
* Address vanishing gradient problem