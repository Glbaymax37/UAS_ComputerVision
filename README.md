# UAS Computer Vision

**Nama:** Richard Riovaldo Simatupang  
**NIM:** 4222201043  
**Kelas:** Teknik Robotika Pagi B

## How to Use
  **Model:** [*llava-v1.5-7b-llamafile*](https://www.kaggle.com/datasets/juanthomaswijaya/indonesian-license-plate-dataset).

 **Prepare LMStudio:**
1. Intstall LMStudio Ikuti intruksi dari [LMStudio Installation](https://lmstudio.ai/docs/app)<br>
   Pilih Sesuai dengan Jenis OS

2. jalankan LMStudio Dan cari model *llava-v1.5-7b-llamafile* pada kolom search model<br>
   dan install model dengan *size 4.38 gb*

   <img width="813" height="424" alt="image" src="https://github.com/user-attachments/assets/af65ed89-a35b-4a7b-873b-4bb814e801e3" />

 **Prepare DataSet:**
1. Ambil data label dan image dari [Indonesian License Plate Dataset](https://www.kaggle.com/datasets/juanthomaswijaya/indonesian-license-plate-dataset).<br>
   pada folder *Test* Di **Indonesian License Plate Recognition Dataset**.
2. Buat Ground Truth.csv yang dimana berisi data acuan untuk model mengukur performa model dengan membandingkan hasil prediksi model terhadap data ground truth <br>
   jalankan Program generate.<br>
   <img width="597" height="71" alt="image" src="https://github.com/user-attachments/assets/3eefe136-7544-43e8-a09f-5f27cfabeff2" /><br>
   *output ketika program berhasil dijalankan*
4. Buat Folder Baru Untuk memisahkan Ground Thurth dengan data kemudian Pindahkan Ground truth<br>
   sehingga struktur Folder akan seperti Berikut:<br>
   <img width="228" height="166" alt="image" src="https://github.com/user-attachments/assets/f10daf64-a0f6-45ae-87b8-17b6fd2f8a02" />

 **Execute on Windows!!!**

1. Buka Terminal Dan masuk Ke Directory Atau folder 
2. Jalankan Perintah berikut:<br>
   <img width="660" height="110" alt="image" src="https://github.com/user-attachments/assets/cee3036c-00b9-485e-8e4a-2b672e5489e6" /><br>
3. lalu Cek LMStudio Status Model Dengan Perintah
   `lms ls`<br>
   <img width="617" height="140" alt="image" src="https://github.com/user-attachments/assets/492788ce-1947-45da-9757-4fc83c6a88dd" /><br>
   *Contoh Output di Terminal*<br>
4. Load Model Degan Perintah:<br>
   `lms load llava-v1.5-7b-llamafile --gpu 0.5    # Offload 50% of layers to GPU`<br>
   `lms load llava-v1.5-7b-llamafile --gpu max    # Offload all layers to GPU`<br>
   `lms load llava-v1.5-7b-llamafile --gpu off    # Disable GPU offloading`<br>
   *Pilih Sesuai Kebutuhan*<br>
   <img width="613" height="260" alt="image" src="https://github.com/user-attachments/assets/22195484-3e9f-429b-9a05-ac960009b0e3" /><br>
   *Contoh Output Ketika Load Model Berhasil*<br>
5. Start LMStudio Server untuk Menyediakan endpoint API lokal untuk model AI.<br>
   Dengan Perintah:  `lms server start`<br>
   <img width="323" height="74" alt="image" src="https://github.com/user-attachments/assets/e7a01311-9607-45f9-87e1-3e5f6b67425e" /><br>
   *Contoh Output*

6. Jalankan Program Dengan Perintah `python <nama_program> ` <br>
   *example*
   `python ocr_eval.py`<br>
   <img width="855" height="82" alt="image" src="https://github.com/user-attachments/assets/147c6ed3-99bf-40c1-9146-157e46599bc2" /><br>
   *Contoh Output Terminal Ketika Berhasil*<br>

7. Setelah semua gambar telah selesai diprosses Hasil Akan tersimpan dalam format *result.CSV*<br>
   <img width="479" height="304" alt="image" src="https://github.com/user-attachments/assets/66883e2a-f202-4415-b5a8-5b7645af6585" /><br>
   *Contoh Output Pada Excel*



   

   






 
   

 

