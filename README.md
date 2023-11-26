## **Business Problem Understanding**
### **Context**
Sistem peminjaman sepeda adalah generasi baru dari penyewaan sepeda tradisional di mana seluruh proses, mulai dari keanggotaan, penyewaan, dan pengembalian, telah menjadi otomatis. Melalui sistem-sistem ini, seorang pengguna dapat dengan mudah menyewa sepeda dari posisi tertentu dan mengembalikannya ke posisi lain. Saat ini, ada sekitar lebih dari 500 program peminjaman sepeda di seluruh dunia yang terdiri dari lebih dari 500 ribu sepeda. Saat ini, ada minat besar dalam sistem-sistem ini karena peran penting mereka dalam masalah lalu lintas, lingkungan, dan kesehatan.

Selain dari aplikasi dunia nyata yang menarik dari sistem peminjaman sepeda, karakteristik data yang dihasilkan oleh sistem-sistem ini membuat mereka menarik untuk penelitian. Berbeda dengan layanan transportasi lain seperti bus atau kereta bawah tanah, durasi perjalanan, posisi keberangkatan, dan posisi kedatangan secara eksplisit dicatat dalam sistem-sistem ini. Fitur ini mengubah sistem peminjaman sepeda menjadi jaringan sensor virtual yang dapat digunakan untuk mendeteksi mobilitas di kota. Oleh karena itu, diharapkan bahwa peristiwa-peristiwa paling penting di kota dapat terdeteksi melalui pemantauan data ini.

### **Problem Statement**
Dalam menjalankan suatu bisnis, tentu tidak luput dari cost atau biaya, diantaranya adalag biaya operasional dan biaya pemeliharaan. Biaya operasional dan biaya pemeliharaan pada sistem bike sharing dapat bervariasi tergantung pada skala operasi, model bisnis, lokasi, dan infrastruktur yang digunakan. Berikut adalah beberapa elemen umum yang dapat menyumbang terhadap biaya operasional dan pemeliharaan dalam sistem bike sharing:

- Akuisisi dan Pemeliharaan Sepeda:
  - Akuisisi Sepeda: Biaya pembelian sepeda baru atau bekas.
  - Pemeliharaan Sepeda: Biaya perbaikan, perawatan, dan penggantian komponen sepeda.
- Stasiun dan Peralatan:
  - Akuisisi dan Pemasangan Stasiun: Biaya pembelian dan pemasangan stasiun docking untuk sepeda.
  - Pemeliharaan Stasiun: Biaya perbaikan dan perawatan stasiun docking, termasuk perangkat keras dan perangkat lunaknya.
- Pengelolaan Flotilla:
  - Distribusi Sepeda: Biaya untuk memindahkan sepeda dari stasiun satu ke stasiun lainnya untuk menjaga ketersediaan sepeda yang seimbang.
  - Pemantauan dan Pengelolaan Armada: Biaya untuk sistem pelacakan dan pengelolaan armada sepeda.
- Teknologi dan Perangkat Lunak:
  - Pemeliharaan Perangkat Lunak: Biaya pemeliharaan, peningkatan, dan pengembangan perangkat lunak sistem bike sharing.
  - Pengelolaan Platform: Biaya pengelolaan platform dan infrastruktur teknologi yang mendasari sistem.
- Pengelolaan Anggota dan Layanan Pelanggan:
  - Biaya Registrasi dan Verifikasi Anggota: Biaya untuk mendaftar dan memverifikasi anggota baru.
  - Layanan Pelanggan: Biaya untuk menyediakan dukungan pelanggan, penanganan keluhan, dan layanan bantuan.
- Biaya Logistik dan Operasional:
  - Pemeliharaan Stasiun dan Lingkungan: Biaya untuk menjaga kebersihan dan kerapihan stasiun.
  - Logistik Operasional: Biaya untuk personel dan kendaraan yang diperlukan untuk mengelola operasional sehari-hari.
- Promosi dan Pemasaran:
  - Kampanye Pemasaran: Biaya untuk promosi, iklan, dan kampanye pemasaran guna meningkatkan kesadaran dan partisipasi.
- Asuransi dan Tanggung Jawab:
  - Asuransi Armada dan Pihak Ketiga: Biaya asuransi untuk sepeda, stasiun, dan perlindungan terhadap tanggung jawab hukum.

Agar perusahaan dapat tetap menjalankan bisnisnya, memprediksi permintaan yang akurat dapat menjadi solusi agar pengoperasian program bike sharing ini dapat menurunkan cost sehingga dapat meningkatkan profit.

### **Goals**
Berdasarkan permasalahan tersebut, maka, menyediakan jumlah sepeda yang memadai dalam berbagai situasi dan kondisi menjadi kunci. Ketidakseimbangan antara menyediakan terlalu banyak sepeda, yang dapat berdampak pada biaya penyedia, dan kekurangan sepeda, yang berpotensi mengecewakan pengguna, menjadi fokus utama.

