# Week 1
## A. Unix Command Line
- CLI merupakan akronim dari Command Line Interface. Dengan program ini, user bisa mengetik perintah dalam bentuk teks dan memberikan instruksi pada komputer untuk mengerjakan tugas tertentu.
- Saat kita menyebut "command line" atau "command line interface", sebenarnya yang dimaksud adalah shell yang berbasis teks. Shell ini adalah program yang menerima perintah, kemudian meneruskan perintah tersebut ke system untuk dieksekusi. 
- Contoh dari CLI, yaitu : bash dan cmd.exe
- Filesystem mengatur bagaimana data disimpan di dalam sebuah system
- Sistem operasi Windows & Unix-like menyusun file dan direktori menggunakan struktur yang bentuknya mirip tree

**Command untuk navigasi**
a. pwd (Print working directory) : Command untuk melihat current working directory
b. ls (lists) : Command untuk melihat isi file yang ada di sebuah direktori
c. cd <direktori> (change directory) : Command untuk berpindah direktori.

**Command untuk membuat Files dan Direktori**
a. touch : Command untuk membuat sebuah file
b. mkdir : Command untuk membuat sebuah direktori

**Command untuk Melihat isi files**
a. head : Command untuk melihat beberapa line awal dari sebuah file text
b. tail : Command untuk melihat beberapa line akhir dari sebuah file text
c. cat : Command untuk melihat isi sebuah file

**Command untuk menyalin, memindahkan, dan menghapus files & directory**
a. cp (copy) : Command untuk mengcopy files atau directory (cp -R untuk menyalin direktori)
b. mv (move) : Command untuk memindahkan files atau directory (mv -R untuk memindahkan direktori) serta dapat digunakan untuk rename
c. rm (remove) : Command untuk menghapus file atau directory (rm -R atau rm -d untuk menghapus direktori)

## B. GIT & GITHUB
- GIT merupakan tools untuk programmer dan sebagai version control system
- Tugas dari version control system yaitu mencatat setiap perubahan pada File (termasuk code yang kita buat) pada suatu proyek baik dikerjakan secara individu maupun tim.
- Git adalah aplikasi yang dapat melacak setiap perubahan yang terjadi pada suatu folder atau file. Git digunakan sebagai tempat penyimpanan file pemrograman mereka, karena lebih efektif.
- Tujuan dari penggunaan Git dan Github yaitu agar kita bisa berkolaborasi mengerjakan proyek yang sama tanpa harus repot copy dan paste folder aplikasi yang terupdate
- Git dan GitHub menangani commands secara berbeda. Developer yang menggunakan Git dapat menggunakan command-line tool, yaitu pengubah kode dan dapat digabungkan menuju perangkat lokal. Sedangkan, GitHub menyediakan interface grafis berbasis cloud sebagai tempat untuk melakukan seluruh tugas.

**Setup Awal Git**
a. git config --global user.email chandrawsyahputra@gmail.com (email yang digunakan harus sama dengan Github)
b. git config --global user.name "ChandraSyahputra"
c. git config --list untuk melihat hasil konfigurasi
d. git init (dilakukan pada folder yang dibuat) untuk membuka repository
e. git status untuk mengecek perubahan pada Git
f. git add . untuk menambahkan file baru pada Git
g. git commit -m "Pesan Commit" untuk menyimpan perubahan pada Git
h. git push -u origin master / main untuk mengirim file pada remote repository
i. git clone untuk mengambil repository lokal

## C. HTML
- HTML (Hypertext Markup Language) berfungsi untuk membuat kerangka dari sebuah website dan digunakan untuk menampilkan konten pada browser
- HTML memiliki sifat statis dan bukan merupakan bahasa pemrograman
- Tools yang dibutuhkan : Browser dan Code Editor
- Visual Studio Code merupakan salah satu code editor yang dikembangkan oleh Microsoft
- Keunggulan dari Visual Studio Code, yaitu dapat digunakan di Windows, Mac, dan juga Linux.
- Struktur HTML : 

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Belajar HTML</title>
    <link rel="stylesheet" href="test.css" />
  </head>
  <body></body>
</html>

