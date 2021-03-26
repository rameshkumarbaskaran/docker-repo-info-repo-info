## `php-zendserver:latest`

```console
$ docker pull php-zendserver@sha256:d6d8150ca026599fc9cfcd43bf4a400a69d65d843ae2b2ee8c38fa4655e9b8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:latest` - linux; amd64

```console
$ docker pull php-zendserver@sha256:7ae43d5f682b305bd6bf7ecba54e0be70588e9b8e455de81dd23a0117eac27a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.3 MB (482291313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a99bb4946e695c411a209507267e76309635f1884eee72178f185e98ff281a`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 12:19:48 GMT
RUN apt-get update && apt-get install -y       gnupg
# Fri, 26 Mar 2021 12:19:49 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 26 Mar 2021 12:19:49 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 26 Mar 2021 12:21:43 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.7+b403     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 26 Mar 2021 12:21:46 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 26 Mar 2021 12:21:46 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 26 Mar 2021 12:21:47 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Fri, 26 Mar 2021 12:21:48 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Fri, 26 Mar 2021 12:21:48 GMT
WORKDIR /usr/local/zs-init
# Fri, 26 Mar 2021 12:21:53 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Fri, 26 Mar 2021 12:21:53 GMT
COPY dir:eecd98e9ebf1c61a12ae67558eb2a6ce846b9ebfadabbf08503e90b3e30d9496 in /usr/local/bin 
# Fri, 26 Mar 2021 12:21:54 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 26 Mar 2021 12:21:54 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Fri, 26 Mar 2021 12:21:55 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 26 Mar 2021 12:21:55 GMT
EXPOSE 80
# Fri, 26 Mar 2021 12:21:55 GMT
EXPOSE 443
# Fri, 26 Mar 2021 12:21:55 GMT
EXPOSE 10081
# Fri, 26 Mar 2021 12:21:55 GMT
EXPOSE 10082
# Fri, 26 Mar 2021 12:21:56 GMT
WORKDIR /var/www/html
# Fri, 26 Mar 2021 12:21:56 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09e9fb21ea14f3d4fd3e0eb488f5fbf7e4b0ab58cdb70cb7caa708fe04c3ed8`  
		Last Modified: Fri, 26 Mar 2021 12:24:49 GMT  
		Size: 32.3 MB (32313870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d842d28e5b2934da62e3393a05d3ca8905f51b2abf4652e0098bd4f8cb5c8570`  
		Last Modified: Fri, 26 Mar 2021 12:24:43 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1bef7a9258fbbc984d3d84da120330fb50816634221752630f98e20d9de157`  
		Last Modified: Fri, 26 Mar 2021 12:24:43 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2430d61861afed165bec80e5395d05d244229764018cabf8bb8667a41762a3`  
		Last Modified: Fri, 26 Mar 2021 12:26:02 GMT  
		Size: 418.1 MB (418085079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e994fa72fcecb985b9f316c77dfb9ff6803c74cb9fc342f2b61a8b4e51a6e052`  
		Last Modified: Fri, 26 Mar 2021 12:24:42 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6d603ea63961f890aceb5d9626d1d4457ae482f29d27ad7f1ed2ebe398fa99`  
		Last Modified: Fri, 26 Mar 2021 12:24:42 GMT  
		Size: 18.9 KB (18928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6084673048196810d230d49e5f235fa815c086d8468451e5302f7f27492ecf50`  
		Last Modified: Fri, 26 Mar 2021 12:24:40 GMT  
		Size: 5.1 MB (5141254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2951fc02fdf1e381fc6a8ef9e59c421b5bab3e4bcc5c3bb566268c692854bbe`  
		Last Modified: Fri, 26 Mar 2021 12:24:40 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7e9ccf42ae3ade52793d46430d753b09efb4c587f3d0064f3db6de3da3b006`  
		Last Modified: Fri, 26 Mar 2021 12:24:39 GMT  
		Size: 2.6 KB (2556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b953d70d86e29477f45306d26c65f39f1c3bbed4b69c5a38629eacd8d1b2f8`  
		Last Modified: Fri, 26 Mar 2021 12:24:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc2296c2ef763ad8cf55b5d2ff3d435857fa215481f2ea84a6ef49de24f27cf`  
		Last Modified: Fri, 26 Mar 2021 12:24:39 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
