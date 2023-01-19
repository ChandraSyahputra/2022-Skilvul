**Scope**
- scope merupakan konsep dalam flow data variabel
- digunakan untuk menentukan suatu variabel bisa diakses pada scope tertentu atau tidak.

1. Blocks
- blocks adalah code yang berada di dalam curly braces {}.
- blocks dapat digunakan dalam conditional, function, dan looping.

2. Global Scope
- artinya variabel yang dibuat dapat diakses di manapun dalam suatu file.
- variabel harus dideklarasikan diluar Blocks agar dapat menjadi Global Scope.

  let namaSaya = "chandra";
  function greeting() {
    return namaSaya;
  }
  console.log(namaSaya);
  // menampilkan chandra

3. Local Scope
- artinya kita mendeklarasikan variabel di dalam sebuah blocks seperti conditional, function, dan looping.
- variabel hanya bisa diakses di dalam blocks saya. Tidak bisa diakses diluar blocks.

  function greeting() {
    let namaSaya = "chandra";
    return namaSaya;
  }

  console.log(greeting()); // menampilkan chandra
  console.log(namaSaya); // akan eror karena variabel nama saya merupakan local scope

**Fucntion**
- Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task/1 fitur.
- Jika kita membutuhkan fitur tersebut kita dapat langsung menggunakannya.

- Membuat function
  function greeting() {
    return "Hello world";
  }

- Memanggil function
  greeting() // memanggil sebuah function
  console.log(greeting()) // menampilkan output: "Hello world"

- Parameter Function
  - Dengan parameter, function dapat menerima sebuah inputan data dan menggunakannya untuk melakukan task/tugas.
  - Saat membuat function/fitur, kita harus tahu data-data yang dibutuhkan. Misalnya saat membuat function penambahan 2 buah nilai. Data yang dibutuhkan adalah 2 buah nilai tersebut.

  function penambahan(a, b) {
    return a + b;
  }

- Argumen Function
  - Argumen adalah nilai yang digunakan saat memanggil function.
  - Jumlah argumen harus sama dengan jumlah parameternya
  - Jadi jika di function penambahan ada 2 parameter nilai saat membuat function. Saat memanggil function kita gunakan 2 buah nilai argumen.

  function penambahan(a, b) {
    return a + b;
  }

  console.log(penambahan(10, 5)) //output: 15

- Default Parameters
  Default paramaters digunakan untuk memberikan nilai awal/default pada parameter function.

  Default parameters bisa digunakan jika kita ingin menjaga function agar tidak error saat dipanggil tanpa argumen.

  function greetOnWebsite(name = "Stranger") {
    return "Hello " + name
  }

  console.log(greetOnWebsite("david")) //Output: "Hello David"
  console.log(greetOnWebsite()); //Output: "Hello Stranger"

- Function Helper
  Kita bisa menggunakan function yang sudah dibuat pada function lain.

  function multiplyByNineFifths(number) {
    return number * (9/5);
  }

  function getFahrenheit(celcius) {
    return multiplyByNineFifths(celcius) + 32;
  }

  getFahrenheit(15); returns 59

- Arrow Function
  Merupakan cara lain untuk menuliskan function

  const greeting = () => {
    return "Hello world";
  }

  const penambahan = (a, b) => {
    return a + b;
  }

**Tipe data dalam Javascript**
- *Boolean* merupakan tipe data yang memiliki nilai true / false (1 / 0)
  Boolean sering digunakan untuk memutuskan bagian kode mana yang akan dieksekusi (seperti dalam pernyataan if) atau ulangi (seperti dalam perulangan for).

- *Null* merupakan salah satu tipe data yang berarti tidak bernilai atau tidak memiliki nilai. Meskipun demikian, null tidak sama dengan string kosong.
  String kosong berarti string yang tidak terisi nilai. Jika menggunakan typeof, maka null adalah object. Ini berarti null merupakan sebuah object yang tidak memiliki nilai.

- *Undefined* merupakan sebuah hasil yang didapat dari sebuah proses.Secara mudah, undefined merupakan nilai yang sudah dideklarasi namun belum didefinisikan atau belum diberi nilai

  Jika dilihat sekilas, undefined memiliki persamaan dengan null. Namun demikian, pengertian undefined dianggap lebih dalam dari pada null. Jika null merupakan sebuah objek khusus, maka jika menggunakan typeof undefined adalah undefined.

  Beberapa proses yang akan menghasilkan undefined diantaranya adalah :
    - Proses pemanggilan variabel yang belum didefinisikan.
    - Proses pemanggilan object yang belum ada
    - Proses pemanggilan fungsi yang tidak mengembalikan nilai

- *Number* merupakan tipe data yang digunakan untuk menunjukan angka, baik positif maupun negatif.
  Tipe data number juga bisa mengeluarkan nilai NaN. Nan merupkan Not a Number, sebuah nilai hasil dari operasi matematika yang biasanya tidak valid, salah, ataupun nilai yang tidak terdefinisikan seperti hasil dari membagi dengan angka nol.

  Secara lebih spesifik, tipe data ini juga bisa dipecah menjadi dua tipe data lain yaitu integer dan float.

