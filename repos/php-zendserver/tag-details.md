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
$ docker pull php-zendserver@sha256:156eae12dc2703adde99a46b7bbe5188fba92a8ec1ed00e9782bc20296bbef1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:2019.0` - linux; amd64

```console
$ docker pull php-zendserver@sha256:e85fc05ad0dcb52db2388cb3d1f2ca03d82df0dda56e425900c9d0e34c269a63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.4 MB (491419057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b369291f87b577cadde29a42dc919bc19a56d1ac2712fd8cc80436699a8d4f`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Wed, 19 Aug 2020 21:13:50 GMT
ADD file:5c125b7f411566e9daa738d8cb851098f36197810f06488c2609074296f294b2 in / 
# Wed, 19 Aug 2020 21:13:52 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:13:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:13:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:13:55 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 23:38:46 GMT
RUN apt-get update && apt-get install -y       gnupg
# Wed, 19 Aug 2020 23:38:47 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Wed, 19 Aug 2020 23:38:47 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Wed, 19 Aug 2020 23:40:18 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.4+b392     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Wed, 19 Aug 2020 23:40:19 GMT
ENV ZS_INIT_VERSION=0.3
# Wed, 19 Aug 2020 23:40:19 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Wed, 19 Aug 2020 23:40:19 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Wed, 19 Aug 2020 23:40:20 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Wed, 19 Aug 2020 23:40:20 GMT
WORKDIR /usr/local/zs-init
# Wed, 19 Aug 2020 23:40:30 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Wed, 19 Aug 2020 23:40:30 GMT
COPY dir:7937a6223a1e7805720eca1fbf8c2ccd37938f8f8aa175ae003d409459d49380 in /usr/local/bin 
# Wed, 19 Aug 2020 23:40:30 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Wed, 19 Aug 2020 23:40:31 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Wed, 19 Aug 2020 23:40:31 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Wed, 19 Aug 2020 23:40:32 GMT
EXPOSE 80
# Wed, 19 Aug 2020 23:40:32 GMT
EXPOSE 443
# Wed, 19 Aug 2020 23:40:32 GMT
EXPOSE 10081
# Wed, 19 Aug 2020 23:40:32 GMT
EXPOSE 10082
# Wed, 19 Aug 2020 23:40:32 GMT
WORKDIR /var/www/html
# Wed, 19 Aug 2020 23:40:32 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:f08d8e2a3ba11bea23cf5c17e8e1c620057412ed05c32d1114640e18d6dd0a43`  
		Last Modified: Sat, 08 Aug 2020 12:21:16 GMT  
		Size: 26.7 MB (26700095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9cb2483bd9c5329a44d9c2fe72535625bbd4308bca95785dd58e72c06365`  
		Last Modified: Wed, 19 Aug 2020 21:16:44 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e5ff4c0b1526abf77c236655f21c8f67a23313291c8b970fe6b469549d8153`  
		Last Modified: Wed, 19 Aug 2020 21:16:44 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1860925334f940c3145808527480b4f0cba7f01279087fdb27679e4354fba967`  
		Last Modified: Wed, 19 Aug 2020 21:16:44 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddcc9b3b04d4af7f8cd42b20b4d4eeab5eae7a2062a53b9e99a0c0577b85790`  
		Last Modified: Wed, 19 Aug 2020 23:42:57 GMT  
		Size: 28.3 MB (28267258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3726f4ff6b1261712ea3b160ce213d525018b5875b3afa7f81e9b517d373cbe0`  
		Last Modified: Wed, 19 Aug 2020 23:42:53 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c404c30bcee943368cf18404142c5daea79043736b7f70615cc6ccd3fa2a62`  
		Last Modified: Wed, 19 Aug 2020 23:42:52 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0732084791d941a2b2f0830bfc2ef3c0e99cab7530d5e8200124aad21d993a88`  
		Last Modified: Wed, 19 Aug 2020 23:43:55 GMT  
		Size: 417.6 MB (417572070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73a7901bfecf4ba69c435dd68ac7611416eda5409fff77245428f22f5883524`  
		Last Modified: Wed, 19 Aug 2020 23:42:52 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ed38341a32b31bc4e0792be1cddb2bea646e4a340a4f13806a0d8cc2fdcf8`  
		Last Modified: Wed, 19 Aug 2020 23:42:52 GMT  
		Size: 18.9 KB (18902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77d4388fb3a6eb617d5956ca2d52931504e7e6e9e041e99e4043b06de56593e`  
		Last Modified: Wed, 19 Aug 2020 23:42:54 GMT  
		Size: 18.8 MB (18804061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5f12d237947485aeadebc5c92e678cd7fc870cd91dd2040ecab1c6157a22a`  
		Last Modified: Wed, 19 Aug 2020 23:42:51 GMT  
		Size: 14.2 KB (14249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd8fe24f26e10152c37029e53bd072eb9b32e08984fb6520171253832caf86c`  
		Last Modified: Wed, 19 Aug 2020 23:42:51 GMT  
		Size: 2.5 KB (2529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13abb24f1ca2419f43a0db5a1886aaa0fd521b3471d6d23ff603f8404c6b9c08`  
		Last Modified: Wed, 19 Aug 2020 23:42:51 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3177cec03260e9f6d9812c47e245d3cfe1ecd837beb98b48053c22449f3860c7`  
		Last Modified: Wed, 19 Aug 2020 23:42:51 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:5.6`

```console
$ docker pull php-zendserver@sha256:63407a239c07141e3a6a370c83ca39c319b4526273dd04636f4fec866d488333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:639f2f2e6db8295970ffd5e79c1c9f91ba38378f0466a1fb17b08ef79af1ff15
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.2 MB (327160108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2472a77ef711c6a3a7d15f78210f8f7a77ec07e931f3ab408a4f30c933860e6`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Wed, 19 Aug 2020 21:16:18 GMT
ADD file:144835a276ed2d8eaf6e893d5560444fe0d6a6f9b9bdadec1eb56e7bd9814427 in / 
# Wed, 19 Aug 2020 21:16:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 21:16:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:16:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:16:22 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 23:34:32 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Wed, 19 Aug 2020 23:34:32 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Wed, 19 Aug 2020 23:34:32 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Wed, 19 Aug 2020 23:36:18 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.15+b8     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Wed, 19 Aug 2020 23:36:19 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Wed, 19 Aug 2020 23:36:20 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Wed, 19 Aug 2020 23:36:21 GMT
RUN /usr/sbin/a2enmod headers
# Wed, 19 Aug 2020 23:36:21 GMT
ENV ZS_INIT_VERSION=0.3
# Wed, 19 Aug 2020 23:36:21 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Wed, 19 Aug 2020 23:36:22 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Wed, 19 Aug 2020 23:36:22 GMT
WORKDIR /usr/local/zs-init
# Wed, 19 Aug 2020 23:36:35 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Wed, 19 Aug 2020 23:36:35 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Wed, 19 Aug 2020 23:36:35 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Wed, 19 Aug 2020 23:36:36 GMT
RUN rm /var/www/html/index.html
# Wed, 19 Aug 2020 23:36:36 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Wed, 19 Aug 2020 23:36:36 GMT
EXPOSE 80
# Wed, 19 Aug 2020 23:36:37 GMT
EXPOSE 443
# Wed, 19 Aug 2020 23:36:37 GMT
EXPOSE 10081
# Wed, 19 Aug 2020 23:36:37 GMT
EXPOSE 10082
# Wed, 19 Aug 2020 23:36:37 GMT
WORKDIR /var/www/html
# Wed, 19 Aug 2020 23:36:37 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:8e097b52bfb8e743e52ccd2dfbd5a0363e48a00b06cdd3728a6fd4d1f3a34280`  
		Last Modified: Sat, 08 Aug 2020 13:20:06 GMT  
		Size: 44.4 MB (44447543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a613a9b4553ca86fac22546f2f79e2ff3d17d8d6aeea8b97d67862a5a40ad8ec`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc000f015361df35e770a910ce03d30691e35aa10d52f4a4f432f183a6c03db`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73eef93b7466c41f22f32d28aae5eb87e1ebc0c4d232c5f5e68c955d0e798dca`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98204131f91a066ec4e6e91dcdb20a24d8906a3eb1636c5f65410ef1223320a`  
		Last Modified: Wed, 19 Aug 2020 23:41:00 GMT  
		Size: 14.7 KB (14701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336864dddbcba89b7bd2621372c7bbaf0cf61cc6371b466da2ee065173c45eae`  
		Last Modified: Wed, 19 Aug 2020 23:40:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7b358c258493e4503bfe7f59f593e5b78d6dfae8f64480d4fe680c0a0564f0`  
		Last Modified: Wed, 19 Aug 2020 23:41:00 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1597d5300d3c45587d3be35815c237998889e983e162551349fdbe3febda74`  
		Last Modified: Wed, 19 Aug 2020 23:41:46 GMT  
		Size: 263.9 MB (263862003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc83abc04f42bb4ca044ce3c725a1effe649b340f51e6e2403b037a9286324c`  
		Last Modified: Wed, 19 Aug 2020 23:40:59 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18ede7c5c3a5ea4667c3d56e342fe51cff1ca9def9854775fd2c19383b644a1`  
		Last Modified: Wed, 19 Aug 2020 23:40:59 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6ed62fb80dadbe098e4c36c090f5f001b3ea36b5a14cff98b14f1cb568d158`  
		Last Modified: Wed, 19 Aug 2020 23:40:58 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fef609a9890bd830da97c23f412e52cafaaea8f5209117677e65c8f254be54`  
		Last Modified: Wed, 19 Aug 2020 23:40:58 GMT  
		Size: 18.8 KB (18826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e7ea21820ca70d8f23f351313164ad09291ecd8f72d0b1625fecaffdc9eb0e`  
		Last Modified: Wed, 19 Aug 2020 23:41:02 GMT  
		Size: 18.8 MB (18796774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38250c3bff2bc1aa21aa94cdb1949ed5121158274ef160f4ffef669f0b63e613`  
		Last Modified: Wed, 19 Aug 2020 23:40:58 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110316c2157fcd45726e6c19c34aaa544af9cd82d302403d11440d110663dd67`  
		Last Modified: Wed, 19 Aug 2020 23:40:57 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ee703da6cfeda8ab3494ce1bb6040da0d3596b2c3b38cf13d904731ec0469f`  
		Last Modified: Wed, 19 Aug 2020 23:40:57 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b7b4936cd67accb683d1d562836b1d6b64ae0cff71200ed0a5c80b084d06e3`  
		Last Modified: Wed, 19 Aug 2020 23:40:57 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5`

```console
$ docker pull php-zendserver@sha256:63407a239c07141e3a6a370c83ca39c319b4526273dd04636f4fec866d488333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:8.5` - linux; amd64

```console
$ docker pull php-zendserver@sha256:639f2f2e6db8295970ffd5e79c1c9f91ba38378f0466a1fb17b08ef79af1ff15
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.2 MB (327160108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2472a77ef711c6a3a7d15f78210f8f7a77ec07e931f3ab408a4f30c933860e6`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Wed, 19 Aug 2020 21:16:18 GMT
ADD file:144835a276ed2d8eaf6e893d5560444fe0d6a6f9b9bdadec1eb56e7bd9814427 in / 
# Wed, 19 Aug 2020 21:16:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 21:16:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:16:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:16:22 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 23:34:32 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Wed, 19 Aug 2020 23:34:32 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Wed, 19 Aug 2020 23:34:32 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Wed, 19 Aug 2020 23:36:18 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.15+b8     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Wed, 19 Aug 2020 23:36:19 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Wed, 19 Aug 2020 23:36:20 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Wed, 19 Aug 2020 23:36:21 GMT
RUN /usr/sbin/a2enmod headers
# Wed, 19 Aug 2020 23:36:21 GMT
ENV ZS_INIT_VERSION=0.3
# Wed, 19 Aug 2020 23:36:21 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Wed, 19 Aug 2020 23:36:22 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Wed, 19 Aug 2020 23:36:22 GMT
WORKDIR /usr/local/zs-init
# Wed, 19 Aug 2020 23:36:35 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Wed, 19 Aug 2020 23:36:35 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Wed, 19 Aug 2020 23:36:35 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Wed, 19 Aug 2020 23:36:36 GMT
RUN rm /var/www/html/index.html
# Wed, 19 Aug 2020 23:36:36 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Wed, 19 Aug 2020 23:36:36 GMT
EXPOSE 80
# Wed, 19 Aug 2020 23:36:37 GMT
EXPOSE 443
# Wed, 19 Aug 2020 23:36:37 GMT
EXPOSE 10081
# Wed, 19 Aug 2020 23:36:37 GMT
EXPOSE 10082
# Wed, 19 Aug 2020 23:36:37 GMT
WORKDIR /var/www/html
# Wed, 19 Aug 2020 23:36:37 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:8e097b52bfb8e743e52ccd2dfbd5a0363e48a00b06cdd3728a6fd4d1f3a34280`  
		Last Modified: Sat, 08 Aug 2020 13:20:06 GMT  
		Size: 44.4 MB (44447543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a613a9b4553ca86fac22546f2f79e2ff3d17d8d6aeea8b97d67862a5a40ad8ec`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc000f015361df35e770a910ce03d30691e35aa10d52f4a4f432f183a6c03db`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73eef93b7466c41f22f32d28aae5eb87e1ebc0c4d232c5f5e68c955d0e798dca`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98204131f91a066ec4e6e91dcdb20a24d8906a3eb1636c5f65410ef1223320a`  
		Last Modified: Wed, 19 Aug 2020 23:41:00 GMT  
		Size: 14.7 KB (14701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336864dddbcba89b7bd2621372c7bbaf0cf61cc6371b466da2ee065173c45eae`  
		Last Modified: Wed, 19 Aug 2020 23:40:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7b358c258493e4503bfe7f59f593e5b78d6dfae8f64480d4fe680c0a0564f0`  
		Last Modified: Wed, 19 Aug 2020 23:41:00 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1597d5300d3c45587d3be35815c237998889e983e162551349fdbe3febda74`  
		Last Modified: Wed, 19 Aug 2020 23:41:46 GMT  
		Size: 263.9 MB (263862003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc83abc04f42bb4ca044ce3c725a1effe649b340f51e6e2403b037a9286324c`  
		Last Modified: Wed, 19 Aug 2020 23:40:59 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18ede7c5c3a5ea4667c3d56e342fe51cff1ca9def9854775fd2c19383b644a1`  
		Last Modified: Wed, 19 Aug 2020 23:40:59 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6ed62fb80dadbe098e4c36c090f5f001b3ea36b5a14cff98b14f1cb568d158`  
		Last Modified: Wed, 19 Aug 2020 23:40:58 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fef609a9890bd830da97c23f412e52cafaaea8f5209117677e65c8f254be54`  
		Last Modified: Wed, 19 Aug 2020 23:40:58 GMT  
		Size: 18.8 KB (18826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e7ea21820ca70d8f23f351313164ad09291ecd8f72d0b1625fecaffdc9eb0e`  
		Last Modified: Wed, 19 Aug 2020 23:41:02 GMT  
		Size: 18.8 MB (18796774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38250c3bff2bc1aa21aa94cdb1949ed5121158274ef160f4ffef669f0b63e613`  
		Last Modified: Wed, 19 Aug 2020 23:40:58 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110316c2157fcd45726e6c19c34aaa544af9cd82d302403d11440d110663dd67`  
		Last Modified: Wed, 19 Aug 2020 23:40:57 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ee703da6cfeda8ab3494ce1bb6040da0d3596b2c3b38cf13d904731ec0469f`  
		Last Modified: Wed, 19 Aug 2020 23:40:57 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b7b4936cd67accb683d1d562836b1d6b64ae0cff71200ed0a5c80b084d06e3`  
		Last Modified: Wed, 19 Aug 2020 23:40:57 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5-php5.6`

```console
$ docker pull php-zendserver@sha256:63407a239c07141e3a6a370c83ca39c319b4526273dd04636f4fec866d488333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:8.5-php5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:639f2f2e6db8295970ffd5e79c1c9f91ba38378f0466a1fb17b08ef79af1ff15
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.2 MB (327160108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2472a77ef711c6a3a7d15f78210f8f7a77ec07e931f3ab408a4f30c933860e6`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Wed, 19 Aug 2020 21:16:18 GMT
ADD file:144835a276ed2d8eaf6e893d5560444fe0d6a6f9b9bdadec1eb56e7bd9814427 in / 
# Wed, 19 Aug 2020 21:16:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 21:16:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:16:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:16:22 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 23:34:32 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Wed, 19 Aug 2020 23:34:32 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Wed, 19 Aug 2020 23:34:32 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Wed, 19 Aug 2020 23:36:18 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.15+b8     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Wed, 19 Aug 2020 23:36:19 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Wed, 19 Aug 2020 23:36:20 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Wed, 19 Aug 2020 23:36:21 GMT
RUN /usr/sbin/a2enmod headers
# Wed, 19 Aug 2020 23:36:21 GMT
ENV ZS_INIT_VERSION=0.3
# Wed, 19 Aug 2020 23:36:21 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Wed, 19 Aug 2020 23:36:22 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Wed, 19 Aug 2020 23:36:22 GMT
WORKDIR /usr/local/zs-init
# Wed, 19 Aug 2020 23:36:35 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Wed, 19 Aug 2020 23:36:35 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Wed, 19 Aug 2020 23:36:35 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Wed, 19 Aug 2020 23:36:36 GMT
RUN rm /var/www/html/index.html
# Wed, 19 Aug 2020 23:36:36 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Wed, 19 Aug 2020 23:36:36 GMT
EXPOSE 80
# Wed, 19 Aug 2020 23:36:37 GMT
EXPOSE 443
# Wed, 19 Aug 2020 23:36:37 GMT
EXPOSE 10081
# Wed, 19 Aug 2020 23:36:37 GMT
EXPOSE 10082
# Wed, 19 Aug 2020 23:36:37 GMT
WORKDIR /var/www/html
# Wed, 19 Aug 2020 23:36:37 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:8e097b52bfb8e743e52ccd2dfbd5a0363e48a00b06cdd3728a6fd4d1f3a34280`  
		Last Modified: Sat, 08 Aug 2020 13:20:06 GMT  
		Size: 44.4 MB (44447543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a613a9b4553ca86fac22546f2f79e2ff3d17d8d6aeea8b97d67862a5a40ad8ec`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc000f015361df35e770a910ce03d30691e35aa10d52f4a4f432f183a6c03db`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73eef93b7466c41f22f32d28aae5eb87e1ebc0c4d232c5f5e68c955d0e798dca`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98204131f91a066ec4e6e91dcdb20a24d8906a3eb1636c5f65410ef1223320a`  
		Last Modified: Wed, 19 Aug 2020 23:41:00 GMT  
		Size: 14.7 KB (14701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336864dddbcba89b7bd2621372c7bbaf0cf61cc6371b466da2ee065173c45eae`  
		Last Modified: Wed, 19 Aug 2020 23:40:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7b358c258493e4503bfe7f59f593e5b78d6dfae8f64480d4fe680c0a0564f0`  
		Last Modified: Wed, 19 Aug 2020 23:41:00 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1597d5300d3c45587d3be35815c237998889e983e162551349fdbe3febda74`  
		Last Modified: Wed, 19 Aug 2020 23:41:46 GMT  
		Size: 263.9 MB (263862003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc83abc04f42bb4ca044ce3c725a1effe649b340f51e6e2403b037a9286324c`  
		Last Modified: Wed, 19 Aug 2020 23:40:59 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18ede7c5c3a5ea4667c3d56e342fe51cff1ca9def9854775fd2c19383b644a1`  
		Last Modified: Wed, 19 Aug 2020 23:40:59 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6ed62fb80dadbe098e4c36c090f5f001b3ea36b5a14cff98b14f1cb568d158`  
		Last Modified: Wed, 19 Aug 2020 23:40:58 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fef609a9890bd830da97c23f412e52cafaaea8f5209117677e65c8f254be54`  
		Last Modified: Wed, 19 Aug 2020 23:40:58 GMT  
		Size: 18.8 KB (18826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e7ea21820ca70d8f23f351313164ad09291ecd8f72d0b1625fecaffdc9eb0e`  
		Last Modified: Wed, 19 Aug 2020 23:41:02 GMT  
		Size: 18.8 MB (18796774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38250c3bff2bc1aa21aa94cdb1949ed5121158274ef160f4ffef669f0b63e613`  
		Last Modified: Wed, 19 Aug 2020 23:40:58 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110316c2157fcd45726e6c19c34aaa544af9cd82d302403d11440d110663dd67`  
		Last Modified: Wed, 19 Aug 2020 23:40:57 GMT  
		Size: 2.5 KB (2534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ee703da6cfeda8ab3494ce1bb6040da0d3596b2c3b38cf13d904731ec0469f`  
		Last Modified: Wed, 19 Aug 2020 23:40:57 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b7b4936cd67accb683d1d562836b1d6b64ae0cff71200ed0a5c80b084d06e3`  
		Last Modified: Wed, 19 Aug 2020 23:40:57 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:9.1`

```console
$ docker pull php-zendserver@sha256:b19a8728fcc49b37a32be2049b53b4ee4ff53eb75e0eac2738358cbb50fbc3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:9.1` - linux; amd64

```console
$ docker pull php-zendserver@sha256:e00d0c71fbd52d5c0e1e4a44a0f4990049f1ec52f4600c4e4217978c2799319a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.8 MB (410823198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b4dfb0f15e598ab54a3bac8d0d3670e71e434607563688084a1eab73fb5b56`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Wed, 19 Aug 2020 21:16:18 GMT
ADD file:144835a276ed2d8eaf6e893d5560444fe0d6a6f9b9bdadec1eb56e7bd9814427 in / 
# Wed, 19 Aug 2020 21:16:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 21:16:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:16:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:16:22 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 23:34:32 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Wed, 19 Aug 2020 23:36:48 GMT
COPY file:0d4830b5060fb75cec6a47b30d343d82f9c3d6f95f20c11635618b93dedb5720 in /etc/apt/sources.list.d/zend-server.list 
# Wed, 19 Aug 2020 23:38:09 GMT
RUN apt-get update     && apt-get install -y       curl       libmysqlclient20       unzip       git       zend-server-php-7.1=9.1.10+b202     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Wed, 19 Aug 2020 23:38:11 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Wed, 19 Aug 2020 23:38:11 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Wed, 19 Aug 2020 23:38:12 GMT
RUN /usr/sbin/a2enmod headers
# Wed, 19 Aug 2020 23:38:12 GMT
ENV ZS_INIT_VERSION=0.3
# Wed, 19 Aug 2020 23:38:12 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Wed, 19 Aug 2020 23:38:13 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Wed, 19 Aug 2020 23:38:13 GMT
WORKDIR /usr/local/zs-init
# Wed, 19 Aug 2020 23:38:25 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Wed, 19 Aug 2020 23:38:26 GMT
COPY dir:864637d3fa0817ce3be0c7e34e1298851fa2ea4cfb86583e2ec811f00c6a95fd in /usr/local/bin 
# Wed, 19 Aug 2020 23:38:26 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Wed, 19 Aug 2020 23:38:27 GMT
RUN rm /var/www/html/index.html
# Wed, 19 Aug 2020 23:38:27 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Wed, 19 Aug 2020 23:38:27 GMT
EXPOSE 80
# Wed, 19 Aug 2020 23:38:27 GMT
EXPOSE 443
# Wed, 19 Aug 2020 23:38:27 GMT
EXPOSE 10081
# Wed, 19 Aug 2020 23:38:27 GMT
EXPOSE 10082
# Wed, 19 Aug 2020 23:38:28 GMT
WORKDIR /var/www/html
# Wed, 19 Aug 2020 23:38:28 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:8e097b52bfb8e743e52ccd2dfbd5a0363e48a00b06cdd3728a6fd4d1f3a34280`  
		Last Modified: Sat, 08 Aug 2020 13:20:06 GMT  
		Size: 44.4 MB (44447543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a613a9b4553ca86fac22546f2f79e2ff3d17d8d6aeea8b97d67862a5a40ad8ec`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc000f015361df35e770a910ce03d30691e35aa10d52f4a4f432f183a6c03db`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73eef93b7466c41f22f32d28aae5eb87e1ebc0c4d232c5f5e68c955d0e798dca`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98204131f91a066ec4e6e91dcdb20a24d8906a3eb1636c5f65410ef1223320a`  
		Last Modified: Wed, 19 Aug 2020 23:41:00 GMT  
		Size: 14.7 KB (14701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e47565094be116552f7e584933eaf4996019a03c31dde6260dac8927649f554`  
		Last Modified: Wed, 19 Aug 2020 23:41:54 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641cd36fa2fe9a99c95392a742a434f149b0f0d47c38e89d93f7bdc0f6be4158`  
		Last Modified: Wed, 19 Aug 2020 23:42:44 GMT  
		Size: 347.5 MB (347517279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0194fe719789440160725de86fecf8aaaa6e5dbca937138c8adbc5efc0a2f74`  
		Last Modified: Wed, 19 Aug 2020 23:41:53 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31760f0893db322a4d80531e07f172abf75870473b303dd04639afa0162ab8dc`  
		Last Modified: Wed, 19 Aug 2020 23:41:53 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cae13aa84ae1f3d3d8149eec8b6981a0b92c4baba7a2e8bdeef6146826bb3e3`  
		Last Modified: Wed, 19 Aug 2020 23:41:53 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d3f43060e7726e3090a302e2afbce6541aec9aae3042a8ab41d8b5d5feae98`  
		Last Modified: Wed, 19 Aug 2020 23:41:52 GMT  
		Size: 18.8 KB (18832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db625b47f532d5566eb537980b39a93bf489e05332b3b2ba7a10ae38ea6f3f4`  
		Last Modified: Wed, 19 Aug 2020 23:41:54 GMT  
		Size: 18.8 MB (18803923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0873c814091f0201b321f04b127edcdfd89b1c340fa6aaea30dcb10847496baf`  
		Last Modified: Wed, 19 Aug 2020 23:41:51 GMT  
		Size: 14.3 KB (14298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024890e8d8efc6732e378fb8748bbbf527b148fd5e34110316870f1912e8e45f`  
		Last Modified: Wed, 19 Aug 2020 23:41:52 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2d94b5fb715d8fddbab270af5b430d91b739015dff0954dfdef5b62ec2e70b`  
		Last Modified: Wed, 19 Aug 2020 23:41:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a65db2c454edcea9b55a505c0ee260692c8d315a06ffda7c632d0b9d0c6688`  
		Last Modified: Wed, 19 Aug 2020 23:41:52 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:latest`

```console
$ docker pull php-zendserver@sha256:156eae12dc2703adde99a46b7bbe5188fba92a8ec1ed00e9782bc20296bbef1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:latest` - linux; amd64

```console
$ docker pull php-zendserver@sha256:e85fc05ad0dcb52db2388cb3d1f2ca03d82df0dda56e425900c9d0e34c269a63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.4 MB (491419057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b369291f87b577cadde29a42dc919bc19a56d1ac2712fd8cc80436699a8d4f`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Wed, 19 Aug 2020 21:13:50 GMT
ADD file:5c125b7f411566e9daa738d8cb851098f36197810f06488c2609074296f294b2 in / 
# Wed, 19 Aug 2020 21:13:52 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:13:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:13:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:13:55 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 23:38:46 GMT
RUN apt-get update && apt-get install -y       gnupg
# Wed, 19 Aug 2020 23:38:47 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Wed, 19 Aug 2020 23:38:47 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Wed, 19 Aug 2020 23:40:18 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.4+b392     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Wed, 19 Aug 2020 23:40:19 GMT
ENV ZS_INIT_VERSION=0.3
# Wed, 19 Aug 2020 23:40:19 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Wed, 19 Aug 2020 23:40:19 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Wed, 19 Aug 2020 23:40:20 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Wed, 19 Aug 2020 23:40:20 GMT
WORKDIR /usr/local/zs-init
# Wed, 19 Aug 2020 23:40:30 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Wed, 19 Aug 2020 23:40:30 GMT
COPY dir:7937a6223a1e7805720eca1fbf8c2ccd37938f8f8aa175ae003d409459d49380 in /usr/local/bin 
# Wed, 19 Aug 2020 23:40:30 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Wed, 19 Aug 2020 23:40:31 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Wed, 19 Aug 2020 23:40:31 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Wed, 19 Aug 2020 23:40:32 GMT
EXPOSE 80
# Wed, 19 Aug 2020 23:40:32 GMT
EXPOSE 443
# Wed, 19 Aug 2020 23:40:32 GMT
EXPOSE 10081
# Wed, 19 Aug 2020 23:40:32 GMT
EXPOSE 10082
# Wed, 19 Aug 2020 23:40:32 GMT
WORKDIR /var/www/html
# Wed, 19 Aug 2020 23:40:32 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:f08d8e2a3ba11bea23cf5c17e8e1c620057412ed05c32d1114640e18d6dd0a43`  
		Last Modified: Sat, 08 Aug 2020 12:21:16 GMT  
		Size: 26.7 MB (26700095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9cb2483bd9c5329a44d9c2fe72535625bbd4308bca95785dd58e72c06365`  
		Last Modified: Wed, 19 Aug 2020 21:16:44 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e5ff4c0b1526abf77c236655f21c8f67a23313291c8b970fe6b469549d8153`  
		Last Modified: Wed, 19 Aug 2020 21:16:44 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1860925334f940c3145808527480b4f0cba7f01279087fdb27679e4354fba967`  
		Last Modified: Wed, 19 Aug 2020 21:16:44 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddcc9b3b04d4af7f8cd42b20b4d4eeab5eae7a2062a53b9e99a0c0577b85790`  
		Last Modified: Wed, 19 Aug 2020 23:42:57 GMT  
		Size: 28.3 MB (28267258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3726f4ff6b1261712ea3b160ce213d525018b5875b3afa7f81e9b517d373cbe0`  
		Last Modified: Wed, 19 Aug 2020 23:42:53 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c404c30bcee943368cf18404142c5daea79043736b7f70615cc6ccd3fa2a62`  
		Last Modified: Wed, 19 Aug 2020 23:42:52 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0732084791d941a2b2f0830bfc2ef3c0e99cab7530d5e8200124aad21d993a88`  
		Last Modified: Wed, 19 Aug 2020 23:43:55 GMT  
		Size: 417.6 MB (417572070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73a7901bfecf4ba69c435dd68ac7611416eda5409fff77245428f22f5883524`  
		Last Modified: Wed, 19 Aug 2020 23:42:52 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ed38341a32b31bc4e0792be1cddb2bea646e4a340a4f13806a0d8cc2fdcf8`  
		Last Modified: Wed, 19 Aug 2020 23:42:52 GMT  
		Size: 18.9 KB (18902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77d4388fb3a6eb617d5956ca2d52931504e7e6e9e041e99e4043b06de56593e`  
		Last Modified: Wed, 19 Aug 2020 23:42:54 GMT  
		Size: 18.8 MB (18804061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d5f12d237947485aeadebc5c92e678cd7fc870cd91dd2040ecab1c6157a22a`  
		Last Modified: Wed, 19 Aug 2020 23:42:51 GMT  
		Size: 14.2 KB (14249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd8fe24f26e10152c37029e53bd072eb9b32e08984fb6520171253832caf86c`  
		Last Modified: Wed, 19 Aug 2020 23:42:51 GMT  
		Size: 2.5 KB (2529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13abb24f1ca2419f43a0db5a1886aaa0fd521b3471d6d23ff603f8404c6b9c08`  
		Last Modified: Wed, 19 Aug 2020 23:42:51 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3177cec03260e9f6d9812c47e245d3cfe1ecd837beb98b48053c22449f3860c7`  
		Last Modified: Wed, 19 Aug 2020 23:42:51 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
