<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Cabinet dentaire Dr Oumaima Babas - Chirurgien-dentiste à Marrakech, quartier Akiyoud Gueliz. Soins dentaires de qualité, expertise moderne.">
    <meta name="keywords" content="dentiste Marrakech, chirurgien-dentiste Gueliz, soins dentaires, Dr Oumaima Babas">
    <meta name="author" content="Dr Oumaima Babas">
    <title>Dr Oumaima Babas | Cabinet Dentaire Marrakech</title>
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #0f2b4d;
            --primary-light: #1e4d7c;
            --accent: #3b82f6;
            --accent-light: #7bc5f7;
            --white: #ffffff;
            --light: #f0f9ff;
            --gray: #e2e8f0;
            --text: #334155;
            --text-light: #64748b;
            --instagram: #E4405F;
            --facebook: #1877F2;
            --whatsapp: #25D366;
            --shadow-sm: 0 4px 6px rgba(0,0,0,0.05);
            --shadow-md: 0 10px 25px -5px rgba(0,0,0,0.1);
            --shadow-lg: 0 20px 40px -15px rgba(0,0,0,0.15);
            --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            --header-height: 80px;
        }

        body {
            font-family: 'Segoe UI', 'Poppins', system-ui, sans-serif;
            background-color: var(--light);
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Navigation */
        header {
            background: rgba(15, 43, 77, 0.95);
            backdrop-filter: blur(10px);
            height: var(--header-height);
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 5%;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: var(--shadow-sm);
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            text-decoration: none;
            cursor: pointer;
        }

        .logo-icon {
            font-size: 2rem;
        }

        .logo-text h2 {
            color: var(--white);
            font-size: 1.2rem;
            line-height: 1.2;
        }

        .logo-text span {
            color: var(--accent-light);
            font-size: 0.8rem;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 0.5rem;
            flex-wrap: wrap;
        }

        .nav-links a {
            color: var(--white);
            text-decoration: none;
            padding: 0.5rem 1rem;
            border-radius: 8px;
            font-weight: 500;
            font-size: 0.9rem;
            transition: var(--transition);
            cursor: pointer;
        }

        .nav-links a:hover,
        .nav-links a.active {
            background: rgba(123, 197, 247, 0.2);
            color: var(--accent-light);
        }

        /* Menu Burger */
        .burger {
            display: none;
            cursor: pointer;
            font-size: 1.8rem;
            color: var(--white);
        }

        /* Sections */
        section {
            padding: 80px 10%;
            min-height: 100vh;
            display: none;
            animation: fadeIn 0.5s ease;
        }

        section.active-section {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-light) 100%);
            border-radius: 30px;
            padding: 60px 40px;
            text-align: center;
            color: var(--white);
            margin-bottom: 40px;
        }

        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 15px;
        }

        .hero h1 span {
            color: var(--accent-light);
        }

        .hero .tooth-icon {
            font-size: 4rem;
            margin-bottom: 20px;
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }

        /* Grilles */
        .grid-2,
        .grid-3,
        .grid-4 {
            display: grid;
            gap: 30px;
            margin-top: 30px;
        }

        .grid-2 { grid-template-columns: repeat(auto-fit, minmax(400px, 1fr)); }
        .grid-3 { grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); }
        .grid-4 { grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); }

        /* Cartes */
        .card {
            background: var(--white);
            border-radius: 20px;
            padding: 30px;
            box-shadow: var(--shadow-sm);
            transition: var(--transition);
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-md);
        }

        .card-icon {
            font-size: 3rem;
            margin-bottom: 15px;
        }

        .card h3 {
            color: var(--primary);
            margin-bottom: 15px;
        }

        /* Images SVG personnalisées */
        .dental-svg {
            width: 100%;
            height: auto;
            max-width: 120px;
            margin: 0 auto;
            display: block;
        }

        .cabinet-svg {
            width: 100%;
            height: 200px;
            object-fit: cover;
            background: linear-gradient(135deg, var(--primary), var(--primary-light));
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .svg-icon {
            width: 80px;
            height: 80px;
            margin: 0 auto;
        }

        /* Images dentaires SVG */
        .dental-images {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            margin: 30px 0;
        }

        .dental-img {
            width: 130px;
            height: 130px;
            background: linear-gradient(135deg, var(--white), var(--light));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: var(--shadow-md);
            transition: var(--transition);
            cursor: pointer;
            border: 3px solid var(--accent-light);
        }

        .dental-img svg {
            width: 70px;
            height: 70px;
        }

        .dental-img:hover {
            transform: scale(1.1);
            background: var(--accent-light);
        }

        .dental-img:hover svg path {
            fill: white;
        }

        /* Cabinet showcase */
        .cabinet-showcase {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin: 30px 0;
        }

        .cabinet-card {
            background: var(--white);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: var(--shadow-sm);
            transition: var(--transition);
            text-align: center;
        }

        .cabinet-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-md);
        }

        .cabinet-card .cabinet-svg {
            background: linear-gradient(135deg, var(--primary), var(--primary-light));
            padding: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .cabinet-card .cabinet-svg svg {
            width: 120px;
            height: 120px;
        }

        .cabinet-card .info {
            padding: 20px;
        }

        .cabinet-card .info h4 {
            color: var(--primary);
            margin-bottom: 10px;
        }

        /* Carte de localisation */
        .location-card {
            background: var(--white);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: var(--shadow-md);
        }

        .map-container {
            height: 300px;
            background: #e2e8f0;
        }

        .location-info {
            padding: 30px;
        }

        .address-highlight {
            background: linear-gradient(135deg, var(--primary), var(--primary-light));
            color: white;
            padding: 20px;
            border-radius: 15px;
            margin: 20px 0;
            text-align: center;
        }

        .address-highlight p {
            font-size: 1.2rem;
            margin: 10px 0;
        }

        .address-code {
            font-family: monospace;
            font-size: 1.5rem;
            font-weight: bold;
            letter-spacing: 2px;
            background: rgba(255,255,255,0.2);
            display: inline-block;
            padding: 5px 15px;
            border-radius: 10px;
            margin-top: 10px;
        }

        /* Tarifs */
        .price-table {
            width: 100%;
            border-collapse: collapse;
            background: var(--white);
            border-radius: 20px;
            overflow: hidden;
        }

        .price-table th,
        .price-table td {
            padding: 15px 20px;
            text-align: left;
            border-bottom: 1px solid var(--gray);
        }

        .price-table th {
            background: var(--primary);
            color: var(--white);
            font-weight: 600;
        }

        .price-table tr:hover {
            background: var(--light);
        }

        .price {
            color: var(--accent);
            font-weight: bold;
        }

        /* Formulaire */
        .contact-form {
            background: var(--white);
            padding: 40px;
            border-radius: 20px;
            box-shadow: var(--shadow-md);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 12px 15px;
            border: 2px solid var(--gray);
            border-radius: 10px;
            font-size: 1rem;
            transition: var(--transition);
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--accent);
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            background: var(--accent);
            color: var(--white);
            border: none;
            border-radius: 50px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            text-decoration: none;
        }

        .btn:hover {
            background: var(--primary-light);
            transform: translateY(-2px);
        }

        /* Réseaux sociaux */
        .social-card {
            display: flex;
            align-items: center;
            gap: 15px;
            padding: 15px 20px;
            background: var(--white);
            border-radius: 15px;
            margin-bottom: 15px;
            transition: var(--transition);
            text-decoration: none;
            color: var(--text);
        }

        .social-card:hover {
            transform: translateX(5px);
            box-shadow: var(--shadow-sm);
        }

        .social-icon {
            width: 50px;
            height: 50px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            color: white;
        }

        .social-icon.instagram { background: var(--instagram); }
        .social-icon.facebook { background: var(--facebook); }
        .social-icon.whatsapp { background: var(--whatsapp); }

        .social-info h4 {
            margin-bottom: 5px;
            color: var(--primary);
        }

        .social-info p {
            color: var(--text-light);
            font-size: 0.85rem;
        }

        /* Footer */
        footer {
            background: var(--primary);
            color: var(--white);
            padding: 40px 10% 20px;
            margin-top: 60px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 30px;
        }

        .footer-grid h4 {
            margin-bottom: 15px;
            color: var(--accent-light);
        }

        .footer-social {
            display: flex;
            gap: 15px;
            margin-top: 15px;
        }

        .footer-social a {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-decoration: none;
            transition: var(--transition);
            font-size: 1.2rem;
        }

        .footer-social a.instagram { background: var(--instagram); }
        .footer-social a.facebook { background: var(--facebook); }
        .footer-social a.whatsapp { background: var(--whatsapp); }

        .footer-social a:hover {
            transform: translateY(-3px);
            opacity: 0.9;
        }

        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
        }

        /* Horaires */
        .hours-card {
            background: linear-gradient(135deg, var(--primary), var(--primary-light));
            color: white;
        }

        .hours-card .day {
            display: flex;
            justify-content: space-between;
            padding: 10px 0;
            border-bottom: 1px solid rgba(255,255,255,0.2);
        }

        .hours-card .day:last-child {
            border-bottom: none;
        }

        /* Lightbox */
        .lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.9);
            z-index: 2000;
            justify-content: center;
            align-items: center;
            cursor: pointer;
        }

        .lightbox.active {
            display: flex;
        }

        .lightbox-content {
            text-align: center;
            background: white;
            padding: 20px;
            border-radius: 20px;
            max-width: 90%;
            max-height: 90%;
        }

        .lightbox-content svg {
            width: 300px;
            height: 300px;
        }

        .close-lightbox {
            position: absolute;
            top: 20px;
            right: 40px;
            color: white;
            font-size: 40px;
            cursor: pointer;
        }

        .landmark-badge {
            display: inline-block;
            background: var(--accent);
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.8rem;
            margin-top: 10px;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
                flex-direction: column;
                position: absolute;
                top: var(--header-height);
                left: 0;
                width: 100%;
                background: rgba(15, 43, 77, 0.98);
                padding: 20px;
                gap: 10px;
            }
            
            .nav-links.active {
                display: flex;
            }
            
            .burger {
                display: block;
            }
            
            section {
                padding: 60px 5%;
            }
            
            .hero h1 {
                font-size: 1.8rem;
            }
            
            .grid-2 {
                grid-template-columns: 1fr;
            }
        }

        /* Bouton rendez-vous flottant */
        .rdv-float {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: var(--accent);
            color: var(--white);
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            cursor: pointer;
            box-shadow: var(--shadow-lg);
            transition: var(--transition);
            z-index: 99;
            text-decoration: none;
            border: none;
        }

        .rdv-float:hover {
            transform: scale(1.1);
            background: var(--primary-light);
        }

        .phone-link, .email-link {
            color: var(--accent);
            text-decoration: none;
            font-weight: bold;
        }

        .phone-link:hover, .email-link:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>

