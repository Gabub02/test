<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blitzblank Kassel | Premium Gebäudereinigung & Unterhaltsreinigung</title>
    <meta name="description" content="Professionelle Gebäudereinigung in Kassel - Praxisreinigung, Büroreinigung, Bauendreinigung, Fensterreinigung. Jetzt kostenloses Angebot anfordern!">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #0056b3;
            --primary-dark: #004494;
            --secondary: #e6f2ff;
            --accent: #ff7b00;
            --accent-dark: #e66d00;
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
            width: 42px;
            height: 42px;
            background: linear-gradient(135deg, var(--accent) 0%, var(--accent-dark) 100%);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 700;
            font-size: 1.2em;
            box-shadow: 0 4px 12px rgba(255, 123, 0, 0.3);
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

        .phone-link {
            display: flex;
            align-items: center;
            gap: 8px;
            color: var(--white);
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1em;
            transition: var(--transition);
        }

        .phone-link:hover {
            color: var(--accent);
            transform: translateY(-1px);
        }

        .phone-icon {
            background: var(--accent);
            width: 36px;
            height: 36px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: var(--transition);
        }

        .phone-link:hover .phone-icon {
            background: var(--accent-dark);
            transform: scale(1.1);
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
                rgba(0, 84, 179, 0.92) 0%, 
                rgba(0, 40, 85, 0.95) 100%),
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
            box-shadow: 0 4px 15px rgba(255, 123, 0, 0.3);
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
            box-shadow: 0 6px 20px rgba(255, 123, 0, 0.4);
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
            box-shadow: 0 10px 30px rgba(255, 123, 0, 0.6);
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
            border: 1px solid rgba(0, 86, 179, 0.1);
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

        .about-stats {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-top: 30px;
        }

        .about-stat {
            text-align: center;
            padding: 25px;
            background: var(--light);
            border-radius: var(--border-radius);
            border: 1px solid rgba(0, 0, 0, 0.05);
        }

        .about-stat-number {
            display: block;
            font-size: 2.5em;
            font-weight: 800;
            color: var(--primary);
            line-height: 1;
            margin-bottom: 5px;
        }

        .about-stat-label {
            font-size: 0.9em;
            color: var(--text-light);
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
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-top: 50px;
        }

        .gallery-item {
            position: relative;
            height: 280px;
            border-radius: var(--border-radius);
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            cursor: pointer;
        }

        .gallery-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, var(--primary) 0%, transparent 100%);
            opacity: 0;
            transition: var(--transition);
            z-index: 1;
        }

        .gallery-item::after {
            content: '🔍 Vergrößern';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) scale(0.8);
            color: white;
            font-weight: 600;
            opacity: 0;
            transition: var(--transition);
            z-index: 2;
        }

        .gallery-item:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-lg);
        }

        .gallery-item:hover::before {
            opacity: 0.8;
        }

        .gallery-item:hover::after {
            opacity: 1;
            transform: translate(-50%, -50%) scale(1);
        }

        .gallery-placeholder {
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, var(--primary) 0%, var(--dark) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: rgba(255, 255, 255, 0.9);
            font-weight: 600;
            font-size: 1.1em;
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

        .cta-box {
            background: rgba(255, 255, 255, 0.05);
            padding: 40px;
            border-radius: var(--border-radius);
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            text-align: center;
        }

        .cta-box h3 {
            font-size: 1.6em;
            font-weight: 700;
            margin-bottom: 15px;
            color: var(--white);
        }

        .cta-box p {
            color: rgba(255, 255, 255, 0.8);
            margin-bottom: 25px;
            line-height: 1.6;
        }

        .guarantee-badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: rgba(255, 123, 0, 0.1);
            color: var(--accent);
            padding: 10px 20px;
            border-radius: 50px;
            font-weight: 600;
            margin-top: 20px;
            border: 1px solid rgba(255, 123, 0, 0.2);
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
        }
    </style>
