[index.html](https://github.com/user-attachments/files/25326386/index.html)
<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>Vladis P.Plot - Real Estate Construction in the Dominican Republic</title>
<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" rel="stylesheet"/>
<style>
        :root {
            --primary-color: #0056b3;
            --secondary-color: #003366;
            --accent-color: #7ec8e3;
            --light-color: #f8f9fa;
            --dark-color: #343a40;
            --text-color: #333;
            --white: #ffffff;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            color: var(--text-color);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Styles */
        header {
            background-color: var(--white);
            box-shadow: var(--shadow);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            padding: 15px 0;
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 24px;
            font-weight: 700;
            color: var(--primary-color);
            text-decoration: none;
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 30px;
        }

        nav ul li a {
            text-decoration: none;
            color: var(--dark-color);
            font-weight: 500;
            transition: var(--transition);
            position: relative;
        }

        nav ul li a:hover {
            color: var(--primary-color);
        }

        nav ul li a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background: var(--primary-color);
            bottom: -5px;
            left: 0;
            transition: var(--transition);
        }

        nav ul li a:hover::after {
            width: 100%;
        }

        .language-switcher {
            display: flex;
            align-items: center;
        }

        .language-switcher select {
            padding: 5px;
            border: 1px solid #ddd;
            border-radius: 4px;
            margin-left: 10px;
            cursor: pointer;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 24px;
            cursor: pointer;
            color: var(--dark-color);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), url('https://images.unsplash.com/photo-1560518883-ce09059eeffa?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
            height: 100vh;
            display: flex;
            align-items: center;
            text-align: center;
            color: var(--white);
            margin-top: 60px;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
            animation: fadeInDown 1s ease;
        }

        .hero p {
            font-size: 20px;
            margin-bottom: 30px;
            animation: fadeInUp 1s ease;
        }

        .btn {
            display: inline-block;
            background: var(--primary-color);
            color: var(--white);
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
            border: 2px solid var(--primary-color);
            animation: fadeIn 1.5s ease;
        }

        .btn:hover {
            background: transparent;
            color: var(--white);
            border-color: var(--white);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--white);
            margin-left: 15px;
        }

        .btn-outline:hover {
            background: var(--white);
            color: var(--primary-color);
        }

        /* About Section */
        .section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title h2 {
            font-size: 36px;
            color: var(--primary-color);
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            width: 70px;
            height: 3px;
            background: var(--primary-color);
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
        }

        .about-content {
            display: flex;
            align-items: center;
            flex-wrap: wrap;
        }

        .about-text {
            flex: 1;
            min-width: 300px;
            padding-right: 30px;
        }

        .about-image {
            flex: 1;
            min-width: 300px;
        }

        .about-image img {
            width: 100%;
            border-radius: 10px;
            box-shadow: var(--shadow);
        }

        /* Services Section */
        .services {
            background: var(--light-color);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .service-card {
            background: var(--white);
            padding: 30px;
            border-radius: 10px;
            box-shadow: var(--shadow);
            transition: var(--transition);
            text-align: center;
        }

        .service-card:hover {
            transform: translateY(-10px);
        }

        .service-icon {
            font-size: 50px;
            color: var(--primary-color);
            margin-bottom: 20px;
        }

        .service-card h3 {
            margin-bottom: 15px;
            color: var(--secondary-color);
        }

        /* Portfolio Section */
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
        }

        .portfolio-item {
            position: relative;
            overflow: hidden;
            border-radius: 10px;
            height: 250px;
        }

        .portfolio-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }

        .portfolio-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 86, 179, 0.8);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: var(--transition);
            color: var(--white);
            padding: 20px;
            text-align: center;
        }

        .portfolio-item:hover .portfolio-overlay {
            opacity: 1;
        }

        .portfolio-item:hover img {
            transform: scale(1.1);
        }

        /* Testimonials Section */
        .testimonials {
            background: var(--light-color);
        }

        .testimonial-slider {
            max-width: 800px;
            margin: 0 auto;
            position: relative;
        }

        .testimonial {
            background: var(--white);
            padding: 30px;
            border-radius: 10px;
            box-shadow: var(--shadow);
            text-align: center;
            margin: 20px;
        }

        .testimonial img {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            object-fit: cover;
            margin-bottom: 20px;
        }

        .testimonial-text {
            font-style: italic;
            margin-bottom: 20px;
        }

        .testimonial-author {
            font-weight: 700;
            color: var(--primary-color);
        }

        /* Contact Section */
        .contact-container {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
        }

        .contact-info {
            flex: 1;
            min-width: 300px;
        }

        .contact-info h3 {
            margin-bottom: 20px;
            color: var(--primary-color);
        }

        .contact-details {
            margin-bottom: 30px;
        }

        .contact-details p {
            margin-bottom: 10px;
            display: flex;
            align-items: center;
        }

        .contact-details i {
            margin-right: 10px;
            color: var(--primary-color);
        }

        .social-links {
            display: flex;
            gap: 15px;
        }

        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: var(--primary-color);
            color: var(--white);
            border-radius: 50%;
            transition: var(--transition);
        }

        .social-links a:hover {
            background: var(--secondary-color);
            transform: translateY(-3px);
        }

        .contact-form {
            flex: 1;
            min-width: 300px;
            background: var(--light-color);
            padding: 30px;
            border-radius: 10px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: 500;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
        }

        .form-group textarea {
            height: 150px;
        }

        .submit-btn {
            background: var(--primary-color);
            color: var(--white);
            border: none;
            padding: 12px 30px;
            border-radius: 30px;
            cursor: pointer;
            font-weight: 600;
            transition: var(--transition);
        }

        .submit-btn:hover {
            background: var(--secondary-color);
        }

        /* FAQ Section */
        .faq-item {
            margin-bottom: 20px;
            border: 1px solid #ddd;
            border-radius: 5px;
            overflow: hidden;
        }

        .faq-question {
            padding: 15px 20px;
            background: var(--light-color);
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-weight: 600;
        }

        .faq-question:hover {
            background: #e9ecef;
        }

        .faq-answer {
            padding: 0 20px;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease;
        }

        .faq-item.active .faq-answer {
            padding: 20px;
            max-height: 500px;
        }

        /* Footer */
        footer {
            background: var(--secondary-color);
            color: var(--white);
            padding: 50px 0 20px;
        }

        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-bottom: 30px;
        }

        .footer-col h3 {
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }

        .footer-col h3::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 50px;
            height: 2px;
            background: var(--accent-color);
        }

        .footer-col ul {
            list-style: none;
        }

        .footer-col ul li {
            margin-bottom: 10px;
        }

        .footer-col ul li a {
            color: #ddd;
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-col ul li a:hover {
            color: var(--white);
            padding-left: 5px;
        }

        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* WhatsApp Button */
        .whatsapp-btn {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: #25D366;
            color: white;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 30px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
            z-index: 999;
            transition: var(--transition);
            text-decoration: none;
        }

        .whatsapp-btn:hover {
            transform: scale(1.1);
            box-shadow: 0 6px 16px rgba(0, 0, 0, 0.3);
        }

        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Responsive Styles */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 36px;
            }
            .hero p {
                font-size: 18px;
            }
        }

        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }
            nav {
                position: fixed;
                top: 70px;
                left: -100%;
                width: 80%;
                height: calc(100vh - 70px);
                background: var(--white);
                box-shadow: var(--shadow);
                transition: var(--transition);
                padding: 20px;
            }
            nav.active {
                left: 0;
            }
            nav ul {
                flex-direction: column;
            }
            nav ul li {
                margin: 15px 0;
            }
            .hero {
                margin-top: 70px;
                height: auto;
                padding: 100px 0;
            }
            .about-text {
                padding-right: 0;
                margin-bottom: 30px;
            }
            .section {
                padding: 60px 0;
            }
        }

        @media (max-width: 576px) {
            .hero h1 {
                font-size: 28px;
            }
            .hero p {
                font-size: 16px;
            }
            .btn {
                padding: 10px 20px;
                font-size: 14px;
            }
            .section-title h2 {
                font-size: 28px;
            }
        }
    
#turnkey.highlight {
  box-shadow: 0 0 10px 4px rgba(0,123,255,0.6);
  transition: box-shadow 0.3s ease-in-out;
}

#design.highlight {
  box-shadow: 0 0 10px 4px rgba(0,123,255,0.6);
  transition: box-shadow 0.3s ease-in-out;
}

#legal.highlight {
  box-shadow: 0 0 10px 4px rgba(0,123,255,0.6);
  transition: box-shadow 0.3s ease-in-out;
}

#property.highlight {
  box-shadow: 0 0 10px 4px rgba(0,123,255,0.6);
  transition: box-shadow 0.3s ease-in-out;
}

#immigration.highlight {
  box-shadow: 0 0 10px 4px rgba(0,123,255,0.6);
  transition: box-shadow 0.3s ease-in-out;
}

#investment.highlight {
  box-shadow: 0 0 10px 4px rgba(0,123,255,0.6);
  transition: box-shadow 0.3s ease-in-out;
}

html { scroll-behavior: smooth; }</style>
<!-- Injected to apply liquid glass light blue on input fields -->
<style>
input:not([type=checkbox]):not([type=radio]),
select,
textarea {
  background: rgba(126, 200, 227, 0.15); /* light sky blue glass */
  border: 1px solid #7EC8E3;
  transition: border-color 0.2s ease, box-shadow 0.2s ease;
}
input:focus, select:focus, textarea:focus {
  border-color: #7EC8E3;
  box-shadow: 0 0 0 3px rgba(126, 200, 227, 0.45);
}
</style>
<!-- Liquid Glass Gradient for selection buttons -->
<style>
/* Apply gradient blue glass look to any element with bg-[#7ec8e3] class
   except the NEXT button which is bg-blue-600 */
[class*="bg-[#7ec8e3]"] {
  background: linear-gradient(180deg, #cbe7ff 0%, #9fd3ff 100%) !important;
  color: #0f1d31 !important;
  border: 1px solid rgba(159, 211, 255, 0.8);
  backdrop-filter: blur(12px) saturate(180%);
}

[class*="bg-[#7ec8e3]"]:hover {
  background: linear-gradient(180deg, #b5deff 0%, #7ecaff 100%) !important;
}
</style>
<style>
/* === Apple‑style system font stack (San Francisco) === */
body, button, input, select, textarea {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Helvetica, Arial, sans-serif;
}
</style>
<style>
.glass-toast {
  position: fixed;
  top:100px;
  left: 50%;
  transform: translateX(-50%);
  z-index: 9999;
  padding: 12px 24px;
  background: rgba(203, 231, 255, 0.45);
  backdrop-filter: blur(10px);
  border: 1px solid #9FD3FF;
  border-radius: 16px;
  color: #0f172a;
  font-weight: 600;
  box-shadow: 0 4px 20px rgba(0,0,0,0.15);
  opacity: 0;
  transition: opacity 0.3s ease, transform 0.3s ease;
}
.glass-toast.show {
  opacity: 1;
  transform: translateX(-50%) translateY(0);
}
</style>
<!-- === 2025‑06‑15 Dark hero + compact buttons override === -->
<style>
/* Black‑blue hero background */
.hero{
    background:#0f172a !important;           /* dark navy */
}

/* Ensure hero content container is centered and buttons grouped */
.hero .hero-content > div{
    display:flex !important;
    justify-content:center;
    gap:1rem;
    flex-wrap:wrap;
    margin-top:1.5rem;
}

/* Base pill button style */
.hero .btn,
.hero .btn-outline{
    display:inline-flex !important;
    align-items:center;
    justify-content:center;
    font:600 1rem/1 'Inter',sans-serif;
    padding:.75rem 2rem;
    border-radius:9999px;
    transition:all .25s ease;
    white-space:nowrap;
    width:auto !important;
    max-width:18rem !important;
    flex:0 0 auto !important;
}

/* Primary filled */
.hero .btn{
    background:#0d6efd !important;
    color:#fff !important;
    border:2px solid transparent !important;
    box-shadow:0 2px 6px rgba(0,0,0,.25);
}
.hero .btn:hover{
    background:#0b5ed7 !important;
}

/* Secondary outline */
.hero .btn-outline{
    background:transparent !important;
    color:#fff !important;
    border:2px solid #fff !important;
}
.hero .btn-outline:hover{
    background:#fff !important;
    color:#0d6efd !important;
}
</style>

<!-- ===== BEGIN HERO OVERRIDE (2025-06-15 15:18) ===== -->
<style>

/* ===== Global Brand Palette ===== */
:root{
    --brand-primary:#1673ff;      /* фирменный синий */
    --brand-dark:#0f172a;         /* navy‑black */
    --brand-dark-2:#151d2d;
}

/* ===== Hero Section ===== */
.hero{
    position:relative;
    min-height:100vh;
    color:#fff;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    text-align:center;
    padding:4rem 1rem 6rem;
    overflow:hidden;
}

/* — Фоновое фото + мягкий градиент — */
.hero::before{
    content:"";
    position:absolute;
    inset:0;
    background:url('https://images.unsplash.com/photo-1600585154351-537c3b5e292d?auto=format&fit=crop&w=1920&q=80') center/cover no-repeat;
    filter:brightness(.35) saturate(.8);
    z-index:-2;
}
.hero::after{
    content:"";
    position:absolute;
    inset:0;
    background:radial-gradient(ellipse at top,rgba(34,44,66,.6) 0%,rgba(15,23,42,.9) 60%,rgba(15,23,42,1) 100%);
    z-index:-1;
}

/* ===== Content ===== */
.hero h1{
    font-size:clamp(2.25rem,5vw,3.5rem);
    font-weight:700;
    letter-spacing:-.02em;
    line-height:1.15;
    max-width:900px;
    margin-inline:auto;
}
.hero p{
    max-width:540px;
    font-size:clamp(1rem,2.2vw,1.25rem);
    opacity:.9;
    margin:1.25rem auto 2.75rem;
}

/* ===== Call‑to‑Action Buttons ===== */
.hero-actions{
    display:flex;
    gap:1rem;
    flex-wrap:wrap;
    justify-content:center;
    max-width:420px;
}
.btn{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    padding:.9rem 2.25rem;
    font-weight:600;
    font-size:1rem;
    border-radius:9999px;
    white-space:nowrap;
    transition:all .25s cubic-bezier(.4,0,.2,1);
    transform:translateY(0);
}
.btn-primary{
    background:var(--brand-primary);
    color:#fff;
    border:2px solid transparent;
    box-shadow:0 3px 6px rgba(0,0,0,.3);
}
.btn-primary:hover{
    transform:translateY(-2px) scale(1.03);
    box-shadow:0 8px 16px rgba(0,0,0,.45);
}
.btn-outline{
    background:transparent;
    color:#fff;
    border:2px solid #fff;
}
.btn-outline:hover{
    background:#fff;
    color:var(--brand-primary);
    transform:translateY(-2px) scale(1.03);
}

/* ===== Decorative Wave Separator ===== */
.wave{
    position:absolute;
    bottom:-1px;
    left:0;
    width:100%;
    height:120px;
    background:url('data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTYwMCIgaGVpZ2h0PSIxMjAiIHZpZXdCb3g9IjAgMCAxNjAwIDEyMCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cGF0aCBkPSJNMCAwaDE2MDB2MTAwYy0zNTAgMzAtNzAwIDgwLTEwMDAgODBzLTY1MC0xMC0xMDAwLTgwdjEwMEgwVjB6IiBmaWxsPSIjZmZmIiBmaWxsLW9wYWNpdHk9IjEuMDUiLz48L3N2Zz4=') bottom center/cover no-repeat;
    transform:scaleY(-1);
    z-index:-1;
}

/* ===== Next section placeholder ===== */
#next{
    background:#fff;
    padding:4rem 1.5rem;
}
#next h2{
    font-size:2rem;
    font-weight:600;
    text-align:center;
    color:#1e293b;
}

