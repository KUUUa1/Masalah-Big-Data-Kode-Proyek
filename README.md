# Masalah-Big-Data-Kode-Proyek
# Analisis Hasil Smart Home Dataset dengan Informasi Cuaca
Informasi Baru dari Korelasi Data:

Analisis korelasi antara data energi, cuaca, dan aktivitas penghuni dalam Smart Home Dataset with weather Information memberikan beberapa informasi baru:

Pengaruh Cuaca pada Konsumsi Energi:

Suhu dan konsumsi energi berkorelasi positif. Ketika suhu naik, konsumsi energi untuk pendinginan ruangan meningkat.
Kecepatan angin dan konsumsi energi berkorelasi negatif. Angin kencang membantu mendinginkan rumah, sehingga mengurangi kebutuhan pendinginan.

Pengaruh Aktivitas Penghuni pada Konsumsi Energi:

Konsumsi energi di dapur dan ruang tamu meningkat pada waktu makan dan malam hari, menunjukkan aktivitas penghuni.
Konsumsi energi di kamar tidur meningkat pada malam hari dan pagi hari, menunjukkan pola tidur penghuni.

Pengaruh Kombinasi Cuaca dan Aktivitas:

Pada hari panas dengan aktivitas tinggi, konsumsi energi mencapai puncaknya.
Pada hari dingin dengan aktivitas rendah, konsumsi energi minimal.

Analisis ini menunjukkan bahwa konsumsi energi rumah pintar dipengaruhi oleh cuaca dan aktivitas penghuni. Informasi ini dapat membantu:

Memprediksi konsumsi energi: 
Mengetahui pola konsumsi energi berdasarkan cuaca dan aktivitas dapat membantu memprediksi kebutuhan energi di masa depan.
Mengembangkan strategi hemat energi: Memahami faktor-faktor yang mempengaruhi konsumsi energi dapat membantu mengembangkan strategi hemat energi yang efektif.
Meningkatkan efisiensi energi: Mengoptimalkan sistem pemanas, pendingin, dan peralatan elektronik berdasarkan cuaca dan aktivitas dapat meningkatkan efisiensi energi rumah.
Kinerja Klasifikasi:
Model klasifikasi yang dilatih pada dataset ini dapat memprediksi kategori konsumsi energi (tinggi, sedang, rendah) dengan akurasi yang cukup tinggi, misalnya 85%.

Matriks Confusion:

Matriks confusion menunjukkan performa model klasifikasi dalam membedakan kategori konsumsi energi. Matriks ini membantu mengidentifikasi kesalahan klasifikasi dan area yang perlu ditingkatkan.

Loss Performance:

Kehilangan kinerja (loss) menunjukkan seberapa besar perbedaan antara prediksi model dan nilai aktual. Nilai loss yang rendah menunjukkan performa model yang baik.

Hasil Klasifikasi:
Hasil klasifikasi menunjukkan kategori konsumsi energi untuk setiap periode waktu dalam dataset. Informasi ini dapat membantu visualisasi pola konsumsi energi dan mengidentifikasi periode penggunaan energi yang tinggi

Penjelasan kode SVM :

1.	Impor Modul: Langkah pertama adalah mengimpor modul-modul Python yang akan digunakan dalam skrip, seperti modul untuk berinteraksi dengan sistem operasi, membuka URL, menangani file arsip, dan lainnya.
  
2.	Pengaturan Variabel: Variabel diatur untuk menentukan ukuran blok untuk pembacaan data, daftar sumber data yang akan diunduh, dan path untuk menyimpan data dan hasil kerja.
	
4.	Persiapan Lingkungan: Langkah ini melibatkan membersihkan path yang telah ada sebelumnya, membuat path baru untuk menyimpan data, dan melepas mount direktori input Kaggle jika ada.
  
5.	Loop Unduhan dan Ekstraksi: Melakukan loop melalui setiap sumber data yang telah ditentukan, mendekode URL, mengunduh data, dan mengekstraknya ke direktori yang sesuai.
  
6.	Impor Modul dan Data: Mengimpor modul yang diperlukan untuk analisis data serta membaca data dari file CSV yang telah diekstrak sebelumnya.
     
7.	Pemrosesan Data: Melibatkan pembersihan dan persiapan data untuk analisis lebih lanjut, seperti memberi nama kolom dan menghapus kolom yang tidak diperlukan.

8.	Analisis Deskriptif: Menampilkan statistik deskriptif, menghitung persentase nilai yang hilang, dan memberikan informasi tentang dataset

9.	Visualisasi Data: Membuat visualisasi data menggunakan plot sebar dan diagram kotak untuk menganalisis distribusi data.

10. Pemodelan Pembelajaran Mesin: Memisahkan fitur dan target, melakukan penskalaan fitur, membagi data menjadi data latih dan data uji, melatih model pembelajaran mesin, dan mengevaluasi kinerjanya menggunakan metrik yang sesuai.


Penjelasan kode ANN:

1.	Preprocessing Data:
Kolom yang tidak relevan seperti "Unnamed : 0" dihapus, dan data numerik dinormalisasi menggunakan MinMaxScaler untuk memastikan semua fitur memiliki skala yang serupa.

3.	Linear Regression:
Model regresi linear (LinearRegression) diuji dengan membagi data menjadi train dan test set. Skor akurasi pada data train dan test ditampilkan, dengan nilai yang sangat tinggi, menunjukkan bahwa model ini sangat baik dalam memprediksi

5.	Artificial Neural Network (ANN):
Selanjutnya, sebuah model jaringan saraf tiruan (ANN) dengan dua lapisan (32 neuron pada lapisan pertama dan 1 neuron pada lapisan kedua) dibuat. Model ini di-compile dengan optimizer Adam dan loss function mean squared error.

7.	Perbandingan Prediksi Linear Regression dan ANN:
Scatter plot digunakan untuk membandingkan prediksi dari kedua model. Hasil menunjukkan bahwa model ANN memiliki akurasi yang lebih tinggi dibandingkan dengan regresi linear.

9.	Grafik Training dan Validasi:
Grafik training loss dan validation loss, serta training accuracy dan validation accuracy, digunakan untuk memantau kinerja model selama proses pelatihan. Epoch terbaik ditandai dengan titik biru, menunjukkan
performa optimal model.

Dari hasil evaluasi, ditemukan bahwa model ANN memiliki skor R2 yang lebih tinggi pada data test dibandingkan dengan regresi linear, yaitu sebesar 0.9999. Dengan demikian, disimpulkan bahwa metode ANN lebih baik dalam memprediksi data suhu, kelembapan, dan indeks panas daripada regresi linear, dengan akurasi yang lebih tinggi. Oleh karena itu, disarankan untuk menggunakan model ANN dalam melakukan prediksi pada dataset ini.
