<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blitzblank Kassel | Professionelle Gebäudereinigung</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #0056b3;
            --secondary: #e6f2ff;
            --accent: #ff7b00;
            --dark: #1a365d;
            --light: #f8f9fa;
        }
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.7;
            color: #333;
            background-color: #fff;
            overflow-x: hidden;
        }
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Header mit Logo */
        header {
            background-color: rgba(255, 255, 255, 0.97);
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.08);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(10px);
            transition: all 0.4s ease;
        }
        .header-scrolled {
            padding: 5px 0;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
        }
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
            transition: all 0.4s ease;
        }
        .logo-container {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        .logo {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, var(--primary) 0%, var(--dark) 100%);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            box-shadow: 0 4px 10px rgba(0, 84, 179, 0.3);
        }
        .logo::before {
            content: '';
            position: absolute;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, transparent 40%, rgba(255,255,255,0.3) 50%, transparent 60%);
            animation: shine 3s infinite linear;
        }
        .logo-inner {
            width: 30px;
            height: 30px;
            background-color: white;
            border-radius: 4px;
            position: relative;
            transform: rotate(45deg);
        }
        .logo-inner::after {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 18px;
            height: 18px;
            background: var(--accent);
            border-radius: 2px;
        }
        .logo-text {
            font-size: 1.8em;
            font-weight: 700;
            color: var(--dark);
        }
        .logo-text span {
            color: var(--primary);
        }
        nav ul {
            list-style: none;
            display: flex;
        }
        nav li {
            margin-left: 30px;
        }
        nav a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 600;
            font-size: 1.05em;
            transition: color 0.3s ease;
            position: relative;
        }
        nav a:hover {
            color: var(--primary);
        }
        nav a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background-color: var(--accent);
            transition: width 0.3s ease;
        }
        nav a:hover::after {
            width: 100%;
        }

        /* Hero Section - JETZT WICHTIG: DIESE SECTION WAR WEG! */
        .hero {
            background: linear-gradient(135deg, rgba(0, 84, 179, 0.85) 0%, rgba(0, 40, 85, 0.9) 100%), url('https://images.unsplash.com/photo-1581578731548-c64695cc6952?ixlib=rb-4.0.3') no-repeat center center/cover;
            height: 100vh;
            display: flex;
            align-items: center;
            text-align: left;
            color: white;
            margin-top: 0;
            position: relative;
        }
        .hero-content {
            max-width: 800px;
        }
        .hero-content h1 {
            font-size: 3.5em;
            margin-bottom: 20px;
            line-height: 1.2;
            font-weight: 700;
            opacity: 0;
            transform: translateY(30px);
            animation: fadeInUp 1s ease forwards 0.5s;
        }
        .hero-content p {
            font-size: 1.4em;
            margin-bottom: 35px;
            max-width: 600px;
            font-weight: 300;
            opacity: 0;
            transform: translateY(30px);
            animation: fadeInUp 1s ease forwards 0.8s;
        }
        .btn {
            display: inline-block;
            background: var(--accent);
            color: white;
            padding: 15px 40px;
            border: none;
            border-radius: 50px;
            text-decoration: none;
            font-size: 1.1em;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(255, 123, 0, 0.3);
            opacity: 0;
            transform: translateY(30px);
            animation: fadeInUp 1s ease forwards 1.1s;
        }
        .btn:hover {
            background: #e66d00;
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(255, 123, 0, 0.4);
        }

        /* Abschnitte */
        section {
            padding: 100px 0;
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease;
        }
        .visible {
            opacity: 1;
            transform: translateY(0);
        }
        h2 {
            text-align: center;
            margin-bottom: 20px;
            color: var(--dark);
            font-size: 2.5em;
            font-weight: 700;
            position: relative;
            padding-bottom: 15px;
        }
        h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: var(--accent);
        }
        .section-subtitle {
            text-align: center;
            font-size: 1.2em;
            color: #666;
            max-width: 700px;
            margin: 0 auto 60px auto;
        }

        /* Leistungen */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
        }
        .service-card {
            background: white;
            padding: 40px 30px;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
            transition: all 0.4s ease;
            border-top: 5px solid var(--primary);
            position: relative;
            overflow: hidden;
        }
        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 0;
            background: var(--primary);
            opacity: 0.05;
            transition: height 0.4s ease;
        }
        .service-card:hover::before {
            height: 100%;
        }
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
        .service-icon {
            font-size: 2.5em;
            margin-bottom: 20px;
            color: var(--primary);
            transition: all 0.4s ease;
        }
        .service-card:hover .service-icon {
            transform: scale(1.1);
            color: var(--accent);
        }
        .service-card h3 {
            color: var(--dark);
            margin-bottom: 15px;
            font-size: 1.5em;
        }
        .service-card p {
            color: #555;
            margin-bottom: 20px;
        }
        .service-price {
            font-weight: 700;
            color: var(--accent);
            font-size: 1.1em;
        }

        /* Über Uns */
        .about {
            background: var(--secondary);
        }
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        .about-text {
            flex: 2;
        }
        .about-text p {
            margin-bottom: 20px;
            font-size: 1.1em;
        }
        .about-image {
            flex: 1;
            background: #ccc;
            height: 400px;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #777;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            position: relative;
            overflow: hidden;
        }
        .about-image::after {
            content: 'Teamfoto Platzhalter';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            background: #e0e0e0;
        }
        .usp-list {
            list-style: none;
            margin-top: 30px;
        }
        .usp-list li {
            margin-bottom: 15px;
            padding-left: 30px;
            position: relative;
        }
        .usp-list li::before {
            content: '✓';
            position: absolute;
            left: 0;
            color: var(--accent);
            font-weight: bold;
            font-size: 1.2em;
        }

        /* Galerie */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
        }
        .gallery-item {
            background: #eee;
            height: 250px;
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #999;
            font-weight: 600;
            transition: all 0.5s ease;
            overflow: hidden;
            position: relative;
        }
        .gallery-item::after {
            content: 'Bild Platzhalter';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            background: #e0e0e0;
            transition: all 0.5s ease;
        }
        .gallery-item:hover::after {
            transform: scale(1.05);
            filter: brightness(0.9);
        }

        /* Kontakt */
        #contact {
            background: var(--dark);
            color: white;
        }
        #contact h2 {
            color: white;
        }
        #contact h2::after {
            background: var(--accent);
        }
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 50px;
        }
        .contact-info h3 {
            margin-bottom: 20px;
            font-size: 1.5em;
        }
        .contact-detail {
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            transition: all 0.3s ease;
            padding: 10px;
            border-radius: 5px;
        }
        .contact-detail:hover {
            background: rgba(255, 255, 255, 0.05);
            transform: translateX(5px);
        }
        .contact-detail i {
            margin-right: 15px;
            font-size: 1.2em;
            color: var(--accent);
            width: 20px;
            text-align: center;
        }
        .cta-box {
            background: rgba(255,255,255,0.1);
            padding: 30px;
            border-radius: 10px;
            text-align: center;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.1);
            transition: all 0.4s ease;
        }
        .cta-box:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }
        .cta-box h3 {
            margin-bottom: 20px;
        }

        /* Footer */
        footer {
            background: #111;
            color: #aaa;
            text-align: center;
            padding: 30px 0;
            font-size: 0.9em;
        }

        /* Animationen */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes shine {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }

        /* Scroll-Animation */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease;
        }
        
        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }

        /* Responsive Anpassungen */
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                padding: 10px 0;
            }
            .logo-container {
                margin-bottom: 10px;
            }
            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }
            nav li {
                margin: 5px 10px;
            }
            .hero-content h1 {
                font-size: 2.5em;
            }
            .about-content {
                flex-direction: column;
            }
            .hero-content p {
                font-size: 1.2em;
            }
        }
    </style>
