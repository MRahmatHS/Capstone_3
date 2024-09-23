# **E-COMMERCE CUSTOMER CHURN**

#### By : **M.RAHMAT HIDAYAT SYACHRUDIN**
---
---
### **Business Problem Understanding**
---
### **Context**
Dalam era persaingan bisnis e-commerce yang semakin ketat, mempertahankan pelanggan menjadi elemen kunci untuk menjaga keberlanjutan dan pertumbuhan perusahaan. Customer churn, atau hilangnya pelanggan yang beralih ke layanan atau produk lain, menjadi ancaman signifikan yang dapat memengaruhi profitabilitas secara langsung. Saat pelanggan memilih untuk meninggalkan platform e-commerce dan beralih ke kompetitor, perusahaan tidak hanya kehilangan pendapatan, tetapi juga dihadapkan pada biaya besar untuk mendapatkan pelanggan baru—biaya ini bisa mencapai lima kali lipat dari upaya mempertahankan pelanggan yang sudah ada. Oleh karena itu, upaya retensi pelanggan harus menjadi fokus utama dalam strategi bisnis. Dengan semakin banyaknya pilihan platform e-commerce, inovasi, personalisasi layanan, dan penawaran promosi yang menarik menjadi krusial untuk menjaga loyalitas pelanggan. Melalui analisis data churn, perusahaan dapat mengidentifikasi pola perilaku pelanggan yang cenderung beralih dan merumuskan langkah-langkah preventif, seperti pengembangan program loyalitas, peningkatan kualitas layanan, atau personalisasi pengalaman berbelanja. Strategi retensi yang berbasis data ini tidak hanya membantu mengurangi churn, tetapi juga meningkatkan kepuasan dan loyalitas pelanggan, yang pada akhirnya akan mendukung keberhasilan jangka panjang perusahaan di pasar e-commerce yang dinamis.
### **Problem Statement**
Masalah churn pelanggan adalah tantangan signifikan bagi bisnis e-commerce, di mana hilangnya pelanggan secara terus-menerus dapat mengancam pendapatan jangka panjang. Untuk menjaga stabilitas bisnis, perusahaan perlu mampu memprediksi pelanggan yang berisiko churn sehingga dapat mengambil langkah proaktif, seperti menawarkan promosi atau insentif yang tepat sasaran. Namun, memberikan promosi kepada pelanggan yang sebenarnya tidak akan churn bisa menyebabkan kerugian operasional, karena sumber daya digunakan secara tidak efektif. Di tengah persaingan yang ketat, biaya akuisisi pelanggan baru semakin tinggi, sehingga mempertahankan pelanggan yang ada menjadi lebih krusial. Jika gagal, perusahaan tidak hanya kehilangan pendapatan, tetapi juga berisiko mengalami penurunan reputasi, terutama jika pelanggan yang churn menyampaikan ulasan negatif. Oleh karena itu, strategi retensi yang efektif dan berbasis data sangat diperlukan untuk mengarahkan promosi kepada pelanggan yang benar-benar berisiko, memastikan efisiensi biaya, menjaga loyalitas pelanggan, dan mendukung pertumbuhan bisnis secara berkelanjutan.
### **Goals**
Tujuan analisis ini adalah mengembangkan model prediksi machine learning untuk secara akurat mengidentifikasi pelanggan yang berpotensi churn, sehingga perusahaan e-commerce dapat mengoptimalkan strategi promosi dengan lebih efisien. Dengan fokus pada pelanggan yang memiliki probabilitas tinggi untuk churn, perusahaan dapat mengurangi kerugian pendapatan yang tidak perlu dan memaksimalkan efektivitas biaya pemasaran. Selain itu, analisis ini membantu perusahaan memahami faktor-faktor yang memengaruhi churn, memungkinkan mereka untuk menyusun strategi retensi yang lebih personal dan efektif. Hasil akhirnya adalah peningkatan loyalitas pelanggan, penurunan tingkat churn, serta peningkatan profitabilitas dan daya saing di pasar e-commerce yang kompetitif.
### **Analytic approach**
Pertama, kami akan menganalisis data pelanggan untuk mengidentifikasi pola yang memisahkan pelanggan yang cenderung churn dari mereka yang tidak. Selanjutnya, kami akan mengembangkan model klasifikasi yang dapat memperkirakan kemungkinan pelanggan akan churn, sehingga perusahaan dapat menerapkan strategi retensi yang lebih tepat sasaran untuk mengurangi tingkat churn dan mempertahankan basis pelanggan mereka.
### **Metric Evaluation**
- True Positive (TP) : pelanggan churn dengan benar dari total pelanggan yang churn
- True Negative (TN) : pelanggan non-churn berhasil diklasifikasikan dengan benar
- False Positive (FP): pelanggan non-churn yang salah diklasifikasikan sebagai churn
- False Negative (FN): pelanggan churn yang salah diklasifikasikan sebagai non-churn

