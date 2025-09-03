# Actividad-ulica-9---Template-HTML-CSS
alumna: Luciana Nadine Rojas
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HELLO WORLD - News Magazine</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Times New Roman', serif;
            background-color: #f5f5f5;
            color: #333;
        }

        .header {
            background: white;
            padding: 10px 0;
            border-bottom: 1px solid #ddd;
        }

        .top-bar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            font-size: 12px;
        }

        .logo-section {
            text-align: center;
            padding: 20px 0;
        }

        .logo-section h1 {
            font-size: 48px;
            letter-spacing: 8px;
            font-weight: normal;
            margin-bottom: 5px;
        }

        .tagline {
            font-size: 12px;
            letter-spacing: 2px;
        }

        .main-nav {
            background: white;
            border-top: 2px solid #333;
            border-bottom: 2px solid #333;
            padding: 15px 0;
        }

        .nav-list {
            display: flex;
            justify-content: center;
            list-style: none;
            max-width: 1200px;
            margin: 0 auto;
            gap: 40px;
        }

        .nav-list li {
            font-size: 14px;
            font-weight: bold;
            letter-spacing: 1px;
        }

        .nav-list a {
            text-decoration: none;
            color: #333;
            cursor: pointer;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 30px;
            padding: 30px 20px;
        }

        .main-content {
            background: white;
        }

        .featured-articles {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 15px;
            margin-bottom: 30px;
        }

        .article-card {
            text-align: center;
        }

        .article-card img {
            width: 100%;
            height: 120px;
            object-fit: cover;
            margin-bottom: 10px;
        }

        .article-card h3 {
            font-size: 14px;
            margin-bottom: 5px;
            line-height: 1.3;
        }

        .article-meta {
            font-size: 11px;
            color: #666;
        }

        .main-article {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-bottom: 40px;
        }

        .main-article-image {
            width: 100%;
            height: 400px;
            object-fit: cover;
        }

        .main-article-content h2 {
            font-size: 32px;
            line-height: 1.2;
            margin-bottom: 20px;
            font-weight: normal;
        }

        .author-info {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 15px;
        }

        .author-avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            object-fit: cover;
        }

        .recent-posts {
            margin-top: 40px;
        }

        .section-title {
            text-align: center;
            font-size: 24px;
            margin-bottom: 30px;
            font-weight: normal;
            letter-spacing: 2px;
        }

        .post-list {
            display: grid;
            gap: 20px;
        }

        .post-item {
            display: grid;
            grid-template-columns: 150px 1fr;
            gap: 15px;
            padding-bottom: 20px;
            border-bottom: 1px solid #eee;
        }

        .post-item img {
            width: 100%;
            height: 100px;
            object-fit: cover;
        }

        .post-content h4 {
            font-size: 16px;
            margin-bottom: 10px;
            line-height: 1.3;
        }

        .sidebar {
            background: white;
            padding: 20px;
            height: fit-content;
        }

        .popular-articles {
            margin-bottom: 30px;
        }

        .popular-item {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px solid #eee;
        }

        .popular-item img {
            width: 80px;
            height: 60px;
            object-fit: cover;
        }

        .popular-content {
            flex: 1;
        }

        .popular-content h5 {
            font-size: 14px;
            line-height: 1.3;
            margin-bottom: 5px;
        }

        .search-box {
            margin-bottom: 30px;
        }

        .search-box input {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            margin-bottom: 10px;
        }

        .search-box button {
            width: 100%;
            padding: 10px;
            background: #333;
            color: white;
            border: none;
            cursor: pointer;
        }

        .trending-section {
            margin-bottom: 30px;
        }

        .trending-item {
            margin-bottom: 15px;
        }

        .trending-item img {
            width: 100%;
            height: 150px;
            object-fit: cover;
            margin-bottom: 10px;
        }

        .tags-section {
            margin-bottom: 30px;
        }

        .tag {
            display: inline-block;
            background: #f0f0f0;
            padding: 5px 10px;
            margin: 5px;
            font-size: 12px;
            text-decoration: none;
            color: #333;
        }

        .footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 40px 0;
            margin-top: 40px;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 30px;
            padding: 0 20px;
        }

        .footer-section h3 {
            font-size: 16px;
            margin-bottom: 15px;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section ul li {
            margin-bottom: 8px;
        }

        .footer-section ul li a {
            color: #ccc;
            text-decoration: none;
            font-size: 14px;
        }

        .social-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 10px;
        }

        .social-grid img {
            width: 100%;
            height: 60px;
            object-fit: cover;
        }

        .pagination {
            text-align: center;
            margin: 30px 0;
        }

        .pagination a {
            display: inline-block;
            padding: 8px 15px;
            margin: 0 5px;
            text-decoration: none;
            color: #333;
            border: 1px solid #ddd;
        }

        .pagination a.active {
            background: #333;
            color: white;
        }

        .category-badge {
            background: #333;
            color: white;
            padding: 2px 8px;
            font-size: 10px;
            position: absolute;
            top: 10px;
            right: 10px;
        }

        .featured-large {
            position: relative;
            overflow: hidden;
        }
    </style>
