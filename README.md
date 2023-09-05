Olist Product Category Analysis

# **Objective**
Sebagai sebuah e-commerce, terdapat banyak kategori produk yang dijual di platform Olist. Kategori produk ini dapat dianalisis untuk mencari tahu strategi sales dan marketing yang tepat sasaran sehingga Olist dapat terus meningkatkan penjualan. Category Analysis dilakukan dengan cara menganalisa dataset Olist dengan objektif sebagai berikut:
1. Mencari tahu 10 (sepuluh) kategori yang paling banyak terjual (top 10 category) dan 10 (sepuluh) kategori yang paling sedikit terjual (bottom 10 category)
2. Dari informasi yang didapatkan pada poin nomor 1, akan dilakukan analisis trend penjualan per kategori untuk kategori bottom 10. Hal ini dilakukan untuk melihat kategori mana yang tidak mengalami peningkatan penjualan dan membutuhkan marketing support untuk dapat meningkatkan penjualannya.
3. Dari informasi yang didapatkan pada poin nomor 1, akan dicari tahu jumlah produk dari masing-masing kategori yang ada di top 10 category. Hal ini dilakukan untuk melihat apakah ada kategori yang berkontribusi tinggi terhadap penjualan tapi memiliki jumlah produk yang masih sedikit dibandingkan kategori lainnya. Sehingga nanti dapat dilakukan strategi penambahan produk untuk meningkatkan penjualan.

# **Data Overview**
Dari objective yang telah disusun, berikut data yang akan digunakan untuk proses analisa:
1. olist_order_dataset
   Dataset ini akan digunakan karena proses analisa membutuhkan data timeframe dari setiap order yang terjadi.   
2. olist_order_items_dataset
   Pada dataset order items, proses analisa akan menggunakan detail item dan harga item pada setiap order
3. olist_products_dataset
   Products dataset dibutuhkan untuk mengidentifikasi kategori dari setiap order yang telah diorder oleh user.
4. product_category_name_translation
   Pada dataset nomor 3, nama kategori masih tertulis dalam bahasa spanyol. Supaya proses analisa dapat lebih mudah dipahami, akan digunakan dataset name translation untuk mengetahui      nama kategori dalam bahasa Inggris.
Dari 4 table yang akan digunakan, di bawah ini merupakan gambaran relasi table tersebut di dalam database:
<img width="794" alt="image" src="https://github.com/corneliasdrjt/olist/assets/136590789/3015d00e-d013-441b-a0f1-dd7fe465cd2c">


# **Data Checking & Solving**

1. Order & Order Items Dataset
   Sebelum melakukan pengecekan data, terlebih dahulu dilakukan merge antara order dataset dan order item dataset.



