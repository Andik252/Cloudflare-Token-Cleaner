# Cloudflare API Token Deleter

## Deskripsi
Skrip ini memungkinkan Anda untuk menghapus token API Cloudflare secara otomatis. Dengan menggunakan Node.js dan Axios, Anda dapat mengelola token API Anda dengan lebih efisien.

## Cara Instalasi

1. **Install Node.js dan Git**:
   ```bash
   sudo apt install -y nodejs git
   ```
   
2. **Clone repositori ini**:
   ```bash
   git clone https://github.com/Andik252/Cloudflare-Token-Cleaner.git

3. **Masuk ke folder repositori dan install dependensi**:
   ```bash
   cd Cloudflare-Token-Cleaner && npm init -y && npm install axios
   ```

4. **Edit file `deleteTokens.js`**:
   
   ```bash
    nano deleteTokens.js
   ```
   
   - Ganti nilai `email` dengan alamat email akun Cloudflare Anda.
     
   - Ganti nilai `apiKey` dengan Global API Key Cloudflare Anda.
     
   - Jika ada token yang ingin Anda kecualikan dari penghapusan, tambahkan nama token tersebut ke dalam array `exceptions`.

   Edit file ini :
   ```javascript
   const email = 'your_email@example.com'; // Ganti dengan email akun Cloudflare kamu
   const apiKey = 'your_global_api_key'; // Ganti dengan Global API Key Cloudflare kamu
   const exceptions = ['Token-Kecualian']; // isi Jika ada Token pengecualian yang tidak ingin dihapus
   ```
   Simpan file dengan perintah `Ctrl + x`, lalu `y`, dan `Enter`.

6. **Jalankan program**:
   ```bash
   node deleteTokens.js
   ```
## Catatan Penting
- **Hati-hati dengan Penghapusan**: Skrip ini akan menghapus token API yang tidak Anda kecualikan. Pastikan Anda telah memeriksa daftar token dan menentukan token mana yang ingin Anda simpan.
- **Rate Limiting**: Cloudflare API memiliki batasan laju. Jika Anda memiliki banyak token untuk dihapus, Anda mungkin perlu menangani batasan ini dengan menambahkan penundaan antara permintaan.
- **Error Handling**: Pastikan untuk memeriksa output log untuk mengidentifikasi setiap kesalahan yang mungkin terjadi selama proses penghapusan.