</style>
<!-- ===== END HERO OVERRIDE ===== -->

<style>
/* Equal width for hero CTA buttons */
.hero-actions .btn{
    width:240px !important;
    height:56px !important;
    display:inline-flex;
    align-items:center;
    justify-content:center;
    white-space:nowrap;
    box-sizing:border-box;
    font-size:18px;
}

/* make outline button visually match filled by moving border inwards */
.hero-actions .btn-outline{
    border-width:2px !important;
    box-shadow:inset 0 0 0 2px #ffffff;
}
</style>

</head>
<body>
<!-- Header -->
<header>
<div class="container header-container">
<a class="logo" href="#home"><img alt="Vladis Logo" src="vladis_main_logo.png" style="height:40px;"/></a>
<button class="mobile-menu-btn">
<i class="fas fa-bars"></i>
</button>
<nav>
<button class="lg:hidden text-gray-800 focus:outline-none" id="mobile-menu-btn">
<svg class="h-8 w-8" fill="none" stroke="currentColor" viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
<path d="M4 6h16M4 12h16M4 18h16" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"></path>
</svg>
</button>
<ul>
<li><a href="#home">Home</a></li>
<li><a href="#about">About</a></li>
<li><a href="#services">Services</a></li>
<li><a href="#portfolio">Portfolio</a></li>
<li><a href="#contact">Contact</a></li>
<li>
<div class="language-switcher">
<i class="fas fa-globe"></i>
<select id="language-selector">
<option value="en">🇬🇧 English</option>
<option value="es">🇪🇸 Español</option>
<option value="ru">🇷🇺 Русский</option>
</select>
</div>
</li>
</ul>
</nav>
</div>
</header>
<!-- Hero Section -->
<section class="hero" id="home">
  <h1 id="hero-title">Real Estate Construction in Sosúa – Cabarete</h1>
  <p id="hero-subtitle">
    Over 17 years of experience developing unique real‑estate projects in Sosúa and Cabarete, Dominican Republic.
  </p>

  <div class="hero-actions">
    <a href="#contact" class="btn btn-primary cta-contact">Contact Us</a>
    <a href="#portfolio" class="btn btn-outline cta-projects">Our Projects</a>
  </div>

  <div aria-hidden="true" class="wave"></div>
</section>
<!-- About Section -->
<section class="section" id="about">
<div class="container max-w-screen-xl mx-auto px-4 sm:px-6 lg:px-8">
<div class="section-title">
<h2 class="lang-en">About Us</h2>
<h2 class="lang-es" style="display:none">Sobre Nosotros</h2>
<h2 class="lang-ru" style="display:none">О компании</h2>
</div>
<div class="about-content flex flex-col lg:flex-row gap-10 items-center">
<div class="about-text">
<p class="lang-en">Founded in 2007 by Vladis P. Plot, Homeinvestor has become a trusted partner in the construction and management of luxury real estate in the Dominican Republic.</p>
<p class="lang-es" style="display:none">Vladis P. Plot fundó Homeinvestor en 2007 y, desde entonces, la empresa se ha consolidado como un socio confiable en la construcción y gestión de bienes raíces de lujo en la República Dominicana.</p>
<p class="lang-ru" style="display:none">В 2007 году Владис П. Плот основал компанию Homeinvestor, которая с тех пор зарекомендовала себя как надёжный партнёр в строительстве и управлении элитной недвижимостью в Доминиканской Республике.</p>
<p class="lang-en">Our internationally experienced team has delivered numerous successful projects, including premium-class villas and residential complexes.</p>
<p class="lang-es" style="display:none">Nuestro equipo de profesionales, con experiencia internacional, ha completado numerosos proyectos exitosos, incluidas villas de clase premium y complejos residenciales.</p>
<p class="lang-ru" style="display:none">Наша команда профессионалов реализовала множество успешных проектов, включая виллы премиум-класса и жилые комплексы.</p>
<p class="lang-en">We provide an individual approach to every client, ensuring top-quality construction, full transparency throughout all processes, and competitive pricing.</p>
<p class="lang-es" style="display:none">Ofrecemos un enfoque individual para cada cliente, garantizando una construcción de alta calidad, total transparencia en todos los procesos y precios competitivos.</p>
<p class="lang-ru" style="display:none">Мы предлагаем индивидуальный подход к каждому клиенту, гарантируя высокое качество строительства, прозрачность всех процессов и конкурентоспособные цены.</p>
</div>
<div class="about-image">
<img alt="About Us" src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?ixlib=rb-1.2.1&amp;auto=format&amp;fit=crop&amp;w=1350&amp;q=80"/>
</div>
</div>
</div>
</section>
<!-- Services Section -->
<section class="section services" id="services">
<div class="container max-w-screen-xl mx-auto px-4 sm:px-6 lg:px-8">
<div class="section-title">
<h2 class="lang-en">Our Services</h2>
<h2 class="lang-es" style="display:none">Nuestros Servicios</h2>
<h2 class="lang-ru" style="display:none">Наши услуги</h2>
</div>
<div class="services-grid">
<div class="service-card" id="turnkey">
<div class="service-icon">
<i class="fas fa-home"></i>
</div>
<h3 class="lang-en">Turnkey Construction</h3>
<h3 class="lang-es" style="display:none">Construcción Llave en Mano</h3>
<h3 class="lang-ru" style="display:none">Строительство "под ключ"</h3>
<p class="lang-en">Full cycle of construction of villas and apartments from design to handover with finishing.</p>
<p class="lang-es" style="display:none">Ciclo completo de construcción de villas y apartamentos desde el diseño hasta la entrega con acabados.</p>
<p class="lang-ru" style="display:none">Полный цикл строительства вилл и апартаментов от проектирования до сдачи объекта с отделкой.</p>
</div>
<div class="service-card" id="design">
<div class="service-icon">
<i class="fas fa-drafting-compass"></i>
</div>
<h3 class="lang-en">Architectural Design</h3>
<h3 class="lang-es" style="display:none">Diseño Arquitectónico</h3>
<h3 class="lang-ru" style="display:none">Архитектурное проектирование</h3>
<p class="lang-en">Creation of unique architectural solutions with 3D visualization of the future project.</p>
<p class="lang-es" style="display:none">Creación de soluciones arquitectónicas únicas con visualización 3D del proyecto futuro.</p>
<p class="lang-ru" style="display:none">Создание уникальных архитектурных решений с 3D-визуализацией будущего проекта.</p>
</div>
<div class="service-card" id="legal">
<div class="service-icon">
<i class="fas fa-file-contract"></i>
</div>
<h3 class="lang-en">Legal Support</h3>
<h3 class="lang-es" style="display:none">Asesoría Legal</h3>
<h3 class="lang-ru" style="display:none">Юридическое сопровождение</h3>
<p class="lang-en">Full range of legal services, including property registration and obtaining permits.</p>
<p class="lang-es" style="display:none">Servicios legales completos, incluyendo registro de propiedad y obtención de permisos.</p>
<p class="lang-ru" style="display:none">Полный комплекс юридических услуг, включая оформление собственности и получение разрешений.</p>
</div>
<div class="service-card" id="immigration">
<div class="service-icon">
<i class="fas fa-passport"></i>
</div>
<h3 class="lang-en">Immigration Issues</h3>
<h3 class="lang-es" style="display:none">Temas Migratorios</h3>
<h3 class="lang-ru" style="display:none">Иммиграционные вопросы</h3>
<p class="lang-en">Consultations and assistance in processing residence visas and Dominican Republic citizenship.</p>
<p class="lang-es" style="display:none">Consultas y asistencia en el procesamiento de visas de residencia y ciudadanía dominicana.</p>
<p class="lang-ru" style="display:none">Консультации и помощь в оформлении резидентских виз и гражданства Доминиканской Республики.</p>
</div>
<div class="service-card" id="property">
<div class="service-icon">
<i class="fas fa-handshake"></i>
</div>
<h3 class="lang-en">Property Management</h3>
<h3 class="lang-es" style="display:none">Gestión de Propiedades</h3>
<h3 class="lang-ru" style="display:none">Управление недвижимостью</h3>
<p class="lang-en">Professional management of your property, including rental and maintenance.</p>
<p class="lang-es" style="display:none">Gestión profesional de su propiedad, incluyendo alquiler y mantenimiento.</p>
<p class="lang-ru" style="display:none">Профессиональное управление вашей собственностью, включая аренду и техническое обслуживание.</p>
</div>
<div class="service-card" id="investment">
<div class="service-icon">
<i class="fas fa-search-dollar"></i>
</div>
<h3 class="lang-en">Investment Consultations</h3>
<h3 class="lang-es" style="display:none">Consultoría de Inversiones</h3>
<h3 class="lang-ru" style="display:none">Инвестиционные консультации</h3>
<p class="lang-en">Real estate market analysis and assistance in choosing the most promising investment projects.</p>
<p class="lang-es" style="display:none">Análisis del mercado inmobiliario y asistencia en la elección de los proyectos de inversión más prometedores.</p>
<p class="lang-ru" style="display:none">Анализ рынка недвижимости и помощь в выборе наиболее перспективных инвестиционных проектов.</p>
</div>
</div>
</div>
</section>
<!-- Portfolio Section -->
<section class="section" id="portfolio">
<div class="container max-w-screen-xl mx-auto px-4 sm:px-6 lg:px-8">
<div class="section-title">
<h2 class="lang-en">Our Projects</h2>
<h2 class="lang-es" style="display:none">Nuestros Proyectos</h2>
<h2 class="lang-ru" style="display:none">Наши проекты</h2>
</div>
<div class="portfolio-grid">
<div class="portfolio-item"><img alt="Perla Marina – Comfortable 115 m² villa in resort area" src="perla-marina.jpeg"/><div class="portfolio-overlay"><h3>Perla Marina</h3><p class="lang-en">Comfortable 115 m² villa in resort area</p><p class="lang-es" style="display:none">Cómoda villa de 115 m² en zona turística</p><p class="lang-ru" style="display:none">Уютная вилла 115 м² в курортной зоне</p></div></div><div class="portfolio-item"><img alt="Sea Horse Ranch – Exclusive 500 m² villa in gated community" src="sea-horse-ranch.jpeg"/><div class="portfolio-overlay"><h3>Sea Horse Ranch</h3><p class="lang-en">Exclusive 500 m² villa in gated community</p><p class="lang-es" style="display:none">Villa exclusiva de 500 m² en comunidad cerrada</p><p class="lang-ru" style="display:none">Эксклюзивная вилла 500 м² в охраняемом посёлке</p></div></div><div class="portfolio-item"><img alt="Sosua Ocean Village – 300 m² villa with panoramic ocean view and private pool" src="sosua-ocean-village.jpeg"/><div class="portfolio-overlay"><h3>Sosua Ocean Village</h3><p class="lang-en">300 m² villa with panoramic ocean view and private pool</p><p class="lang-es" style="display:none">Villa de 300 m² con vista panorámica al océano y piscina privada</p><p class="lang-ru" style="display:none">Вилла 300 м² с панорамным видом на океан и частным бассейном</p></div></div><div class="portfolio-item"><img alt="ProCab Cabarete – Modern 300 m² villa in prestigious Cabarete area" src="procab-cabarete.jpeg"/><div class="portfolio-overlay"><h3>ProCab Cabarete</h3><p class="lang-en">Modern 300 m² villa in prestigious Cabarete area</p><p class="lang-es" style="display:none">Moderna villa de 300 m² en la prestigiosa zona de Cabarete</p><p class="lang-ru" style="display:none">Современная вилла 300 м² в престижном районе Кабарете</p></div></div><div class="portfolio-item"><img alt="Panorama Village Sosua – Luxury 450 m² villa with view of Sosua Bay" src="panorama-village-sosua.jpeg"/><div class="portfolio-overlay"><h3>Panorama Village Sosua</h3><p class="lang-en">Luxury 450 m² villa with view of Sosua Bay</p><p class="lang-es" style="display:none">Villa de lujo de 450 m² con vista a la bahía de Sosua</p><p class="lang-ru" style="display:none">Роскошная вилла 450 м² с видом на залив Сосуа</p></div></div><div class="portfolio-item"><img alt="Campo del Mar – Cozy 120 m² villa within walking distance to the beach" src="campo-del-mar.jpeg"/><div class="portfolio-overlay"><h3>Campo del Mar</h3><p class="lang-en">Cozy 120 m² villa within walking distance to the beach</p><p class="lang-es" style="display:none">Acogedora villa de 120 m² a poca distancia de la playa</p><p class="lang-ru" style="display:none">Уютная вилла 120 м² в шаговой доступности от пляжа</p></div></div><div class="portfolio-item"><img alt="Sea Horse Ranch – Exclusive 500 m² villa in gated community" src="sea-horse-ranch-2.jpeg"/><div class="portfolio-overlay"><h3>Sea Horse Ranch</h3><p class="lang-en">Exclusive 500 m² villa in gated community</p><p class="lang-es" style="display:none">Villa exclusiva de 500 m² en comunidad cerrada</p><p class="lang-ru" style="display:none">Эксклюзивная вилла 500 м² в охраняемом посёлке</p></div></div><div class="portfolio-item"><img alt="Villa in Hispaniola – 110 m² villa with pool, 2 bedrooms and 2 bathrooms" src="villa-in-hispaniola.jpeg"/><div class="portfolio-overlay"><h3>Villa in Hispaniola</h3><p class="lang-en">110 m² villa with pool, 2 bedrooms and 2 bathrooms</p><p class="lang-es" style="display:none">Villa de 110 m² con piscina, 2 dormitorios y 2 baños</p><p class="lang-ru" style="display:none">Вилла 110 м² с бассейном, 2 спальни и 2 ванные комнаты</p></div></div><div class="portfolio-item"><img alt="Perla Marina Cabarete – 300 m² villa with 5 bedrooms and 4 bathrooms" src="perla-marina-cabarete.jpeg"/><div class="portfolio-overlay"><h3>Perla Marina Cabarete</h3><p class="lang-en">300 m² villa with 5 bedrooms and 4 bathrooms</p><p class="lang-es" style="display:none">Villa de 300 m² con 5 dormitorios y 4 baños</p><p class="lang-ru" style="display:none">Вилла 300 м² с 5 спальнями и 4 ванными комнатами</p></div></div></div>
</div>
</section>
<!-- Testimonials Section -->
<!-- FAQ Section -->
<section class="section">
<div class="container max-w-screen-xl mx-auto px-4 sm:px-6 lg:px-8">
<div class="section-title">
<h2 class="lang-en">Frequently Asked Questions</h2>
<h2 class="lang-es" style="display:none">Preguntas Frecuentes</h2>
<h2 class="lang-ru" style="display:none">Часто задаваемые вопросы</h2>
</div>
<div class="faq-container">
<div class="faq-item">
<div class="faq-question">
<span class="lang-en">What is the construction time for a turnkey villa?</span>
<span class="lang-es" style="display:none">¿Cuál es el tiempo de construcción para una villa llave en mano?</span>
<span class="lang-ru" style="display:none">Какой срок строительства виллы под ключ?</span>
<i class="fas fa-chevron-down"></i>
</div>
<div class="faq-answer">
<p class="lang-en">Construction time depends on the complexity of the project and the area of the object. On average, the construction of a villa with an area of 300-400 m² takes from 8 to 12 months. We always comply with the agreed terms and provide the client with a detailed work schedule.</p>
<p class="lang-es" style="display:none">El tiempo de construcción depende de la complejidad del proyecto y el área del objeto. En promedio, la construcción de una villa de 300-400 m² toma de 8 a 12 meses. Siempre cumplimos con los plazos acordados y proporcionamos al cliente un cronograma detallado de trabajo.</p>
<p class="lang-ru" style="display:none">Срок строительства зависит от сложности проекта и площади объекта. В среднем, строительство виллы площадью 300-400 м² занимает от 8 до 12 месяцев. Мы всегда соблюдаем оговоренные сроки и предоставляем клиенту детальный график работ.</p>
</div>
</div>
<div class="faq-item">
<div class="faq-question">
<span class="lang-en">What guarantees do you provide?</span>
<span class="lang-es" style="display:none">¿Qué garantías proporcionan?</span>
<span class="lang-ru" style="display:none">Какие гарантии вы предоставляете?</span>
<i class="fas fa-chevron-down"></i>
</div>
<div class="faq-answer">
<p class="lang-en">We provide a 5-year warranty on building structures and a 2-year warranty on engineering systems. All warranty obligations are fixed in the contract. We also provide after-warranty service at the request of the client.</p>
<p class="lang-es" style="display:none">Proporcionamos una garantía de 5 años en estructuras de construcción y 2 años en sistemas de ingeniería. Todas las obligaciones de garantía se fijan en el contrato. También brindamos servicio post-garantía a solicitud del cliente.</p>
<p class="lang-ru" style="display:none">Мы предоставляем гарантию 5 лет на строительные конструкции и 2 года на инженерные системы. Все гарантийные обязательства фиксируются в договоре. Также мы оказываем послегарантийное обслуживание по желанию клиента.</p>
</div>
</div>
<div class="faq-item">
<div class="faq-question">
<span class="lang-en">How does the property registration process work?</span>
<span class="lang-es" style="display:none">¿Cómo funciona el proceso de registro de propiedad?</span>
<span class="lang-ru" style="display:none">Как происходит процесс оформления собственности?</span>
<i class="fas fa-chevron-down"></i>
</div>
<div class="faq-answer">
<p class="lang-en">Our lawyers fully accompany the property registration process (deslinde), which includes: obtaining a cadastral plan, registration in the National Registry, registration of a tax certificate. On average, the process takes 3-4 months.</p>
<p class="lang-es" style="display:none">Nuestros abogados acompañan completamente el proceso de registro de propiedad (deslinde), que incluye: obtención de un plan catastral, registro en el Registro Nacional, registro de un certificado fiscal. En promedio, el proceso toma 3-4 meses.</p>
<p class="lang-ru" style="display:none">Наши юристы полностью сопровождают процесс оформления собственности (deslinde), который включает: получение кадастрового плана, регистрацию в Национальном реестре, оформление налогового свидетельства. В среднем процесс занимает 3-4 месяца.</p>
</div>
</div>
<div class="faq-item">
<div class="faq-question">
<span class="lang-en">Can I get a residence visa when buying real estate?</span>
<span class="lang-es" style="display:none">¿Puedo obtener una visa de residencia al comprar una propiedad?</span>
<span class="lang-ru" style="display:none">Можно ли получить резидентскую визу при покупке недвижимости?</span>
<i class="fas fa-chevron-down"></i>
</div>
<div class="faq-answer">
<p class="lang-en">Yes, investments in real estate in the Dominican Republic give the right to obtain an investor residence visa. Our company provides full support in collecting documents and processing residency for the client and his family.</p>
<p class="lang-es" style="display:none">Sí, las inversiones en bienes raíces en República Dominicana dan derecho a obtener una visa de residencia de inversionista. Nuestra empresa brinda apoyo completo en la recopilación de documentos y el procesamiento de la residencia para el cliente y su familia.</p>
<p class="lang-ru" style="display:none">Да, инвестиции в недвижимость Доминиканской Республики дают право на получение резидентской визы инвестора. Наша компания оказывает полное сопровождение в сборе документов и оформлении резидентства для клиента и его семьи.</p>
</div>
</div>
</div>
</div>
</section>
<!-- Contact Section -->
<section class="section" id="contact">
<div class="container max-w-screen-xl mx-auto px-4 sm:px-6 lg:px-8">
<div class="section-title">
<h2 class="lang-en">Contact Us</h2>
<h2 class="lang-es" style="display:none">Contáctenos</h2>
<h2 class="lang-ru" style="display:none">Контакты</h2>
</div>
<div class="contact-container">
<div class="contact-info">
<h3 class="lang-en">Our Contacts</h3>
<h3 class="lang-es" style="display:none">Nuestros Contactos</h3>
<h3 class="lang-ru" style="display:none">Наши контакты</h3>
<div class="contact-details">
<p><i class="fas fa-map-marker-alt"></i> Sosúa, Dominican Republic, 57000</p>
<p><i class="fas fa-phone-alt"></i> +1 (829) 994-8888</p>
<p><i class="fas fa-envelope"></i> admin@vlad.pw</p>
</div>
<h3 class="lang-en">Follow Us</h3>
<h3 class="lang-es" style="display:none">Síganos</h3>
<h3 class="lang-ru" style="display:none">Мы в соцсетях</h3>
<div class="social-links">
<a aria-label="Facebook" href="https://www.facebook.com/aguasol24/" id="social-facebook" rel="noopener" target="_blank"><i class="fab fa-facebook-f"></i></a>
<a aria-label="Instagram" href="https://www.instagram.com/aguasol24/" id="social-instagram" rel="noopener" target="_blank"><i class="fab fa-instagram"></i></a>
<a aria-label="LinkedIn" href="https://www.linkedin.com/in/aguasol24/" id="social-linkedin" rel="noopener" target="_blank"><i class="fab fa-linkedin-in"></i></a>
<a aria-label="Telegram" href="https://t.me/casalinda" id="social-telegram" rel="noopener" target="_blank"><i class="fab fa-telegram-plane"></i></a>
</div>
<h3 class="lang-en" style="margin-top:16px">Working Hours</h3>
<h3 class="lang-es" style="margin-top:16px; display:none">Horario de Trabajo</h3>
<h3 class="lang-ru" style="margin-top:16px; display:none">Часы работы</h3>
<p><i class="far fa-clock"></i> <span class="lang-en">Mon–Fri: 9:00 - 18:00</span><span class="lang-es" style="display:none">Lun–Vie: 9:00 - 18:00</span><span class="lang-ru" style="display:none">Пн–Пт: 9:00 - 18:00</span></p>
<p><i class="far fa-clock"></i> <span class="lang-en">Sat: Closed</span><span class="lang-es" style="display:none">Sáb: Cerrado</span><span class="lang-ru" style="display:none">Сб: выходной</span></p>
<p><i class="far fa-clock"></i> <span class="lang-en">Sun: 11:00 - 15:00</span><span class="lang-es" style="display:none">Dom: 11:00 - 15:00</span><span class="lang-ru" style="display:none">Вс: 10:00 - 15:00</span></p>
</div>
<div class="contact-form">
<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>Vladis Multi-Step Form</title>
<script src="https://cdn.tailwindcss.com"></script>
<!-- Injected to apply liquid glass light blue on input fields -->
<style>
input:not([type=checkbox]):not([type=radio]),
select,
textarea {
  background: rgba(126, 200, 227, 0.15); /* light sky blue glass */
  border: 1px solid #7EC8E3;
  transition: border-color 0.2s ease, box-shadow 0.2s ease;
}
input:focus, select:focus, textarea:focus {
  border-color: #7EC8E3;
  box-shadow: 0 0 0 3px rgba(126, 200, 227, 0.45);
}
</style>
<!-- Liquid Glass Gradient for selection buttons -->
<style>
/* Apply gradient blue glass look to any element with bg-[#7ec8e3] class
   except the NEXT button which is bg-blue-600 */
