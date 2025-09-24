# Imaginary Challenge
Solve challenge #999. Unfortunately, this challenge does not exist.

Link challenge: http://localhost:3000/#/score-board?categories=Cryptographic%20Issues

### Writeup
1. Saat menyelesaikan sebuah challenge terdapat cookie bernama `continueCode`
<img width="2542" height="1354" alt="image" src="https://github.com/user-attachments/assets/c79fd509-45d9-44e7-b90c-cfee6afb0dc7" />

2. Jika membuka file `package.json.bak` dari endpoint `/ftp` ditemukan bahwa web menggunakan library `hashid`
<img width="2498" height="1309" alt="image" src="https://github.com/user-attachments/assets/cca5f812-7b5a-42df-86a4-503cdb3c1224" />

3. Jika kita melakukan PUT request dengan `http://localhost:3000/rest/continue-code/apply/(continueCode)` kita akan dianggap menyelesaikan challenge sesuai dengan continueCode
<img width="1781" height="1326" alt="image" src="https://github.com/user-attachments/assets/93040c5a-927a-42ac-a98f-e66665020463" />

4. Karena panjang continueCodenya adalah 60 karakter dan salt yang dipakai sebagai demo di library `hashid` adalah `this is my salt` maka kita lakukan hal yang sama dengan melakukan hash pada angka `999`
<img width="1692" height="1316" alt="image" src="https://github.com/user-attachments/assets/e92c2cf9-3c15-4042-869b-332107ab52e8" />

<img width="1674" height="1224" alt="image" src="https://github.com/user-attachments/assets/97f56dcd-874e-470a-8260-c25c88432e48" />

5. Challenge selesai
<img width="1906" height="77" alt="image" src="https://github.com/user-attachments/assets/882f7f5d-cde1-4708-a254-81206a29589f" />
