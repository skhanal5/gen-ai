### Scenario
* Think of auto-complete:
	* It uses the previous 2-3 words to suggest the next one
	* What happens if you spam click each suggestion?
		* Sentence doesn't make sense because suggestions take into consideration the entire sentence
### Transformers 
* Keep track of what is being written and use it to suggest next word
* Generation is done word by word in sequence
* Trained using all data in the internet
### Architecture
*  Comprised of:
	* Tokenization
	* Embedding
	* Positional encoding
	* Multiple transformer blocks
	* Softmax
#### Tokenization
* Comprised of a large dataset of tokens
	* Factors in every word, punctuation signs, prefix/suffix, etc and maps to a token
#### Embeddings
* Given the tokens, you can turn the words into numbers
* Each token becomes a vector, together the sentence is a combination of vectors
#### Positional Encoding
* Now that we have multiple vectors, we want to encode them into one vector
* Naive way:
	* Add each vector component wise (coordinate by coordinate)
	* Problem:
		* Rearranging words of a sentence and adding them together will give you the same encoding
* Positional encoding:
	* Adding a sequence of predefined vectors to the embedding vectors of words
	* This will factor in the position of each word when summing the vectors together
		* Ensures re-arranging the words will always produce a different result
	* For example:
		* Write a story => Write(1) a(2) story(3)
#### Transformer Block
* Purpose: predict the next word in this sentence
* This is where the attention component is used
	* [[Attention]]
* Each transformer block is comprised of an attention component
	* Each block has the goal of predicting a word
	* This attention component is tied to a feedforward neural network that accomplishes that goal
* Transformer block are  chained together, taking the result of the previous block
* Outputs a score for each word, highest score is given the word that is most likely to be next
#### Softmax Layer
 * Turns the score from the transformer block into probabilities
 * Higher score = higher probabilities
 * Sample out of each probability to get the next word
 * Output is the word
#### Repeat
* Using the output of the softmax layer, repeat everything above
### Post Training
* Once you train a transformer on the internet, you train it again on known Q&A's
* It is biased towards whatever it just learned