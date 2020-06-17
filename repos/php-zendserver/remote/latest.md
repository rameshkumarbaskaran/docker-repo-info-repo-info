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
