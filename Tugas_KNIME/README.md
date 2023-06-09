**TUGAS                 KEAMANAN JARINGAN “DATA MINING”** 

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.001.png)

Nama : Mega Putri Rahmawati Darta 

Kelas : D4 LJ IT B 

NRP  : 3122640038 

**POLITEKNIK ELEKTRONIKA NEGERI SURABAYA TAHUN AJARAN 2022/2023** 

1. Installasi Wireshark  

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.002.jpeg)

2. ‘Installasi Knime 

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.003.jpeg)

3. Untuk mempermudah pada saat proses analisa yang akan dilakukan nantinya, kita akan mengambil data dengan ip versi 4 (ipv4) dan protocol TCP, DNS saja. Untuk proses tersebut dapat dilakukan pada wireshark menggunakan perintah ip.version==4 && tcp || dns pada kolom display filter tepat dibawah toolbar 

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.004.jpeg)

4. Menambahkan kolom baru  

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.005.jpeg)

5. Hasil penambahan kolom  

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.006.jpeg)

6. Langkah terakhir yaitu export file pcap tersebut keformat Comma-separated Value (.csv) dengan cara klik File – Export Packet Dissections – As CSV. Yang perlu diperhatikan yaitu pada Pacet Range, pastikan yang terpilih yaitu Displayed, karena data pada Displayed ini sudah terfilter denga nip version 4. 

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.007.jpeg)

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.008.jpeg)

\*saya hanya menggunakan 1 file 

7. Buka software knime untuk melakukan proses analisa pada traffic DNS. Berikut adalah file yang telah. Terdapat bagian-bagian penting sebagai berikut :  
   1. Yang pertama yaitu Knime Explorer yang isinya adalah project project yang kita buat pada software ini 
   1. Terdapat Node Repository, bagian ini merupakan bagian yang sangat penting, karena berisi seluruh fungsi tools dari software ini yang dinamakan dengan Node. 
   1. Knime Workflow, bagian ini adalah bagian visual pada Knime, seluruh fungsi yang digunakan akan ditampilkan pada bagian ini. Berikut adalah contoh tampilan pada Knime Workflow 
7. Setelah  mengenal  semua  bagian  dari  Knime.  Setelah  itu  kita  akan  membuat workflow/project baru. Dengan cara klik File – New – New Knime Workflow – Tulis Nama workflow dan Lokasi workflow tersebut – Klik Finish 

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.009.jpeg)

9. Selanjutnya yaitu menggabungkan seluruh data tadi menjadi 1 data. Node yang dibutuhkan untuk proses ini yaitu :  
1. File Reader : untuk membaca data  
1. Concatenate : untuk menggabungkan data 
- Membuat file reader dan menginputkan file yang digunakan 

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.010.jpeg)

- Berikut tampilannya (disini saya hanya menggunakan 1 file dataset saja) 

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.011.jpeg)

- Menjalankan concatenate, dengan cara klik kanan pada note → execute. Bila berhasil dijalankan status node akan berubah menjadi hijau. 

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.012.jpeg)

- Menambahkan tabel baru  

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.013.jpeg)

- Menambahkan dan setting joiner 

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.014.jpeg)

- Excecute joiner 

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.015.jpeg)

- Menampilkan tabel hasil joiner, terdapat label yang masih berisi “?” 

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.016.jpeg)

10. Menggunakan missing value untuk mengisi data kosong  

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.017.jpeg)

11. Menggunakan value counter untuk melihat jumlah  

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.018.jpeg)

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.019.png)

12. Export file ke dalam .csv 

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.020.jpeg)

13. Proses cleaning 
- Membuat dan memasukkan data dalam file reader 

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.021.png)

- Konfigurasi Filter  

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.022.jpeg)

- Konfigurasi missing value  

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.023.jpeg)

- Excecute data 

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.024.png)

14. Data Transformation  
- Menambahkan normalizer 

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.025.png)

- Konfigurasi normalizer 

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.026.jpeg)

- Excecute normalizer 

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.027.png)

15. Data Mining  
- Menambahkan proses seperti ini  

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.028.png)

- Konfigurasi x-partitioner 

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.029.jpeg)

- Konfigurasi decision tree 

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.030.jpeg)

- Konfigurasi decision tree predictor 

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.031.jpeg)

- X-aggregator tanpa konfigurasi, dan berikut hasilnya :  

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.032.png)

16. Evaluation  
- Menambahkan score dengan konfigurasi berikut :  

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.033.jpeg)

- Melihat akurasi**  

![](image/Aspose.Words.0b62c9d7-8e30-4dd6-8594-407bddd0d425.034.png)
