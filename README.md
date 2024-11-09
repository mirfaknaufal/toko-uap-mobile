# Toko Uap
Nama : Mirfak Naufal Pratama Putra

NPM: 2306244961

Kelas: PBP A

<details>
<summary>Tugas 7</summary>
  
## Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget, dan jelaskan perbedaan dari keduanya.
StatelessWidget adalah widget yang tidak memiliki state yang dapat berubah, sehingga tampilannya bersifat statis dan hanya diinisialisasi sekali, cocok untuk elemen UI yang tidak perlu memperbarui diri, seperti teks atau ikon. Sementara itu, StatefulWidget adalah widget yang memiliki state yang dapat berubah-ubah seiring waktu atau interaksi pengguna, memungkinkan tampilan untuk di-rebuild setiap kali state-nya diperbarui, seperti dalam kasus formulir atau animasi. Perbedaan utama antara keduanya adalah bahwa StatelessWidget bersifat statis dan tidak berubah, sedangkan StatefulWidget dinamis dan dapat berubah mengikuti state-nya.

## Sebutkan widget apa saja yang kamu gunakan pada proyek ini dan jelaskan fungsinya.
Widget utama adalah MaterialApp yang membungkus seluruh aplikasi dan menyediakan pengaturan tema dan navigasi. Scaffold digunakan untuk memberikan struktur halaman lengkap dengan AppBar di atas dan body di bawahnya. Di dalam body, terdapat Column dan Row untuk menyusun elemen-elemen UI secara vertikal dan horizontal. InfoCard adalah widget khusus yang menampilkan data seperti NPM, nama, dan kelas dalam bentuk kartu menggunakan Card. Kemudian, GridView.count membuat tata letak berbentuk grid untuk menampilkan ItemCard, yaitu kartu berikon dan teks dari list item. InkWell pada ItemCard memungkinkan interaksi dengan memberikan efek ketukan dan menampilkan SnackBar sebagai respons saat kartu ditekan.

## Apa fungsi dari `setState()?` Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.
Fungsi setState() dalam Flutter digunakan pada StatefulWidget untuk memberi tahu framework bahwa state widget telah berubah, sehingga UI perlu diperbarui atau di-rebuild. Ketika setState() dipanggil, Flutter akan memicu proses rebuild pada widget yang terpengaruh untuk menyesuaikan tampilan dengan data terbaru. Variabel yang terdampak setState() adalah semua variabel yang memengaruhi tampilan atau perilaku widget terkait, seperti counter, status autentikasi, teks input, atau pengaturan tampilan tertentu (misalnya warna atau visibilitas elemen) agar UI dapat mencerminkan kondisi terbaru.

##  Jelaskan perbedaan antara const dengan final.
Perbedaan utama antara const dan final di Dart terletak pada waktu inisialisasi dan immutability. const digunakan untuk nilai yang bersifat tetap dan konstan secara compile-time, artinya nilainya harus sudah diketahui saat kompilasi dan tidak akan pernah berubah. Sementara itu, final digunakan untuk variabel yang nilainya tetap setelah diinisialisasi, tetapi nilai tersebut bisa ditentukan pada saat runtime. Dengan kata lain, const mengharuskan nilai konstan secara penuh di compile-time, sedangkan final mengizinkan inisialisasi di runtime namun tetap tidak bisa diubah setelahnya.

## Jelaskan bagaimana cara kamu mengimplementasikan checklist-checklist di atas.
1. Membuat folder untuk menyimpan project lalu menggunakan sebuah command untuk start project pada folder tersebut.
2. Membuat file baru bernama `menu.dart`, lalu merapikan project.
3. Mengubah warna tema aplikasi pada `main.dart`, mengubah sifat widget halaman menu menjadi stateless, membuat card untuk isi data, membuat button card untuk ketiga button yang diminta, lalu mengintegrasikan seluruh project.
</details>

<details>
<summary>Tugas 8</summary>