### **Analytic Approach**
Jadi, kita perlu melakukan analisis data untuk mengidentifikasi pola di antara fitur-fitur yang membedakan pola penyewaan sepeda. Setelah itu, kita akan membuat model regresi sebagai alat untuk memprediksi jumlah sepeda yang diperlukan pada waktu tertentu. Model ini akan menjadi sumber daya berharga bagi Tim Operasional dalam mengoptimalkan distribusi sepeda pada saat yang tepat, meningkatkan kepuasan pelanggan terhadap sistem. Dengan menganalisis data dan membangun model regresi, kita dapat memberikan solusi yang efektif untuk meningkatkan efisiensi dan responsivitas layanan penyewaan sepeda.

### **Metric Evaluation**
Evaluasi metrik yang akan digunakan adalah RMSE, MAE, dan MAPE.

- RMSE adalah rata-rata akar kuadrat dari error.
- MAE adalah nilai absolut rata-rata dari error.
- MAPE adalah rata-rata proporsi error yang dihasilkan oleh model regresi.

Semakin rendah nilai RMSE, MAE, dan MAPE, semakin baik model memprediksi jumlah sepeda berdasarkan batasan fitur yang digunakan. Lebih khusus, nilai RMSE dan MAE yang lebih rendah menunjukkan tingkat akurasi yang lebih tinggi, sedangkan nilai MAPE yang lebih kecil mengindikasikan bahwa model memberikan perkiraan persentase yang lebih akurat.

Selain itu, jika model yang akan digunakan sebagai model akhir adalah model linear, kita dapat menggunakan R-squared atau Adjusted R-squared. Nilai R-squared digunakan untuk mengetahui seberapa baik model dapat merepresentasikan varians keseluruhan data. Semakin mendekati 1, maka semakin fit pula modelnya terhadap data observasi. Namun, metrik ini tidak valid untuk model non-linear.

## **Conclusion**
### **Exploratory Data Analysis**
- Sepeda paling banyak disewa pada saat cuaca clear, sedangkan paling sedikit disewa pada saat heavy rain/snow, dan bukan pada saat holiday.
- Registered Users lebih banyak menggunakan sepeda daripada Casual Users.
- Registered Users lebih banyak menggunakan sepada selama hari kerja, dan menurun pada akhir pekan, sedangkan casual users sebaliknya. Kemungkinan, hal ini disebabkan oleh registered users menggunakan sepeda untuk keperluan pekerjaan sehari-hari sedangkan casual users menggunakan sepeda untuk melakukan aktivitas ringan atau bersantai.
- Jam dengan jumlah peminjaman sepeda tertinggi adalah pada pukul 8 pagi, 5 dan 6 sore. Hal ini mendukung kemungkinan pada point sebelumnya karena sepeda banyak digunakan pada saat jam berangkat dan pulang bekerja.

### **Machine Learning Modeling**
- Di antara model regresi yang diuji yaitu Linear Regression, KNN Regressor, Decision Tree Regressor, Random Forest Regressor dan XGBoost Regressor, ternyata Model XGBoost yang yang unggul dalam hal RMSE, MAE dan MAPE.
- Model yang dipilih adalah model XGBosst yang sudah di tranfformasi ke skala logaritmik, kemudian ditransformasi kembali ke fungsi inverse. Parameter tuning terbaik pada model XGBoost ini adalah:
  - 'model__regressor__subsample': 0.8,
  - 'model__regressor__reg_alpha': 1.0,
  - 'model__regressor__n_estimators': 188,
  - 'model__regressor__max_depth': 7,
  - 'model__regressor__learning_rate': 0.16,
  - 'model__regressor__colsample_bytree': 0.9
- Model mengalami peningkatan performa (nilai RMSE, MAE & MAPE berkurang) setelah dilakukan hyperparamter tuning kedua, walaupun hanya sedikit.
  - RMSE, MAE & MAPE sebelum tuning : 43.64, 28.88, 0.49
  - RMSE, MAE & MAPE setelah tuning pertama : 45.39, 29.66, 0.50
  - RMSE, MAE & MAPE setelah tuning kedua : 43.56, 27.35, 0.28
- Nilai MAPE 0.28 memiliki arti bahwa rata-rata hasil prediksi model adalah 28% dari target. Maknanya, perkiraan jumlah unit rata-ratanya akan meleset kurang lebih sebesar 28% dari jumlah unit seharusnya.
- Nilai tersebut menjadikan model ini dapat dikategorikan ke dalam 'reasonable forecasting', namun masih terdapat beberapa hasil prediksi yang menyimpang baik lebih tinggi (overestimation) atau lebih rendah (underestimation).
- Hour menjadi fitur yang paling berpengaruh terhadap taget, yaitu count.
- Limitasi:
  - Project ini memiliki beberapa keterbatasan karena selalu ada outlier dalam praktiknya dan model mungkin gagal memprediksinya.
  - Datanya hanya 2 tahun (2011 - 2012) sehingga hanya dapat menunjukan pola 2 tahun.
