<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `php-zendserver`

-	[`php-zendserver:2019.0`](#php-zendserver20190)
-	[`php-zendserver:2021.0`](#php-zendserver20210)
-	[`php-zendserver:5.6`](#php-zendserver56)
-	[`php-zendserver:8.5`](#php-zendserver85)
-	[`php-zendserver:8.5-php5.6`](#php-zendserver85-php56)
-	[`php-zendserver:9.1`](#php-zendserver91)
-	[`php-zendserver:latest`](#php-zendserverlatest)

## `php-zendserver:2019.0`

```console
$ docker pull php-zendserver@sha256:aac1f97ae06aefebc3e07485eda39532f95ef57c900bc95d99905fcff2ac485a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:2019.0` - linux; amd64

```console
$ docker pull php-zendserver@sha256:628bb2ab22999198ab98be53e4c9e74f242da3e5a4689fe8dadc3b5a2f6e2e5d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.7 MB (483681348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a366dbfb7baf11e0185df884191a0c75d7a139c206079c0b81cb0d8e247b69ec`
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
# Tue, 27 Jul 2021 02:07:22 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Tue, 27 Jul 2021 02:09:07 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.7+b403     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Tue, 27 Jul 2021 02:09:11 GMT
ENV ZS_INIT_VERSION=0.3
# Tue, 27 Jul 2021 02:09:11 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Tue, 27 Jul 2021 02:09:11 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Tue, 27 Jul 2021 02:09:12 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Tue, 27 Jul 2021 02:09:12 GMT
WORKDIR /usr/local/zs-init
# Tue, 27 Jul 2021 02:09:18 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Tue, 27 Jul 2021 02:09:18 GMT
COPY dir:eecd98e9ebf1c61a12ae67558eb2a6ce846b9ebfadabbf08503e90b3e30d9496 in /usr/local/bin 
# Tue, 27 Jul 2021 02:09:18 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Tue, 27 Jul 2021 02:09:19 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Tue, 27 Jul 2021 02:09:19 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Tue, 27 Jul 2021 02:09:20 GMT
EXPOSE 80
# Tue, 27 Jul 2021 02:09:20 GMT
EXPOSE 443
# Tue, 27 Jul 2021 02:09:20 GMT
EXPOSE 10081
# Tue, 27 Jul 2021 02:09:20 GMT
EXPOSE 10082
# Tue, 27 Jul 2021 02:09:20 GMT
WORKDIR /var/www/html
# Tue, 27 Jul 2021 02:09:21 GMT
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
	-	`sha256:ca520356044ade40d3afbf6412d8dbb21efea1ee351f8ea1d5c03f0f8f1c93cb`  
		Last Modified: Tue, 27 Jul 2021 02:13:35 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df9b78941aeffdf00695c03970cbc71352bc653285d5531c679ef98c29fd2d2`  
		Last Modified: Tue, 27 Jul 2021 02:14:27 GMT  
		Size: 418.6 MB (418614354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346d150a9e1043577cc0c2f8723df76a8ee751415045577ce95ce57366be3583`  
		Last Modified: Tue, 27 Jul 2021 02:13:34 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750e7b4d7c0617cf9f4f8be1b6ac66cbce1e849e97f3cc725c902445b2a78177`  
		Last Modified: Tue, 27 Jul 2021 02:13:34 GMT  
		Size: 18.9 KB (18924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364998204e4072c3df23c743cf70293bb7ca2ed3b09f8062ffc592296adbfda6`  
		Last Modified: Tue, 27 Jul 2021 02:13:33 GMT  
		Size: 5.1 MB (5148976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac99097762e5ff3eca8305f45f1775b9aa6f5227341e22253afa47a473837cd`  
		Last Modified: Tue, 27 Jul 2021 02:13:32 GMT  
		Size: 14.3 KB (14292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f1e5f95812ec45ea7b5a7f0daf26bf7d231388f03f3d749094a5cd04973468`  
		Last Modified: Tue, 27 Jul 2021 02:13:32 GMT  
		Size: 2.6 KB (2560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3b6daf836e0a628d715d907a73f66dd0eb2c551b99440a2246736fb69a7595`  
		Last Modified: Tue, 27 Jul 2021 02:13:32 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc45c0e20fb6613217943694e480af76cd6e49976c615aa8eb8435d09100c79`  
		Last Modified: Tue, 27 Jul 2021 02:13:32 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:2021.0`

```console
$ docker pull php-zendserver@sha256:b59276bddcabf2546fa700b4be2b8127ef179ad8b56f762944817e4ddf2242c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:2021.0` - linux; amd64

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

## `php-zendserver:5.6`

```console
$ docker pull php-zendserver@sha256:b90156eaca7ef2c8b758873a3cd4bcff77a36836cc43e3904cf398c94beeb234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:ace129f951d15af719dfd478fb7b4730ef2311b6558af565f3f6b48a1fbe7643
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.6 MB (315604299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e31539ea4b65a5763f6f090c06c89fbeac973a1d1c03e076d46900f097adab`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Mon, 26 Jul 2021 21:22:15 GMT
ADD file:a94a87e268e99c78143fae5148bd1200bf0da90c0e7f42bd8c168bb205ccb105 in / 
# Mon, 26 Jul 2021 21:22:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 26 Jul 2021 21:22:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:22:17 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 26 Jul 2021 21:22:18 GMT
CMD ["/bin/bash"]
# Tue, 27 Jul 2021 02:02:38 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Tue, 27 Jul 2021 02:02:39 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Tue, 27 Jul 2021 02:02:39 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Tue, 27 Jul 2021 02:04:48 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Tue, 27 Jul 2021 02:04:51 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Tue, 27 Jul 2021 02:04:52 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Tue, 27 Jul 2021 02:04:52 GMT
RUN /usr/sbin/a2enmod headers
# Tue, 27 Jul 2021 02:04:53 GMT
ENV ZS_INIT_VERSION=0.3
# Tue, 27 Jul 2021 02:04:53 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Tue, 27 Jul 2021 02:04:54 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Tue, 27 Jul 2021 02:04:54 GMT
WORKDIR /usr/local/zs-init
# Tue, 27 Jul 2021 02:05:01 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Tue, 27 Jul 2021 02:05:01 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Tue, 27 Jul 2021 02:05:01 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Tue, 27 Jul 2021 02:05:02 GMT
RUN rm /var/www/html/index.html
# Tue, 27 Jul 2021 02:05:02 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Tue, 27 Jul 2021 02:05:03 GMT
EXPOSE 80
# Tue, 27 Jul 2021 02:05:03 GMT
EXPOSE 443
# Tue, 27 Jul 2021 02:05:03 GMT
EXPOSE 10081
# Tue, 27 Jul 2021 02:05:03 GMT
EXPOSE 10082
# Tue, 27 Jul 2021 02:05:03 GMT
WORKDIR /var/www/html
# Tue, 27 Jul 2021 02:05:04 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:52818491084148fa3469964bbcc3576686018a3b16b2e29be0407565c4c80b44`  
		Last Modified: Thu, 22 Jul 2021 16:25:00 GMT  
		Size: 46.5 MB (46497362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9df81d603d28f2a294b2f11b4f60d07b5b833b2ad7d6659a3f59b10cff2696`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636d9303bf663657be8e6796d720913bb985b5343da7949749ae1e72b54a88d8`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672b5bdcef61237567b311ad3d349f5eae18ba839ce2b204858a3083437a0a59`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed538dda0db70fb8dc46dcd6c20ed29860391557a1e5f11c024b8b7ee026358a`  
		Last Modified: Tue, 27 Jul 2021 02:11:52 GMT  
		Size: 14.7 KB (14703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e659282b775740b64bf1b3c90d5585ca367b75ddda32c9f986d2f66509b5bab`  
		Last Modified: Tue, 27 Jul 2021 02:11:52 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed7daeb6f8f3105e131056889e94d0ebdecba10daab89c90d2f2d246cf08c1b`  
		Last Modified: Tue, 27 Jul 2021 02:11:52 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039c92c54de8ffae773c5f437b35537ceb8a3b16f877690347d283ed85134787`  
		Last Modified: Tue, 27 Jul 2021 02:12:20 GMT  
		Size: 263.9 MB (263908856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2980aef8e8af07bcb5239654ebf7b5aa44d8eee7bbc870c046367974be2c2e`  
		Last Modified: Tue, 27 Jul 2021 02:11:50 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4122db113dd54dc5672e9a437101a6344310ac7e3f7f97fbf1acf5376581835b`  
		Last Modified: Tue, 27 Jul 2021 02:11:49 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95447ddcd739f528788e072c850b3300b564884c79571d5108f3c41705a9279a`  
		Last Modified: Tue, 27 Jul 2021 02:11:49 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93447f3f42ea655dc07a084f8274a8dcdbcfa8216cce819fe7c2cc5d4453339`  
		Last Modified: Tue, 27 Jul 2021 02:11:49 GMT  
		Size: 18.9 KB (18858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8939379c4c9359a8af1efa5678b8b6d6dca892d09ec19701149878cfc6993ea3`  
		Last Modified: Tue, 27 Jul 2021 02:11:48 GMT  
		Size: 5.1 MB (5144220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1295219a7225ac33b2151de163992d5b9d129ec9daaea06afe61ffda6a83826c`  
		Last Modified: Tue, 27 Jul 2021 02:11:47 GMT  
		Size: 13.4 KB (13353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81eb20faae46fe8ce264bfc6e03b424f80c286b1f02bd4bccc24ab6400b4494d`  
		Last Modified: Tue, 27 Jul 2021 02:11:47 GMT  
		Size: 2.6 KB (2565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3733a6423d58bc96bf1868b0272a3ea0e47785b42b0359d20bc1d493fcbccf6`  
		Last Modified: Tue, 27 Jul 2021 02:11:47 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6161a1621b1afc2b8fcf937a42d5b0b0c9b87942deca12a18d45f50d527b1b90`  
		Last Modified: Tue, 27 Jul 2021 02:11:47 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5`

```console
$ docker pull php-zendserver@sha256:b90156eaca7ef2c8b758873a3cd4bcff77a36836cc43e3904cf398c94beeb234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:8.5` - linux; amd64

```console
$ docker pull php-zendserver@sha256:ace129f951d15af719dfd478fb7b4730ef2311b6558af565f3f6b48a1fbe7643
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.6 MB (315604299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e31539ea4b65a5763f6f090c06c89fbeac973a1d1c03e076d46900f097adab`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Mon, 26 Jul 2021 21:22:15 GMT
ADD file:a94a87e268e99c78143fae5148bd1200bf0da90c0e7f42bd8c168bb205ccb105 in / 
# Mon, 26 Jul 2021 21:22:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 26 Jul 2021 21:22:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:22:17 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 26 Jul 2021 21:22:18 GMT
CMD ["/bin/bash"]
# Tue, 27 Jul 2021 02:02:38 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Tue, 27 Jul 2021 02:02:39 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Tue, 27 Jul 2021 02:02:39 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Tue, 27 Jul 2021 02:04:48 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Tue, 27 Jul 2021 02:04:51 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Tue, 27 Jul 2021 02:04:52 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Tue, 27 Jul 2021 02:04:52 GMT
RUN /usr/sbin/a2enmod headers
# Tue, 27 Jul 2021 02:04:53 GMT
ENV ZS_INIT_VERSION=0.3
# Tue, 27 Jul 2021 02:04:53 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Tue, 27 Jul 2021 02:04:54 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Tue, 27 Jul 2021 02:04:54 GMT
WORKDIR /usr/local/zs-init
# Tue, 27 Jul 2021 02:05:01 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Tue, 27 Jul 2021 02:05:01 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Tue, 27 Jul 2021 02:05:01 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Tue, 27 Jul 2021 02:05:02 GMT
RUN rm /var/www/html/index.html
# Tue, 27 Jul 2021 02:05:02 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Tue, 27 Jul 2021 02:05:03 GMT
EXPOSE 80
# Tue, 27 Jul 2021 02:05:03 GMT
EXPOSE 443
# Tue, 27 Jul 2021 02:05:03 GMT
EXPOSE 10081
# Tue, 27 Jul 2021 02:05:03 GMT
EXPOSE 10082
# Tue, 27 Jul 2021 02:05:03 GMT
WORKDIR /var/www/html
# Tue, 27 Jul 2021 02:05:04 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:52818491084148fa3469964bbcc3576686018a3b16b2e29be0407565c4c80b44`  
		Last Modified: Thu, 22 Jul 2021 16:25:00 GMT  
		Size: 46.5 MB (46497362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9df81d603d28f2a294b2f11b4f60d07b5b833b2ad7d6659a3f59b10cff2696`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636d9303bf663657be8e6796d720913bb985b5343da7949749ae1e72b54a88d8`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672b5bdcef61237567b311ad3d349f5eae18ba839ce2b204858a3083437a0a59`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed538dda0db70fb8dc46dcd6c20ed29860391557a1e5f11c024b8b7ee026358a`  
		Last Modified: Tue, 27 Jul 2021 02:11:52 GMT  
		Size: 14.7 KB (14703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e659282b775740b64bf1b3c90d5585ca367b75ddda32c9f986d2f66509b5bab`  
		Last Modified: Tue, 27 Jul 2021 02:11:52 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed7daeb6f8f3105e131056889e94d0ebdecba10daab89c90d2f2d246cf08c1b`  
		Last Modified: Tue, 27 Jul 2021 02:11:52 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039c92c54de8ffae773c5f437b35537ceb8a3b16f877690347d283ed85134787`  
		Last Modified: Tue, 27 Jul 2021 02:12:20 GMT  
		Size: 263.9 MB (263908856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2980aef8e8af07bcb5239654ebf7b5aa44d8eee7bbc870c046367974be2c2e`  
		Last Modified: Tue, 27 Jul 2021 02:11:50 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4122db113dd54dc5672e9a437101a6344310ac7e3f7f97fbf1acf5376581835b`  
		Last Modified: Tue, 27 Jul 2021 02:11:49 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95447ddcd739f528788e072c850b3300b564884c79571d5108f3c41705a9279a`  
		Last Modified: Tue, 27 Jul 2021 02:11:49 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93447f3f42ea655dc07a084f8274a8dcdbcfa8216cce819fe7c2cc5d4453339`  
		Last Modified: Tue, 27 Jul 2021 02:11:49 GMT  
		Size: 18.9 KB (18858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8939379c4c9359a8af1efa5678b8b6d6dca892d09ec19701149878cfc6993ea3`  
		Last Modified: Tue, 27 Jul 2021 02:11:48 GMT  
		Size: 5.1 MB (5144220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1295219a7225ac33b2151de163992d5b9d129ec9daaea06afe61ffda6a83826c`  
		Last Modified: Tue, 27 Jul 2021 02:11:47 GMT  
		Size: 13.4 KB (13353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81eb20faae46fe8ce264bfc6e03b424f80c286b1f02bd4bccc24ab6400b4494d`  
		Last Modified: Tue, 27 Jul 2021 02:11:47 GMT  
		Size: 2.6 KB (2565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3733a6423d58bc96bf1868b0272a3ea0e47785b42b0359d20bc1d493fcbccf6`  
		Last Modified: Tue, 27 Jul 2021 02:11:47 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6161a1621b1afc2b8fcf937a42d5b0b0c9b87942deca12a18d45f50d527b1b90`  
		Last Modified: Tue, 27 Jul 2021 02:11:47 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5-php5.6`

```console
$ docker pull php-zendserver@sha256:b90156eaca7ef2c8b758873a3cd4bcff77a36836cc43e3904cf398c94beeb234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:8.5-php5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:ace129f951d15af719dfd478fb7b4730ef2311b6558af565f3f6b48a1fbe7643
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.6 MB (315604299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e31539ea4b65a5763f6f090c06c89fbeac973a1d1c03e076d46900f097adab`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Mon, 26 Jul 2021 21:22:15 GMT
ADD file:a94a87e268e99c78143fae5148bd1200bf0da90c0e7f42bd8c168bb205ccb105 in / 
# Mon, 26 Jul 2021 21:22:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 26 Jul 2021 21:22:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:22:17 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 26 Jul 2021 21:22:18 GMT
CMD ["/bin/bash"]
# Tue, 27 Jul 2021 02:02:38 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Tue, 27 Jul 2021 02:02:39 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Tue, 27 Jul 2021 02:02:39 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Tue, 27 Jul 2021 02:04:48 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Tue, 27 Jul 2021 02:04:51 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Tue, 27 Jul 2021 02:04:52 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Tue, 27 Jul 2021 02:04:52 GMT
RUN /usr/sbin/a2enmod headers
# Tue, 27 Jul 2021 02:04:53 GMT
ENV ZS_INIT_VERSION=0.3
# Tue, 27 Jul 2021 02:04:53 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Tue, 27 Jul 2021 02:04:54 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Tue, 27 Jul 2021 02:04:54 GMT
WORKDIR /usr/local/zs-init
# Tue, 27 Jul 2021 02:05:01 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Tue, 27 Jul 2021 02:05:01 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Tue, 27 Jul 2021 02:05:01 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Tue, 27 Jul 2021 02:05:02 GMT
RUN rm /var/www/html/index.html
# Tue, 27 Jul 2021 02:05:02 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Tue, 27 Jul 2021 02:05:03 GMT
EXPOSE 80
# Tue, 27 Jul 2021 02:05:03 GMT
EXPOSE 443
# Tue, 27 Jul 2021 02:05:03 GMT
EXPOSE 10081
# Tue, 27 Jul 2021 02:05:03 GMT
EXPOSE 10082
# Tue, 27 Jul 2021 02:05:03 GMT
WORKDIR /var/www/html
# Tue, 27 Jul 2021 02:05:04 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:52818491084148fa3469964bbcc3576686018a3b16b2e29be0407565c4c80b44`  
		Last Modified: Thu, 22 Jul 2021 16:25:00 GMT  
		Size: 46.5 MB (46497362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9df81d603d28f2a294b2f11b4f60d07b5b833b2ad7d6659a3f59b10cff2696`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636d9303bf663657be8e6796d720913bb985b5343da7949749ae1e72b54a88d8`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672b5bdcef61237567b311ad3d349f5eae18ba839ce2b204858a3083437a0a59`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed538dda0db70fb8dc46dcd6c20ed29860391557a1e5f11c024b8b7ee026358a`  
		Last Modified: Tue, 27 Jul 2021 02:11:52 GMT  
		Size: 14.7 KB (14703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e659282b775740b64bf1b3c90d5585ca367b75ddda32c9f986d2f66509b5bab`  
		Last Modified: Tue, 27 Jul 2021 02:11:52 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed7daeb6f8f3105e131056889e94d0ebdecba10daab89c90d2f2d246cf08c1b`  
		Last Modified: Tue, 27 Jul 2021 02:11:52 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039c92c54de8ffae773c5f437b35537ceb8a3b16f877690347d283ed85134787`  
		Last Modified: Tue, 27 Jul 2021 02:12:20 GMT  
		Size: 263.9 MB (263908856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2980aef8e8af07bcb5239654ebf7b5aa44d8eee7bbc870c046367974be2c2e`  
		Last Modified: Tue, 27 Jul 2021 02:11:50 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4122db113dd54dc5672e9a437101a6344310ac7e3f7f97fbf1acf5376581835b`  
		Last Modified: Tue, 27 Jul 2021 02:11:49 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95447ddcd739f528788e072c850b3300b564884c79571d5108f3c41705a9279a`  
		Last Modified: Tue, 27 Jul 2021 02:11:49 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93447f3f42ea655dc07a084f8274a8dcdbcfa8216cce819fe7c2cc5d4453339`  
		Last Modified: Tue, 27 Jul 2021 02:11:49 GMT  
		Size: 18.9 KB (18858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8939379c4c9359a8af1efa5678b8b6d6dca892d09ec19701149878cfc6993ea3`  
		Last Modified: Tue, 27 Jul 2021 02:11:48 GMT  
		Size: 5.1 MB (5144220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1295219a7225ac33b2151de163992d5b9d129ec9daaea06afe61ffda6a83826c`  
		Last Modified: Tue, 27 Jul 2021 02:11:47 GMT  
		Size: 13.4 KB (13353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81eb20faae46fe8ce264bfc6e03b424f80c286b1f02bd4bccc24ab6400b4494d`  
		Last Modified: Tue, 27 Jul 2021 02:11:47 GMT  
		Size: 2.6 KB (2565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3733a6423d58bc96bf1868b0272a3ea0e47785b42b0359d20bc1d493fcbccf6`  
		Last Modified: Tue, 27 Jul 2021 02:11:47 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6161a1621b1afc2b8fcf937a42d5b0b0c9b87942deca12a18d45f50d527b1b90`  
		Last Modified: Tue, 27 Jul 2021 02:11:47 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:9.1`

```console
$ docker pull php-zendserver@sha256:7df6dcf3dd0103424dbe18b83604de06989b6c566b65c00d8436ff1bf4a789f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:9.1` - linux; amd64

```console
$ docker pull php-zendserver@sha256:6e9a7730f768daa3fb4b64ecedc511cfaa83e7589c5ca0bcb14e1d89ca1d3b02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.2 MB (399249074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92af8d9f87d5875146b8cf0f62846900dc1107ecd229a9f4bdc046b68d094f9`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Mon, 26 Jul 2021 21:22:15 GMT
ADD file:a94a87e268e99c78143fae5148bd1200bf0da90c0e7f42bd8c168bb205ccb105 in / 
# Mon, 26 Jul 2021 21:22:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 26 Jul 2021 21:22:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:22:17 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 26 Jul 2021 21:22:18 GMT
CMD ["/bin/bash"]
# Tue, 27 Jul 2021 02:02:38 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Tue, 27 Jul 2021 02:05:18 GMT
COPY file:0d4830b5060fb75cec6a47b30d343d82f9c3d6f95f20c11635618b93dedb5720 in /etc/apt/sources.list.d/zend-server.list 
# Tue, 27 Jul 2021 02:06:43 GMT
RUN apt-get update     && apt-get install -y       curl       libmysqlclient20       unzip       git       zend-server-php-7.1=9.1.12+b211     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Tue, 27 Jul 2021 02:06:46 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Tue, 27 Jul 2021 02:06:47 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Tue, 27 Jul 2021 02:06:48 GMT
RUN /usr/sbin/a2enmod headers
# Tue, 27 Jul 2021 02:06:48 GMT
ENV ZS_INIT_VERSION=0.3
# Tue, 27 Jul 2021 02:06:48 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Tue, 27 Jul 2021 02:06:49 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Tue, 27 Jul 2021 02:06:49 GMT
WORKDIR /usr/local/zs-init
# Tue, 27 Jul 2021 02:06:56 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Tue, 27 Jul 2021 02:06:57 GMT
COPY dir:5966ca4828c37f68d48d11da814350a590451453f42aa83ef2eab6893db3e4cc in /usr/local/bin 
# Tue, 27 Jul 2021 02:06:57 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Tue, 27 Jul 2021 02:06:58 GMT
RUN rm /var/www/html/index.html
# Tue, 27 Jul 2021 02:06:58 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Tue, 27 Jul 2021 02:06:58 GMT
EXPOSE 80
# Tue, 27 Jul 2021 02:06:58 GMT
EXPOSE 443
# Tue, 27 Jul 2021 02:06:58 GMT
EXPOSE 10081
# Tue, 27 Jul 2021 02:06:59 GMT
EXPOSE 10082
# Tue, 27 Jul 2021 02:06:59 GMT
WORKDIR /var/www/html
# Tue, 27 Jul 2021 02:06:59 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:52818491084148fa3469964bbcc3576686018a3b16b2e29be0407565c4c80b44`  
		Last Modified: Thu, 22 Jul 2021 16:25:00 GMT  
		Size: 46.5 MB (46497362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9df81d603d28f2a294b2f11b4f60d07b5b833b2ad7d6659a3f59b10cff2696`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636d9303bf663657be8e6796d720913bb985b5343da7949749ae1e72b54a88d8`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672b5bdcef61237567b311ad3d349f5eae18ba839ce2b204858a3083437a0a59`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed538dda0db70fb8dc46dcd6c20ed29860391557a1e5f11c024b8b7ee026358a`  
		Last Modified: Tue, 27 Jul 2021 02:11:52 GMT  
		Size: 14.7 KB (14703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3620faeb9e2917c331c2fc763101c70e785ae0f6f66373acef8de4e3a3f17a`  
		Last Modified: Tue, 27 Jul 2021 02:12:41 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d7090506b46d9c027f5b3e71e39e63f1b99d19de1c180f4b2d4852970500ca`  
		Last Modified: Tue, 27 Jul 2021 02:13:23 GMT  
		Size: 347.5 MB (347548176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6870d183e4bf87fd312d9afc3c50fe35b8852586d98e62db9243f8e051f95dc9`  
		Last Modified: Tue, 27 Jul 2021 02:12:39 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833e843a0501f4d0c733bb131079cdc4feae953a5e1adfe3b8335ece6749ad1f`  
		Last Modified: Tue, 27 Jul 2021 02:12:39 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb75fd84244fb17ceabf72c3ee7f7674a6a538f6a05d3e1763b0d34a6d7e03e`  
		Last Modified: Tue, 27 Jul 2021 02:12:38 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7336d824b8c20d7ba187d67f370adc530938622dd4dcf461e6f58ce4a424643`  
		Last Modified: Tue, 27 Jul 2021 02:12:38 GMT  
		Size: 18.9 KB (18860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02725d30e9ed394a294150b43e0cfeced2a57db37e7b0208dd83adb40856d690`  
		Last Modified: Tue, 27 Jul 2021 02:12:37 GMT  
		Size: 5.1 MB (5148968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b81e448d3e65f92d0d558b679c99daa9c741f212c981c6a4662074462fcafc`  
		Last Modified: Tue, 27 Jul 2021 02:12:36 GMT  
		Size: 14.3 KB (14323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb1fb957bcb0f2271a0be21b1cc9c008ceec6eee1d9dd9852d6ff359330c8fb`  
		Last Modified: Tue, 27 Jul 2021 02:12:36 GMT  
		Size: 2.6 KB (2562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2327595a6d3b0b9804be3ee6074353080a9405e354bf69f0c06fee9e4d064175`  
		Last Modified: Tue, 27 Jul 2021 02:12:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6157a67afcdf99c5873c49a3df305272df27dabb3c90383afcf91eabaf0b42ec`  
		Last Modified: Tue, 27 Jul 2021 02:12:36 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
