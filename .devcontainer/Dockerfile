FROM mcr.microsoft.com/devcontainers/python:3.9

WORKDIR /development

RUN apt-get update && \
    apt-get install -y git

COPY requirements.txt requirements.txt
COPY requirements.yml requirements.yml

RUN python3 -m pip install --upgrade pip && \
    python3 -m pip install -r requirements.txt
    
RUN ansible-galaxy install -r requirements.yml
