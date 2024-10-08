### About
* Optimizes output of an LLM by referencing a knowledge base **outside of its training data**
* Allows you to extend existing LLM functionality to a specific domain
	* e.g. internal knowledge base
* Benefit:
	* No need to retrain the model
	* Cost effective
	* Gives you full control over generated output since you control the knowledge base
		* Accuracy
### Flow
* Create external data
* Use an embedding model to convert data 
* Store embedded data into a vector database
* User queries
* Convert that query to a vector representation (via embedding) and match with data in the vector database
* RAG will augment the existing user prompt with this data
	* via prompt engineering
* LLM will generate an output accordingly
### Semantic Search
* Retrieval System
	* Pulls *K* documents*/passages from knowledge source
* Re-ranker
	* Reranks the *K* retrieved passages 
	* Improves relevance
* Generative Model
	* Uses retrieved passages to generate final output
### Resources
1. [What is RAG?](https://aws.amazon.com/what-is/retrieval-augmented-generation/)
2. [RAG vs VectorDB](https://medium.com/@bijit211987/rag-vs-vectordb-2c8cb3e0ee52)
