# NoSQL Manipulation

Link Resource: https://juice-shop.herokuapp.com/#/score-board?categories=Injection&showDisabledChallenges=false

### Jawaban

1. Saat menambahkan review, ubah requestnya dari `PUT` ke `PATCH` dan tambahkan `{"$ne":-1}` agar mengubah semua review yang ada menjadi message yang dimasukkan
<img width="1833" height="1132" alt="image" src="https://github.com/user-attachments/assets/2da64aeb-02d9-4bb4-babf-4a8400f38e15" />

<img width="1834" height="1115" alt="image" src="https://github.com/user-attachments/assets/26ed31ea-a46b-4232-9029-750f6d027fb0" />
