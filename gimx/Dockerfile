FROM balenalib/raspberrypi3-ubuntu:xenial

RUN apt-get update

RUN apt-get install -y wget

RUN wget https://github.com/matlo/GIMX/releases/download/v7.15/gimx_7.15-1_armhf.deb

RUN apt-get install -y ./gimx_7.15-1_armhf.deb

COPY ./gimx-ps4-helper.sh .
RUN chmod +x gimx-ps4-helper.sh
