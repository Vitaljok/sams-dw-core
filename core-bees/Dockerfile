FROM openjdk:11-jre

ENV TZ=Europe/Riga
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

ARG VER=*
ADD ./build/libs/bees-dwh-core-${VER}.jar /opt/app/bees-dwh-core.jar

WORKDIR /opt/app/

ENTRYPOINT java $JAVA_OPTIONS -Dspring.profiles.active=prod -jar bees-dwh-core.jar

EXPOSE 8080
