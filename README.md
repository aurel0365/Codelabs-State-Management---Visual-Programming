# 🌟 Flutter State Management Codelab 🌟

## ✨ Deskripsi
Codelab ini akan memberikan panduan tentang dua pendekatan utama dalam mengelola state pada aplikasi Flutter:
1. **Ephemeral State**: Mengelola status lokal dengan menggunakan `StatefulWidget`.
2. **App State**: Mengelola status global dengan bantuan paket `scoped_model`.

Dengan mengikuti tutorial ini, Anda akan mendapatkan pemahaman yang lebih baik tentang cara mengelola state di aplikasi Flutter, baik untuk kasus yang sederhana maupun yang lebih kompleks.

---

## 📂 Struktur Proyek
Repositori ini terdiri dari dua contoh implementasi:
- 📁 **ephemeral_state_codelab**: Contoh menggunakan `StatefulWidget` untuk status lokal.
- 📁 **app_state_codelab**: Contoh menggunakan `scoped_model` untuk status global.

---

## 🆚 Perbandingan Pendekatan

| **🛠️ Aspek**               | **Ephemeral State** (StatefulWidget)             | **App State** (scoped_model)                     |
|----------------------------|------------------------------------------------|-------------------------------------------------|
| **📌 Scope (Lingkup)**      | Terbatas pada widget tertentu.                  | Menyeluruh di seluruh aplikasi.                 |
| **🗄️ Penyimpanan Status**   | Status disimpan dalam widget menggunakan `StatefulWidget`. | Status disimpan dalam model yang dapat diakses oleh berbagai widget. |
| **🔄 Pembaruan Status**     | Menggunakan `setState` untuk memperbarui tampilan lokal. | Menggunakan `notifyListeners` untuk memperbarui widget terkait. |
| **📦 Ketergantungan**       | Tidak membutuhkan paket tambahan (API bawaan Flutter). | Memerlukan paket eksternal `scoped_model`.      |
| **⚙️ Implementasi**         | Mudah untuk fitur sederhana.                    | Membutuhkan pemahaman tentang model global.     |
| **⏳ Persistensi Status**   | Status hilang saat widget dihapus atau aplikasi di-restart. | Status tetap ada selama aplikasi berjalan.     |
| **📋 Contoh Penggunaan**    | Cocok untuk fitur kecil seperti tombol atau formulir input. | Ideal untuk aplikasi besar seperti autentikasi atau keranjang belanja. |
| **📈 Kompleksitas**         | Sederhana dan cocok untuk aplikasi kecil.       | Lebih kompleks, namun cocok untuk aplikasi besar dengan banyak status. |

---

## 🌐 Keunggulan App State Management dalam Aplikasi Besar

Ketika mengembangkan aplikasi yang lebih besar, pengelolaan status yang baik sangat penting untuk menjaga performa dan kejelasan kode. Berikut adalah beberapa alasan mengapa **App State Management** lebih cocok untuk aplikasi besar:

1. **Pengelolaan Autentikasi Pengguna**:
   - Dengan App State, status pengguna yang sedang login dapat dikelola secara global, sehingga dapat dengan mudah mempengaruhi bagian lain dari aplikasi tanpa membuat kode menjadi berantakan.
   - Misalnya, setelah pengguna login, status login bisa langsung mempengaruhi tampilan halaman beranda atau akses ke fitur tertentu.

2. **Keranjang Belanja dalam Aplikasi E-Commerce**:
   - Untuk aplikasi e-commerce, App State memungkinkan pengelolaan status keranjang belanja dengan lebih mudah. Anda dapat mengupdate item di keranjang dari berbagai layar tanpa harus mengelola state secara manual di masing-masing widget.

3. **Pengelolaan Status yang Konsisten**:
   - Dengan menggunakan App State, status seperti tema aplikasi atau pilihan bahasa dapat dikelola secara konsisten di seluruh aplikasi, dan pembaruan status akan langsung terlihat pada seluruh widget yang terhubung.

4. **Skalabilitas yang Lebih Baik**:
   - Ketika aplikasi berkembang, App State memberikan fleksibilitas yang dibutuhkan untuk menambahkan lebih banyak fitur tanpa membuat kode menjadi semakin rumit.

5. **Menjaga Persistensi Status**:
   - App State memastikan bahwa status tetap ada selama aplikasi berjalan, meskipun aplikasi dimatikan atau di-restart, memberikan pengalaman pengguna yang lebih mulus.

---

## 🔍 Pengamatan dan Kesimpulan

### 🧐 Pengamatan
1. **Ephemeral State**:
   - Cocok untuk fitur-fitur kecil yang hanya mempengaruhi widget tertentu.
   - Tidak ideal untuk aplikasi dengan banyak status yang perlu disinkronkan antar-widget.

2. **App State**:
   - Lebih fleksibel dan efisien ketika aplikasi membutuhkan pengelolaan status yang lebih kompleks.
   - Memerlukan pemahaman lebih mendalam mengenai arsitektur global dalam aplikasi.

### 💡 Kesimpulan
- **Ephemeral State** lebih cocok digunakan untuk aplikasi kecil atau fitur sederhana.
- **App State** lebih tepat digunakan dalam aplikasi besar yang membutuhkan pengelolaan status di seluruh aplikasi, seperti pada aplikasi yang melibatkan autentikasi atau pengelolaan data pengguna.

---

## 🚀 Cara Menjalankan Proyek

1. Clone repositori ini ke komputer Anda:
   ```bash
   git clone <repo-url>
   cd <repo-folder>
