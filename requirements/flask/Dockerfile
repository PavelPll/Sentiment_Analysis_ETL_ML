FROM python:3.8-slim

WORKDIR /app

COPY ./requirements.txt .

RUN pip3 install -r requirements.txt

CMD [ "python", "main.py" ]
