FROM python:3.7

ENV DJANGODIR="/opt/services/django/src"
ENV PYTHONUNBUFFERED 1

RUN mkdir -p $DJANGODIR
WORKDIR $DJANGODIR

RUN python -m pip install --upgrade pip
COPY requirements.txt requirements.txt
RUN python -m pip install -r requirements.txt

RUN useradd -m django
USER django
