FROM python:3.12
ENV PYTHONUNBUFFERED=1
# Устанавливаем рабочую директорию
WORKDIR /app

# Копируем зависимости и устанавливаем их
COPY requirements.txt .
RUN pip install -r requirements.txt

# Копируем весь проект в контейнер
COPY . .

# Команда для запуска приложения
CMD ["gunicorn", "mysite.wsgi:application", "--bind", "0.0.0.0:8000"]
