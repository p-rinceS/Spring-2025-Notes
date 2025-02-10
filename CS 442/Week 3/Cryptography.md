

[[TLS Protocol]] makes use of symmetric and asymmetric cryptography.

Symmetric Cryptography
	- Same key is used for both encryption and decryption.
	- Key must be kept a secret between parties in communication.
	
Asymmetric Cryptography
	- Two keys are used:
		- Public key
			- Used for encryption and digital signature verification.
			- Can be shared with anyone
		- Private key
			- Used for decryption and digital signature creation.
			- Must be kept a secret.

Sender encrypts message with recipient's public key.
	This message can only be deciphered by the recipient's private key.


Diffie-Hellman Key Exchange:
	- Diffie Helman is a key exchange algorithm that allows two parties to securely exchange a shared secret key over an insecure channel.
	- Shared secret key can then be used for symmetric encryption
	- This algorithm is secure even if an attacker can eavesdrop on the communication between the two parties.

