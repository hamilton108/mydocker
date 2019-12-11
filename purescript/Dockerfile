FROM node:12.4

MAINTAINER Hamilton 

# ENV PURESCRIPT_DOWNLOAD_SHA1 249be2fa812c544d69dadaff45af53943d428215

# ENV PURESCRIPT_DOWNLOAD_SHA1 3d0259a82a48a776e31116bd7a5f607a2f035c49  

# ENV PURESCRIPT_DOWNLOAD_SHA1 8a28fb73445bbee411dd5d7f5997ec917bc071c8 

ENV PURESCRIPT_DOWNLOAD_SHA1 58b14014ba08ef6550fa61700797688d27a9a2f3


RUN npm install -g pulp psc-package

RUN cd /opt \
    && wget https://github.com/purescript/purescript/releases/download/v0.13.5/linux64.tar.gz \
    && echo "$PURESCRIPT_DOWNLOAD_SHA1 linux64.tar.gz" | sha1sum -c - \
    && tar -xvf linux64.tar.gz \
    && rm /opt/linux64.tar.gz

ENV PATH /opt/purescript:$PATH 

RUN userdel node

RUN useradd -m -s /bin/bash pureuser 

WORKDIR /home/pureuser

USER pureuser

# RUN mkdir tmp && cd tmp && pulp init

RUN mkdir tmp 

# RUN mkdir tmp && cd tmp && pulp init

CMD cd tmp && pulp psci

