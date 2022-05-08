# Claims

## Introduction

Authorization is a process of determining whether the user is able to access the system resource.
The identity membership system allows us to map one or more roles with the user;  based on the role, we can do authorization.

## Claim-based authorization
Claims are the user data and they are issued by a trusted source. If we are working with token-based authentication, a claim may be added within a token by the server that generates the token. A claim can have any kind of data such as "DateOfJoining", "DateOfBirth", "email", etc. Based on a claim that a user has, a system provides the access to the page, which is called Claim based authorization. For example, the system will provide access to the  page, if the user has a "DateOfBirth" claim. In short, claim based authorization checks the value of the claim and allows access to the system resource based on the value of a claim.

## Policy-based authorization
 
The .NET Core Framework allows us to create policies to authorization. We can either use pre-configured policies or can create a custom policy based on our requirement.
 
## Authorization Requirements
 
The requirement is the collection of data which can be used to evaluate the user principal. To create the requirement, the class must implement interface IAuthorizationRequirement that is an empty interface.

## Authorization handlers
 
The authorization handler contains the evaluation mechanism for properties of requirement. The handler must evaluate the requirement properties against the AuthorizationContext and decide if the user is allowed to access the system resources or not. One requirement may have multiple handlers. The authorization handler must inherit from AuthorizationHandler<T> class; here T is a type of requirement class.

## Handler registration
 
The handle that is using authorization must register in service collection. We can add the service collection by using "services.AddSingleton<IAuthorizationHandler, ourHandlerClass>()" method where we need to pass handler class.

***To learn More*** [Claims](https://www.c-sharpcorner.com/article/claim-based-and-policy-based-authorization-with-asp-net-core-2-1/).


# JWT 

## What is a JWT?
JSON Web Tokens are an open and standard (RFC 7519) way for you to represent your user’s identity securely during a two-party interaction. That is to say, when two systems exchange data you can use a JSON Web Token to identify your user without having to send private credentials on every request.

## The structure of the token
The token itself, returned by the API is (simply put) an encoded string. It comprises three different sections, separated from each other by a dot character:

```header.payload.signature```

Each section contains a vital piece of the puzzle. Once decoded, the first two will be JSON representations of data, containing relevant information, and the last one will be used to verify the authenticity of the token:

* **The header** will contain data related to the type of token we’re dealing with and the algorithm used for its generation. There are several compatible algorithms to be specified here, but the most common ones are HS256 and RS256. It’ll depend on what security standards and measures you’re looking for. In these two examples, one uses a secret key known by both the server and the client and the other one uses a private key used by the server in combination with a public key known by the client.
* **The payload** will contain data pertaining to the request and the user making it. There are a set of standard key/value pairs that are defined as part of JWT which you can use on your implementation, such as:
* **Sub** (subject)- in other words, a way to identify the user making the request/being authenticated
* **Iss** (issuer)- or rather, the server that issued the token. In our case, it would probably make sense to include the URI used.
* **Aud** (audience)- it tried to provide some form of identification of the recipient of this token
* **Exp** (expiration date)- the tokens usually don’t last forever, this is to ensure that whoever is using it, is actually providing a recently generated token

* **The signature** is just an encoded string, used by both the server and the client to verify the authenticity of the payload.

## Abstract

JSON Web Token (JWT) is a compact, URL-safe means of representing
claims to be transferred between two parties.  The claims in a JWT
are encoded as a JSON object that is used as the payload of a JSON
Web Signature (JWS) structure or as the plaintext of a JSON Web
Encryption (JWE) structure, enabling the claims to be digitally
signed or integrity protected with a Message Authentication Code
(MAC) and/or encrypted.


## Producer and Consumer concept of API’s

* **Producer** is the one who gives a service. It will be the provider(Server) of the API(s) which are JWT protected.

* **Consumer** is the one who uses it. It will be the customer(Server/Mobile App/ Web App/ Client) who will be providing the valid JWT token to consume the API(s) being provided by the Producer.