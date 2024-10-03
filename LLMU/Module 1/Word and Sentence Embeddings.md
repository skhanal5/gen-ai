### Word Embeddings
* Categorizes words together based on 
* Ideal word embedding should have these properties:
	* Similar words should be near each other
	* Different words should be far away from each other
	* Should be able to capture many features
		* e.g. semantic meaning
* Recall: the first two properties are similar to clustering algo's
* Recall: one feature is a dimension
* X amount of features/coordinates = a vector
### Sentence Embeddings
* How can you represent a sentence?
* Naive approach:
	* Take the sum of word embeddings
	* Problem: rearranging the same sentence produces the same word even if meaning is different
* Properties:
	* Similar sentences are assigned to similar vectors
	* Deference sentences are assigned to different vectors
	* Each coordinate of the vector identifies a property of the sentence
* Note: vectors can explode in dimensionality
	* Recall: using **Principal Component Analysis** to reduce dimensionality
