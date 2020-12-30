# DjangoDockerTest
Тестовый образ докера для Django

Методы запуска:

- После клонирования гита на сервер, если сервер linux, то проверить привелегии файлов entrypoint.point.sh и entrypoinr.sh. Должно быть chmod +x entry...
- Стартуем dev:

    $ docker-compose down -v
    
    $ docker-compose up -d --build
    
    $ docker-compose exec web python manage.py migrate --noinput
    
    $ docker-compose exec web python manage.py collectstatic --no-input --clear
    
- Стартуем prod:

    $ docker-compose down -v
    
    $ docker-compose -f docker-compose.prod.yml up -d --build
    
    $ docker-compose -f docker-compose.prod.yml exec web python manage.py migrate --noinput
    
    $ docker-compose -f docker-compose.prod.yml exec web python manage.py collectstatic --no-input --clear
    
    