</head>
<body>
    <header class="header">
        <div class="top-bar">
            <span>≡ MORE</span>
            <span>⊙ Friday 5 January 2024</span>
            <span>⊙ ⊗ ⊕ 🔍 SEARCH</span>
        </div>
        
        <div class="logo-section">
            <h1>HELLO WORLD</h1>
            <p class="tagline">∼ NEWSPAPER | MAGAZINE | PUBLISHER ∼</p>
        </div>

        <nav class="main-nav">
            <ul class="nav-list">
                <li><a href="#" onclick="showHome()">• HOME</a></li>
                <li><a href="#" onclick="showLayout()">• LAYOUT</a></li>
                <li><a href="#" onclick="showNews()">NEWS</a></li>
                <li><a href="#" onclick="showEconomy()">ECONOMY</a></li>
                <li><a href="#" onclick="showEntertainment()">• ENTERTAINMENT</a></li>
                <li><a href="#" onclick="showJobs()">JOBS</a></li>
            </ul>
        </nav>
    </header>

    <div id="content">
        <!-- HOME PAGE -->
        <div id="home-page">
            <div class="container">
                <main class="main-content">
                    <section class="featured-articles">
                        <article class="article-card">
                            <img src="https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?w=300&h=200&fit=crop" alt="Ciudad moderna">
                            <h3>Lorem ipsum del edificio moderno</h3>
                            <p class="article-meta">1 FEB 2024 • NO NEWS</p>
                        </article>
                        <article class="article-card">
                            <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=300&h=200&fit=crop" alt="Retrato">
                            <h3>Ut enim ad minima veniam quis</h3>
                            <p class="article-meta">28 JAN 2024 • FASHION</p>
                        </article>
                        <article class="article-card">
                            <img src="https://images.unsplash.com/photo-1551632811-561732d1e306?w=300&h=200&fit=crop" alt="Negocios">
                            <h3>Quis autem vel eum iure reprehenderit</h3>
                            <p class="article-meta">5 JAN 2024 • BUSINESS</p>
                        </article>
                        <article class="article-card">
                            <img src="https://images.unsplash.com/photo-1494790108755-2616c64c29b8?w=300&h=200&fit=crop" alt="Persona">
                            <h3>At vero eos et accusamus et iusto</h3>
                            <p class="article-meta">15 FEB 2024 • LIFESTYLE</p>
                        </article>
                    </section>

                    <section class="main-article">
                        <div class="featured-large">
                            <img src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?w=600&h=400&fit=crop" alt="Hombre barba blanca" class="main-article-image">
                            <span class="category-badge">Fashion, Man</span>
                        </div>
                        <div class="main-article-content">
                            <h2>Lorem ipsum dui sollic itudin praesent ut mollis primis eros torquent fames</h2>
                            <div class="author-info">
                                <img src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?w=80&h=80&fit=crop" alt="Steven Job" class="author-avatar">
                                <div>
                                    <strong>Steven Job</strong>
                                    <p style="font-size: 12px; color: #666;">3 FEB 2024</p>
                                </div>
                            </div>
                            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation...</p>
                        </div>
                    </section>

                    <section class="recent-posts">
                        <h2 class="section-title">∼∼∼ RECENT POSTS ∼∼∼</h2>
                        <div class="post-list">
                            <article class="post-item">
                                <img src="https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?w=200&h=150&fit=crop" alt="Edificios">
                                <div class="post-content">
                                    <h4>Magna aliqua ut enim ad minim veniam</h4>
                                    <div class="author-info">
                                        <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=30&h=30&fit=crop" alt="Writer" class="author-avatar">
                                        <small>Writer Six • POLITICS EDITOR • 18 JAN 2024</small>
                                    </div>
                                </div>
                            </article>

                            <article class="post-item">
                                <img src="https://images.unsplash.com/photo-1494790108755-2616c64c29b8?w=200&h=150&fit=crop" alt="Mujer">
                                <div class="post-content">
                                    <h4>Leitraeset sheeds containing Lorem Ipsum passages, and more recently</h4>
                                    <div class="author-info">
                                        <img src="https://images.unsplash.com/photo-1494790108755-2616c64c29b8?w=30&h=30&fit=crop" alt="Writer" class="author-avatar">
                                        <small>Writer Six • POLITICS EDITOR • 18 JAN 2024</small>
                                    </div>
                                </div>
                            </article>

                            <article class="post-item">
                                <img src="https://images.unsplash.com/photo-1517245386807-bb43f82c33c4?w=200&h=150&fit=crop" alt="Oficina">
                                <div class="post-content">
                                    <h4>There are many variations of passages of Lorem Ipsum available, but the majority have suffered</h4>
                                    <div class="author-info">
                                        <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=30&h=30&fit=crop" alt="Writer" class="author-avatar">
                                        <small>Writer Six • POLITICS EDITOR • 18 JAN 2024</small>
                                    </div>
                                </div>
                            </article>

                            <article class="post-item">
                                <img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=200&h=150&fit=crop" alt="Montañas">
                                <div class="post-content">
                                    <h4>It uses a dictionary of over 200 Latin words, combined</h4>
                                    <div class="author-info">
                                        <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=30&h=30&fit=crop" alt="Writer" class="author-avatar">
                                        <small>Writer Six • POLITICS EDITOR • 18 JAN 2024</small>
                                    </div>
                                </div>
                            </article>

                            <article class="post-item">
                                <img src="https://images.unsplash.com/photo-1551632811-561732d1e306?w=200&h=150&fit=crop" alt="Oficina">
                                <div class="post-content">
                                    <h4>Reading is not only informed by what's going on with us at that moment</h4>
                                    <div class="author-info">
                                        <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=30&h=30&fit=crop" alt="Writer" class="author-avatar">
                                        <small>Writer Six • POLITICS EDITOR • 18 JAN 2024</small>
                                    </div>
                                </div>
                            </article>

                            <article class="post-item">
                                <img src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?w=200&h=150&fit=crop" alt="Hombre pensativo">
                                <div class="post-content">
                                    <h4>What you see and what you're experiencing as you read these</h4>
                                    <div class="author-info">
                                        <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=30&h=30&fit=crop" alt="Writer" class="author-avatar">
                                        <small>Writer Six • POLITICS EDITOR • 18 JAN 2024</small>
                                    </div>
                                </div>
                            </article>
                        </div>

                        <div class="pagination">
                            <a href="#">PREV</a>
                            <a href="#" class="active">1</a>
                            <a href="#">2</a>
                            <a href="#">3</a>
                            <a href="#">4</a>
                            <a href="#">NEXT</a>
                        </div>
                    </section>
                </main>

                <aside class="sidebar">
                    <section class="popular-articles">
                        <h3>• POPULAR ARTICLES</h3>
                        <div class="popular-item">
                            <span style="font-size: 24px; font-weight: bold; color: #ccc;">1.</span>
                            <img src="https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?w=100&h=80&fit=crop" alt="Ciudad">
                            <div class="popular-content">
                                <h5>Ut enim ad minima veniam, quis nostrum</h5>
                                <small style="color: #666;">5 FEB 2024 • NO NEWS</small>
                            </div>
                        </div>

                        <div class="popular-item">
                            <span style="font-size: 24px; font-weight: bold; color: #ccc;">2.</span>
                            <img src="https://images.unsplash.com/photo-1517245386807-bb43f82c33c4?w=100&h=80&fit=crop" alt="Oficina">
                            <div class="popular-content">
                                <h5>Cum soluta nobis conseque turis</h5>
                                <small style="color: #666;">5 FEB 2024 • BUSINESS</small>
                            </div>
                        </div>

                        <div class="popular-item">
                            <span style="font-size: 24px; font-weight: bold; color: #ccc;">3.</span>
                            <img src="https://images.unsplash.com/photo-1494790108755-2616c64c29b8?w=100&h=80&fit=crop" alt="Mujer">
                            <div class="popular-content">
                                <h5>Faliquet lorem mollius dae augue</h5>
                                <small style="color: #666;">5 FEB 2024 • LIFESTYLE</small>
                            </div>
                        </div>

                        <div class="popular-item">
                            <span style="font-size: 24px; font-weight: bold; color: #ccc;">4.</span>
                            <img src="https://images.unsplash.com/photo-1551632811-561732d1e306?w=100&h=80&fit=crop" alt="Negocios">
                            <div class="popular-content">
                                <h5>Quam mauris lorem eget all euismod</h5>
                                <small style="color: #666;">5 FEB 2024 • BUSINESS</small>
                            </div>
                        </div>

                        <div class="popular-item">
                            <span style="font-size: 24px; font-weight: bold; color: #ccc;">5.</span>
                            <img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=100&h=80&fit=crop" alt="Paisaje">
                            <div class="popular-content">
                                <h5>Nec elit lorem phus sensus gravida</h5>
                                <small style="color: #666;">5 FEB 2024 • TRAVEL</small>
                            </div>
                        </div>
                    </section>

                    <section class="search-box">
                        <h3>• SEARCH</h3>
                        <input type="text" placeholder="Buscar...">
                        <button>SEARCH</button>
                    </section>

                    <section class="trending-section">
                        <h3>• TRENDING</h3>
                        <div class="trending-item">
                            <img src="https://images.unsplash.com/photo-1540039155733-5bb30b53aa14?w=300&h=200&fit=crop" alt="Concierto">
                            <div style="position: relative;">
                                <span style="position: absolute; top: -30px; right: 10px; background: #333; color: white; padding: 5px; font-size: 12px;">Best Blog</span>
                                <h5>Nos agnas is lorem agissum etui lues et purpors ar desiror et dilius</h5>
                            </div>
                        </div>

                        <div class="trending-item">
                            <img src="https://images.unsplash.com/photo-1494790108755-2616c64c29b8?w=300&h=200&fit=crop" alt="Mujer elegante">
                            <h5>Magna aliqua ut enim ad minim veniam</h5>
                            <small>10 JAN 2024</small>
                        </div>

                        <div class="trending-item">
                            <img src="https://images.unsplash.com/photo-1517245386807-bb43f82c33c4?w=300&h=200&fit=crop" alt="Reunión">
                            <h5>Magna aliqua ut enim ad minim veniam</h5>
                            <small>10 JAN 2024</small>
                        </div>

                        <div class="trending-item">
                            <img src="https://images.unsplash.com/photo-1494790108755-2616c64c29b8?w=300&h=200&fit=crop" alt="Retrato">
                            <h5>Magna aliqua ut enim ad minim veniam</h5>
                            <small>10 JAN 2024</small>
                        </div>
                    </section>

                    <section class="tags-section">
                        <h3>• TAGS CLOUD</h3>
                        <a href="#" class="tag">Business</a>
                        <a href="#" class="tag">Technology</a>
                        <a href="#" class="tag">Sport</a>
                        <a href="#" class="tag">Art</a>
                        <a href="#" class="tag">Lifestyle</a>
                        <a href="#" class="tag">Three</a>
                        <a href="#" class="tag">Photography</a>
                        <a href="#" class="tag">Lifestyle</a>
                        <a href="#" class="tag">Art</a>
                        <a href="#" class="tag">Education</a>
                        <a href="#" class="tag">Social</a>
                        <a href="#" class="tag">Three</a>
                    </section>
                </aside>
            </div>
        </div>

        <!-- NEWS PAGE -->
        <div id="news-page" style="display: none;">
            <div class="container">
                <main class="main-content">
                    <h1 style="text-align: center; margin: 40px 0; font-size: 36px;">NOTICIAS</h1>
                    <div class="post-list">
                        <article class="post-item">
                            <img src="https://images.unsplash.com/photo-1504711434969-e33886168f5c?w=200&h=150&fit=crop" alt="Noticias">
                            <div class="post-content">
                                <h4>Últimas noticias del mundo empresarial</h4>
                                <p>Las empresas tecnológicas siguen liderando el mercado...</p>
                                <small>2 FEB 2024 • BUSINESS</small>
                            </div>
                        </article>
                        
                        <article class="post-item">
                            <img src="https://images.unsplash.com/photo-1585829365295-ab7cd400c167?w=200&h=150&fit=crop" alt="Política">
                            <div class="post-content">
                                <h4>Nuevos desarrollos en política internacional</h4>
                                <p>Los líderes mundiales se reúnen para discutir temas globales...</p>
                                <small>1 FEB 2024 • POLITICS</small>
                            </div>
                        </article>
                        
                        <article class="post-item">
                            <img src="https://images.unsplash.com/photo-1581092786450-7ef25586ac07?w=200&h=150&fit=crop" alt="Ciencia">
                            <div class="post-content">
                                <h4>Avances científicos revolucionarios</h4>
                                <p>Nuevos descubrimientos prometen cambiar nuestra comprensión...</p>
                                <small>31 JAN 2024 • SCIENCE</small>
                            </div>
                        </article>
                    </div>
                </main>
                <aside class="sidebar">
                    <h3>Noticias Destacadas</h3>
                    <div class="popular-item">
                        <img src="https://images.unsplash.com/photo-1504711434969-e33886168f5c?w=100&h=80&fit=crop" alt="Destacada">
                        <div class="popular-content">
                            <h5>Noticia más leída del día</h5>
                            <small>HOY • TRENDING</small>
                        </div>
                    </div>
                </aside>
            </div>
        </div>

        <!-- ECONOMY PAGE -->
        <div id="economy-page" style="display: none;">
            <div class="container">
                <main class="main-content">
                    <h1 style="text-align: center; margin: 40px 0; font-size: 36px;">ECONOMÍA</h1>
                    <div class="post-list">
                        <article class="post-item">
                            <img src="https://images.unsplash.com/photo-1611974789855-9c2a0a7236a3?w=200&h=150&fit=crop" alt="Finanzas">
                            <div class="post-content">
                                <h4>Análisis del mercado financiero actual</h4>
                                <p>Los mercados muestran tendencias positivas este trimestre...</p>
                                <small>3 FEB 2024 • FINANCE</small>
                            </div>
                        </article>
                        
                        <article class="post-item">
                            <img src="https://images.unsplash.com/photo-1590283603385-17ffb3a7f29f?w=200&h=150&fit=crop" alt="Criptomonedas">
                            <div class="post-content">
                                <h4>El futuro de las criptomonedas</h4>
                                <p>Bitcoin y otras monedas digitales siguen ganando adopción...</p>
                                <small>2 FEB 2024 • CRYPTO</small>
                            </div>
                        </article>
                    </div>
                </main>
                <aside class="sidebar">
                    <h3>Datos Económicos</h3>
                    <div class="popular-item">
                        <div class="popular-content">
                            <h5>Inflación: 3.2%</h5>
                            <h5>Desempleo: 4.1%</h5>
                            <h5>PIB: +2.8%</h5>
                        </div>
                    </div>
                </aside>
            </div>
        </div>

        <!-- ENTERTAINMENT PAGE -->
        <div id="entertainment-page" style="display: none;">
            <div class="container">
                <main class="main-content">
                    <h1 style="text-align: center; margin: 40px 0; font-size: 36px;">ENTRETENIMIENTO</h1>
                    <div class="post-list">
                        <article class="post-item">
                            <img src="https://images.unsplash.com/photo-1489599112