[class*="bg-[#7ec8e3]"] {
  background: linear-gradient(180deg, #cbe7ff 0%, #9fd3ff 100%) !important;
  color: #0f1d31 !important;
  border: 1px solid rgba(159, 211, 255, 0.8);
  backdrop-filter: blur(12px) saturate(180%);
}

[class*="bg-[#7ec8e3]"]:hover {
  background: linear-gradient(180deg, #b5deff 0%, #7ecaff 100%) !important;
}
</style>
<style>
/* === Apple‑style system font stack (San Francisco) === */
body, button, input, select, textarea {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Helvetica, Arial, sans-serif;
}
</style>
<style>
.glass-toast {
  position: fixed;
  top: 20px;
  left: 50%;
  transform: translateX(-50%);
  z-index: 9999;
  padding: 12px 24px;
  background: rgba(203, 231, 255, 0.45);
  backdrop-filter: blur(10px);
  border: 1px solid #9FD3FF;
  border-radius: 16px;
  color: #0f172a;
  font-weight: 600;
  box-shadow: 0 4px 20px rgba(0,0,0,0.15);
  opacity: 0;
  transition: opacity 0.3s ease, transform 0.3s ease;
}
.glass-toast.show {
  opacity: 1;
  transform: translateX(-50%) translateY(0);
}
</style>
</head>
<body class="bg-gray-100 text-gray-800">
<div class="w-full max-w-2xl bg-white rounded-xl shadow p-6 space-y-6 mx-auto">
<div class="text-center">
<h2 class="text-2xl font-bold text-blue-600" id="step-title">Step 1 of 5</h2>
<p class="mt-2 text-base font-medium" id="step-question">What are you looking for?</p>
</div>
<div class="space-y-4" id="step-content">
<button class="w-full py-2 rounded-xl bg-[#7ec8e3] text-gray-900 font-semibold hover:bg-[#6ab2cf] transition" onclick="selectOption('Buy')">Buy</button>
<button class="w-full py-2 rounded-xl bg-[#7ec8e3] text-gray-900 font-semibold hover:bg-[#6ab2cf] transition" onclick="selectOption('Rent')">Rent</button>
<button class="w-full py-2 rounded-xl bg-[#7ec8e3] text-gray-900 font-semibold hover:bg-[#6ab2cf] transition" onclick="selectOption('Build')">Build</button>
</div>
<div class="flex justify-between pt-4">
<button class="bg-gray-200 text-gray-700 px-5 py-2 rounded-xl hover:bg-gray-300" id="backBtn" onclick="prevStep()">Back</button>
<button class="bg-blue-600 text-white px-5 py-2 rounded-xl hover:bg-blue-700" id="nextBtn" onclick="nextStep()">Next</button>
</div>
</div>
<script>
  let currentStep = 1;
let selectedOption = null;
  const totalSteps = 5;
  const steps = [
    {
      title: "Step 1 of 5",
      question: "What are you looking for?",
      options: ["Buy", "Rent", "Build"]
    },
    {
      title: "Step 2 of 5",
      question: "What type of property?",
      options: ["Villa", "Apartment", "Project"]
    },
    {
      title: "Step 3 of 5",
      question: "In what area or city?",
      options: ["Sosúa", "Cabarete", "Punta Cana", "Other"]
    },
    {
      title: "Step 4 of 5",
      question: "Approximate monthly budget in $USD",
      input: "text"
    },
    {
      title: "Step 5 of 5",
      question: "Please leave your contact:",
      inputs: ["Full Name", "Email", "WhatsApp"]
    }
  ];

  function renderStep() {
    document.getElementById("step-title").innerText = steps[currentStep - 1].title;
    document.getElementById("step-question").innerText = steps[currentStep - 1].question;

    const content = document.getElementById("step-content");
    content.innerHTML = "";

    const step = steps[currentStep - 1];

    if (step.options) {
      step.options.forEach(opt => {
        const btn = document.createElement("button");
        btn.className = "w-full py-2 rounded-xl bg-[#7ec8e3] text-gray-900 font-semibold hover:bg-[#6ab2cf] transition";
        btn.innerText = opt;
        btn.onclick = () => selectOption(opt);
        content.appendChild(btn);
      });
    }

    if (step.input) {
      const input = document.createElement("input");
      input.type = step.input;
      input.placeholder = "$ USD";
      input.className = "w-full px-4 py-2 border rounded-xl";
      content.appendChild(input);
    
      input.addEventListener("input", () => localStorage.setItem("step4", input.value));}

    if (step.inputs) {
      step.inputs.forEach(ph => {
        const input = document.createElement("input");
        input.type = "text";
        input.placeholder = ph;
        input.className = "w-full px-4 py-2 border rounded-xl";
        content.appendChild(input);
      });

      const submit = document.createElement("button");
      submit.className = "w-full py-2 mt-2 rounded-xl bg-[#7ec8e3] text-gray-900 font-semibold hover:bg-[#6ab2cf] transition";
      submit.innerText = "Submit";
      submit.onclick = () => {
  const name = content.querySelector('input[placeholder="Full Name"]')?.value.trim() || "N/A";
  const email = content.querySelector('input[placeholder="Email"]')?.value.trim() || "N/A";
  const phone = content.querySelector('input[placeholder="WhatsApp"]')?.value.trim() || "N/A";

  
  const namePattern = /^[A-Za-zÀ-ÿ\u0400-\u04FF]+(?:\s+[A-Za-zÀ-ÿ\u0400-\u04FF]+)+$/;
  const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
  const phonePattern = /^\+?\d{7,15}$/;

  if (!namePattern.test(name)) {
    showToast("Please enter your full name (first and last).");
    return;
  }
  if (!emailPattern.test(email)) {
    showToast("Please enter a valid email address.");
    return;
  }
  if (!phonePattern.test(phone)) {
    showToast("Please enter your WhatsApp number in international format, e.g. +18291234567.");
    return;
  }


  const step1 = localStorage.getItem("step1") || "N/A";
  const step2 = localStorage.getItem("step2") || "N/A";
  const step3 = localStorage.getItem("step3") || "N/A";
  const budgetInput = content.querySelector('input[placeholder="$ USD"]')?.value.trim();
  const budget = budgetInput || localStorage.getItem("step4") || "N/A";
  const now = new Date().toLocaleString();

  fetch("https://ipapi.co/json/")
    .then(response => response.json())
    .then(location => {
      const ip = location.ip || "N/A";
      const city = location.city || "Unknown";
      const country = location.country_name || "Unknown";

      const message = `📬 New Client Request – Construction Form

🕒 Date: ${now}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${step1}
🔹 Step 2: ${step2}
🔹 Step 3: ${step3}
🔹 Budget: ${budget}

👤 Name: ${name}
📱 WhatsApp: ${phone}
✉️ Email: ${email}`;

      fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          chat_id: "92750995",
          text: message
        })
      });

      content.innerHTML = `<div class="flex flex-col items-center justify-center gap-6 p-8 bg-white/70 backdrop-blur-md rounded-3xl shadow-2xl text-center max-w-md mx-auto">
  <div class="w-20 h-20 flex items-center justify-center rounded-full bg-green-500 text-white text-5xl">✓</div>
  <h2 class="text-3xl font-semibold text-gray-900">Thank you!</h2>
  <p class="text-gray-700 leading-relaxed">Your request has been received.<br/>We will contact you shortly.</p>
</div>
`;
    // Reduce to two visual layers: remove background & shadow from outer container
    const outerCard = document.querySelector('.w-full.max-w-2xl');
    if (outerCard) {
      outerCard.classList.remove('bg-white','shadow');
      outerCard.classList.add('bg-transparent','shadow-none');
    }
    
      document.getElementById("step-question").innerText = "";
      document.getElementById("nextBtn").style.display = "none";
      document.getElementById("backBtn").style.display = "none";
    });
};
      content.appendChild(submit);
    }

    document.getElementById("backBtn").style.display = currentStep === 1 ? "none" : "inline-block";
    document.getElementById("nextBtn").style.display = currentStep < totalSteps ? "inline-block" : "none";
  document.getElementById("nextBtn").disabled = step.options ? true : false;
  }

  function nextStep() {
    if (currentStep < totalSteps) {
      currentStep++;
      renderStep();
    }
  }

  function prevStep() {
    if (currentStep > 1) {
      currentStep--;
      renderStep();
    }
  }

  function selectOption(value) {
  selectedOption = value;
  localStorage.setItem(`step${currentStep}`, value);
  document.getElementById('nextBtn').disabled = false;
    nextStep();
  }

  document.addEventListener("DOMContentLoaded", renderStep);
