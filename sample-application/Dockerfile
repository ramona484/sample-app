FROM python:latest


LABEL maintainer="ramona"

RUN adduser sasquatch -D

ADD . /app

WORKDIR app
RUN pip install -r requirements.txt

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2

EXPOSE 5000

USER sasquatch

CMD python ./index.py
