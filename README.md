# ГБУ ОО ЗО "Алексеевская СОШ"
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
            background-color: #FFFFF0;
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
<img src="https://raw.githubusercontent.com/invertedhole/ooalexsosh/main/картинка2.PNG" width="1200" height="300">
    </header>
    <main>
        <!-- Основное содержимое сайта -->
        <ul class="tabs">
            <li class="active" data-tab="tab1">О нас</li>
            <li data-tab="tab2">Жизнь школы</li>
            <li data-tab="tab3">Новости</li>
        </ul>
        <div id="tab1" class="tab-content"> active">
            <p>Контактные данные
<p>Директор:+7 990 077 2103
<p>Отдел кадров +7 990 058 1933</p>   
            <div id="tab2" class="tab-content"> 
   <body>
    <div class="tab-container">
        <div class="tab-links">
            <button class="tab-link active" onclick="openTab(event, 'Tab1')">Выпуск 2024</button>
            <button class="tab-link" onclick="openTab(event, 'Tab2')">Мероприятия</button>
            <button class="tab-link" onclick="openTab(event, 'Tab3')">Первый звонок 2024</button>
        <div class="tab-content" id="Tab1">
            <h2>Выпуск 2024 Content</h2>
            <p>This is the content for Tab 1.</p>
        <div class="tab-content" id="Tab2" style="display:none;">
            <h2>Мероприятия Content</h2>
            <p>This is the content for Tab 2.</p>
        <div class="tab-content" id="Tab3" style="display:none;">
            <h2>Первый звонок 2024 Content</h2>
            <p>This is the content for Первый звонок 2024.</p>
    <script src="scripts.js"></script>
 <style>
    font-family: Arial, sans-serif;
}
.tab-container {
    display: flex;
}
.tab-links {
    flex: 1;
    display: flex;
    flex-direction: column;
}
.tab-link {
    padding: 10px;
    background-color: #f1f1f1;
    border: none;
    outline: none;
    text-align: left;
    cursor: pointer;
    transition: background-color 0.3s ease;
}
.tab-link:hover {
    background-color: #ddd;
}
.tab-link.active {
    background-color: #ccc;
}
.tab-content {
    flex: 4;
    padding: 20px;
    border-left: 1px solid #ccc;
}
.tab-content h2 {
    margin-top: 0;
} 
</style>
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
     <div id="tab3" class="tab-content">
            <p>Контент вкладки 3</p>
        </div>
    </main>
    <footer>
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
