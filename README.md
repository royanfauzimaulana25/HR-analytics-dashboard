# *Human Resource* Dashboard
## Business Understanding

Jaya Jaya Maju merupakan salah satu perusahaan multinasional yang telah berdiri sejak tahun 2000. Ia memiliki lebih dari 1000 karyawan yang tersebar di seluruh penjuru negeri.

Walaupun telah menjadi menjadi perusahaan yang cukup besar, Jaya Jaya Maju masih cukup kesulitan dalam mengelola karyawan. Hal ini berimbas tingginya attrition rate (rasio jumlah karyawan yang keluar dengan total karyawan keseluruhan) hingga lebih dari 10%.

*Attrition rate* yang tinggi akan berdampak pada berbagai sektor perusahaan seperti kebutuhan finansial yang tinggi akibat biaya perekrutan terus menerus dan operasional yang terganggu akibat pegawai baru yang memerlukan adaptasi. Seluruh hal tersebut berujung akan berujung pada produktivitas dan kinerja perusahaan yang menurun serta citra buruk bagi perusahaan. Oleh Karena itu diharapkan dengan diketahuinya faktor yang mempengaruhi *attrition rate*, perusahaan dapat mencegah dan menghindari masalah tersebut.

### Permasalahan Bisnis
Tingkat *Attrition rate* akan berdampak pada kinerja perusahaan karena dapat mengganggu finansial dan operasional perusahaan akibar rekrutan baru. Adapun permasalahan yang dapat dirumuskan pada kasus ini adalah sebagai berikut : 

- Berapa jumlah pegawai yang mengalami *attrition* ?
- Pada umur berapakah pegawai yang mengalami *attrition* ?
- Apakah *salary / montyly income* pegawai mempengaruhi jumlah *attrition* ?
- Bagaimana *satisfaction* pegawai pada tiap *job role* pada perusahaan tersebut ?
- Berapa rata rata lama bekerja pegawai yang mengalami *attrition* ?  

### Cakupan Proyek

 Proyek ini akan membuat sebuah *business dashboard* yang berfungsi sebagai *monitoring* data pegawai yang berpengaruh pada *attrition rate* perusahaan.
 Melalui data yang disajikan dengan *dashboard* tersebut akan didapatkan *insight* bermakna untuk membuat sebuah kebijakan / keputusan dalam mengurangi *attrition rate*.  

 *Dashboard* akan dibuat menggunakan *Metabase* yang dihubungkan ke database *postgresql* yang dihosting di *platform Supabase*.

 Pada *Metabase* data akan dibuat menjadi sebuah model data yang nantinya akan proses menjadi beberapa fitur *dashboard* seperti :
 1. Fitur jumlah data terkait
 2. Visualisasi data dengan berbagai diagram / *chart*

### Persiapan

 Sumber Data : [Perusahaan Jaya Jaya Maju](https://github.com/dicodingacademy/dicoding_dataset/tree/main/employee)

 Setup *environment* :
 1. Instalasi *library* `Pandas` `Sqlalchemy`.
 2. Membuat *container* *`Metabase`* versi *`metabase/metabase:latest`* pada *`Docker`* dan dijalankan di *port* 3000:3000.

## *Business Dashboard*

Jelaskan tentang business dashboard yang telah dibuat. Jika ada, sertakan juga link untuk mengakses dashboard tersebut.

*Dashboard* yang dibuat terdiri atas visualisasi data dalam bentuk aktual jumlah data dan grafik. Adapun penjelasan tiap fitur dashboard yang dibuat sebagai berikut :
1. Fitur Jumlah data aktual yang memberikan nilai yang ada pada *dataset*.
![Data aktual](https://github.com/royanfauzimaulana25/HR-analytics-dashboard/assets/99244948/5fd6cb3e-dcac-4d5e-adc1-d6e7f2b5a363)
Gambar 1. Fitur data aktual.

Adapun fitur tersebut berfungsi untuk memonitor nilai aktual data saat ini yang terdiri atas :    
  - Jumlah Pegawai 
  - Jumlah pegawai yang mengalami *Attrition*
  - *Attrition Rate* yang membagi nilai pegawai mengalami *attrition* dengan jumlah keseluruhan pegawai. 
  - Rata rata umur pegawai yang mengalami*attrition*
  - Rata rata gaji pegawai yang mengalami *attrition*
  - Rata rata lama bekerja pegawai yang mengalami *attrition* di perusahaan Jaya Jaya Maju.

2. Grafik data bagi pegawai yang mengalami attrition berfungsi sebagai memonitor pembanding dan komposisi data yang terdiri atas :
   ![Grafik Data](https://github.com/royanfauzimaulana25/HR-analytics-dashboard/assets/99244948/c30e6aba-625e-4e60-91a6-71514138414e)
   Gambar 2. Grafik data *human resource*

  - Grafik *pie* *attrition by education* untuk melihat komposisi pegawai yang mengalami *attrition*
  - Grafik *bar* *attrition by age* untuk melihat perbandingan usia pegawai yang mengalami *attrition*
  - Grafik *pie* *attrition by gender* untuk melihat komposisi jenis kelamin pegawai yang mengalami *attrition*
  - *Pivot Table* *job roles satisfaction* untuk melihat tingkat kepuasaan pegawai yang mengalami *attrition* berdasarkan peran/ jabatannya. 
  - Grafik *bar* *attrition by salary* untuk melihat perbandingan gaji pegawai yang mengalami *attrition*
  - Grafik *Area* *attrition by total working experience* untuk melihat pengaruh lama bekerja di perusahaan terhadap pegawai yang mengalami attrition. 
  - grafik *bar* *attrition by job role* untuk melihat perbandingan jumlah pegawai yang mengalami *attrition* berdasarkan jabatannya. 


## *Conclusion*

Berdasarkan *dashboard* yang telah dirancang didapatkan beberapa insight terkait pegawai yang mengalami *attrition* yaitu :    
1. Tingkat *attrition* melebihi 10 % dari keselurahan pegawai yang menandakan bahwa terdapat tingkat keinginan *attrition* pegawai yang cukup tinggi yaitu mencapai 16.9 %.
2. Pegawai yang mengalami *attrition* rerata berumur 33 tahun dengan rerata lama bekerja 8 tahun. 
3. rerata gaji pegawai yang mengalami *attrition* yaitu berada di kisaran $5.500. 
4. Pegawai yang mengalami *attrition* didominasi oleh pegawai berpendidikan *life science* dan *medical* dimana untuk kedua pendidikan memiliki salary berkisar $2.500 - $5000. 
5. Berdasarkan pendidikan *life science dan medical* diketahui bahwa pegawai yang mengalami attrition berlatar belakang tersebut pada faktor *job role* didominasi *laboratory technician* dan memiliki pengalaman kerja kurang dari sama dengan 10 tahun. 
6. Adapun tingkat *satisfaction* untuk pendidikan *life science dan medical* di posisi *laboratory technican* berada pada level 1 yang dapat diartikan kurang memuaskan. 


### Rekomendasi *Action Items*

Rekomendasi yang dapat diterapkan oleh perusahaan berdasarkan hasil analisa dari *dasboard* yang telah dirancang dan kesimpulan diatas adalah sebagai berikut :    
1. Perusahaan dapat mengevaluasi kembali gaji pegawai pada posisi *laboratory technican* dan *research scienctist* agar *job satisfaction* dapat meningkat yang berpengaruh pada *attrition* agar dapat berkurang.
