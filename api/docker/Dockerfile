FROM ruby:alpine3.16

RUN apk update \
    && apk upgrade --no-cache \
    && apk add libc6-compat \
    && apk add nodejs npm\
    && npm install -g widdershins \
    && apk add git \
    && apk add --no-cache build-base \
    && gem install bundler \
    && gem update --system
    #&& bundle update --bundler
# Install node packages and gems
#RUN npm install -g widdershins


# working directory
WORKDIR /openapi

RUN git clone https://github.com/slatedocs/slate
RUN cd slate \
    && bundle install