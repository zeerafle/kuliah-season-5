---

title: Jaringan Hebb
feed: show
permalink: /jst/hebb
date: 30-08-2022

---

Jaringan Hebb untuk Pengenalan Pola.

# Hebb

Model Neuron yang diperkenalkan McCulloch-Pitts mengharuskan kita untuk menentukan bobot garis dan bias secara analitik.

Dasar dari hebb adalah:
- Bila 2 neuron yang dihubungkan dengan sinapsis serentak menjadi aktif, maka kekuatan sinapsisnya meningkat
- Bila kedua neuron aktif secara tidak sinkron, maka kekuatan sinapsisnya melemah.

Dalam tiap iterasi, bobot diubah dengan persamaan:

$$w_i (baru) = W_i (lama) + x_i \dot y$$

dimana:
- $w_i$ = bobot data ke i
- $x_i$ = input ke i
- y = output

## Algoritma Hebb

- Jumlah bobotnya sama dengan jumlah inputnya
- Untuk semua vektor input (s) dan unit target output (t), lakukan:
  - Set aktivasi unit input -> $x_i = s_i$
  - Set aktivasi unit output -> $y=t$
  - Perbaiki bobot (w)
  - Perbaiki bias (b)
- Perubahan/perbaikan bobot ditandai dengan $\delta w$

## Jaringan Hebb Untuk Pengenalan Pola

Jaringan Hebb dapat dipakai untuk membedakan 2 macam pola.

![](../assets/img/2022-08-30-09-45-07.png)

- Tiap sel pola dianggap sebagai sebuah unit masukan. Pola 1 ada $x_1, \dots, x_{25}$
- Misal sel biru diberi nilai = 1, dan kuning = -1

![](../assets/img/2022-08-30-09-50-05.png)

