FROM debian:jessie

RUN apt-get update && apt-get install -y php5-common php5-cli php5-fpm php5-mcrypt php5-mysql php5-apcu php5-gd php5-imagick php5-curl php5-intl

ADD app.ini /etc/php5/fpm/conf.d/
ADD app.ini /etc/php5/cli/conf.d/

ADD app.pool.conf /etc/php5/fpm/pool.d/

RUN usermod -u 1000 www-data

CMD ["php5-fpm", "-F"]

EXPOSE 9000