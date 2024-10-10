# Penjelasan Proses pada Program 

Nama   : Nabilla Tsani Ayasi

NIM    : H1D022058

Shift  : F


# Registrasi
Proses registrasi yang terjadi dalam kode ini melibatkan beberapa langkah utama:

1. Pengisian Form: Pengguna mengisi form registrasi yang terdiri dari nama, email, password, dan konfirmasi password. Setiap input memiliki validasi, seperti minimal panjang karakter dan format email yang benar.

2. Validasi Input: Setelah pengguna menekan tombol registrasi, form akan divalidasi. Jika ada kesalahan, pesan error akan muncul di setiap field yang tidak valid.

3. Mengirim Data ke Server: Jika validasi berhasil, data yang diinput dikirim ke server menggunakan Postman. Data yang dikirim berupa nama, email, dan password.

4. Respon dari Server: Server merespon dengan status berhasil atau gagal. Jika berhasil, dialog sukses muncul, dan pengguna diarahkan untuk login. Jika gagal, dialog peringatan ditampilkan, meminta pengguna mencoba lagi.

5. Feedback dan Error Handling: Aplikasi menangani error yang mungkin terjadi selama proses registrasi dan memberikan umpan balik yang sesuai kepada pengguna.

Proses ini memastikan bahwa data registrasi diverifikasi dan dikirim secara benar ke server, sambil memberikan informasi yang jelas kepada pengguna tentang hasilnya.

