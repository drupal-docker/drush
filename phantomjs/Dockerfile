FROM drupaldocker/drush:latest
MAINTAINER drupal-docker

RUN apt-get update && apt-get install -y libfontconfig1 bzip2 \
  && rm -rf /var/lib/apt/lists/*

ADD https://bitbucket.org/ariya/phantomjs/downloads/phantomjs-2.1.1-linux-x86_64.tar.bz2 /root
RUN cd /root && tar xvjf phantomjs-2.1.1-linux-x86_64.tar.bz2 && mv phantomjs-2.1.1-linux-x86_64 phantomjs

CMD ["/root/phantomjs/bin/phantomjs", "--webdriver=8643"]

