# JWT Secrets
The most common signing algorithms used in JWTs are HS256 and RS256. The first is a symmetric signing scheme using a HMAC with the SHA256 hash function. The second is an asymmetric signing scheme based on RSA.
A lot of guides on the internet recommend using HS256 as it's more straightforward. The secret key used to sign a token is the same as the key used to verify it.
However, if the signing secret key is compromised, an attacker can sign arbitrary tokens and forge sessions of other users, potentially causing total compromise of a webapp. HS256 makes the secret key harder to secure than an asymmetric keypair, as the key must be available on all servers that verify HS256 tokens (unless better infrastructure with a separate token verifying service is in place, which usually isn't the case). In contrast, with the asymmetric scheme of RS256, the signing key can be better protected while the verifying key is distributed freely. Even worse, developers sometimes use a default or weak HS256 secret key.
Here is a snippet of source code with one function to create a session and another function to authorise a session and check for admin permissions. But there's a strange comment about the secret key. What are you going to do?
Play at https://web.cryptohack.org/jwt-secrets

Link challenge: https://cryptohack.org/challenges/web/

### Writeup
1. Diberikan sebuah web, dapat clue untuk membaca PyJWT readme key
<img width="2474" height="1312" alt="image" src="https://github.com/user-attachments/assets/ec2e8b61-17e8-43f7-b2db-b90a611ff744" />

2. Di PyJWT readme didapat key `secret`
<img width="1089" height="304" alt="image" src="https://github.com/user-attachments/assets/6f8cc1d7-5e8c-435c-b9b7-7d4500bd20fc" />

3. Buat JWT dengan kode berikut
<img width="1820" height="1293" alt="image" src="https://github.com/user-attachments/assets/99c8d986-ebe6-4257-ae26-e5a1cced4e33" />

4. Masukkan token ke web dan dapatkan flagnya
<img width="2467" height="1298" alt="image" src="https://github.com/user-attachments/assets/1e93d87e-dcab-424d-8b8a-187a9a8f378b" />
