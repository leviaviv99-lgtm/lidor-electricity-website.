# lidor-electricity-website.[lf_electricity_landing.html](https://github.com/user-attachments/files/22100887/lf_electricity_landing.html)
<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>L.F ELECTRICITY - פולבש הנדסת חשמל | פתרונות חשמל מקצועיים</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            background: linear-gradient(135deg, #0f0f23 0%, #1a1a2e 50%, #16213e 100%);
            color: #fff;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            background: rgba(0, 0, 0, 0.3);
            backdrop-filter: blur(10px);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            transition: all 0.3s ease;
        }

        header.scrolled {
            background: rgba(0, 0, 0, 0.8);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            background: linear-gradient(45deg, #ffd700, #ffed4e);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 10px rgba(255, 215, 0, 0.3);
        }

        .contact-btn {
            background: linear-gradient(45deg, #25d366, #128c7e);
            color: white;
            padding: 12px 24px;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            font-weight: bold;
            font-size: 1rem;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .contact-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(37, 211, 102, 0.3);
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grid" width="10" height="10" patternUnits="userSpaceOnUse"><path d="M 10 0 L 0 0 0 10" fill="none" stroke="%23333" stroke-width="0.5" opacity="0.3"/></pattern></defs><rect width="100" height="100" fill="url(%23grid)"/></svg>');
            opacity: 0.1;
        }

        .hero-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
            position: relative;
            z-index: 2;
        }

        .hero-text h1 {
            font-size: 3.5rem;
            font-weight: 800;
            margin-bottom: 1rem;
            background: linear-gradient(45deg, #ffd700, #fff, #00d4ff);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            line-height: 1.2;
            animation: glow 3s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from { filter: drop-shadow(0 0 20px rgba(255, 215, 0, 0.3)); }
            to { filter: drop-shadow(0 0 30px rgba(0, 212, 255, 0.5)); }
        }

        .hero-text .subtitle {
            font-size: 1.4rem;
            color: #b0b0b0;
            margin-bottom: 2rem;
            font-weight: 300;
        }

        .hero-visual {
            position: relative;
            height: 400px;
        }

        .electric-animation {
            position: absolute;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at center, rgba(255, 215, 0, 0.1) 0%, transparent 70%);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 8rem;
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); opacity: 0.7; }
            50% { transform: scale(1.05); opacity: 1; }
        }

        /* Services Section */
        .services {
            padding: 6rem 0;
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.05) 0%, rgba(255, 255, 255, 0.02) 100%);
        }

        .section-title {
            text-align: center;
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 3rem;
            background: linear-gradient(45deg, #ffd700, #fff);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-bottom: 4rem;
        }

        .service-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 2rem;
            text-align: center;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 215, 0, 0.1), transparent);
            transition: left 0.5s ease;
        }

        .service-card:hover::before {
            left: 100%;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(255, 215, 0, 0.2);
        }

        .service-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
            color: #ffd700;
        }

        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: #fff;
        }

        .service-card p {
            color: #b0b0b0;
            line-height: 1.6;
        }

        /* About Section */
        .about {
            padding: 6rem 0;
            background: rgba(0, 0, 0, 0.2);
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 4rem;
            align-items: center;
        }

        .about-image {
            position: relative;
            height: 300px;
            background: linear-gradient(45deg, #ffd700, #00d4ff);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            color: #fff;
        }

        .about-text h2 {
            font-size: 2.5rem;
            margin-bottom: 2rem;
            color: #ffd700;
        }

        .about-text p {
            color: #b0b0b0;
            font-size: 1.1rem;
            margin-bottom: 1.5rem;
        }

        /* Why Choose Us */
        .why-us {
            padding: 6rem 0;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .feature-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 1.5rem;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            transition: all 0.3s ease;
        }

        .feature-item:hover {
            background: rgba(255, 215, 0, 0.1);
            transform: translateX(10px);
        }

        .feature-icon {
            font-size: 2rem;
            color: #25d366;
        }

        .feature-text {
            font-size: 1.1rem;
            color: #fff;
        }

        /* Contact Section */
        .contact {
            padding: 6rem 0;
            background: linear-gradient(135deg, rgba(37, 211, 102, 0.1) 0%, rgba(18, 140, 126, 0.1) 100%);
        }

        .contact-content {
            text-align: center;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 3rem;
            margin: 3rem 0;
            flex-wrap: wrap;
        }

        .contact-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1rem;
        }

        .contact-item .icon {
            font-size: 2rem;
            color: #25d366;
        }

        .contact-item .text {
            font-size: 1.1rem;
            color: #fff;
        }

        .whatsapp-btn {
            background: linear-gradient(45deg, #25d366, #128c7e);
            color: white;
            padding: 20px 40px;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            font-weight: bold;
            font-size: 1.2rem;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            margin-top: 2rem;
        }

        .whatsapp-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 30px rgba(37, 211, 102, 0.4);
        }

        /* Animations */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            animation: fadeIn 0.8s ease forwards;
        }

        @keyframes fadeIn {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hero-content {
                grid-template-columns: 1fr;
                gap: 2rem;
                text-align: center;
            }

            .hero-text h1 {
                font-size: 2.5rem;
            }

            .about-content {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .contact-info {
                flex-direction: column;
                gap: 2rem;
            }

            .services-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Floating Elements */
        .floating-elements {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }

        .floating-element {
            position: absolute;
            color: rgba(255, 215, 0, 0.1);
            animation: float 6s ease-in-out infinite;
        }

        .floating-element:nth-child(1) { top: 20%; left: 10%; animation-delay: 0s; }
        .floating-element:nth-child(2) { top: 60%; right: 15%; animation-delay: 2s; }
        .floating-element:nth-child(3) { bottom: 30%; left: 20%; animation-delay: 4s; }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }
    </style>
</head>
<body>
    <div class="floating-elements">
        <div class="floating-element">⚡</div>
        <div class="floating-element">🔌</div>
        <div class="floating-element">💡</div>
    </div>

    <header id="header">
        <div class="container">
            <nav>
                <div class="logo">⚡ L.F ELECTRICITY</div>
                <a href="#contact" class="contact-btn">
                    📞 צור קשר
                </a>
            </nav>
        </div>
    </header>

    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text fade-in">
                    <h1>פולבש הנדסת חשמל</h1>
                    <p class="subtitle">פתרונות חשמל ותקשורת בהתאמה אישית לכל פרויקט</p>
                    <p style="font-size: 1.2rem; color: #ccc; margin-bottom: 2rem;">
                        מהנדס חשמל מוסמך (B.Sc) עם רישיון חשמלאי מהנדס<br>
                        מעניק שירותי תכנון, ייעוץ וליווי פרויקטים מקצועיים
                    </p>
                    <a href="#contact" class="whatsapp-btn">
                        💬 התחל פרויקט עכשיו
                    </a>
                </div>
                <div class="hero-visual fade-in">
                    <div class="electric-animation">
                        ⚡
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="services">
        <div class="container">
            <h2 class="section-title fade-in">השירותים שלי</h2>
            <div class="services-grid">
                <div class="service-card fade-in">
                    <div class="service-icon">🏗️</div>
                    <h3>תכנון מערכות חשמל</h3>
                    <p>תכנון מקצועי לבנייה חדשה, תמ"א 38 והתחדשות עירונית. פתרונות מותאמים לכל סוג פרויקט.</p>
                </div>
                <div class="service-card fade-in">
                    <div class="service-icon">💡</div>
                    <h3>ייעוץ מקצועי</h3>
                    <p>ייעוץ מומחה ליזמים, קבלנים ואדריכלים. ליווי צמוד בכל שלבי הפרויקט.</p>
                </div>
                <div class="service-card fade-in">
                    <div class="service-icon">📋</div>
                    <h3>בדיקות והפקת תכניות</h3>
                    <p>הפקת תכניות חשמל מקצועיות לאישור כלל הרשויות, בזק הוט וחברת חשמל.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="about">
        <div class="container">
            <div class="about-content">
                <div class="about-image fade-in">
                    👨‍💼
                </div>
                <div class="about-text fade-in">
                    <h2>מי אני?</h2>
                    <p>אני לידור פולבש, מהנדס חשמל מוסמך (B.Sc) ובעל רישיון <strong>חשמלאי מהנדס</strong>.</p>
                    <p>מעניק שירותי תכנון, ייעוץ וליווי פרויקטים במערכות חשמל ותקשורת משלב הרישוי ועד הביצוע.</p>
                    <p><strong>מתמחה בעבודה עבור:</strong></p>
                    <p>🏗️ יזמים • 🏢 חברות בנייה • 🏠 בעלי נכסים פרטיים</p>
                </div>
            </div>
        </div>
    </section>

    <section class="why-us">
        <div class="container">
            <h2 class="section-title fade-in">למה לבחור בי?</h2>
            <div class="features-grid">
                <div class="feature-item fade-in">
                    <div class="feature-icon">✔️</div>
                    <div class="feature-text">ניסיון בעבודה מול יזמים וקבלנים</div>
                </div>
                <div class="feature-item fade-in">
                    <div class="feature-icon">✔️</div>
                    <div class="feature-text">התאמה אישית לכל פרויקט</div>
                </div>
                <div class="feature-item fade-in">
                    <div class="feature-icon">✔️</div>
                    <div class="feature-text">ליווי צמוד עד לאישור סופי</div>
                </div>
                <div class="feature-item fade-in">
                    <div class="feature-icon">✔️</div>
                    <div class="feature-text">זמינות גבוהה ושירות מקצועי</div>
                </div>
            </div>
        </div>
    </section>

    <section class="contact" id="contact">
        <div class="container">
            <div class="contact-content">
                <h2 class="section-title fade-in">צור קשר עכשיו</h2>
                <p class="fade-in" style="font-size: 1.2rem; margin-bottom: 2rem; color: #ccc;">
                    מוכן להתחיל את הפרויקט שלך? בוא נדבר!
                </p>
                <div class="contact-info">
                    <div class="contact-item fade-in">
                        <div class="icon">📞</div>
                        <div class="text">052-2328567</div>
                    </div>
                    <div class="contact-item fade-in">
                        <div class="icon">📧</div>
                        <div class="text">fulbashelectricity@gmail.com</div>
                    </div>
                </div>
                <a href="https://wa.me/972522328567" class="whatsapp-btn fade-in" target="_blank">
                    📱 צור קשר בווטסאפ
                </a>
            </div>
        </div>
    </section>

    <script>
        // Header scroll effect
        window.addEventListener('scroll', () => {
            const header = document.getElementById('header');
            if (window.scrollY > 100) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Intersection Observer for animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animationDelay = '0.1s';
                    entry.target.classList.add('fade-in');
                }
            });
        }, observerOptions);

        // Observe all elements with fade-in class
        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });

        // Add some interactive lightning effects
        document.addEventListener('mousemove', (e) => {
            const electricElements = document.querySelectorAll('.electric-animation');
            electricElements.forEach(el => {
                const rect = el.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                
                if (x > 0 && x < rect.width && y > 0 && y < rect.height) {
                    el.style.filter = 'drop-shadow(0 0 20px #ffd700) drop-shadow(0 0 40px #00d4ff)';
                } else {
                    el.style.filter = '';
                }
            });
        });
    </script>
</body>
</html>
