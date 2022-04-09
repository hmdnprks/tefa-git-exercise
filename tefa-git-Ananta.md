## Jawaban Soal Latihan Konsep Git

1.  command `git pull`, digunakan untuk mengambil commit terbaru dan merge dengan branch yang sedang aktif, sedangkan command `git fetch`, digunakan untuk menggambil commit, pada git fetch tidak langsung melakukan merge
2.  `git rebase` digunakan untuk menggabungkan atau menggeser commit base. Rebase pada dasarnya membutuhkan satu set commit, dan menyalin atau meletakan di tempat lain
3.  untuk menyalin serangkaian commit yang ditentukan di bawah lokasi yang sedang aktif, digunakan ketika ingin menyalin beberpa commit yang ditentukan misalnya, pada commit c2 dan c4, yang mana hanya commit tsb yang akan disalin
4.  - cara paling mudah untuk menyelesaikan file yang konflik adalah dangan membuka dan mengubahnya.
    - setelah melakukan perubahan pada file, gunakan command `git add` untuk menampilka konten baru yang digabungkan. Untuk menyelesaikan penggabungan buat commit baru.
    - Git akan melihat bahwa konflik telah diselesaikan dan membuat commit gabungan baru untuk menyelesaikan penggabungan.
5.  untuk membatalkan commit dapat menggunakan command `git revert` dan `git reset`

## Jawaban Soal Latihan Command Git

1.  `git branch -d feature-login`, digunakan untuk menghapus branch feature-login
2.  `git checkout -b feature-register` untuk membuat branch baru feature-register dan berpindah ke branch feature-register
3.  `git stash apply`, untuk menerapkan git stash ke direktori kerja saat ini
4.  `git tag -a v1.0.1`
5.  `git diff HEAD introduction.html`, untuk membandingkan versi file di direktori kerja dengan file repositori introduction.html
6.  `git pull --rebase`, untuk menerapkan perubahan lokal diterapkan kembali di atas perubahan remote
7.  `git commit -m "some changes" --no-verify`, melakukan commit dengan pesan "some change" tanpa menjalankan git hooks
8.  `git remote add upstream https://github.com/hmdnprks/tefa-git-exercise.git`, untuk menetapkan repo GitHub "hmdnprks/tefa-git-exercise.git" sebagai remote
9.  `git reset --hard`, untuk menghapus snapshot commit dan perubahan pada file secara otomatis tanpa perintah lanjutan secara permanen
10. `git mv home.html Home.html`, untuk rename file "home.html" menjadi "Home.html"
