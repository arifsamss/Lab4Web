# Pemograman Web
~~~
Nama  : Arif Samsudin
NIM   : 311910255
Kelas : TI 19 C1
~~~
# 1.Membuat dokumen HTML
Persiapan membuat dokumen HTML dengan nama file lab4_box.html seperti berikut.
~~~
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Box Element</title>
</head>
<body>
<header>
<h1>Box Element</h1>
</header>
</body>
</html>
~~~
![1  Persiapan](https://user-images.githubusercontent.com/81839328/115941725-d47c4980-a4d0-11eb-8859-f8b22d1acc30.JPG)
# 2. Membuat Box Element
Kemudian tambahkan kode untuk membuat box element dengan tag div seperti berikut.
~~~
<section>
<div class="div1">Div 1</div>
<div class="div2">Div 2</div>
<div class="div3">Div 3</div>
</section>
~~~
![2  Membuat box elemen](https://user-images.githubusercontent.com/81839328/115941786-1c02d580-a4d1-11eb-9aec-b1c43b730ef4.JPG)
# 3. CSS Float Property
Selanjutnya tambahkan deklarasi CSS pada head untuk membuat float element, seperti berikut.
~~~
<style>
div {
float:left;
padding: 10px;
}
.div1 {
background: red;
}
.div2 {
background: yellow;
}
.div3 {
background: green;
}
</style>
~~~
![3  Menambahkan CSS](https://user-images.githubusercontent.com/81839328/115941871-916ea600-a4d1-11eb-9a93-1b9b2c1d202e.JPG)
# 4. Mengatur Clearfix Element
Clearfix digunakan untuk mengatur element setelah float element. Property clear digunakan untuk mengaturnya.
Tambahkan element div lainnya seteleah div3 seperti berikut.
~~~
<section>
<div class="div1">Div 1</div>
<div class="div2">Div 2</div>
<div class="div3">Div 3</div>
<div class="div4">Div 4</div>
</section>
~~~
Kemudian atur property clear pada CSS, seperti berikut.
~~~
.div4 {
background-color: blue;
clear: left;
float: none;
}
~~~
![4  Mengatur Clearfix Element](https://user-images.githubusercontent.com/81839328/115941968-f2967980-a4d1-11eb-82cb-2b0faafe05b9.JPG)
Lakukan eksperimen terhadap penggunaan property clear dengan nilai lainnya (left, both, right), dan amati perubahannya.
# 5. Membuat Layout Sederhana
Kita akan membuat layout web sederhana seperti gambar berikut.

![5 1](https://user-images.githubusercontent.com/81839328/115942045-5d47b500-a4d2-11eb-8dee-607ed2d4adc1.JPG)

Buat folder baru dengan nama lab4_layout, kemudian buatlah file baru didalamnya dengan nama home.html, dan file css dengan nama style.css.
~~~
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Layout Sederhana</title>
<link rel="stylesheet" href="style.css">
</head>
<body>
<div id="container">
</div>
</body>
</html>
~~~
Kemudian buat kerangka layout dengan semantics element seperti berikut.

![5 2](https://user-images.githubusercontent.com/81839328/115942093-a7c93180-a4d2-11eb-8664-cbe45f8dd0e7.JPG)

Kemudian tulis kode berikut.
~~~
<header>
<h1>Layout Sederhana</h1>
</header>
<nav>
<a href="home.html" class="active">Home</a>
<a href="artikel.html">Artikel</a>
<a href="about.html">About</a>
<a href="kontak.html">Kontak</a>
</nav>
<section id="hero"></section>
<section id="wrapper">
<section id="main"></section>
<aside id="sidebar"></aside>
</section>
<footer>
<p>&copy; 2021 - Universitas Pelita Bangsa</p>
</footer>
~~~
![5  Membuat Layout Sederhana](https://user-images.githubusercontent.com/81839328/115942151-055d7e00-a4d3-11eb-9294-9eb3081905fb.JPG)
Kemudian tambahkan kode CSS untuk membuat layoutnya.
~~~
/* import google font */
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400
;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap');
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0
,300;0,700;1,300&display=swap');
/* Reset CSS */
* {
margin: 0;
padding: 0;
}
body {
line-height:1;
font-size:100%;
font-family:'Open Sans', sans-serif;
color:#5a5a5a;
}
#container {
width: 980px;
margin: 0 auto;
box-shadow: 0 0 1em #cccccc;
}
/* header */
header {
padding: 20px;
}
header h1 {
margin: 20px 10px;
color: #b5b5b5;
}
~~~
![6  Manambahkan CSS](https://user-images.githubusercontent.com/81839328/115942198-38077680-a4d3-11eb-90a2-2df00597040f.JPG)
# 6. Membuat Navigasi
Kemudian selanjutnya mengatur navigasi.
~~~
/* navigasi */
nav {
display: block;
background-color: #1f5faa;
}
nav a {
padding: 15px 30px;
display: inline-block;
color: #ffffff;
font-size: 14px;
text-decoration: none;
font-weight: bold;
}
nav a.active,
nav a:hover {
background-color: #2b83ea;
}
~~~
![7  Mengatur Navigasi](https://user-images.githubusercontent.com/81839328/115942227-62593400-a4d3-11eb-8f37-4400bfa370cd.JPG)
# 7. Membuat Hero Panel.
Selanjutnya membuat hero panel. Tambahkan kode HTML dan CSS seperti berikut.
~~~
<section id="hero">
<h1>Hello World!</h1>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
pretium ac.</p>
<a href="home.html" class="btn btn-large">Learn more &raquo;</a>
</section>
~~~
~~~
/* Hero Panel */
#hero {
background-color: #e4e4e5;
padding: 50px 20px;
margin-bottom: 20px;
}
#hero h1 {
margin-bottom: 20px;
font-size: 35px;
}
#hero p {
margin-bottom: 20px;
font-size: 18px;
line-height: 25px;
}
~~~
![8 1 Menambahkan section Hero](https://user-images.githubusercontent.com/81839328/115942282-a5b3a280-a4d3-11eb-8993-492e8775cf89.JPG)
![8 2 Hasil](https://user-images.githubusercontent.com/81839328/115942289-ab10ed00-a4d3-11eb-9b94-7337aa021ee7.JPG)
# 8. Mengatur Layout Main dan Sidebar
Selanjutnya mengatur main content dan sidebar, tambahkan CSS float.
~~~
/* main content */
#wrapper {
margin: 0;
}
#main {
float: left;
width: 640px;
padding: 20px;
}
/* sidebar area */
#sidebar {
float: left;
width: 260px;
padding: 20px;
}
~~~
![9  Mengatur layout main dan sidebar](https://user-images.githubusercontent.com/81839328/115942326-e3183000-a4d3-11eb-8ed8-28f923ab20c4.JPG)
# 9. Membuat Sidebar Widget
Kemudian selanjutnya menambahkan element lain dalam sidebar.
~~~
<aside id="sidebar">
<div class="widget-box">
<h3 class="title">Widget Header</h3>
<ul>
<li><a href="#">Widget Link</a></li>
<li><a href="#">Widget Link</a></li>
<li><a href="#">Widget Link</a></li>
<li><a href="#">Widget Link</a></li>
<li><a href="#">Widget Link</a></li>
</ul>
</div>
<div class="widget-box">
<h3 class="title">Widget Text</h3>
<p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt
arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer
pharetra est nunc, nec pretium nunc pretium ac.</p>
</div>
</aside>
~~~
Kemudian tambahkan CSS.
~~~
/* widget */
.widget-box {
border:1px solid #eee;
margin-bottom:20px;
}
.widget-box .title {
padding:10px 16px;
background-color:#428bca;
color:#fff;
}
.widget-box ul {
list-style-type:none;
}
.widget-box li {
border-bottom:1px solid #eee;
}
.widget-box li a {
padding:10px 16px;
color:#333;
display:block;
text-decoration:none;
}
.widget-box li:hover a {
background-color:#eee;
}
.widget-box p {
padding:15px;
line-height:25px;
}
~~~
![10 1 Menambahkan sidebar widget](https://user-images.githubusercontent.com/81839328/115942362-22df1780-a4d4-11eb-8267-e74a43711a4d.JPG)
![10 2 Hasil](https://user-images.githubusercontent.com/81839328/115942363-25417180-a4d4-11eb-9c85-05bf157f1c3e.JPG)
# 10. Mengatur Footer
Selanjutnya mengatur tampilan footer. Tambahkan CSS untuk footer.
~~~
/* footer */
footer {
clear:both;
background-color:#1d1d1d;
padding:20px;
color:#eee;
}
~~~
![11  Mengatur Footer](https://user-images.githubusercontent.com/81839328/115942455-93863400-a4d4-11eb-9d80-31acbc614677.JPG)
# 11. Menambahkan Elemen lainnya pada Main Content
~~~
<section id="main">
<div class="row">
<div class="box">
<img src="https://dummyimage.com/120/db7d25/fff.png" alt=""
class="image-circle">
<h3>Heading</h3>
<p>Donec sed odio dui. Etiam porta sem malesuada magna mollis
euismod.</p>
<a href="#" class="btn btn-default">View detail</a>
</div>
<div class="box">
<img src="https://dummyimage.com/120/3e73e6/fff.png" alt=""
class="image-circle">
<h3>Heading</h3>
<p>Donec sed odio dui. Etiam porta sem malesuada magna mollis
euismod.</p>
<a href="#" class="btn btn-default">View detail</a>
</div>
<div class="box">
<img src="https://dummyimage.com/120/71e6d4/fff.png" alt=""
class="image-circle">
<h3>Heading</h3>
<p>Donec sed odio dui. Etiam porta sem malesuada magna mollis
euismod.</p>
<a href="#" class="btn btn-default">View detail</a>
</div>
</div>
</section>
~~~
Kemudian tambahkan CSS.
~~~
/* box */
.box {
display:block;
float:left;
width:33.333333%;
box-sizing:border-box;
-moz-box-sizing:border-box;
-webkit-box-sizing:border-box;
padding:0 10px;
text-align:center;
}
.box h3 {
margin: 15px 0;
}
.box p {
line-height: 20px;
font-size: 14px;
margin-bottom: 15px;
}
box img {
border: 0;
vertical-align: middle;
}
.image-circle {
border-radius: 50%;
}
.row {
margin: 0 -10px;
box-sizing: border-box;
-moz-box-sizing: border-box;
-webkit-box-sizing: border-box;
}
.row:after, .row:before,
.entry:after, .entry:before {
content:'';
display:table;
}
.row:after,
.entry:after {
clear:both;
}
~~~
![12  Menambahkan main content](https://user-images.githubusercontent.com/81839328/115942542-f4ae0780-a4d4-11eb-9574-2bfba6d67ad7.JPG)
![12 2 Hasil](https://user-images.githubusercontent.com/81839328/115942544-f7106180-a4d4-11eb-99ac-67a622c04969.JPG)
# 12. Menambahkan Content Artikel
Selanjutnya membuat content artikel. Tambahkan HTML berikut pada main content.
~~~
<hr class="divider" />
<article class="entry">
<h2>First featurette heading.</h2>
<img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
pretium ac.</p>
</article>
<hr class="divider" />
<article class="entry">
<h2>First featurette heading.</h2>
<img src="https://dummyimage.com/150/7b8a70/fff.png" alt=""
class="right-img">
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
pretium ac.</p>
</article>
~~~
Kemudian tambahkan CSS.
~~~
.divider {
border:0;
border-top:1px solid #eeeeee;
margin:40px 0;
}
/* entry */
.entry {
margin: 15px 0;
}
.entry h2 {
margin-bottom: 20px;
}
.entry p {
line-height: 25px;
}
.entry img {
float: left;
border-radius: 5px;
margin-right: 15px;
}
.entry .right-img {
float: right;
}
~~~
![13 1 Menambahkam main content](https://user-images.githubusercontent.com/81839328/115942632-5cfce900-a4d5-11eb-92a0-47aeca437e79.JPG)
![13 2 Hasil](https://user-images.githubusercontent.com/81839328/115942633-5f5f4300-a4d5-11eb-9de4-e479c42fafcf.JPG)
# Pertanyaan dan Tugas
1. Tambahkan Layout untuk menu About

=> buat single layout yang berisi deskripsi, portfolio, dll

![Pertanyaan 1](https://user-images.githubusercontent.com/81839328/115944062-def11000-a4dd-11eb-9e9a-6d3449f511e5.JPG)

2. Tambahkan layout untuk menu Contact

=> yang berisi form isian: nama, email, message, dll



