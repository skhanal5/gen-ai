## About
* LLM is given a meta prompt and some examples of tasks it will perform
	* Meta prompt is a instruction to improve performance of tasks w/ examples
* Uses prior knowledge + examples to perform task
*  Why:
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