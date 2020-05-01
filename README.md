# Лабораторные работы по курсу "Введение в машинное обучение"
## Лабораторная 1
На основании транзакционных данных клиентов, а также их социально-демографических характеристик обучить логистическую линейную модель вероятности визита клиента в следущие полгода. Данные: https://yadi.sk/d/O2jjJGkrDFDyMA. Задачи:

    Считать файлы из формата CSV. Необходимо правильно настроить разделитель между ячейками и десятичный разделитель.

    Для каждого клиента по транзакционным данным необходимо:

        Зафикисировать дату 2017-07-01 как дату, на которую считаются характеристики клиентов.

        Для каждого клиента определить, совершал ли он визит в период между 2017-07-01 и 2017-12-31 включительно. Полученный флаг является зависимой переменной Y, которую требуется предсказывать

        Для каждого клиента расчитать Recency (количество дней до последнего визита клиента перед зафиксированной датой 2017-07-01), Frequency (средняя частота походов клиентов на дату 2017-07-01, измеряется как среднее количество визитов в месяц [месяц полагать равным 30 дням] за время между 2017-07-01 и первым визитом клиента) и Monetary Value (средний чек клиента по всем покупкам до 2017-07-01). Необходимо помнить, что данные являются реальными данными по москвоским ресторанам. Необходимо проверить на адекватность получаемые значения. Например, не может быть средний чек большого количества клиентов быть меньше 200 рублей, либо частота визитов типичного клиента равно 20 посещениям в месяц.

        Для каждого клиента студенту необходимо самостоятельно придумать и расчитать характеристику клиента по транзакционным данным, которая могла бы помочь предсказывать зависимую переменную Y. Необходимо пояснить, почему выбрана именно эта характеристика.

        Все задания этого пункта выполняются через «pandas.DataFrame.groupby», т.е. циклы, лямбды и прочие цикло-образные конструкции не должны быть основным способом получения результата по каждому из пунктов (или подпунктов).

    Для каждого клиента к уже рассчитанным характеристикам необходимо из второй таблицы притянуть данные по полу и возрасту клиента.

    Разбить клиентов случайно на две группы в соотношении 80:20. Большая группа — это обучающая выборка, а маленькая группа это тестовая выборка.

    Обучить модель логистической регрессии на обучающей выборке.

    Предсказать вероятность прихода на тестовой выборке.

    Посчитать метрики Precision и Recall на основании предсказаний на тестовой выборке и истинных значений зависимой переменной Y.
