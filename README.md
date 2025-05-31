
# 🕹️ Tralalelo Menyebrang - Game 3D Menyeberang Jalan dengan Kontrol Gestur Tangan

Sebuah game 3D sederhana ala **Frogger**, tapi dengan tampilan **3D** dan kontrol unik lewat **gestur tangan** menggunakan **OpenCV** dan **MediaPipe**. Dibuat menggunakan [Ursina Engine](https://www.ursinaengine.org/).

---

## 👤 Anggota Kelompok
1. Hijrah Fahrezi H.L.T. (122140175)
2. M. Ihsan Nur Tsaqib (122140176)
3. Roy Sebastian Surbakti (122140216)

---

## 🎮 Fitur-Fitur

- Jalan 3D dengan mobil-mobil yang datang dari kejauhan
- Kamera mengikuti karakter
- Karakter bisa dikendalikan dengan gestur tangan lewat webcam:
  - 👉 Tunjuk kanan → Jalan maju
  - 👈 Tunjuk kiri → Jalan mundur
  - ✋ Telapak tangan terbuka → Berhenti
- Versi game alternatif dengan kontrol keyboard biasa
- Tes deteksi gestur secara real-time

---

## 📁 Struktur Proyek

| File                   | Fungsi                                             |
|------------------------|----------------------------------------------------|
| `game.py`              | Game utama dengan kontrol gestur                  |
| `test_game.py`         | Versi game tanpa gestur, pakai keyboard saja      |
| `gesture_worker.py`    | Proses pendeteksi gestur berbasis webcam          |
| `test_recogniser.py`   | Menjalankan tes kamera dan deteksi gestur langsung|
| `gestures/recogniser.py` | Logika utama pengenalan gestur pakai MediaPipe  |
| `requirements.txt`     | Semua dependensi Python yang dibutuhkan           |

---

## 🚀 Cara Menjalankan Game

### 1. Install Python

Pastikan kamu sudah menginstall **Python 3.8–3.11**.  
Kalau belum, bisa unduh di: https://www.python.org/downloads/

### 2. Clone Repositori Ini

```bash
git clone https://github.com/pantomath000/tralalelo_menyebrang.git
cd tralalelo_menyebrang
```

### 3. Install Semua Dependensi

```bash
pip install -r requirements.txt
```

> Ini akan meng-install `ursina`, `opencv-python`, `mediapipe`, `pyautogui`, dll.

---

## 🎮 Menjalankan Game

### 🖐️ Mode Gestur (kontrol tangan via webcam)

```bash
python game.py
```

- Pastikan webcam aktif dan ruangan cukup terang
- Arahkan tangan ke kamera untuk mulai menggerakkan karakter
- Ketika melakukan gesture menunjuk, pastikan bagian samping tangan (punggung tangan menghadap ke atas) menghadap ke kamera supaya gestur terbaca. Jika punggung tangan atau bagian telapak yang mengahadap ke kamera, gestur tidak akan terbaca.

### ⌨️ Mode Keyboard (tanpa webcam)

```bash
python test_game.py
```

Gunakan tombol:
- `A` → Pindah kiri
- `D` → Pindah kanan

### 👀 Tes Pendeteksi Gestur

```bash
python test_recogniser.py
```

- Akan membuka jendela webcam dan menampilkan gestur yang terdeteksi secara real-time

---

## ✋ Daftar Gestur

| Gestur             | Fungsi                        |
|--------------------|-------------------------------|
| 👉 Tunjuk ke kanan | Jalan maju ke kanan           |
| 👈 Tunjuk ke kiri  | Jalan mundur ke kiri          |
| ✋ Telapak terbuka | Berhenti (tidak bergerak)     |

---

## 💻 Kompatibilitas Platform

- ❌ Windows *(DLL error atau black screen)*
- ✅ Linux *(Berjalan dengan lancar)*
- ❔ macOS *(Belum dites)*

---

## ⚙️ Syarat & Tips

- Butuh webcam yang aktif
- Pastikan tangan terlihat jelas di kamera
- Usahakan pencahayaan cukup agar deteksi lebih akurat

---

## 📄 Lisensi

Proyek ini menggunakan lisensi **MIT**.  
Bebas digunakan, dimodifikasi, dan dibagikan.

---

## ✅ To-do

1. Buat asset pohon dan objek lingkungan lainnya.
2. buat background music
3. buat mode portrait
4. buat sistem score
5. buat level dan mekanik difficulty yang berubah tiap level
6. Tampilkan wajah pengguna di background

---

## 📅 Logbook Mingguan

| File                   | Fungsi                                                                                |
|------------------------|---------------------------------------------------------------------------------------|
| `Minggu ke-1`          | Membuat file recogniser.py untuk mendeteksi gesture tangan menggunakan webcam         |
| `Minggu ke-2`          | Membuat game.py menggunakan library ursina untuk membuat logika dan mekanik game      |
| `Minggu ke-3`          | Menambahkan asset karakter tralalelo dan mobil di game                                |
| `Minggu ke-4`          | Finalisasi project dan menambahkan report.pdf                                         |
