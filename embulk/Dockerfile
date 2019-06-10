FROM openjdk:8-jre-alpine

RUN apk add --update curl

RUN curl --create-dirs -o ~/.embulk/bin/embulk -L "https://dl.embulk.org/embulk-latest.jar" \
  && chmod +x ~/.embulk/bin/embulk 

#CMD ["java", "-jar", "/.embulk/bin/embulk"]
