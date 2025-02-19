

```java

class C {
	private volatile static Config config = null;
	public static config getConfig() {
	if config == null
		synchronized (this) {
			if config == null
				config = config.parseFile();
		}
		return config;
	} . . .
}

class Config {public final String field;}
```


### [[Happens-Before Relationship]]
