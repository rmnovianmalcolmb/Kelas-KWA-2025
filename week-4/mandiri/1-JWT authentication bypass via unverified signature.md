# JWT authentication bypass via unverified signature
This lab uses a JWT-based mechanism for handling sessions. Due to implementation flaws, the server doesn't verify the signature of any JWTs that it receives.
To solve the lab, modify your session token to gain access to the admin panel at /admin, then delete the user carlos.
You can log in to your own account using the following credentials: wiener:peter

Link challenge: https://portswigger.net/web-security/jwt/lab-jwt-authentication-bypass-via-unverified-signature

### Writeup
1. Setelah login sebagai wiener, cek cookie session, ditemukan `"sub":wiener`
<img width="2453" height="784" alt="image" src="https://github.com/user-attachments/assets/5365b851-a02e-43f9-8190-cc2df98e4715" />

2. Saat mencoba `/admin` tidak bisa
<img width="1836" height="1126" alt="image" src="https://github.com/user-attachments/assets/be75c124-4325-429c-924d-ddbf6d4935b1" />

3. Ubah `"sub":wiener` menjadi `"sub":administrator` dan `/admin` bisa diakses
<img width="2459" height="1132" alt="image" src="https://github.com/user-attachments/assets/0611d4dc-ed98-40af-9ca1-13e85d11e353" />

<img width="2543" height="1341" alt="image" src="https://github.com/user-attachments/assets/f84c4f84-83fa-4465-95fc-985146528c18" />

4. Hapus akun carlos dan challenge selesai
<img width="2545" height="1343" alt="image" src="https://github.com/user-attachments/assets/04c66080-ce50-46b1-80cb-da95db885659" />
