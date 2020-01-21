# Basic docker based environment
# Necessary to trick dokku into building the documentation
# using dockerfile instead of herokuish
FROM ubuntu:17.04

# Add basic tools
RUN apt-get update && \
  apt-get install -y build-essential \
    software-properties-common \
    curl \
    git \
    libxml2 \
    libffi-dev \
    libssl-dev && \
  LC_ALL=C.UTF-8 add-apt-repository ppa:ondrej/php && \
  apt-get update && \
  apt-get install -y php7.4-cli php7.4-mbstring php7.4-xml php7.4-zip php7.4-intl php7.4-opcache php7.4-sqlite &&\
  apt-get clean &&\
  rm -rf /var/lib/apt/lists/*

WORKDIR /code

VOLUME ["/code"]

CMD [ '/bin/bash' ]
