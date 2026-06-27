# 🌾 Sistem Deteksi Penyakit Tanaman Padi Berdasarkan Citra Menggunakan Algoritma Convolutional Neural Network (CNN) Berbasis Web

Sistem ini merupakan aplikasi berbasis web yang dikembangkan untuk mendeteksi penyakit pada daun tanaman padi menggunakan metode **Convolutional Neural Network (CNN)**. Pengguna dapat mengunggah citra daun padi, kemudian sistem akan melakukan klasifikasi secara otomatis menggunakan model CNN dan menampilkan hasil deteksi beserta informasi penyakit.

---

## 📌 Fitur Utama

- Login dan autentikasi pengguna
- Dashboard aplikasi
- Upload citra daun padi
- Deteksi penyakit menggunakan CNN
- Menampilkan confidence/akurasi prediksi
- Riwayat hasil deteksi
- Informasi lengkap penyakit tanaman padi
- Dashboard administrator
- Pengelolaan data penyakit

---

# 🛠 Teknologi yang Digunakan

## Backend

- Laravel 12
- PHP 8.3
- MySQL

## Frontend

- React
- TypeScript
- Inertia.js
- Tailwind CSS
- Vite

## Machine Learning

- Python
- Flask
- TensorFlow
- Keras
- OpenCV
- NumPy

---

# 📂 Struktur Project

```
cnndeep-learning-apps
│
├── app/
├── bootstrap/
├── config/
├── database/
├── public/
├── resources/
├── routes/
├── storage/
├── tests/
│
├── python-api/
│   ├── app.py
│   ├── model/
│   ├── preprocessing/
│   ├── requirements.txt
│   └── disease_descriptions.json
│
├── composer.json
├── package.json
├── vite.config.ts
├── tsconfig.json
└── README.md
```

---

# 💻 Persyaratan Sistem

Pastikan perangkat telah terinstal:

- Laragon
- PHP 8.3 atau lebih baru
- Composer
- Node.js
- npm
- Python 3.10+
- Git
- MySQL

---

# 🚀 Instalasi Project

## 1. Clone Repository

```bash
git clone https://github.com/LisaMenden/SISTEM-DETEKSI-PENYAKIT-TANAMAN-PADI-BERDASARKAN-CITRA-MENGGUNAKAN-ALGORITMA-CNN-BERBASIS-WEB.git
```

Pindahkan project ke folder

```
C:\laragon\www\
```

sehingga menjadi

```
C:\laragon\www\cnndeep-learning-apps
```

---

## 2. Install Dependency Laravel

Masuk ke folder project

```bash
composer install
```

Install dependency frontend

```bash
npm install
```

---

## 3. Konfigurasi Environment

Salin file

```
.env.example
```

menjadi

```
.env
```

Kemudian jalankan

```bash
php artisan key:generate
```

---

## 4. Konfigurasi Database

Buat database MySQL baru, misalnya

```
cnn_rice
```

Atur konfigurasi database pada file `.env`

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=cnn_rice
DB_USERNAME=root
DB_PASSWORD=
```

Kemudian jalankan

```bash
php artisan migrate --seed
```

---

## 5. Menjalankan Laravel

Jika menggunakan Laragon

Klik

```
Start All
```

atau melalui terminal

```bash
php artisan serve
```

Aplikasi dapat diakses melalui

```
http://localhost/cnndeep-learning-apps/public
```

atau

```
http://cnndeep-learning-apps.test
```

jika Virtual Host Laragon telah aktif.

---

## 6. Menjalankan Frontend

```bash
npm run dev
```

---

## 7. Menjalankan Python API

Masuk ke folder

```
python-api
```

Buat Virtual Environment

```bash
python -m venv venv
```

Aktifkan

Windows

```bash
venv\Scripts\activate
```

Install library

```bash
pip install -r requirements.txt
```

Jalankan Flask API

```bash
python app.py
```

API akan berjalan pada

```
http://127.0.0.1:5000
```

---

# 🔄 Alur Kerja Sistem

1. Pengguna login ke sistem.
2. Pengguna mengunggah citra daun padi.
3. Laravel mengirim gambar ke Python Flask API.
4. Flask melakukan preprocessing citra.
5. Model CNN melakukan klasifikasi penyakit.
6. Flask mengirim hasil prediksi ke Laravel.
7. Laravel menyimpan hasil ke database.
8. Hasil deteksi ditampilkan kepada pengguna.

---

# 📊 Penyakit yang Dideteksi

Sistem mampu mengidentifikasi beberapa penyakit tanaman padi, antara lain:

- Bacterial Blight
- Blast
- Brown Spot
- Tungro
- Healthy Leaf

*(Sesuaikan dengan kelas yang digunakan pada model CNN Anda.)*

---

# 📁 Dataset

Dataset citra tidak disertakan pada repository GitHub karena ukurannya cukup besar.

---

# 🤖 Model CNN

File model TensorFlow (.h5) tidak disertakan pada repository GitHub karena melebihi batas ukuran GitHub.

Model dapat disimpan pada folder:

```
python-api/trained_models/
```

Setelah diunduh dari penyimpanan eksternal (misalnya Google Drive atau GitHub Releases).

---

# 📸 Tampilan Sistem

Tambahkan screenshot aplikasi pada folder

```
screenshots/
```

Contoh:

```
screenshots/
│
├── login.png
├── dashboard.png
├── upload.png
├── result.png
├── history.png
└── disease.png
```

Kemudian tampilkan pada README

```markdown
## Dashboard

![Dashboard](screenshots/dashboard.png)

## Upload Gambar

![Upload](screenshots/upload.png)

## Hasil Deteksi

![Result](screenshots/result.png)
```

---

# 👩‍💻 Pengembang

**Lisa Menden**

Program Studi Teknik Informatika

Universitas Negeri Manado

---

# 📄 Lisensi

Project ini dikembangkan untuk keperluan penelitian akademik dan penyusunan skripsi.

Apabila digunakan sebagai referensi, harap mencantumkan sumber sesuai etika akademik.
