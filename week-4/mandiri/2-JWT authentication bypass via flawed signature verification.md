# JWT authentication bypass via flawed signature verification
This lab uses a JWT-based mechanism for handling sessions. The server is insecurely configured to accept unsigned JWTs.
To solve the lab, modify your session token to gain access to the admin panel at /admin, then delete the user carlos.
You can log in to your own account using the following credentials: wiener:peter

Link challenge: https://portswigger.net/web-security/jwt/lab-jwt-authentication-bypass-via-flawed-signature-verification

### Writeup
1. Setelah login sebagai wiener, cek cookie session, ditemukan `"sub":"wiener"`, ubah ke `"sub":"administrator"`
<img width="2452" height="1127" alt="image" src="https://github.com/user-attachments/assets/4d6822ac-b374-4f08-b923-ccbf5b2e9620" />

2. Pada header, ubah `"alg":"RS256"` ke `"alg":"none"` agar tidak perlu verifikasi
<img width="2452" height="1126" alt="image" src="https://github.com/user-attachments/assets/dfe93132-fc0e-43ad-b05e-fa7b479d322b" />

<img width="2454" height="1130" alt="image" src="https://github.com/user-attachments/assets/6a96f92a-9a2f-456e-912c-25dbb00446d7" />

3. Hapus signature dari JWT
<img width="2448" height="1132" alt="image" src="https://github.com/user-attachments/assets/b9ee2d1f-e76e-4091-adc4-7996e15bce38" />

<img width="1836" height="1130" alt="image" src="https://github.com/user-attachments/assets/5a31fe72-421c-4826-97f7-6ec4515c04cc" />

4. Perbarui session dan hapus akun carlos
<img width="2536" height="1279" alt="image" src="https://github.com/user-attachments/assets/e54ccfe3-2d49-4a5b-9f58-7f1e38890429" />
