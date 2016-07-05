Dasar HTML
===========

Pengertian Tag dalam HTML
----------------------------

Sebagai sebuah bahasa markup, HTML membutuhkan cara untuk memberitahu
web browser untuk apa fungsi sebuah text. Apakah text itu ditulis
sebagai sebuah paragraf, list, atau sebagai link? Dalam HTML, tanda ini
dikenal dengan istilah tag.

Hampir semua tag di dalam HTML ditulis secara berpasangan, yakni tag
pembuka dan tag penutup, dimana objek yang dikenai perintah tag berada
di antara tag pembuka dan tag penutup ini. Objek disini dapat berupa
text, gambar, maupun video. Penulisan tag berada di antara dua kurung
siku: “&lt;” dan “&gt;”.

Berikut adalah format dasar penulisan tag HTML:

```html
<tag_pembuka>objek yang dikenai perintah tag </tag_penutup>
```

Sebagai contoh, perhatikan kode HTML berikut :

&lt;p&gt; Ini adalah sebuah paragraf &lt;/p&gt; &lt;p&gt; adalah tag
pembuka, dalam contoh ini p adalah tag untuk paragraf. &lt;/p&gt; adalah
tag penutup paragraf. Perbedaannya dengan tag pembuka terletak dari
tanda backslash(/) Jika kita lupa memberikan penutup tag, umumnya
browser akan “memaafkan” hal ini dan tetap menampilkan hasilnya
seolah-olah kita menuliskan tag penutup. Walaupun hal ini memudahkan
kita, namun tidak disarankan.

Contohnya lainnya, jika kita ingin membuat suatu text dalam sebuah
paragraf di tulis tebal atau miring, di dalam HTML dapat ditulis sebagai
berikut:

```html
<p>Ini adalah sebuah paragraf. <i>Hanya kumpulan beberapa kalimat</i>. 
Paragraf ini terdiri dari <b>3 kalimat</b></p>.
```

Hasil dari kode HTML diatas, diterjemahkan oleh browser menjadi:

“Ini adalah sebuah paragraf. Tidak lain dari kumpulan beberapa kalimat.
Paragraf ini terdiri dari 3 kalimat.”

Tag &lt;i&gt; pada kode HTML diatas memberikan perintah kepada browser
untuk menampilkan text secara garis miring (i, singkatan dari italic),
dan tag &lt;b&gt; untuk menebalkan tulisan (b, singkatan dari bold).

Terdapat pengecualian beberapa tag yang tidak berpasangan, seperti
&lt;br&gt; untuk break (pindah baris) atau &lt;hr&gt; untuk horizontal
line (garis horizontal). Tag ini dikenal juga dengan sebutan self
closing tag atau void tag, untuk penulisannya bisa ditulis dengan
&lt;br&gt;, maupun &lt;br /&gt;.

HTML tidak case-sensitif, dalam artian penulisan &lt;p&gt; dianggap sama
dengan &lt;P&gt;. Pada awal kemunculan HTML, programmer web umumnya
menggunakan huruf besar untuk seluruh tag agar membedakan dengan text
yang berupa isi dari web. Namun varian HTML, xHTML mewajibkan huruf
kecil untuk semua tag.

Dalam HTML5, aturan ini kembali tidak diharuskan. Akan tetapi kebiasaan
web programmer saat ini adalah menggunakan huruf kecil untuk seluruh
tag.

Pengertian Elemen dalam HTML
------------------------------

Elemen adalah isi dari tag yang berada diantara tag pembuka dan tag
penutup. Sebagai contoh, berikut adalah kode HTML:

```html
<p> Ini adalah sebuah paragraf </p>
```

Pada contoh diatas, “Ini adalah sebuah paragraf” merupakan elemen dari
tag &lt;p&gt;.

Elemen tidak hanya berisi text, namun juga bisa tag lain.

Contoh elemen:

```html
    <p> Ini adalah sebuah <em>paragraf</em> </p>
```

Dari contoh diatas, Ini adalah sebuah &lt;em&gt;paragraf&lt;/em&gt;
merupakan elemen dari tag &lt;p&gt;.

Pengertian Atribut dalam HTML
-----------------------------

Atribut adalah informasi tambahan yang diberikan kepada tag. Informasi
ini bisa berupa instruksi untuk warna dari text, besar huruf dari text,
dll. Setiap atribut memiliki pasangan nama dan nilai (value), dan
ditulis dengan name=”value”. Value diapit tanda kutip, boleh menggunakan
tanda kutip satu (‘) atau dua (“).

Contoh kode HTML:

```html
    <a href="http://www.duniailkom.com">ini adalah sebuah link</a>
```

Pada kode HTML diatas, href=”http://www.duniailkom.com” adalah atribut.
href merupakan nama dari atribut, dan http://www.duniailkom.com adalah
value atau nilai dari atribut tersebut.

Tidak semua tag membutuhkan atribut, tapi anda akan sering melihat
sebuah tag dengan atribut, terutama atribut id dan class yang sering
digunakan untuk manipulasi halaman web menggunakan CSS maupun
JavaScript.

