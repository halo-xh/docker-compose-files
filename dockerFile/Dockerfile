FROM openjdk:17.0.2-oracle

ARG BUILD_FROM=arm64v8

MAINTAINER xiaohong

ENV SPRING_OUTPUT_ANSI_ENABLED=ALWAYS \
    JAVA_OPTS="" \
    PORT=8081 \
    PROFILES="dev"

ADD ./shop-service-1.2-SNAPSHOT.jar /shop-service-1.2-SNAPSHOT.jar

ENTRYPOINT ["sh", "-c", "java $JAVA_OPTS -jar /shop-service-1.2-SNAPSHOT.jar --spring.profiles.active=$PROFILES"]

EXPOSE $PORT
