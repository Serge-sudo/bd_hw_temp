# bd_hw_temp

hw1 - Уровни изоляции:
Почитать про уровни изоляции и повторить(мне понравилась эта статья, но можно и по офф
доке) https://habr.com/ru/articles/469415/

hw2 - - Создать таблицу, проиндексировать её различными индексами и сравнить хранимый объём (только индекс). Рассмотреть индекс по одной колонке, по двум и по выражению. Среди индексов использовать как минимум 4: хэш-индекс, B-дерево, Bloom filter и еще один по вашему выбору из доступных в PostgreSQL (включая расширения).
- Пусть для Bloom-фильтра используется хэш шириной 32 бита (т.е. для хранения требуется 2^30 / 8 / 1024^2 = 512 Мбайт). Посчитать вероятность, что при вставке 2 млн записей с различными (уникальными) ключами возникнет хотя бы одна коллизия. Множество ключей конечно. Набор записываемых ключей (2 млн записей) выбирается равномерно из всех подмножеств (соответствующего размера) множества ключей. Возвращаемые значения хэш-функции распределены равномерно, если ключи из множества ключей выбираются равномерно. Вывести формулу, где число записываемых ключей считать переменной, а затем подставить в неё 2 млн. Если затрудняетесь посчитать точно, то хотя бы приблизительно оцените формулой/методом на ваш выбор.

hw3- - Создать базу
- Заполнить её данными: одна или несколько таблиц
- Выполнить ANALYZE
- Придумать SQL запрос(ы) к базе
- Замерить их производительность
- Отключить автоматическое переанализироание
- Поменять содержимое базы, желательно не меняя её объем, но меняя распределение
- Повторно произвести замеры: должно стать медленнее

При этом подобрать запросы и данные так, что бы разница по скорости была ощутима. Желательно в десятки процентов или даже в 2 раза

hw4- Протестировать производительность (pgbench) базы данных с различными значениями двух параметров: размер страницы и размер кэша (shared_buffers). В качестве нагрузки использовать вставку 2 млн записей с уникальными (неповторяющимися) ключами. Если у вас мощное оборудование, и вставка происходит слишком быстро можно повысить объем до 16 млн ключей.

Кроме производительности проанализировать cache hit ratio.
