# DmitriiKuvshinov_microservices
DmitriiKuvshinov microservices repository
## ДЗ 12
<b>Введение в Docker</b>
Знакомство и введение в технологию контейнеризации


## ДЗ 13
<b>Docker-образа. Микросервисы.</b>

```
Обратите внимание! Сборка ui началась не с первого шага. Подумайте - почему?
```

Сборка началась с первого шага

```
docker build -t kuvshinov/ui:1 ./ui/
Sending build context to Docker daemon  26.11kB
Step 1/13 : FROM ruby:2.2
 ---> 6c8e6f9667b2
Step 2/13 : RUN apt-get update -qq && apt-get install -y build-essential
 ---> Using cache
 ---> d648bcc36f5d
Step 3/13 : ENV APP_HOME /app
 ---> Using cache
 ---> 8cfb71471729
Step 4/13 : RUN mkdir $APP_HOME
 ---> Using cache
 ---> ce5b8b4ff64f
Step 5/13 : WORKDIR $APP_HOME
 ---> Using cache
```
Произведена работа с контейнерами и микросервисами. Работа с тэгированной лоакльной сетью
Проверить работоспособность сервиса можно по адресу http://127.0.0.1:9292

## ДЗ14
<b>Docker: сети,docker-compose</b>
```
Запустите несколько раз (2-4)
> docker run --network host -d nginx
Каков результат? Что выдал docker ps? Как думаете почему?
```
В списке контейнеров отображается только 1, потому ключ -d подразумевает операцию deattach.

```
Узнайте как образуется базовое имя проекта. Можноли его задать? Если можно то как? 
```
Docker compose будет использовать имя каталога с вашим компоновочным файлом в качестве имени проекта, если вы не установите через - p option или параметром в .env файле 
Применение параметризации:

set -a
source .my-env

## ДЗ15

<b>Устройство Gitlab CI. Построение процесса непрерывной интеграции</b>

Подготовить инсталляцию Gitlab CI
Развернута и подготовлена ВМ в облаке GCP при помощи Ansible

Подготовлен репозиторий с кодом приложения
Запущен раннер для тестирования нового кода

## ДЗ16

<b>Введение в мониторинг.Системы мониторинга.</b>

• Prometheus: запуск, конфигурация, знакомство с
Web UI
• Мониторинг состояния микросервисов
• Сбор метрик хоста с использованием экспортера

## ДЗ17

<b>Мониторинг приложения и инфраструктуры</b>

• Мониторинг Docker контейнеров
• Визуализация метрик
• Сбор метрик работы приложения и бизнес
метрик
• Настройка и проверка алертинга

## ДЗ
Основные модели безопасности и контроллеры в Kubernetes 

<b>В процессе сделано:</b>
Работа с кластером k8s в minikube. перенос на GCP

<b>Как запустить проект:</b>
Запустить pod-ы

<b>Как проверить работоспособность:</b>
Перейти на порт работы приложения, потыкать 

## В процессе изучено:
• Ingress Controller
• Ingress
• Secret
• TLS
• LoadBalancer Service
• Network Policies
• PersistentVolumes
• PersistentVolumeClaims

## Как запустить проект:
Запустить приложение в GCP

## Как проверить работоспособность:
Потыкать веб интерфейс приложения
