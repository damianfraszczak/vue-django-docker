# syntax=docker/dockerfile:1
FROM python:3
ENV PYTHONUNBUFFERED=1
EXPOSE 8000
WORKDIR /app
COPY requirements.txt /app/
RUN pip install -r requirements.txt
COPY . /app/
CMD python3 manage.py migrate && python3 manage.py runserver 0.0.0.0:8000