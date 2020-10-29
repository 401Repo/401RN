[Home](https://401repo.github.io/401RN/README)

# Readings: OAuth

![Source](https://i.ytimg.com/vi/CPbvxxslDTU/maxresdefault.jpg)

## Why is authentication important?

So that we cn establish a user session was valid and we can take the info and create a way to verify a user across multiple services.

## Why should we be careful about storing a user’s password?

Because we never want anyone but the user to know it. We hash it to compare but we never actually keep it saved. it only exist duing the signing in/up process.

## What is the difference between hashing and encryption?

>Encryption is a two-way function; what is encrypted can be decrypted with the proper key. Hashing, however, is a one-way function that scrambles plain text to produce a unique message digest. With a properly designed algorithm, there is no way to reverse the hashing process to reveal the original password. An attacker who steals a file of hashed passwords must then guess the password.

[source](https://gcn.com/articles/2013/12/02/hashing-vs-encryption.aspx#:~:text=Encryption%20is%20a%20two%2Dway,to%20reveal%20the%20original%20password.)

## What is the difference between encryption and encoding?

Encoding: Reversible transformation of data format, used to preserve usability of data.

Encryption: Secure encoding of data used to protect confidentiality of data.

[source](https://www.packetlabs.net/encryption-encoding-and-hashing/#:~:text=Encoding%3A%20Reversible%20transformation%20of%20data,to%20protect%20confidentiality%20of%20data.)

## What is a token used for?

Token proves that a succesful session was done and we can use our proved credentials on one si

*authentication*

The user signs in and creates a valid sign in session token to use with approved credentials

*authorization*

a token shows a user validated data and its used to authorize access to data

*encryption*

Encryption: Secure encoding of data used to protect confidentiality of data.

*hashing*

One-way function that scrambles plain text to produce a unique message digest.

*session*

a user logged in and creates a user session

*token*

The token endpoint is where apps make a request to get an access token for a user. This section describes how to verify token requests and how to return the appropriate response and errors.

*encoding*

Encoding: Reversible transformation of data format, used to preserve usability of data.

*secret*

secret is stored in a microprocessor that has no ability for anything to programmatically extract it, where that microprocessor can cryptographically sign data instead of sending the secret itself.

*cryptography*

Secure encoding of data used to protect confidentiality of data.

[source](https://www.oauth.com/oauth2-servers/client-registration/client-id-secret/)

*Client Secret*

The client_secret is a secret known only to the application and the authorization server. It must be sufficiently random to not be guessable, which means you should avoid using common UUID libraries which often take into account the timestamp or MAC address of the server generating it. A great way to generate a secure secret is to use a cryptographically-secure library to generate a 256-bit value and converting it to a hexadecimal representation.

[source](https://www.oauth.com/oauth2-servers/client-registration/client-id-secret/)

*Authentication Endpoint*

Authorization/Authentication Endpoint
The authorization endpoint can be used to request either access tokens or authorization codes (implicit and authorization code flow). You either use a web browser or a web view to start the process.

[source](https://identityserver.github.io/Documentation/docsv2/endpoints/authorization.html)

*API Endpoint*

The routes from which we can send the data (or errors) back from the requests.

*Authorization Code*

An authorization code is an alphanumeric password that authorizes its user to purchase, sell or transfer items, or to enter information into a security-protected space.

[source](https://identityserver.github.io/Documentation/docsv2/endpoints/authorization.html)

*Access Token*

we use an authorization code in an access token for a request to an api.

[Home](https://401repo.github.io/401RN/README)