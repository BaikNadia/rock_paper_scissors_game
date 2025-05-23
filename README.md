#  Интерактивная игра "Камень, ножницы, бумага", где пользователь соревнуется с компьютером.

## Как это работает?
1. Выбор пользователя :
Игрок вводит свой выбор ("камень", "ножницы" или "бумага").
Если игрок введёт "выход", игра завершится.

2. Выбор компьютера :
Компьютер случайно выбирает один из трёх вариантов с помощью random.choice().

3. Определение победителя :
Если выборы совпадают, объявляется ничья.
Используются условия для проверки, кто победил, основываясь на правилах игры.

4.Подсчёт очков :
За каждую победу начисляются очки игроку или компьютеру.

## Как можно развивать этот код?
1. Добавить несколько раундов :
Реализовать ограниченное количество раундов (например, 5) и определить общего победителя.

2. Графический интерфейс :
Использовать библиотеку tkinter для создания оконного приложения.

3. Расширить правила :
Добавить новые элементы (например, ящерицу и спока из расширенной версии игры).

# Игра дополнена блоком visual_version:
Что нового?

Функция show_final_score :
Отображает итоговый счёт в диалоговом окне.
После показа результата закрывает окно игры (root.destroy()).
Кнопка "Завершить игру" :
Добавлена новая кнопка, которая вызывает функцию show_final_score.

Сохранение результатов :
Сохранять результаты игры в файл для последующего просмотра.

# Игра дополнена файлом visual.html для запуска игры в браузере

Как это работает?

1.HTML :
Создаёт основную структуру игры.
Кнопки ("Камень", "Ножницы", "Бумага") позволяют игроку сделать выбор.
Отображается текущий счёт (player-score и computer-score) и результат последнего раунда (result).

2.CSS :
Добавляет базовое оформление для кнопок, текста и контейнера игры.
Создаёт привлекательный внешний вид с использованием цветов, отступов и теней.

3.JavaScript :
Логика игры реализована в функции play().
Функция getComputerChoice() генерирует случайный выбор компьютера.
После каждого хода обновляется счёт с помощью updateScores().
Функция resetGame() показывает итоговый счёт в диалоговом окне (alert) и сбрасывает игру.

## Как запустить игру?

Сохраните код в файл с расширением .html (например, rock_paper_scissors.html).

# Игра дополнена файлом visual_add.html для запуска игры в браузере

Как это работает?

HTML :
Добавлены две новые кнопки: "Ящерица" и "Спок".
Структура осталась той же, но теперь доступно 5 вариантов выбора.

CSS :
Новый дизайн сохраняет привлекательный внешний вид, даже при добавлении двух дополнительных кнопок.

JavaScript :
Правила игры реализованы через объект winRules, где для каждого элемента указаны те, которых он побеждает.
Например, "камень" побеждает "ножницы" и "ящерицу".
Если выбор игрока побеждает выбор компьютера, игрок получает очко. В противном случае очко получает компьютер.

Откройте этот файл в любом браузере (Google Chrome, Firefox, Edge и т.д.).

Пример работы

Интерфейс:

Игрок может выбрать один из пяти вариантов: "Камень", "Ножницы", "Бумага", "Ящерица", "Спок".
После каждого хода отображается результат (result) и обновляется счёт.

Ход игры:

Игрок выбирает один из элементов.
Компьютер случайно выбирает свой вариант.

Результат определяется согласно правилам игры:

Камень побеждает ножницы и ящерицу.
Ножницы побеждают бумагу и ящерицу.
Бумага побеждает камень и спока.
Ящерица побеждает спока и бумагу.
Спок побеждает ножницы и камень.

# Игра дополнена блоком visual_version_2:

## Что было изменено?

Добавлен Frame для кнопок :
Создан фрейм (buttons_frame) для группировки кнопок.
Фрейм позволяет лучше контролировать расположение элементов.

Равномерное распределение кнопок :
При создании кнопок используется параметр expand=True и fill="both" для равномерного распределения кнопок по горизонтали.
Параметр padx=5 добавляет отступы между кнопками.

Улучшенная читаемость :
Код стал более организованным благодаря использованию фрейма для кнопок.

## Дополнительные советы
Настройка размера окна :
Если вы хотите, чтобы кнопки занимали больше или меньше места, измените параметр size в функции load_images. Например:

python

images = load_images(images_directory, size=(70, 70))  # Размер иконок 70x70 пикселей

Адаптивность :
Благодаря использованию фрейма и параметров expand=True и fill="both", кнопки будут адаптироваться к размеру окна.

Добавление новых элементов :
Если вы решите добавить новые элементы в игру, просто поместите соответствующие изображения в папку images и обновите словарь win_rules.

