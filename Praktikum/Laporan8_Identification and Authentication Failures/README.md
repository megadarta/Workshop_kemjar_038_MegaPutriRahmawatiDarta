**TUGAS                 KEAMANAN JARINGAN** 

**“A07: IDENTIFICATION AND AUTHENTICATION FAILURES”** 

![](image/Aspose.Words.53ce6031-c35c-4572-8398-38281ab90858.001.png)

Disusun Oleh kelompok A9 D4 LJ IT B : 

1. Mega Putri Rahmawati Darta (3122640038) 
1. Akhmad Mufti Ali Wafa (3122640048) 

**POLITEKNIK ELEKTRONIKA NEGERI SURABAYA TAHUN AJARAN 2022/2023** 

1. **PENDAHULUAN** 

Identifikasi  dan  autentikasi  membantu  framework  digital  sebagai  pertahanan  awal. Identifikasi  melibatkan  pengatribusian  identitas  untuk  setiap  pengguna  dalam menggunakan layanan aplikasi. Autentikasi mevalidasi sesi pengguna berdasar identitas yang  ditetapkan  dan  kredensial  akses.  Kegagalan  identifikasi  dan  autentikasi  terjadi ketika aplikasi gagal merupakan fungsi yang terkait dengan identitas pengguna, keaslian, dan  manajemen  sesi  dengan  benar.  Kegagalan  ini  sering  digunakan  penyerang  untuk mengambil identitas pengguna, oencurian data, atau kompromi seluruh sistem. 

2. **PERCOBAAN 1** 

Pada  percobaan  ini  akan  mereset  password  dari  akun  OWASP  Bjoern melalui  forgot password dengan menjawab petanyaan keamanan yang diberikan oleh sistem. 

1. Mencari akun dari user bjoern pada review  

![](image/Aspose.Words.53ce6031-c35c-4572-8398-38281ab90858.002.jpeg)

2. Menuju ke halaman login, lalu klik forgot password 

![](image/Aspose.Words.53ce6031-c35c-4572-8398-38281ab90858.003.jpeg)

Kemudian diminta untuk melengkapi form berikut :  

![](image/Aspose.Words.53ce6031-c35c-4572-8398-38281ab90858.004.jpeg)

3. Untuk  mengisi  pertanyaan  keamanan  yaitu  hewan  favorite  maka  bisa  mencoba mencari melalui internet :  

![](image/Aspose.Words.53ce6031-c35c-4572-8398-38281ab90858.005.jpeg)

4. Melanjutkan pengisian form, disini saya mengisikan password : bjoern123 

![](image/Aspose.Words.53ce6031-c35c-4572-8398-38281ab90858.006.jpeg)

5. Lalu klik “Change” , dan akan tampil berikut ini :  

![](image/Aspose.Words.53ce6031-c35c-4572-8398-38281ab90858.007.jpeg)

6. Mencoba login dengan password baru  

![](image/Aspose.Words.53ce6031-c35c-4572-8398-38281ab90858.008.jpeg)

![](image/Aspose.Words.53ce6031-c35c-4572-8398-38281ab90858.009.jpeg)

Berhasil login dengan password baru milik akun[ bjoern@owasp.org ](mailto:bjoern@owasp.org)

3. **PERCOBAAN 2** 

Percobaan kedua adalah login dengan user dari administrator tanpa mengubah password saat ini atau menerapkan SQL Injection 

1. Ketik perintah berikut :**  

sqlmap  -u  “http://localhost:3000/rest/user/login”  -- data=“email=test@test.com&password=test”  --level=5  --risk=3  --banner  --  ignore- code=401 --dbms='sqlite' --technique=b 

![](image/Aspose.Words.53ce6031-c35c-4572-8398-38281ab90858.010.jpeg)

Hasil perintah diatas kode 401, yang berarti autentikasi gagal. 

2. Mengganti perintah dengan menggunakan email admin, sebagai berikut :  

![](image/Aspose.Words.53ce6031-c35c-4572-8398-38281ab90858.011.jpeg)

Hasil dari perintah diatas tetap 401 – unauthorize 

3. Mencoba kembali dengan menggunakan password admin123 

![](image/Aspose.Words.53ce6031-c35c-4572-8398-38281ab90858.012.jpeg)

Jika kembali ke juice shop, maka akan muncul pop up berikut yang berarti sukses menjalankan misi. 

![](image/Aspose.Words.53ce6031-c35c-4572-8398-38281ab90858.013.jpeg)
