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
$ docker pull php-zendserver@sha256:10a5b078798c3930129f262017313ac5346b23918d8139d9f2811cd411c949bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:2019.0` - linux; amd64

```console
$ docker pull php-zendserver@sha256:bef80852773b2fdd80c58c8beb28f557e0dc3bfdd627a84c778820b392215792
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.8 MB (491795212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090dde0a08e609a8d8428f21fcd1c8032f8e715ef6c50ac66ef1bda2711481bb`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Wed, 17 Jun 2020 01:20:29 GMT
ADD file:1e8d02626176dc8141df3c0a1365774ce73d79934654fe24a4b1e7f173108232 in / 
# Wed, 17 Jun 2020 01:20:30 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:20:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:20:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:20:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:59:51 GMT
RUN apt-get update && apt-get install -y       gnupg
# Wed, 17 Jun 2020 03:59:52 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Wed, 17 Jun 2020 03:59:52 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Wed, 17 Jun 2020 04:01:41 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.4+b392     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Wed, 17 Jun 2020 04:01:42 GMT
ENV ZS_INIT_VERSION=0.3
# Wed, 17 Jun 2020 04:01:42 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Wed, 17 Jun 2020 04:01:42 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Wed, 17 Jun 2020 04:01:43 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Wed, 17 Jun 2020 04:01:43 GMT
WORKDIR /usr/local/zs-init
# Wed, 17 Jun 2020 04:01:53 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Wed, 17 Jun 2020 04:01:53 GMT
COPY dir:7937a6223a1e7805720eca1fbf8c2ccd37938f8f8aa175ae003d409459d49380 in /usr/local/bin 
# Wed, 17 Jun 2020 04:01:53 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Wed, 17 Jun 2020 04:01:54 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Wed, 17 Jun 2020 04:01:54 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Wed, 17 Jun 2020 04:01:54 GMT
EXPOSE 80
# Wed, 17 Jun 2020 04:01:55 GMT
EXPOSE 443
# Wed, 17 Jun 2020 04:01:55 GMT
EXPOSE 10081
# Wed, 17 Jun 2020 04:01:55 GMT
EXPOSE 10082
# Wed, 17 Jun 2020 04:01:55 GMT
WORKDIR /var/www/html
# Wed, 17 Jun 2020 04:01:55 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:d7c3167c320d7a820935f54cf4290890ea19567da496ecf774e8773b35d5f065`  
		Last Modified: Wed, 27 May 2020 12:21:15 GMT  
		Size: 26.7 MB (26688718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131f805ec7fd68d45a887e2ef82de61de0247b4eb934ab03b7c933650e854baa`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 35.4 KB (35369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322ed380e680a77f30528ba013e3a802a7b44948a0609c7d1d732dd46a9a310d`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac240b130982ad1c3ba3188abbf18ba4e54bdd9e504ce2d5c2eff6d3e86b8dd`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93ea707929bfafedb3b75f852537eec5259a7dccfe5c40edc9e83b1dfe0288d`  
		Last Modified: Wed, 17 Jun 2020 04:04:13 GMT  
		Size: 27.9 MB (27926487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d02f9a0979dffa0332814e23ceaa22e93fcf59fa61f1c86c2afb5ebdcebf38`  
		Last Modified: Wed, 17 Jun 2020 04:04:09 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b8868e0ef3791c3aee9b4a0226b628b5f942f8482baf11d1a19cef5d82c7c0`  
		Last Modified: Wed, 17 Jun 2020 04:04:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa006cda84ab7e4c5c6309b8e2a39695cc506d6b97e4f182523cf468adfb55f`  
		Last Modified: Wed, 17 Jun 2020 04:05:12 GMT  
		Size: 417.6 MB (417566090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3a38d705cde0eea59be0effc6cae6fe8a7377a4aa29d26b57e34252d262444`  
		Last Modified: Wed, 17 Jun 2020 04:04:07 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37cbe4406d1feff8e260da249499e0e0447b02fc94c083bbd809e2f98a900b1b`  
		Last Modified: Wed, 17 Jun 2020 04:04:07 GMT  
		Size: 18.9 KB (18904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3faf409dc5327562280c1fb96738de183d3916c9bebaa481fc29cfac879db96c`  
		Last Modified: Wed, 17 Jun 2020 04:04:10 GMT  
		Size: 19.5 MB (19538341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b2e0811db258040a30273c034f5bd35eb85b4fb44283cdc42f2fb650d2723c`  
		Last Modified: Wed, 17 Jun 2020 04:04:06 GMT  
		Size: 14.3 KB (14254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a8ae49a3b97227c921aab89897d95d81186b7fa41ccd4f38ceadf294ec185`  
		Last Modified: Wed, 17 Jun 2020 04:04:06 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a8bbba9255c257d9dd7dd2ecabcc42f8f664a2763f45f2e7f550b597a7af26`  
		Last Modified: Wed, 17 Jun 2020 04:04:07 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68002d3a116feecc1f66e1df52f0af4ff077fde13cd29fe01bfe1d78255f08fe`  
		Last Modified: Wed, 17 Jun 2020 04:04:06 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:5.6`

```console
$ docker pull php-zendserver@sha256:20a684fc2d33b7113a79407dbf1373df5e9db4cd99f7a29a5e7f99af7d8b8bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:089287f73ae3f7b64bf53c7c9de9ec5170aa3da8671de51ae43caf0c695a68b4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.8 MB (327770081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b6049600d308a4b72ff5fde528eb53230ee1f363c8f92d3e4e69ecf311322f`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Wed, 17 Jun 2020 01:21:26 GMT
ADD file:52af30f80ba214985a59cb0ef7073c64f8514d58396c0de48f8d7056dec2a58a in / 
# Wed, 17 Jun 2020 01:21:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:21:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:21:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:55:21 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Wed, 17 Jun 2020 03:55:21 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Wed, 17 Jun 2020 03:55:22 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Wed, 17 Jun 2020 03:57:13 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.15+b8     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Wed, 17 Jun 2020 03:57:14 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Wed, 17 Jun 2020 03:57:15 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Wed, 17 Jun 2020 03:57:15 GMT
RUN /usr/sbin/a2enmod headers
# Wed, 17 Jun 2020 03:57:16 GMT
ENV ZS_INIT_VERSION=0.3
# Wed, 17 Jun 2020 03:57:16 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Wed, 17 Jun 2020 03:57:17 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Wed, 17 Jun 2020 03:57:17 GMT
WORKDIR /usr/local/zs-init
# Wed, 17 Jun 2020 03:57:31 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Wed, 17 Jun 2020 03:57:31 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Wed, 17 Jun 2020 03:57:31 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Wed, 17 Jun 2020 03:57:32 GMT
RUN rm /var/www/html/index.html
# Wed, 17 Jun 2020 03:57:32 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Wed, 17 Jun 2020 03:57:33 GMT
EXPOSE 80
# Wed, 17 Jun 2020 03:57:33 GMT
EXPOSE 443
# Wed, 17 Jun 2020 03:57:33 GMT
EXPOSE 10081
# Wed, 17 Jun 2020 03:57:33 GMT
EXPOSE 10082
# Wed, 17 Jun 2020 03:57:33 GMT
WORKDIR /var/www/html
# Wed, 17 Jun 2020 03:57:33 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:b5e173e44934e01d8d2674bc8b1da00f761c4fe796e0fb2bee1bd1129d2e4ae1`  
		Last Modified: Fri, 15 May 2020 13:20:22 GMT  
		Size: 44.3 MB (44320272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29047100b0407dff554ea80b8005380d62b13a66d7fe2e2adb07b9c091b9f2c0`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 531.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15743a713c2a4033877dab08fb3989280f8c856234227158a4011811c7991372`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bc9e2987763aa991b7dfd742be04c7b3bb04448982ffe88e58d55c93b76d4`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ad2346736b97ffb0d2642415e6c37b89098dd5fb4b16ea34dd9c84c3e4b5ab`  
		Last Modified: Wed, 17 Jun 2020 04:02:17 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a7452596541aa31f758fe3d55c256ad8ac2122507d954f02c28a52c8b81f02`  
		Last Modified: Wed, 17 Jun 2020 04:02:17 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ae26b3f0d0749f80551a1941dad5f5f2fa6770a330705b851dcd89bca19528`  
		Last Modified: Wed, 17 Jun 2020 04:02:17 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e318dca63be589f906b920e0b79c783bb18e8a228c59283321008a1e3c2188`  
		Last Modified: Wed, 17 Jun 2020 04:03:02 GMT  
		Size: 263.9 MB (263866856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1d868cd90215ba0f13a2d345f5570c3226bf144709fe5a94563213d005d0ca`  
		Last Modified: Wed, 17 Jun 2020 04:02:15 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a17e74bf3f5d4dc88b09ce5960f9b87f5974e21a9caf19076ea9e16ddc78c0`  
		Last Modified: Wed, 17 Jun 2020 04:02:15 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466e5051c0c65c917f21f3e7240d8dc86194f52bb0c7dba5c5b65b6947a15d1f`  
		Last Modified: Wed, 17 Jun 2020 04:02:15 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63618d70b12475ea45ebe40db4037b72c7ba2f20039278dac3ae52f15ae3144`  
		Last Modified: Wed, 17 Jun 2020 04:02:15 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16089dffd0807a1f8895185ac6aed28140056743d02b9ab5dd54ad69caa5b10f`  
		Last Modified: Wed, 17 Jun 2020 04:02:20 GMT  
		Size: 19.5 MB (19530788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7deef06332fea41aecbeeef3544eb38a83f3f5aba6d42dc9790e293c9651a2`  
		Last Modified: Wed, 17 Jun 2020 04:02:13 GMT  
		Size: 13.4 KB (13358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1123aa7ff350416c515d8d3633875897bbcf327c84dca7d2c7a99e9206fac818`  
		Last Modified: Wed, 17 Jun 2020 04:02:13 GMT  
		Size: 2.5 KB (2535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee05e253abbd1a13406ead9d2c569c391c1ac3c1b671458334624ff983c9fcc3`  
		Last Modified: Wed, 17 Jun 2020 04:02:13 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8e2b14dae4aba434caf95862680e1d29dede6e5eccf8c59df64327fc6492ed`  
		Last Modified: Wed, 17 Jun 2020 04:02:13 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5`

```console
$ docker pull php-zendserver@sha256:20a684fc2d33b7113a79407dbf1373df5e9db4cd99f7a29a5e7f99af7d8b8bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:8.5` - linux; amd64

```console
$ docker pull php-zendserver@sha256:089287f73ae3f7b64bf53c7c9de9ec5170aa3da8671de51ae43caf0c695a68b4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.8 MB (327770081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b6049600d308a4b72ff5fde528eb53230ee1f363c8f92d3e4e69ecf311322f`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Wed, 17 Jun 2020 01:21:26 GMT
ADD file:52af30f80ba214985a59cb0ef7073c64f8514d58396c0de48f8d7056dec2a58a in / 
# Wed, 17 Jun 2020 01:21:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:21:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:21:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:55:21 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Wed, 17 Jun 2020 03:55:21 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Wed, 17 Jun 2020 03:55:22 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Wed, 17 Jun 2020 03:57:13 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.15+b8     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Wed, 17 Jun 2020 03:57:14 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Wed, 17 Jun 2020 03:57:15 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Wed, 17 Jun 2020 03:57:15 GMT
RUN /usr/sbin/a2enmod headers
# Wed, 17 Jun 2020 03:57:16 GMT
ENV ZS_INIT_VERSION=0.3
# Wed, 17 Jun 2020 03:57:16 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Wed, 17 Jun 2020 03:57:17 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Wed, 17 Jun 2020 03:57:17 GMT
WORKDIR /usr/local/zs-init
# Wed, 17 Jun 2020 03:57:31 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Wed, 17 Jun 2020 03:57:31 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Wed, 17 Jun 2020 03:57:31 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Wed, 17 Jun 2020 03:57:32 GMT
RUN rm /var/www/html/index.html
# Wed, 17 Jun 2020 03:57:32 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Wed, 17 Jun 2020 03:57:33 GMT
EXPOSE 80
# Wed, 17 Jun 2020 03:57:33 GMT
EXPOSE 443
# Wed, 17 Jun 2020 03:57:33 GMT
EXPOSE 10081
# Wed, 17 Jun 2020 03:57:33 GMT
EXPOSE 10082
# Wed, 17 Jun 2020 03:57:33 GMT
WORKDIR /var/www/html
# Wed, 17 Jun 2020 03:57:33 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:b5e173e44934e01d8d2674bc8b1da00f761c4fe796e0fb2bee1bd1129d2e4ae1`  
		Last Modified: Fri, 15 May 2020 13:20:22 GMT  
		Size: 44.3 MB (44320272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29047100b0407dff554ea80b8005380d62b13a66d7fe2e2adb07b9c091b9f2c0`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 531.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15743a713c2a4033877dab08fb3989280f8c856234227158a4011811c7991372`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bc9e2987763aa991b7dfd742be04c7b3bb04448982ffe88e58d55c93b76d4`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ad2346736b97ffb0d2642415e6c37b89098dd5fb4b16ea34dd9c84c3e4b5ab`  
		Last Modified: Wed, 17 Jun 2020 04:02:17 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a7452596541aa31f758fe3d55c256ad8ac2122507d954f02c28a52c8b81f02`  
		Last Modified: Wed, 17 Jun 2020 04:02:17 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ae26b3f0d0749f80551a1941dad5f5f2fa6770a330705b851dcd89bca19528`  
		Last Modified: Wed, 17 Jun 2020 04:02:17 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e318dca63be589f906b920e0b79c783bb18e8a228c59283321008a1e3c2188`  
		Last Modified: Wed, 17 Jun 2020 04:03:02 GMT  
		Size: 263.9 MB (263866856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1d868cd90215ba0f13a2d345f5570c3226bf144709fe5a94563213d005d0ca`  
		Last Modified: Wed, 17 Jun 2020 04:02:15 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a17e74bf3f5d4dc88b09ce5960f9b87f5974e21a9caf19076ea9e16ddc78c0`  
		Last Modified: Wed, 17 Jun 2020 04:02:15 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466e5051c0c65c917f21f3e7240d8dc86194f52bb0c7dba5c5b65b6947a15d1f`  
		Last Modified: Wed, 17 Jun 2020 04:02:15 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63618d70b12475ea45ebe40db4037b72c7ba2f20039278dac3ae52f15ae3144`  
		Last Modified: Wed, 17 Jun 2020 04:02:15 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16089dffd0807a1f8895185ac6aed28140056743d02b9ab5dd54ad69caa5b10f`  
		Last Modified: Wed, 17 Jun 2020 04:02:20 GMT  
		Size: 19.5 MB (19530788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7deef06332fea41aecbeeef3544eb38a83f3f5aba6d42dc9790e293c9651a2`  
		Last Modified: Wed, 17 Jun 2020 04:02:13 GMT  
		Size: 13.4 KB (13358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1123aa7ff350416c515d8d3633875897bbcf327c84dca7d2c7a99e9206fac818`  
		Last Modified: Wed, 17 Jun 2020 04:02:13 GMT  
		Size: 2.5 KB (2535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee05e253abbd1a13406ead9d2c569c391c1ac3c1b671458334624ff983c9fcc3`  
		Last Modified: Wed, 17 Jun 2020 04:02:13 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8e2b14dae4aba434caf95862680e1d29dede6e5eccf8c59df64327fc6492ed`  
		Last Modified: Wed, 17 Jun 2020 04:02:13 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5-php5.6`

```console
$ docker pull php-zendserver@sha256:20a684fc2d33b7113a79407dbf1373df5e9db4cd99f7a29a5e7f99af7d8b8bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:8.5-php5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:089287f73ae3f7b64bf53c7c9de9ec5170aa3da8671de51ae43caf0c695a68b4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.8 MB (327770081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b6049600d308a4b72ff5fde528eb53230ee1f363c8f92d3e4e69ecf311322f`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Wed, 17 Jun 2020 01:21:26 GMT
ADD file:52af30f80ba214985a59cb0ef7073c64f8514d58396c0de48f8d7056dec2a58a in / 
# Wed, 17 Jun 2020 01:21:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:21:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:21:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:55:21 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Wed, 17 Jun 2020 03:55:21 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Wed, 17 Jun 2020 03:55:22 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Wed, 17 Jun 2020 03:57:13 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.15+b8     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Wed, 17 Jun 2020 03:57:14 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Wed, 17 Jun 2020 03:57:15 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Wed, 17 Jun 2020 03:57:15 GMT
RUN /usr/sbin/a2enmod headers
# Wed, 17 Jun 2020 03:57:16 GMT
ENV ZS_INIT_VERSION=0.3
# Wed, 17 Jun 2020 03:57:16 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Wed, 17 Jun 2020 03:57:17 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Wed, 17 Jun 2020 03:57:17 GMT
WORKDIR /usr/local/zs-init
# Wed, 17 Jun 2020 03:57:31 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Wed, 17 Jun 2020 03:57:31 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Wed, 17 Jun 2020 03:57:31 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Wed, 17 Jun 2020 03:57:32 GMT
RUN rm /var/www/html/index.html
# Wed, 17 Jun 2020 03:57:32 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Wed, 17 Jun 2020 03:57:33 GMT
EXPOSE 80
# Wed, 17 Jun 2020 03:57:33 GMT
EXPOSE 443
# Wed, 17 Jun 2020 03:57:33 GMT
EXPOSE 10081
# Wed, 17 Jun 2020 03:57:33 GMT
EXPOSE 10082
# Wed, 17 Jun 2020 03:57:33 GMT
WORKDIR /var/www/html
# Wed, 17 Jun 2020 03:57:33 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:b5e173e44934e01d8d2674bc8b1da00f761c4fe796e0fb2bee1bd1129d2e4ae1`  
		Last Modified: Fri, 15 May 2020 13:20:22 GMT  
		Size: 44.3 MB (44320272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29047100b0407dff554ea80b8005380d62b13a66d7fe2e2adb07b9c091b9f2c0`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 531.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15743a713c2a4033877dab08fb3989280f8c856234227158a4011811c7991372`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bc9e2987763aa991b7dfd742be04c7b3bb04448982ffe88e58d55c93b76d4`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ad2346736b97ffb0d2642415e6c37b89098dd5fb4b16ea34dd9c84c3e4b5ab`  
		Last Modified: Wed, 17 Jun 2020 04:02:17 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a7452596541aa31f758fe3d55c256ad8ac2122507d954f02c28a52c8b81f02`  
		Last Modified: Wed, 17 Jun 2020 04:02:17 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ae26b3f0d0749f80551a1941dad5f5f2fa6770a330705b851dcd89bca19528`  
		Last Modified: Wed, 17 Jun 2020 04:02:17 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e318dca63be589f906b920e0b79c783bb18e8a228c59283321008a1e3c2188`  
		Last Modified: Wed, 17 Jun 2020 04:03:02 GMT  
		Size: 263.9 MB (263866856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1d868cd90215ba0f13a2d345f5570c3226bf144709fe5a94563213d005d0ca`  
		Last Modified: Wed, 17 Jun 2020 04:02:15 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a17e74bf3f5d4dc88b09ce5960f9b87f5974e21a9caf19076ea9e16ddc78c0`  
		Last Modified: Wed, 17 Jun 2020 04:02:15 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466e5051c0c65c917f21f3e7240d8dc86194f52bb0c7dba5c5b65b6947a15d1f`  
		Last Modified: Wed, 17 Jun 2020 04:02:15 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63618d70b12475ea45ebe40db4037b72c7ba2f20039278dac3ae52f15ae3144`  
		Last Modified: Wed, 17 Jun 2020 04:02:15 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16089dffd0807a1f8895185ac6aed28140056743d02b9ab5dd54ad69caa5b10f`  
		Last Modified: Wed, 17 Jun 2020 04:02:20 GMT  
		Size: 19.5 MB (19530788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7deef06332fea41aecbeeef3544eb38a83f3f5aba6d42dc9790e293c9651a2`  
		Last Modified: Wed, 17 Jun 2020 04:02:13 GMT  
		Size: 13.4 KB (13358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1123aa7ff350416c515d8d3633875897bbcf327c84dca7d2c7a99e9206fac818`  
		Last Modified: Wed, 17 Jun 2020 04:02:13 GMT  
		Size: 2.5 KB (2535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee05e253abbd1a13406ead9d2c569c391c1ac3c1b671458334624ff983c9fcc3`  
		Last Modified: Wed, 17 Jun 2020 04:02:13 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8e2b14dae4aba434caf95862680e1d29dede6e5eccf8c59df64327fc6492ed`  
		Last Modified: Wed, 17 Jun 2020 04:02:13 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:9.1`

```console
$ docker pull php-zendserver@sha256:48fccb3475a279aa7007db489df49fcc314fe56ab03026023bad2c18e7464534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:9.1` - linux; amd64

```console
$ docker pull php-zendserver@sha256:6a23e2d66bbd501743b26d9259a10f0eb4b68b1349df0896ae72e73615fd7e50
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.1 MB (416093461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654f5697686525c3f0913dcf03840bafc6b6c67bdbfe11bba6324e0389ce43c4`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Wed, 17 Jun 2020 01:21:26 GMT
ADD file:52af30f80ba214985a59cb0ef7073c64f8514d58396c0de48f8d7056dec2a58a in / 
# Wed, 17 Jun 2020 01:21:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:21:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:21:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:55:21 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Wed, 17 Jun 2020 03:57:52 GMT
COPY file:0d4830b5060fb75cec6a47b30d343d82f9c3d6f95f20c11635618b93dedb5720 in /etc/apt/sources.list.d/zend-server.list 
# Wed, 17 Jun 2020 03:59:16 GMT
RUN apt-get update     && apt-get install -y       curl       libmysqlclient20       unzip       git       zend-server-php-7.1=9.1.10+b202     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Wed, 17 Jun 2020 03:59:17 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Wed, 17 Jun 2020 03:59:18 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Wed, 17 Jun 2020 03:59:19 GMT
RUN /usr/sbin/a2enmod headers
# Wed, 17 Jun 2020 03:59:19 GMT
ENV ZS_INIT_VERSION=0.3
# Wed, 17 Jun 2020 03:59:19 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Wed, 17 Jun 2020 03:59:20 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Wed, 17 Jun 2020 03:59:20 GMT
WORKDIR /usr/local/zs-init
# Wed, 17 Jun 2020 03:59:30 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Wed, 17 Jun 2020 03:59:30 GMT
COPY dir:864637d3fa0817ce3be0c7e34e1298851fa2ea4cfb86583e2ec811f00c6a95fd in /usr/local/bin 
# Wed, 17 Jun 2020 03:59:31 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Wed, 17 Jun 2020 03:59:31 GMT
RUN rm /var/www/html/index.html
# Wed, 17 Jun 2020 03:59:32 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Wed, 17 Jun 2020 03:59:32 GMT
EXPOSE 80
# Wed, 17 Jun 2020 03:59:32 GMT
EXPOSE 443
# Wed, 17 Jun 2020 03:59:32 GMT
EXPOSE 10081
# Wed, 17 Jun 2020 03:59:32 GMT
EXPOSE 10082
# Wed, 17 Jun 2020 03:59:33 GMT
WORKDIR /var/www/html
# Wed, 17 Jun 2020 03:59:33 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:b5e173e44934e01d8d2674bc8b1da00f761c4fe796e0fb2bee1bd1129d2e4ae1`  
		Last Modified: Fri, 15 May 2020 13:20:22 GMT  
		Size: 44.3 MB (44320272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29047100b0407dff554ea80b8005380d62b13a66d7fe2e2adb07b9c091b9f2c0`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 531.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15743a713c2a4033877dab08fb3989280f8c856234227158a4011811c7991372`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bc9e2987763aa991b7dfd742be04c7b3bb04448982ffe88e58d55c93b76d4`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ad2346736b97ffb0d2642415e6c37b89098dd5fb4b16ea34dd9c84c3e4b5ab`  
		Last Modified: Wed, 17 Jun 2020 04:02:17 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92fabaf9b94d09d1b0d70df6d91157889020d3f7bbf64590f0282143c43befc6`  
		Last Modified: Wed, 17 Jun 2020 04:03:12 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677f93d0da0b7ce630c03600c0a03172093637f91e1de3532c0652a96f3d06a3`  
		Last Modified: Wed, 17 Jun 2020 04:04:02 GMT  
		Size: 352.2 MB (352182181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19eeccc1efca756b8e8b3b60270fb884bd9181fa68229cb5a583b538bf40d43`  
		Last Modified: Wed, 17 Jun 2020 04:03:10 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0be63beee082fb706e3a2f808380a9a283e5e0d4000dcd5bcc33f7c9143b553`  
		Last Modified: Wed, 17 Jun 2020 04:03:10 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907dd90c061a034515aaa94ffaeb974c5bd2796fb2dbbc180b80032204ae293a`  
		Last Modified: Wed, 17 Jun 2020 04:03:10 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5650811f10cce8f0a58a2b747debb3fd5f9e342bce3ad80ead8a5c17d3e6a5d4`  
		Last Modified: Wed, 17 Jun 2020 04:03:10 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd32cc72cf481564b58e73fe04344a1e6dda4f44ebc0408bc324a4918449b0d`  
		Last Modified: Wed, 17 Jun 2020 04:03:12 GMT  
		Size: 19.5 MB (19538169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26cae1786de9f1097c0bfa09718f5e2b5b931f02cfd4ea907f54117cecf1b8`  
		Last Modified: Wed, 17 Jun 2020 04:03:09 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8843c1a22ff10a71d7a3ae8132893fa1d0cbfd00ecd0279605b9b1964db1d8eb`  
		Last Modified: Wed, 17 Jun 2020 04:03:08 GMT  
		Size: 2.5 KB (2535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3a0ab7e6825a3ac2fdcba729258f5e2b910d35424a37bbfede1d45a3253fbf`  
		Last Modified: Wed, 17 Jun 2020 04:03:09 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e112274e12cf33cefcfd9702ff101af1c07435f3863df66ceedeb650682b694d`  
		Last Modified: Wed, 17 Jun 2020 04:03:08 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:latest`

```console
$ docker pull php-zendserver@sha256:10a5b078798c3930129f262017313ac5346b23918d8139d9f2811cd411c949bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:latest` - linux; amd64

```console
$ docker pull php-zendserver@sha256:bef80852773b2fdd80c58c8beb28f557e0dc3bfdd627a84c778820b392215792
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.8 MB (491795212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090dde0a08e609a8d8428f21fcd1c8032f8e715ef6c50ac66ef1bda2711481bb`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Wed, 17 Jun 2020 01:20:29 GMT
ADD file:1e8d02626176dc8141df3c0a1365774ce73d79934654fe24a4b1e7f173108232 in / 
# Wed, 17 Jun 2020 01:20:30 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:20:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:20:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:20:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:59:51 GMT
RUN apt-get update && apt-get install -y       gnupg
# Wed, 17 Jun 2020 03:59:52 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Wed, 17 Jun 2020 03:59:52 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Wed, 17 Jun 2020 04:01:41 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.4+b392     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Wed, 17 Jun 2020 04:01:42 GMT
ENV ZS_INIT_VERSION=0.3
# Wed, 17 Jun 2020 04:01:42 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Wed, 17 Jun 2020 04:01:42 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Wed, 17 Jun 2020 04:01:43 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Wed, 17 Jun 2020 04:01:43 GMT
WORKDIR /usr/local/zs-init
# Wed, 17 Jun 2020 04:01:53 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Wed, 17 Jun 2020 04:01:53 GMT
COPY dir:7937a6223a1e7805720eca1fbf8c2ccd37938f8f8aa175ae003d409459d49380 in /usr/local/bin 
# Wed, 17 Jun 2020 04:01:53 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Wed, 17 Jun 2020 04:01:54 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Wed, 17 Jun 2020 04:01:54 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Wed, 17 Jun 2020 04:01:54 GMT
EXPOSE 80
# Wed, 17 Jun 2020 04:01:55 GMT
EXPOSE 443
# Wed, 17 Jun 2020 04:01:55 GMT
EXPOSE 10081
# Wed, 17 Jun 2020 04:01:55 GMT
EXPOSE 10082
# Wed, 17 Jun 2020 04:01:55 GMT
WORKDIR /var/www/html
# Wed, 17 Jun 2020 04:01:55 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:d7c3167c320d7a820935f54cf4290890ea19567da496ecf774e8773b35d5f065`  
		Last Modified: Wed, 27 May 2020 12:21:15 GMT  
		Size: 26.7 MB (26688718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131f805ec7fd68d45a887e2ef82de61de0247b4eb934ab03b7c933650e854baa`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 35.4 KB (35369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322ed380e680a77f30528ba013e3a802a7b44948a0609c7d1d732dd46a9a310d`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac240b130982ad1c3ba3188abbf18ba4e54bdd9e504ce2d5c2eff6d3e86b8dd`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93ea707929bfafedb3b75f852537eec5259a7dccfe5c40edc9e83b1dfe0288d`  
		Last Modified: Wed, 17 Jun 2020 04:04:13 GMT  
		Size: 27.9 MB (27926487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d02f9a0979dffa0332814e23ceaa22e93fcf59fa61f1c86c2afb5ebdcebf38`  
		Last Modified: Wed, 17 Jun 2020 04:04:09 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b8868e0ef3791c3aee9b4a0226b628b5f942f8482baf11d1a19cef5d82c7c0`  
		Last Modified: Wed, 17 Jun 2020 04:04:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa006cda84ab7e4c5c6309b8e2a39695cc506d6b97e4f182523cf468adfb55f`  
		Last Modified: Wed, 17 Jun 2020 04:05:12 GMT  
		Size: 417.6 MB (417566090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3a38d705cde0eea59be0effc6cae6fe8a7377a4aa29d26b57e34252d262444`  
		Last Modified: Wed, 17 Jun 2020 04:04:07 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37cbe4406d1feff8e260da249499e0e0447b02fc94c083bbd809e2f98a900b1b`  
		Last Modified: Wed, 17 Jun 2020 04:04:07 GMT  
		Size: 18.9 KB (18904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3faf409dc5327562280c1fb96738de183d3916c9bebaa481fc29cfac879db96c`  
		Last Modified: Wed, 17 Jun 2020 04:04:10 GMT  
		Size: 19.5 MB (19538341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b2e0811db258040a30273c034f5bd35eb85b4fb44283cdc42f2fb650d2723c`  
		Last Modified: Wed, 17 Jun 2020 04:04:06 GMT  
		Size: 14.3 KB (14254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a8ae49a3b97227c921aab89897d95d81186b7fa41ccd4f38ceadf294ec185`  
		Last Modified: Wed, 17 Jun 2020 04:04:06 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a8bbba9255c257d9dd7dd2ecabcc42f8f664a2763f45f2e7f550b597a7af26`  
		Last Modified: Wed, 17 Jun 2020 04:04:07 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68002d3a116feecc1f66e1df52f0af4ff077fde13cd29fe01bfe1d78255f08fe`  
		Last Modified: Wed, 17 Jun 2020 04:04:06 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
