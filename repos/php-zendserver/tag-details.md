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
$ docker pull php-zendserver@sha256:6083d887bf31af2bef79225656bf53a4df1160bc1d95cd0c10d3a85d9a43c72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:2019.0` - linux; amd64

```console
$ docker pull php-zendserver@sha256:fe10a50c9345447eabb82a796cdda2780054b99038306ee3a109ec3b2596db03
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.6 MB (483596251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a88e998b0574e194cc53852172e8e5340428857b29e7854560aa36d394a39a`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:23 GMT
ADD file:0d82cd095966e8ee78b593cb47a352eec842edb7bd9d9468e8a70154522447d1 in / 
# Fri, 01 Oct 2021 02:23:24 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:36:23 GMT
RUN apt-get update && apt-get install -y       gnupg
# Fri, 01 Oct 2021 05:36:31 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 01 Oct 2021 05:36:32 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 01 Oct 2021 05:38:14 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.7+b403     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 01 Oct 2021 05:38:18 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 01 Oct 2021 05:38:18 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 01 Oct 2021 05:38:18 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Fri, 01 Oct 2021 05:38:19 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Fri, 01 Oct 2021 05:38:19 GMT
WORKDIR /usr/local/zs-init
# Fri, 01 Oct 2021 05:38:25 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Fri, 01 Oct 2021 05:38:25 GMT
COPY dir:eecd98e9ebf1c61a12ae67558eb2a6ce846b9ebfadabbf08503e90b3e30d9496 in /usr/local/bin 
# Fri, 01 Oct 2021 05:38:26 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 01 Oct 2021 05:38:27 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Fri, 01 Oct 2021 05:38:27 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 01 Oct 2021 05:38:27 GMT
EXPOSE 80
# Fri, 01 Oct 2021 05:38:27 GMT
EXPOSE 443
# Fri, 01 Oct 2021 05:38:28 GMT
EXPOSE 10081
# Fri, 01 Oct 2021 05:38:28 GMT
EXPOSE 10082
# Fri, 01 Oct 2021 05:38:28 GMT
WORKDIR /var/www/html
# Fri, 01 Oct 2021 05:38:28 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:284055322776031bac33723839acb0db2d063a525ba4fa1fd268a831c7553b26`  
		Last Modified: Fri, 01 Oct 2021 02:25:02 GMT  
		Size: 26.7 MB (26705075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13529e6cc57a67237d07debf77c65a80a1fdf4fb0aec5905f55df52d1e78bbe2`  
		Last Modified: Fri, 01 Oct 2021 05:40:59 GMT  
		Size: 33.6 MB (33631991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76953dd729571f350a75f1a5815fead56b07b3af9fc0ee184928d2c325c45be8`  
		Last Modified: Fri, 01 Oct 2021 05:40:55 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824d9f4c5f189cdadf8b8b16cb2a947b44cc619697f1ebff3fa431872b4c17e9`  
		Last Modified: Fri, 01 Oct 2021 05:40:53 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b1c5c60ef0437db1fac486e5468b493ac8e3df98cb5266ae603faf890151db`  
		Last Modified: Fri, 01 Oct 2021 05:41:46 GMT  
		Size: 418.1 MB (418067932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3110ec646c3c34e53e3f351235bded56edfcc7330e681eca4c16b60d9930d3b2`  
		Last Modified: Fri, 01 Oct 2021 05:40:53 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87c06909a571e91ea7b56390c543d552ed1edf42c235d048623aac04f4cdcbd`  
		Last Modified: Fri, 01 Oct 2021 05:40:53 GMT  
		Size: 18.9 KB (18927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9765ec9b961541b24cb96c13a4bf0856a9d2dba258b7c1bb0d48c0b0ca732b9`  
		Last Modified: Fri, 01 Oct 2021 05:40:52 GMT  
		Size: 5.2 MB (5151962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874ed5af5dfda20a8b3dd8513a5791fd464f56a56623197f69974e55b5b0a035`  
		Last Modified: Fri, 01 Oct 2021 05:40:51 GMT  
		Size: 14.3 KB (14295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba55984c36e7ad6baa310b0a4d55c69a83a2f1c06ad6e3fb02de1a286ca28c5`  
		Last Modified: Fri, 01 Oct 2021 05:40:51 GMT  
		Size: 2.6 KB (2555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93fdfebb9a057bb50f380f95ae41df20b588f93e8ed5d79a3756bd93c9a6c47a`  
		Last Modified: Fri, 01 Oct 2021 05:40:51 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e61ef459e52c00335ed5639efec3f11a9433eefe7aa6bc42754829a42d7eee0`  
		Last Modified: Fri, 01 Oct 2021 05:40:51 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:2021.0`

```console
$ docker pull php-zendserver@sha256:d5073cf0f25c89032a58e7f2153b9a523f4e44c091f742792aeabdda56a4529f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:2021.0` - linux; amd64

```console
$ docker pull php-zendserver@sha256:94fba0713bc7af4fea7a270b099cf2ddcde22f1477de9239a2ae176108686430
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.0 MB (392019779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606eaa5ee825af782c1feee4a3540aa8f0bae5ac65c19b59cd99e7b5b3c79d64`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:23 GMT
ADD file:0d82cd095966e8ee78b593cb47a352eec842edb7bd9d9468e8a70154522447d1 in / 
# Fri, 01 Oct 2021 02:23:24 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:36:23 GMT
RUN apt-get update && apt-get install -y       gnupg
# Fri, 01 Oct 2021 05:36:31 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 01 Oct 2021 05:38:42 GMT
COPY file:1e70d8fd6f9643bffb703528edddba0aa02a58e95cc53e92f58a86cde29e732a in /etc/apt/sources.list.d/zend-server.list 
# Fri, 01 Oct 2021 05:40:17 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2021.0.0+b74     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 01 Oct 2021 05:40:20 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 01 Oct 2021 05:40:20 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 01 Oct 2021 05:40:20 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Fri, 01 Oct 2021 05:40:21 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Fri, 01 Oct 2021 05:40:21 GMT
WORKDIR /usr/local/zs-init
# Fri, 01 Oct 2021 05:40:26 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Fri, 01 Oct 2021 05:40:27 GMT
COPY dir:eecd98e9ebf1c61a12ae67558eb2a6ce846b9ebfadabbf08503e90b3e30d9496 in /usr/local/bin 
# Fri, 01 Oct 2021 05:40:27 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 01 Oct 2021 05:40:28 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Fri, 01 Oct 2021 05:40:28 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 01 Oct 2021 05:40:28 GMT
EXPOSE 80
# Fri, 01 Oct 2021 05:40:28 GMT
EXPOSE 443
# Fri, 01 Oct 2021 05:40:29 GMT
EXPOSE 10081
# Fri, 01 Oct 2021 05:40:29 GMT
EXPOSE 10082
# Fri, 01 Oct 2021 05:40:29 GMT
WORKDIR /var/www/html
# Fri, 01 Oct 2021 05:40:29 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:284055322776031bac33723839acb0db2d063a525ba4fa1fd268a831c7553b26`  
		Last Modified: Fri, 01 Oct 2021 02:25:02 GMT  
		Size: 26.7 MB (26705075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13529e6cc57a67237d07debf77c65a80a1fdf4fb0aec5905f55df52d1e78bbe2`  
		Last Modified: Fri, 01 Oct 2021 05:40:59 GMT  
		Size: 33.6 MB (33631991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76953dd729571f350a75f1a5815fead56b07b3af9fc0ee184928d2c325c45be8`  
		Last Modified: Fri, 01 Oct 2021 05:40:55 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95787698ef79284c6687ac84c6578b635144e5c9e2e76086f11ea3cdc8fed6c7`  
		Last Modified: Fri, 01 Oct 2021 05:41:56 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0bd401fb40cbd966d06e5a0b01a64aac211b5348d4307650d8c0b64d2b6738`  
		Last Modified: Fri, 01 Oct 2021 05:42:39 GMT  
		Size: 326.5 MB (326491629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d70065c1b0e4ee1a948a67af9d2814f99ddfdc92d388c1c0f06884f762642b`  
		Last Modified: Fri, 01 Oct 2021 05:41:55 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5fecc52ec2d2095e9a5fd96c39fbd4ac5232bdf5f3deea4d70de253231ad27`  
		Last Modified: Fri, 01 Oct 2021 05:41:55 GMT  
		Size: 18.9 KB (18926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148c1f01c9f851cc22a569250cf046d73452a1e993c83752d5e14f3a421649c2`  
		Last Modified: Fri, 01 Oct 2021 05:41:54 GMT  
		Size: 5.2 MB (5151799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abad7c8350f1cc7e3078d8ae0630b637a91ca18e3fde2b2d8684b5b3195a6a3`  
		Last Modified: Fri, 01 Oct 2021 05:41:53 GMT  
		Size: 14.3 KB (14290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c6a1b02f75d6f1a4e9eb87d1852dfa41deb6b2cbf63d0ec86b33e42ccb4a26`  
		Last Modified: Fri, 01 Oct 2021 05:41:53 GMT  
		Size: 2.6 KB (2554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4422c60a427858daf6a80e5459ca93f077eedda89c321931664304f18111053`  
		Last Modified: Fri, 01 Oct 2021 05:41:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62f4339c940f22096aa029711a7fa6760293f1edc13f677846505a03f0dae35`  
		Last Modified: Fri, 01 Oct 2021 05:41:53 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:5.6`

```console
$ docker pull php-zendserver@sha256:46087476dd829477b235937b1b774e539c67177fb9c637bde91b28b2e6cf9299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:5393691a9d8617643c002a7ec19c90639a480868ae335ab538499d1a05865d4d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.6 MB (315608578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513ed7b8cb626435a0c10f51c07b1631f83e70f06549e79357644c19c6d30670`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:27 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Tue, 31 Aug 2021 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:21:29 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:21:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:21:30 GMT
CMD ["/bin/bash"]
# Tue, 31 Aug 2021 04:02:14 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Tue, 31 Aug 2021 04:02:15 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Tue, 31 Aug 2021 04:02:15 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Tue, 31 Aug 2021 04:04:03 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Tue, 31 Aug 2021 04:04:06 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Tue, 31 Aug 2021 04:04:06 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Tue, 31 Aug 2021 04:04:07 GMT
RUN /usr/sbin/a2enmod headers
# Tue, 31 Aug 2021 04:04:07 GMT
ENV ZS_INIT_VERSION=0.3
# Tue, 31 Aug 2021 04:04:08 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Tue, 31 Aug 2021 04:04:09 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Tue, 31 Aug 2021 04:04:09 GMT
WORKDIR /usr/local/zs-init
# Tue, 31 Aug 2021 04:04:16 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Tue, 31 Aug 2021 04:04:16 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Tue, 31 Aug 2021 04:04:16 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Tue, 31 Aug 2021 04:04:17 GMT
RUN rm /var/www/html/index.html
# Tue, 31 Aug 2021 04:04:17 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Tue, 31 Aug 2021 04:04:17 GMT
EXPOSE 80
# Tue, 31 Aug 2021 04:04:18 GMT
EXPOSE 443
# Tue, 31 Aug 2021 04:04:18 GMT
EXPOSE 10081
# Tue, 31 Aug 2021 04:04:18 GMT
EXPOSE 10082
# Tue, 31 Aug 2021 04:04:18 GMT
WORKDIR /var/www/html
# Tue, 31 Aug 2021 04:04:18 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Thu, 05 Aug 2021 00:25:05 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Tue, 31 Aug 2021 01:23:09 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2102dd9376f61b14df18139d78a96caeb38426131bb6a85847a5733f84d83c32`  
		Last Modified: Tue, 31 Aug 2021 04:11:12 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae050479344fbb7ea0f86b97e8c772b7ae45103fa5cfc2bea2a4b79c631a1534`  
		Last Modified: Tue, 31 Aug 2021 04:11:11 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d990e63418cea6828a1754a0cfd88662fe780fa88dd2de23528d624ab6bc35`  
		Last Modified: Tue, 31 Aug 2021 04:11:11 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e78264dffd8afd8084e307db7cfd44f971f55d76534559ccd72b50b64108726`  
		Last Modified: Tue, 31 Aug 2021 04:11:40 GMT  
		Size: 263.9 MB (263910611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd783101a133a035071fca065237130e373e2f4cc4151957c9c461ae9a79cdf2`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19cbd07b1b667393092b9d2df1833f0b331cfe1eb5e6ad304f4acbda03136ab`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21aeee9b83798ca4fd42d7e5aa46ecd288c027160673f1be4f3d9d57b70a383`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7e05a640abfb3d3865705d1a482da844acc818d5c32089ee78ec8ba477136d`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 18.9 KB (18859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be58af708ccc85c876f8148b3f7af699d37b1d23a25d76c1c8eaedd03b6dcc9b`  
		Last Modified: Tue, 31 Aug 2021 04:11:08 GMT  
		Size: 5.1 MB (5146536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1df10206b55b2eb8839919bb0d056e7256e1dd2bb398a492c5b8317235fe6d`  
		Last Modified: Tue, 31 Aug 2021 04:11:07 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703d37b5f26f094cbc47c55b9abf4e3fe103e96208d7e102c579384ffe6add64`  
		Last Modified: Tue, 31 Aug 2021 04:11:06 GMT  
		Size: 2.6 KB (2566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15716512d8f97648b13d29fdbc7df5b8f6ec04e2ca06aa9447b31525f08c1c2c`  
		Last Modified: Tue, 31 Aug 2021 04:11:06 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72ae8545d8a1d76de6aadb8a94a839c2d60e2f164e0323e0ad4cc73a1853110`  
		Last Modified: Tue, 31 Aug 2021 04:11:06 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5`

```console
$ docker pull php-zendserver@sha256:46087476dd829477b235937b1b774e539c67177fb9c637bde91b28b2e6cf9299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:8.5` - linux; amd64

```console
$ docker pull php-zendserver@sha256:5393691a9d8617643c002a7ec19c90639a480868ae335ab538499d1a05865d4d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.6 MB (315608578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513ed7b8cb626435a0c10f51c07b1631f83e70f06549e79357644c19c6d30670`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:27 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Tue, 31 Aug 2021 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:21:29 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:21:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:21:30 GMT
CMD ["/bin/bash"]
# Tue, 31 Aug 2021 04:02:14 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Tue, 31 Aug 2021 04:02:15 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Tue, 31 Aug 2021 04:02:15 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Tue, 31 Aug 2021 04:04:03 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Tue, 31 Aug 2021 04:04:06 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Tue, 31 Aug 2021 04:04:06 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Tue, 31 Aug 2021 04:04:07 GMT
RUN /usr/sbin/a2enmod headers
# Tue, 31 Aug 2021 04:04:07 GMT
ENV ZS_INIT_VERSION=0.3
# Tue, 31 Aug 2021 04:04:08 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Tue, 31 Aug 2021 04:04:09 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Tue, 31 Aug 2021 04:04:09 GMT
WORKDIR /usr/local/zs-init
# Tue, 31 Aug 2021 04:04:16 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Tue, 31 Aug 2021 04:04:16 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Tue, 31 Aug 2021 04:04:16 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Tue, 31 Aug 2021 04:04:17 GMT
RUN rm /var/www/html/index.html
# Tue, 31 Aug 2021 04:04:17 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Tue, 31 Aug 2021 04:04:17 GMT
EXPOSE 80
# Tue, 31 Aug 2021 04:04:18 GMT
EXPOSE 443
# Tue, 31 Aug 2021 04:04:18 GMT
EXPOSE 10081
# Tue, 31 Aug 2021 04:04:18 GMT
EXPOSE 10082
# Tue, 31 Aug 2021 04:04:18 GMT
WORKDIR /var/www/html
# Tue, 31 Aug 2021 04:04:18 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Thu, 05 Aug 2021 00:25:05 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Tue, 31 Aug 2021 01:23:09 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2102dd9376f61b14df18139d78a96caeb38426131bb6a85847a5733f84d83c32`  
		Last Modified: Tue, 31 Aug 2021 04:11:12 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae050479344fbb7ea0f86b97e8c772b7ae45103fa5cfc2bea2a4b79c631a1534`  
		Last Modified: Tue, 31 Aug 2021 04:11:11 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d990e63418cea6828a1754a0cfd88662fe780fa88dd2de23528d624ab6bc35`  
		Last Modified: Tue, 31 Aug 2021 04:11:11 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e78264dffd8afd8084e307db7cfd44f971f55d76534559ccd72b50b64108726`  
		Last Modified: Tue, 31 Aug 2021 04:11:40 GMT  
		Size: 263.9 MB (263910611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd783101a133a035071fca065237130e373e2f4cc4151957c9c461ae9a79cdf2`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19cbd07b1b667393092b9d2df1833f0b331cfe1eb5e6ad304f4acbda03136ab`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21aeee9b83798ca4fd42d7e5aa46ecd288c027160673f1be4f3d9d57b70a383`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7e05a640abfb3d3865705d1a482da844acc818d5c32089ee78ec8ba477136d`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 18.9 KB (18859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be58af708ccc85c876f8148b3f7af699d37b1d23a25d76c1c8eaedd03b6dcc9b`  
		Last Modified: Tue, 31 Aug 2021 04:11:08 GMT  
		Size: 5.1 MB (5146536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1df10206b55b2eb8839919bb0d056e7256e1dd2bb398a492c5b8317235fe6d`  
		Last Modified: Tue, 31 Aug 2021 04:11:07 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703d37b5f26f094cbc47c55b9abf4e3fe103e96208d7e102c579384ffe6add64`  
		Last Modified: Tue, 31 Aug 2021 04:11:06 GMT  
		Size: 2.6 KB (2566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15716512d8f97648b13d29fdbc7df5b8f6ec04e2ca06aa9447b31525f08c1c2c`  
		Last Modified: Tue, 31 Aug 2021 04:11:06 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72ae8545d8a1d76de6aadb8a94a839c2d60e2f164e0323e0ad4cc73a1853110`  
		Last Modified: Tue, 31 Aug 2021 04:11:06 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5-php5.6`

```console
$ docker pull php-zendserver@sha256:46087476dd829477b235937b1b774e539c67177fb9c637bde91b28b2e6cf9299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:8.5-php5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:5393691a9d8617643c002a7ec19c90639a480868ae335ab538499d1a05865d4d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.6 MB (315608578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513ed7b8cb626435a0c10f51c07b1631f83e70f06549e79357644c19c6d30670`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:27 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Tue, 31 Aug 2021 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:21:29 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:21:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:21:30 GMT
CMD ["/bin/bash"]
# Tue, 31 Aug 2021 04:02:14 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Tue, 31 Aug 2021 04:02:15 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Tue, 31 Aug 2021 04:02:15 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Tue, 31 Aug 2021 04:04:03 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Tue, 31 Aug 2021 04:04:06 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Tue, 31 Aug 2021 04:04:06 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Tue, 31 Aug 2021 04:04:07 GMT
RUN /usr/sbin/a2enmod headers
# Tue, 31 Aug 2021 04:04:07 GMT
ENV ZS_INIT_VERSION=0.3
# Tue, 31 Aug 2021 04:04:08 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Tue, 31 Aug 2021 04:04:09 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Tue, 31 Aug 2021 04:04:09 GMT
WORKDIR /usr/local/zs-init
# Tue, 31 Aug 2021 04:04:16 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Tue, 31 Aug 2021 04:04:16 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Tue, 31 Aug 2021 04:04:16 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Tue, 31 Aug 2021 04:04:17 GMT
RUN rm /var/www/html/index.html
# Tue, 31 Aug 2021 04:04:17 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Tue, 31 Aug 2021 04:04:17 GMT
EXPOSE 80
# Tue, 31 Aug 2021 04:04:18 GMT
EXPOSE 443
# Tue, 31 Aug 2021 04:04:18 GMT
EXPOSE 10081
# Tue, 31 Aug 2021 04:04:18 GMT
EXPOSE 10082
# Tue, 31 Aug 2021 04:04:18 GMT
WORKDIR /var/www/html
# Tue, 31 Aug 2021 04:04:18 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Thu, 05 Aug 2021 00:25:05 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Tue, 31 Aug 2021 01:23:09 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2102dd9376f61b14df18139d78a96caeb38426131bb6a85847a5733f84d83c32`  
		Last Modified: Tue, 31 Aug 2021 04:11:12 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae050479344fbb7ea0f86b97e8c772b7ae45103fa5cfc2bea2a4b79c631a1534`  
		Last Modified: Tue, 31 Aug 2021 04:11:11 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d990e63418cea6828a1754a0cfd88662fe780fa88dd2de23528d624ab6bc35`  
		Last Modified: Tue, 31 Aug 2021 04:11:11 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e78264dffd8afd8084e307db7cfd44f971f55d76534559ccd72b50b64108726`  
		Last Modified: Tue, 31 Aug 2021 04:11:40 GMT  
		Size: 263.9 MB (263910611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd783101a133a035071fca065237130e373e2f4cc4151957c9c461ae9a79cdf2`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19cbd07b1b667393092b9d2df1833f0b331cfe1eb5e6ad304f4acbda03136ab`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21aeee9b83798ca4fd42d7e5aa46ecd288c027160673f1be4f3d9d57b70a383`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7e05a640abfb3d3865705d1a482da844acc818d5c32089ee78ec8ba477136d`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 18.9 KB (18859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be58af708ccc85c876f8148b3f7af699d37b1d23a25d76c1c8eaedd03b6dcc9b`  
		Last Modified: Tue, 31 Aug 2021 04:11:08 GMT  
		Size: 5.1 MB (5146536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1df10206b55b2eb8839919bb0d056e7256e1dd2bb398a492c5b8317235fe6d`  
		Last Modified: Tue, 31 Aug 2021 04:11:07 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703d37b5f26f094cbc47c55b9abf4e3fe103e96208d7e102c579384ffe6add64`  
		Last Modified: Tue, 31 Aug 2021 04:11:06 GMT  
		Size: 2.6 KB (2566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15716512d8f97648b13d29fdbc7df5b8f6ec04e2ca06aa9447b31525f08c1c2c`  
		Last Modified: Tue, 31 Aug 2021 04:11:06 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72ae8545d8a1d76de6aadb8a94a839c2d60e2f164e0323e0ad4cc73a1853110`  
		Last Modified: Tue, 31 Aug 2021 04:11:06 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:9.1`

```console
$ docker pull php-zendserver@sha256:cc80372d5dcac564f69bb3c8c066a46638ee40115142f5247079084a5ddc1179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:9.1` - linux; amd64

```console
$ docker pull php-zendserver@sha256:7b079ac3a11ceab944593ab3fbfbbac482a4d6611fa431c710e2bd0472c87888
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.3 MB (399260011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ac8051a5f543e6f729a4fc404e53a1f68ef6dc6c6443b992634a95664429c3`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:27 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Tue, 31 Aug 2021 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:21:29 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:21:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:21:30 GMT
CMD ["/bin/bash"]
# Tue, 31 Aug 2021 04:02:14 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Tue, 31 Aug 2021 04:04:22 GMT
COPY file:0d4830b5060fb75cec6a47b30d343d82f9c3d6f95f20c11635618b93dedb5720 in /etc/apt/sources.list.d/zend-server.list 
# Tue, 31 Aug 2021 04:05:46 GMT
RUN apt-get update     && apt-get install -y       curl       libmysqlclient20       unzip       git       zend-server-php-7.1=9.1.12+b211     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Tue, 31 Aug 2021 04:05:50 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Tue, 31 Aug 2021 04:05:51 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Tue, 31 Aug 2021 04:05:52 GMT
RUN /usr/sbin/a2enmod headers
# Tue, 31 Aug 2021 04:05:52 GMT
ENV ZS_INIT_VERSION=0.3
# Tue, 31 Aug 2021 04:05:52 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Tue, 31 Aug 2021 04:05:53 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Tue, 31 Aug 2021 04:05:53 GMT
WORKDIR /usr/local/zs-init
# Tue, 31 Aug 2021 04:06:00 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Tue, 31 Aug 2021 04:06:00 GMT
COPY dir:5966ca4828c37f68d48d11da814350a590451453f42aa83ef2eab6893db3e4cc in /usr/local/bin 
# Tue, 31 Aug 2021 04:06:01 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Tue, 31 Aug 2021 04:06:01 GMT
RUN rm /var/www/html/index.html
# Tue, 31 Aug 2021 04:06:02 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Tue, 31 Aug 2021 04:06:02 GMT
EXPOSE 80
# Tue, 31 Aug 2021 04:06:02 GMT
EXPOSE 443
# Tue, 31 Aug 2021 04:06:02 GMT
EXPOSE 10081
# Tue, 31 Aug 2021 04:06:02 GMT
EXPOSE 10082
# Tue, 31 Aug 2021 04:06:03 GMT
WORKDIR /var/www/html
# Tue, 31 Aug 2021 04:06:03 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Thu, 05 Aug 2021 00:25:05 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Tue, 31 Aug 2021 01:23:09 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2102dd9376f61b14df18139d78a96caeb38426131bb6a85847a5733f84d83c32`  
		Last Modified: Tue, 31 Aug 2021 04:11:12 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef9ee709ba9d99042fc4eae3385479692614cfd72cbc83c98522170944f9f1a`  
		Last Modified: Tue, 31 Aug 2021 04:12:01 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837980bcf5c021764e8ff0b5e1826fa0d23d4d4bbd2fe02962a470f7d8df8f11`  
		Last Modified: Tue, 31 Aug 2021 04:12:43 GMT  
		Size: 347.6 MB (347557251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f311d7aa89c09f28fce59942e782699474050c73dc60b2c0570f5eb2fe64c4fc`  
		Last Modified: Tue, 31 Aug 2021 04:11:59 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c9384096c8027661058200d5dd435498203ae6cea4ffada13ffcc34a17f730`  
		Last Modified: Tue, 31 Aug 2021 04:11:59 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a391773894550b0dcf95133d7a0ebfc325acd5a660c35f96c77133e3fd8f740c`  
		Last Modified: Tue, 31 Aug 2021 04:11:59 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99104e97158863a1815e4b564104f84c3c0671a3ef2a49ddf935cb20a41e537`  
		Last Modified: Tue, 31 Aug 2021 04:11:59 GMT  
		Size: 18.9 KB (18859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc404237abddc7a47d1e606dc92470e0035dcd32745c3c0bf383528304c96d7`  
		Last Modified: Tue, 31 Aug 2021 04:11:58 GMT  
		Size: 5.2 MB (5150653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63099d2783ee41f72d28cc95ab35ba28c5674108eead4fba7719574ecddb2c99`  
		Last Modified: Tue, 31 Aug 2021 04:11:57 GMT  
		Size: 14.3 KB (14320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16df2874073685e8fadc4aa9c04fc75132336de6749145d708e7d664cc03a03f`  
		Last Modified: Tue, 31 Aug 2021 04:11:57 GMT  
		Size: 2.6 KB (2559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b978107de3a3767f2ffe65e620f34ce62d93b74cbd20b77b1821327e7458539b`  
		Last Modified: Tue, 31 Aug 2021 04:11:57 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3a81a9d2085d59971d4608251a552a6c9631466fcac109142e49c26602cf12`  
		Last Modified: Tue, 31 Aug 2021 04:11:57 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:latest`

```console
$ docker pull php-zendserver@sha256:d5073cf0f25c89032a58e7f2153b9a523f4e44c091f742792aeabdda56a4529f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:latest` - linux; amd64

```console
$ docker pull php-zendserver@sha256:94fba0713bc7af4fea7a270b099cf2ddcde22f1477de9239a2ae176108686430
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.0 MB (392019779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606eaa5ee825af782c1feee4a3540aa8f0bae5ac65c19b59cd99e7b5b3c79d64`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:23 GMT
ADD file:0d82cd095966e8ee78b593cb47a352eec842edb7bd9d9468e8a70154522447d1 in / 
# Fri, 01 Oct 2021 02:23:24 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:36:23 GMT
RUN apt-get update && apt-get install -y       gnupg
# Fri, 01 Oct 2021 05:36:31 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 01 Oct 2021 05:38:42 GMT
COPY file:1e70d8fd6f9643bffb703528edddba0aa02a58e95cc53e92f58a86cde29e732a in /etc/apt/sources.list.d/zend-server.list 
# Fri, 01 Oct 2021 05:40:17 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2021.0.0+b74     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 01 Oct 2021 05:40:20 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 01 Oct 2021 05:40:20 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 01 Oct 2021 05:40:20 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Fri, 01 Oct 2021 05:40:21 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Fri, 01 Oct 2021 05:40:21 GMT
WORKDIR /usr/local/zs-init
# Fri, 01 Oct 2021 05:40:26 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Fri, 01 Oct 2021 05:40:27 GMT
COPY dir:eecd98e9ebf1c61a12ae67558eb2a6ce846b9ebfadabbf08503e90b3e30d9496 in /usr/local/bin 
# Fri, 01 Oct 2021 05:40:27 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 01 Oct 2021 05:40:28 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Fri, 01 Oct 2021 05:40:28 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 01 Oct 2021 05:40:28 GMT
EXPOSE 80
# Fri, 01 Oct 2021 05:40:28 GMT
EXPOSE 443
# Fri, 01 Oct 2021 05:40:29 GMT
EXPOSE 10081
# Fri, 01 Oct 2021 05:40:29 GMT
EXPOSE 10082
# Fri, 01 Oct 2021 05:40:29 GMT
WORKDIR /var/www/html
# Fri, 01 Oct 2021 05:40:29 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:284055322776031bac33723839acb0db2d063a525ba4fa1fd268a831c7553b26`  
		Last Modified: Fri, 01 Oct 2021 02:25:02 GMT  
		Size: 26.7 MB (26705075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13529e6cc57a67237d07debf77c65a80a1fdf4fb0aec5905f55df52d1e78bbe2`  
		Last Modified: Fri, 01 Oct 2021 05:40:59 GMT  
		Size: 33.6 MB (33631991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76953dd729571f350a75f1a5815fead56b07b3af9fc0ee184928d2c325c45be8`  
		Last Modified: Fri, 01 Oct 2021 05:40:55 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95787698ef79284c6687ac84c6578b635144e5c9e2e76086f11ea3cdc8fed6c7`  
		Last Modified: Fri, 01 Oct 2021 05:41:56 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0bd401fb40cbd966d06e5a0b01a64aac211b5348d4307650d8c0b64d2b6738`  
		Last Modified: Fri, 01 Oct 2021 05:42:39 GMT  
		Size: 326.5 MB (326491629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d70065c1b0e4ee1a948a67af9d2814f99ddfdc92d388c1c0f06884f762642b`  
		Last Modified: Fri, 01 Oct 2021 05:41:55 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5fecc52ec2d2095e9a5fd96c39fbd4ac5232bdf5f3deea4d70de253231ad27`  
		Last Modified: Fri, 01 Oct 2021 05:41:55 GMT  
		Size: 18.9 KB (18926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148c1f01c9f851cc22a569250cf046d73452a1e993c83752d5e14f3a421649c2`  
		Last Modified: Fri, 01 Oct 2021 05:41:54 GMT  
		Size: 5.2 MB (5151799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abad7c8350f1cc7e3078d8ae0630b637a91ca18e3fde2b2d8684b5b3195a6a3`  
		Last Modified: Fri, 01 Oct 2021 05:41:53 GMT  
		Size: 14.3 KB (14290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c6a1b02f75d6f1a4e9eb87d1852dfa41deb6b2cbf63d0ec86b33e42ccb4a26`  
		Last Modified: Fri, 01 Oct 2021 05:41:53 GMT  
		Size: 2.6 KB (2554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4422c60a427858daf6a80e5459ca93f077eedda89c321931664304f18111053`  
		Last Modified: Fri, 01 Oct 2021 05:41:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62f4339c940f22096aa029711a7fa6760293f1edc13f677846505a03f0dae35`  
		Last Modified: Fri, 01 Oct 2021 05:41:53 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
