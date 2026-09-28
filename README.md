# IsyaratKita

**Repo:** `meicha-isyarat`  
**Project Akhir:** Pemrograman Framework Laravel  
**Platform belajar Bahasa Isyarat Indonesia (BISINDO) untuk anak tunarungu, tuli, dan bisu — serta orang tua & guru.**

Guest/Public melihat konten dari database. Admin mengelola seluruh data.

## Masalah yang diselesaikan

Anak dengan hambatan dengar/bicara sering kekurangan materi belajar isyarat yang terstruktur, visual, dan mudah diakses keluarga. IsyaratKita menjadi pusat kamus isyarat, modul belajar bertahap, cerita visual, dan informasi kegiatan — dikelola admin, dikonsumsi publik.

## Peran pengguna

| Peran | Akses |
| --- | --- |
| Guest / Public | Beranda, kamus isyarat, modul belajar, cerita, artikel, agenda kegiatan, pencarian & filter |
| Admin | Login, dashboard, CRUD kategori/isyarat/modul/media/artikel/kegiatan, unggah gambar/video, laporan |

## Konsep Laravel yang diterapkan

- Arsitektur MVC, request flow (Route → Middleware → Controller → Validation → Model → Blade)
- Eloquent & relasi tabel, seeder data dummy
- Auth, session, middleware role admin
- Upload file (gambar & video isyarat)
- Search, filter, pagination
- Blade template, Blade component, layout Guest vs Admin
- Git history per fitur (bukan satu commit raksasa)

## Struktur data (rencana)

- `users` — akun admin
- `categories` — tema isyarat (keluarga, sekolah, emosi, angka, …)
- `signs` — entri kamus (kata, deskripsi, tingkat, media)
- `lessons` — modul belajar berurutan
- `lesson_sign` — relasi modul ↔ isyarat
- `articles` — panduan orang tua / guru
- `events` — workshop / kelas komunitas
- `media` — file gambar/video

## Template referensi (belum diterapkan)

Akan dibahas terpisah sesuai arahan dosen. Calon referensi Themewagon:

- Guest: tema edukasi anak (contoh Kidkinder / Education)
- Admin: dashboard gratis (contoh AdminKit / Soft UI)

Sumber: https://themewagon.com/theme-price/free/

## Menjalankan lokal

```bash
composer install
copy .env.example .env
php artisan key:generate
php artisan migrate
php artisan serve
```

## Commit convention (nanti)

```
feat: menambahkan CRUD kamus isyarat
feat: membuat halaman beranda guest
fix: memperbaiki validasi form unggah media
refactor: membuat blade component navbar
```
