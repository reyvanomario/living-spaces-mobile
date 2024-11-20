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


PERTANYAAN TUGAS 9
1. Jelaskan mengapa kita perlu membuat model untuk melakukan pengambilan ataupun pengiriman data JSON? Apakah akan terjadi error jika kita tidak membuat model terlebih dahulu?
Jawab: agar data bisa direpresentasikan secara terstruktur. jika tidak membuat model, belum tentu akan error tapi akan lebih sulit dalam mengolah data.

2. Jelaskan fungsi dari library http yang sudah kamu implementasikan pada tugas ini
Jawab: untuk melakukan perintah http request

3. Jelaskan fungsi dari CookieRequest dan jelaskan mengapa instance CookieRequest perlu untuk dibagikan ke semua komponen di aplikasi Flutter.
Jawab: CookieRequest berfungsi untuk mengelola dan menyimpan cookie secara lokal, perlu untuk dibagikan ke semua komponen agar menghindari redundansi karena setiap komponen tidak perlu mengelola session secara tersendiri.

4. Jelaskan mekanisme pengiriman data mulai dari input hingga dapat ditampilkan pada Flutter.
Jawab: 
- Data diambil dari field misalnya TextFormField
- Dilakukan validasi pada data yang ambil dengan validator
- Data yang sudah divalidasi dikirim ke server (di tugas ini ke server django)
- Data diambil dari server, lalu disimpan ke state
- Data ditampilkan dalam widget flutter

5. Jelaskan mekanisme autentikasi dari login, register, hingga logout. Mulai dari input data akun pada Flutter ke Django hingga selesainya proses autentikasi oleh Django dan tampilnya menu pada Flutter.
Jawab: 
Register:
- User input username dan passwordnya lalu dikirimkan ke url "http://127.0.0.1:8000/auth/register/". Berhasil atau tidaknya register ditentukan di django dan di flutter akan ditampilkan pesan sesuai dengan response yang diberikan django di fungsi await request.postJson

Login:
- User input username dan passwordnya lalu dikirimkan ke url "http://127.0.0.1:8000/auth/login/". Berhasil atau tidaknya login ditentukan di django dan di flutter akan ditampilkan pesan sesuai dengan output di fungsi "context.watch<CookieRequest>();". Jika login berhasil, pengguna akan diteruskan ke halaman utama aplikasi

Logout:
- Memanggil url "http://127.0.0.1:8000/auth/logout/" dan menjalankan fungsi logout di django serta menampilkan pesan logout berdasarkan respons di fungsi "await request.logout".

6. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial).
Jawab:
a. Mengimplementasikan fitur registrasi akun pada proyek tugas Flutter.
Membuat fungsi register di proyek django di app authentication, melakukan routing, lalu membuat folder baru di proyek flutter bernama screens dan di dalamnya membuat halaman register.dart. Setelah itu akan mengirim request register ke django dan django akan memberikan respons.

b. Membuat halaman login pada proyek tugas Flutter.
Membuat fungsi login di proyek django di app authentication, melakukan routing, lalu membuat halaman register.dart di folder screens di proyek flutter. Setelah itu akan mengirim request untuk login ke django dan django akan memberikan respons apakah login berhasil atau tidak.

c. Mengintegrasikan sistem autentikasi Django dengan proyek tugas Flutter.
Memanggil fungsi  await request.postJson(...) yang mengirimkan request ke parameter url yaitu django di localhost

d. Membuat model kustom sesuai dengan proyek aplikasi Django.
Mengambil data dalam bentuk json yang ada di proyek django, lalu mengubah ke dalam bahasa dart menggunakan bantuan website Quicktype dan memasukkannya ke file product_entry.dart di folder baru bernama models.

e. Membuat halaman yang berisi daftar semua item yang terdapat pada endpoint JSON di Django yang telah kamu deploy.
Membuat file list_productentry lalu menampilkan tiap fields product di widget Text dengan cara Text("${snapshot.data![index].fields.name}") untuk fields name, dan fields-fields lainnya.

f. Membuat halaman detail untuk setiap item yang terdapat pada halaman daftar Item.

g. Melakukan filter pada halaman daftar item dengan hanya menampilkan item yang terasosiasi dengan pengguna yang login.
Mengambil data produk dengan fungsi fetchProduct ke url http://127.0.0.1:8000/json/ dan mengonversi ke list object Product

