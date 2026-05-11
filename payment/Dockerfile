FROM python:3.9

WORKDIR /app

EXPOSE 8080

COPY requirements.txt .

RUN apt-get update && \
    apt-get install -y gcc build-essential && \
    pip3 install -r requirements.txt

COPY *.py .
COPY payment.ini .

CMD ["uwsgi", "--ini", "payment.ini"]