# Dokumen Spesifikasi Kebutuhan Perangkat Lunak (SRS)
## Aplikasi: My Habit Streaks (Pelacak Kebiasaan Sederhana)
**Versi:** 1.0
**Tanggal:** [28 Mei 2025]
**Penyusun:** [Janziar Nanda Veranty] - [221240001321]

## Daftar Isi
1. Pendahuluan
    1.1 Tujuan
    1.2 Ruang Lingkup Produk
    1.3 Definisi, Akronim, dan Singkatan
    1.4 Referensi
    1.5 Tinjauan Umum Dokumen
2. Deskripsi Umum
    2.1 Perspektif Produk
    2.2 Fungsi Produk
    2.3 Karakteristik Pengguna
    2.4 Batasan Umum
    2.5 Asumsi dan Ketergantungan
3. Kebutuhan Spesifik
    3.1 Kebutuhan Fungsional
    3.2 Kebutuhan Antarmuka Eksternal
        3.2.1 Antarmuka Pengguna (UI)
    3.3 Kebutuhan Non-Fungsional
        3.3.1 Kebutuhan Kinerja
        3.3.2 Kebutuhan Keamanan
        3.3.3 Kebutuhan Keandalan
        3.3.4 Kebutuhan Portabilitas
    3.4 Kebutuhan Basis Data
4. Apendiks (Opsional)

---

## 1. Pendahuluan

### 1.1 Tujuan
Dokumen ini mendeskripsikan spesifikasi kebutuhan untuk "My Habit Streaks", sebuah aplikasi mobile yang dirancang untuk membantu pengguna individu mendefinisikan, melacak, dan membangun kebiasaan positif dengan fokus pada visualisasi rentetan keberhasilan (streak).

### 1.2 Ruang Lingkup Produk (Cakupan MVP)
Aplikasi "My Habit Streaks" versi MVP akan fokus pada:
1.  **Manajemen Kebiasaan (CRUD):**
    *   Menambah kebiasaan baru (nama, deskripsi opsional, ikon/warna opsional).
    *   Melihat daftar semua kebiasaan yang aktif.
    *   Melihat detail kebiasaan, termasuk visualisasi progres (misal, kalender) dan statistik streak.
    *   Mengedit informasi kebiasaan.
    *   Menghapus kebiasaan (beserta data progresnya).
2.  **Pencatatan Progres Harian (CRUD):**
    *   Untuk setiap kebiasaan, pengguna dapat menandai apakah kebiasaan tersebut dilakukan atau tidak pada hari tertentu.
    *   Mengedit status progres harian (misal, jika salah input).
    *   (MVP mungkin tidak butuh hapus progres harian individual, cukup edit jadi "tidak dilakukan").

### 1.3 Definisi, Akronim, dan Singkatan
*   **SRS:** Software Requirements Specification
*   **MVP:** Minimum Viable Product
*   **UI:** User Interface
*   **UX:** User Experience
*   **CRUD:** Create, Read, Update, Delete
*   **Streak:** Rentetan hari berturut-turut di mana kebiasaan berhasil dilakukan.

### 1.4 Referensi
*   Diskusi kebutuhan pengguna (simulasi).
*   Analisis aplikasi pelacak kebiasaan sederhana di Play Store.

### 1.5 Tinjauan Umum Dokumen
Dokumen ini akan menguraikan deskripsi umum produk, fungsi utama, karakteristik pengguna, batasan, serta kebutuhan fungsional dan non-fungsional.

---

## 2. Deskripsi Umum

### 2.1 Perspektif Produk
"My Habit Streaks" adalah aplikasi *self-improvement tool* mobile untuk Android dan iOS (Flutter) yang bertujuan memotivasi pengguna melalui pelacakan dan visualisasi progres kebiasaan. Semua data disimpan lokal.

