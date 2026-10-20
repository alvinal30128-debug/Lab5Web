# Lab5Web
Praktikum Pemrograman Web 5
A.	Langkah Kerja Praktikum 
1.	Pertama adalah pengenalan cara menampilkan output di halaman browser, buka file yang telah dibuat yaitu index.html dengan halaman html sederhana dan script.js dengan memasukan code berikut:

// script.js
document.getElementById("pesan").textContent = "Hello World";
console.log("Hello World");
Hasil: Muncul tulisan Pengenalan JavaScript dan Hello World.
<img width="940" height="332" alt="image" src="https://github.com/user-attachments/assets/22d18e8c-c2e2-48bf-a8bd-c144136dd4d7" />

________________________________________
2.	Kedua pembuatan Alert dan prompt yang memuncul pop up berupa perintah untuk memasukan nama. Masukan code :
 
const namaPengguna = prompt("Masukkan nama Anda:", "");
if (namaPengguna && namaPengguna.trim() !== "") {
alert("Halo, " + namaPengguna + "!");
document.getElementById("pesan").textContent = "Selamat datang, " + namaPengguna + ".";
} else {
alert("Nama belum diisi.");
}
<img width="940" height="351" alt="image" src="https://github.com/user-attachments/assets/4c4f3528-a5a6-4af7-b825-60742437f36d" />

 Hasil: Muncul pop up untuk mengisi inputan,
 <img width="940" height="348" alt="image" src="https://github.com/user-attachments/assets/30fbf02f-17df-42b2-bcca-e5bd677a4d1f" />

Hasil : Jika nama tidak di isi.
<img width="940" height="435" alt="image" src="https://github.com/user-attachments/assets/92a28a11-e3e8-4c8d-ab08-ea8d83afabbd" />

 Hasil: Jika nama berhasil di isi.
________________________________________
3.	Ketiga Function dan operasi aritmatika sederhana, masukan code berikut pada script.js:

function operasiDasar(a, b) {
console.log("Penjumlahan:", a + b);
console.log("Pengurangan:", a - b);
console.log("Perkalian:", a * b);
console.log("Pembagian:", b !== 0 ? a / b : "Tidak dapat dibagi nol");
console.log("Modulus:", a % b);
}
operasiDasar(9, 4);
 <img width="863" height="359" alt="image" src="https://github.com/user-attachments/assets/4c230056-f2e6-478c-ac83-421b1a03b0c8" />

Hasil : Semua bilangan yang muncul pada tab console dari program yang dibuat.
________________________________________ 
4.	Keempat seleksi kondisi if-else untuk perulangan yang menyatakan nilai minimal 60 dapat dinyatakan lulus namun sebaliknya jika dibawah 60 maka dapat dinyatakan belum lulus. Masukan code pada script.js:

const inputNilai = prompt("Masukkan nilai (0–100):");
const nilaiMahasiswa = Number(inputNilai);
if (inputNilai === null || inputNilai.trim() === "" ||
Number.isNaN(nilaiMahasiswa) || nilaiMahasiswa < 0 || nilaiMahasiswa > 100) {
alert("Input nilai tidak valid.");
} else if (nilaiMahasiswa >= 60) {
alert("Lulus");
} else {
alert("Belum lulus");
} 
<img width="940" height="443" alt="image" src="https://github.com/user-attachments/assets/ac1a8d26-9126-4ac3-ad19-6e5166262fa5" />

Hasil: Muncul pop up untuk mengisi nilai
<img width="940" height="404" alt="image" src="https://github.com/user-attachments/assets/a24aaf96-4b8e-405c-87b3-a69c40a5ebc4" />

  Hasil : Jika inputan yang diberikan kosong.
  <img width="940" height="302" alt="image" src="https://github.com/user-attachments/assets/efb29d4a-6a80-46b8-a280-6b0c646b7993" />

 Hasil: Jika inputan yang diberikan dibawah 60.
 <img width="940" height="315" alt="image" src="https://github.com/user-attachments/assets/6108235e-9621-4a83-ad0a-249c65ed2799" />

 Hasil: Jika nilai yang diberikan diatas 60.
________________________________________
5.	 Seleksi kondisi switch untuk meminta pengguna memasukan angka 1-5 dan menampilkan nama bilangan yang dimasukkan, masukan code berikut pada script.js:
<img width="940" height="435" alt="image" src="https://github.com/user-attachments/assets/f933301b-da60-4bfb-856f-daec8b564449" />

