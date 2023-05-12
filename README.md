# Выделение групп пользователей на основе поведения в мобильном приложении "Ненужные вещи"

## Цель проекта:

Отдел менеджмента заказал анализ данных пользователей приложения. Цель - продавать как можно больше товаров, тем самым повысить монитезацию.

## Описание данных:

Датасет содержит данные о событиях, совершенных в мобильном приложении "Ненужные вещи". В нем пользователи продают свои ненужные вещи, размещая их на доске объявлений.

В датасете содержатся данные пользователей, впервые совершивших действия в приложении после 7 октября 2019 года.

Датасет mobile_dataset.csv содержит колонки:

* event.time — время совершения
* event.name — название события
* user.id — идентификатор пользователя

Датасет mobile_sources.csv содержит колонки:

* userId — идентификатор пользователя
* source — источник, с которого пользователь установил приложение

Расшифровки событий:

* advert_open — открытие карточки объявления
* photos_show — просмотр фотографий в объявлении
* tips_show — пользователь увидел рекомендованные объявления
* tips_click — пользователь кликнул по рекомендованному объявлению
* contacts_show и show_contacts — пользователь нажал на кнопку "посмотреть номер телефона" на карточке объявления
* contacts_call — пользователь позвонил по номеру телефона на карточке объявления
* map — пользователь открыл карту размещенных объявлений
* search_1 — search_7 — разные события, связанные с поиском по сайту
* favorites_add — добавление объявления в избранное

## План работы:

1. Загрузка файлов с данными Загрузить данные о событиях и об источниках.

2. Предобработка данных Обьединить две таблицы в одну. Изучить данные и выполнитье предобработку. Есть ли в данных пропуски и дубликаты? Убедится, что типы данных во всех колонках соответствуют сохранённым в них значениям. Обратить внимание на столбцы с датой и временем.

3. Исследовательский анализ данных

* 3.1 Retention Rate.
* 3.2 Время, проведённое в приложении.
* 3.3 Частота действий.
* 3.4 Конверсия в целевое действие - просмотр контактов.

4. Сегментирование пользователей на основе действий

* 4.1 Сегментирование пользователей.
* 4.2 Retention Rate по полученным группам.
* 4.3 Конверсия в целевое действие по группам

5. Проверика гипотезы

* 5.1. Некоторые пользователи установили приложение по ссылке из yandex, другие — из google.
Нулевая гипотеза: Две группы пользователей из yandex и из google не имеют статистической разницы в конверсиях в просмотры контактов.
Альтернативная гипотеза: две эти группы имеют статистическую разницу в конверсиях в просмотры контактов.
* 5.2 Одни пользователи совершают действия tips_show и tips_click, другие — только tips_show.
Нулевая гипотеза: Две группы пользователей не имеют статистической разницы в конверсиях в просмотры контактов.
Альтернативная гипотеза: две эти группы имеют статистическую разницу в конверсиях в просмотры контактов.
* 5.3 Одни пользователи совершают действия tips_show и tips_click, другие — search и advert_open.
Нулевая гипотеза: Две группы пользователей не имеют статистической разницы в конверсиях в просмотры контактов.
Альтернативная гипотеза: две эти группы имеют статистическую разницу в конверсиях в просмотры контактов.
6. Общий вывод и рекомендации