</script>
<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>Vladis Multi-Step Form</title>
<script src="https://cdn.tailwindcss.com"></script>
<script src="https://unpkg.com/i18next@21.6.14/dist/umd/i18next.min.js"></script>
<script>
  function detectLang() {
    const urlParams = new URLSearchParams(window.location.search);
    const urlLang = urlParams.get('lang');
    if (['en', 'es', 'ru'].includes(urlLang)) return urlLang;

    const htmlLang = document.documentElement.lang;
    if (['en', 'es', 'ru'].includes(htmlLang)) return htmlLang;

    const browserLang = (navigator.language || navigator.userLanguage).split('-')[0];
    return ['en', 'es', 'ru'].includes(browserLang) ? browserLang : 'en';
  }

  const lang = detectLang();

  const resources = {
    en: {
      translation: {
        step1: "What are you looking for?",
        step2: "What type of property?",
        step3: "In what area or city?",
        step4: "Approximate monthly budget in $USD",
        step5: "Please leave your contact:",
        buy: "Buy",
        rent: "Rent",
        build: "Build",
        villa: "Villa",
        apartment: "Apartment",
        project: "Project",
        sosua: "Sosúa",
        cabarete: "Cabarete",
        other: "Other",
        name: "Name",
        email: "Email",
        whatsapp: "WhatsApp",
        submit: "Submit",
        thankyou: "✅ Thank you! Your request has been received. We will contact you shortly."
      }
    },
    es: {
      translation: {
        step1: "¿Qué está buscando?",
        step2: "¿Qué tipo de propiedad?",
        step3: "¿En qué zona o ciudad?",
        step4: "Presupuesto mensual aproximado en $USD",
        step5: "Por favor, deje su contacto:",
        buy: "Comprar",
        rent: "Alquilar",
        build: "Construir",
        villa: "Villa",
        apartment: "Apartamento",
        project: "Proyecto",
        sosua: "Sosúa",
        cabarete: "Cabarete",
        other: "Otro",
        name: "Nombre",
        email: "Correo",
        whatsapp: "WhatsApp",
        submit: "Enviar",
        thankyou: "✅ ¡Gracias! Su solicitud ha sido recibida. Nos pondremos en contacto pronto."
      }
    },
    ru: {
      translation: {
        step1: "Что вас интересует?",
        step2: "Какой тип недвижимости?",
        step3: "В каком районе или городе?",
        step4: "Примерный бюджет в $USD",
        step5: "Оставьте, пожалуйста, ваши данные:",
        buy: "Купить",
        rent: "Аренда",
        build: "Строительство",
        villa: "Вилла",
        apartment: "Квартира",
        project: "Проект",
        sosua: "Сосуа",
        cabarete: "Кабарете",
        other: "Другое",
        name: "Имя",
        email: "Email",
        whatsapp: "WhatsApp",
        submit: "Отправить",
        thankyou: "✅ Спасибо! Ваша заявка получена. Мы свяжемся с вами в ближайшее время."
      }
    }
  };

  i18next.init({ lng: lang, debug: false, resources }, function(err, t) {
    window.translations = t;
    renderStep();
  });
</script>
<!-- Injected to apply liquid glass light blue on input fields -->
<style>
input:not([type=checkbox]):not([type=radio]),
select,
textarea {
  background: rgba(126, 200, 227, 0.15); /* light sky blue glass */
  border: 1px solid #7EC8E3;
  transition: border-color 0.2s ease, box-shadow 0.2s ease;
}
input:focus, select:focus, textarea:focus {
  border-color: #7EC8E3;
  box-shadow: 0 0 0 3px rgba(126, 200, 227, 0.45);
}
</style>
<!-- Liquid Glass Gradient for selection buttons -->
<style>
/* Apply gradient blue glass look to any element with bg-[#7ec8e3] class
   except the NEXT button which is bg-blue-600 */
[class*="bg-[#7ec8e3]"] {
  background: linear-gradient(180deg, #cbe7ff 0%, #9fd3ff 100%) !important;
  color: #0f1d31 !important;
  border: 1px solid rgba(159, 211, 255, 0.8);
  backdrop-filter: blur(12px) saturate(180%);
}

[class*="bg-[#7ec8e3]"]:hover {
  background: linear-gradient(180deg, #b5deff 0%, #7ecaff 100%) !important;
}
</style>
<style>
/* === Apple‑style system font stack (San Francisco) === */
body, button, input, select, textarea {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Helvetica, Arial, sans-serif;
}
</style>
<style>
.glass-toast {
  position: fixed;
  top: 20px;
  left: 50%;
  transform: translateX(-50%);
  z-index: 9999;
  padding: 12px 24px;
  background: rgba(203, 231, 255, 0.45);
  backdrop-filter: blur(10px);
  border: 1px solid #9FD3FF;
  border-radius: 16px;
  color: #0f172a;
  font-weight: 600;
  box-shadow: 0 4px 20px rgba(0,0,0,0.15);
  opacity: 0;
  transition: opacity 0.3s ease, transform 0.3s ease;
}
.glass-toast.show {
  opacity: 1;
  transform: translateX(-50%) translateY(0);
}
</style>
</head>
<body class="bg-gray-100 text-gray-800">
<script>
  let currentStep = 1;
let selectedOption = null;
  const totalSteps = 5;
  const steps = [
    {
      title: "Step 1 of 5",
      question: "What are you looking for?",
      options: ["Buy", "Rent", "Build"]
    },
    {
      title: "Step 2 of 5",
      question: "What type of property?",
      options: ["Villa", "Apartment", "Project"]
    },
    {
      title: "Step 3 of 5",
      question: "In what area or city?",
      options: ["Sosúa", "Cabarete", "Punta Cana", "Other"]
    },
    {
      title: "Step 4 of 5",
      question: "Approximate monthly budget in $USD",
      input: "text"
    },
    {
      title: "Step 5 of 5",
      question: "Please leave your contact:",
      inputs: ["Full Name", "Email", "WhatsApp"]
    }
  ];

  function renderStep() {
    document.getElementById("step-title").innerText = steps[currentStep - 1].title;
    document.getElementById("step-question").innerText = steps[currentStep - 1].question;

    const content = document.getElementById("step-content");
    content.innerHTML = "";

    const step = steps[currentStep - 1];

    if (step.options) {
      step.options.forEach(opt => {
        const btn = document.createElement("button");
        btn.className = "w-full py-3 rounded-xl bg-[#7ec8e3] text-gray-900 font-semibold hover:bg-[#6ab2cf] transition";
        btn.innerText = opt;
        btn.onclick = () => selectOption(opt);
        content.appendChild(btn);
      });
    }

    if (step.input) {
      const input = document.createElement("input");
      input.type = step.input;
      input.placeholder = "$ USD";
      input.className = "w-full px-4 py-3 border rounded-xl";
      content.appendChild(input);
    
      input.addEventListener("input", () => localStorage.setItem("step4", input.value));}

    if (step.inputs) {
      step.inputs.forEach(ph => {
        const input = document.createElement("input");
        input.type = "text";
        input.placeholder = ph;
        input.className = "w-full px-4 py-3 border rounded-xl";
        content.appendChild(input);
      });

      const submit = document.createElement("button");
      submit.className = "w-full py-3 mt-2 rounded-xl bg-[#7ec8e3] text-gray-900 font-semibold hover:bg-[#6ab2cf] transition";
      submit.innerText = "Submit";
      submit.onclick = () => {
  const name = content.querySelector('input[placeholder="Full Name"]')?.value.trim() || "N/A";
  const email = content.querySelector('input[placeholder="Email"]')?.value.trim() || "N/A";
  const phone = content.querySelector('input[placeholder="WhatsApp"]')?.value.trim() || "N/A";

  if (!name || !email || !phone) {
    showToast("Please fill in Name, Email and WhatsApp.");
    return;
  }

  const step1 = localStorage.getItem("step1") || "N/A";
  const step2 = localStorage.getItem("step2") || "N/A";
  const step3 = localStorage.getItem("step3") || "N/A";
  const budgetInput = content.querySelector('input[placeholder="$ USD"]')?.value.trim();
  const budget = budgetInput || localStorage.getItem("step4") || "N/A";
  const now = new Date().toLocaleString();

  fetch("https://ipapi.co/json/")
    .then(response => response.json())
    .then(location => {
      const ip = location.ip || "N/A";
      const city = location.city || "Unknown";
      const country = location.country_name || "Unknown";

      const message = `📬 New Client Request – Construction Form

🕒 Date: ${now}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${step1}
🔹 Step 2: ${step2}
🔹 Step 3: ${step3}
🔹 Budget: ${budget}

👤 Name: ${name}
📱 WhatsApp: ${phone}
✉️ Email: ${email}`;

      fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          chat_id: "92750995",
          text: message
        })
      });

      content.innerHTML = `<div class="text-green-600 font-semibold text-center">✅ Thank you! Your request has been received. We will contact you shortly.</div>`;
      document.getElementById("step-question").innerText = "";
      document.getElementById("nextBtn").style.display = "none";
      document.getElementById("backBtn").style.display = "none";
    });
};
      content.appendChild(submit);
    }

    document.getElementById("backBtn").style.display = currentStep === 1 ? "none" : "inline-block";
    document.getElementById("nextBtn").style.display = currentStep < totalSteps ? "inline-block" : "none";
  document.getElementById("nextBtn").disabled = step.options ? true : false;
  }

  function nextStep() {
    if (currentStep < totalSteps) {
      currentStep++;
      renderStep();
    }
  }

  function prevStep() {
    if (currentStep > 1) {
      currentStep--;
      renderStep();
    }
  }

  function selectOption(value) {
  selectedOption = value;
  localStorage.setItem(`step${currentStep}`, value);
  document.getElementById('nextBtn').disabled = false;
    nextStep();
  }

  document.addEventListener("DOMContentLoaded", renderStep);
</script>
<script>
function submitFormTelegram() {
    const steps = document.querySelectorAll('.step');
    const answers = [];

    steps.forEach((step) => {
        const selected = step.querySelector('button.selected');
        const input = step.querySelector('input, textarea');
        if (selected) answers.push(selected.innerText);
        else if (input && input.value) answers.push(input.value);
        else answers.push("N/A");
    });

    const now = new Date();
    const formattedDate = now.toLocaleString();

    fetch("https://ipapi.co/json/")
      .then(response => response.json())
      .then(location => {
        const ip = location.ip || "N/A";
        const city = location.city || "N/A";
        const country = location.country_name || "N/A";

        const message = `
📬 New Form Submission

🕒 Date: ${formattedDate}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${answers[0]}
🔹 Step 2: ${answers[1]}
🔹 Step 3: ${answers[2]}
🔹 Step 4: ${answers[3]}
🔹 Name: ${answers[4]}
🔹 Phone: ${answers[5]}
🔹 Email: ${answers[6]}
`;

        fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
            method: "POST",
            headers: { "Content-Type": "application/json" },
            body: JSON.stringify({
                chat_id: "92750995",
                text: message.trim()
            })
        });

        document.querySelector('.quiz-container').innerHTML = `
            <div style="text-align:center;padding:20px;background:#f8f9fa;border-radius:10px;">
                <h2>✅ Thank You!</h2>
                <p>Your submission has been successfully sent. We'll contact you shortly.</p>
            </div>
        `;
      });
}

