# create your custom drupal image here, based of official drupal

FROM drupal:8

RUN /bin/bash -c "apt-get update && apt-get install -y git"
RUN /bin/bash -c "rm -rf /var/lib/apt/lists/*"

WORKDIR /var/www/html/themes

RUN /bin/bash -c "git clone --branch 8.x-3.x --single-branch --depth 1 \
    https://git.drupalcode.org/project/bootstrap.git \
    && chown -R www-data:www-data bootstrap"

WORKDIR /var/www/html

