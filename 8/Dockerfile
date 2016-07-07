FROM drupaldocker/php-dev:cli
MAINTAINER drupal-docker

RUN apt-get update && apt-get install -y mysql-client openssh-client rsync \
  && composer global require drush/drush:8.* \
  && ln -s ~/.composer/vendor/bin/drush /usr/local/bin/drush \
  && drush core-status -y \
  && rm -rf /var/lib/apt/lists/*

CMD ["drush", "core-cli"]
