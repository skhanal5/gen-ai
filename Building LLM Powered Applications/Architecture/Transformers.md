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
![[Transformer Diagram.png]]
#### Encoding
* Input embedding
	* Vector representation of tokenized inputs
* Positional encoding
	* A way of denoting the position of each word in the input
* Multi-head attention
	* Multiple self-attention mechanisms run in parallel across different parts of input data
* Add and norm layer
	* Adds output of layer to the original input
	* Then applies normalization
* Feed forward layer
	* Transforming normalized output of attention layers into suitable representation
		* E.g., use softmax here or any non-linear function
#### Decoding
* Output embedded
	* We take the target sequence (encoding's output) and shift it by one to the right
	* We remove the last token from the target sequence and pad a start of sequence token
	* For example:
		* Input: How are you (end)
		* Output of encoding: I am fine  (end)
		* Target Sequence: I am find (end)
		* Decoder input: (start) I am fine (end)
* Layers
	* Same as encoding
* Linear and softmax
	* Apply a linear and non-linear transformation
	* Softmax takes output vector into a probability distribution (set of candidate words)
		* Word with the highest probability is picked