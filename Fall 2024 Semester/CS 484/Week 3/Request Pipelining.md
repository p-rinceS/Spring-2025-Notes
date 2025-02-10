


The idea that a client can send multiple requests to the server without waiting for a response to the first one.

Bad idea in practice because of a problem called "head of line blocking".
	- If the server is slow to respond to one request, it will block all other responses that are in the pipeline behind it.
	- Client cannot take advantage of parallelism that it could have if it had waited for the response to the first before sending the second or if it had sent the request in parallel over a different TCP connection.

[[HTTP 1.1]]