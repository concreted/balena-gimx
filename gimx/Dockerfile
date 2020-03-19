FROM balenalib/raspberrypi3-ubuntu:16.04

RUN apt-get update

RUN apt-get install -y wget

RUN wget https://github.com/matlo/GIMX/releases/download/v7.15/gimx_7.15-1_armhf.deb

RUN apt-get install ./gimx_7.15-1_armhf.deb
