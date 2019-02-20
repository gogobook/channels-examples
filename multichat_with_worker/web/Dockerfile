FROM python:3.7.2-alpine3.8

ENV PYTHONUNBUFFERED 1
ENV REDIS_HOST "redis"
RUN apk update && apk add gcc musl-dev
RUN mkdir /code
WORKDIR /code
ADD . /code/
RUN pip install -r requirements.txt
RUN python manage.py migrate

