# Dev Usage, run from .docker/ directory:
# docker-compose build
# docker-compose run

FROM webdevops/php:8.1

RUN ln -sf /usr/share/zoneinfo/Asia/Bangkok /etc/localtime

ENV FPM_PM_MAX_CHILDREN=10 \
    FPM_PM_START_SERVERS=3 \
    FPM_PM_MIN_SPARE_SERVERS=2 \
    FPM_PM_MAX_SPARE_SERVERS=5 \
    FPM_MAX_REQUESTS=100

#install Imagemagick & PHP Imagick ext
RUN apt-get update && apt-get install -y \
        libmagickwand-dev --no-install-recommends
# RUN pecl install imagick && docker-php-ext-enable imagick
