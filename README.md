# Youpi 1
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Perpustakaan Digital</title>
    <style>
        /* Reset dan style dasar */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f4f4f4;
        }
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #6e8efb, #a777e3);
            color: white;
            padding: 1rem 0;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        nav {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            margin-bottom: 1rem;
        }
        .nav-links {
            list-style: none;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
        }
        .nav-links li {
            margin: 0 10px;
        }
        .nav-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s ease;
        }
        .nav-links a:hover {
            color: #ffd700;
        }

        /* Search Bar */
        .search-container {
            width: 100%;
            max-width: 600px;
            margin: 1rem auto 0;
        }
        .search-form {
            display: flex;
        }
        .search-input {
            flex-grow: 1;
            padding: 0.75rem;
            border: 2px solid #ddd;
            border-right: none;
            border-top-left-radius: 5px;
            border-bottom-left-radius: 5px;
        }
        .search-btn {
            padding: 0.75rem 1.5rem;
            background: #ffd700;
            color: #333;
            border: none;
            border-top-right-radius: 5px;
            border-bottom-right-radius: 5px;
            cursor: pointer;
            transition: background 0.3s ease;
        }
        .search-btn:hover {
            background: #ffec8b;
        }

        /* Hero Section */
        .hero {
            background: url('fiksilatar.jpeg') center/cover no-repeat;
            height: 400px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            position: relative;
        }
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0,0,0,0.5);
        }
        .hero-content {
            position: relative;
            z-index: 1;
        }
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }
        .btn {
            display: inline-block;
            background: #ffd700;
            color: #333;
            padding: 0.75rem 1.5rem;
            text-decoration: none;
            border-radius: 5px;
            transition: background 0.3s ease;
        }
        .btn:hover {
            background: #ffec8b;
        }

        /* Kategori Buku */
        .categories {
            padding: 3rem 0;
        }
        .categories h2 {
            text-align: center;
            margin-bottom: 2rem;
            color: #333;
        }
        .category-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
        }
        .category-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }
        .category-card:hover {
            transform: translateY(-5px);
        }
        .category-card img {
            width: 100%;
            height: 150px;
            object-fit: cover;
        }
        .category-card h3 {
            padding: 1rem;
            text-align: center;
        }

        /* Koleksi Terbaru */
        .new-collection {
            background: #e9ecef;
            padding: 3rem 0;
        }
        .new-collection h2 {
            text-align: center;
            margin-bottom: 2rem;
            color: #333;
        }
        .book-slider {
            display: flex;
            overflow-x: auto;
            padding-bottom: 1rem;
        }
        .book-card {
            flex: 0 0 auto;
            width: 200px;
            margin-right: 1rem;
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        .book-card img {
            width: 100%;
            height: 250px;
            object-fit: cover;
        }
        .book-info {
            padding: 1rem;
        }
        .book-info h3 {
            font-size: 1rem;
            margin-bottom: 0.5rem;
        }
        .book-info p {
            font-size: 0.9rem;
            color: #666;
        }

        /* Footer */
        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 1rem 0;
            margin-top: 2rem;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-links {
                flex-direction: column;
                align-items: center;
            }
            .nav-links li {
                margin: 5px 0;
            }
            .hero h1 {
                font-size: 2rem;
            }
            .hero p {
                font-size: 1rem;
            }
            .category-grid {
                grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            }
            .book-card {
                width: 150px;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav class="container">
            <div class="logo">📚 Perpustakaan Digital</div>
            <ul class="nav-links">
                <li><a href="PERPUSTAKAAN.html">Beranda</a></li>
                <li><a href="KATEGORI.html">Kategori</a></li>
                <li><a href="KOLEKSI.html">Koleksi Baru</a></li>
                <li><a href="about.html">Tentang</a></li>
                <li><a href="services.html">Layanan</a></li>
                <li><a href="contact.html">Kontak</a></li>
            </ul>
            <div class="search-container">
                <form class="search-form">
                    <input type="text" class="search-input" placeholder="Cari judul buku atau penulis...">
                    <button type="submit" class="search-btn">Cari</button>
                </form>
            </div>
        </nav>
    </header>

    <main>
        <section class="hero">
            <div class="hero-content">
                <h1>Selamat Datang di Perpustakaan Digital</h1>
                <p>Temukan ribuan buku dari berbagai genre</p>
                <a href=""class="btn">Jelajahi Sekarang</a>
            </div>
        </section>

        <section id="categories" class="categories container">
            <h2>Kategori Buku</h2>
            <div class="category-grid">
                <a href="KATEGORI.html" class="category-card">
                    <img src="fiksi.png" alt="Fiksi">
                    <h3>Fiksi</h3>
                </a>
                <a href="KATEGORI.html" class="category-card">
                    <img src="fiksi1.png" alt="Non-Fiksi">
                    <h3>Non-Fiksi</h3>
                </a>
                <a href="KATEGORI.html" class="category-card">
                    <img src="fiksi2.png" alt="Pendidikan">
                    <h3>Pendidikan</h3>
                </a>
                <a href="KATEGORI.html" class="category-card">
                    <img src="fiksi3.png" alt="Anak-anak">
                    <h3>Anak-anak</h3>
                </a>
            </div>
        </section>

        <section id="new-collection" class="new-collection">
            <div class="container">
                <h2>Koleksi Terbaru</h2>
                <div class="book-slider">
                    <a href="book1.html" class="book-card">
                        <img src="fiksi7.png" alt="Buku 1">
                        <div class="book-info">
                            <h3>Hujan</h3>
                            <p>Penulis: Tere liye</p>
                        </div>
                    </a>
                    <a href="book2.html" class="book-card">
                        <img src="fiksi4.png" alt="Buku 2">
                        <div class="book-info">
                            <h3>Pulang</h3>
                            <p>Penulis: Tere Liye</p>
                        </div>
                    </a>
                    <a href="book3.html" class="book-card">
                        <img src="fiksi6.png" alt="Buku 3">
                        <div class="book-info">
                            <h3>Judul Bumi</h3>
                            <p>Penulis: Tere liye</p>
                        </div>
                    </a>
                    <a href="book4.html" class="book-card">
                        <img src="fiksi5.png" alt="Buku 4">
                        <div class="book-info">
                            <h3>Pergi</h3>
                            <p>Penulis: Tere Liye</p>
                        </div>
                    </a>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <p>&copy; 2024 Perpustakaan Digital. Hak Cipta Dilindungi.</p>
    </footer>
</body>
</html>
