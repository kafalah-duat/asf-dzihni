# العصف الذهني للتوسع الدعوي للمشاريع ١٤٤٨ هـ

Website statis untuk GitHub Pages. Semua, termasuk data, ada di satu repository GitHub.
Data disimpan di file `data.json`; setiap perubahan menjadi commit.

## Isi folder
- `index.html` : aplikasi
- `config.js` : isi username dan nama repo
- `data.json` : data proyek (awalnya kosong)
- `.nojekyll`

## Langkah 1: Repo & Pages
1. Buat repository baru di GitHub, unggah semua isi folder ini (termasuk `.nojekyll`).
2. Isi `config.js`: `GH_OWNER` (username) dan `GH_REPO` (nama repo), lalu commit.
3. **Settings > Pages > Source: Deploy from a branch > main / (root)**.
4. Situs tampil di `https://USERNAME.github.io/NAMA-REPO/`.

## Langkah 2: Token untuk yang mengedit
Setiap pengedit membuat token sendiri (hanya sekali per browser):
1. GitHub > **Settings > Developer settings > Personal access tokens > Fine-grained tokens > Generate new token**.
2. *Repository access*: **Only select repositories** > pilih repo ini.
3. *Permissions > Repository permissions > Contents*: **Read and write**.
4. Salin token, buka situs, klik **تسجيل الدخول للتحرير** di sidebar, tempel token.

Pengunjung tanpa token hanya bisa melihat (read-only). Pemilik repo harus menambahkan pengedit lain sebagai **Collaborator** (Settings > Collaborators) agar token mereka bisa menulis.

## Menambah / mengubah bagian
- **Tambah bagian**: tombol **+ إضافة قسم** di sidebar (setelah login).
- **Ubah nama**: buka halaman bagian, klik nama besar di atas, lalu ketik nama baru.
- **Hapus bagian**: tombol **حذف القسم**; hanya bisa jika bagian itu sudah tidak punya proyek.
- Daftar bagian tersimpan di `data.json` (bagian `depts`), jadi berlaku untuk semua orang.

## Catatan
- Token tersimpan di browser pengedit (localStorage). Jangan dipakai di komputer umum; pakai tombol keluar setelah selesai.
- Jika repo **public**, `data.json` bisa dibaca siapa saja. Repo private tidak bisa dibuka lewat Pages gratis.
- Setiap simpan membuat satu commit, jadi riwayat perubahan ada di GitHub. Simpan berjalan 2 detik setelah berhenti mengetik.
- Data diperbarui otomatis tiap 90 detik; muat ulang halaman untuk melihat perubahan orang lain segera.
- Perubahan `data.json` memicu build ulang Pages (tidak berbahaya). Bila mau menghindarinya, simpan data di branch lain (`GH_BRANCH:"data"`) yang dibuat manual.
