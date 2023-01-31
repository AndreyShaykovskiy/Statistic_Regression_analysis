Дана база с информацией о характеристиках автомобилей (данные в файле cars.csv).

### Задачи:
1. Определить от каких факторов зависит ценообразование на автомобили.
2. Определить, какие переменные важны для прогнозирования и насколько хорошо полученная модель описывает данные.
3. Предсказать стоимость машин
### После некоторых преобразований данных была построена первая модель всего с одним предиктором цены: (price) – horsepower
Данная модель объясняет 65% изменчивости цен.
![2023-01-31_23-05-28](https://user-images.githubusercontent.com/122619433/215870736-2175cf04-351a-4f15-8ba6-1137f8fa2f79.png)
### Затем была построена модель со всеми предикторами
Данная модель объясняет 95% изменчивости цен. Однако только 3 марки машин значимы в данной модели (p<0.05)
![2023-01-31_23-08-25](https://user-images.githubusercontent.com/122619433/215871353-5f956786-5a3c-4442-83fb-7b4152006268.png)
![2023-01-31_23-16-16](https://user-images.githubusercontent.com/122619433/215872927-37503c46-fb6e-4053-9567-fec762e06691.png)
![2023-01-31_23-17-42](https://user-images.githubusercontent.com/122619433/215873206-14326dd6-cf2a-46bc-8b87-4e32838a1852.png)
### Затем была построена модель со всеми предикторами, кроме марок машин
Данная модель объясняет 90% изменчивости цен. Среди предикторов 11 из 28 оказались не значимыми (p > 0.05)
![2023-01-31_23-20-34](https://user-images.githubusercontent.com/122619433/215873855-42e347ce-aa7f-4169-8b96-425a10437705.png)
![2023-01-31_23-22-07](https://user-images.githubusercontent.com/122619433/215874480-197c5742-9b30-4ca9-9d65-4267830e098c.png)
### Итог: так как Adj. R-squared в последних двух моделях изменился не значительно, то лучше выбрать модель без марок машин
### Интерпретация (предсказание цены) при условии, что остальные переменные остаются неизменными:
- при единичном изменении показателя horsepower, цена ВОЗРАСТАЕТ на 86.8164
- при единичном изменении показателя enginesize, цена ВОЗРАСТАЕТ на 36.0515
- при единичном изменении показателя wheelbase, цена ВОЗРАСТАЕТ на 71.1868 и т.д.
