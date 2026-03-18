# 🛍️ E-commerce Mijozlarini Segmentlash (Customer Segmentation)

Ushbu loyiha Machine Learning (Unsupervised Learning) algoritmlari yordamida haqiqiy onlayn do'kon xaridorlarini ularning xarid xulq-atvoriga qarab guruhlarga ajratishga (segmentatsiya qilishga) qaratilgan. Loyihada mijozlarni baholash uchun biznesda keng tarqalgan **RFM (Recency, Frequency, Monetary)** tahlilidan foydalanildi.

## 📊 Ma'lumotlar bazasi (Dataset)
Loyiha uchun [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/352/online+retail) dagi **"Online Retail"** ochiq ma'lumotlar to'plami ishlatildi. Bu Buyuk Britaniyada joylashgan onlayn do'konning 1 yillik real tranzaksiyalar tarixini o'z ichiga oladi (500 mingdan ortiq qator).

## 🛠️ Qo'llanilgan Texnologiyalar
* **Dasturlash tili:** Python
* **Kutubxonalar:** Pandas, NumPy, Scikit-learn, Scikit-learn-extra, Matplotlib, Seaborn
* **Ma'lumotlarni qayta ishlash:** StandardScaler, Log Transformation, PCA (Asosiy komponentlar tahlili)

## 🧠 Sinovdan o'tkazilgan Modellar
Loyihada quyidagi 5 xil klasterlash algoritmlari o'qitildi va ularning natijalari **Silhouette Score** yordamida taqqoslandi:
1. K-Means
2. Hierarchical (Agglomerative) Clustering
3. DBSCAN
4. Gaussian Mixture Models (GMM)
5. **K-Medoids (Eng yaxshi natija ko'rsatgan model 🏆)**

## 📈 Biznes Natijalar va Xulosalar
K-Medoids modeli xaridorlarni ma'lumotlardagi anomaliyalarga (outliers) qaramay, 4 ta mantiqiy biznes guruhga ajratib berdi:

* **1-Klaster (VIP / Chempion mijozlar):** Do'konga eng ko'p daromad keltiruvchi, tez-tez va yaqinda xarid qilgan sodiq mijozlar. Ularni ushlab qolish uchun maxsus VIP xizmatlar va yopiq chegirmalar taklif qilinishi kerak.
* **3-Klaster (Istiqbolli / Yangi mijozlar):** Yaqinda kelgan, biroq hali ko'p xarid qilishga ulgurmagan mijozlar. Ularni doimiy mijozga aylantirish uchun "Ikkinchi xarid uchun chegirma" kabi kampaniyalar o'tkazish tavsiya etiladi.
* **2-Klaster (Sodiq, lekin passiv mijozlar):** Oldin ko'p xarid qilgan, ammo oxirgi vaqtlarda ko'rinmay qolganlar. Ularni uyg'otish uchun yangi tovarlar haqida eslatmalar yuborish lozim.
* **0-Klaster (Yo'qotilayotgan mijozlar):** Eng uzoq vaqt (o'rtacha 7 oy) oldin kelgan va qariyb qaytib kelmagan guruh. Ularga so'nggi imkoniyat sifatida katta chegirmalar yuborib ko'rish mumkin.

## 🚀 Qanday ishga tushirish mumkin?
1. Repozitoriyni kompyuteringizga yuklab oling (Clone).
2. Kerakli kutubxonalarni o'rnating: `pip install pandas numpy scikit-learn scikit-learn-extra matplotlib seaborn openpyxl`
3. `customer_segmentation.ipynb` faylini Jupyter Notebook yoki Google Colab orqali ochib, katakchalarni ishga tushiring. Ma'lumotlar avtomatik ravishda UCI omboridan yuklanadi.