## Apa kegunaan const di Flutter? Jelaskan apa keuntungan ketika menggunakan const pada kode Flutter. Kapan sebaiknya kita menggunakan const, dan kapan sebaiknya tidak digunakan?
Di Flutter, const digunakan untuk membuat objek yang bersifat immutable dan sudah ditentukan nilainya saat kompilasi, yang dapat meningkatkan efisiensi memori dan kinerja aplikasi karena objek const hanya dibuat satu kali dan dapat digunakan ulang tanpa perlu mengalokasikan ulang memori. Keuntungan menggunakan const adalah mengurangi beban kerja pada Garbage Collector serta mempercepat rendering UI karena widget yang tidak berubah tidak perlu di-render ulang. const sebaiknya digunakan pada widget atau objek yang nilai dan tampilannya tidak akan berubah selama aplikasi berjalan, seperti teks statis, ikon, atau padding tetap. Namun, const sebaiknya tidak digunakan jika objek tersebut memiliki nilai yang dinamis atau bergantung pada variabel yang dapat berubah saat runtime, karena ini akan menghambat fleksibilitas kode.

## Jelaskan dan bandingkan penggunaan Column dan Row pada Flutter. Berikan contoh implementasi dari masing-masing layout widget ini!
Di Flutter, Column dan Row adalah widget layout dasar yang menyusun elemen secara vertikal dan horizontal. Column menempatkan widget dalam susunan vertikal dari atas ke bawah, cocok untuk menampilkan daftar elemen yang mengikuti aliran vertikal. Sebaliknya, Row menyusun widget secara horizontal dari kiri ke kanan, ideal untuk elemen yang berbaris sejajar. Keduanya memiliki properti mainAxisAlignment dan crossAxisAlignment untuk mengatur posisi dan penyelarasan widget di dalamnya.

## Sebutkan apa saja elemen input yang kamu gunakan pada halaman form yang kamu buat pada tugas kali ini. Apakah terdapat elemen input Flutter lain yang tidak kamu gunakan pada tugas ini? Jelaskan!
Pada halaman form tugas ini, saya menggunakan elemen input TextFormField untuk mengisi informasi seperti produk, genre, dan harga. Elemen input Flutter lainnya yang tidak digunakan meliputi Checkbox, Radio, Switch, Slider, dan DropdownButton. Checkbox dan Switch berguna untuk memilih opsi ya/tidak, Radio untuk memilih satu opsi dari beberapa pilihan, Slider untuk mengatur nilai dalam rentang tertentu, dan DropdownButton menampilkan daftar pilihan dalam bentuk dropdown. Setiap elemen ini dapat digunakan sesuai kebutuhan untuk meningkatkan fleksibilitas input pengguna di aplikasi.

## Bagaimana cara kamu mengatur tema (theme) dalam aplikasi Flutter agar aplikasi yang dibuat konsisten? Apakah kamu mengimplementasikan tema pada aplikasi yang kamu buat?
Untuk mengatur tema konsisten dalam aplikasi Flutter, saya mendefinisikan tema global di main.dart dengan ThemeData pada properti theme di MaterialApp. Pada aplikasi ini, primarySwatch diset ke warna `Colors.deepPurple`, sementara secondary diset ke `Colors.deepPurple[400]` untuk menyesuaikan tampilan. Dengan konfigurasi ini, warna dan gaya elemen di seluruh aplikasi, seperti AppBar dan tombol, otomatis mengikuti tema yang telah ditentukan, sehingga tampilan aplikasi menjadi seragam dan konsisten.

## Bagaimana cara kamu menangani navigasi dalam aplikasi dengan banyak halaman pada Flutter?
Dalam aplikasi Flutter dengan banyak halaman, navigasi dapat ditangani menggunakan kombinasi Navigator.push dan Navigator.pushReplacement pada Drawer dan ItemCard. Pada LeftDrawer, saya menggunakan Navigator.pushReplacement untuk berpindah ke halaman utama tanpa kembali ke halaman sebelumnya, seperti pada MyHomePage, dan Navigator.push untuk menambahkan halaman baru ke tumpukan, seperti saat membuka ProductEntryFormPage. Di ItemCard, periksa nama item dan arahkan ke halaman terkait menggunakan Navigator.push, misalnya ketika item bernama "Tambah Item" untuk membuka ProductEntryFormPage. Pendekatan ini memungkinkan navigasi yang efisien dan intuitif antarhalaman.

</details>