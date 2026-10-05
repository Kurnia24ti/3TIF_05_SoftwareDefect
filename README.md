# Analisis Perbandingan Metrik Kompleksitas Kode pada Modul Perangkat Lunak Cacat dan Tidak Cacat

Studi Kasus: Software Defect Dataset by NASA (JM1)

Projek Probabilitas dan Statistika, Kelompok 5, Kelas 3 TI F  
Program Studi Teknik Informatika, Politeknik Caltex Riau, 2026

## Anggota Kelompok

| Nama | NIM |
|---|---|
| Kurnia Setiawan | 2455301224 |
| Mulki Ahmad Mubasir | 2455301230 |
| Nazwa Amalya Shaliha | 2455301231 |
| Wulan Aulia Rahma | 2455301239 |

Dosen pengampu: Mona Elviyenti

## Tujuan

1. Mendeskripsikan karakteristik jumlah baris kode (LOC) dan kompleksitas siklomatik (VG).
2. Menguji perbedaan LOC dan VG antara modul cacat dan tidak cacat.
3. Menentukan peluang modul cacat dan kekuatan hubungan LOC dengan VG.

## Data

- Sumber: Software Defect (JM1, NASA) di Kaggle  
  https://www.kaggle.com/datasets/radowanulhaque/software-defect
- Data asli 10.885 modul. Diambil sampel acak 5.000 modul (`random_state = 42`).
- Satu baris anomali (ID_Modul 1, bernilai desimal) dikeluarkan, sehingga 4.999 modul dianalisis.
- Berkas: `3TIF_05_SoftwareDefect (1).xlsx`
  - `Dataset`: sampel 5.000 modul (7 kolom)
  - `Dataset_asli`: data asli lengkap
  - `Keterangan Variabel` dan `Catatan Data`: penjelasan variabel dan pra-pemrosesan

## Isi Repository

| Berkas | Keterangan |
|---|---|
| `KELOMPOK_5.ipynb` | Kode Python untuk seluruh analisis |
| `3TIF_05_SoftwareDefect (1).xlsx` | Data penelitian |
| `README.md` | Penjelasan repository |

## Metode Analisis

Statistika deskriptif, uji normalitas (Shapiro-Wilk, D'Agostino) dan uji Levene,
distribusi binomial dan lognormal, uji Mann-Whitney, korelasi Spearman,
dan regresi linear sederhana (taraf signifikansi 5%).

## Cara Menjalankan

1. Buka `KELOMPOK_5.ipynb` di Google Colab.
2. Unggah berkas `3TIF_05_SoftwareDefect (1).xlsx` ke Colab (satu folder dengan notebook).
3. Jalankan seluruh sel secara berurutan (Runtime > Run all).

Pustaka: pandas, NumPy, SciPy, Matplotlib.

## Hasil Utama

- Proporsi modul cacat: 19,56% (978 dari 4.999 modul).
- Modul cacat memiliki LOC dan VG yang lebih tinggi (Mann-Whitney, p < 0,001).
- LOC dan VG berkorelasi positif sangat kuat (Spearman rho = 0,81).
