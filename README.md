<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Технология Прогресса - Окна и двери в Новосибирске</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
        }
        
        header {
            background: linear-gradient(135deg, #0057b7, #003d7a);
            color: white;
            padding: 20px 0;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .logo {
            font-size: 28px;
            font-weight: bold;
            margin-bottom: 10px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        nav {
            margin-top: 15px;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            margin: 0 15px;
            font-weight: 500;
            transition: all 0.3s;
        }
        
        nav a:hover {
            color: #ffd700;
        }
        
        .hero {
            background: url('https://via.placeholder.com/1200x600') no-repeat center center/cover;
            height: 80vh;
            min-height: 500px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            position: relative;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            padding: 0 20px;
        }
        
        .hero h1 {
            font-size: 42px;
            margin-bottom: 20px;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.5);
        }
        
        .hero p {
            font-size: 20px;
            margin-bottom: 30px;
        }
        
        .btn {
            display: inline-block;
            background: #ffd700;
            color: #333;
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            margin: 10px;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }
        
        .btn:hover {
            background: transparent;
            color: #ffd700;
            border-color: #ffd700;
            transform: translateY(-3px);
        }
        
        .btn-secondary {
            background: transparent;
            color: #ffd700;
            border-color: #ffd700;
        }
        
        .btn-secondary:hover {
            background: #ffd700;
            color: #333;
        }
        
        section {
            padding: 80px 0;
        }
        
        h2 {
            font-size: 36px;
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }
        
        h2::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: #ffd700;
            margin: 15px auto 0;
        }
        
        .services {
            background-color: #fff;
        }
        
        .service-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }
        
        .service-item {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            text-align: center;
            border: 1px solid #eee;
        }
        
        .service-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
        
        .service-item i {
            font-size: 50px;
            color: #0057b7;
            margin-bottom: 20px;
            display: block;
        }
        
        .service-item h3 {
            margin-bottom: 15px;
            color: #0057b7;
            font-size: 22px;
        }
        
        .about {
            background: #f9f9f9;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
            flex-wrap: wrap;
        }
        
        .about-text {
            flex: 1;
            min-width: 300px;
        }
        
        .about-image {
            flex: 1;
            min-width: 300px;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        .advantages {
            background: #0057b7;
            color: white;
        }
        
        .advantages h2 {
            color: white;
        }
        
        .advantages h2::after {
            background: #ffd700;
        }
        
        .advantage-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .advantage-item {
            text-align: center;
            padding: 30px;
        }
        
        .advantage-item i {
            font-size: 40px;
            color: #ffd700;
            margin-bottom: 20px;
        }
        
        .advantage-item h3 {
            margin-bottom: 15px;
            font-size: 22px;
        }
        
        .portfolio {
            background: #fff;
        }
        
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }
        
        .portfolio-item {
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            height: 250px;
        }
        
        .portfolio-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .portfolio-item:hover img {
            transform: scale(1.1);
        }
        
        .portfolio-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: rgba(0, 87, 183, 0.8);
            color: white;
            padding: 20px;
            transform: translateY(100%);
            transition: transform 0.3s;
        }
        
        .portfolio-item:hover .portfolio-overlay {
            transform: translateY(0);
        }
        
        .contact {
            background: #f9f9f9;
        }
        
        .contact-container {
            display: flex;
            flex-wrap: wrap;
            gap: 50px;
        }
        
        .contact-info {
            flex: 1;
            min-width: 300px;
        }
        
        .contact-info h3 {
            font-size: 24px;
            margin-bottom: 20px;
            color: #0057b7;
        }
        
        .contact-info p {
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }
        
        .contact-info i {
            margin-right: 10px;
            color: #0057b7;
            font-size: 20px;
            width: 25px;
        }
        
        .contact-form {
            flex: 1;
            min-width: 300px;
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
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
        .form-group textarea,
        .form-group select {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
        }
        
        .form-group textarea {
            height: 120px;
            resize: vertical;
        }
        
        footer {
            background: #222;
            color: white;
            padding: 40px 0 20px;
        }
        
        .footer-content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .footer-column {
            flex: 1;
            min-width: 200px;
        }
        
        .footer-column h3 {
            color: #ffd700;
            margin-bottom: 20px;
            font-size: 20px;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: #bbb;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column ul li a:hover {
            color: #ffd700;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 15px;
        }
        
        .social-links a {
            color: white;
            background: #444;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s;
        }
        
        .social-links a:hover {
            background: #ffd700;
            color: #333;
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #444;
            color: #bbb;
            font-size: 14px;
        }
        
        /* Иконки */
        .icon {
            display: inline-block;
            width: 1em;
            height: 1em;
            stroke-width: 0;
            stroke: currentColor;
            fill: currentColor;
        }
        
        /* Анимации */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .animate {
            animation: fadeIn 1s ease-out forwards;
        }
        
        .delay-1 { animation-delay: 0.2s; }
        .delay-2 { animation-delay: 0.4s; }
        .delay-3 { animation-delay: 0.6s; }
        
        /* Адаптивность */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 32px;
            }
            
            .hero p {
                font-size: 18px;
            }
            
            section {
                padding: 60px 0;
            }
            
            h2 {
                font-size: 30px;
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
</head>
<body>
    <header>
        <div class="container">
            <div class="logo">Технология Прогресса</div>
            <p>Производство и установка оконных и дверных конструкций</p>
            <nav>
                <a href="#services">Услуги</a>
                <a href="#about">О компании</a>
                <a href="#advantages">Преимущества</a>
                <a href="#portfolio">Портфолио</a>
                <a href="#contact">Контакты</a>
            </nav>
        </div>
    </header>
    
    <section class="hero">
        <div class="hero-content">
            <h1 class="animate">Качественные окна и двери от производителя</h1>
            <p class="animate delay-1">Собственное производство в Новосибирске. Гарантия качества и доступные цены.</p>
            <div>
                <a href="#contact" class="btn animate delay-2">Оставить заявку</a>
                <a href="tel:+73832483654" class="btn btn-secondary animate delay-2">Позвонить нам</a>
            </div>
        </div>
    </section>
    
    <section class="services" id="services">
        <div class="container">
            <h2>Наши услуги</h2>
            <div class="service-grid">
                <div class="service-item animate">
                    <i class="material-icons">window</i>
                    <h3>Окна ПВХ</h3>
                    <p>Изготовление и установка пластиковых окон любой сложности с гарантией качества. Энергосберегающие технологии, шумоизоляция.</p>
                </div>
                <div class="service-item animate delay-1">
                    <i class="material-icons">balcony</i>
                    <h3>Алюминиевые конструкции</h3>
                    <p>Остекление балконов, лоджий, витражей и фасадов алюминиевым профилем. Современные решения для коммерческих объектов.</p>
                </div>
                <div class="service-item animate delay-2">
                    <i class="material-icons">nature</i>
                    <h3>Деревянные окна</h3>
                    <p>Экологичные деревянные окна с современными технологиями теплоизоляции. Натуральные материалы и ручная работа.</p>
                </div>
                <div class="service-item animate delay-3">
                    <i class="material-icons">door_front</i>
                    <h3>Двери</h3>
                    <p>Входные и межкомнатные двери из различных материалов. Повышенная безопасность и звукоизоляция.</p>
                </div>
            </div>
        </div>
    </section>
    
    <section class="about" id="about">
        <div class="container">
            <h2>О компании</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Компания "Технология Прогресса" занимается изготовлением, установкой и гарантийным обслуживанием ПВХ, алюминиевых и деревянных конструкций с 2021 года.</p>
                    <p>Мы предлагаем полный цикл услуг: от замера и проектирования до монтажа и последующего обслуживания.</p>
                    <p>Наше производство оснащено современным оборудованием, что позволяет нам создавать продукцию высокого качества с точностью до миллиметра.</p>
                    <p>Опытные специалисты компании готовы реализовать даже самые сложные и нестандартные проекты.</p>
                    <a href="#contact" class="btn">Узнать больше</a>
                </div>
                <div class="about-image">
                    <img src="https://via.placeholder.com/600x400" alt="Наше производство">
                </div>
            </div>
        </div>
    </section>
    
    <section class="advantages" id="advantages">
        <div class="container">
            <h2>Наши преимущества</h2>
            <div class="advantage-grid">
                <div class="advantage-item">
                    <i class="material-icons">verified</i>
                    <h3>Гарантия качества</h3>
                    <p>Предоставляем официальную гарантию до 10 лет на все наши изделия и монтажные работы.</p>
                </div>
                <div class="advantage-item">
                    <i class="material-icons">factory</i>
                    <h3>Собственное производство</h3>
                    <p>Полный контроль качества на всех этапах производства без посредников.</p>
                </div>
                <div class="advantage-item">
                    <i class="material-icons">engineering</i>
                    <h3>Опытные специалисты</h3>
                    <p>Квалифицированные монтажники с опытом работы более 5 лет в сфере остекления.</p>
                </div>
                <div class="advantage-item">
                    <i class="material-icons">savings</i>
                    <h3>Доступные цены</h3>
                    <p>Оптимизация производства позволяет предлагать конкурентные цены без потери качества.</p>
                </div>
            </div>
        </div>
    </section>
    
    <section class="portfolio" id="portfolio">
        <div class="container">
            <h2>Наши работы</h2>
            <div class="portfolio-grid">
                <div class="portfolio-item">
                     <img src='https://i.postimg.cc/zHK14S9d/okno11.jpg' border='0' alt='okno11'/> alt="Окна ПВХ">
                    <div class="portfolio-overlay">
                        <h3>Остекление квартиры</h3>
                        <p>ЖК "Солнечный", пластиковые окна с энергосберегающим стеклопакетом</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <img src="https://via.placeholder.com/400x300" alt="Балкон">
                    <div class="portfolio-overlay">
                        <h3>Остекление балкона</h3>
                        <p>Утепление и отделка балкона с раздвижной алюминиевой системой</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <img src="https://via.placeholder.com/400x300" alt="Загородный дом">
                    <div class="portfolio-overlay">
                        <h3>Остекление коттеджа</h3>
                        <p>Панорамное остекление загородного дома деревянными окнами</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <img src="https://via.placeholder.com/400x300" alt="Офисное здание">
                    <div class="portfolio-overlay">
                        <h3>Коммерческий объект</h3>
                        <p>Остекление офисного центра алюминиевыми витражами</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section class="contact" id="contact">
        <div class="container">
            <h2>Контакты</h2>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Как нас найти</h3>
                    <p><i class="material-icons">location_on</i> <strong>Адрес:</strong> Россия, г. Новосибирск, ул. Фабричная 4, 3 этаж, офис 306</p>
                    <p><i class="material-icons">phone</i> <strong>Телефон:</strong> <a href="tel:+73832483654">+7 (383) 248-36-54</a></p>
                    <p><i class="material-icons">email</i> <strong>Email:</strong> <a href="mailto:gneprogress@gmail.com">gneprogress@gmail.com</a></p>
                    <p><i class="material-icons">schedule</i> <strong>Режим работы:</strong> Пн-Пт: 9:00-18:00, Сб: 10:00-15:00, Вс: выходной</p>
                    
                    
                    </div>
                </div>
                
                <div class="contact-form">
                    <h3>Оставить заявку</h3>
                    <form id="feedback-form">
                        <div class="form-group">
                            <label for="name">Ваше имя</label>
                            <input type="text" id="name" name="name" required>
                        </div>
                        <div class="form-group">
                            <label for="phone">Телефон</label>
                            <input type="tel" id="phone" name="phone" required>
                        </div>
                        <div class="form-group">
                            <label for="service">Интересующая услуга</label>
                            <select id="service" name="service">
                                <option value="windows">Окна ПВХ</option>
                                <option value="aluminum">Алюминиевые конструкции</option>
                                <option value="wooden">Деревянные окна</option>
                                <option value="doors">Двери</option>
                                <option value="other">Другое</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label for="message">Сообщение</label>
                            <textarea id="message" name="message"></textarea>
                        </div>
                        <button type="submit" class="btn">Отправить заявку</button>
                    </form>
                </div>
            </div>
        </div>
    </section>
    
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Технология Прогресса</h3>
                    <p>Производство и установка оконных и дверных конструкций в Новосибирске с 2021 года.</p>
                </div>
                <div class="footer-column">
                    <h3>Услуги</h3>
                    <ul>
                        <li><a href="#">Окна ПВХ</a></li>
                        <li><a href="#">Алюминиевые конструкции</a></li>
                        <li><a href="#">Деревянные окна</a></li>
                        <li><a href="#">Двери</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Контакты</h3>
                    <ul>
                        <li><a href="tel:+73832483654">+7 (383) 248-36-54</a></li>
                        <li><a href="mailto:gneprogress@gmail.com">gneprogress@gmail.com</a></li>
                        <li>ул. Фабричная 4, оф. 306</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 ООО "Технология Прогресса". Все права защищены.</p>
            </div>
        </div>
    </footer>
    
    <script>
        // Плавная прокрутка для якорных ссылок
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
        
        // Анимация при скролле
        const animateElements = document.querySelectorAll('.animate');
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = 1;
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, { threshold: 0.1 });
        
        animateElements.forEach(el => {
            el.style.opacity = 0;
            el.style.transform = 'translateY(20px)';
            el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(el);
        });
        
        // Обработка формы
        const form = document.getElementById('feedback-form');
        form.addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Спасибо за вашу заявку! Мы свяжемся с вами в ближайшее время.');
            form.reset();
        });
    </script>
</body>
</html>
