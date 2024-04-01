# Laporan Proyek : prediksi calon pembeli & regresi logistik

### Domain Proyek

Harga mobil merupakan salah satu faktor penting yang perlu diperhatikan saat membeli mobil baru. Harga mobil berbeda tergantung pada merek, tipe, dan tahun produksi mobil. Harga merupakan seberapa besar pengorbanan (sacrifice) yang diperlukan untuk membeli suatu produk sekaligus dijadikan sebagai indicator level of quality. Sedangkan (Kotler, 2015) mendefinisikan harga sebagai sejumlah uang yang dibayarkan atas barang dan jasa, atau jumlah nilai yang konsumen tukarkan dalam rangka mendapatkan manfaat dari memiliki atau menggunakan barang dan jasa.Oleh karena itu, dengan mempertimbangkan faktor-faktor tersebut, yang juga tersedia pada dataset, maka dapat diestimasi harga dari mobil tersebut dan melihat seberapa besar korelasi pengaruh faktor-faktor tersebut.

## Business Understanding

Pengembangan model prediksi harga mobil memiliki dampak yang sangat bermanfaat dalam mengambil keputusan oleh calon pembebeli mobil.Contohnya adalah prediksi harga mobil yang akurat dalam pengambilan keputusan dan mempertimbangkan apakah calon pembeli akan membeli mobil atau tidak.

### Pertanyaan Masalah
- Apa saja fitur-fitur yang paling signifikanataset eksplorasi yang mempengaruhi estimasi harga mobil?
- Bagaimana cara mengolah dataset mobil untuk membangun model prediksi harga yang akurat?
- Apa strategi yang efektif untuk meningkatkan nilai kinerja model prediksi harga mobil?
 
### Sasaran

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

Gambar 1a.Analisis Univariat (Data Kategori)

![image](https://github.com/Nadiamalau/Proyek-Pertama-Prediktif-Analisis/assets/164990623/9e5e9ee4-b0d2-42f9-88df-fa0d2e46f391)


						
							
							
							
							
							
							
							
							

						
							
							
							
							
										
											
											
											
											

				
					
			


						
			
							
							
							
							
							
							
							
					
	

						
							
							
							
							
							
							
							
							

						
							
							
							
							
										
											
											
											
											









  