<header>
    <div class="logo" onclick="showPage('accueil')">
        <div class="logo-icon">🦷</div>
        <div class="logo-text">
            <h2>Dr Oumaima Babas</h2>
            <span>Chirurgien-Dentiste</span>
        </div>
    </div>
    <nav>
        <ul class="nav-links" id="navLinks">
            <li><a onclick="showPage('accueil')">Accueil</a></li>
            <li><a onclick="showPage('cabinet')">Le Cabinet</a></li>
            <li><a onclick="showPage('soins')">Soins & Expertises</a></li>
            <li><a onclick="showPage('premiere-visite')">Première Visite</a></li>
            <li><a onclick="showPage('tarifs')">Tarifs & Remboursement</a></li>
            <li><a onclick="showPage('conseils')">Conseils Santé</a></li>
            <li><a onclick="showPage('plateau-technique')">Plateau Technique</a></li>
            <li><a onclick="showPage('contact')">Infos & Contact</a></li>
        </ul>
    </nav>
    <div class="burger" id="burger">☰</div>
</header>

<main>
    <!-- PAGE 1 - ACCUEIL -->
    <section id="accueil" class="active-section">
        <div class="hero">
            <div class="tooth-icon">🦷</div>
            <h1>Dr <span>Oumaima Babas</span></h1>
            <p>Chirurgien-Dentiste à Marrakech</p>
            <p style="margin-top: 15px;">"Le sourire, notre passion"</p>
            <button class="btn" style="margin-top: 25px;" onclick="showPage('contact')">Prendre rendez-vous</button>
        </div>

        <!-- Images dentaires SVG -->
        <div class="dental-images">
            <div class="dental-img" onclick="openLightbox('tooth')">
                <svg viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M50 15C35 15 25 25 25 40V65C25 75 30 85 40 85C45 85 48 80 50 75C52 80 55 85 60 85C70 85 75 75 75 65V40C75 25 65 15 50 15Z" fill="#3b82f6" stroke="#0f2b4d" stroke-width="2"/>
                    <rect x="40" y="30" width="20" height="25" rx="5" fill="white"/>
                    <line x1="45" y1="35" x2="55" y2="35" stroke="#0f2b4d" stroke-width="2"/>
                    <line x1="45" y1="42" x2="55" y2="42" stroke="#0f2b4d" stroke-width="2"/>
                    <line x1="45" y1="49" x2="55" y2="49" stroke="#0f2b4d" stroke-width="2"/>
                </svg>
            </div>
            <div class="dental-img" onclick="openLightbox('smile')">
                <svg viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <circle cx="50" cy="50" r="40" fill="#7bc5f7" stroke="#0f2b4d" stroke-width="2"/>
                    <circle cx="35" cy="45" r="5" fill="#0f2b4d"/>
                    <circle cx="65" cy="45" r="5" fill="#0f2b4d"/>
                    <path d="M35 65 Q50 80 65 65" stroke="#0f2b4d" stroke-width="3" fill="none" stroke-linecap="round"/>
                </svg>
            </div>
            <div class="dental-img" onclick="openLightbox('star')">
                <svg viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <polygon points="50,10 61,35 90,40 68,60 73,90 50,75 27,90 32,60 10,40 39,35" fill="#fbbf24" stroke="#0f2b4d" stroke-width="2"/>
                    <text x="50" y="65" text-anchor="middle" fill="#0f2b4d" font-size="20" font-weight="bold">★</text>
                </svg>
            </div>
            <div class="dental-img" onclick="openLightbox('heart')">
                <svg viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M50 88L44 82C30 69 20 59 20 47C20 37 28 29 38 29C44 29 48 32 50 36C52 32 56 29 62 29C72 29 80 37 80 47C80 59 70 69 56 82L50 88Z" fill="#ef4444" stroke="#0f2b4d" stroke-width="2"/>
                    <text x="50" y="58" text-anchor="middle" fill="white" font-size="20">🦷</text>
                </svg>
            </div>
        </div>

        <div class="grid-2">
            <div class="card">
                <div class="card-icon">🏆</div>
                <h3>Excellence dentaire</h3>
                <p>Dr Oumaima Babas met son expertise à votre service pour des soins dentaires de qualité, dans un cadre moderne et apaisant.</p>
            </div>
            <div class="card">
                <div class="card-icon">💙</div>
                <h3>Soins personnalisés</h3>
                <p>Chaque patient est unique. Une approche sur mesure, à l'écoute de vos besoins et de vos attentes.</p>
            </div>
            <div class="card">
                <div class="card-icon">📍</div>
                <h3>À Marrakech - Gueliz</h3>
                <p>Notre cabinet est situé au quartier Akiyoud, Gueliz, Marrakech, facilement accessible.</p>
            </div>
            <div class="card">
                <div class="card-icon">📅</div>
                <h3>Disponibilité</h3>
                <p>Consultations du lundi au samedi, avec des créneaux adaptés à votre emploi du temps.</p>
            </div>
        </div>

        <div style="text-align: center; margin-top: 40px;">
            <h3 style="color: var(--primary);">Ils nous font confiance</h3>
            <div class="grid-4" style="margin-top: 20px;">
                <div class="card"><span style="font-size: 2rem;">★★★★★</span><p>Sophie M.</p></div>
                <div class="card"><span style="font-size: 2rem;">★★★★★</span><p>Karim B.</p></div>
                <div class="card"><span style="font-size: 2rem;">★★★★★</span><p>Nadia L.</p></div>
                <div class="card"><span style="font-size: 2rem;">★★★★★</span><p>Youssef R.</p></div>
            </div>
        </div>
    </section>

    <!-- PAGE 2 - LE CABINET -->
    <section id="cabinet">
        <h2 style="color: var(--primary); margin-bottom: 20px;">📍 Notre Cabinet</h2>
        
        <div class="address-highlight">
            <div class="card-icon" style="font-size: 2rem;">📍</div>
            <p><strong>Notre adresse exacte :</strong></p>
            <p style="font-size: 1.3rem;">MX29W5C Essence pour moto Cash</p>
            <p>Quartier Akiyoud, Gueliz, Marrakech</p>
            <div class="address-code">MX29W5C</div>
            <div class="landmark-badge">📍 À côté de la station essence Cash</div>
        </div>

        <!-- Images du cabinet en SVG -->
        <div class="cabinet-showcase">
            <div class="cabinet-card">
                <div class="cabinet-svg">
                    <svg viewBox="0 0 200 150" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <rect x="20" y="40" width="160" height="100" rx="10" fill="#1e4d7c" stroke="white" stroke-width="2"/>
                        <rect x="40" y="60" width="30" height="30" rx="5" fill="#7bc5f7"/>
                        <rect x="80" y="60" width="30" height="30" rx="5" fill="#7bc5f7"/>
                        <rect x="120" y="60" width="30" height="30" rx="5" fill="#7bc5f7"/>
                        <rect x="60" y="100" width="80" height="40" rx="5" fill="#3b82f6"/>
                        <circle cx="100" cy="80" r="15" fill="white"/>
                        <text x="100" y="85" text-anchor="middle" fill="#0f2b4d" font-size="16">🦷</text>
                    </svg>
                </div>
                <div class="info">
                    <h4>Salle de soins moderne</h4>
                    <p>Équipée des dernières technologies dentaires</p>
                </div>
            </div>
            <div class="cabinet-card">
                <div class="cabinet-svg">
                    <svg viewBox="0 0 200 150" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <rect x="20" y="40" width="160" height="100" rx="10" fill="#1e4d7c" stroke="white" stroke-width="2"/>
                        <rect x="30" y="50" width="140" height="80" rx="8" fill="#7bc5f7"/>
                        <circle cx="60" cy="80" r="15" fill="white"/>
                        <circle cx="140" cy="80" r="15" fill="white"/>
                        <text x="60" y="85" text-anchor="middle" fill="#0f2b4d" font-size="14">☕</text>
                        <text x="140" y="85" text-anchor="middle" fill="#0f2b4d" font-size="14">📖</text>
                        <rect x="80" y="110" width="40" height="20" rx="5" fill="#3b82f6"/>
                    </svg>
                </div>
                <div class="info">
                    <h4>Salle d'attente confortable</h4>
                    <p>Un espace apaisant pour vous détendre</p>
                </div>
            </div>
            <div class="cabinet-card">
                <div class="cabinet-svg">
                    <svg viewBox="0 0 200 150" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <rect x="20" y="40" width="160" height="100" rx="10" fill="#1e4d7c" stroke="white" stroke-width="2"/>
                        <circle cx="60" cy="70" r="20" fill="#7bc5f7"/>
                        <circle cx="140" cy="70" r="20" fill="#7bc5f7"/>
                        <rect x="40" y="100" width="120" height="8" rx="4" fill="#3b82f6"/>
                        <text x="60" y="75" text-anchor="middle" fill="white" font-size="18">🔬</text>
                        <text x="140" y="75" text-anchor="middle" fill="white" font-size="18">💻</text>
                    </svg>
                </div>
                <div class="info">
                    <h4>Équipement de pointe</h4>
                    <p>Technologie moderne pour des soins précis</p>
                </div>
            </div>
        </div>

        <div class="location-card">
            <div class="map-container">
                <iframe 
                    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3401.234567890123!2d-8.012345678901234!3d31.63456789012345!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zMzHCsDM4JzA0LjQiTiA4wrAwMCc0NC40Ilc!5e0!3m2!1sfr!2sma!4v1647600000000!5m2!1sfr!2sma" 
                    width="100%" 
                    height="100%" 
                    style="border:0; width:100%; height:100%;" 
                    allowfullscreen="" 
                    loading="lazy">
                </iframe>
            </div>
            <div class="location-info">
                <h3>Comment nous trouver ?</h3>
                <p style="margin: 15px 0;"><strong>📍 Adresse complète :</strong><br>MX29W5C Essence pour moto Cash<br>Quartier Akiyoud, Gueliz, Marrakech</p>
                <p><strong>Point de repère :</strong> À côté de la station essence Cash</p>
                <p>🚗 Parking facile à proximité</p>
                <p>🚌 Accès par bus ligne 1, 8, 14</p>
                <button class="btn" style="margin-top: 20px;" onclick="showPage('contact')">Prendre rendez-vous</button>
            </div>
        </div>

        <div class="grid-2" style="margin-top: 40px;">
            <div class="card hours-card">
                <div class="card-icon">⏰</div>
                <h3 style="color: white;">Horaires d'ouverture</h3>
                <div class="day">
                    <span>Lundi - Vendredi</span>
                    <span><strong>9h00 - 20h00</strong></span>
                </div>
                <div class="day">
                    <span>Samedi</span>
                    <span><strong>8h30 - 13h30</strong></span>
                </div>
                <div class="day">
                    <span>Dimanche</span>
                    <span>Fermé</span>
                </div>
                <p style="margin-top: 15px;"><em>📞 Urgences : Appelez le <a href="tel:+212524434811" style="color: var(--accent-light);">+212 524 434 811</a></em></p>
            </div>
            <div class="card">
                <div class="card-icon">🏥</div>
                <h3>Un cadre moderne et apaisant</h3>
                <p>Notre cabinet a été pensé pour votre confort :</p>
                <ul style="margin-top: 10px; margin-left: 20px;">
                    <li>Salles de soins équipées des dernières technologies</li>
                    <li>Salle d'attente confortable</li>
                    <li>Accessibilité PMR</li>
                    <li>Ambiance relaxante</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- PAGE 3 - SOINS & EXPERTISES -->
    <section id="soins">
        <h2 style="color: var(--primary); margin-bottom: 20px;">Soins & Expertises</h2>
        <p style="margin-bottom: 30px;">Dr Oumaima Babas vous propose une large gamme de soins dentaires de haute qualité.</p>
        
        <div class="grid-3">
            <div class="card">
                <div class="card-icon">🦷</div>
                <h3>Soins conservateurs</h3>
                <p>Traitement des caries, obturations esthétiques, soins dentaires préventifs.</p>
            </div>
            <div class="card">
                <div class="card-icon">✨</div>
                <h3>Dentisterie esthétique</h3>
                <p>Facettes, blanchiment, composites, pour un sourire éclatant.</p>
            </div>
            <div class="card">
                <div class="card-icon">🦷</div>
                <h3>Endodontie</h3>
                <p>Traitement canalaire précis et indolore pour sauver vos dents.</p>
            </div>
            <div class="card">
                <div class="card-icon">👑</div>
                <h3>Prothèses dentaires</h3>
                <p>Couronnes, bridges, prothèses amovibles sur mesure.</p>
            </div>
            <div class="card">
                <div class="card-icon">🦷</div>
                <h3>Chirurgie orale</h3>
                <p>Extractions, dents de sagesse, soins sous microscope.</p>
            </div>
            <div class="card">
                <div class="card-icon">😁</div>
                <h3>Orthodontie</h3>
                <p>Gouttières invisibles, aligneurs, pour adultes et enfants.</p>
            </div>
            <div class="card">
                <div class="card-icon">🦷</div>
                <h3>Parodontologie</h3>
                <p>Traitement des gencives, détartrage, surfaçage radiculaire.</p>
            </div>
            <div class="card">
                <div class="card-icon">👶</div>
                <h3>Pédodontie</h3>
                <p>Soins dentaires pour enfants, approche douce et pédagogique.</p>
            </div>
            <div class="card">
                <div class="card-icon">🦷</div>
                <h3>Prévention</h3>
                <p>Bilans réguliers, détartrage, conseils personnalisés.</p>
            </div>
        </div>
    </section>

    <!-- PAGE 4 - PREMIÈRE VISITE -->
    <section id="premiere-visite">
        <h2 style="color: var(--primary); margin-bottom: 20px;">Votre Première Visite</h2>
        <div class="grid-2">
            <div class="card">
                <div class="card-icon">📋</div>
                <h3>Déroulement de la consultation</h3>
                <ol style="margin-left: 20px; margin-top: 10px;">
                    <li>Accueil et prise de contact</li>
                    <li>Questionnaire médical</li>
                    <li>Examen clinique complet</li>
                    <li>Radiographies si nécessaire</li>
                    <li>Diagnostic et plan de traitement</li>
                    <li>Explication et devis détaillé</li>
                </ol>
            </div>
            <div class="card">
                <div class="card-icon">📝</div>
                <h3>Documents à apporter</h3>
                <ul style="margin-left: 20px; margin-top: 10px;">
                    <li>Carte d'identité</li>
                    <li>Carte vitale / Mutuelle</li>
                    <li>Radiographies récentes si disponibles</li>
                    <li>Liste des traitements médicaux en cours</li>
                </ul>
            </div>
        </div>

        <div class="card" style="margin-top: 30px; background: var(--primary); color: white;">
            <h3 style="color: var(--accent-light);">Pourquoi choisir Dr Oumaima Babas ?</h3>
            <div class="grid-3" style="margin-top: 20px;">
                <div>✓ 10+ ans d'expérience</div>
                <div>✓ Équipement de dernière génération</div>
                <div>✓ Approche personnalisée</div>
                <div>✓ Soins indolores</div>
                <div>✓ Tarifs transparents</div>
                <div>✓ Suivi post-traitement</div>
            </div>
        </div>
    </section>

    <!-- PAGE 5 - TARIFS & REMBOURSEMENT -->
    <section id="tarifs">
        <h2 style="color: var(--primary); margin-bottom: 20px;">Tarifs & Remboursement</h2>
        <p style="margin-bottom: 20px;">Des prix transparents et adaptés à tous les budgets. Nos tarifs sont indicatifs et peuvent varier selon la complexité du soin.</p>
        
        <table class="price-table">
            <thead>
                <tr><th>Soin</th><th>Tarif (TTC)</th><th>Remboursement*</th></tr>
            </thead>
            <tbody>
                <tr><td>Consultation + Détartrage</td><td class="price">500 DH</td><td>Jusqu'à 70%</td〉
                <tr><td>Obturation (plombage)</td><td class="price">400 - 600 DH</td><td>Jusqu'à 70%</td〉
                <tr><td>Extraction dentaire</td><td class="price">300 - 800 DH</td><td>Jusqu'à 70%</td〉
                <tr><td>Traitement canalaire</td><td class="price">800 - 1500 DH</td><td>Jusqu'à 70%</td〉
                <tr><td>Couronne céramique</td><td class="price">2500 - 4000 DH</td><td>Jusqu'à 50%</td〉
                <tr><td>Facette dentaire</td><td class="price">3000 - 5000 DH</td><td>Selon mutuelle</td〉
                <tr><td>Blanchiment dentaire</td><td class="price">2500 DH</td><td>Non remboursé</td〉
                <tr><td>Gouttières orthodontiques</td><td class="price">15000 - 25000 DH</td><td>Selon mutuelle</td〉
            </tbody>
        </table>
        <p style="margin-top: 15px; font-size: 0.9rem;">* Remboursement selon votre mutuelle. Nous acceptons toutes les cartes de mutuelle.</p>
        <button class="btn" style="margin-top: 20px;" onclick="showPage('contact')">Demander un devis personnalisé</button>
    </section>

    <!-- PAGE 6 - CONSEILS SANTÉ -->
    <section id="conseils">
        <h2 style="color: var(--primary); margin-bottom: 20px;">Conseils Santé</h2>
        <div class="grid-2">
            <div class="card">
                <div class="card-icon">🪥</div>
                <h3>Bien se brosser les dents</h3>
                <p>Brossez-vous 2 fois par jour pendant 2 minutes. Utilisez un dentifrice fluoré et changez votre brosse à dents tous les 3 mois.</p>
            </div>
            <div class="card">
                <div class="card-icon">🧵</div>
                <h3>Utiliser du fil dentaire</h3>
                <p>Le fil dentaire élimine la plaque entre les dents où la brosse n'accède pas. À utiliser 1 fois par jour.</p>
            </div>
            <div class="card">
                <div class="card-icon">🍎</div>
                <h3>Alimentation équilibrée</h3>
                <p>Limitez les sucres, privilégiez les fruits, légumes et produits laitiers riches en calcium.</p>
            </div>
            <div class="card">
                <div class="card-icon">📅</div>
                <h3>Visites régulières</h3>
                <p>Consultez votre dentiste tous les 6 mois pour un contrôle et un détartrage professionnel.</p>
            </div>
            <div class="card">
                <div class="card-icon">🚭</div>
                <h3>Arrêter le tabac</h3>
                <p>Le tabac jaunit les dents et augmente les risques de maladies parodontales et de cancer.</p>
            </div>
            <div class="card">
                <div class="card-icon">💧</div>
                <h3>Hydratation</h3>
                <p>Buvez beaucoup d'eau pour favoriser la production de salive, qui protège naturellement vos dents.</p>
            </div>
        </div>
    </section>

    <!-- PAGE 7 - PLATEAU TECHNIQUE -->
    <section id="plateau-technique">
        <h2 style="color: var(--primary); margin-bottom: 20px;">Plateau Technique Moderne</h2>
        <div class="grid-2">
            <div class="card">
                <div class="card-icon">📷</div>
                <h3>Caméra intra-orale</h3>
                <p>Visualisation en temps réel de vos dents pour un diagnostic précis.</p>
            </div>
            <div class="card">
                <div class="card-icon">🩻</div>
                <h3>Radiologie numérique</h3>
                <p>Radiographies à faible dose de radiation, résultats immédiats.</p>
            </div>
            <div class="card">
                <div class="card-icon">🦷</div>
                <h3>Microscope dentaire</h3>
                <p>Précision extrême pour les traitements canalaires.</p>
            </div>
            <div class="card">
                <div class="card-icon">💉</div>
                <h3>Sédation consciente</h3>
                <p>Pour les patients anxieux, soins sans stress.</p>
            </div>
            <div class="card">
                <div class="card-icon">🔬</div>
                <h3>Stérilisation de pointe</h3>
                <p>Autoclave classe B pour une sécurité maximale.</p>
            </div>
            <div class="card">
                <div class="card-icon">💻</div>
                <h3>CFAO dentaire</h3>
                <p>Conception et fabrication de prothèses sur mesure en une séance.</p>
            </div>
        </div>
    </section>

    <!-- PAGE 8 - INFOS & CONTACT -->
    <section id="contact">
        <h2 style="color: var(--primary); margin-bottom: 20px;">Informations & Contact</h2>
        <div class="grid-2">
            <div>
                <div class="card">
                    <div class="card-icon">📍</div>
                    <h3>Adresse</h3>
                    <p><strong>MX29W5C Essence pour moto Cash</strong></p>
                    <p>Quartier Akiyoud, Gueliz, Marrakech</p>
                    <p class="landmark-badge">📍 À côté de la station essence Cash</p>
                </div>
                
                <div class="card">
                    <div class="card-icon">📞</div>
                    <h3>Téléphone</h3>
                    <p><a href="tel:+212524434811" class="phone-link">+212 524 434 811</a></p>
                    <p style="font-size: 0.9rem; margin-top: 5px;">(Urgences : même numéro)</p>
                </div>
                
                <div class="card">
                    <div class="card-icon">✉️</div>
                    <h3>Email</h3>
                    <p><a href="mailto:boumiakhadija72@gmail.com" class="email-link">boumiakhadija72@gmail.com</a></p>
                </div>

                <div class="card">
                    <div class="card-icon">🌐</div>
                    <h3>Suivez-nous</h3>
                    
                    <a href="https://www.instagram.com/boumiakhadija11" target="_blank" class="social-card">
                        <div class="social-icon instagram">📷</div>
                        <div class="social-info">
                            <h4>Instagram</h4>
                            <p>@boumiakhadija11</p>
                        </div>
                    </a>
                    
                    <a href="https://www.facebook.com/boumia.khadija" target="_blank" class="social-card">
                        <div class="social-icon facebook">📘</div>
                        <div class="social-info">
                            <h4>Facebook</h4>
                            <p>Boumia Khadija</p>
                        </div>
                    </a>
                    
                    <a href="https://wa.me/212607623757" target="_blank" class="social-card">
                        <div class="social-icon whatsapp">💬</div>
                        <div class="social-info">
                            <h4>WhatsApp</h4>
                            <p>+212 6 07 62 37 57</p>
                        </div>
                    </a>
                </div>
                
                <div class="card hours-card">
                    <div class="card-icon">⏰</div>
                    <h3 style="color: white;">Horaires</h3>
                    <div class="day">
                        <span>Lundi - Vendredi</span>
                        <span><strong>9h00 - 20h00</strong></span>
                    </div>
                    <div class="day">
                        <span>Samedi</span>
                        <span><strong>8h30 - 13h30</strong></span>
                    </div>
                    <div class="day">
                        <span>Dimanche</span>
                        <span>Fermé</span>
                    </div>
                </div>
            </div>
            
            <div>
                <form class="contact-form" id="contactForm">
                    <h3>Prendre rendez-vous</h3>
                    <div class="form-group">
                        <input type="text" id="nom" placeholder="Nom complet" required>
                    </div>
                    <div class="form-group">
                        <input type="email" id="email" placeholder="Email" required>
                    </div>
                    <div class="form-group">
                        <input type="tel" id="telephone" placeholder="Téléphone" required>
                    </div>
                    <div class="form-group">
                        <select id="motif">
                            <option value="">Motif de consultation</option>
                            <option>Consultation simple</option>
                            <option>Douleur dentaire</option>
                            <option>Détartrage</option>
                            <option>Esthétique dentaire</option>
                            <option>Urgence</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <input type="date" id="date" placeholder="Date souhaitée">
                    </div>
                    <div class="form-group">
                        <textarea id="message" rows="4" placeholder="Message"></textarea>
                    </div>
                    <button type="submit" class="btn">Envoyer la demande</button>
                </form>
            </div>
        </div>
    </section>
