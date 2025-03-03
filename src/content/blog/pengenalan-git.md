---
author: Agung
pubDatetime: 2025-02-14T20:58:52.737Z
modDatetime: 2025-03-01T09:27:28.605Z
title: "Git Dasar: Setting up Git"
slug: pengenalan-git
featured: false
tags:
  - technoob
  - git
description: Ini catatanku tentang fundamental Git. Yang penting juga buat kamu yang ingin jadi programmer handal.
---
## Table of Contents

## Pengenalan Git
Secara official, Git diperkenalkan sebagai version control system. Bagi yang mulai--maupun terbiasa menggunakannya, ia seperti **epic save button**.

Menyimpan file melalui teks editor, merekam semua kata dalam dokumen sebagai satu file, termasuk segala perubahannya. Kita cukup hanya memiliki satu versi file, misalnya `skripsi.doc`, kecuali memang kita membutuhkan salinannya (yang tentu akan menyulitkan untuk diingat--mana yang paling update, di kemudian hari). Tentu dengannya kita tidak perlu lagi membuat banyak versi file seperti berikut: `skripsi.doc`, `skripsi_1.doc`, `skripsi_update.doc`, `skripsi_update_banget.doc`

Namun, ketika kita menyimpan file menggunakan Git, Git akan merekam perbedaan dalam file dan folder serta menyimpan riwayat setiap perubahannya. Fitur ini benar-benar sebuah *game changer*.

Sebagai pengembang individu, Git memungkinkan kita meninjau bagaimana proyek kita berkembang serta dengan mudah melihat atau mengembalikan keadaan file dari masa lalu. Setelah terhubung ke jaringan, Git memungkinkan Anda mengunggah proyek ke GitHub atau alternatif lain seperti Bitbucket, Beanstalk, atau GitLab untuk berbagi dan berkolaborasi dengan pengembang lain.

Saya sendiri lebih aktif menggunakan Github. Secara operasinal, prinsip penggunaan Git di berbagai platform mungkin sama ya. Jadi, silahkan pilih platform Git mana yang akan Anda gunakan.

>GitHub adalah layanan yang memungkinkan Anda mengunggah, menyimpan, dan mengelola kode menggunakan Git melalui antarmuka web yang intuitif.

Meskipun GitHub dan Git terdengar mirip, keduanya sebenarnya berbeda dan bahkan dikembangkan oleh perusahaan yang berbeda.

Git bekerja di komputer lokal kita, sedangkan GitHub adalah tempat penyimpanan berbasis web untuk semua proyek coding kita. Artinya, dengan mempelajari Git, Anda juga bisa memamerkan portofolio Anda di GitHub! Ini sangat penting karena hampir semua perusahaan pengembang perangkat lunak menganggap penggunaan Git sebagai keterampilan penting bagi pengembang program moder. Memiliki portofolio di GitHub akan menjadi bukti bagi calon pemberi kerja tentang kemampuan Anda.

## Install Git

### Pengguna Windows
Karena saya noob yang menggunakan windows, untuk instalasi Git, saya menggunakan installer Git yang bisa kita dapatkan melalaui [git-scm.com](https://git-scm.com/downloads).

### Pengguna Linux
Untuk pengguna linux, Anda juga bisa melakukan instalasi malalui command di terminal.

```
sudo add-apt-repository ppa:git-core/ppa
sudo apt update
sudo apt install git
```
Mungkin saja terdapat beberapa perbedaan command instalasi untuk beberapa distribusi Linux, serta bergantung pada package manager yang digunakan. Selengkapnya Anda bisa baca [petunjuknya di sini](https://git-scm.com/downloads/linux).

### Pengguna MacOS
Sementara untuk pengguna MacOS, Anda bisa gunakan langkah berikut.
```
$ brew install git
```
Setelah instalasi selesai, baik untuk pengguna Windos, Linux, maupun MacOS, untuk memastikan Git telah terinstal dengan benar pada sistem operasi yang kita gunakan, ketikkan command berikut pada terminal.
```
git --version
```
Command tersebut akan menghasilan version number untuk Git yang telah terinstal di komputer kita.

## Konfigurasi Git dan Github

### Buat Akun GitHub
Buka [GitHub.com](https://github.com/) dan buat akun! Saat proses pendaftaran, Anda akan diminta untuk memasukkan alamat email. Pastikan email yang Anda gunakan adalah email asli, karena akan digunakan secara default untuk mengidentifikasi kontribusi Anda.

Jika Anda peduli dengan privasi atau tidak ingin alamat email Anda tersedia untuk publik, silahkan menuju ke personal account settings, dan silahkan pelajari pengaturan privasi email yang tersedia.

### Konfigurasi Git
Agar Git dapat berfungsi dengan baik, kita perlu mengonfigurasinya sehingga Git dapat menghubungkan pengguna lokal (Anda) dengan GitHub. Saat bekerja dalam tim, ini memungkinkan anggota tim melihat siapa yang melakukan commit dan siapa yang menulis setiap baris kode.

Gunakan perintah berikut untuk mengatur Git. Pastikan Anda memasukkan informasi Anda sendiri di dalam tanda kutip (tetap sertakan tanda kutipnya!).

```
git config --global user.name "Your Name"
git config --global user.email "yourname@example.com"
```
Jika Anda menerapkan private email pada Github, command pada baris kedua disesuaikan dengan email Github (yang bisa dilihat melalui pengaturan personal account Github), sebagai berikut.

```
git config --global user.email "123456789+odin@users.noreply.github.com" # Remember to use your own private GitHub email here.
```
Untuk memastikan semuanya berfungsi dengan baik, masukkan perintah berikut dan periksa apakah outputnya sesuai dengan nama dan alamat email Anda.
```
git config --get user.name
git config --get user.email
```
Selanjutnya kita masuk pada pembuatan repositori dan command dasar git, di [posting selanjutnya](https://www.theodinproject.com/lessons/foundations-git-basics)

sumber belajar: [theodinproject.com](https://www.theodinproject.com/lessons/foundations-setting-up-git)