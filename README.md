Кластеризация клиентов торгового центра

## Описание проекта
Этот проект демонстрирует применение методов кластеризации (K-means и DEC - Deep Embedded Clustering) к данным о клиентах торгового центра. Анализ позволяет выявить сегменты покупателей на основе их характеристик.

## Данные
Используется датасет `Mall_Customers.csv`, содержащий информацию о клиентах:
- Возраст
- Годовой доход
- Spending Score (оценка расходов, 1-100)

## Структура блокнота

1. **Импорты библиотек** (скрытая ячейка)
   - Pandas, NumPy, Matplotlib, Seaborn
   - Scikit-learn (KMeans, метрики)
   - TensorFlow/Keras (для DEC)

2. **Загрузка и предобработка данных** 

3. **Анализ данных и визуализация** 

4. **Определение оптимального числа кластеров** 
   - Метод локтя
   - Silhouette анализ

5. **Эксперименты с random_state** 
   - Тестирование устойчивости кластеризации

6. **K-means кластеризация** 
   - Обучение модели
   - Визуализация результатов
   - Интерпретация кластеров

7. **DEC (Deep Embedded Clustering)** 
   - Архитектура нейросети
   - Процесс обучения
   - Визуализация результатов

## Результаты кластеризации

### Метрики качества:

**DEC:**
- Silhouette: 0.485 (чем ближе к 1, тем лучше)
- Calinski-Harabasz: 397.9 (чем выше, тем лучше)
- Davies-Bouldin: 0.667 (чем ближе к 0, тем лучше)

**K-Means:**
- Silhouette: 0.452
- Calinski-Harabasz: 233.6
- Davies-Bouldin: 0.736

## Как использовать
1. Откройте блокнот в Google Colab или Jupyter Notebook
2. Запустите ячейки последовательно
3. Для просмотра скрытых ячеек:
   - В Colab: меню "View" → "Show hidden cells"
   - В Jupyter: щелкнуть по скрытой ячейке

## Требования
- Python 3.7+
- Библиотеки: pandas, numpy, matplotlib, seaborn, scikit-learn, tensorflow

## Интерпретация результатов
DEC показал лучшие результаты по всем метрикам, что свидетельствует о более четком разделении на кластеры по сравнению с K-means. Это особенно заметно по индексу Calinski-Harabasz, где DEC превосходит K-means почти в 1.7 раза.
