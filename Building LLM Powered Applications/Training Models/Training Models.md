### Common Terms
* Parameters: 
	* Number of connections between neurons
	* The weights
* Training set
	* The corpus used to learn and train parameters
### Training Steps
1. Data collection
2. Data preprocessing
3. Model architecture
	2. Picking the NN used and its structure
	3. Number/size of layers
	4. Etc.
4. Model initialization
	1. Assigning initial values to weights of LLM
	2. Can be done randomly or by using pre-trained weights
5. Model pre-training
	1. Updating weights by feeding data and computing the loss function
	2. LLM tries to minimize loss using an optimization algo
		1. Gradient descent
		2. [[Stochastic Gradient Descent]]
6. Fine tuning
	1. Model is trained with data in the following structure:
		1. (prompt, ideal response)
	2. Also referred to as supervised fine-tuned learning (SFT)
7. Reinforcement learning from Human Feedback (RLHF)
	1. Optimizing SFT with reward model