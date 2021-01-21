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
$ docker pull php-zendserver@sha256:cb395da0d7905552f1ce7565c7e1868db998d8a8fe8acfd9b9a56a59603bdf34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:2019.0` - linux; amd64

```console
$ docker pull php-zendserver@sha256:d75325f9a5f40459077e8ac9b820d30af19c751bafdf56d7237ea6ebb18a8d4b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.5 MB (492497209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb441f9ef1883978a1e5bb228b3e0f3542aed948c492dcfa39cb81c113840f0`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 01:14:21 GMT
RUN apt-get update && apt-get install -y       gnupg
# Sat, 26 Sep 2020 01:14:21 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Sat, 26 Sep 2020 01:14:22 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Sat, 26 Sep 2020 01:16:01 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.4+b392     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Sat, 26 Sep 2020 01:16:01 GMT
ENV ZS_INIT_VERSION=0.3
# Sat, 26 Sep 2020 01:16:02 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Sat, 26 Sep 2020 01:16:02 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Sat, 26 Sep 2020 01:16:02 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Sat, 26 Sep 2020 01:16:03 GMT
WORKDIR /usr/local/zs-init
# Sat, 26 Sep 2020 01:16:12 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Sat, 26 Sep 2020 01:16:12 GMT
COPY dir:7937a6223a1e7805720eca1fbf8c2ccd37938f8f8aa175ae003d409459d49380 in /usr/local/bin 
# Sat, 26 Sep 2020 01:16:12 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Sat, 26 Sep 2020 01:16:13 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Sat, 26 Sep 2020 01:16:13 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Sat, 26 Sep 2020 01:16:13 GMT
EXPOSE 80
# Sat, 26 Sep 2020 01:16:14 GMT
EXPOSE 443
# Sat, 26 Sep 2020 01:16:14 GMT
EXPOSE 10081
# Sat, 26 Sep 2020 01:16:14 GMT
EXPOSE 10082
# Sat, 26 Sep 2020 01:16:14 GMT
WORKDIR /var/www/html
# Sat, 26 Sep 2020 01:16:14 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d25ea472f1de12f80e58430b1b7f3f00d4bc8e869d7a2936049a748508899d4`  
		Last Modified: Sat, 26 Sep 2020 01:18:37 GMT  
		Size: 28.5 MB (28531625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa4a20a4688fda442a588ed4d1e4ebe5e84282b635b39c7c5b845d93cf5e7c7`  
		Last Modified: Sat, 26 Sep 2020 01:18:34 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee0e3fb707955145a7f055ecf9477f1054eec3c648fadb7607c43b28abf898c`  
		Last Modified: Sat, 26 Sep 2020 01:18:33 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067f6ec87d1a0921a2e201d14bc871de38a28f732249323a61cfc7f7d17084a0`  
		Last Modified: Sat, 26 Sep 2020 01:19:37 GMT  
		Size: 418.1 MB (418117003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964778aa7557739bc53d9237c77300baf80cf7325b2c7448f47a1d77f331eac0`  
		Last Modified: Sat, 26 Sep 2020 01:18:33 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70852fa4a26d14e8fae00524ae46be5e02524d41b3de324866eabd752b4e81`  
		Last Modified: Sat, 26 Sep 2020 01:18:33 GMT  
		Size: 18.9 KB (18902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e0177886aaf1f949cb435cc14b60fd396a5425c503020b86cf1bc645ab577f`  
		Last Modified: Sat, 26 Sep 2020 01:18:35 GMT  
		Size: 19.1 MB (19106769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896f79fecbb3e25efe648cc2772ee81b289154679bba55316bc100b6ac0a7fc9`  
		Last Modified: Sat, 26 Sep 2020 01:18:32 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba471bd014c4ccd8e970aaa4ba565ca1ff341200a3eb2c940f062cd4fc33c36`  
		Last Modified: Sat, 26 Sep 2020 01:18:32 GMT  
		Size: 2.5 KB (2527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18f139f66e26c7937f9ac5fa431af4460309617848cfd61ff67bcf26cf4c30a`  
		Last Modified: Sat, 26 Sep 2020 01:18:32 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4796c9744ddf7d7875ae51305b478ff0bf18021b2fdb55c352a536c1e01fda3`  
		Last Modified: Sat, 26 Sep 2020 01:18:32 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:5.6`

```console
$ docker pull php-zendserver@sha256:6b1c1627a9fa169527ef06f1c47437d79393f8bc03a78478d0d60989039bb537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:e2e599182fdbfd86192846b9d37ca143b84a7e1935cbd0e78ce5e41b975e070e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 MB (315066441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d530a69b49e5a12a175ba030565f3d2716ba4c5508d7b8b92e5ea9f8a2307ba`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 10:13:44 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Thu, 21 Jan 2021 10:13:45 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Thu, 21 Jan 2021 10:13:45 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Thu, 21 Jan 2021 10:15:36 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.15+b8     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Thu, 21 Jan 2021 10:15:37 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Thu, 21 Jan 2021 10:15:38 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Thu, 21 Jan 2021 10:15:39 GMT
RUN /usr/sbin/a2enmod headers
# Thu, 21 Jan 2021 10:15:39 GMT
ENV ZS_INIT_VERSION=0.3
# Thu, 21 Jan 2021 10:15:39 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Thu, 21 Jan 2021 10:15:40 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Thu, 21 Jan 2021 10:15:40 GMT
WORKDIR /usr/local/zs-init
# Thu, 21 Jan 2021 10:15:49 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Thu, 21 Jan 2021 10:15:49 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Thu, 21 Jan 2021 10:15:50 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Thu, 21 Jan 2021 10:15:51 GMT
RUN rm /var/www/html/index.html
# Thu, 21 Jan 2021 10:15:51 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Thu, 21 Jan 2021 10:15:51 GMT
EXPOSE 80
# Thu, 21 Jan 2021 10:15:51 GMT
EXPOSE 443
# Thu, 21 Jan 2021 10:15:51 GMT
EXPOSE 10081
# Thu, 21 Jan 2021 10:15:52 GMT
EXPOSE 10082
# Thu, 21 Jan 2021 10:15:52 GMT
WORKDIR /var/www/html
# Thu, 21 Jan 2021 10:15:52 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bb48c286ca8642e912c6e47938932b20bdb0474be8d62372cf507a876977ce`  
		Last Modified: Thu, 21 Jan 2021 10:18:53 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4b72bff92b6a40bc58f55edff1667301e414af0fea3c3b9abe34e5e7d772ff`  
		Last Modified: Thu, 21 Jan 2021 10:18:53 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6edd9e029a4d7cf8ee7e95e79bcb421423e27c96834fb75fcb68f2e30c394ee0`  
		Last Modified: Thu, 21 Jan 2021 10:18:53 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30bb622f2eafc62de114f99839d7817fc1cfb9a058c66bd72ae21f5afb3dceb9`  
		Last Modified: Thu, 21 Jan 2021 10:19:36 GMT  
		Size: 263.9 MB (263918774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f80b2864db8a24cc419f9951824e4d213a0713b281d458cddd0fca59cddc67`  
		Last Modified: Thu, 21 Jan 2021 10:18:51 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880ed6797b9cf8f290e7f1ded7ed1d791d3e912d6e2a808cdcbd1dff95c752eb`  
		Last Modified: Thu, 21 Jan 2021 10:18:53 GMT  
		Size: 311.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b7e05a0df588c663f196ce8c9d481d3551f835b37ba1982f567465889ce431`  
		Last Modified: Thu, 21 Jan 2021 10:18:52 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a4cd52da033d8566989aa04091905ac756b20ae835269abdc84347f28b467f`  
		Last Modified: Thu, 21 Jan 2021 10:18:50 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94179d46b26c230a37af58a50f5a2afa734ce20bf6952b77b72bc8d2242321e3`  
		Last Modified: Thu, 21 Jan 2021 10:18:49 GMT  
		Size: 5.1 MB (5131538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac5064c621f30273c4a3b190a2914b8b432e2f7b2fd77ce973dd5f093529e10`  
		Last Modified: Thu, 21 Jan 2021 10:18:49 GMT  
		Size: 13.4 KB (13351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa5b0b1eaeda6526740b64efd3fdafb13dd5b6a436fef752da424eea8883de2`  
		Last Modified: Thu, 21 Jan 2021 10:18:49 GMT  
		Size: 2.5 KB (2535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b1c1215b4fb5b8d5bca7275300429271d52202c8eff40398dbdec8992f2135`  
		Last Modified: Thu, 21 Jan 2021 10:18:49 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f112310c236e625eb024401de38e3f18d5493f0fe40998dec7021c0a6f1e5936`  
		Last Modified: Thu, 21 Jan 2021 10:18:48 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5`

```console
$ docker pull php-zendserver@sha256:6b1c1627a9fa169527ef06f1c47437d79393f8bc03a78478d0d60989039bb537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:8.5` - linux; amd64

```console
$ docker pull php-zendserver@sha256:e2e599182fdbfd86192846b9d37ca143b84a7e1935cbd0e78ce5e41b975e070e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 MB (315066441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d530a69b49e5a12a175ba030565f3d2716ba4c5508d7b8b92e5ea9f8a2307ba`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 10:13:44 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Thu, 21 Jan 2021 10:13:45 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Thu, 21 Jan 2021 10:13:45 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Thu, 21 Jan 2021 10:15:36 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.15+b8     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Thu, 21 Jan 2021 10:15:37 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Thu, 21 Jan 2021 10:15:38 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Thu, 21 Jan 2021 10:15:39 GMT
RUN /usr/sbin/a2enmod headers
# Thu, 21 Jan 2021 10:15:39 GMT
ENV ZS_INIT_VERSION=0.3
# Thu, 21 Jan 2021 10:15:39 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Thu, 21 Jan 2021 10:15:40 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Thu, 21 Jan 2021 10:15:40 GMT
WORKDIR /usr/local/zs-init
# Thu, 21 Jan 2021 10:15:49 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Thu, 21 Jan 2021 10:15:49 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Thu, 21 Jan 2021 10:15:50 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Thu, 21 Jan 2021 10:15:51 GMT
RUN rm /var/www/html/index.html
# Thu, 21 Jan 2021 10:15:51 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Thu, 21 Jan 2021 10:15:51 GMT
EXPOSE 80
# Thu, 21 Jan 2021 10:15:51 GMT
EXPOSE 443
# Thu, 21 Jan 2021 10:15:51 GMT
EXPOSE 10081
# Thu, 21 Jan 2021 10:15:52 GMT
EXPOSE 10082
# Thu, 21 Jan 2021 10:15:52 GMT
WORKDIR /var/www/html
# Thu, 21 Jan 2021 10:15:52 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bb48c286ca8642e912c6e47938932b20bdb0474be8d62372cf507a876977ce`  
		Last Modified: Thu, 21 Jan 2021 10:18:53 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4b72bff92b6a40bc58f55edff1667301e414af0fea3c3b9abe34e5e7d772ff`  
		Last Modified: Thu, 21 Jan 2021 10:18:53 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6edd9e029a4d7cf8ee7e95e79bcb421423e27c96834fb75fcb68f2e30c394ee0`  
		Last Modified: Thu, 21 Jan 2021 10:18:53 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30bb622f2eafc62de114f99839d7817fc1cfb9a058c66bd72ae21f5afb3dceb9`  
		Last Modified: Thu, 21 Jan 2021 10:19:36 GMT  
		Size: 263.9 MB (263918774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f80b2864db8a24cc419f9951824e4d213a0713b281d458cddd0fca59cddc67`  
		Last Modified: Thu, 21 Jan 2021 10:18:51 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880ed6797b9cf8f290e7f1ded7ed1d791d3e912d6e2a808cdcbd1dff95c752eb`  
		Last Modified: Thu, 21 Jan 2021 10:18:53 GMT  
		Size: 311.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b7e05a0df588c663f196ce8c9d481d3551f835b37ba1982f567465889ce431`  
		Last Modified: Thu, 21 Jan 2021 10:18:52 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a4cd52da033d8566989aa04091905ac756b20ae835269abdc84347f28b467f`  
		Last Modified: Thu, 21 Jan 2021 10:18:50 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94179d46b26c230a37af58a50f5a2afa734ce20bf6952b77b72bc8d2242321e3`  
		Last Modified: Thu, 21 Jan 2021 10:18:49 GMT  
		Size: 5.1 MB (5131538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac5064c621f30273c4a3b190a2914b8b432e2f7b2fd77ce973dd5f093529e10`  
		Last Modified: Thu, 21 Jan 2021 10:18:49 GMT  
		Size: 13.4 KB (13351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa5b0b1eaeda6526740b64efd3fdafb13dd5b6a436fef752da424eea8883de2`  
		Last Modified: Thu, 21 Jan 2021 10:18:49 GMT  
		Size: 2.5 KB (2535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b1c1215b4fb5b8d5bca7275300429271d52202c8eff40398dbdec8992f2135`  
		Last Modified: Thu, 21 Jan 2021 10:18:49 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f112310c236e625eb024401de38e3f18d5493f0fe40998dec7021c0a6f1e5936`  
		Last Modified: Thu, 21 Jan 2021 10:18:48 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5-php5.6`

```console
$ docker pull php-zendserver@sha256:6b1c1627a9fa169527ef06f1c47437d79393f8bc03a78478d0d60989039bb537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:8.5-php5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:e2e599182fdbfd86192846b9d37ca143b84a7e1935cbd0e78ce5e41b975e070e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 MB (315066441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d530a69b49e5a12a175ba030565f3d2716ba4c5508d7b8b92e5ea9f8a2307ba`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 10:13:44 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Thu, 21 Jan 2021 10:13:45 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Thu, 21 Jan 2021 10:13:45 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Thu, 21 Jan 2021 10:15:36 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.15+b8     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Thu, 21 Jan 2021 10:15:37 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Thu, 21 Jan 2021 10:15:38 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Thu, 21 Jan 2021 10:15:39 GMT
RUN /usr/sbin/a2enmod headers
# Thu, 21 Jan 2021 10:15:39 GMT
ENV ZS_INIT_VERSION=0.3
# Thu, 21 Jan 2021 10:15:39 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Thu, 21 Jan 2021 10:15:40 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Thu, 21 Jan 2021 10:15:40 GMT
WORKDIR /usr/local/zs-init
# Thu, 21 Jan 2021 10:15:49 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Thu, 21 Jan 2021 10:15:49 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Thu, 21 Jan 2021 10:15:50 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Thu, 21 Jan 2021 10:15:51 GMT
RUN rm /var/www/html/index.html
# Thu, 21 Jan 2021 10:15:51 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Thu, 21 Jan 2021 10:15:51 GMT
EXPOSE 80
# Thu, 21 Jan 2021 10:15:51 GMT
EXPOSE 443
# Thu, 21 Jan 2021 10:15:51 GMT
EXPOSE 10081
# Thu, 21 Jan 2021 10:15:52 GMT
EXPOSE 10082
# Thu, 21 Jan 2021 10:15:52 GMT
WORKDIR /var/www/html
# Thu, 21 Jan 2021 10:15:52 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bb48c286ca8642e912c6e47938932b20bdb0474be8d62372cf507a876977ce`  
		Last Modified: Thu, 21 Jan 2021 10:18:53 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4b72bff92b6a40bc58f55edff1667301e414af0fea3c3b9abe34e5e7d772ff`  
		Last Modified: Thu, 21 Jan 2021 10:18:53 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6edd9e029a4d7cf8ee7e95e79bcb421423e27c96834fb75fcb68f2e30c394ee0`  
		Last Modified: Thu, 21 Jan 2021 10:18:53 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30bb622f2eafc62de114f99839d7817fc1cfb9a058c66bd72ae21f5afb3dceb9`  
		Last Modified: Thu, 21 Jan 2021 10:19:36 GMT  
		Size: 263.9 MB (263918774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f80b2864db8a24cc419f9951824e4d213a0713b281d458cddd0fca59cddc67`  
		Last Modified: Thu, 21 Jan 2021 10:18:51 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880ed6797b9cf8f290e7f1ded7ed1d791d3e912d6e2a808cdcbd1dff95c752eb`  
		Last Modified: Thu, 21 Jan 2021 10:18:53 GMT  
		Size: 311.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b7e05a0df588c663f196ce8c9d481d3551f835b37ba1982f567465889ce431`  
		Last Modified: Thu, 21 Jan 2021 10:18:52 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a4cd52da033d8566989aa04091905ac756b20ae835269abdc84347f28b467f`  
		Last Modified: Thu, 21 Jan 2021 10:18:50 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94179d46b26c230a37af58a50f5a2afa734ce20bf6952b77b72bc8d2242321e3`  
		Last Modified: Thu, 21 Jan 2021 10:18:49 GMT  
		Size: 5.1 MB (5131538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac5064c621f30273c4a3b190a2914b8b432e2f7b2fd77ce973dd5f093529e10`  
		Last Modified: Thu, 21 Jan 2021 10:18:49 GMT  
		Size: 13.4 KB (13351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa5b0b1eaeda6526740b64efd3fdafb13dd5b6a436fef752da424eea8883de2`  
		Last Modified: Thu, 21 Jan 2021 10:18:49 GMT  
		Size: 2.5 KB (2535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b1c1215b4fb5b8d5bca7275300429271d52202c8eff40398dbdec8992f2135`  
		Last Modified: Thu, 21 Jan 2021 10:18:49 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f112310c236e625eb024401de38e3f18d5493f0fe40998dec7021c0a6f1e5936`  
		Last Modified: Thu, 21 Jan 2021 10:18:48 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:9.1`

```console
$ docker pull php-zendserver@sha256:08aca877bba420bbb3305c289efe9ec79dbf0990f551d32f4343f644d60cdc68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:9.1` - linux; amd64

```console
$ docker pull php-zendserver@sha256:f0191d5705a1fc518ff1ea62106c6256a9455124eadebe5315205d22119cb28d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.3 MB (403323532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4734e025669280a57f79c8a2b109863decdea4952e6c83255e1083328ce6b5`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 10:13:44 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Thu, 21 Jan 2021 10:16:00 GMT
COPY file:0d4830b5060fb75cec6a47b30d343d82f9c3d6f95f20c11635618b93dedb5720 in /etc/apt/sources.list.d/zend-server.list 
# Thu, 21 Jan 2021 10:17:29 GMT
RUN apt-get update     && apt-get install -y       curl       libmysqlclient20       unzip       git       zend-server-php-7.1=9.1.10+b202     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Thu, 21 Jan 2021 10:17:30 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Thu, 21 Jan 2021 10:17:31 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Thu, 21 Jan 2021 10:17:32 GMT
RUN /usr/sbin/a2enmod headers
# Thu, 21 Jan 2021 10:17:32 GMT
ENV ZS_INIT_VERSION=0.3
# Thu, 21 Jan 2021 10:17:32 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Thu, 21 Jan 2021 10:17:33 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Thu, 21 Jan 2021 10:17:33 GMT
WORKDIR /usr/local/zs-init
# Thu, 21 Jan 2021 10:17:42 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Thu, 21 Jan 2021 10:17:43 GMT
COPY dir:864637d3fa0817ce3be0c7e34e1298851fa2ea4cfb86583e2ec811f00c6a95fd in /usr/local/bin 
# Thu, 21 Jan 2021 10:17:43 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Thu, 21 Jan 2021 10:17:44 GMT
RUN rm /var/www/html/index.html
# Thu, 21 Jan 2021 10:17:44 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Thu, 21 Jan 2021 10:17:44 GMT
EXPOSE 80
# Thu, 21 Jan 2021 10:17:44 GMT
EXPOSE 443
# Thu, 21 Jan 2021 10:17:45 GMT
EXPOSE 10081
# Thu, 21 Jan 2021 10:17:45 GMT
EXPOSE 10082
# Thu, 21 Jan 2021 10:17:45 GMT
WORKDIR /var/www/html
# Thu, 21 Jan 2021 10:17:45 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bb48c286ca8642e912c6e47938932b20bdb0474be8d62372cf507a876977ce`  
		Last Modified: Thu, 21 Jan 2021 10:18:53 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f39511b5c8ea19e57da59bec59babd3f9dc977f37b73a9aff87c6d95e177c73`  
		Last Modified: Thu, 21 Jan 2021 10:19:54 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65157f10d06848e5a861f2027c2b126d8a838284a43c27b4accc438d40ab5677`  
		Last Modified: Thu, 21 Jan 2021 10:20:43 GMT  
		Size: 352.2 MB (352169011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ee6849b3ded929e1fcb40ecbceac066e96da0b527deb047f4059f08ee4d5a7`  
		Last Modified: Thu, 21 Jan 2021 10:19:54 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7370d046f91a211a88cc46626ca7c7f878a9df7517efc238610139668a82c9`  
		Last Modified: Thu, 21 Jan 2021 10:19:52 GMT  
		Size: 312.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc509f3b75579bba43fe0a56e649583523395bd827430b9168e8264e15ee9e7`  
		Last Modified: Thu, 21 Jan 2021 10:19:50 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814dd68bb3cff77f8aee8e500c112e1c8c441c8a21a67a3f9da2276b0123776b`  
		Last Modified: Thu, 21 Jan 2021 10:19:53 GMT  
		Size: 18.8 KB (18832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ade4ed56a46698dd4c124d8e5cdb9284ef063fdc5105ec1ad407ca6d80889ac`  
		Last Modified: Thu, 21 Jan 2021 10:19:50 GMT  
		Size: 5.1 MB (5137723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce8cc361b33db7d36a1db8aa7ac7fc547b85115a2620fb904ed16765fee3aa6`  
		Last Modified: Thu, 21 Jan 2021 10:19:49 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aead5b4ce2f356bd745428e611a45a48bd2c120396e9af6b33f72bf3e6436a1`  
		Last Modified: Thu, 21 Jan 2021 10:19:49 GMT  
		Size: 2.5 KB (2530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9481c8710ae49f7d6481e4d32d94086645539f7539480692d4319095e5621410`  
		Last Modified: Thu, 21 Jan 2021 10:19:50 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9623167d89e1cdbaa4ccd0eb15d5b284396e8848b4d62628ba20cdd7b4c282`  
		Last Modified: Thu, 21 Jan 2021 10:19:49 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:latest`

```console
$ docker pull php-zendserver@sha256:cb395da0d7905552f1ce7565c7e1868db998d8a8fe8acfd9b9a56a59603bdf34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:latest` - linux; amd64

```console
$ docker pull php-zendserver@sha256:d75325f9a5f40459077e8ac9b820d30af19c751bafdf56d7237ea6ebb18a8d4b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.5 MB (492497209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb441f9ef1883978a1e5bb228b3e0f3542aed948c492dcfa39cb81c113840f0`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 01:14:21 GMT
RUN apt-get update && apt-get install -y       gnupg
# Sat, 26 Sep 2020 01:14:21 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Sat, 26 Sep 2020 01:14:22 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Sat, 26 Sep 2020 01:16:01 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.4+b392     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Sat, 26 Sep 2020 01:16:01 GMT
ENV ZS_INIT_VERSION=0.3
# Sat, 26 Sep 2020 01:16:02 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Sat, 26 Sep 2020 01:16:02 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Sat, 26 Sep 2020 01:16:02 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Sat, 26 Sep 2020 01:16:03 GMT
WORKDIR /usr/local/zs-init
# Sat, 26 Sep 2020 01:16:12 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Sat, 26 Sep 2020 01:16:12 GMT
COPY dir:7937a6223a1e7805720eca1fbf8c2ccd37938f8f8aa175ae003d409459d49380 in /usr/local/bin 
# Sat, 26 Sep 2020 01:16:12 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Sat, 26 Sep 2020 01:16:13 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Sat, 26 Sep 2020 01:16:13 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Sat, 26 Sep 2020 01:16:13 GMT
EXPOSE 80
# Sat, 26 Sep 2020 01:16:14 GMT
EXPOSE 443
# Sat, 26 Sep 2020 01:16:14 GMT
EXPOSE 10081
# Sat, 26 Sep 2020 01:16:14 GMT
EXPOSE 10082
# Sat, 26 Sep 2020 01:16:14 GMT
WORKDIR /var/www/html
# Sat, 26 Sep 2020 01:16:14 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d25ea472f1de12f80e58430b1b7f3f00d4bc8e869d7a2936049a748508899d4`  
		Last Modified: Sat, 26 Sep 2020 01:18:37 GMT  
		Size: 28.5 MB (28531625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa4a20a4688fda442a588ed4d1e4ebe5e84282b635b39c7c5b845d93cf5e7c7`  
		Last Modified: Sat, 26 Sep 2020 01:18:34 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee0e3fb707955145a7f055ecf9477f1054eec3c648fadb7607c43b28abf898c`  
		Last Modified: Sat, 26 Sep 2020 01:18:33 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067f6ec87d1a0921a2e201d14bc871de38a28f732249323a61cfc7f7d17084a0`  
		Last Modified: Sat, 26 Sep 2020 01:19:37 GMT  
		Size: 418.1 MB (418117003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964778aa7557739bc53d9237c77300baf80cf7325b2c7448f47a1d77f331eac0`  
		Last Modified: Sat, 26 Sep 2020 01:18:33 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70852fa4a26d14e8fae00524ae46be5e02524d41b3de324866eabd752b4e81`  
		Last Modified: Sat, 26 Sep 2020 01:18:33 GMT  
		Size: 18.9 KB (18902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e0177886aaf1f949cb435cc14b60fd396a5425c503020b86cf1bc645ab577f`  
		Last Modified: Sat, 26 Sep 2020 01:18:35 GMT  
		Size: 19.1 MB (19106769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896f79fecbb3e25efe648cc2772ee81b289154679bba55316bc100b6ac0a7fc9`  
		Last Modified: Sat, 26 Sep 2020 01:18:32 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba471bd014c4ccd8e970aaa4ba565ca1ff341200a3eb2c940f062cd4fc33c36`  
		Last Modified: Sat, 26 Sep 2020 01:18:32 GMT  
		Size: 2.5 KB (2527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18f139f66e26c7937f9ac5fa431af4460309617848cfd61ff67bcf26cf4c30a`  
		Last Modified: Sat, 26 Sep 2020 01:18:32 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4796c9744ddf7d7875ae51305b478ff0bf18021b2fdb55c352a536c1e01fda3`  
		Last Modified: Sat, 26 Sep 2020 01:18:32 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
