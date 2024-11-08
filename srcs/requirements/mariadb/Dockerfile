FROM debian:buster

RUN apt -y update &&  apt-get install mariadb-server -y

COPY conf/50-server.cnf	/etc/mysql/mariadb.conf.d/50-server.cnf

COPY ./tools/scriptdb.sh /

RUN chmod 777 /scriptdb.sh

RUN chown -R mysql:mysql /var/lib/mysql

CMD ["/scriptdb.sh"]