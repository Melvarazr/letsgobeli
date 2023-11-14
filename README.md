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

# Tugas 8

## 1. Jelaskan perbedaan antara Navigator.push() dan Navigator.pushReplacement(), disertai dengan contoh mengenai penggunaan kedua metode tersebut yang tepat!

Navigator.push() dan Navigator.pushReplacement() adalah dua metode yang digunakan dalam Flutter untuk melakukan navigasi antara halaman atau layar aplikasi.

- Navigator.push() digunakan untuk menambahkan halaman baru ke dalam tumpukan navigasi. Ini memungkinkan pengguna untuk kembali ke halaman sebelumnya dengan menekan tombol kembali pada perangkat mereka. Contoh: Ketika pengguna menekan tombol untuk membuka halaman detail dari suatu item pada daftar, maka halaman detail akan ditambahkan ke dalam tumpukan navigasi.

- Navigator.pushReplacement() digunakan untuk mengganti halaman saat ini dengan halaman baru. Ketika pengguna menekan tombol kembali pada perangkat, mereka akan langsung kembali ke halaman sebelumnya sebelum halaman saat ini. Contoh: Ketika pengguna menyelesaikan suatu tugas pada halaman saat ini dan ingin kembali ke halaman sebelumnya, maka halaman saat ini akan diganti dengan halaman baru yang menampilkan pesan sukses atau ringkasan dari tugas yang telah selesai.

## 2. Jelaskan masing-masing layout widget pada Flutter dan konteks penggunaannya masing-masing!

- Align: mengatur posisi widget anaknya di dalam parent.
- Card: membuat kotak berbentuk kartu.
- Wrap: mengatur widget anaknya ke dalam baris atau kolom yang sesuai dengan ukuran layar (biasanya untuk handle widget jika kepenuhan).
- SizedBox: memberikan batasan ukuran pada widget anaknya.
- GridView: mengatur anak-anaknya dalam bentuk kotak.
- Expanded dan Flexible: Memberikan fleksibilitas dan ruang lebih pada widget anaknya.
- Listview: engelompokan yang bergulir yang mengatur anak-anaknya dalam satu daftar.
- Stack: Membuat widget dapat bertumpukan.
- Row: Mengatur widget dalam 1 baris horizontal.
- Column: Mengatur widget dalam 1 baris vertikal.
- Container: Membuat frame sehingga dapat memposisikan widget dengan lebih baik.

## 3. Sebutkan apa saja elemen input pada form yang kamu pakai pada tugas kali ini dan jelaskan mengapa kamu menggunakan elemen input tersebut!

1. Form: Widget ini saya gunakan agar menjadi wadah untuk berbagai input field widget yang telah saya buat
2. TextFormField: Widget ini saya gunakan untuk menerima input user dalam bentuk string.

## 4. Bagaimana penerapan clean architecture pada aplikasi Flutter?

Clean architecture adalah desain software yang menggunakan separation of concerns. Hal ini bertujuan untuk menghasilkan kode yang modular, scalable, dan testable. Pada flutter clean architecture terdiri atas:

1. Presentation Layer (UI): Mencakup komponen user interface, seperti widgets, screens, dan views.
2. Domain Layer (Business Logic): Berisi logika bisnis inti aplikasi. Bagian ini berisi use cases, entities, dan business rules.
3. Data Layer: Berisi data untuk pengambilan dan penyimpanan. Bagian ini terdiri dari repositori dan sumber data. Repositori menyediakan lapisan abstraksi untuk mengakses dan memanipulasi data.

## 5. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial)

- Modifikasi `main.dart`:
```dart
import 'package:flutter/material.dart';
import 'package:shopping_list/screens/menu.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Pinkloset',
      theme: ThemeData(
        // This is the theme of your application.
        //
        // TRY THIS: Try running your application with "flutter run". You'll see
        // the application has a blue toolbar. Then, without quitting the app,
        // try changing the seedColor in the colorScheme below to Colors.green
        // and then invoke "hot reload" (save your changes or press the "hot
        // reload" button in a Flutter-supported IDE, or press "r" if you used
        // the command line to start the app).
        //
        // Notice that the counter didn't reset back to zero; the application
        // state is not lost during the reload. To reset the state, use hot
        // restart instead.
        //
        // This works for code too, not just values: Most code changes can be
        // tested with just a hot reload.
        colorScheme: ColorScheme.fromSeed(seedColor: Colors.indigo),
        useMaterial3: true,
      ),
      home: MyHomePage(),
    );
  } 
}
```

