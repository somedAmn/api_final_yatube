# Описание
Проект для реализации API в сервисе Yatube

# Установка
Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/somedAmn/api_final_yatube/
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
```

Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```

# Примеры запросов
- Получение публикации --> http://example.com/api/v1/posts/0/
> response example
```
{
    "id": 0,
    "author": "string",
    "text": "string",
    "pub_date": "2019-08-24T14:15:22Z",
    "image": "string",
    "group": 0
}
```
- Удаление комментария --> http://example.com/api/v1/posts/0/comments/0/
- Обновление публикации --> http://example.com/api/v1/posts/0/
> request example
```
{
    "text": "string",
    "image": "string",
    "group": 0
}
```
- Получение JWT-токена --> http://example.com/api/v1/jwt/create/
> request example
```
{
    "username": "string",
    "password": "string"
}
```
> response example
```
{
    "refresh": "string",
    "access": "string"
}
```
