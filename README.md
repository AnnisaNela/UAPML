# Prediksi Kelas Harga Rumah dengan FNN, Random Forest, dan XGBoost

## Overview Project 
Proyek ini bertujuan untuk memprediksi kelas harga rumah berdasarkan kategori Low, Medium, High, Very High, dan Luxury. Prediksi dilakukan dengan menggunakan berbagai aspek yang memengaruhi harga properti, yaitu:

1. Luas Properti: Total luas properti yang menjadi indikator utama dalam menentukan kelas harga.
2. Jumlah Kamar: Banyaknya kamar tidur yang tersedia dalam properti.
3. Jumlah Kamar Mandi: Fasilitas kamar mandi yang berkontribusi terhadap nilai properti.
4. Kota: Lokasi geografis di mana properti berada, yang sangat memengaruhi nilai pasar properti.
5. Lokasi Spesifik: Lingkungan atau area spesifik yang dapat memberikan gambaran lebih rinci tentang nilai properti.
6. Tipe Properti: Kategori properti seperti flat, room, house, dll.
7. Tujuan (For Sale/For Rent): Properti yang dijual cenderung memiliki kelas harga yang berbeda dibandingkan dengan properti yang disewakan.

**Link Dataset** 
https://www.kaggle.com/datasets/howisusmanali/house-prices-2023-dataset

## Langkah Instalasi
```
python -m pip install virtualenv
python -m venv virtvenv
cd Scraping/myenv/Scripts
activate.bat
pip install -r requirements.txt
```

## Run Streamlit App
```
streamlit run web.py
```

## Deskripsi Model 
### FeedForward Neural Network 
**Architecture**
![Sample-of-a-feed-forward-neural-network_W640](https://github.com/user-attachments/assets/ace82954-b091-4cd6-a443-9d089397641b)

**Preprocesing** 
Selama pelatihan, data dibagi menjadi dua:
Training Set: 80% dari data digunakan untuk melatih model.
Validation Set: 20% digunakan untuk mengevaluasi performa model selama pelatihan.

**Modelling**
Model ini merupakan jaringan saraf tiruan (Artificial Neural Network) yang dirancang untuk klasifikasi data ke dalam beberapa kategori (multiclass classification). Model terdiri dari tiga lapisan (layers):
![image](https://github.com/user-attachments/assets/808e92f6-5a5a-4793-966c-36453d86798a)

**Model Evaluation**
![image](https://github.com/user-attachments/assets/5d46c847-f1dd-4d34-a7bd-39dfc065a2bf)

### Random Forest
**Architecture**
![Random-forest-regression-architecture](https://github.com/user-attachments/assets/8feefbdb-708b-466c-94e4-635cb0e43bf6)

**Preprocesing** 
Training: Model dilatih dengan mempelajari pola dalam data pelatihan (X_train dan y_train). Setiap pohon dalam Random Forest dilatih menggunakan subset data acak (bootstrap sampling) dan subset fitur acak untuk menentukan split.
Bagging: Metode ensemble ini menggabungkan hasil prediksi dari setiap pohon dengan cara voting mayoritas (untuk klasifikasi).

**Modelling**
Model ini merupakan metode berbasis ensemble learning. Random Forest membangun sejumlah pohon keputusan (decision trees) selama pelatihan dan menggabungkan prediksi dari setiap pohon untuk memberikan hasil klasifikasi akhir.

**Model Evaluation**
![image](https://github.com/user-attachments/assets/a0b065c3-4285-49ea-b7ff-0d7eeafe164f)

### XGBoost
**Architechture**
![Architecture-and-inner-flow-of-XGBoost-model-for-boosting-the-performance-of-soil-carbon](https://github.com/user-attachments/assets/d4bfb972-2e4b-4bc3-8f33-d61116032e9c)

**Preprocessing**
Training: Model dilatih dengan data pelatihan (X_train dan y_train), di mana setiap pohon bertujuan untuk meminimalkan kesalahan (residual error) dari prediksi sebelumnya.
Objective Function:
Menggunakan fungsi loss logaritmik (log-loss) untuk klasifikasi multikelas.
Memaksimalkan probabilitas kelas target yang benar dengan pendekatan softmax.

**Modelling**
Model ini merupakan metode boosting berbasis pohon (tree-based boosting algorithm). 

**Model Evaluation**
![image](https://github.com/user-attachments/assets/0da39c07-1afe-4e23-b230-372667952da8)

## Link Live Demo
https://housepricepredictionclass.streamlit.app/
