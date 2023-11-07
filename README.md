# Tugas 7

## 1. Apa perbedaan utama antara stateless dan stateful widget dalam konteks pengembangan aplikasi Flutter?

Stateless Widgets: Jenis widget yang memiliki status yang tidak dapat diubah setelah widget tersebut dibuat. Setelah dikembangkan, widget ini tidak dapat diubah, sehingga setiap perubahan pada variabel, ikon, tombol, atau pengambilan data tidak akan berdampak pada status aplikasi.

Stateful Widgets: Jenis widget yang memiliki status yang dapat diubah setelah widget dibuat. Status widget ini bisa berubah beberapa kali selama hidupnya. Ini berarti bahwa status aplikasi dapat mengalami perubahan seiring dengan berbagai variabel, input, dan data. Stateful Widgets biasanya digunakan dalam situasi di mana antarmuka pengguna dapat berubah dengan cepat. Contoh nya adalah CheckBox, RadioButton, Form, dan TextField.

## 2. Sebutkan seluruh widget yang kamu gunakan untuk menyelesaikan tugas ini dan jelaskan fungsinya masing-masing.

1. main.dart

    Di dalam main.dart, aplikasi Flutter dibangun menggunakan MaterialApp sebagai fondasi utama. MaterialApp ini mengatur tema dan navigasi global aplikasi. ThemeData digunakan untuk memberikan tema yang konsisten melalui aplikasi, dengan ColorScheme.fromSeed digunakan untuk menghasilkan skema warna berdasarkan warna benih yang telah ditentukan, yaitu Colors.indigo, sehingga menciptakan tampilan yang seragam dan menarik secara visual. Terdapat juga konfigurasi khusus untuk tampilan AppBar di seluruh aplikasi dengan AppBarTheme yang menetapkan background color menjadi indigo yang sesuai dengan tema. Widget MyApp adalah inti dari aplikasi ini yang mengarahkan ke halaman utama, yaitu MyHomePage, yang akan muncul ketika aplikasi dibuka.

2. menu.dart

    Dalam menu.dart ini mendefinisikan MyHomePage, sebuah widget stateless yang berfungsi sebagai halaman utama dari aplikasi. Ini menggunakan Scaffold sebagai kerangka dasar dengan AppBar dan area konten yang dapat discroll dengan SingleChildScrollView. Dalam Scaffold ini, GridView.count digunakan untuk menciptakan layout grid yang menampung elemen-elemen seperti ShopCard yang merepresentasikan visual dari ShopItem dengan judul dan ikon. Setiap ShopCard adalah widget yang interaktif dan dibungkus oleh Material dan InkWell untuk memberikan efek visual dan feedback sentuhan, seperti menampilkan SnackBar ketika diklik. Widget Column dan Padding digunakan untuk mengatur dan memberikan ruang antara elemen-elemen, sementara Container, Center, Icon, dan Text digunakan untuk menampilkan informasi dan ikonografi yang relevan secara estetis dan berfokus pada pengguna.

## 3. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial)

### Langkah 1: Membuat Struktur Folder Flutter

- Buat sebuah folder untuk proyek Flutter, misalnya dengan nama `pinkloset`.

- Di dalam folder proyek, buat subfolder dengan nama ```lib``` untuk menyimpan kode Dart.
- Di dalam folder ```lib```, buat file baru dengan nama ```menu.dart``` untuk menampung kode widget homepage.

### Langkah 2: Menghubungkan dengan Repository GitHub

- Buatlah sebuah repository GitHub kosong untuk proyek jika belum ada.
- Inisialisasi Git di dalam folder proyek dengan perintah ```git init```.
- Tambahkan semua file dan folder proyek ke dalam Git dengan perintah ```git add .```
- Buat commit pertama dengan perintah ```git commit -m "Initial commit"```.
Tambahkan remote repository GitHub ke proyek dengan perintah ```git remote add origin [URL_REPO_GITHUB]```.
Push proyek ke repository GitHub dengan perintah ```git push -u origin master```.

### Langkah 3: Membuat File menu.dart

- Buat file ```menu.dart``` di dalam subfolder ```lib``` proyek.
- Tambahkan class ```ShopItem``` untuk menyimpan informasi tentang item produk.
- Tambahkan kelas ```ShopCard``` untuk menampilkan tiap produk yang ada.
- Modifikasi kelas MyHomePage untuk menggunakan ```ShopItem``` dan menampilkan produk-produk.

### Langkah 4: Modifikasi main.dart

- Modifikasi file ```main.dart``` untuk mengimpor file ```menu.dart```.
- Di dalam kelas MyApp, gunakan MyHomePage sebagai halaman utama (home).
- Sesuaikan tema (theme) aplikasi sesuai kebutuhan.