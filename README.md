🚀 Описание проекта
Это простое Flask-приложение для управления списком задач (To-Do List).
Проект использует PostgreSQL в качестве базы данных и запускается в контейнерах с помощью Docker и Docker Compose.

🏗️ Структура проекта

docker_lab/
│
├── migrations/          # Миграции базы данных (Alembic)
├── templates/           # HTML-шаблоны для фронтенда
│   └── index.html
├── static/              # CSS и статика
│   └── style.css
├── Dockerfile           # Сборка образа для Flask
├── docker-compose.yml   # Конфигурация для Docker Compose
├── requirements.txt     # Python-зависимости
├── app.py               # Основной код приложения Flask
└── models.py            # Описание модели БД (SQLAlchemy)


⚙️ Установка и запуск

1. 📦 Установка Docker и Docker Compose

Установите Docker и Docker Compose, если их ещё нет.


3. 🏗️ Сборка и запуск контейнеров

docker-compose build
docker-compose up -d

Контейнеры поднимутся и будут работать в фоновом режиме.
	•	Flask-приложение доступно по адресу: http://localhost:5056
	•	PostgreSQL работает внутри контейнера и не требует ручного запуска.

4. 🔧 Применение миграций 

docker-compose exec web flask db init
docker-compose exec web flask db migrate -m "Initial migration"
docker-compose exec web flask db upgrade


