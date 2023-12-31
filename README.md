# Module21_AB_Test
ДР по модулю 21 А/В Тест

Цель практической работы
Вы провели А/В-тестирование старого и нового подходов к формированию стоимости полиса ВЗР. Первый подход включает в себя традиционную оценку рисков, а второй — использование результатов кластеризации.  Основные влияющие факторы: цена полиса, конверсия в оформления и убыточность. В этой практической работе вам предстоит провести статистический анализ результатов теста и, основываясь на полученных данных, порекомендовать бизнесу новый или старый вариант ценообразования.

Что нужно сделать
Проведите расчёт A/B-теста в Jupyter Notebook и посчитайте значения основных метрик. Рекомендуем выбрать метрики на основе влияющих факторов, но финальное определение метрики за вами. Статистический тест можно использовать любой, но в этой задаче будет достаточно стандартного t-test.
После расчёта значений метрик сделайте бизнес-рекомендацию и обоснуйте, почему предлагаете такое решение (рассмотрите позитивное и негативное влияние на бизнес).

РЕШЕНИЕ:
Выбрано 2 метрики: 1. "Кол-во потерь" и 2. "среднее число потерь". 

Контрольная группа и тестовая группа проверена на кол-во ожидаемых элементов (50/50) Power_divergenceResult(statistic=5.601182281966151, pvalue=0.017948361469529415) SRM is not present НЕТ НЕСООТВЕТСВИЯ ПОЛЬЗОВАТЕЛЕЙ ГРУПП ОЖИДАЕМЫМ

По метрике "кол-во потерь"  Stats loss    2.558502 dtype: float64, p-value [0.00525621] На уровне значимости 0.05 нулевая гипотеза отвергается в пользу альтернативной: Вариаент А более значим (значимая разница Варианта А перед вариантом Б есть)  30 потерь в контрольной группе это значимо больше, чем 14 в тестовой.

По метрике  "средний объем потерь" TtestResult(statistic=array([-0.34528481]), pvalue=array([0.72988769]), df=array([9771.57595476])) Средняя потеря по пользователю контрольная группа loss    876.690844 dtype: float64 Средняя потеря по пользователю тестовая группа loss    1080.716454 dtype: float64  Уровень p-value 72%>5% следовательно на уровне значимости 0.05 не можем отвергнуть нулевую гипотезу, Следовательно средний объем потерь по полисам не изменился после внедрения нового подхода к ценообразованию.

ВЫВОД:

Предлагается не менять подход к ценообразованию, т.к. не смотря на то, что кол-во потерь значимо уменьшилось, среднее число потерь осталось значимо неизменным. 
