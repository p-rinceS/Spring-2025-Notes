


```scala


class MyListsTests extends munit.FunSuite:
	test("MyList allows you to prepend elements."):
		val x = NonEmptyList[Int](1, NonEmptyList(2, NonEmptyList(3, NonEmptyList())));
		val y = x.prepend(2);
		assertEquals (y, ...List) // Obtained, Expected (but iant writing allat)
a
```