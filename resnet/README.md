# Определение возраста покупателей
Сетевой супермаркет внедряет систему компьютерного зрения для обработки фотографий покупателей. Фотофиксация в прикассовой зоне поможет определять возраст клиентов, чтобы:
<br> - Анализировать покупки и предлагать товары, которые могут заинтересовать покупателей этой возрастной группы;
<br> - Контролировать добросовестность кассиров при продаже алкоголя.
<br>Нужно построить модель, которая по фотографии определит приблизительный возраст человека. 
<br>В нашем распоряжении набор фотографий людей с указанием возраста.
<br>В датасете 7591 фотографий людей разного возраста: от года до ста лет. Большая всего фотографий людей от 20 до 30 лет. Разное освещение на фотографиях, качество, цветовая гамма и положение головы. Будем увеличивать обучающую выборку с помощью аугментации изображений.
## Итог
Для определения возраста посетителей супермаркета использовалась сверточная нейросеть ResNet, адаптированная под нашу задачу. Загружались предобученные веса.
<br>Использовался оптимизатор Adam с показателем learning_rate 0.0001.
<br> Для определения качества обучения использоваталась метрика MAE. На тесте на 20 эпо модель показала результат 6.3429, что является хорошим резутальтом. 