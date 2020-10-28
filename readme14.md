[Home](https://401repo.github.io/401RN/README)

# Readings: Bearer Authorization

![Source](https://cdn.ppolyzos.com/wp-content/uploads/2017/10/jwt-support-swagger-aspnet-core.png)

### Write the following steps in the correct order:

Ask the client if they want to sign in via a third party
Receive access token
Make a request to the access token endpoint
Register your application to get a client_id and client_secret
Receive authorization code
Redirect to a third party authentication endpoint
Make a request to a third-party API endpoint

What can you do with an authorization code?
What can you do with an access token?

Its a way of saying "i grant access to the holder of this code" and the token is a sign that an authorized sign in was done.

What’s a benefit of using OAuth instead of your own basic authentication?

It is an api built in functionality that does all of the user security credential handling without giving out the password out, and the best part is that it saves us the effort to code it for ourselves.

*Client ID*

The client_id is a public identifier for apps. Even though it’s public, it’s best that it isn’t guessable by third parties, so many implementations use something like a 32-character hex string. It must also be unique across all clients that the authorization server handles. If the client ID is guessable, it makes it slightly easier to craft phishing attacks against arbitrary applications.

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