// Назначим функцию на кнопку Submit
document.querySelector('.btn-main[onclick="submitForm()"]').setAttribute('onclick', 'submitFormTelegram()');
</script>
<script>
function submitFormTelegram() {
  const steps = document.querySelectorAll('.step');
  const answers = [];

  steps.forEach((step) => {
    const selected = step.querySelector('button.selected');
    const input = step.querySelector('input, textarea');
    if (selected) answers.push(selected.innerText);
    else if (input && input.value) answers.push(input.value);
    else answers.push("N/A");
  });

  const now = new Date().toLocaleString();

  fetch("https://ipapi.co/json/")
    .then(response => response.json())
    .then(location => {
      const ip = location.ip || "N/A";
      const city = location.city || "N/A";
      const country = location.country_name || "N/A";

      const message = `
📬 New Client Request – Construction Form

🕒 Date: ${now}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${answers[0]}
🔹 Step 2: ${answers[1]}
🔹 Step 3: ${answers[2]}
🔹 Budget: ${answers[3]}

👤 Name: ${answers[4]}
📱 WhatsApp: ${answers[5]}
✉️ Email: ${answers[6]}
`;

      fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          chat_id: "92750995",
          text: message
        })
      });

      document.querySelector('.quiz-container').innerHTML = `
        <div style="text-align:center;padding:20px;background:#f8f9fa;border-radius:10px;">
          <h2>✅ Thank You!</h2>
          <p>Your submission has been successfully sent. We'll contact you shortly.</p>
        </div>
      `;
    });
}
</script>
<script>
function submitFormTelegram() {
  const steps = document.querySelectorAll('.step');
  const answers = [];

  steps.forEach((step) => {
    const selected = step.querySelector('button.selected');
    const input = step.querySelector('input, textarea');
    if (selected) answers.push(selected.innerText);
    else if (input && input.value) answers.push(input.value);
    else answers.push("N/A");
  });

  const now = new Date().toLocaleString();

  fetch("https://ipapi.co/json/")
    .then(response => response.json())
    .then(location => {
      const ip = location.ip || "N/A";
      const city = "Málaga";
      const country = "Spain";

      const message = `📬 New Client Request – Construction Form

🕒 Date: ${now}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${answers[0]}
🔹 Step 2: ${answers[1]}
🔹 Step 3: ${answers[2]}
🔹 Budget: ${answers[3]}

👤 Name: ${answers[4]}
📱 WhatsApp: ${answers[5]}
✉️ Email: ${answers[6]}`;

      fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          chat_id: "92750995",
          text: message
        })
      });

      document.querySelector('.quiz-container').innerHTML = `
        <div style="text-align:center;padding:20px;background:#f8f9fa;border-radius:10px;">
          <h2>✅ Thank You!</h2>
          <p>Your submission has been successfully sent. We'll contact you shortly.</p>
        </div>
      `;
    });
}
</script>
<script>
function showToast(message) {
  let toast = document.getElementById("glass-toast");
  if (!toast) {
    toast = document.createElement("div");
    toast.id = "glass-toast";
    toast.className = "glass-toast";
    document.body.appendChild(toast);
  }
  toast.innerText = message;
  toast.classList.add("show");
  setTimeout(() => {
    toast.classList.remove("show");
  }, 4000);
}
</script>
<script>
const btn = document.getElementById("mobile-menu-btn");
if(btn){
  const navLinks = btn.nextElementSibling;
  btn.addEventListener("click", ()=> {
    navLinks.classList.toggle("hidden");
  });
}
</script>
</body>
</html>
<script>
function submitFormTelegram() {
    const steps = document.querySelectorAll('.step');
    const answers = [];

    steps.forEach((step) => {
        const selected = step.querySelector('button.selected');
        const input = step.querySelector('input, textarea');
        if (selected) answers.push(selected.innerText);
        else if (input && input.value) answers.push(input.value);
        else answers.push("N/A");
    });

    const now = new Date();
    const formattedDate = now.toLocaleString();

    fetch("https://ipapi.co/json/")
      .then(response => response.json())
      .then(location => {
        const ip = location.ip || "N/A";
        const city = location.city || "N/A";
        const country = location.country_name || "N/A";

        const message = `
📬 New Form Submission

🕒 Date: ${formattedDate}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${answers[0]}
🔹 Step 2: ${answers[1]}
🔹 Step 3: ${answers[2]}
🔹 Step 4: ${answers[3]}
🔹 Name: ${answers[4]}
🔹 Phone: ${answers[5]}
🔹 Email: ${answers[6]}
`;

        fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
            method: "POST",
            headers: { "Content-Type": "application/json" },
            body: JSON.stringify({
                chat_id: "92750995",
                text: message.trim()
            })
        });

        document.querySelector('.quiz-container').innerHTML = `
            <div style="text-align:center;padding:20px;background:#f8f9fa;border-radius:10px;">
                <h2>✅ Thank You!</h2>
                <p>Your submission has been successfully sent. We'll contact you shortly.</p>
            </div>
        `;
      });
}

// Назначим функцию на кнопку Submit
document.querySelector('.btn-main[onclick="submitForm()"]').setAttribute('onclick', 'submitFormTelegram()');
</script>
<script>
function submitFormTelegram() {
  const steps = document.querySelectorAll('.step');
  const answers = [];

  steps.forEach((step) => {
    const selected = step.querySelector('button.selected');
    const input = step.querySelector('input, textarea');
    if (selected) answers.push(selected.innerText);
    else if (input && input.value) answers.push(input.value);
    else answers.push("N/A");
  });

  const now = new Date().toLocaleString();

  fetch("https://ipapi.co/json/")
    .then(response => response.json())
    .then(location => {
      const ip = location.ip || "N/A";
      const city = location.city || "N/A";
      const country = location.country_name || "N/A";

      const message = `
📬 New Client Request – Construction Form

🕒 Date: ${now}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${answers[0]}
🔹 Step 2: ${answers[1]}
🔹 Step 3: ${answers[2]}
🔹 Budget: ${answers[3]}

👤 Name: ${answers[4]}
📱 WhatsApp: ${answers[5]}
✉️ Email: ${answers[6]}
`;

      fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          chat_id: "92750995",
          text: message
        })
      });

      document.querySelector('.quiz-container').innerHTML = `
        <div style="text-align:center;padding:20px;background:#f8f9fa;border-radius:10px;">
          <h2>✅ Thank You!</h2>
          <p>Your submission has been successfully sent. We'll contact you shortly.</p>
        </div>
      `;
    });
}
</script>
<script>
function submitFormTelegram() {
  const steps = document.querySelectorAll('.step');
  const answers = [];

  steps.forEach((step) => {
    const selected = step.querySelector('button.selected');
    const input = step.querySelector('input, textarea');
    if (selected) answers.push(selected.innerText);
    else if (input && input.value) answers.push(input.value);
    else answers.push("N/A");
  });

  const now = new Date().toLocaleString();

  fetch("https://ipapi.co/json/")
    .then(response => response.json())
    .then(location => {
      const ip = location.ip || "N/A";
      const city = "Málaga";
      const country = "Spain";

      const message = `📬 New Client Request – Construction Form

🕒 Date: ${now}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${answers[0]}
🔹 Step 2: ${answers[1]}
🔹 Step 3: ${answers[2]}
🔹 Budget: ${answers[3]}

👤 Name: ${answers[4]}
📱 WhatsApp: ${answers[5]}
✉️ Email: ${answers[6]}`;

      fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          chat_id: "92750995",
          text: message
        })
      });

      document.querySelector('.quiz-container').innerHTML = `
        <div style="text-align:center;padding:20px;background:#f8f9fa;border-radius:10px;">
          <h2>✅ Thank You!</h2>
          <p>Your submission has been successfully sent. We'll contact you shortly.</p>
        </div>
      `;
    });
}
</script>
<script>
function showToast(message) {
  let toast = document.getElementById("glass-toast");
  if (!toast) {
    toast = document.createElement("div");
    toast.id = "glass-toast";
    toast.className = "glass-toast";
    document.body.appendChild(toast);
  }
  toast.innerText = message;
  toast.classList.add("show");
  setTimeout(() => {
    toast.classList.remove("show");
  }, 4000);
}
</script>
<script>
const btn = document.getElementById("mobile-menu-btn");
if(btn){
  const navLinks = btn.nextElementSibling;
  btn.addEventListener("click", ()=> {
    navLinks.classList.toggle("hidden");
  });
}
</script>
</body>
</html>
</div>
</div>
</div>
</section>
<!-- Footer -->
<footer>
<div class="container max-w-screen-xl mx-auto px-4 sm:px-6 lg:px-8">
<div class="footer-container">
<div class="footer-col">
<h3>Vladis P.Plot</h3>
<p class="lang-en">Construction and management of luxury real estate in the Dominican Republic since 2007.</p>
<p class="lang-es" style="display:none">Construcción y gestión de bienes raíces de lujo en República Dominicana desde 2007.</p>
<p class="lang-ru" style="display:none">Строительство и управление элитной недвижимостью в Доминиканской Республике с 2007 года.</p>
</div>
<div class="footer-col">
<h3 class="lang-en">Navigation</h3>
<h3 class="lang-es" style="display:none">Navegación</h3>
<h3 class="lang-ru" style="display:none">Навигация</h3>
<ul>
<li><a class="lang-en" href="#home">Home</a><a class="lang-es" href="#home" style="display:none">Inicio</a><a class="lang-ru" href="#home" style="display:none">Главная</a></li>
<li><a class="lang-en" href="#about">About</a><a class="lang-es" href="#about" style="display:none">Sobre Nosotros</a><a class="lang-ru" href="#about" style="display:none">О компании</a></li>
<li><a class="lang-en" href="#services">Services</a><a class="lang-es" href="#services" style="display:none">Servicios</a><a class="lang-ru" href="#services" style="display:none">Услуги</a></li>
<li><a class="lang-en" href="#portfolio">Portfolio</a><a class="lang-es" href="#portfolio" style="display:none">Portafolio</a><a class="lang-ru" href="#portfolio" style="display:none">Портфолио</a></li>
<li><a class="lang-en" href="#contact">Contact</a><a class="lang-es" href="#contact" style="display:none">Contacto</a><a class="lang-ru" href="#contact" style="display:none">Контакты</a></li>
</ul>
</div>
<div class="footer-col">
<h3 class="lang-en">Services</h3>
<h3 class="lang-es" style="display:none">Servicios</h3>
<h3 class="lang-ru" style="display:none">Услуги</h3>
<ul>
<li><a class="lang-en" href="#turnkey">Turnkey Construction</a><a class="lang-es" href="#turnkey" style="display:none">Construcción Llave en Mano</a><a class="lang-ru" href="#turnkey" style="display:none">Строительство под ключ</a></li>
<li><a class="lang-en" href="#design">Architectural Design</a><a class="lang-es" href="#design" style="display:none">Diseño Arquitectónico</a><a class="lang-ru" href="#design" style="display:none">Архитектурное проектирование</a></li>
<li><a class="lang-en" href="#legal">Legal Support</a><a class="lang-es" href="#legal" style="display:none">Asesoría Legal</a><a class="lang-ru" href="#legal" style="display:none">Юридическое сопровождение</a></li>
<li><a class="lang-en" href="#property">Property Management</a><a class="lang-es" href="#property" style="display:none">Gestión de Propiedades</a><a class="lang-ru" href="#property" style="display:none">Управление недвижимостью</a></li>
<li><a class="lang-en" href="#immigration">Immigration Services</a><a class="lang-es" href="#immigration" style="display:none">Servicios Migratorios</a><a class="lang-ru" href="#immigration" style="display:none">Иммиграционные услуги</a></li>
</ul>
</div>
<div class="footer-col">
<h3 class="lang-en">Contacts</h3>
<h3 class="lang-es" style="display:none">Contactos</h3>
<h3 class="lang-ru" style="display:none">Контакты</h3>
<ul>
<li><i class="fas fa-map-marker-alt"></i> Sosúa, Dominican Republic</li>
<li><i class="fas fa-phone-alt"></i> +1 (829) 994-8888</li>
<li><i class="fas fa-envelope"></i> admin@vlad.pw</li>
</ul>
</div>
</div>
<div class="copyright">
<p>© 2026 Vladis P.Plot. <span class="lang-en">All rights reserved.</span><span class="lang-es" style="display:none">Todos los derechos reservados.</span><span class="lang-ru" style="display:none">Все права защищены.</span></p>
</div>
</div>
</footer>
<!-- WhatsApp Button -->
<a class="whatsapp-btn" href="https://wa.me/18299948888" target="_blank">
<i class="fab fa-whatsapp"></i>
</a>
<!-- Scripts -->
<script>
        // Mobile Menu Toggle
        const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
        const nav = document.querySelector('nav');

        mobileMenuBtn.addEventListener('click', () => {
            nav.classList.toggle('active');
            mobileMenuBtn.innerHTML = nav.classList.contains('active') ? 
                '<i class="fas fa-times"></i>' : '<i class="fas fa-bars"></i>';
        });

        // FAQ Accordion
        const faqQuestions = document.querySelectorAll('.faq-question');
        
        faqQuestions.forEach(question => {
            question.addEventListener('click', () => {
                const item = question.parentNode;
                item.classList.toggle('active');
                
                const icon = question.querySelector('i');
                icon.className = item.classList.contains('active') ? 
                    'fas fa-chevron-up' : 'fas fa-chevron-down';
            });
        });

        // Smooth Scrolling for Anchor Links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                if (this.getAttribute('href') === '#') return;
                
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    window.scrollTo({
                        top: target.offsetTop - 70,
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu if open
                    if (nav.classList.contains('active')) {
                        nav.classList.remove('active');
                        mobileMenuBtn.innerHTML = '<i class="fas fa-bars"></i>';
                    }
                }
            });
        });

        // Language Switcher Functionality
        const languageSelector = document.getElementById('language-selector');
        
        function changeLanguage(lang) {
            // Hide all language elements
            document.querySelectorAll('.lang-en, .lang-es, .lang-ru').forEach(el => {
                el.style.display = 'none';
            });
            
            // Show elements for selected language
            document.querySelectorAll(`.lang-${lang}`).forEach(el => {
                el.style.display = 'block' || 'inline' || 'inline-block';
            });
            
            
    // === Hero & CTA translations ===
    const heroTranslations = {
        en: {
            title: 'Real Estate Construction in Sosúa – Cabarete',
            subtitle: 'Over 17 years of experience developing unique real‑estate projects in Sosúa and Cabarete, Dominican Republic.',
            contact: 'Contact Us',
            projects: 'Our Projects'
        },
        es: {
            title: 'Construcción inmobiliaria en Sosúa – Cabarete',
            subtitle: 'Más de 17 años de experiencia desarrollando proyectos inmobiliarios únicos en Sosúa y Cabarete, República Dominicana.',
            contact: 'Contáctenos',
            projects: 'Nuestros Proyectos'
        },
        ru: {
            title: 'Строительство недвижимости в Сосуа – Кабарете',
            subtitle: 'Более 17 лет опыта в реализации уникальных проектов недвижимости в Сосуа и Кабарете, Доминиканская Республика.',
            contact: 'Связаться',
            projects: 'Наши проекты'
        }
    };

    // Update hero text & buttons
    document.getElementById('hero-title').textContent      = heroTranslations[lang].title;
    document.getElementById('hero-subtitle').textContent   = heroTranslations[lang].subtitle;
    document.querySelector('.cta-contact').textContent     = heroTranslations[lang].contact;
    document.querySelector('.cta-projects').textContent    = heroTranslations[lang].projects;

            // Change HTML lang attribute
            document.documentElement.lang = lang;
            
            // Update navigation menu text based on language
            if (lang === 'en') {
                document.querySelector('nav ul li:nth-child(1) a').textContent = 'Home';
                document.querySelector('nav ul li:nth-child(2) a').textContent = 'About';
                document.querySelector('nav ul li:nth-child(3) a').textContent = 'Services';
                document.querySelector('nav ul li:nth-child(4) a').textContent = 'Portfolio';
                document.querySelector('nav ul li:nth-child(5) a').textContent = 'Contact';
            } else if (lang === 'es') {
                document.querySelector('nav ul li:nth-child(1) a').textContent = 'Inicio';
                document.querySelector('nav ul li:nth-child(2) a').textContent = 'Sobre Nosotros';
                document.querySelector('nav ul li:nth-child(3) a').textContent = 'Servicios';
                document.querySelector('nav ul li:nth-child(4) a').textContent = 'Portafolio';
                document.querySelector('nav ul li:nth-child(5) a').textContent = 'Contacto';
            } else if (lang === 'ru') {
                document.querySelector('nav ul li:nth-child(1) a').textContent = 'Главная';
                document.querySelector('nav ul li:nth-child(2) a').textContent = 'О компании';
                document.querySelector('nav ul li:nth-child(3) a').textContent = 'Услуги';
                document.querySelector('nav ul li:nth-child(4) a').textContent = 'Портфолио';
                document.querySelector('nav ul li:nth-child(5) a').textContent = 'Контакты';
            }
        }
        
        // Set default language to English
        changeLanguage('en');
        
        // Language selector event listener
        languageSelector.addEventListener('change', (e) => {
            changeLanguage(e.target.value);
        });

        // Form Submission
        const contactForm = document.querySelector('.contact-form form');
        if (contactForm) {
            contactForm.addEventListener('submit', (e) => {
                e.preventDefault();
                const currentLang = document.documentElement.lang;
                if (currentLang === 'en') {
                    alert('Thank you for your message! We will contact you soon.');
                } else if (currentLang === 'es') {
                    alert('¡Gracias por su mensaje! Nos pondremos en contacto con usted pronto.');
                } else if (currentLang === 'ru') {
                    alert('Спасибо за ваше сообщение! Мы свяжемся с вами в ближайшее время.');
                }
                contactForm.reset();
            });
        }

        // Sticky Header on Scroll
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            header.classList.toggle('sticky', window.scrollY > 0);
        });
    
