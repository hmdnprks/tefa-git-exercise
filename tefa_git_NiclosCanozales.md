Soal Latihan Konsep Git

1. git pull  : mengambil commit terbaru dari remote repository + digabung dengan branch yang aktif (merge).
   git fetch : mengambil commit terbaru dari remote repository.

2. merge  : menggabungkan dua atau lebih branch menghasilkan satu commit baru.
   rebase : mengambil commit dari branch lain dan menambahkannya pada branch.

3. git cherry-pick berguna untuk mengaplikasikan commit dari suatu branch ke branch yang lainnya.
   git cherry-pick dapat digunakan ketika kita commit ke branch yang salah sehingga kita hanya perlu
   melakukan cherry-pick ke branch yang benar.

4. Langkah-langkah Resolve Conflicts pada Git
	1. Mengidentifikasi Files mana yang Conflicts.
	2. Buka setiap Files tersebut dan periksa diffs untuk mengetahui versi block yang perlu diubah
	3. Setelah suatu konflik diselesaikan lakukan git add [files]
	4. Ketika sudah menyelesaikan seluruh konflik lakukan git rebase --continue

5. Kita dapat melakukannya dengan perintah git revert <commit_hash>

Soal Latihan Command Git

1. Menghapus branch feature-login
2. Membuat branch feature-login dan pindah ke branch tersebut
3. Menyimpan current directory dan pindah ke latest commit.
   Simpanan tersebut berada pada stash list yang dapat diakses kembali nantinya.
4. Membuat annotated tag pada series 1.0.1
5. Membandingkan versi/perubahan antara latest commit dengan introduction.html
6. git pull berarti git fetch + merge
   --rebase mengubah merge menjadi rebase
7. Melakukan commit dengan memberi pesan "some changes" dan mengabaikan pesan commit sebelumnya.
8. Mensinkronisasi Local Repository dengan Remote/Central Repository
9. Melakukan reset files pada index atau staging area namun seluruh untracked files akan dihapus.
10. Rename dan memindahkan files dari home.html menjadi Home.html
