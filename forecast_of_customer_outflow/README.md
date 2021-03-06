### Прогнозирование оттока клиентов

## Данные

В наличии были следующие данные об абонентах:

* ID пользователя
* датазаключения контракта и дата расторжения(при наличии)
* Переодичность и метод оплаты услуг, средние платежи за месяц/год
* Пол/возрастная группа/семейное положение/наличие детей
* Список услуг интенета/телефонии

Для построения модели были собраны данные по пользователям в 4 таблицы:

*	contract.csv — информация о договоре;
*	personal.csv — персональные данные клиента;
*	internet.csv — информация об интернет-услугах;
*	phone.csv — информация об услугах телефонии.

## Задача

Оператор связи «МиниЛайн» обеспокоен темпами оттока клиентов. Необходимо построить модель, которая предскажет уход клиента

Задача компании минимизировать отток пользователей и не потратить лишние средства на повышении лояльности пользователей, которые уходить не собирались.

## Используются следующие библиотеки:

*	pandas
*	numpy
*	seaborn
*	matplotlib
*	datetime
*	sklearn

## Краткое содержание

* проверяются и правятся данные
* проводится исследовательский анализ
* происходит выбор способа решения и подбор оптимальной модели
* определяются наиболее значимые признаки
* обозначаются проблемы, на которые стоит обратить внимание при сборе данных и выделяется группа, пользователи в которой чаще остальных расторгают контракт
* графическое подкрепление некоторых данных и выводов

### Вывод

Задача компании минимизировать отток пользователей и не потратить лишние средства на повышении лояльности пользователей, которые уходить не собирались. Лучше всего с этой задачей справляется RandomForestClassifier, позволяя не ошибаться в 86 случаев из 100. Это достаточно хороший результат, т.к. на оставшиеся 14 ошибочных предсказаний(по статистике данной выборки) придётся только 3-4 ушедших, а другие 10 человек получат бонус и повысится уровень лояльности. Следовательно затраты компании на повышение лояльности пользователей возможно сократить на 86%, предлагая мотивацию не всем, а только клиентам, чья вероятность уйти к конкурентам очень высока
