# Tutorial

## Halaman
 - [Boxplot](#Boxplot)
 - [Precission](#Precission)
 - [Recall](#Recall)
 - [Specificity](#Specificity)
 - [Deployment Tensorflow Serving](#Deployment)

## Boxplot
Nilai-nilai yang termuat pada boxplot antara lain meliputi nilai minimum, kuartil bawah (Q1), kuartil tengah (Q2) atau median (Me), kuartil atas (Q3), dan nilai maksimum. Cara membaca boxplot secara umum mengikuti keterangan nilai-nilai pada boxplot berikut.

![Cara-Membaca-Boxplot](https://user-images.githubusercontent.com/109187938/179443098-4c5bbaf7-8fec-448a-842b-0ba78099a5ab.jpg)

**Data simetris (berdistribusi normal)** ditunjukkan oleh boxplot dengan garis median berada di tengah kotak. Selain itu data simetris juga ditunjukkan oleh panjang whisker bawah sama dengan panjang whisker bawah, serta tidak terdapat nilai outlier dan ekstrim.

![Boxplot-dengan-Data-Berdistribusi-Normal](https://user-images.githubusercontent.com/109187938/179443880-082f66b0-3267-4bf3-be2e-143bc1dce559.jpg)

**Data miring (tidak simetris)** ditunjukkan oleh boxplot dengan letak garis median tidak berada di tengah kotak. Data miring juga ditandai dari panjang whisker tidak sama antara atas-bawah atau kanan-kiri. Whisker atas lebih panjang dan terdapat outlier di bagian atas menandakan data cenderung miring ke kanan ***(positive skewness)***. Whisker bawah lebih panjang dan terdapat outlier di bagian bawah menandakan data cenderung miring ke kiri ***(negative skewness)***.

![Boxplot-dengan-Data-Tidak-Simetrik-atau-Miring](https://user-images.githubusercontent.com/109187938/179443968-3dd471a0-1915-4b58-a6b1-7c64a2f215ea.jpg)

## Precission

Merupakan rasio prediksi benar positif dibandingkan dengan keseluruhan hasil yang diprediksi positf. Precission menjawab pertanyaan “Berapa persen konsumen yang benar berlangganan dari keseluruhan mahasiswa yang diprediksi berlangganan?”

Precission = **(TP) / (TP+FP)**

## Recall (Sensitifitas)

Merupakan rasio prediksi benar positif dibandingkan dengan keseluruhan data yang benar positif. Recall menjawab pertanyaan “Berapa persen konsumen yang diprediksi berlangganan dibandingkan keseluruhan mahasiswa yang sebenarnya berlangganan”.

Recall = **(TP) / (TP + FN)**


## Specificity

Merupakan kebenaran memprediksi negatif dibandingkan dengan keseluruhan data negatif. Specificity menjawab pertanyaan “Berapa persen konsumen yang benar diprediksi tidak berlangganan dibandingkan dengan keseluruhan konsumen yang sebenarnya tidak berlangganan”.

Specificity = **(TN)/ (TN + FP)**

## Deployment
```bash
docker run --name fintech_portugies -it -v /home/keluarga-gigih/model_fintech_portugies:/model_fintech_portugies -e MODEL_NAME=fintech_portugies -p 8601:8601 --entrypoint /bin/bash tensorflow/serving
```

```bash
docker run -it -v /home/keluarga-gigih/model_fintech_portugies:/model_fintech_portugies -e MODEL_NAME=fintech_portugies -p 8601:8601 --entrypoint /bin/bash tensorflow/serving
```
