FROM node:alpine

MAINTAINER Marcus Baer

ENV PATH /root/.yarn/bin:$PATH

# Install Yarn
RUN apk add --no-cache curl bash binutils tar \
    && /bin/bash \
    && touch ~/.bashrc \
    && curl -o- -L https://yarnpkg.com/install.sh | bash

EXPOSE 3000
