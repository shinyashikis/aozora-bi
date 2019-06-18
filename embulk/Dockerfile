FROM openjdk:8-jre-alpine

RUN apk add --update curl

RUN mkdir /embulk \
  && curl --create-dirs -o /embulk/embulk -L "https://dl.embulk.org/embulk-latest.jar" \
  && chmod +x /embulk/embulk 

RUN apk add libc6-compat \
  && /embulk/embulk gem install embulk-output-elasticsearch