- HTML Element : Opening tag, Content, dan Closing tag
- HTML attribute merupakan properties dari HTML Element (id, class)
- HTML Comment berfungsi untuk memberikan penjelasan line dari code yang kita kerjakan (<!-- -->)
- Terdapat Single tag dan Double tag pada HTML (Single tag : <br>, Double tag : <h2> </h2>)
- Untuk menampilkan file HTML secara live kita bisa menginstall extension bernama "Live Server" pada Visual Studio Code
- Semantic HTML yaitu menggunakan elemen HTML sesuai kebutuhan konten seperti header, footer, dan nav
- Contoh penggunaan Semantic HTML tag : 

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Belajar HTML</title>
    <link rel="stylesheet" href="test.css" />
  </head>
  <body>
    <nav>
      <ul>
        <li><a href="">Home</a></li>
        <li><a href="">Shop</a></li>
        <li><a href="">About</a></li>
      </ul>
    </nav>
    <script src="script.js"></script>
  </body>
</html>

- Kita bisa menggunakan Netlify untuk melakukan deploy HTML yang sudah kita buat agar bisa diakses oleh semua orang

## D. CSS
- CSS (Cascading Style Sheets) berfungsi untuk mendesain sebuah halaman website.
- kita bisa mengubah warna, menggunakan font custom, editing text format, dan mengatur tata letak dengan menggunakan CSS
- Struktur CSS, yaitu :

.ElementHTML {
  property: value;
}

- CSS Comment memiliki fungsi yang sama dengan HTML Comment yaitu untuk memberikan penjelasan line dari code yang kita kerjakan (/* */)
- Terdapat 3 cara penggunaan CSS :
  a. Inline Style : menambahkan CSS pada attribute element HTML
  b. Internal Style : menggunakan tag style di bagian head
  c. External Style : menggunakan file css terpisah dengan html
- . / titik : merupakan selector untuk tag html yang memiliki properti class
- Contoh properti pada CSS : color, background-color
- Cara menghubungkan / mengakses file CSS pada HTML

<link rel="stylesheet" href="contoh.css" />

- CSS - Tag Name : Kita bisa menggunakan Tag Elemen HTML secara langsung pada CSS dan elemen tersebut akan bersifat global (mempengaruhi seluruh Tag Elemen HTML yang ada pada file tersebut)

h1 {
  color: red;
}

- CSS - Class Name : Kita bisa menggunakan attribute class pada elemen HTML lalu memanggil nama class tersebut pada CSS (class yang sama akan mempunyai styling yang sama saat digunakan pada CSS)

.contoh {
  color: red;
}

- CSS - ID Name : Berbeda dengan Class Name. ID Name bersifat unik artinya hanya ada 1 nama ID pada 1 element HTML.

#navigation {
  display: inline;
}

- Perbedaan antara ID dan Class adalah ID Name digunakan  jika hanya ada 1 elemen pada file/halaman HTML seperti header dan footer. Sedangkan Class Name digunakan ika akan ada beberapa element HTML yang memiliki styling/desain yang sama.
- Nested element : Parent and Child (konsep pada css)
- Multiple selector digunakan agar codingan kita semakin efisien dan tidak berulang ulang

Sebelum :
h1 {
    color: brown;
    font-family: 'Courier New', Courier, monospace;
}

p {
    font-family: 'Courier New', Courier, monospace;
}

Sesudah ;
h1 {
  color: brown;
}

h1, p {
  font-family: "Courier New", Courier, monospace;
}

**FLEXBOX**
- FlexFlexbox merupakan cara untuk mengatur layout serta dapat menyesuaikan layout secara otomatis.
- Flexbox memiliki 1 parent dan beberapa child
- flex-direction digunakan untuk mengatur letak item child.
- flex-wrap digunakan untuk membatasi jumlah item children dalam 1 line
- flex-flow digunakan sebagai shortcut untuk set up flex-direction dan flex-wrap bersamaan.
- Properti order berfungsi untuk ordering item mana yang ingin kita atur posisinya berdasarkan urutan order.
- justify-content digunakan untuk mengatur tata letak dan space antar item child secara horizontal 
- align-items digunakan untuk mengatur align dari item child secara vertikal 
- align-self digunakan untuk mengatur align item pada masing-masing item.
- flex-grow dapat mengatur size suatu item child pada flexbox.
- flex-shrink adalah properti yang membuat size suatu item child mengecil secara relatif terhadap item child lainnya.
- flex-basis adalah properti yang sama fungsinya seperti width yaitu mengatur width dari setiap item child

