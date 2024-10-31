Berikut adalah pembaruan untuk

1. **Clone repositori ini**:
   ```bash
   git clone <URL_REPOSITORI>
   ```

2. **Masuk ke folder repositori dan install dependensi**:
   ```bash
   cd <NAMA_FOLDER> && npm init -y && npm install axios
   ```

3. **Edit file `deleteTokens.js`**:
   - Buka file `deleteTokens.js` menggunakan editor teks.
   - Ganti nilai `email` dengan alamat email akun Cloudflare Anda.
   - Ganti nilai `apiKey` dengan Global API Key Cloudflare Anda.

   Contoh:
   ```javascript
   const email = 'your_email@example.com'; // Ganti dengan email akun Cloudflare kamu
   const apiKey = 'your_global_api_key'; // Ganti dengan Global API Key Cloudflare kamu
   ```

4. **Jalankan program**:
   ```bash
   node deleteTokens.js
   ```
