# Setup Profil GitHub — Aldiss1

Checklist singkat supaya README di atas benar-benar tampil.

---

## 1. Buat repo profil

1. Buka https://github.com/new
2. Nama repo: **`Aldiss1`** (harus sama persis dengan username, huruf besar/kecil berpengaruh)
3. Set **Public**
4. Jangan centang "Add a README file"
5. Create repository

Lalu dari folder ini:

```bash
cd ~/Aldiss1
git init
git add README.md
git commit -m "Add profile README"
git branch -M main
git remote add origin https://github.com/Aldiss1/Aldiss1.git
git push -u origin main
```

GitHub otomatis mendeteksi repo `Aldiss1/Aldiss1` sebagai profile README.

> Kalau `git push` minta login, pakai Personal Access Token (Settings → Developer settings → Tokens) atau `gh auth login`.

---

## 2. Ganti placeholder di README

Cari tanda `[ ... ]` lalu ganti:

| Placeholder | Ganti dengan |
| :-- | :-- |
| `[ struktur data lanjutan / clean architecture / topik lain ]` | yang benar-benar sedang kamu pelajari |
| `[ email kamu ]` (2 tempat) | email publik |
| `[username-linkedin]` | username LinkedIn |
| `[username-ig]` | username Instagram |

Kalau tidak punya LinkedIn/Instagram, hapus blok `<a>...</a>` yang bersangkutan.

---

## 3. Isi bio profil

Buka https://github.com/settings/profile

- **Bio** (maks 160 karakter), contoh:
  ```
  Mahasiswa Polinema · Web & Mobile Developer · Laravel, Flutter, MySQL
  ```
- **Company / Location**: `Politeknik Negeri Malang`
- **Website**: link GitHub Pages `portfolio` kalau sudah live
- **Social accounts**: tambahkan LinkedIn & Instagram

---

## 4. Isi description + topics repo (penting!)

Repo tanpa description membuat kartu pinned terlihat kosong. Buka tiap repo → ikon gear di sebelah **About**.

| Repo | Description | Topics |
| :-- | :-- | :-- |
| `portfolio` | Personal portfolio website built with TypeScript | `portfolio`, `typescript`, `web` |
| `PBL_SmartReceipt` | Mobile app for scanning and managing shopping receipts | `flutter`, `dart`, `ocr`, `mobile-app` |
| `MPPM_Aldi` | Data analysis and machine learning experiments | `jupyter-notebook`, `machine-learning`, `data-analysis` |
| `PWL_POS` | Point of sale system for transactions and stock management | `pos`, `javascript`, `web-app` |
| `PraktikumPWL` | Web programming course assignments | `php`, `laravel`, `coursework` |
| `CM1_ASD25_03_07` | Data structures coursework (Java) | `java`, `data-structures` |

---

## 5. Pin repo

Di halaman profil → **Customize your pins** → pilih maksimal 6:

1. `portfolio`
2. `PBL_SmartReceipt`
3. `PWL_POS`
4. `MPPM_Aldi`
5. `PraktikumPWL`
6. `CM1_ASD25_03_07`

Urutan pin menentukan urutan tampil.

---

## 6. Cek hasil

Buka https://github.com/Aldiss1 dan pastikan:

- [ ] Banner tampil, teks terbaca di light **dan** dark mode (toggle tema di Settings → Appearance)
- [ ] Typing SVG bergerak
- [ ] Ikon tech stack muncul semua
- [ ] Kartu stats & streak berdampingan di desktop, bertumpuk di mobile
- [ ] Tabel proyek rapi
- [ ] Badge kontak bisa diklik

---

## Catatan teknis

**Kalau kartu stats kosong / "Something went wrong"**
Instance publik `github-readme-stats.vercel.app` punya rate limit bersama. Solusi:
- Tunggu beberapa menit lalu refresh (cache GitHub juga ikut, bisa sampai 1 jam)
- Atau ganti ke `https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Aldiss1`
- Atau self-host: fork `anuraghazra/github-readme-stats` lalu deploy ke Vercel sendiri

**Kalau ingin commit privat ikut terhitung**
`count_private=true` hanya bekerja untuk commit di repo yang kamu miliki. Untuk organisasi, perlu izin akses repo saat authorize app-nya.

**Menghindari README berat**
Jangan tambahkan snake animation, trophies, atau visitor counter. Ketiganya menambah request gambar dan sering gagal render di cache GitHub.
