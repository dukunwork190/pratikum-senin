# Praktikum Pemrograman Web
1. Pengertian Bootstrap dan KegunaannyaBootstrap adalah sebuah framework front-end sumber terbuka (open-source) yang dirancang untuk mempercepat dan mempermudah pengembangan situs web yang responsif serta berorientasi pada perangkat seluler (mobile-first).   Kegunaan utama Bootstrap adalah menyediakan kumpulan komponen antarmuka (UI components) siap pakai seperti tombol, bilah navigasi (navbar), formulir, dan kartu, serta sistem grid dan kelas utilitas CSS yang konsisten agar pengembang tidak perlu membangun tata letak dari nol.   
2. Cara Memasang BootstrapBeberapa cara untuk mengimpor atau menggunakan Bootstrap ke dalam suatu proyek web meliputi:Menggunakan CDN (Content Delivery Network) dengan menyertakan tautan CSS resmi di dalam tag <head> dan skrip JavaScript di bagian bawah dokumen HTML.   Mengunduh file compiled CSS and JS secara langsung dari situs resmi Bootstrap dan menyimpannya ke dalam struktur folder proyek lokal.   Menggunakan manajer paket seperti npm atau yarn melalui perintah instalasi terminal pada proyek berbasis Node.js.   
3. Grid dan BreakpointClass Grid: Sistem tata letak berbasis flexbox di dalam Bootstrap yang tersusun atas wadah (container), baris (row), dan kolom (col) untuk mengatur penataan elemen secara terstruktur dalam 12 kolom per baris.   Breakpoint: Titik batas ukuran layar (viewport width) yang menggunakan media queries untuk menentukan bagaimana sistem grid dan komponen beradaptasi pada berbagai ukuran perangkat.   
4. Class Bootstrap Beserta KegunaannyaLima contoh kelas (class) yang disediakan oleh Bootstrap beserta kegunaannya:container atau container-fluid: Berfungsi untuk membungkus konten dan menyediakan lebar tetap yang responsif atau lebar penuh secara dinamis.   row: Berfungsi sebagai pembungkus horizontal untuk menampung kolom-kolom dalam sistem grid.   col-*: Berfungsi untuk mendefinisikan lebar kolom dalam grid 12 kolom pada berbagai ukuran breakpoint.   btn dan btn-success: Berfungsi untuk mengubah elemen HTML menjadi komponen tombol bergaya standar dengan variasi warna hijau tertentu.   shadow-sm atau shadow: Berfungsi untuk memberikan efek bayangan (box-shadow) pada elemen agar tampak berlapis dan rapi.   
5. Gambar ResponsifCara membuat gambar pada website menjadi responsif agar menyesuaikan ukuran layar perangkat adalah dengan menambahkan class img-fluid pada elemen tag <img>.   Kelas ini menerapkan properti CSS max-width: 100% dan height: auto sehingga gambar secara otomatis mengecil atau membesar proporsional mengikuti lebar kontainer induknya tanpa merusak rasio aspek.   
6. HTML<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ruang Baca - Login</title>
    <!-- Memuat Bootstrap 5.3.8 CSS CDN -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body class="bg-light">

    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-success px-4">
        <div class="container-fluid">
            <a class="navbar-brand fw-bold" href="#">Ruang Baca</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#">Beranda</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Tentang</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Bantuan</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Konten Utama / Form Login -->
    <div class="container d-flex justify-content-center align-items-center" style="min-height: 85vh;">
        <div class="row w-100 justify-content-center">
            <div class="col-md-6 col-lg-5 col-xl-4">
                <div class="card shadow-sm border-0 p-4 bg-white rounded-4">
                    <div class="card-body text-center">
                        <h3 class="fw-bold mb-1">Masuk ke Ruang Baca</h3>
                        <p class="text-muted small mb-4">Temukan bacaan untuk hari ini</p>
                        
                        <form>
                            <div class="mb-3 text-start">
                                <label for="username" class="form-label text-secondary small">Username</label>
                                <input type="text" class="form-control" id="username" placeholder="Masukkan username">
                            </div>
                            
                            <div class="mb-3 text-start">
                                <label for="password" class="form-label text-secondary small">Password</label>
                                <input type="password" class="form-control" id="password" placeholder="Masukkan password">
                            </div>
                            
                            <div class="mb-3 form-check text-start">
                                <input type="checkbox" class="form-check-input" id="rememberMe">
                                <label class="form-check-label small" for="rememberMe">Ingat saya</label>
                            </div>
                            
                            <div class="d-grid mb-3">
                                <button type="submit" class="btn btn-success py-2">Masuk</button>
                            </div>
                            
                            <div>
                                <a href="#" class="text-decoration-none small text-success">Lupa password?</a>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Memuat Bootstrap 5.3.8 JS Bundle CDN -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
