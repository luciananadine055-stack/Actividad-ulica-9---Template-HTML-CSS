# Actividad-ulica-9---Template-HTML-CSS
alumna: Luciana Nadine Rojas
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HELLO WORLD</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Georgia', serif;
            line-height: 1.6;
            color: #333;
            background-color: #fff;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        .top-bar {
            background-color: #f8f8f8;
            padding: 10px 0;
            font-size: 12px;
            border-bottom: 1px solid #e0e0e0;
        }

        .top-bar .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .top-bar-left {
            display: flex;
            align-items: center;
        }

        .top-bar-left span {
            margin-right: 15px;
        }

        .top-bar-right {
            display: flex;
            align-items: center;
        }

        .social-icons {
            display: flex;
            gap: 10px;
            margin-right: 15px;
        }

        .search-box {
            padding: 5px 10px;
            border: 1px solid #ccc;
            font-size: 11px;
        }

        /* Logo and Navigation */
        .header {
            text-align: center;
            padding: 30px 0;
        }

        .logo {
            font-size: 36px;
            font-weight: bold;
            letter-spacing: 3px;
            margin-bottom: 10px;
        }

        .tagline {
            font-size: 12px;
            color: #666;
            margin-bottom: 30px;
        }

        .navigation {
            border-top: 2px solid #000;
            border-bottom: 2px solid #000;
            padding: 15px 0;
        }

        .nav-menu {
            display: flex;
            justify-content: center;
            list-style: none;
            gap: 40px;
        }

        .nav-menu li a {
            text-decoration: none;
            color: #333;
            font-size: 14px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Main Content Layout */
        .main-content {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 30px;
            padding: 30px 0;
        }

        /* News Grid */
        .news-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            margin-bottom: 30px;
        }

        .news-card {
            display: flex;
            gap: 15px;
            padding-bottom: 15px;
            border-bottom: 1px solid #e0e0e0;
        }

        .news-image {
            width: 80px;
            height: 60px;
            background-color: #f0f0f0;
            flex-shrink: 0;
            background-size: cover;
            background-position: center;
        }

        .news-content h3 {
            font-size: 14px;
            margin-bottom: 5px;
            line-height: 1.4;
        }

        .news-meta {
            font-size: 11px;
            color: #999;
        }

        /* Featured Article */
        .featured-article {
            margin-bottom: 40px;
        }

        .featured-image {
            width: 100%;
            height: 300px;
            background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), url('https://images.unsplash.com/photo-1504711434969-e33886168f5c?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&q=80');
            background-size: cover;
            background-position: center;
            margin-bottom: 20px;
            position: relative;
        }

        .featured-title {
            font-size: 28px;
            font-weight: bold;
            margin-bottom: 15px;
            line-height: 1.3;
        }

        .author-info {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }

        .author-avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: url('https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-4.0.3&auto=format&fit=crop&w=100&q=80');
            background-size: cover;
            background-position: center;
            margin-right: 10px;
        }

        .author-name {
            font-size: 12px;
            font-weight: bold;
        }

        .article-excerpt {
            font-size: 14px;
            color: #666;
            line-height: 1.6;
        }

        /* Recent Posts */
        .recent-posts {
            margin-top: 40px;
        }

        .section-title {
            text-align: center;
            font-size: 20px;
            font-weight: bold;
            margin-bottom: 30px;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .recent-posts-list {
            display: grid;
            gap: 20px;
        }

        .recent-post {
            display: flex;
            gap: 15px;
            padding-bottom: 15px;
            border-bottom: 1px solid #e0e0e0;
        }

        .recent-post-image {
            width: 100px;
            height: 70px;
            background-color: #f0f0f0;
            flex-shrink: 0;
            background-size: cover;
            background-position: center;
        }

        .recent-post-content h4 {
            font-size: 16px;
            margin-bottom: 8px;
            line-height: 1.4;
        }

        .recent-post-meta {
            font-size: 11px;
            color: #999;
            display: flex;
            gap: 15px;
        }

        /* Sidebar */
        .sidebar {
            padding-left: 20px;
        }

        .sidebar-section {
            margin-bottom: 40px;
        }

        .sidebar-title {
            font-size: 16px;
            font-weight: bold;
            margin-bottom: 20px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .popular-articles {
            list-style: none;
        }

        .popular-articles li {
            display: flex;
            gap: 10px;
            margin-bottom: 15px;
            font-size: 14px;
        }

        .popular-articles .number {
            font-weight: bold;
            color: #666;
        }

        .search-section input {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            margin-bottom: 10px;
        }

        .search-btn {
            width: 100%;
            padding: 10px;
            background-color: #333;
            color: white;
            border: none;
            cursor: pointer;
            text-transform: uppercase;
        }

        .trending-image {
            width: 100%;
            height: 150px;
            background-color: #f0f0f0;
            margin-bottom: 10px;
            background-size: cover;
            background-position: center;
        }

        .trending-title {
            font-size: 14px;
            font-weight: bold;
            margin-bottom: 5px;
        }

        .trending-excerpt {
            font-size: 12px;
            color: #666;
            margin-bottom: 5px;
        }

        .trending-meta {
            font-size: 11px;
            color: #999;
        }

        /* Footer Navigation */
        .footer-nav {
            background-color: #f8f8f8;
            padding: 30px 0;
            margin-top: 50px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 30px;
        }

        .footer-section h4 {
            font-size: 14px;
            font-weight: bold;
            margin-bottom: 15px;
            text-transform: uppercase;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section ul li {
            margin-bottom: 8px;
        }

        .footer-section ul li a {
            text-decoration: none;
            color: #666;
            font-size: 12px;
        }

        .footer-post {
            display: flex;
            gap: 10px;
            margin-bottom: 15px;
        }

        .footer-post-image {
            width: 50px;
            height: 35px;
            background-color: #ddd;
            flex-shrink: 0;
            background-size: cover;
            background-position: center;
        }

        .footer-post-content {
            font-size: 11px;
        }

        .footer-post-title {
            font-weight: bold;
            margin-bottom: 3px;
        }

        /* Bottom Footer */
        .bottom-footer {
            text-align: center;
            padding: 20px 0;
            border-top: 1px solid #e0e0e0;
        }

        .bottom-footer .logo {
            font-size: 24px;
            margin-bottom: 10px;
        }

        .copyright {
            font-size: 11px;
            color: #999;
        }

        /* Pagination */
        .pagination {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin: 30px 0;
        }

        .pagination a {
            padding: 8px 12px;
            text-decoration: none;
            color: #333;
            border: 1px solid #ddd;
        }

        .pagination a.active {
            background-color: #333;
            color: white;
        }

        /* Tag Cloud */
        .tag-cloud {
            display: flex;
            flex-wrap: wrap;
            gap: 5px;
        }

        .tag {
            background-color: #f0f0f0;
            padding: 5px 10px;
            font-size: 11px;
            text-decoration: none;
            color: #666;
        }
    </style>
</head>
<body>
    <!-- Top Bar -->
    <div class="top-bar">
        <div class="container">
            <div class="top-bar-left">
                <span>☰ MORE</span>
                <span>📅 Friday 5 January 2023</span>
            </div>
            <div class="top-bar-right">
                <div class="social-icons">
                    <span>📧</span>
                    <span>💬</span>
                    <span>📱</span>
                </div>
                <input type="text" placeholder="SEARCH" class="search-box">
            </div>
        </div>
    </div>

    <!-- Header -->
    <header class="header">
        <div class="container">
            <h1 class="logo">HELLO WORLD</h1>
            <div class="tagline">≈ NEWSPAPER / MAGAZINE / PUBLISHER ≈</div>
            
            <!-- Navigation -->
            <nav class="navigation">
                <ul class="nav-menu">
                    <li><a href="#">→ HOME</a></li>
                    <li><a href="#">→ LAYOUT</a></li>
                    <li><a href="#">NEWS</a></li>
                    <li><a href="#">ECONOMY</a></li>
                    <li><a href="#">→ ENTERTAINMENT</a></li>
                    <li><a href="#">JOBS</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Main Content -->
    <div class="container">
        <div class="main-content">
            <!-- Left Column -->
            <main>
                <!-- Top News Grid -->
                <div class="news-grid">
                    <article class="news-card">
                        <div class="news-image" style="background-image: url('https://images.unsplash.com/photo-1486312338219-ce68e2c6b387?ixlib=rb-4.0.3&auto=format&fit=crop&w=200&q=80');"></div>
                        <div class="news-content">
                            <h3>Lorem ipsum dui sollic studin</h3>
                            <div class="news-meta">8 JAN 2023 · NO VIEWS</div>
                        </div>
                    </article>
                    
                    <article class="news-card">
                        <div class="news-image" style="background-image: url('https://images.unsplash.com/photo-1551434678-e076c223a692?ixlib=rb-4.0.3&auto=format&fit=crop&w=200&q=80');"></div>
                        <div class="news-content">
                            <h3>Ut enim ad minim veniat</h3>
                            <div class="news-meta">8 JAN 2023 · NO VIEWS</div>
                        </div>
                    </article>
                    
                    <article class="news-card">
                        <div class="news-image" style="background-image: url('https://images.unsplash.com/photo-1444653614773-995cb1ef9efa?ixlib=rb-4.0.3&auto=format&fit=crop&w=200&q=80');"></div>
                        <div class="news-content">
                            <h3>Quis nostrum vel enim lorem laboret</h3>
                            <div class="news-meta">8 JAN 2023 · NO VIEWS</div>
                        </div>
                    </article>
                    
                    <article class="news-card">
                        <div class="news-image" style="background-image: url('https://images.unsplash.com/photo-1557804506-669a67965ba0?ixlib=rb-4.0.3&auto=format&fit=crop&w=200&q=80');"></div>
                        <div class="news-content">
                            <h3>At vero eos et oboro dignos et harum</h3>
                            <div class="news-meta">8 JAN 2023 · NO VIEWS</div>
                        </div>
                    </article>
                </div>

                <!-- Featured Article -->
                <article class="featured-article">
                    <div class="featured-image"></div>
                    <h2 class="featured-title">Lorem ipsum dui sollic itudin praesent ut mollis primis eros torquent fames</h2>
                    <div class="author-info">
                        <div class="author-avatar"></div>
                        <div class="author-name">Steven Job<br><small>8 JAN 2023</small></div>
                    </div>
                    <p class="article-excerpt">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
                </article>

                <!-- Recent Posts -->
                <section class="recent-posts">
                    <h2 class="section-title">≈≈≈ RECENT POSTS ≈≈≈</h2>
                    <div class="recent-posts-list">
                        <article class="recent-post">
                            <div class="recent-post-image" style="background-image: url('https://images.unsplash.com/photo-1495020689067-958852a7765e?ixlib=rb-4.0.3&auto=format&fit=crop&w=200&q=80');"></div>
                            <div class="recent-post-content">
                                <h4>Magna aliqua ut enim ad minim veniam</h4>
                                <div class="recent-post-meta">
                                    <span>👤 Steven Job</span>
                                    <span>📅 POLITICS, STORY</span>
                                    <span>📅 18 JAN 2023</span>
                                </div>
                            </div>
                        </article>

                        <article class="recent-post">
                            <div class="recent-post-image" style="background-image: url('https://images.unsplash.com/photo-1585282263861-f55e341878f8?ixlib=rb-4.0.3&auto=format&fit=crop&w=200&q=80');"></div>
                            <div class="recent-post-content">
                                <h4>Laborant shects containing Lorem Ipsum passages, and more recently</h4>
                                <div class="recent-post-meta">
                                    <span>👤 Steven Job</span>
                                    <span>📅 POLITICS, STORY</span>
                                    <span>📅 18 JAN 2023</span>
                                </div>
                            </div>
                        </article>

                        <article class="recent-post">
                            <div class="recent-post-image" style="background-image: url('https://images.unsplash.com/photo-1524178232363-1fb2b075b655?ixlib=rb-4.0.3&auto=format&fit=crop&w=200&q=80');"></div>
                            <div class="recent-post-content">
                                <h4>There are many variations of passages of Lorem Ipsum available, but the majority have suffered</h4>
                                <div class="recent-post-meta">
                                    <span>👤 Steven Job</span>
                                    <span>📅 POLITICS, STORY</span>
                                    <span>📅 18 JAN 2023</span>
                                </div>
                            </div>
                        </article>

                        <article class="recent-post">
                            <div class="recent-post-image" style="background-image: url('https://images.unsplash.com/photo-1481627834876-b7833e8f5570?ixlib=rb-4.0.3&auto=format&fit=crop&w=200&q=80');"></div>
                            <div class="recent-post-content">
                                <h4>It uses a dictionary of over 200 Latin words, combined</h4>
                                <div class="recent-post-meta">
                                    <span>👤 Steven Job</span>
                                    <span>📅 POLITICS, STORY</span>
                                    <span>📅 18 JAN 2023</span>
                                </div>
                            </div>
                        </article>

                        <article class="recent-post">
                            <div class="recent-post-image" style="background-image: url('https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&auto=format&fit=crop&w=200&q=80');"></div>
                            <div class="recent-post-content">
                                <h4>Reading is not only informed by what's going on with us at that moment</h4>
                                <div class="recent-post-meta">
                                    <span>👤 Steven Job</span>
                                    <span>📅 POLITICS, STORY</span>
                                    <span>📅 18 JAN 2023</span>
                                </div>
                            </div>
                        </article>

                        <article class="recent-post">
                            <div class="recent-post-image" style="background-image: url('https://images.unsplash.com/photo-1519389950473-47ba0277781c?ixlib=rb-4.0.3&auto=format&fit=crop&w=200&q=80');"></div>
                            <div class="recent-post-content">
                                <h4>What you see and what you're experiencing as you read these</h4>
                                <div class="recent-post-meta">
                                    <span>👤 Steven Job</span>
                                    <span>📅 POLITICS, STORY</span>
                                    <span>📅 18 JAN 2023</span>
                                </div>
                            </div>
                        </article>
                    </div>
                </section>

                <!-- Pagination -->
                <div class="pagination">
                    <a href="#">‹‹‹</a>
                    <a href="#" class="active">1</a>
                    <a href="#">2</a>
                    <a href="#">3</a>
                    <a href="#">4</a>
                    <a href="#">NEXT ›</a>
                </div>
            </main>

            <!-- Sidebar -->
            <aside class="sidebar">
                <!-- Popular Articles -->
                <section class="sidebar-section">
                    <h3 class="sidebar-title">● POPULAR ARTICLES</h3>
                    <ol class="popular-articles">
                        <li><span class="number">1.</span> Ut enim ad minim veniam, quis nostrum</li>
                        <li><span class="number">2.</span> Cum sociis natique penibus tempi cursus</li>
                        <li><span class="number">3.</span> Nullam lorem risitas tetur augue</li>
                        <li><span class="number">4.</span> Quam mauris lorem orci sit rutmonis</li>
                        <li><span class="number">5.</span> Nec elit libor platea societas gravida</li>
                    </ol>
                </section>

                <!-- Search -->
                <section class="sidebar-section">
                    <h3 class="sidebar-title">● SEARCH</h3>
                    <div class="search-section">
                        <input type="text" placeholder="Search...">
                        <button class="search-btn">SEARCH</button>
                    </div>
                </section>

                <!-- Trending -->
                <section class="sidebar-section">
                    <h3 class="sidebar-title">● TRENDING</h3>
                    <article>
                        <div class="trending-image" style="background-image: url('https://images.unsplash.com/photo-1540575467063-178a50c2df87?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80');"></div>
                        <h4 class="trending-title">Best Blog</h4>
                        <p class="trending-excerpt">Nos gente di thierry superior who loves or pursues or desires to obtain</p>
                        <div class="trending-meta">18 JAN 2023</div>
                    </article>
                </section>

                <!-- More Articles -->
                <section class="sidebar-section">
                    <div style="margin-bottom: 15px;">
                        <div class="trending-image" style="height: 80px; background-image: url('https://images.unsplash.com/photo-1552664730-d307ca884978?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80');"></div>
                        <div class="trending-title" style="font-size: 12px;">Magna aliqua ut enim ad minim veniam</div>
                        <div class="trending-meta">18 JAN 2023</div>
                    </div>
                    <div style="margin-bottom: 15px;">
                        <div class="trending-image" style="height: 80px; background-image: url('https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80');"></div>
                        <div class="trending-title" style="font-size: 12px;">Magna aliqua ut enim ad minim veniam</div>
                        <div class="trending-meta">18 JAN 2023</div>
                    </div>
                    <div style="margin-bottom: 15px;">
                        <div class="trending-image" style="height: 80px; background-image: url('https://images.unsplash.com/photo-1551836022-deb4988cc6c0?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80');"></div>
                        <div class="trending-title" style="font-size: 12px;">Magna aliqua ut enim ad minim veniam</div>
                        <div class="trending-meta">18 JAN 2023</div>
                    </div>
                </section>

                <!-- Tags -->
                <section class="sidebar-section">
                    <h3 class="sidebar-title">● TAGS CLOUD</h3>
                    <div class="tag-cloud">
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
                    </div>
                </section>
            </aside>
        </div>
    </div>

    <!-- Footer -->
    <footer class="footer-nav">
        <div class="container">
            <div class="footer-content">
                <!-- Most Comments -->
                <div class="footer-section">
                    <h4>● MOST COMMENTS</h4>
                    <ol>
                        <li><a href="#">Efficitur adipiscing mollis orci semper class</a></li>
                        <li><a href="#">Anceritisol pul cuncibus risus ut amet rutilot</a></li>
                        <li><a href="#">Quam placerat et culpa sollicitis molore libero</a></li>
                        <li><a href="#">Amet for hoc proch hello and beautiful pharetra cursus</a></li>
                    </ol>
                </div>

                <!-- Latest -->
                <div class="footer-section">
                    <h4>● LATEST</h4>
                    <div class="footer-post">
                        <div class="footer-post-image" style="background-image: url('https://images.unsplash.com/photo-1526628953301-3e589a6a8b74?ixlib=rb-4.0.3&auto=format&fit=crop&w=100&q=80');"></div>
                        <div class="footer-post-content">
                            <div class="footer-post-title">Magna aliqua ut enim ad minim veniam</div>
                            <div class="footer-post-meta">18 JAN 2023</div>
                        </div>
                    </div>
                    <div class="footer-post">
                        <div class="footer-post-image" style="background-image: url('https://images.unsplash.com/photo-1518709268805-4e9042af2176?ixlib=rb-4.0.3&auto=format&fit=crop&w=100&q=80');"></div>
                        <div class="footer-post-content">
                            <div class="footer-post-title">Magna aliqua ut enim ad minim veniam</div>
                            <div class="footer-post-meta">18 JAN 2023</div>
                        </div>
                    </div>
                    <div class="footer-post">
                        <div class="footer-post-image" style="background-image: url('https://images.unsplash.com/photo-1553877522-43269d4ea984?ixlib=rb-4.0.3&auto=format&fit=crop&w=100&q=80');"></div>
                        <div class="footer-post-content">
                            <div class="footer-post-title">Magna aliqua ut enim ad minim veniam</div>
                            <div class="footer-post-meta">18 JAN 2023</div>
                        </div>
                    </div>
                </div>

                <!-- Categories -->
                <div class="footer-section">
                    <h4>● CATEGORIES</h4>
                    <ul>
                        <li><a href="#">Business</a></li>
                        <li><a href="#">Environment</a></li>
                        <li><a href="#">Life style</a></li>
                        <li><a href="#">Technology</a></li>
                    </ul>
                    <ul style="margin-top: 20px;">
                        <li><a href="#">Entertainment</a></li>
                        <li><a href="#">Health</a></li>
                        <li><a href="#">Politics</a></li>
                        <li><a href="#">World</a></li>
                    </ul>
                </div>

                <!-- Instagram -->
                <div class="footer-section">
                    <h4>● INSTAGRAM</h4>
                    <div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 5px;">
                        <div style="width: 50px; height: 50px; background: url('https://images.unsplash.com/photo-1611224923853-80b023f02d71?ixlib=rb-4.0.3&auto=format&fit=crop&w=100&q=80'); background-size: cover; background-position: center;"></div>
                        <div style="width: 50px; height: 50px; background: url('https://images.unsplash.com/photo-1557318041-1ce374d55ebf?ixlib=rb-4.0.3&auto
