FROM node:11.6

MAINTAINER Hamilton 

ENV PURESCRIPT_DOWNLOAD_SHA1 8b93532f0668a58c1c42b816c5fff11962fd8197   


RUN npm install -g bower pulp psc-package

RUN cd /opt \
    && wget https://github.com/purescript/purescript/releases/download/v0.12.1/linux64.tar.gz \
    && echo "$PURESCRIPT_DOWNLOAD_SHA1 linux64.tar.gz" | sha1sum -c - \
    && tar -xvf linux64.tar.gz \
    && rm /opt/linux64.tar.gz

ENV PATH /opt/purescript:$PATH 

RUN userdel node

RUN useradd -m -s /bin/bash pureuser 

WORKDIR /home/pureuser

USER pureuser

RUN mkdir tmp && cd tmp && pulp init

CMD cd tmp && pulp psci

