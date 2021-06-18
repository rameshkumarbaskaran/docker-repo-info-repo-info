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
$ docker pull php-zendserver@sha256:be4f3c754ef6bf7c24bed2dfb51988d073384666faaa9069c58dd8db86ccbaa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:2019.0` - linux; amd64

```console
$ docker pull php-zendserver@sha256:246ad7d71f96c02781599c45efad967d67287b00dc56b9ef06c4d5d6753cb77e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.4 MB (483377482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2024545d8e4ae1a93ee5fa74c6134ceab81c8e0ead752d4c33bdcced51d59c98`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:43:09 GMT
RUN apt-get update && apt-get install -y       gnupg
# Fri, 18 Jun 2021 04:43:10 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 18 Jun 2021 04:43:10 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 18 Jun 2021 04:45:00 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.7+b403     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 18 Jun 2021 04:45:01 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 18 Jun 2021 04:45:02 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 18 Jun 2021 04:45:02 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Fri, 18 Jun 2021 04:45:03 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Fri, 18 Jun 2021 04:45:03 GMT
WORKDIR /usr/local/zs-init
# Fri, 18 Jun 2021 04:45:09 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Fri, 18 Jun 2021 04:45:09 GMT
COPY dir:eecd98e9ebf1c61a12ae67558eb2a6ce846b9ebfadabbf08503e90b3e30d9496 in /usr/local/bin 
# Fri, 18 Jun 2021 04:45:09 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 18 Jun 2021 04:45:11 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Fri, 18 Jun 2021 04:45:11 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 18 Jun 2021 04:45:11 GMT
EXPOSE 80
# Fri, 18 Jun 2021 04:45:11 GMT
EXPOSE 443
# Fri, 18 Jun 2021 04:45:11 GMT
EXPOSE 10081
# Fri, 18 Jun 2021 04:45:11 GMT
EXPOSE 10082
# Fri, 18 Jun 2021 04:45:12 GMT
WORKDIR /var/www/html
# Fri, 18 Jun 2021 04:45:12 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536290a811a9179d6382b466707053ad0ee85c0fb032e75084cef77ac6a03136`  
		Last Modified: Fri, 18 Jun 2021 04:49:29 GMT  
		Size: 32.9 MB (32876343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747fc8577b5436cf166399a6ba5d19e8940c3764202c8b6e14479eb84bc8ede9`  
		Last Modified: Fri, 18 Jun 2021 04:49:24 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8cbfaf77c2586201e96b00b4b040910f4552f09bed5e84791616df59fc8c4c`  
		Last Modified: Fri, 18 Jun 2021 04:49:23 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e9f46d29c2ebf2c1517777123a160efeb9842e78a071c1f6d87b5221414b75`  
		Last Modified: Fri, 18 Jun 2021 04:50:19 GMT  
		Size: 418.6 MB (418613513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf92cd0f0c4d774b73a1501f73fbbb4400f0623b2152db5cb2f54c0862f8c2d1`  
		Last Modified: Fri, 18 Jun 2021 04:49:23 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cb6279aafacc20898acd75b2030b3e3a61eab4a6d8fae59fd4fd13984ea5c7`  
		Last Modified: Fri, 18 Jun 2021 04:49:23 GMT  
		Size: 18.9 KB (18932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f06b1e407a7b8c311829c2ce42dc183c1ee3b7175f32039c629b53d763ee33`  
		Last Modified: Fri, 18 Jun 2021 04:49:21 GMT  
		Size: 5.1 MB (5147620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0289167887c4a544becd84b9907e4221cdb883af4d2485a625afd94d7b2999`  
		Last Modified: Fri, 18 Jun 2021 04:49:20 GMT  
		Size: 14.3 KB (14292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c66e03a090e4d12466cc3c21b8097df1335e7bfc31d04c69c01947305f3195`  
		Last Modified: Fri, 18 Jun 2021 04:49:20 GMT  
		Size: 2.6 KB (2560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c74406ef3a8742de21a641a56a89c87b5012cdba71644e630e02026e97a392`  
		Last Modified: Fri, 18 Jun 2021 04:49:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124d7cc7602148314e697c969621883bd356d7e16e7c39f43927034fdcf5cc36`  
		Last Modified: Fri, 18 Jun 2021 04:49:20 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:2021.0`

```console
$ docker pull php-zendserver@sha256:24814f1b4cfe12e3aaa104aed181c6aee3b00148ef4492bcfdc31152f4a9dc24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:2021.0` - linux; amd64

```console
$ docker pull php-zendserver@sha256:6bbe477fe3c81def043ce3aa3e6f082d51a9983e6c906ff3c2f6201d9b230df8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.3 MB (391250990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab00502b2a986700b2fafdc89faf5444016260b4b6919501afab35ee391704b1`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:43:09 GMT
RUN apt-get update && apt-get install -y       gnupg
# Fri, 18 Jun 2021 04:43:10 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 18 Jun 2021 04:45:27 GMT
COPY file:1e70d8fd6f9643bffb703528edddba0aa02a58e95cc53e92f58a86cde29e732a in /etc/apt/sources.list.d/zend-server.list 
# Fri, 18 Jun 2021 04:46:59 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2021.0.0+b74     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 18 Jun 2021 04:47:02 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 18 Jun 2021 04:47:03 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 18 Jun 2021 04:47:03 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Fri, 18 Jun 2021 04:47:04 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Fri, 18 Jun 2021 04:47:04 GMT
WORKDIR /usr/local/zs-init
# Fri, 18 Jun 2021 04:47:09 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Fri, 18 Jun 2021 04:47:10 GMT
COPY dir:eecd98e9ebf1c61a12ae67558eb2a6ce846b9ebfadabbf08503e90b3e30d9496 in /usr/local/bin 
# Fri, 18 Jun 2021 04:47:10 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 18 Jun 2021 04:47:11 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Fri, 18 Jun 2021 04:47:11 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 18 Jun 2021 04:47:11 GMT
EXPOSE 80
# Fri, 18 Jun 2021 04:47:12 GMT
EXPOSE 443
# Fri, 18 Jun 2021 04:47:12 GMT
EXPOSE 10081
# Fri, 18 Jun 2021 04:47:12 GMT
EXPOSE 10082
# Fri, 18 Jun 2021 04:47:12 GMT
WORKDIR /var/www/html
# Fri, 18 Jun 2021 04:47:12 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536290a811a9179d6382b466707053ad0ee85c0fb032e75084cef77ac6a03136`  
		Last Modified: Fri, 18 Jun 2021 04:49:29 GMT  
		Size: 32.9 MB (32876343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747fc8577b5436cf166399a6ba5d19e8940c3764202c8b6e14479eb84bc8ede9`  
		Last Modified: Fri, 18 Jun 2021 04:49:24 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c0cfe7cb1351190c998322ca84c71f9eb02a5caa63a6e3b24c61fb8523c8a0`  
		Last Modified: Fri, 18 Jun 2021 04:50:30 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc25dfee1254c12262639d59e81f91e2b0b3357b5aa68bf962a386b138e3efc`  
		Last Modified: Fri, 18 Jun 2021 04:51:16 GMT  
		Size: 326.5 MB (326487090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8822f69ca2d8d4c45249a89e247bf0ff48acc7c880092a169eb60cff39fa6b87`  
		Last Modified: Fri, 18 Jun 2021 04:50:30 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3850592cb1b1b6d570795961d01695c39a4ad3ac4da644051b809bd234ae798`  
		Last Modified: Fri, 18 Jun 2021 04:50:30 GMT  
		Size: 18.9 KB (18929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ec9e33ded17542b8212353a810d27e82040894fec444348050495b9953e86f`  
		Last Modified: Fri, 18 Jun 2021 04:50:28 GMT  
		Size: 5.1 MB (5147556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e454f2ddb5ddfffcbd3569923b7190dc5af1d2f7662c5340bd2bddaaa563469`  
		Last Modified: Fri, 18 Jun 2021 04:50:27 GMT  
		Size: 14.3 KB (14294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8ec627b06a03993ebc4f374563b74fa1d58b527fb86684c40821dd10a892b1`  
		Last Modified: Fri, 18 Jun 2021 04:50:27 GMT  
		Size: 2.6 KB (2558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8addf7b2de152519be95a495cb7999fe6ed75077b48dbb199ea8e17f4ffd3407`  
		Last Modified: Fri, 18 Jun 2021 04:50:27 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c06ee456c1830192299e86f72813e0ea4c6dd9c48c61a25bf390826dc04a1ef`  
		Last Modified: Fri, 18 Jun 2021 04:50:27 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:5.6`

```console
$ docker pull php-zendserver@sha256:34581269a8ce4c3ec34ff8964b469af35d4ef717c97e14b83ab8927cdcba139c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:f0b2326271ad93fad4ca168a26b979d91c1107dcf8b3e9953744ce8919a754ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.6 MB (315600007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd05544332d00c484670363ddd32e665a1ad9f81271f92e2269c425daacd2b07`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 17 Jun 2021 23:32:06 GMT
ADD file:4dd75f16753c9c921fd05b1d0ed5b425d74d87405a76a0b3afcbf9723a50d1ce in / 
# Thu, 17 Jun 2021 23:32:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 17 Jun 2021 23:32:08 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 17 Jun 2021 23:32:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 17 Jun 2021 23:32:09 GMT
CMD ["/bin/bash"]
# Fri, 18 Jun 2021 04:38:41 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 18 Jun 2021 04:38:41 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 18 Jun 2021 04:38:41 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Fri, 18 Jun 2021 04:40:39 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 18 Jun 2021 04:40:39 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Fri, 18 Jun 2021 04:40:41 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Fri, 18 Jun 2021 04:40:42 GMT
RUN /usr/sbin/a2enmod headers
# Fri, 18 Jun 2021 04:40:42 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 18 Jun 2021 04:40:42 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 18 Jun 2021 04:40:44 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Fri, 18 Jun 2021 04:40:44 GMT
WORKDIR /usr/local/zs-init
# Fri, 18 Jun 2021 04:40:51 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Fri, 18 Jun 2021 04:40:51 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Fri, 18 Jun 2021 04:40:52 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 18 Jun 2021 04:40:53 GMT
RUN rm /var/www/html/index.html
# Fri, 18 Jun 2021 04:40:53 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 18 Jun 2021 04:40:53 GMT
EXPOSE 80
# Fri, 18 Jun 2021 04:40:53 GMT
EXPOSE 443
# Fri, 18 Jun 2021 04:40:54 GMT
EXPOSE 10081
# Fri, 18 Jun 2021 04:40:54 GMT
EXPOSE 10082
# Fri, 18 Jun 2021 04:40:54 GMT
WORKDIR /var/www/html
# Fri, 18 Jun 2021 04:40:54 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:61e03ba1d4149ac4eb681c6bf75aef8ac4b3f0d6fbb08e9623c4089889396fc8`  
		Last Modified: Sat, 12 Jun 2021 00:25:16 GMT  
		Size: 46.5 MB (46496785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb39f216bd4e336f9b78584bae0f6bcb77150107471d8d67d3b8abfbdea46a`  
		Last Modified: Thu, 17 Jun 2021 23:34:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e489abdc9f902f737bfef2c0c7ff5c35ca9b3ca11e73405a472f31a25f2dcc69`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999fff7bcc2450fcf1210182802f3907e35cd7cf7569568bd2a179b9144d9c57`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5631633fccf1bcda88d09d98c1c798eccd1d18d85ddb54a06237d796ce1690`  
		Last Modified: Fri, 18 Jun 2021 04:47:39 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92c8dec756784510c2d498f3b496927d90745552522721efc0df813757de8db`  
		Last Modified: Fri, 18 Jun 2021 04:47:39 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541314792bd5649f36f63eccb7a6d520bd8f8beaba8ae5fc70cc65338b2efd91`  
		Last Modified: Fri, 18 Jun 2021 04:47:39 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b999895f08e1ed0580f4fe9f62323fc993dae6b71528c38f4ee1161bfb2d8be`  
		Last Modified: Fri, 18 Jun 2021 04:48:10 GMT  
		Size: 263.9 MB (263907849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4c6cc5e8fc44d67934f7168f15577dcd1b117f6618105868f0d04da0064ea3`  
		Last Modified: Fri, 18 Jun 2021 04:47:37 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f1d944f30a9fe7657085fe9faff96a7f4736c18b0df23b518f0be01e6670bf`  
		Last Modified: Fri, 18 Jun 2021 04:47:37 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2addc2530de3e6056311524eef8379eead3bfe12683d63728d04e8d861d45c`  
		Last Modified: Fri, 18 Jun 2021 04:47:37 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff6bbf0f17ba5089bb97dcc68edd2ea55883fd34564c0dca548af218cbac698`  
		Last Modified: Fri, 18 Jun 2021 04:47:37 GMT  
		Size: 18.9 KB (18859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6393611c7131a0d96834122c2b10bfb0534efbbc4e2ac0111bfc030600011842`  
		Last Modified: Fri, 18 Jun 2021 04:47:35 GMT  
		Size: 5.1 MB (5141515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f37efab53ab1574c6e2fdbb8fd208eef416e70b6b35aa1b532f3e2d9365cdd`  
		Last Modified: Fri, 18 Jun 2021 04:47:34 GMT  
		Size: 13.4 KB (13353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2633522c25962c8843ba625614b354b6678e00d43f88492f15e01ea508f8c2de`  
		Last Modified: Fri, 18 Jun 2021 04:47:34 GMT  
		Size: 2.6 KB (2566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6825ac574ffb323514c53fd972471243a9096f77f91cd1e8e9ee82e897083012`  
		Last Modified: Fri, 18 Jun 2021 04:47:35 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9822530b0942b2794d04f98f55d60ffeba4009b2353671b601cfbdc9ebb59e43`  
		Last Modified: Fri, 18 Jun 2021 04:47:34 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5`

```console
$ docker pull php-zendserver@sha256:34581269a8ce4c3ec34ff8964b469af35d4ef717c97e14b83ab8927cdcba139c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:8.5` - linux; amd64

```console
$ docker pull php-zendserver@sha256:f0b2326271ad93fad4ca168a26b979d91c1107dcf8b3e9953744ce8919a754ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.6 MB (315600007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd05544332d00c484670363ddd32e665a1ad9f81271f92e2269c425daacd2b07`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 17 Jun 2021 23:32:06 GMT
ADD file:4dd75f16753c9c921fd05b1d0ed5b425d74d87405a76a0b3afcbf9723a50d1ce in / 
# Thu, 17 Jun 2021 23:32:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 17 Jun 2021 23:32:08 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 17 Jun 2021 23:32:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 17 Jun 2021 23:32:09 GMT
CMD ["/bin/bash"]
# Fri, 18 Jun 2021 04:38:41 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 18 Jun 2021 04:38:41 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 18 Jun 2021 04:38:41 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Fri, 18 Jun 2021 04:40:39 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 18 Jun 2021 04:40:39 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Fri, 18 Jun 2021 04:40:41 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Fri, 18 Jun 2021 04:40:42 GMT
RUN /usr/sbin/a2enmod headers
# Fri, 18 Jun 2021 04:40:42 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 18 Jun 2021 04:40:42 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 18 Jun 2021 04:40:44 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Fri, 18 Jun 2021 04:40:44 GMT
WORKDIR /usr/local/zs-init
# Fri, 18 Jun 2021 04:40:51 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Fri, 18 Jun 2021 04:40:51 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Fri, 18 Jun 2021 04:40:52 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 18 Jun 2021 04:40:53 GMT
RUN rm /var/www/html/index.html
# Fri, 18 Jun 2021 04:40:53 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 18 Jun 2021 04:40:53 GMT
EXPOSE 80
# Fri, 18 Jun 2021 04:40:53 GMT
EXPOSE 443
# Fri, 18 Jun 2021 04:40:54 GMT
EXPOSE 10081
# Fri, 18 Jun 2021 04:40:54 GMT
EXPOSE 10082
# Fri, 18 Jun 2021 04:40:54 GMT
WORKDIR /var/www/html
# Fri, 18 Jun 2021 04:40:54 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:61e03ba1d4149ac4eb681c6bf75aef8ac4b3f0d6fbb08e9623c4089889396fc8`  
		Last Modified: Sat, 12 Jun 2021 00:25:16 GMT  
		Size: 46.5 MB (46496785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb39f216bd4e336f9b78584bae0f6bcb77150107471d8d67d3b8abfbdea46a`  
		Last Modified: Thu, 17 Jun 2021 23:34:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e489abdc9f902f737bfef2c0c7ff5c35ca9b3ca11e73405a472f31a25f2dcc69`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999fff7bcc2450fcf1210182802f3907e35cd7cf7569568bd2a179b9144d9c57`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5631633fccf1bcda88d09d98c1c798eccd1d18d85ddb54a06237d796ce1690`  
		Last Modified: Fri, 18 Jun 2021 04:47:39 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92c8dec756784510c2d498f3b496927d90745552522721efc0df813757de8db`  
		Last Modified: Fri, 18 Jun 2021 04:47:39 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541314792bd5649f36f63eccb7a6d520bd8f8beaba8ae5fc70cc65338b2efd91`  
		Last Modified: Fri, 18 Jun 2021 04:47:39 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b999895f08e1ed0580f4fe9f62323fc993dae6b71528c38f4ee1161bfb2d8be`  
		Last Modified: Fri, 18 Jun 2021 04:48:10 GMT  
		Size: 263.9 MB (263907849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4c6cc5e8fc44d67934f7168f15577dcd1b117f6618105868f0d04da0064ea3`  
		Last Modified: Fri, 18 Jun 2021 04:47:37 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f1d944f30a9fe7657085fe9faff96a7f4736c18b0df23b518f0be01e6670bf`  
		Last Modified: Fri, 18 Jun 2021 04:47:37 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2addc2530de3e6056311524eef8379eead3bfe12683d63728d04e8d861d45c`  
		Last Modified: Fri, 18 Jun 2021 04:47:37 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff6bbf0f17ba5089bb97dcc68edd2ea55883fd34564c0dca548af218cbac698`  
		Last Modified: Fri, 18 Jun 2021 04:47:37 GMT  
		Size: 18.9 KB (18859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6393611c7131a0d96834122c2b10bfb0534efbbc4e2ac0111bfc030600011842`  
		Last Modified: Fri, 18 Jun 2021 04:47:35 GMT  
		Size: 5.1 MB (5141515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f37efab53ab1574c6e2fdbb8fd208eef416e70b6b35aa1b532f3e2d9365cdd`  
		Last Modified: Fri, 18 Jun 2021 04:47:34 GMT  
		Size: 13.4 KB (13353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2633522c25962c8843ba625614b354b6678e00d43f88492f15e01ea508f8c2de`  
		Last Modified: Fri, 18 Jun 2021 04:47:34 GMT  
		Size: 2.6 KB (2566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6825ac574ffb323514c53fd972471243a9096f77f91cd1e8e9ee82e897083012`  
		Last Modified: Fri, 18 Jun 2021 04:47:35 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9822530b0942b2794d04f98f55d60ffeba4009b2353671b601cfbdc9ebb59e43`  
		Last Modified: Fri, 18 Jun 2021 04:47:34 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5-php5.6`

```console
$ docker pull php-zendserver@sha256:34581269a8ce4c3ec34ff8964b469af35d4ef717c97e14b83ab8927cdcba139c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:8.5-php5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:f0b2326271ad93fad4ca168a26b979d91c1107dcf8b3e9953744ce8919a754ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.6 MB (315600007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd05544332d00c484670363ddd32e665a1ad9f81271f92e2269c425daacd2b07`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 17 Jun 2021 23:32:06 GMT
ADD file:4dd75f16753c9c921fd05b1d0ed5b425d74d87405a76a0b3afcbf9723a50d1ce in / 
# Thu, 17 Jun 2021 23:32:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 17 Jun 2021 23:32:08 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 17 Jun 2021 23:32:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 17 Jun 2021 23:32:09 GMT
CMD ["/bin/bash"]
# Fri, 18 Jun 2021 04:38:41 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 18 Jun 2021 04:38:41 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 18 Jun 2021 04:38:41 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Fri, 18 Jun 2021 04:40:39 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 18 Jun 2021 04:40:39 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Fri, 18 Jun 2021 04:40:41 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Fri, 18 Jun 2021 04:40:42 GMT
RUN /usr/sbin/a2enmod headers
# Fri, 18 Jun 2021 04:40:42 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 18 Jun 2021 04:40:42 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 18 Jun 2021 04:40:44 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Fri, 18 Jun 2021 04:40:44 GMT
WORKDIR /usr/local/zs-init
# Fri, 18 Jun 2021 04:40:51 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Fri, 18 Jun 2021 04:40:51 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Fri, 18 Jun 2021 04:40:52 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 18 Jun 2021 04:40:53 GMT
RUN rm /var/www/html/index.html
# Fri, 18 Jun 2021 04:40:53 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 18 Jun 2021 04:40:53 GMT
EXPOSE 80
# Fri, 18 Jun 2021 04:40:53 GMT
EXPOSE 443
# Fri, 18 Jun 2021 04:40:54 GMT
EXPOSE 10081
# Fri, 18 Jun 2021 04:40:54 GMT
EXPOSE 10082
# Fri, 18 Jun 2021 04:40:54 GMT
WORKDIR /var/www/html
# Fri, 18 Jun 2021 04:40:54 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:61e03ba1d4149ac4eb681c6bf75aef8ac4b3f0d6fbb08e9623c4089889396fc8`  
		Last Modified: Sat, 12 Jun 2021 00:25:16 GMT  
		Size: 46.5 MB (46496785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb39f216bd4e336f9b78584bae0f6bcb77150107471d8d67d3b8abfbdea46a`  
		Last Modified: Thu, 17 Jun 2021 23:34:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e489abdc9f902f737bfef2c0c7ff5c35ca9b3ca11e73405a472f31a25f2dcc69`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999fff7bcc2450fcf1210182802f3907e35cd7cf7569568bd2a179b9144d9c57`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5631633fccf1bcda88d09d98c1c798eccd1d18d85ddb54a06237d796ce1690`  
		Last Modified: Fri, 18 Jun 2021 04:47:39 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92c8dec756784510c2d498f3b496927d90745552522721efc0df813757de8db`  
		Last Modified: Fri, 18 Jun 2021 04:47:39 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541314792bd5649f36f63eccb7a6d520bd8f8beaba8ae5fc70cc65338b2efd91`  
		Last Modified: Fri, 18 Jun 2021 04:47:39 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b999895f08e1ed0580f4fe9f62323fc993dae6b71528c38f4ee1161bfb2d8be`  
		Last Modified: Fri, 18 Jun 2021 04:48:10 GMT  
		Size: 263.9 MB (263907849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4c6cc5e8fc44d67934f7168f15577dcd1b117f6618105868f0d04da0064ea3`  
		Last Modified: Fri, 18 Jun 2021 04:47:37 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f1d944f30a9fe7657085fe9faff96a7f4736c18b0df23b518f0be01e6670bf`  
		Last Modified: Fri, 18 Jun 2021 04:47:37 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2addc2530de3e6056311524eef8379eead3bfe12683d63728d04e8d861d45c`  
		Last Modified: Fri, 18 Jun 2021 04:47:37 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff6bbf0f17ba5089bb97dcc68edd2ea55883fd34564c0dca548af218cbac698`  
		Last Modified: Fri, 18 Jun 2021 04:47:37 GMT  
		Size: 18.9 KB (18859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6393611c7131a0d96834122c2b10bfb0534efbbc4e2ac0111bfc030600011842`  
		Last Modified: Fri, 18 Jun 2021 04:47:35 GMT  
		Size: 5.1 MB (5141515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f37efab53ab1574c6e2fdbb8fd208eef416e70b6b35aa1b532f3e2d9365cdd`  
		Last Modified: Fri, 18 Jun 2021 04:47:34 GMT  
		Size: 13.4 KB (13353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2633522c25962c8843ba625614b354b6678e00d43f88492f15e01ea508f8c2de`  
		Last Modified: Fri, 18 Jun 2021 04:47:34 GMT  
		Size: 2.6 KB (2566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6825ac574ffb323514c53fd972471243a9096f77f91cd1e8e9ee82e897083012`  
		Last Modified: Fri, 18 Jun 2021 04:47:35 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9822530b0942b2794d04f98f55d60ffeba4009b2353671b601cfbdc9ebb59e43`  
		Last Modified: Fri, 18 Jun 2021 04:47:34 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:9.1`

```console
$ docker pull php-zendserver@sha256:36a2bb19b11ff1b30ede523b8203a29b5dd23c62c0ced408380fa6f6bb8bbe25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:9.1` - linux; amd64

```console
$ docker pull php-zendserver@sha256:a03df1a3c6880a523620105f29c3e6b77051ddaa33ae539f8e8bcbf61c042a90
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.3 MB (399252621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7496ddcb4d19607a495b0e660ef9681c9a135376b12306c54cc3c8fcda12913`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 17 Jun 2021 23:32:06 GMT
ADD file:4dd75f16753c9c921fd05b1d0ed5b425d74d87405a76a0b3afcbf9723a50d1ce in / 
# Thu, 17 Jun 2021 23:32:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 17 Jun 2021 23:32:08 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 17 Jun 2021 23:32:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 17 Jun 2021 23:32:09 GMT
CMD ["/bin/bash"]
# Fri, 18 Jun 2021 04:38:41 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 18 Jun 2021 04:41:05 GMT
COPY file:0d4830b5060fb75cec6a47b30d343d82f9c3d6f95f20c11635618b93dedb5720 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 18 Jun 2021 04:42:32 GMT
RUN apt-get update     && apt-get install -y       curl       libmysqlclient20       unzip       git       zend-server-php-7.1=9.1.12+b211     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 18 Jun 2021 04:42:35 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Fri, 18 Jun 2021 04:42:36 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Fri, 18 Jun 2021 04:42:37 GMT
RUN /usr/sbin/a2enmod headers
# Fri, 18 Jun 2021 04:42:37 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 18 Jun 2021 04:42:37 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 18 Jun 2021 04:42:39 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Fri, 18 Jun 2021 04:42:39 GMT
WORKDIR /usr/local/zs-init
# Fri, 18 Jun 2021 04:42:45 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Fri, 18 Jun 2021 04:42:46 GMT
COPY dir:5966ca4828c37f68d48d11da814350a590451453f42aa83ef2eab6893db3e4cc in /usr/local/bin 
# Fri, 18 Jun 2021 04:42:46 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 18 Jun 2021 04:42:47 GMT
RUN rm /var/www/html/index.html
# Fri, 18 Jun 2021 04:42:47 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 18 Jun 2021 04:42:47 GMT
EXPOSE 80
# Fri, 18 Jun 2021 04:42:48 GMT
EXPOSE 443
# Fri, 18 Jun 2021 04:42:48 GMT
EXPOSE 10081
# Fri, 18 Jun 2021 04:42:48 GMT
EXPOSE 10082
# Fri, 18 Jun 2021 04:42:48 GMT
WORKDIR /var/www/html
# Fri, 18 Jun 2021 04:42:48 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:61e03ba1d4149ac4eb681c6bf75aef8ac4b3f0d6fbb08e9623c4089889396fc8`  
		Last Modified: Sat, 12 Jun 2021 00:25:16 GMT  
		Size: 46.5 MB (46496785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb39f216bd4e336f9b78584bae0f6bcb77150107471d8d67d3b8abfbdea46a`  
		Last Modified: Thu, 17 Jun 2021 23:34:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e489abdc9f902f737bfef2c0c7ff5c35ca9b3ca11e73405a472f31a25f2dcc69`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999fff7bcc2450fcf1210182802f3907e35cd7cf7569568bd2a179b9144d9c57`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5631633fccf1bcda88d09d98c1c798eccd1d18d85ddb54a06237d796ce1690`  
		Last Modified: Fri, 18 Jun 2021 04:47:39 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f84569a808c6595c99505dae85f57066e351d69a3a35f4bba969d129c282f6`  
		Last Modified: Fri, 18 Jun 2021 04:48:30 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4218acc5696030f9dccacbff6726914b2f1cf3984dc584c76f026374faa61ddd`  
		Last Modified: Fri, 18 Jun 2021 04:49:12 GMT  
		Size: 347.6 MB (347553623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fe5d638e440f4e9523b27973749323a6d299217e23694955da3f19b17eb55a`  
		Last Modified: Fri, 18 Jun 2021 04:48:28 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af82abb1124418bd5ea9b29e782936167940477ba08a29f53acfed7df770a5c4`  
		Last Modified: Fri, 18 Jun 2021 04:48:27 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0857bef2d0a2db371524eb9027d554141144c4a989ac337296cdd021107f442`  
		Last Modified: Fri, 18 Jun 2021 04:48:27 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ebe4de9752d0e28088e9996f419d7396bbf0522a93887c82a3611a6b3659b4`  
		Last Modified: Fri, 18 Jun 2021 04:48:27 GMT  
		Size: 18.9 KB (18861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5b42f3ef1dece17bb7bb5886066274b8c4fc3bca3d04ff5a780a21eac3ef9f`  
		Last Modified: Fri, 18 Jun 2021 04:48:26 GMT  
		Size: 5.1 MB (5147652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01fb5bf891760dc11e1a8994a4b6d339b9a44e5993ea2b955721a9d9d2a9b70`  
		Last Modified: Fri, 18 Jun 2021 04:48:25 GMT  
		Size: 14.3 KB (14320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0f509e636b9781550a6ba0b9fcd9318e1e6286924f59851d27979ff695da51`  
		Last Modified: Fri, 18 Jun 2021 04:48:25 GMT  
		Size: 2.6 KB (2563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50723b75d1d964d3580ae731f0ed2620fead8ea5decc5ced0e5d2cca678b1a1f`  
		Last Modified: Fri, 18 Jun 2021 04:48:25 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972efbfcac80f9afc7304542510a9753a9f0a8099c4a4f8be1c14c426eec48c4`  
		Last Modified: Fri, 18 Jun 2021 04:48:25 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:latest`

```console
$ docker pull php-zendserver@sha256:24814f1b4cfe12e3aaa104aed181c6aee3b00148ef4492bcfdc31152f4a9dc24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:latest` - linux; amd64

```console
$ docker pull php-zendserver@sha256:6bbe477fe3c81def043ce3aa3e6f082d51a9983e6c906ff3c2f6201d9b230df8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.3 MB (391250990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab00502b2a986700b2fafdc89faf5444016260b4b6919501afab35ee391704b1`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 04:43:09 GMT
RUN apt-get update && apt-get install -y       gnupg
# Fri, 18 Jun 2021 04:43:10 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 18 Jun 2021 04:45:27 GMT
COPY file:1e70d8fd6f9643bffb703528edddba0aa02a58e95cc53e92f58a86cde29e732a in /etc/apt/sources.list.d/zend-server.list 
# Fri, 18 Jun 2021 04:46:59 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2021.0.0+b74     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 18 Jun 2021 04:47:02 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 18 Jun 2021 04:47:03 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 18 Jun 2021 04:47:03 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Fri, 18 Jun 2021 04:47:04 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Fri, 18 Jun 2021 04:47:04 GMT
WORKDIR /usr/local/zs-init
# Fri, 18 Jun 2021 04:47:09 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Fri, 18 Jun 2021 04:47:10 GMT
COPY dir:eecd98e9ebf1c61a12ae67558eb2a6ce846b9ebfadabbf08503e90b3e30d9496 in /usr/local/bin 
# Fri, 18 Jun 2021 04:47:10 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 18 Jun 2021 04:47:11 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Fri, 18 Jun 2021 04:47:11 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 18 Jun 2021 04:47:11 GMT
EXPOSE 80
# Fri, 18 Jun 2021 04:47:12 GMT
EXPOSE 443
# Fri, 18 Jun 2021 04:47:12 GMT
EXPOSE 10081
# Fri, 18 Jun 2021 04:47:12 GMT
EXPOSE 10082
# Fri, 18 Jun 2021 04:47:12 GMT
WORKDIR /var/www/html
# Fri, 18 Jun 2021 04:47:12 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536290a811a9179d6382b466707053ad0ee85c0fb032e75084cef77ac6a03136`  
		Last Modified: Fri, 18 Jun 2021 04:49:29 GMT  
		Size: 32.9 MB (32876343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747fc8577b5436cf166399a6ba5d19e8940c3764202c8b6e14479eb84bc8ede9`  
		Last Modified: Fri, 18 Jun 2021 04:49:24 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c0cfe7cb1351190c998322ca84c71f9eb02a5caa63a6e3b24c61fb8523c8a0`  
		Last Modified: Fri, 18 Jun 2021 04:50:30 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc25dfee1254c12262639d59e81f91e2b0b3357b5aa68bf962a386b138e3efc`  
		Last Modified: Fri, 18 Jun 2021 04:51:16 GMT  
		Size: 326.5 MB (326487090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8822f69ca2d8d4c45249a89e247bf0ff48acc7c880092a169eb60cff39fa6b87`  
		Last Modified: Fri, 18 Jun 2021 04:50:30 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3850592cb1b1b6d570795961d01695c39a4ad3ac4da644051b809bd234ae798`  
		Last Modified: Fri, 18 Jun 2021 04:50:30 GMT  
		Size: 18.9 KB (18929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ec9e33ded17542b8212353a810d27e82040894fec444348050495b9953e86f`  
		Last Modified: Fri, 18 Jun 2021 04:50:28 GMT  
		Size: 5.1 MB (5147556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e454f2ddb5ddfffcbd3569923b7190dc5af1d2f7662c5340bd2bddaaa563469`  
		Last Modified: Fri, 18 Jun 2021 04:50:27 GMT  
		Size: 14.3 KB (14294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8ec627b06a03993ebc4f374563b74fa1d58b527fb86684c40821dd10a892b1`  
		Last Modified: Fri, 18 Jun 2021 04:50:27 GMT  
		Size: 2.6 KB (2558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8addf7b2de152519be95a495cb7999fe6ed75077b48dbb199ea8e17f4ffd3407`  
		Last Modified: Fri, 18 Jun 2021 04:50:27 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c06ee456c1830192299e86f72813e0ea4c6dd9c48c61a25bf390826dc04a1ef`  
		Last Modified: Fri, 18 Jun 2021 04:50:27 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
