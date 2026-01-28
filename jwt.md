### asymmetric vs symmetric

symmetric encryption,  same key is used for encryption and decryption. Asymmetric encryption, sender/reciever use differnt key for encryption/decryption.

### JWT

First started with session based authentication, where it is problem, then we moved to token based authentication.
The client sends a request to the server with a username/password.
The application validates the credentials and generates a secure, signed token for the client.
The token is sent back to the client and stored there.
When the client needs to access something new on the server, it sends the token through the HTTP header.
The server decodes and verifies the attached token. If it is valid, the server sends a response to the client.
When the client logs out, the token is destroyed.
