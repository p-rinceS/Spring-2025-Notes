
Transport Layer Security 
	- Cryptographic protocol that provides confidentiality and integrity in communication between two parties.
	- Wrapper around HTTP.
		- HTTPS is just HTTP communication wrapped in TLS, with verification of the server's identity (the Host: header and the domain name seen in the URL bar).



# TLS Overview

- **Handshake:** The client and server negotiate a secure connection by exchanging messages to agree on cryptographic parameters and establish a shared secret key.
	- The client sends a `ClientHello` message to the server
	- The server responds with `ServerHello` 
	- By using the server's public key, the client securely generates and sends a shared session key through a secure key exchange algorithm (Diffie-Hellman or Elliptic Curve Diffie-Hellman).


TLS is engineered to allow whoever uses it to choose which cryptographic algorithm to use.
