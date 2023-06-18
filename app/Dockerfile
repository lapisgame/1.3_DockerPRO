FROM python:latest

RUN apt-get update && apt-get install

RUN apt-get install -y \
  dos2unix \
  libpq-dev \
  libmariadb-dev-compat \
  libmariadb-dev \
  gcc \
  && apt-get clean

RUN python -m pip install --upgrade pip

WORKDIR /app/

COPY requirements.txt requirements.txt
RUN python -m pip install -r requirements.txt

COPY app.py app.py

CMD ["python","app.py"]
