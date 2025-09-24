# Forged Coupon
Forge a coupon code that gives you a discount of at least 80%.

Link challenge: http://localhost:3000/#/score-board?categories=Cryptographic%20Issues

### Writeup
1. Sebelum menyelesaikan challenge ini kita harus menyelesaikan challenge `Forgotten Sales Backup` terlebih dahulu
<img width="735" height="270" alt="image" src="https://github.com/user-attachments/assets/e7e795d0-37d7-4c4d-8141-66f4ec31f5ff" />

2. Untuk menyelesaikan challenge tersebut kita hanya perlu mendownload file `coupons_2013.md.bak` berekstensi `.bak` yang menandakan file backup dari `/ftp`
<img width="2559" height="556" alt="image" src="https://github.com/user-attachments/assets/30e1943a-1f4a-44db-9919-578d4b85d0b4" />

3. Dalam file tersebut terdapat beberapa kode kupon
<img width="201" height="496" alt="image" src="https://github.com/user-attachments/assets/0335ec9d-578c-4d90-987c-1c19bed15ef6" />

4. Saat didecode menggunakan Z85 ditemukan bahwa format kuponnya adalah (BULAN)(TAHUN)-(DISKON)
<img width="2545" height="1332" alt="image" src="https://github.com/user-attachments/assets/a598a4d7-19c2-41d8-a8c9-c9168d676c8a" />

5. Saya membuat kupon bernama `SEP25-99` yang saya encode dengan Z85 menjadi `q:<Irh7Z*G`
<img width="2519" height="1347" alt="image" src="https://github.com/user-attachments/assets/07a78c5a-f382-4182-b1fe-6780164eb591" />

6. Saya memasukkan kupon saat checkout sebagai jim
<img width="2549" height="1359" alt="image" src="https://github.com/user-attachments/assets/17ab7397-7964-4d86-91f1-4171feea7c75" />

<img width="2511" height="1364" alt="image" src="https://github.com/user-attachments/assets/bfa37e40-3fa5-4b4c-9dfc-8d03afcfac6c" />

7. Challenge selesai
<img width="2518" height="1196" alt="image" src="https://github.com/user-attachments/assets/a8fa5d2a-6183-456b-9a49-504d21c6adbe" />