// Highlight anchor after scroll
document.querySelectorAll('a[href^="#"]').forEach(link => {
  link.addEventListener('click', function(e) {
    const target = document.querySelector(this.getAttribute('href'));
    if (target) {
      target.classList.add('highlight');
      setTimeout(() => target.classList.remove('highlight'), 2000);
    }
  });
});
</script>
<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>Vladis Multi-Step Form</title>
<script src="https://cdn.tailwindcss.com"></script>
<!-- Injected to apply liquid glass light blue on input fields -->
<style>
input:not([type=checkbox]):not([type=radio]),
select,
textarea {
  background: rgba(126, 200, 227, 0.15); /* light sky blue glass */
  border: 1px solid #7EC8E3;
  transition: border-color 0.2s ease, box-shadow 0.2s ease;
}
input:focus, select:focus, textarea:focus {
  border-color: #7EC8E3;
  box-shadow: 0 0 0 3px rgba(126, 200, 227, 0.45);
}
</style>
<!-- Liquid Glass Gradient for selection buttons -->
<style>
/* Apply gradient blue glass look to any element with bg-[#7ec8e3] class
   except the NEXT button which is bg-blue-600 */
[class*="bg-[#7ec8e3]"] {
  background: linear-gradient(180deg, #cbe7ff 0%, #9fd3ff 100%) !important;
  color: #0f1d31 !important;
  border: 1px solid rgba(159, 211, 255, 0.8);
  backdrop-filter: blur(12px) saturate(180%);
}

[class*="bg-[#7ec8e3]"]:hover {
  background: linear-gradient(180deg, #b5deff 0%, #7ecaff 100%) !important;
}
</style>
<style>
/* === Apple‑style system font stack (San Francisco) === */
body, button, input, select, textarea {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Helvetica, Arial, sans-serif;
}
</style>
<style>
.glass-toast {
  position: fixed;
  top: 20px;
  left: 50%;
  transform: translateX(-50%);
  z-index: 9999;
  padding: 12px 24px;
  background: rgba(203, 231, 255, 0.45);
  backdrop-filter: blur(10px);
  border: 1px solid #9FD3FF;
  border-radius: 16px;
  color: #0f172a;
  font-weight: 600;
  box-shadow: 0 4px 20px rgba(0,0,0,0.15);
  opacity: 0;
  transition: opacity 0.3s ease, transform 0.3s ease;
}
.glass-toast.show {
  opacity: 1;
  transform: translateX(-50%) translateY(0);
}
</style>
</head>
<body class="bg-gray-100 text-gray-800">
<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>Vladis Multi-Step Form</title>
<script src="https://cdn.tailwindcss.com"></script>
<script src="https://unpkg.com/i18next@21.6.14/dist/umd/i18next.min.js"></script>
<script>
  function detectLang() {
    const urlParams = new URLSearchParams(window.location.search);
    const urlLang = urlParams.get('lang');
    if (['en', 'es', 'ru'].includes(urlLang)) return urlLang;

    const htmlLang = document.documentElement.lang;
    if (['en', 'es', 'ru'].includes(htmlLang)) return htmlLang;

    const browserLang = (navigator.language || navigator.userLanguage).split('-')[0];
    return ['en', 'es', 'ru'].includes(browserLang) ? browserLang : 'en';
  }

  const lang = detectLang();

  const resources = {
    en: {
      translation: {
        step1: "What are you looking for?",
        step2: "What type of property?",
        step3: "In what area or city?",
        step4: "Approximate monthly budget in $USD",
        step5: "Please leave your contact:",
        buy: "Buy",
        rent: "Rent",
        build: "Build",
        villa: "Villa",
        apartment: "Apartment",
        project: "Project",
        sosua: "Sosúa",
        cabarete: "Cabarete",
        other: "Other",
        name: "Name",
        email: "Email",
        whatsapp: "WhatsApp",
        submit: "Submit",
        thankyou: "✅ Thank you! Your request has been received. We will contact you shortly."
      }
    },
    es: {
      translation: {
        step1: "¿Qué está buscando?",
        step2: "¿Qué tipo de propiedad?",
        step3: "¿En qué zona o ciudad?",
        step4: "Presupuesto mensual aproximado en $USD",
        step5: "Por favor, deje su contacto:",
        buy: "Comprar",
        rent: "Alquilar",
        build: "Construir",
        villa: "Villa",
        apartment: "Apartamento",
        project: "Proyecto",
        sosua: "Sosúa",
        cabarete: "Cabarete",
        other: "Otro",
        name: "Nombre",
        email: "Correo",
        whatsapp: "WhatsApp",
        submit: "Enviar",
        thankyou: "✅ ¡Gracias! Su solicitud ha sido recibida. Nos pondremos en contacto pronto."
      }
    },
    ru: {
      translation: {
        step1: "Что вас интересует?",
        step2: "Какой тип недвижимости?",
        step3: "В каком районе или городе?",
        step4: "Примерный бюджет в $USD",
        step5: "Оставьте, пожалуйста, ваши данные:",
        buy: "Купить",
        rent: "Аренда",
        build: "Строительство",
        villa: "Вилла",
        apartment: "Квартира",
        project: "Проект",
        sosua: "Сосуа",
        cabarete: "Кабарете",
        other: "Другое",
        name: "Имя",
        email: "Email",
        whatsapp: "WhatsApp",
        submit: "Отправить",
        thankyou: "✅ Спасибо! Ваша заявка получена. Мы свяжемся с вами в ближайшее время."
      }
    }
  };

  i18next.init({ lng: lang, debug: false, resources }, function(err, t) {
    window.translations = t;
    renderStep();
  });
</script>
<!-- Injected to apply liquid glass light blue on input fields -->
<style>
input:not([type=checkbox]):not([type=radio]),
select,
textarea {
  background: rgba(126, 200, 227, 0.15); /* light sky blue glass */
  border: 1px solid #7EC8E3;
  transition: border-color 0.2s ease, box-shadow 0.2s ease;
}
input:focus, select:focus, textarea:focus {
  border-color: #7EC8E3;
  box-shadow: 0 0 0 3px rgba(126, 200, 227, 0.45);
}
</style>
<!-- Liquid Glass Gradient for selection buttons -->
<style>
/* Apply gradient blue glass look to any element with bg-[#7ec8e3] class
   except the NEXT button which is bg-blue-600 */
[class*="bg-[#7ec8e3]"] {
  background: linear-gradient(180deg, #cbe7ff 0%, #9fd3ff 100%) !important;
  color: #0f1d31 !important;
  border: 1px solid rgba(159, 211, 255, 0.8);
  backdrop-filter: blur(12px) saturate(180%);
}

[class*="bg-[#7ec8e3]"]:hover {
  background: linear-gradient(180deg, #b5deff 0%, #7ecaff 100%) !important;
}
</style>
<style>
/* === Apple‑style system font stack (San Francisco) === */
body, button, input, select, textarea {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Helvetica, Arial, sans-serif;
}
</style>
<style>
.glass-toast {
  position: fixed;
  top: 20px;
  left: 50%;
  transform: translateX(-50%);
  z-index: 9999;
  padding: 12px 24px;
  background: rgba(203, 231, 255, 0.45);
  backdrop-filter: blur(10px);
  border: 1px solid #9FD3FF;
  border-radius: 16px;
  color: #0f172a;
  font-weight: 600;
  box-shadow: 0 4px 20px rgba(0,0,0,0.15);
  opacity: 0;
  transition: opacity 0.3s ease, transform 0.3s ease;
}
.glass-toast.show {
  opacity: 1;
  transform: translateX(-50%) translateY(0);
}
</style>
</head>
<body class="bg-gray-100 text-gray-800">
<script>
  let currentStep = 1;
let selectedOption = null;
  const totalSteps = 5;
  const steps = [
    {
      title: "Step 1 of 5",
      question: "What are you looking for?",
      options: ["Buy", "Rent", "Build"]
    },
    {
      title: "Step 2 of 5",
      question: "What type of property?",
      options: ["Villa", "Apartment", "Project"]
    },
    {
      title: "Step 3 of 5",
      question: "In what area or city?",
      options: ["Sosúa", "Cabarete", "Punta Cana", "Other"]
    },
    {
      title: "Step 4 of 5",
      question: "Approximate monthly budget in $USD",
      input: "text"
    },
    {
      title: "Step 5 of 5",
      question: "Please leave your contact:",
      inputs: ["Full Name", "Email", "WhatsApp"]
    }
  ];

  function renderStep() {
    document.getElementById("step-title").innerText = steps[currentStep - 1].title;
    document.getElementById("step-question").innerText = steps[currentStep - 1].question;

    const content = document.getElementById("step-content");
    content.innerHTML = "";

    const step = steps[currentStep - 1];

    if (step.options) {
      step.options.forEach(opt => {
        const btn = document.createElement("button");
        btn.className = "w-full py-3 rounded-xl bg-[#7ec8e3] text-gray-900 font-semibold hover:bg-[#6ab2cf] transition";
        btn.innerText = opt;
        btn.onclick = () => selectOption(opt);
        content.appendChild(btn);
      });
    }

    if (step.input) {
      const input = document.createElement("input");
      input.type = step.input;
      input.placeholder = "$ USD";
      input.className = "w-full px-4 py-3 border rounded-xl";
      content.appendChild(input);
    
      input.addEventListener("input", () => localStorage.setItem("step4", input.value));}

    if (step.inputs) {
      step.inputs.forEach(ph => {
        const input = document.createElement("input");
        input.type = "text";
        input.placeholder = ph;
        input.className = "w-full px-4 py-3 border rounded-xl";
        content.appendChild(input);
      });

      const submit = document.createElement("button");
      submit.className = "w-full py-3 mt-2 rounded-xl bg-[#7ec8e3] text-gray-900 font-semibold hover:bg-[#6ab2cf] transition";
      submit.innerText = "Submit";
      submit.onclick = () => {
  const name = content.querySelector('input[placeholder="Full Name"]')?.value.trim() || "N/A";
  const email = content.querySelector('input[placeholder="Email"]')?.value.trim() || "N/A";
  const phone = content.querySelector('input[placeholder="WhatsApp"]')?.value.trim() || "N/A";

  if (!name || !email || !phone) {
    showToast("Please fill in Name, Email and WhatsApp.");
    return;
  }

  const step1 = localStorage.getItem("step1") || "N/A";
  const step2 = localStorage.getItem("step2") || "N/A";
  const step3 = localStorage.getItem("step3") || "N/A";
  const budgetInput = content.querySelector('input[placeholder="$ USD"]')?.value.trim();
  const budget = budgetInput || localStorage.getItem("step4") || "N/A";
  const now = new Date().toLocaleString();

  fetch("https://ipapi.co/json/")
    .then(response => response.json())
    .then(location => {
      const ip = location.ip || "N/A";
      const city = location.city || "Unknown";
      const country = location.country_name || "Unknown";

      const message = `📬 New Client Request – Construction Form

🕒 Date: ${now}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${step1}
🔹 Step 2: ${step2}
🔹 Step 3: ${step3}
🔹 Budget: ${budget}

👤 Name: ${name}
📱 WhatsApp: ${phone}
✉️ Email: ${email}`;

      fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          chat_id: "92750995",
          text: message
        })
      });

      content.innerHTML = `<div class="text-green-600 font-semibold text-center">✅ Thank you! Your request has been received. We will contact you shortly.</div>`;
      document.getElementById("step-question").innerText = "";
      document.getElementById("nextBtn").style.display = "none";
      document.getElementById("backBtn").style.display = "none";
    });
};
      content.appendChild(submit);
    }

    document.getElementById("backBtn").style.display = currentStep === 1 ? "none" : "inline-block";
    document.getElementById("nextBtn").style.display = currentStep < totalSteps ? "inline-block" : "none";
  document.getElementById("nextBtn").disabled = step.options ? true : false;
  }

  function nextStep() {
    if (currentStep < totalSteps) {
      currentStep++;
      renderStep();
    }
  }

  function prevStep() {
    if (currentStep > 1) {
      currentStep--;
      renderStep();
    }
  }

  function selectOption(value) {
  selectedOption = value;
  localStorage.setItem(`step${currentStep}`, value);
  document.getElementById('nextBtn').disabled = false;
    nextStep();
  }

  document.addEventListener("DOMContentLoaded", renderStep);
