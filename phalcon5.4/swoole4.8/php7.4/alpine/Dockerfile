#rockyio/phalcon-swoole:phalcon5.4-swoole4.8-php7.4-alpine
FROM phpswoole/swoole:4.8.13-php7.4-alpine 
RUN set -ex && \
	sed -i 's/dl-cdn.alpinelinux.org/mirrors.ustc.edu.cn/g' /etc/apk/repositories && \
	apk update && \
	apk add --no-cache libstdc++ && \
	apk add --no-cache --virtual .build-deps $PHPIZE_DEPS curl-dev openssl-dev pcre-dev pcre2-dev zlib-dev && \
	pecl install psr && \
	docker-php-ext-enable psr && \
	pecl install phalcon-5.4.0 && \
	docker-php-ext-enable phalcon && \
	pecl clear-cache && \
	apk del .build-deps

WORKDIR "/var/www/"
