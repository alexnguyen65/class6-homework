FROM ubuntu:latest

RUN apt-get update \
    && apt-get install -y python3-pip \
    && pip3 install --upgrade pip

RUN pip3 install pandas matplotlib opencv-python

WORKDIR /app

COPY "dataset-processor.py" /app
COPY "housing.data" /app

CMD ["python3", "-u", "./dataset-processor.py"]
