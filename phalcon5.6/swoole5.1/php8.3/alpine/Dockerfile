#rockyio/phalcon-swoole:phalcon5.6-swoole5.1-php8.3-alpine
FROM phpswoole/swoole:5.1.2-php8.3-alpine
RUN set -ex && \
	sed -i 's/dl-cdn.alpinelinux.org/mirrors.ustc.edu.cn/g' /etc/apk/repositories && \
	apk update && \
	apk add --no-cache libstdc++ && \
	apk add --no-cache --virtual .build-deps $PHPIZE_DEPS curl-dev openssl-dev pcre-dev pcre2-dev zlib-dev && \
	pecl install psr && \
	docker-php-ext-enable psr && \
	pecl install phalcon-5.6.0 && \
	docker-php-ext-enable phalcon && \
	pecl clear-cache && \
	apk del .build-deps

WORKDIR "/var/www/"
