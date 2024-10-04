### Structure of ANN's
* Smallest unit in an ANN is a neuron 
* Neurons are layered with connections in between
* Those connections are weighted
	* Represents strength of connection 
* Weights are also referred to as the parameters of the model 
* ANN's are just mathematical operations
	* Can only operate on numbers
### ANN Inputs
* Context of LLM: comprised of unstructured textual data 
* Thus data must be transformed
#### Tokenizing
* Taking unstructured text based data and breaking it down into tokens
* A token can be a character, prefix/suffix, word -> unit depends on algo 
#### Embedding 
* Token is converted to a numerical vector 
* Captures semantic meaning of each token 
### More on ANN Layers
* Structure:
	* Input layer
	* Hidden layer
	* Output layer
#### Input Layer
* Receives input data 
* Each neuron in this layer = feature/attr of input data 
#### Hidden layer 
* uses math to transform inputs and extracts patterns from data 
#### Output layer 
* Produces final output -> prediction/classification/etc.

### Backpropagation 
* This will iteratively adjust the weights of each neuron connection based on training data and the desired outputs 
* Comprised of two phases: 
	* Forward pass 
		* data goes through network to compute the output
	* Backward pass
		* errors propagate backwards to update the network's parameters and improve its performance \
* "Learning" occurs by comparing output with expected result and minimizing the error 
	* error/loss is another metric 
### Generation Explained 
* Using prompts to generate words in sequence is based on Bayes Theorem 
* At some point we will have a vector of probable words
	* Vector contains probabilities computed using Baye's
	* We select the word that corresponds to the highest probability and move on 
### Softmax / Last Layer 
* Converts a vector of real numbers into a probability distribution 
* Used to normalize output of NN