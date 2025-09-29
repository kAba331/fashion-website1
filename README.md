[deepseek_html_20250929_85253d.html](https://github.com/user-attachments/files/22595383/deepseek_html_20250929_85253d.html)[U<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fashion Vision - Мир высокой моды</title>
    <style>
        :root {
            --gold: #D4AF37;
            --black: #1a1a1a;
            --white: #ffffff;
            --gray: #f5f5f5;
            --dark-gray: #333;
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Playfair Display', 'Times New Roman', serif;
            background: var(--white);
            color: var(--black);
            line-height: 1.6;
        }

        /* Header */
        .luxury-header {
            background: var(--black);
            color: var(--white);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            border-bottom: 2px solid var(--gold);
        }

        .header-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 2rem;
            font-weight: 700;
            color: var(--gold);
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--white);
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            position: relative;
        }

        .nav-links a:hover {
            color: var(--gold);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--gold);
            transition: var(--transition);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), 
                        url('https://images.unsplash.com/photo-1445205170230-053b83016050?ixlib=rb-4.0.3') center/cover;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: var(--white);
            margin-top: 80px;
        }

        .hero-content h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        .hero-content p {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .cta-button {
            display: inline-block;
            padding: 15px 40px;
            background: var(--gold);
            color: var(--black);
            text-decoration: none;
            font-weight: 600;
            border-radius: 2px;
            transition: var(--transition);
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .cta-button:hover {
            background: var(--white);
            transform: translateY(-2px);
        }

        /* Featured Articles */
        .featured-section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: var(--black);
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 100px;
            height: 3px;
            background: var(--gold);
            margin: 1rem auto;
        }

        .articles-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .article-card {
            background: var(--white);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: var(--transition);
            border: 1px solid #eee;
        }

        .article-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }

        .article-image {
            height: 250px;
            background: var(--gray);
            overflow: hidden;
        }

        .article-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }

        .article-card:hover .article-image img {
            transform: scale(1.1);
        }

        .article-content {
            padding: 2rem;
        }

        .article-category {
            color: var(--gold);
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-size: 0.8rem;
            margin-bottom: 0.5rem;
        }

        .article-title {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--black);
        }

        .article-excerpt {
            color: var(--dark-gray);
            margin-bottom: 1.5rem;
            line-height: 1.8;
        }

        .read-more {
            color: var(--black);
            text-decoration: none;
            font-weight: 600;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            transition: var(--transition);
        }

        .read-more:hover {
            color: var(--gold);
            gap: 1rem;
        }

        /* Designer Spotlight */
        .designer-spotlight {
            background: var(--black);
            color: var(--white);
            padding: 5rem 2rem;
        }

        .spotlight-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .designer-image {
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 20px 40px rgba(212, 175, 55, 0.3);
        }

        .designer-image img {
            width: 100%;
            height: auto;
            display: block;
        }

        .designer-info h3 {
            color: var(--gold);
            font-size: 1.2rem;
            margin-bottom: 1rem;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .designer-info h2 {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
        }

        .designer-bio {
            margin-bottom: 2rem;
            line-height: 1.8;
            opacity: 0.9;
        }

        .fun-fact {
            background: rgba(212, 175, 55, 0.1);
            padding: 1.5rem;
            border-left: 4px solid var(--gold);
            margin-bottom: 1.5rem;
        }

        .fun-fact h4 {
            color: var(--gold);
            margin-bottom: 0.5rem;
        }

        /* Newsletter */
        .newsletter {
            background: var(--gray);
            padding: 4rem 2rem;
            text-align: center;
        }

        .newsletter-content {
            max-width: 600px;
            margin: 0 auto;
        }

        .newsletter h2 {
            font-size: 2rem;
            margin-bottom: 1rem;
        }

        .newsletter-form {
            display: flex;
            gap: 1rem;
            margin-top: 2rem;
        }

        .newsletter-input {
            flex: 1;
            padding: 1rem;
            border: 1px solid #ddd;
            border-radius: 2px;
            font-family: inherit;
        }

        .newsletter-button {
            padding: 1rem 2rem;
            background: var(--black);
            color: var(--white);
            border: none;
            border-radius: 2px;
            cursor: pointer;
            transition: var(--transition);
        }

        .newsletter-button:hover {
            background: var(--gold);
            color: var(--black);
        }

        /* Footer */
        .luxury-footer {
            background: var(--black);
            color: var(--white);
            padding: 3rem 2rem 1rem;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
            margin-bottom: 2rem;
        }

        .footer-section h3 {
            color: var(--gold);
            margin-bottom: 1.5rem;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 0.5rem;
        }

        .footer-links a {
            color: var(--white);
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-links a:hover {
            color: var(--gold);
        }

        .copyright {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid #444;
            color: #999;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 1rem;
            }

            .nav-links {
                gap: 1rem;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }

            .spotlight-content {
                grid-template-columns: 1fr;
                gap: 2rem;
            }

            .newsletter-form {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="luxury-header">
        <div class="header-content">
            <a href="#" class="logo">FASHION VISION</a>
            <nav>
                <ul class="nav-links">
                    <li><a href="#trends">Тренды</a></li>
                    <li><a href="#designers">Дизайнеры</a></li>
                    <li><a href="#history">История</a></li>
                    <li><a href="#news">Новости</a></li>
                    <li><a href="#contact">Контакты</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>Искусство в каждом стежке</h1>
            <p>Исследуйте мир высокой моды с Fashion Vision</p>
            <a href="#articles" class="cta-button">Открыть коллекции</a>
        </div>
    </section>

    <!-- Featured Articles -->
    <section class="featured-section" id="articles">
        <h2 class="section-title">Главные материалы</h2>
        <div class="articles-grid">
            <article class="article-card">
                <div class="article-image">
                    <img src="https://images.unsplash.com/photo-1539109136881-3be0616acf4b" alt="Осенняя мода">
                </div>
                <div class="article-content">
                    <div class="article-category">Тренды</div>
                    <h3 class="article-title">Осень-Зима 2024: Главные тенденции</h3>
                    <p class="article-excerpt">От объемных силуэтов до винтажных аксессуаров - разбираем ключевые направления предстоящего сезона.</p>
                    <a href="#" class="read-more">
                        Читать далее
                        <span>→</span>
                    </a>
                </div>
            </article>

            <article class="article-card">
                <div class="article-image">
                    <img src="https://images.unsplash.com/photo-1445205170230-053b83016050" alt="Устойчивая мода">
                </div>
                <div class="article-content">
                    <div class="article-category">Устойчивость</div>
                    <h3 class="article-title">Эко-мода: Будущее индустрии</h3>
                    <p class="article-excerpt">Как бренды переходят на устойчивое производство и что это значит для потребителей.</p>
                    <a href="#" class="read-more">
                        Читать далее
                        <span>→</span>
                    </a>
                </div>
            </article>

            <article class="article-card">
                <div class="article-image">
                    <img src="https://images.unsplash.com/photo-1515886657613-9f3515b0c78f" alt="Неделя моды">
                </div>
                <div class="article-content">
                    <div class="article-category">События</div>
                    <h3 class="article-title">Paris Fashion Week: Итоги</h3>
                    <p class="article-excerpt">Самые яркие показы, скандалы и открытия главного модного события года.</p>
                    <a href="#" class="read-more">
                        Читать далее
                        <span>→</span>
                    </a>
                </div>
            </article>
        </div>
    </section>

    <!-- Designer Spotlight -->
    <section class="designer-spotlight" id="designers">
        <div class="spotlight-content">
            <div class="designer-image">
                <img src="https://images.unsplash.com/photo-1519345182560-3f2917c472ef" alt="Коко Шанель">
            </div>
            <div class="designer-info">
                <h3>Легенда моды</h3>
                <h2>Коко Шанель</h2>
                <p class="designer-bio">
                    Габриэль Бонёр "Коко" Шанель - французский модельер, основавшая модный дом Chanel. 
                    Она освободила женщин от корсетов и ввела в моду практичную элегантность.
                </p>
                
                <div class="fun-fact">
                    <h4>Интересный факт</h4>
                    <p>Шанель начала свою карьеру как певица в кабаре, где получила прозвище "Коко". 
                    Ее маленькое черное платье стало символом простоты и элегантности.</p>
                </div>

                <div class="fun-fact">
                    <h4>Наследие</h4>
                    <p>Дом Chanel продолжает влиять на мировую моду, сохраняя наследие основательницы 
                    через культовые продукты как твидовые костюмы и духи Chanel No. 5.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Additional Articles -->
    <section class="featured-section">
        <h2 class="section-title">Истории дизайнеров</h2>
        <div class="articles-grid">
            <article class="article-card">
                <div class="article-image">
                    <img src="https://images.unsplash.com/photo-1581044777550-4cfa60707c03" alt="Ив Сен-Лоран">
                </div>
                <div class="article-content">
                    <div class="article-category">Биография</div>
                    <h3 class="article-title">Ив Сен-Лоран: Революционер</h3>
                    <p class="article-excerpt">
                        <strong>Интересный факт:</strong> Сен-Лоран стал главным дизайнером Dior в 21 год. 
                        Он ввел в женскую моду смокинг и прозрачные блузы, шокировав публику.
                    </p>
                    <a href="#" class="read-more">
                        Узнать больше
                        <span>→</span>
                    </a>
                </div>
            </article>

            <article class="article-card">
                <div class="article-image">
                    <img src="https://images.unsplash.com/photo-1595950653106-6c9ebd614d3a" alt="Джорджио Армани">
                </div>
                <div class="article-content">
                    <div class="article-category">Стиль</div>
                    <h3 class="article-title">Армани: Искусство минимализма</h3>
                    <p class="article-excerpt">
                        <strong>Интересный факт:</strong> До моды Армани изучал медицину. 
                        Его фирменный бежевый цвет был вдохновлен оттенками итальянского пейзажа.
                    </p>
                    <a href="#" class="read-more">
                        Узнать больше
                        <span>→</span>
                    </a>
                </div>
            </article>
        </div>
    </section>

    <!-- Newsletter -->
    <section class="newsletter">
        <div class="newsletter-content">
            <h2>Будьте в курсе модных тенденций</h2>
            <p>Подпишитесь на нашу рассылку и получайте эксклюзивные материалы</p>
            <form class="newsletter-form">
                <input type="email" class="newsletter-input" placeholder="Ваш email" required>
                <button type="submit" class="newsletter-button">Подписаться</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer class="luxury-footer">
        <div class="footer-content">
            <div class="footer-section">
                <h3>Fashion Vision</h3>
                <p>Ваш гид в мире высокой моды и стиля. Исследуем, вдохновляем, образовываем.</p>
            </div>
            <div class="footer-section">
                <h3>Разделы</h3>
                <ul class="footer-links">
                    <li><a href="#trends">Тренды</a></li>
                    <li><a href="#designers">Дизайнеры</a></li>
                    <li><a href="#history">История моды</a></li>
                    <li><a href="#news">Новости</a></li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>Контакты</h3>
                <ul class="footer-links">
                    <li><a href="mailto:info@fashionvision.ru">info@fashionvision.ru</a></li>
                    <li><a href="tel:+79991234567">+7 999 123-45-67</a></li>
                </ul>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2024 Fashion Vision. Все права защищены.</p>
        </div>
    </footer>

    <script>
        // Плавная прокрутка для навигации
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

        // Обработка формы подписки
        document.querySelector('.newsletter-form').addEventListener('submit', function(e) {
            e.preventDefault();
            const email = this.querySelector('input[type="email"]').value;
            alert(`Спасибо за подписку, ${email}! Вы будете получать наши обновления.`);
            this.reset();
        });

        // Анимация при скролле
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Наблюдаем за карточками статей
        document.querySelectorAll('.article-card').forEach(card => {
            card.style.opacity = '0';
            card.style.transform = 'translateY(30px)';
            card.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(card);
        });
    </script>
</body>
</html>ploading deepseek_html_20250929_85253d.html…]()
