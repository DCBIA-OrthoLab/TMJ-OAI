FROM python:3.7

RUN apt-get update && \
	apt-get install -y git

RUN mkdir /app
WORKDIR /app

RUN wget https://github.com/DCBIA-OrthoLab/OAI/archive/refs/tags/3.23.zip
RUN unzip 3.23.zip
RUN mv OAI-3.23 OAI
RUN rm -rf 3.23.zip \
	rm -rf 3.23

WORKDIR /app/OAI/python
RUN pip3 install -r ./requirements.txt
RUN wget https://github.com/DCBIA-OrthoLab/OAI/releases/download/3.23/Models.zip
RUN unzip Models.zip

RUN chmod +x /app/OAI/python/src/main_training.sh