- *NaN*
  Tipe data JavaScript *NaN* atau Not a Number digunakan untuk merepresentasikan sebuah kesalahan. Kesalahan dalam penghitungan, hal itu terjadi karena perbedaan tipe data. Seperti halnya string dengan number. Proses aritmatika yang salah, sebuah string tidak dapat dihitung dengan numbernya.

- *BigInt* merupakan numerik dalam JavaScript yang dapat mewakili bilangan bulat dengan presisi arbitrer.
  Dengan BigInts, kita dapat dengan aman menyimpan dan mengoperasikan bilangan bulat besar bahkan di luar batas bilangan bulat aman untuk Numbers dan dapat menggunakan operator +, , -, *, dan % dengan BigInts seperti halnya dengan Numbers.

- *String* merupakan tipe data yang tidak dapat dijumlahkan. Umumnya yang berisi kata atau kalimat dan bisa juga sebuah angka. Namun tidak dapat menjumlahkannya dengan tipe data number.
  
  Penulisan tipe data dari string diawali dan diakhiri dengan tanda kutip (“). Selain itu juga bisa menggunakan tanda kutip tunggal (‘). Setiap karakter yang terbalut dengan kutip satu (‘) atau kutip dua (“). Penulisan tersebut yang dianggap sebagai string oleh JavaScript.

  Kadang anda membutuhkan kombinasi diantara keduanya. Tipe data yang satu ini biasa penggunaannya untuk memuat data. Seperti nama seseorang, nama benda, alamat dan kata atau kalimat.

- *Array*  merupakan tipe data yang digunakan untuk menyimpan banyak nilai pada satu variabel.
  Setiap nilai, atau pada tipe data ini disebut elemen akan memiliki posisi sendiri yang disebut indeks. Setiap nilai ini juga bisa berisi banyak tipe data lain. Tipe data ini biasa digunakan untuk membuat pilihan dengan banyak objek.


- *Object* merupakan sebuah variabel yang menyimpan nilai (properti) dan fungsi (method).

- *Symbol* merupakan tipe data baru setelah kehadiran ECMAScript 6 (ES6). Tipe data simbol yang digunakan sebagai pengenal properti objeknya.


**Math**
*Math* adalah objek yang berisi fungsi-fungsi matematika dan beberapa konstanta untuk melakukan perhitungan matematika seperti sin, cos, tan, eksponen, akar kuadrat, dll.

Objek Math di Javascript menyediakan fungsi sebagai berikut:
- log() untuk algoritma
- pow() untuk pemangkatan 
- exp() untuk menghitung eksponensial
- floor() membulatkan ke bawah;
- round() membulatkan ke yang terdekat, bisa ke bawah dan ke atas;
- ceil() membulatkan ke atas.
- sqrt() untuk menghitung akar
- cbrt() untuk menghitung akar kubik

**Primitive & Non-Primitive**
- Tipe data primitif memiliki sifat immutable dan tidak memiliki properties.
- Tipe data Non-primitif bersifat mutable dan memiliki properties. 

>Maksud dari immutable itu setelah pertama kali diinisiasi, nilai tersebut tidak bisa diubah lagi dalam memori. Nilai yang tersimpan dalam memori akan tetap sama seperti pertama kali

contoh tipe data primitif & Non-primitif

*Primitif*
1. Numbers
2. Strings
3. Booleans
4. Undefined
5. Null

*Non-Primitif*
1. Objects
2. Arrays

**Javascript dan HTML DOM**
- Proses rendering di balik layar
    HTML -> Parsing -> Tokens -> DOM
    CSS -> Parsing -> Tokens -> CSSOM
    DOM + CSSOM = Render Tree
    Layouting

- Terdapat isu terkait proses rendering. Jika saat proses parsing HTML, ditemukan tag <script>, secara default proses parsing akan dihentikan sampai script tersebut selesai diunduh dan dijalankan.

- Solusi dari isu terkait proses rendering
  - Solusi paling umum agar dia mulai diproses setelah parsing HTML selesai adalah menaruh tag <script> eksternal sebelum tag penutup </body>.
  - Menaruh tag <script> sedini mungkin dan gunakan atribut async. Atribut async akan membuat script tersebut diunduh tanpa menghentikan proses parsing dan dieksekusi seselesainya ia diunduh.
  - Menaruh tag <script> sedini mungkin dan gunakan atribut defer untuk script yang bergantung pada DOM. Atribut defer akan membuat script tersebut diunduh tanpa menghentikan proses parsing dan dieksekusi seselesainya proses parsing selesai.

- DOM adalah singkatan dari Document Object Model
- DOM bukan bagian dari Javascript, melainkan browser (Web API).
- Dengan adanya DOM, Javascript diberi akses untuk membuat HTML menjadi dinamis, seperti:
  a. Mengubah element HTML pada halaman website.
  b. Mengubah attribute HTML pada halaman website.
  c. Mengubah CSS style pada halaman website.
  d. Menambah dan/atau menghapus element maupun attribute HTML.
  e. Menambah HTML event seperti efek klik pada mouse, hover pada mouse, dan lain lain pada halaman website.
  f. Berinteraksi dengan semua HTML event di website.

