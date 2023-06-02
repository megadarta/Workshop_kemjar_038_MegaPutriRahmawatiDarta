**TUGAS                     KEAMANAN JARINGAN    “KERENTANAN PADA VDI”** 

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.001.png)

Nama : Mega Putri Rahmawati Darta 

Kelas : D4 LJ IT B 

NRP  : 3122640038 

**POLITEKNIK ELEKTRONIKA NEGERI SURABAYA TAHUN AJARAN 2022/2023** 

**1.  MENGAMBIL DATA DATABASE MENGGUNAKAN SQLMAP** 

Berikut merupakan langkah langkah dari pengambilan database menggunakan sqlmap pada kali linux :  

1. Melakukan cek ip kali linux dengan menggunakan perintah “ifconfig” 

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.002.jpeg)

2. Mengecek ssh yang open dan berada pada satu network dengan kali linux, dengan menggunakan perintah nmap sebagai berikut :  

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.003.png)

3. Selain  menjalankan  kali  linux,  disini  juga  harus  dijalankan  ubuntu  “Skenario Serangan” 

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.004.jpeg)

4. Kemudian  mencoba  kembali  untuk  melihat  ssh  yang  open  dengan  menggunakan perintah step ke 2 diatas.  

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.005.png)

Dari gambar diatas didapatkan bahwa ssh dari ubuntu yaitu 192.168.9.148 

5. Mencoba menjalankan ip tersebut pada browser dengan menambahkan /index.php. Maka akan tampil web berikut ini :  

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.006.jpeg)

Jika dilihat script dari web tersebut maka didapatkan koneksi database nya, seperti gambar dibawah ini :

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.007.jpeg)

Jika menuju ke 192.168.9.148/lib/koneksi.php, dapat dilihat username, password, dan database yang digunakan seperti berikut :  

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.008.jpeg)

Selain informasi koneksi database, didapatkan juga halaman lainnya seperti menu, konten, sidebar 

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.009.jpeg)

6. Disini  mencoba  untuk  masuk  ke  halaman  konten  “192.168.9.148/konten.php”  :

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.010.jpeg)

Setelah mengunjungi halaman konten.php, dan jika dilihat pada scriptnya terdapat perintah sql sebagai berikut :  

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.011.jpeg)

Dengan mendapatkan url memanggil database tersebut, dapat digunakan pada sqlmap. 

7. Menjalankan sqlmap dengan perintah berikut ini :  

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.012.png)

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.013.png)

Dari  informasi  yang  didapatkan  pada  sqlmap  sudah  sama  dengan  informasi  yang didapatkan dari /lib/koneksi.php 

8. Selanjutnya mengecek tabel apa saja yang ada di dalam database 

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.014.jpeg)

Hasil akhir dari perintah tersebut adalah sebagai berikut :  

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.015.png)

Dari informasi diatas didapatkan terdapat 7 tabel dalam database.  

9. Melihat tabel User dengan perintah dibawah ini :  

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.016.png)

Hasil akhir dari perintah tersebut adalah sebagai berikut :  

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.017.png)

10. Mendapatkan data yang ada didalam tabel User, dengan perintah sebagai berikut :  

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.018.png)

Hasil akhir dari perintah tersebut adalah :  

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.019.png)

11. Dari proses ini dapat disimpulkan bahwa telah berhasil mengambil data dari database dengan menggunakan sqlmap.  

**2.  MENCARI TAU PASSWORD ROOT MENGGUNAKAN HYDRA** 

Langkah yang saya lakukan sebagai berikut :  

- Mencari list username dan password yang nantinya akan dicek kombinasinya dengan hydra: 

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.020.jpeg)

- Menjalankan perintah hydra sebagai berikut :  

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.021.png)

![](image/Aspose.Words.d245c1b2-d808-4fb7-b8cd-b48e12a7390c.022.png)

- Hasil :  

Belum didapatkan password dan username yang cocok. 
