# MY-PROJECT
          
          karpov_courses
          
          
# final_project (анализ A/B-теста, SQL, автообновление данных A/B-теста)

# Задача 1. A/B–тестирование

# Цель проекта:
* проанализировать результаты A/B-теста новой механики оплаты;
* выбрать метрики;
* объяснить имеющиеся различия в значениях метрик разных групп;
* для групп разного размера определить являются ли различия статистически значимыми;
* сделать выводы о целесообразности запуска новой механики на всех пользователей.

# В мои задачи входило:
* объединение 4-х файлов csv;
* выбор "рабочей" аудитории в группах из общей массы пользователей;
* выбор метрик;
* реализация функции проверки гипотез методом bootstrap.

# Результат:
* в период проведения экспериментов были выявлены оплаты от неактивных пльзователей, их было решено не брать их в расчёт;
* для оценки метрик в группах размер которых отличался в 4 раза принято решение использовать метод bootstrap;
* расчитаны CR в покупку (эффект отрицательный), ARPU и ARPPU (эффект положительный);
* различия в ARPU и ARPPU приняты статистически значимыми, различия в CR - статистически не значимыми;

# сделан вывод:
* новая механика оплаты даёт статистически значимый прирост в метриках ARPU и ARPPU, отрицательное изменение метрики CR не подтвердилось.

# В работе использовались:
* библиотеки requests и urllib.parse для получения прямой ссылки и загрузки файлов с Яндекс.Диска;
* библиотеки tqdm.auto для визуализации индикатора програсса;
* библиотеки pandas, seaborn, scipy.stats, matplotlib.pyplot для обработки и визуализации данных.

# Задача 2. SQL

# Цель проекта:
* написать оптимальный запрос, который даст информацию о количестве очень усердных студентов за март 2020 года;
* в одном запросе выгрузить: ARPU, ARPAU, CR в покупку, СR активного пользователя в покупку, CR пользователя из активности по математике в  покупку курса по математике;

# В мои задачи входило:
* объединение таблиц различными видами джойнов;
* расчёт метрик.

# Результат:
* запросы написаны и проверены в СУБД Postgresql;
# В работе использовались:
* подзапросы;
* оконные функции.

# Задача 3. Python

# Цель проекта:
* написать функцию для обновления данных и пересчёта метрик;
* написать функцию для визуализации пересчитываемых метрик.
# В мои задачи входило:
* разработка логики работы функций;
* написание целевых и вспомогательных функций на Python.
# Результат:
* функция обновления данных скачивает дополнительный файл по веб-ссылке, или использует файл, расположенный локально, дополняет данные, выдаёт датафрэйм с метриками, рассчитанными на каждом этапе обновления;
* функция визуализации метрик берёт на вход датафрэйм, полученный функцией обновления и строит 6 графиков: 3 метрики и 3 p-value этих метрик для каждого шага обновления, показывая динамику.

# В работе использовались:
* библиотека re для автоматического определения разделителя CSV-файла;
* функция bootstrap с первого задания;
* библиотеки pandas, seaborn, matplotlib.pyplot для обработки и визуализации данных.











