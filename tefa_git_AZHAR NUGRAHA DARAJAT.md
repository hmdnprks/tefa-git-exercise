# Soal & Jawaban Tugas Exercise Git
***Azhar Nugraha Darajat
Front-End Role***

## Latihan Konsep Git

1.  Jelaskan perbedaan antara command  `git pull`  dan  `git fetch`.
- `git pull`
Perintah ini akan mengambil commit terbaru dari branch remote repository kemudian melakukan merge kedalam local repository kita. Perintah ini digunakan ketika kita tidak pernah melakukan commit pada local repository kita. Jika kita menggunakan perintah ini ketika sudah melakukan commit di local repo, maka akan terjadi *merge conflict*.
- `git fetch`
Mirip seperti perintah `git pull`, perintah ini akan mengambil commit terbaru dari branch remote repository hanya saja tidak melakukan merge langsung ke local repository kita. Oleh karena itu, perintah ini dinilai aman dibandingkan dengan perintah `git pull`, karena perintah ini tidak akan mengubah current working file di local repository. Perintah ini kurang lebih akan melakukan cek perubahan pada remote repository.

2.  Jelaskan konsep  `rebase`  pada Git dan perbedaannya dengan  `merge`.
Perintah `rebase` mengizinkan kita untuk memindahkan atau menggabungkan seluruh commit dari suatu branch ke branch lain. Sederhananya, perintah ini akan mengabungkan seluruh commit dari kedua branch menjadi satu. Disamping itu, perintah `merge` akan menggabungkan seluruh commit dari suatu branch menjadi satu commit baru yang kemudian disatukan ke branch lain.

3.  Apakah itu  `git cherry-pick`  dan kapan sebaiknya kita menggunakan command tersebut?
Perintah ini digunakan untuk memilih satu atau beberapa commit dari suatu branch kemudian menambahkannya kedalam branch lainnya sebagai current HEAD. Perintah ini sebaiknya digunakan ketika bug hotfixes telah dilakukan, dimana dalam kolaborasi team seseorang telah melakukan perbaikan dari suatu fitur tertentu di branch lain, maka perbaikan tersebut dapat kita ambil dengan perintah `git cherry-pick <commit-hash>`. Selain itu, ketika kita secara tidak sengaja melakukan commit ke branch yang salah, maka kita dapat memindahkan commit tersebut ke branch yang seharusnya dituju dengan perintah ini.

5.  Jelaskan langkah-langkah cara  _resolve conflict_  di Git.
- Git akan menampilkan file mana saja yang terjadi *conflict* ketika kita melakukan merging file yang memiliki *conflict*
- Kita dapat melihat *conflict* tersebut dengan membuka file tersebut dengan code editor disertai dengan tanda berikut:
a. <<<<<<<	: Baris awal dari *conflict*
b. =======	: Batas pemisah antara kedua perubahan yang memiliki *conflict*
c. >>>>>>>	: Baris akhir dari *conflict*
- Untuk memutuskan bagaimana cara menyelesaikan *conflict* tersebut, kita dapat mendiskusikannya dengan developer  yang membuat commit pada file *conflict* tersebut.
- Masukkan file tersebut kedalam staging area dengan perintah `git add <file>`
- Eksekusi perintah rebase yaitu `git rebase --continue` atau bisa juga dengan perintah commit `git commit -m <message>`

6.  Bagaimana cara membatalkan  `commit`  yang sudah terlanjut ter-_push_  ke repository?
Dengan menggunakan perintah `git revert` disertai dengan hash commit yang akan di rollback: `git revert <commit_hash>`.

## Soal & Jawaban Latihan Command Git

Jelaskan fungsi-fungsi dari  _list command_  Git berikut

1.  `git branch -d feature-login`
Menghapus local branch bernama `feature-login`.

2.  `git checkout -b feature-register`
Membuat local branch bernama `feature-register`.

3.  `git stash apply`
Mengembalikan perubahan yang telah kita simpan dengan perintah `git stash`.

5.  `git tag -a v1.0.1`
Membuat sebuah annotated tag dengan identifier `v1.0.1`.

6.  `git diff HEAD introduction.html`
Membandingkan perubahan pada file di *working directory* dengan file `introduction.html`.

7.  `git pull --rebase`
mengambil commit terbaru dari branch remote repository kemudian melakukan rebase kedalam local repository kita.

8.  `git commit -m "some changes" --no-verify`
Melakukan commit dengan pesan "some changes" tanpa menjalankan *git hooks*.

9.  `git remote add upstream https://github.com/hmdnprks/tefa-git-exercise.git`
Membuat koneksi baru ke repository yang di-*fork* ke repository kita yaitu `https://github.com/hmdnprks/tefa-git-exercise.git`.

10.  `git reset --hard`  
Mengubah state di current HEAD kembali ke state commit terakhir.
 
11. `git mv home.html Home.html`
Rename file `home.html` menjadi `Home.html`.
