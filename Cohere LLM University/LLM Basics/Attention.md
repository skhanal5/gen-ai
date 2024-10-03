### Scenario
* Suppose a word can be used in two different contexts
* The model needs the context of the sentence in order to pick which meaning of the word to use
* Example:
```
- The bank of the river.
- Money in the bank.
```
* bank fits in both sentences
### Attention in Practice
* We need to use nearby words to help deduce the context of this current word
* Using the example above:
	* river & money both are keywords that give context
* Given a word embedding of all words in each sentence:
	* Make copies of the current word, bank
		* bank1 
		* bank2
	* Move each closer to their respective keyword 
#### Filtering "Junk" Words
* Using similarity, we can filter out junk words from the current word
	* e.g., we can expect the similarity of the word "the" and "bank" to be significantly less compared to other words like "river"
	* model will ignore these words
* Suppose we make a 2D matrix that compares each word to one another, including itself
	* The cells will be the similarity of each word
* We can transform each word by taking the sum of products of its similarity for each other word
	* Example with the in "the bank of the river":
		* the1 = (the * 1) + (bank * (similarity(the, bank)) + ...
* Now, we can transform the entire sentence using this