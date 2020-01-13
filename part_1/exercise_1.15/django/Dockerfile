FROM python:3.8

RUN mkdir /project
WORKDIR /project
COPY ./requirements.txt .
RUN pip install -r requirements.txt
RUN django-admin startproject mysite
WORKDIR /project/mysite
EXPOSE 8888
CMD python manage.py runserver 0.0.0.0:8888
