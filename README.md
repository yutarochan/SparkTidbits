# SparkTidbits
Bunch of cookbook style code snippets, notes and other trivial Spark &amp; Scala tips for myself. 

---
**Flatten a List of Tuples**

Spark complains that there isn't an explicit conversion, and so you need to define that as follows:

	val tupleList = List((1,2), (3,4), (5,6))
  	tupleList.flatten {case (a,b) => List(a,b)}
  	>> List(1, 2, 3, 4, 5, 6)

