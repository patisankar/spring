## How JWT works 
(clearly explained in under 2 mins):

JWTs are one of the most widely used methods for API authentication, providing a secure, stateless and scalable way to verify clients.

𝗛𝗲𝗿𝗲’𝘀 𝗮 𝘀𝗶𝗺𝗽𝗹𝗲-𝘁𝗼-𝘂𝗻𝗱𝗲𝗿𝘀𝘁𝗮𝗻𝗱 𝗯𝗿𝗲𝗮𝗸𝗱𝗼𝘄𝗻 𝗼𝗳 𝗵𝗼𝘄 𝗶𝘁 𝘄𝗼𝗿𝗸𝘀, 𝘀𝘁𝗲𝗽 𝗯𝘆 𝘀𝘁𝗲𝗽:

𝟭) 𝗖𝗹𝗶𝗲𝗻𝘁 𝗮𝘂𝘁𝗵𝗲𝗻𝘁𝗶𝗰𝗮𝘁𝗶𝗼𝗻
The client (a user, app, or device) provides credentials (eg; username/password) to the authentication server.

𝟮) 𝗦𝗲𝗿𝘃𝗲𝗿 𝘃𝗲𝗿𝗶𝗳𝗶𝗰𝗮𝘁𝗶𝗼𝗻
The authentication server checks the credentials against its database or identity provider to confirm their validity.

𝟯) 𝗝𝗪𝗧 𝗶𝘀𝘀𝘂𝗮𝗻𝗰𝗲
If authentication is successful, the server:

☑ Generates a JWT with claims (eg; user ID, roles, permissions).
☑ Signs the JWT using a secret key (HS256) or a private key (RS256).

𝟰) 𝗧𝗼𝗸𝗲𝗻 𝗱𝗲𝗹𝗶𝘃𝗲𝗿𝘆
The server sends the signed JWT back to the client in the response.

𝟱) 𝗦𝗲𝗰𝘂𝗿𝗲 𝘀𝘁𝗼𝗿𝗮𝗴𝗲
The client stores the JWT securely to prevent unauthorized access. HTTP-only cookies are the most secure and widely used method.

𝟲) 𝗔𝗣𝗜 𝗿𝗲𝗾𝘂𝗲𝘀𝘁𝘀 𝘄𝗶𝘁𝗵 𝗝𝗪𝗧
For each request to a protected API, the client includes the JWT in the Authorization header:
`Authorization: Bearer <JWT>`

𝟳) 𝗦𝗲𝗿𝘃𝗲𝗿 𝘃𝗮𝗹𝗶𝗱𝗮𝘁𝗲𝘀 𝘁𝗵𝗲 𝗝𝗪𝗧
The API server verifies the JWT before granting access by checking:

☑ Signature – Confirms token integrity (not tampered with).
☑ Expiration – Ensures the token hasn’t expired.
☑ Audience (aud claim) – Checks if the token is meant for this API.
☑ Issuer (iss claim) – Confirms the token was issued by a trusted authority.

If the JWT is valid, the server grants access to the requested resource. Otherwise, it rejects the request (401 Unauthorized).

𝟴) 𝗧𝗼𝗸𝗲𝗻 𝗲𝘅𝗽𝗶𝗿𝗮𝘁𝗶𝗼𝗻 & 𝗿𝗲𝗳𝗿𝗲𝘀𝗵
Since JWTs expire for security reasons, the client needs a refresh token to get a new one:
↳ Client sends refresh token to the server.
↳ Server verifies & issues a new JWT if the refresh token is valid.
↳ New JWT replaces the expired one, and the client continues making requests.

This workflow ensures secure, stateless, and efficient authentication for APIs while keeping performance and scalability in check.
