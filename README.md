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
