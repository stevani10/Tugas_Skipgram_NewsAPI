# Implementasi Skipgram dengan NewsAPI
## Deskripsi Proyek
Proyek ini bertujuan untuk membangun model word embeddings menggunakan Skip-gram dengan TensorFlow/Keras. Dataset diambil langsung dari NewsAPI dengan topik yang dapat ditentukan secara dinamis. Model akan dilatih dengan berbagai ukuran window dan dimensi embedding untuk mengevaluasi performa dalam menemukan kata-kata yang relevan.

### Cara Menggunakan Kode
1. Clone Repository : git clone https://github.com/stevani10/repository_name.git
2. Install Dependencies :  
   Pastikan Anda memiliki Python 3.8+ dan Jupyter Notebook.
3. Dapatkan API Key NewsAPI : 
Buat akun di NewsAPI dan dapatkan API key. Masukkan API key di dalam notebook sebelum menjalankan kode.
4. Jalankan Notebook :
Buka Jupyter Notebook dan jalankan file: jupyter notebook 'Tugas_Implementasi_Skipgram_dengan_NewsAPI_.ipynb'

### Penjelasan Parameter Eksperimen
Dalam eksperimen ini, saya menguji berbagai parameter model:
- Ukuran Window (window size)
Digunakan untuk menentukan seberapa jauh kata target bisa melihat konteksnya.
Variasi yang digunakan: 1, 2, 3.
- Dimensi Embedding (embedding_dim)
Jumlah dimensi vektor kata yang dihasilkan oleh model.
Variasi yang digunakan: 50, 100, 200.
- Jumlah Epoch
Model dilatih selama 5 epoch dengan batch size 4 untuk memastikan konvergensi.
- Sumber Data
Data dikumpulkan dari NewsAPI, difilter berdasarkan topik tertentu (contoh: "technology").

### Hasil Analisis dan Kesimpulan
Setelah melatih model dengan berbagai kombinasi parameter, berikut adalah temuan utama:
1. Ukuran window kecil (1) menghasilkan embeddings yang lebih spesifik, tetapi kurang mampu menangkap konteks yang lebih luas.
2. Ukuran window besar (3) menangkap hubungan lebih baik, tetapi bisa memperkenalkan kata-kata yang kurang relevan.
3. Dimensi embedding yang lebih tinggi (200) memberikan hasil yang lebih akurat dalam menemukan kata-kata yang mirip.
4. Evaluasi menggunakan kata kunci seperti "technology" menunjukkan bahwa model dapat menemukan kata-kata yang relevan seperti "innovation", "AI", dan "software".

Secara keseluruhan, window size = 2 dan embedding_dim = 100 memberikan keseimbangan terbaik antara spesifisitas dan generalisasi.

