# Laporan Praktikum Pertemuan 5 — Pemrograman Web 1 
Nama  : Selvi Mardiana
NIM   : 2510010232
Kelas : 3B TI REG BJB 

### Tabel Pengamatan 3.3

| No | Kondisi      | Lebar Kotak A (px) | Lebar Kotak B (px) |
|----|--------------|--------------------|--------------------|
| 1  | padding 20px |350                 |300                 |
| 2  | padding 40px |390                 |300                 |

| No | Kondisi                 | Jarak judul-paragraf (px) |
|----|-------------------------|---------------------------|
| 3  | Block biasa             |30                         |
| 4  | Di dalam flex column    |50                         |

| No | Kondisi .menu a     | Latar menimpa teks lain? (ya/tidak)|
|----|---------------------|------------------------------------|
| 5  | inline (bawaan)     |ya                                  |
| 6  | inline-block        |tidak                               |

### Tabel Pengamatan 4.3

| No | Properti dan nilai                               | Pengamatan (tulis dengan kalimat Anda sendiri)                                                                |
|----|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 1  | display: flex                                    | Item pindah posisi dari atas kebawah menjadi berderet kesamping.                                                       |
| 2  | justify-content: space-between                   | Item menempel di ujung kiri dan kanan, sisa ruang terbagi rata di antara item.                                |
| 2  | justify-content: space-evenly                    | Jarak kosong di tepi kiri, kanan, dan antar-item terbagi sama rata secara sejajar.                            |
| 3  | align-items: stretch vs center                   | Stretch ditarik memenuhi wadah, sedangkan center membuat item berada di tengah vertikal.                      |
| 4  | flex-direction: column + justify-content: center | Item tersusun vertikal, dan justify-content memindahkan item ke posisi tengah secara vertikal.                |
| 5  | 8 item x 200 px, nowrap vs wrap                  | Pada nowrap item dipaksa mengecil, sedangkan pada wrap item yang tidak muat pindah ke baris baru di bawahnya. |
| 6  | .b { flex-grow: 1 }                              | Item B akan melebar mengisi seluruh sisa ruang yang kosong pada wadah.                                    |
| 7  | Lebar A / B / C (px)                             | Lebar A = 200px, Lebar B = 300px, Lebar C = 400px.                                                            |
| 8  | .c { order: -1 }                                 | Urutan tampilan item C pindah menjadi paling pertama di sebelah kiri.                                |
| 9  | .c { margin-left: auto }                         | Item C tergeser ke ujung paling kanan wadah, menyisakan ruang yang   kosong di sebelah kirinya.                     |
| 10 | gap: 24px                                        | Terbentuk jarak pemisah sebesar 24px secara konsisten di antara item.                                         |

### Tabel Pengamatan 5.3

| No  | Eksperimen                                 | Pengamatan                                                                                                                                                                                           |
|-----|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | Header sticky saat digulir                 | Header mengikut alur dokumen saat di atas, lalu menempel terkunci di batas atas layar (`top: 0`) ketika halaman digulir ke bawah.                                                                    |
| 2a  | Header fixed tanpa padding-top body        | Header keluar dari alur dokumen normal sehingga menutupi bagian atas dari judul `h1` dan paragraf pertama halaman.                                                                                   |
| 2b  | Header fixed dengan padding-top 64px       | Konten halaman turun ke bawah sejauh 64px sehingga teks awal halaman kembali terlihat sepenuhnya dan tidak tertutup header.                                                                          |
| 3   | .notif tanpa position: relative            | Badge angka "3" melompat keluar dari tombol lonceng dan menempel ke pojok kanan atas elemen leluhur terdekat yang memiliki posisi (`.header`).                                                       |
| 4   | .lapis-1 z-index 3, lalu lapis-2 z-index 5 | Urutan tumpukan berubah; Lapis 1 menutupi Lapis 3, kemudian Lapis 2 yang memiliki `z-index` paling tinggi (5) berada di posisi paling depan menutupi semuanya.                                       |
| 5   | Header z-index 1                           | Header masih berada di atas elemen lapis yang tidak memiliki `z-index`, tetapi elemen lapis yang memiliki `z-index` lebih tinggi (seperti Lapis 1 dan Lapis 2) akan menutupi header saat bersentuhan.|
| 6   | Tombol Bantuan di layar 375 px             | Tombol bantuan dengan posisi `fixed` akan tetap konsisten menempel melayang di pojok kanan bawah jendela browser meskipun layar dipersempit atau digulir.                                            |


### Tabel Pengamatan 5.3

