[English](Lecture-Steps) · [Dansk](Lecture-Steps-da) · **Bahasa Melayu**

# Langkah kuliah

## 1. Pasang Git dan Git Bash

**Apa yang kami lakukan:** Memuat turun Git untuk Windows, menerima lesen, mengekalkan pilihan lalai (Git Bash ditanda) dan menetapkan Git Bash sebagai profil terminal lalai dalam VS Code. Pengguna Mac boleh langkau: Bash sudah dipasang.

![Pasang Git dan Git Bash](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/01-install-git.png)

**Apa yang kami peroleh:** Arahan `git` yang berfungsi dan shell gaya Unix pada Windows, supaya setiap arahan seterusnya dalam kursus berjalan sama pada semua sistem.

## 2. Apakah kawalan versi?

**Apa yang kami lakukan:** Kawalan versi menyimpan versi (titik simpan) fail anda. Jika kod rosak, anda membandingkan dengan versi terdahulu dan mengembalikannya. Git juga menyokong klon, fork, pull request dan gabungan (merge).

![Apakah kawalan versi?](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/02-version-control.png)

**Apa yang kami peroleh:** Memahami bahawa tiada apa yang hilang: setiap perubahan ialah langkah yang boleh dipulihkan, jadi bereksperimen lebih selamat.

## 3. Kawalan versi setempat

**Apa yang kami lakukan:** Dalam folder `Story` kami menjalankan `git init`, mencipta `chapter1.txt`, menyediakannya dengan `git add`, menyimpan dengan `git commit -m "Complete chapter 1"` (kala kini), melihat sejarah dengan `git log`, membandingkan dengan `git diff` dan memulihkan fail dengan `git checkout -- <fail>`.

![Kawalan versi setempat](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/03-local-git.png)
![Kawalan versi setempat](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/03b-diff-restore.png)

**Apa yang kami peroleh:** Perbezaan antara direktori kerja dan kawasan staging, cara membuat commit, membaca sejarah dan membatalkan suntingan yang tidak diingini.

## 4. GitHub dan repositori jauh

**Apa yang kami lakukan:** Mencipta akaun GitHub dan repositori kosong (awam atau peribadi), kemudian menyambung repositori setempat dengan `git remote add origin <url>` dan memuat naik dengan `git push -u origin main`. Tangkapan skrin ini menolak ke repositori bare setempat supaya berfungsi tanpa internet.

![GitHub dan repositori jauh](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/04-remote-push.png)

**Apa yang kami peroleh:** Salinan jauh sebagai sandaran dan untuk perkongsian, serta maksud `origin` dan cabang `main`.

## 5. Fail .gitignore

**Apa yang kami lakukan:** Mencipta `.gitignore` sebelum commit pertama dan menyenaraikan `secrets.txt`, `.DS_Store`, `*.pyc` dan `.venv/`. Git kemudian berhenti memaparkan fail itu dan tidak akan melakukan commit. Templat mengikut bahasa: github.com/github/gitignore.

![Fail .gitignore](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/05-gitignore.png)

**Apa yang kami peroleh:** Cara menyimpan kata laluan dan kunci API di luar repositori setempat dan awam, serta bahawa kad bebas dan komen `#` berfungsi dalam fail ini.

## 6. Cabang dan gabungan

**Apa yang kami lakukan:** Mencipta cabang `alien-plot` dengan `git branch`, bertukar dengan `git checkout`, melakukan commit di situ, kembali ke `main` dan menggabungkan kerja dengan `git merge alien-plot`. Latihan pilihan: learngitbranching.js.org.

![Cabang dan gabungan](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/06-branching.png)

**Apa yang kami peroleh:** Eksperimen dan ciri baharu boleh wujud berasingan daripada `main` yang kekal stabil, dan hanya digabungkan apabila berfungsi.

## 7. Fork dan pull request

**Apa yang kami lakukan:** Mengkaji empat kawasan (direktori kerja, kawasan staging, repositori setempat, repositori jauh). Fork ialah salinan anda sendiri bagi repositori orang lain; selepas mengubahnya anda membuka pull request meminta pemilik menggabungkannya. Hanya pemilik boleh menggabungkan.

![Fork dan pull request](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/08-four-areas.png)
![Fork dan pull request](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/07-fork-pull-request.png)

**Apa yang kami peroleh:** Cara kerjasama sumber terbuka berfungsi: mencadangkan perubahan tanpa menyentuh yang asal, menyemak kod satu sama lain dan menyumbang kepada projek.
