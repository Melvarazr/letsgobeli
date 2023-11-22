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
```

# Tugas 9

## 1. Apakah bisa kita melakukan pengambilan data JSON tanpa membuat model terlebih dahulu? Jika iya, apakah hal tersebut lebih baik daripada membuat model sebelum melakukan pengambilan data JSON?

Ya, kita bisa mengambil data JSON tanpa perlu membuat model terlebih dahulu, contohnya dengan menyimpan data-data JSON tersebut di dalam map. Namun, hal tersebut tidak lebih baik daripada membuat model sebelum melakukan pengambilan data JSON, karena akan menjadi lebih rumit dan mengurangi tingkat readability kode. Dengan membuat model, kode akan menjadi lebih teratur dan terabstraksi, dimana itu merupakan manfaat dari OOP.

## 2. Jelaskan fungsi dari CookieRequest dan jelaskan mengapa instance CookieRequest perlu untuk dibagikan ke semua komponen di aplikasi Flutter.

Kelas CookieRequest berfungsi untuk membuat dan mengelola permintaan HTTP yang melibatkan cookie. Ini digunakan untuk mengirim permintaan ke server yang memerlukan informasi cookie untuk otentikasi atau sesi.

Instance CookieRequest perlu dibagikan ke semua komponen di aplikasi Flutter agar informasi cookie dapat diakses dan digunakan secara konsisten di seluruh aplikasi. Ketika instance CookieRequest dibagikan, semua komponen dapat menggunakan instance yang sama untuk mengirim permintaan HTTP dengan cookie yang sama.

Hal ini penting karena ketika aplikasi berinteraksi dengan server, informasi cookie yang diperoleh dari respons server harus disimpan dan digunakan dalam permintaan selanjutnya. Jika setiap komponen memiliki instance CookieRequest yang terpisah, maka setiap komponen akan memiliki informasi cookie yang berbeda, yang dapat menyebabkan masalah dalam otentikasi atau sesi.

Dengan membagikan instance CookieRequest ke semua komponen, dipastikan bahwa seluruh komponen menggunakan informasi cookie yang sama. Ini memastikan konsistensi dalam otentikasi atau sesi di seluruh aplikasi.

## 3. Jelaskan mekanisme pengambilan data dari JSON hingga dapat ditampilkan pada Flutter.

- Membaca data JSON

  Langkah awal adalah mengambil data JSON dari sumbernya, yang dapat berupa API endpoint, file JSON lokal, atau sumber data lainnya. Package http dapat digunakan untuk mengirim permintaan HTTP ke API endpoint dan mendapatkan respons JSON. Jika kita memiliki file JSON lokal, kita dapat menggunakan package dart:convert untuk membaca file tersebut.

- Parsing data JSON

  Setelah mendapatkan respons JSON, langkah berikutnya adalah mem-parsing data tersebut agar dapat digunakan di Flutter. Package dart:convert dapat digunakan untuk mengubah respons JSON menjadi objek Dart yang dapat digunakan di aplikasi Flutter. Contohnya, metode jsonDecode() dapat digunakan untuk mengubah respons JSON menjadi objek Dart.

- Membuat model data

  Agar penggunaan data JSON di aplikasi Flutter menjadi lebih mudah, kita dapat membuat model data yang sesuai dengan struktur JSON. Model data ini akan mewakili entitas atau objek dalam JSON. Kita dapat membuat kelas Dart dengan properti yang sesuai dengan struktur JSON dan metode untuk mengonversi objek Dart menjadi JSON dan sebaliknya. Ini akan mempermudah dalam mengakses dan memanipulasi data JSON.

- Menampilkan data di Flutter

  Setelah berhasil melakukan parsing data JSON dan membuat model data yang sesuai, kita dapat menampilkannya di aplikasi Flutter. Kita dapat memanfaatkan widget seperti ListView, GridView, atau DataTable untuk menampilkan data dalam bentuk daftar, grid, atau tabel. Properti dari objek model data dapat diakses untuk menampilkan nilai-nilai relevan di dalam widget.

## 4. Jelaskan mekanisme autentikasi dari input data akun pada Flutter ke Django hingga selesainya proses autentikasi oleh Django dan tampilnya menu pada Flutter.

Pengguna menginput username dan password melalui TextField dalam framework Flutter, dan data ini disimpan dalam variabel username dan password. Saat tombol login ditekan, aplikasi mengirimkan HTTP POST request ke endpoint /auth/login/ di server Django. Data username dan password dikirimkan sebagai bagian dari body request dalam format JSON.

Server Django menerima request dan melakukan proses autentikasi terhadap pengguna. Jika autentikasi berhasil, Django mengirimkan respon berisi pesan sukses dan data pengguna. Namun, jika autentikasi gagal, Django mengirimkan respon dengan pesan kesalahan. Aplikasi Flutter menerima respon dari Django dan memeriksa apakah autentikasi berhasil. Jika berhasil, aplikasi akan mengarahkan pengguna ke halaman utama (MyHomePage); sebaliknya, jika gagal, aplikasi akan menampilkan pesan kesalahan.

Setelah pengguna berhasil login, mereka akan diarahkan ke halaman utama aplikasi di mana menu aplikasi ditampilkan.

## 5. Sebutkan seluruh widget yang kamu pakai pada tugas ini dan jelaskan fungsinya masing-masing.

- ElevatedButton: Sebuah tombol ditinggikan yang berfungsi untuk menyimpan data item setelah diisi melalui formulir.
- TextFormField: Widget input teks yang memungkinkan pengguna memasukkan informasi seperti nama item, jumlah, harga, dan deskripsi.
- GridView.count: Menampilkan daftar item dalam tata letak grid dengan jumlah kolom yang dapat diatur.
- Navigator: Bertanggung jawab atas navigasi antar halaman dalam aplikasi Flutter.
- Column: Mengorganisir widget secara vertikal, berguna untuk menyusun dan menata elemen-elemen tampilan.
- MaterialApp: Widget root yang menentukan tema dan halaman awal aplikasi Flutter.
- SnackBar: Notifikasi yang muncul setelah berhasil menyimpan item atau jika terjadi kesalahan.
- Icon: Menampilkan ikon yang mewakili setiap item.
- ShopCard: Widget kustom untuk menampilkan setiap item dalam format card.
- Text: Menampilkan teks seperti nama item untuk memberikan informasi kepada pengguna.
- Drawer: Menyediakan daftar opsi menu untuk navigasi.
- InkWell: Widget responsif terhadap sentuhan pengguna, digunakan untuk menanggapi interaksi seperti tap pada ShopCard.
- Provider: Digunakan untuk menyediakan instance CookieRequest ke seluruh aplikasi.
- Form: Menyediakan kerangka untuk membuat formulir input data item.
- Material: Mengatur warna latar belakang item di dalam grid.
- ListView: Menampilkan daftar opsi menu dalam drawer untuk navigasi.
- FutureBuilder: Mengelola tampilan berdasarkan status future untuk mendapatkan dan menampilkan data item secara asinkronus.
- Scaffold: Menyusun dasar aplikasi dengan AppBar, Drawer, dan body.
- ListTile: Membuat opsi menu dalam drawer dengan tampilan konsisten dan mudah diakses.
- GridView.builder: Menampilkan daftar item dalam bentuk grid yang dapat di-scroll.

## 6. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial).

### 1. Membuat Halaman `login.dart` pada folder screens.
```dart
import 'package:pinkloset/screens/menu.dart';
import 'package:flutter/material.dart';
import 'package:pbp_django_auth/pbp_django_auth.dart';
import 'package:provider/provider.dart';
import 'package:pinkloset/screens/register.dart';

