#rockyio/phalcon-swoole:phalcon5.5-swoole5.0-php8.0-alpine
FROM phpswoole/swoole:5.0.3-php8.0-alpine
RUN set -ex && \
	sed -i 's/dl-cdn.alpinelinux.org/mirrors.ustc.edu.cn/g' /etc/apk/repositories && \
	apk update && \
	apk add --no-cache libstdc++ && \
	apk add --no-cache --virtual .build-deps $PHPIZE_DEPS curl-dev openssl-dev pcre-dev pcre2-dev zlib-dev && \
	pecl install psr && \
	docker-php-ext-enable psr && \
	pecl install phalcon-5.5.0 && \
	docker-php-ext-enable phalcon && \
	pecl clear-cache && \
	apk del .build-deps

WORKDIR "/var/www/"
