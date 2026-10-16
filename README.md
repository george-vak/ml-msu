# ML-MSU — практические работы по машинному обучению

Здесь собраны мои домашние работы по курсу ML-MSU за 2024–2025 учебный год.

В заданиях я готовлю данные, обучаю модели, подбираю параметры и сравниваю результаты. Некоторые вещи, например масштабирование, кросс-валидацию и кодирование категорий, реализую самостоятельно.

Работы разделены на две части:

- `base` — применение некоторых методов на практике.
- `research` — дополнительные эксперименты и более подробный разбор определенных тем.

Решения находятся в Jupyter-ноутбуках и отдельных `.py`-файлах. В ноутбуках оставлены условия заданий, код, графики и выводы. Условия и шаблоны взяты из материалов курса.

## Темы и структура

### Базовая часть

| Каталог | Содержание |
| --- | --- |
| [01_python_intro](base/01_python_intro/) | Функции, строки, коллекции, классы и итераторы Python |
| [02_numpy_pandas_matplotlib](base/02_numpy_pandas_matplotlib/) | Работа с таблицами и массивами, анализ популярных видео на YouTube, построение графиков |
| [03_sklearn_scaling_cv](base/03_sklearn_scaling_cv/) | Метод ближайших соседей, масштабирование признаков и подбор параметров на кросс-валидации |
| [04_data_analysis_feature_processing](base/04_data_analysis_feature_processing/) | Анализ Airbnb: типы признаков, пропуски, выбросы, кодирование категорий |
| [05_linear_models_regression](base/05_linear_models_regression/) | Линейная регрессия, Ridge и Lasso, регуляризация и оценка ошибки |
| [06_linear_models_classification](base/06_linear_models_classification/) | Логистическая регрессия на задаче прогноза дождя, оценка качества классификации |
| [07_svm](base/07_svm/) | Метод опорных векторов, разные ядра и сравнение с логистической регрессией |
| [08_decision_tree](base/08_decision_tree/) | Деревья решений: выбор глубины, переобучение и важность признаков |
| [09_random_forest_feature_selection](base/09_random_forest_feature_selection/) | Случайный лес, влияние числа деревьев на результат и отбор признаков |
| [10_boosting_part_1](base/10_boosting_part_1/) | Сравнение четырёх реализаций градиентного бустинга на ценах автомобилей |
| [11_boosting_part_2](base/11_boosting_part_2/) | Подбор параметров бустинга с GridSearchCV и Hyperopt, прогноз числа наград фильмов |
| [12_clusterization](base/12_clusterization/) | Метрики кластеризации Silhouette и B-Cubed в `solution.py`; задания в ноутбуке выполнены частично |

### Исследовательская часть

| Каталог | Содержание |
| --- | --- |
| [01_numpy_pandas_matplotlib](research/01_numpy_pandas_matplotlib/) | Дополнительный анализ YouTube и сравнение скорости обычного Python-кода с NumPy |
| [02_knn](research/02_knn/) | Влияние масштабирования на kNN, классификация текстов с CountVectorizer и TF-IDF |
| [03_linear_models_regression](research/03_linear_models_regression/) | Как L1- и L2-регуляризация влияют на веса линейной модели |
| [04_linear_models_classification](research/04_linear_models_classification/) | Обучение логистической регрессии и сравнение способов кодирования категорий |
| [05_svm](research/05_svm/) | SVM при дисбалансе классов, сокращение числа признаков с PCA и калибровка вероятностей |
| [06_ensembles](research/06_ensembles/) | Объединение моделей: голосование, бэггинг, стекинг и блендинг; задача на данных о физических потенциалах |

Основные инструменты: Python, Jupyter Notebook, NumPy, pandas, scikit-learn, Matplotlib и Seaborn. В заданиях по бустингу — XGBoost, LightGBM, CatBoost и Hyperopt.

## Просмотр и запуск

Ноутбуки можно смотреть прямо на GitHub — результаты и графики сохранены. Для запуска подойдёт Jupyter или Google Colab.

Для локального запуска создайте отдельное окружение из корня репозитория:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install jupyterlab numpy pandas scipy scikit-learn matplotlib seaborn plotly tqdm gdown
python -m pip install catboost==1.2.7 xgboost lightgbm hyperopt
python -m jupyter lab
```

На Windows окружение активируется командой `.venv\Scripts\activate`. Открывайте ноутбук из его папки, чтобы работали импорты соседних `.py`-файлов.

Часть ноутбуков написана для Colab, поэтому при локальном запуске нужно заменить пути `/content/...` на свои. Не все данные лежат в репозитории: в ноутбуках есть команды и ссылки для их загрузки. Для исследовательского задания по классификации можно взять `weatherAUS.csv` из `base/06_linear_models_classification/`.

Работы выполнялись с версиями библиотек 2024–2025 года. Команды выше устанавливают основные зависимости; если возникают ошибки совместимости, версии можно сверить с requirements-файлом курса, который скачивается в начальных ячейках ноутбуков.
