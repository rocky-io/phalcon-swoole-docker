### php镜像 dockerfile 文件仓库
此镜像包含 phalcon 扩展 和 swoole 扩展，不包含php-fpm。

此镜像文件在 [phpswoole/swoole](https://hub.docker.com/r/phpswoole/swoole) 镜像的基础上增加了phalcon扩展。

由于国内服务器无法访问 dl-cdn.alpinelinux.org 地址，基于alpine的镜像需加上：

    sed -i 's/dl-cdn.alpinelinux.org/mirrors.ustc.edu.cn/g' /etc/apk/repositories

