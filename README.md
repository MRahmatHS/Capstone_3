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
>
> ---
> ---
