# **SOAL SHIFT SISOP 20 MODUL 4**

**Soal Nomor 1**
Variabel dirpath digunakan untuk mendefinisikan direktori yang akan di mount.

Variabel cs digunakan untuk deklarasi karakter caesar chipper.

Fungsi enc1 menerima 2 parameter: path digunakan untuk path file dan key untuk key caesar cipher. Variabel length digunakan untuk menyimpan panjang string pathfile. Pada loop pertama. Pathfile akan dicek dari karakter paling belakang. Pengecekan ini ada 2: yang pertama mengecek apakah karakter merupakan tanda slash "/" di pathfile, jika iya, loop akan langsung berhenti untuk kemudian pindah ke loop selanjutnya. Pengecekan pertama ini digunakan untuk mencari dimulainya enkripsi. Pengecekan yang ke dua mengecek apakah karakter merupakan tanda ".", jika iya maka karakter tersebut merupakan awal dari ekstensi file yang nantinya tidak ikut dienkripsi. Pada loop kedua, jika karakter path ke - i adalah slash , maka enkripsi akan dimulai pada karakter tersebut. Pada loop selanjutnya, jika pada pathfile terdapat karakter slash, maka karakter akan diabaikan.

Fungsi dec1 mirip dengan fungsi enc1, bedanya karakter-karakternya akan diganti dengan indeks key.

Fungsi getattr untuk mengambil pathfile direktori yang akan dimount. Variabel path akan berisi pathfile dari direktori. Pathfile selanjutnya dicopy ke array temp. Setelah itu, isi dari path akan dibandingkan dengan /encv1, jika sama, folder tersebut isinya akan di enkrip.

Fungsi readdir, fungsi ini akan mendapatkan path file, lalu pathfile akan dicopy ke variabel temp. Selanjutnya dilakukan pengecekan apakah path nya = "/encv1_" jika iya, maka akan dilakukan enkripsi versi 1 dengan memanggil fungsi enc1(tmp,10).

Struct fuse_operations xmp_oper berisi fungsi2 yang akan diimplementasiin ke fuse.

Fungsi main memanggil fungsi fuse main untuk pembuatan fuse.


**Soal Nomor 4**
Logpath untuk menyimpan path file fs.log

Fungsi writelog akan dipanggil di dalam semua fungsi fuse (kecuali getattr dan readdir). Fungsi writelog mempunyai 2 parameter. Yang prtama level, berisi string level log yang gunanya untuk warning atau info, yang kedua cmd_desc yang gunanya sebagai syscall dan path file. Variabel fp berisi fungsi fopen. Fungsi fopen ini menerima 2 parameter. Parameter pertama, logpath, berisi path file dari sf.log. Parameter kedua berisi option file "a+" yang ditujukan ke parameter pertama. Pada tahap ini file akan dibuka untuk melakukan reading dan penambahan isi ke dalam file . Jika file belum ada, maka file akan dibuat otomatis.