</main>

<footer>
    <div class="footer-grid">
        <div>
            <h4>Dr Oumaima Babas</h4>
            <p>Chirurgien-Dentiste<br>Quartier Akiyoud, Gueliz<br>Marrakech</p>
        </div>
        <div>
            <h4>Liens rapides</h4>
            <p><a onclick="showPage('accueil')" style="color: white; cursor: pointer;">Accueil</a></p>
            <p><a onclick="showPage('cabinet')" style="color: white; cursor: pointer;">Le Cabinet</a></p>
            <p><a onclick="showPage('tarifs')" style="color: white; cursor: pointer;">Tarifs</a></p>
            <p><a onclick="showPage('contact')" style="color: white; cursor: pointer;">Contact</a></p>
        </div>
        <div>
            <h4>Contact rapide</h4>
            <p>📞 <a href="tel:+212524434811" style="color: var(--accent-light);">+212 524 434 811</a></p>
            <p>✉️ <a href="mailto:boumiakhadija72@gmail.com" style="color: var(--accent-light);">boumiakhadija72@gmail.com</a></p>
            <p>💬 <a href="https://wa.me/212607623757" target="_blank" style="color: var(--accent-light);">WhatsApp: 06 07 62 37 57</a></p>
        </div>
        <div>
            <h4>Suivez-nous</h4>
            <div class="footer-social">
                <a href="https://www.instagram.com/boumiakhadija11" target="_blank" class="instagram">📷</a>
                <a href="https://www.facebook.com/boumia.khadija" target="_blank" class="facebook">📘</a>
                <a href="https://wa.me/212607623757" target="_blank" class="whatsapp">💬</a>
            </div>
        </div>
    </div>
    <div class="copyright">
        <p>&copy; 2026 Dr Oumaima Babas - Tous droits réservés</p>
    </div>
