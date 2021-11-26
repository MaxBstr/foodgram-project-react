# Выпускной проект Яндекс.Практикума
# Продуктовый помощник Foodgram

Проект развернут по адресу:  http://maxbstr.ydns.eu/

## Описание сервиса

Проект Продуктовый помощник - это сайт, который позволяет пользователям публиковать и делиться рецептами, добавлять чужие рецепты в избранное и подписываться на публикации других авторов, а также автоматически создавать список продуктов, , которые нужно купить для приготовления выбранных блюд, и скачивать его.

## Установка сервиса

* backend - образ бэкенда
* frontend - образ фронтенда
* postgres - образ базы данных PostgreSQL v 12.04
* nginx

## Команда клонирования репозитория:

```
git clone https://github.com/MaxBstr/foodgram-project-react.git
```

## Заполнение .env:

Переименуйте .env.dist в .env и заполните своими данными

## Запуск проекта:
 * Установите Докер
 * Перейдите в папку в проекте infra/
 * Выполните команду:

```
docker-compose up -d --build
```

## Первоначальная настройка Django:

```bash
- sudo docker-compose exec backend python manage.py migrate --noinput
- sudo docker-compose exec backend python manage.py collectstatic --no-input
```

## Создание суперпользователя:
```bash
- sudo docker-compose exec backend python manage.py createsuperuser
```
## Загружаем фикстуры ингредиентов:
```bash
- sudo docker-compose exec backend python manage.py loaddata ingredients.json
```

## Тестовые пользователи:
### Админ: admin@admin.com admin123
