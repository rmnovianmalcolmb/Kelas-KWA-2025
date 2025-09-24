# baby-web

Link Challenge : http://localhost:10009/

### Writeup

1. Jika dibuka source codenya terlihat bahwa input yang dimasukkan harus mengandung `key` agar mendapat flag
<img width="1341" height="241" alt="image" src="https://github.com/user-attachments/assets/237cb056-f50b-464a-a6b2-95b9ee6d792b" />

2. Jika dicek keynya adalah string `randomBytes(16).toString('hex')`
<img width="733" height="53" alt="image" src="https://github.com/user-attachments/assets/bd5ffa99-a3f2-4148-b49a-9b03ecd195c3" />

3. Sementara itu sistem akan memblokir jika inputan mengandung string/kata `String`
<img width="1259" height="125" alt="image" src="https://github.com/user-attachments/assets/233cc02c-253c-4510-827a-a9408059c1fb" />

4. Untuk mengakalinya kita perlu mengakali dengan merubah `query` menjadi `query[]` saat melakukan input agar dianggap sebagai array bukan string, dan flag ditemukan
<img width="1689" height="1169" alt="image" src="https://github.com/user-attachments/assets/904b5353-889d-4584-bf61-3da0ee2766c0" />