</head>
<body>
    <!-- ===== ULTRA PREMIUM HEADER ===== -->
    <header id="main-header">
        <div class="container header-container">
            <a href="#home" class="logo">
                <div class="logo-icon">BB</div>
                <div>
                    <div class="logo-text">Blitz<span>blank</span> Kassel</div>
                    <div class="logo-tagline">PREMIUM GEBÄUDEREINIGUNG</div>
                </div>
            </a>

            <nav id="main-nav">
                <ul>
                    <li><a href="#home" class="active">Start</a></li>
                    <li><a href="#services">Leistungen</a></li>
                    <li><a href="#about">Über Uns</a></li>
                    <li><a href="#gallery">Referenzen</a></li>
                    <li><a href="#contact">Kontakt</a></li>
                </ul>
            </nav>

            <div class="header-cta">
                <a href="tel:+4915151816181" class="phone-link">
                    <div class="phone-icon">
                        <i class="fas fa-phone"></i>
                    </div>
                    +49 1515 1816181
                </a>
            </div>

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
                
                <h1>Mehr als nur sauber.<br>Ein perfekter erster Eindruck.</h1>
                
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
                <h2 class="section-title">Ihr Spezialist für perfekte Sauberkeit</h2>
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
                    
                    <div class="service-price">Ab 0,90 €/m² pro Reinigung</div>
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
                        <li><i class="fas fa-check"></i> Teppich- und Bodenpflege</li>
                        <li><i class="fas fa-check"></i> Küchen- und Sanitärreinigung</li>
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
                    
                    <div class="service-price">Ab 3,50 €/m² (pauschal)</div>
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
                        <li><i class="fas fa-check"></i> Hochhausreinigung</li>
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
                    <div class="about-stats">
                        <div class="about-stat">
                            <span class="about-stat-number">4</span>
                            <span class="about-stat-label">Erfahrene Profis</span>
                        </div>
                        <div class="about-stat">
                            <span class="about-stat-number">2</span>
                            <span class="about-stat-label">Eingespielte Teams</span>
                        </div>
                        <div class="about-stat">
                            <span class="about-stat-number">24/7</span>
                            <span class="about-stat-label">Erreichbarkeit</span>
                        </div>
                        <div class="about-stat">
                            <span class="about-stat-number">100%</span>
                            <span class="about-stat-label">Kundenzufriedenheit</span>
                        </div>
                    </div>
                </div>

                <div class="about-text">
                    <div class="section-badge">Warum Blitzblank Kassel?</div>
                    <h2>Ihr Partner für makellose Sauberkeit</h2>
                    
                    <p>Wir sind <strong>Blitzblank Kassel</strong> – ein eingespieltes Team von vier leidenschaftlichen Reinigungsexperten. Während andere hetzen, nehmen wir uns die Zeit, die es braucht, um jedes Detail perfekt zu machen.</p>
                    
                    <p>Unsere Stärke ist die Zuverlässigkeit. Als Team von zwei eingespielten Zweier-Teams sind wir flexibel und können Ihnen auch bei kurzfristigen oder großen Projekten garantieren, dass die Arbeit termingerecht und in höchster Qualität erledigt wird.</p>

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
                <div class="gallery-item">
                    <div class="gallery-placeholder">
                        <i class="fas fa-clinic-medical"></i>
                        Praxis-Reinigung
                    </div>
                </div>
                <div class="gallery-item">
                    <div class="gallery-placeholder">
                        <i class="fas fa-building"></i>
                        Büro-Reinigung
                    </div>
                </div>
                <div class="gallery-item">
                    <div class="gallery-placeholder">
                        <i class="fas fa-tools"></i>
                        Bauendreinigung
                    </div>
                </div>
                <div class="gallery-item">
                    <div class="gallery-placeholder">
                        <i class="fas fa-window-restore"></i>
                        Fensterreinigung
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== ULTRA PREMIUM CONTACT SECTION ===== -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-header">
                <div class="section-badge">Kontakt aufnehmen</div>
                <h2 class="section-title">Startbereit für makellose Sauberkeit?</h2>
                <p class="section-subtitle">Kontaktieren Sie uns noch heute für ein unverbindliches und transparentes Angebot.</p>
            </div>

            <div class="contact-container">
                <div class="contact-info">
                    <div class="contact-method">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div class="contact-details">
                            <h3>Telefonisch erreichen</h3>
                            <p>Mo-Fr: 8-18 Uhr | Sa: Nach Vereinbarung</p>
                            <a href="tel:+4915151816181" class="contact-link">+49 1515 1816181</a>
                        </div>
                    </div>

                    <div class="contact-method">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div class="contact-details">
                            <h3>Per E-Mail</h3>
                            <p>Antwort innerhalb von 2 Stunden</p>
                            <a href="mailto:info@blitzblank-kassel.de" class="contact-link">info@blitzblank-kassel.de</a>
                        </div>
                    </div>

                    <div class="contact-method">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="contact-details">
                            <h3>Einsatzgebiet</h3>
                            <p>Kassel & Umgebung</p>
                            <p>Bundesweit für Großprojekte</p>
                        </div>
                    </div>

                    <div class="contact-method">
                        <div class="contact-icon">
                            <i class="fas fa-clock"></i>
                        </div>
                        <div class="contact-details">
                            <h3>Notfallservice</h3>
                            <p>24/7 für akute Notfälle</p>
                            <p>Wasserschäden, Einbrüche, etc.</p>
                        </div>
                    </div>
                </div>

                <div class="cta-box">
                    <h3>Angebot in 24 Stunden</h3>
                    <p>Senden Sie uns eine kurze Beschreibung Ihrer Räumlichkeiten und wir lassen Ihnen innerhalb von 24 Stunden ein detailliertes, unverbindliches Angebot zukommen.</p>
                    
                    <a href="mailto:info@blitzblank-kassel.de" class="btn">
                        <i class="fas fa-paper-plane"></i>
                        E-Mail senden
                    </a>

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
                    <div class="logo-text">Blitz<span>blank</span> Kassel</div>
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
                        <li><a href="#contact">Kontakt</a></li>
                        <li><a href="#contact">Anfahrt</a></li>
                        <li><a href="#contact">Karriere</a></li>
                    </ul>
                </div>

                <div class="footer-section">
                    <h3 class="footer-heading">Rechtliches</h3>
                    <ul class="footer-links">
                        <li><a href="#">Impressum</a></li>
                        <li><a href="#">Datenschutz</a></li>
                        <li><a href="#">AGB</a></li>
                        <li><a href="#">Cookies</a></li>
                    </ul>
                </div>
            </div>

            <div class="footer-bottom">
                <p>&copy; 2025 Blitzblank Kassel | Professionelle Gebäudereinigung GmbH | Alle Rechte vorbehalten</p>
            </div>
        </div>
    </footer>

    <script>
        // Premium JavaScript für ultra-smooth Interaktionen
        document.addEventListener('DOMContentLoaded', function() {
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
            document.querySelectorAll('nav a').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href');
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

            // Aktive Navigation basierend auf Scroll-Position
            const sections = document.querySelectorAll('section');
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
            document.querySelectorAll('.service-card, .about-content, .gallery-item, .contact-method').forEach(el => {
                el.style.opacity = '0';
                el.style.transform = 'translateY(30px)';
                el.style.transition = 'all 0.6s ease-out';
                observer.observe(el);
            });
        });
    </script>
</body>
</html>
