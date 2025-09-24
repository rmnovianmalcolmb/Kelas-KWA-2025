# No Way Jose
Let's look at JWT algorithms. The first part of a JWT is the JOSE header, and when you decode it, looks like this:

`{"typ":"JWT","alg":"HS256"}`

This tells the server it's a JWT and which algorithm to use to verify it. Can you see the issue here? The server has to process this untrusted input before it is actually able to verify the integrity of the token! In ideal cryptographic protocols, you verify messages you receive before performing any further operations on them, otherwise in Moxie Marlinspike's words, "it will somehow inevitably lead to doom".
The "none" algorithm in JWTs is a case in point. The link below takes you to a page where you can interact with a broken session API, which emulates a vulnerability that existed in a lot of JWT libraries. Use it to bypass authorisation and get the flag.

Link challenge: https://cryptohack.org/challenges/web/

### Writeup
1. Diberikan web, kita dapat input token dan username
<img width="2559" height="1414" alt="image" src="https://github.com/user-attachments/assets/da8145be-9590-44ed-a34f-fbdb25e3cf32" />

2. Input `admin` ke username dan mendapat session
<img width="2513" height="1353" alt="image" src="https://github.com/user-attachments/assets/8b2cf04f-f400-4a3d-8a5c-6fa8fd0bbac0" />

3. Saat didecode ternyata admin false
<img width="2287" height="1041" alt="image" src="https://github.com/user-attachments/assets/baed6359-30b7-4d06-acd2-8f89370e25b2" />

4. Edit admin jadi true dan alg jadi none
<img width="2246" height="803" alt="image" src="https://github.com/user-attachments/assets/271e18ac-b27e-42e2-98e0-d15d84353d09" />

5. Masukkan JWT dan dapat flagnya
<img width="2477" height="1317" alt="image" src="https://github.com/user-attachments/assets/5f0c55b2-a0f1-4be2-8a7e-015cad75d14a" />