| No  | Eksperimen                                 | Pengamatan                                                                                                                                                                                           |
|-----|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | Header sticky saat digulir                 | Header mengikut alur dokumen saat di atas, lalu menempel dan terkunci pada batas atas layar (`top: 0`) ketika halaman digulir ke bawah.                                                                    |
| 2a  | Header fixed tanpa padding-top body        | Header keluar dari alur dokumen normal hingga menutupi bagian atas dari judul `h1` dan paragraf pertama halaman.                                                                                   |
| 2b  | Header fixed dengan padding-top 64px       | Konten halaman turun ke bawah sejauh 64px sehingga teks awal halaman kembali terlihat sepenuhnya dan tidak tertutup header.                                                                          |
| 3   | .notif tanpa position: relative            | Badge angka "3" melompat keluar dari tombol lonceng dan menempel ke pojok kanan atas elemen leluhur terdekat yang memiliki posisi (`.header`).                                                       |
| 4   | .lapis-1 z-index 3, lalu lapis-2 z-index 5 | Urutan tumpukan berubah; Lapis 1 menutupi Lapis 3, kemudian Lapis 2 yang memiliki `z-index` paling tinggi (5) berada di posisi paling depan menutupi semuanya.                                       |
| 5   | Header z-index 1                           | Header masih berada di atas elemen lapis yang tidak memiliki `z-index`, tetapi elemen lapis yang memiliki `z-index` lebih tinggi (seperti Lapis 1 dan Lapis 2) akan menutupi header saat bersentuhan.|
| 6   | Tombol Bantuan di layar 375 px             | Tombol bantuan dengan posisi `fixed` akan tetap konsisten menempel melayang di pojok kanan bawah jendela browser meskipun layar dipersempit atau digulir.                                            |

## Percobaan 4 — Dashboard 
Hasil tangkap layar saya letakkan di folder img.

## Jawaban Pertanyaan Analisis
1. Aturan box-sizing: border-box di awal stylesheet
Penggunaan border-box membuat perhitungan lebar (width) dan tinggi (height) elemen mencakup padding dan border. Hal ini memudahkan pengaturan tata letak karena ukuran elemen tidak akan bertambah lebar atau rusak saat kita menambahkan padding atau border.
2. ​Pengaruh flex-direction: column pada justify-content: center
Secara bawaan, main axis berarah horizontal dan cross axis berarah vertikal. Saat kita mengubah flex-direction menjadi column, main axis berputar menjadi vertikal. Karena justify-content bertugas mengatur elemen di sepanjang main axis, maka properti tersebut memusatkan item secara vertikal.
3. ​Perhitungan lebar item B dan C pada eksperimen 7
Pada flex: 0 0 200px untuk A, flex: 1 untuk B, dan flex: 2 untuk C, item A berukuran tetap 200px. Sisa ruang (800px) dibagi dengan rasio 1:2, sehingga B mendapat \approx 266,7\text{px} dan C mendapat \approx 533,3\text{px}. Jika B diberi flex: 1 1 auto, B akan memperhitungkan lebar awal kontennya terlebih dahulu sebelum mengambil sisa ruang kosong.
4. ​Alasan badge menempel ke header saat position: relative pada .notif dihapus
Elemen dengan position: absolute akan mencari elemen leluhur (parent) terdekat yang memiliki posisi non-static sebagai titik acuannya. Ketika position: relative pada .notif dihapus, badge mencari ke atas dan menemukan .header (yang memiliki position: sticky), sehingga badge menempel di pojok header.
5. ​Perbandingan sticky dan fixed untuk navbar dashboard
Saya memilih sticky. Alasannya, sticky tetap mempertahankan alur dokumen normal saat halaman di bagian atas sehingga elemen di bawahnya tidak tertutup, berbeda dengan fixed yang membutuhkan padding-top pada body agar konten utama tidak tertutup navbar.
6. ​Fungsi flex: 1 pada .wrapper
Properti flex: 1 pada .wrapper berfungsi untuk meregangkan area utama agar mengisi seluruh sisa ruang vertikal layar yang tersedia. Jika baris ini dihapus, .wrapper hanya setinggi kontennya sehingga footer akan naik ke tengah layar saat isi halaman sedikit.

## Kesimpulan 
(3–5 kalimat: apa yang dipelajari dan kendala yang dihadapi) 
Pada praktikum ini, saya mempelajari konsep CSS Box Model, Flexbox layout, dan Positioning untuk membangun struktur dashboard web yang rapi dan mudah dipahami. Saya memahami pentingnya penggunaan border-box agar ukuran elemen tetap konsisten serta pemanfaatan Flexbox untuk mengatur tata letak yang fleksibel di layar desktop maupun mobile. Kendala yang sempat dihadapi adalah penyesuaian ukuran tampilan responsif di DevTools, namun dapat diatasi dengan baik menggunakan media query.