## E. Algoritma & Pseudocode
- Algoritma merupakan proses menyelsaikan suatu masalah yang dilakukan secara logis dan sistematis
- Belajar algoritma sama dengan mengingat kembali alur berfikir yang terstruktur
- Mempelajari algoritma merupakan hal penting di dalam dunia programming
- Ciri-ciri algoritma : Input, Output, Definiteness (pasti), Finiteness (memiliki batas), dan Effectiveness (tepat dan efisien)
- Perbedaan antara algoritma dan data struktur yaitu data struktur berfungsi untuk mengatur / mengelola suatu data, sedangkan algoritma berfungsi menyelesaikan masalah menggunakan data-data tersebut
- Contoh algoritma secara deskriptif :

1. Apakah kamu haus?
2. Jika ya, minum lalu ke no 4
3. Jika tidak, tidak perlu minum lalu ke no 4
4. Selesai

- Pseudocode merupakan penulisan algoritma sebelum kita implementasikan ke bahasa pemograman tertentu.
- Panduan menulis pseudocode :

1. Menggunakan huruf besar pada kata kunci. 
2. 1 statement terdiri dari 1 baris 
3. Gunakan indentasi
4. Spesifik dan simpel

- Contoh pseudocode :

Deklarasi
Var sisi,keliling: integer; 
Implementasi
Read(sisi);
Keliling = sisi*4;
Write(keliling);

- Jenis-jenis pseudocode :
a. Procedural : Berpikir secara runtut
b. Conditional : Percabangan kasus (if else)
c. Looping : Proses yang sama berulang-ulang (for, while)
d. Recursive : Algoritma yang memanggil method / function

## F. Javascript
- Javascript adalah bahasa pemrograman yang digunakan untuk membuat website menjadi interaktif dan dinamis
- Pada Javascript terdapat syntax dan statement. Syntax itu seperti kosa kata pada bahasa pemrograman.
- Contoh Syntax pada javascript : Alert(), Confirm().
- Untuk cek logic pemrograman atau melakukan debugging pada Javascript, kita dapat menggunakan Console.log
- Comments adalah syntax yang digunakan untuk memberikan keterangan terhadap suatu statement. Comments tidak akan dijalankan oleh program.

**Tipe Data**
- Tipe data merupakan klasifikasi untuk membedakan berbagai macam data yang digunakan dalam programming.
- Ada 6 tipe data fundamental pada Javascipt: string, number, boolean, null, undefined, object.
- string : tipe data yang didalamnya terdapat kumpulan karakter berupa huruf, angka, spasi, simbol, dan lainnya.
- number : tipe data yang mengandung semua angka termasuk angka desimal.
- boolean : tipe data yang memiliki 2 nilai yaitu TRUE(benar) atau FALSE(salah).
- null : tipe data yang berarti sebuah variabel/data tidak memiliki nilai.
- undefined : tipe data yang merepresentasikan variabel/data yang tidak memiliki nilai (biasanya ditemukan ketika eror).
- object : tipe data yang memiliki koleksi data yang saling berhubungan. tipe data object dapat menyimpan data dengan tipe data apapun seperti string, number, boolean, dan lainnya.

**Variabel**
- Variabel merupakan wadah/tempat untuk menyimpan sebuah nilai pada bahasa pemrograman.
- Hal yang dapat dilakukan pada variabel
1. Membuat variabel dengan nama yang jelas dan menggambarkan tentang data tersebut.
2. Menyimpan dan mengupdate informasi/data yang disimpan.
3. Mendapatkan/menampilkan data yang tersimpan.

- 3 Cara untuk mendefinisikan variabel
1. var
2. let : versi javascript terbaru ES6. Variabel let mendukung kaidah global variabel dan local variabel. let dapat diberi nilai yang baru nantinya.
3. const : digunakan jika variabel tidak dapat diubah nilainya. contoh phi = 3.14

- Aturan penamaan variabel
1. Harus mendeskripsikan tantang data yang disimpan.
2. tidak bisa menggunakan number pad awal nama variabel.
3. Gunakan camelCase untuk penamaan yang lebih dari satu kata. contoh : makananKesukakan, namaSaya.

