# JWT
JSON Web Token (JWT) is currently the most popular cross-domain authentication solution.
It consists of three part `Header`,`Payload`,`Signature`.
##Header
It contains the type and the algorithm utilized to sign signature and etc.
```
{
"TYP":"JWT",
"ALG":"SHA256"
}
```

## Payload
It contains the detailed information of token such as the issuer of JWT, the expiration of the token and etc.
```
{
"ISS":"JUNYEMAO",
"EXP":"Today"
}
```

## Signature
It is encrypted by the secret key stored in the JWT generator with the information in the Header and Payload.
You can use SHA 1,2,256 etc to encrypt it.

## Process Flow
First client service will send requst to server with its Account,password and key information include.
Server accepts the request and use secret key to generate a token(Signature) with specialised encryption algorithm.
Then,server and user use this token to make communication.
