# Laporan Proyek : prediksi calon pembeli & regresi logistik

### Domain Proyek

Harga mobil merupakan salah satu faktor penting yang perlu diperhatikan saat membeli mobil baru. Harga mobil berbeda tergantung pada merek, tipe, dan tahun produksi mobil. Harga merupakan seberapa besar pengorbanan (sacrifice) yang diperlukan untuk membeli suatu produk sekaligus dijadikan sebagai indicator level of quality. Sedangkan (Kotler, 2015) mendefinisikan harga sebagai sejumlah uang yang dibayarkan atas barang dan jasa, atau jumlah nilai yang konsumen tukarkan dalam rangka mendapatkan manfaat dari memiliki atau menggunakan barang dan jasa.Oleh karena itu, dengan mempertimbangkan faktor-faktor tersebut, yang juga tersedia pada dataset, maka dapat diestimasi harga dari mobil tersebut dan melihat seberapa besar korelasi pengaruh faktor-faktor tersebut.

# Regresi Logistik (Logistic Regression)

Regresi logistik (Logistic Regression) adalah salah satu metode statistik yang digunakan untuk menganalisis hubungan antara variabel dependen biner (dichotomous) dengan satu atau lebih variabel independen. Variabel dependen biner adalah variabel yang hanya memiliki dua kemungkinan nilai, seperti "ya" atau "tidak," "sukses" atau "gagal," "positif" atau "negatif." Regresi logistik digunakan untuk memodelkan probabilitas bahwa variabel dependen akan mengambil salah satu dari dua nilai tersebut sebagai fungsi dari variabel independen.Regresi logistik (Logistic Regression) adalah salah satu metode statistik yang digunakan untuk menganalisis hubungan antara variabel dependen biner (dichotomous) dengan satu atau lebih variabel independen. Variabel dependen biner adalah variabel yang hanya memiliki dua kemungkinan nilai, seperti "ya" atau "tidak," "sukses" atau "gagal," "positif" atau "negatif." Regresi logistik digunakan untuk memodelkan probabilitas bahwa variabel dependen akan mengambil salah satu dari dua nilai tersebut sebagai fungsi dari variabel independen.

## Business Understanding

Pengembangan model prediksi harga mobil memiliki dampak yang sangat bermanfaat dalam mengambil keputusan oleh calon pembebeli mobil.Contohnya adalah prediksi harga mobil yang akurat dalam pengambilan keputusan dan mempertimbangkan apakah calon pembeli akan membeli mobil atau tidak.

### Pertanyaan Masalah
- Apa saja fitur-fitur yang paling signifikanataset eksplorasi yang mempengaruhi estimasi harga mobil?
- Bagaimana cara mengolah dataset mobil untuk membangun model prediksi harga yang akurat?
- Apa strategi yang efektif untuk meningkatkan nilai kinerja model prediksi harga mobil?
 
### Sasaran
Mengeksplorasi semua fitur yang tersedia pada dataset kemudian membuat melihat korelasi harga dari semua fitur yang sedia untuk melihat faktor apa saja yang paling berpengaruh sampai paling kurang berpengaruh terhadap harga rumah
Melakukan proses penyimpanan data dan persiapan data terhadap dataset agar dapat dibuat model predksi harga rumah
Melakukan beberapa variasi model untuk mendapatkan model yang paling baik dari beberapa model yang telah dibuat untuk prediksi harga rumah

### pernyataan Solusi
- Untuk eksplorasi fitur dilakukan Analisis Univariat dan Analisis Multivariat. Analisis Univariat dilakukan untuk mengeksploasi data numerik dan kategorik data. Analisis Multivariat dilakukan untuk melihat hubungan antar fitur. Teknik yang digunakan adalah menggunakan catplot, pairplot, dan heatmap untuk melihat Correlation Matrix dari fitur-fitur yang dimiliki.
- Agar diperoleh model prediksi yang baik maka dilakukan proses Data Wragling yang meliputi Data Gathering,Data Assessing ,dan Data Cleaning .
- Untuk mengetahui model kinerja dilakukan pengecekan kinerja dengan metrik evaluasi.
  
### Pemahaman Data 
Model ini menggunakan data yang telah ada sebelumnya dan terkumpul di platform Kaggle sebagai data sumbernya.Dengan nama prediksi calon pembeli & regresi logistik
URL : https://www.kaggle.com/code/ajieraflipamungkas/prediksi-calon-pembeli-regresi-logistik/notebook
Berikut merupakan detail dari _dataseat_ yang digunakan untuk pembuatan model:
- Kumpulan data berupa CSV
- Data terdiri dari 1000 __record_ dengan 7 buah fitur yang diukur
- Data terdiri dari 1 kategori dan 6 data numerik


