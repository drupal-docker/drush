FROM drupaldocker/php-dev:5.6-alpine-cli
MAINTAINER drupal-docker

RUN apk add --no-cache mysql-client openssh-client rsync \
  && composer global require drush/drush:7.* \
  && rm -f /usr/local/bin/drush \
  && ln -s ~/.composer/vendor/bin/drush /usr/local/bin/drush \
  && drush core-status -y

CMD ["drush", "core-cli"]
