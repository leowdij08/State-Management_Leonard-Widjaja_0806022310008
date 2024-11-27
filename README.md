Leonard Widjaja - 0806022310008
---

# Pengelolaan State di Flutter: **Ephemeral** vs **App State**

## 📖 Tentang Proyek
Proyek ini bertujuan untuk mempelajari dua cara mengelola *state* (data) di Flutter:
1. **Ephemeral State Management**: Mengelola data sementara yang hanya digunakan di satu widget tertentu.
2. **App State Management**: Mengelola data yang bisa dibagikan ke seluruh aplikasi menggunakan paket `scoped_model`.

---

## 🚀 Langkah-Langkah

### **Bagian 1: Ephemeral State Management**
- **Proyek**: `ephemeral_state_codelab`.
- **Tujuan**: Mengelola data lokal dalam widget menggunakan `StatefulWidget`.
- **Cara Kerja**:
  1. Data (_state_) disimpan di dalam widget tertentu.
  2. Ketika tombol "Increment" ditekan, nilai **counter** bertambah dan UI diperbarui dengan `setState`.

- **Hasil**:
  - **Teks**: `Counter Value: X` (menampilkan nilai counter).
  - **Tombol**: "Increment" untuk menaikkan nilai counter.

---

### **Bagian 2: App State Management**
- **Proyek**: `app_state_codelab`.
- **Tujuan**: Mengelola data yang bisa digunakan oleh banyak widget di seluruh aplikasi.
- **Cara Kerja**:
  1. Membuat model `CounterModel` untuk menyimpan data counter dan fungsi untuk menambah/mengurangi nilainya.
  2. `ScopedModel` digunakan untuk membagikan data ini ke seluruh widget.
  3. `ScopedModelDescendant` dipakai untuk mendapatkan data di widget dan memperbarui UI.

- **Hasil**:
  - **Teks**: `Counter Value: X`.
  - **Tombol**: "Increment" untuk menaikkan nilai.
  - **Tombol**: "Decrement" untuk menurunkan nilai.

---

## 🔍 Kesimpulan dan Perbandingan

### **Perilaku Kedua Metode**
1. **Ephemeral State Management**:
   - Data hanya dikelola di widget tertentu.
   - Perubahan data hanya berdampak pada widget tersebut.
   - Cocok untuk kebutuhan sederhana (misalnya, tombol atau form kecil).

2. **App State Management**:
   - Data bisa dibagikan ke seluruh aplikasi.
   - Semua widget yang menggunakan data akan diperbarui otomatis jika ada perubahan.
   - Cocok untuk aplikasi besar dengan banyak bagian yang berbagi data.

---

## ✅ Kelebihan dan Kekurangan

### **Ephemeral State Management**
- **Kelebihan:**
  - Mudah dipahami dan digunakan.
  - Tidak butuh paket tambahan.
  - Cocok untuk kebutuhan kecil.
- **Kekurangan:**
  - Tidak bisa digunakan untuk membagikan data antar widget.
  - Kurang cocok untuk aplikasi besar.

### **App State Management (Scoped Model)**
- **Kelebihan:**
  - Data bisa dibagikan ke mana saja dalam aplikasi.
  - Lebih rapi karena memisahkan logika data dari UI.
  - Cocok untuk aplikasi kompleks.
- **Kekurangan:**
  - Membutuhkan paket tambahan (`scoped_model`).
  - Implementasinya lebih rumit dibandingkan dengan state lokal.

---

## 🎯 Kesimpulan Akhir
- Gunakan **Ephemeral State Management** untuk kebutuhan sederhana seperti tombol atau komponen kecil.
- Gunakan **App State Management** (dengan `scoped_model`) jika aplikasi Anda memiliki banyak bagian yang membutuhkan data yang sama.

Memahami kapan menggunakan masing-masing cara ini akan membantu Anda membuat aplikasi yang lebih efisien dan mudah dirawat.