Jika kita memfokuskan pada empat parameter berikut, maka evaluasi metrik yang digunakan adalah:
1. Accuracy: Digunakan untuk menilai sejauh mana model dapat secara akurat memprediksi pelanggan yang akan churn dibandingkan dengan keseluruhan prediksi yang dibuat oleh model.
2. Precision: Digunakan untuk mengukur tingkat ketepatan model dalam memprediksi pelanggan yang akan churn, bertujuan untuk menghindari kesalahan prediksi yang dapat mengakibatkan penggunaan anggaran promosi yang tidak efektif.
3. Recall: Digunakan untuk mengevaluasi kemampuan model dalam memprediksi pelanggan yang akan churn dibandingkan dengan semua pelanggan yang sebenarnya churn. Metrik ini penting untuk menilai seberapa baik model kita dalam mengidentifikasi seluruh pelanggan yang akan churn.
4. F1-Score: Merupakan kombinasi dari precision dan recall, yang memberikan gambaran menyeluruh tentang performa model dalam prediksi churn.

> Namun, di antara keempat metrik tersebut, karena prioritas perusahaan adalah memastikan anggaran promosi tepat sasaran untuk pelanggan yang benar-benar churn, fokus utama kita akan berada pada Recall. Hal ini disebabkan karena recall mampu menunjukkan sejauh mana model mampu mengidentifikasi semua pelanggan yang akan churn.

---
---

### **Feature Importance**
> Dari visualisasi Feature Importance di atas, kita dapat mengidentifikasi beberapa fitur yang memiliki pengaruh paling besar dalam memprediksi churn pelanggan. Berikut interpretasi dari setiap fitur yang menonjol dan relevansinya terhadap business knowledge:

**1. Tenure :**
- Interpretasi: Fitur ini merupakan faktor terpenting dalam model prediksi churn. "Tenure" mengacu pada lamanya pelanggan telah menggunakan layanan. Biasanya, semakin lama pelanggan tetap bersama layanan, semakin kecil kemungkinan mereka untuk berhenti (churn), karena mereka cenderung memiliki pengalaman positif atau merasa lebih terikat dengan layanan.
- Business Knowledge: Ini menunjukkan bahwa perusahaan harus fokus pada program loyalitas atau insentif untuk pelanggan jangka panjang agar tetap setia. Memahami pola perilaku pelanggan dengan masa layanan yang panjang juga dapat memberikan wawasan tentang bagaimana meningkatkan retensi pelanggan baru.

**2. PreferedOrderCat :**
- Interpretasi: Preferensi pelanggan dalam jenis produk atau kategori yang mereka pesan juga berpengaruh dalam prediksi churn. Pelanggan dengan preferensi yang spesifik memungkinkan memiliki loyalitas yang lebih kuat terhadap produk tertentu.
- Business Knowledge: Mengetahui preferensi kategori pesanan dapat membantu perusahaan menyusun strategi pemasaran yang lebih tepat sasaran. Dengan mempersonalisasi pengalaman berdasarkan preferensi, perusahaan dapat meningkatkan pengalaman pelanggan dan mengurangi churn.

**3. Complain :**
- Interpretasi: Keluhan adalah indikator kuat lainnya. Pelanggan yang sering mengajukan keluhan lebih memungkinkan untuk churn, terutama jika masalah mereka tidak diatasi dengan baik.
- Business Knowledge: Mengelola keluhan pelanggan secara efektif dapat secara signifikan mengurangi churn. Perusahaan perlu meninjau kembali sistem penanganan keluhan, meningkatkan layanan pelanggan, dan menangani masalah dengan cepat untuk menghindari kehilangan pelanggan.

