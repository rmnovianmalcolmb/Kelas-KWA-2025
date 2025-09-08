# Database Schema

Link Resource: https://juice-shop.herokuapp.com/#/score-board?categories=Injection&showDisabledChallenges=false

### Jawaban

1. Search akan memunculkan produk yang memiliki nama atau description yang sesuai dengan keyword yang dicari
<img width="1837" height="1040" alt="image" src="https://github.com/user-attachments/assets/727a4f55-60a6-48d3-86ff-d9b0bc854530" />

<img width="1847" height="927" alt="image" src="https://github.com/user-attachments/assets/b1521654-8049-47b2-8e0f-acec7b92c22f" />

<img width="1829" height="738" alt="image" src="https://github.com/user-attachments/assets/3715e2d2-a1e3-45ec-94c6-722a119caf43" />

2. Setelah dicek ternyata ada 9 column di database
<img width="1825" height="825" alt="image" src="https://github.com/user-attachments/assets/2903a0f7-94f3-4f61-9834-6b9d8b1897eb" />

3. Masukkan payload
`
'))+UNION+SELECT+sql,2,3,4,5,6,7,8,9+FROM+sqlite_master--
` dan berhasil mendapatkan database schemanya
<img width="1832" height="909" alt="image" src="https://github.com/user-attachments/assets/fdecfda6-e1a5-473c-9c92-1b6d206e9041" />

<img width="1825" height="904" alt="image" src="https://github.com/user-attachments/assets/d4e60d8e-f751-4573-977a-06b7b3f1ad33" />
