# Customer Churn Analysis Mengidentifikasi dan Mengurangi Tingkat Kehilangan Pelanggan
## 📝 Deskripsi Singkat

Ini adalah proyek analisis data pertama saya yang dibuat menggunakan **SQL (MySQL)**. Proyek ini saya kerjakan sebagai bentuk latihan untuk menerapkan pengetahuan yang telah saya pelajari dari sebuah platform pembelajaran online. Fokus utama dari proyek ini adalah untuk memahami **faktor-faktor yang memengaruhi pelanggan melakukan churn** (berhenti berlangganan) di perusahaan telekomunikasi.

---

## 🎯 Tujuan Proyek

Proyek ini bertujuan untuk:
- Mengidentifikasi **faktor-faktor utama** yang mendorong churn pelanggan.
- Menganalisis **segmen pelanggan yang paling berisiko churn**, terutama mereka dengan kontrak bulanan dan biaya tertentu.
- Memberikan **rekomendasi strategis** kepada perusahaan telekomunikasi untuk:
  - Meningkatkan **retensi pelanggan**,
  - Mengurangi **tingkat kehilangan pelanggan** di masa mendatang.

---

## 📂 Sumber Data

Dataset yang digunakan dalam proyek ini adalah dataset publik dari **Kaggle** dengan judul:

