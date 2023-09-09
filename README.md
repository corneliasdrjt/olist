# **Olist Product Category Analysis**

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


# **Data Cleansing**
1. Order & Order Items Dataset
   Sebelum melakukan pengecekan data, terlebih dahulu dilakukan merge antara order dataset dan order item dataset.

   <img width="776" alt="image" src="https://github.com/corneliasdrjt/olist/assets/136590789/f4656f90-6246-4572-beb8-5f4860d3a8ff">
   
   Selanjutnya melakukan pemeriksaan apakah ada data Null pada table hasil merge

   <img width="308" alt="image" src="https://github.com/corneliasdrjt/olist/assets/136590789/dc330e60-311d-4e5d-afb5-f1ae458beafb">
   
   Data yang null ada sebanyak 775 rows atau sebesar 0.683% di mana semua data null terletak pada order_item_id, product_id, dan price. Asumsinya data null ini adalah order yang           statusnya canceled, dan karena jumlahnya sangat sedikit atau tidak signifikan dibandingkan dengan keseluruhan data, makan akan kita ignore.

   Pada dataset order_new terdapat data harga yang akan diperiksa distribusi atau persebaran datanya.

   <img width="692" alt="image" src="https://github.com/corneliasdrjt/olist/assets/136590789/319c581c-7eb5-4f37-a7e6-642aa2a1607a">
   
   <img width="716" alt="image" src="https://github.com/corneliasdrjt/olist/assets/136590789/1a574f3f-5ebc-4aa7-a77b-152afb0154e2">
   
   Data price memiliki distribusi normal dan outlier, namun outlier pada price ini akan dibiarkan mengingat data price bisa sangat beragam karena keberagaman produk terjual pada           platform Olist. Selain itu data harga akan mempengaruhi objective analisis kategori yang akan dilakukan.

3. Product Dataset
   Proses checking terhadap dataset dimulai dengan memeriksa apakah terdapat data Null.


Analysis Report: https://medium.com/@corneliaendra95/product-category-analysis-olist-5b6443dc309c

