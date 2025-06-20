# Telegram-бот для Московского Зоопарка


## Описание бота
Этот telegram-бот написан к дополнению основного телеграм-канала и сайта **Московского Зоопарка**. \
Бот содержит в себе викторину на тему "Какое Ваше тотемное животное" и дополнительную 
информацию про существующую **программу опеки** Московского Зоопарка. \
**Цель бота**, привлечь внимание к программе и помочь пользователю подобрать животное для опекунства.


### Возможности бота
- Модуль викторины "Какое твоё тотемное животное"
- Информация о программе опеки
- Модуль обратной связи (связь с сотрудником)
- Механизм по сохранению отзывов от пользователей
- Механизм, позволяющий отправить результат прохождения викторины
- Скрытый модуль Администрирования бота


## Установка, настройка и запуск
Установить необходимые библиотеки из файла requirements.txt `pip install -r requirements.txt`
Настройте конфиг (.env). 
   1. (необязательный шаг) Чтобы администрировать бота через телеграм, укажите в переменную 
   **ADMIN_USER** id телеграм пользователей у которых будут доступ к команде **/admin**
   2. Пропишите токен бота.
Разверните базу данных (необязательный шаг. Файл с базой есть в проекте).
   1. (необязательный шаг) У бота есть файл **modul_quiz/questions_db.json** в котором описаны 
   стартовые вопросы по викторине.
   Если хотите составить свой список - поправте этот файл.
   2. Запустите файл **deploy_database.py**. Таким образом вы создадите у себя базу данных 
   (**database_bot.db**), в которой уже будут данные для викторины.
Запустите проект: `python app.py`

.env: \
**TOKEN** - токен бота \
**DB_URL** - путь до базы данных \
**COL_QUESTIONS** - отвечает за количество вопросов в викторине \
**ADMIN_USER** - id телеграм пользователей, которым будет доступен модуль администрирования бота 
(можно оставить пустым)

Контактная информация менеджера, которая отображается пользователю при нажатии
на кнопку "Связь с сотрудником" (по умолчанию указаны тестовые данные) \
**MANAGER_NAME** - Имя \
**MANAGER_EMAIL** - email адрес \
**MANAGER_PHONE** - телефон \
**MANAGER_TELEGRAM_ID** - id телеграм пользователя, которому отправится копия сообщения 
когда кто-то нажмет кнопку "Связь с сотрудником"
