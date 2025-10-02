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

h1 {...}
→ Semua elemen <h1> di halaman akan mendapatkan style tersebut.
(Selector global untuk semua h1).

#intro h1 {...}
→ Hanya elemen <h1> yang berada di dalam elemen dengan id="intro" yang akan terkena style.
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
