# Lab5Web
Praktikum Pemrograman Web 5
A.	Langkah Kerja Praktikum 
1.	Pertama adalah pengenalan cara menampilkan output di halaman browser, buka file yang telah dibuat yaitu index.html dengan halaman html sederhana dan script.js dengan memasukan code berikut:

// script.js
document.getElementById("pesan").textContent = "Hello World";
console.log("Hello World");
Hasil: Muncul tulisan Pengenalan JavaScript dan Hello World.
________________________________________
2.	Kedua pembuatan Alert dan prompt yang memuncul pop up berupa perintah untuk memasukan nama. Masukan code :
 
const namaPengguna = prompt("Masukkan nama Anda:", "");
if (namaPengguna && namaPengguna.trim() !== "") {
alert("Halo, " + namaPengguna + "!");
document.getElementById("pesan").textContent = "Selamat datang, " + namaPengguna + ".";
} else {
alert("Nama belum diisi.");
}
 Hasil: Muncul pop up untuk mengisi inputan,
 
Hasil : Jika nama tidak di isi.
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
} Hasil: Muncul pop up untuk mengisi nilai
  Hasil : Jika inputan yang diberikan kosong.
 Hasil: Jika inputan yang diberikan dibawah 60.
 Hasil: Jika nilai yang diberikan diatas 60.
________________________________________
5.	 Seleksi kondisi switch untuk meminta pengguna memasukan angka 1-5 dan menampilkan nama bilangan yang dimasukkan, masukan code berikut pada script.js:

const inputPilihan = prompt("Masukkan angka 1–5:");
switch (inputPilihan) {
case "1": alert("Bilangan satu"); break;
case "2": alert("Bilangan dua"); break;
case "3": alert("Bilangan tiga"); break;
case "4": alert("Bilangan empat"); break;
case "5": alert("Bilangan lima"); break;
default: alert("Pilihan tidak tersedia");
}
 Hasil: Jika inputan yang diberikan kosong. 
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
 
Hasil: Muncul form untuk melakukan inputan angka Hasil: Muncul bilangan ganjil Ketika memasukan angka bernilai 1 alias ganjil.
 Hasil: Muncul bilangan genap Ketika memasukan angka bernilai 12 alias genap.
________________________________________
7.	Mengubah latarbelakang halaman dengan memberikan 3 tombol sesuai warna yang diberikan dengan menggunakan satu function dan button pada html. Masukan code berikut pada html dan javascript:

function ubahWarnaLatar(warna) {
document.body.style.backgroundColor = warna;
}
<button type="button" onclick="ubahWarnaLatar('lightgreen')">Latar Hijau</button>
    <button type="button" onclick="ubahWarnaLatar('white')">Latar Putih</button>
    <button type="button" onclick="ubahWarnaLatar('lightyellow')">Latar Kuning</button> Hasil: Ketika  memilih  button sesuai latar warna , maka warna halaman akan ikut berubah.
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
Hasil: Maka checkbox pada menu dan total harga akan berubah secara otomatis.
