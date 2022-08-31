---
title: Preprocessing
feed: show
date: 31-08-2022
permalink: /cv/preprocessing
---

Preprocessing --> Image Enhancement. Adalah proses awal dalam pengolahan citra.

- Perbaikan kualitas citra
- Diperlukan karena seringkali citra yang dijadikan objek pembahasan mempunyai kualitas yang buruk / kurang baik.

Tujuannya adalah mendapatkan citra yang lebih mudah untuk diinterpretasikan oleh mata manusia.

Dalam proses ini _ciri-ciri tertentu yang terdapat di dalam citra lebih diperjelas kemunculannya atau disamarkan karena dapat menimbulkan noise_

## Image Enhancement

Contoh citra yang buruk:

- Citra yang mengandung noise
- Citra yang terlalu gelap/terang
- Citra yang kurang tajam
- Citra yang buram

## Lingkup Pre-Processing

### Kekurangan Pre-processing

- Perlu tambahan waktu komputasi
- Metode yang tidak sesuai dapat mengakibatkan informasi penting suatu citra hilang.

### Contoh pre-processing

- Menghilangkan Noise
- Memperjelas features (fitur)
- Memperkecil / memperbesar ukuran data
- Mengubah kecerahan gambar
- Melakukan peregangan kontras (contrast stretching)
- Konversi ruang warna
- Konversi citra RGB -> grayscale
- Binarisasi citra
- Croping citra. Ada suatu citra asli yang memuat objek utama, selain objek utama akan di crop. (Deteksi __Region of Interest__)
- Resize citra.
- Edge detection

#### Image Brightness

- Untuk membuat citra lebih terang atau lebih gelap
- Kecerahan gambar dapat diperbaiki dengan menambahkan (atau mengurangi)
- Secara matematis operasi ini ditulis sebagai berikut:

$$f(x,y)'=f(x,y)+b$$

Jika b positif/negatif, maka...

[[Histogram]]

#### Contrast Stretching

Semacam suatu histogram itu di stretch sehingga intesitasnya merata.

1. Cari batas bawah pengelompokan piksel dengan cara memindai (scan) histogram dan nilai keabuan terkecil ke nilai keabuan terbesar (0 sampai 255) untuk menemukan piksel pertama yang melebihi nilai ambang pertama yang telah dispesifikasikan.
2. ...
3. Piksel-piksel yang berada dibawah nilai ambang pertama di-set sama dengan 0, sedangkan yang diatas sama dengan 255.
4. ...

$$S=\frac{r-r_{max}}{r_{min}-r{max}}\times 255$$

Keterangan:

- $r$ adalah nilai keabuan dalam citra semula
- $s$ adalah nilai keabuan yang baru
- $r_{min}$ adalah nilai keabuan terendah
- $r_{max}$ adalah nilai keabuan tertinggi

#### Pengubahan [[Histogram]]

Ada 2 metode pengubahan citra berdasarkan Histogram

- Perataan Histogram (Histogram Equalization)
- Histogram specification

#### Image Smoothing

- Operasi ini dilakukan untuk menekan komponenyang berfrekuensi tinggi dan meloloskan komponen yang berfrekuensi rendah
- Filter:
  - Low pas filter

    ![low pas filter](https://www.researchgate.net/profile/Ivanna-Timotius/publication/286174555/figure/fig2/AS:315195579748353@1452159890799/The-kernel-of-the-low-pass-filter.png)

    - Median filter

    ![median filter](https://neubias.github.io/training-resources/figures/median_filter_and_ranking.png)

#### Image Sharpening

Filter ini akan meloloskan/ memperkuat komponen yang berfrekuansi tinggi (misal : tepi)

#### Koreksi Geometrik

Yang termasuk dalam operasi koreksi geometrik adalah

- rotasi
- translasi
- penskalaan citra
