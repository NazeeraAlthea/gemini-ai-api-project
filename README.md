Proyek API Gemini AI
Sebuah server backend sederhana yang dibuat dengan Node.js dan Express untuk berinteraksi dengan Google Gemini API. Proyek ini menyediakan beberapa endpoint untuk menghasilkan konten berdasarkan input teks, gambar, dan dokumen.

Fitur Utama
✨ Generate Konten dari Teks: Endpoint untuk menerima input teks biasa dan mendapatkan respons dari AI.
🖼️ Generate Konten dari Gambar: Endpoint untuk mengunggah gambar beserta prompt teks untuk dianalisis oleh AI.
📄 Generate Konten dari Dokumen: Endpoint untuk mengunggah dokumen (seperti PDF) beserta prompt untuk dianalisis.
🚀 Dibangun dengan Express.js: Server yang cepat dan minimalis.
📁 Penanganan Upload File: Menggunakan Multer untuk mengelola unggahan file dengan efisien.

Teknologi yang Digunakan
Node.js: Lingkungan eksekusi JavaScript.

Express.js: Kerangka kerja web untuk Node.js.

@google/generative-ai: SDK resmi dari Google untuk Gemini API.

dotenv: Untuk mengelola variabel lingkungan.

multer: Middleware untuk menangani multipart/form-data (upload file).

Instalasi dan Konfigurasi
Ikuti langkah-langkah ini untuk menjalankan proyek secara lokal.

1. Clone Repositori
Bash

git clone https://github.com/NazeeraAlthea/gemini-ai-api-project.git
cd gemini-ai-api-project
2. Instal Dependensi
Pastikan Anda sudah menginstal Node.js dan npm. Jalankan perintah berikut di terminal:

Bash

npm install
3. Siapkan Variabel Lingkungan
Proyek ini membutuhkan kunci API dari Google AI Studio.

a. Buat file baru di direktori utama proyek dengan nama .env.

b. Salin konten berikut ke dalam file .env dan ganti dengan kunci API Anda.

GEMINI_API_KEY=KUNCI_API_ANDA_DISINI
Anda bisa mendapatkan kunci API dari Google AI Studio.

Menjalankan Server
Setelah instalasi dan konfigurasi selesai, jalankan server dengan perintah:

Bash

node index.js
Server akan berjalan dan aktif di http://localhost:3000.

Dokumentasi API
Gunakan aplikasi seperti Postman atau Insomnia untuk menguji endpoint berikut.

1. Generate dari Teks
URL: /generate-text

Method: POST

Headers:

Content-Type: application/json

Body (raw, JSON):

JSON

{
  "prompt": "Ceritakan sebuah lelucon tentang pemrograman"
}
2. Generate dari Gambar
URL: /generate-from-image

Method: POST

Body: form-data

Key: image, Type: File, Value: (pilih file gambar Anda)

Key: prompt, Type: Text, Value: jelaskan apa yang ada di gambar ini

3. Generate dari Dokumen
URL: /generate-from-document

Method: POST

Body: form-data

Key: document, Type: File, Value: (pilih file dokumen Anda)

Key: prompt, Type: Text, Value: rangkum isi dokumen ini