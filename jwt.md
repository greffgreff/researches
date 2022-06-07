# Json Web Token

<br />

### Introduction
This research aims to understand how authorization works with json web tokens and identify wether they are suitale in the context of Rently's backend. To achieve this, the research was done through a combination of *literary study*, *pro and con compariosons*, and *available product analysis*.

At the end of this research, we will have answered:
1. What are Json Web Tokens?
2. What are the benefits and disadvantages for using them?
3. Are there any alternatives?
4. Are JWTs suitable for Rently?

<br />

### 1. What are Json Web Tokens?
According to [jwt.io](https://jwt.io/introduction), JWT aim to make the transfer of data more secure:
> JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object.

JWTs are commonly used for authorization purposes and perhaps session management after a successful login:
> Authorization: This is the most common scenario for using JWT. Once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token.

JWTs are base64 encoded plain json objects using a combination of some form of secret and a hasing algorithum: 
> This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

[auth0.com](https://auth0.com/learn/json-web-tokens/) suggests that JWTs can be used within a request URL, headers, perhaps as a substitute to putting raw JSON objects in requests' body:
> Because of its size, it can be sent through an URL, POST parameter, or inside an HTTP header. Additionally, due to its size its transmission is fast.

JWTs are composed of three parts, a header containing information about the encryption algorithm, a payload containing key value pairs known as claims, and a signature which is generated using the previous sections along side a secret and encrypted using the headers algorithm: 
> The header typically consists of two parts: the type of the token, which is JWT, and the signing algorithm being used, such as HMAC SHA256 or RSA.
> The second part of the token is the payload, which contains the claims. Claims are statements about an entity (typically, the user) and additional data
> To create the signature part you have to take the encoded header, the encoded payload, a secret, the algorithm specified in the header, and sign that.

Together, JWT are formed like so [medium.com](https://medium.com/deno-the-complete-reference/sign-verify-jwt-hmac-sha256-4aa72b27042a):
```
JWT=base64URLEncode(header)+’.’+base64URLEncode(payload)+’.’+base64URLEncode(signature)
```

According to [this](https://stackoverflow.com/questions/38725038/c-sharp-how-to-verify-signature-on-jwt-token), the third part of JWTs, the signature, is verified on the receiving endpoint by computing a signature like above and comparing it to the original signature from the request.

<br />

### 2. What are the benefits and disadvantages for using them?

#### Pros
According to [fusionauth.com](https://fusionauth.io/learn/expert-advice/tokens/pros-and-cons-of-jwts):
- JWTs are signed cryptographically. Hacking a JWT to recover a secret is a very slow process process.

According to [auth0.com](https://auth0.com/docs/secure/tokens/token-best-practices):
- JWTs provide a stateless session management, meaning that no data is retained on the server-side about a given user
- JWTs verification are easily deployed across multiple backend services. 
- One JWT is valid across multiple servers.

#### Cons
According to [fusionauth.com](https://fusionauth.io/learn/expert-advice/tokens/pros-and-cons-of-jwts):
- All services that wish to verify JWTs (signed with HMAC algorithms specifically) must have a secret stored somewhere and so is less secure.
- JWTs have a fixed expiration date and time. Once a session is terminated (e.g. user logging out), a JWT could still be valid and could be used to forge requests.

<br />

### 3. Are there any alternatives?
In the context of session management and authorization, sessions cookies are by far the most widespread.

Session cookies are a piece of string that a server can associate to a user/client upon a request. 

According to [medium.com](https://medium.com/@prashantramnyc/difference-between-session-cookies-vs-jwt-json-web-tokens-for-session-management-4be67d2f066e), a session cookie is generated on the server and stores a session's information on a dedicated database, as opposed to a client's device in an encrypted JWT.
> In case of the session cookie based approach, the sessionId does not contain any userId information, but is a random string generated and signed by the “secret key”. The sessionId is then saved within a sessionDB.

<br />

### 4. Are JWTs suitable for Rently?
Given that Rently is a project with no budget and limited time, JWTs are perfectly suitable for it for session management. Unlike alternatives, the implementation of JWTs within the project would require much less development time. Since Rently already operates multiple services deployed on different SaaP, configuring a connection to a database on all services requires more development time. Additionally, no dedicated database is needed to facilitate session cookies for example.

<br />

### Works cited
[JWTs in essence](https://jwt.io/introduction) &nbsp; &nbsp;
[When are JWT suitable?](https://auth0.com/learn/json-web-tokens/) &nbsp; &nbsp;
[JWTs formed](https://medium.com/deno-the-complete-reference/sign-verify-jwt-hmac-sha256-4aa72b27042a) &nbsp; &nbsp;
[Disadantages](https://fusionauth.io/learn/expert-advice/tokens/pros-and-cons-of-jwts) &nbsp; &nbsp;
[Advantages](https://auth0.com/docs/secure/tokens/json-web-tokens) &nbsp; &nbsp;
[JWTs stateless](https://auth0.com/docs/secure/tokens/token-best-practices) &nbsp; &nbsp;
[Session cookies](https://medium.com/@prashantramnyc/difference-between-session-cookies-vs-jwt-json-web-tokens-for-session-management-4be67d2f066e)
