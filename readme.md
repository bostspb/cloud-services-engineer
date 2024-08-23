# Yandex Cloud: Инженер облачных сервисов
> https://practicum.yandex.ru/ycloud/

`Yandex Cloud` `Управление облачной инфраструктурой` `Хранение и анализ данных` `Работа с контейнерами` 
`Разработка приложений в облаке` `Защита облачных ресурсов`

## 1. Начало работы в облаке
### 1.1 Введение
1. Начнём с теста
2. О профессии «Инженер облачных сервисов»
3. Давайте познакомимся
4. Что такое облачные технологии
5. Облачные сервисы
6. Внутри облака
7. Доступ к ресурсам, платежный аккаунт, пробный период

### 1.2 Виртуальные машины
1. Практическая работа. Создание аккаунта
2. Основная информация о виртуальных машинах
3. Практическая работа. Создание виртуальной машины и подключение к ней
4. Изучаем страницу создания виртуальной машины
5. Последовательный порт и серийная консоль
6. Практическая работа. Получаем доступ к серийной консоли
7. Прерываемые машины и уровни производительности
8. Практическая работа. Создаем ВМ с 5% vCPU и учимся использовать мониторинг
9. Сервис метаданных и cloud-init

### 1.3 Диски, снимки и образы
1. Диски. Зависимость производительности от объёма
2. Что такое снимок и зачем он нужен
3. [Практическая работа. Создаем снимок диска ВМ](1_3_2_create_snapshot.md)
4. Что такое образы и публичные образы

### 1.4 Виртуальная сеть
1. Виртуальные сети, подсети, IP-адресация
2. Практическая работа. Создание новой сети с подсетями и ВМ
3. Публичные IP-адреса
4. Статическая маршрутизация
5. Группы безопасности
6. Практическая работа. Создаем группу безопасности и открываем доступ к серверу

### 1.5 Балансировка нагрузки
1. Балансировка нагрузки
2. Yandex Network Load Balancer
3. Проверка состояния
4. [Практическая работа. Знакомство с Yandex Cloud CLI](1_5_4_yandex_cloud_cli.md)
5. Практическая работа. Создание балансировщика
6. Как правильно использовать балансировщики

### 1.6 Группы виртуальных машин
1. Зачем нужны группы виртуальных машин
2. Практическая работа. Создание группы виртуальных машин
3. Автоматическое восстановление
4. Автоматическое масштабирование
5. Практическая работа. Автоматическое масштабирование под нагрузкой
6. Практическая работа. Воссоздание виртуальных машин в группе

### 1.7 Итоговое тестирование


## 2. Хранение и анализ данных
### 2.1 Об управляемых базах данных
1. Введение
2. Кластеры, масштабируемость, доступность и отказоустойчивость
3. Реляционные базы данных
4. Нереляционные базы данных
5. Выбор базы данных

### 2.2 Object Storage
1. Object Storage и S3-совместимые хранилища
2. Метаданные
3. Управление доступом
4. [Практическая работа. Создание бакетов и загрузка объектов. Работа с утилитой S3cmd](2_2_4_s3_bucket_creating.md)
5. Резервное копирование
   1. [Поддерживаемые инструменты для резервного копирования](https://cloud.yandex.ru/docs/storage/tools/)
6. Версионирование бакетов
7. [Практическая работа. Хранение статических веб-сайтов в Object Storage](2_2_7_s3_website.md)


### 2.3 Реляционные базы данных в облаке — PostgreSQL, MySQL
1. Практическая работа. Создание кластера базы данных MySQL
2. Лимиты, квоты и тарификация
3. Практическая работа. Подключение к базе данных
4. Распределение ответственности между Yandex Cloud и пользователем
5. Логи и мониторинг кластера
6. Резервное копирование и восстановление данных
7. Практическая работа. Создание кластера базы данных PostgreSQL
8. Репликация
9. Миграция данных в облако репликацией
10. Data Transfer. Инструмент для миграции баз данных


### 2.4 MongoDB
1. Введение. Несколько слов о NoSQL
2. Практическая работа. Создание кластера MongoDB
3. Шардирование коллекций
4. Особенности сервиса управляемых баз данных MongoDB


### 2.5 ClickHouse
1. Описание ClickHouse
2. Практическая работа. Создание кластера ClickHouse и подключение к нему
3. Практическая работа. Работа с данными из объектного хранилища
4. Практическая работа. Добавление данных
5. Особенности сервиса управляемых баз данных ClickHouse


### 2.6 YDB
1. Краткий обзор YDB
2. Модель и схема данных в YDB, запросы и транзакции
3. Практическая работа. Создание базы данных
4. Практическая работа. YQL и работа с данными
5. План запроса
6. Диагностика и мониторинг
7. Создание резервных копий


### 2.7 Hadoop
1. Большие данные, Apache Hadoop и Apache Spark
2. Обзор Yandex Data Proc
3. Практическая работа. Создание кластера Hadoop
4. Практическая работа. Подключение к кластеру и работа с Hive


### 2.8 DataLens
1. Описание и особенности DataLens
2. Обзор DataLens, модель данных
3. Практическая работа. Создание датасетов, чартов и дашбордов

### 2.9 Итоговое тестирование


## 3. DevOps и автоматизация
### 3.1 CLI Yandex Cloud
1. Вводный урок
2. Как пользоваться CLI Yandex Cloud
3. Практическая работа. Начало работы в CLI
4. Практическая работа. Создание виртуальных машин с помощью CLI
5. Практическая работа. Использование файлов спецификаций
   1. [Файл спецификации](specification.yaml)


### 3.2 Packer
1. О Packer
2. Практическая работа. Создаём образ виртуальной машины
   1. [Спецификация образа](Packer/my-ubuntu-nginx.pkr.hcl)  
   2. [Документация Packer](https://developer.hashicorp.com/packer/docs/templates/hcl_templates)

### 3.3 Terraform
1. О Terraform
2. Практическая работа. Создаём виртуальную машину из образа и базу данных

### 3.4 Контейнеры и Docker Container Registry
1. Контейнеризация
2. Docker
3. Yandex Container Registry
4. Практическая работа. Создание и загрузка Docker-образа в Container Registry

### 3.5 Managed Kubernetes
1. Оркестрация и Kubernetes
2. Практическая работа. Создание кластера
3. Практическая работа. Первое приложение в кластере
4. Практическая работа. Балансировка нагрузки
5. Автоматическое масштабирование
6. Практическая работа. Автомасштабирование в Yandex Managed Kubernetes
7. Мониторинг Managed Kubernetes
8. Отказоустойчивость Managed Kubernetes
9. Управление доступом

### 3.6 Отказоустойчивость
1. Принципы отказоустойчивости
2. Практическая работа. Сбой виртуальной машины
3. Практическая работа. Сбой зоны доступности
4. Практическая работа. Обновление приложения
5. Практическая работа. Сбой приложения

### 3.7 Мониторинг и алерты
1. Зачем нужен мониторинг. Yandex Monitoring
2. Начало работы с Yandex Monitoring
3. Практическая работа. Отправка собственных метрик
4. Практическая работа. Выгрузка метрик в формате Prometheus
5. Алерты
6. Практическая работа. Создание алерта

### 3.8 Итоговое тестирование