## `php-zendserver:latest`

```console
$ docker pull php-zendserver@sha256:b59276bddcabf2546fa700b4be2b8127ef179ad8b56f762944817e4ddf2242c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:latest` - linux; amd64

```console
$ docker pull php-zendserver@sha256:58ea481e2d0a8f19fcb1e4b146432799f8a3a45dcf340b68014e5ca212369a30
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.0 MB (391005078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f26bf9e3a6a671c115ba7e9da7457c9463c98bee3fe0dc4c0bbf9a1c6eb1a`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:07:21 GMT
RUN apt-get update && apt-get install -y       gnupg
# Tue, 27 Jul 2021 02:07:22 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Tue, 27 Jul 2021 02:09:24 GMT
COPY file:1e70d8fd6f9643bffb703528edddba0aa02a58e95cc53e92f58a86cde29e732a in /etc/apt/sources.list.d/zend-server.list 
# Tue, 27 Jul 2021 02:11:08 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2021.0.0+b74     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Tue, 27 Jul 2021 02:11:11 GMT
ENV ZS_INIT_VERSION=0.3
# Tue, 27 Jul 2021 02:11:11 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Tue, 27 Jul 2021 02:11:12 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Tue, 27 Jul 2021 02:11:13 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Tue, 27 Jul 2021 02:11:13 GMT
WORKDIR /usr/local/zs-init
# Tue, 27 Jul 2021 02:11:18 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Tue, 27 Jul 2021 02:11:18 GMT
COPY dir:eecd98e9ebf1c61a12ae67558eb2a6ce846b9ebfadabbf08503e90b3e30d9496 in /usr/local/bin 
# Tue, 27 Jul 2021 02:11:18 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Tue, 27 Jul 2021 02:11:19 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Tue, 27 Jul 2021 02:11:19 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Tue, 27 Jul 2021 02:11:20 GMT
EXPOSE 80
# Tue, 27 Jul 2021 02:11:20 GMT
EXPOSE 443
# Tue, 27 Jul 2021 02:11:20 GMT
EXPOSE 10081
# Tue, 27 Jul 2021 02:11:20 GMT
EXPOSE 10082
# Tue, 27 Jul 2021 02:11:20 GMT
WORKDIR /var/www/html
# Tue, 27 Jul 2021 02:11:21 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439d450bb5138ad0d576cb80ca7e5ad9e0230f80134fb62551a6668781fc19bc`  
		Last Modified: Tue, 27 Jul 2021 02:13:41 GMT  
		Size: 33.2 MB (33169690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbc94fbf2820d51e5790fafb84847514c4b10ea0509bf158fa25e5a74b07814`  
		Last Modified: Tue, 27 Jul 2021 02:13:36 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f441c68a534b6795b936216285a2d0d8699819283adf32a2891e5cc189c569f`  
		Last Modified: Tue, 27 Jul 2021 02:14:39 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdacdf62256a14efd288ed2736b683053169b174b19bfae7e12354ea74d4cbf8`  
		Last Modified: Tue, 27 Jul 2021 02:15:22 GMT  
		Size: 325.9 MB (325938190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a86f99df2338aeeb32e25354a545dc91e36d1328aa0096cf6a10e4284036728`  
		Last Modified: Tue, 27 Jul 2021 02:14:41 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4eb13304513592bae13d354e59ceaefa11563d5c134361a7d2b2cc12c2103a3`  
		Last Modified: Tue, 27 Jul 2021 02:14:38 GMT  
		Size: 18.9 KB (18927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06784d5f4893d981bc835355e96a3194d7b8782ed32dea6f4bbb40adbb80c10`  
		Last Modified: Tue, 27 Jul 2021 02:14:37 GMT  
		Size: 5.1 MB (5148878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe7538c44534a500304d663f86bbddab3f596abdeecc5f62bae44a932ac58a0`  
		Last Modified: Tue, 27 Jul 2021 02:14:35 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98155d7040d006c5231bd0d66df85d309137fb4c9db8010d90ca566fbc3c3fe7`  
		Last Modified: Tue, 27 Jul 2021 02:14:36 GMT  
		Size: 2.6 KB (2556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7926673e71089d1ebfb960282b049285f01aeaf881265ce6b5e1fcc173e3c96`  
		Last Modified: Tue, 27 Jul 2021 02:14:36 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc81a1cfe7f2d522dbf563ecec1d4aae732c6dee8cf565d3a5b3fa2864f29fa`  
		Last Modified: Tue, 27 Jul 2021 02:14:35 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
