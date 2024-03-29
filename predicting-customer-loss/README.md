# Прогнозирование оттока клиентов (client loss)

Оператор связи хочет научиться прогнозировать отток клиентов. Для любого бизнеса важно не только привлекать новых клиентов, но и удерживать уже существующих.
Зачастую, удержать клиента дешевле, чем привлечь нового.
Прогнозируя отток, бизнес может вовремя среагировать и сдеать попытку удержать клиента, который хочет уйти.

Команда оператора собрала персональные данные о некоторых клиентах, информацию об их тарифах и договорах. Нам предоставлен набор данных, который содержит информацию о 7 043 пользователях, их демографических характеристиках, услугах, которыми они пользуются, длительности пользования услугами оператора, методе оплаты, размере оплаты.

## Задача: Проанализировать данные и спрогнозировать отток пользователей

### План:
    1. Предобработка данных
        1.1. Обзор данных
        1.2. Исследование данных на наличие задублированных данных
    2. Исследовательский анализ данный
        2.1. Исследование данных на наличие выбросов
        2.2. Построение гистограмм
        2.3. Приведение целевого признака к бинарному виду
        2.4. Оценка баланса классов
    3. Слияние датафреймов
        3.1. Слияние выбранных столбцов
        3.2. Заполнение пустых значений
        3.3. Преобразование категориальных признаков
    4. Подготовка обучающей и тестовой выборки
        4.1. Разделение выборок
        4.2. Стандартизация численных признаков
        4.3. Борьба с дисбалансом
    5. Машинное обучение
        5.1. Обучить несколько моделей, выбрать наилучшую
        5.2. Усовершенствовать выбранную модель
        5.3. Подготовить отчет
        5.4. Сформулировать рекомендации для бизнеса

Оператор предоставляет два основных типа услуг:
    1. Стационарную телефонную связь. Возможно подключение телефонного аппарата к нескольким линиям одновременно.
    2. Интернет. Подключение может быть двух типов: через телефонную линию (DSL, от англ. digital subscriber line, «цифровая абонентская линия») или оптоволоконный кабель (Fiber optic).

Также доступны такие услуги:
    - Интернет-безопасность: антивирус (DeviceProtection) и блокировка небезопасных сайтов (OnlineSecurity);
    - Выделенная линия технической поддержки (TechSupport);
    - Облачное хранилище файлов для резервного копирования данных (OnlineBackup);
    - Стриминговое телевидение (StreamingTV) и каталог фильмов (StreamingMovies).

За услуги клиенты могут платить каждый месяц или заключить договор на 1–2 года. Доступны различные способы расчёта и возможность получения электронного чека.

Данные состоят из файлов, полученных из разных источников:
    - contract.csv — информация о договоре;
    - personal.csv — персональные данные клиента;
    - internet.csv — информация об интернет-услугах;
    - phone.csv — информация об услугах телефонии.

Во всех файлах столбец customerID содержит код клиента.

Информация о договорах актуальна на 1 февраля 2020.

## Используемые библиотеки:
    pandas
    numpy
    datetime
    seaborn
    matplotlib
    sklearn
    catboost
    lightgbm
