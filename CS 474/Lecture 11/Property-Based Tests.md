

A property based test as apposed to standard unit testing:

Unit tests test against specific values:

(1,2,3,4).append(5) == (1,2,3,4,5)


```scala
class IntegerSuite extends ScalaCheckSuite:
	property('addition is commutative'):
		forAll: (i: Int, j: Int =>
			assertEquals(i+j, j+i)

	property('subtraction is NOT commutative'):
		forAll: (i: Int, j: Int =>
			assertNotEquals(i-j, j-i)
```



You can write property based tests to test properties rather than values. So you can expect the same results for any lists. 

**These are properties that should be true for all lists or objects**
