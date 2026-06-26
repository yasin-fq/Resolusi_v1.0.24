# 🎯 Resolusi Tahun Baru — v1.0.24 (Beta)

Aplikasi web resolusi tahun baru yang inspiratif & **bekerja 100% offline**.
Catat capaian, harapan, dan langkah terukur di **5 area kehidupan**.

> Dibuat dengan HTML, CSS, dan JavaScript murni — tanpa link eksternal. Bisa
> dijalankan tanpa internet, dan terpasang sebagai PWA di layar utama.
> Mendukung **2 bahasa: Indonesia & English**.

## 📦 Isi Paket Distribusi

| File | Keterangan |
|------|------------|
| `resolusi.html` | **Aplikasi utama** — satu file berisi semua (HTML+CSS+JS+PWA+i18n), siap di-hosting |
| `README.md` | File panduan ini |

## 🌐 Bahasa

Aplikasi mendukung **2 bahasa**:
- 🇮🇩 **Indonesia** (default)
- 🇬🇧 **English**

Tombol toggle bahasa (bulat, bertuliskan "EN"/"ID") tersedia di:
- Layar kode akses (pojok kanan atas)
- Halaman onboarding (pojok kanan atas)
- Dashboard header (di samping tombol edit tahun)

Pilihan bahasa tersimpan otomatis di perangkat.

## 🔐 Kode Akses (PIN)

Saat pertama dibuka, aplikasi meminta kode akses:

```
PIN: 1 3 5 7 9 0
```

**Catatan keamanan:** Input kode berupa field teks (password, ter-mask) —
bukan keypad 6 digit. Ini agar penebak tidak tahu format kode (bisa
huruf/angka/simbol, panjang berapa pun). Kode yang benar tetap 6 digit angka.

Kode hanya diminta **sekali**. Setelah benar dimasukkan, aplikasi terbuka
langsung tanpa kode lagi.

> Untuk mengganti PIN: edit baris `var DEVELOPER_PIN = "135790";` di dalam
> `resolusi.html`, ganti dengan kode pilihanmu.

## ✨ Fitur Utama

- **Pilihan penanggalan**: Masehi (Gregorian), Hijriah, atau kalender kustom
- **5 area resolusi**: Rohani, Finansial, Fisik & Kebugaran, Pengembangan Diri, Sosial
- **CRUD lengkap** per kategori: capaian tahun ini, harapan tahun depan, langkah-langkah terukur (ceklis)
- **Progres terukur** per kategori & keseluruhan + kutipan motivasi otomatis
- **Kode akses (PIN)** mengunci konten saat pertama dibuka
- **Ekspor / Impor Data** (backup JSON) untuk pindah antar perangkat
- **Reset Semua** untuk mulai dari awal
- **PWA** — bisa dipasang ke layar utama seperti aplikasi native
- **2 bahasa** — Indonesia & English
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
3. Aplikasi terpasang sebagai aplikasi desktop dengan ikon sendiri.

> 💡 Setelah terpasang, aplikasi bisa dibuka **tanpa internet**. Data tersimpan
> otomatis di perangkat.

## 🌐 Hosting https Gratis (opsional)

Jika belum punya hosting https, gunakan layanan gratis berikut:

| Layanan | Cara | URL |
|---------|------|-----|
| **Netlify Drop** | Drag & drop folder berisi `resolusi.html`, instan | https://app.netlify.com/drop |
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
| **Nama area resolusi** | `I18N` dict, key `cat.*.label` | ubah `id`/`en` |
| **Teks UI / terjemahan** | `I18N` dict | ubah/tambah key |
| **Kutipan motivasi** | `I18N` dict, key `quote.0`–`quote.6` | tambah/ubah |
| **Warna tema** | `:root { ... }` di `<style>` | ubah variabel CSS |

## ❓ FAQ

**Q: Apakah data saya aman?**
A: Ya. Semua data tersimpan lokal di perangkat Anda, tidak dikirim ke server mana pun.

**Q: Apakah bisa dipakai tanpa internet?**
A: Ya, 100% offline. Setelah aplikasi terpasang, tidak butuh internet lagi.

**Q: Bagaimana jika lupa PIN?**
A: Hapus data situs di browser, atau hapus file lalu unduh/buka lagi — layar
PIN akan muncul dan Anda bisa masukkan `135790`.

**Q: Bisakah data dipindah ke HP lain?**
A: Bisa, lewat Ekspor Data (file JSON) lalu Impor di HP tujuan.

**Q: Bagaimana ganti bahasa?**
A: Klik tombol bulat "EN"/"ID" di pojok kanan atas (atau di header dashboard).

---

© 2026 Resolusi 1.0.24 (Beta) | Hak Cipta Dilindungi
