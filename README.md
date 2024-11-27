# 🌟 Flutter State Management Codelab 🌟

## ✨ Deskripsi
Codelab ini akan mengeksplorasi dua pendekatan utama dalam state management pada Flutter. Dimana anda akan belajar mengenai:
1. **Ephemeral State**: Mengelola status lokal menggunakan `StatefulWidget`.
2. **App State**: Mengelola status global menggunakan paket `scoped_model`.

Dua pendekatan ini akan memberikan wawasan tentang cara mengelola status aplikasi, baik untuk skenario sederhana maupun kompleks.

---

## 📂 Struktur Proyek
Repositori ini terdiri dari dua proyek:
- 📁 **ephemeral_state_codelab**: Contoh implementasi dengan `StatefulWidget`.
- 📁 **app_state_codelab**: Contoh implementasi dengan `scoped_model`.

---

## 🆚 Perbandingan Pendekatan

| **🛠️ Aspek**               | **Ephemeral State** (StatefulWidget)             | **App State** (scoped_model)                     |
|----------------------------|------------------------------------------------|-------------------------------------------------|
| **📌 Scope (Lingkup)**      | Berlaku hanya pada widget tertentu.             | Berlaku global di seluruh aplikasi.             |
| **🗄️ Penyimpanan Status**   | Disimpan dalam widget menggunakan `StatefulWidget`. | Disimpan dalam model yang diakses banyak widget. |
| **🔄 Pembaruan Status**     | Menggunakan `setState` untuk memperbarui UI lokal. | Menggunakan `notifyListeners` untuk memperbarui semua widget terkait. |
| **📦 Ketergantungan**       | Tidak memerlukan paket eksternal (API bawaan Flutter). | Membutuhkan instalasi paket `scoped_model`.      |
| **⚙️ Implementasi**         | Mudah dan cepat untuk fitur kecil.              | Memerlukan pemahaman tambahan tentang model global. |
| **⏳ Persistensi Status**   | Status hilang saat widget dihapus atau aplikasi di-restart. | Status tetap terjaga selama aplikasi berjalan.   |
| **📋 Contoh Penggunaan**    | Fitur kecil seperti tombol atau formulir input. | Aplikasi kompleks seperti autentikasi atau keranjang belanja. |
| **📈 Kompleksitas**         | Cocok untuk skenario sederhana.                 | Lebih kompleks, tetapi fleksibel untuk aplikasi besar. |

---

## 🔍 Pengamatan dan Kesimpulan

### 🧐 Pengamatan
1. **Ephemeral State Management**:
   - Ideal untuk fitur-fitur kecil dan lokal.
   - Kurang efisien untuk kebutuhan status global.

2. **App State Management**:
   - Sangat fleksibel dan efisien untuk aplikasi dengan status yang kompleks.
   - Memerlukan pemahaman tambahan tentang arsitektur model global.

### 💡 Kesimpulan
Pemilihan metode tergantung pada kebutuhan aplikasi:
- Gunakan **Ephemeral State** untuk interaksi lokal yang sederhana.
- Gunakan **App State** untuk aplikasi besar yang membutuhkan koordinasi status antar-widget.

---

## 🚀 Cara Menjalankan Proyek

1. Clone repositori ini ke komputer Anda:
   ```bash
   git clone <repo-url>
   cd <repo-folder>
