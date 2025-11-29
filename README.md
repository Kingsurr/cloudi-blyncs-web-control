# 🚀 Cloudi Blyncs Web Control
### Solusi Web untuk Pengendalian Perangkat IoT

Selamat datang di repositori proyek **Cloudi Blyncs Web Control**! Ini adalah antarmuka web yang dirancang untuk memantau dan mengendalikan perangkat Internet of Things (IoT) yang terhubung menggunakan platform **Blynk Cloud**.

Aplikasi ini bertujuan untuk menyediakan panel kontrol yang mudah digunakan, *real-time*, dan dapat diakses dari mana saja melalui *browser* web.

---

## ✨ Fitur Utama
Proyek **Cloudi Blyncs Web Control** menyediakan kontrol dan pemantauan mendalam atas perangkat ESP32 Anda melalui Blynk Virtual Pins:

* **Kontrol Daya Dimmer (V0):** Mengatur tingkat daya antara **0% hingga 100%** menggunakan *slider* dan input angka.
* **Kontrol Lebar Pulsa Gate (V1):** Mengatur lebar pulsa gate antara **200 $\mu$s hingga 4000 $\mu$s** (*mikrodetik*), yang penting untuk perangkat switching daya.
* **Mode Daya Penuh (V3):** Tombol *toggle* sederhana untuk mengaktifkan atau menonaktifkan mode daya penuh.
* **Uji Pulsa Gate (V2):** Kontrol tekan-dan-tahan untuk mengirimkan sinyal pulsa gate secara instan.
* **Sistem Timer Terpadu (V4, V5, V7):**
    * Mengatur durasi timer (V4) hingga **60 menit**.
    * Tombol **Start Timer (V5)** dan **Stop Timer (V7)**.
    * Menampilkan **Status Timer (V6)** secara *real-time* dari Blynk Cloud.
* **Status Koneksi Perangkat:** Menampilkan status koneksi perangkat ESP32 ke Blynk Cloud (**ONLINE/OFFLINE**).
* **Desain Neumorphism Responsif:** Tampilan modern dan *mobile-friendly* (adaptif untuk layar kecil).

---

## 🛠️ Teknologi yang Digunakan
Proyek ini adalah aplikasi *front-end* murni yang berkomunikasi langsung dengan Blynk API.

| Kategori | Teknologi/Komponen | Keterangan |
| :--- | :--- | :--- |
| **Frontend** | HTML5, CSS3 | Struktur dan gaya, menggunakan desain *Neumorphism* kustom. |
| **Logika** | JavaScript | Menangani sinkronisasi nilai *slider/input* dan logika kontrol. |
| **Platform IoT** | **Blynk Cloud API** | Digunakan untuk membaca dan menulis nilai ke **Virtual Pins (V0, V1, V2, V3, V4, V5, V6, V7)**. |
| **Perangkat Keras** | ESP32 (Diasumsikan) | Target perangkat keras yang menjalankan kode Blynk. |
| **Hosting** | GitHub Pages | Hosting statis yang digunakan untuk menampilkan antarmuka web. |

### Detail Pin Virtual
Berikut adalah pemetaan *Virtual Pin* yang digunakan dalam aplikasi **Cloudi Blyncs Web Control**:

* **V0:** Daya Dimmer (0-100%)
* **V1:** Lebar Pulsa Gate (200 $\mu$s - 4000 $\mu$s)
* **V2:** Uji Pulsa Gate (Momenary/Tekan-Tahan)
* **V3:** Mode Daya Penuh (ON/OFF)
* **V4:** Durasi Timer (0-60 Menit)
* **V5:** Tombol Start Timer
* **V6:** Display Status Timer
* **V7:** Tombol Stop Timer

---

## 🚀 Instalasi & Penggunaan
Untuk menjalankan **Cloudi Blyncs Web Control**, Anda hanya perlu menyalin kode dan mengkonfigurasi token API Anda.

### Persyaratan
1.  Perangkat IoT (seperti ESP32) yang sudah diprogram dan terhubung ke **Blynk Cloud**.
2.  **Auth Token** dari Proyek Blynk Anda.

### Langkah-langkah
1.  **Clone Repositori:**
    ```bash
    git clone [https://github.com/kingsunr/cloudi-blyncs-web-control.git](https://github.com/kingsunr/cloudi-blyncs-web-control.git)
    ```
2.  **Konfigurasi API:** Buka file `index.html` dan ganti nilai variabel `BLYNK_AUTH_TOKEN` pada bagian `<script>`:
    ```javascript
    const BLYNK_AUTH_TOKEN = "KUJWMkmFarXyPL2FUxReLa7-GNsupY0f"; // GANTI DENGAN TOKEN ANDA
    const BLYNK_API_URL = "[https://blynk.cloud/external/api/](https://blynk.cloud/external/api/)";
    ```
3.  **Deploy atau Buka:** Anda dapat membuka file `index.html` langsung di *browser* Anda untuk pengujian lokal, atau *deploy* ke GitHub Pages (seperti yang sudah Anda lakukan) agar dapat diakses publik.

## 🖼️ Tampilan Aplikasi
> [Ganti teks ini dengan tag gambar, misalnya: ``](./docs/screenshot-dashboard.jpg)
> [Ganti teks ini dengan tag gambar, misalnya: ``](./docs/screenshot-sensor.jpg)

## ✍️ Kontributor
Proyek **Cloudi Blyncs Web Control** dikembangkan oleh:

* [Hary Suryadi/Kingsurr]

Anda dapat mengunjungi situs proyek ini secara langsung di:
[Tautan ke GitHub Pages Anda: `https://kingsurr.github.io/cloudi-blyncs-web-control/`]

---
*Dibuat dengan ❤️ untuk kemudahan kontrol IoT.*
