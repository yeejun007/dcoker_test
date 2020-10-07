FROM ubuntu:latest

# RUN apt-get update
# RUN apt-get upgrade -y
# RUN apt-get install -y python3-pip

RUN apt-get update
RUN apt-get install -y libzmq3-dev python3-pip
# RUN apt-get clean && rm -rf /var/lib/apt/lists/*
RUN pip3 install --upgrade pip

COPY . /app
WORKDIR /app

RUN pip install -r requirements.txt

ENTRYPOINT ["python3"]
CMD ["app.py", "KNN_FXCM_ALGO.py"]