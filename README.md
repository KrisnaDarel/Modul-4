# Modul-4
#### Nama: Krisna Darel A.
#### Kelas: XII RPL 1
#### No Absen: 31

### View Blade Template.
>Tugas 1 membuat view untuk project anda.

#### 1.Membuat folder dan file yang akan di isi.

Nama folder yang harus dibuat. 
- barang
- kategori
- layout

Nama file yang harus dibuat.
- home.blade.php
- index.blade.php
- app.blade.php

Folder dan file-file nya menjadi satu seperti. 

![image](https://user-images.githubusercontent.com/109930564/183358390-12755e76-f2dd-4bbc-ad20-72589548be66.png)

>Tugas 2 membuat layout dengan master template blade untuk project anda.

#### 2.Pada folder layout `file app.blade.php` kita mengambil **css dan js di bootstrap** ini linknya.

[Bootstrap](https://getbootstrap.com/docs/5.2/getting-started/introduction/)
>![image](https://user-images.githubusercontent.com/109929687/183342789-f6776591-ea33-4712-88ac-e847218de516.png)

gambar diatas adalah bagian bootstrap yang kita pakai sebagai css dengan menambahkan syntax sebagai berikut.
```
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css">
```

selanjutnya bagian js dengan menambahkan syntax sebagai berikut.
```
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/js/bootstrap.bundle.min.js"></script>
```

Selanjutnya isi file `app.blade.php` dengan all codenya
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>@yield('title')</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-gH2yIJqKdNHPEq0n4Mqa/HGKIhSkIHeL5AyhkYV8i59U5AR6csBvApHHNl/vI1Bx" crossorigin="anonymous">

</head>
<body>
    <!-- untuk navbar -->
    <div class="container">
    <nav class="navbar navbar-expand-lg bg-light">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Penjualan</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="/">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/kategori">Kategori</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/barang">barang</a>
        </li>
        
    </div>
  </div>
</nav>
    </div>
    <!-- content -->
    <div class="container">
    @yield('content')
    </div>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/js/bootstrap.bundle.min.js" integrity="sha384-A3rJD856KowSb7dwlZdYEkO39Gagi7vIsF0jrRAoQmDKKtQBHUuLZ9AsSv4jD4Xa" crossorigin="anonymous"></script>
</body>
</html>
```
saya tidak menggunakan cara yang saya jelaskan karena di bootstrap sudah ada yang mudah jadi saya tinggal copy dan paste saja.

Selanjutnya folder **barang** yang berisi file `home.blade.php`.

all codenya akan terlihat seperti dibawah ini karena kurang lebih saya memahami isi code dibawah.
```
@extends('layout.app')

@section('title')
    Barang
@endsection

@section('content')
<div class ="mt-3">
    <table class="table table-striped">
        <thead>
            <tr>
                <th width-5%>No,</th>
                <th>Nama</th>
                <th width-15%>Kategori</th>
                <th width-15%>Qty</th>
                <th width-20%>Harga Beli</th>
                <th width-20%>Harga Jual</th>
                <th width-15%>Aksi</th>
            </tr>
            </thead>

            <tbody>
                <tr>
                    <td>1</td>
                    <td>Meja</td>
                    <td>Aksesoris</td>
                    <td>10</td>
                    <td>100.000</td>
                    <td>300.000</td>
                    <td>Hapus | Edit</td>
                </tr>
           <tbody>
                <tr>
                    <td>1</td>
                    <td>Televisi</td>
                    <td>Elektronik</td>
                    <td>15</td>
                    <td>400.000</td>
                    <td>800.000</td>
                    <td>Hapus | Edit</td>
                </tr>
            </tbody>
        </tbody>
    </table>
    
</div>
@endsection
```
Selanjutnya pada folder **kategori** file `index.blade.php`.

all codenya akan ditampilkan di bawah ini.
```
@extends('layout.app')

@section('title')
    kategori
@endsection

@section('content')
<div class ="mt-3">
    <table class="table table-striped">
        <thead>
            <tr>
                <th width-5%>No,</th>
                <th>Nama</th>
                <th>Kategori</th>
                <th width-15%>Aksi</th>
            </tr>
            </thead>

            <tbody>
                <tr>
                    <td>1</td>
                    <td>Meja</td>
                    <td>Aksesoris</td>
                    <td>Hapus | Edit</td>
                </tr>
            </tbody>
            <tbody>
                <tr>
                    <td>2</td>
                    <td>Televisi</td>
                    <td>Aksesoris</td>
                    <td>Hapus | Edit</td>
                </tr>
            </tbody>
        </tbody>
    </table>

</div>
@endsection
```
