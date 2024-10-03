### Dot Product Similarity
* Taking the sum of products for each coordinate in the vector
* Properties:
	* Similar points should have a high similarity score
	* Distance points should have a low similarity score
* Example:
```
- Dot product for the pair [You’ve got mail, Taken] = 0*7 + 5*0 = 0
- Dot product for the pair [Rush Hour, Rush Hour 2] = 6*7 + 5*4 = 62
```
### Cosine Similarity
* Look at the angle between vectors
* Naive measurement: Suppose you take the Euclidean distance for two items
	* Points far away will have a higher distance
	* Points close will have a smaller distance
	* Problem: this is intuitively wrong, the closer you are, the higher the score
* Using cosine:
	* Create two rays that start at the origin and cross through each point
	* Look at the angle between the rays
	* Angle is small, if points are close together
	* Angle is large, if points are further part
	* Take the cosine distance = cosine of the angles formed by the two rays
* Cosine similarity properties:
	* Two identical items have similarity score 1
		* Since the angle is 0
	* The lowest score you can get is -1
	* [-1,1]
* 