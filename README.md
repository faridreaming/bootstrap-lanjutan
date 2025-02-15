# # Online Resume/CV dengan Bootstrap (Dark Mode)

## 🎯 Tujuan

- Membuat resume online sederhana menggunakan **Bootstrap**
- Menambahkan **Dark Mode** menggunakan Bootstrap Theme Toggle
- Memastikan proyek lengkap dengan semua komponen utama

---

## 🛠️ Tools & Teknologi

- **Bootstrap 5** (CDN)
- **HTML, CSS, JavaScript**
- **Font Awesome** (ikon)
- **Lorem Picsum** (gambar placeholder)

---

## 1️⃣ Setup Proyek

Buat folder proyek dan file utama:

```
resume/
 ├── index.html
 ├── style.css
 ├── script.js
 ├── img/
```

Gunakan Bootstrap CDN di **index.html**:

```html
<!doctype html>
<html lang="en" data-bs-theme="light">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Online Resume</title>
    <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css"
    />
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script src="script.js"></script>
  </body>
</html>
```

---

## 2️⃣ Navbar dengan Dark Mode Toggle

Tambahkan navigasi di bagian atas dengan **dark mode toggle**:

```html
<nav class="navbar navbar-expand-lg bg-body-tertiary">
  <div class="container">
    <a class="navbar-brand" href="#">My Resume</a>
    <button
      class="navbar-toggler"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarNav"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item"><a class="nav-link" href="#about">About</a></li>
        <li class="nav-item">
          <a class="nav-link" href="#experience">Experience</a>
        </li>
        <li class="nav-item"><a class="nav-link" href="#skills">Skills</a></li>
        <li class="nav-item">
          <a class="nav-link" href="#contact">Contact</a>
        </li>
        <li class="nav-item">
          <button id="theme-toggle" class="btn btn-outline-dark">🌙</button>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

---

## 3️⃣ Hero Section

Tambahkan hero dengan tinggi penuh:

```html
<header
  class="d-flex align-items-center justify-content-center text-center"
  style="height: 100vh;"
>
  <div>
    <h1>Nama Anda</h1>
    <p>Web Developer | UI/UX Designer</p>
    <a href="#contact" class="btn btn-primary">Hire Me</a>
  </div>
</header>
```

---

## 4️⃣ Struktur Resume

Gunakan Bootstrap untuk membuat layout dengan **Container, Row, Col**:

```html
<div class="container mt-5" id="about">
  <div class="row">
    <div class="col-md-4 text-center">
      <img
        src="https://picsum.photos/200"
        class="rounded-circle img-fluid"
        alt="Profile"
      />
      <h2 class="mt-3">Nama Anda</h2>
      <p>Web Developer | UI/UX Designer</p>
    </div>
    <div class="col-md-8">
      <h3>About Me</h3>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit...</p>
    </div>
  </div>
</div>
```

---

## 5️⃣ Experience & Skills

Tambahkan **Experience, Skills, dan Contact**:

```html
<div class="container mt-4" id="experience">
  <h3>Experience</h3>
  <ul>
    <li>Frontend Developer - XYZ Company</li>
    <li>Intern UI/UX - ABC Studio</li>
  </ul>
</div>

<div class="container mt-4" id="skills">
  <h3>Skills</h3>
  <div class="progress">
    <div class="progress-bar bg-primary" style="width: 80%;">HTML & CSS</div>
  </div>
  <div class="progress mt-2">
    <div class="progress-bar bg-warning" style="width: 70%;">JavaScript</div>
  </div>
</div>
```

---

## 6️⃣ Dark Mode Toggle dengan Bootstrap

Di **script.js**, tambahkan kode untuk toggle dark mode di seluruh halaman:

```js
document.getElementById("theme-toggle").addEventListener("click", function () {
  let html = document.documentElement;
  let currentTheme = html.getAttribute("data-bs-theme");
  let newTheme = currentTheme === "light" ? "dark" : "light";
  html.setAttribute("data-bs-theme", newTheme);
});
```

---

## 7️⃣ Contact Section

Tambahkan formulir kontak sederhana:

```html
<div class="container mt-4" id="contact">
  <h3>Contact Me</h3>
  <form>
    <div class="mb-3">
      <label class="form-label">Name</label>
      <input type="text" class="form-control" />
    </div>
    <div class="mb-3">
      <label class="form-label">Email</label>
      <input type="email" class="form-control" />
    </div>
    <div class="mb-3">
      <label class="form-label">Message</label>
      <textarea class="form-control"></textarea>
    </div>
    <button type="submit" class="btn btn-primary">Send</button>
  </form>
</div>
```

---

## 8️⃣ Footer & Responsiveness

Tambahkan **footer dan pastikan responsif**:

```html
<footer class="text-center mt-4 p-3 bg-body-tertiary">
  &copy; 2025 Nama Anda. All Rights Reserved.
</footer>
```

Gunakan Bootstrap Grid untuk **mobile-friendly** design.

---

## 🎉 Hasil Akhir

Sebuah Online Resume **responsive** dengan **Dark Mode** yang menggunakan Bootstrap Theme Toggle!

---

## 🚀 Next Steps

- Tambahkan **portofolio** dengan Bootstrap Cards
- Gunakan **GitHub Pages** untuk hosting gratis
- Integrasikan dengan **Google Fonts** untuk tampilan lebih menarik

---

Selamat mencoba! 🚀
