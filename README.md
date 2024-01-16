# Этот проект позволит вам выкладывать свои и любоваться чужими фото котов и кошек. В описание добавьте имя, цвет и достижения.
### Описание проекта

### Проект Kittygram находится по адресу: https://kittyghram.ddns.net/
### Стэк технологий

  *  Python 3.9
  *  Django 3.2.3
  *  djangorestframework 3.12.4
  *  djoser 2.1.0
  *  webcolors 1.11.1
  *  gunicorn 20.1.0
  *  psycopg2-binary 2.9.6
  *  pytest-django 4.4.0
  *  pytest-pythonpath 0.7.3
  *  pytest 6.2.4
  *  PyYAML 6.0

### Локальный запуск проекта

### Клонировать репозиторий и перейти в него в командной строке:

git clone git@github.com:misha1113111/kittygram_final.git

* Cоздать и активировать виртуальное окружение, установить зависимости:

  *  python3 -m venv venv  
  *  source venv/scripts/activate 
  *  python -m pip install --upgrade pip 
  *  pip install -r backend/requirements.txt

#### Установите docker compose на свой компьютер.

#### Запустите проект через docker-compose:

 * docker compose -f docker-compose.yml up --build -d

#### Выполнить миграции:

 * docker compose -f docker-compose.yml exec backend python manage.py migrate

#### Соберите статику и скопируйте ее:

 * docker compose -f docker-compose.yml exec backend python manage.py collectstatic  
 * docker compose -f docker-compose.yml exec backend cp -r /app/collectstatic/. /backend_static/static/

#### .env

#### В корне проекта создайте файл .env и пропишите в него свои данные.

  * Пример:

  * POSTGRES_DB=kittygram
  * POSTGRES_USER=kittygram_user
  * POSTGRES_PASSWORD=kittygram_password
  * DB_NAME=kittygram
