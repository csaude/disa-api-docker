FROM openjdk:17-jdk-alpine

LABEL maintainer="his@fgh.org.mz" 

VOLUME [ "/opt/disa/data" ]

RUN ln -s /usr/share/zoneinfo/Africa/Maputo /etc/localtime

EXPOSE 8080

# Prod
# ENTRYPOINT [ "java", "-Djava.security.egd=file:/dev/./urandom", "-Xdebug", "-jar", "/opt/disa/data/disa-api-integ.jar" ]

# Dev
ENTRYPOINT [ "java", "-Djava.security.egd=file:/dev/./urandom", "-Xdebug", "-Xrunjdwp:server=y,transport=dt_socket,address=8001,suspend=n", "-jar", "/opt/disa/data/disa-api-integ.jar" ]