</head>
<body>
    <!-- Header mit Logo -->
    <header id="main-header">
        <div class="container header-container">
            <div class="logo-container">
                <div class="logo">
                    <div class="logo-inner"></div>
                </div>
                <div class="logo-text">Blitz<span>blank</span> Kassel</div>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Start</a></li>
                    <li><a href="#services">Leistungen</a></li>
                    <li><a href="#about">Warum Wir</a></li>
                    <li><a href="#gallery">Einblicke</a></li>
                    <li><a href="#contact">Kontakt</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section - DIESE SECTION FEHLTE! -->
    <section id="home" class="hero">
        <div class="container hero-content">
            <h1>Mehr als nur sauber.<br>Ein perfekter erster Eindruck.</h1>
            <p>Wir machen Ihre Praxis, Ihr Büro oder Ihre Baustelle nicht nur rein, sondern strahlend sauber. Denn Sauberkeit ist das Fundament für Vertrauen und Erfolg.</p>
            <a href="#contact" class="btn">Kostenlose Erstreinigung anfragen</a>
        </div>
    </section>

    <!-- Leistungen -->
    <section id="services" class="fade-in">
        <div class="container">
            <h2>Unsere Spezialgebiete</h2>
            <p class="section-subtitle">Maßgeschneiderte Reinigungslösungen für anspruchsvolle Gewerbekunden</p>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-clinic-medical"></i></div>
                    <h3>Praxen-Reinigung</h3>
                    <p>Höchste Hygienestandards für den sensibelsten Bereich. Ihre Patienten und Mitarbeiter verdienen das Beste.</p>
                    <div class="service-price">Ab 0,90 €/m² pro Reinigung</div>
                </div>
                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-building"></i></div>
                    <h3>Büroreinigung</h3>
                    <p>Steigern Sie die Produktivität und das Wohlbefinden in Ihrem Team mit einer einladenden Arbeitsumgebung.</p>
                    <div class="service-price">Individuelle Angebote</div>
                </div>
                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-tools"></i></div>
                    <h3>Bauendreinigung</h3>
                    <p>Von der Baustelle zum bezugsfertigen Traum. Wir entfernen jeden letzten Krümel und Fleck.</p>
                    <div class="service-price">Ab 3,50 €/m² (pauschal)</div>
                </div>
                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-window-restore"></i></div>
                    <h3>Fensterreinigung</h3>
                    <p>Streifenfreie Sicht für mehr Licht und eine positive Außenwirkung. Innen & Außen, auch in Höhen.</p>
                    <div class="service-price">Ab 4,50 € pro Scheibe</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Über Uns / Warum Wir -->
    <section id="about" class="about fade-in">
        <div class="container">
            <h2>Warum Kunden uns vertrauen</h2>
            <p class="section-subtitle">Weil wir anders sind. Konzentriert auf Qualität, nicht auf Masse.</p>
            <div class="about-content">
                <div class="about-text">
                    <p>Wir sind <strong>Blitzblank Kassel</strong> – ein eingespieltes Quartett mit Leidenschaft für makellose Ergebnisse. Während andere hetzen, nehmen wir uns die Zeit, die es braucht, um jedes Detail perfekt zu machen.</p>
                    <p>Unsere Stärke ist die Zuverlässigkeit. Als Team von zwei Zweier-Teams sind wir flexibel und können Ihnen auch bei kurzfristigen oder großen Projekten garantieren, dass die Arbeit termingenu und in höchster Qualität erledigt wird.</p>
                    <ul class="usp-list">
                        <li><strong>Kein Kleingedrucktes:</strong> Klare Preise, keine versteckten Kosten.</li>
                        <li><strong>Zuverlässigkeit:</strong> Wir kommen, wann wir sagen, dass wir kommen.</li>
                        <li><strong>Detailverliebt:</strong> Wir sehen, was andere übersehen.</li>
                        <li><strong>Lokale Stärke:</strong> Wir sind aus Kassel, für Kassel.</li>
                    </ul>
                </div>
                <div class="about-image">
                    <!-- Platzhalter für Teamfoto -->
                </div>
            </div>
        </div>
    </section>

    <!-- Galerie -->
    <section id="gallery" class="fade-in">
        <div class="container">
            <h2>Verwandlungskunst</h2>
            <p class="section-subtitle">Bilder sagen mehr als Worte. Sehen Sie selbst.</p>
            <div class="gallery-grid">
                <div class="gallery-item"></div>
                <div class="gallery-item"></div>
                <div class="gallery-item"></div>
                <div class="gallery-item"></div>
            </div>
        </div>
    </section>

    <!-- Kontakt -->
    <section id="contact" class="fade-in">
        <div class="container">
            <h2>Startbereit für mehr Sauberkeit?</h2>
            <p class="section-subtitle" style="color: #ccc;">Kontaktieren Sie uns noch heute für ein unverbindliches und transparentes Angebot.</p>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>So erreichen Sie uns</h3>
                    <div class="contact-detail">
                        <i class="fas fa-phone"></i> <span><strong>Telefon:</strong> [Ihre Nummer folgt]</span>
                    </div>
                    <div class="contact-detail">
                        <i class="fas fa-envelope"></i> <span><strong>E-Mail:</strong> [Ihre E-Mail folgt]</span>
                    </div>
                    <div class="contact-detail">
                        <i class="fas fa-clock"></i> <span><strong>Erreichbarkeit:</strong> Mo-Fr: 8-18 Uhr<br>Sa: Nach Vereinbarung</span>
                    </div>
                    <div class="contact-detail">
                        <i class="fas fa-map-marker-alt"></i> <span><strong>Einsatzgebiet:</strong> Kassel & Umgebung</span>
                    </div>
                </div>
                <div class="cta-box">
                    <h3>Angebot in 24h</h3>
                    <p>Senden Sie uns eine kurze Beschreibung Ihrer Räumlichkeiten und wir lassen Ihnen innerhalb von 24 Stunden ein detailliertes Angebot zukommen.</p>
                    <a href="#" class="btn" style="margin-top: 15px;">E-Mail schreiben</a>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2023 Blitzblank Kassel | Professionelle Gebäudereinigung</p>
        </div>
    </footer>

    <script>
        // Scroll-Animation für Abschnitte
        const fadeElements = document.querySelectorAll('.fade-in');
        
        const appearOptions = {
            threshold: 0.1,
            rootMargin: "0px 0px -100px 0px"
        };
        
        const appearOnScroll = new IntersectionObserver(function(entries, appearOnScroll) {
            entries.forEach(entry => {
                if (!entry.isIntersecting) return;
                entry.target.classList.add('visible');
                appearOnScroll.unobserve(entry.target);
            });
        }, appearOptions);
        
        fadeElements.forEach(element => {
            appearOnScroll.observe(element);
        });
        
        // Header-Animation beim Scrollen
        window.addEventListener('scroll', function() {
            const header = document.getElementById('main-header');
            if (window.scrollY > 50) {
                header.classList.add('header-scrolled');
            } else {
                header.classList.remove('header-scrolled');
            }
        });
    </script>
</body>
</html>
