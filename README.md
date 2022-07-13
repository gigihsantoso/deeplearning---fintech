[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/gigihsantoso/prediksi-berlangganan-deposito-berjangka-deeplearning/blob/main/Deep_Learning_Fintech.ipynb)

# Fintech

Data tersebut terkait dengan kampanye pemasaran langsung dari lembaga perbankan Portugis. Kampanye pemasaran didasarkan pada panggilan telepon. Seringkali, lebih dari satu kontak ke klien yang sama diperlukan, untuk mengakses apakah produk (deposito berjangka bank) akan ('ya') atau tidak ('tidak') dilanggan oleh pelanggan atau tidak. Folder data berisi dua kumpulan data: -

train.csv: 45.211 baris dan 18 kolom diurutkan berdasarkan tanggal (dari Mei 2008 hingga November 2010)

test.csv: 4521 baris dan 18 kolom dengan 10% contoh (4521), dipilih secara acak dari train.csv


## Halaman 
 - [Setup](#Setup)
 
##Setup
  ```python
  import pathlib
  import tensorflow as tf
  import zipfile
  import os
  import matplotlib.pyplot as plt
  import pandas as pd
  import numpy as np
  import seaborn as sns
  from google.colab import drive
  from google.colab import data_table
  import tensorflow as tf
  from sklearn.metrics import confusion_matrix
  ```
