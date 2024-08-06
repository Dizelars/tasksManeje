# Челендж Frontend-разработчика (стажировка)

## Как получить проект из репозитория и запустить?
1. Создаем пустую папку, открываем ее в редакторе __Visual Studio Code__
2. Запускаем терминал, и в нем добавляем второй терминал __bash__
3. Вводим следующий набо команд в терминал __bash__:
	* Копирование проекта в папку:
	    + ```git clone https://github.com/Dizelars/tasksManeje```
	* Создаем свою уникальную ветку:
		+ ```git checkout -b имя_ветки_например_ваша_фамилия```
4. Переключаемся на обычный терминал, и вводим следующие команды для работы проекта:
	* Проверяем что мы в нужной папке:
		+ Последняя папка должна называться __tasksManeje__
        + Чтобы перейти в другую папку введите команду: ```cd название_папки```
	* Устанавливаем проект:
		+ ```npm install```
	* Запускаем проект:
		+ ```npm run dev```

Если не понятно в какой вы сейчас ветке, то текущая ветка указывается в скобках синим цветом, чтобы перейти на какую то ветку, вводим команду: ```git checkout имя_ветки```

Все готово, можно знакомиться со структурой проекта и заданиями.

Для того, чтобы зафиксировать свою работу, находясь в __своей ветке__, вводим последовательность команд:
1. Сохраняем свои наработки:
    * ```git add .```
2. Комментируем их:
    * ```git commit -m"свой комментарий, например, какие задания сделали"```
3. Заливаем в свою уникальную ветку:
    * ```git push origin ту_что_создавали_ранее```

__Готов, результат сохранен!!__

## Структура проекта:
Есть 2 основные папки, __src__ и __static__, с ними нам и предстоит взаимодействовать.

Файлы вне этих папок мы __не изменяем__, но открыть никто не запрещает

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

## Тебя ждет 3 задачи

### Задача №1 (CSS (Grid + Flexbox))
__Цель:__

Починить сетку карточек, используя __Grid__ для расположения карточек внутри контейнера и __Flexbox__ для расположения контента внутри карточек.

__Описание:__
* __HTML:__
    + Верстка карточек уже готова, нужно ее изучить.
* __CSS:__
    + Используйте __Grid__ для размещения карточек в контейнере;
    + На экранах __шире 1200px__ карточки должны располагаться в __4 колонки__;
    + На экранах шириной __1200px и меньше__ карточки должны располагаться в __3 колонки__, при этом одна карточка должна быть расположена внизу слева;
    + На экранах шириной __1024px и меньше__ карточки должны располагаться в __2 колонки__;
    + На экранах шириной __500px и меньше__ карточки должны располагаться в __1 колонку__, друг под другом;
    + __Карточки и изображения__ внутри них должны быть __одинакового__ размера;
    + Используйте __Flexbox__ для расположения контента __внутри карточек__.

### Задача №2 (CSS (Анимации @keyframe))
__Цель:__

Создать анимацию, чтобы при наведении на карточку, блок с классом __.pulse__ внутри карточки, начал увеличиваться в размерах, создавая эффект пульсации под блоком с классом __.date_svg__.

__Описание:__
* __HTML:__
    + Используйте уже готовую верстку из 4-х карточек.
* __CSS:__
    + Создайте __анимацию пульсации при наведении__ на карточку, для блока с классом __.pulse__ внутри карточки;
    + Анимации должны быть плавными и пропорциональными.

### Задача №3 (JavaScript (получение данных из JSON))
__Цель:__

Найти и устранить баги, мешающие использовать данные из __JSON-файла__ для динамической __отрисовки карточек__ (фото, дата, заголовок и описание).

__Описание:__
* __HTML:__
    + Верстка для динамической отрисовки карточек уже готова;
    + __JSON-файл__ содержит необходимые данные для каждой карточки.
* __CSS:__
    + Используем стили из предыдущих 2-х заданий.
* __JavaScript:__ (файл содержит баги, которые необходимо устранить)
    + Функция __loadCardsFromJson__ не может получить все карточки;
    + Функция __createCardHTML__ выводит одинаковые карточки, а нам необходимы уникальные карточки, на основе данных из __JSON-файла__ (фото, дата, заголовок и описание).