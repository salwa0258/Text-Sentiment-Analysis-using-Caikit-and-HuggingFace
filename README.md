<h1 align="center"> Text Sentiment Analysis using Caikit and HuggingFace </h1>
<p align="center"> Berisi tentang analisis dari modul pada Cognitive Class AI yang berjudul "Text Sentiment Analysis using Caikit and HuggingFace" </p>

<div align="center">

<img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54">
<img src="https://img.shields.io/badge/-HuggingFace-FDEE21?style=for-the-badge&logo=HuggingFace&logoColor=black">
<img src="https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white">

</div>

<h2 align="center"> Hasil analisa "Text Sentiment Analysis using Caikit and HuggingFace" </h2> 

(Sebenarnya saya tidak terlalu paham kak yang harus dianalisis yang bagian mananya, jadi saya hanya menjelaskan per file sebisa saya :)

**Create the data model specification**

- Pada file classification.py yang ditempatkan pada file data_model digunakan untuk mendefinisikan data model classes yang mewakili AI model atributes dalam kode. Setelah membuat file classification.py buat file __init__.py agar classes dapat terlihat di project yang telah dibuat.

**Create the model wrapper**

- Membuat module class yang memwrap model AI Huggingface agar caikit dapat memuat dan menjalankannya dengan cara membuat directory baru, yaitu models lalu buat file config.yml yang digunakan untuk mengelola dan mengidentifikasi "HuggingFaceSentimentModule".

    - Setelah itu membuat directory baru untuk modle/wrapper classes dan menamainya dengan runtime_model. Di dalam directory buat file baru yang digunakan untuk mengintegrasi model analisis sentimen Hugging Face yang telah dilatih sebelumnya ke dalam alur `caikit`, yang memungkinkannya untuk disimpan, dimuat, dan digunakan dengan mudah di berbagai aplikasi dan file tersebut diberi nama hf_module.py. Setelahnya membuat file __init__.py agar dapat terlihat pada project yang telah dibuat. 
    - Kembali ke top-level python package dan sediakan library-specific configuration yang akan digunakan oleh runtime dengan membuat file config.yml. lalu kofigurasikan library dengan configuration file path dan buat data_model and runtime_model packages terlihat dengan cara menambahkan ke file __init__.py. Buat file tersebut berada di same top-level text_sentiment directory yang sama dengan file config.yml

**Include the module and package dependencies**
menyiapkan Python environment tailored untuk menggunakan pustaka `caikit`  beserta tools Hugging Face untuk natural language processing.
Setelah membuat file tersebut lakukan install the requirements pada terminal
```
pip install -r requirements.txt
```

**Start the Caikit runtime**
The Caikit runtime serves the Hugging Face model sehingga dapat di panggil untuk inference. The runtime starts a gRPC server, yang memuat model saat startup. Setelah itu barulah kita dapat memanggil model untuk melakukan analisis sentimen. Kita dapat menjalankannya di terminal untuk start the caikit runtime.
```
python start_runtime.py
```

**Test the sentiment analysis**
Pada file code ini diberi nama file client.py yang digunakan untuk model yang dibuat dan text yang saya berikan adalah "Aku tidak suka hari Senin", "Aku suka menonton drama" dan mengahasilkan respon negative pada kalimat "Aku tidak suka hari Senin" sedangkan pada kalimat  "Aku suka menonton drama" menghasilkan respon positive. 
Untuk menjalankannya di terminal kita dapat menuliskan python client.py untuk menjalankan test sentiment analysis

```
python client.py
```