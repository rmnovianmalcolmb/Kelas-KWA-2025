# Token Appreciation
JavaScript Object Signing and Encryption (JOSE) is a framework specifying ways to securely transmit information on the Internet. It's most well-known for JSON Web Tokens (JWTs), which are used to authorise yourself on a website or application. JWTs typically do this by storing your "login session" in your browser after you have authenticated yourself by entering your username and password. In other words, the website gives you a JWT that contains your user ID, and can be presented to the site to prove who you are without logging in again. JWTs look like this:
`eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJmbGFnIjoiY3J5cHRve2p3dF9jb250ZW50c19jYW5fYmVfZWFzaWx5X3ZpZXdlZH0iLCJ1c2VyIjoiQ3J5cHRvIE1jSGFjayIsImV4cCI6MjAwNTAzMzQ5M30.shKSmZfgGVvd2OSB2CGezzJ3N6WAULo3w9zCl_T47KQ`

You can recognise it because it's base64-encoded data split into three parts (separated by a .): the header, the payload, and the signature. In fact, it's a variant of base64 encoding, where the + and / have been replaced by different special characters since they can cause issues in URLs.
Some developers believe that the JWT encoding is like encryption, so they put sensitive data inside the tokens. To prove them wrong, decode the JWT above to find the flag. There are online tools to do this quickly, but working with Python's PyJWT library will prepare you best for future challenges.

Link challenge: https://cryptohack.org/challenges/web/

### Writeup
1. Didapatkan sebuah JWT Token
<img width="1861" height="1180" alt="image" src="https://github.com/user-attachments/assets/1c65d977-84c3-419d-bdc4-882cb3374acc" />

2. Decode JWT Tokennya dan flag didapatkan
<img width="2273" height="1254" alt="image" src="https://github.com/user-attachments/assets/2192d2d2-891b-4786-be7d-cd16a589cc30" />
