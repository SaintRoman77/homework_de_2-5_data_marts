# DWH.Витрины данных (homework_de_2-5_data_marts)

### Описание:

Docker-контейнер для homework_de_2-5_data_marts. Создает БД библиотеки, наполняет ее данными, выполняет запросы по заданию (описание задач ниже).

### Шаблон наполнения env-файла:

Создайте файл .env с переменными окружения для работы с базой данных:

```
POSTGRES_PASSWORD=postgres # пароль для подключения к БД (установите свой)
POSTGRES_USER=postgres # логин для подключения к базе данных
POSTGRES_DB=testdb # название базы данных
```

### Команды для запуска приложения в контейнерах:

Собрать контейнер (из папки infra):

```
docker-compose up -d --build
```

Остановить контейнер:

```
docker stop ID-контейнера
```

Запустить контейнер:

```
docker run ID-контейнера
```

Подключиться к работающему контейнеру, запускать интерфейс psql и вносить новые данные:

```
docker exec -it infra-db-1 psql -U postgres testdb
```

### Описание задания:

```
1. Доработать структуру БД, добавить недостающую таблицу (shops).
```

```
2. Разработать SQL-скрипт, который формирует таблицу со следующим набором атрибутов(scr_data_mart.sql):
   - shop_name — название магазина,
   - product_name — название товара,
   - sales_fact — количество фактических продаж на конец месяца,
   - sales_plan — количество запланированных продаж на конец месяца,
   - sales_fact/sales_plan — отношение количества фактических продаже к запланированному,
   - income_fact — фактический доход,
   - income_plan — планируемый доход,
   - income_fact/income_plan — отношение фактического дохода к запланированному.
```