HTML memiliki banyak atribut yang beberapa diantaranya hanya cocok untuk
tag tertentu saja. Sebagai contoh, atribut “href” diatas hanya digunakan
untuk tag &lt;a&gt; saja (dan beberapa tag lain). Penjelasan tentang
tujuan dan pengertian dari atribut seperti href ini akan kita bahas pada
tutorial-tutorial selanjutnya.

Struktur Dasar HTML
--------------------

Setiap halaman HTML setidaknya memiliki struktur dasar yang terdiri dari
: Tag DTD atau DOCTYPE, tag html, tag head, dan tag body. Inilah yang
merupakan struktur paling dasar dari HTML, walaupun HTML tidak hanya
berisi struktur tersebut.

Agar lebih mudah memahaminya, silahkan buka text editor (Notepad++),
lalu ketikkan kode berikut ini:

Contoh struktur dasar HTML:

```html
    <!DOCTYPE html>
    <html>
    <head>
    <title>Title dari Websiteku</title>
    </head>
    <body>
    <p>Selamat Pagi Dunia, Hello World!</p>
    </body>
    </html>
```

Save sebagai halaman.html dan jalankan file dengan cara double klik file
tersebut, atau klik kanan –&gt; Open With –&gt; Firefox. Kita akan
membahas tag-tag yang ditulis tersebut pada toturial kali ini.

## Mengenal Struktur Dasar HTML

### Pengertian DTD atau DOCTYPE


Tag paling awal dari contoh HTML diatas adalah DTD atau DOCTYPE. DTD
adalah singkatan dari Document Type Declaration. Yang berfungsi untuk
memberi tahu kepada web browser bahwa dokumen yang akan diproses adalah
HTML.

DTD memiliki banyak versi tergantung kepada versi HTML yang kita
gunakan. Pada contoh diatas, kita menggunakan DTD versi HTML 5. Sebelum
HTML 5, DTD terdiri dari text panjang yang hampir mustahil dihafal.
Contohnya, DTD untuk xHTML 1.0 adalah:

&lt;!DOCTYPE html PUBLIC “-//W3C//DTD XHTML 1.0 Strict//EN”
“http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd”&gt; Jika kita tidak
menuliskan DTD, browser akan tetap menampilkan dan memproses halaman web
kita seperti tidak terjadi apa-apa. Namun browser sebenarnya menjalankan
halaman HTML tersebut pada mode khusus yang disebut quirk mode. Pada
quirk mode ini, web browser menerjemahkan halaman web dan terutama CSS
sedikit berbeda dari seharusnya. Hal ini karena web browser menganggap
jika tidak ada DTD, maka halaman tersebut kemungkinan adalah halaman web
usang, dan menggunakan aturan-aturan yang berbeda agar dapat
ditampilkan.

Cara untuk mengetahui apakah web browser berjalan pada quirk mode atau
standard mode : Pada Firefox, klik kanan pada halaman web, lalu pilih
Page Info. Pada bagian Render Mode akan terlihat apakah quirk mode, atau
standard mode.

### Perbedaan quirk mode dan standard mode HTML

Penjelasan lebih jauh tentang doctype atau DTD akan kita bahas dalam
tutorial HTML5: Pengertian dan cara penulisan doctype pada HTML5.

### Tag &lt;html&gt;


Setelah DTD, tag berikutnya adalah tag &lt;html&gt;.

Ini adalah tag pembuka dari keseluruhan halaman web. Semua kode HTML
akan berada di dalam tag ini. Tag html dimulai dengan &lt;html&gt; dan
diakhiri dengan &lt;/html&gt;

### Tag &lt;head&gt;


Elemen pada tag &lt;head&gt; umumnya akan berisi berbagai definisi
halaman, seperti kode CSS, JavaScript, dan kode-kode lainnya yang tidak
tampil di browser.

### Tag &lt;title&gt;


dalam contoh kita digunakan untuk menampilkan title dari sebuah halaman
web, dan biasanya ditampilkan pada bagian paling atas web browser.
Contohnya pada tampilan halaman.html, ‘Title dari Websiteku’ akan
ditampilkan pada tab browser.

### Tag &lt;body&gt;


Tag &lt;body&gt; akan berisi semua elemen yang akan tampil dalam halaman
web, seperti paragraf, tabel, link, gambar, dll. Tag body ini ditutup
dengan &lt;/body&gt;. Sebagian besar waktu kita dalam merancang web
adalah di dalam tag &lt;body&gt; ini.

Perhatikan bahwa setiap tag akan diakhiri dengan penutup tag. Termasuk
&lt;html&gt; yang merupakan tag paling awal dari sebuah halaman web.

Stuktur HTML yang kita bahas disini adalah struktur sangat sederhana.
Sebuah halaman web bisa memiliki ratusan bahkan ribuan baris, dan
menggunakan berbagai tag HTML.
