


[[Singleton]] 
- Only one instance of a class is able to be created.


```scala
class Singleton private (inner: String){
	private var s: Singleton = null
	def getInstance() : Singleton{
		return s
	}

}
```




[[Factory Method Pattern]]




[[Visitor]]






[[Magnet]]