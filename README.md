# 🎯 Resolusi Tahun Baru — v1.0.24 (Beta)

Aplikasi web resolusi tahun baru yang inspiratif & **bekerja 100% offline**.
Catat capaian, harapan, dan langkah terukur di **5 area kehidupan**.

> Aplikasi ini dibuat dengan HTML, CSS, dan JavaScript murni — **tanpa link
> eksternal sama sekali**. Cukup satu file `resolusi.html`, bisa dijalankan
> tanpa internet.

## 📦 Isi Paket Distribusi

| File | Keterangan |
|------|------------|
| `resolusi.html` | **Aplikasi utama** — satu file berisi semua (HTML+CSS+JS), bisa langsung dibuka |
| `README.md` | File panduan ini |

## 🔐 Kode Akses (PIN)

Saat pertama dibuka, aplikasi meminta kode akses **6 digit** yang ditetapkan developer:

```
PIN: 1 3 5 7 9 0
```

Kode ini hanya diminta **sekali** (saat aplikasi pertama dibuka). Setelah benar
dimasukkan, aplikasi terbuka langsung tanpa kode lagi.

> Untuk mengganti PIN: edit baris `var DEVELOPER_PIN = "135790";` di dalam
> `resolusi.html`, ganti dengan 6 digit angka pilihanmu.

## ✨ Fitur Utama

- **Pilihan penanggalan**: Masehi, Hijriah, atau kalender kustom
- **5 area resolusi**: Rohani, Finansial, Fisik & Kebugaran, Pengembangan Diri, Sosial
- **CRUD lengkap** per kategori: capaian tahun ini, harapan tahun depan, langkah-langkah terukur (ceklis)
- **Progres terukur** per kategori & keseluruhan + kutipan motivasi otomatis
- **Kode akses (PIN)** mengunci konten saat pertama dibuka
- **Ekspor / Impor Data** (backup JSON) untuk pindah antar perangkat
- **Reset Semua** untuk mulai dari awal
- **PWA-ready**: bisa di-install ke layar utama seperti aplikasi native
- **100% offline** — data tersimpan di localStorage browser perangkat

## 📱 Cara Pakai & Pasang

### 💻 Di Komputer (Windows/Mac/Linux)
1. Simpan `resolusi.html` di folder yang mudah dijangkau.
2. Klik ganda file → otomatis terbuka di browser → langsung bisa dipakai offline.
3. (Opsional) Tarik tab browser ke taskbar/dock untuk akses cepat.

### 📱 iPhone / iPad (paling mudah — tanpa https)
1. Pindahkan `resolusi.html` ke HP (via AirDrop, iCloud, email, atau Files app).
2. Buka file di **Safari**.
3. Tap tombol **Bagikan □↑** → **"Tambahkan ke Layar Utama"**.
4. Ikon muncul di layar → buka seperti aplikasi, bekerja offline penuh. ✅

### 🤖 Android
**Opsi 1 — Pintasan cepat (tanpa https):**
1. Pindahkan file ke HP (WhatsApp, email, USB).
2. Buka file di **Chrome**.
3. Tap menu **⋮** → **"Tambahkan ke Layar Utama"** (jadi pintasan).

**Opsi 2 — Install penuh (butuh https):**
1. Hosting file di **Netlify Drop** (gratis, otomatis https):
   - Buka https://app.netlify.com/drop
   - Drag folder berisi `resolusi.html` ke sana
   - Dapat URL https langsung
2. Buka URL https-nya di **Chrome Android**.
3. Akan muncul tombol **"Install"** (atau menu ⋮ → "Install app").

### 🌐 Hosting https gratis (opsional, untuk Android install penuh)
| Layanan | Cara | URL |
|---------|------|-----|
| **Netlify Drop** | Drag & drop folder, instan | https://app.netlify.com/drop |
| **GitHub Pages** | Upload ke repo → Settings → Pages | https://pages.github.com |
| **Cloudflare Pages** | Connect repo, deploy | https://pages.cloudflare.com |
| **Vercel** | Connect repo, deploy | https://vercel.com |

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
| **PIN akses** | `var DEVELOPER_PIN = "135790";` | ganti `"135790"` |
| **Nama area resolusi** | `CATEGORIES = [...]` | ubah `label:` |
| **Kutipan motivasi** | `var QUOTES = [...]` | tambah/ubah array |
| **Warna tema** | `:root { ... }` di `<style>` | ubah variabel CSS |

## ❓ FAQ

**Q: Apakah data saya aman?**
A: Ya. Semua data tersimpan lokal di perangkat Anda, tidak dikirim ke server mana pun.

**Q: Apakah bisa dipakai tanpa internet?**
A: Ya, 100% offline. Setelah file dibuka sekali, tidak butuh internet lagi.

**Q: Bagaimana jika lupa PIN?**
A: Hapus data situs di browser, atau hapus file lalu unduh/buka lagi — layar
PIN akan muncul dan Anda bisa masukkan `135790`.

**Q: Bisakah data dipindah ke HP lain?**
A: Bisa, lewat Ekspor Data (file JSON) lalu Impor di HP tujuan.

---

© 2026 Resolusi 1.0.24 (Beta) | Hak Cipta Dilindungi
