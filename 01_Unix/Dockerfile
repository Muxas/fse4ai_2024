# syntax=docker/dockerfile:1

FROM ubuntu:24.04 AS fse4ai_01

LABEL maintainer "Aleksandr Mikhalev <al.mikhalev@skoltech.ru>"

ENV TZ=Europe/Moscow

RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && \
    echo $TZ > /etc/timezone

WORKDIR /workspace

ADD practical_1_unix_local_machine_1.zip .

RUN apt update && \
    apt install -y --no-install-recommends \
    man-db \
    unminimize \
    unzip

RUN yes | unminimize

RUN unzip practical_1_unix_local_machine_1.zip

WORKDIR /workspace/practical_1_unix_local_machine_1