- Pada HTML DOM, semua element HTML dari sebuah website dianggap sebagai object.
- Object element HTML pada HTML DOM juga mempunyai properti dan method atau yang lebih dikenal dengan istilah DOM Property dan DOM Method.

**Mengakses element HTML**
- getElementById (id)
  Kita dapat menggunakan getElementById untuk mengakses element HTML berdasarkan nilai id-nya.

  <!-- html -->
  <input id="umur" type="text" value="20"/>

  <!-- js -->
  let umur = document.getElementById("umur").value;

  console.log(umur); // Output: 20

- getElementsByTagName(tag)
  Kita dapat menggunakan getElementsByTagName untuk mengakses element-element HTML berdasarkan jenis tag-nya.

  <!-- html -->
  <h1 id="title">Hello, World!</h1>
  <p>Selamat Datang di Skilvul</p>
  <h1 class="subtitle">Mari Belajar JavaScript</h1>
  
  <!-- js -->
  let semuaTagH1 = document.getElementsByTagName("h1");

  console.log(semuaTagH1); // Output: HTMLCollection(2) [h1#title, h1.subtitle]
  console.log(semuaTagH1[0]); // Output: <h1 id="title">Hello, World!</h1>
  console.log(semuaTagH1[1]); // Output: <h1 class="subtitle">Mari Belajar JavaScript</h1>

- getElementsByClassName(className)
  Kita dapat menggunakan getElementsByClassName untuk mengakses element-element HTML berdasarkan nilai attribute class-nya.

  <!-- html -->
  <h1 class="header">Hello, World!</h1>
  <p>Selamat Datang di Skilvul</p>
  <span class="header">Mari Belajar JavaScript</span>

  <!-- js -->
  let semuaClassHeader = document.getElementsByClassName("header");

  console.log(semuaClassHeader); // Output: HTMLCollection(2) [h1.header, span.header]
  console.log(semuaClassHeader[0]); // Output: <h1 class="header">Hello, World!</h1>
  console.log(semuaClassHeader[1]); // Output: <span class="header">Mari Belajar JavaScript</span>

- querySelectorAll(cssSelector)
  Kita dapat menggunakan querySelectorAll untuk mengakses element-element HTML berdasarkan CSS Selector-nya HTML.

  <!-- html -->
  <h1 class="header">Hello, World!</h1>
  <p id="header2">Selamat Datang di Skilvul</p>
  <span class="header">Mari Belajar JavaScript</span>

  <!-- js -->
  let h1ClassHeader = document.querySelectorAll('h1.header');

  console.log(h1ClassHeader); // Output: NodeList [h1.header]
  console.log(h1ClassHeader[0]); // Output: <h1 class="header">Hello, World!</h1>

  let idHeader2 = document.querySelectorAll('#header2');

  console.log(idHeader2); // Output: NodeList [p#header2]
  console.log(idHeader2[0]); // Output: <p id="header2">Selamat Datang di Skilvul</p>

**DOM Event**
- DOM Event dapat digunakan agar tampilan website menjadi interaktif seperti memunculkan popup window.

- EventListener
  - EventListener - Clik
  Jika kita mempunyai element <input id=”user-input” />  dan <button id=”alert-button”>show</button>. 
  Kita ingin menampilkan pop up box yang berisi teks di dalam input tadi.
  
  // cari dulu kedua element tersebut berdasarkan id-nya
  const input = document.getElementById(“user-input”)
  const button = document.getElementById(“alert-button”)

  // baru tambahkan event listener
  button.addEventListener(“click”, function() {
      alert(input.value)
  })

  // atau
  button.onclick = function() { alert(input.value) }

  - EventListener - Blur
  “Blur”, lawan dari “focus”, adalah event di mana sebuah element kehilangan fokus dari user (misal user klk mouse di luar element tersebut atau user klik tab untuk berpindah element)

  Misalkan kita ingin memvalidasi isi dari <input id=”username” /> agar panjangnya minimal 6 karakter..

  // cari dulu element tersebut berdasarkan id-nya
  const input = document.getElementById(“username”)

  // tambahkan event listener
  input.addEventListener(“blur”, () => {
      if(input.value.length < 6) alert(“Panjang username minimal 6”)
  })

  - EventListener - Form Submission
  Misalkan kita mempunyai element beberapa input dalam sebuah form <input name=”email /> dan <input type=”password” name=”password” />. Bagaimana caranya  kita mendapatkan isi dari kedua input tersebut saat submit form?

  Pasang event listener di form, lalu gunakan FormData untuk mengambil data dari masing-masing input.

  const form = document.getElementById(“form”)

  form.addEventListener(“submit”, function(event) {
      // cegah page refresh
      event.preventDefault()

      const formData = new FormData(form)
      const values = Object.fromEntries(formData) // { email: ... }
  })