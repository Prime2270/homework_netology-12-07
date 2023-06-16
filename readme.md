# Домашнее задание к занятию "`Репликация и масштабирование. Часть 2`" - `Яковлев Константин`

### Задание 1 Опишите основные преимущества использования масштабирования методами:

```
1) активный master-сервер и пассивный репликационный slave-сервер;
2) master-сервер и несколько slave-серверов;
3) активный сервер со специальным механизмом репликации — distributed replicated block device (DRBD);
4) SAN-кластер.

Дайте ответ в свободной форме.

```
```
1) В этом случае преимущество будет в относительно равномерной нагрузке на БД. 
2) В этом случае нагрузка на единицу кластера будет снижена за счет большего кол-ва slave-ов.
3) У данного метода очень мало преимуществ, и они скорее “под конкретный случай”. Репликация блочных устройств. При проблемах с drbd можно подключится сразу к устройству. 
4) Такой вид позволяет сравнительно безопасно в рамках полноценного кластера не терять данные. На вебинаре были приведены примеры с VMware, ProxMox.

```
### Задание 2 Разработайте план для выполнения горизонтального и вертикального шаринга базы данных. База данных состоит из трёх таблиц:

```
- пользователи,
- книги,
- магазины 
(столбцы произвольно)
```

![Вертикальный шардинг](https://github.com/Prime2270/homework_netology-12-07/blob/main/screenshots/%D0%92%D0%B5%D1%80%D1%82%D0%B8%D0%BA%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D0%B9%20%D1%88%D0%B0%D1%80%D0%B4%D0%B8%D0%BD%D0%B3.png)

```
Вертикальный шардинг — это выделение таблицы или группы таблиц на отдельный сервер
```

![Горизонтальный шардинг](https://github.com/Prime2270/homework_netology-12-07/blob/main/screenshots/%D0%93%D0%BE%D1%80%D0%B8%D0%B7%D0%BE%D0%BD%D1%82%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D0%B9%20%D1%88%D0%B0%D1%80%D0%B4%D0%B8%D0%BD%D0%B3.png)

```
Горизонтальный шардинг — это разделение одной таблицы на разные сервера
```
