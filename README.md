# ST
Hllo everyone 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NEXUS Gaming | Level Up Your World</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    
    <style>
        /* --- CSS VARIABLES & RESET --- */
        :root {
            --primary: #00d4ff; /* Neon Cyan */
            --secondary: #7000ff; /* Neon Purple */
            --accent: #ff0055; /* Neon Pink */
            --bg-dark: #0a0a12;
            --bg-card: #151520;
            --text-light: #ffffff;
            --text-gray: #a0a0a0;
            --gradient: linear-gradient(135deg, var(--secondary), var(--primary));
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Roboto', sans-serif;
            background-color: var(--bg-dark);
            color: var(--text-light);
            overflow-x: hidden;
        }

        h1, h2, h3, .logo {
            font-family: 'Orbitron', sans-serif;
            text-transform: uppercase;
        }

        a {
            text-decoration: none;
            color: var(--text-light);
            transition: 0.3s;
        }

        ul {
            list-style: none;
        }

        /* --- HEADER & NAV --- */
        header {
            background: rgba(10, 10, 18, 0.95);
            padding: 1rem 5%;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 900;
            background: var(--gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            letter-spacing: 2px;
        }

        nav ul {
            display: flex;
            gap: 2rem;
        }

        nav a:hover {
            color: var(--primary);
            text-shadow: 0 0 10px var(--primary);
        }

        .auth-buttons .btn {
            padding: 0.5rem 1.5rem;
            border-radius: 5px;
            font-weight: bold;
            cursor: pointer;
        }

        .btn-login {
            background: transparent;
            border: 1px solid var(--primary);
            color: var(--primary);
            margin-right: 10px;
        }

        .btn-signup {
            background: var(--primary);
            color: var(--bg-dark);
        }

        .btn-signup:hover {
            background: var(--secondary);
            color: white;
            box-shadow: 0 0 15px var(--secondary);
        }

        /* Mobile Menu Toggle */
        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* --- HERO SECTION --- */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(10,10,18,0.7), var(--bg-dark)), 
                        url('https://images.unsplash.com/photo-1542751371-adc38448a05e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 0 20px;
        }

        .hero-content h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            line-height: 1.1;
        }

        .hero-content h1 span {
            color: var(--primary);
        }

        .hero-content p {
            font-size: 1.2rem;
            color: var(--text-gray);
            margin-bottom: 2rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .cta-btn {
            padding: 1rem 2.5rem;
            background: var(--gradient);
            color: white;
            font-family: 'Orbitron', sans-serif;
            font-weight: bold;
            border: none;
            clip-path: polygon(10% 0, 100% 0, 100% 70%, 90% 100%, 0 100%, 0 30%);
            cursor: pointer;
            transition: 0.3s;
            font-size: 1.1rem;
        }

        .cta-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 0 20px rgba(0, 212, 255, 0.5);
        }

        /* --- FEATURED GAMES --- */
        .section {
            padding: 5rem 10%;
        }

        .section-title {
            font-size: 2.5rem;
            margin-bottom: 3rem;
            text-align: center;
        }

        .section-title span {
            border-bottom: 3px solid var(--accent);
        }

        .games-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .game-card {
            background: var(--bg-card);
            border-radius: 10px;
            overflow: hidden;
            transition: 0.3s;
            position: relative;
            border: 1px solid rgba(255,255,255,0.05);
        }

        .game-card:hover {
            transform: translateY(-10px);
            border-color: var(--primary);
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        }

        .game-image {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .game-info {
            padding: 1.5rem;
        }

        .game-tags {
            display: flex;
            gap: 10px;
            margin-bottom: 10px;
        }

        .tag {
            font-size: 0.8rem;
            padding: 2px 8px;
            background: rgba(255,255,255,0.1);
            border-radius: 3px;
            color: var(--primary);
        }

        .game-info h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }

        .rating {
            color: #ffd700;
            margin-bottom: 1rem;
            font-size: 0.9rem;
        }

        .download-btn {
            display: block;
            width: 100%;
            padding: 10px;
            background: rgba(255,255,255,0.05);
            text-align: center;
            border-radius: 5px;
            margin-top: 1rem;
        }

        .download-btn:hover {
            background: var(--primary);
            color: var(--bg-dark);
        }

        /* --- TOURNAMENT BANNER --- */
        .tournament {
            background: linear-gradient(rgba(112, 0, 255, 0.8), rgba(0, 212, 255, 0.8)), url('https://images.unsplash.com/photo-1511512578047-dfb367046420?ixlib=rb-1.2.1&auto=format&fit=crop&w=1951&q=80');
            background-size: cover;
            background-attachment: fixed;
            text-align: center;
            padding: 6rem 20px;
        }

        .tournament h2 {
            font-size: 3rem;
            margin-bottom: 1rem;
            text-shadow: 0 2px 10px rgba(0,0,0,0.5);
        }

        .tournament p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }

        /* --- FOOTER --- */
        footer {
            background: #050508;
            padding: 4rem 10% 1rem;
            border-top: 1px solid rgba(255,255,255,0.1);
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .footer-col h4 {
            color: var(--primary);
            margin-bottom: 1.5rem;
            font-size: 1.2rem;
        }

        .footer-col ul li {
            margin-bottom: 0.8rem;
        }

        .footer-col ul li a {
            color: var(--text-gray);
        }

        .footer-col ul li a:hover {
            color: white;
        }

        .social-links a {
            font-size: 1.5rem;
            margin-right: 1rem;
            color: var(--text-gray);
        }

        .social-links a:hover {
            color: var(--primary);
        }

        .copyright {
            text-align: center;
            color: var(--text-gray);
            padding-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.05);
        }

        /* --- RESPONSIVE --- */
        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
            }

            nav ul {
                position: absolute;
                top: 70px;
                left: 0;
                width: 100%;
                background: var(--bg-card);
                flex-direction: column;
                padding: 2rem;
                text-align: center;
                display: none;
            }

            nav ul.active {
                display: flex;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }
            
            .auth-buttons {
                display: none; /* Hide buttons on mobile for simplicity */
            }
        }
    </style>
