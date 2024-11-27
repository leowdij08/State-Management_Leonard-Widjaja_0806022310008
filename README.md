Leonard Widjaja - 0806022310008
---

# *State Management* di Flutter: ***Ephemeral State Management*** vs ***App State Management***

## 📖 Tentang Proyek
Proyek ini membahas dua pendekatan utama dalam *State Management* di Flutter, yaitu:
1. **Ephemeral State Management**: Mengelola data lokal dalam *widget* menggunakan `StatefulWidget`.
2. **App State Management**: Mengelola data global yang dapat diakses di seluruh aplikasi menggunakan *package* `scoped_model`.

---

## 🔍 Perbandingan Kedua Metode

### ***Ephemeral State Management* ('StatefulWidget')**
Pada *Ephemeral State Management*, data disimpan dalam `StatefulWidget` dan hanya tersedia untuk *widget* tersebut, sehingga perubahan data hanya akan mempengaruhi *widget* tempat data berada. 
- ***Emphermal State Management* dapat digunakan untuk, antara lain:**
  - Membuat tombol sederhana untuk menaikkan nilai.
  - Mengelola input dalam satu form kecil.
- **Kelebihan *Emphermal State Management***:
  - Mudah dipahami dan diimplementasikan.
  - Tidak membutuhkan *package* tambahan.
  - Cocok untuk komponen independen dan sederhana.
- **Kekurangan *Emphermal State Management***:
  - Tidak bisa digunakan untuk membagikan data antar *widget*.
  - Kurang cocok untuk aplikasi besar atau kompleks.

### ***App State Management* ('Scoped Model')**
Pada *App State Management*, data dikelola di satu tempat (model), yang kemudian dapat diakses oleg semua *widget* dalam aplikasi. Apabila ada terjadi perubahan data, maka seluruh *widget* yang menggunakannya akan terperbarui. 
- ***App State Management* dapat digunakan untuk, antara lain:**
  - Ketika berurusan dengan *User Authentication*, *App State Management* mampu menyimpan informasi pengguna yang login dan membagikannya ke seluruh aplikasi.
  - Mengelola daftar produk yang dipilih pengguna, menghitung total, dan menyinkronkan data pada fitur *Shopping Cart*.
  - Membagikan notifikasi atau pesan ke berbagai halaman dalam aplikasi.
- **Kelebihan *App State Management***:
  - Mempermudah berbagi data antar widget.
  - Membantu memisahkan logika data dari UI (lebih terstruktur).
  - Cocok untuk aplikasi besar yang membutuhkan koordinasi antar banyak komponen.
- **Kekurangan *App State Management***:
  - Membutuhkan paket tambahan seperti `scoped_model`.
  - Lebih kompleks dibandingkan `StatefulWidget`.

---

## 🎯 Keunggulan *App State Management* untuk Aplikasi Besar
*App State Management* lebih unggul untuk aplikasi dengan kebutuhan kompleks seperti:
1. **User Authentication**:
   - Data pengguna (misalnya, token, nama, dan preferensi) dapat diakses di berbagai bagian aplikasi.
   - Memungkinkan pembaruan otomatis saat pengguna *login* atau *logout*.
2. **Shopping Cart**:
   - Memudahkan pengelolaan item di keranjang belanja yang diakses dari beberapa halaman (produk, checkout, dll.).
   - Perubahan di satu halaman langsung terlihat di seluruh aplikasi.
3. **Notifikasi dan Status Global**:
   - Membagikan pesan atau indikator status (misalnya, *loading*, *error*) ke berbagai *widget* tanpa duplikasi kode.

---

## 🎯 Kesimpulan
- **Ephemeral State Management**: Digunakan untuk kebutuhan lokal, sederhana, dan terbatas pada satu *widget*.
- **App State Management**: Pilihan utama untuk aplikasi besar dengan banyak komponen yang berbagi data, seperti pada *User Authentication*, *Shopping Cart*, dan notifikasi global.

Memahami kebutuhan aplikasi dan memilih metode pengelolaan *state* yang tepat akan sangat membantu untuk membangun aplikasi Flutter yang efisien, mudah dirawat, dan sesuai skala.

