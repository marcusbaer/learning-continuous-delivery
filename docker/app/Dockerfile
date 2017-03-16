FROM node:alpine

MAINTAINER Marcus Baer

ENV PATH /root/.yarn/bin:$PATH

# Install Yarn and AWS CLI
RUN apk add --no-cache curl bash binutils tar \
    && curl -o- -L https://yarnpkg.com/install.sh | bash \
    && apk del curl tar binutils \
    && apk add --no-cache make gcc g++ \
    && mkdir -p /aws \
    && apk -Uuv add groff less python py-pip \
    && pip install awscli \
    && apk --purge -v del py-pip \
    && rm /var/cache/apk/*

# Create app directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# Install dependencies
COPY package.json /usr/src/app/
RUN npm install

# Bundle source
COPY . /usr/src/app
RUN npm run build

EXPOSE 3000
EXPOSE 8080
CMD [ "npm", "start" ]
