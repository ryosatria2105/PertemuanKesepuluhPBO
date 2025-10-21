# 🖥️📚 TUGAS PBO – Pertemuan Kesepuluh

**Implementasi Fitur Upload CSV pada Aplikasi CRUD Member Gym (Java Swing + JDBC + PostgreSQL)**  

---

## 📄 Studi Kasus  
Tugas ini dibuat untuk **memenuhi mata kuliah Pemrograman Berorientasi Objek (PBO)** dengan studi kasus pengembangan sistem CRUD Data Member Gym yang sebelumnya sudah dibuat pada pertemuan ke-6.  
Pada versi kali ini, sistem dikembangkan dengan penambahan fitur Upload CSV, yang berfungsi untuk mengimpor data member secara otomatis dari file CSV ke database PostgreSQL tanpa harus menginput data secara manual satu per satu.  

Data yang diimpor meliputi:  
- 🆔 ID Member  
- 👤 Nama  
- 🏋️‍♂️ Tipe Paket  
- 🧑‍🏫 Coach  

---

## 🧩 Peran Fitur Upload CSV  
Fitur **Upload CSV** berfungsi untuk mempercepat proses input data massal ke dalam sistem, terutama ketika data member disimpan dalam format eksternal seperti Excel atau Google Sheets.  

Fungsinya yakni:  
- 📂 **Pemilihan File CSV**  
  Menggunakan `JFileChooser` untuk memilih file dari penyimpanan lokal.  
- 📖 **Pembacaan Data CSV**  
  Menggunakan `BufferedReader` untuk membaca isi file baris demi baris.  
- 🔗 **Koneksi ke Database PostgreSQL**  
  Data dari file CSV dimasukkan langsung ke tabel `member_gym` menggunakan koneksi `JDBC`.  
- 🔄 **Refresh Otomatis JTable**  
  Setelah upload berhasil, tabel di GUI otomatis menampilkan data terbaru tanpa restart aplikasi.  

---

## ⚙️ Langkah-Langkah Implementasi  
1. **Menambahkan Tombol Upload**  
   - Tambahkan tombol **Upload** pada `MemberFrame.java` di NetBeans, Klik dua kali tombol tersebut untuk membuat event `btnUploadActionPerformed`.
     <img width="777" height="500" alt="image" src="https://github.com/user-attachments/assets/b62090da-dc71-4079-9386-acab1c921b56" />

2. **Menulis Kode Event Upload**  
   - Gunakan `JFileChooser` untuk memilih file CSV, lalu baca isinya dengan `BufferedReader`.
     <img width="777" height="500" alt="image" src="https://github.com/user-attachments/assets/a23cec4a-a33e-4543-98dc-b8ec4851f798" />

     <img width="777" height="500" alt="image" src="https://github.com/user-attachments/assets/1a9d26af-6139-4e5d-b2b0-3348a2ae9222" />

4. **Menyiapkan File CSV**  
   - Buat file CSV menggunakan Excel dengan struktur kolom:  
     <img width="777" height="500" alt="image" src="https://github.com/user-attachments/assets/8705885e-3741-4e1d-987d-76e7b32b89a8" />

   - Simpan file dalam format **CSV UTF-8 (Comma delimited)** dan pastikan tanda pemisahnya menggunakan `;`.
     <img width="777" height="500" alt="image" src="https://github.com/user-attachments/assets/01218abb-7a86-4875-87c2-d43a48c9b5ce" />


5. **Uji Coba Program**  
   - Jalankan aplikasi, lalu klik tombol **Upload**.
     <img width="777" height="500" alt="image" src="https://github.com/user-attachments/assets/daa9f1ab-0e6b-4610-b360-595f64a2df98" />

   - Pilih file CSV yang sudah dibuat, klik **Open**, dan tunggu hingga muncul pesan **“Upload berhasil!”**
     <img width="777" height="500" alt="image" src="https://github.com/user-attachments/assets/c55e8c40-3fa7-4364-8562-95ff0b1234e6" />

   - Data dari file akan otomatis masuk ke database dan langsung muncul pada tabel aplikasi.
     <img width="777" height="500" alt="image" src="https://github.com/user-attachments/assets/e3d64b0a-9dc1-4496-9955-7efc0dde2e72" />


---

## 🖼️ Tampilan Aplikasi  

- Tampilan Form Utama dengan tombol Upload CSV  
  <img width="777" height="500" alt="image" src="https://github.com/user-attachments/assets/2bb5a0af-b9fe-4ebe-bc97-ba7477f7b482" />
 

- Tampilan saat memilih file CSV melalui JFileChooser  
  <img width="777" height="500" alt="image" src="https://github.com/user-attachments/assets/d2682bf9-620c-4691-87f8-787f6ba2d101" />


- Pesan sukses setelah proses Upload selesai  
  <img width="777" height="236" alt="image" src="https://github.com/user-attachments/assets/566dc09f-dca0-4d0a-ac62-630c291949ab" />


- Data baru otomatis muncul di JTable GUI  
  <img width="777" height="500" alt="image" src="https://github.com/user-attachments/assets/29b13c60-8b25-499c-b48a-675cafcf1e92" />


  Laporan PDF : [TugasPertemuan10PBO.pdf](https://github.com/user-attachments/files/23024697/TugasPertemuan10PBO.pdf)


---

## 👨‍💻 Author  
**Ryo Satriagung Hidayat**  
NIM: 09010624015  
Program Studi: Sistem Informasi  
Universitas Islam Negeri Sunan Ampel Surabaya – 2025  

---
