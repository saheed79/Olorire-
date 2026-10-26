<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ascitizen | Nigeria's Leading News Chronicle</title>
    <style>
        :root {
            --primary-color: #0b2e13; /* Deep Nigerian Green Theme */
            --accent-color: #d9534f;
            --light-bg: #f8f9fa;
            --border-color: #dee2e6;
            --text-main: #212529;
            --text-muted: #6c757d;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            color: var(--text-main);
            background-color: #fff;
            line-height: 1.6;
        }

        /* Header & Navigation */
        header {
            border-bottom: 1px solid var(--border-color);
            background: #fff;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .top-bar {
            max-width: 1200px;
            margin: 0 auto;
            padding: 8px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 0.85rem;
            color: var(--text-muted);
            border-bottom: 1px solid var(--light-bg);
        }

        .logo-area {
            text-align: center;
            padding: 24px 0;
            background-color: #fff;
            border-bottom: 1px solid var(--border-color);
        }

        .logo-area h1 {
            font-size: 3rem;
            font-family: Georgia, serif;
            letter-spacing: -1px;
            text-transform: uppercase;
            color: var(--primary-color);
        }

        .logo-area p {
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            color: var(--text-muted);
            margin-top: 4px;
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: center;
            gap: 25px;
            padding: 12px 20px;
            overflow-x: auto;
        }

        nav a {
            text-decoration: none;
            color: var(--primary-color);
            font-weight: 700;
            font-size: 0.95rem;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            transition: color 0.2s;
            white-space: nowrap;
        }

        nav a:hover, nav a.active {
            color: var(--accent-color);
        }

        /* Main Container Layout */
        .container {
            max-width: 1200px;
            margin: 30px auto;
            padding: 0 20px;
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 40px;
        }

        @media (max-width: 768px) {
            .container {
                grid-template-columns: 1fr;
            }
        }

        /* Hero / Featured Article */
        .featured-article {
            margin-bottom: 40px;
            border-bottom: 1px solid var(--border-color);
            padding-bottom: 30px;
        }

        .featured-img {
            width: 100%;
            height: 380px;
            background-color: #ddd;
            background-size: cover;
            background-position: center;
            margin-bottom: 20px;
        }

        .tag {
            background-color: var(--accent-color);
            color: #fff;
            padding: 4px 8px;
            font-size: 0.75rem;
            text-transform: uppercase;
            font-weight: bold;
            display: inline-block;
            margin-bottom: 10px;
        }

        .featured-article h2 {
            font-family: Georgia, serif;
            font-size: 2.1rem;
            line-height: 1.25;
            margin-bottom: 15px;
        }

        .featured-article p {
            color: var(--text-muted);
            font-size: 1.05rem;
            margin-bottom: 15px;
        }

        .meta {
            font-size: 0.85rem;
            color: var(--text-muted);
        }

        /* News Grid Section */
        .news-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        @media (max-width: 480px) {
            .news-grid {
                grid-template-columns: 1fr;
            }
        }

        .news-card {
            border-bottom: 1px solid var(--border-color);
            padding-bottom: 20px;
        }

        .news-card-img {
            width: 100%;
            height: 180px;
            background-color: #ddd;
            background-size: cover;
            background-position: center;
            margin-bottom: 12px;
        }

        .news-card h3 {
            font-family: Georgia, serif;
            font-size: 1.2rem;
            margin-bottom: 8px;
            line-height: 1.3;
        }

        .news-card p {
            font-size: 0.9rem;
            color: var(--text-muted);
            margin-bottom: 8px;
        }

        /* Sidebar Section */
        aside {
            border-left: 1px solid var(--border-color);
            padding-left: 30px;
        }

        @media (max-width: 768px) {
            aside {
                border-left: none;
                padding-left: 0;
                border-top: 1px solid var(--border-color);
                padding-top: 30px;
            }
        }

        .sidebar-section h3 {
            font-size: 1.2rem;
            text-transform: uppercase;
            border-bottom: 2px solid var(--primary-color);
            padding-bottom: 8px;
            margin-bottom: 20px;
            letter-spacing: 0.5px;
        }

        .trending-item {
            display: flex;
            gap: 15px;
            margin-bottom: 20px;
            align-items: flex-start;
        }

        .trending-number {
            font-size: 2rem;
            font-family: Georgia, serif;
            font-weight: bold;
            color: var(--border-color);
            line-height: 1;
        }

        .trending-content h4 {
            font-size: 0.95rem;
            font-family: Georgia, serif;
            margin-bottom: 5px;
            line-height: 1.3;
        }

        /* Footer */
        footer {
            background-color: var(--primary-color);
            color: #fff;
            padding: 50px 20px 20px;
            margin-top: 50px;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 30px;
            margin-bottom: 40px;
        }

        .footer-col h4 {
            font-size: 1rem;
            text-transform: uppercase;
            margin-bottom: 15px;
            letter-spacing: 1px;
            color: #e9ecef;
        }

        .footer-col ul {
            list-style: none;
        }

        .footer-col ul li {
            margin-bottom: 10px;
        }

        .footer-col ul li a {
            color: #adb5bd;
            text-decoration: none;
            font-size: 0.9rem;
            transition: color 0.2s;
        }

        .footer-col ul li a:hover {
            color: #fff;
        }

        .footer-bottom {
            max-width: 1200px;
            margin: 0 auto;
            border-top: 1px solid rgba(255,255,255,0.1);
            padding-top: 20px;
            text-align: center;
            font-size: 0.8rem;
            color: #adb5bd;
        }
    </style>
