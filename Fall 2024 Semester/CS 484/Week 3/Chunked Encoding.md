
Related to [[HTTP 1.1]]


If you don't know where the end of a response is,  the server can use a process called "chunked encoding".

This will send the message in pieces.

This is done by setting the Transfer-Encoding: chunked header in the response, and then send the response in chunks, each of which is preceded by the length of the chunk.
	- The end of the response is indicated with a chunk of length 0.