**4. DaySinceLastOrder :**
- Interpretasi: Fitur ini menunjukkan waktu yang telah berlalu sejak pesanan terakhir pelanggan. Jika seorang pelanggan belum melakukan pemesanan dalam waktu lama, kemungkinan mereka akan churn lebih tinggi.
- Business Knowledge: Perusahaan dapat menggunakan data ini untuk menyusun kampanye pemasaran ulang (retargeting) dan menawarkan promosi khusus kepada pelanggan yang telah lama tidak aktif.

**5. NumberOfAddress :**
- Interpretasi: Jumlah alamat yang terdaftar dapat berhubungan dengan tingkat kepercayaan dan fleksibilitas yang diinginkan oleh pelanggan. Misalnya, pelanggan dengan lebih banyak alamat memungkinkan lebih sering melakukan pembelian.
- Business Knowledge: Perusahaan bisa menilai bagaimana memberikan fleksibilitas dalam pengiriman atau pelayanan pelanggan dengan alamat lebih dari satu. Program yang mengakomodasi pelanggan dengan mobilitas tinggi dapat membantu mengurangi churn.

**6. SatisfactionScore :**
- Interpretasi: Skor kepuasan pelanggan sangat penting dalam menentukan apakah pelanggan akan churn atau tidak. Pelanggan dengan skor kepuasan rendah lebih memungkinkan untuk churn.
- Business Knowledge: Perusahaan perlu fokus pada survei kepuasan pelanggan secara teratur dan meningkatkan pengalaman pelanggan berdasarkan umpan balik untuk mengurangi churn.

**7. WarehouseToHome :**
- Interpretasi: Jarak antara gudang dan rumah pelanggan juga tampaknya berpengaruh terhadap churn. Pengiriman yang cepat atau efisien memainkan peran penting dalam keputusan pelanggan untuk tetap menggunakan layanan.
- Business Knowledge: Perusahaan perlu mempertimbangkan bagaimana optimisasi rantai pasokan dan logistik dapat meningkatkan pengalaman pengiriman dan, pada akhirnya, mengurangi churn.

Secara keseluruhan, fitur-fitur ini memberikan wawasan penting bagi bisnis untuk merancang strategi retensi pelanggan yang lebih efektif. Perusahaan dapat memfokuskan upaya mereka pada kelompok pelanggan yang lebih berisiko churn, misalnya, dengan memberikan perhatian ekstra pada pelanggan dengan keluhan yang belum terselesaikan, atau pada mereka yang belum melakukan pesanan dalam jangka waktu yang lama.

---
---
---
## **Kesimpulan dan Rekomendasi**
### **1. Kesimpulan**
> Berdasarkan analisis yang telah dilakukan melalui berbagai langkah eksplorasi, preprocessing, modeling, dan evaluasi model, berikut adalah beberapa poin kesimpulan penting:
**Distribusi Pelanggan yang Churn**
- Dari Distribusi Pelanggan yang Churn, ditemukan bahwa proporsi pelanggan yang churn adalah 14.71%, menunjukkan bahwa mayoritas pelanggan masih tetap menggunakan layanan. Namun, persentase churn ini tetap signifikan dan perlu diperhatikan, terutama dalam rangka mempertahankan basis pelanggan.

**Handling Missing Values dan Outliers**
- Missing values yang ditemukan pada beberapa kolom seperti Tenure, WarehouseToHome, dan DaySinceLastOrder ditangani dengan menghapus data yang hilang, mengingat persentase yang kecil.
- Meskipun terdapat outliers pada beberapa fitur, seperti Tenure dan CashbackAmount, outliers dipertahankan karena mereka mencerminkan realitas dalam data yang berhubungan dengan perilaku pelanggan.

**Feature Importance**
- Tenure adalah fitur yang paling penting dalam memprediksi churn. Pelanggan dengan masa langganan yang lebih lama cenderung tidak churn.
- Fitur lainnya seperti Preferred Order Category, Complain, dan Day Since Last Order juga berperan penting dalam memprediksi churn.
- Kepuasan pelanggan dan jumlah keluhan memiliki dampak signifikan terhadap keputusan pelanggan untuk churn.

