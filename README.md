<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>KristallRein Kassel | Premium Gebäudereinigung & Unterhaltsreinigung</title>
    <meta name="description" content="Professionelle Gebäudereinigung in Kassel - Praxisreinigung, Büroreinigung, Bauendreinigung, Fensterreinigung. Jetzt kostenloses Angebot anfordern!">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #0066cc;
            --primary-dark: #0052a3;
            --secondary: #e6f2ff;
            --accent: #00b894;
            --accent-dark: #00a085;
            --dark: #1a365d;
            --darker: #0f2342;
            --light: #f8f9fa;
            --text: #2d3748;
            --text-light: #718096;
            --white: #ffffff;
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            --shadow-lg: 0 20px 50px rgba(0, 0, 0, 0.15);
            --border-radius: 12px;
            --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            scroll-padding-top: 80px;
        }

        body {
            font-family: 'Inter', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.7;
            color: var(--text);
            background-color: var(--white);
            overflow-x: hidden;
            font-weight: 400;
        }

        .container {
            width: 90%;
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* ===== COOKIE BANNER ===== */
        .cookie-banner {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            background: var(--dark);
            color: var(--white);
            padding: 25px;
            z-index: 9999;
            box-shadow: 0 -5px 20px rgba(0, 0, 0, 0.2);
            transform: translateY(100%);
            transition: transform 0.5s ease;
        }

        .cookie-banner.active {
            transform: translateY(0);
        }

        .cookie-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 30px;
        }

        .cookie-text {
            flex: 1;
        }

        .cookie-text h3 {
            margin-bottom: 10px;
            color: var(--white);
        }

        .cookie-text p {
            color: rgba(255, 255, 255, 0.8);
            font-size: 0.95em;
            line-height: 1.5;
        }

        .cookie-text a {
            color: var(--accent);
            text-decoration: none;
        }

        .cookie-text a:hover {
            text-decoration: underline;
        }

        .cookie-buttons {
            display: flex;
            gap: 15px;
            flex-shrink: 0;
        }

        .cookie-btn {
            padding: 12px 25px;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            font-size: 0.95em;
        }

        .cookie-accept {
            background: var(--accent);
            color: white;
        }

        .cookie-accept:hover {
            background: var(--accent-dark);
            transform: translateY(-2px);
        }

        .cookie-settings {
            background: transparent;
            color: var(--white);
            border: 1px solid rgba(255, 255, 255, 0.3);
        }

        .cookie-settings:hover {
            background: rgba(255, 255, 255, 0.1);
        }

        /* ===== PREMIUM HEADER ===== */
        header {
            background: linear-gradient(135deg, var(--dark) 0%, var(--darker) 100%);
            padding: 18px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: var(--shadow);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            transition: var(--transition);
        }

        header.scrolled {
            padding: 12px 0;
            background: rgba(26, 54, 93, 0.95);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: relative;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
            text-decoration: none;
        }

        .logo-icon {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, var(--accent) 0%, var(--primary) 100%);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 700;
            font-size: 1.5em;
            box-shadow: 0 4px 15px rgba(0, 184, 148, 0.4);
            position: relative;
            overflow: hidden;
        }

        .logo-icon::before {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            background: rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            top: 5px;
            left: 10px;
        }

        .logo-icon::after {
            content: '✨';
            position: absolute;
            font-size: 0.8em;
            bottom: 5px;
            right: 8px;
        }

        .logo-text {
            font-size: 1.8em;
            font-weight: 800;
            color: var(--white);
            letter-spacing: -0.5px;
        }

        .logo-text span {
            color: var(--accent);
            font-weight: 800;
        }

        .logo-tagline {
            font-size: 0.7em;
            color: var(--accent);
            font-weight: 500;
            margin-top: -2px;
            letter-spacing: 0.5px;
        }

        /* Navigation */
        nav ul {
            list-style: none;
            display: flex;
            gap: 35px;
            margin: 0;
            padding: 0;
        }

        nav a {
            text-decoration: none;
            color: var(--white);
            font-weight: 600;
            font-size: 1.05em;
            transition: var(--transition);
            position: relative;
            padding: 8px 0;
        }

        nav a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent);
            transition: var(--transition);
        }

        nav a:hover {
            color: var(--accent);
        }

        nav a:hover::after {
            width: 100%;
        }

        nav a.active {
            color: var(--accent);
        }

        nav a.active::after {
            width: 100%;
        }

        .header-cta {
            display: flex;
            align-items: center;
            gap: 20px;
        }

        /* Mobile Menu */
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: var(--white);
            font-size: 1.5em;
            cursor: pointer;
            padding: 5px;
        }

        /* ===== ULTRA PREMIUM HERO SECTION ===== */
        .hero {
            background: linear-gradient(135deg, 
                rgba(0, 102, 204, 0.92) 0%, 
                rgba(0, 66, 138, 0.95) 100%),
                url('https://images.unsplash.com/photo-1581578731548-c64695cc6952?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80') center/cover;
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
            margin-top: 0;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url("data:image/svg+xml,%3Csvg width='100' height='100' viewBox='0 0 100 100' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M11 18c3.866 0 7-3.134 7-7s-3.134-7-7-7-7 3.134-7 7 3.134 7 7 7zm48 25c3.866 0 7-3.134 7-7s-3.134-7-7-7-7 3.134-7 7 3.134 7 7 7zm-43-7c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zm63 31c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zM34 90c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zm56-76c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zM12 86c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm28-65c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm23-11c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm-6 60c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm29 22c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zM32 63c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm57-13c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm-9-21c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM60 91c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM35 41c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM12 60c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2z' fill='%23ffffff' fill-opacity='0.03' fill-rule='evenodd'/%3E%3C/svg%3E");
            animation: float 20s infinite linear;
        }

        @keyframes float {
            0% { transform: translateX(0) translateY(0); }
            100% { transform: translateX(-100px) translateY(-100px); }
        }

        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 650px;
            color: var(--white);
        }

        .hero-badge {
            display: inline-block;
            background: linear-gradient(135deg, var(--accent) 0%, var(--accent-dark) 100%);
            color: white;
            padding: 8px 20px;
            border-radius: 50px;
            font-weight: 600;
            font-size: 0.9em;
            margin-bottom: 25px;
            box-shadow: 0 4px 15px rgba(0, 184, 148, 0.4);
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        .hero-content h1 {
            font-size: 3.8em;
            font-weight: 800;
            line-height: 1.1;
            margin-bottom: 25px;
            letter-spacing: -1px;
            background: linear-gradient(135deg, #ffffff 0%, #e6f2ff 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero-content p {
            font-size: 1.3em;
            font-weight: 400;
            margin-bottom: 40px;
            line-height: 1.6;
            color: rgba(255, 255, 255, 0.9);
            max-width: 550px;
        }

        .hero-stats {
            display: flex;
            gap: 30px;
            margin-bottom: 40px;
        }

        .stat {
            text-align: center;
        }

        .stat-number {
            display: block;
            font-size: 2.2em;
            font-weight: 800;
            color: var(--accent);
            line-height: 1;
        }

        .stat-label {
            font-size: 0.9em;
            color: rgba(255, 255, 255, 0.8);
            font-weight: 500;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            gap: 12px;
            background: linear-gradient(135deg, var(--accent) 0%, var(--accent-dark) 100%);
            color: white;
            padding: 18px 45px;
            border: none;
            border-radius: 50px;
            text-decoration: none;
            font-size: 1.1em;
            font-weight: 700;
            cursor: pointer;
            transition: var(--transition);
            box-shadow: 0 6px 20px rgba(0, 184, 148, 0.4);
            position: relative;
            overflow: hidden;
        }

        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: var(--transition);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(0, 184, 148, 0.6);
        }

        .btn:hover::before {
            left: 100%;
        }

        .btn-secondary {
            background: transparent;
            border: 2px solid rgba(255, 255, 255, 0.3);
            box-shadow: none;
        }

        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.1);
            border-color: rgba(255, 255, 255, 0.5);
        }

        .btn-group {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        /* ===== PREMIUM SERVICES SECTION ===== */
        .services {
            padding: 120px 0;
            background: var(--light);
            position: relative;
        }

        .services::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 1px;
            background: linear-gradient(90deg, transparent, var(--primary), transparent);
        }

        .section-header {
            text-align: center;
            margin-bottom: 70px;
        }

        .section-badge {
            display: inline-block;
            background: var(--secondary);
            color: var(--primary);
            padding: 8px 20px;
            border-radius: 50px;
            font-weight: 600;
            font-size: 0.9em;
            margin-bottom: 20px;
            border: 1px solid rgba(0, 102, 204, 0.1);
        }

        .section-title {
            font-size: 3em;
            font-weight: 800;
            color: var(--dark);
            margin-bottom: 20px;
            line-height: 1.1;
        }

        .section-subtitle {
            font-size: 1.3em;
            color: var(--text-light);
            max-width: 600px;
            margin: 0 auto;
            line-height: 1.6;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }

        .service-card {
            background: var(--white);
            padding: 45px 35px;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            transition: var(--transition);
            position: relative;
            overflow: hidden;
            border: 1px solid rgba(0, 0, 0, 0.05);
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(135deg, var(--primary) 0%, var(--accent) 100%);
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-lg);
        }

        .service-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, var(--secondary) 0%, #d4e6ff 100%);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 25px;
            color: var(--primary);
            font-size: 2em;
            transition: var(--transition);
        }

        .service-card:hover .service-icon {
            transform: scale(1.1) rotate(5deg);
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-dark) 100%);
            color: white;
        }

        .service-card h3 {
            font-size: 1.6em;
            font-weight: 700;
            color: var(--dark);
            margin-bottom: 15px;
            line-height: 1.3;
        }

        .service-card p {
            color: var(--text-light);
            margin-bottom: 25px;
            line-height: 1.6;
        }

        .service-features {
            list-style: none;
            margin-bottom: 25px;
        }

        .service-features li {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 8px;
            color: var(--text);
            font-weight: 500;
        }

        .service-features li i {
            color: var(--accent);
            font-size: 0.9em;
        }

        .service-price {
            font-size: 1.4em;
            font-weight: 800;
            color: var(--accent);
            margin-bottom: 20px;
        }

        .service-cta {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            color: var(--primary);
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
        }

        .service-cta:hover {
            color: var(--accent);
            gap: 12px;
        }

        /* ===== PREMIUM ABOUT SECTION ===== */
        .about {
            padding: 120px 0;
            background: var(--white);
            position: relative;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 80px;
            align-items: center;
        }

        .about-image {
            position: relative;
        }

        .about-image-main {
            width: 100%;
            height: 500px;
            background: linear-gradient(135deg, var(--primary) 0%, var(--dark) 100%);
            border-radius: var(--border-radius);
            position: relative;
            overflow: hidden;
            box-shadow: var(--shadow-lg);
        }

        .about-image-main::after {
            content: 'Professionelles Reinigungsteam';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, var(--primary) 0%, var(--dark) 100%);
            color: rgba(255, 255, 255, 0.8);
            font-size: 1.2em;
            font-weight: 600;
        }

        .about-text h2 {
            font-size: 2.8em;
            font-weight: 800;
            color: var(--dark);
            margin-bottom: 25px;
            line-height: 1.1;
        }

        .about-text p {
            font-size: 1.1em;
            color: var(--text-light);
            margin-bottom: 25px;
            line-height: 1.7;
        }

        .usp-list {
            list-style: none;
            margin: 35px 0;
        }

        .usp-list li {
            display: flex;
            align-items: flex-start;
            gap: 15px;
            margin-bottom: 20px;
            padding: 20px;
            background: var(--light);
            border-radius: var(--border-radius);
            border-left: 4px solid var(--accent);
            transition: var(--transition);
        }

        .usp-list li:hover {
            transform: translateX(5px);
            background: var(--secondary);
        }

        .usp-icon {
            width: 50px;
            height: 50px;
            background: var(--white);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--accent);
            font-size: 1.2em;
            flex-shrink: 0;
            box-shadow: var(--shadow);
        }

        .usp-content h4 {
            font-size: 1.2em;
            font-weight: 700;
            color: var(--dark);
            margin-bottom: 5px;
        }

        .usp-content p {
            margin: 0;
            font-size: 0.95em;
        }

        /* ===== PREMIUM GALLERY SECTION ===== */
        .gallery {
            padding: 120px 0;
            background: var(--light);
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(600px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }

        .gallery-comparison {
            position: relative;
            height: 400px;
            border-radius: var(--border-radius);
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            cursor: pointer;
            display: flex;
        }

        .gallery-comparison:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-lg);
        }

        .gallery-before, .gallery-after {
            width: 50%;
            height: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 600;
            font-size: 1.5em;
            position: relative;
            overflow: hidden;
        }

        .gallery-before {
            background: linear-gradient(135deg, #666 0%, #333 100%);
        }

        .gallery-after {
            background: linear-gradient(135deg, var(--primary) 0%, var(--dark) 100%);
        }

        .gallery-badge {
            position: absolute;
            top: 20px;
            padding: 8px 20px;
            background: rgba(0, 0, 0, 0.7);
            color: white;
            border-radius: 4px;
            font-size: 0.8em;
            z-index: 2;
        }

        .gallery-before .gallery-badge {
            left: 20px;
            background: rgba(102, 102, 102, 0.9);
        }

        .gallery-after .gallery-badge {
            right: 20px;
            background: rgba(0, 102, 204, 0.9);
        }

        .gallery-icon {
            font-size: 2.5em;
            margin-bottom: 15px;
        }

        .gallery-label {
            margin-top: 10px;
            font-size: 1.2em;
        }

        /* ===== SOCIAL MEDIA SECTION ===== */
        .social-media {
            padding: 100px 0;
            background: var(--white);
            text-align: center;
        }

        .social-header {
            margin-bottom: 60px;
        }

        .social-title {
            font-size: 2.5em;
            font-weight: 800;
            color: var(--dark);
            margin-bottom: 20px;
        }

        .social-subtitle {
            font-size: 1.2em;
            color: var(--text-light);
            max-width: 600px;
            margin: 0 auto;
        }

        .social-platforms {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
        }

        .platform-card {
            background: var(--light);
            padding: 40px 30px;
            border-radius: var(--border-radius);
            transition: var(--transition);
            border: 1px solid rgba(0, 0, 0, 0.05);
        }

        .platform-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-lg);
        }

        .platform-icon {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 25px;
            font-size: 2em;
            color: white;
            transition: var(--transition);
        }

        .instagram .platform-icon {
            background: linear-gradient(45deg, #f09433, #e6683c, #dc2743, #cc2366, #bc1888);
        }

        .facebook .platform-icon {
            background: #3b5998;
        }

        .whatsapp .platform-icon {
            background: #25D366;
        }

        .tiktok .platform-icon {
            background: #000000;
        }

        .platform-card:hover .platform-icon {
            transform: scale(1.1) rotate(5deg);
        }

        .platform-card h3 {
            font-size: 1.4em;
            font-weight: 700;
            margin-bottom: 15px;
            color: var(--dark);
        }

        .platform-card p {
            color: var(--text-light);
            line-height: 1.6;
        }

        .social-exclusive {
            background: linear-gradient(135deg, var(--primary) 0%, var(--dark) 100%);
            color: white;
            padding: 50px;
            border-radius: var(--border-radius);
            margin-top: 50px;
            position: relative;
            overflow: hidden;
        }

        .social-exclusive::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url("data:image/svg+xml,%3Csvg width='100' height='100' viewBox='0 0 100 100' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M11 18c3.866 0 7-3.134 7-7s-3.134-7-7-7-7 3.134-7 7 3.134 7 7 7zm48 25c3.866 0 7-3.134 7-7s-3.134-7-7-7-7 3.134-7 7 3.134 7 7 7zm-43-7c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zm63 31c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zM34 90c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zm56-76c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zM12 86c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm28-65c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm23-11c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm-6 60c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm29 22c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zM32 63c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm57-13c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm-9-21c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM60 91c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM35 41c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM12 60c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2z' fill='%23ffffff' fill-opacity='0.03' fill-rule='evenodd'/%3E%3C/svg%3E");
        }

        .social-exclusive-content {
            position: relative;
            z-index: 2;
        }

        .social-exclusive h3 {
            font-size: 1.8em;
            font-weight: 700;
            margin-bottom: 15px;
        }

        .social-exclusive p {
            font-size: 1.1em;
            opacity: 0.9;
            max-width: 600px;
            margin: 0 auto;
        }

        /* ===== PREMIUM CONTACT SECTION ===== */
        .contact {
            padding: 120px 0;
            background: linear-gradient(135deg, var(--dark) 0%, var(--darker) 100%);
            color: var(--white);
            position: relative;
        }

        .contact::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url("data:image/svg+xml,%3Csvg width='100' height='100' viewBox='0 0 100 100' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M11 18c3.866 0 7-3.134 7-7s-3.134-7-7-7-7 3.134-7 7 3.134 7 7 7zm48 25c3.866 0 7-3.134 7-7s-3.134-7-7-7-7 3.134-7 7 3.134 7 7 7zm-43-7c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zm63 31c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zM34 90c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zm56-76c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zM12 86c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm28-65c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm23-11c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm-6 60c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm29 22c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zM32 63c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm57-13c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm-9-21c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM60 91c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM35 41c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM12 60c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2z' fill='%23ffffff' fill-opacity='0.03' fill-rule='evenodd'/%3E%3C/svg%3E");
        }

        .contact .section-title {
            color: var(--white);
        }

        .contact .section-subtitle {
            color: rgba(255, 255, 255, 0.8);
        }

        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            position: relative;
            z-index: 2;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        .contact-method {
            display: flex;
            align-items: flex-start;
            gap: 20px;
            padding: 25px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: var(--border-radius);
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: var(--transition);
            backdrop-filter: blur(10px);
        }

        .contact-method:hover {
            background: rgba(255, 255, 255, 0.1);
            transform: translateX(5px);
        }

        .contact-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, var(--accent) 0%, var(--accent-dark) 100%);
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5em;
            flex-shrink: 0;
        }

        .contact-details h3 {
            font-size: 1.3em;
            font-weight: 700;
            margin-bottom: 8px;
            color: var(--white);
        }

        .contact-details p {
            color: rgba(255, 255, 255, 0.8);
            margin-bottom: 5px;
            line-height: 1.5;
        }

        .contact-link {
            color: var(--accent);
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
        }

        .contact-link:hover {
            color: var(--white);
        }

        /* ===== FORMULAR STYLES ===== */
        .form-container {
            background: rgba(255, 255, 255, 0.05);
            padding: 40px;
            border-radius: var(--border-radius);
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
        }

        .form-header {
            margin-bottom: 30px;
        }

        .form-header h3 {
            font-size: 1.8em;
            font-weight: 700;
            margin-bottom: 10px;
            color: var(--white);
        }

        .form-header p {
            color: rgba(255, 255, 255, 0.8);
            line-height: 1.6;
        }

        .form-group {
            margin-bottom: 25px;
        }

        .form-label {
            display: block;
            color: var(--white);
            font-weight: 600;
            margin-bottom: 8px;
            font-size: 0.95em;
        }

        .form-label span {
            color: var(--accent);
        }

        .form-input, .form-select, .form-textarea {
            width: 100%;
            padding: 15px 20px;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 8px;
            color: var(--white);
            font-size: 1em;
            transition: var(--transition);
        }

        .form-input:focus, .form-select:focus, .form-textarea:focus {
            outline: none;
            border-color: var(--accent);
            background: rgba(255, 255, 255, 0.15);
        }

        .form-textarea {
            min-height: 120px;
            resize: vertical;
        }

        .form-checkbox {
            display: flex;
            align-items: flex-start;
            gap: 10px;
            margin-top: 25px;
        }

        .form-checkbox input {
            margin-top: 5px;
        }

        .form-checkbox label {
            color: rgba(255, 255, 255, 0.8);
            font-size: 0.9em;
            line-height: 1.5;
        }

        .form-submit {
            width: 100%;
            margin-top: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }

        .form-submit .btn {
            width: 100%;
            justify-content: center;
        }

        .guarantee-badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: rgba(0, 184, 148, 0.1);
            color: var(--accent);
            padding: 10px 20px;
            border-radius: 50px;
            font-weight: 600;
            margin-top: 20px;
            border: 1px solid rgba(0, 184, 148, 0.2);
        }

        /* ===== RECHTLICHE SEITEN STYLES ===== */
        .legal-page {
            padding: 140px 0 80px;
            background: var(--light);
            min-height: 100vh;
        }

        .legal-container {
            background: var(--white);
            padding: 60px;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            max-width: 900px;
            margin: 0 auto;
        }

        .legal-header {
            margin-bottom: 40px;
            padding-bottom: 20px;
            border-bottom: 2px solid var(--secondary);
        }

        .legal-header h1 {
            font-size: 2.5em;
            color: var(--dark);
            margin-bottom: 10px;
        }

        .legal-header .date {
            color: var(--text-light);
            font-size: 0.95em;
        }

        .legal-content {
            line-height: 1.8;
        }

        .legal-content h2 {
            color: var(--dark);
            margin: 30px 0 15px;
            font-size: 1.5em;
        }

        .legal-content h3 {
            color: var(--text);
            margin: 25px 0 10px;
            font-size: 1.2em;
        }

        .legal-content p {
            margin-bottom: 15px;
            color: var(--text);
        }

        .legal-content ul, .legal-content ol {
            margin: 15px 0 15px 30px;
            color: var(--text);
        }

        .legal-content li {
            margin-bottom: 8px;
        }

        .legal-content a {
            color: var(--primary);
            text-decoration: none;
        }

        .legal-content a:hover {
            text-decoration: underline;
        }

        .back-to-home {
            display: inline-block;
            margin-top: 40px;
            color: var(--primary);
            text-decoration: none;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .back-to-home:hover {
            color: var(--accent);
            gap: 12px;
        }

        /* ===== PREMIUM FOOTER ===== */
        footer {
            background: var(--darker);
            color: var(--white);
            padding: 60px 0 30px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-logo {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .footer-logo .logo-text {
            font-size: 1.8em;
        }

        .footer-description {
            color: rgba(255, 255, 255, 0.7);
            line-height: 1.6;
            max-width: 300px;
        }

        .footer-heading {
            font-size: 1.2em;
            font-weight: 700;
            margin-bottom: 20px;
            color: var(--white);
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 12px;
        }

        .footer-links a {
            color: rgba(255, 255, 255, 0.7);
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-links a:hover {
            color: var(--accent);
            padding-left: 5px;
        }

        .footer-bottom {
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            text-align: center;
            color: rgba(255, 255, 255, 0.6);
            font-size: 0.9em;
        }

        /* ===== RESPONSIVE DESIGN ===== */
        @media (max-width: 1024px) {
            .hero-content h1 {
                font-size: 3.2em;
            }
            
            .about-content {
                gap: 50px;
            }
            
            .footer-content {
                grid-template-columns: 1fr 1fr;
                gap: 40px;
            }
            
            .social-platforms {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .gallery-grid {
                grid-template-columns: 1fr;
            }
            
            .cookie-content {
                flex-direction: column;
                text-align: center;
            }
            
            .legal-container {
                padding: 40px 30px;
            }
        }

        @media (max-width: 768px) {
            .container {
                width: 95%;
                padding: 0 15px;
            }

            .header-container {
                flex-wrap: wrap;
            }

            .mobile-menu-btn {
                display: block;
            }

            nav {
                position: fixed;
                top: 80px;
                left: 0;
                width: 100%;
                background: var(--dark);
                padding: 20px;
                transform: translateY(-100%);
                opacity: 0;
                transition: var(--transition);
                box-shadow: var(--shadow);
            }

            nav.active {
                transform: translateY(0);
                opacity: 1;
            }

            nav ul {
                flex-direction: column;
                gap: 0;
            }

            nav li {
                margin: 0;
            }

            nav a {
                display: block;
                padding: 15px 0;
                border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            }

            .header-cta {
                display: none;
            }

            .hero-content h1 {
                font-size: 2.5em;
            }

            .hero-content p {
                font-size: 1.1em;
            }

            .hero-stats {
                flex-direction: column;
                gap: 20px;
            }

            .btn-group {
                flex-direction: column;
            }

            .services-grid {
                grid-template-columns: 1fr;
            }

            .about-content {
                grid-template-columns: 1fr;
                gap: 40px;
            }

            .contact-container {
                grid-template-columns: 1fr;
                gap: 40px;
            }

            .section-title {
                font-size: 2.2em;
            }

            .footer-content {
                grid-template-columns: 1fr;
                gap: 30px;
            }
            
            .social-platforms {
                grid-template-columns: 1fr;
            }
            
            .social-title {
                font-size: 2em;
            }
            
            .gallery-grid {
                grid-template-columns: 1fr;
            }
            
            .gallery-comparison {
                height: 300px;
                flex-direction: column;
            }
            
            .gallery-before, .gallery-after {
                width: 100%;
                height: 50%;
            }
            
            .cookie-buttons {
                flex-direction: column;
                width: 100%;
            }
            
            .cookie-btn {
                width: 100%;
            }
            
            .legal-page {
                padding: 120px 0 60px;
            }
            
            .legal-container {
                padding: 30px 20px;
            }
            
            .legal-header h1 {
                font-size: 2em;
            }
        }

        @media (max-width: 480px) {
            .hero-content h1 {
                font-size: 2em;
            }

            .section-title {
                font-size: 1.8em;
            }

            .service-card {
                padding: 30px 20px;
            }

            .btn {
                padding: 15px 30px;
                font-size: 1em;
            }
            
            .social-exclusive {
                padding: 30px 20px;
            }
            
            .form-container {
                padding: 25px 20px;
            }
        }
    </style>
</head>
<body>
    <!-- ===== COOKIE BANNER ===== -->
    <div class="cookie-banner" id="cookieBanner">
        <div class="container">
            <div class="cookie-content">
                <div class="cookie-text">
                    <h3>🍪 Cookies & Datenschutz</h3>
                    <p>Wir verwenden Cookies, um Ihnen das beste Erlebnis auf unserer Website zu bieten. Einige Cookies sind notwendig für den Betrieb der Seite, andere helfen uns, Ihre Erfahrung zu verbessern. Weitere Informationen finden Sie in unserer <a href="#datenschutz">Datenschutzerklärung</a>.</p>
                </div>
                <div class="cookie-buttons">
                    <button class="cookie-btn cookie-accept" id="acceptCookies">Alle akzeptieren</button>
                    <button class="cookie-btn cookie-settings" id="cookieSettings">Einstellungen</button>
                </div>
            </div>
        </div>
    </div>

    <!-- ===== ULTRA PREMIUM HEADER ===== -->
    <header id="main-header">
        <div class="container header-container">
            <a href="#home" class="logo">
                <div class="logo-icon">KR</div>
                <div>
                    <div class="logo-text">Kristall<span>Rein</span> Kassel</div>
                    <div class="logo-tagline">PREMIUM GEBÄUDEREINIGUNG</div>
                </div>
            </a>

            <nav id="main-nav">
                <ul>
                    <li><a href="#home" class="active">Start</a></li>
                    <li><a href="#services">Leistungen</a></li>
                    <li><a href="#about">Über Uns</a></li>
                    <li><a href="#gallery">Referenzen</a></li>
                    <li><a href="#social">Social Media</a></li>
                    <li><a href="#contact">Kontakt</a></li>
                </ul>
            </nav>

            <button class="mobile-menu-btn" id="mobile-menu-toggle">
                <i class="fas fa-bars"></i>
            </button>
        </div>
    </header>

    <!-- ===== ULTRA PREMIUM HERO SECTION ===== -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="hero-badge">
                    <i class="fas fa-star"></i> Nr. 1 in Kassel
                </div>
                
                <h1>Kristall-klare Sauberkeit.<br>Ein perfekter erster Eindruck.</h1>
                
                <p>Wir machen Ihre Praxis, Ihr Büro oder Ihre Baustelle nicht nur rein, sondern strahlend sauber. Denn Sauberkeit ist das Fundament für Vertrauen und Erfolg.</p>

                <div class="hero-stats">
                    <div class="stat">
                        <span class="stat-number">500+</span>
                        <span class="stat-label">Zufriedene Kunden</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number">24h</span>
                        <span class="stat-label">Schnelle Reaktion</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number">100%</span>
                        <span class="stat-label">Zufriedenheit</span>
                    </div>
                </div>

                <div class="btn-group">
                    <a href="#contact" class="btn">
                        <i class="fas fa-bolt"></i>
                        Kostenlose Erstreinigung
                    </a>
                    <a href="#services" class="btn btn-secondary">
                        <i class="fas fa-play-circle"></i>
                        Leistungen entdecken
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== ULTRA PREMIUM SERVICES SECTION ===== -->
    <section id="services" class="services">
        <div class="container">
            <div class="section-header">
                <div class="section-badge">Unsere Premium-Leistungen</div>
                <h2 class="section-title">Ihr Spezialist für kristall-klare Sauberkeit</h2>
                <p class="section-subtitle">Maßgeschneiderte Reinigungslösungen für anspruchsvolle Gewerbekunden in Kassel und Umgebung</p>
            </div>

            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-clinic-medical"></i>
                    </div>
                    <h3>Praxen- & Arztreinigung</h3>
                    <p>Höchste Hygienestandards für medizinische Einrichtungen. Wir garantieren sterile Sauberkeit für Ihre Patienten und Mitarbeiter.</p>
                    
                    <ul class="service-features">
                        <li><i class="fas fa-check"></i> Desinfektion aller Oberflächen</li>
                        <li><i class="fas fa-check"></i> Spezialreinigung OP-Bereiche</li>
                        <li><i class="fas fa-check"></i> Hygienekonzept nach DIN</li>
                        <li><i class="fas fa-check"></i> Flexible Reinigungszeiten</li>
                    </ul>
                    
                    <div class="service-price">Ab 4€/m² pro Reinigung</div>
                    <a href="#contact" class="service-cta">
                        Angebot anfordern
                        <i class="fas fa-arrow-right"></i>
                    </a>
                </div>

                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-building"></i>
                    </div>
                    <h3>Büroreinigung</h3>
                    <p>Steigern Sie die Produktivität und das Wohlbefinden in Ihrem Team mit einer einladenden Arbeitsumgebung.</p>
                    
                    <ul class="service-features">
                        <li><i class="fas fa-check"></i> Tägliche Grundreinigung</li>
                        <li><i class="fas fa-check"></i> Müllentsorgung</li>
                    </ul>
                    
                    <div class="service-price">Individuelle Angebote</div>
                    <a href="#contact" class="service-cta">
                        Angebot anfordern
                        <i class="fas fa-arrow-right"></i>
                    </a>
                </div>

                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-tools"></i>
                    </div>
                    <h3>Bauendreinigung</h3>
                    <p>Von der Baustelle zum bezugsfertigen Traum. Wir entfernen jeden letzten Krümel und Fleck professionell.</p>
                    
                    <ul class="service-features">
                        <li><i class="fas fa-check"></i> Entfernung von Bauschmutz</li>
                        <li><i class="fas fa-check"></i> Fensterreinigung innen/außen</li>
                        <li><i class="fas fa-check"></i> Bodenaufbereitung</li>
                        <li><i class="fas fa-check"></i> Endkontrolle & Übergabe</li>
                    </ul>
                    
                    <div class="service-price">Individuelle Angebote</div>
                    <a href="#contact" class="service-cta">
                        Angebot anfordern
                        <i class="fas fa-arrow-right"></i>
                    </a>
                </div>

                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-window-restore"></i>
                    </div>
                    <h3>Fensterreinigung</h3>
                    <p>Streifenfreie Sicht für mehr Licht und eine positive Außenwirkung. Innen & Außen, auch in schwierigen Höhen.</p>
                    
                    <ul class="service-features">
                        <li><i class="fas fa-check"></i> Innen- und Außenreinigung</li>
                        <li><i class="fas fa-check"></i> Wintergartenreinigung</li>
                        <li><i class="fas fa-check"></i> Streifenfreie Trocknung</li>
                    </ul>
                    
                    <div class="service-price">Ab 4,50 € pro Scheibe</div>
                    <a href="#contact" class="service-cta">
                        Angebot anfordern
                        <i class="fas fa-arrow-right"></i>
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== ULTRA PREMIUM ABOUT SECTION ===== -->
    <section id="about" class="about">
        <div class="container">
            <div class="about-content">
                <div class="about-image">
                    <div class="about-image-main"></div>
                </div>

                <div class="about-text">
                    <div class="section-badge">Warum KristallRein Kassel?</div>
                    <h2>Ihr Partner für makellose Sauberkeit</h2>
                    
                    <p>Wir sind <strong>KristallRein Kassel</strong> – ein eingespieltes Team von vier leidenschaftlichen Reinigungsexperten. Während andere hetzen, nehmen wir uns die Zeit, die es braucht, um jedes Detail perfekt zu machen.</p>

                    <ul class="usp-list">
                        <li>
                            <div class="usp-icon">
                                <i class="fas fa-shield-alt"></i>
                            </div>
                            <div class="usp-content">
                                <h4>Premium Qualitätsgarantie</h4>
                                <p>100% Zufriedenheit oder wir reinigen kostenlos nach</p>
                            </div>
                        </li>
                        <li>
                            <div class="usp-icon">
                                <i class="fas fa-clock"></i>
                            </div>
                            <div class="usp-content">
                                <h4>Flexible Terminierung</h4>
                                <p>Wir passen uns Ihrem Zeitplan an - auch außerhalb der Geschäftszeiten</p>
                            </div>
                        </li>
                        <li>
                            <div class="usp-icon">
                                <i class="fas fa-leaf"></i>
                            </div>
                            <div class="usp-content">
                                <h4>Ökologische Reinigung</h4>
                                <p>Umweltfreundliche Reinigungsmittel für Ihre Gesundheit</p>
                            </div>
                        </li>
                        <li>
                            <div class="usp-icon">
                                <i class="fas fa-award"></i>
                            </div>
                            <div class="usp-content">
                                <h4>Lokale Expertise</h4>
                                <p>Wir kennen Kassel und die Bedürfnisse der lokalen Unternehmen</p>
                            </div>
                        </li>
                    </ul>

                    <a href="#contact" class="btn">
                        <i class="fas fa-handshake"></i>
                        Jetzt persönlich beraten lassen
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== ULTRA PREMIUM GALLERY SECTION ===== -->
    <section id="gallery" class="gallery">
        <div class="container">
            <div class="section-header">
                <div class="section-badge">Unsere Referenzen</div>
                <h2 class="section-title">Verwandlungskunst in Perfektion</h2>
                <p class="section-subtitle">Bilder sagen mehr als Worte. Sehen Sie selbst, wie wir Räume verwandeln.</p>
            </div>

            <div class="gallery-grid">
                <div class="gallery-comparison">
                    <div class="gallery-before">
                        <div class="gallery-badge">VORHER</div>
                        <div class="gallery-icon"><i class="fas fa-clinic-medical"></i></div>
                        <div class="gallery-label">Praxis-Reinigung</div>
                    </div>
                    <div class="gallery-after">
                        <div class="gallery-badge">NACHHER</div>
                        <div class="gallery-icon"><i class="fas fa-clinic-medical"></i></div>
                        <div class="gallery-label">Praxis-Reinigung</div>
                    </div>
                </div>
                
                <div class="gallery-comparison">
                    <div class="gallery-before">
                        <div class="gallery-badge">VORHER</div>
                        <div class="gallery-icon"><i class="fas fa-building"></i></div>
                        <div class="gallery-label">Büro-Reinigung</div>
                    </div>
                    <div class="gallery-after">
                        <div class="gallery-badge">NACHHER</div>
                        <div class="gallery-icon"><i class="fas fa-building"></i></div>
                        <div class="gallery-label">Büro-Reinigung</div>
                    </div>
                </div>

                <div class="gallery-comparison">
                    <div class="gallery-before">
                        <div class="gallery-badge">VORHER</div>
                        <div class="gallery-icon"><i class="fas fa-tools"></i></div>
                        <div class="gallery-label">Bauendreinigung</div>
                    </div>
                    <div class="gallery-after">
                        <div class="gallery-badge">NACHHER</div>
                        <div class="gallery-icon"><i class="fas fa-tools"></i></div>
                        <div class="gallery-label">Bauendreinigung</div>
                    </div>
                </div>

                <div class="gallery-comparison">
                    <div class="gallery-before">
                        <div class="gallery-badge">VORHER</div>
                        <div class="gallery-icon"><i class="fas fa-window-restore"></i></div>
                        <div class="gallery-label">Fensterreinigung</div>
                    </div>
                    <div class="gallery-after">
                        <div class="gallery-badge">NACHHER</div>
                        <div class="gallery-icon"><i class="fas fa-window-restore"></i></div>
                        <div class="gallery-label">Fensterreinigung</div>
                    </div>
                </div>

                <div class="gallery-comparison">
                    <div class="gallery-before">
                        <div class="gallery-badge">VORHER</div>
                        <div class="gallery-icon"><i class="fas fa-building"></i></div>
                        <div class="gallery-label">Fassadenreinigung</div>
                    </div>
                    <div class="gallery-after">
                        <div class="gallery-badge">NACHHER</div>
                        <div class="gallery-icon"><i class="fas fa-building"></i></div>
                        <div class="gallery-label">Fassadenreinigung</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== SOCIAL MEDIA SECTION ===== -->
    <section id="social" class="social-media">
        <div class="container">
            <div class="social-header">
                <h2 class="social-title">Folge uns auf Social Media</h2>
                <p class="social-subtitle">Bleibe auf dem Laufenden mit unseren neuesten Projekten, Reinigungstipps und Special Offers!</p>
            </div>

            <div class="social-platforms">
                <div class="platform-card instagram">
                    <div class="platform-icon">
                        <i class="fab fa-instagram"></i>
                    </div>
                    <h3>Instagram</h3>
                    <p>Before/After<br>Bilder & Stories</p>
                </div>

                <div class="platform-card facebook">
                    <div class="platform-icon">
                        <i class="fab fa-facebook-f"></i>
                    </div>
                    <h3>Facebook</h3>
                    <p>Bewertungen & Updates</p>
                </div>

                <div class="platform-card tiktok">
                    <div class="platform-icon">
                        <i class="fab fa-tiktok"></i>
                    </div>
                    <h3>TikTok</h3>
                    <p>Reinigungs-Videos & Trends</p>
                </div>
            </div>

            <div class="social-exclusive">
                <div class="social-exclusive-content">
                    <h3>Exklusiv für Follower</h3>
                    <p>Special-Angebote die es nur auf Social Media gibt!</p>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== ULTRA PREMIUM CONTACT SECTION ===== -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-header">
                <div class="section-badge">Kontakt aufnehmen</div>
                <h2 class="section-title">Startbereit für kristall-klare Sauberkeit?</h2>
                <p class="section-subtitle">Kontaktieren Sie uns noch heute für ein unverbindliches und transparentes Angebot.</p>
            </div>

            <div class="contact-container">
                <div class="contact-info">
                    <div class="contact-method">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div class="contact-details">
                            <h3>Per E-Mail</h3>
                            <p>Antwort in kürzester Zeit</p>
                            <a href="mailto:info@krystalrein-kassel.de" class="contact-link">info@krystalrein-kassel.de</a>
                        </div>
                    </div>

                    <div class="contact-method">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="contact-details">
                            <h3>Einsatzgebiet</h3>
                            <p>Kassel & Umgebung</p>
                        </div>
                    </div>

                    <div class="contact-method">
                        <div class="contact-icon">
                            <i class="fas fa-clock"></i>
                        </div>
                        <div class="contact-details">
                            <h3>Notfallservice</h3>
                            <p>Weil wir unsere Kunden schätzen</p>
                            <p>auch nachmittags und abends nach Absprache</p>
                        </div>
                    </div>
                </div>

                <div class="form-container">
                    <div class="form-header">
                        <h3>Kostenloses Angebot anfordern</h3>
                        <p>Füllen Sie das Formular aus und wir melden uns innerhalb von 24 Stunden.</p>
                    </div>
                    
                    <form id="offer-form">
                        <div class="form-group">
                            <label class="form-label" for="name">Ihr Name <span>*</span></label>
                            <input type="text" id="name" class="form-input" placeholder="Max Mustermann" required>
                        </div>
                        
                        <div class="form-group">
                            <label class="form-label" for="email">Ihre E-Mail <span>*</span></label>
                            <input type="email" id="email" class="form-input" placeholder="max@beispiel.de" required>
                        </div>
                        
                        <div class="form-group">
                            <label class="form-label" for="phone">Telefon (optional)</label>
                            <input type="tel" id="phone" class="form-input" placeholder="+49 1515 1816181">
                        </div>
                        
                        <div class="form-group">
                            <label class="form-label" for="service">Dienstleistung <span>*</span></label>
                            <select id="service" class="form-select" required>
                                <option value="">Bitte wählen</option>
                                <option value="praxis">Praxen- & Arztreinigung</option>
                                <option value="office">Büroreinigung</option>
                                <option value="construction">Bauendreinigung</option>
                                <option value="windows">Fensterreinigung</option>
                                <option value="other">Andere Dienstleistung</option>
                            </select>
                        </div>
                        
                        <div class="form-group">
                            <label class="form-label" for="description">Projektbeschreibung <span>*</span></label>
                            <textarea id="description" class="form-textarea" placeholder="Fläche in m², Besonderheiten, gewünschter Zeitpunkt..." required></textarea>
                        </div>
                        
                        <div class="form-checkbox">
                            <input type="checkbox" id="privacy" required>
                            <label for="privacy">100% vertraulich & unverbindlich. *Pflichtfelder</label>
                        </div>
                        
                        <div class="form-submit">
                            <button type="submit" class="btn">
                                <i class="fas fa-paper-plane"></i>
                                Kostenloses Angebot anfordern
                            </button>
                        </div>
                    </form>

                    <div class="guarantee-badge">
                        <i class="fas fa-lock"></i>
                        Kostenlos & unverbindlich
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== ULTRA PREMIUM FOOTER ===== -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-logo">
                    <div class="logo-text">Kristall<span>Rein</span> Kassel</div>
                    <p class="footer-description">Ihr Premium-Partner für professionelle Gebäudereinigung in Kassel. Makellose Sauberkeit für Unternehmen, die Wert auf Qualität legen.</p>
                </div>

                <div class="footer-section">
                    <h3 class="footer-heading">Leistungen</h3>
                    <ul class="footer-links">
                        <li><a href="#services">Praxenreinigung</a></li>
                        <li><a href="#services">Büroreinigung</a></li>
                        <li><a href="#services">Bauendreinigung</a></li>
                        <li><a href="#services">Fensterreinigung</a></li>
                        <li><a href="#services">Fassadenreinigung</a></li>
                    </ul>
                </div>

                <div class="footer-section">
                    <h3 class="footer-heading">Unternehmen</h3>
                    <ul class="footer-links">
                        <li><a href="#about">Über Uns</a></li>
                        <li><a href="#gallery">Referenzen</a></li>
                        <li><a href="#social">Social Media</a></li>
                        <li><a href="#contact">Kontakt</a></li>
                        <li><a href="#contact">Karriere</a></li>
                    </ul>
                </div>

                <div class="footer-section">
                    <h3 class="footer-heading">Rechtliches</h3>
                    <ul class="footer-links">
                        <li><a href="#impressum">Impressum</a></li>
                        <li><a href="#datenschutz">Datenschutz</a></li>
                        <li><a href="#agb">AGB</a></li>
                        <li><a href="#cookies">Cookies</a></li>
                    </ul>
                </div>
            </div>

            <div class="footer-bottom">
                <p>&copy; 2025 KristallRein Kassel | Professionelle Gebäudereinigung | Alle Rechte vorbehalten</p>
            </div>
        </div>
    </footer>

    <!-- ===== RECHTLICHE SEITEN ===== -->
    <!-- Diese sind zunächst versteckt und werden über die Footer-Links aufgerufen -->
    
    <!-- Impressum -->
    <section id="impressum" class="legal-page" style="display: none;">
        <div class="container">
            <div class="legal-container">
                <div class="legal-header">
                    <h1>Impressum</h1>
                    <div class="date">Stand: Januar 2025</div>
                </div>
                
                <div class="legal-content">
                    <h2>Angaben gemäß § 5 TMG</h2>
                    <p><strong>KristallRein Kassel</strong><br>
                    Musterstraße 123<br>
                    34117 Kassel<br>
                    Deutschland</p>
                    
                    <h2>Kontakt</h2>
                    <p>Telefon: +49 1515 1816181<br>
                    E-Mail: info@krystalrein-kassel.de<br>
                    Website: www.kristallrein-kassel.de</p>
                    
                    <h2>Vertreten durch</h2>
                    <p>Max Mustermann (Geschäftsführer)</p>
                    
                    <h2>Umsatzsteuer-ID</h2>
                    <p>Umsatzsteuer-Identifikationsnummer gemäß § 27 a Umsatzsteuergesetz:<br>
                    DE 123 456 789</p>
                    
                    <h2>Berufsbezeichnung und berufsrechtliche Regelungen</h2>
                    <p>Berufsbezeichnung: Gebäudereiniger<br>
                    Zuständige Kammer: Handwerkskammer Kassel<br>
                    Verliehen in: Deutschland</p>
                    
                    <h2>EU-Streitschlichtung</h2>
                    <p>Die Europäische Kommission stellt eine Plattform zur Online-Streitbeilegung (OS) bereit: 
                    <a href="https://ec.europa.eu/consumers/odr/" target="_blank">https://ec.europa.eu/consumers/odr/</a>.<br>
                    Unsere E-Mail-Adresse finden Sie oben im Impressum.</p>
                    
                    <h2>Verbraucherstreitbeilegung/Universalschlichtungsstelle</h2>
                    <p>Wir sind nicht bereit oder verpflichtet, an Streitbeilegungsverfahren vor einer Verbraucherschlichtungsstelle teilzunehmen.</p>
                    
                    <h2>Haftung für Inhalte</h2>
                    <p>Als Diensteanbieter sind wir gemäß § 7 Abs.1 TMG für eigene Inhalte auf diesen Seiten nach den allgemeinen Gesetzen verantwortlich. Nach §§ 8 bis 10 TMG sind wir als Diensteanbieter jedoch nicht verpflichtet, übermittelte oder gespeicherte fremde Informationen zu überwachen oder nach Umständen zu forschen, die auf eine rechtswidrige Tätigkeit hinweisen.</p>
                    
                    <a href="#home" class="back-to-home">
                        <i class="fas fa-arrow-left"></i> Zurück zur Startseite
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Datenschutz -->
    <section id="datenschutz" class="legal-page" style="display: none;">
        <div class="container">
            <div class="legal-container">
                <div class="legal-header">
                    <h1>Datenschutzerklärung</h1>
                    <div class="date">Stand: Januar 2025</div>
                </div>
                
                <div class="legal-content">
                    <h2>1. Datenschutz auf einen Blick</h2>
                    <h3>Allgemeine Hinweise</h3>
                    <p>Die folgenden Hinweise geben einen einfachen Überblick darüber, was mit Ihren personenbezogenen Daten passiert, wenn Sie diese Website besuchen. Personenbezogene Daten sind alle Daten, mit denen Sie persönlich identifiziert werden können.</p>
                    
                    <h3>Datenerfassung auf dieser Website</h3>
                    <p><strong>Wer ist verantwortlich für die Datenerfassung auf dieser Website?</strong><br>
                    Die Datenverarbeitung auf dieser Website erfolgt durch den Websitebetreiber. Dessen Kontaktdaten können Sie dem Abschnitt „Hinweis zur Verantwortlichen Stelle" in dieser Datenschutzerklärung entnehmen.</p>
                    
                    <h2>2. Hosting</h2>
                    <p>Wir hosten die Inhalte unserer Website bei folgendem Anbieter:</p>
                    <h3>Externes Hosting</h3>
                    <p>Diese Website wird extern gehostet. Die personenbezogenen Daten, die auf dieser Website erfasst werden, werden auf den Servern des Hosters / der Hoster gespeichert.</p>
                    
                    <h2>3. Allgemeine Hinweise und Pflichtinformationen</h2>
                    <h3>Datenschutz</h3>
                    <p>Die Betreiber dieser Seiten nehmen den Schutz Ihrer persönlichen Daten sehr ernst. Wir behandeln Ihre personenbezogenen Daten vertraulich und entsprechend den gesetzlichen Datenschutzvorschriften sowie dieser Datenschutzerklärung.</p>
                    
                    <h2>4. Datenerfassung auf dieser Website</h2>
                    <h3>Cookies</h3>
                    <p>Unsere Internetseiten verwenden so genannte „Cookies". Cookies sind kleine Textdateien und richten auf Ihrem Endgerät keinen Schaden an. Sie werden entweder vorübergehend für die Dauer einer Sitzung (Session-Cookies) oder dauerhaft (permanente Cookies) auf Ihrem Endgerät gespeichert.</p>
                    
                    <h3>Kontaktformular</h3>
                    <p>Wenn Sie uns per Kontaktformular Anfragen zukommen lassen, werden Ihre Angaben aus dem Anfrageformular inklusive der von Ihnen dort angegebenen Kontaktdaten zwecks Bearbeitung der Anfrage und für den Fall von Anschlussfragen bei uns gespeichert.</p>
                    
                    <h2>5. Ihre Rechte</h2>
                    <p>Sie haben jederzeit das Recht, unentgeltlich Auskunft über Herkunft, Empfänger und Zweck Ihrer gespeicherten personenbezogenen Daten zu erhalten. Sie haben außerdem ein Recht, die Berichtigung oder Löschung dieser Daten zu verlangen.</p>
                    
                    <a href="#home" class="back-to-home">
                        <i class="fas fa-arrow-left"></i> Zurück zur Startseite
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- AGB -->
    <section id="agb" class="legal-page" style="display: none;">
        <div class="container">
            <div class="legal-container">
                <div class="legal-header">
                    <h1>Allgemeine Geschäftsbedingungen (AGB)</h1>
                    <div class="date">Stand: Januar 2025</div>
                </div>
                
                <div class="legal-content">
                    <h2>§ 1 Geltungsbereich</h2>
                    <p>Diese Allgemeinen Geschäftsbedingungen (AGB) gelten für alle Verträge zwischen KristallRein Kassel (im Folgenden "Unternehmen") und seinen Kunden (im Folgenden "Kunde") über die Erbringung von Gebäudereinigungsdienstleistungen.</p>
                    
                    <h2>§ 2 Angebot und Vertragsschluss</h2>
                    <p>1. Angebote des Unternehmens sind freibleibend und unverbindlich.<br>
                    2. Der Vertrag kommt durch schriftliche Auftragsbestätigung des Unternehmens oder durch Ausführung der Leistung zustande.</p>
                    
                    <h2>§ 3 Leistungsumfang</h2>
                    <p>1. Der genaue Leistungsumfang ergibt sich aus der schriftlichen Vereinbarung.<br>
                    2. Das Unternehmen erbringt seine Leistungen mit der gebotenen Sorgfalt nach den Regeln der Gebäudereinigerbranche.</p>
                    
                    <h2>§ 4 Preise und Zahlungsbedingungen</h2>
                    <p>1. Alle Preise verstehen sich zuzüglich der gesetzlichen Mehrwertsteuer.<br>
                    2. Rechnungen sind innerhalb von 14 Tagen nach Rechnungsdatum ohne Abzug zahlbar.</p>
                    
                    <h2>§ 5 Haftung</h2>
                    <p>1. Das Unternehmen haftet für Vorsatz und grobe Fahrlässigkeit.<br>
                    2. Bei leichter Fahrlässigkeit haftet das Unternehmen nur bei Verletzung wesentlicher Vertragspflichten.</p>
                    
                    <h2>§ 6 Kündigung</h2>
                    <p>1. Der Vertrag kann von beiden Seiten mit einer Frist von 4 Wochen zum Monatsende gekündigt werden.<br>
                    2. Das Recht zur fristlosen Kündigung aus wichtigem Grund bleibt unberührt.</p>
                    
                    <h2>§ 7 Schlussbestimmungen</h2>
                    <p>1. Es gilt das Recht der Bundesrepublik Deutschland.<br>
                    2. Gerichtsstand ist Kassel.</p>
                    
                    <a href="#home" class="back-to-home">
                        <i class="fas fa-arrow-left"></i> Zurück zur Startseite
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Cookies -->
    <section id="cookies" class="legal-page" style="display: none;">
        <div class="container">
            <div class="legal-container">
                <div class="legal-header">
                    <h1>Cookie-Richtlinie</h1>
                    <div class="date">Stand: Januar 2025</div>
                </div>
                
                <div class="legal-content">
                    <h2>Was sind Cookies?</h2>
                    <p>Cookies sind kleine Textdateien, die auf Ihrem Gerät (Computer, Smartphone, Tablet) gespeichert werden, wenn Sie unsere Website besuchen. Sie enthalten Informationen über Ihr Surfverhalten und dienen dazu, Ihren Besuch auf unserer Website komfortabler zu gestalten.</p>
                    
                    <h2>Welche Cookies verwenden wir?</h2>
                    <h3>Notwendige Cookies</h3>
                    <p>Diese Cookies sind für den Betrieb der Website unerlässlich und können nicht deaktiviert werden. Sie werden in der Regel als Reaktion auf von Ihnen getätigte Aktionen gesetzt, wie z.B. das Festlegen Ihrer Datenschutzeinstellungen.</p>
                    
                    <h3>Funktionale Cookies</h3>
                    <p>Diese Cookies ermöglichen es der Website, erweiterte Funktionen und Personalisierung bereitzustellen. Sie können von uns oder von Drittanbietern, deren Dienste wir auf unseren Seiten verwenden, gesetzt werden.</p>
                    
                    <h3>Analytische Cookies</h3>
                    <p>Diese Cookies helfen uns zu verstehen, wie Besucher mit der Website interagieren, indem Informationen anonym gesammelt und gemeldet werden.</p>
                    
                    <h2>Cookie-Verwaltung</h2>
                    <p>Die meisten Browser akzeptieren Cookies automatisch. Sie können Ihren Browser so einstellen, dass Cookies abgelehnt oder Sie benachrichtigt werden, wenn ein Cookie gesetzt wird. Bitte beachten Sie, dass das Deaktivieren von Cookies die Funktionalität dieser Website einschränken kann.</p>
                    
                    <h2>Detaillierte Cookie-Liste</h2>
                    <table style="width: 100%; border-collapse: collapse; margin: 20px 0;">
                        <tr style="background: var(--secondary);">
                            <th style="padding: 10px; text-align: left; border: 1px solid #ddd;">Cookie-Name</th>
                            <th style="padding: 10px; text-align: left; border: 1px solid #ddd;">Zweck</th>
                            <th style="padding: 10px; text-align: left; border: 1px solid #ddd;">Ablauf</th>
                        </tr>
                        <tr>
                            <td style="padding: 10px; border: 1px solid #ddd;">cookie_consent</td>
                            <td style="padding: 10px; border: 1px solid #ddd;">Speichert Ihre Cookie-Einstellungen</td>
                            <td style="padding: 10px; border: 1px solid #ddd;">1 Jahr</td>
                        </tr>
                        <tr>
                            <td style="padding: 10px; border: 1px solid #ddd;">session_id</td>
                            <td style="padding: 10px; border: 1px solid #ddd;">Erkennt Sie während Ihres Besuchs</td>
                            <td style="padding: 10px; border: 1px solid #ddd;">Session</td>
                        </tr>
                    </table>
                    
                    <h2>Ihre Rechte</h2>
                    <p>Sie haben das Recht, jederzeit der Verwendung von Cookies zu widersprechen, die nicht für den Betrieb der Website notwendig sind. Bitte nutzen Sie dazu die Cookie-Einstellungen in Ihrem Browser oder unser Cookie-Banner.</p>
                    
                    <a href="#home" class="back-to-home">
                        <i class="fas fa-arrow-left"></i> Zurück zur Startseite
                    </a>
                </div>
            </div>
        </div>
    </section>

    <script>
        // Premium JavaScript für ultra-smooth Interaktionen
        document.addEventListener('DOMContentLoaded', function() {
            // Cookie Banner Funktionen
            const cookieBanner = document.getElementById('cookieBanner');
            const acceptCookiesBtn = document.getElementById('acceptCookies');
            const cookieSettingsBtn = document.getElementById('cookieSettings');
            
            // Prüfen ob Cookie-Einstellungen bereits gespeichert sind
            const cookiesAccepted = localStorage.getItem('cookiesAccepted');
            
            if (!cookiesAccepted) {
                // Zeige Cookie-Banner nach 1 Sekunde
                setTimeout(() => {
                    cookieBanner.classList.add('active');
                }, 1000);
            }
            
            // Cookie akzeptieren
            acceptCookiesBtn.addEventListener('click', function() {
                localStorage.setItem('cookiesAccepted', 'true');
                localStorage.setItem('cookiesDate', new Date().toISOString());
                cookieBanner.classList.remove('active');
                showNotification('Cookies erfolgreich akzeptiert!');
            });
            
            // Cookie-Einstellungen
            cookieSettingsBtn.addEventListener('click', function() {
                // Hier könnte man ein erweitertes Cookie-Einstellungsfenster öffnen
                // Für jetzt einfach zur Cookie-Seite navigieren
                showLegalPage('cookies');
            });
            
            // Header Scroll Effect
            const header = document.getElementById('main-header');
            window.addEventListener('scroll', function() {
                if (window.scrollY > 100) {
                    header.classList.add('scrolled');
                } else {
                    header.classList.remove('scrolled');
                }
            });

            // Mobile Menu Toggle
            const mobileMenuToggle = document.getElementById('mobile-menu-toggle');
            const mainNav = document.getElementById('main-nav');
            
            mobileMenuToggle.addEventListener('click', function() {
                mainNav.classList.toggle('active');
                const icon = mobileMenuToggle.querySelector('i');
                if (mainNav.classList.contains('active')) {
                    icon.classList.remove('fa-bars');
                    icon.classList.add('fa-times');
                } else {
                    icon.classList.remove('fa-times');
                    icon.classList.add('fa-bars');
                }
            });

            // Smooth Scroll für Navigation
            document.querySelectorAll('nav a, .footer-links a').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href');
                    
                    // Prüfen ob es sich um eine rechtliche Seite handelt
                    if (targetId.startsWith('#')) {
                        const pageId = targetId.substring(1);
                        const legalPages = ['impressum', 'datenschutz', 'agb', 'cookies'];
                        
                        if (legalPages.includes(pageId)) {
                            showLegalPage(pageId);
                            return;
                        }
                    }
                    
                    const targetElement = document.querySelector(targetId);
                    
                    if (targetElement) {
                        const headerHeight = header.offsetHeight;
                        const targetPosition = targetElement.offsetTop - headerHeight;
                        
                        window.scrollTo({
                            top: targetPosition,
                            behavior: 'smooth'
                        });

                        // Mobile Menu schließen
                        if (mainNav.classList.contains('active')) {
                            mainNav.classList.remove('active');
                            mobileMenuToggle.querySelector('i').classList.replace('fa-times', 'fa-bars');
                        }
                    }
                });
            });

            // Funktion zum Anzeigen rechtlicher Seiten
            function showLegalPage(pageId) {
                // Alle rechtlichen Seiten verstecken
                document.querySelectorAll('.legal-page').forEach(page => {
                    page.style.display = 'none';
                });
                
                // Hauptinhalt verstecken
                document.querySelectorAll('section:not(.legal-page)').forEach(section => {
                    section.style.display = 'none';
                });
                
                // Footer verstecken
                document.querySelector('footer').style.display = 'none';
                
                // Gewünschte Seite anzeigen
                const legalPage = document.getElementById(pageId);
                if (legalPage) {
                    legalPage.style.display = 'block';
                    window.scrollTo({
                        top: 0,
                        behavior: 'smooth'
                    });
                }
                
                // Mobile Menu schließen
                if (mainNav.classList.contains('active')) {
                    mainNav.classList.remove('active');
                    mobileMenuToggle.querySelector('i').classList.replace('fa-times', 'fa-bars');
                }
            }
            
            // Zurück zur Startseite Funktion
            document.querySelectorAll('.back-to-home').forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    
                    // Alle rechtlichen Seiten verstecken
                    document.querySelectorAll('.legal-page').forEach(page => {
                        page.style.display = 'none';
                    });
                    
                    // Hauptinhalt anzeigen
                    document.querySelectorAll('section:not(.legal-page)').forEach(section => {
                        section.style.display = 'block';
                    });
                    
                    // Footer anzeigen
                    document.querySelector('footer').style.display = 'block';
                    
                    // Zur Startseite scrollen
                    window.scrollTo({
                        top: 0,
                        behavior: 'smooth'
                    });
                });
            });

            // Aktive Navigation basierend auf Scroll-Position
            const sections = document.querySelectorAll('section:not(.legal-page)');
            const navLinks = document.querySelectorAll('nav a');

            function updateActiveNav() {
                let current = '';
                const headerHeight = header.offsetHeight;
                
                sections.forEach(section => {
                    const sectionTop = section.offsetTop - headerHeight - 100;
                    const sectionHeight = section.clientHeight;
                    if (window.scrollY >= sectionTop && window.scrollY < sectionTop + sectionHeight) {
                        current = section.getAttribute('id');
                    }
                });

                navLinks.forEach(link => {
                    link.classList.remove('active');
                    if (link.getAttribute('href') === '#' + current) {
                        link.classList.add('active');
                    }
                });
            }

            window.addEventListener('scroll', updateActiveNav);

            // Animation on Scroll
            const observerOptions = {
                threshold: 0.1,
                rootMargin: '0px 0px -50px 0px'
            };

            const observer = new IntersectionObserver(function(entries) {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = '1';
                        entry.target.style.transform = 'translateY(0)';
                    }
                });
            }, observerOptions);

            // Beobachte alle Service-Cards und andere Elemente
            document.querySelectorAll('.service-card, .about-content, .gallery-comparison, .contact-method, .platform-card').forEach(el => {
                el.style.opacity = '0';
                el.style.transform = 'translateY(30px)';
                el.style.transition = 'all 0.6s ease-out';
                observer.observe(el);
            });

            // Formular-Handling
            const offerForm = document.getElementById('offer-form');
            if (offerForm) {
                offerForm.addEventListener('submit', function(e) {
                    e.preventDefault();
                    
                    // Hier würde normalerweise die Formular-Daten an einen Server gesendet werden
                    // Für dieses Beispiel zeigen wir nur eine Alert-Box
                    
                    const name = document.getElementById('name').value;
                    const email = document.getElementById('email').value;
                    
                    // Erfolgsmeldung anzeigen
                    showNotification(`Vielen Dank ${name}! Wir haben Ihre Anfrage erhalten und melden uns innerhalb von 24 Stunden unter ${email}.`);
                    
                    // Formular zurücksetzen
                    offerForm.reset();
                });
            }
            
            // Benachrichtigung anzeigen
            function showNotification(message) {
                const notification = document.createElement('div');
                notification.style.cssText = `
                    position: fixed;
                    top: 20px;
                    right: 20px;
                    background: linear-gradient(135deg, var(--accent) 0%, var(--accent-dark) 100%);
                    color: white;
                    padding: 15px 25px;
                    border-radius: 8px;
                    box-shadow: 0 5px 15px rgba(0,0,0,0.2);
                    z-index: 10000;
                    animation: slideIn 0.3s ease;
                `;
                
                notification.innerHTML = `
                    <div style="display: flex; align-items: center; gap: 10px;">
                        <i class="fas fa-check-circle"></i>
                        <span>${message}</span>
                    </div>
                `;
                
                document.body.appendChild(notification);
                
                // Nach 5 Sekunden entfernen
                setTimeout(() => {
                    notification.style.animation = 'slideOut 0.3s ease';
                    setTimeout(() => {
                        notification.remove();
                    }, 300);
                }, 5000);
            }
            
            // CSS für Animationen hinzufügen
            const style = document.createElement('style');
            style.textContent = `
                @keyframes slideIn {
                    from { transform: translateX(100%); opacity: 0; }
                    to { transform: translateX(0); opacity: 1; }
                }
                
                @keyframes slideOut {
                    from { transform: translateX(0); opacity: 1; }
                    to { transform: translateX(100%); opacity: 0; }
                }
            `;
            document.head.appendChild(style);
        });
    </script>
</body>
</html>>
