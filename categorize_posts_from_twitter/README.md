# Yandex_Practicum_test_task

В этом задании будем классифицировать посты из твиттера.

В файле train.csv мы найдем 30 000 постов, каждый из которых сопоставлен с одним из 13 классов эмоций.

В test.csv находятся еще 10 000 постов, для которых эмоцию нужно предсказать.

Результат предсказания положим в файл test_predictions.csv.

Метрика качества - *accuracy*.

**Для работы с данным заданием мы применяли библиотеки:**

- *torch*: библиотека PyTorch применяется в задачах обработки естественного текста и компьютерного зрения
- *transformers*: библиотека PyTorch для работы с моделями типа BERT
- *tqdm*: библиотека, которая наглядно показывает индикатор прогресса. В Jupyter применим функцию notebook() из этой библиотеки в момент создания эмбеддингов
- *pymystem3*: библиотека предоставляет программный интерфейс к анализатору для языка программирования Python
- *Mystem*: морфологический анализатор
- *re*: встроенный модуль для работы с регулярными выражениями
- *nltk*: пакет библиотек и программ для символьной и статистической обработки естественного языка
- *TfidfVectorizer*: счётчик величин TF-IDF
- *train_test_split*: функция для разделения датафрейма перед обучением
- *GridSearchCV*: инструмент для автоматического подбора параметров для моделей машинного обучения

**Модели машинного обучения:**

- DecisionTreeClassifier
- RandomForestClassifier
- LogisticRegression

**Мы применили метод подготовки текстов к обучению BERT.**

С помощью BERT мы создали векторные представления постов.

Также был предложен метод подготовки постов - TF-IDF. С помощью TF-IDF можно провести оценку важности слов.

После подготовки постов мы обучили 3 модели машинного обучения: Классификатор дерева решений, Случайный лес и Логистическая регрессия.
С помощью метрики **accuracy** мы выбрали наилучшую модель машинного обучения и с помощью нее получили целевые признаки - эмоцию - для тестового датасета.

Результат предсказания мы сохранили в файл **test_predictions.csv**.

**Дополнительно**

Для применения метода BERT была использована предобученная многоязычная модель BERT-base:
- *http://files.deeppavlov.ai/deeppavlov_data/bert/multi_cased_L-12_H-768_A-12_pt.tar.gz*

data_features_train и data_features_test, полученные путем создания эмбеддингов можно посмотреть:
- *data_features_train: https://drive.google.com/file/d/1Dd60PY35epstIC3g_str27SPjqbWDx8O/view?usp=sharing*
- *data_features_test: https://drive.google.com/file/d/1qKUGqiZ_9hBctSLn1bJ-xA2MM1YPUGVE/view?usp=sharing*
