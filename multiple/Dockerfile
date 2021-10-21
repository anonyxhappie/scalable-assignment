FROM python:3.6-slim

ARG REPO_NAME
ARG PORT

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN pip install --upgrade pip

RUN apt-get update -y
RUN apt-get install -y tar git curl nano wget dialog net-tools build-essential

RUN git clone https://github.com/anonyxhappie/${REPO_NAME}
RUN pip install -r /${REPO_NAME}/requirements.txt

EXPOSE ${PORT}
