# yamdb_final
![example workflow](https://github.com/blkvk/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

# YaMBd

## Описание  

YaMDb — база отзывов о фильмах, книгах и музыке.

## Технологии 
 
- [Python 3.9](https://docs.python.org/3/index.html)
- [Django 3.0.5](https://docs.djangoproject.com/en/3.2/)
- [DRF 3.11](https://www.django-rest-framework.org/)
- [Postgres](https://www.postgresql.org/docs/)
- [PyJWT 1.7.10](https://pyjwt.readthedocs.io/en/stable/)
- [Docker 20.10.7](https://docs.docker.com/)
- [gunicorn 20.0.4](https://gunicorn.org/#docs)


## Перед работой с проектом

Для работы с проектом нужно установить Docker (https://www.docker.com/), с помощью которого в последствии Вы сможете запустить проект.

## Работа с проектом 

Необходимо создать файл *.env* по примеру *env.example*.

Для запуска проекта необходимо собрать и запустить образ ``` $ docker-compose up ```.   

Чтобы запустить контейнер ``` $ docker-compose run -it -p 8000:8000 yamdb ```.  

Для запуска миграций ``` $ docker-compose exec web python manage.py migrate --noinput ```.  

Для создания суперпользователя ``` $ docker-compose exec web python manage.py createsuperuser ```.  

Собрать статику ``` docker-compose exec web python manage.py collectstatic --no-input ```. 

Для того, чтобы загрузить фикстуры ``` $ manage.py loaddata fixtures.json ```.  

Для того, чтобы заполнить базу данными Вы можете воспользоваться админ-панелью в Django.  

Чтобы убедиться, что проект запущен локально и все работает откройте в браузере http://localhost:8000/.

При коммите в master ветку, проект автоматически будет задеплоен. Его можно проверить по адресу: http://62.84.112.161/
http://62.84.112.161/admin/ - админка
http://62.84.112.161/redoc/ - документация API 

## Автор  

Беляков Кирилл - tg @blkvk
