# Soal Latihan Command Git

 1. `git pull` digunakan untuk menggabungkan semua perubahan yang ada di remote repository ke directory lokal sementara `git fetch` digunakan untuk menampilkan semua object dari remote repository yang tidak berada di direktori lokal.
 2. `Rebase` adalah menulis kembali commit diatas branch lainnya, git akan menghapus commit dari satu cabang dan menambahkannya ke cabang lain. Ketika menggunakan `rebase` awal brach yang dipindahkan akan melanjutkan brach utama (master) sementara `merge` akan menggabungkan akhir dari brach ke branch utama.
 3. `git cherry-pick` adalah command yang digunakan untuk menerapkan perubahan yang diperkenalkan oleh beberapa commit yang sudah ada. Beberapa skenario penggunaan `git cherry-pick` adalah saat kolaborasi tim, bug hotfixes, membatalkan perubahan dan mengembalikan commit yang hilang.
 4. - Melakukan perubahan pada file tesebut sehingga tidak terjadi conflict
	 - Setelah mengedit file, kita dapat menggunakan perintah `git add` untuk menampilkan konten baru yang digabungkan
	 - Langkah terakhir adalah membuat komit baru dengan bantuan perintah git commit
	 - Git akan membuat merge commit baru untuk menyelesaikan penggabungan.
 6. Jalankan command `git reset --hard <commit-id>` , setelah itu lanjutkan dengan perintah `git clean -f -d` , kemudian cek status repository menggunakan command `git status` 

# Soal Latihan Command Git
1. `git branch -d feature-login` : menghapus branch dengan nama feature-login.
2. `git checkout -b feature-register` : membuat branch dengan nama feature-register.
3. `git stash apply` : menerapkan perubahan yang sudah disimpan dalam stash tanpa menghapus perubahan tersebut dari stash.
4. `git tag -a v1.0.1` : membuat annotated tag dengan nama v1.0.1
5. `git diff HEAD introduction.html` : menampilkan perbedaan commit terakhir pada file introduction.html dengan commit-commit yang sudah dilakukan sebelumnya.
6. `git pull --rebase` : melakukan rebase branch saat ini diatas brach upstream setelah melakukan fetching.
7. `git commit -m "some changes" --no-verify` : melakukan bypass commit dengan pesan some changes
8. `git remote add upstream https://github.com/hmdnprks/tefa-git-exercise.git` : mengatur repository `https://github.com/hmdnprks/tefa-git-exercise.git` sebagai remote repository dan upstream branch.
9. `git reset --hard` : mengatur ulang indeks pada working tree, setiap perubahan yang sebelumnya tertunda pada staging area dan working directory akan hilang.
10. `git mv home.html Home.html` : melakukan rename home.html menjadi Home.html

