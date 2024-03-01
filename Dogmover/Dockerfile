FROM python:3.13.0a4-slim

WORKDIR /dogmover
COPY requirements.txt requirements.txt

RUN pip install -r requirements.txt --upgrade

ENTRYPOINT ["./dogmover.py"]