</head>
<body>

    <!-- Header & Navigation -->
    <header>
        <div class="top-bar">
            <span>Monday, October 26, 2026 | Abuja, Nigeria</span>
            <span>National Desk</span>
        </div>
        <div class="logo-area">
            <h1>Ascitizen</h1>
            <p>Truth, Clarity, and National Perspective</p>
        </div>
        <nav>
            <a href="#" class="active">Home</a>
            <a href="#">Politics</a>
            <a href="#">Metro</a>
            <a href="#">Business & Economy</a>
            <a href="#">Technology</a>
            <a href="#">Opinion</a>
        </nav>
    </header>

    <!-- Main Grid Content -->
    <div class="container">
        <!-- Main News Column -->
        <main>
            <!-- Featured Lead Story (Nigeria Trends) -->
            <article class="featured-article">
                <div class="tag">Breaking News</div>
                <div class="featured-img" style="background-image: url('https://images.unsplash.com/photo-1590012314607-cda9d9b699ae?auto=format&fit=crop&w=1200&q=80');"></div>
                <h2>SERAP Files Lawsuit Against Federal Government Over ₦78.8 Billion Cash Transfer Queries</h2>
                <p>The Socio-Economic Rights and Accountability Project has launched legal proceedings seeking total transparency and comprehensive tracking regarding reported public cash transfer expenditures across states.</p>
                <div class="meta">By Ascitizen Political Desk &bull; 35 mins ago</div>
            </article>

            <!-- Secondary Grid Stories -->
            <div class="news-grid">
                <article class="news-card">
                    <div class="news-card-img" style="background-image: url('https://images.unsplash.com/photo-1541872703-74c5e44368f9?auto=format&fit=crop&w=600&q=80');"></div>
                    <span class="tag" style="background-color: var(--primary-color);">Infrastructure</span>
                    <h3>Housing Ministry Accelerates Nation-Wide Renewed Hope Urban Projects</h3>
                    <p>Federal officials inspect rapid construction phases aimed at delivering sustainable mass housing units nationwide.</p>
                    <div class="meta">2 hours ago</div>
                </article>

                <article class="news-card">
                    <div class="news-card-img" style="background-image: url('https://images.unsplash.com/photo-1576091160399-112ba8d25d1d?auto=format&fit=crop&w=600&q=80');"></div>
                    <span class="tag" style="background-color: var(--primary-color);">Health Watch</span>
                    <h3>NCDC Steps Up Surveillance and Contact Monitoring Nationwide</h3>
                    <p>Health authorities assure the public of active containment protocols, safety frameworks, and medical support packages.</p>
                    <div class="meta">4 hours ago</div>
                </article>
            </div>
        </main>

        <!-- Sidebar Column -->
        <aside>
            <div class="sidebar-section">
                <h3>Trending Headlines</h3>
                
                <div class="trending-item">
                    <div class="trending-number">01</div>
                    <div class="trending-content">
                        <h4>2027 Political Realignments: Coalitions Form Campaign Strategy Committees</h4>
                        <div class="meta">Politics</div>
                    </div>
                </div>

                <div class="trending-item">
                    <div class="trending-number">02</div>
                    <div class="trending-content">
                        <h4>Tech Hubs in Lagos and Abuja Record Surge in Seed Investments</h4>
                        <div class="meta">Business</div>
                    </div>
                </div>

                <div class="trending-item">
                    <div class="trending-number">03</div>
                    <div class="trending-content">
                        <h4>Power Sector Generation Records Upward Stability Across Grids</h4>
                        <div class="meta">Economy</div>
                    </div>
                </div>

                <div class="trending-item">
                    <div class="trending-number">04</div>
                    <div class="trending-content">
                        <h4>Super Eagles Gear Up for Crucial International Qualifiers</h4>
                        <div class="meta">Sports</div>
                    </div>
                </div>
            </div>
        </aside>
    </div>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-col">
                <h4>Ascitizen</h4>
                <p style="font-size: 0.85rem; color: #adb5bd; line-height: 1.5;">Committed to delivering reliable, verified, and insightful news coverage across Nigeria and the wider African continent.</p>
            </div>
            <div class="footer-col">
                <h4>Categories</h4>
                <ul>
                    <li><a href="#">Nigerian Politics</a></li>
                    <li><a href="#">Business & Markets</a></li>
                    <li><a href="#">Metro & Society</a></li>
                    <li><a href="#">Tech & Innovation</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h4>Editorial</h4>
                <ul>
                    <li><a href="#">About Ascitizen</a></li>
                    <li><a href="#">Our Code of Ethics</a></li>
                    <li><a href="#">Submit a Scoop</a></li>
                    <li><a href="#">Careers</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h4>Policies</h4>
                <ul>
                    <li><a href="#">Privacy Policy</a></li>
                    <li><a href="#">Terms of Service</a></li>
                    <li><a href="#">Contact Us</a></li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            &copy; 2026 Ascitizen Publishing Ltd. All rights reserved.
        </div>
    </footer>

</body>
</html>
