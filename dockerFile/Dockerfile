FROM openjdk:8u342-oracle

ARG BUILD_FROM=arm64v8

MAINTAINER xiaohong

ENV SPRING_OUTPUT_ANSI_ENABLED=ALWAYS \
    JAVA_OPTS="" \
    PORT=8081 \
    PROFILES="dev"

ADD ./app.jar /app.jar

ENTRYPOINT ["sh", "-c", "java $JAVA_OPTS -jar /app.jar -Dspring.profiles.active=$PROFILES"]

EXPOSE $PORT
