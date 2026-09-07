# backend-nrp

Repo tugas mata kuliah **Pengembangan Backend Dasar**, dibuat dari template [`webdev-if-its/backend-template`](https://github.com/webdev-if-its/backend-template). Ganti judul di atas jadi nama repo kalian sendiri (`backend-nrp`, contoh: `backend-5025201012`).

## Aturan Umum

- Tugas tiap pertemuan disimpan di folder `pertemuan-XX/` pada repo ini.
- Commit message wajib menyebut level yang dicapai: `pertemuan-XX: level N selesai`.
- Deadline push: sebelum pertemuan berikutnya dimulai.
- Semua level dicek otomatis lewat `go test` — baca `pertemuan-XX/SOAL.md` tiap minggu untuk detail levelnya.

## Mengambil Pertemuan Baru Tiap Minggu

Repo ini **tidak otomatis sinkron** dengan template dosen. Begitu ada pertemuan baru, jalankan (ganti `pertemuan-02` sesuai minggu berjalan):

```bash
git fetch https://github.com/webdev-if-its/backend-template.git main
git checkout FETCH_HEAD -- pertemuan-02
```

Perintah ini **aman dijalankan kapan pun** — tidak akan menimpa folder pertemuan lain yang sudah kalian kerjakan, karena hanya mengambil folder yang disebutkan. Setelah itu, commit folder barunya seperti biasa.

Kalau dosen memperbaiki sesuatu di pertemuan yang sudah dirilis (mis. ada bug di test), biasanya cukup ambil ulang file yang diperbaiki saja, bukan seluruh folder — akan diumumkan file mana yang berubah.

---

Bagian di bawah ini **isi bertahap** sesuai level yang sedang kalian kerjakan (lihat `pertemuan-01/SOAL.md`) — heading-nya dicek otomatis, jangan diganti namanya.

## Identitas
- Nama: Hanifah Dwi Setyowati
- NRP: 5053241022
- Kelas: M

## Commit vs Push
git commit adalah ketika programmer menyimpan perubahan yang ada di kode di konteks lokal komputernya. sedangkan git push adalah ketika programmer mengirimkan perubahan kodenya ke atas, dari lokal komputer ke online agar bisa diakses oleh timnya.

contoh situasinya misal ada anggota tim yang commit satu modul fitur aplikasi tetapi lupa untuk push kodenya. akibatnya, anggota tim lain yang pull dari github tidak melihat adanya pembaruan dari modul fitur tersebut dan bisa saja mengerjakannya sendiri dari awal. ini mengakibatkan adanya pemborosan waktu karena tim jadi mengerjakan ulang modul yang sebenarnya sudah dikerjakan sebelumnya.

## Reproducibility
jika ada anggota tim yang menjalankan program ini dengan versi go berbeda, tidak akan ada masalah nyata yang terjadi. perbedaan versi go ini akan menjadi masalah ketika di tes program ada yang mengecek output dari runtime.Version() yang harus sama persis angka versinya. jika kasusnya seperti itu, maka tesnya bisa gagal di komputer anggota tim lain meskipun kodenya tidak salah.  

## Catatan Merge Conflict
merge conflict terjadi di baris return yang ada di dalam CetakInfo. bentrok terjadi karena ada branch yang mengubah baris yang sama. hasil akhirnya, kedua perubahan yang ada di dua branch ini digabung jadi satu. 

## Kenapa .gitignore Penting
.gitignore perlu untuk mencegah file penting yang harusnya pribadi malah tercommit ke repo online. misalkan file .exe ikut tercommit. setiap anggota tim yang build ulang kodenya di komputer, file buildnya bisa saja jadi bentrok dengan file build anggota lain yang ada di riwayat git nya. 

## Refleksi
yang paling membingungkan adalah soal nomor 8 yang menyelesaikan merge conflict. ketika ada conflict yang muncul bingung dan takut salah edit sehingga kode jadi rusak. karena di soal dijelaskan harus tidak ada sisa conflict marker, jadi saya hapus saja semua bagian kode yg conflict dan tulis ulang lalu menggabungkan perubahan yang terjadi.