### 2.2 Fungsi Produk (MVP)
1.  **FP01 - Tambah Kebiasaan (Create):**
    *   Pengguna dapat memasukkan nama kebiasaan.
    *   Pengguna dapat menambahkan deskripsi opsional (misal, "Minum 8 gelas air sehari").
    *   (Opsional MVP) Pengguna dapat memilih ikon dan/atau warna untuk membedakan kebiasaan.
2.  **FP02 - Lihat Daftar Kebiasaan (Read):**
    *   Menampilkan daftar semua kebiasaan yang sedang dilacak oleh pengguna.
    *   Setiap item menampilkan nama kebiasaan dan mungkin tombol cepat untuk menandai "dilakukan hari ini".
3.  **FP03 - Lihat Detail & Progres Kebiasaan (Read):**
    *   Menampilkan detail kebiasaan (nama, deskripsi).
    *   Visualisasi progres, misalnya dalam bentuk kalender bulanan yang menandai hari-hari kebiasaan dilakukan.
    *   Menampilkan statistik kunci: streak saat ini, streak terpanjang, total hari dilakukan.
4.  **FP04 - Edit Kebiasaan (Update):**
    *   Mengubah nama, deskripsi, ikon/warna kebiasaan.
5.  **FP05 - Hapus Kebiasaan (Delete):**
    *   Menghapus kebiasaan dan semua data progres terkaitnya dengan konfirmasi.
6.  **FP06 - Tandai Progres Harian (Create/Update):**
    *   Untuk setiap kebiasaan, pengguna dapat menandai status untuk hari ini (dilakukan/tidak dilakukan).
    *   Pengguna dapat melihat kalender dan menandai/mengubah status untuk hari-hari sebelumnya (misal, jika lupa input kemarin).
7.  **FP07 - Kalkulasi Streak:**
    *   Sistem secara otomatis menghitung streak saat ini dan streak terpanjang berdasarkan data progres harian.

### 2.3 Karakteristik Pengguna
Pengguna target adalah individu yang ingin membangun kebiasaan baru atau mempertahankan kebiasaan baik, dan termotivasi oleh visualisasi progres serta pencapaian rentetan (streak).

### 2.4 Batasan Umum
1.  Aplikasi *single-user*. Data disimpan lokal.
2.  Tidak ada fitur sosial, pengingat (notifikasi) kompleks, atau target kuantitatif (misal, "baca 10 halaman") di MVP. Fokus pada biner: dilakukan/tidak.
3.  Jenis kebiasaan tidak terbatas (misal, harian, mingguan X kali) di MVP, hanya harian.

### 2.5 Asumsi dan Ketergantungan
1.  Pengguna memiliki smartphone yang kompatibel.
2.  Pengguna secara manual dan jujur mencatat progres kebiasaan mereka.

---

## 3. Kebutuhan Spesifik

### 3.1 Kebutuhan Fungsional

| ID    | Deskripsi Kebutuhan                                                                                                | Prioritas |
| :---- | :----------------------------------------------------------------------------------------------------------------- | :-------- |
| KF001 | Pengguna harus dapat menambahkan kebiasaan baru dengan nama. Deskripsi, ikon, warna bersifat opsional.               | Tinggi    |
| KF002 | Sistem harus menyimpan data kebiasaan ke penyimpanan lokal.                                                            | Tinggi    |
| KF003 | Pengguna harus dapat melihat daftar semua kebiasaan yang aktif.                                                      | Tinggi    |
| KF004 | Pengguna harus dapat menandai kebiasaan sebagai "dilakukan" atau "tidak dilakukan" untuk tanggal tertentu.         | Tinggi    |
| KF005 | Sistem harus menyimpan catatan progres harian untuk setiap kebiasaan.                                                | Tinggi    |
| KF006 | Pengguna harus dapat melihat detail kebiasaan, termasuk visualisasi kalender progresnya.                             | Tinggi    |
| KF007 | Sistem harus menghitung dan menampilkan streak saat ini dan streak terpanjang untuk setiap kebiasaan.                 | Tinggi    |
| KF008 | Pengguna harus dapat mengedit detail kebiasaan (nama, deskripsi, ikon/warna).                                       | Tinggi    |
| KF009 | Pengguna harus dapat menghapus kebiasaan (beserta semua data progresnya) dengan konfirmasi.                           | Tinggi    |
| KF010 | Pengguna harus dapat mengubah status progres harian yang sudah dicatat sebelumnya.                                    | Sedang    |

