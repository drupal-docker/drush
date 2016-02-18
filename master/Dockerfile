FROM drupaldocker/php:cli
MAINTAINER drupal-docker

ADD http://files.drush.org/drush.phar /usr/local/bin/drush
RUN php /usr/local/bin/drush core-status -y && chmod a+x /usr/local/bin/drush
RUN drush init -y

CMD ["drush", "core-cli"]