- Buat direktori `lib/screens` dan `lib/widgets`
- Pindahkan file `menu.dart` ke dalam direktori `lib/screens`
- Modifikasi file `menu.dart` dan tambahkan file  `shop_card.dart` dalam direktori `lib/widgets`:

```dart
import 'package:flutter/material.dart';
import 'package:shopping_list/widgets/left_drawer.dart';
import 'package:shopping_list/widgets/shop_card.dart';

class ShopItem {
  final String name;
  final IconData icon;

  ShopItem(this.name, this.icon);
}

class MyHomePage extends StatelessWidget {
  MyHomePage({Key? key}) : super(key: key);
  final List<ShopItem> items = [
    ShopItem("Lihat Item", Icons.checklist),
    ShopItem("Tambah Item", Icons.add_shopping_cart),
    ShopItem("Logout", Icons.logout),
  ];
  // This widget is the home page of your application. It is stateful, meaning
  // that it has a State object (defined below) that contains fields that affect
  // how it looks.

  // This class is the configuration for the state. It holds the values (in this
  // case the title) provided by the parent (in this case the App widget) and
  // used by the build method of the State. Fields in a Widget subclass are
  // always marked "final".

  
  @override
  Widget build(BuildContext context) {
    // This method is rerun every time setState is called, for instance as done
    // by the _incrementCounter method above.
    //
    // The Flutter framework has been optimized to make rerunning build methods
    // fast, so that you can just rebuild anything that needs updating rather
    // than having to individually change instances of widgets.
    return Scaffold(
      appBar: AppBar(
        title: const Text(
          'Pinkloset <3',
        ),
        backgroundColor: Colors.pink.shade900,
        foregroundColor: Colors.white,
      ),
      // Masukkan drawer sebagai parameter nilai drawer dari widget Scaffold
      drawer: const LeftDrawer(),
      body: SingleChildScrollView(
        // Widget wrapper yang dapat discroll
        child: Padding(
          padding: const EdgeInsets.all(10.0), // Set padding dari halaman
          child: Column(
            // Widget untuk menampilkan children secara vertikal
            children: <Widget>[
              const Padding(
                padding: EdgeInsets.only(top: 10.0, bottom: 10.0),
                // Widget Text untuk menampilkan tulisan dengan alignment center dan style yang sesuai
                child: Text(
                  'Pinkloset', // Text yang menandakan toko
                  textAlign: TextAlign.center,
                  style: TextStyle(
                    fontSize: 30,
                    fontWeight: FontWeight.bold,
                  ),
                ),
              ),
              // Grid layout
              GridView.count(
                // Container pada card kita.
                primary: true,
                padding: const EdgeInsets.all(20),
                crossAxisSpacing: 10,
                mainAxisSpacing: 10,
                crossAxisCount: 3,
                shrinkWrap: true,
                children: items.map((ShopItem item) {
                  // Iterasi untuk setiap item
                  return ShopCard(item);
                }).toList(),
              ),
            ],
          ),
        ),
      ),
    );
  }
}
```

