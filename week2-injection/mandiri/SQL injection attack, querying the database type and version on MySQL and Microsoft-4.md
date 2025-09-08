# SQL injection attack, querying the database type and version on MySQL and Microsoft

Link: https://portswigger.net/web-security/sql-injection/examining-the-database/lab-querying-database-version-mysql-microsoft

### Jawaban
1. Melakukan `ORDER BY` untuk menemukan berapa jumlah column untuk request filter category dan ditemukan saat `'ORDER BY 3#` terjadi error maka columnnya berjumlah 2
<img width="2494" height="1340" alt="image" src="https://github.com/user-attachments/assets/a233b1ed-1636-496f-ab5c-c79c5bc45450" />

<img width="2502" height="625" alt="image" src="https://github.com/user-attachments/assets/75c32469-60fc-43fc-9ad6-92537c8b82fc" />

2. Mengambil data version dengan `%27+UNION+SELECT+@@version,+NULL%23`
<img width="1349" height="600" alt="image" src="https://github.com/user-attachments/assets/74585b95-9193-4017-9117-4c750585ef74" />

<img width="1865" height="1317" alt="image" src="https://github.com/user-attachments/assets/bc8dd058-54a9-4a6b-8656-1c56603ebf0c" />
