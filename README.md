# Челендж Frontend-разработчика (стажировка)

## Структура проекта:
Есть 2 основные папки, __src__ и __static__, с ними нам и предстоит взаимодействовать.
Файлы вне этих папок мы __не изменяем__, но глянуть никто не запрещает

Папка __src__:

Внутри этой папки находится весь код проекта:
* Папка __fonts__, содержит файлы шрифтов;
* Папка __js__, содержит 2 файла:
    + __dataCards.json__ - содержит __JSON__ данные, необходимые для наполнения контента карточек;
    + __renderCards.js__ - содержит код __JavaScript__, отвечающий за отрисовку карточек, на основе данных из файла __JSON__.
* Папка __style__ содержит структуру стилей:
    + Папка __default__, содержит 2 файла:
        - __base.css__ - сброс стилей при помощи __reset.css__ + стили контейнера и __body__ (__не редактируем__);
        - __fonts.css__ - подключение шрифтов из знакомой уже папки __fonts__ (__не редактируем__).
    + Папка __layout__, содержит 4 файла:
        - __cardAnimation.css__ - анимации;
        - __cardMedia.css__ - медиа-запросы;
        - __cardStyle.css__ - основные стили;
        - __main.css__ - содержит все стили из 3-х файлов выше (__не редактируем__).
* Файл __index.html__ - основной файл с версткой __HTML__;
* Файл __script.js__ - основной файл __JavaScript__, содержащий все скрипты из папки __js__, и подключаемый к основной странице __HTML__, то-есть __index.html__;
* Файл __style.css__ - основной файл стилей __CSS__, содержащий все стили из папки __style__, и подключаемый к основной странице __HTML__, то-есть __index.html__.

Папка __static__:

Внутри этой папки находится контент для наполнения страницы:
* Папка __images__, содержит изображения для карточек.

## Тебя ждет 3 задачи (можно выполнять в любом порядке)

### Задача №1 (CSS (Grid + Flexbox))
__Цель:__

Создать адаптивную сетку карточек, используя __Grid__ для расположения карточек внутри контейнера и __Flexbox__ для расположения контента внутри карточек.

__Описание:__
* __HTML:__
    + Создайте контейнер для карточек с классом __cards_grid-container__;
    + Внутри контейнера создайте 4 карточки с классом __card__, каждая из которых содержит изображение, дату с иконкой, заголовок и краткое описание.

* __CSS:__
    + Используйте __Grid__ для размещения карточек в контейнере;
    + На экранах __шире 1200px__ карточки должны располагаться в __4 колонки__;
    + На экранах шириной __1200px и меньше__ карточки должны располагаться в __3 колонки__, при этом одна карточка должна быть расположена внизу слева;
    + На экранах шириной __1024px и меньше__ карточки должны располагаться в __2 колонки__;
    + На экранах шириной __500px и меньше__ карточки должны располагаться в __1 колонку__, друг под другом;
    + __Карточки и изображения__ внутри них должны быть __одинакового__ размера;
    + Используйте __Flexbox__ для расположения контента __внутри карточек__.