
# Soal Latihan Konsep GIT

1. Jelaskan perbedaan antara command `git pull` dan `git fetch`.
	**Jawab**: `git fetch` merupakan command yang melakukan pengambilan meta-data terbaru dari remote repository ke local repository kita tanpa melakukan transfer file (seakan-akan seperti melakukan pengecekan apakah ada perbedaan antara remote repository dengan local repository). Sedangkan `git pull` melakukan apa yang dilakukan oleh `git fetch` dan membawa perubahan itu ke local repository dan melakukan `merge` dengan apa yang ada di local repository kita. Secara singkat, `git pull` adalah command yang melakukan `git fetch` dan kemudian melakukan `git merge`.

![Git Fetch Command {How to Use It + Examples}](https://phoenixnap.com/kb/wp-content/uploads/2021/12/git-pull-vs-git-fetch.png)

2. Jelaskan konsep `rebase` pada Git dan perbedaannya dengan `merge`
**Jawab**: Konsep dari `rebase` adalah memindahkan keseluruhan branch dan memindahkannya ke ujung branch lainnya dan menulis ulang *history project* dengan membuat commit baru untuk setiap commit dari branch originalnya.

![A forked commit history](https://wac-cdn.atlassian.com/dam/jcr:1523084b-d05a-4f5a-bd1a-01866ec09ca3/01%20A%20forked%20commit%20history.svg?cdnVersion=309)

Command ini akan sangat berguna apabila kita ingin menggabungkan antara branch main dengan branch feature tetapi posisi HEAD dari branch main lebih maju daripada branch feature sehingga tidak bisa dilakukan `merge fast forward` dan harus melakukan `three ways merge` dan hal itu kurang baik jika digunakan pada project sekala besar dengan tim yang besar juga karena akan sulit untuk melakukan *tracking*.

![Rebasing the feature branch onto master](https://wac-cdn.atlassian.com/dam/jcr:3bafddf5-fd55-4320-9310-3d28f4fca3af/03%20Rebasing%20the%20feature%20branch%20into%20main.svg?cdnVersion=309)

Sedangkan untuk `merge`, kita akan membuat sebuah `merge commit` baru yang mengikat kedua *history branch* dan akan terlihat seperti ini:

![Merging master into the feature branch](https://wac-cdn.atlassian.com/dam/jcr:4639eeb8-e417-434a-a3f8-a972277fc66a/02%20Merging%20main%20into%20the%20feature%20branh.svg?cdnVersion=309)

3. Apakah itu `git cherry-pick` dan kapan sebaiknya kita menggunakan command tersebut?
**Jawab**: `git cherry-pick` adalah sebuah command Git yang *powerful* sehingga memungkinkan untuk memillih commit berdasarkan *refference* dan menambahkannya ke ke HEAD yang berfungsi saat ini. Kita dapat menggunakan command ini pada saat melakukan hotfix pada sebuah bug yang mana harus cepat diselesaikan dengan cara membuat sebuah commit eksplisit untuk patching bug nya. Setelah itu, commit tersebut dapat kita `cherry-pick` ke branch main untuk memperbaiki bug sebelum berefek pada user lainnya.  

4. Jelaskan langkah-langkah cara *resolve conflict* di Git.
**Jawab**: Langkah-langkah untuk melakukan *resolve conflict* terutama bila kita melakukan `merge` di Git itu cukup sederhana. Pertama, hapus *designations* yang ditambahkan oleh Git. Kedua, perbaiki kode yang terjadi konflik (kita bisa memilih apakah akan menerima kode dari stream yang datang atau tetap pada kodingan sebelumnya). Ketiga, simpan file yang telah kita *resolve* tersebut. Terakhir, kita dapat menjalankan command `git add <filename>` kemudian `git commit -m "commit message"` lalu push dengan `git push origin <branch_name>`.

5. Bagaimana cara membatalkan `commit` yang sudah terlanjur ter-*push* ke repository?
**Jawab**: Untuk dapat membatalkan atau *undo*  `commit` yang sudah kita *push* ke repository memerlukan informasi hash dari `commit` yang ingin kita batalkan tersebut dengan cara mengeksekusi command `git log --oneline` kemudian eksekusi command `git revert <commit_hash>`. Tetapi, perlu diingat bahwa cara ini hanya akan membatalkan `commit` pada hash tertentu dan tidak akan membatalkan `commit` yang datang setelahnya. Untuk dapat melakukan hal tersebut kita dapat mengeksekusi command `git revert <oldest_commit_hash>..<latest_commit_hash>` yang mana akan membatalkan `commit` setelah `<oldest_commit_hash>` hingga `<latest_commit_hash>`.

  

# Soal Latihan Konsep Git

Jelaskan fungsi-fungsi dari *list command* Git berikut

  

1.  `git branch -d feature-login`: command ini digunakan untuk menghapus branch `feature-login` secara lokal hanya jika branch tersebut sudah kita push dan merge dengan remote branch. Jika kita ingin memaksakan untuk menghapus branch tersebut walau belum kita lakukan push dan merge ke remote, gunakan `git branch -D feature-login`.

2.  `git checkout -b feature-register`: command ini digunakan untuk memindahkan branch aktif kita ke branch `feature-register` dan akan secara otomatis membuat branch tersebut apabila belum terbuat. Command ini sebenarnya melakukan hal yang sama dengan `git branch feature-register` diikuti dengan `git checkout feature-register` namun hanya dalam satu line saja.

3.  `git stash apply`: command ini digunakan untuk mengembalikan commit yang sudah di `stash` ke direktori aktif saat ini.

4.  `git tag -a v1.0.1`: command ini digunakan untuk menandai sebuah commit dengan label `v1.0.1` atau bisa juga disebut sebagai *annotated tag*.

5.  `git diff HEAD introduction.html`: command ini digunakan untuk membandingkan kode **introduction.html** pada direktori aktif dengan kode **introduction.html** yang ada pada HEAD (posisi commit yang ditunjuk oleh HEAD).

6.  `git pull -rebase`: command ini digunakan untuk memaksa menggabungkan *unpublished changes* di lokal kita dengan kode pada commit terbaru yang ada di remote repository menggunakan konsep rebase (secara default git pull akan menggunakan metode merge). Untuk perbedaan konsep antara merge dan rebase dapat dilihat pada penjelasan jawaban soal latihan konsep Git poin 2.

7.  `git commit -m "some changes" --no-verify`: command ini digunakan untuk melakukan `commit` dengan pesan `"some changes"` tanpa menjalankan *git hooks* (biasanya digunakan apabila melakukan perubahan yang nantinya tidak diperbolehkan oleh *pre-commit hooks*).

8.  `git remote add upstream https://github.com/hmdnprks/tefa-git-exercise.git`: command ini digunakan untuk menghubungkan local repository kita ke *central repository*  `github.com/hmdnprks/tefa-git-exercise.git`.

9.  `git reset --hard`: command ini digunakan untuk melakukan `revert` ke `commit` tertentu secara paksa. Hal ini akan membuat *staging index* dan *working directory* ter-*reset* untuk menyamakan dengan `commit` tersebut.

10.  `git mv home.html Home.html`: command ini digunakan untuk melakukan perubahan nama file dari `home.html` menjadi `Home.html`.