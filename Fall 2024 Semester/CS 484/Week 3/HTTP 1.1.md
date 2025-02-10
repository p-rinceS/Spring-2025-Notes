
Protocol that was in use when the web was becoming a popular way to access information on the Internet






Round trip time:
	Additional latency costs regardless of how much data you're sending.
	- If a client needs to send one bit to the server and wait for the server to respond, it doesn't matter how fast the server is, the entire system will have to wait for the entire round trip.

Every time a computer wants to make a connection to a host , it needs to send a DNA query to a DNA server. It will need to wait for a DNA lookup (full RTT) before it can start the HTTP connection.


One way to reduce latency of HTTP requests is by reusing the same connection for multiple requests
	- "keep alive" connection.
		- If the server can indicate where the end of their response is, the client can send another request without needing to wait to establish a new connection
	- This is the default behavior in HTTP 1.1
	- The end of a response is indicated by the server setting the Content-Length header, it will tell the client how many bytes to expect in the response.

[[Chunked Encoding]]


After we have a primitive of "keepalive" connections, we can start to think about how we can make the more efficiently.
	One way we can do this is with [[Request Pipelining]]


## Simultaneous connection limits and domain sharding


Most browsers limit the number of simultaneous connections to 6 per domain.

	[[Domain sharding]]


## Caching

- Http Headers can be used to indicate to the client that the response can be cached.

Using the `Cache-Control` header, which can have a number of different values:
	- `Cache-Control: no-cache`
		- the client can cache the response, but also revalidate it with the server before use.
	- `Cache-Control: no-store`
		- client must not cache the response
	- `Cache-Control: max-age=3600`
		- client can cache the response for 3600 seconds (1hour) before revalidating it with the server


Header is typically set by server 


## Content Encoding (compression)

`Content-Encoding` header tells the client how the response is encoded.
	- Typically used for compression, where the server compresses the response before sending it to the client

Most common encoding is `Content-Encoding: gzip`
	- Lossless compression algorithm widely supported browsers and servers.


## Range requests

`Ranger` header allows the client to request only part of a response.
- Useful for large responses like videos.



## CDNs
	