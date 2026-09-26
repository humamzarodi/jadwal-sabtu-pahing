# Jadwal Penceramah Pengajian Malam Sabtu Pahing

Website statis untuk menampilkan jadwal penceramah pengajian rutin
**Takmir Masjid An-Nuur & Langgar Kakung**.

## Struktur folder

```
jadwal-penceramah/
├── index.html              ← halaman utama
├── css/
│   └── style.css           ← semua styling
└── assets/
    ├── logo.svg             ← logo masjid
    ├── avatars/              ← foto placeholder (belum ada foto asli)
    │   ├── avatar-placeholder-1.svg
    │   ├── avatar-placeholder-2.svg
    │   └── avatar-placeholder-3.svg
    └── photos/
        └── humam-zarodi.jpg  ← foto penceramah asli
```

## Cara menambah / mengubah jadwal

Buka `index.html`, cari blok `<div class="entry">...</div>` yang mewakili
satu penceramah, lalu ubah:

- **Tanggal** — angka di `<span class="day">` dan bulan+tahun di `<span class="month">`
- **Foto** — ganti `src="..."` pada `<img class="avatar">` ke file foto di folder `assets/photos/`
  (upload foto barunya ke folder itu dulu)
- **Nama** — ubah teks di `<p class="name">`

Untuk menambah entri baru, salin (copy-paste) satu blok `<div class="entry">...</div>`
lalu ubah isinya.

## Cara upload ke GitHub & tayangkan lewat GitHub Pages

1. Buat repository baru di GitHub (boleh public atau private, tapi GitHub Pages
   gratis hanya untuk repo public — atau pakai GitHub Pro untuk repo private).
2. Upload seluruh isi folder ini (`index.html`, folder `css/`, folder `assets/`)
   ke repo tersebut — bisa lewat web ("Add file → Upload files") atau lewat git:
   ```bash
   git init
   git add .
   git commit -m "Jadwal penceramah pengajian"
   git branch -M main
   git remote add origin https://github.com/USERNAME/NAMA-REPO.git
   git push -u origin main
   ```
3. Di repo GitHub, buka **Settings → Pages**.
4. Pada **Source**, pilih branch `main` dan folder `/ (root)`, lalu **Save**.
5. Tunggu 1–2 menit, situs akan tayang di:
   `https://USERNAME.github.io/NAMA-REPO/`

Tidak perlu build tool atau server tambahan — semua file sudah statis dan siap pakai.
