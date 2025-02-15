# Materi Bootstrap Dasar - Lengkap dengan Dark Mode dan Komponen Lanjutan

## 1. Pengenalan Bootstrap

### Apa itu Bootstrap?

Bootstrap adalah framework CSS open-source yang dirancang untuk membantu pengembang dalam membangun situs web yang responsif dan mobile-first dengan cepat. Bootstrap menyediakan sistem grid, komponen UI siap pakai, serta berbagai utilitas untuk styling.

### Mengapa Menggunakan Bootstrap?

- Mempercepat pengembangan web
- Responsif secara default
- Dukungan komponen UI yang lengkap
- Dokumentasi yang luas dan komunitas besar

## 2. Instalasi Bootstrap

### a) Menggunakan CDN

Cara termudah menggunakan Bootstrap adalah dengan menyertakan link ke CDN dalam HTML:

```html
<!doctype html>
<html lang="id">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Bootstrap Dasar</title>
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css"
      rel="stylesheet"
    />
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
  </head>
  <body>
    <h1>Hello, Bootstrap!</h1>
  </body>
</html>
```

### b) Menggunakan Paket NPM

Jika ingin mengelola dependensi dengan NPM:

```sh
npm install bootstrap
```

Lalu impor di dalam proyek JavaScript:

```js
import "bootstrap/dist/css/bootstrap.min.css";
import "bootstrap/dist/js/bootstrap.bundle.min.js";
```

## 3. Sistem Grid Bootstrap

Bootstrap menggunakan sistem grid berbasis 12 kolom untuk mengatur layout.

```html
<div class="container">
  <div class="row">
    <div class="col-md-6 bg-primary text-white p-3">Kolom 1 (6/12)</div>
    <div class="col-md-6 bg-secondary text-white p-3">Kolom 2 (6/12)</div>
  </div>
</div>
```

## 4. Komponen Dasar Bootstrap

### a) Navbar

```html
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <div class="container">
    <a class="navbar-brand" href="#">MyWebsite</a>
    <button
      class="navbar-toggler"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarNav"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item"><a class="nav-link" href="#">Home</a></li>
        <li class="nav-item"><a class="nav-link" href="#">About</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Contact</a></li>
      </ul>
    </div>
  </div>
</nav>
```

### b) Card

```html
<div class="card" style="width: 18rem;">
  <img src="https://via.placeholder.com/150" class="card-img-top" alt="..." />
  <div class="card-body">
    <h5 class="card-title">Judul Kartu</h5>
    <p class="card-text">Deskripsi singkat tentang kartu ini.</p>
    <a href="#" class="btn btn-primary">Lihat Selengkapnya</a>
  </div>
</div>
```

### c) Form

```html
<form>
  <div class="mb-3">
    <label class="form-label">Email</label>
    <input type="email" class="form-control" placeholder="Masukkan email" />
  </div>
  <button type="submit" class="btn btn-success">Submit</button>
</form>
```

## 5. Dark Mode dengan Bootstrap

Bootstrap mendukung dark mode dengan class `data-bs-theme="dark"`.

```html
<body data-bs-theme="dark"></body>
```

Namun, untuk dark mode yang bisa diubah oleh pengguna, kita bisa menggunakan JavaScript:

```html
<button id="toggleTheme" class="btn btn-warning">Toggle Dark Mode</button>
<script>
  const toggleButton = document.getElementById("toggleTheme");
  toggleButton.addEventListener("click", () => {
    document.body.dataset.bsTheme =
      document.body.dataset.bsTheme === "dark" ? "light" : "dark";
  });
</script>
```

## 6. Proyek Praktik: Portfolio Sederhana

Kita akan membuat halaman portfolio sederhana dengan fitur dark mode.

```html
<!doctype html>
<html lang="id">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Portfolio</title>
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css"
      rel="stylesheet"
    />
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
  </head>
  <body data-bs-theme="light">
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
      <div class="container">
        <a class="navbar-brand" href="#">Portfolio</a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNav"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item"><a class="nav-link" href="#">Home</a></li>
            <li class="nav-item"><a class="nav-link" href="#">Projects</a></li>
          </ul>
        </div>
      </div>
    </nav>

    <div class="container mt-5">
      <button id="toggleTheme" class="btn btn-warning mb-3">
        Toggle Dark Mode
      </button>
      <div class="row">
        <div class="col-md-4">
          <div class="card">
            <img
              src="https://via.placeholder.com/150"
              class="card-img-top"
              alt="Project"
            />
            <div class="card-body">
              <h5 class="card-title">Project 1</h5>
              <p class="card-text">Deskripsi singkat.</p>
              <a href="#" class="btn btn-primary">Lihat</a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <script>
      const toggleButton = document.getElementById("toggleTheme");
      toggleButton.addEventListener("click", () => {
        document.body.dataset.bsTheme =
          document.body.dataset.bsTheme === "dark" ? "light" : "dark";
      });
    </script>
  </body>
</html>
```

## Kesimpulan

Dengan menggunakan Bootstrap, kita dapat membuat halaman web yang responsif dan modern dengan cepat. Dark mode serta berbagai komponen UI membantu meningkatkan pengalaman pengguna.
