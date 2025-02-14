

If you fail to get the [[lock]]
	- Wait for a random duration before retrying
	- Each subsequent failure will double the wait time.



Formal Definition:

a retry strategy where, upon encountering a failure, a system progressively increases the wait time between subsequent retry attempts


In reality this is a general concept that can be used for anywhere that requires loading or waiting. I know this is used in some places that require network connections and it doesnt want to obliterate the website with constant retries when connecting to the site.