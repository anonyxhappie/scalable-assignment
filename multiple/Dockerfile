FROM python:3.6-slim

ARG REPO_NAME
ARG PORT

RUN echo ${REPO_NAME}

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN pip install --upgrade pip

RUN apt-get update -y
RUN apt-get install -y git

RUN git clone https://github.com/anonyxhappie/${REPO_NAME}
RUN pip install -r /${REPO_NAME}/requirements.txt
COPY .env ${REPO_NAME}/

EXPOSE ${PORT}
