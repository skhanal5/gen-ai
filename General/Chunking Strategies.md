### About
* Chunking: 
	* Process of breaking down large pieces of text into a smaller segment
	* Maintains semantic meaning
* Usage:
	* Used to optimize relevance of the content we get from a vector database
### Chunk Size
* If chunks are too small or too large, it can lead to imprecise search results or missed opportunities 
* Rule of thumb: if chunk makes sense without surrounding context to humans -> works for LLM's too
* For external model providers:
	* We need to determine if we can fit retrieved text into our context 
	* Every model has a limited context window
### Content Size
* If we embed sentences, vectors will capture sentence meaning and will be used to compare against other sentence embeddings
	* Missing paragraph/document level context
* If we embed paragraphs, we can consider both paragraph level context and sentence/phrase level context
	* Large input text sizes can introduce noise though
* Length of query has an influence:
	* shorter queries will be good for sentence-level matching
	* longer queries are good for paragraph/document level
### Chunking Considerations
* Nature of content being indexed
* Embedding model being used
	* Might perform optimally on a certain chunk size
* Expectation for length and complexity of user queries
* How will retrieved results be utilized
### Methods
#### Fixed-sized chunking
* Decide the number of tokens in our chunk beforehand
* Decide if there should be any overlap (optional)
* Benefits:
	* Computationally cheap
	* Simple to use
* **Most common** approach
#### Sentence Chunking
* If we know our content is based on sentences use this
* Naive splitting:
	* Splitting by period
	* Doesn't work for edge cases
* NLTK:
	* Library that comes with a sentence tokenizer
* spaCy:
	* comes with sentence segmentation
#### Recursive Chunking
 * Divides input into smaller chunks in a hierarchical and iterative manner
 * Algo:
	 * We specify the chunk size and overlap
	 * The method runs for the first time
	 * Then the method recursively calls itself on resulting chunks in case the first attempt didn't produce enough chunks of that size
#### Specialized Chunking
* Markdown splitter
	* Divide content based on markdown structure and hierarchy
* LaTex Splitting
	* Divide content based on LaTex
#### Semantic Chunking
* Greg Kamradt mentions that global chunking size is too trivial
	* Might miss meaning completely depending on the size which is arbitrarily determined
* Semantic chunking uses the following principle:
	* Use embeddings which have semantic meaning
	* Using those embeddings create chunks
* Steps:
	* Break document into sentences
	* Create sentence group
		* For each sentence have a group of sentences with sentences before/after it
		* Each group has an anchor sentence (the original sentence)
	* Generate embeddings for each sentence group and associate with their anchor sentence
	* Compare distances between each group
		* Anchor and the group **before it** will have a low distance