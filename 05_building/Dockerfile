# syntax=docker/dockerfile:1

FROM ubuntu:24.04 AS fse4ai_05

LABEL maintainer "Aleksandr Mikhalev <al.mikhalev@skoltech.ru>"

ENV TZ=Europe/Moscow

RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && \
    echo $TZ > /etc/timezone

WORKDIR /workspace

ADD practical_5_building_software.zip .

RUN apt update && \
    apt install -y --no-install-recommends \
    man-db \
    unminimize \
    vim \
    unzip \
    build-essential \
    wget \
    cmake \
    libgmp-dev \
    libmpfr-dev \
    libboost-thread-dev

RUN yes | unminimize

RUN unzip practical_5_building_software.zip

WORKDIR /workspace/practical_5_building_software
