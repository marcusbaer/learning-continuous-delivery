FROM node:alpine

MAINTAINER Marcus Baer

ENV PATH /root/.yarn/bin:$PATH

# Install Yarn
RUN apk add --no-cache curl bash binutils tar \
    && curl -o- -L https://yarnpkg.com/install.sh | bash \
    && apk del curl tar binutils \
    && apk add --no-cache make gcc g++

EXPOSE 3000
