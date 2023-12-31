﻿# text-prediction

## Цели работы:
-	Реализовать алгоритм LSTM.
-	Сравнить решение с марковской цепью (автоматом).
-	Анализ результатов.

## Набор данных

Выберите любой доступный достаточно длинный текст. Разбейте текст по предложениям на строки. Максимально сократите число различных символов в тексте: приведите все буквы к нижнему регистру, уберите лишние знаки препинания. Если используемая модель будет плохо или медленно обучаться, разбейте текст на строки по словам. В таком случае в качестве набора данных можно взять какой-либо словарь.
Используя one-hot кодирование, получите векторное представление каждого символа. В том числе и символа конца строки (точки или пробела), после которого генерация строки прекращается. Хотя её также следует искусственно ограничить максимальной длинной строки.
Задание
Обучите модель на выбранном тексте. И используйте обученную модель для генерации продолжения строки по её началу. Задачу стоит решить двумя моделями: LSTM и марковской цепью (автоматом).
## LSTM
Обучите LSTM предсказывать следующий символ по предыдущим. Обучать стоит по одной строке. Для обучения можно использовать любую подходящую функцию ошибки (например MSE или CrossEntropy). Для обучения используйте адаптивный градиентный спуск.
	Для предсказания следующего символа можно использовать arg-max вектора ответа либо использовать случайный символ с вероятностью, полученной soft-arg-max-ом.

В реализации разрешается использовать `tf.keras.layers.RNN` 

