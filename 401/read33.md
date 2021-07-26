# A Production Stack
- A production setup usually consists of multiple components, each designed and built to be really good at one specific thing. They are fast, reliable and very focused.

- When a request arrives at server, it should be passed to a dedicated web server. Nginx is an example for a good web server.

### How Does Django Fit In?
- This function calls the code, and produces a response object which is passed to the WSGI server. There the response is translated into a HTTP response and is passed back to the web server, which finally delivers it to the user.


# How to Use JWT Authentication with Django REST Framework?

![](https://simpleisbetterthancomplex.com/media/2018/12/featured-jwt.jpg)

- JWT stand for JSON Web Token and it is an authentication strategy used by client/server applications where the client is a Web application using JavaScript and some frontend framework like Angular, React or VueJS.

### How JWT Works?
- The JWT is just an authorization token that should be included in all requests:
- <curl http://127.0.0.1:8000/hello/ -H 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ0b2tlbl90eXBlIjoiYWNjZXNzIiwiZXhwIjoxNTQzODI4NDMxLCJqdGkiOiI3ZjU5OTdiNzE1MGQ0NjU3OWRjMmI0OTE2NzA5N2U3YiIsInVzZXJfaWQiOjF9.Ju70kdcaHKn1Qaz8H42zrOYk0Jx9kIckTn9Xx7vhikY'
>

- The JWT is acquired by exchanging an username + password for an access token and an refresh token.



# What is JSON Web Token?
- JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed.

### When should we use JSON Web Tokens?

- - Authorization:Once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token.

- - Information Exchange: JSON Web Tokens are a good way of securely transmitting information between parties. Because JWTs can be signed—for example, using public/private key pairs—you can be sure the senders are who they say they are.

### What is the JSON Web Token structure?

- JSON Web Tokens consist of three parts separated by dots (.), which are:
- - Header
- - Payload
- - Signature

##### Header:
- The header typically consists of two parts: the type of the token, which is JWT, and the signing algorithm being used, such as HMAC SHA256 or RSA.

##### Payload:
- The second part of the token is the payload, which contains the claims. Claims are statements about an entity (typically, the user) and additional data. There are three types of claims: registered, public, and private claims.

##### Signature:
- To create the signature part we have to take the encoded header, the encoded payload, a secret, the algorithm specified in the header, and sign that.