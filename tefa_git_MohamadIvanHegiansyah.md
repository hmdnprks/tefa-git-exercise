## Latihan Konsep Git
1. Jelaskan perbedaan antara command  `git pull`  dan  `git fetch`. <br> 
Command `git pull` dan `git fetch` memliki fungsinya sama, yaitu mengambil `commit` terbaru dari *remote repository.* Namun perbedaannya adalah `git pull` akan mengambil `commit` terbaru lalu otomatis menggabungkan (`merge`) dengan *branch* yang sedang aktif. **Sedangkan** `git fetch` akan mengambil `commit` nya saja. Command `git fetch` tidak akan langsung melakukan `merge`.

2. Jelaskan konsep  `rebase`  pada Git dan perbedaannya dengan  `merge`.<br> 
`git rebase` digunakan untuk menggeser `commit` *base*. Perbedaannya dengan `merge` adalah `git merge` akan menggabungkan dua *branch* dan menghasilkan satu `commit` baru. **Sedangkan** `git rebase` hanya mengambil commit dari *branch* lain dan **tidak akan** membuat `commit` baru.

3. Apakah itu  `git cherry-pick`  dan kapan sebaiknya kita menggunakan tersebut? <br> 
`git cherry-pick` adalah untuk melakukan `merge` by `commit` atau `merge`-nya tidak sepenuhnya terhadap semua commit yang ada di suatu *branch*. Jadi, `git cherry-pick` hanya melakukan `merge` by `commit` yang ingin kita `merge`-kan. 
`git cherry-pick` biasanya dilakukan ketika ingin melakukan merge suatu cabang ke master, namun masih ingin menyertakan perubahan dari suatu cabang tersebut. 

4. Jelaskan langkah-langkah cara  _resolve conflict_  di Git. <br> 
Langkah-langkah yang harus dilakukan untuk *resolve conflict* ketika melakukan suatu `merge` adalah dengan melihat baris kode yang mana yang menyebabkan penggabungannya menjadi *conflict* lalu ketika sudah ditemukan, maka kita dapat memilih untuk menggunakan kode yang berada pada *repository*, lokal, ataupun menggunakan kedua kode-kodenya. jika sudah aman maka kita bisa langsung melakukan *push* ke *repository*.

5. Bagaimana cara membatalkan  `commit`  yang sudah terlanjut ter-_push_  ke repository? <br> 
`git reset --hard <commit-id>`
`git clean -f -d`
`git fetch --all`
`git push -u origin +<branch-name>`


## Latihan Command Git
1. `git branch -d feature-login` <br> 
untuk menghapus *branch feature-login*.

2. `git checkout -b feature-register` <br> 
untuk membuat *branch feature-register* lalu langsung pindah ke *branch* tersebut.

3. `git stash apply` <br> 
untuk mengembalikan kode ke *working directory* dari *stash*.

4. `git tag -a v1.0.1` <br> 
Untuk menandai commit dengan label `v1.0.1` (*annontated tag*).

5. `git diff HEAD introduction.html` <br> 
Untuk membandingkan kode yang berada pada *working directory* di **introduction.html** dengan kode versi terakhir yang di-`commit` pada *repository*.

6. `git pull --rebase` <br> 
Untuk menerapkan kembali perubahan lokal diatas perubahan *repository*.

7. `git commit -m "some changes" --no-verify` <br> 
Untuk melakukan `commit` dengan melewati `pre-commit` *validations*.

8. `git remote add upstream https://github.com/hmdnprks/tefa-git-exercise.git` <br> 
Untuk terhubung ke *central repository* yaitu `hmdnprks/tefa-git-exercise.git`

9. `git reset --hard` <br> 
Untuk melakukan *revert* ke `commit` tertentu dengan paksa.

10. `git mv home.html Home.html` <br> 
Untuk melakukan *rename* dari `home.html` menjadi `Home.html`
