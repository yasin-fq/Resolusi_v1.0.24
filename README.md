# 🎯 Resolusi Tahun Baru — v1.0.24 (Beta)

Aplikasi web resolusi tahun baru yang inspiratif & **bekerja 100% offline**.
Catat capaian, harapan, dan langkah terukur di **5 area kehidupan**.

> Dibuat dengan HTML, CSS, dan JavaScript murni — tanpa link eksternal. Bisa
> dijalankan tanpa internet, dan terpasang sebagai PWA di layar utama.

## 📦 Isi Paket Distribusi

| File | Keterangan |
|------|------------|
| `resolusi.html` | **Aplikasi utama** — satu file berisi semua (HTML+CSS+JS+PWA), siap di-hosting |
| `README.md` | File panduan ini |

## 🔐 Kode Akses (PIN)

Saat pertama dibuka, aplikasi meminta kode akses yang ditetapkan developer, jika perlu kode akses silahkan kujungi:

```
https://lynk.id/qafstudio
```

Kode ini hanya diminta **sekali** (saat aplikasi pertama dibuka). Setelah benar
dimasukkan, aplikasi terbuka langsung tanpa kode lagi.

> Untuk mengganti PIN: edit baris `var DEVELOPER_PIN = "123579";` di dalam
> `resolusi.html`, ganti dengan 6 digit angka pilihanmu.

## ✨ Fitur Utama

- **Pilihan penanggalan**: Masehi, Hijriah, atau kalender kustom
- **5 area resolusi**: Rohani, Finansial, Fisik & Kebugaran, Pengembangan Diri, Sosial
- **CRUD lengkap** per kategori: capaian tahun ini, harapan tahun depan, langkah-langkah terukur (ceklis)
- **Progres terukur** per kategori & keseluruhan + kutipan motivasi otomatis
- **Kode akses (PIN)** mengunci konten saat pertama dibuka
- **Ekspor / Impor Data** (backup JSON) untuk pindah antar perangkat
- **Reset Semua** untuk mulai dari awal
- **PWA** — bisa dipasang ke layar utama seperti aplikasi native
- **100% offline** — data tersimpan di localStorage browser perangkat

## 📱 Cara Memasang di Layar Utama (PWA)

> Asumsi: aplikasi sudah di-hosting pada alamat **https** (mis. Vercel, Netlify,
> GitHub Pages, atau hosting https Anda sendiri).

### 🤖 Android
1. Buka aplikasi di **Chrome**.
2. Tap menu **⋮** di kanan atas.
3. Pilih **"Tambahkan ke Layar Utama"** atau **"Install app"**.
4. Ikon muncul di layar HP — buka seperti aplikasi biasa.

### 🍎 iPhone / iPad
1. Buka aplikasi di **Safari**.
2. Tap tombol **Bagikan □↑**.
3. Pilih **"Tambah ke Layar Utama"**.
4. Buka dari ikon di layar — bekerja offline penuh.

### 💻 Komputer (Windows/Mac/Linux)
1. Buka aplikasi di **Chrome** atau **Edge**.
2. Klik ikon **Install** di address bar (ikon ⊕ atau tanda +).
3. Aplikasi terpasang sebagai aplikasi desktop dengan ikon sendiri — bisa dibuka dari Start Menu / Launchpad.

> 💡 Setelah terpasang, aplikasi bisa dibuka **tanpa internet**. Data tersimpan
> otomatis di perangkat.

## 💾 Manajemen Data

- Data tersimpan **otomatis** di browser perangkat (localStorage) — tidak perlu internet.
- **Pindah perangkat**: gunakan menu ⋮ → **Ekspor Data** (unduh file `.json`),
  lalu di perangkat baru: menu ⋮ → **Impor Data**.
- **Mulai dari awal**: menu ⋮ → **Reset Semua** (menghapus data + kode akses,
  layar PIN akan muncul lagi).

## 🛠️ Kustomisasi (untuk developer)

Semua konfigurasi ada di dalam `resolusi.html`:

| Yang diubah | Cari di file | Contoh |
|-------------|--------------|--------|
| **PIN akses** | `var DEVELOPER_PIN = "123579";` | ganti `"123579"` |
| **Nama area resolusi** | `CATEGORIES = [...]` | ubah `label:` |
| **Kutipan motivasi** | `var QUOTES = [...]` | tambah/ubah array |
| **Warna tema** | `:root { ... }` di `<style>` | ubah variabel CSS |

## ❓ FAQ

**Q: Apakah data saya aman?**
A: Ya. Semua data tersimpan lokal di perangkat Anda, tidak dikirim ke server mana pun.

**Q: Apakah bisa dipakai tanpa internet?**
A: Ya, 100% offline. Setelah aplikasi terpasang, tidak butuh internet lagi.

**Q: Bagaimana jika lupa PIN?**
A: Hapus data situs di browser, atau hapus file lalu unduh/buka lagi — layar
PIN akan muncul dan Anda bisa masukkan `123579`.

**Q: Bisakah data dipindah ke HP lain?**
A: Bisa, lewat Ekspor Data (file JSON) lalu Impor di HP tujuan.

---

© 2026 Resolusi 1.0.24 (Beta) | Hak Cipta Dilindungi
