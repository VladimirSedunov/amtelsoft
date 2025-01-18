<h1 align="center">Проект по тестированию сайта<br>"Амтел-Софт - цифровой интегратор."</h1>
> <a target="_blank" href="https://amtelsoft.ru/">Ссылка на единый портал</a>
<hr>

![This is an image](/design/images/main_page.PNG)

### Список проверок, реализованных в автотестах
- [x] Наличие требуемых заголовков на каждой из страниц, соответствующих пунктам в главном (верхнем) меню
- [x] Наличие текста "+7(495)108-95-07" и "info@amtelsoft.ru" на основной странице
- [x] Наличие сообщения 'Not Found' и 'The requested URL was not found on this server.' при попытке перехода на несуществующую страницу
- [x] Наличие подпунктов меню главного меню (при наведении курсора мыши) и корректное открытие соответствующих страниц
- [x] Проверки при отправке сообщений из меню "Отправка сообщения из блока 'Свяжитесь с нами прямо сейчас.'" с корректным и некорректными наборами реквизитов, реализованные с помощью параметризации теста.
- [x] Проверка контактных данных на главной странице (адрес, email и телефон есть и соответствуют реальным данным).

## Проект реализован с использованием
Python = Pytest = Selenium = Selene = Selenoid = Allure Report = Jenkins = Telegram = Java

![](/design/icons/Python.png)&emsp;![](/design/icons/Pytest.png)&emsp;![](/design/icons/Selenium.png)&emsp;![](/design/icons/Selene.png)&emsp;![](/design/icons/Selenoid.png)&emsp;![](/design/icons/Allure_Report.png)&emsp;![](/design/icons/Jenkins.png)&emsp;![](/design/icons/Telegram.png)&emsp;![](/design/icons/Java.png)


## Запуск автотестов выполняется на сервере Jenkins


### Параметры сборки

* SELECT_TESTS (default: tests -m jenkins_ok). Параметр определяет группу тестов или отдельный тест для запуска.
* browser (default: chrome). Браузер chrome или firefox.
* browser_version (default: 96.0). Версия браузера на Selenoid.
* window_size (default: 1920x1080). Размер окна браузера.


### Для запуска автотестов в Jenkins
#### 1. Открыть проект

![](/design/images/jenkins1.PNG)

#### 2. Выбрать пункт "Собрать с параметрами"
#### 3. В случае необходимости изменить параметры, выбрав значения из выпадающих списков
#### 4. Нажать "Собрать"
#### 5. Результат запуска сборки можно посмотреть в отчёте Allure
![](/design/images/jenkins2.png)

## Локальный запуск автотестов
Пример командной строки:
```
pytest tests -m jenkins_ok
```

Получение отчёта:
```
allure.bat serve allure-results
```

## Настроено автоматическое оповещение о результатах сборки Jenkins в Telegram-бот
![](/design/images/telegram_bot.PNG)


## Видеоотчёт теста
![](https://github.com/VladimirSedunov/amtelsoft/tree/master/design/video/test_video.mp4)
https://github.com/VladimirSedunov/amtelsoft/tree/master/design/video/test_video.mp4
![](https://github.com/VladimirSedunov/amtelsoft/blob/master/design/video/test_video.mp4)
