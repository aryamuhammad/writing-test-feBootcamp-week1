## Writing Test FE Bootcamp Week 1
Nama : Muhammad Arya Wirawan     
Track : Front End Web Development      
Group Track : 2      
Mentor : Thoriq Nur Faizal      

<br>

###  Intro React JS
##### Definisi
React JS adalah framework view library javascript untuk membuat tampilan (UI) pada website. React JS merupakan framework component based. Component Based memungkinkan kita untuk membuat secara terpisah tiap komponen dan dapat digunakan pada banyak section.     
React JS dapat membuat website menjadi Single Page Application (SPA). SPA hanya memiliki 1 file HTML. SPA membuat website kita tidak merefresh halamannya ketika kita berpindah halaman / merequest sesuatu.
##### Instalasi React JS
Untuk dapat menggunakan React JS, kita harus menginstallnya terlebih dahulu. Langkah-langkah menginstall react js:
- Download dan Install Node JS
  Dengan menggunakan Node JS, Javascript dapat digunakan di luar browser
- Buka Gitbash, lalu ketik
  ```
  npx create-react-app [nama-fie-react]
  ```
- Setelah itu tunggu prosesnya sampai selesai.

##### Virtual DOM
Virtual DOM merupakan replika dari suatu DOM yang sebenarnya. Untuk mengubah DOM asli menggunakan react diperlukan perantara. Perantara tersebut adalah virtual DOM. Ketika terjadi update pada suatu komponen, maka React JS hanya melalukan render ulang pada komponen tersebut saja, tidak melakukan update pada seluruh DOM.

#### Struktur folder React JS
![](asset/basic-react-struc.png)
Source: [medium] (https://medium.com/swlh/demystifying-the-folder-structure-of-a-react-app-c60b29d90836) 

Gambar diatas merupakan gambaran struktur file ketika kita menggunakan React JS. React JS hanya memiliki 1 file index.html yang berada pada folder public.     


Untuk melakukan explorasi, dapat kita lakukan pada folder src.  Terdapat 1 file utama yaitu index.js     

Ketika kita akan melakukan penambahan elemen atau component untuk website kita, untuk menampilkannya kita dapat memanggilnya pada file app.js

![](asset/appjs.png)
#### JSX
JSX merupakan semacam translator untuk menjadikan suatu elemen menjadi react element.
#### Component
Component merupakan bagian kecil dari tampilan website.
Best practise untuk membuat component, kita dapat membuat folder components pada folder src. nantinya kita akan membuat component-component di dalam folder tersebut
Contoh component:
![](asset/Navbar-component.png)
Setelah kita buat componentnya, kita panggil component tersebut ke dalam app.js
![](asset/navbaronappjs.png)

Kita juga dapat memanggil satu component lebih dari satu kali
![](asset/banyakcomponent.png)

### React JS - Component
Component adalah salah satu core dari react JS. Component membagi UI ke dalam  satuan-satuan kecil. Artinya, dalam 1 halaman, ada beberapa component yang bisa kita buat

Component dibuat jika component tersebut bersifat reusable code atau dapat digunakan berkali kali. Buatlah component jika component tersebut akan dibutuhkan pada section yang lain.

Contoh Component:
![](asset/memberinfo.png)

Setelah kita buat component, untuk menampilkannya kita panggil component yang sudah kita buat di file app.js
![](asset/showcomponent.png)

#### States and Props
- States adalah data local yang akan dikirimkan ke props
- Props digunakan untuk menangkap data yang dikirimkan state untuk dapat digunakan oleh suatu component.
![](asset/state.png)
Penjelasan
name dan umur merupakan state yang berisikan nilai yang akan ditangkap oleh props
![](asset/props.png)
Props mirip seperti parameter pada sebuah fungsi. Digunakan untuk menerima data yang akan digunakan oleh suatu komponen.

#### Event Handler
Sama seperti menggunakan DOM biasa, di react JS terdapat beberapa event handler seperti onclick, onhover, onsubmit dan lain-lain.
![](asset/onclick.png)
Penjelasan:
Ketika button diklik, jalankan function increment.

Untuk function yang membutuhkan parameter, maka kita gunakan callback pada event onclick
![](asset/onclickparam.png)

#### Use State
Definisi use state sama seperti state pada umumnya. Use state biasanya digunakan ketika terjadi perubahan data pada suatu elemen
![](asset/usestate.png)

#### Mengubah State
Untuk mengubah nilai state, kita dapat menggunakan setCount
![](asset/setcount.png)
#### Mapping
Fungsi mapping mirip seperti forEach pada array yaitu untuk menampilkan setiap data.
![](asset/mapping.png)
#### Conditional Rendering
Conditional rendering digunakan ketika kita ingin menampilkan atau merender komponen pada suatu kondisi tertentu. 
![](asset/conditional%20rendering.png)

Penjelasan:
- Terdapat state isLogin yang bernilai false
- Terdapat button yang memiliki event onclick yang mana memanggil setIsLogin dan merubah isLogin menjadi true
- Ketika button diklik, maka isLogin berubah menjadi true
- Lalu, lakukan conditional rendering
- Ketika isLogin bernilai true, maka munculkan Counter
- Ketika isLogin bernilai false, maka munculkan span Login Dulu

#### Lifecycle
Lifescycle merupakan siklus hidup dari suatu komponen. Lifecycle ini biasanya terbagi menjadi 3:
- Mounting => Kondisi dimana suatu component muncul
- Update => Kondisi dimana suatu component update
- Unmount => Kondisi dimana suatu component hilang

kita dapat menambahkan 'efek samping' pada proses lifecycle. 'Efek samping' tersebut kita sebut dengan use effect

#### Use Effect
Use effect biasanya digunakan saat kita membuat suatu call API. 
![](asset/useeffect.png)

#### Form
- Membuat form di react js
![](asset/form.png)

Form diatas memiliki value. untuk membuat value menjadi dinamis, kita dapat menggunakan state
![](asset/stateform.png)
Tetapi, value diatas hanya 'read only'. kita memerlukan events untuk berinteraksi dua arah dengan form. Event yang dibutuhkan adalah onchange
- onChange
![](asset/onchange.png)

- Menampilkan hasil input
  Untuk menampilkan hasil input yang sudah diisi, kita perlu menampungnya di variabel/state yang berbeda
  ![](asset/statedata.png)
  Setelah itu, kita masukkan data state dari state name dan address ke state data.
  ![](asset/setdata.png)
