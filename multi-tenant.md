# Penjelasan
Dalam sebuah aplikasi bisa ada sebuah entitas yang memiliki shared table. Semisal terdapat sebuah company dimana tiap company menggunakan tabel `product` yang dibedakan dengan `company_id`.

Dalam kasus tersebut terdapat beberapa strategi pendekatan yang dapat dilakukan:
- shared table
    Sama seperti solusi penjelasan diatas, memiliki kekurangan dimana semua data terkumpul pada satu table sehingga membuat operasi ke table tersebut lemot. Tetapi sangat simple dalam proses development dan cocok untuk skala kecil.
- multi-schema
    Masing-masing company memiliki schema untuk menyimpan tabel2 nya sendiri. Dapat mengatasi masalah pada shared table, tetapi proses development lebih kompleks
- multi-database
    Masing-masing company memiliki database instance yang harus diinstall pada server.