![Screenshot 2024-10-10 094630](https://github.com/user-attachments/assets/c8785353-2887-440a-9cf5-b5978b7691ad)
![Screenshot 2024-10-10 112024](https://github.com/user-attachments/assets/5dbcfa50-fea4-4633-a407-78c602078ba7)

# Login
Proses login yang terjadi dalam kode ini dapat dijelaskan sebagai berikut:

1. Pengisian Form: Pengguna memasukkan email dan password ke dalam form login. Setelah itu, pengguna menekan tombol "Login".

2. Validasi Input: Email dan password yang diisi divalidasi terlebih dahulu. Jika tidak sesuai, pesan error muncul. Jika valid, proses login dilanjutkan.

3. Mengirim Data ke Server: Data email dan password dikirim ke server menggunakan Postman melalui **`LoginBloc.login()`**.

4. Respon dari Server: Jika login berhasil (kode respon 200), token dan ID pengguna disimpan menggunakan **`UserInfo()`**, dan pengguna diarahkan ke halaman produk. Jika gagal, pesan peringatan ditampilkan.

5. Penanganan Error: Jika terjadi kesalahan saat menghubungi server atau data tidak cocok, dialog error akan muncul, dan login dinyatakan gagal.

Proses ini mengatur validasi dan pengiriman data login, serta memberikan umpan balik kepada pengguna berdasarkan hasilnya. Jika login berhasil maka akan dialihkan ke halaman List Produk, jika login gagal maka akan muncul pop up pesan gagal.

![Screenshot 2024-10-10 105842](https://github.com/user-attachments/assets/d0078f4f-20a6-414d-b2b6-369f698dde40)
![Screenshot 2024-10-02 225625](https://github.com/user-attachments/assets/c72714f7-d0eb-4ed7-8ca0-8ae87fbfbf71)

# View Produk
Proses melihat produk pada kode ini terjadi secara singkat sebagai berikut:

1. Menampilkan Daftar Produk: Pada halaman utama, aplikasi memanggil data produk melalui metode `getProduks()` dari `ProdukBloc` yang mengambil daftar produk dari API. Data produk tersebut ditampilkan dalam bentuk daftar (list) di aplikasi menggunakan widget `ListView.builder`.

2. Navigasi ke Detail Produk: Setiap item produk yang ada dalam daftar dapat diklik. Saat pengguna menekan salah satu produk, aplikasi akan membawa mereka ke halaman detail produk menggunakan `Navigator.push()`. Halaman detail menampilkan informasi lebih lengkap tentang produk yang dipilih.

3. Tambah Produk: Pengguna juga dapat menambahkan produk baru dengan menekan ikon tambah (+) pada bagian atas kanan layar. Ini akan membawa pengguna ke halaman form untuk menambah produk baru.

Proses ini memberikan pengalaman melihat daftar produk dan detail setiap produk dengan navigasi yang jelas dan mudah.

![Screenshot 2024-10-02 225625](https://github.com/user-attachments/assets/c72714f7-d0eb-4ed7-8ca0-8ae87fbfbf71)

# Add Produk
Proses tambah produk yang terjadi dalam kode ini dapat dijelaskan sebagai berikut:

1. Pengisian Form: Pengguna mengisi form dengan kode produk, nama produk, dan harga produk.

2. Validasi Input: Sebelum data dikirim, form melakukan validasi. Jika ada field yang kosong atau tidak sesuai, pesan error muncul.

3. Pengiriman Data ke Server: Setelah validasi berhasil, data produk dikirim ke server melalui metode **`addProduk()`** menggunakan Postman.

4. Respon Server: Jika server berhasil menambahkan produk, pengguna diarahkan kembali ke halaman produk. Jika gagal, dialog peringatan muncul yang memberitahukan pengguna untuk mencoba lagi.

Proses ini memastikan produk baru ditambahkan ke sistem dengan validasi dan feedback yang tepat.

![Screenshot 2024-10-02 225645](https://github.com/user-attachments/assets/5469314f-6d75-453b-9b2a-bcca0ec19626)

# Detail Produk
Proses melihat detail produk dalam kode ini terjadi sebagai berikut:

1. Menampilkan Data Produk: Saat pengguna membuka halaman detail produk, data produk yang dipilih ditampilkan di layar, seperti kode produk, nama produk, dan harga produk.

2. Tombol Edit dan Hapus: Pengguna diberikan dua pilihan, yaitu mengedit produk atau menghapusnya. Tombol Edit akan membawa pengguna ke halaman form untuk mengubah data produk, sedangkan tombol Hapus akan menampilkan konfirmasi sebelum produk dihapus.

3. Konfirmasi Hapus: Jika pengguna memilih untuk menghapus produk, dialog konfirmasi akan muncul. Setelah dikonfirmasi, produk akan dihapus dari database, dan pengguna diarahkan kembali ke halaman daftar produk.

Proses ini memastikan bahwa pengguna dapat melihat detail produk serta melakukan tindakan lanjutan, seperti mengedit atau menghapus produk dengan mudah.

![Screenshot 2024-10-02 225701](https://github.com/user-attachments/assets/cd16799c-9345-4473-abe9-b8ef8c38afe5)


# Edit Produk
Proses edit produk dalam kode ini berlangsung sebagai berikut:

1. Pengisian Form: Jika produk yang akan diedit sudah ada, form akan terisi otomatis dengan data produk lama (kode produk, nama produk, dan harga). Pengguna dapat mengubah data yang diperlukan.

2. Validasi Input: Setelah pengguna mengedit dan menekan tombol "Ubah", form memvalidasi input. Jika ada yang tidak sesuai, pesan error akan ditampilkan.

3. Pengiriman Data ke Server: Setelah validasi berhasil, data produk yang sudah diperbarui dikirim ke server menggunakan Postman PUT melalui metode **`updateProduk()`**.

4. Respon Server: Jika proses update berhasil, pengguna diarahkan kembali ke halaman produk. Jika gagal, muncul dialog peringatan agar pengguna mencoba lagi.

Proses ini memastikan bahwa perubahan pada data produk disimpan dengan baik dan memberikan umpan balik kepada pengguna.

![Screenshot 2024-10-02 225716](https://github.com/user-attachments/assets/ae998614-9057-45ef-bff4-70124b478a2c)

# Delete Produk
Proses penghapusan produk berlangsung sebagai berikut:

1. Akses Tombol Hapus: Pada halaman detail produk, terdapat tombol "DELETE". Saat pengguna menekan tombol tersebut, aplikasi akan menampilkan kotak dialog konfirmasi yang menanyakan apakah pengguna yakin ingin menghapus produk tersebut.

2. Konfirmasi Penghapusan: Jika pengguna memilih untuk melanjutkan dan menekan tombol "Ya", aplikasi akan memanggil metode `deleteProduk()` dari `ProdukBloc`. Metode ini akan mengirim permintaan ke API untuk menghapus produk berdasarkan ID yang dipilih.

3. Tindak Lanjut Setelah Penghapusan: Jika proses penghapusan berhasil, pengguna akan diarahkan kembali ke halaman daftar produk (`ProdukPage`), dan produk yang telah dihapus tidak lagi ditampilkan dalam daftar.

Proses ini memastikan pengguna bisa mengonfirmasi sebelum menghapus, dan produk yang dihapus dihilangkan dari daftar secara real-time.

# Logout
Proses logout berlangsung dengan langkah-langkah berikut:

1. Akses Menu Logout: Pengguna dapat menemukan opsi logout di menu samping (drawer) aplikasi. Ketika pengguna menekan opsi ini, fungsi `logout()` dari `LogoutBloc` dipanggil.

2. Hapus Informasi Pengguna: Fungsi `logout()` akan menghapus semua informasi pengguna yang tersimpan menggunakan metode `UserInfo().logout()`. Ini memastikan bahwa sesi pengguna terputus.

3. Navigasi ke Halaman Login: Setelah logout berhasil, pengguna akan diarahkan ke halaman login (`LoginPage`) dengan menggunakan `Navigator.of(context).pushAndRemoveUntil`. Ini memastikan pengguna tidak bisa kembali ke halaman sebelumnya tanpa login ulang.

Proses ini memastikan pengguna keluar dari aplikasi dengan aman, dan harus login kembali untuk mengakses fitur-fitur selanjutnya.

# Kesimpulan
Kesimpulan dari proses-proses yang ada pada program ini adalah:

1. Manajemen Produk: Aplikasi ini memungkinkan pengguna untuk melihat daftar produk, menambahkan produk baru, mengedit produk yang sudah ada, serta menghapus produk. Pengelolaan ini diatur melalui beberapa kelas, seperti `ProdukBloc` yang mengelola interaksi API untuk mengambil, menambah, memperbarui, dan menghapus data produk, serta halaman-halaman terkait seperti `ProdukPage`, `ProdukForm`, dan `ProdukDetail` yang bertanggung jawab untuk antarmuka pengguna.

2. Logout: Fitur logout memungkinkan pengguna untuk keluar dari aplikasi. Proses ini menghapus informasi sesi pengguna yang disimpan, dan mengarahkan pengguna kembali ke halaman login, memastikan keamanan akses data dan privasi.

3. Interaksi dengan Backend: Program ini berkomunikasi dengan backend melalui API yaitu Postman untuk melakukan operasi CRUD (Create, Read, Update, Delete) pada data produk. Setiap perubahan yang dilakukan pada produk, seperti penambahan, pengeditan, atau penghapusan, langsung diteruskan ke server melalui permintaan HTTP.

4. Navigasi yang Terstruktur: Aplikasi ini menerapkan navigasi yang mulus, dengan transisi antar halaman yang mudah dipahami oleh pengguna. Pengguna dapat menambahkan, mengedit, atau menghapus produk dari daftar, serta logout dengan langkah-langkah yang sederhana.

Secara keseluruhan, program ini mengimplementasikan fungsionalitas pengelolaan data produk dan manajemen sesi pengguna dengan struktur yang rapi dan user-friendly.
