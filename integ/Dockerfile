FROM openjdk:8-jdk-alpine

LABEL maintainer="his@fgh.org.mz" 

VOLUME [ "/opt/disa/data" ]

EXPOSE 8080

# Prod
#ENTRYPOINT [ "java", "-Djava.security.egd=file:/dev/./urandom", "-Xdebug", "-jar", "/opt/disa/data/disa-api-integ.jar" ]

# Dev
ENTRYPOINT [ "java", "-Djava.security.egd=file:/dev/./urandom", "-Xdebug", "-Xrunjdwp:server=y,transport=dt_socket,address=8000,suspend=n", "-jar", "/opt/disa/data/disa-api-integ.jar" ]
