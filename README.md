# TugasADJ-191402102

Sebelum menjelaskan langkah-langkah menjalankan sebuah web menggunakan docker, pastikan docker telah terinstal di pc kita. Kita dapat mendownload docker di situs resmi docker bersamaan dengan langkah-langkah untuk melakukan instalasi.
https://docs.docker.com/desktop/windows/install/

Setelah melakukan instalasi pastikan docker telah terhubung di pc kita. Perhatikan logo docker pada sudut kiri bawah. Jika logo tersebut sudah berwarna hijau, berarti docker sudah terhubung dengan pc kita. Logo docker akan berwarna merah jika docker tidak terhubung dengan pc kita.

![1](https://user-images.githubusercontent.com/66837982/132792851-0347ba37-707a-4f68-ba87-45b8c2c493a1.png)

Berikut adalah langkah-langkah untuk menjalankan web dengan menggunakan docker :

Pastikan telah melakukan pull nginx dengan menggunakan command berikut :
docker pull nginx

Buatlah folder site-content yang berisi Dockerfile, index.html beserta file-file lain.

![2](https://user-images.githubusercontent.com/66837982/132793179-bd60c783-cecf-4479-87e6-1f7e9d762f11.png)

File Dockerfile berisi perintah seperti berikut ini:

![3](https://user-images.githubusercontent.com/66837982/132793267-c302a8e4-0f0b-4e38-90fe-4deb6e35cab8.png)

Baris pertama mendefinisikan image nginx yang gunakan.
Baris kedua menyalin keseluruhan file yang terdapat di folder site-content ke dalam direktori yang dituju.
Baris ketiga menghubungkan kita dengan repositori yang akan kita gunakan pada akun github nanti.

Command build berfungsi untuk membuat sebuah image baru bernama tugas-adj dengan tag f1. Parameter -t memungkinkan kita untuk membuat nama sesuai keinginan kita.

![4](https://user-images.githubusercontent.com/66837982/132793370-a88743f6-ea73-41b3-9e10-0e6a89d518ad.png)

Command ini akan menampilkan semua image yang ada pada docker kita. Dapat dilihat bahwa image tugas-adj dengan tag f1 sudah ada di dalam daftar image.

![5](https://user-images.githubusercontent.com/66837982/132793466-be7211df-4d90-4a62-a034-7966047e0eb1.png)

Command ini berfungsi untuk menjalankan container dengan menggunakan image yang baru kita buat. Parameter -p menunjukkan port yang akan kita gunakan.

![6](https://user-images.githubusercontent.com/66837982/132793574-5a7e43d4-f0c1-42a8-b02b-878186a34e0d.png)

Buka localhost:8080 untuk melihat hasil atau tampilannya. Jika sudah menampilkan hasil yang sesuai, maka kita telah berhasil membuat web dengan docker.

![7](https://user-images.githubusercontent.com/66837982/132793624-40e10178-0b3c-4d11-9c61-4bb14cf354da.png)

Buat repositori baru pada akun github.

![8](https://user-images.githubusercontent.com/66837982/132793696-3c95be94-757d-43bd-aec8-bbd818535ef7.png)

Buat token pada akun github. Token ini akan digunakan sebagai password untuk menghubungkan docker dengan akun github. Beri tanda centang untuk write:packages, read:packages, dan delete:packages.

![9](https://user-images.githubusercontent.com/66837982/132793743-b2c90441-0a31-4fae-ae03-b03b7de59e05.png)

Login akun github pada docker.

![10](https://user-images.githubusercontent.com/66837982/132793790-922f09ac-878b-4c83-a8a6-37e208d1ced6.png)

Kemudian salin id dari image yang akan diunggah ke github diikutin dengan akun github dan juga nama image.

![11](https://user-images.githubusercontent.com/66837982/132793850-dc2ac67f-6ab3-4955-867b-09e9d227f81c.png)

Jika image seperti gambar di bawah telah tersedia, ini berarti duplikat image telah berhasil dibuat.

![12](https://user-images.githubusercontent.com/66837982/132793900-dc11063e-0ef7-4e84-a478-1054ae38ff2c.png)

Unggah image dengan menggunakan command push seperti gambar berikut :

![13](https://user-images.githubusercontent.com/66837982/132793961-b555fc9f-2d31-43f5-b361-479bd5ff53ea.png)

Image telah berhasil diunggah pada akun github.

![14](https://user-images.githubusercontent.com/66837982/132794030-f0352abe-1b1e-46e9-87e5-e94ca0b48086.png)

Kemudian ubah visibility package menjadi public.

![15](https://user-images.githubusercontent.com/66837982/132794075-899b1800-10e5-40ab-8670-e96aed1a972a.png)

Berikut tangkapan layar dari repositori pada akun github yang sedang digunakan :

![16](https://user-images.githubusercontent.com/66837982/132794158-5b94cddf-026b-406e-867e-2055faea72ef.png)
