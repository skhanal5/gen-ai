### About
* Few shot learning:
	* Basically, providing models with examples of how we want it to respond
* Difference from fine-tuning:
	* We don't update the models parameters by doing this
* Why:
	* Models can achieve strong performance in a few-shot setting
	* Read: *Language Models are Few-Shot Learners*
### Example
* Comes from the book
```
system_message = """

You are an AI marketing assistant. You help users to create taglines for new product names.

Given a product name, produce a tagline similar to the following examples:

Peak Pursuit - Conquer Heights with Comfort

Summit Steps - Your Partner for Every Ascent

Crag Conquerors - Step Up, Stand Tall

Product name:

"""

product_name = 'Elevation Embrace'
```