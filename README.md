# SIG_TEORI_TGS2
 TUGAS PETA 2
1. Temukan file ne_10m_populated_places_simple.zip di Browser QGIS dan perluas. Pilih file ne_10m_populated_places_simple.shp dan seret ke kanvas.

2. Lapisan baru ne_10m_populated_places_simple sekarang akan dimuat di QGIS dan Anda akan melihat banyak titik yang mewakili tempat-tempat berpenduduk di dunia. Tampilan default di kanvas QGIS menunjukkan geometri lapisan GIS. Setiap titik juga memiliki atribut terkait. Mari kita lihat mereka. Temukan Bilah Alat Atribut. Toolbar ini berisi banyak alat yang berguna untuk memeriksa, melihat, memilih, dan memodifikasi atribut dari sebuah lapisan.

3. Klik tombol Identifikasi pada Bilah Alat Atribut. Setelah alat dipilih, klik titik mana pun di kanvas. Atribut terkait dari titik itu akan ditampilkan di panel Identifikasi Hasil baru. Setelah Anda selesai menjelajahi atribut dari titik yang berbeda, Anda dapat mengklik tombol Tutup.

4. Daripada melihat atribut satu fitur pada satu waktu, kita dapat melihat semuanya bersama-sama sebagai sebuah tabel. Klik tombol Open Attribute Table pada Attributes Toolbar. Anda juga dapat mengklik kanan layer ne_10m_populated_places_simple dan memilih Open Attribute Table.

5. Anda dapat menggulir secara horizontal dan menemukan kolom pop_max. Bidang ini berisi populasi tempat terkait. Anda dapat mengklik dua kali pada tajuk bidang untuk mengurutkan kolom dalam urutan menurun.

6. Sekarang kita siap untuk melakukan query kita pada atribut-atribut ini. QGIS menggunakan ekspresi seperti SQL untuk melakukan query. Klik Pilih fitur menggunakan tombol ekspresi.

7. Di jendela Select By Expression, perluas bagian Fields and Values ​​dan klik dua kali label pop_max. Anda akan melihat bahwa itu ditambahkan ke bagian ekspresi di bagian bawah. Jika Anda tidak yakin tentang nilai bidang, Anda dapat mengklik tombol Semua Unik untuk melihat nilai atribut apa yang ada dalam kumpulan data. Untuk latihan ini, kami mencari semua fitur yang memiliki populasi lebih dari 1 juta. Jadi lengkapi ekspresi seperti di bawah ini dan klik Select Features lalu Close. "pop_max" > 1000000

8. Anda akan melihat bahwa beberapa baris dalam tabel atribut sekarang dipilih. Jendela label juga berubah dan menunjukkan jumlah fitur yang dipilih.

9. Tutup jendela tabel atribut dan kembali ke jendela utama QGIS. Anda akan melihat bahwa subset poin sekarang dirender dengan warna kuning. Ini adalah hasil dari kueri kami dan titik yang dipilih adalah titik yang memiliki nilai atribut pop_max lebih besar dari 1000000.

10. Mari kita perbarui kueri kita untuk menyertakan syarat bahwa tempat itu juga harus menjadi ibu kota selain memiliki populasi lebih dari 1 juta. Untuk membuka editor ekspresi dengan cepat, Anda dapat menggunakan tombol Select Features by Expression di Attributes Toolbar.

11. Kolom yang berisi data tentang huruf kapital adalah adm0cap. Nilai 1 menunjukkan bahwa tempat tersebut adalah ibukota. Kita dapat menambahkan kriteria ini ke ekspresi kita sebelumnya menggunakan operator and. Masukkan ekspresi seperti di bawah ini dan klik Select Features lalu Close. "pop_max" > 1000000 and "adm0cap" = 1.

12. Kembali ke jendela utama QGIS. Sekarang Anda akan melihat subset yang lebih kecil dari poin yang dipilih. Ini adalah hasil dari kueri kedua dan menunjukkan semua tempat dari kumpulan data yang merupakan ibu kota negara serta memiliki populasi lebih dari 1 juta.

13. Sekarang kita akan mengekspor fitur yang dipilih sebagai layer baru. Klik kanan layer ne_10m_populated_places_simple dan pergi ke Ekspor Simpan Fitur Terpilih Sebagai…

14. Anda dapat memilih format apa pun yang Anda sukai sebagai Format. Untuk latihan ini, kita akan memilih GeoJSON. GeoJSON adalah format berbasis teks yang digunakan secara luas dalam pemetaan web. Klik tombol … di sebelah Nama file dan masukkan population_capitals.geojson sebagai file output.

15. Data input memiliki banyak kolom. Anda hanya dapat memilih sebagian dari kolom asli untuk diekspor. Perluas bagian Pilih bidang yang akan diekspor dan opsi ekspornya. Klik Deselect All dan centang kolom nama dan pop_max. Klik Oke.

16. Sebuah layer baru population_capitals akan dimuat di QGIS. Anda dapat menghapus centang pada lapisan ne_10m_populated_places_simple untuk menyembunyikannya dan melihat poin dari lapisan yang baru diekspor.