### 3.2 Kebutuhan Antarmuka Eksternal

#### 3.2.1 Antarmuka Pengguna (UI)
*   **Halaman Utama/Daftar Kebiasaan:** List kebiasaan. Setiap item menampilkan nama, mungkin ikon/warna, dan tombol cepat "Tandai Selesai Hari Ini". Tombol Tambah Kebiasaan (FAB).
*   **Halaman Tambah/Edit Kebiasaan:** Form input nama, deskripsi. Pilihan ikon/warna (jika diimplementasikan). Tombol Simpan.
*   **Halaman Detail Kebiasaan:**
    *   Info kebiasaan (nama, deskripsi).
    *   Widget kalender yang interaktif untuk menandai progres harian. Hari yang "dilakukan" ditandai berbeda.
    *   Tampilan statistik (streak saat ini, streak terpanjang).
    *   Tombol Edit dan Hapus Kebiasaan.

UI harus memotivasi, bersih, dan memberikan feedback visual yang jelas tentang progres.

### 3.3 Kebutuhan Non-Fungsional

#### 3.3.1 Kebutuhan Kinerja
*   Aplikasi harus responsif, terutama saat berinteraksi dengan kalender atau memuat daftar kebiasaan.

#### 3.3.2 Kebutuhan Keamanan
*   Data disimpan lokal.

#### 3.3.3 Kebutuhan Keandalan
*   Tidak boleh ada kehilangan data progres kebiasaan. Kalkulasi streak harus akurat.

#### 3.3.4 Kebutuhan Portabilitas
*   Flutter untuk Android (API 21+) dan iOS (iOS 11+).

### 3.4 Kebutuhan Basis Data
*   Aplikasi akan menggunakan database SQLite lokal.
    *   **Tabel Kebiasaan (Habits):**
        *   `id` (INTEGER, PRIMARY KEY, AUTOINCREMENT)
        *   `name` (TEXT, NOT NULL)
        *   `description` (TEXT, NULLABLE)
        *   `icon_name` (TEXT, NULLABLE) -- Nama ikon dari set yang disediakan
        *   `color_hex` (TEXT, NULLABLE) -- Warna untuk representasi
        *   `created_at` (TEXT -- ISO8601)
    *   **Tabel ProgresHarian (DailyProgress):**
        *   `id` (INTEGER, PRIMARY KEY, AUTOINCREMENT)
        *   `habit_id` (INTEGER, NOT NULL, FOREIGN KEY ke Habits(id) ON DELETE CASCADE)
        *   `date` (TEXT, NOT NULL -- 'YYYY-MM-DD', UNIQUE constraint on (habit_id, date))
        *   `is_completed` (INTEGER, NOT NULL -- 0 for false, 1 for true)
        *   `notes` (TEXT, NULLABLE -- opsional, catatan singkat untuk hari itu)

---

## 4. Pendekatan Arsitektur (Awal)
*   **Bahasa Pemrograman:** Dart
*   **Framework:** Flutter
*   **Manajemen State:** Provider / Riverpod.
*   **Penyimpanan Lokal:** `sqflite`.
*   **Kalender Widget:** Package seperti `table_calendar` atau custom.
*   **Navigasi:** `GoRouter` atau `Navigator 2.0`.
*   **Struktur Proyek:** Feature-first.

*Detail arsitektur akan disempurnakan.*