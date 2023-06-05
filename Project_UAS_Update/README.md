**TUGAS                     KEAMANAN JARINGAN    “KERENTANAN PADA VDI”** 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.001.png)

Nama : Mega Putri Rahmawati Darta 

Kelas : D4 LJ IT B 

NRP  : 3122640038 

**POLITEKNIK ELEKTRONIKA NEGERI SURABAYA TAHUN AJARAN 2022/2023** 

**1.  MENGAMBIL DATA DATABASE MENGGUNAKAN SQLMAP** 

Berikut merupakan langkah langkah dari pengambilan database menggunakan sqlmap pada kali linux :  

1. Melakukan cek ip kali linux dengan menggunakan perintah “ifconfig” 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.002.jpeg)

2. Mengecek ssh yang open dan berada pada satu network dengan kali linux, dengan menggunakan perintah nmap sebagai berikut :  

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.003.png)

3. Selain  menjalankan  kali  linux,  disini  juga  harus  dijalankan  ubuntu  “Skenario Serangan” 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.004.jpeg)

4. Kemudian  mencoba  kembali  untuk  melihat  ssh  yang  open  dengan  menggunakan perintah step ke 2 diatas.  

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.005.png)

Dari gambar diatas didapatkan bahwa ssh dari ubuntu yaitu 192.168.9.148 

5. Mencoba menjalankan ip tersebut pada browser dengan menambahkan /index.php. Maka akan tampil web berikut ini :  

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.006.jpeg)

Jika dilihat script dari web tersebut maka didapatkan koneksi database nya, seperti gambar dibawah ini :

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.007.jpeg)

Jika menuju ke 192.168.9.148/lib/koneksi.php, dapat dilihat username, password, dan database yang digunakan seperti berikut :  

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.008.jpeg)

Selain informasi koneksi database, didapatkan juga halaman lainnya seperti menu, konten, sidebar 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.009.jpeg)

6. Disini  mencoba  untuk  masuk  ke  halaman  konten  “192.168.9.148/konten.php”  :

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.010.jpeg)

Setelah mengunjungi halaman konten.php, dan jika dilihat pada scriptnya terdapat perintah sql sebagai berikut :  

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.011.jpeg)

Dengan mendapatkan url memanggil database tersebut, dapat digunakan pada sqlmap. 

7. Menjalankan sqlmap dengan perintah berikut ini :  

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.012.png)

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.013.png)

Dari  informasi  yang  didapatkan  pada  sqlmap  sudah  sama  dengan  informasi  yang didapatkan dari /lib/koneksi.php 

8. Selanjutnya mengecek tabel apa saja yang ada di dalam database 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.014.jpeg)

Hasil akhir dari perintah tersebut adalah sebagai berikut :  

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.015.png)

Dari informasi diatas didapatkan terdapat 7 tabel dalam database.  

9. Mendapatkan data yang ada didalam tabel :  
1. Tabel User, dengan perintah sebagai berikut :  
- Mencari tahu kolom dari tabel user 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.016.png)

- Hasil dari kolom tabel user  

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.017.png)

- Melihat data user 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.018.png)

- Hasil data user  

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.019.png)

2. Tabel Artikel 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.020.jpeg)

- Mencari tahu kolom dari tabel artikel 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.021.png)

- Hasil dari kolom tabel artikel 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.022.jpeg)

- Melihat data artikel 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.023.jpeg)

- Hasil data artikel 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.024.jpeg)

3. Tabel Galeri  

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.025.jpeg)

- Mencari tahu kolom dari tabel galeri 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.026.png)

- Hasil dari kolom tabel galeri 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.027.png)

- Melihat data galeri 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.028.jpeg)

- Hasil data galeri 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.029.png)

4. Tabel Halaman 
- Mencari tahu kolom dari tabel halaman 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.030.png)

- Hasil dari kolom tabel halaman 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.031.png)

- Melihat data halaman 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.032.jpeg)

- Hasil data halaman 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.033.jpeg)

5. Tabel Komentar 
- Mencari tahu kolom dari tabel komentar 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.034.jpeg)

- Hasil dari kolom tabel komentar 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.035.png)

- Melihat data komentar 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.036.jpeg)

- Hasil data komentar 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.037.png)

6. Tabel Menu 
- Mencari tahu kolom dari tabel menu 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.038.jpeg)

- Hasil dari kolom tabel menu 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.039.png)

- Melihat data menu 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.040.png)

- Hasil data menu 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.041.png)

7. Tabel Pesan 
- Mencari tahu kolom dari tabel pesan 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.042.jpeg)

- Hasil dari kolom tabel pesan 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.043.png)

- Melihat data pesan 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.044.jpeg)

- Hasil data pesan 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.045.png)

Hasil  :  Dari  proses  ini  dapat  disimpulkan  bahwa  telah  berhasil  mengambil  data  dari database dengan menggunakan sqlmap.  

**2.  MENCARI TAU PASSWORD ROOT MENGGUNAKAN HYDRA** 

Langkah yang saya lakukan sebagai berikut :  

- Mencari list username dan password yang nantinya akan dicek kombinasinya dengan hydra: 

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.046.jpeg)

- Menjalankan perintah hydra sebagai berikut :  

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.047.png)

![](image/Aspose.Words.50dc1750-5d41-4751-8a15-605d84afd545.048.png)

- Hasil :  

Belum didapatkan password dan username yang cocok. 
