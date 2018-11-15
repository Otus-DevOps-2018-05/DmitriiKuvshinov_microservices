FROM python:3.6.0-alpine
FROM ubuntu
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update -qq && apt-get install -y gcc && apt-get install -y musl-dev
RUN apt-get install -y python
RUN apt-get install -y python-pip
RUN pip install --upgrade pip

WORKDIR /app
ADD . /app
RUN pip install -r /app/requirements.txt

ENV POST_DATABASE_HOST post_db
ENV POST_DATABASE posts

ENTRYPOINT ["python3", "post_app.py"]
