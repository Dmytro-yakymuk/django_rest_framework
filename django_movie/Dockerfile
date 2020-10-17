#FROM python:3.8
#
#ENV PYTHONDONTWRITEBYTECODE 1
#
#WORKDIR /app
#
#RUN apt update && apt install postgresql-dev gcc python3-dev musl-dev
#
#RUN pip install --upgrade pip
#COPY ./req.txt .
#RUN pip install -r req.txt
#
#COPY . .
#
#EXPOSE 8000

FROM python:3.8

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

WORKDIR /usr/src/dm_rest

COPY ./req.txt /usr/src/req.txt
RUN pip install -r /usr/src/req.txt

COPY . /usr/src/dm_rest

EXPOSE 8000
#CMD ["python", "manage.py", "migrate"]
#CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]