> **Telco Customer Churn**  
> 📎 [Link Dataset (Kaggle)](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

Dataset yang digunakan dalam proyek ini memuat informasi pelanggan dari sebuah perusahaan telekomunikasi. Di dalamnya terdapat data demografis pelanggan, jenis layanan yang mereka gunakan seperti internet dan layanan keamanan, serta rincian biaya bulanan dan durasi mereka berlangganan. Selain itu, dataset ini juga mencatat status churn, yaitu apakah pelanggan tersebut masih aktif berlangganan atau sudah berhenti menggunakan layanan perusahaan. Data ini sangat relevan untuk dianalisis karena mencakup berbagai aspek penting yang dapat memengaruhi perilaku pelanggan dalam mengambil keputusan untuk tetap atau meninggalkan layanan.

---

## 🧪 Metodologi & Tools

### 🔍 Metodologi Analisis

Proyek ini menggunakan pendekatan eksplorasi data untuk memahami pola dan faktor yang memengaruhi pelanggan melakukan churn. Langkah-langkah utama metodologinya adalah:

1. **Eksplorasi Data Awal (EDA)**  
   Langkah pertama dimulai dengan eksplorasi data awal (EDA) untuk memeriksa struktur tabel, jenis kolom, serta distribusi data secara umum. Pada tahap ini, juga dihitung jumlah total pelanggan yang churn dan jenis kontrak yang tersedia dalam data.

2. **Analisis Korelasi Churn**  
    Langkah kedua dilakukan analisis korelasi antara churn dan beberapa variabel kunci seperti jenis kontrak (Contract), biaya bulanan (MonthlyCharges), durasi berlangganan (Tenure), serta penggunaan layanan tambahan seperti OnlineSecurity dan InternetService. Dari analisis ini, mulai terlihat segmen-segmen pelanggan yang memiliki kecenderungan churn lebih tinggi.

3. **Segmentasi Pelanggan Berisiko Tinggi**  
   Fokus kemudian diarahkan pada segmentasi pelanggan yang paling berisiko, yaitu pelanggan dengan kontrak bulanan (Month-to-month) dan biaya bulanan sekitar $70 hingga $75. Segmen ini dianalisis lebih dalam untuk melihat pola-pola berdasarkan layanan keamanan yang digunakan, jenis layanan internet yang dipilih, serta lama pelanggan bertahan sebelum melakukan churn. Pendekatan ini membantu menghasilkan insight yang lebih tajam dan dapat digunakan untuk merancang strategi retensi pelanggan yang lebih efektif.

---

## ❓ Pertanyaan Bisnis yang Dijawab

Dalam proyek ini, saya mencoba menjawab beberapa pertanyaan bisnis utama yang berkaitan dengan perilaku pelanggan dan alasan di balik keputusan mereka untuk berhenti berlangganan (*churn*). Pertanyaan-pertanyaan ini dirancang untuk menggali pola dan faktor risiko yang dapat digunakan perusahaan dalam menyusun strategi retensi pelanggan. Adapun pertanyaan-pertanyaan spesifik yang dianalisis adalah sebagai berikut:

1. **Mengapa pelanggan dengan kontrak bulanan (*Month-to-month*) memiliki tingkat churn yang paling tinggi dibandingkan jenis kontrak lainnya?**

2. **Apa faktor utama yang mendorong churn di kalangan pelanggan dengan kontrak bulanan dan biaya bulanan sekitar $73?**

3. **Mengapa sebagian besar pelanggan dalam segmen tersebut tidak menggunakan layanan keamanan seperti *Online Security*, *Tech Support*, dan *Device Protection*?**

4. **Apa peran jenis layanan internet—khususnya penggunaan *Fiber Optic*—terhadap meningkatnya churn di segmen tertentu?**

5. **Mengapa churn cenderung lebih tinggi pada 0–6 bulan pertama masa berlangganan pelanggan?**

Pertanyaan-pertanyaan ini menjadi dasar dalam melakukan eksplorasi data, segmentasi pelanggan, dan penarikan insight yang dapat digunakan untuk pengambilan keputusan strategis oleh pihak manajemen.

---

## 🔍 Temuan (Key Insights)

Berikut adalah temuan utama yang diperoleh dari analisis data churn pelanggan pada perusahaan telekomunikasi:

- **Pelanggan dengan kontrak *Month-to-month* menunjukkan tingkat churn yang secara signifikan lebih tinggi** dibandingkan pelanggan dengan kontrak jangka panjang (*One year* atau *Two year*). Hal ini menunjukkan bahwa fleksibilitas tinggi tanpa komitmen jangka panjang dapat meningkatkan risiko churn.

- **Sebanyak lebih dari 90% pelanggan dengan kontrak bulanan dan biaya bulanan sekitar $73 yang churn adalah pengguna layanan *Fiber Optic***. Ini mengindikasikan potensi isu terkait **value for money** atau persepsi kualitas layanan di segmen ini.

- **Lebih dari 90% pelanggan dalam segmen berisiko tinggi ini tidak berlangganan layanan keamanan atau dukungan teknis**, seperti *Online Security*, *Tech Support*, dan *Device Protection*. Kurangnya layanan pendukung ini dapat menjadi salah satu penyebab utama rendahnya loyalitas pelanggan.

- **Sekitar 57% pelanggan churn pada segmen tersebut terjadi pada 0–6 bulan pertama masa berlangganan** yang dapat mengindikasikan adanya masalah dalam proses onboarding, pengalaman awal pelanggan, atau ekspektasi yang tidak terpenuhi sejak awal.

---

## 💡 Rekomendasi (Actionable Recommendations)

Berdasarkan temuan yang diperoleh dari analisis churn pelanggan, berikut adalah beberapa rekomendasi strategis yang dapat diterapkan oleh perusahaan untuk meningkatkan retensi pelanggan:

1. **Tawarkan paket bundling yang mencakup layanan keamanan dan dukungan teknis**, seperti *Online Security* dan *Tech Support*, khususnya kepada pelanggan *Fiber Optic* dengan kontrak *Month-to-month*. Strategi ini dapat meningkatkan persepsi nilai dan keterikatan pelanggan terhadap layanan.

2. **Perkuat komunikasi manfaat dari setiap layanan yang ditawarkan** terutama layanan tambahan seperti keamanan dan dukungan teknis. Edukasi yang tepat dapat membantu pelanggan memahami manfaat dari biaya bulanan yang mereka bayarkan.

3. **Optimalkan proses onboarding pelanggan baru** dengan memberikan panduan, dukungan proaktif, atau komunikasi rutin selama 3 bulan pertama. Hal ini bertujuan untuk menciptakan pengalaman awal yang positif dan mengurangi churn dini.

4. **Berikan insentif khusus atau diskon progresif kepada pelanggan *Month-to-month* yang loyal untuk beralih ke kontrak jangka panjang**. Strategi ini dapat membantu menstabilkan pendapatan dan menurunkan tingkat churn secara keseluruhan.

5. **Lakukan segmentasi pelanggan secara berkala berdasarkan risiko churn dan nilai pelanggan**, lalu terapkan pendekatan personalisasi dalam retensi, misalnya dengan pengingat layanan yang belum diaktifkan atau penawaran khusus berdasarkan riwayat penggunaan.


---

