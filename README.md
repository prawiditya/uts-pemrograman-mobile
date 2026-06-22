
<p align="center">

![Nama](https://img.shields.io/badge/Nama-Prawiditya%20Sahrul%20Akbar-0A66C2?style=for-the-badge&logo=github&logoColor=white)
![Kelas](https://img.shields.io/badge/Kelas-I%2024%201A-1ABC9C?style=for-the-badge)
![Matkul](https://img.shields.io/badge/Matakuliah-Pemrograman%20Mobile2-FF6F00?style=for-the-badge&logo=android&logoColor=wh)

</p>

# 💰 CatatUang - Aplikasi Pencatat Keuangan Yang bernama Financeku

> **Catat Uang, Atur Masa Depan.**

**CatatUang** adalah aplikasi Android modern untuk mengelola keuangan pribadi. Aplikasi ini memungkinkan pengguna mencatat pemasukan dan pengeluaran, serta berkonsultasi dengan asisten keuangan berbasis AI (Groq Llama).

---


## ✨ Fitur Utama

### 📊 Manajemen Keuangan
- Tambah pemasukan & pengeluaran
- Riwayat transaksi tersimpan rapi


### 🤖 Asisten Keuangan AI
- Analisis pemasukan & pengeluaran
- Saran keuangan personal
- Chat dengan AI yang mengetahui data keuangan dan target tabungan Anda


### 📈 Statistik & Laporan
- Grafik pemasukan vs pengeluaran


### 🎨 UI Modern
- Material 3
- Animasi halus

---

## 📸 Preview Aplikasi

<p align="center">
 <img width="359" height="804" alt="Screenshot 2026-05-02 072722" src="https://github.com/user-attachments/assets/ea57bb3e-81f2-4e2d-91d6-9d0d84205447" />
 <img width="366" height="807" alt="Screenshot 2026-05-02 072744" src="https://github.com/user-attachments/assets/fa1bf4ed-9d9b-4c48-b591-5ccd997bf465" />
 <img width="266" height="546" alt="Screenshot 2026-05-02 080238" src="https://github.com/user-attachments/assets/9b4be145-a3bf-40b9-8be4-4d3b6fe9e8ec" />
 

<p align="center">
  🏠 <b>Dashboard</b> &nbsp;&nbsp;&nbsp;&nbsp;
  🤖 <b>AI Chat</b>
</p>

---

## ⚙️ Instalasi & Setup

### 1. Persyaratan

- Android Studio Hedgehog (2023.1.1+)
- JDK 11+
- minSdk 24
- targetSdk 34

---

### 2. Konfigurasi API Key (Groq)

Buat file:

```
secrets.properties
```

Isi dengan:

```
properties
GROQ_API_KEY=gsk_kunci_anda
```

---

### 3. Tambahkan ke build.gradle.kts

```
kotlin
android {
    buildFeatures {
        buildConfig = true
    }
}

val secretsProperties = java.util.Properties()
val secretsFile = rootProject.file("secrets.properties")

if (secretsFile.exists()) {
    secretsProperties.load(secretsFile.inputStream())
}

android.defaultConfig {
    buildConfigField(
        "String",
        "GROQ_API_KEY",
        "\"\${secretsProperties.getProperty("GROQ_API_KEY")}\""
    )
}


---


xml
<paths>
    <cache-path name="cache" path="/" />
</paths>
```

---

### 6. Jalankan Aplikasi

- Hubungkan device / emulator
- Klik tombol Run ▶️

---

## 🧠 Cara Kerja AI

  

### 🤖 AI Assistant
- Membaca data keuangan pengguna
- Memberikan insight & saran finansial

---

## 📁 Struktur Project
```
com.example.financeku
├── MainActivity.kt
├── LuxuryCatatUangScreen.jv
├── GroqClient.kt
├── AppPrefs.jv
└── BuildConfig


---

## ❗Catatan Penting

- API Key Groq wajib diisi. Tanpa key, fitur AI dan ekstraksi item struk tidak akan bekerja (akan return kosong).
- Koneksi internet diperlukan untuk memanggil Groq API.
- Aplikasi tidak menggunakan database SQLite, seluruh data disimpan di SharedPreferences (cocok untuk skala kecil).

## 📜 License
Hak Cipta © 2026 - Tugas Pemrograman Mobile
Dibuat untuk keperluan pendidikan. Boleh dimodifikasi dan didistribusikan.

## Hasil SCRUM
![Uploading Screenshot 2026-06-22 135317.png…]()

