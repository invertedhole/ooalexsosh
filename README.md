<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Мой сайт</title>
    <style>
       /* Базовый стиль для всего сайта */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #F0FFF0;
        }
        /* Стиль для вкладок */
        .tabs {
            display: flex;
            list-style: none;
            margin: 0;
            padding: 0;
             overflow: hidden;
    border: none;
    background-color: #8FBC8F;
        }
        .tabs li {
            flex: 1;
            text-align: center;
            border-bottom: 2px solid transparent;
            cursor: pointer;
            padding: 10px;
        }
        .tabs li.active {
            border-bottom: 2px solid #007bff;
        }
        /* Стиль для контента вкладок */
        .tab-content {
            display: none;
            padding: 20px;
        }
        .tab-content.active {
            display: block;
        }
    </style>
</head>
<body>
    <header>
        <!-- Заголовок сайта -->
        <h1></h1>
<p>> <img src= https://raw.githubusercontent.com/invertedhole/ooalexsosh/main/картинка2.PNG>
    </header>
 
<main>
        <!-- Основное содержимое сайта -->
        <ul class="tabs">
            <li class="active" data-tab="tab1">О нас</li>
            <li data-tab="tab2">Жизнь школы</li>
            <li data-tab="tab3">Новости</li>
        </ul>
        <div id="tab1" class="tab-content active">
            <p>Контактные данные
<p>Директор:+7 990 077 2103
<p>Отдел кадров +7 990 058 1933</p>
           
<div id="tab2" class="tab-content">
<p>fdfdf</p>
<body>
    <div class="tab-container">
        <div class="tab-links">
            <button class="tab-link active" onclick="openTab(event, 'Home')">Home</button>
            <button class="tab-link" onclick="openTab(event, 'About')">About</button>
            <button class="tab-link" onclick="openTab(event, 'Projects')">Projects</button>
            <button class="tab-link" onclick="openTab(event, 'Contact')">Contact</button>
        </div>
        <div class="tab-content" id="Home">
            <h2>Home</h2>
            <p>Welcome to my GitHub page!</p>
            <img src="images/home.jpg" alt="Home Image">
        </div>
        <div class="tab-content" id="About" style="display:none;">
            <h2>About</h2>
            <p>This is the about section.</p>
            <img src="images/about.jpg" alt="About Image">
        </div>
        <div class="tab-content" id="Projects" style="display:none;">
            <h2>Projects</h2>
            <p>These are my projects.</p>
            <img src="images/projects.jpg" alt="Projects Image">
        </div>
        <div class="tab-content" id="Contact" style="display:none;">
            <h2>Contact</h2>
            <p>Get in touch with me.</p>
            <img src="images/contact.jpg" alt="Contact Image">
        </div>
    </div>
    <script src="scripts.js"></script>
</body>
        <div id="tab3" class="tab-content">
            <p>Контент вкладки 3</p>
        </div>
    </main>
    <footer>
        <!-- Нижняя часть сайта -->
        <p>&copy; 2024  сайт  ГБУ ОО ЗО "Алексеевская СОШ"</p>
    </footer>
    <script>
        // JavaScript для управления вкладками
        const tabs = document.querySelectorAll('.tabs li');
        const tabContents = document.querySelectorAll('.tab-content');
        tabs.forEach(tab => {
            tab.addEventListener('click', () => {
                const targetTab = tab.dataset.tab;
                const targetContent = document.getElementById(targetTab);
                tabs.forEach(tab => {
                    tab.classList.remove('active');
                });
                tabContents.forEach(content => {
                    content.classList.remove('active');
                });
                tab.classList.add('active');
                targetContent.classList.add('active');
            });
        });
    </script>
</body>
</html>
