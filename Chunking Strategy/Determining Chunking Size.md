## Factors
### Query Size
* Recall: 
	* Queries will be embedded into a vector and used to compare against the existing embeddings
* For the sake of comparison, we need the queries to be roughly the same size as the document embeddings
### Nature of Content
* If we are working with long documents, then longer context is needed
* If we are using random snippets, then use smaller context 
### Embedding Models
* Certain embedding models work better on a specific sequence length
### LLM Token Limit
* LLM's have a limited context window
* If we are using RAG, then the amount of augmented data to the original prompt must fit