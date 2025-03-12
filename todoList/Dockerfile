FROM python:3.12-slim

WORKDIR /app/backend

COPY requirements.txt .

RUN apt-get update 
RUN apt-get upgrade -y 
RUN apt-get install -y gcc default-libmysqlclient-dev pkg-config
RUN rm -rf /var/lib/apt/lists/*
RUN pip install -r requirements.txt

COPY . .

EXPOSE 8000