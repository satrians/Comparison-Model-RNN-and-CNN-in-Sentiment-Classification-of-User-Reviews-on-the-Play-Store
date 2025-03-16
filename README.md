# Comparison-Model-RNN-and-CNN-in-Sentiment-Classification-of-User-Reviews-on-the-Play-Store
Example Proyek Data Desain
# Dataset
Topik Dataset : User Reviews on the Play Store
Tentang Dataset : Dataset ini berasal dari data aplikasi Play Store yang dapat digunakan untuk membangun model klasifikasi teks guna membedakan antara tweet yang sekiranya positif dan negatif

# Latar Belakang Masalah
Dalam era digital, ulasan pengguna di platform seperti Google Play Store menjadi sumber informasi berharga untuk memahami opini masyarakat. Namun, analisis sentimen terhadap ulasan ini menghadapi tantangan, seperti keragaman bahasa dan ketidakseimbangan data sentimen. Proyek ini membandingkan performa algoritma deep learning, yaitu CNN dan RNN, untuk analisis sentimen pada lima kategori aplikasi: desain, fotografi, game, media sosial, dan streaming. Diharapkan, hasil penelitian ini dapat membantu pengembang memilih algoritma yang sesuai untuk meningkatkan akurasi klasifikasi sentimen.

# Tujuan dan Target Pencapaian
Proyek ini bertujuan untuk membandingkan performa algoritma RNN dan CNN dalam klasifikasi sentimen ulasan pengguna dari lima kategori aplikasi di Google Play Store. Dengan menggunakan teknik SMOTE untuk mengatasi ketidakseimbangan data, penelitian ini berfokus pada menentukan algoritma mana yang tepat untuk setiap kategori.

# Data Loading
Menggunakan Dataset dari scrapping google play store
Membaca dataset ke dalam DataFrame menggunakan pandas.
contoh membaca data salah satu data dari data desain
![Screenshot 2025-03-16 141102](https://github.com/user-attachments/assets/2cfa5c22-d2e8-424f-ab55-ee1bdfad1a33)

# Data Cleaning
Menghapus kolom yang tidak terpakai
Melakukan preprocessing kata dengan menggunakan Stopword dan WordNetLemmatizer
![Screenshot 2025-03-16 141247](https://github.com/user-attachments/assets/fd51ee9b-195c-4d12-ac62-ad4a11fea5a1)

# EDA (Exploratory Data Analysis)
Menggunakan WordCloud untuk visualisasi kata-kata yang sering muncul dalam tweet ulasan pengguna aplikasi Canva di Google Play Store.
![Screenshot 2025-03-16 141500](https://github.com/user-attachments/assets/0321e2b6-e2ba-4583-923c-a127638b83f4)
Menampilkan distribusi target berdasarkan target
Menampilkan jumlah kata pada kolom "sentiment"
Menampilkan panjang tweet pada kolom "sentiment"
![Screenshot 2025-03-16 141925](https://github.com/user-attachments/assets/0ac03eae-2c5b-4cf4-98b8-c17af4dee4f9)
![image](https://github.com/user-attachments/assets/ed394a9d-3deb-4d71-b446-5e3095405d6a)

# Feature Engineering
Menggunakan train_test_split untuk membagi dataset menjadi dua subset: satu untuk pelatihan (training set) dan satu lagi untuk pengujian (testing set).
Untuk kolom yang digunakan untuk membagi subset menjadi dua yaitu kolom clean_content dan kolom sentiment
![Screenshot 2025-03-16 142613](https://github.com/user-attachments/assets/f333ddcf-1faa-4ed6-9e01-69154a096f14)

# Model Architecture Definition
Menggunakan model Deep Learning RNN (Recurrent Neural Network) dan CNN (Convolutional Neural Network)
![Screenshot 2025-03-16 142719](https://github.com/user-attachments/assets/bf5d88a8-6600-4a2e-80f0-c812c0bd77be)
![Screenshot 2025-03-16 142923](https://github.com/user-attachments/assets/cb7b0fbd-79ec-49a3-b830-3017449311ea)
![Screenshot 2025-03-16 143010](https://github.com/user-attachments/assets/3ce95c5d-f6cc-40cc-8aa3-3b60f990a891)
![Screenshot 2025-03-16 143042](https://github.com/user-attachments/assets/b42ade4d-49fd-44f8-9730-908e6d5253c8)

# Model Training
Pelatihan Model
Membagi dataset menjadi training dan validation set.
Melatih model dengan 100 epoch dengan library EarlyStopping.
![Screenshot 2025-03-16 143330](https://github.com/user-attachments/assets/aeb77868-5be0-473c-a5b6-dff586087d95)
![Screenshot 2025-03-16 143400](https://github.com/user-attachments/assets/d795d70b-b913-4e11-927e-9345a9988553)
![Screenshot 2025-03-16 143448](https://github.com/user-attachments/assets/0ec3232d-6f26-4ee6-b78d-25fe45be3507)

# Model Evaluasi
Evaluasi Model
Menampilkan diagram loss dan accuracy
![image](https://github.com/user-attachments/assets/94d27783-800f-4003-9830-ad43a2ce6df6)
![image](https://github.com/user-attachments/assets/2ddf8c50-b0db-46b0-a234-447e109dd3a1)

Menghitung metrik evaluasi seperti accuracy, precision, recall, dan F1-score.
Menampilkan classification report dan confusion matrix.
![Screenshot 2025-03-16 145259](https://github.com/user-attachments/assets/9face5ef-ee6e-4c3b-b7f4-71657fceb1fa)
![Screenshot 2025-03-16 145324](https://github.com/user-attachments/assets/abd12375-5247-4bff-9c4c-b62a2fb8d965)
![Screenshot 2025-03-16 145344](https://github.com/user-attachments/assets/c46cb90e-8c51-4d23-a09e-fc11738af24b)
![image](https://github.com/user-attachments/assets/c3d92087-36d6-4da6-aaa0-e9cf7f4e58f8)
![image](https://github.com/user-attachments/assets/dfec800b-6b62-4ccb-b1c3-b221567116b8)

# Kesimpulan 
Proyek ini berusaha untuk menjawab tantangan dalam mengidentifikasi tweet yang relevan dengan ulasan pengguna menggunakan teknik NLP dengan model RNN dan CNN. Dengan berhasil mengembangkan model yang dapat membedakan tweet yang relevan dari yang tidak, kita dapat:
Proyek ini berhasil membandingkan performa model CNN dan RNN untuk analisis sentimen pada ulasan lima kategori (desain, fotografi, game, media sosial, dan streaming). Model CNN menunjukkan akurasi dan stabilitas yang lebih tinggi dibandingkan RNN di sebagian besar kategori, dengan akurasi tertinggi pada kategori desain (85%) dan loss terendah (0.41%).

