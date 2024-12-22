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
