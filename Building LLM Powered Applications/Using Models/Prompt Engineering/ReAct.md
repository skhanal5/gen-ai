### About
* ReAct: combines reasoning and acting with LLM's
* It does two things:
	* Prompts model to generate verbal reasoning traces and actions for a task
	* Receives observations from external sources
* Benefits:
	* Performs dynamic resaoning
	* Quickly adapts its action plan based on external information
* Example:
	* Prompt LLM to answer a question by first reasoning about it and then performing an action to search on the web
	* Then, observe the search results and continue with thought + action until we get a good response
* 