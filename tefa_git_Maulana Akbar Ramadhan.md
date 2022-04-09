## Soal Latihan Konsep Git
1.  Jelaskan perbedaan antara command  `git pull`  dan  `git fetch`.
	**Jawaban** :
	
	**Remote Repository**** --------->(git fetch) --------->**Local Repository** --------->(git merge) --------->**Workspace**
	**Remote Repository** --------->(git pull (git fetch + git merge)) --------->**Workspace**
	
	`git pull` merupakan perintah yang digunakan untuk men-*download* data dari sebuah *remote repository* dan secara langsung meng-*update* *workspace* yang tehubung dengan *remote repository*.  `git pull` melakukan `git fetch` dan `git merge` secara bersamaan untuk mengupdate *workspace* pada data *contributor* yang melakukan `git pull`.
	Sedangkan `git fetch` merupakan suatu perintah yang digunakan untuk men-*download* data dari *remote repository* ke *local repository* tanpa mengaplikasan *data fetch* pada *workspace* sehingga diperlukan `git merge` untuk mengaplikasikan pada *workspace*.
	
2.  Jelaskan konsep  `rebase`  pada Git dan perbedaannya dengan  `merge`.
	**Jawaban** :    
	 `rebase` merupakan proses pemindahan atau menggabungkan urutan `commit` pada `commit`base baru. Sebagai contoh terdapat suatu `branch` baru yang berisi beberapa `commit`pada `commit` terakhir `main` sehingga posisi `main` dan `branch` terhubung secara langsung (*direct path*) . Disisi lain, terdapat `commit`baru pada `main` sehingga `main` dan `branch` tidak terhubung secara langsung melainkan bercabang. Penggunaan `rebase` pada kasus ini adalah dengan cara memindahkan `branch` baru tersebut kedepan sehingga `main` dan `branch` baru dapat terhubung kembali (*direct path*). Sehingga setelah itu akan dilakukan `merge` agar `main` dan `branch` baru menjadi satu path pada *pointer* yang sama.

	Sedangkan `merge`, ketika terdapat `branch` baru yang berisi beberapa commit pada commit terakhir `main` sehingga posisi `branch` dan `main` terhubung secara langsung (*direct path*), maka untuk menggabungkan `branch` dan `main` membutuhkan `commit` baru (*Three way Merge*/*Merge Commit*) agar `commit` terakhir berada pada satu pointer yang sama.
	
		
3.  Apakah itu  `git cherry-pick`  dan kapan sebaiknya kita menggunakan command tersebut?
	**Jawaban** :
	`git cherry-pick` merupakan perintah untuk mengambil dan menerapkan suatu `commit` pada `branch` yang diinginkan. `git cherry-pick` dapat membatalkan perubahan yang tidak disengaja yang dibuat pada suatu `branch` pada git. Cara kerja dari `git cherry-pick` adalah ketika suatu `commit`  pada `branch` mengalami kesalahan, kemudian `commit`tersebut tidak ingin diterapkan, maka `git cherry-pick` akan mengambil `commit` sebelumnya untuk diimplementasikan sehingga membentuk cabang pada `commit` sebelumnya untuk diimpementasi. 

4.  Jelaskan langkah-langkah cara  _resolve conflict_  di Git.
	**Jawaban** 
	*Resolve git conflict*
	a. *Git fails to start the merge*
		*Conflict* ini terjadi karena terjadi penundaan *merge* terhadap *file* yang berada pada *local*. Sehingga status lokal perlu distabilkan menggunakan `git stash`, `git checkout`, `git commit`, atau `git reset`. *Error* pada *conflict* ini berupa : `error: Entry '<fileName>' not uptodate. Cannot merge. (Changes in working directory)`
	b. *Git fails during the merge*
	Jenis *conflict* ini terjadi karena suatu data yang sama diubah oleh dua orang atau lebih ketika diimplementasikan (*merge*). Hal ini juga dapat terjadi karena seseorang menghapus *file* dan di sisi lain seseorang sedang mengubah atau memodifikasi file tersebut. Git tidak bisa secara otomatis memilih perubahan terbaik terhadap *file conflict* yang sama. Ketika terjadi suatu *conflict*, git akan memberi tanda bahwa terdapat suatu *conflict* saat *file* akan di-*merge*. Permasalahan ini dapa diselesaikan dengan cara manual yaitu dengan memilih data yang ingin diterapkan. *Error* yang ditampilkan berupa : `error: Entry '<fileName>' would be overwritten by merge. Cannot merge. (Changes in staging area)`
		
5.  Bagaimana cara membatalkan  `commit`  yang sudah terlanjut ter-_push_  ke repository?
	**Jawaban** :
	Untuk membatalkan `commit` yang sudah ter-*push* pada repository menggunakan `git revert <hash/commit-id>`. Commit id merupakan kode unik pada suatu `commit` yang dilakukan. Dengan begitu `commit` dapat dibatalkan dari repository

## Soal Latihan Command Git

Jelaskan fungsi-fungsi dari  _list command_  Git berikut

1.  `git branch -d feature-login`
	=> Mendelete `branch` feature-login
2.  `git checkout -b feature-register`
	=> Membuat `branch`dengan nama feature-register sekaligus masuk ke dalam `branch` tersebut 
3.  `git stash apply`
	=> Menerapkan perubahan yang berada pada `stash`
4.  `git tag -a v1.0.1`
	=> Membuat anotasi tag versi
5.  `git diff HEAD introduction.html`
	=> Menampilkan semua perubahan pada file introduction.html
6.  `git pull --rebase`
	=> Menerapkan perubahan pada `local branch` sekaligus merubah *base*-nya sehingga sama dengan `remote branch`
7.  `git commit -m "some changes" --no-verify`
	=> Membuat commit dengan pesan "some changes" tanpa pre-commit dan commit-msg. Karena secara default pre-commit dan commit-msg hooks dijalakan
8.  `git remote add upstream https://github.com/hmdnprks/tefa-git-exercise.git`
	=> Menambahkan remot pada local repository dan tersinkron langsung dengan repository yang telah di fork
9.  `git reset --hard` 
	=> Mengatur ulang indeks dan working tree dengan membuang semua perubahan
10. `git mv home.html Home.html`
	=> Mengubah home.html menjadi Home.html
