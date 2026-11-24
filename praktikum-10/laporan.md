# Laporan Praktikum Pertemuan 10 — Pemrograman Web 1 
## Percobaan 1 — Navbar Lab 
(tabel pengamatan 2.3) 
| No| Eksperimen                                                   | Pengamatan                                                                                                                                                                                       |
| 1 | Class `#menuLab` dan nilai `aria-expanded` saat menu terbuka  | Saat menu terbuka, class `show` ditambahkan pada `#menuLab` dan nilai `aria-expanded` berubah menjadi `true`. Saat ditutup, class `show` dihapus dan nilainya menjadi `false`.                  |
| 2 | Hamburger di 1000 px dengan `navbar-expand-lg`                | Hamburger tidak tampil karena lebar 1000 px lebih besar dari 992 px. Menu tampil berjajar secara horizontal.                                                                                    |
| 3 | Perilaku di 800 px: `-md` / tanpa sufiks / tanpa class expand | Dengan `navbar-expand-md`, menu berjajar dan hamburger tidak muncul. Tanpa sufiks atau tanpa class expand, menu selalu tampil berderet, termasuk di desktop.                                    |
| 4 | `data-bs-target` salah ketik                                  | Tombol hamburger tidak dapat membuka menu karena target tidak sesuai dengan ID elemen menu.                                                                                                     |
| 5 | Tanpa JS bundle                                               | Tampilan tetap sama, tetapi hamburger dan dropdown tidak berfungsi karena JavaScript Bootstrap tidak tersedia.                                                                                  |
| 6 | `bg-dark` tanpa dan dengan `data-bs-theme="dark"`             | `bg-dark` saja membuat latar belakang gelap, tetapi teks menu juga gelap sehingga sulit dibaca. Dengan `data-bs-theme="dark"`, teks dan ikon hamburger menjadi terang.                          |
| 7 | `sticky-top` vs `fixed-top`                                   | `sticky-top` membuat navbar menempel saat halaman digulir dan tidak menutupi judul. `fixed-top` membuat navbar tetap berada di atas dan dapat menutupi judul karena keluar dari aliran dokumen. |

_
Catatan: Hasil pengamatan di atas mengikuti bagian 2.4 Hasil yang Diharapkan pada modul. Pastikan hasil percobaan di browser sesuai sebelum dimasukkan ke laporan.

## Percobaan 2 — Buttons & Badges 
(tabel pengamatan 3.3) 
| No| Eksperimen                                              | Pengamatan                                                                                                                                                                                      | 
| 1 | Kelompok Batal–Simpan di 375 px dan 1000 px             | Pada 375 px, kedua tombol bertumpuk selebar penuh. Pada 1000 px, tombol berjajar dan rata kanan.                                                                                                |
| 2 | Elemen nonaktif yang masih bisa difokus dengan Tab      | Tombol disabled tidak bisa difokus dengan Tab. Tautan yang hanya diberi class disabled masih bisa difokus dan diaktifkan dengan Enter. Tautan dengan aria-disabled="true" tidak menerima fokus. |
| 3 | Kontras text-bg-warning vs bg-warning                   | text-bg-warning menghasilkan teks gelap di atas warna kuning dengan kontras yang memenuhi standar AA. bg-warning saja menggunakan teks putih bawaan badge sehingga kontrasnya rendah.           |
| 4 | Nama tombol Notifikasi dengan dan tanpa visually-hidden | Dengan visually-hidden, nama tombol terbaca "Notifikasi 3 notifikasi belum dibaca". Tanpanya, nama tombol hanya "Notifikasi 3".                                                                 |

Catatan: Hasil pengamatan di atas mengikuti bagian 3.4 Hasil yang Diharapkan pada modul. Pastikan kamu sudah melakukan percobaan di browser sebelum memasukkan hasilnya ke laporan.

