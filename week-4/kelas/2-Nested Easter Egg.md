# Nested Easter Egg
Apply some advanced cryptanalysis to find the real easter egg.

Link challenge: http://localhost:3000/#/score-board?categories=Cryptographic%20Issues

### Writeup
1. Challenge ini merupakan lanjutan dari challenge `Easter Egg` pada section Broken Access Control, dimana kita mendapatkan sebuah file pdf
<img width="727" height="336" alt="image" src="https://github.com/user-attachments/assets/32af441b-1f8f-4628-9b6d-8b6a32c56a35" />

<img width="523" height="130" alt="image" src="https://github.com/user-attachments/assets/8c5318f2-5529-4caa-8a3b-419d411076df" />

2. File pdf tidak bisa dibuka secara normal jadi saya membukanya melalui hex editor
<img width="2542" height="1409" alt="image" src="https://github.com/user-attachments/assets/eac5b2d7-2d5f-4a71-9582-a693c79f19f8" />

<img width="1773" height="922" alt="image" src="https://github.com/user-attachments/assets/91e1ca16-0099-42f0-a124-48dab2294e9e" />

3. Saat melakukan decrypt dengan base64 ditemukan hasil berikut
<img width="2551" height="1238" alt="image" src="https://github.com/user-attachments/assets/da41bfbd-4eb0-4e31-8143-d11df62f0a28" />

4. Saat mencoba dimasukkan ke url tidak terjadi apa-apa
<img width="2559" height="1411" alt="image" src="https://github.com/user-attachments/assets/6a2da2b3-ede7-46bb-9d34-d521939c9865" />

5. Saya melakukan decrypt lagi dengan ROT13
<img width="2559" height="1279" alt="image" src="https://github.com/user-attachments/assets/9b4e754c-1ea1-4429-82bc-0a9933cbc45e" />

6. Saat dimasukkan ke url muncul ini dan challenge selesai
<img width="2559" height="1422" alt="image" src="https://github.com/user-attachments/assets/7de68b7c-a905-4126-9a2d-b320123e6c79" />

<img width="2285" height="109" alt="image" src="https://github.com/user-attachments/assets/382c12ab-9a17-4d24-8764-eba7d5da8eb7" />

