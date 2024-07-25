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
            background-color: #F5F5DC;
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
     body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}
header {
    background-color: #333;
    color: white;
    padding: 10px 0;
    text-align: center;
}
nav {
    display: flex;
    justify-content: center;
    background-color: #444;
}
nav a {
    color: white;
    padding: 14px 20px;
    text-decoration: none;
    text-align: center;
}
nav a:hover {
    background-color: #555;
}
.content {
    padding: 20px;
}
/* Vertical Tabs */
.vertical-tabs {
    display: flex;
}
.tab {
    flex: 1;
    background-color: #f1f1f1;
    padding: 10px;
    border-right: 1px solid #ccc;
}
.tab button {
    display: block;
    background-color: inherit;
    color: black;
    padding: 10px 15px;
    width: 100%;
    border: none;
    outline: none;
    text-align: left;
    cursor: pointer;
    transition: 0.3s;
}
.tab button:hover {
    background-color: #ddd;
}
.tab button.active {
    background-color: #ccc;
}
.tabcontent {
    flex: 3;
    padding: 10px;
    border-left: 1px solid #ccc;
    display: none;
}
.tabcontent.show {
    display: block;
}
footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px 0;
    position: fixed;
    width: 100%;
    bottom: 0;
}
    </style>
</head>
<body>
    <header>
        <!-- Заголовок сайта -->
        <h1>ГБУ ОО ЗО "Алексеевская СОШ"</h1>
 <img src="https://raw.githubusercontent.com/invertedhole/ooalexsosh/main/картинка2.PNG">
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
          </div>
           <div id="tab2" class="tab-content active">
<body>
    <header>
        <img src="images/logo.png" alt="Logo">
        <h1>Welcome to My Website</h1>
    </header>
    <nav>
        <a href="index.html">Home</a>
        <a href="about.html">About</a>
        <a href="services.html">Services</a>
        <a href="contact.html">Contact</a>
    </nav>
    <div class="content">
        <h2>Home Page</h2>
        <p>This is the home page content.</p>
        <!-- Vertical Tabs -->
        <div class="vertical-tabs">
            <div class="tab">
                <button class="tablinks" onclick="openTab(event, 'Tab1')">Tab 1</button>
                <button class="tablinks" onclick="openTab(event, 'Tab2')">Tab 2</button>
                <button class="tablinks" onclick="openTab(event, 'Tab3')">Tab 3</button>
            </div>
            <div id="Tab1" class="tabcontent">
                <h3>Tab 1</h3>
                <p>Content for Tab 1.</p>
            </div>
            <div id="Tab2" class="tabcontent">
                <h3>Tab 2</h3>
                <p>Content for Tab 2.</p>
            </div>
            <div id="Tab3" class="tabcontent">
                <h3>Tab 3</h3>
                <p>Content for Tab 3.</p>
            </div>
        </div>
    </div>
    <footer>
        <p>&copy; 2024 My Website</p>
    </footer>
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
// Simple script to highlight the current page in the navigation menu
document.addEventListener("DOMContentLoaded", function () {
    const currentPath = window.location.pathname;
    const navLinks = document.querySelectorAll("nav a");
    navLinks.forEach(link => {
        if (link.getAttribute("href") === currentPath) {
            link.style.backgroundColor = "#555";
        }
    });
});
function openTab(evt, tabName) {
    var i, tabcontent, tablinks;
    // Get all elements with class="tabcontent" and hide them
    tabcontent = document.getElementsByClassName("tabcontent");
    for (i = 0; i < tabcontent.length; i++) {
        tabcontent[i].style.display = "none";
    }
    // Get all elements with class="tablinks" and remove the class "active"
    tablinks = document.getElementsByClassName("tablinks");
    for (i = 0; i < tablinks.length; i++) {
        tablinks[i].className = tablinks[i].className.replace(" active", "");
    }
    // Show the current tab, and add an "active" class to the button that opened the tab
    document.getElementById(tabName).style.display = "block";
    evt.currentTarget.className += " active";
}
// Show the first tab by default
document.addEventListener("DOMContentLoaded", function () {
    document.querySelector(".tablinks").click();
});
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
