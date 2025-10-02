# Lab2Web

## MUHAMAD WAFA MUFIDA ZULFI
## TI.24.A4
## 312410334
## PEMOGRAMAN WEB 1
## AGUNG NUGROHO, S.Kom., M.Kom.

### 1. Eksperimen CSS dengan CSS Cheat Sheet

```
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Eksperimen CSS</title>
    <style>
        h1 {
            color: blue;
            text-align: center;
            font-size: 40px;
        }

        p {
            color: green;
            font-style: italic;
            background-color: #f0f0f0;
            padding: 10px;
            border: 2px solid black;
        }
    </style>
</head>
<body>
    <h1>Halo, ini eksperimen CSS!</h1>
    <p>Belajar CSS jadi lebih mudah kalau sambil praktik.</p>
</body>
</html>
````

### 2. Perbedaan h1 {...} dengan #intro h1 {...}

Semua elemen di halaman akan mendapatkan style tersebut.
(Selector global untuk semua h1).

Hanya elemen yang berada di dalam elemen dengan id="intro" yang akan terkena style.
(Selector spesifik ke elemen tertentu).


```
<style>
    h1 {
        color: red;
    }

    #intro h1 {
        color: blue;
    }
</style>

<div>
    <h1>Judul 1 (merah)</h1>
</div>

<div id="intro">
    <h1>Judul 2 (biru karena ada dalam #intro)</h1>
</div>
````
### 3. Urutan Prioritas (Internal, Eksternal, Inline CSS)

Urutan prioritas CSS:

Inline CSS → style langsung di elemen → paling kuat

Internal CSS → di dalam <style> pada file HTML

Eksternal CSS → di file .css terpisah

👉 Kalau ada konflik, maka Inline > Internal > Eksternal.

Contoh:
```
<head>
    <!-- Eksternal CSS -->
    <link rel="stylesheet" href="style.css">

    <!-- Internal CSS -->
    <style>
        p {
            color: blue;
        }
    </style>
</head>
<body>
    <!-- Inline CSS -->
    <p style="color: red;">Teks ini berwarna merah (inline lebih kuat)</p>
</body>
```

📌 Hasil: Teks jadi merah, walaupun internal biru & eksternal misalnya hijau.

### 4. Jika Elemen Punya ID dan Class (Siapa Menang?)

👉 Urutan spesifisitas selector CSS:

Inline Style (terkuat)

ID Selector (#id) lebih kuat daripada

Class Selector (.class) lebih kuat daripada

Elemen selector (p, h1, div)

Contoh:
````
<style>
    p {
        color: green;
    }

    .text-paragraf {
        color: blue;
    }

    #paragraf-1 {
        color: red;
    }
</style>

<p id="paragraf-1" class="text-paragraf">
    Ini paragraf contoh
</p>
````

📌 Hasil: Paragraf akan berwarna merah, karena ID lebih kuat daripada Class maupun selector elemen p.

✅ Jadi kesimpulannya:

h1 berlaku umum, #intro h1 lebih spesifik.

Prioritas CSS: Inline > Internal > Eksternal.

ID lebih kuat dari Class.

