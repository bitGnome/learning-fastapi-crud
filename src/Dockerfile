FROM mcr.microsoft.com/vscode/devcontainers/python:3

WORKDIR /usr/src/app

ENV PYTHONDONTWRITEBYTECODE 1
ENV PTYHONBUFFERED 1

COPY ./requirements.txt /usr/src/app/requirements.txt

RUN apt-get update \
    && pip install --upgrade pip setuptools wheel \
    && pip install -r /usr/src/app/requirements.txt \
    && rm -rf /root/.cache/pip \

COPY ./src /usr/src/app

