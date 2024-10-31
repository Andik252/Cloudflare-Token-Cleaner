# Cloudflare API Token Deleter

## Cara Instalasi

1. **Install Node.js dan Git**:
   ```bash
   sudo apt install -y nodejs git
   ```
   
2. **Clone repositori ini**:
   ```bash
   git clone https://github.com/Andik252/cloudflare-token-cleaner/tree/48bdbe45ec4e697bb38fccde5ebfed4d4b71281c/Cloudflare-Token-Cleaner


3. **Masuk ke folder repositori dan install dependensi**:
   ```bash
   cd Cloudflare-Token-Cleaner && npm init -y && npm install axios
   ```

4. **Edit file `deleteTokens.js`**:
   - Buka file `deleteTokens.js` menggunakan editor teks.     
   - Ganti nilai `email` dengan alamat email akun Cloudflare Anda.
     
   - Ganti nilai `apiKey` dengan Global API Key Cloudflare Anda.
     
   - Jika ada token yang ingin Anda kecualikan dari penghapusan, tambahkan nama token tersebut ke dalam array `exceptions`.

   Contoh:
   ```javascript
   const email = 'your_email@example.com'; // Ganti dengan email akun Cloudflare kamu
   const apiKey = 'your_global_api_key'; // Ganti dengan Global API Key Cloudflare kamu
   const exceptions = ['Token-Kecualian']; // Token pengecualian yang tidak akan dihapus Jika ada isi
   ```

5. **Jalankan program**:
   ```bash
   node deleteTokens.js
   ```
