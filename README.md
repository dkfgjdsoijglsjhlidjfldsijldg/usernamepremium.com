<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EliteUsernames | Премиум юзернеймы в Telegram</title>
    <style>
        :root {
            --primary: #6c5ce7;
            --primary-dark: #5649c0;
            --secondary: #00cec9;
            --dark: #2d3436;
            --darker: #1e272e;
            --light: #f5f6fa;
            --accent: #fd79a8;
            --gold: #fdcb6e;
            --silver: #b2bec3;
            --bronze: #e17055;
            --diamond: #0984e3;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }
        
        body {
            background-color: #000;
            color: var(--light);
            line-height: 1.6;
            overflow-x: hidden;
            position: relative;
        }
        
        /* Анимированный фон с летающими юзернеймами */
        .floating-usernames {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            overflow: hidden;
        }
        
        .floating-username {
            position: absolute;
            color: rgba(255, 255, 255, 0.1);
            font-size: 20px;
            font-weight: bold;
            animation: float 15s linear infinite;
            pointer-events: none;
        }
        
        @keyframes float {
            0% {
                transform: translateY(100vh) translateX(0);
                opacity: 0;
            }
            10% {
                opacity: 0.1;
            }
            90% {
                opacity: 0.1;
            }
            100% {
                transform: translateY(-100px) translateX(100px);
                opacity: 0;
            }
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Анимации */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* Хедер */
        header {
            background-color: rgba(0, 0, 0, 0.8);
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            backdrop-filter: blur(5px);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            color: var(--light);
            font-size: 24px;
            font-weight: 700;
            text-decoration: none;
            display: flex;
            align-items: center;
        }
        
        .logo i {
            color: var(--gold);
            margin-right: 10px;
        }
        
        .logo span {
            color: var(--primary);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 30px;
        }
        
        nav ul li a {
            color: var(--light);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: var(--primary);
        }
        
        /* Кнопка авторизации */
        .auth-btn {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 20px;
            cursor: pointer;
            transition: all 0.3s;
            font-weight: 500;
            margin-left: 20px;
        }
        
        .auth-btn:hover {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
        }
        
        /* Герой секция */
        .hero {
            height: 100vh;
            background: rgba(0, 0, 0, 0.7);
            display: flex;
            align-items: center;
            padding-top: 80px;
            position: relative;
            overflow: hidden;
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 600px;
        }
        
        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
            line-height: 1.2;
        }
        
        .hero p {
            font-size: 18px;
            margin-bottom: 30px;
            opacity: 0.9;
        }
        
        /* Кнопки */
        .btn {
            display: inline-block;
            padding: 12px 30px;
            background-color: var(--primary);
            color: white;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            border: 2px solid var(--primary);
            position: relative;
            overflow: hidden;
        }
        
        .btn span {
            position: relative;
            z-index: 1;
        }
        
        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: 0.5s;
        }
        
        .btn:hover::before {
            left: 100%;
        }
        
        .btn:hover {
            background-color: var(--primary-dark);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .btn-outline {
            background-color: transparent;
            color: var(--light);
            margin-left: 15px;
        }
        
        .btn-outline:hover {
            background-color: var(--primary);
            color: white;
        }
        
        /* Категории */
        .categories {
            padding: 60px 0;
            background-color: rgba(0, 0, 0, 0.7);
        }
        
        .category-tabs {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 15px;
        }
        
        .category-tab {
            padding: 10px 25px;
            background-color: rgba(30, 39, 46, 0.8);
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s;
            font-weight: 500;
        }
        
        .category-tab:hover {
            background-color: var(--primary);
            transform: translateY(-3px);
        }
        
        .category-tab.active {
            background-color: var(--primary);
            font-weight: 600;
        }
        
        /* Продукты */
        .products {
            padding: 80px 0;
            background-color: rgba(0, 0, 0, 0.7);
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .section-title h2 {
            font-size: 36px;
            margin-bottom: 15px;
        }
        
        .section-title p {
            color: var(--silver);
            font-size: 18px;
        }
        
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .product-card {
            background-color: rgba(30, 39, 46, 0.8);
            border-radius: 15px;
            overflow: hidden;
            transition: all 0.3s;
            position: relative;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            backdrop-filter: blur(5px);
        }
        
        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }
        
        .product-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .badge-default {
            background-color: var(--silver);
            color: var(--dark);
        }
        
        .badge-vip {
            background-color: var(--gold);
            color: var(--dark);
        }
        
        .badge-premium {
            background-color: var(--primary);
            color: white;
        }
        
        .badge-super-premium {
            background-color: var(--accent);
            color: white;
        }
        
        .product-image {
            height: 150px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, var(--darker), var(--dark));
        }
        
        .product-image i {
            font-size: 60px;
            color: var(--primary);
        }
        
        .product-info {
            padding: 25px;
        }
        
        .product-info h3 {
            font-size: 22px;
            margin-bottom: 10px;
        }
        
        .product-info p {
            color: var(--silver);
            margin-bottom: 15px;
            font-size: 14px;
        }
        
        .product-meta {
            display: flex;
            justify-content: space-between;
            font-size: 12px;
            color: var(--silver);
            margin-bottom: 20px;
        }
        
        .product-price {
            font-size: 24px;
            font-weight: 700;
            margin-bottom: 20px;
        }
        
        .price-default {
            color: var(--silver);
        }
        
        .price-vip {
            color: var(--gold);
        }
        
        .price-premium {
            color: var(--primary);
        }
        
        .price-super-premium {
            color: var(--accent);
        }
        
        .product-actions {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .quantity-control {
            display: flex;
            align-items: center;
            border: 1px solid var(--silver);
            border-radius: 30px;
            overflow: hidden;
        }
        
        .quantity-btn {
            background-color: transparent;
            border: none;
            color: var(--light);
            width: 30px;
            height: 30px;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s;
        }
        
        .quantity-btn:hover {
            background-color: rgba(255, 255, 255, 0.1);
        }
        
        .quantity-input {
            width: 30px;
            text-align: center;
            background-color: transparent;
            border: none;
            color: var(--light);
        }
        
        /* Футер */
        footer {
            background-color: rgba(0, 0, 0, 0.8);
            padding: 50px 0 20px;
            text-align: center;
            backdrop-filter: blur(5px);
        }
        
        .footer-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            margin-bottom: 30px;
            gap: 20px;
        }
        
        .social-links a {
            color: var(--light);
            background-color: var(--darker);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s;
            text-decoration: none;
        }
        
        .social-links a:hover {
            background-color: var(--primary);
            transform: translateY(-3px);
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }
        
        .footer-links a {
            color: var(--silver);
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: var(--primary);
        }
        
        .copyright {
            color: var(--silver);
            font-size: 14px;
        }
        
        /* Анимации при скролле */
        .animate-on-scroll {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.6s ease-out;
        }
        
        .animate-on-scroll.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        /* Модальные окна */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 2000;
            align-items: center;
            justify-content: center;
        }
        
        .modal-content {
            background-color: rgba(30, 39, 46, 0.9);
            border-radius: 15px;
            padding: 30px;
            max-width: 500px;
            width: 90%;
            position: relative;
            animation: fadeIn 0.5s;
            backdrop-filter: blur(5px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        .close-modal {
            position: absolute;
            top: 15px;
            right: 15px;
            font-size: 24px;
            color: var(--silver);
            cursor: pointer;
            transition: color 0.3s;
        }
        
        .close-modal:hover {
            color: var(--primary);
        }
        
        .modal-title {
            font-size: 24px;
            margin-bottom: 20px;
            color: var(--primary);
        }
        
        .modal-text {
            margin-bottom: 20px;
            line-height: 1.6;
        }
        
        .payment-methods {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-bottom: 30px;
        }
        
        .payment-method {
            background-color: var(--darker);
            padding: 15px;
            border-radius: 10px;
            display: flex;
            align-items: center;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .payment-method:hover {
            background-color: var(--primary-dark);
        }
        
        .payment-method i {
            font-size: 24px;
            margin-right: 15px;
            color: var(--primary);
        }
        
        .payment-method-info h4 {
            margin-bottom: 5px;
        }
        
        .payment-method-info p {
            font-size: 12px;
            color: var(--silver);
        }
        
        /* Форма авторизации */
        .auth-form {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        
        .form-group {
            display: flex;
            flex-direction: column;
        }
        
        .form-group label {
            margin-bottom: 5px;
            color: var(--silver);
        }
        
        .form-group input {
            padding: 12px 15px;
            border-radius: 8px;
            border: 1px solid var(--silver);
            background-color: rgba(0, 0, 0, 0.5);
            color: var(--light);
            font-size: 16px;
        }
        
        .form-group input:focus {
            outline: none;
            border-color: var(--primary);
        }
        
        /* Адаптивность */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
            }
            
            nav ul {
                margin-top: 20px;
            }
            
            nav ul li {
                margin-left: 15px;
                margin-right: 15px;
            }
            
            .hero h1 {
                font-size: 36px;
            }
            
            .hero p {
                font-size: 16px;
            }
            
            .btn-outline {
                margin-left: 0;
                margin-top: 15px;
                display: block;
            }
            
            .product-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <!-- Анимированный фон с летающими юзернеймами -->
    <div class="floating-usernames" id="floatingUsernames"></div>
    
    <header>
        <div class="container">
            <div class="header-content">
                <a href="#" class="logo"><i class="fas fa-crown"></i>Elite<span>Usernames</span></a>
                <nav>
                    <ul>
                        <li><a href="#products">Каталог</a></li>
                        <li><a href="#categories">Категории</a></li>
                        <li><a href="#contact">Контакты</a></li>
                        <li id="admin-nav-item" style="display: none;"><a href="#admin">Админка</a></li>
                        <li><button class="auth-btn" id="auth-btn">Войти</button></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
    
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Эксклюзивные юзернеймы для Telegram</h1>
                <p>Получите уникальное, запоминающееся имя пользователя, которое подчеркнет ваш статус и индивидуальность в Telegram.</p>
                <a href="#products" class="btn"><span>Выбрать юзернейм</span></a>
                <a href="#contact" class="btn btn-outline"><span>Связаться с нами</span></a>
            </div>
        </div>
    </section>
    
    <section class="categories" id="categories">
        <div class="container">
            <div class="category-tabs">
                <div class="category-tab active" data-category="all">Все</div>
                <div class="category-tab" data-category="default">Default</div>
                <div class="category-tab" data-category="vip">Vip</div>
                <div class="category-tab" data-category="premium">Premium</div>
                <div class="category-tab" data-category="super-premium">Super Premium</div>
            </div>
        </div>
    </section>
    
    <section class="products" id="products">
        <div class="container">
            <div class="section-title animate-on-scroll">
                <h2>Наши юзернеймы</h2>
                <p>Выберите идеальное имя для вашего аккаунта Telegram</p>
            </div>
            
            <div class="product-grid">
                <!-- Default -->
                <div class="product-card animate-on-scroll" data-category="default">
                    <div class="product-badge badge-default">Default</div>
                    <div class="product-image">
                        <i class="fas fa-user"></i>
                    </div>
                    <div class="product-info">
                        <h3>@SimpleUser</h3>
                        <p>Простой и понятный юзернейм для повседневного использования</p>
                        <div class="product-meta">
                            <span>Доступно: 10</span>
                            <span>Популярность: ★★★☆☆</span>
                        </div>
                        <div class="product-price price-default">$49</div>
                        <div class="product-actions">
                            <div class="quantity-control">
                                <button class="quantity-btn minus">-</button>
                                <input type="text" class="quantity-input" value="1" readonly>
                                <button class="quantity-btn plus">+</button>
                            </div>
                            <button class="btn buy-btn" data-product="@SimpleUser" data-price="49"><span>Купить</span></button>
                        </div>
                    </div>
                </div>

                <div class="product-card animate-on-scroll" data-category="vip">
                    <div class="product-badge badge-vip">Vip</div>
                    <div class="product-image">
                        <i class="fas fa-user-tie"></i>
                    </div>
                    <div class="product-info">
                        <h3>@BusinessPro</h3>
                        <p>Профессиональный юзернейм для деловых людей и компаний</p>
                        <div class="product-meta">
                            <span>Доступно: 5</span>
                            <span>Популярность: ★★★★☆</span>
                        </div>
                        <div class="product-price price-vip">$99</div>
                        <div class="product-actions">
                            <div class="quantity-control">
                                <button class="quantity-btn minus">-</button>
                                <input type="text" class="quantity-input" value="1" readonly>
                                <button class="quantity-btn plus">+</button>
                            </div>
                            <button class="btn buy-btn" data-product="@BusinessPro" data-price="99"><span>Купить</span></button>
                        </div>
                    </div>
                </div>
                
                <div class="product-card animate-on-scroll" data-category="premium">
                    <div class="product-badge badge-premium">Premium</div>
                    <div class="product-image">
                        <i class="fas fa-user-secret"></i>
                    </div>
                    <div class="product-info">
                        <h3>@ShadowMaster</h3>
                        <p>Эксклюзивный юзернейм для загадочных личностей</p>
                        <div class="product-meta">
                            <span>Доступно: 2</span>
                            <span>Популярность: ★★★★★</span>
                        </div>
                        <div class="product-price price-premium">$199</div>
                        <div class="product-actions">
                            <div class="quantity-control">
                                <button class="quantity-btn minus">-</button>
                                <input type="text" class="quantity-input" value="1" readonly>
                                <button class="quantity-btn plus">+</button>
                            </div>
                            <button class="btn buy-btn" data-product="@ShadowMaster" data-price="199"><span>Купить</span></button>
                        </div>
                    </div>
                </div>
                
                <!-- Super Premium -->
                <div class="product-card animate-on-scroll" data-category="super-premium">
                    <div class="product-badge badge-super-premium">Super Premium</div>
                    <div class="product-image">
                        <i class="fas fa-crown"></i>
                    </div>
                    <div class="product-info">
                        <h3>@King</h3>
                        <p>Элитный юзернейм для тех, кто привык быть первым</p>
                        <div class="product-meta">
                            <span>Доступно: 1</span>
                            <span>Популярность: ★★★★★</span>
                        </div>
                        <div class="product-price price-super-premium">$499</div>
                        <div class="product-actions">
                            <div class="quantity-control">
                                <button class="quantity-btn minus">-</button>
                                <input type="text" class="quantity-input" value="1" readonly>
                                <button class="quantity-btn plus">+</button>
                            </div>
                            <button class="btn buy-btn" data-product="@King" data-price="499"><span>Купить</span></button>
                        </div>
                    </div>
                </div>
                
                <div class="product-card animate-on-scroll" data-category="default">
                    <div class="product-badge badge-default">Default</div>
                    <div class="product-image">
                        <i class="fas fa-user-ninja"></i>
                    </div>
                    <div class="product-info">
                        <h3>@Ninja</h3>
                        <p>Быстрый и незаметный, как настоящий ниндзя</p>
                        <div class="product-meta">
                            <span>Доступно: 8</span>
                            <span>Популярность: ★★★★☆</span>
                        </div>
                        <div class="product-price price-default">$59</div>
                        <div class="product-actions">
                            <div class="quantity-control">
                                <button class="quantity-btn minus">-</button>
                                <input type="text" class="quantity-input" value="1" readonly>
                                <button class="quantity-btn plus">+</button>
                            </div>
                            <button class="btn buy-btn" data-product="@Ninja" data-price="59"><span>Купить</span></button>
                        </div>
                    </div>
                </div>
                
                <div class="product-card animate-on-scroll" data-category="vip">
                    <div class="product-badge badge-vip">Vip</div>
                    <div class="product-image">
                        <i class="fas fa-rocket"></i>
                    </div>
                    <div class="product-info">
                        <h3>@Rocket</h3>
                        <p>Для тех, кто всегда на шаг впереди</p>
                        <div class="product-meta">
                            <span>Доступно: 3</span>
                            <span>Популярность: ★★★★☆</span>
                        </div>
                        <div class="product-price price-vip">$129</div>
                        <div class="product-actions">
                            <div class="quantity-control">
                                <button class="quantity-btn minus">-</button>
                                <input type="text" class="quantity-input" value="1" readonly>
                                <button class="quantity-btn plus">+</button>
                            </div>
                            <button class="btn buy-btn" data-product="@Rocket" data-price="129"><span>Купить</span></button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section class="contact" id="contact">
        <div class="container">
            <div class="section-title animate-on-scroll">
                <h2>Контакты</h2>
                <p>Свяжитесь с нами для получения дополнительной информации</p>
            </div>
            
            <div class="contact-content animate-on-scroll">
                <div class="contact-info">
                    <h3>Наши контакты</h3>
                    <p><i class="fas fa-envelope"></i> support@eliteusernames.com</p>
                    <p><i class="fas fa-paper-plane"></i> @EliteUsernamesSupport</p>
                </div>
                
                <form class="contact-form">
                    <div class="form-group">
                        <input type="text" placeholder="Ваше имя" required>
                    </div>
                    <div class="form-group">
                        <input type="email" placeholder="Ваш email" required>
                    </div>
                    <div class="form-group">
                        <textarea placeholder="Ваше сообщение" rows="5" required></textarea>
                    </div>
                    <button type="submit" class="btn"><span>Отправить</span></button>
                </form>
            </div>
        </div>
    </section>
    
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="social-links">
                    <a href="#"><i class="fab fa-telegram"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                </div>
                <div class="footer-links">
                    <a href="#">Политика конфиденциальности</a>
                    <a href="#">Условия использования</a>
                    <a href="#">FAQ</a>
                </div>
                <div class="copyright">© 2023 EliteUsernames. Все права защищены.</div>
            </div>
        </div>
    </footer>
    
    <!-- Модальное окно оплаты -->
    <div class="modal" id="payment-modal">
        <div class="modal-content">
            <span class="close-modal">&times;</span>
            <h3 class="modal-title">Оплата через Telegram</h3>
            <p class="modal-text">Для завершения покупки <span id="product-name"></span> за <span id="product-price"></span>$, перейдите в нашего бота и следуйте инструкциям.</p>
            
            <div class="payment-methods">
                <div class="payment-method" id="crypto-payment">
                    <i class="fab fa-bitcoin"></i>
                    <div class="payment-method-info">
                        <h4>Криптовалюта</h4>
                        <p>Оплата BTC, ETH, USDT и другими криптовалютами</p>
                    </div>
                </div>
            </div>
            
            <a href="https://t.me/send?start=IVz2HZ1qsWF2" class="btn" target="_blank" id="payment-link"><span>Перейти к оплате</span></a>
        </div>
    </div>
    
    <!-- Модальное окно авторизации -->
    <div class="modal" id="auth-modal">
        <div class="modal-content">
            <span class="close-modal">&times;</span>
            <h3 class="modal-title">Авторизация</h3>
            <form class="auth-form" id="login-form">
                <div class="form-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" required>
                </div>
                <div class="form-group">
                    <label for="password">Пароль</label>
                    <input type="password" id="password" required>
                </div>
                <button type="submit" class="btn"><span>Войти</span></button>
            </form>
        </div>
    </div>
    
    <!-- Модальное окно админки -->
    <div class="modal" id="admin-modal">
        <div class="modal-content">
            <span class="close-modal">&times;</span>
            <h3 class="modal-title">Админ-панель</h3>
            <div class="admin-content">
                <h4>Добро пожаловать, администратор!</h4>
                <p>Здесь вы можете управлять юзернеймами, просматривать статистику и управлять заказами.</p>
                
                <div class="admin-actions">
                    <button class="btn" id="manage-usernames"><span>Управление юзернеймами</span></button>
                    <button class="btn" id="view-orders"><span>Просмотр заказов</span></button>
                    <button class="btn" id="view-stats"><span>Статистика</span></button>
                </div>
            </div>
        </div>
    </div>
    
    <script>
        // Создаем летающие юзернеймы на фоне
        function createFloatingUsernames() {
            const container = document.getElementById('floatingUsernames');
            const usernames = [
                '@King', '@Queen', '@Pro', '@Elite', '@VIP', '@Gold', 
                '@Diamond', '@Legend', '@Master', '@Boss', '@Ninja',
                '@Hacker', '@Ghost', '@Shadow', '@Wolf', '@Eagle'
            ];
            
            for (let i = 0; i < 20; i++) {
                const username = document.createElement('div');
                username.className = 'floating-username';
                username.textContent = usernames[Math.floor(Math.random() * usernames.length)];
                
                // Случайная позиция и задержка анимации
                username.style.left = Math.random() * 100 + '%';
                username.style.animationDelay = Math.random() * 15 + 's';
                username.style.animationDuration = 10 + Math.random() * 20 + 's';
                
                container.appendChild(username);
            }
        }
        
        // Анимация при скролле
        function animateOnScroll() {
            const elements = document.querySelectorAll('.animate-on-scroll');
            
            elements.forEach(element => {
                const elementPosition = element.getBoundingClientRect().top;
                const screenPosition = window.innerHeight / 1.3;
                
                if (elementPosition < screenPosition) {
                    element.classList.add('visible');
                }
            });
        }
        
        // Фильтрация по категориям
        const categoryTabs = document.querySelectorAll('.category-tab');
        const productCards = document.querySelectorAll('.product-card');
        
        categoryTabs.forEach(tab => {
            tab.addEventListener('click', () => {
                // Удаляем активный класс у всех вкладок
                categoryTabs.forEach(t => t.classList.remove('active'));
                // Добавляем активный класс текущей вкладке
                tab.classList.add('active');
                
                const category = tab.dataset.category;
                
                // Показываем/скрываем карточки в зависимости от категории
                productCards.forEach(card => {
                    if (category === 'all' || card.dataset.category === category) {
                        card.style.display = 'block';
                    } else {
                        card.style.display = 'none';
                    }
                });
            });
        });
        
        // Управление количеством
        const minusButtons = document.querySelectorAll('.minus');
        const plusButtons = document.querySelectorAll('.plus');
        const quantityInputs = document.querySelectorAll('.quantity-input');
        
        minusButtons.forEach((button, index) => {
            button.addEventListener('click', () => {
                let value = parseInt(quantityInputs[index].value);
                if (value > 1) {
                    quantityInputs[index].value = value - 1;
                }
            });
        });
        
        plusButtons.forEach((button, index) => {
            button.addEventListener('click', () => {
                let value = parseInt(quantityInputs[index].value);
                quantityInputs[index].value = value + 1;
            });
        });
        
        // Модальное окно оплаты
        const paymentModal = document.getElementById('payment-modal');
        const buyButtons = document.querySelectorAll('.buy-btn');
        const closeModals = document.querySelectorAll('.close-modal');
        const productName = document.getElementById('product-name');
        const productPrice = document.getElementById('product-price');
        const paymentLink = document.getElementById('payment-link');
        
        buyButtons.forEach(button => {
            button.addEventListener('click', () => {
                const name = button.dataset.product;
                const price = button.dataset.price;
                const quantity = button.closest('.product-actions').querySelector('.quantity-input').value;
                
                productName.textContent = name;
                productPrice.textContent = price * quantity;
                
                // Обновляем ссылку с параметрами
                paymentLink.href = `https://t.me/send?start=IVz2HZ
                // Модальное окно авторизации
const authModal = document.getElementById('auth-modal');
const authBtn = document.getElementById('auth-btn');
const loginForm = document.getElementById('login-form');
const adminModal = document.getElementById('admin-modal');
const adminNavItem = document.getElementById('admin-nav-item');

// Показать модальное окно авторизации
authBtn.addEventListener('click', () => {
    authModal.style.display = 'flex';
});

// Закрыть модальные окна
closeModals.forEach(closeBtn => {
    closeBtn.addEventListener('click', () => {
        paymentModal.style.display = 'none';
        authModal.style.display = 'none';
        adminModal.style.display = 'none';
    });
});

// Закрыть при клике вне модального окна
window.addEventListener('click', (e) => {
    if (e.target === paymentModal) paymentModal.style.display = 'none';
    if (e.target === authModal) authModal.style.display = 'none';
    if (e.target === adminModal) adminModal.style.display = 'none';
});

// Обработка формы авторизации
loginForm.addEventListener('submit', (e) => {
    e.preventDefault();
    
    const email = document.getElementById('email').value;
    const password = document.getElementById('password').value;
    
    // Проверка учетных данных администратора
    if (email === 'sddd89521022287@gmail.com' && password === 's200791dimr') {
        // Успешная авторизация
        authBtn.textContent = 'Выйти';
        adminNavItem.style.display = 'block';
        authModal.style.display = 'none';
        
        // Сохраняем статус в localStorage
        localStorage.setItem('isAdmin', 'true');
        
        // Показываем сообщение об успешной авторизации
        alert('Вы успешно вошли как администратор!');
    } else {
        alert('Неверные учетные данные!');
    }
});

// Проверка авторизации при загрузке страницы
window.addEventListener('DOMContentLoaded', () => {
    createFloatingUsernames();
    
    // Проверяем, авторизован ли администратор
    if (localStorage.getItem('isAdmin') === 'true') {
        authBtn.textContent = 'Выйти';
        adminNavItem.style.display = 'block';
    }
    
    // Обработчик выхода
    authBtn.addEventListener('click', function() {
        if (this.textContent === 'Выйти') {
            localStorage.removeItem('isAdmin');
            this.textContent = 'Войти';
            adminNavItem.style.display = 'none';
            alert('Вы вышли из системы');
        }
    });
    
    // Открытие админки
    adminNavItem.addEventListener('click', (e) => {
        e.preventDefault();
        adminModal.style.display = 'flex';
    });
    
    // Кнопки в админке
    document.getElementById('manage-usernames').addEventListener('click', () => {
        alert('Раздел "Управление юзернеймами" в разработке');
    });
    
    document.getElementById('view-orders').addEventListener('click', () => {
        alert('Раздел "Просмотр заказов" в разработке');
    });
    
    document.getElementById('view-stats').addEventListener('click', () => {
        alert('Раздел "Статистика" в разработке');
    });
});

// Анимация при скролле
window.addEventListener('scroll', animateOnScroll);
// Инициализация анимации при загрузке
animateOnScroll();