</footer>

<button class="rdv-float" onclick="showPage('contact')">📅</button>

<!-- Lightbox -->
<div class="lightbox" id="lightbox" onclick="closeLightbox()">
    <span class="close-lightbox">&times;</span>
    <div class="lightbox-content" id="lightboxContent"></div>
</div>

<script>
    // Lightbox functions
    function openLightbox(type) {
        const lightbox = document.getElementById('lightbox');
        const content = document.getElementById('lightboxContent');
        
        let svgHtml = '';
        
        if (type === 'tooth') {
            svgHtml = `<svg width="200" height="200" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M50 15C35 15 25 25 25 40V65C25 75 30 85 40 85C45 85 48 80 50 75C52 80 55 85 60 85C70 85 75 75 75 65V40C75 25 65 15 50 15Z" fill="#3b82f6" stroke="#0f2b4d" stroke-width="2"/>
                <rect x="40" y="30" width="20" height="25" rx="5" fill="white"/>
                <line x1="45" y1="35" x2="55" y2="35" stroke="#0f2b4d" stroke-width="2"/>
                <line x1="45" y1="42" x2="55" y2="42" stroke="#0f2b4d" stroke-width="2"/>
                <line x1="45" y1="49" x2="55" y2="49" stroke="#0f2b4d" stroke-width="2"/>
            </svg>
            <p style="margin-top:15px;"><strong>Soin dentaire de qualité</strong></p>`;
        } else if (type === 'smile') {
            svgHtml = `<svg width="200" height="200" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
                <circle cx="50" cy="50" r="40" fill="#7bc5f7" stroke="#0f2b4d" stroke-width="2"/>
                <circle cx="35" cy="45" r="5" fill="#0f2b4d"/>
                <circle cx="65" cy="45" r="5" fill="#0f2b4d"/>
                <path d="M35 65 Q50 80 65 65" stroke="#0f2b4d" stroke-width="3" fill="none" stroke-linecap="round"/>
            </svg>
            <p style="margin-top:15px;"><strong>Sourire éclatant</strong></p>`;
        } else if (type === 'star') {
            svgHtml = `<svg width="200" height="200" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
                <polygon points="50,10 61,35 90,40 68,60 73,90 50,75 27,90 32,60 10,40 39,35" fill="#fbbf24" stroke="#0f2b4d" stroke-width="2"/>
                <text x="50" y="65" text-anchor="middle" fill="#0f2b4d" font-size="25" font-weight="bold">★</text>
            </svg>
            <p style="margin-top:15px;"><strong>Excellence dentaire</strong></p>`;
        } else if (type === 'heart') {
            svgHtml = `<svg width="200" height="200" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M50 88L44 82C30 69 20 59 20 47C20 37 28 29 38 29C44 29 48 32 50 36C52 32 56 29 62 29C72 29 80 37 80 47C80 59 70 69 56 82L50 88Z" fill="#ef4444" stroke="#0f2b4d" stroke-width="2"/>
                <text x="50" y="58" text-anchor="middle" fill="white" font-size="25">🦷</text>
            </svg>
            <p style="margin-top:15px;"><strong>Soins avec passion</strong></p>`;
        }
        
        content.innerHTML = svgHtml;
        lightbox.classList.add('active');
    }
    
    function closeLightbox() {
        const lightbox = document.getElementById('lightbox');
        lightbox.classList.remove('active');
    }
    
    // Navigation entre pages
    function showPage(pageId) {
        const sections = document.querySelectorAll('section');
        sections.forEach(section => {
            section.classList.remove('active-section');
        });
        
        const activeSection = document.getElementById(pageId);
        if (activeSection) {
            activeSection.classList.add('active-section');
        }
        
        const links = document.querySelectorAll('.nav-links a');
        links.forEach(link => {
            link.classList.remove('active');
            if (link.getAttribute('onclick') === `showPage('${pageId}')`) {
                link.classList.add('active');
            }
        });
        
        window.scrollTo({ top: 0, behavior: 'smooth' });
        
        const navLinksElem = document.getElementById('navLinks');
        navLinksElem.classList.remove('active');
    }
    
    // Menu Burger
    const burger = document.getElementById('burger');
    const navLinksElem = document.getElementById('navLinks');
    
    burger.addEventListener('click', () => {
        navLinksElem.classList.toggle('active');
    });
    
    // Formulaire de contact
    const contactForm = document.getElementById('contactForm');
    if (contactForm) {
        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();
            const nom = document.getElementById('nom').value;
            alert(`✅ Merci ${nom} ! Votre demande a été envoyée à Dr Oumaima Babas.\n\n📞 Vous serez contacté(e) dans les plus brefs délais.`);
            contactForm.reset();
        });
    }
    
    // Initialisation
    showPage('accueil');
</script>
</body>
</html>