### Variabel-variabel pada _dataset_ adalah sebagai berikut:
- bujur : koordinat geografis yang digunakan untuk menunjukkan posisi suatu titik dari arah utara ke selatan yang digunakan menentukan posisi suatu titik pada permukaan bumi (diukur dalam satuan derajat)
- garis lintang : koordinat geografis yang digunakan untuk menunjukkan posisi suatu titik dari arah timur ke barat yang digunakan untuk menentukan posisi suatu titik pada permukaan bumi (diukur dalam satuan derajat)
- Id : Merupakan angka dari data tersebut
- Usia : usia dari calon pembeli mobil
- Status : merujuk pada beberapa point
- Status Pembelian: Ini bisa berarti apakah mobil sudah dibeli atau belum. 
  Mungkin ada kategori seperti "dibeli" atau "belum dibeli".
- Status Kepemilikan: Ini dapat merujuk pada apakah mobil tersebut dimiliki 
  secara pribadi, disewa, atau mungkin masih dalam proses pembiayaan.
- Status Kendaraan: Ini bisa mencakup kondisi kendaraan seperti baru, bekas,  
  atau mungkin dalam kondisi tertentu seperti mobil demo.
- Status Pembayaran: Ini bisa merujuk pada apakah pembayaran telah dilakukan 
  sepenuhnya atau masih dalam proses pembayaran kredit atau cicilan.
- Kelamin: Jenis kelamin dari calon pembeli mobil(wanita atau laki-laki)
- Memiliki mobil :
- Penghasilan : merujuk pada jumlah pendapatan yang diperoleh oleh individu 
  atau rumah tangga.Penghasilan dapat diukur dalam berbagai interval 
  waktu,seperti bulanan atau tahunan.Ini adalah sumber dana yang digunakan 
  untuk memenuhi kebutuhan sehari-hari,membayar tagihan,menabung,berinvestasi 
  dan lain sebagainya.
- Beli mobil : prediksi calon pembeli yang ingin membeli mobil atau tidak.
  Untuk memahami data lebih lanjut,dilakukan Analisis Univariat dan Analisis Multivariat,serta Visualisasi Data
