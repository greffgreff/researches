# Json Web Token

### Introduction
This research aims to understand how authorization works with json web tokens and identify wether they are suitale in the context of Rently's backend. To achieve this, the research was done through a combination of *literary study*, *pro and con compariosons*, and *available product analysis*.

At the end of this research, we will have answered:
1. What are Json Web Tokens?
2. What are the benefits and disadvantages for using them?
3. Are there any alternatives?
4. Are JWTs suitable for Rently?

### 1. What are Json Web Tokens?
According to [jwt.io](https://jwt.io/introduction), JWT aim to make the transfer of data more secure:
> JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object.

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

### 2. What are the benefits and disadvantages for using them?

### Works cited
[what are jwt](https://jwt.io/introduction)
[where to use](https://auth0.com/learn/json-web-tokens/)
[how are they formed](https://medium.com/deno-the-complete-reference/sign-verify-jwt-hmac-sha256-4aa72b27042a)
