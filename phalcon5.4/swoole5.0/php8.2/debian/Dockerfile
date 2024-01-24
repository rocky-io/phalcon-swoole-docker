#rockyio/phalcon-swoole:phalcon5.4-swoole5.0-php8.2-debian
FROM phpswoole/swoole:5.0.3-php8.2
RUN set -ex && \
	pecl install psr && \
	docker-php-ext-enable psr && \
	pecl install phalcon-5.4.0 && \
	docker-php-ext-enable phalcon && \
	pecl clear-cache

WORKDIR "/var/www/"