</script>
<script>
function submitFormTelegram() {
    const steps = document.querySelectorAll('.step');
    const answers = [];

    steps.forEach((step) => {
        const selected = step.querySelector('button.selected');
        const input = step.querySelector('input, textarea');
        if (selected) answers.push(selected.innerText);
        else if (input && input.value) answers.push(input.value);
        else answers.push("N/A");
    });

    const now = new Date();
    const formattedDate = now.toLocaleString();

    fetch("https://ipapi.co/json/")
      .then(response => response.json())
      .then(location => {
        const ip = location.ip || "N/A";
        const city = location.city || "N/A";
        const country = location.country_name || "N/A";

        const message = `
📬 New Form Submission

🕒 Date: ${formattedDate}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${answers[0]}
🔹 Step 2: ${answers[1]}
🔹 Step 3: ${answers[2]}
🔹 Step 4: ${answers[3]}
🔹 Name: ${answers[4]}
🔹 Phone: ${answers[5]}
🔹 Email: ${answers[6]}
`;

        fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
            method: "POST",
            headers: { "Content-Type": "application/json" },
            body: JSON.stringify({
                chat_id: "92750995",
                text: message.trim()
            })
        });

        document.querySelector('.quiz-container').innerHTML = `
            <div style="text-align:center;padding:20px;background:#f8f9fa;border-radius:10px;">
                <h2>✅ Thank You!</h2>
                <p>Your submission has been successfully sent. We'll contact you shortly.</p>
            </div>
        `;
      });
}

// Назначим функцию на кнопку Submit
document.querySelector('.btn-main[onclick="submitForm()"]').setAttribute('onclick', 'submitFormTelegram()');
</script>
<script>
function submitFormTelegram() {
  const steps = document.querySelectorAll('.step');
  const answers = [];

  steps.forEach((step) => {
    const selected = step.querySelector('button.selected');
    const input = step.querySelector('input, textarea');
    if (selected) answers.push(selected.innerText);
    else if (input && input.value) answers.push(input.value);
    else answers.push("N/A");
  });

  const now = new Date().toLocaleString();

  fetch("https://ipapi.co/json/")
    .then(response => response.json())
    .then(location => {
      const ip = location.ip || "N/A";
      const city = location.city || "N/A";
      const country = location.country_name || "N/A";

      const message = `
📬 New Client Request – Construction Form

🕒 Date: ${now}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${answers[0]}
🔹 Step 2: ${answers[1]}
🔹 Step 3: ${answers[2]}
🔹 Budget: ${answers[3]}

👤 Name: ${answers[4]}
📱 WhatsApp: ${answers[5]}
✉️ Email: ${answers[6]}
`;

      fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          chat_id: "92750995",
          text: message
        })
      });

      document.querySelector('.quiz-container').innerHTML = `
        <div style="text-align:center;padding:20px;background:#f8f9fa;border-radius:10px;">
          <h2>✅ Thank You!</h2>
          <p>Your submission has been successfully sent. We'll contact you shortly.</p>
        </div>
      `;
    });
}
</script>
<script>
function submitFormTelegram() {
  const steps = document.querySelectorAll('.step');
  const answers = [];

  steps.forEach((step) => {
    const selected = step.querySelector('button.selected');
    const input = step.querySelector('input, textarea');
    if (selected) answers.push(selected.innerText);
    else if (input && input.value) answers.push(input.value);
    else answers.push("N/A");
  });

  const now = new Date().toLocaleString();

  fetch("https://ipapi.co/json/")
    .then(response => response.json())
    .then(location => {
      const ip = location.ip || "N/A";
      const city = "Málaga";
      const country = "Spain";

      const message = `📬 New Client Request – Construction Form

🕒 Date: ${now}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${answers[0]}
🔹 Step 2: ${answers[1]}
🔹 Step 3: ${answers[2]}
🔹 Budget: ${answers[3]}

👤 Name: ${answers[4]}
📱 WhatsApp: ${answers[5]}
✉️ Email: ${answers[6]}`;

      fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          chat_id: "92750995",
          text: message
        })
      });

      document.querySelector('.quiz-container').innerHTML = `
        <div style="text-align:center;padding:20px;background:#f8f9fa;border-radius:10px;">
          <h2>✅ Thank You!</h2>
          <p>Your submission has been successfully sent. We'll contact you shortly.</p>
        </div>
      `;
    });
}
</script>
<script>
function showToast(message) {
  let toast = document.getElementById("glass-toast");
  if (!toast) {
    toast = document.createElement("div");
    toast.id = "glass-toast";
    toast.className = "glass-toast";
    document.body.appendChild(toast);
  }
  toast.innerText = message;
  toast.classList.add("show");
  setTimeout(() => {
    toast.classList.remove("show");
  }, 4000);
}
</script>
<script>
const btn = document.getElementById("mobile-menu-btn");
if(btn){
  const navLinks = btn.nextElementSibling;
  btn.addEventListener("click", ()=> {
    navLinks.classList.toggle("hidden");
  });
}
</script>
</body>
</html>
<script>
function submitFormTelegram() {
    const steps = document.querySelectorAll('.step');
    const answers = [];

    steps.forEach((step) => {
        const selected = step.querySelector('button.selected');
        const input = step.querySelector('input, textarea');
        if (selected) answers.push(selected.innerText);
        else if (input && input.value) answers.push(input.value);
        else answers.push("N/A");
    });

    const now = new Date();
    const formattedDate = now.toLocaleString();

    fetch("https://ipapi.co/json/")
      .then(response => response.json())
      .then(location => {
        const ip = location.ip || "N/A";
        const city = location.city || "N/A";
        const country = location.country_name || "N/A";

        const message = `
📬 New Form Submission

🕒 Date: ${formattedDate}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${answers[0]}
🔹 Step 2: ${answers[1]}
🔹 Step 3: ${answers[2]}
🔹 Step 4: ${answers[3]}
🔹 Name: ${answers[4]}
🔹 Phone: ${answers[5]}
🔹 Email: ${answers[6]}
`;

        fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
            method: "POST",
            headers: { "Content-Type": "application/json" },
            body: JSON.stringify({
                chat_id: "92750995",
                text: message.trim()
            })
        });

        document.querySelector('.quiz-container').innerHTML = `
            <div style="text-align:center;padding:20px;background:#f8f9fa;border-radius:10px;">
                <h2>✅ Thank You!</h2>
                <p>Your submission has been successfully sent. We'll contact you shortly.</p>
            </div>
        `;
      });
}

// Назначим функцию на кнопку Submit
document.querySelector('.btn-main[onclick="submitForm()"]').setAttribute('onclick', 'submitFormTelegram()');
</script>
<script>
function submitFormTelegram() {
  const steps = document.querySelectorAll('.step');
  const answers = [];

  steps.forEach((step) => {
    const selected = step.querySelector('button.selected');
    const input = step.querySelector('input, textarea');
    if (selected) answers.push(selected.innerText);
    else if (input && input.value) answers.push(input.value);
    else answers.push("N/A");
  });

  const now = new Date().toLocaleString();

  fetch("https://ipapi.co/json/")
    .then(response => response.json())
    .then(location => {
      const ip = location.ip || "N/A";
      const city = location.city || "N/A";
      const country = location.country_name || "N/A";

      const message = `
📬 New Client Request – Construction Form

🕒 Date: ${now}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${answers[0]}
🔹 Step 2: ${answers[1]}
🔹 Step 3: ${answers[2]}
🔹 Budget: ${answers[3]}

👤 Name: ${answers[4]}
📱 WhatsApp: ${answers[5]}
✉️ Email: ${answers[6]}
`;

      fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          chat_id: "92750995",
          text: message
        })
      });

      document.querySelector('.quiz-container').innerHTML = `
        <div style="text-align:center;padding:20px;background:#f8f9fa;border-radius:10px;">
          <h2>✅ Thank You!</h2>
          <p>Your submission has been successfully sent. We'll contact you shortly.</p>
        </div>
      `;
    });
}
</script>
<script>
function submitFormTelegram() {
  const steps = document.querySelectorAll('.step');
  const answers = [];

  steps.forEach((step) => {
    const selected = step.querySelector('button.selected');
    const input = step.querySelector('input, textarea');
    if (selected) answers.push(selected.innerText);
    else if (input && input.value) answers.push(input.value);
    else answers.push("N/A");
  });

  const now = new Date().toLocaleString();

  fetch("https://ipapi.co/json/")
    .then(response => response.json())
    .then(location => {
      const ip = location.ip || "N/A";
      const city = "Málaga";
      const country = "Spain";

      const message = `📬 New Client Request – Construction Form

🕒 Date: ${now}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${answers[0]}
🔹 Step 2: ${answers[1]}
🔹 Step 3: ${answers[2]}
🔹 Budget: ${answers[3]}

👤 Name: ${answers[4]}
📱 WhatsApp: ${answers[5]}
✉️ Email: ${answers[6]}`;

      fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          chat_id: "92750995",
          text: message
        })
      });

      document.querySelector('.quiz-container').innerHTML = `
        <div style="text-align:center;padding:20px;background:#f8f9fa;border-radius:10px;">
          <h2>✅ Thank You!</h2>
          <p>Your submission has been successfully sent. We'll contact you shortly.</p>
        </div>
      `;
    });
}
</script>
<script>
function showToast(message) {
  let toast = document.getElementById("glass-toast");
  if (!toast) {
    toast = document.createElement("div");
    toast.id = "glass-toast";
    toast.className = "glass-toast";
    document.body.appendChild(toast);
  }
  toast.innerText = message;
  toast.classList.add("show");
  setTimeout(() => {
    toast.classList.remove("show");
  }, 4000);
}
</script>
<script>
const btn = document.getElementById("mobile-menu-btn");
if(btn){
  const navLinks = btn.nextElementSibling;
  btn.addEventListener("click", ()=> {
    navLinks.classList.toggle("hidden");
  });
}
</script>
</body>
</html>
<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>Vladis Multi-Step Form</title>
<script src="https://cdn.tailwindcss.com"></script>
<script src="https://unpkg.com/i18next@21.6.14/dist/umd/i18next.min.js"></script>
<script>
  function detectLang() {
    const urlParams = new URLSearchParams(window.location.search);
    const urlLang = urlParams.get('lang');
    if (['en', 'es', 'ru'].includes(urlLang)) return urlLang;

    const htmlLang = document.documentElement.lang;
    if (['en', 'es', 'ru'].includes(htmlLang)) return htmlLang;

    const browserLang = (navigator.language || navigator.userLanguage).split('-')[0];
    return ['en', 'es', 'ru'].includes(browserLang) ? browserLang : 'en';
  }

  const lang = detectLang();

  const resources = {
    en: {
      translation: {
        step1: "What are you looking for?",
        step2: "What type of property?",
        step3: "In what area or city?",
        step4: "Approximate monthly budget in $USD",
        step5: "Please leave your contact:",
        buy: "Buy",
        rent: "Rent",
        build: "Build",
        villa: "Villa",
        apartment: "Apartment",
        project: "Project",
        sosua: "Sosúa",
        cabarete: "Cabarete",
        other: "Other",
        name: "Name",
        email: "Email",
        whatsapp: "WhatsApp",
        submit: "Submit",
        thankyou: "✅ Thank you! Your request has been received. We will contact you shortly."
      }
    },
    es: {
      translation: {
        step1: "¿Qué está buscando?",
        step2: "¿Qué tipo de propiedad?",
        step3: "¿En qué zona o ciudad?",
        step4: "Presupuesto mensual aproximado en $USD",
        step5: "Por favor, deje su contacto:",
        buy: "Comprar",
        rent: "Alquilar",
        build: "Construir",
        villa: "Villa",
        apartment: "Apartamento",
        project: "Proyecto",
        sosua: "Sosúa",
        cabarete: "Cabarete",
        other: "Otro",
        name: "Nombre",
        email: "Correo",
        whatsapp: "WhatsApp",
        submit: "Enviar",
        thankyou: "✅ ¡Gracias! Su solicitud ha sido recibida. Nos pondremos en contacto pronto."
      }
    },
    ru: {
      translation: {
        step1: "Что вас интересует?",
        step2: "Какой тип недвижимости?",
        step3: "В каком районе или городе?",
        step4: "Примерный бюджет в $USD",
        step5: "Оставьте, пожалуйста, ваши данные:",
        buy: "Купить",
        rent: "Аренда",
        build: "Строительство",
        villa: "Вилла",
        apartment: "Квартира",
        project: "Проект",
        sosua: "Сосуа",
        cabarete: "Кабарете",
        other: "Другое",
        name: "Имя",
        email: "Email",
        whatsapp: "WhatsApp",
        submit: "Отправить",
        thankyou: "✅ Спасибо! Ваша заявка получена. Мы свяжемся с вами в ближайшее время."
      }
    }
  };

  i18next.init({ lng: lang, debug: false, resources }, function(err, t) {
    window.translations = t;
    renderStep();
  });
</script>
<!-- Injected to apply liquid glass light blue on input fields -->
<style>
input:not([type=checkbox]):not([type=radio]),
select,
textarea {
  background: rgba(126, 200, 227, 0.15); /* light sky blue glass */
  border: 1px solid #7EC8E3;
  transition: border-color 0.2s ease, box-shadow 0.2s ease;
}
input:focus, select:focus, textarea:focus {
  border-color: #7EC8E3;
  box-shadow: 0 0 0 3px rgba(126, 200, 227, 0.45);
}
</style>
<!-- Liquid Glass Gradient for selection buttons -->
<style>
/* Apply gradient blue glass look to any element with bg-[#7ec8e3] class
   except the NEXT button which is bg-blue-600 */
