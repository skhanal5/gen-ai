### About
* Introduced in Attention is All You Need
* Contains of attention mechanisms
### What is Attention?
* A mechanism in the architecture that allows the model to capture the most relevant context in the input in order to produce an output
* General flow:
	* Calculates attention scores between input and outputs
	* Uses softmax to get weights
	* Takes a weighted sum of input sequence to get context vectors
* Attention is referred to as self-attention since it is used in the *current* sequence being generated
#### How it Works
* Need a few values:
	* query
		* current focus of the attention mechanism
	* key
		* which parts of input should be given attention
	* value
		* used to compute context vectors
* (Softmax function ( ( Q * K ) ) / dim of K ) * V
#### Components
* Encoder
	* Takes input sequence and produces a sequence of hidden states
	* Each state is a weighted sum of all input embeddings
* Decoder
	* Takes output sequence and produces a sequence of predictions
	* Note: output sequence is shifted right by one
	* Each prediction is a weighted sum of all encoder's hidden states and the previous decoder's hidden states
#### Simplified Transformer Diagram Explained