const inputPilihan = prompt("Masukkan angka 1–5:");
switch (inputPilihan) {
case "1": alert("Bilangan satu"); break;
case "2": alert("Bilangan dua"); break;
case "3": alert("Bilangan tiga"); break;
case "4": alert("Bilangan empat"); break;
case "5": alert("Bilangan lima"); break;
default: alert("Pilihan tidak tersedia");
}
<img width="940" height="446" alt="image" src="https://github.com/user-attachments/assets/576cfc70-1ff5-411e-95a5-5d23da1ab406" />

 Hasil: Jika inputan yang diberikan kosong. 
 <img width="940" height="430" alt="image" src="https://github.com/user-attachments/assets/cbf8e8ac-901a-4a67-869b-65ab845e9e72" />

 Hasil: Jika inputan yang diberikan angka 5 maka akan muncul pop up yang memberikan alert Bilangan Lima.
________________________________________
 
6.	Keenam membuat form untuk membedakan bilangan genap atau ganjil dengan membuat button unutuk melakukan interaksi. Masukan code pada halaman html terlebih dahulu lalu masukan pada script.js :
<label for="bilangan">Masukkan bilangan bulat:</label>
<input type="number" id="bilangan" step="1">
<button type="button" onclick="cekBilangan()">Periksa</button>
<p id="hasilBilangan"></p>
function cekBilangan() {
const input = document.getElementById("bilangan").value;
const angka = Number(input);
const hasil = document.getElementById("hasilBilangan");
if (input.trim() === "" || !Number.isInteger(angka)) {
hasil.textContent = "Masukkan bilangan bulat yang valid.";
} else if (angka % 2 === 0) {
hasil.textContent = "Bilangan genap";
} else {
hasil.textContent = "Bilangan ganjil";
}
}
 <img width="940" height="369" alt="image" src="https://github.com/user-attachments/assets/cc19c67f-2d85-4f32-9763-c172729da9f7" />

Hasil: Muncul form untuk melakukan inputan angka Hasil: Muncul bilangan ganjil Ketika memasukan angka bernilai 1 alias ganjil.
<img width="940" height="401" alt="image" src="https://github.com/user-attachments/assets/13ed123c-55eb-4902-9ef7-d371da1cba57" />

 Hasil: Muncul bilangan genap Ketika memasukan angka bernilai 12 alias genap.
 <img width="940" height="462" alt="image" src="https://github.com/user-attachments/assets/7aea65ad-1db4-4b41-8270-9d0e8ac0c582" />

________________________________________
7.	Mengubah latarbelakang halaman dengan memberikan 3 tombol sesuai warna yang diberikan dengan menggunakan satu function dan button pada html. Masukan code berikut pada html dan javascript:

function ubahWarnaLatar(warna) {
document.body.style.backgroundColor = warna;
}
<button type="button" onclick="ubahWarnaLatar('lightgreen')">Latar Hijau</button>
    <button type="button" onclick="ubahWarnaLatar('white')">Latar Putih</button>
    <button type="button" onclick="ubahWarnaLatar('lightyellow')">Latar Kuning</button> 
 
Hasil: Ketika  memilih  button sesuai latar warna , maka warna halaman akan ikut berubah.
<img width="940" height="475" alt="image" src="https://github.com/user-attachments/assets/30b024de-5251-4fba-9189-dce96f397731" />

________________________________________
8.	Pembuata DOM dan checkbox menu makanan yang Dimana Ketika kita mengklik menu tersebut maka total harga akan ikut berubah otomatis sesuai harganya. Buat terlebih dahulu menu makanan pada file html lalu masukan code javascriptnya.:

<h3>Daftar Menu Makanan</h3>
<label><input type="checkbox" class="menu" value="5000"> Ayam Goreng — Rp5.000</label><br>
<label><input type="checkbox" class="menu" value="500"> Tempe — Rp500</label><br>
<label><input type="checkbox" class="menu" value="2500"> Telur Dadar — Rp2.500</label><br>
<p>Total: Rp<span id="total">0</span></p>
BUAT SCRIPT DIAKHIR SEBELUM TAG</BODY>
const daftarMenu = document.querySelectorAll(".menu");
daftarMenu.forEach((item) => {
item.addEventListener("change", hitungTotal);
});
function hitungTotal() {
let total = 0;
daftarMenu.forEach((item) => {
if (item.checked) total += Number(item.value);
});
document.getElementById("total").textContent = total.toLocaleString("id-ID");
}
<img width="940" height="624" alt="image" src="https://github.com/user-attachments/assets/c7d2d3d1-3910-446d-bedf-3a42af41f71e" />

Hasil: Maka checkbox pada menu dan total harga akan berubah secara otomatis.
