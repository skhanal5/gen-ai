### About
* Allows application to reference user interactions
	* e.g. follow up questions, previous conversations saved as threads
* First, you need to store interactions somewhere else:
	* Redis
	* Cassandra
	* Postgres
	* etc.
* Then you can query memory using memory types
### Memory Types
#### Conversational Buffer Memory
#### Conversational Buffer Window Memory
* Lets you have a sliding window of K interactions
#### Entity Memory
* Remember specific entities in a conversation
* An *entity* can be:
	* names
	* concepts
	* place
	* things
	* concepts