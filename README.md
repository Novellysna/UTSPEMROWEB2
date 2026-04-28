## UTSPEMROWEB2
### NAMA   : NOVELLYSNA NURZISKA
### NIM    : 312410131
### KELAS  : TI.24.A.1
### MATKUL : PEMROGRAMAN WEB 2

Analisis Eksperimen DOM-Based Cross-Site Scripting (XSS)

Analisis Eksperimen DOM-Based
Cross-Site Scripting (XSS)
Pendahuluan
Keamanan aplikasi web merupakan aspek penting dalam pengembangan sistem modern. Salah
satu kerentanan yang sering terjadi adalah Cross-Site Scripting (XSS). Pada eksperimen ini,
dilakukan pengujian sederhana untuk memahami bagaimana XSS dapat terjadi pada manipulasi
DOM menggunakan JavaScript.
Kode Program
Berikut kode HTML yang digunakan dalam eksperimen:
Langkah Pengujian
1. Jalankan file HTML di browser
2. Masukkan input normal (contoh: Novellysna Nurziska)
3. Amati hasil output
4. Masukkan script XSS: <script>alert('XSS')</script>
5. Klik tombol kirim dan amati hasil
Hasil Pengujian
Tambahkan screenshot berikut:
[Screenshot 1: Tampilan awal form]
[Screenshot 2: Hasil input normal]
[Screenshot 3: Alert XSS muncul]
Perbaikan
Ubah innerHTML menjadi innerText:
document.getElementById("output").innerText = "Halo, " + nama;
Tambahkan screenshot setelah perbaikan:
[Screenshot 4: Tidak ada alert setelah perbaikan]
Kesimpulan
XSS dapat terjadi akibat penggunaan innerHTML tanpa validasi. Dengan mengganti ke
innerText, eksekusi script dapat dicegah.
