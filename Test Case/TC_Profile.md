# Laporan Hasil Pengujian Fungsional - Fitur Profil, Dashboard, dan Logout

Ringkasan hasil pengujian untuk fungsionalitas terkait Profil pengguna, Dashboard, dan proses Logout pada sistem SIPETAHUT.

## Ringkasan Eksekutif

| Status      | Jumlah Kasus Uji |
| ----------- | ---------------- |
| **Pass**    | **7**            |
| **Fail**    | **0**            |
| **Pending** | **0**            |
| **Total**   | **7**            |

---

## Detail Kasus Uji (Test Cases)

Berikut adalah rincian dari setiap kasus uji yang telah dieksekusi.

### Fitur: Profil & Dashboard

| ID        | Nama Test Case  | Deskripsi                                                             | Pre-Kondisi        | Langkah-langkah                                                                                  | Hasil yang Diharapkan                                                                                              | Hasil Aktual                                                                                                       | Status   |
| :-------- | :-------------- | :-------------------------------------------------------------------- | :----------------- | :----------------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------- | :------- |
| **TC-43** | Akses Profil    | Memastikan pengguna yang terdaftar dapat mengakses tampilan profil.   | User setelah Login | 1. Klik gambar foto profil atau nama pengguna di sisi kanan atas.<br>2. Klik tombol 'Profil'.    | Pengguna berhasil mengakses halaman profil. Sistem menampilkan rincian profil yang sesuai dengan biodata pengguna. | Pengguna berhasil mengakses halaman profil. Sistem menampilkan rincian profil yang sesuai dengan biodata pengguna. | **Pass** |
| **TC-44** | Akses Dashboard | Memastikan pengguna yang terdaftar dapat mengakses halaman dashboard. | User setelah Login | 1. Klik gambar foto profil atau nama pengguna di sisi kanan atas.<br>2. Klik tombol 'Dashboard'. | Pengguna berhasil mengakses halaman dashboard sesuai hak akses peran pengguna.                                     | Pengguna berhasil mengakses halaman dashboard sesuai hak akses peran pengguna.                                     | **Pass** |

### Fitur: Logout & Validasi Sesi

| ID        | Nama Test Case                 | Deskripsi                                                                                          | Pre-Kondisi         | Langkah-langkah                                                                                       | Hasil yang Diharapkan                                                                                                                     | Hasil Aktual                                                                                                                              | Status   |
| :-------- | :----------------------------- | :------------------------------------------------------------------------------------------------- | :------------------ | :---------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------- | :------- |
| **TC-45** | Keluar Akun                    | Memastikan pengguna berhasil mengakses menu untuk keluar dari akunnya saat ini.                    | User setelah Login  | 1. Klik gambar foto profil atau nama pengguna di sisi kanan atas.<br>2. Klik tombol 'Keluar'.         | Sistem menampilkan popup konfirmasi logout ("Keluar dari akun?").                                                                         | Sistem menampilkan popup konfirmasi logout ("Keluar dari akun?").                                                                         | **Pass** |
| **TC-46** | Batal Keluar                   | Memastikan pengguna tetap dalam keadaan login ketika batal melakukan logout.                       | User setelah Login  | 1. Klik tombol 'batal' pada pop up konfirmasi keluar.                                                 | Pengguna tetap dalam keadaan login dan memiliki akses bagi pengguna terdaftar.                                                            | Pengguna tetap dalam keadaan login dan memiliki akses bagi pengguna terdaftar.                                                            | **Pass** |
| **TC-47** | Berhasil Keluar                | Memastikan pengguna dapat keluar dari akun dan kehilangan akses bagi pengguna terdaftar.           | User setelah Login  | 1. Klik tombol 'keluar' pada pop up konfirmasi keluar.                                                | Sesi pengguna berakhir dan pengguna diarahkan ke halaman beranda. Pengguna tidak lagi bisa mengakses halaman Profil dan Dashboard.        | Sesi pengguna berakhir dan pengguna diarahkan ke halaman beranda. Pengguna tidak lagi bisa mengakses halaman Profil dan Dashboard.        | **Pass** |
| **TC-48** | Validasi Sesi (Tombol Kembali) | Memastikan pengguna tidak bisa kembali ke halaman yang memerlukan login setelah logout berhasil.   | User setelah logout | 1. Buka beranda sistem SIPETAHUT.<br>2. Klik tombol kembali (back) di browser.                        | Pengguna tidak dapat mengakses halaman yang memerlukan login dengan tombol kembali (back) di browser dan akan diarahkan ke halaman Login. | Pengguna tidak dapat mengakses halaman yang memerlukan login dengan tombol kembali (back) di browser dan akan diarahkan ke halaman Login. | **Pass** |
| **TC-49** | Validasi Sesi (Akses URL)      | Memastikan pengguna tidak bisa mengakses URL yang memerlukan login secara langsung setelah logout. | User setelah logout | 1. Buka beranda sistem SIPETAHUT.<br>2. Paste URL dashboard atau profil.<br>3. Memulai pencarian URL. | Pengguna tidak dapat mengakses halaman yang memerlukan login dengan URL dan akan diarahkan ke halaman Login.                              | Pengguna tidak dapat mengakses halaman yang memerlukan login dengan URL dan akan diarahkan ke halaman Login.                              | **Pass** |
