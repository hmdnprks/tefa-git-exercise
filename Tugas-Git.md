## Soal Latihan Konsep Git
1.  Jelaskan perbedaan antara command  `git pull`  dan  `git fetch`.
***`git pull` dan  `git fetch` sama-sama mengambil commit terbaru, namun `git pull` secara otomatis melakukan merge dengan branch yang sedang aktif sedangkan `git fetch` tidak secara otomatis melakukanya.***
2.  Jelaskan konsep  `rebase`  pada Git dan perbedaannya dengan  `merge`.
**_`rebase` dipakai untuk memodifikasi riwayat commit yang sudah ada. Walaupun memberikan hasil yang sama, keduanya memiliki efek samping yang berbeda. Operasi `merge` akan menghasilkan commit baru sementara `rebase` tidak._**	
3.  Apakah itu  `git cherry-pick`  dan kapan sebaiknya kita menggunakan command tersebut?
	***`git cherry-pick` adalah alat sederhana namun kuat yang mentransfer commit secara selektif dari satu cabang ke cabang lainnya. `git cherry-pick`  dapat menggunakannya jika tidak ingin menggabungkan seluruh cabang menjadi master, tetapi masih ingin menyertakan perubahan dari cabang fitur.***
4.  Jelaskan langkah-langkah cara  _resolve conflict_  di Git.
	***_resolve conflict_ dapat dilakukan dengan `merge conflict`. Sama seperti pada `merge fast-forward`, perbedaannya adalah pada screen merge, kita harus melakukan proses resolve.***
5.  Bagaimana cara membatalkan  `commit`  yang sudah terlanjur ter-_push_  ke repository?
	***Membatalkan commit dapat dilakukan dengan perintah `reset --hard`***

## Soal Latihan Command Git
Jelaskan fungsi-fungsi dari _list command_ Git berikut

1.  `git branch -d feature-login`
	***menghapus branch bernama feature-login***
2.  `git checkout -b feature-register`
	***membuat branch baru bernama feature-register***
3.  `git stash apply`
	***menerapkan perubahan yang telah disimpan di git stash***
4.  `git tag -a v1.0.1`
	***membuat annotated tag dengan nama v1.0.1***
5.  `git diff HEAD introduction.html`
	***membandingkan file version pada repository aktif dengan***
6.  `git pull --rebase`
	***git pull dengan fungsi rebase, artinya perubahan lokal di-reapply diatas perubahan remote***
7.  `git commit -m "some changes" --no-verify`
	***melakukan commit dengan pesan dan menjalankan commit tanpa melalui pre-commit hook***
8.  `git remote add upstream https://github.com/hmdnprks/tefa-git-exercise.git`
	***menambahkan upstream pada repo***
9.  `git reset --hard`  
	***mereset file indeks (atau staging area) dan direktori kerja.***
10. `git mv home.html Home.html`
	***rename file***