## Percobaan 3 — Tipografi 
(tabel pengamatan 4.3) 
| No| Class lama                     | Utilitas pengganti (isi)                     | Tampilan sama? (ya/tidak)    |
| 1 |.judul-besar                    | display-5 text-center                        | Ya                           | 
| 2 |.pembuka                        | lead text-body-secondary text-center         | Ya                           |
| 3 |.label                          | text-uppercase fw-bold small`                | Ya, kecuali jarak antarhuruf |
| 4 |.catatan                        | small fst-italic`                            | Ya                           |
| 5 |.nim                            | font-monospace`                              | Ya                           |
| 6 | Temuan Lighthouse untuk `<h4>` | Tetap menggunakan `<h2>` dengan `class="h4"` | Ya                           |

Class .pembuka diganti dengan lead text-body-secondary text-center untuk membuat teks pembuka lebih besar, berwarna abu-abu, dan berada di tengah.
Class .label diganti dengan text-uppercase fw-bold small. Jarak antarhuruf sedikit berbeda karena Bootstrap tidak menyediakan utilitas bawaan untuk letter-spacing.
Class .catatan diganti dengan small fst-italic untuk membuat teks lebih kecil dan miring.
Class .nim diganti dengan font-monospace untuk menggunakan jenis huruf monospace.
Temuan Lighthouse menunjukkan urutan heading tidak berurutan menurun. Solusinya adalah tetap menggunakan <h2> dan menambahkan class="h4" agar tampilannya lebih kecil tanpa mengubah urutan heading.



## Jawaban Pertanyaan Analisis 
1. Berdasarkan Percobaan 1 langkah 1, jelaskan apa yang dilakukan JavaScript Bootstrap terhadap DOM saat hamburger diklik. Kaitkan dengan materi manipulasi DOM pertemuan 6.
Saat tombol hamburger diklik, JavaScript Bootstrap memanipulasi DOM dengan menambahkan atau menghapus class show pada elemen menu navbar. Jika menu terbuka, atribut aria-expanded berubah menjadi true. Jika menu ditutup, atribut tersebut berubah menjadi false. Hal ini merupakan contoh manipulasi DOM menggunakan JavaScript untuk mengubah tampilan dan perilaku elemen HTML tanpa harus memuat ulang halaman.

2. Mengapa pada Percobaan 1 langkah 5 tampilan navbar tetap ada tetapi interaksinya hilang?
Karena file Bootstrap CSS masih dimuat sehingga tampilan navbar tetap terlihat. Namun, JavaScript Bootstrap tidak dimuat sehingga tombol hamburger dan dropdown tidak dapat berfungsi. CSS mengatur tampilan elemen, sedangkan JavaScript mengatur interaksi dan perubahan DOM.

3. Dari Percobaan 2, mengapa tautan dengan class disabled yang masih memiliki href dianggap tidak aman?
Karena class disabled hanya mengubah tampilan tautan agar terlihat seperti elemen nonaktif. Tautan tersebut masih dapat difokuskan menggunakan tombol Tab dan diaktifkan menggunakan Enter karena masih memiliki atribut href. Hal ini dapat membingungkan pengguna, terutama pengguna keyboard dan pembaca layar. Oleh karena itu, untuk tautan yang benar-benar nonaktif, atribut href perlu dihilangkan dan ditambahkan aria-disabled="true" jika diperlukan.

4. Sebutkan dua alasan <h2 class="h5"> lebih baik daripada <h5> untuk judul panel dashboard.
<h2 class="h5"> tetap mempertahankan hierarki heading yang benar secara semantik. Hal ini membantu pengguna pembaca layar dan alat seperti Lighthouse memahami struktur halaman.
Class h5 dari Bootstrap hanya mengubah ukuran tampilan teks tanpa mengubah tingkat heading. Dengan demikian, judul panel dapat terlihat lebih kecil tanpa harus melewati urutan heading, misalnya dari <h1> langsung ke <h5>.

5. Berapa skor Lighthouse Accessibility dashboard Anda? Temuan apa yang Anda perbaiki?
Untuk nomor 5, isi skor sesuai hasil pengujian Lighthouse pada dashboard milikmu. Skor tersebut tidak terlihat pada gambar yang dikirimkan.
Contoh penulisan jika skor Lighthouse kamu 95:
Skor Lighthouse Accessibility dashboard adalah 95. Temuan yang diperbaiki meliputi penyesuaian hierarki heading, penambahan atribut aksesibilitas pada elemen interaktif, serta perbaikan kontras warna teks dan latar belakang. Perbaikan ini dilakukan agar halaman lebih mudah digunakan oleh pengguna, termasuk pengguna yang menggunakan pembaca layar dan navigasi keyboard.

## Kesimpulan
Berdasarkan hasil Praktikum 10 Pemrograman Web 1, dapat disimpulkan bahwa Bootstrap mempermudah pembuatan tampilan website yang responsif, menarik, dan mudah digunakan. Pada Percobaan 1, navbar dapat menyesuaikan tampilan berdasarkan ukuran layar serta menggunakan JavaScript Bootstrap untuk mengatur interaksi menu hamburger dan dropdown. Pada Percobaan 2, penggunaan buttons dan badges membantu membuat elemen interaktif yang lebih jelas, serta memperhatikan aksesibilitas melalui navigasi keyboard, kontras warna, dan atribut tambahan. Pada Percobaan 3, CSS buatan sendiri dapat diganti dengan utilitas tipografi Bootstrap tanpa mengubah tampilan halaman secara signifikan. Selain itu, penggunaan heading yang sesuai membantu menjaga struktur halaman agar tetap benar secara semantik. Dengan demikian, Bootstrap dapat membantu pengembangan website yang responsif, konsisten, dan lebih mudah diakses oleh berbagai pengguna.