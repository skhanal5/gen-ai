## About
* A framework that helps you define *pipelines* with LLM's in your application
## Components
* Definition:
	* A part of a pipeline that does a task
* Implementation:
	* A class with methods you can call
* As the user, you define:
	* the input and output types of a component
	* Which component connects to another
* Can make custom components (outside of what Haystack supports)
### Generator
* A component that generates a response to an input
### Retriever
* A component that fetches docs relevant to query and passes it to the next component
## Document Store
* Object that stores documents
* Used by components
### Data Classes
* A way to define the data carried throughout the pipeline
* Usually the I/O of pipelines
	* `Document` and `Answer` are common
## Pipelines
* Combining components, Doc Stores, etc. to make a system