> **Evaluasi Model**
![image](https://github.com/user-attachments/assets/c82cec66-eb2f-4082-909d-10adad130d27)

 **Prediksi Churn untuk Perusahaan E-commerce Menggunakan Machine Learning**

 **1. Tujuan Project**
Tujuan dari project ini adalah untuk memprediksi apakah seorang pelanggan akan melakukan churn (berhenti menggunakan layanan) atau tetap setia menggunakan layanan e-commerce. Menggunakan **machine learning**, kita dapat mengidentifikasi pelanggan yang memiliki risiko churn, sehingga perusahaan dapat memberikan penawaran atau promosi yang lebih tepat sasaran untuk mencegah churn dan mengurangi kerugian.

---

 **2. Evaluasi Hasil Model XGBoost**
Model terbaik yang digunakan untuk prediksi churn adalah **XGBoost**. Berikut adalah hasil performa dari model berdasarkan **classification report**:

- **Precision:**
    - Pelanggan yang tidak churn: 93%
    - Pelanggan yang churn: 95%

- **Recall:**
    - Pelanggan yang tidak churn: 95%
    - Pelanggan yang churn: 93%

- **F1-Score:**
    - Pelanggan yang tidak churn: 94%
    - Pelanggan yang churn: 94%

Model ini berhasil mencapai tingkat akurasi keseluruhan sebesar **94%**, menunjukkan bahwa model cukup handal dalam memprediksi pelanggan yang akan churn dan tidak churn.

---

 **3. Biaya Tanpa Menggunakan Machine Learning**
Tanpa menggunakan **machine learning**, perusahaan harus melakukan promosi kepada semua pelanggan secara merata untuk mengurangi risiko churn. Ini menyebabkan pemborosan besar, karena perusahaan memberikan promosi kepada pelanggan yang sebenarnya tidak akan churn. Berikut adalah perhitungan biaya promosi dan kerugian jika perusahaan tidak menggunakan machine learning:

| Target | Biaya |
| --- | --- |
| asumsi semua pelanggan menerima biaya promosi | 50 USD / pelanggan |
|asumsi pelanggan yang akan churn menerima biaya promosi  | 5x dari biaya pelanggan yg tdk churn `atau` 250 USD|

 **Biaya Promosi:**
- Semua pelanggan menerima promosi: `50 USD x 1426 pelanggan = 71.300 USD`
- Biaya yang tepat sasaran (pelanggan churn yang benar-benar perlu promosi): `250 USD x 715 pelanggan = 178.750 USD`

 **Total Biaya yang Tidak Tepat Sasaran:**
- **71.300 USD** - **178.750 USD** = **- 107.450 USD** kerugian untuk **1426 pelanggan**.

Tanpa menggunakan machine learning, perusahaan akan menghadapi kerugian sebesar **- 107.450 USD** per sekali Campaign.

---

 **4. Menggunakan Machine Learning (ML)**
Dengan menggunakan model **XGBoost** yang telah di-tuning, perusahaan dapat menghemat pengeluaran promosi dengan fokus hanya pada pelanggan yang diprediksi akan churn. Berikut adalah estimasi pengeluaran dan penghematan dengan menggunakan model ML:

 **Biaya Promosi Tepat Sasaran (FP + TP):**
- (654 pelanggan FP + 1426 pelanggan TP) x 50 USD = **104.000 USD**

 **Biaya Kehilangan Pelanggan (FN):**
- 53 pelanggan FN x 250 USD = **13.250 USD**

 **Biaya Tepat Sasaran (TP):**
- 662 pelanggan TP x 250 USD = **165.500 USD**

 **Total Pengeluaran dengan ML:**
- **104.000  USD** (biaya FP + TP) + **13.250 USD** (biaya kehilangan FN) = **177.250 USD**

 **Biaya Promosi:**
- **165.500 USD** dari promosi tepat sasaran.

 **Total Biaya yang Tidak Tepat Sasaran:**
- **177.250 USD** - **165.500 USD** = ** -11.750 USD** keuntungan bersih untuk **1426 pelanggan**.

Dengan menggunakan ML, perusahaan akan menghadapi kerugian sebesar **- 11.750 USD**.

---

 **5. Perbandingan Tanpa dan Dengan Machine Learning**
- **Tanpa Machine Learning:** Perusahaan akan mengalami kerugian hingga **- 107.450 USD** per sekali Campaign.
- **Dengan Machine Learning:** perusahaan akan menghadapi kerugian sebesar **- 11.750 USD** per sekali Campaign.

![image](https://github.com/user-attachments/assets/06856114-5734-413c-8b86-332174fe283a)

Dengan demikian, menggunakan **Machine Learning** memberikan dampak finansial yang signifikan terhadap bisnis, menghemat biaya promosi sebesar 89.04% yang tidak tepat sasaran, dan meningkatkan pendapatan dengan mempertahankan pelanggan yang lebih berisiko churn.

---

 **6. Kesimpulan dan Rekomendasi**
- **Model XGBoost** setelah tuning menghasilkan performa yang baik dengan **akurasi 94%** dan F1-score yang konsisten untuk kelas churn dan tidak churn.
- Menggunakan **machine learning** membantu perusahaan mengalokasikan sumber daya promosi secara lebih efisien, fokus pada pelanggan yang berisiko churn, sehingga perusahaan dapat menghemat biaya promosi yang tidak perlu dan meningkatkan retensi pelanggan.
- **Rekomendasi:** Perusahaan harus terus mengembangkan model prediksi churn ini dengan melakukan evaluasi secara berkala. Selain itu, strategi promosi yang tepat sasaran untuk pelanggan berisiko churn perlu diperkuat, seperti melalui program loyalitas, penawaran khusus, atau peningkatan layanan pelanggan.

---

 **Literatur dan Referensi**
1. **Cost of Customer Churn**: SuperOffice Blog. Available at: [SuperOffice Customer Churn](https://www.superoffice.com/blog/reduce-customer-churn/)
2. **Operating Loss**: Investopedia. Available at: [Operating Loss Definition](https://www.investopedia.com/terms/o/operating-loss.asp)
3. **Impact of False Positive and False Negative**: Science Direct. Available at: [Cost of Promotion](https://www.sciencedirect.com/science/article/abs/pii/S0969698916303411)

---

Dengan penerapan **machine learning** dalam prediksi churn, perusahaan e-commerce ini dapat meraih **profit** yang lebih tinggi dan meminimalkan **loss** dalam strategi promosi mereka.
### **2. Rekomendasi**
#### **1. Rekomendasi untuk Kedepannya**
**1. Fokus pada Retensi Pelanggan dengan Tenure Rendah :**
- Mengingat Tenure menjadi indikator paling signifikan dalam memprediksi churn, perusahaan sebaiknya fokus pada retensi pelanggan baru atau yang memiliki masa langganan singkat. Strategi seperti memberikan diskon berkelanjutan, program loyalitas, atau insentif lainnya bisa menjadi langkah untuk memperpanjang masa berlangganan mereka.

**2. Perbaiki Pengelolaan Keluhan Pelanggan**
- Pelanggan yang mengajukan keluhan lebih memungkinkan untuk churn. Menyediakan layanan pelanggan yang cepat dan efektif, serta memberikan solusi yang memadai terhadap keluhan, dapat mengurangi tingkat churn secara signifikan.

**3. Tingkatkan Pengalaman Berbelanja untuk Kategori Produk Utama**
- Fitur Preferred Order Category juga menunjukkan bahwa pelanggan yang lebih sering membeli kategori produk tertentu (misalnya, Laptop & Accessories, dan Mobile Phone) lebih cenderung untuk tetap berlangganan. Dengan mengoptimalkan penawaran dan pengalaman belanja untuk kategori ini, perusahaan bisa meningkatkan loyalitas pelanggan.

**4. Pantau Pelanggan yang Tidak Aktif**
- Pelanggan yang tidak melakukan pesanan dalam waktu yang lama lebih memungkinkan untuk churn. Strategi retargeting dengan email marketing atau penawaran spesial kepada pelanggan yang telah lama tidak melakukan transaksi bisa membantu mencegah churn.

**5. Perbaiki Pengalaman Pengiriman**
- Mengoptimalkan pengiriman, terutama pada pelanggan dengan jarak pengiriman yang jauh (Warehouse to Home), bisa membantu mengurangi churn. Efisiensi dalam pengiriman atau memberi opsi pengiriman yang lebih cepat dapat meningkatkan kepuasan pelanggan.
  
## **Penutup**
Menggunakan pendekatan machine learning dalam prediksi churn memungkinkan e-commerce ini untuk memahami lebih dalam tentang pelanggan mereka, mempersonalisasi pengalaman pelanggan, dan pada akhirnya meningkatkan loyalitas serta mengurangi churn.

# **Terima Kasih**


