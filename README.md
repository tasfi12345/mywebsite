<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Palestine - Land of Heritage and Culture</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #006633;
            --secondary: #cc0000;
            --accent: #000000;
            --background: #ffffff;
            --foreground: #0a0a0a;
            --muted: #f5f5f5;
            --muted-foreground: #737373;
            --border: #e5e5e5;
            --input: #ffffff;
            --card: #ffffff;
            --card-foreground: #0a0a0a;
            --popover: #ffffff;
            --popover-foreground: #0a0a0a;
            --destructive: #ef4444;
            --destructive-foreground: #f9fafb;
            --ring: #006633;
            --radius: 0.5rem;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', sans-serif;
            line-height: 1.6;
            color: var(--foreground);
            background-color: var(--background);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1rem;
        }

        /* Navigation */
        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid var(--border);
            z-index: 1000;
            padding: 1rem 0;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--foreground);
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(135deg, var(--primary) 0%, #004d26 100%);
            color: white;
            text-align: center;
            padding-top: 80px;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
            line-height: 1.2;
        }

        .hero-content p {
            font-size: 1.25rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .btn {
            display: inline-block;
            padding: 0.75rem 2rem;
            background: var(--secondary);
            color: white;
            text-decoration: none;
            border-radius: var(--radius);
            font-weight: 500;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
        }

        .btn:hover {
            background: #990000;
            transform: translateY(-2px);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid white;
        }

        .btn-outline:hover {
            background: white;
            color: var(--primary);
        }

        /* Section Styles */
        .section {
            padding: 5rem 0;
        }

        .section-header {
            text-align: center;
            margin-bottom: 3rem;
        }

        .section-header h2 {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
            color: var(--primary);
        }

        .section-header p {
            font-size: 1.125rem;
            color: var(--muted-foreground);
            max-width: 600px;
            margin: 0 auto;
        }

        /* Introduction */
        .intro {
            background: var(--muted);
        }

        .intro-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .intro-card {
            background: white;
            padding: 2rem;
            border-radius: var(--radius);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .intro-card .icon {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .intro-card h3 {
            font-size: 1.25rem;
            font-weight: 600;
            margin-bottom: 1rem;
        }

        /* Culture Section */
        .culture-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .culture-card {
            background: white;
            border-radius: var(--radius);
            overflow: hidden;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .culture-card:hover {
            transform: translateY(-5px);
        }

        .culture-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .culture-card-content {
            padding: 1.5rem;
        }

        .culture-card h3 {
            font-size: 1.25rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        .culture-card p {
            color: var(--muted-foreground);
            margin-bottom: 1rem;
        }

        .tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .tag {
            background: var(--primary);
            color: white;
            padding: 0.25rem 0.75rem;
            border-radius: 1rem;
            font-size: 0.875rem;
        }

        /* Timeline */
        .timeline {
            max-width: 800px;
            margin: 0 auto;
            position: relative;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 30px;
            top: 0;
            bottom: 0;
            width: 2px;
            background: var(--primary);
        }

        .timeline-item {
            position: relative;
            margin-bottom: 2rem;
            padding-left: 80px;
        }

        .timeline-icon {
            position: absolute;
            left: 0;
            top: 0;
            width: 60px;
            height: 60px;
            background: var(--primary);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            font-weight: 600;
        }

        .timeline-content h3 {
            font-size: 1.25rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        /* Cities Grid */
        .cities-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .city-card {
            background: white;
            border-radius: var(--radius);
            overflow: hidden;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .city-card:hover {
            transform: translateY(-5px);
        }

        .city-card img {
            width: 100%;
            height: 250px;
            object-fit: cover;
        }

        .city-card-content {
            padding: 1.5rem;
        }

        /* Gallery */
        .gallery {
            background: var(--muted);
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1rem;
            margin-top: 3rem;
        }

        .gallery-item {
            border-radius: var(--radius);
            overflow: hidden;
            cursor: pointer;
            transition: transform 0.3s ease;
        }

        .gallery-item:hover {
            transform: scale(1.05);
        }

        .gallery-item img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        /* Resources */
        .resources-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .resource-category h3 {
            font-size: 1.5rem;
            font-weight: 600;
            margin-bottom: 1rem;
            color: var(--primary);
        }

        .resource-list {
            list-style: none;
        }

        .resource-list li {
            margin-bottom: 0.5rem;
        }

        .resource-list a {
            color: var(--foreground);
            text-decoration: none;
            padding: 0.5rem 0;
            display: block;
            border-bottom: 1px solid var(--border);
            transition: color 0.3s ease;
        }

        .resource-list a:hover {
            color: var(--primary);
        }

        /* Contact Form */
        .contact {
            background: var(--muted);
        }

        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            margin-top: 3rem;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 0.75rem;
            border: 1px solid var(--border);
            border-radius: var(--radius);
            font-family: inherit;
        }

        .form-group textarea {
            min-height: 120px;
            resize: vertical;
        }

        .checkbox-group {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            margin-bottom: 1.5rem;
        }

        /* Footer */
        .footer {
            background: var(--primary);
            color: white;
            padding: 3rem 0 1rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-section h3 {
            margin-bottom: 1rem;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section a {
            color: rgba(255, 255, 255, 0.8);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-section a:hover {
            color: white;
        }

        .newsletter-form {
            display: flex;
            gap: 0.5rem;
            margin-top: 1rem;
        }

        .newsletter-form input {
            flex: 1;
            padding: 0.75rem;
            border: 1px solid rgba(255, 255, 255, 0.3);
            border-radius: var(--radius);
            background: rgba(255, 255, 255, 0.1);
            color: white;
        }

        .newsletter-form input::placeholder {
            color: rgba(255, 255, 255, 0.7);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.2);
            color: rgba(255, 255, 255, 0.8);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .mobile-menu-btn {
                display: block;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }

            .section-header h2 {
                font-size: 2rem;
            }

            .contact-grid {
                grid-template-columns: 1fr;
            }

            .timeline::before {
                left: 15px;
            }

            .timeline-item {
                padding-left: 60px;
            }

            .timeline-icon {
                width: 40px;
                height: 40px;
                font-size: 1rem;
            }
        }

        .hidden {
            display: none;
        }

        .alert {
            padding: 1rem;
            border-radius: var(--radius);
            margin-bottom: 1rem;
        }

        .alert-success {
            background: #dcfce7;
            color: #166534;
            border: 1px solid #bbf7d0;
        }

        .alert-error {
            background: #fef2f2;
            color: #dc2626;
            border: 1px solid #fecaca;
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar">
        <div class="container">
            <div class="nav-container">
                <a href="#home" class="logo">🇵🇸 Palestine</a>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#culture">Culture</a></li>
                    <li><a href="#history">History</a></li>
                    <li><a href="#cities">Cities</a></li>
                    <li><a href="#gallery">Gallery</a></li>
                    <li><a href="#resources">Resources</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                <button class="mobile-menu-btn">☰</button>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Welcome to Palestine</h1>
                <p>Discover the rich heritage, vibrant culture, and timeless beauty of the Holy Land</p>
                <div style="display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap; margin-top: 2rem;">
                    <a href="#about" class="btn">Explore Our Heritage</a>
                    <a href="#culture" class="btn btn-outline">Discover Culture</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Introduction Section -->
    <section id="about" class="section intro">
        <div class="container">
            <div class="section-header">
                <h2>About Palestine</h2>
                <p>Palestine is a land of profound historical significance, rich cultural heritage, and natural beauty. From ancient cities to modern communities, discover what makes this land unique.</p>
            </div>
            <div class="intro-grid">
                <div class="intro-card">
                    <div class="icon">🏛</div>
                    <h3>Rich History</h3>
                    <p>Explore thousands of years of history, from ancient civilizations to modern times, with archaeological sites and historical landmarks.</p>
                </div>
                <div class="intro-card">
                    <div class="icon">🎨</div>
                    <h3>Vibrant Culture</h3>
                    <p>Experience the diverse cultural traditions, arts, music, and crafts that have been preserved and celebrated for generations.</p>
                </div>
                <div class="intro-card">
                    <div class="icon">🌍</div>
                    <h3>Global Heritage</h3>
                    <p>Discover a land that has been a crossroads of civilizations, connecting different cultures and traditions throughout history.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Culture Section -->
    <section id="culture" class="section">
        <div class="container">
            <div class="section-header">
                <h2>Palestinian Culture</h2>
                <p>Immerse yourself in the rich cultural tapestry of Palestine, from traditional arts to contemporary expressions.</p>
            </div>
            <div class="culture-grid">
                <div class="culture-card">
                    <img src="https://images.unsplash.com/photo-1578662996442-48f60103fc96?w=400&h=200&fit=crop" alt="Traditional Palestinian Embroidery">
                    <div class="culture-card-content">
                        <h3>Traditional Embroidery</h3>
                        <p>The intricate art of Palestinian tatreez embroidery, passed down through generations, tells stories through colorful threads and patterns.</p>
                        <div class="tags">
                            <span class="tag">Handicrafts</span>
                            <span class="tag">Traditional</span>
                            <span class="tag">Art</span>
                        </div>
                    </div>
                </div>
                <div class="culture-card">
                    <img src="https://images.unsplash.com/photo-1493770348161-369560ae357d?w=400&h=200&fit=crop" alt="Palestinian Music">
                    <div class="culture-card-content">
                        <h3>Music & Dance</h3>
                        <p>From the rhythmic beats of the dabke dance to the melodious sounds of the oud, Palestinian music celebrates life and heritage.</p>
                        <div class="tags">
                            <span class="tag">Music</span>
                            <span class="tag">Dance</span>
                            <span class="tag">Celebration</span>
                        </div>
                    </div>
                </div>
                <div class="culture-card">
                    <img src="https://images.unsplash.com/photo-1565299624946-b28f40a0ca4b?w=400&h=200&fit=crop" alt="Palestinian Cuisine">
                    <div class="culture-card-content">
                        <h3>Culinary Heritage</h3>
                        <p>Savor the flavors of Palestinian cuisine, featuring dishes like maqluba, knafeh, and fresh olive oil from ancient groves.</p>
                        <div class="tags">
                            <span class="tag">Food</span>
                            <span class="tag">Heritage</span>
                            <span class="tag">Tradition</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- History Timeline -->
    <section id="history" class="section">
        <div class="container">
            <div class="section-header">
                <h2>Historical Timeline</h2>
                <p>Journey through the key moments that have shaped Palestinian history and identity.</p>
            </div>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-icon">3000</div>
                    <div class="timeline-content">
                        <h3>Ancient Civilizations</h3>
                        <p>The land witnesses the rise of Canaanite cities and becomes a crossroads of ancient civilizations, with evidence of continuous habitation for millennia.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-icon">638</div>
                    <div class="timeline-content">
                        <h3>Islamic Conquest</h3>
                        <p>The region becomes part of the Islamic world, with Jerusalem becoming the third holiest city in Islam, fostering a rich Islamic cultural heritage.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-icon">1187</div>
                    <div class="timeline-content">
                        <h3>Saladin's Victory</h3>
                        <p>Saladin recaptures Jerusalem, marking a significant moment in medieval history and the protection of religious sites for all faiths.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-icon">1516</div>
                    <div class="timeline-content">
                        <h3>Ottoman Period</h3>
                        <p>Palestine becomes part of the Ottoman Empire, experiencing centuries of relative stability and cultural development.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-icon">1948</div>
                    <div class="timeline-content">
                        <h3>Modern Era</h3>
                        <p>The establishment of Israel leads to displacement and the beginning of the ongoing Palestinian struggle for statehood and recognition.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Cities Section -->
    <section id="cities" class="section">
        <div class="container">
            <div class="section-header">
                <h2>Palestinian Cities</h2>
                <p>Explore the historic cities and towns that form the heart of Palestinian heritage and identity.</p>
            </div>
            <div class="cities-grid">
                <div class="city-card">
                    <img src="https://images.unsplash.com/photo-1544967919-6d4a2e3da4c1?w=400&h=250&fit=crop" alt="Jerusalem">
                    <div class="city-card-content">
                        <h3>Jerusalem (Al-Quds)</h3>
                        <p>The eternal city, home to holy sites of three major religions. The Dome of the Rock and Al-Aqsa Mosque stand as symbols of Palestinian heritage.</p>
                        <div class="tags">
                            <span class="tag">Holy City</span>
                            <span class="tag">Historic</span>
                            <span class="tag">Cultural</span>
                        </div>
                    </div>
                </div>
                <div class="city-card">
                    <img src="https://images.unsplash.com/photo-1570077188670-e3a8d69ac5ff?w=400&h=250&fit=crop" alt="Bethlehem">
                    <div class="city-card-content">
                        <h3>Bethlehem</h3>
                        <p>The birthplace of Jesus Christ, featuring the Church of the Nativity and a rich Christian Palestinian heritage that spans centuries.</p>
                        <div class="tags">
                            <span class="tag">Biblical</span>
                            <span class="tag">Christian</span>
                            <span class="tag">Pilgrimage</span>
                        </div>
                    </div>
                </div>
                <div class="city-card">
                    <img src="https://images.unsplash.com/photo-1539037116277-4db20889f2d4?w=400&h=250&fit=crop" alt="Hebron">
                    <div class="city-card-content">
                        <h3>Hebron (Al-Khalil)</h3>
                        <p>One of the oldest continuously inhabited cities in the world, home to the Ibrahimi Mosque and known for its traditional crafts and markets.</p>
                        <div class="tags">
                            <span class="tag">Ancient</span>
                            <span class="tag">Crafts</span>
                            <span class="tag">Heritage</span>
                        </div>
                    </div>
                </div>
                <div class="city-card">
                    <img src="https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?w=400&h=250&fit=crop" alt="Nablus">
                    <div class="city-card-content">
                        <h3>Nablus</h3>
                        <p>Famous for its ancient soap factories, knafeh dessert, and the historic old city with its traditional architecture and bustling souqs.</p>
                        <div class="tags">
                            <span class="tag">Commerce</span>
                            <span class="tag">Traditional</span>
                            <span class="tag">Cuisine</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section id="gallery" class="section gallery">
        <div class="container">
            <div class="section-header">
                <h2>Photo Gallery</h2>
                <p>Visual journey through the landscapes, architecture, and daily life of Palestine.</p>
            </div>
            <div class="gallery-grid">
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1544967919-6d4a2e3da4c1?w=300&h=200&fit=crop" alt="Dome of the Rock">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1578662996442-48f60103fc96?w=300&h=200&fit=crop" alt="Traditional Crafts">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1565299624946-b28f40a0ca4b?w=300&h=200&fit=crop" alt="Palestinian Food">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1570077188670-e3a8d69ac5ff?w=300&h=200&fit=crop" alt="Ancient Architecture">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1493770348161-369560ae357d?w=300&h=200&fit=crop" alt="Traditional Music">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1539037116277-4db20889f2d4?w=300&h=200&fit=crop" alt="Market Scene">
                </div>
            </div>
        </div>
    </section>

    <!-- Resources Section -->
    <section id="resources" class="section">
        <div class="container">
            <div class="section-header">
                <h2>Educational Resources</h2>
                <p>Learn more about Palestinian history, culture, and current affairs through these educational resources.</p>
            </div>
            <div class="resources-grid">
                <div class="resource-category">
                    <h3>📚 Educational</h3>
                    <ul class="resource-list">
                        <li><a href="#" onclick="return false;">Palestine Institute for Public Diplomacy</a></li>
                        <li><a href="#" onclick="return false;">Palestinian Academic Society</a></li>
                        <li><a href="#" onclick="return false;">Institute for Palestine Studies</a></li>
                        <li><a href="#" onclick="return false;">Palestinian Heritage Foundation</a></li>
                    </ul>
                </div>
                <div class="resource-category">
                    <h3>🎥 Media & Arts</h3>
                    <ul class="resource-list">
                        <li><a href="#" onclick="return false;">Palestinian Cinema Archive</a></li>
                        <li><a href="#" onclick="return false;">Traditional Music Collection</a></li>
                        <li><a href="#" onclick="return false;">Contemporary Palestinian Art</a></li>
                        <li><a href="#" onclick="return false;">Documentary Films</a></li>
                    </ul>
                </div>
                <div class="resource-category">
                    <h3>🏛 Cultural</h3>
                    <ul class="resource-list">
                        <li><a href="#" onclick="return false;">Palestinian Museum</a></li>
                        <li><a href="#" onclick="return false;">Cultural Heritage Sites</a></li>
                        <li><a href="#" onclick="return false;">Traditional Crafts Directory</a></li>
                        <li><a href="#" onclick="return false;">Language Learning Resources</a></li>
                    </ul>
                </div>
                <div class="resource-category">
                    <h3>📰 News & Current Affairs</h3>
                    <ul class="resource-list">
                        <li><a href="#" onclick="return false;">Palestine News Network</a></li>
                        <li><a href="#" onclick="return false;">Middle East Monitor</a></li>
                        <li><a href="#" onclick="return false;">Al Jazeera Palestine</a></li>
                        <li><a href="#" onclick="return false;">Human Rights Organizations</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section contact">
        <div class="container">
            <div class="section-header">
                <h2>Get in Touch</h2>
                <p>Have questions or want to learn more? We'd love to hear from you.</p>
            </div>
            <div class="contact-grid">
                <div>
                    <h3>Send us a Message</h3>
                    <div id="contact-alert" class="hidden"></div>
                    <form id="contact-form">
                        <div class="form-group">
                            <label for="name">Full Name</label>
                            <input type="text" id="name" name="name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email Address</label>
                            <input type="email" id="email" name="email" required>
                        </div>
                        <div class="form-group">
                            <label for="subject">Subject</label>
                            <input type="text" id="subject" name="subject" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" name="message" required></textarea>
                        </div>
                        <div class="checkbox-group">
                            <input type="checkbox" id="newsletter" name="newsletter">
                            <label for="newsletter">Subscribe to our newsletter for updates</label>
                        </div>
                        <button type="submit" class="btn">Send Message</button>
                    </form>
                </div>
                <div>
                    <h3>Contact Information</h3>
                    <div style="margin-top: 1.5rem;">
                        <p><strong>📧 Email:</strong> info@palestine-heritage.org</p>
                        <p><strong>📞 Phone:</strong> +1 (555) 123-4567</p>
                        <p><strong>📍 Address:</strong> 123 Heritage Lane, Cultural District</p>
                        <p><strong>🕒 Hours:</strong> Monday - Friday, 9:00 AM - 5:00 PM</p>
                    </div>
                    <div style="margin-top: 2rem;">
                        <h4>Follow Our Mission</h4>
                        <p>Stay connected with our efforts to preserve and share Palestinian heritage with the world.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>Palestine Heritage</h3>
                    <p>Preserving and sharing the rich cultural heritage of Palestine with the world.</p>
                </div>
                <div class="footer-section">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#about">About</a></li>
                        <li><a href="#culture">Culture</a></li>
                        <li><a href="#history">History</a></li>
                        <li><a href="#cities">Cities</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Resources</h3>
                    <ul>
                        <li><a href="#resources">Educational</a></li>
                        <li><a href="#gallery">Gallery</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Newsletter</h3>
                    <p>Subscribe to receive updates about Palestinian culture and heritage.</p>
                    <div id="newsletter-alert" class="hidden"></div>
                    <form id="newsletter-form" class="newsletter-form">
                        <input type="email" name="email" placeholder="Enter your email" required>
                        <button type="submit" class="btn">Subscribe</button>
                    </form>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2024 Palestine Heritage. All rights reserved. | Built with love for Palestinian culture and history.</p>
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                if (this.getAttribute('href') !== '#' && !this.hasAttribute('onclick')) {
                    e.preventDefault();
                    const target = document.querySelector(this.getAttribute('href'));
                    if (target) {
                        target.scrollIntoView({
                            behavior: 'smooth',
                            block: 'start'
                        });
                    }
                }
            });
        });

        // Mobile menu toggle
        const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
        const navLinks = document.querySelector('.nav-links');

        mobileMenuBtn.addEventListener('click', () => {
            navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
        });

        // Contact form submission
        document.getElementById('contact-form').addEventListener('submit', async (e) => {
            e.preventDefault();
            
            const formData = new FormData(e.target);
            const data = {
                name: formData.get('name'),
                email: formData.get('email'),
                subject: formData.get('subject'),
                message: formData.get('message'),
                newsletter: formData.get('newsletter') === 'on'
            };

            const alertDiv = document.getElementById('contact-alert');
            
            try {
                // Simulate form submission (replace with actual API call)
                await new Promise(resolve => setTimeout(resolve, 1000));
                
                alertDiv.className = 'alert alert-success';
                alertDiv.textContent = 'Thank you for your message! We\'ll get back to you soon.';
                alertDiv.classList.remove('hidden');
                
                e.target.reset();
            } catch (error) {
                alertDiv.className = 'alert alert-error';
                alertDiv.textContent = 'Sorry, there was an error sending your message. Please try again.';
                alertDiv.classList.remove('hidden');
            }
        });

        // Newsletter form submission
        document.getElementById('newsletter-form').addEventListener('submit', async (e) => {
            e.preventDefault();
            
            const formData = new FormData(e.target);
            const email = formData.get('email');

            const alertDiv = document.getElementById('newsletter-alert');
            
            try {
                // Simulate newsletter subscription (replace with actual API call)
                await new Promise(resolve => setTimeout(resolve, 1000));
                
                alertDiv.className = 'alert alert-success';
                alertDiv.textContent = 'Successfully subscribed to our newsletter!';
                alertDiv.classList.remove('hidden');
                
                e.target.reset();
            } catch (error) {
                alertDiv.className = 'alert alert-error';
                alertDiv.textContent = 'Sorry, there was an error with your subscription. Please try again.';
                alertDiv.classList.remove('hidden');
            }
        });

        // Gallery image click handlers
        document.querySelectorAll('.gallery-item img').forEach(img => {
            img.addEventListener('click', function() {
                // Simple lightbox effect
                const overlay = document.createElement('div');
                overlay.style.cssText = `
                    position: fixed;
                    top: 0;
                    left: 0;
                    width: 100%;
                    height: 100%;
                    background: rgba(0, 0, 0, 0.9);
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    z-index: 9999;
                    cursor: pointer;
                `;
                
                const imgClone = this.cloneNode();
                imgClone.style.maxWidth = '90%';
                imgClone.style.maxHeight = '90%';
                imgClone.style.objectFit = 'contain';
                
                overlay.appendChild(imgClone);
                document.body.appendChild(overlay);
                
                overlay.addEventListener('click', () => {
                    document.body.removeChild(overlay);
                });
            });
        });

        // Active navigation highlighting
        window.addEventListener('scroll', () => {
            const sections = document.querySelectorAll('section[id]');
            const navLinks = document.querySelectorAll('.nav-links a');
            
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop - 100;
                if (window.scrollY >= sectionTop) {
                    current = section.getAttribute('id');
                }
            });

            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href') === #${current}) {
                    link.classList.add('active');
                }
            });
        });
    </script>
</body>
</html># mywebsite
