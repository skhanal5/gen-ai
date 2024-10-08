### About
* Allows you to retrieve non-parametric data
	* [[Knowledge]]
* Within a data connection, there are different types of "building blocks"
### Building Blocks
#### Document Loaders
* Load documents from CSV, HTML, etc.
#### Document Transformers
* Modify documents into chunks
* LangChain offers:
	* text-splitters
		* Allows you to split doc into chunks and maintain semantic meaning
##### Text Splitters
* Give you lots of customization when splitting your text -> affects your chunk output
	* `chunk_size`
	* `chunk_overlap`
#### Text Embedding Models
* **Very important**
* This is how your data will be represented and is the basis of "knowledge" for the LLM
#### Vector Stores
* Database that can store and search over unstructured data with embeddings
* Performs a fast and accurate *similarity search*
	* [[Building LLM Powered Applications/Vocabulary/Similarity|Similarity]]
* General flow:
	* Data from our data source is embedded into vector store
	* Queries (user prompts) are embedded and then searched against vector store
	* Retrieve most relevant data back to user from vector store
#### Retrievers
* Finds documents relevant to an unstructured query
* Retrievers don't need to store the documents, only needs to retrieve them from a source
* Methods of retrieval:
	* Keyword matching
	* Semantic search
	* Ranking algorithms
* Difference from vector store:
	* Doesn't need embeddings
	* Retrievers can use different sources of documents
		* Vector store need the data itself
* Vector store can be integrated into retrievers (vector store retriever)
	* Retriever looks at vector store and fetches relevant docs