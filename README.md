# Mini Project 2 - Investigate Hotel Business using Data Visualization
"Sangat penting bagi suatu perusahaan untuk selalu menganalisa performa bisnisnya. Pada kesempatan kali ini, kita akan lebih mendalami bisnis dalam bidang perhotelan. Fokus yang kita tuju adalah untuk mengetahui bagaimana perilaku pelanggan kita dalam melakukan pemesanan hotel, dan hubungannya terhadap tingkat pembatalan pemesanan hotel. Hasil dari insight yang kita temukan akan kita sajikan dalam bentuk data visualisasi agar lebih mudah dipahami dan bersifat lebih persuasif. ”

## Data Preprocessing
Data Preprocessing dilakukan untuk mempersiapkan data mentah menjadi data yang bersih dan siap diolah.

### 1. Mengatasi Data Null
Setelah ditemukan ada jumlah data null yang cukup banyak dalam dataset, maka akan dilakukan replace data dengan median atau modus data dari kolom tersebut, untuk menghindari kehilangan terlalu banyak data jika dihapus.
- Kolom ‘city’ dengan modus.
- Kolom ‘agent’ dengan median.
- Kolom ‘company’ dengan median.

### 2. Mengganti Value Tidak Sesuai
Mengubah value data pada kolom ‘meal’ agar lebih sesuai dengan bahasa standar data booking hotel:
- Breakfast: Bed & Breakfast (BB)
- Dinner: Half Board (HB)
- Full Board: Full Board (FB)
- No Meal: Self Catering (SC)
- Undefined: Undefined

### 3. Membuang Data Tidak Diperlukan
- Menghitung jumlah total tamu dengan menambahkan jumlah tamu dewasa (‘adult’), tamu anak-anak (‘children’), tamu bayi (‘babies’) ke dalam kolom baru 'total_guests’.
- Melakukan filtering untuk membuang data total jumlah tamu yang berisi 0 karena tidak diperlukan.


## Monthly Hotel Booking Analysis Based on Hotel Type
![image](https://github.com/regitafif/mp2_coba/assets/167510010/36a65ec8-3f13-4ad0-8add-198bc853e485)
Kesimpulan:
- Ada fluktuasi jumlah pemesanan yang cukup besar untuk City Hotel, namun jumlah pemesanan cenderung stabil untuk Resort Hotel.
- Ada puncak pemesanan di bulan-bulan tertentu pada City Hotel yang mungkin berkaitan dengan waktu liburan. Kenaikan ada di bulan Juni hingga Agustus, yang mungkin disebabkan libur Hari Raya Idul Fitri 1439H di Bulan Juni, serta libur Hari Kemerdekaan Indonesia dan Hari Raya Idul Adha 1439H di Bulan Agustus.
- Penurunan terjadi setelah bulan Agustus, namun mengalami kenaikan lagi hingga bulan Desember yang memiliki libur Hari Raya Natal dan Tahun Baru.


## Impact Analysis of Stay Duration on Hotel Bookings Cancellation Rates
![image](https://github.com/regitafif/mp2_coba/assets/167510010/2a40bf0c-cd55-4417-9876-404a4922af7c)
Kesimpulan:
- City Hotel memiliki rasio pembatalan yang cukup tinggi ketika durasi menginap yang sangat lama yaitu lebih dari 2 minggu, namun memiliki rasio pembatalan yang serupa untuk durasi penginapan 3 hari sampai 2 minggu. Tamu yang memesan untuk durasi singkat lebih konsisten dengan rencana penginapan mereka.
- Resort Hotel memiliki rasio pembatalan yang cukup serupa untuk setiap durasi penginapan, tetapi memiliki rasio pembatalan yang rendah untuk durasi penginapan kurang dari 3 hari. Namun rasio pembatalan untuk Resort Hotel cenderung lebih rendah dari pada City Hotel yang mungkin menunjukkan bahwa tamu Resort Hotel lebih konsisten dengan rencana penginapan mereka secara keseluruhan tanpa terlalu melihat durasi penginapan.
- 


