FROM ubuntu:22.04

ARG HOSTIP
ENV http_proxy=${HOSTIP}:7890
ENV https_proxy=${HOSTIP}:7890
ENV all_proxy=${HOSTIP}:7890
ENV HTTP_PROXY=
ENV HTTPS_PROXY=
ENV ALL_PROXY=
RUN echo Acquire::http::Proxy \"http://${HOSTIP}:7890\"\; \
    >> /etc/apt/apt.conf && \
    echo Acquire::https::Proxy \"http://${HOSTIP}:7890\"\; \
    >> /etc/apt/apt.conf && \
    apt update && \
    apt install -y \
    curl \
    git \
    build-essential
RUN apt update && \
    apt install -y \
    python3 \
    python3-pip