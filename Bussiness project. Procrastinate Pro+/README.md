# Анализ бизнес-показателей приложения Procrastinate Pro+

## Описание проекта

Проект направлен на анализ бизнес-показателей приложения **Procrastinate Pro+**, в частности, для выяснения причин убытков несмотря на значительные инвестиции в рекламу. Цель исследования — разобраться в текущей ситуации и помочь компании выйти на прибыль. В процессе анализа изучались динамика рекламных затрат, конверсии пользователей, а также влияние различных источников трафика и устройств на прибыльность.

Проект полезен для маркетологов, специалистов по рекламе и аналитиков, занимающихся оптимизацией рекламных стратегий, улучшением удержания пользователей и повышением общей прибыльности компании.

### Необходимые библиотеки:
- pandas
- numpy
- matplotlib
- seaborn
- scipy

## Данные

Проект основывается на трех датасетах, которые предоставляют информацию о посещениях сайта, заказах пользователей и расходах на рекламу:

### 1. **visits_info_short.csv**
- **User Id** — уникальный идентификатор пользователя.
- **Region** — страна пользователя.
- **Device** — тип устройства пользователя (ПК, Android, iOS).
- **Channel** — идентификатор источника перехода (например, FaceBoom, TipTop).
- **Session Start** — дата и время начала сессии.
- **Session End** — дата и время окончания сессии.

### 2. **orders_info_short.csv**
- **User Id** — уникальный идентификатор пользователя.
- **Event Dt** — дата и время покупки.
- **Revenue** — сумма заказа.

### 3. **costs_info_short.csv**
- **dt** — дата проведения рекламной кампании.
- **Channel** — идентификатор рекламного источника.
- **costs** — расходы на рекламную кампанию.

Эти данные используются для оценки эффективности рекламных кампаний и прогнозирования доходности приложения.

## Выводы

Проект завершен, и результаты анализа позволяют выделить несколько ключевых выводов и проблемных областей.

### 1. **Общая эффективность рекламы**
- Реклама не окупается: ROI на 14-й день составил 80%, и динамика показала, что окупаемость исчезла в июне.
- Стоимость привлечения клиентов (CAC) начала расти с середины мая, что указывает на проблемы с ростом расходов на рекламу.
- Лайфтайм пользователей (LTV) остается стабильным, что подтверждает, что причина проблемы не в качестве пользователей, а в увеличении рекламных затрат.
- Конверсия пользователей стабильна, однако удержание платящих клиентов ниже, чем у неплатящих.

### 2. **Выводы по странам**
- Реклама не окупается в США, несмотря на высокую LTV у пользователей из этой страны.
- Стоимость привлечения для США значительно возросла с середины мая, в то время как для других стран она стабилизировалась.
- В UK наблюдаются всплески ROI в середине периода, что может быть связано с локальными событиями.

### 3. **Выводы по устройствам**
- CAC стабильно растет на всех устройствах, что связано с увеличением расходов на два основных источника рекламы — TipTop и FaceBoom.
- ПК показывают наименьший CAC, а устройства Apple имеют самый высокий CAC, что может быть связано с высокой стоимостью пользователей из США.
- Лайфтайм пользователей стабильный, но пользователи с ПК окупаются быстрее всех.

### 4. **Выводы по источникам рекламы**
- Лучшая динамика LTV наблюдается у пользователей, пришедших через **lambdamediaAds**.
- Наилучшая окупаемость у **YRabbit**, при этом источники **AdNonSense**, **FaceBoom** и **TipTop** показывают низкую окупаемость.
- Конверсия пользователей по источникам рекламы варьируется, с наилучшей конверсией у **FaceBoom**.
- **TipTop** показывает постоянно растущий CAC с середины мая и требует пересмотра условий рекламы.

### 5. **Выводы по источникам рекламы в США**
- Проблемные источники: **FaceBoom** и **TipTop**. Оба не окупаются, и их эффективность значительно снижается в США.
- Перспективные источники: **YRabbit**, **MediaTornado**, **RocketSuperAds**. Эти каналы показывают высокий LTV и хороший ROI, несмотря на слегка более высокий CAC.
- **FaceBoom** имеет низкое удержание пользователей, что может указывать на проблемы с совместимостью рекламы с устройствами Apple или высокой конкуренцией.

## Рекомендации
1. **Выяснить причину низкого удержания пользователей из FaceBoom**, возможно, с помощью опросов или дополнительного анализа данных.
2. **Договориться о скидке на рекламу в TipTop**, в противном случае рассмотреть возможность отказаться от этого источника рекламы.
3. **Перенаправить расходы на рекламу** в более перспективные источники, такие как **RocketSuperAds** (высокий LTV, низкий CAC) и **YRabbit** (высокий ROI).
4. Оценить возможность **оптимизации рекламных расходов в США**, так как текущие затраты на рекламу в этом регионе не приносят ожидаемой прибыли.

### Статус проекта:
Завершён, готов для внедрения рекомендаций в рекламные стратегии и бизнес-процессы компании.
