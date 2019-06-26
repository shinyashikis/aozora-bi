FROM openjdk:8-jre-alpine

RUN apk add --update curl

RUN curl --create-dirs -o /bin/embulk -L "https://dl.embulk.org/embulk-latest.jar" \
  && chmod +x /bin/embulk 

RUN apk add libc6-compat \
  && /bin/embulk gem install embulk-output-elasticsearch

ENTRYPOINT ["java", "-jar", "/bin/embulk"]
