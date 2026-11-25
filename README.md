# Heart Disease Risk Assessment

Aplikasi Streamlit untuk demonstrasi klasifikasi risiko penyakit jantung menggunakan model machine learning. Data dapat dimasukkan secara manual atau diunggah dalam bentuk CSV.

## Menjalankan aplikasi

Buka terminal di folder repository `projecthma`, lalu jalankan:

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
streamlit run main.py
```

Aplikasi akan terbuka di browser melalui alamat lokal yang ditampilkan Streamlit.

## Input CSV

Pilih **Upload CSV** pada sidebar. CSV harus berisi kolom berikut dengan nama yang sama persis:

```text
cp,thalach,slope,oldpeak,exang,ca,thal,sex,age
```

Nilai `sex` menggunakan `1` untuk pria dan `0` untuk perempuan. Nilai kategorikal lain harus mengikuti kode yang dijelaskan di aplikasi.

## File pendukung

`generate_heart_disease.pkl` harus berada di folder yang sama dengan `main.py`; aplikasi memuat file ini saat menjalankan prediksi. Pastikan model berasal dari sumber tepercaya karena file pickle dapat menjalankan kode saat dimuat.

`data.csv` tidak diperlukan untuk menjalankan aplikasi dan diabaikan oleh Git melalui `.gitignore`.

## Deploy ke Streamlit Community Cloud

1. Push repository ini ke GitHub.
2. Buat aplikasi baru di Streamlit Community Cloud dan pilih repository serta branch.
3. Isi **Main file path** dengan `main.py`.
4. Pastikan `generate_heart_disease.pkl`, `requirements.txt`, dan `runtime.txt` tersedia di root repository.

Versi Python ditetapkan di `runtime.txt`; dependensi aplikasi ditetapkan di `requirements.txt`.

## Catatan

Aplikasi ini dibuat untuk tujuan pembelajaran dan demonstrasi. Hasil prediksi bukan diagnosis medis dan tidak menggantikan pemeriksaan atau saran tenaga kesehatan.