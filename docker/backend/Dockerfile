FROM ubuntu:18.04

LABEL maintainer="Artem Galitskiy"

USER root
ENV HOME /root
ENV DEBIAN_FRONTEND noninteractive
ENV PYTHONPATH /backend
WORKDIR /backend

RUN echo 'debconf debconf/frontend select Noninteractive' | debconf-set-selections \
    && apt-get update -qq \
    && apt-get install -y -qq --no-install-recommends \
        python3 python3-pip locales python3-setuptools python3-dev sqlite3 \
    && pip3 install wheel \
    && apt-get -qq clean \
    && dpkg-reconfigure locales && locale-gen en_US.UTF-8 && locale-gen ru_RU.UTF-8 \
    && apt-get -qq autoremove \
    && rm -rf /var/lib/apt/lists/* /var/tmp/*

COPY docker/backend/requirements.txt /
RUN pip3 install -r /requirements.txt \
    && rm -rf /root/.cache/pip/*

COPY backend /backend
