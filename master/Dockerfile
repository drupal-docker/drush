FROM drupaldocker/php-dev:7.0-cli
MAINTAINER drupal-docker

RUN apt-get update && apt-get install -y mysql-client openssh-client rsync \
  && cd ~ \
  && git clone --depth 1 --branch master https://github.com/drush-ops/drush.git drush \
  && cd drush \
  && composer install \
  && rm -f /usr/local/bin/drush \
  && ln -s ~/drush/drush /usr/local/bin/drush \
  && drush core-status -y \
  && drush core-init -y \
  && rm -rf /var/lib/apt/lists/*

CMD ["drush", "core-cli"]
