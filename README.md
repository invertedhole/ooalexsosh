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
        <span> id="tab1" class="tab-content active">
            <p>Контактные данные
<p>Директор:+7 990 077 2103
<p>Отдел кадров +7 990 058 1933</p>   
</span>
            <div id="tab2" class="tab-content"> 
<div class="tabs-container">
  <div class="tab">
    <div class="tab-content">
      <!-- Контент для первой вкладки -->
    </div>
  </div>
  <div class="tab">
    <div class="tab-content">
      <!-- Контент для второй вкладки -->
    </div>
  </div>
  <!-- Добавьте другие вкладки с аналогичной структурой -->
.tabs-container {
  display: flex;
  flex-direction: column;
  border: 1px solid #ccc;
  border-radius: 5px;
  overflow: hidden;
}
.tab {
  display: none;
  flex-grow: 1;
  padding: 10px;
  transition: background-color 0.3s ease;
}
.tab:hover {
  background-color: #f2f2f2;
}
.tab.active {
  display: flex;
  background-color: #f2f2f2;
}
.tab-content {
  display: none;
  flex-grow: 1;
  padding: 10px;
  transition: opacity 0.3s ease;
}
.tab-content.active {
  display: flex;
  opacity: 1;
}
.tab.active .tab-content.active {
  animation: fadeIn 0.3s ease;
}
@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
const tabs = document.querySelectorAll('.tab');
tabs.forEach(tab => {
  tab.addEventListener('click', () => {
    tabs.forEach(tab => tab.classList.remove('active'));
    tab.classList.add('active');

    const tabNumber = tab.getAttribute('data-tab');
    const tabContents = document.querySelectorAll('.tab-content');

    tabContents.forEach(content => content.classList.remove('active'));
    tabContents[tabNumber - 1].classList.add('active');
  });
});
Вы можете загрузить файл с этим скриптом на GitHub, но он не будет работать на GitHub Pages. Вместо этого, используйте CSS-псевдоклассы для управления активными вкладками:

.tab:target {
  display: flex;
  background-color: #f2f2f2;
}
.tab:target .tab-content {
  display: flex;
  opacity: 1;
}
<div class="tabs-container">
  <div class="tab" id="tab1">
    <div class="tab-content">
      <!-- Контент для первой вкладки -->
    </div>
  </div>
  <div class="tab" id="tab2">
    <div class="tab-content">
      <!-- Контент для второй вкладки -->
    </div>
  </div>
  <!-- Добавьте другие вкладки с аналогичной структурой -->
</div>
<syle>
.tabs-container {
  display: flex;
  flex-direction: column;
  border: 1px solid #ccc;
  border-radius: 5px;
  overflow: hidden;
}
.tab {
  display: none;
  flex-grow: 1;
  padding: 10px;
  transition: background-color 0.3s ease;
}
.tab:hover {
  background-color: #f2f2f2;
}
.tab.active {
  display: flex;
  background-color: #f2f2f2;
}
.tab-content {
  display: none;
  flex-grow: 1;
  padding: 10px;
  transition: opacity 0.3s ease;
}
.tab-content.active {
  display: flex;
  opacity: 1;
}
.tab.active .tab-content.active {
  animation: fadeIn 0.3s ease;
}
@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.tab:target {
  display: flex;
  background-color: #f2f2f2;
}

.tab:target .tab-content {
  display: flex;
  opacity: 1;
} 
</syle>
  </div>
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
