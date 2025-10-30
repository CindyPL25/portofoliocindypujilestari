# Portfolio - Cindy Puji Lestari

Selamat datang di repositori portofolio Cindy Puji Lestari — sebuah website portofolio personal yang dirancang dengan estetika pastel, layout responsif, dan struktur sederhana sehingga mudah dipelihara dan dipublikasikan.

Website ini dibuat sebagai showcase pribadi untuk memperlihatkan profil, pencapaian, galeri, dan informasi kontak.

## Ringkasan

- Nama proyek : Portfolio Cindy Puji Lestari
- Pemilik : Cindy Puji Lestari
- Tipe : Static website (HTML, CSS)
- Lokasi file utama : `portofoliocindy.html`
- Tujuan : Menampilkan profil personal, pendidikan, pengalaman organisasi, pencapaian, foto galeri, dan kontak.

## Fitur utama

- Halaman beranda (Hero) dengan deskripsi singkat.
- Bagian "Tentang Saya" dengan tab Hobi, Pengalaman, dan Pendidikan (CSS-only tabs).
- Bagian Pencapaian (achievements) dengan kartu proyek.
- Galeri foto responsif.
- Form kontak statis (HTML form — perlu backend jika ingin menerima pesan).
- Desain responsif untuk berbagai ukuran layar.

## Teknologi yang digunakan

- HTML5
- CSS3 (variabel CSS, responsive media queries)

## Struktur proyek

```
portofolio/                      # root project
├─ portofoliocindy.html          # file HTML utama
├─ style.css                     # stylesheet utama
├─ README.md                     # (Anda sedang melihat ini)
├─ img/                          # folder gambar (foto, ikon proyek, dsb)
```

## Cara menjalankan secara lokal (menggunakan XAMPP)

1. Pastikan XAMPP terpasang dan Apache berjalan.
2. Salin/move folder proyek (`portofolio`) ke dalam folder `htdocs` XAMPP. Contoh path pada mesin Windows:

```powershell
# contoh (jalankan di PowerShell) - adaptasikan paths sesuai lokasi Anda
# pindah folder proyek ke htdocs jika belum berada di sana
Move-Item -Path "C:\path\ke\proyek\portofolio" -Destination "C:\xampp\htdocs\"
```

3. Buka browser dan akses:

```
http://localhost/portofolio/portofoliocindy.html
```

Catatan: Anda juga bisa membuka file langsung (double click pada `portofoliocindy.html`) tapi beberapa fitur (mis. fetch API atau request relatif) lebih andal melalui server lokal.

## Cara publish ke GitHub (GitHub Pages)

1. Buat repository baru di GitHub (mis. `portofoliocindy`).
2. Di folder proyek lokal, inisialisasi git dan push ke remote (ganti URL remote dengan milik Anda):

```powershell
cd C:\xampp\htdocs\portofolio
git init
git add .
git commit -m "Initial commit: portfolio Cindy"
git branch -M main
# ganti <URL-REPO> dengan URL repository Anda, contoh: https://github.com/username/portofoliocindy.git
git remote add origin <URL-REPO>
git push -u origin main
```

3. Aktifkan GitHub Pages di repository:
   - Buka Settings -> Pages -> Source -> pilih branch `main` dan folder `/ (root)` -> Save.
   - Setelah beberapa menit, website akan tersedia di `https://<username>.github.io/<repo>/`.

Tips: Jika Anda ingin menggunakan nama domain kustom, tambahkan file `CNAME` sesuai instruksi GitHub Pages.

## Hal yang perlu diperhatikan (catatan teknis)

- Pastikan semua gambar di folder `img/` ada dan memiliki ukuran yang sesuai untuk performa.
- Form kontak saat ini statis — untuk menerima pesan, tambahkan backend sederhana (mis. Netlify Forms, Formspree, atau server sendiri).

## Memperbaiki masalah tab (studi kasus)

Jika tab di bagian "Tentang Saya" tidak menampilkan isinya, penyebab yang umum:
- Struktur input radio dan konten tidak menjadi sibling yang sesuai dengan selector CSS.
- CSS men-set `.tab-content { display: none }` dan selector `#tab-hobby:checked ~ #hobby` membutuhkan input radio menjadi sibling langsung dari `#hobby`.

Solusi: Pastikan input radio berada di luar container label (sebagai sibling langsung terhadap `#hobby`, `#experience`, dan `#education`) atau gunakan JavaScript untuk meng-handle aktivasi tab.

## Cara berkontribusi

Jika Anda ingin membantu meningkatkan website ini:

1. Fork repository ini.
2. Buat branch fitur: `git checkout -b feature/nama-fitur`.
3. Lakukan perubahan dan commit.
4. Buka Pull Request ke repository utama.

Mohon sertakan screenshot atau penjelasan singkat untuk perubahan desain.

## Lisensi

Jika Anda ingin lisensi permissive, saya merekomendasikan MIT. Bila Anda setuju, saya bisa tambahkan file `LICENSE`.

## Kontak

Jika perlu bantuan lebih lanjut atau ingin saya bantu menambahkan fitur (mis. JavaScript untuk tab + menu, atau setup deployment otomatis), hubungi:

- Email: cindypujilestari8@gmail.com

---

Terima kasih telah membagikan portofolio Anda — website ini sudah terlihat sangat rapi dan estetik. Jika mau, saya bisa:
- Tambahkan file `LICENSE` (MIT).
- Bantu menyiapkan GitHub Actions untuk deploy otomatis ke GitHub Pages.

Beritahu saya mana yang mau Anda lanjutkan.

## Gambar Dokumentasi (keterangan gambar + gambar saja)

Tempat untuk menaruh gambar dokumentasi tiap halaman. Format: satu baris keterangan singkat (nama file), lalu baris gambar. Anda yang akan mengisi gambar di folder `img/docs/<halaman>/`.

### Home
home-1.png
![home-1](img/docs/home/home-1.png)

### About
about-1.png
![about-1](img/docs/about/about-1.png)

### Achievements
achievements-1.png
![achievements-1](img/docs/achievements/achievements-1.png)

### Gallery
gallery-1.png
![gallery-1](img/docs/gallery/gallery-1.png)

### Contact
contact-1.png
![contact-1](img/docs/contact/contact-1.png)