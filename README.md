# 🛍️ Lokaria — Toko Online Interaktif

Website toko online satu halaman yang interaktif dan menarik, lengkap dengan sistem login. Dibuat dengan HTML, CSS, dan JavaScript murni (tanpa framework), sehingga mudah di-hosting di GitHub Pages.

## ✨ Fitur

- **Tampilan modern**: hero bergradasi, animasi hover, mode gelap/terang, dan responsif di HP maupun desktop
- **Katalog produk**: pencarian, filter kategori, dan pengurutan (terpopuler, harga, rating)
- **Detail produk**: tampilan popup dengan deskripsi dan harga diskon
- **Wishlist**: simpan produk favorit
- **Keranjang belanja**: tambah, kurangi, dan hapus item, tersimpan otomatis
- **Sistem login**: daftar, masuk, dan keluar, dengan password yang di-hash (SHA-256)
- **Checkout**: hanya untuk pengguna yang sudah login, dengan riwayat pesanan per akun
- **Flash sale**: hitung mundur yang reset setiap tengah malam
- **Gratis ongkir**: otomatis untuk belanja minimal Rp300.000

## 🚀 Cara Menjalankan

### Secara lokal
Buka file `index.html` langsung di browser. Tidak perlu instalasi apa pun.

### Publish di GitHub Pages
1. Unggah `index.html` dan `README.md` ke repository **Public**.
2. Buka **Settings → Pages**.
3. Pada *Build and deployment*, pilih **Deploy from a branch**, branch `main`, folder `/ (root)`, lalu **Save**.
4. Tunggu 1–3 menit. Situs akan aktif di `https://username.github.io/nama-repo`.

## 🎨 Kustomisasi

Semua ada di satu file `index.html`.

| Yang ingin diubah | Lokasi |
|---|---|
| Nama toko | Cari teks `Lokaria` (logo, `<title>`, footer) |
| Warna utama | Variabel `--primary` dan `--primary2` di bagian `:root` |
| Produk | Array `PRODUCTS` di bagian `<script>` |
| Batas gratis ongkir | Cari `300000` di fungsi checkout |

Contoh produk:

```js
{id:13, name:"Nama Produk", cat:"Kategori", price:150000, old:200000,
 rating:4.8, sold:100, emoji:"🎁", c:["#6c4dff","#b79dff"], desc:"Deskripsi singkat."}
```

## ⚠️ Catatan Penting

GitHub Pages hanya mendukung hosting statis, sehingga:

- Akun, keranjang, dan pesanan disimpan di **localStorage** browser. Data tidak dibagikan antar perangkat.
- Sistem login ini cocok untuk **demo dan presentasi**, belum aman untuk produksi.
- Pembayaran dan pesanan bersifat simulasi.

Untuk toko sungguhan, hubungkan ke backend seperti **Firebase Auth/Firestore** atau **Supabase**, serta payment gateway seperti **Midtrans** atau **Xendit**.

## 🛠️ Teknologi

HTML5 · CSS3 (Grid, Flexbox, variabel CSS) · JavaScript ES6 · Web Crypto API · localStorage

## 📄 Lisensi

Bebas digunakan dan dimodifikasi untuk kebutuhan proyek Anda.
