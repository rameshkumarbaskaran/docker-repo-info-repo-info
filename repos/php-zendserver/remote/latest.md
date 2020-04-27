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
