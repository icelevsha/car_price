# Моделирование задачи регрессии

Проект посвящён решению задачи регрессии на табличных данных с помощью различных моделей машинного обучения. Цель - сравнить качество моделей и выбрать наилучшую по метрике MAE.

---

## Этапы работы

1.  **Загрузка и первичный анализ данных**
   - Разделение на признаки (`X`) и целевую переменную (`y`)
   - Проверка и обработка пропущенных значений
   - Декодирование категориальных признаков (`OneHotEncoder`)
   - Визуализация корреляций между признаками

2.  **Предобработка**
   - Разделение на обучающую и тестовую выборки (`train_test_split`)
   - Масштабирование данных (`StandardScaler`)

3.  **Обучение моделей**
   Модели обучались с использованием единого пайплайна и оценивались по **MAE (Mean Absolute Error)**:

   - `LinearRegression()`
   - `Ridge(alpha=1.0)`
   - `Lasso(alpha=0.1)`
   - `DecisionTreeRegressor(max_depth=5, random_state=42)`
   - `RandomForestRegressor(n_estimators=100, random_state=42)`
   - `GradientBoostingRegressor(n_estimators=100, learning_rate=0.1, random_state=42)`
   - `KNeighborsRegressor(n_neighbors=5)`

4. **Оценка и визуализация результатов**
   - Вычисление MAE на тестовой выборке для каждой модели
   - Визуализация результатов с помощью `matplotlib` (столбчатая диаграмма)
