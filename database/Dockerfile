FROM mysql:5.6

LABEL maintainer="his@fgh.org.mz" 

ENV MYSQL_ROOT_PASSWORD=root
ENV MYSQL_DATABASE=ViralLoadData
ENV MYSQL_USER=aphlinteg
ENV MYSQL_PASSWORD=D1saL1nk
ENV MYSQL_DATA_DIRECTORY=/opt/disa/data/system/mysql

ADD mysql.cnf /root/.my.cnf
ADD localtime /etc/localtime

COPY run.sh /run.sh

VOLUME /opt/disa/data

EXPOSE 3306

CMD ["/run.sh"]