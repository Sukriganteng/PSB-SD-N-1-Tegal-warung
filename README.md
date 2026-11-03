# SPMB SD Negeri 1 Tegalwarung — Tahun Ajaran 2026/2027

Website statis untuk Penerimaan Murid Baru (SPMB) SD Negeri 1 Tegalwarung. Memuat profil sekolah, alur pendaftaran, persyaratan, jadwal, FAQ, galeri, kontak, dan tombol menuju formulir pendaftaran (Google Form).

## Struktur file

```
.
├── index.html     # Struktur & isi halaman
├── style.css      # Tampilan (tema warna, layout, mode gelap)
├── script.js      # Data sekolah (CONFIG), hitung mundur, pencarian, navigasi
├── README.md
└── images/        # Foto galeri kegiatan
    ├── drumband.jpg
    ├── pramuka.jpg
    ├── silat.jpg
    ├── badminton.jpg
    ├── lomba-lari.jpg
    └── kegiatan-religi.jpg
```

## Cara menjalankan

Tidak perlu instalasi. Cukup buka `index.html` di browser. Pastikan semua file tetap berada dalam satu folder dengan susunan seperti di atas.

Untuk menayangkannya secara online, unggah seluruh folder ke hosting statis seperti GitHub Pages, Netlify, atau Cloudflare Pages.

## Mengubah data sekolah

Buka `script.js`, lalu edit objek `CONFIG` di bagian atas:

| Kunci | Fungsi |
|---|---|
| `alamat`, `telp`, `email`, `jam` | Data kontak yang tampil di bagian Kontak |
| `waNumber` | Nomor WhatsApp, format internasional tanpa `+` (contoh `6281327635272`) |
| `penutupan` | Batas akhir pendaftaran untuk hitung mundur (format `YYYY-MM-DDTHH:MM:SS`) |
| `formUrl` | Tautan Google Form pendaftaran |
| `maps` | Tautan Google Maps lokasi sekolah |
| `instagram`, `facebook`, `youtube` | Tautan media sosial di footer |

## Mengubah isi lain

- **Teks, jadwal, persyaratan, FAQ:** edit langsung di `index.html`. Tanggal pada tabel jadwal masih berupa contoh, sesuaikan dengan jadwal resmi.
- **Warna tema:** ubah variabel di blok `:root` pada bagian atas `style.css`.
- **Foto galeri:** ganti file di folder `images/` dengan nama yang sama, atau ubah `src` dan `alt` pada bagian Galeri di `index.html`.

## Fitur

- Satu halaman per menu (navigasi berbasis `#hash`, mis. `index.html#syarat`)
- Hitung mundur penutupan pendaftaran
- Pencarian informasi (ikon 🔍)
- Mode terang/gelap, tersimpan otomatis di browser
- Tampilan responsif untuk ponsel dan desktop
- Tombol WhatsApp dan tombol kembali ke atas
- Animasi muncul saat scroll (dinonaktifkan otomatis bila pengguna memilih *reduced motion*)

## Catatan

- Font Nunito dan Poppins dimuat dari Google Fonts, jadi perlu koneksi internet. Tanpa koneksi, tampilan memakai font bawaan sistem.
- Peta belum disematkan; tombol "Buka di Google Maps" membuka tautan dari `CONFIG.maps`.
