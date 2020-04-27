<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `php-zendserver`

-	[`php-zendserver:2019.0`](#php-zendserver20190)
-	[`php-zendserver:5.6`](#php-zendserver56)
-	[`php-zendserver:8.5`](#php-zendserver85)
-	[`php-zendserver:8.5-php5.6`](#php-zendserver85-php56)
-	[`php-zendserver:9.1`](#php-zendserver91)
-	[`php-zendserver:latest`](#php-zendserverlatest)

## `php-zendserver:2019.0`

```console
$ docker pull php-zendserver@sha256:269b654cb2bb78c59b6e104312eb1ca897a8c0e9b0743fdcbe592174d25210ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:2019.0` - linux; amd64

```console
$ docker pull php-zendserver@sha256:56543b0e9457391ddd5e60fe7ed47da4e54f0fd20f9d6676134bb0f349eac0a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.7 MB (491680761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8ae27d8795553ad9d6933f8b9d45ab9bcf97adcf7724ae3f19ffb52872458a`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Mon, 27 Apr 2020 21:23:02 GMT
RUN apt-get update && apt-get install -y       gnupg
# Mon, 27 Apr 2020 21:23:03 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Mon, 27 Apr 2020 21:23:03 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Mon, 27 Apr 2020 21:24:55 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.4+b392     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Mon, 27 Apr 2020 21:24:56 GMT
ENV ZS_INIT_VERSION=0.3
# Mon, 27 Apr 2020 21:24:56 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Mon, 27 Apr 2020 21:24:56 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Mon, 27 Apr 2020 21:24:57 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Mon, 27 Apr 2020 21:24:57 GMT
WORKDIR /usr/local/zs-init
# Mon, 27 Apr 2020 21:25:09 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Mon, 27 Apr 2020 21:25:09 GMT
COPY dir:7937a6223a1e7805720eca1fbf8c2ccd37938f8f8aa175ae003d409459d49380 in /usr/local/bin 
# Mon, 27 Apr 2020 21:25:09 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Mon, 27 Apr 2020 21:25:10 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Mon, 27 Apr 2020 21:25:10 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Mon, 27 Apr 2020 21:25:10 GMT
EXPOSE 80
# Mon, 27 Apr 2020 21:25:10 GMT
EXPOSE 443
# Mon, 27 Apr 2020 21:25:11 GMT
EXPOSE 10081
# Mon, 27 Apr 2020 21:25:11 GMT
EXPOSE 10082
# Mon, 27 Apr 2020 21:25:11 GMT
WORKDIR /var/www/html
# Mon, 27 Apr 2020 21:25:11 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3952dd9aa51ff9fd5afeadc57b89c1060b1e262773cb329e4d0c685930ef1d8`  
		Last Modified: Mon, 27 Apr 2020 21:26:32 GMT  
		Size: 27.7 MB (27657988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8d12d6d4dd3e2321d60ac32b12fae135dafe46386d9e35507f90bb05173113`  
		Last Modified: Mon, 27 Apr 2020 21:26:28 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5f32558834cbc4c686a14320d1ddfeae948f5dd7848bd4f1e3bde8889db363`  
		Last Modified: Mon, 27 Apr 2020 21:26:28 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a820d7b6724d1fd02914dac90a2f6e97cfea783a25536371f8145c76d2a744bb`  
		Last Modified: Mon, 27 Apr 2020 21:27:31 GMT  
		Size: 418.1 MB (418143562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9807ddc4ba33dd4012911627d2e6c9a5c0f02d697141b223cf1ea780b93c93a4`  
		Last Modified: Mon, 27 Apr 2020 21:26:27 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a8c68e82a4284424683b15827233325989cdfd3fdfdcebf9dba1ad0926b5a5`  
		Last Modified: Mon, 27 Apr 2020 21:26:26 GMT  
		Size: 18.9 KB (18906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f664bca6bedcc3f68abf3d2ca9675430dd4b5a03dcccb687273adeb44fdf5bb`  
		Last Modified: Mon, 27 Apr 2020 21:26:29 GMT  
		Size: 19.1 MB (19113833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6e4afddff59d64e7e4b57081aa07659b39ab22be776660f54a57730c2396f9`  
		Last Modified: Mon, 27 Apr 2020 21:26:26 GMT  
		Size: 14.3 KB (14254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef99e88063a193b5b91602a6e133015c99440c089ec68f66c9907a8f50bcf7c`  
		Last Modified: Mon, 27 Apr 2020 21:26:25 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91cc7b65386d6b3d39b02172fe792ee88ed1ef49c6319cf4fac6e53dc0affba`  
		Last Modified: Mon, 27 Apr 2020 21:26:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213db83567d1c040ed376ca5e00d2028de6638db6363a86cee33284c4144fadc`  
		Last Modified: Mon, 27 Apr 2020 21:26:26 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:5.6`

```console
$ docker pull php-zendserver@sha256:54cd776411228279007a85441fbc2846cb2573a1bbde42b6c97bf128381afbfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:a917123c23944494f755e756fd4d4eed7de91a31a49cfa553535d199a89e5fac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.3 MB (327331226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a089d0ebb7632c6816f65be5720fa2f41e00ca43e66eb85074b45a28c045b29`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 24 Apr 2020 01:08:29 GMT
ADD file:4fe14d9555e739e4d006eecb273a2f4a53e6dbe93bd0db26d5f999168b5d4114 in / 
# Fri, 24 Apr 2020 01:08:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 01:08:33 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:08:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:08:35 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:36:11 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Mon, 27 Apr 2020 21:20:04 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Mon, 27 Apr 2020 21:20:04 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Mon, 27 Apr 2020 21:21:54 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.15+b8     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Mon, 27 Apr 2020 21:21:55 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Mon, 27 Apr 2020 21:21:56 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Mon, 27 Apr 2020 21:21:57 GMT
RUN /usr/sbin/a2enmod headers
# Mon, 27 Apr 2020 21:21:57 GMT
ENV ZS_INIT_VERSION=0.3
# Mon, 27 Apr 2020 21:21:57 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Mon, 27 Apr 2020 21:21:58 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Mon, 27 Apr 2020 21:21:58 GMT
WORKDIR /usr/local/zs-init
# Mon, 27 Apr 2020 21:22:11 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Mon, 27 Apr 2020 21:22:11 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Mon, 27 Apr 2020 21:22:12 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Mon, 27 Apr 2020 21:22:12 GMT
RUN rm /var/www/html/index.html
# Mon, 27 Apr 2020 21:22:13 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Mon, 27 Apr 2020 21:22:13 GMT
EXPOSE 80
# Mon, 27 Apr 2020 21:22:13 GMT
EXPOSE 443
# Mon, 27 Apr 2020 21:22:13 GMT
EXPOSE 10081
# Mon, 27 Apr 2020 21:22:13 GMT
EXPOSE 10082
# Mon, 27 Apr 2020 21:22:13 GMT
WORKDIR /var/www/html
# Mon, 27 Apr 2020 21:22:14 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:e92ed755c008afc1863a616a5ba743b670c09c1698f7328f05591932452a425f`  
		Last Modified: Fri, 27 Mar 2020 14:20:10 GMT  
		Size: 44.2 MB (44247132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fd7cb1ff8f489cf082781b0e1fe0c13b840e20147e8fc8204b4592da7c2f70`  
		Last Modified: Fri, 24 Apr 2020 01:09:44 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee690f2d57a128744cf4c5b52646ad0ba7a5af113d9d7e0e02b62c06d35fd14c`  
		Last Modified: Fri, 24 Apr 2020 01:09:45 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e3366ec435596bed2563cc882ba47ec25df6be2b1027e3243e83589c667c1e`  
		Last Modified: Fri, 24 Apr 2020 01:09:44 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dd6efaf2106877d2c05041b9f5e7fe7da7805d9d6a416a1f30d6758d387463`  
		Last Modified: Fri, 24 Apr 2020 20:38:38 GMT  
		Size: 13.1 KB (13062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ab3c61b2ae66b0a77beb7728cfeac866016e8f7eed3402dc985ff3328c2939`  
		Last Modified: Mon, 27 Apr 2020 21:25:28 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e15b74f42f58fcffd09e83c52054b725999ec57caa862cc26387653b5c4267`  
		Last Modified: Mon, 27 Apr 2020 21:25:28 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe096b83c86f6b4209fec3155bc5303d823c0bab999341939da9b0c2ba272e9`  
		Last Modified: Mon, 27 Apr 2020 21:26:14 GMT  
		Size: 263.9 MB (263927241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94164b844039f921cb5f03e365bf2bd4cecf607e9f74de15979520cb23b5c01c`  
		Last Modified: Mon, 27 Apr 2020 21:25:27 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46522a3259ea373f4e69c0325ddafb1259165e2264ab71b6812666dec03d2c8`  
		Last Modified: Mon, 27 Apr 2020 21:25:26 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36269951a1e05bf0e3530fe8cf12c433b136df8bff0ac1e742f9cf977bb3a1f3`  
		Last Modified: Mon, 27 Apr 2020 21:25:26 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce33929c4ea67e272d1cda0108a80d67cba21ec93e6032996b18d075d41ce50`  
		Last Modified: Mon, 27 Apr 2020 21:25:27 GMT  
		Size: 18.8 KB (18832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295ff30ae8182cef8c303e8f26a0895ec360f7378db59f981d039a9bf7df869b`  
		Last Modified: Mon, 27 Apr 2020 21:25:28 GMT  
		Size: 19.1 MB (19104690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898028059b23ae6991464212b6f151bfe2ca01ddefbd5231988cb1d3bdd3f516`  
		Last Modified: Mon, 27 Apr 2020 21:25:24 GMT  
		Size: 13.4 KB (13355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaef7a6b6ddee9ffa90c10046d52da3801cf8070ce9fb1eee4ef4d70a19bf3b`  
		Last Modified: Mon, 27 Apr 2020 21:25:25 GMT  
		Size: 2.5 KB (2539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf3dc5b176472e9466b5e11814612c5c67b56e8086629fa6a8e73447ae2b53b`  
		Last Modified: Mon, 27 Apr 2020 21:25:25 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e671c4a466a1938e5f8ad6751903d360179bb0b0c627e451b358ec7e44919fc3`  
		Last Modified: Mon, 27 Apr 2020 21:25:25 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5`

```console
$ docker pull php-zendserver@sha256:54cd776411228279007a85441fbc2846cb2573a1bbde42b6c97bf128381afbfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:8.5` - linux; amd64

```console
$ docker pull php-zendserver@sha256:a917123c23944494f755e756fd4d4eed7de91a31a49cfa553535d199a89e5fac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.3 MB (327331226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a089d0ebb7632c6816f65be5720fa2f41e00ca43e66eb85074b45a28c045b29`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 24 Apr 2020 01:08:29 GMT
ADD file:4fe14d9555e739e4d006eecb273a2f4a53e6dbe93bd0db26d5f999168b5d4114 in / 
# Fri, 24 Apr 2020 01:08:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 01:08:33 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:08:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:08:35 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:36:11 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Mon, 27 Apr 2020 21:20:04 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Mon, 27 Apr 2020 21:20:04 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Mon, 27 Apr 2020 21:21:54 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.15+b8     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Mon, 27 Apr 2020 21:21:55 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Mon, 27 Apr 2020 21:21:56 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Mon, 27 Apr 2020 21:21:57 GMT
RUN /usr/sbin/a2enmod headers
# Mon, 27 Apr 2020 21:21:57 GMT
ENV ZS_INIT_VERSION=0.3
# Mon, 27 Apr 2020 21:21:57 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Mon, 27 Apr 2020 21:21:58 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Mon, 27 Apr 2020 21:21:58 GMT
WORKDIR /usr/local/zs-init
# Mon, 27 Apr 2020 21:22:11 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Mon, 27 Apr 2020 21:22:11 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Mon, 27 Apr 2020 21:22:12 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Mon, 27 Apr 2020 21:22:12 GMT
RUN rm /var/www/html/index.html
# Mon, 27 Apr 2020 21:22:13 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Mon, 27 Apr 2020 21:22:13 GMT
EXPOSE 80
# Mon, 27 Apr 2020 21:22:13 GMT
EXPOSE 443
# Mon, 27 Apr 2020 21:22:13 GMT
EXPOSE 10081
# Mon, 27 Apr 2020 21:22:13 GMT
EXPOSE 10082
# Mon, 27 Apr 2020 21:22:13 GMT
WORKDIR /var/www/html
# Mon, 27 Apr 2020 21:22:14 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:e92ed755c008afc1863a616a5ba743b670c09c1698f7328f05591932452a425f`  
		Last Modified: Fri, 27 Mar 2020 14:20:10 GMT  
		Size: 44.2 MB (44247132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fd7cb1ff8f489cf082781b0e1fe0c13b840e20147e8fc8204b4592da7c2f70`  
		Last Modified: Fri, 24 Apr 2020 01:09:44 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee690f2d57a128744cf4c5b52646ad0ba7a5af113d9d7e0e02b62c06d35fd14c`  
		Last Modified: Fri, 24 Apr 2020 01:09:45 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e3366ec435596bed2563cc882ba47ec25df6be2b1027e3243e83589c667c1e`  
		Last Modified: Fri, 24 Apr 2020 01:09:44 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dd6efaf2106877d2c05041b9f5e7fe7da7805d9d6a416a1f30d6758d387463`  
		Last Modified: Fri, 24 Apr 2020 20:38:38 GMT  
		Size: 13.1 KB (13062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ab3c61b2ae66b0a77beb7728cfeac866016e8f7eed3402dc985ff3328c2939`  
		Last Modified: Mon, 27 Apr 2020 21:25:28 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e15b74f42f58fcffd09e83c52054b725999ec57caa862cc26387653b5c4267`  
		Last Modified: Mon, 27 Apr 2020 21:25:28 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe096b83c86f6b4209fec3155bc5303d823c0bab999341939da9b0c2ba272e9`  
		Last Modified: Mon, 27 Apr 2020 21:26:14 GMT  
		Size: 263.9 MB (263927241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94164b844039f921cb5f03e365bf2bd4cecf607e9f74de15979520cb23b5c01c`  
		Last Modified: Mon, 27 Apr 2020 21:25:27 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46522a3259ea373f4e69c0325ddafb1259165e2264ab71b6812666dec03d2c8`  
		Last Modified: Mon, 27 Apr 2020 21:25:26 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36269951a1e05bf0e3530fe8cf12c433b136df8bff0ac1e742f9cf977bb3a1f3`  
		Last Modified: Mon, 27 Apr 2020 21:25:26 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce33929c4ea67e272d1cda0108a80d67cba21ec93e6032996b18d075d41ce50`  
		Last Modified: Mon, 27 Apr 2020 21:25:27 GMT  
		Size: 18.8 KB (18832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295ff30ae8182cef8c303e8f26a0895ec360f7378db59f981d039a9bf7df869b`  
		Last Modified: Mon, 27 Apr 2020 21:25:28 GMT  
		Size: 19.1 MB (19104690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898028059b23ae6991464212b6f151bfe2ca01ddefbd5231988cb1d3bdd3f516`  
		Last Modified: Mon, 27 Apr 2020 21:25:24 GMT  
		Size: 13.4 KB (13355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaef7a6b6ddee9ffa90c10046d52da3801cf8070ce9fb1eee4ef4d70a19bf3b`  
		Last Modified: Mon, 27 Apr 2020 21:25:25 GMT  
		Size: 2.5 KB (2539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf3dc5b176472e9466b5e11814612c5c67b56e8086629fa6a8e73447ae2b53b`  
		Last Modified: Mon, 27 Apr 2020 21:25:25 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e671c4a466a1938e5f8ad6751903d360179bb0b0c627e451b358ec7e44919fc3`  
		Last Modified: Mon, 27 Apr 2020 21:25:25 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5-php5.6`

```console
$ docker pull php-zendserver@sha256:54cd776411228279007a85441fbc2846cb2573a1bbde42b6c97bf128381afbfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:8.5-php5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:a917123c23944494f755e756fd4d4eed7de91a31a49cfa553535d199a89e5fac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.3 MB (327331226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a089d0ebb7632c6816f65be5720fa2f41e00ca43e66eb85074b45a28c045b29`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 24 Apr 2020 01:08:29 GMT
ADD file:4fe14d9555e739e4d006eecb273a2f4a53e6dbe93bd0db26d5f999168b5d4114 in / 
# Fri, 24 Apr 2020 01:08:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 01:08:33 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:08:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:08:35 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:36:11 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Mon, 27 Apr 2020 21:20:04 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Mon, 27 Apr 2020 21:20:04 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Mon, 27 Apr 2020 21:21:54 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.15+b8     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Mon, 27 Apr 2020 21:21:55 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Mon, 27 Apr 2020 21:21:56 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Mon, 27 Apr 2020 21:21:57 GMT
RUN /usr/sbin/a2enmod headers
# Mon, 27 Apr 2020 21:21:57 GMT
ENV ZS_INIT_VERSION=0.3
# Mon, 27 Apr 2020 21:21:57 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Mon, 27 Apr 2020 21:21:58 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Mon, 27 Apr 2020 21:21:58 GMT
WORKDIR /usr/local/zs-init
# Mon, 27 Apr 2020 21:22:11 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Mon, 27 Apr 2020 21:22:11 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Mon, 27 Apr 2020 21:22:12 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Mon, 27 Apr 2020 21:22:12 GMT
RUN rm /var/www/html/index.html
# Mon, 27 Apr 2020 21:22:13 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Mon, 27 Apr 2020 21:22:13 GMT
EXPOSE 80
# Mon, 27 Apr 2020 21:22:13 GMT
EXPOSE 443
# Mon, 27 Apr 2020 21:22:13 GMT
EXPOSE 10081
# Mon, 27 Apr 2020 21:22:13 GMT
EXPOSE 10082
# Mon, 27 Apr 2020 21:22:13 GMT
WORKDIR /var/www/html
# Mon, 27 Apr 2020 21:22:14 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:e92ed755c008afc1863a616a5ba743b670c09c1698f7328f05591932452a425f`  
		Last Modified: Fri, 27 Mar 2020 14:20:10 GMT  
		Size: 44.2 MB (44247132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fd7cb1ff8f489cf082781b0e1fe0c13b840e20147e8fc8204b4592da7c2f70`  
		Last Modified: Fri, 24 Apr 2020 01:09:44 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee690f2d57a128744cf4c5b52646ad0ba7a5af113d9d7e0e02b62c06d35fd14c`  
		Last Modified: Fri, 24 Apr 2020 01:09:45 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e3366ec435596bed2563cc882ba47ec25df6be2b1027e3243e83589c667c1e`  
		Last Modified: Fri, 24 Apr 2020 01:09:44 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dd6efaf2106877d2c05041b9f5e7fe7da7805d9d6a416a1f30d6758d387463`  
		Last Modified: Fri, 24 Apr 2020 20:38:38 GMT  
		Size: 13.1 KB (13062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ab3c61b2ae66b0a77beb7728cfeac866016e8f7eed3402dc985ff3328c2939`  
		Last Modified: Mon, 27 Apr 2020 21:25:28 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e15b74f42f58fcffd09e83c52054b725999ec57caa862cc26387653b5c4267`  
		Last Modified: Mon, 27 Apr 2020 21:25:28 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe096b83c86f6b4209fec3155bc5303d823c0bab999341939da9b0c2ba272e9`  
		Last Modified: Mon, 27 Apr 2020 21:26:14 GMT  
		Size: 263.9 MB (263927241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94164b844039f921cb5f03e365bf2bd4cecf607e9f74de15979520cb23b5c01c`  
		Last Modified: Mon, 27 Apr 2020 21:25:27 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46522a3259ea373f4e69c0325ddafb1259165e2264ab71b6812666dec03d2c8`  
		Last Modified: Mon, 27 Apr 2020 21:25:26 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36269951a1e05bf0e3530fe8cf12c433b136df8bff0ac1e742f9cf977bb3a1f3`  
		Last Modified: Mon, 27 Apr 2020 21:25:26 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce33929c4ea67e272d1cda0108a80d67cba21ec93e6032996b18d075d41ce50`  
		Last Modified: Mon, 27 Apr 2020 21:25:27 GMT  
		Size: 18.8 KB (18832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295ff30ae8182cef8c303e8f26a0895ec360f7378db59f981d039a9bf7df869b`  
		Last Modified: Mon, 27 Apr 2020 21:25:28 GMT  
		Size: 19.1 MB (19104690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898028059b23ae6991464212b6f151bfe2ca01ddefbd5231988cb1d3bdd3f516`  
		Last Modified: Mon, 27 Apr 2020 21:25:24 GMT  
		Size: 13.4 KB (13355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaef7a6b6ddee9ffa90c10046d52da3801cf8070ce9fb1eee4ef4d70a19bf3b`  
		Last Modified: Mon, 27 Apr 2020 21:25:25 GMT  
		Size: 2.5 KB (2539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf3dc5b176472e9466b5e11814612c5c67b56e8086629fa6a8e73447ae2b53b`  
		Last Modified: Mon, 27 Apr 2020 21:25:25 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e671c4a466a1938e5f8ad6751903d360179bb0b0c627e451b358ec7e44919fc3`  
		Last Modified: Mon, 27 Apr 2020 21:25:25 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:9.1`

```console
$ docker pull php-zendserver@sha256:e14edc569be4e9ae1301298a1d5b546d8ff13906d3534fe8d72066a194ed38d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:9.1` - linux; amd64

```console
$ docker pull php-zendserver@sha256:82b9a654feda4295273929383f6453cf905b0e3baafe0db2f4db727b8a620162
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.5 MB (407529048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8651333b9d2ecf0a2e0ea5c2daeed601c8b29fb476572255b9821604698ec4`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 24 Apr 2020 01:08:29 GMT
ADD file:4fe14d9555e739e4d006eecb273a2f4a53e6dbe93bd0db26d5f999168b5d4114 in / 
# Fri, 24 Apr 2020 01:08:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 01:08:33 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:08:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:08:35 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:36:11 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 24 Apr 2020 20:36:11 GMT
COPY file:0d4830b5060fb75cec6a47b30d343d82f9c3d6f95f20c11635618b93dedb5720 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 24 Apr 2020 20:37:43 GMT
RUN apt-get update     && apt-get install -y       curl       libmysqlclient20       unzip       git       zend-server-php-7.1=9.1.10+b202     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Mon, 27 Apr 2020 21:22:20 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Mon, 27 Apr 2020 21:22:24 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Mon, 27 Apr 2020 21:22:26 GMT
RUN /usr/sbin/a2enmod headers
# Mon, 27 Apr 2020 21:22:26 GMT
ENV ZS_INIT_VERSION=0.3
# Mon, 27 Apr 2020 21:22:26 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Mon, 27 Apr 2020 21:22:27 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Mon, 27 Apr 2020 21:22:27 GMT
WORKDIR /usr/local/zs-init
# Mon, 27 Apr 2020 21:22:40 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Mon, 27 Apr 2020 21:22:40 GMT
COPY dir:864637d3fa0817ce3be0c7e34e1298851fa2ea4cfb86583e2ec811f00c6a95fd in /usr/local/bin 
# Mon, 27 Apr 2020 21:22:40 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Mon, 27 Apr 2020 21:22:41 GMT
RUN rm /var/www/html/index.html
# Mon, 27 Apr 2020 21:22:41 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Mon, 27 Apr 2020 21:22:42 GMT
EXPOSE 80
# Mon, 27 Apr 2020 21:22:42 GMT
EXPOSE 443
# Mon, 27 Apr 2020 21:22:42 GMT
EXPOSE 10081
# Mon, 27 Apr 2020 21:22:42 GMT
EXPOSE 10082
# Mon, 27 Apr 2020 21:22:42 GMT
WORKDIR /var/www/html
# Mon, 27 Apr 2020 21:22:42 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:e92ed755c008afc1863a616a5ba743b670c09c1698f7328f05591932452a425f`  
		Last Modified: Fri, 27 Mar 2020 14:20:10 GMT  
		Size: 44.2 MB (44247132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fd7cb1ff8f489cf082781b0e1fe0c13b840e20147e8fc8204b4592da7c2f70`  
		Last Modified: Fri, 24 Apr 2020 01:09:44 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee690f2d57a128744cf4c5b52646ad0ba7a5af113d9d7e0e02b62c06d35fd14c`  
		Last Modified: Fri, 24 Apr 2020 01:09:45 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e3366ec435596bed2563cc882ba47ec25df6be2b1027e3243e83589c667c1e`  
		Last Modified: Fri, 24 Apr 2020 01:09:44 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dd6efaf2106877d2c05041b9f5e7fe7da7805d9d6a416a1f30d6758d387463`  
		Last Modified: Fri, 24 Apr 2020 20:38:38 GMT  
		Size: 13.1 KB (13062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77646021918b7f46ddfe78991a6d14d2e5477d25d4325bfe689f56a3756c10c4`  
		Last Modified: Fri, 24 Apr 2020 20:38:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3017c8a79c77d56bebc576d9f08bd9a38a5380210344a302f6e4b3b3ee2b3bd`  
		Last Modified: Fri, 24 Apr 2020 20:39:43 GMT  
		Size: 344.1 MB (344115440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd24aaaaaff6be2a76b1b250a041494ea0f3a0b902127dbf4fa08693a160a7c`  
		Last Modified: Mon, 27 Apr 2020 21:26:20 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0a07eb9ec77426fe0e452bb56e5f88698bd44da93bcf087073d7591eb8ce88`  
		Last Modified: Mon, 27 Apr 2020 21:26:21 GMT  
		Size: 321.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c79842827c1ea4bd9f65730bac719f6ca39e28003ca961f101ec5683a20b73`  
		Last Modified: Mon, 27 Apr 2020 21:26:20 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce6b84e24796ad96911e75741076e916b17daca8b9ee1ad94f1b31c7c982e1a`  
		Last Modified: Mon, 27 Apr 2020 21:26:20 GMT  
		Size: 18.8 KB (18835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c1d85332751986b4c65cea4a82a5b9231121de5e53fa26c8298982c6df88df`  
		Last Modified: Mon, 27 Apr 2020 21:26:22 GMT  
		Size: 19.1 MB (19113639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728b26ba5b8e5dc06b2321b4d3724828f72b20ca72f01531a56e1e1364c2704d`  
		Last Modified: Mon, 27 Apr 2020 21:26:19 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ee5629adcc402a130be5fc6baef8616485a1dcfdd47148397cb1637cf92987`  
		Last Modified: Mon, 27 Apr 2020 21:26:19 GMT  
		Size: 2.5 KB (2539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e91946a2571fc639f3ed14297bdca618769d19098818a4be9a035165b16fa33`  
		Last Modified: Mon, 27 Apr 2020 21:26:19 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823d571bad067323682b8f9133bdc3b8df573799666df8eedef7dcf3001cd159`  
		Last Modified: Mon, 27 Apr 2020 21:26:19 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:latest`

```console
$ docker pull php-zendserver@sha256:269b654cb2bb78c59b6e104312eb1ca897a8c0e9b0743fdcbe592174d25210ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:latest` - linux; amd64

```console
$ docker pull php-zendserver@sha256:56543b0e9457391ddd5e60fe7ed47da4e54f0fd20f9d6676134bb0f349eac0a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.7 MB (491680761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8ae27d8795553ad9d6933f8b9d45ab9bcf97adcf7724ae3f19ffb52872458a`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Mon, 27 Apr 2020 21:23:02 GMT
RUN apt-get update && apt-get install -y       gnupg
# Mon, 27 Apr 2020 21:23:03 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Mon, 27 Apr 2020 21:23:03 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Mon, 27 Apr 2020 21:24:55 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.4+b392     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Mon, 27 Apr 2020 21:24:56 GMT
ENV ZS_INIT_VERSION=0.3
# Mon, 27 Apr 2020 21:24:56 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Mon, 27 Apr 2020 21:24:56 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Mon, 27 Apr 2020 21:24:57 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Mon, 27 Apr 2020 21:24:57 GMT
WORKDIR /usr/local/zs-init
# Mon, 27 Apr 2020 21:25:09 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Mon, 27 Apr 2020 21:25:09 GMT
COPY dir:7937a6223a1e7805720eca1fbf8c2ccd37938f8f8aa175ae003d409459d49380 in /usr/local/bin 
# Mon, 27 Apr 2020 21:25:09 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Mon, 27 Apr 2020 21:25:10 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Mon, 27 Apr 2020 21:25:10 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Mon, 27 Apr 2020 21:25:10 GMT
EXPOSE 80
# Mon, 27 Apr 2020 21:25:10 GMT
EXPOSE 443
# Mon, 27 Apr 2020 21:25:11 GMT
EXPOSE 10081
# Mon, 27 Apr 2020 21:25:11 GMT
EXPOSE 10082
# Mon, 27 Apr 2020 21:25:11 GMT
WORKDIR /var/www/html
# Mon, 27 Apr 2020 21:25:11 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3952dd9aa51ff9fd5afeadc57b89c1060b1e262773cb329e4d0c685930ef1d8`  
		Last Modified: Mon, 27 Apr 2020 21:26:32 GMT  
		Size: 27.7 MB (27657988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8d12d6d4dd3e2321d60ac32b12fae135dafe46386d9e35507f90bb05173113`  
		Last Modified: Mon, 27 Apr 2020 21:26:28 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5f32558834cbc4c686a14320d1ddfeae948f5dd7848bd4f1e3bde8889db363`  
		Last Modified: Mon, 27 Apr 2020 21:26:28 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a820d7b6724d1fd02914dac90a2f6e97cfea783a25536371f8145c76d2a744bb`  
		Last Modified: Mon, 27 Apr 2020 21:27:31 GMT  
		Size: 418.1 MB (418143562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9807ddc4ba33dd4012911627d2e6c9a5c0f02d697141b223cf1ea780b93c93a4`  
		Last Modified: Mon, 27 Apr 2020 21:26:27 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a8c68e82a4284424683b15827233325989cdfd3fdfdcebf9dba1ad0926b5a5`  
		Last Modified: Mon, 27 Apr 2020 21:26:26 GMT  
		Size: 18.9 KB (18906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f664bca6bedcc3f68abf3d2ca9675430dd4b5a03dcccb687273adeb44fdf5bb`  
		Last Modified: Mon, 27 Apr 2020 21:26:29 GMT  
		Size: 19.1 MB (19113833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6e4afddff59d64e7e4b57081aa07659b39ab22be776660f54a57730c2396f9`  
		Last Modified: Mon, 27 Apr 2020 21:26:26 GMT  
		Size: 14.3 KB (14254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef99e88063a193b5b91602a6e133015c99440c089ec68f66c9907a8f50bcf7c`  
		Last Modified: Mon, 27 Apr 2020 21:26:25 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91cc7b65386d6b3d39b02172fe792ee88ed1ef49c6319cf4fac6e53dc0affba`  
		Last Modified: Mon, 27 Apr 2020 21:26:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213db83567d1c040ed376ca5e00d2028de6638db6363a86cee33284c4144fadc`  
		Last Modified: Mon, 27 Apr 2020 21:26:26 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
