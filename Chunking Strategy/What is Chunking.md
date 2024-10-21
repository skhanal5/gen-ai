## About
* Given a document, we want to split it into roughly uniform sized chunks
* Why?
	* When we retrieve information from a vector database, this will help us retrieve **relevant** info
### Benefits of Chunking
* By splitting text into chunks, we prevent noise from interfering with retrieval
* We do not want to grab too much information than is needed for a prompt
* Conversely, if our chunks are too small, then we will fail to get enough information
