# Проект по Сегментации дефектов на Изображениях
___

## Описание Проекта
Этот проект посвящен разработке системы автоматического распознавания и сегментации дефектов(грязи) на камере с использованием глубокого обучения. Основной задачей является создание модели U-Net, способной предсказывать маски сегментации для изображений, применимых в задачах анализа данных.
Модель реализована на TensorFlow с использованием предобученной архитектуры MobileNetV2 для извлечения признаков и библиотеки Pix2Pix для повышения качества результата.
___

## Основные Характеристики

    Архитектура: U-Net с предобученной MobileNetV2 в качестве энкодера
    Задача: Бинарная сегментация (объект/фон)
    Фреймворк: TensorFlow 2.x
    Размер входных изображений: 224x224 пикселей
    Метрики качества: Accuracy, Binary IoU
___

## Структура Проекта
    Nornikel_Hack/                
    ├── main.ipynb                         # Основной ноутбук с кодом проекта
    ├── README.md                          # Документация проекта         
    ├── train_dataset.zip                 # Исходные данные для обучения
___

Процесс Обучения
1. Предобработка Данных

    Загрузка и чтение изображений и масок из файлов.
    Изменение размера изображений и масок до 224x224 пикселей.
    Нормализация данных:
        Изображения нормализуются к диапазону [0, 1].
        Маски делятся на максимальное значение пикселей.
___

2. Аугментация Данных

Для повышения устойчивости модели используется горизонтальное отражение изображений и масок.
___

3. Разделение Данных

    Тренировочная выборка: 70%
    Тестовая выборка: 30%
___

4. Настройки Обучения

    Оптимизатор: Adam (learning rate = 1e-5)
    Функция потерь: Binary Crossentropy
    Размер батча: 8
    Количество эпох: 25
___

Результаты

    Модель успешно обучена для бинарной сегментации объектов.
    Визуализация результатов предсказания включает входное изображение, истинную маску и предсказанную маску.
    Основные метрики:
        Accuracy
        Binary IoU
___

Требования

    Python 3.x
    TensorFlow 2.x
    NumPy
    Matplotlib
    OpenCV
    Google Colab (для запуска ноутбуков)
___

Примечание

Проект разрабатывался на Google Colab с использованием GPU.