Analisis univariat adalah proses menganalisis data yang berkonsentrasi pada satu  variabel tunggal pada suatu waktu.Ini melibatkan pemeriksaan statik deskriptif dan visualisasi untuk memahami distribusi variabel tersebut dalam dataset.Sebaliknya,analisis multivariat melibatkan lebih dari dua variabel sekaligus dan bertujuan untuk memahami hubungan tentang pola dan iterabksi yang memungkinkan terjadi di antara fitur-fitur tersebut dalam dataset multidimensional.
Selain analisis,visualisasi data juga sangat penting dalam pemahaman dataset.Melalui visualisasi,kita dapat memperoleh pemahaman yang lebih mendalam tentang perilaku berbagai fitur dalam dataset.Beberapa teknik visualisai yang digunakan dalam proyek ini termasuk penggunaan catplot,yang berguna untuk memplot distribusi data kategorikal yang membantu dalam mengeksplorasi hubungan antara berbagai fitur dalam dataset;dan heatmap,yang memungkinkan kita untuk memvisulaisasikan kolerasi antar fitur dalam bentuk matriks,memudahkan identifikasi pola hubungan di antara variabel-variabel tersebut.
Berikut adalah hasil Exploratory Data Analysis(EDA),dimana Gamabar 1 merupakan EDA Analisis Univariat dan Gambar 2 merupakan EDA Analisis Multivariat. ![image](https://github.com/Nadiamalau/Proyek-Pertama-Prediktif-Analisis/assets/164990623/608cf83c-9f5f-4949-98a0-35b12567d1a1)

gambar 1a Pie Chart Value Counts

![image](https://github.com/Nadiamalau/Proyek-Pertama-Prediktif-Analisis/assets/164990623/9dfcab20-14a0-4655-b1f2-383a697a5751)

Dari data pie chart value count, terlihat bahwa 63,7% dari calon pembeli tertarik untuk membeli mobil, sementara 36,3% dari calon pembeli tidak memiliki keinginan untuk membeli mobil.

gambar 1b Analisis univariat(Data kategori)
![image](https://github.com/Nadiamalau/Proyek-Pertama-Prediktif-Analisis/assets/164990623/304dc196-544b-4bac-9020-f63e41fef301)

Gambar 1c.Analisis multivariat (Data Kategori)

![image](https://github.com/Nadiamalau/Proyek-Pertama-Prediktif-Analisis/assets/164990623/9e5e9ee4-b0d2-42f9-88df-fa0d2e46f391)

Gambar 2a.Analisis Univrait (Data Numerik)

Berdasarkan Gambar 1b, dapat dilihat bahwa distribusi kategori untuk
- jenis kelamin dapat diperhatikan bahwa nilai 0 adalah prediksi untuk jenis kelamin pria dan nilai 1 adalah prediksi jenis kelamin wanita
untuk data 
- distribusi status menikah,pada peringkat pertama yaitu sudah menikah terletak pada frekuensi 550,lalu pada peringkat kedua ada pada statut belum/tidak menikah terletak pada frekuensi 220 dan yang terakhir yaitu cerai pada frekuensi 210.
- status ekonomi yaitu kelas atas terletak pada frekuensi 498 dan selanjutnya kelas menengah dan kelas bawah terletak pada frekuensi 250.
- Beli vs tidak beli dan memiliki mobil,pada distribusi ini kemungkinan
  2.a Analisis Multivariate(Data Numerik)
  ![image](https://github.com/Nadiamalau/Proyek-Pertama-Prediktif-Analisis/assets/164990623/900b4f57-9ffc-4994-a544-f1a07212e244)
  
  Gambar 2c. Analisis Multivariat (Correlation Matrix)

Pada Gambar 2a tampak persebaran data 'Penghasilan' terhadap 'Beli_Mobil'. Dengan mengamati rata-rata 'Beli_Mobil' relatif terhadap fitur kategori di atas
* Kesimpulan akhir, fitur kategori memiliki pengaruh terhadap fitur numerik 'Penghasilan'.
Pada Gambar 2b, dengan menggunakan fungsi pairplot dari library seaborn, tampak terlihat relasi pasangan dalam dataset. Dari gambar, terlihat plot relasi masing-masing fitur numerik pada dataset. Pada pola sebaran data grafik pairplot, terlihat bahwa 'median_income' memiliki korelasi dengan fitur 'Beli_Mobil'. Sedangkan kedua fitur lainnya terlihat memiliki korelasi yang lemah karena sebarannya tidak membentuk pola

Terakhir, Gambar 2c merupakan Correlation Matrix menunjukkan hubungan antar fitur dalam nilai korelasi. Jika diamati, fitur 'median_income' memiliki skor korelasi yang cukup besar (0.76) dengan fitur 'Beli_Mobil'. Artinya, fitur 'median_house_value' berkorelasi cukup tinggi dengan keempat fitur tersebut. Sementara itu, fitur lainnya memiliki korelasi negatif sehingga fitur tersebut dapat dieliminasi.
* Pemodelan
Seperti yang dijelaskan di awal, model yang dipilih adalah model regresi karena merupakan salah satu algoritma yang paling umum digunakan dalam pembuatan model prediksi. Dalam bentuk yang sederhana, regresi terdiri dari perpotongan dan kemiringan yang dituliskan dalam rumusan berikut:
![image](https://github.com/Nadiamalau/Proyek-Pertama-Prediktif-Analisis/assets/164990623/febf5ece-9018-4c44-bdcb-c014647ed06c)
di mana:
![image](https://github.com/Nadiamalau/Proyek-Pertama-Prediktif-Analisis/assets/164990623/99d19776-b5f3-4b06-bbfc-7de67269a104)
Secara umum, regresi ini sendiri digunakan untuk memperkirakan pengaruh variabel prediktor terhadap variabel kriterium atau membuktikan ada atau tidaknya hubungan fungsional antara variabel bebas (X) dengan variabel terikat (y).

Namun begitu terdapat kelebihan dan kekurangan dari model regresi, yaitu:

Kelebihan regresi:

Kemudahan untuk digunakan
Kekuatan Prediktor dalam mengidentifikasi konfrontasi apa pengaruh yang diberikan oleh variabel prediktor (variabel independen) terhadap variabel lainnya (variabel dependen).
Dapat memprediksi nilai/tren di masa mendatang
Kelemahan dari model regresi adalah karena hasil ramalan dari analisis regresi merupakan nilai estimasi sehingga kemungkinan tidak sesuai dengan data aktual tetaplah ada.

Pada proyek yang dikerjakan, algoritma regresi yang coba dibandingkan adalah regresi linier, regresi ridge, random forest regressor , dan random forest regressor dengan hyperparamter tuning. Regresi linier adalah teknik analisis data yang memprediksi nilai data yang tidak diketahui dengan menggunakan nilai data lain yang terkait dan diketahui dimana secara matematis dimodelkan sebagai persamaan linier, regresi ridge merupakan metode estimasi koefisien regresi yang diperoleh melalui penambahan konstanta bias c, dan random forest adalah suatu hal algoritma yang digunakan pada klasifikasi data dalam jumlah yang besar dimana teknik klasifikasi random forest dilakukan melalui penggabungan pohon dengan melakukan pelatihan pada sampel data yang dimiliki.

Untuk meningkatkan model, dilakukan penyetelan hyperparamter . Adapun parameter yang di-tuning antara lain n_estimators', 'max_ depth', 'min_samples_split', dan 'min_samples_leaf. Untuk memudahkan proses tuning digunakan GridSearchCV. GridSearchCV itu sendiri merupakan bagian dari modul scikit-learn yang dapat digunakan untuk mendapatkan nilai hyperparameter secara otomatis. Grid Search adalah metode yang digunakan untuk mencari parameter yang paling tepat untuk meningkatkan performa model dengan mencoba seluruh kombinasi hyperparameter yang diberikan.

Berikut adalah nilai penyetelan parameter tuning

Berdasarkan hasil pengujian, terpilih grid.best_params_ yaitu
```
params = {'n_estimators' : [50,80,100],
          'max_depth' : [3,5,10],
           'min_samples_split':[2,3,4],
          'min_samples_leaf': [2,3,4]}
```
Berdasarkan hasil pengujian, terpilih grid.best_params_ yaitu
```
{'max_depth': 10,
 'min_samples_leaf': 4,
 'min_samples_split': 2,
 'n_estimators': 100}
```
Parameter dengan nilai inilah yang kemudian dibuat sebagai model.

## Evaluation
Adapun metrik yang sebagai alat ukur perfoma model yang dibuat antara lain **MSE · MAE · R<sup>2</sup>**. 

Berikut merupakan rumus dari masing-masing metrik yang digunakan:

$$ MAE = (1/n) Σ |y<sub>i</sub> - ŷ<sub>i</sub>| $$

$$ MSE = (1/n) Σ (y<sub>i</sub> - ŷ<sub>i</sub>)<sup>2</sup> $$

$$ R<sup>2</sup> = 1 - (MSE / Var(y)) $$

y<sub>i</sub> mewakili nilai yang diamati,
ŷ<sub>i</sub> mewakili nilai prediksi,
n adalah jumlah titik data,
Var(y) mewakili varians dari nilai yang diamati.

Berikut merupakan penjelasan kegunaan dari masing-masing metrik yang digunakan:
- MAE menghitung rata-rata dari selisih absolut antara nilai prediksi dan nilai aktual. Semakin kecil nilai MAE, semakin baik kualitas model tersebut.
- MSE menghitung rata-rata dari selisih kuadrat antara nilai prediksi dan nilai aktual. Semakin kecil nilai MSE, semakin baik kualitas model tersebut.
- R<sup>2</sup> digunakan untuk menilai seberapa besar pengaruh variabel independen tertentu terhadap variabel dependen

|     |Model 1|Model 2|Model 3|Model 4|
|---|---|---|---|---|
|R<sup>2</sup>|-43541.34341721751|-43436.738548114765|-0.47827417380660986|-0.3985567327101067|
|MSE|103.30647787801117|103.18231301023896|0.6019343818058577|0.5854795087680243|
|MAE|97.17220808367905|97.0557699747759|0.39289999999999997|0.38328028887778887|

Berdasarkan Tabel 1, secara umum Model 3 (RF1) dan Model 4 (RF2) menampilkan hasil performa yang lebih baik dimana masing-masing memiliki nilai R^2 yaitu sebesar -0.47827417380660986 dan -0.3985567327101067.

## REFERENSI
1. Hair Jr, Joseph F., et al. "Multivariate Data Analysis." Pearson College Division, 2010.
2. Hastie, Trevor, et al. "The Elements of Statistical Learning: Data Mining, Inference, and Prediction." Springer Science & Business Media, 2009.
3. Agresti, Alan. "An Introduction to Categorical Data Analysis." John Wiley & Sons, 2018.
4. Hosmer Jr, David W., Stanley Lemeshow, and Rodney X. Sturdivant. "Applied Logistic Regression." John Wiley & Sons, 2013.
5. King, Gary, et al. "Logistic Regression in Rare Events Data." Political Analysis 9.2 (2001): 137-163.
6. Menard, Scott. "Applied Logistic Regression Analysis." SAGE Publications, 2002.
7. Montgomery, Douglas C., et al. "Introduction to Linear Regression Analysis." John Wiley & Sons, 2012.
8. Japkowicz, Nathalie, and Mohak Shah. "Evaluating Learning Algorithms: A Classification Perspective." Cambridge University Press, 2011.
9. Gelman, Andrew, et al. "Bayesian Data Analysis." CRC Press, 2013.
10. McCullagh, Peter, and John A. Nelder. "Generalized Linear Models." Chapman and Hall/CRC, 1989.







							
							
							
							
							
							
							
							

						
							
							
							
							
										
											
											
											
											









  
