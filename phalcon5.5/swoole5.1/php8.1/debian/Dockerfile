#rockyio/phalcon-swoole:phalcon5.5-swoole5.1-php8.1-debian
FROM phpswoole/swoole:5.1.2-php8.1
RUN set -ex && \
	pecl install psr && \
	docker-php-ext-enable psr && \
	pecl install phalcon-5.5.0 && \
	docker-php-ext-enable phalcon && \
	pecl clear-cache

WORKDIR "/var/www/"
