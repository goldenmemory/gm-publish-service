FROM frolvlad/alpine-oraclejdk8:slim
MAINTAINER Golden Memory Team <team@chatops.in>

WORKDIR /opt/goldenmemory/

ADD gm-publish-service.jar app.jar
ENV JAVA_OPTS="-Xdebug -Xrunjdwp:server=y,transport=dt_socket,suspend=n"
ENTRYPOINT java $JAVA_OPTS -Djava.security.egd=file:/dev/urandom -jar /opt/goldenmemory/app.jar