void main() {
    runApp(const LoginApp());
}

class LoginApp extends StatelessWidget {
const LoginApp({super.key});

@override
Widget build(BuildContext context) {
    return MaterialApp(
        title: 'Login',
        theme: ThemeData(
            primarySwatch: Colors.blue,
    ),
    home: const LoginPage(),
    );
    }
}

class LoginPage extends StatefulWidget {
    const LoginPage({super.key});

    @override
    State<LoginPage> createState() {
      return _LoginPageState();
    }
}

class _LoginPageState extends State<LoginPage> {
    final TextEditingController _usernameController = TextEditingController();
    final TextEditingController _passwordController = TextEditingController();

    @override
    Widget build(BuildContext context) {
        final request = context.watch<CookieRequest>();
        return Scaffold(
            appBar: AppBar(
                title: const Center(
                  child: Text('Login'),
                ),
                backgroundColor: Colors.pink.shade900,
                foregroundColor: Colors.white,
            ),
            body: Container(
                padding: const EdgeInsets.all(16.0),
                child: Column(
                    mainAxisAlignment: MainAxisAlignment.center,
                    children: [
                        TextField(
                            controller: _usernameController,
                            decoration: const InputDecoration(
                                labelText: 'Username',
                            ),
                        ),
                        const SizedBox(height: 12.0),
                        TextField(
                            controller: _passwordController,
                            decoration: const InputDecoration(
                                labelText: 'Password',
                            ),
                            obscureText: true,
                        ),
                        const SizedBox(height: 24.0),
                        ElevatedButton(
                            onPressed: () async {
                                String username = _usernameController.text;
                                String password = _passwordController.text;

                                // Cek kredensial
                                // Untuk menyambungkan Android emulator dengan Django pada localhost,
                                // gunakan URL http://10.0.2.2/
                                final response = await request.login("http://127.0.0.1:8000/auth/login/", {
                                'username': username,
                                'password': password,
                                });
                    
                                if (request.loggedIn) {
                                    if(context.mounted){

                                      String message = response['message'];
                                      String uname = response['username'];
                                      Navigator.pushReplacement(
                                          context,
                                          MaterialPageRoute(builder: (context) => MyHomePage()),
                                      );
                                      ScaffoldMessenger.of(context)
                                          ..hideCurrentSnackBar()
                                          ..showSnackBar(
                                              SnackBar(content: Text("$message Selamat datang, $uname.")));

                                    }
                                    } else {
                                      if(context.mounted){
                                        showDialog(
                                            context: context,
                                            builder: (context) => AlertDialog(
                                                title: const Text('Login Gagal'),
                                                content:
                                                    Text(response['message']),
                                                actions: [
                                                    TextButton(
                                                        child: const Text('OK'),
                                                        onPressed: () {
                                                            Navigator.pop(context);
                                                        },
                                                    ),
                                                ],
                                            ),
                                        );

                                      }
                                }
                            },
                            child: const Text('Login'),
                        ),
                    const SizedBox(height: 24.0),
                    ElevatedButton(
                      onPressed: () {
                        Navigator.push(
                          context,
                          MaterialPageRoute(
                            builder: (context) => const RegisterPage()),
                  );
                },
                child: const Text('Register'))
          ],
        ),
      ),
    );
  }
}
```

### 2. Mengintegrasikan sistem autentikasi Django dengan proyek Flutter.
  - Pertama kita harus menambahkan app `authentication` pada Django. Selanjutnya, kita `pip install django-cors-headers` dan menambahkan `corsheaders.middleware.CorsMiddleware` pada `settings.py` aplikasi. Lalu, kita menambahkan variabel-variabel cors, session, dan csrf
  ```python 
  CORS_ALLOW_ALL_ORIGINS = True
  CORS_ALLOW_CREDENTIALS = True
  CSRF_COOKIE_SECURE = True
  SESSION_COOKIE_SECURE = True
  CSRF_COOKIE_SAMESITE = 'None'
  SESSION_COOKIE_SAMESITE = 'None'
  ```

  - Buat fungsi login pada `authentication/views.py`
  ```python
  from django.shortcuts import render
  from django.contrib.auth import authenticate, login as auth_login
  from django.http import JsonResponse
  from django.views.decorators.csrf import csrf_exempt

  @csrf_exempt
  def login(request):
      username = request.POST['username']
      password = request.POST['password']
      user = authenticate(username=username, password=password)
      if user is not None:
          if user.is_active:
              auth_login(request, user)
              # Status login sukses.
              return JsonResponse({
                  "username": user.username,
                  "status": True,
                  "message": "Login sukses!"
                  # Tambahkan data lainnya jika ingin mengirim data ke Flutter.
              }, status=200)
          else:
              return JsonResponse({
                  "status": False,
                  "message": "Login gagal, akun dinonaktifkan."
              }, status=401)

      else:
          return JsonResponse({
              "status": False,
              "message": "Login gagal, periksa kembali email atau kata sandi."
          }, status=401)
    ```

    - Tambahkan buat `urls.py` dan menambahkan path login dan path authentication di `urls.py` aplikasi
    ```python
    from django.urls import path
  from authentication.views import login

  app_name = 'authentication'

  urlpatterns = [
      path('login/', login, name='login'),
      path('auth/', include('authentication.urls')),
  ]
  ```

  - Setelah selesai setup Django kita integrasikan dengan flutter memanfaatkan package `provider` dan `pbp_django_auth`
  ```dart
      Widget build(BuildContext context) {
    return Provider(
      create: (_) {
          CookieRequest request = CookieRequest();
          return request;
      },
      child: MaterialApp(
          title: 'Flutter App',
          theme: ThemeData(
              colorScheme: ColorScheme.fromSeed(seedColor: Colors.indigo),
              useMaterial3: true,
          ),
          home: MyHomePage()),
      ),
  ...
  }
  ```
  - Selanjutnya kita dapat membuat halaman login dan meminta request dengan username dan password dengan controller untuk login dan url aplikasi kita untuk login

### 3. Membuat Halaman `MODELS` pada folder screens.
  - Membuat folder models dan membuat file `product.dart`
  - Membuat dari `quicktype.io`
  ```dart
  // To parse this JSON data, do
  //
  //     final product = productFromJson(jsonString);

  import 'dart:convert';

  List<Product> productFromJson(String str) => List<Product>.from(json.decode(str).map((x) => Product.fromJson(x)));

  String productToJson(List<Product> data) => json.encode(List<dynamic>.from(data.map((x) => x.toJson())));

  class Product {
      String model;
      int pk;
      Fields fields;

      Product({
          required this.model,
          required this.pk,
          required this.fields,
      });

      factory Product.fromJson(Map<String, dynamic> json) => Product(
          model: json["model"],
          pk: json["pk"],
          fields: Fields.fromJson(json["fields"]),
      );

      Map<String, dynamic> toJson() => {
          "model": model,
          "pk": pk,
          "fields": fields.toJson(),
      };
  }

  class Fields {
      int user;
      String name;
      DateTime dateAdded;
      int price;
      String description;

      Fields({
          required this.user,
          required this.name,
          required this.dateAdded,
          required this.price,
          required this.description,
      });

      factory Fields.fromJson(Map<String, dynamic> json) => Fields(
          user: json["user"],
          name: json["name"],
          dateAdded: DateTime.parse(json["date_added"]),
          price: json["price"],
          description: json["description"],
      );

      Map<String, dynamic> toJson() => {
          "user": user,
          "name": name,
          "date_added": "${dateAdded.year.toString().padLeft(4, '0')}-${dateAdded.month.toString().padLeft(2, '0')}-${dateAdded.day.toString().padLeft(2, '0')}",
          "price": price,
          "description": description,
      };
  }
  ```

### 4. Membuat halaman yang berisi daftar semua item yang terdapat pada endpoint JSON di Django yang telah di deploy.
  - Mengubah file `list_product.dart` dan mengambil data menggunakan `Future` dan `FutureBuilder`
  ```dart
  import 'package:flutter/material.dart';
  import 'package:http/http.dart' as http;
  import 'dart:convert';
  import 'package:shopping_list/models/product.dart';
  import 'package:shopping_list/widgets/left_drawer.dart';

  class ProductPage extends StatefulWidget {
      const ProductPage({Key? key}) : super(key: key);

      @override
      State<ProductPage> createState() => _ProductPageState();
  }

  class _ProductPageState extends State<ProductPage> {
  Future<List<Product>> fetchProduct() async {
      var url = Uri.parse(
          'http://127.0.0.1:8000/json/');
      var response = await http.get(
          url,
          headers: {"Content-Type": "application/json"},
      );

      // melakukan decode response menjadi bentuk json
      var data = jsonDecode(utf8.decode(response.bodyBytes));

      // melakukan konversi data json menjadi object Product
      List<Product> listProduct = [];
      for (var d in data) {
          if (d != null) {
              listProduct.add(Product.fromJson(d));
          }
      }
      return listProduct;
  }

  @override
  Widget build(BuildContext context) {
      return Scaffold(
          appBar: AppBar(
            title: const Center(
              child: Text('Daftar Produk'),
            ),
            backgroundColor: Colors.pink.shade900,
            foregroundColor: Colors.white,
          ),
          drawer: const LeftDrawer(),
          body: FutureBuilder(
              future: fetchProduct(),
              builder: (context, AsyncSnapshot snapshot) {
                  if (snapshot.data == null) {
                      return const Center(child: CircularProgressIndicator());
                  } else {
                      if (!snapshot.hasData) {
                      return const Column(
                          children: [
                          Text(
                              "Tidak ada data produk.",
                              style:
                                  TextStyle(color: Color(0xff59A5D8), fontSize: 20),
                          ),
                          SizedBox(height: 8),
                          ],
                      );
                  } else {
                      return ListView.builder(
                          itemCount: snapshot.data!.length,
                          itemBuilder: (_, index) => Container(
                                  margin: const EdgeInsets.symmetric(
                                      horizontal: 16, vertical: 12),
                                  padding: const EdgeInsets.all(20.0),
                                  child: Column(
                                  mainAxisAlignment: MainAxisAlignment.start,
                                  crossAxisAlignment: CrossAxisAlignment.start,
                                  children: [
                                      Text(
                                      "${snapshot.data![index].fields.name}",
                                      style: const TextStyle(
                                          fontSize: 18.0,
                                          fontWeight: FontWeight.bold,
                                      ),
                                      ),
                                      const SizedBox(height: 10),
                                      Text("${snapshot.data![index].fields.price}"),
                                      const SizedBox(height: 10),
                                      Text(
                                          "${snapshot.data![index].fields.description}")
                                  ],
                                  ),
                              ));
                      }
                  }
              }));
      }
  }
  ```