**Operator**
- Assignment operator : digunakan untuk menyimpan sebuah nilai pada variabel.
- Mahematical Assignment operator : digunakan untuk operasi matematika dengan tipe data number.
- Increment dan Decrement : digunakan untuk menambah atau mengurangi sebesar 1 nilai.
- Arithmetic operator : digunakan untuk melakukan operasi matematika.
- Comparison Operator : digunakan untuk membandingkan satu nilai dengan nilai lainnya. Hasil comparison akan berupa true atau false.
- Logical opeartor : digunakan untuk sebuah conditional pada pemrograman yang menghasilkan nilai boolean yaitu true atau false.
- terdapat beberapa symbol dari logical operator
- AND(&&) : menghasilkan nilai true jika kedua nilai atau semua premis bernilai TRUE.
- OR(||) : menghasilkan nilai true jika salah satu premis mengandung nilai TRUE.
- NOT(!) : mengembalikan sebulah nilai boolean dari TRUE menjadi FALSE atau sebaliknya.

**Conditional**
- Conditional merupakan statement percabangan yang menggambarkan suatu kondisi. 
- Conditional statement akan mengecek kondisi dan menjalankan perintah berdasarkan kondisi yang telah diberikan.
- Jika kondisi bernilai TRUE, maka code di dalam kondisi tersebut akan dijalankan.

- Ada beberapa conditional
1. IF Statement
  let nilai = 10;
  if (nilai === 10) {
    console.log("Variabel nilai yang dimasukkan adalah benar 10");
  }

2. IF...ELSE Statement
- else akan mengeksekusi ketika statement pada suatu kondisi bernilai FALSE.
  let ngantuk = false;
  if (ngantuk) {
    console.log("Pergi tidur");
  } else {
    console.log("Tidak tidur");
  }

3. IF...ELSE IF... Statement
- else...if statement digunakan jika mempunyai berbagai kondisi.
  let lampu = "kuning";
  if (lampu === "merah") {
    console.log("Berhenti!");
  } else if (lampu === "kuning") {
    console.log("Pelan-pelan");
  } else if (lampu === "hijau") {
    console.log("Jalan!");
  } else {
    console.log("Hati-hati, tidak dikenal");
  }

4. Switch Case Conditional
- Switch case digunakan jika kondisi dan percabangan terlalu banyak.
  let tekanTombol = 1;
  switch(tekanTombol) {
    case 1:
      console.log("Matikan TV"); 
      break;
    case 2:
      console.log("Tingkatkan volume TV"); 
      break;
    case 3:
      console.log("Turunkan volume TV"); 
      break;
    case 4:
      console.log("Matikan suara TV"); 
      break;
    default:
      console.log("Tidak terjadi apa-apa"); 
      break;
  }

**Looping**
- Looping adalah statement yang mengulang sebuah instruksi hingga kondisi terpenuhi atau jika kondisi berhenti tercapai.
  
- Ada beberapa looping
1. Manual Looping
  console.log(1);
  console.log(2);
  console.log(3);
  console.log(4);
  console.log(5);
  // akan menampilkan nilai 1-5

2. For Loop
- for loop digunakan ketika kita tahu seberapa banyak nilai pasti untuk mengulangnya.
  let angka = 1;
  for (angka; angka <= 10; angka++) {
    console.log(angka);
  }
  // akan menampilkan angka 1-10

3. While Loop
- while loop akan menjalankan instruksi jika pengulangan kondisi bernilai true.
- digunakan ketika kita tidak mengetahui jumlah pasti pengulangan.
  let angka = 1;
  while (angka <= 10) {
    console.log(angka);
    angka++;
  }
  // akan menampilkan angka 1-10

4. Do While Loop
- digunakan ketika kita ingin setidaknya menjalankan pengulangan 1 kali sebelum dilakukan pengecekan kondisi.
  let angka = 10
  do{
    console.log(angka);
    angka--;
  } while (angka > 0)
  // akan menampilkan angka 10-1

5. Nested Loop
- sesuai dengan namanya yang berarti bersarang(looping di dalam looping).
- looping yang pertama dapat dianalogikan sebagai baris.
- looping yang kedua dapat dianalogikan sebagai kolom.
  for (let i = 1; i <= 5; i++) {
    for (let j = 1; j <= i; j++) {
      document.write("<br/>");
      document.write("baris", + i);
      document.write("<br/>");
      document.write("kolom" + j);
    }
  }
  // akan menampilkan 5 baris dan 5 kolom