[class*="bg-[#7ec8e3]"] {
  background: linear-gradient(180deg, #cbe7ff 0%, #9fd3ff 100%) !important;
  color: #0f1d31 !important;
  border: 1px solid rgba(159, 211, 255, 0.8);
  backdrop-filter: blur(12px) saturate(180%);
}

[class*="bg-[#7ec8e3]"]:hover {
  background: linear-gradient(180deg, #b5deff 0%, #7ecaff 100%) !important;
}
</style>
<style>
/* === Apple‑style system font stack (San Francisco) === */
body, button, input, select, textarea {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Helvetica, Arial, sans-serif;
}
</style>
<style>
.glass-toast {
  position: fixed;
  top: 20px;
  left: 50%;
  transform: translateX(-50%);
  z-index: 9999;
  padding: 12px 24px;
  background: rgba(203, 231, 255, 0.45);
  backdrop-filter: blur(10px);
  border: 1px solid #9FD3FF;
  border-radius: 16px;
  color: #0f172a;
  font-weight: 600;
  box-shadow: 0 4px 20px rgba(0,0,0,0.15);
  opacity: 0;
  transition: opacity 0.3s ease, transform 0.3s ease;
}
.glass-toast.show {
  opacity: 1;
  transform: translateX(-50%) translateY(0);
}
</style>
</head>
<body class="bg-gray-100 text-gray-800">
<script>
  let currentStep = 1;
let selectedOption = null;
  const totalSteps = 5;
  const steps = [
    {
      title: "Step 1 of 5",
      question: "What are you looking for?",
      options: ["Buy", "Rent", "Build"]
    },
    {
      title: "Step 2 of 5",
      question: "What type of property?",
      options: ["Villa", "Apartment", "Project"]
    },
    {
      title: "Step 3 of 5",
      question: "In what area or city?",
      options: ["Sosúa", "Cabarete", "Punta Cana", "Other"]
    },
    {
      title: "Step 4 of 5",
      question: "Approximate monthly budget in $USD",
      input: "text"
    },
    {
      title: "Step 5 of 5",
      question: "Please leave your contact:",
      inputs: ["Full Name", "Email", "WhatsApp"]
    }
  ];

  function renderStep() {
    document.getElementById("step-title").innerText = steps[currentStep - 1].title;
    document.getElementById("step-question").innerText = steps[currentStep - 1].question;

    const content = document.getElementById("step-content");
    content.innerHTML = "";

    const step = steps[currentStep - 1];

    if (step.options) {
      step.options.forEach(opt => {
        const btn = document.createElement("button");
        btn.className = "w-full py-3 rounded-xl bg-[#7ec8e3] text-gray-900 font-semibold hover:bg-[#6ab2cf] transition";
        btn.innerText = opt;
        btn.onclick = () => selectOption(opt);
        content.appendChild(btn);
      });
    }

    if (step.input) {
      const input = document.createElement("input");
      input.type = step.input;
      input.placeholder = "$ USD";
      input.className = "w-full px-4 py-3 border rounded-xl";
      content.appendChild(input);
    
      input.addEventListener("input", () => localStorage.setItem("step4", input.value));}

    if (step.inputs) {
      step.inputs.forEach(ph => {
        const input = document.createElement("input");
        input.type = "text";
        input.placeholder = ph;
        input.className = "w-full px-4 py-3 border rounded-xl";
        content.appendChild(input);
      });

      const submit = document.createElement("button");
      submit.className = "w-full py-3 mt-2 rounded-xl bg-[#7ec8e3] text-gray-900 font-semibold hover:bg-[#6ab2cf] transition";
      submit.innerText = "Submit";
      submit.onclick = () => {
  const name = content.querySelector('input[placeholder="Full Name"]')?.value.trim() || "N/A";
  const email = content.querySelector('input[placeholder="Email"]')?.value.trim() || "N/A";
  const phone = content.querySelector('input[placeholder="WhatsApp"]')?.value.trim() || "N/A";

  if (!name || !email || !phone) {
    showToast("Please fill in Name, Email and WhatsApp.");
    return;
  }

  const step1 = localStorage.getItem("step1") || "N/A";
  const step2 = localStorage.getItem("step2") || "N/A";
  const step3 = localStorage.getItem("step3") || "N/A";
  const budgetInput = content.querySelector('input[placeholder="$ USD"]')?.value.trim();
  const budget = budgetInput || localStorage.getItem("step4") || "N/A";
  const now = new Date().toLocaleString();

  fetch("https://ipapi.co/json/")
    .then(response => response.json())
    .then(location => {
      const ip = location.ip || "N/A";
      const city = location.city || "Unknown";
      const country = location.country_name || "Unknown";

      const message = `📬 New Client Request – Construction Form

🕒 Date: ${now}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${step1}
🔹 Step 2: ${step2}
🔹 Step 3: ${step3}
🔹 Budget: ${budget}

👤 Name: ${name}
📱 WhatsApp: ${phone}
✉️ Email: ${email}`;

      fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          chat_id: "92750995",
          text: message
        })
      });

      content.innerHTML = `<div class="text-green-600 font-semibold text-center">✅ Thank you! Your request has been received. We will contact you shortly.</div>`;
      document.getElementById("step-question").innerText = "";
      document.getElementById("nextBtn").style.display = "none";
      document.getElementById("backBtn").style.display = "none";
    });
};
      content.appendChild(submit);
    }

    document.getElementById("backBtn").style.display = currentStep === 1 ? "none" : "inline-block";
    document.getElementById("nextBtn").style.display = currentStep < totalSteps ? "inline-block" : "none";
  document.getElementById("nextBtn").disabled = step.options ? true : false;
  }

  function nextStep() {
    if (currentStep < totalSteps) {
      currentStep++;
      renderStep();
    }
  }

  function prevStep() {
    if (currentStep > 1) {
      currentStep--;
      renderStep();
    }
  }

  function selectOption(value) {
  selectedOption = value;
  localStorage.setItem(`step${currentStep}`, value);
  document.getElementById('nextBtn').disabled = false;
    nextStep();
  }

  document.addEventListener("DOMContentLoaded", renderStep);
</script>
<script>
function submitFormTelegram() {
    const steps = document.querySelectorAll('.step');
    const answers = [];

    steps.forEach((step) => {
        const selected = step.querySelector('button.selected');
        const input = step.querySelector('input, textarea');
        if (selected) answers.push(selected.innerText);
        else if (input && input.value) answers.push(input.value);
        else answers.push("N/A");
    });

    const now = new Date();
    const formattedDate = now.toLocaleString();

    fetch("https://ipapi.co/json/")
      .then(response => response.json())
      .then(location => {
        const ip = location.ip || "N/A";
        const city = location.city || "N/A";
        const country = location.country_name || "N/A";

        const message = `
📬 New Form Submission

🕒 Date: ${formattedDate}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${answers[0]}
🔹 Step 2: ${answers[1]}
🔹 Step 3: ${answers[2]}
🔹 Step 4: ${answers[3]}
🔹 Name: ${answers[4]}
🔹 Phone: ${answers[5]}
🔹 Email: ${answers[6]}
`;

        fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
            method: "POST",
            headers: { "Content-Type": "application/json" },
            body: JSON.stringify({
                chat_id: "92750995",
                text: message.trim()
            })
        });

        document.querySelector('.quiz-container').innerHTML = `
            <div style="text-align:center;padding:20px;background:#f8f9fa;border-radius:10px;">
                <h2>✅ Thank You!</h2>
                <p>Your submission has been successfully sent. We'll contact you shortly.</p>
            </div>
        `;
      });
}

// Назначим функцию на кнопку Submit
document.querySelector('.btn-main[onclick="submitForm()"]').setAttribute('onclick', 'submitFormTelegram()');
</script>
<script>
function submitFormTelegram() {
  const steps = document.querySelectorAll('.step');
  const answers = [];

  steps.forEach((step) => {
    const selected = step.querySelector('button.selected');
    const input = step.querySelector('input, textarea');
    if (selected) answers.push(selected.innerText);
    else if (input && input.value) answers.push(input.value);
    else answers.push("N/A");
  });

  const now = new Date().toLocaleString();

  fetch("https://ipapi.co/json/")
    .then(response => response.json())
    .then(location => {
      const ip = location.ip || "N/A";
      const city = location.city || "N/A";
      const country = location.country_name || "N/A";

      const message = `
📬 New Client Request – Construction Form

🕒 Date: ${now}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${answers[0]}
🔹 Step 2: ${answers[1]}
🔹 Step 3: ${answers[2]}
🔹 Budget: ${answers[3]}

👤 Name: ${answers[4]}
📱 WhatsApp: ${answers[5]}
✉️ Email: ${answers[6]}
`;

      fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          chat_id: "92750995",
          text: message
        })
      });

      document.querySelector('.quiz-container').innerHTML = `
        <div style="text-align:center;padding:20px;background:#f8f9fa;border-radius:10px;">
          <h2>✅ Thank You!</h2>
          <p>Your submission has been successfully sent. We'll contact you shortly.</p>
        </div>
      `;
    });
}
</script>
<script>
function submitFormTelegram() {
  const steps = document.querySelectorAll('.step');
  const answers = [];

  steps.forEach((step) => {
    const selected = step.querySelector('button.selected');
    const input = step.querySelector('input, textarea');
    if (selected) answers.push(selected.innerText);
    else if (input && input.value) answers.push(input.value);
    else answers.push("N/A");
  });

  const now = new Date().toLocaleString();

  fetch("https://ipapi.co/json/")
    .then(response => response.json())
    .then(location => {
      const ip = location.ip || "N/A";
      const city = "Málaga";
      const country = "Spain";

      const message = `📬 New Client Request – Construction Form

🕒 Date: ${now}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${answers[0]}
🔹 Step 2: ${answers[1]}
🔹 Step 3: ${answers[2]}
🔹 Budget: ${answers[3]}

👤 Name: ${answers[4]}
📱 WhatsApp: ${answers[5]}
✉️ Email: ${answers[6]}`;

      fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          chat_id: "92750995",
          text: message
        })
      });

      document.querySelector('.quiz-container').innerHTML = `
        <div style="text-align:center;padding:20px;background:#f8f9fa;border-radius:10px;">
          <h2>✅ Thank You!</h2>
          <p>Your submission has been successfully sent. We'll contact you shortly.</p>
        </div>
      `;
    });
}
</script>
<script>
function showToast(message) {
  let toast = document.getElementById("glass-toast");
  if (!toast) {
    toast = document.createElement("div");
    toast.id = "glass-toast";
    toast.className = "glass-toast";
    document.body.appendChild(toast);
  }
  toast.innerText = message;
  toast.classList.add("show");
  setTimeout(() => {
    toast.classList.remove("show");
  }, 4000);
}
</script>
<script>
const btn = document.getElementById("mobile-menu-btn");
if(btn){
  const navLinks = btn.nextElementSibling;
  btn.addEventListener("click", ()=> {
    navLinks.classList.toggle("hidden");
  });
}
</script>
</body>
</html>
<script>
function submitFormTelegram() {
    const steps = document.querySelectorAll('.step');
    const answers = [];

    steps.forEach((step) => {
        const selected = step.querySelector('button.selected');
        const input = step.querySelector('input, textarea');
        if (selected) answers.push(selected.innerText);
        else if (input && input.value) answers.push(input.value);
        else answers.push("N/A");
    });

    const now = new Date();
    const formattedDate = now.toLocaleString();

    fetch("https://ipapi.co/json/")
      .then(response => response.json())
      .then(location => {
        const ip = location.ip || "N/A";
        const city = location.city || "N/A";
        const country = location.country_name || "N/A";

        const message = `
📬 New Form Submission

🕒 Date: ${formattedDate}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${answers[0]}
🔹 Step 2: ${answers[1]}
🔹 Step 3: ${answers[2]}
🔹 Step 4: ${answers[3]}
🔹 Name: ${answers[4]}
🔹 Phone: ${answers[5]}
🔹 Email: ${answers[6]}
`;

        fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
            method: "POST",
            headers: { "Content-Type": "application/json" },
            body: JSON.stringify({
                chat_id: "92750995",
                text: message.trim()
            })
        });

        document.querySelector('.quiz-container').innerHTML = `
            <div style="text-align:center;padding:20px;background:#f8f9fa;border-radius:10px;">
                <h2>✅ Thank You!</h2>
                <p>Your submission has been successfully sent. We'll contact you shortly.</p>
            </div>
        `;
      });
}

// Назначим функцию на кнопку Submit
document.querySelector('.btn-main[onclick="submitForm()"]').setAttribute('onclick', 'submitFormTelegram()');
</script>
<script>
function submitFormTelegram() {
  const steps = document.querySelectorAll('.step');
  const answers = [];

  steps.forEach((step) => {
    const selected = step.querySelector('button.selected');
    const input = step.querySelector('input, textarea');
    if (selected) answers.push(selected.innerText);
    else if (input && input.value) answers.push(input.value);
    else answers.push("N/A");
  });

  const now = new Date().toLocaleString();

  fetch("https://ipapi.co/json/")
    .then(response => response.json())
    .then(location => {
      const ip = location.ip || "N/A";
      const city = location.city || "N/A";
      const country = location.country_name || "N/A";

      const message = `
📬 New Client Request – Construction Form

🕒 Date: ${now}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${answers[0]}
🔹 Step 2: ${answers[1]}
🔹 Step 3: ${answers[2]}
🔹 Budget: ${answers[3]}

👤 Name: ${answers[4]}
📱 WhatsApp: ${answers[5]}
✉️ Email: ${answers[6]}
`;

      fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          chat_id: "92750995",
          text: message
        })
      });

      document.querySelector('.quiz-container').innerHTML = `
        <div style="text-align:center;padding:20px;background:#f8f9fa;border-radius:10px;">
          <h2>✅ Thank You!</h2>
          <p>Your submission has been successfully sent. We'll contact you shortly.</p>
        </div>
      `;
    });
}
</script>
<script>
function submitFormTelegram() {
  const steps = document.querySelectorAll('.step');
  const answers = [];

  steps.forEach((step) => {
    const selected = step.querySelector('button.selected');
    const input = step.querySelector('input, textarea');
    if (selected) answers.push(selected.innerText);
    else if (input && input.value) answers.push(input.value);
    else answers.push("N/A");
  });

  const now = new Date().toLocaleString();

  fetch("https://ipapi.co/json/")
    .then(response => response.json())
    .then(location => {
      const ip = location.ip || "N/A";
      const city = "Málaga";
      const country = "Spain";

      const message = `📬 New Client Request – Construction Form

🕒 Date: ${now}
🌐 IP: ${ip}
🏙️ Location: ${city}, ${country}

🔹 Step 1: ${answers[0]}
🔹 Step 2: ${answers[1]}
🔹 Step 3: ${answers[2]}
🔹 Budget: ${answers[3]}

👤 Name: ${answers[4]}
📱 WhatsApp: ${answers[5]}
✉️ Email: ${answers[6]}`;

      fetch("https://api.telegram.org/bot7818379129:AAHbmWccPNUk1HyWsA3tgXiYXnFCnyqoPR0/sendMessage", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          chat_id: "92750995",
          text: message
        })
      });

      document.querySelector('.quiz-container').innerHTML = `
        <div style="text-align:center;padding:20px;background:#f8f9fa;border-radius:10px;">
          <h2>✅ Thank You!</h2>
          <p>Your submission has been successfully sent. We'll contact you shortly.</p>
        </div>
      `;
    });
}
</script>
<script>
function showToast(message) {
  let toast = document.getElementById("glass-toast");
  if (!toast) {
    toast = document.createElement("div");
    toast.id = "glass-toast";
    toast.className = "glass-toast";
    document.body.appendChild(toast);
  }
  toast.innerText = message;
  toast.classList.add("show");
  setTimeout(() => {
    toast.classList.remove("show");
  }, 4000);
}
</script>
<script>
const btn = document.getElementById("mobile-menu-btn");
if(btn){
  const navLinks = btn.nextElementSibling;
  btn.addEventListener("click", ()=> {
    navLinks.classList.toggle("hidden");
  });
}
</script>
</body>
</html>
