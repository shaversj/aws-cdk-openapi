FROM ruby:3.1-alpine

RUN apk update \
    && apk upgrade --no-cache \
    && apk add --no-cache --update nodejs npm \
    && apk add git \
    && apk add --no-cache build-base

# Install node packages and gems
RUN npm install -g widdershins \
    && gem install bundler 

# working directory
WORKDIR /openapi

RUN git clone https://github.com/slatedocs/slate
RUN cd slate \
    && bundle install