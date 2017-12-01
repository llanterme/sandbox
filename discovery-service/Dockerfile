FROM node:5.11.1

RUN apt-get update && apt-get install -y libelf1

RUN useradd jenkins --shell /bin/bash --create-home
USER jenkins

MAINTAINER Piotr Minkowski <piotr.minkowski@gmail.com>
ADD target/discovery-service.jar discovery-service.jar
ENTRYPOINT ["java", "-jar", "/discovery-service.jar"]
EXPOSE 8761