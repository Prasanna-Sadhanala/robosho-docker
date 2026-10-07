FROM python:3.9.25-alpine3.22 AS builder
WORKDIR /app
COPY requirements.txt .
COPY payment.ini .
COPY *.py .
RUN pip install --no-cache-dir -r requirements.txt
EXPOSE 8080
CMD ["uwsgi", "--ini", "payment.ini"]