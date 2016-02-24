FROM drupaldocker/php:cli
MAINTAINER drupal-docker

ADD http://files.drush.org/drush.phar /usr/local/bin/drush

RUN apt-get update && apt-get install -y mysql-client \
  && chmod a+x /usr/local/bin/drush \
  && /usr/local/bin/drush core-status -y \
  && drush init -y \
	&& rm -rf /var/lib/apt/lists/*

CMD ["drush", "core-cli"]
