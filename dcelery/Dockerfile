FROM  python:3.11.4-alpine

WORKDIR /usr/src/app

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1
ENV DEBUG 1
ENV SECRET_KEY adjasdhkjdhsadhaeqe34fabcbeufdbffbdfdff
ENV ALLOWED_HOSTS localhost,127.0.0.1


RUN pip install --upgrade pip
COPY ./requirements.txt /usr/src/app/requirements.txt
RUN pip install -r requirements.txt

COPY . /usr/src/app/
RUN echo "Apply database migrations"
RUN python manage.py migrate