```dart
import 'package:flutter/material.dart';
import 'package:shopping_list/screens/menu.dart';
import 'package:shopping_list/screens/shoplist_form.dart';
import 'package:shopping_list/screens/product_list_page.dart';

class ShopCard extends StatelessWidget {
  final ShopItem item;
  
  const ShopCard(this.item, {Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    Color cardColor; // Variabel untuk menentukan warna latar belakang

    // Menentukan warna berdasarkan nama item
    if (item.name == "Lihat Item") {
      cardColor = Colors.pink.shade600; // Warna untuk "Lihat Produk"
    } else if (item.name == "Tambah Item") {
      cardColor = Colors.pink.shade300; // Warna untuk "Tambah Produk"
    } else if (item.name == "Logout") {
      cardColor = Colors.pink.shade100; // Warna untuk "Logout"
    } else {
      cardColor = Colors.indigo; // Warna default jika tidak ada yang cocok
    }

    return Material(
      color: cardColor, // Menggunakan warna yang telah ditentukan
      child: InkWell(
        onTap: () {
          ScaffoldMessenger.of(context)
            ..hideCurrentSnackBar()
            ..showSnackBar(SnackBar(
                content: Text("Kamu telah menekan tombol ${item.name}!")));

            if (item.name == "Tambah Item") {
              Navigator.push(context,
                  MaterialPageRoute(builder: (context) => const ShopFormPage()));
            } else if (item.name == "Lihat Item") {
              Navigator.push(context,
                  MaterialPageRoute(builder: (context) => const ProductListPage()));
            }
        },
        child: Container(
          padding: const EdgeInsets.all(8),
          child: Center(
            child: Column(
              mainAxisAlignment: MainAxisAlignment.center,
              children: [
                Icon(
                  item.icon,
                  color: Colors.white,
                  size: 50.0,
                ),
                const Padding(padding: EdgeInsets.all(3)),
                Text(
                  item.name,
                  textAlign: TextAlign.center,
                  style: const TextStyle(color: Colors.white),
                ),
              ],
            ),
          ),
        ),
      ),
    );
  }
}
```

- Tambahkan left_drawer.dart ke dalam direktori `lib/widgets`:
```dart
import 'package:flutter/material.dart';
import 'package:shopping_list/screens/menu.dart';
import 'package:shopping_list/screens/product_list_page.dart';
import 'package:shopping_list/screens/shoplist_form.dart';

class LeftDrawer extends StatelessWidget {
  const LeftDrawer({super.key});

  @override
  Widget build(BuildContext context) {
    return Drawer(
      child: ListView(
        children: [
          const DrawerHeader(
            decoration: BoxDecoration(
              color: Colors.pinkAccent,
            ),
            child: Column(
              children: [
                Text(
                  'Pinkloset <3',
                  textAlign: TextAlign.center,
                  style: TextStyle(
                    fontSize: 30,
                    fontWeight: FontWeight.bold,
                    color: Colors.white,
                  ),
                ),
                Padding(padding: EdgeInsets.all(10)),
                Text("Catat seluruh keperluan belanjamu di sini!",
                  textAlign: TextAlign.center,
                  style: TextStyle(
                    fontSize: 15,
                    color: Colors.white,
                    fontWeight: FontWeight.normal,
                  ),
                ),
              ],
            ),
          ),
          ListTile(
            leading: const Icon(Icons.home_outlined),
            title: const Text('Halaman Utama'),
            // Bagian redirection ke MyHomePage
            onTap: () {
              Navigator.pushReplacement(
                  context,
                  MaterialPageRoute(
                    builder: (context) => MyHomePage(),
                  ));
            },
          ),
          ListTile(
            leading: const Icon(Icons.add_shopping_cart),
            title: const Text('Tambah Item'),
            // Bagian redirection ke ShopFormPage
            onTap: () {
              /*
              setelah halaman ShopFormPage sudah dibuat.
              */
              Navigator.pop(context);
              Navigator.push(
                context,
                MaterialPageRoute(
                  builder: (context) => const ShopFormPage(),
                ));
            },
          ),
          ListTile(
            leading: const Icon(Icons.checklist),
            title: const Text('Lihat Item'),
            onTap: () {
              Navigator.pop(context);
              Navigator.push(
                context,
                MaterialPageRoute(
                  builder: (context) => const ProductListPage(), // Navigate to the "View Products" page
                ),
              );
            },
          ),
        ],
      ),
    );
  }
}
```
- Tambahkan file `shoplist_form.dart` ke dalam direktori `lib/screens`:
```dart
import 'package:flutter/material.d