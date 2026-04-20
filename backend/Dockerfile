# Используем официальный образ Python
FROM python:3.9-slim

# Устанавливаем рабочую директорию внутри контейнера
WORKDIR /app

# Копируем файл с зависимостями и устанавливаем их
COPY requirements.txt .
RUN pip install -r requirements.txt --no-cache-dir

# Копируем весь исходный код бэкенда
COPY . .

# Команда, которая запустит gunicorn сервер на порту 9000
CMD ["gunicorn", "--bind", "0.0.0.0:9000", "kittygram_backend.wsgi"]