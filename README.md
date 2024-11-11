PERTANYAAN TUGAS 7
1. Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget, dan jelaskan perbedaan dari keduanya.
Jawab: stateless widget adalah widget yang konfigurasinya sudah diatur sedemikian rupa di awal program, sedangkan stateful widget adalah jenis widget yang bisa berubah-ubah sesuai perlakuan user

2. Sebutkan widget apa saja yang kamu gunakan pada proyek ini dan jelaskan fungsinya.
Jawab: 
- Scaffold: struktur dasar page
- AppBar: header aplikasi
- InfoCard: menampilkan informasi nama,kelas,npm
- ItemCard: menampilkan kartu dengan tulisan di dalamnya
- Snackbar: menampilkan notifikasi telah menekan sebuah tombol
- Icon: menampilkan icon / gambar

3. Apa fungsi dari setState()? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.
Jawab: mengatur ulang state widget yang berubah, yang terdampak adalah variabel-variabel pada widget yang berjenis stateful widget

4. Jelaskan perbedaan antara const dengan final.
Jawab: variabel const nilainya bisa diubah-ubah, sedangkan final sudah ditetapkan di awal dan tidak bisa diubah-ubah

5. Jelaskan bagaimana cara kamu mengimplementasikan checklist-checklist di atas.
Jawab:
a. Membuat sebuah program Flutter baru dengan tema E-Commerce yang sesuai dengan tugas-tugas sebelumnya.
Membuat direktori untuk menyimpan project dengan nama yang sama (living-spaces) lalu jalankan 'flutter create living_spaces'

b. Membuat tiga tombol sederhana dengan ikon dan teks.
Di menu.dart, menambahkan List<ItemHomepage> yang berisi nama tombol dan icon nya

c. Mengimplementasikan warna-warna yang berbeda untuk setiap tombol (Lihat Daftar Produk, Tambah Produk, dan Logout).
Menambahkan parameter color di constructor ItemHomepage dan di build pada class ItemCard, mengatur atribut color menjadi item.color

d.Memunculkan Snackbar dengan tulisan:
 "Kamu telah menekan tombol Lihat Daftar Produk" ketika tombol Lihat Daftar Produk ditekan.
 "Kamu telah menekan tombol Tambah Produk" ketika tombol Tambah Produk ditekan.
 "Kamu telah menekan tombol Logout" ketika tombol Logout ditekan.

Di class ItemCard, menambahkan aksi ketika tombolnya berstatus onTap yaitu menampilkan snackbar dengan tulisan 'Kamu telah menekan tombol <nama_tombol>'



PERTANYAAN TUGAS 8
1. Apa kegunaan const di Flutter? Jelaskan apa keuntungan ketika menggunakan const pada kode Flutter. Kapan sebaiknya kita menggunakan const, dan kapan sebaiknya tidak digunakan?
Jawab: const digunakan untuk variabel yang sudah diketahui pada saat proses compile. sebaiknya tidak digunakan pada variabel yang kita ingin bisa diubah pada saat program berjalan.

2. Jelaskan dan bandingkan penggunaan Column dan Row pada Flutter. Berikan contoh implementasi dari masing-masing layout widget ini!
Jawab: row untuk mengatur tata letak widget secara horizontal, contohnya infocard di menu.dart yang berisi nama, npm, kelas. column untuk mengatur tata letak widget secara vertikal, contohnya menu-menu di leftdrawer.

3. Sebutkan apa saja elemen input yang kamu gunakan pada halaman form yang kamu buat pada tugas kali ini. Apakah terdapat elemen input Flutter lain yang tidak kamu gunakan pada tugas ini? Jelaskan!
Jawab: elemen input yang saya gunakan adalah TextFormField. Masih sangat banyak elemen input lain yang tidak digunakan pada tugas ini seperti radio, checkbox, switch, dan lain-lain.

4. Bagaimana cara kamu mengatur tema (theme) dalam aplikasi Flutter agar aplikasi yang dibuat konsisten? Apakah kamu mengimplementasikan tema pada aplikasi yang kamu buat?
Jawab: saya mengatur tema aplikasi saya bernuansa biru.

5. Bagaimana cara kamu menangani navigasi dalam aplikasi dengan banyak halaman pada Flutter?
Jawab: menggunakan Navigator.push untuk berpindah dan Navigator.pop untuk kembali ke halaman sebelumnya.