FROM python:3.9-alpine

ENV LC_ALL=C.UTF-8 LANG=C.UTF-8

RUN apk update
RUN apk add gcc build-base linux-headers bash

WORKDIR /app

# Python Setup
COPY ./requirements.txt ./requirements.txt
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

COPY . .

CMD [ "/bin/bash", "-c", "python manage.py runserver 0:8000" ]