### Muhamad Agil Fachrian

## Soal Konsep Git

1.  Jelaskan perbedaan antara command `git pull` dan `git fetch`.

    > **`git pull`** akan mengambil commit terbaru lalu akan menggabungkannya (merge) dengan branch yang aktif, sedangkan **`git fetch`** hanya mengambil commit saja dan tidak akan langsung melakukan merge.

2.  Jelaskan konsep `rebase` pada Git dan perbedaannya dengan `merge`.

    > **`rebase`** ini akan menggabungkan atau menggeser branch menjadi satu nanti akan membuat urutan commit menjadi linear dan log commit/history repositori akan lebih bersih dengan rebasing. Perbedaannya yaitu saat ketika menggabungkan branch, **`merge`** sangat cocok untuk branch yang sedikit karena jika menggunakan merge untuk branch yang banyak maka akan menjadi sulit membaca grafik commitnya sedangkan **`rebase`** sangat cocok untuk branch yang banyak dan membuat grafik commitnya mudah dibaca.

3.  Apakah itu `git cherry-pick` dan kapan sebaiknya kita menggunakan command tersebut?

    > **`git cherry-pick`** adalah perintah untuk mengambil satu per satu commit dari suatu branch ke branch lain dan nanti ada commit baru di cabang itu. Pemakaian **`git cherry-pick`** ketika kita sedang melakukan kolaborasi team, memperbaiki bug terbaru, membatalkan perubahan dan memulihkan commit yang hilang.

4.  Jelaskan langkah-langkah cara _resolve conflict_ di Git.

    > Salah satu cara yang langsung adalah mengedit file yang konflik atau kita juga bisa menggunakan tools yang bernama **`git mergetool`** yang memandu secara GUI dari konflik yang terjadi.

5.  Bagaimana cara membatalkan `commit` yang sudah terlanjut ter-_push_ ke repository?

    > menggunakan perintah **`git revert`** yang dimana akan membuat commit baru yang mengembalikan perubahan commit yang telah ditentukan dari hash sebelumnya

## Soal Command Git

Jelaskan fungsi-fungsi dari _list command_ Git berikut

1.  `git branch -d feature-login`

    > akan melakukan delete pada branch **`feature-login`**

2.  `git checkout -b feature-register`

    > membuat branch baru dan sekaligus melakukan checkout

3.  `git stash apply`

    > mengembalikan/menggunakan progress yang telah disimpan pada stash

4.  `git tag -a v1.0.1`

    > membuat tag yang tetanda **`v1.0.1`**

5.  `git diff HEAD introduction.html`

    > akan membandingkan versi file yang terakhir di commit pada **`HEAD`** dan file **`introduction.html`**

6.  `git pull --rebase`

    > perintah untuk menjalakan pull menggunakan **rebase** bukan merge

7.  `git commit -m "some changes" --no-verify`

    > melakukan commit dengan pesan **some changes** tanpa menjalankan pre-commit hooks

8.  `git remote add upstream https://github.com/hmdnprks/tefa-git-exercise.git`

    > untuk menambahkan remote ke upstream repository https://github.com/hmdnprks/tefa-git-exercise.git

9.  `git reset --hard`

    > membuang semua perubahan file working, index dan HEAD yang belum di commit

10. `git mv home.html Home.html`

    > melakukan pemindahan/rename pada file **`home.html`** menjadi **`Home.html`**
