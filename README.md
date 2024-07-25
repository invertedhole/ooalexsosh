# ГБУ ОО ЗО "Алексеевская СОШ"
<html lang="en">
<head>
   <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Сайт школы</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #FFDAB9;
        }       
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
        <h1></h1>
<p> <img src=https://raw.githubusercontent.com/invertedhole/ooalexsosh/main/картинка2.PNG>
    <main>
        <ul class="tabs">
            <li class="active" data-tab="tab1">О нас</li>
            <li data-tab="tab2">Жизнь школы</li>
            <li data-tab="tab3">Новости</li>
        </ul>
        <div id="tab1" class="tab-content active">
 <p>Контактные данные
<p>Директор:+7 990 077 2103
<p>Отдел кадров +7 990 058 1933</p>
          </div>
        <div id="tab2" class="tab-content"> 
    <div class="tab-container">
        <div class="tab-links">
            <button class="tab-link active" onclick="openTab(event, 'Tab1')">Overview</button>
            <button class="tab-link" onclick="openTab(event, 'Tab2')">Features</button>
            <button class="tab-link" onclick="openTab(event, 'Tab3')">Installation</button>
            <button class="tab-link" onclick="openTab(event, 'Tab4')">Usage</button>
        </div>
        <div class="tab-content" id="Tab1">
            <h2>Overview</h2>
            <p>This is the overview content.</p>
        </div>
        <div class="tab-content" id="Tab2" style="display:none;">
            <h2>Features</h2>
            <p>These are the features.</p>
        </div>
        <div class="tab-content" id="Tab3" style="display:none;">
            <h2>Installation</h2>
            <p>Instructions for installation.</p>
        </div>
        <div class="tab-content" id="Tab4" style="display:none;">
            <h2>Usage</h2>
            <p>Usage information.</p>
        </div>
    </div>
    <script src="scripts.js"></script>
</body>
<style>               
body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    padding: 20px;
}
.tab-container {
    display: flex;
    max-width: 800px;
    margin: 0 auto;
    background-color: #fff;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
}
.tab-links {
    flex: 1;
    display: flex;
    flex-direction: column;
}
.tab-link {
    padding: 15px;
    background-color: #f1f1f1;
    border: none;
    outline: none;
    text-align: left;
    cursor: pointer;
    transition: background-color 0.3s;
}
.tab-link:hover {
    background-color: #e0e0e0;
}
.tab-link.active {
    background-color: #ccc;
}
.tab-content {
    flex: 3;
    padding: 20px;
    border-left: 1px solid #ccc;
}
.tab-content h2 {
    margin-top: 0;
}
@media screen and (max-width: 600px) {
    .tab-container {
        flex-direction: column;
    }
    .tab-links {
        flex: none;
        width: 100%;
    }
    .tab-content {
        flex: none;
        width: 100%;
        border-left: none;
        border-top: 1px solid #ccc;
    }
}
</style>
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
