### About
* [[Autoregressive Model]]
* Architecture: 
	* Transformer, decoder only
* Three sizes:
	* 7,13,70B
	* each trained on 2T tokens
* Each size has a chat version for conversations
* Fine-tuning contained:
	* supervised fine-tuning with:
		* instruction datasets
		* human annotations
		* also:
			* uses a selected list of prompts to guide outputs and a loss function that focuses on diversity 
	* RLHF