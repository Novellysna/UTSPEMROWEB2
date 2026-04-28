## UTSPEMROWEB2
### NAMA   : NOVELLYSNA NURZISKA
### NIM    : 312410131
### KELAS  : TI.24.A.1
### MATKUL : PEMROGRAMAN WEB 2

Analisis Eksperimen DOM-Based Cross-Site Scripting (XSS)

Pendahuluan
Keamanan aplikasi web merupakan aspek yang sangat penting dalam pengembangan sistem modern, terutama karena meningkatnya ancaman serangan siber. Salah satu jenis kerentanan yang sering ditemukan adalah Cross-Site Scripting (XSS), yaitu serangan yang memungkinkan penyerang menyisipkan kode berbahaya ke dalam halaman web. Pada eksperimen ini, dilakukan pengujian sederhana untuk memahami bagaimana XSS dapat terjadi melalui manipulasi Document Object Model (DOM) menggunakan JavaScript.

Kode Program
Eksperimen ini menggunakan kode HTML sederhana yang menerima input dari pengguna dan menampilkannya kembali di halaman web menggunakan JavaScript. Input tersebut diproses tanpa validasi atau penyaringan khusus, sehingga memungkinkan terjadinya eksekusi script berbahaya jika dimasukkan oleh pengguna.

Langkah Pengujian
Langkah pertama adalah menjalankan file HTML di browser. Selanjutnya, pengguna diminta memasukkan input normal, seperti nama, untuk melihat bagaimana sistem bekerja dalam kondisi aman. Setelah itu, dilakukan pengujian dengan memasukkan script berbahaya, seperti alert('XSS'), lalu menekan tombol kirim. Hasil dari kedua jenis input tersebut kemudian diamati untuk melihat perbedaannya.

Hasil Pengujian
Pada input normal, sistem menampilkan teks sesuai dengan yang dimasukkan pengguna tanpa masalah. Namun, ketika script XSS dimasukkan, browser mengeksekusi kode tersebut dan menampilkan alert, yang menunjukkan bahwa aplikasi rentan terhadap serangan XSS. Hal ini terjadi karena penggunaan innerHTML yang langsung memproses input sebagai HTML.

Perbaikan
Untuk mengatasi masalah tersebut, dilakukan perubahan pada kode dengan mengganti innerHTML menjadi innerText. Dengan cara ini, input dari pengguna akan diperlakukan sebagai teks biasa, bukan sebagai kode HTML atau JavaScript, sehingga mencegah eksekusi script berbahaya.

Kesimpulan
Eksperimen ini menunjukkan bahwa penggunaan innerHTML tanpa validasi dapat menyebabkan kerentanan XSS. Dengan menerapkan metode yang lebih aman seperti innerText, risiko serangan dapat diminimalkan dan keamanan aplikasi web dapat ditingkatkan.
