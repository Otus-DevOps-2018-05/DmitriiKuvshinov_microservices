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

##ДЗ14
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
