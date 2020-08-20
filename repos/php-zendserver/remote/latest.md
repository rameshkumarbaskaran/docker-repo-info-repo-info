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
