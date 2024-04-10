# biostat.HW5
Домашнее задание 5
Тема: построение регрессионных моделей и анализ выживаемости.

Цель: научиться пользоваться основными методами регрессионного анализа, разобраться с принципами анализа выживаемости.

Описание ДЗ
Для выполнения первых двух заданий загрузите датасет Breast Cancer Wisconsin.

В колонке diagnosis содержится информация об опухоли (M = злокачественная, B = доброкачественная).

Выполните перечисленные задания.

Задание 1 (2 балла)
Создайте регрессионную модель, которая бы описывала связь среднего радиуса опухоли и средней площади (а), среднего периметра (б), средней симметричности (в).

Постройте графики, на которых отразите регрессионную прямую, и прокомментируйте свои находки.

Задание 2 (2 балла)
Пусть колонка с диагнозом принимает следующие значения: злокачественная опухоль — 1, а доброкачественная — 0. Постройте модель, которая бы прогнозировала вероятность возникновения злокачественной опухоли от среднего радиуса (а), средней площади (б), средней текстуры (в).

Постройте графики. Создайте модель, которая бы прогнозировала вероятность возникновения злокачественной опухоли от всех трех перечисленных факторов.

Задание 3 (6 балла)
Для выполнения этого задания вам понадобится датасет lung, который встроен в пакет survival. Установите этот пакет и загрузите датасет.

Датасет содержит следующий набор переменных:

inst: код учреждения;
time: время выживаемости в днях;
status: 1 = цензурирование, 2 = смерть;
age: возраст в годах;
sex: мужской = 1, женский = 2;
ph.ecog: шкала опросника ECOG (оценку проводит врач). 0 = отсутствие симптомов, 1= симптомы есть, но пациент наблюдается амбулаторно, 2 = меньше половины дня пациент вынужден проводить в постели, 3 = больше половины дня нуждается в отдыхе лежа, но не прикован к постели, 4 = прикован к постели;
ph.karno: шкала Карновского (от 0 до 100, от худшего к лучшему) по оценке врача;
pat.karno: шкала Карновского (от 0 до 100, от худшего к лучшему) по оценке пациента;
meal.cal: калории потребляемой пищи;
wt.loss: потеря веса за последние полгода.
Создайте переменную event, в которой отразите наличие или отсутствие (1 или 0) интересующего события — смерти пациента.

Изучите работу функций Surv(), survfit() и ggsurvplot():

Постройте кривые выживаемости в зависимости от пола (на одном графике должны получиться две кривые для каждого пола и таблица числа пациентов, подверженных риску (at risk) под ним). Поясните получившееся значение p-value для лог-рангового теста и опишите наблюдаемые результаты.
Постройте график кумулятивной функции рисков (cumulative hazard function) для пола. Проинтерпретируйте график.
С помощью функции coxph() постройте регрессию Кокса и оцените влияние пола на выживаемость. Что вы можете сказать о полученных результатах?
Как отправить задание на проверку
Загрузите файлы на GitHub, в форму приложите ссылку на него. Назовите rmd-файл своими ФИО.

Что нужно отправить: ссылку на репозиторий, который будет содержать rmd-файл с вашим решением.
