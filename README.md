## UTSPEMROWEB2
### NAMA   : NOVELLYSNA NURZISKA
### NIM    : 312410131
### KELAS  : TI.24.A.1
### MATKUL : PEMROGRAMAN WEB 2

#### Analisis Eksperimen DOM-Based Cross-Site Scripting (XSS)

#### Pendahuluan
Keamanan aplikasi web merupakan aspek penting dalam pengembangan sistem modern. Salah
satu kerentanan yang sering terjadi adalah Cross-Site Scripting (XSS). Pada eksperimen ini,
dilakukan pengujian sederhana untuk memahami bagaimana XSS dapat terjadi pada manipulasi
DOM menggunakan JavaScript.
#### Kode Program
#### Berikut kode HTML yang digunakan dalam eksperimen:
```
<!DOCTYPE html>
<html>
<head>
    <title>Uji XSS Sederhana (Aman)</title>
</head>
<body>
    <h2>Form Input</h2>
    <input type="text" id="inputNama" placeholder="Masukkan nama">
    <button onclick="tampilkan()">Kirim</button>

    <h3>Output:</h3>
    <p id="output"></p>

    <script>
        function tampilkan() {
            var nama = document.getElementById("inputNama").value;
            document.getElementById("output").innerText = "Halo, " + nama;
        }
    </script>
</body>
</html>
```
#### Langkah Pengujian
#### 1. Jalankan file HTML di browser
#### 2. Masukkan input normal (contoh: Novellysna Nurziska)
#### 3. Amati hasil output
#### 4. Masukkan script XSS: <script>alert('XSS')</script>
#### 5. Klik tombol kirim dan amati hasil
### Hasil Pengujian
#### Tambahkan screenshot berikut:
#### [Screenshot 1: Tampilan awal form]
<img width="652" height="344" alt="Tampilan form" src="https://github.com/user-attachments/assets/92eabc55-4be9-4034-8581-78414a6bdea1" />

#### [Screenshot 2: Hasil input normal]
<img width="513" height="328" alt="coba input nama" src="https://github.com/user-attachments/assets/dfe7fed4-80bb-4ace-b2de-2e3f6b9358ef" />

#### [Screenshot 3: Alert XSS muncul]
<img width="577" height="337" alt="Saat alert muncul (XSS berhasil)" src="https://github.com/user-attachments/assets/0800c117-fa3f-4668-b0e0-b8934a5fa550" />

#### Perbaikan
#### Ubah innerHTML menjadi innerText:
````
document.getElementById("output").innerText = "Halo, " + nama;
````
Tambahkan screenshot setelah perbaikan:
#### [Screenshot 4: Tidak ada alert setelah perbaikan]
<img width="577" height="337" alt="Saat alert muncul (XSS berhasil)" src="https://github.com/user-attachments/assets/dca428a0-790b-4956-be5e-b28b02b6e8c6" />

#### Kesimpulan
XSS dapat terjadi akibat penggunaan innerHTML tanpa validasi. Dengan mengganti ke
innerText, eksekusi script dapat dicegah.
