FROM python:3.8-rc

ENV PYTHONUNBUFFERED 1

COPY ./requirements.txt /requirements.txt
RUN pip install -r /requirements.txt
RUN apt-get update
# RUN apt-get install -y netcat
# RUN apt-get install -y netcat
RUN python --version

RUN mkdir /app
COPY . /app
WORKDIR /app

RUN bash -c "adduser user"
USER user
