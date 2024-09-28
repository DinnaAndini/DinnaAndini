# Exploratory Data Analysis
## 1. Load Data
"Load data" pada Python berarti membaca atau mengambil data dari sumber eksternal (seperti kaggle, BPS, satudata, dll) ke dalam program Python agar dapat digunakan atau dianalisis lebih lanjut. Ini biasanya dilakukan dengan menggunakan pustaka atau modul tertentu seperti pandas untuk bekerja dengan data berbentuk tabel, seperti CSV atau Excel.

contoh :

input
```sh
import pandas as pd
df = pd.read_csv("C:/Users/ACER/Downloads/Spotify Most Streamed Songs.csv")
df
```
Dari contoh diatas, kita tahu, bahwa dengan menggunakan library pandas, kita bisa membaca file CSV menggunakan python.

## 2. Basic Information about the Dataset
input
```sh
df.head()
```
```sh
df.tail()
```
Dengan menggunakan 'df.head()' dan 'df.tail(), kita dapat mengetahui 5 informasi teratas dan terbawah dari file diatas.

input
```sh
df.info()
```
Dengan menggunakan 'df.info()', kita dapat mengetahui tipe data dari dataset yang sedang diekplorasi.

input
```sh
df.describe()
```
Dengan menggunakan 'df.describe()', kita dapat mengetahui statistika deskriptif dari dataset tersebut.

## 3. Cek Nilai Duplikat dan Nilai Unik
##### Nilai Duplikat
Untuk mengetahui dalam dataset tersebut ada nilai duplikatnya atau tidak, kita bisa menggunakan metode 'df.duplicated().sum()'.

input
```sh
duplikat = df.duplicated().sum()
print(duplikat)
```
output
```sh
0
```
Dari output diatas kita dapat mengetahui bahwa dataset tersebut tidak memiliki nilai duplikat.
##### Nilai Unik
input
```sh
unik = df.nunique()
print(unik)
```
output
```sh
track_name              943
artist(s)_name          645
artist_count              8
released_year            50
released_month           12
released_day             31
in_spotify_playlists    879
in_spotify_charts        82
streams                 949
in_apple_playlists      234
in_apple_charts         172
in_deezer_playlists     348
in_deezer_charts         34
in_shazam_charts        198
bpm                     124
key                      11
mode                      2
danceability_%           72
valence_%                94
energy_%                 80
acousticness_%           98
instrumentalness_%       39
liveness_%               68
speechiness_%            48
cover_url               535
dtype: int64
```

## 4. Visualisasi Jumlah Nilai Unik
input
```sh
unik.plot(kind='hist')
```
output
```sh
<Axes: ylabel='Frequency'>
```
![image](https://github.com/user-attachments/assets/6d0b7c76-4236-4a4f-8b35-41697cab4e91)
Dengan menggunakan 'plot' kita dapat mengetahui grafik dari nilai unik.

## 5. Menemukan Null Values
Dengan menggunakan metode 'isnull()' atau 'isna()' kita dapat mengetahui missing value dari sebuah dataset.

input
```sh
null_values = df.isnull().sum()
print(null_values)
```
output
```sh
track_name               0
artist(s)_name           0
artist_count             0
released_year            0
released_month           0
released_day             0
in_spotify_playlists     0
in_spotify_charts        0
streams                  0
in_apple_playlists       0
in_apple_charts          0
in_deezer_playlists      0
in_deezer_charts         0
in_shazam_charts        50
bpm                      0
key                     95
mode                     0
danceability_%           0
valence_%                0
energy_%                 0
acousticness_%           0
instrumentalness_%       0
liveness_%               0
speechiness_%            0
cover_url                0
dtype: int64
```
Dari output diatas, kita dapat mengetahui missing value dari dataset yaitu pada kolom 'in_shazam_charts' dengan jumlah missing value 50 dan pada kolom 'key' dengan jumlah missing value 95.

## 6. Replace Semua Null Values
input
```sh
df['in_shazam_charts'].fillna('Unknown', inplace=True)
df['key'].fillna('Unknown', inplace=True)
```
Dengan menggunakan metode diatas kita dapat mengubah nilai yang tadinya nol menjadi unknown. 

Setelah itu, kita cek apakah masih ada missing value atau tidak dengan metode yang sama yaitu menggunakan 'isnull'.
input
```sh
df_after_cleaning = df.isnull().sum()
df_after_cleaning
```
output
```sh
track_name              0
artist(s)_name          0
artist_count            0
released_year           0
released_month          0
released_day            0
in_spotify_playlists    0
in_spotify_charts       0
streams                 0
in_apple_playlists      0
in_apple_charts         0
in_deezer_playlists     0
in_deezer_charts        0
in_shazam_charts        0
bpm                     0
key                     0
mode                    0
danceability_%          0
valence_%               0
energy_%                0
acousticness_%          0
instrumentalness_%      0
liveness_%              0
speechiness_%           0
cover_url               0
dtype: int64
```
Kita bisa ketahui, setelah replace menggunakan metode 'fillna', database tersebut sudah tidak memiliki missing value.

## 7. Filter data
input
```sh
df_filter = df[['track_name','artist(s)_name']][(df['released_year']== 2023)]
df_filter
```
Dengan code diatas, kita dapat mengetahui penyanyi yang meriliskan lagunya pada tahun 2023.

## 8. Create a Box Plot
input
```sh
import matplotlib.pyplot as plt
plt.boxplot(df.released_month)
```
Dengan code diatas kita dapat mengetahui box plot dari kolom 'released_month'.

output

![image](https://github.com/user-attachments/assets/b921b15f-ea76-41c2-a2b3-44b755c826b0)

## 9. Correlation
input
```sh
correlation = df.corr()
correlation
```
Dengan menggunakan metode 'corr', kita dapat mengetahui korelasi dari sebuah database.
