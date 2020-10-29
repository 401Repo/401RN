[Home](https://401repo.github.io/401RN/README)

# Readings: ACL

![Source](https://d1cy5sv9pggpkr.cloudfront.net/wp-content/uploads/access-control-lists-definition-types-and-tutorial.png)

### When is Basic Authorization used vs. Bearer Authorization?

The Basic and Digest authentication schemes are dedicated to the authentication using a username and a secret.

The Bearer authentication scheme is dedicated to the authentication using a token and is described by the token. Even if this scheme comes from an OAuth2 specification, you can still use it in any other context where tokens are exchange between a client and a server.

Concerning the JWT authentication and as it is a token, the best choice is the Bearer authentication scheme. Nevertheless, nothing prevent you from using a custom scheme that could fit on your requirements.

[source](https://stackoverflow.com/questions/34013299/web-api-authentication-basic-vs-bearer#:~:text=2%20Answers&text=The%20Basic%20and%20Digest%20authentication,is%20described%20by%20the%20RFC6750.)

### What does the JSON Web Token package do?

JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

[source](https://jwt.io/introduction/#:~:text=JSON%20Web%20Token%20(JWT)%20is,because%20it%20is%20digitally%20signed.)

### What considerations should we make when creating and storing a SECRET?

since its a two part key in authorizing a user to an app, it should be not guesable nor should it ever be able to be seen on the client side.

*encryption*

Using a systematic srambling of cyphers so that information canot easily be used by unathorized people.

*token*

A sign of a succesful sign in we can use to authenticate on 

*bearer*

The beared of a token to be used to grant acces to a system.

*secret*

The client_secret is a secret known only to the application and the authorization server. It must be sufficiently random to not be guessable, which means you should avoid using common UUID libraries which often take into account the timestamp or MAC address of the server generating it. A great way to generate a secure secret is to use a cryptographically-secure library to generate a 256-bit value and converting it to a hexadecimal representation.

[source](https://www.oauth.com/oauth2-servers/client-registration/client-id-secret/)

*JSON Web Token*

JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

Although JWTs can be encrypted to also provide secrecy between parties, we will focus on signed tokens. Signed tokens can verify the integrity of the claims contained within it, while encrypted tokens hide those claims from other parties. When tokens are signed using public/private key pairs, the signature also certifies that only the party holding the private key is the one that signed it.

[source](https://jwt.io/introduction/)

[Home](https://401repo.github.io/401RN/README)