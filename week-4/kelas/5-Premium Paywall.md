# Premium Paywall
Unlock Premium Challenge to access exclusive content.

Link challenge: http://localhost:3000/#/score-board?categories=Cryptographic%20Issues

### Writeup
1. Jika melakukan inspect pada section challenge tersebut ditemukan comment berisi sesuatu yang terenkripsi
<img width="2527" height="1421" alt="image" src="https://github.com/user-attachments/assets/a5a24832-cbd9-4294-bf80-2fdc294841e9" />

2. Agar bisa melakukan decrypt pada comment tersebut diperlukan sebuah key, untuk menemukan keynya kita perlu mencari dimana key itu berada. Setelah melakukan scan dengan ZAP ditemukan endpoint `/encryptionkeys`
<img width="2554" height="1454" alt="image" src="https://github.com/user-attachments/assets/623fc9e7-d267-42b6-a201-57380b30b397" />

<img width="2559" height="1424" alt="image" src="https://github.com/user-attachments/assets/7a9e4711-94bd-4932-9c40-f9cb1f74cd40" />

<img width="843" height="103" alt="image" src="https://github.com/user-attachments/assets/26770361-517c-4d23-a585-8d69d7c98582" />

3. Pakai key tersebut untuk decrypt AES 256 dengan command `echo "IvLuRfBJYlmStf9XfL6ckJFngyd9LfV1JaaN/KRTPQPidTuJ7FR+D/nkWJUF+0xUF07CeCeqYfxq+OJVVa0gNbqgYkUNvn//UbE7e95C+6e+7GtdpqJ8mqm4WcPvUGIUxmGLTTAC2+G9UuFCD1DUjg==" | openssl enc -d -aes-256-cbc -K EA99A61D92D2955B1E9285B55BF2AD42 –iv 337133713371337 -a –A`
<img width="2294" height="269" alt="image" src="https://github.com/user-attachments/assets/d21df2c8-a547-463b-8dd3-f9fc9f8f5990" />

4. Masukkan ke url `this/page/is/hidden/behind/an/incredibly/high/paywall/that/could/only/be/unlocked/by/sending/1btc/to/us` dan challenge selesai
<img width="2558" height="1422" alt="image" src="https://github.com/user-attachments/assets/34136c80-fbb6-4483-b8f0-88628f265892" />

<img width="1948" height="82" alt="image" src="https://github.com/user-attachments/assets/dc0e71b0-366f-4ccb-aee1-9230fec9bfea" />