</head>
<body>

    <!-- HEADER -->
    <header>
        <a href="#" class="logo">NEXUS</a>
        <div class="menu-toggle" id="mobile-menu">
            <i class="fas fa-bars"></i>
        </div>
        <nav>
            <ul id="nav-list">
                <li><a href="#home">Home</a></li>
                <li><a href="#games">Games</a></li>
                <li><a href="#tournaments">Tournaments</a></li>
                <li><a href="#community">Community</a></li>
                <li><a href="#news">News</a></li>
            </ul>
        </nav>
        <div class="auth-buttons">
            <a href="#" class="btn btn-login">Login</a>
            <a href="#" class="btn btn-signup">Join Now</a>
        </div>
    </header>

    <!-- HERO SECTION -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Enter The <br><span>Next Dimension</span></h1>
            <p>Discover the world's most immersive games, join global tournaments, and connect with millions of gamers.</p>
            <button class="cta-btn">EXPLORE GAMES</button>
        </div>
    </section>

    <!-- FEATURED GAMES -->
    <section class="section" id="games">
        <h2 class="section-title"><span>Trending</span> Games</h2>
        <div class="games-grid">
            <!-- Game Card 1 -->
            <div class="game-card">
                <img src="https://images.unsplash.com/photo-1552820728-8b83bb6b773f?ixlib=rb-1.2.1&auto=format&fit=crop&w=900&q=60" alt="Cyber Game" class="game-image">
                <div class="game-info">
                    <div class="game-tags">
                        <span class="tag">RPG</span>
                        <span class="tag">Open World</span>
                    </div>
                    <h3>Cyber Odyssey 2077</h3>
                    <div class="rating">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star-half-alt"></i>
                    </div>
                    <p>Explore a dystopian future in this open-world RPG masterpiece.</p>
                    <a href="#" class="download-btn">Play Now <i class="fas fa-gamepad"></i></a>
                </div>
            </div>

            <!-- Game Card 2 -->
            <div class="game-card">
                <img src="https://images.unsplash.com/photo-1538481199705-c710c4e965fc?ixlib=rb-1.2.1&auto=format&fit=crop&w=900&q=60" alt="Space Game" class="game-image">
                <div class="game-info">
                    <div class="game-tags">
                        <span class="tag">Sci-Fi</span>
                        <span class="tag">Strategy</span>
                    </div>
                    <h3>Galactic Warfare</h3>
                    <div class="rating">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="far fa-star"></i>
                    </div>
                    <p>Command fleets and conquer the galaxy in intense battles.</p>
                    <a href="#" class="download-btn">Play Now <i class="fas fa-gamepad"></i></a>
                </div>
            </div>

            <!-- Game Card 3 -->
            <div class="game-card">
                <img src="https://images.unsplash.com/photo-1509198397868-475647b2a1e5?ixlib=rb-1.2.1&auto=format&fit=crop&w=900&q=60" alt="Fantasy Game" class="game-image">
                <div class="game-info">
                    <div class="game-tags">
                        <span class="tag">Fantasy</span>
                        <span class="tag">MMO</span>
                    </div>
                    <h3>Realms of Eternity</h3>
                    <div class="rating">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                    <p>Forge your destiny in a world of magic and mythical beasts.</p>
                    <a href="#" class="download-btn">Play Now <i class="fas fa-gamepad"></i></a>
                </div>
            </div>
        </div>
    </section>

    <!-- TOURNAMENT SECTION -->
    <section class="tournament" id="tournaments">
        <h2>Global Championship 2024</h2>
        <p>$2,000,000 Prize Pool • 48 Teams • Live Global Stream</p>
        <button class="cta-btn">WATCH LIVE</button>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="footer-content">
            <div class="footer-col">
                <a href="#" class="logo">NEXUS</a>
                <p style="margin-top: 1rem; color: var(--text-gray);">
                    The ultimate destination for competitive gaming, reviews, and community.
                </p>
            </div>
            <div class="footer-col">
                <h4>Explore</h4>
                <ul>
                    <li><a href="#">Top Games</a></li>
                    <li><a href="#">Live Streams</a></li>
                    <li><a href="#">Forums</a></li>
                    <li><a href="#">Hardware</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h4>Support</h4>
                <ul>
                    <li><a href="#">Help Center</a></li>
                    <li><a href="#">Terms of Service</a></li>
                    <li><a href="#">Privacy Policy</a></li>
                    <li><a href="#">Contact Us</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h4>Follow Us</h4>
                <div class="social-links">
                    <a href="#"><i class="fab fa-discord"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-twitch"></i></a>
                    <a href="#"><i class="fab fa-youtube"></i></a>
                </div>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2024 NEXUS Gaming. All rights reserved.</p>
        </div>
    </footer>

    <!-- JAVASCRIPT -->
    <script>
        // Mobile Menu Toggle
        const menuToggle = document.getElementById('mobile-menu');
        const navList = document.getElementById('nav-list');

        menuToggle.addEventListener('click', () => {
            navList.classList.toggle('active');
        });

        // Smooth Scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                navList.classList.remove('active'); // Close mobile menu on click
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Simple Animation on Scroll (Reveal effect)
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = 1;
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        });

        // Apply initial styles for animation
        document.querySelectorAll('.game-card').forEach((el) => {
            el.style.opacity = 0;
            el.style.transform = 'translateY(50px)';
            el.style.transition = 'all 0.6s ease-out';
            observer.observe(el);
        });
    </script>
</body>
</html>
