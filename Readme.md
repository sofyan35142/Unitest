# Manajemen Pesanan Restoran

Program **Manajemen Pesanan Restoran** ini adalah aplikasi berbasis Python yang memudahkan restoran dalam mengelola pesanan pelanggan. Dengan menggunakan file Microsoft Word (`.docx`) sebagai tempat penyimpanan, program ini menyediakan berbagai fitur untuk menambah, menampilkan, memperbarui, menghapus, dan mencari pesanan yang sudah ada. Semua data pesanan disimpan dalam format yang mudah dibaca dan dikelola.

## Fitur Utama

Program ini menyediakan lima fitur utama untuk membantu manajemen pesanan restoran. Setiap fitur memungkinkan Anda untuk mengelola pesanan dengan mudah, baik untuk menambah pesanan baru, memperbarui status pesanan, atau menghapus pesanan yang dibatalkan. Berikut adalah penjelasan rinci dari masing-masing fitur:

### 1. **Tambah Pesanan**
   - **Deskripsi**: Fitur ini memungkinkan pengguna untuk menambahkan pesanan baru ke dalam file `orders.docx`. Program akan meminta input dari pengguna mengenai detail pesanan seperti nama pelanggan, menu yang dipesan, jumlah pesanan, dan path gambar pesanan.
   - **Input yang Diperlukan**:
     - **Nama Pelanggan**: Nama pelanggan yang memesan.
     - **Menu yang Dipesan**: Nama menu yang dipilih oleh pelanggan.
     - **Jumlah Pesanan**: Jumlah porsi atau item yang dipesan.
     - **Path Gambar**: Lokasi gambar yang terkait dengan pesanan. Gambar ini akan disisipkan di dalam dokumen (opsional).
   - **Proses**:
     - Program akan memeriksa apakah file `orders.docx` sudah ada. Jika belum, file tersebut akan dibuat.
     - Informasi pesanan akan disimpan dalam file `orders.docx` dengan format standar, dan gambar akan ditambahkan (jika path gambar valid).
   - **Contoh Input**:
     ```
     Masukkan Nama Pelanggan: Mukhamad Sofyan
     Masukkan Menu yang Dipesan: Nasi Goreng
     Masukkan Jumlah Pesanan: 2
     Masukkan Path Gambar: /path/to/image.jpg
     ```

### 2. **Tampilkan Pesanan**
   - **Deskripsi**: Fitur ini digunakan untuk menampilkan semua pesanan yang ada dalam file `orders.docx`. Ini memberikan gambaran lengkap tentang semua pesanan yang telah dimasukkan, termasuk nama pelanggan, menu yang dipesan, jumlah pesanan, dan status pesanan.
   - **Proses**:
     - Program membaca setiap paragraf dalam file `orders.docx` dan menampilkan informasi pesanan yang sudah ada.
     - Jika pesanan terkait dengan gambar, gambar juga akan ditampilkan.
   - **Output Contoh**:
     ```
     Nama Pelanggan: Mukhamad Sofyan
     Menu yang Dipesan: Nasi Goreng
     Jumlah Pesanan: 2
     Status: diproses
     --------------------------------------------------
     ```

### 3. **Update Pesanan**
   - **Deskripsi**: Fitur ini memungkinkan pengguna untuk memperbarui status pesanan yang sudah ada. Anda bisa mengubah status pesanan berdasarkan nomor urut pesanan yang ingin diubah, misalnya mengubah status pesanan menjadi `diproses`, `selesai`, atau `batal`.
   - **Proses**:
     - Program akan menampilkan daftar pesanan yang ada dan meminta Anda untuk memilih pesanan berdasarkan nomor urut.
     - Setelah memilih pesanan, Anda akan diminta untuk memasukkan status baru.
     - Program kemudian akan memperbarui status pesanan dalam file `orders.docx` dan menyimpannya.
   - **Contoh Input**:
     ```
     Pilih nomor pesanan yang ingin diubah: 1
     Masukkan status baru (diproses/selesai/batal): selesai
     ```
   - **Output Setelah Update**:
     ```
     Status pesanan berhasil diperbarui.
     ```

### 4. **Hapus Pesanan**
   - **Deskripsi**: Fitur ini memungkinkan Anda untuk menghapus pesanan yang memiliki status `batal`. Program akan meminta Anda untuk memilih pesanan berdasarkan nomor urut, dan jika pesanan tersebut memiliki status `batal`, maka pesanan akan dihapus dari file `orders.docx`.
   - **Proses**:
     - Program menampilkan daftar pesanan yang ada beserta statusnya.
     - Anda memilih nomor pesanan yang ingin dihapus.
     - Jika status pesanan adalah `batal`, pesanan akan dihapus beserta gambar terkait (jika ada).
   - **Contoh Input**:
     ```
     Pilih nomor pesanan yang ingin dihapus: 2
     Pesanan berhasil dihapus.
     ```
   - **Catatan**: Hanya pesanan dengan status `batal` yang bisa dihapus. Jika statusnya selain `batal`, pesanan tidak akan dihapus.

### 5. **Cari Pesanan**
   - **Deskripsi**: Fitur ini memungkinkan Anda untuk mencari pesanan berdasarkan nama pelanggan. Program akan mencari seluruh file `orders.docx` dan menampilkan pesanan yang sesuai dengan nama pelanggan yang dicari.
   - **Proses**:
     - Anda diminta untuk memasukkan nama pelanggan yang ingin dicari.
     - Program kemudian akan mencari dan menampilkan informasi pesanan yang sesuai.
   - **Contoh Input**:
     ```
     Masukkan nama pelanggan yang dicari: Mukhamad Sofyan
     ```
   - **Output Setelah Pencarian**:
     ```
     Nama: Mukhamad Sofyan, Menu: Nasi Goreng, Jumlah: 2, Status: diproses
     ```

## Struktur File `orders.docx`

File `orders.docx` akan menyimpan setiap pesanan dalam format berikut:
