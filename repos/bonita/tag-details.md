<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `bonita`

-	[`bonita:7.10`](#bonita710)
-	[`bonita:7.10.6`](#bonita7106)
-	[`bonita:7.11`](#bonita711)
-	[`bonita:7.11.3`](#bonita7113)
-	[`bonita:7.9`](#bonita79)
-	[`bonita:7.9.5`](#bonita795)
-	[`bonita:latest`](#bonitalatest)

## `bonita:7.10`

```console
$ docker pull bonita@sha256:8823019d061ebc25fea3de870e342b2bbd4fbdad1ac00fa1c84d0f5a13aa95ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.10` - linux; amd64

```console
$ docker pull bonita@sha256:ed56b3382c531fcad472135c5b5013d440b6719fc113396af13d6ff8c4ae3ad1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227258338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad0884bd9946aaa33e4bd3c30ec54194282359b3aec75a2d069078a637e4b5f`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Fri, 25 Sep 2020 23:41:10 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 25 Sep 2020 23:41:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:41:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 25 Sep 2020 23:41:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 25 Sep 2020 23:41:50 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 25 Sep 2020 23:41:50 GMT
ARG BONITA_VERSION
# Fri, 25 Sep 2020 23:41:51 GMT
ARG BONITA_SHA256
# Fri, 25 Sep 2020 23:42:15 GMT
ARG BASE_URL
# Fri, 25 Sep 2020 23:42:15 GMT
ARG BONITA_URL
# Fri, 02 Oct 2020 21:19:38 GMT
ENV BONITA_VERSION=7.10.6
# Fri, 02 Oct 2020 21:19:38 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Fri, 02 Oct 2020 21:19:39 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Oct 2020 21:19:39 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Fri, 02 Oct 2020 21:19:40 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 02 Oct 2020 21:19:42 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 02 Oct 2020 21:19:44 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 02 Oct 2020 21:19:45 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 02 Oct 2020 21:19:45 GMT
VOLUME [/opt/bonita]
# Fri, 02 Oct 2020 21:19:46 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Fri, 02 Oct 2020 21:19:46 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 02 Oct 2020 21:19:46 GMT
EXPOSE 8080
# Fri, 02 Oct 2020 21:19:46 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:16b26225e2399009e0af570eebb768bfcbe84cb6c29b1904acdde559aa23f5ea`  
		Last Modified: Fri, 25 Sep 2020 23:43:07 GMT  
		Size: 102.0 MB (101998153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a756bb5a69747c3a85260b46c657b99989e66e321215246e71037a10243f35`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2a72327f28ef87b1a7d940367fe2bd4bde9b327a8efe0d35fd44b7d5c19ab6`  
		Last Modified: Fri, 25 Sep 2020 23:42:49 GMT  
		Size: 1.9 KB (1913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf8ca91d922430c6fecd7439843b96ee71b8d1116fcf27a619ef4ff6b5b5f8e`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 572.4 KB (572374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e8c4364b7e29135cab8b3c39ee8fc8e1cb0a9b06abb413ad8be52e79505dee`  
		Last Modified: Fri, 02 Oct 2020 21:20:13 GMT  
		Size: 98.0 MB (97973905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a72cac0a439bfcc5517ba808040d66a32838c95dcf76008a949272fcec481a`  
		Last Modified: Fri, 02 Oct 2020 21:20:08 GMT  
		Size: 7.6 KB (7623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d744d2f375764cb75665570a25321939441290d01ea744395b112f8db6d23c`  
		Last Modified: Fri, 02 Oct 2020 21:20:09 GMT  
		Size: 1.6 KB (1622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:42bc0ef22551d968160b2428546be1daa32cd72288121939c654116adc136d8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.8 MB (215779953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71156e90cf034912a9496f1a6188612487d305536b31fdf02b9225385edc7ddc`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 25 Nov 2020 22:42:53 GMT
ADD file:e5b221023382c9e42b8558f8887f8317fe7e9759f59feb1799548aed9236e99b in / 
# Wed, 25 Nov 2020 22:42:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:42:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:43:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:43:01 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:19:52 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Wed, 25 Nov 2020 23:21:00 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:21:05 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 25 Nov 2020 23:21:09 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 25 Nov 2020 23:21:12 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 25 Nov 2020 23:21:13 GMT
ARG BONITA_VERSION
# Wed, 25 Nov 2020 23:21:13 GMT
ARG BONITA_SHA256
# Wed, 25 Nov 2020 23:21:55 GMT
ARG BASE_URL
# Wed, 25 Nov 2020 23:21:56 GMT
ARG BONITA_URL
# Wed, 25 Nov 2020 23:21:57 GMT
ENV BONITA_VERSION=7.10.6
# Wed, 25 Nov 2020 23:21:58 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Wed, 25 Nov 2020 23:21:59 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 25 Nov 2020 23:22:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Wed, 25 Nov 2020 23:22:02 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Wed, 25 Nov 2020 23:22:10 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Wed, 25 Nov 2020 23:22:13 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Wed, 25 Nov 2020 23:22:15 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Wed, 25 Nov 2020 23:22:16 GMT
VOLUME [/opt/bonita]
# Wed, 25 Nov 2020 23:22:17 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Wed, 25 Nov 2020 23:22:18 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Wed, 25 Nov 2020 23:22:18 GMT
EXPOSE 8080
# Wed, 25 Nov 2020 23:22:19 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:04da93b342eb651d6b94c74a934a3290697573a907fa0a06067b538095601745`  
		Last Modified: Thu, 19 Nov 2020 16:25:04 GMT  
		Size: 23.7 MB (23733196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b235194751dee33624fc154603f7e25ecdfbb02538fb7d55fa796df9afa95fee`  
		Last Modified: Wed, 25 Nov 2020 22:44:43 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606a67bb8db9a1111022bdc6406442e11c1a66653136c5c777114bf67b61038a`  
		Last Modified: Wed, 25 Nov 2020 22:44:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963a3771da753196019b9ec7438846e332077edafc8fbb958d4b9875a6f8c08c`  
		Last Modified: Wed, 25 Nov 2020 23:24:30 GMT  
		Size: 93.5 MB (93518573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa886be96ef436069e063cfc38c29e97e791aac74a2de17827a9037938c81ecc`  
		Last Modified: Wed, 25 Nov 2020 23:24:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c7801c8831c3bfa0f34a65087747d59edc5c1bb2ef08800eb9c011f9397951`  
		Last Modified: Wed, 25 Nov 2020 23:24:06 GMT  
		Size: 1.9 KB (1915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1dd9294d182f0450f4cb8a4bfb1337db0fd360fcad0286b5868fa2872e8512c`  
		Last Modified: Wed, 25 Nov 2020 23:24:06 GMT  
		Size: 541.8 KB (541821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd3480a82b7f774ecca18c24995dbd0df347570225d236932816e5cd83c112a`  
		Last Modified: Wed, 25 Nov 2020 23:24:47 GMT  
		Size: 98.0 MB (97973947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f809581897998fc12f0b3bf70aa5f6a2347756cc1b14804d94d11b11e16c4d83`  
		Last Modified: Wed, 25 Nov 2020 23:24:40 GMT  
		Size: 7.7 KB (7650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c8ff24730358f1d9ad8203316a43d02ebe0ba95b73a7dd7b2e921575220f5`  
		Last Modified: Wed, 25 Nov 2020 23:24:40 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10` - linux; ppc64le

```console
$ docker pull bonita@sha256:ccda138193c6219e07c827cb18fb84e3f64ed51631191344aa0885f34d0ba462
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.0 MB (223954482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53504672add2122833646f2ddb0798f976993198a3686bb3ab1ebe28f42d2d89`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 03:25:11 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Sat, 26 Sep 2020 03:29:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 03:30:04 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 26 Sep 2020 03:30:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 26 Sep 2020 03:30:33 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 26 Sep 2020 03:30:41 GMT
ARG BONITA_VERSION
# Sat, 26 Sep 2020 03:30:48 GMT
ARG BONITA_SHA256
# Sat, 26 Sep 2020 03:32:40 GMT
ARG BASE_URL
# Sat, 26 Sep 2020 03:32:44 GMT
ARG BONITA_URL
# Fri, 02 Oct 2020 21:18:25 GMT
ENV BONITA_VERSION=7.10.6
# Fri, 02 Oct 2020 21:18:34 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Fri, 02 Oct 2020 21:18:42 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Oct 2020 21:18:52 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Fri, 02 Oct 2020 21:19:09 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 02 Oct 2020 21:19:31 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 02 Oct 2020 21:19:46 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 02 Oct 2020 21:20:01 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 02 Oct 2020 21:20:11 GMT
VOLUME [/opt/bonita]
# Fri, 02 Oct 2020 21:20:13 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Fri, 02 Oct 2020 21:20:17 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 02 Oct 2020 21:20:21 GMT
EXPOSE 8080
# Fri, 02 Oct 2020 21:20:27 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36f615abc241aa46a9f641088be9733489aa54ecdd7656aabbebc59e8babff4`  
		Last Modified: Sat, 26 Sep 2020 03:36:32 GMT  
		Size: 95.0 MB (95018057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7815598247ab5a7495520c70706e93222c19f009b14fa035185abb72878b65fb`  
		Last Modified: Sat, 26 Sep 2020 03:36:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b957f0e55214fe990421d5d9157a1e2b99678772069be9e9b93204567ce98e8`  
		Last Modified: Sat, 26 Sep 2020 03:36:09 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55cf6fc034ce3ae81db3086f9f903bad18df306e4078a9c4a542cf09dcf0773`  
		Last Modified: Sat, 26 Sep 2020 03:36:10 GMT  
		Size: 541.5 KB (541548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430a976f7a64af7c1ad0bd07fb507db383af946510dde0d9153227a59e13dc52`  
		Last Modified: Fri, 02 Oct 2020 21:23:30 GMT  
		Size: 98.0 MB (97973961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a853809ef5ddfb0f940a8cb762287fee5df363a3571236f16478ea0ede2605`  
		Last Modified: Fri, 02 Oct 2020 21:23:23 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b96585853cc722e35c073143958e441b5313c84bf83db33d9c9dfee2d792695`  
		Last Modified: Fri, 02 Oct 2020 21:23:23 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.10.6`

```console
$ docker pull bonita@sha256:8823019d061ebc25fea3de870e342b2bbd4fbdad1ac00fa1c84d0f5a13aa95ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.10.6` - linux; amd64

```console
$ docker pull bonita@sha256:ed56b3382c531fcad472135c5b5013d440b6719fc113396af13d6ff8c4ae3ad1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227258338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad0884bd9946aaa33e4bd3c30ec54194282359b3aec75a2d069078a637e4b5f`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Fri, 25 Sep 2020 23:41:10 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 25 Sep 2020 23:41:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:41:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 25 Sep 2020 23:41:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 25 Sep 2020 23:41:50 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 25 Sep 2020 23:41:50 GMT
ARG BONITA_VERSION
# Fri, 25 Sep 2020 23:41:51 GMT
ARG BONITA_SHA256
# Fri, 25 Sep 2020 23:42:15 GMT
ARG BASE_URL
# Fri, 25 Sep 2020 23:42:15 GMT
ARG BONITA_URL
# Fri, 02 Oct 2020 21:19:38 GMT
ENV BONITA_VERSION=7.10.6
# Fri, 02 Oct 2020 21:19:38 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Fri, 02 Oct 2020 21:19:39 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Oct 2020 21:19:39 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Fri, 02 Oct 2020 21:19:40 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 02 Oct 2020 21:19:42 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 02 Oct 2020 21:19:44 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 02 Oct 2020 21:19:45 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 02 Oct 2020 21:19:45 GMT
VOLUME [/opt/bonita]
# Fri, 02 Oct 2020 21:19:46 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Fri, 02 Oct 2020 21:19:46 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 02 Oct 2020 21:19:46 GMT
EXPOSE 8080
# Fri, 02 Oct 2020 21:19:46 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:16b26225e2399009e0af570eebb768bfcbe84cb6c29b1904acdde559aa23f5ea`  
		Last Modified: Fri, 25 Sep 2020 23:43:07 GMT  
		Size: 102.0 MB (101998153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a756bb5a69747c3a85260b46c657b99989e66e321215246e71037a10243f35`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2a72327f28ef87b1a7d940367fe2bd4bde9b327a8efe0d35fd44b7d5c19ab6`  
		Last Modified: Fri, 25 Sep 2020 23:42:49 GMT  
		Size: 1.9 KB (1913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf8ca91d922430c6fecd7439843b96ee71b8d1116fcf27a619ef4ff6b5b5f8e`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 572.4 KB (572374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e8c4364b7e29135cab8b3c39ee8fc8e1cb0a9b06abb413ad8be52e79505dee`  
		Last Modified: Fri, 02 Oct 2020 21:20:13 GMT  
		Size: 98.0 MB (97973905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a72cac0a439bfcc5517ba808040d66a32838c95dcf76008a949272fcec481a`  
		Last Modified: Fri, 02 Oct 2020 21:20:08 GMT  
		Size: 7.6 KB (7623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d744d2f375764cb75665570a25321939441290d01ea744395b112f8db6d23c`  
		Last Modified: Fri, 02 Oct 2020 21:20:09 GMT  
		Size: 1.6 KB (1622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10.6` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:42bc0ef22551d968160b2428546be1daa32cd72288121939c654116adc136d8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.8 MB (215779953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71156e90cf034912a9496f1a6188612487d305536b31fdf02b9225385edc7ddc`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 25 Nov 2020 22:42:53 GMT
ADD file:e5b221023382c9e42b8558f8887f8317fe7e9759f59feb1799548aed9236e99b in / 
# Wed, 25 Nov 2020 22:42:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:42:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:43:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:43:01 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:19:52 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Wed, 25 Nov 2020 23:21:00 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:21:05 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 25 Nov 2020 23:21:09 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 25 Nov 2020 23:21:12 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 25 Nov 2020 23:21:13 GMT
ARG BONITA_VERSION
# Wed, 25 Nov 2020 23:21:13 GMT
ARG BONITA_SHA256
# Wed, 25 Nov 2020 23:21:55 GMT
ARG BASE_URL
# Wed, 25 Nov 2020 23:21:56 GMT
ARG BONITA_URL
# Wed, 25 Nov 2020 23:21:57 GMT
ENV BONITA_VERSION=7.10.6
# Wed, 25 Nov 2020 23:21:58 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Wed, 25 Nov 2020 23:21:59 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 25 Nov 2020 23:22:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Wed, 25 Nov 2020 23:22:02 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Wed, 25 Nov 2020 23:22:10 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Wed, 25 Nov 2020 23:22:13 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Wed, 25 Nov 2020 23:22:15 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Wed, 25 Nov 2020 23:22:16 GMT
VOLUME [/opt/bonita]
# Wed, 25 Nov 2020 23:22:17 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Wed, 25 Nov 2020 23:22:18 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Wed, 25 Nov 2020 23:22:18 GMT
EXPOSE 8080
# Wed, 25 Nov 2020 23:22:19 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:04da93b342eb651d6b94c74a934a3290697573a907fa0a06067b538095601745`  
		Last Modified: Thu, 19 Nov 2020 16:25:04 GMT  
		Size: 23.7 MB (23733196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b235194751dee33624fc154603f7e25ecdfbb02538fb7d55fa796df9afa95fee`  
		Last Modified: Wed, 25 Nov 2020 22:44:43 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606a67bb8db9a1111022bdc6406442e11c1a66653136c5c777114bf67b61038a`  
		Last Modified: Wed, 25 Nov 2020 22:44:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963a3771da753196019b9ec7438846e332077edafc8fbb958d4b9875a6f8c08c`  
		Last Modified: Wed, 25 Nov 2020 23:24:30 GMT  
		Size: 93.5 MB (93518573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa886be96ef436069e063cfc38c29e97e791aac74a2de17827a9037938c81ecc`  
		Last Modified: Wed, 25 Nov 2020 23:24:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c7801c8831c3bfa0f34a65087747d59edc5c1bb2ef08800eb9c011f9397951`  
		Last Modified: Wed, 25 Nov 2020 23:24:06 GMT  
		Size: 1.9 KB (1915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1dd9294d182f0450f4cb8a4bfb1337db0fd360fcad0286b5868fa2872e8512c`  
		Last Modified: Wed, 25 Nov 2020 23:24:06 GMT  
		Size: 541.8 KB (541821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd3480a82b7f774ecca18c24995dbd0df347570225d236932816e5cd83c112a`  
		Last Modified: Wed, 25 Nov 2020 23:24:47 GMT  
		Size: 98.0 MB (97973947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f809581897998fc12f0b3bf70aa5f6a2347756cc1b14804d94d11b11e16c4d83`  
		Last Modified: Wed, 25 Nov 2020 23:24:40 GMT  
		Size: 7.7 KB (7650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c8ff24730358f1d9ad8203316a43d02ebe0ba95b73a7dd7b2e921575220f5`  
		Last Modified: Wed, 25 Nov 2020 23:24:40 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10.6` - linux; ppc64le

```console
$ docker pull bonita@sha256:ccda138193c6219e07c827cb18fb84e3f64ed51631191344aa0885f34d0ba462
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.0 MB (223954482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53504672add2122833646f2ddb0798f976993198a3686bb3ab1ebe28f42d2d89`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 03:25:11 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Sat, 26 Sep 2020 03:29:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 03:30:04 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 26 Sep 2020 03:30:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 26 Sep 2020 03:30:33 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 26 Sep 2020 03:30:41 GMT
ARG BONITA_VERSION
# Sat, 26 Sep 2020 03:30:48 GMT
ARG BONITA_SHA256
# Sat, 26 Sep 2020 03:32:40 GMT
ARG BASE_URL
# Sat, 26 Sep 2020 03:32:44 GMT
ARG BONITA_URL
# Fri, 02 Oct 2020 21:18:25 GMT
ENV BONITA_VERSION=7.10.6
# Fri, 02 Oct 2020 21:18:34 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Fri, 02 Oct 2020 21:18:42 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Oct 2020 21:18:52 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Fri, 02 Oct 2020 21:19:09 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 02 Oct 2020 21:19:31 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 02 Oct 2020 21:19:46 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 02 Oct 2020 21:20:01 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 02 Oct 2020 21:20:11 GMT
VOLUME [/opt/bonita]
# Fri, 02 Oct 2020 21:20:13 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Fri, 02 Oct 2020 21:20:17 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 02 Oct 2020 21:20:21 GMT
EXPOSE 8080
# Fri, 02 Oct 2020 21:20:27 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36f615abc241aa46a9f641088be9733489aa54ecdd7656aabbebc59e8babff4`  
		Last Modified: Sat, 26 Sep 2020 03:36:32 GMT  
		Size: 95.0 MB (95018057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7815598247ab5a7495520c70706e93222c19f009b14fa035185abb72878b65fb`  
		Last Modified: Sat, 26 Sep 2020 03:36:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b957f0e55214fe990421d5d9157a1e2b99678772069be9e9b93204567ce98e8`  
		Last Modified: Sat, 26 Sep 2020 03:36:09 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55cf6fc034ce3ae81db3086f9f903bad18df306e4078a9c4a542cf09dcf0773`  
		Last Modified: Sat, 26 Sep 2020 03:36:10 GMT  
		Size: 541.5 KB (541548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430a976f7a64af7c1ad0bd07fb507db383af946510dde0d9153227a59e13dc52`  
		Last Modified: Fri, 02 Oct 2020 21:23:30 GMT  
		Size: 98.0 MB (97973961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a853809ef5ddfb0f940a8cb762287fee5df363a3571236f16478ea0ede2605`  
		Last Modified: Fri, 02 Oct 2020 21:23:23 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b96585853cc722e35c073143958e441b5313c84bf83db33d9c9dfee2d792695`  
		Last Modified: Fri, 02 Oct 2020 21:23:23 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11`

```console
$ docker pull bonita@sha256:5c2f8f27b3bc3a288e58d19770eb979734be01331025878384dfb67fe727b9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11` - linux; amd64

```console
$ docker pull bonita@sha256:55ca1a9d6556fab9f400b6a0565b3c448001e3e3be78d0c50082535b49e46875
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234283153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f010c6ada2daea1e12693d8443503cd20713a6d814b0ffdac584f9fbee6af60b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Fri, 06 Nov 2020 20:59:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 06 Nov 2020 21:00:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 06 Nov 2020 21:00:28 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 06 Nov 2020 21:00:29 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 06 Nov 2020 21:00:31 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 06 Nov 2020 21:00:31 GMT
ARG BONITA_VERSION
# Fri, 06 Nov 2020 21:00:31 GMT
ARG BONITA_SHA256
# Fri, 06 Nov 2020 21:00:31 GMT
ARG BASE_URL
# Fri, 06 Nov 2020 21:00:31 GMT
ARG BONITA_URL
# Fri, 06 Nov 2020 21:00:32 GMT
ENV BONITA_VERSION=7.11.3
# Fri, 06 Nov 2020 21:00:32 GMT
ENV BONITA_SHA256=01300373642b7bfcc1fea717e1fd9caf460779ea1f35548d6eed61281f2e6068
# Fri, 06 Nov 2020 21:00:32 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.3.zip
# Fri, 06 Nov 2020 21:00:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 06 Nov 2020 21:00:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.3/BonitaCommunity-7.11.3.zip
# Fri, 06 Nov 2020 21:00:33 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 06 Nov 2020 21:00:34 GMT
RUN mkdir /opt/files
# Fri, 06 Nov 2020 21:00:35 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 06 Nov 2020 21:00:39 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 06 Nov 2020 21:00:40 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 06 Nov 2020 21:00:42 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 06 Nov 2020 21:00:42 GMT
VOLUME [/opt/bonita]
# Fri, 06 Nov 2020 21:00:42 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 06 Nov 2020 21:00:42 GMT
EXPOSE 8080
# Fri, 06 Nov 2020 21:00:43 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:74d558549b4f088b12d8d7f40183737f64e2b8b1b581e31b0cf6b7ba33c2a098`  
		Last Modified: Fri, 06 Nov 2020 21:01:16 GMT  
		Size: 93.7 MB (93657145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299279f6c2b963e1562e7f9eb3cfc08844ff4d84495b349a6a8480ab82aecf99`  
		Last Modified: Fri, 06 Nov 2020 21:01:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729af03f489aa47259b29756fe7ac1f4d93e5a96edea681717f708959736293a`  
		Last Modified: Fri, 06 Nov 2020 21:01:00 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a865a4bf2da9c5ec77ebe85db3355479835300324f57ca4192457b8bf80d6b03`  
		Last Modified: Fri, 06 Nov 2020 21:00:59 GMT  
		Size: 572.4 KB (572375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71f3c965e2fe6c75ece21941927f0255357fb223e0daf65e23deb5283a02062`  
		Last Modified: Fri, 06 Nov 2020 21:00:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab813df46746aeb6b728a516026c5a9578c2a73884bf9e386653cc5603844424`  
		Last Modified: Fri, 06 Nov 2020 21:00:59 GMT  
		Size: 6.9 KB (6860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a0d6b79b05f0f06e86b2587159296c4e1d5b1eec758ee885e3d2f1fa3e17fc`  
		Last Modified: Fri, 06 Nov 2020 21:01:05 GMT  
		Size: 113.3 MB (113340348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823aa99640d53270b3a4aa212ea68c84da33931f1acc06fc11db5d7a390aa8c8`  
		Last Modified: Fri, 06 Nov 2020 21:00:59 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:e1540036a17306fbc9bf5725f28a93bfd4c2fd6d5fc4fe516394ca77b0d793a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222916614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6f7d0940dfaa37734bf3d56eb29c6dd33d354ada87a46fd7084b6fa89f9132`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 25 Nov 2020 22:42:53 GMT
ADD file:e5b221023382c9e42b8558f8887f8317fe7e9759f59feb1799548aed9236e99b in / 
# Wed, 25 Nov 2020 22:42:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:42:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:43:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:43:01 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:22:27 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 25 Nov 2020 23:23:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:23:12 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 25 Nov 2020 23:23:14 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 25 Nov 2020 23:23:17 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 25 Nov 2020 23:23:18 GMT
ARG BONITA_VERSION
# Wed, 25 Nov 2020 23:23:19 GMT
ARG BONITA_SHA256
# Wed, 25 Nov 2020 23:23:20 GMT
ARG BASE_URL
# Wed, 25 Nov 2020 23:23:20 GMT
ARG BONITA_URL
# Wed, 25 Nov 2020 23:23:21 GMT
ENV BONITA_VERSION=7.11.3
# Wed, 25 Nov 2020 23:23:22 GMT
ENV BONITA_SHA256=01300373642b7bfcc1fea717e1fd9caf460779ea1f35548d6eed61281f2e6068
# Wed, 25 Nov 2020 23:23:22 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.3.zip
# Wed, 25 Nov 2020 23:23:23 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 25 Nov 2020 23:23:24 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.3/BonitaCommunity-7.11.3.zip
# Wed, 25 Nov 2020 23:23:26 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 25 Nov 2020 23:23:28 GMT
RUN mkdir /opt/files
# Wed, 25 Nov 2020 23:23:29 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Wed, 25 Nov 2020 23:23:34 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Wed, 25 Nov 2020 23:23:36 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 25 Nov 2020 23:23:39 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 25 Nov 2020 23:23:40 GMT
VOLUME [/opt/bonita]
# Wed, 25 Nov 2020 23:23:41 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 25 Nov 2020 23:23:41 GMT
EXPOSE 8080
# Wed, 25 Nov 2020 23:23:42 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:04da93b342eb651d6b94c74a934a3290697573a907fa0a06067b538095601745`  
		Last Modified: Thu, 19 Nov 2020 16:25:04 GMT  
		Size: 23.7 MB (23733196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b235194751dee33624fc154603f7e25ecdfbb02538fb7d55fa796df9afa95fee`  
		Last Modified: Wed, 25 Nov 2020 22:44:43 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606a67bb8db9a1111022bdc6406442e11c1a66653136c5c777114bf67b61038a`  
		Last Modified: Wed, 25 Nov 2020 22:44:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3335ad1be83802b9f36928a96aa3a203e1f531d22653bdeff056b041e3bc0c`  
		Last Modified: Wed, 25 Nov 2020 23:25:16 GMT  
		Size: 85.3 MB (85289407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d8f8d85c5729d26e222dafc8d445ff4381b1afa3aef91df27ec421dd3490fc`  
		Last Modified: Wed, 25 Nov 2020 23:24:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0fa485948e28ade7253e1e39f15ce35450083f6f490dfa4b16cd16d45b1ae1`  
		Last Modified: Wed, 25 Nov 2020 23:24:56 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da1ea701841366686df534cbdb465cd768dfd42b68dd63782cc0f11f1757c4c`  
		Last Modified: Wed, 25 Nov 2020 23:24:54 GMT  
		Size: 541.8 KB (541828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42f50cf00e70a69ddc0f514891400e5000f417aa34d89a8f1f6cb323f93c160`  
		Last Modified: Wed, 25 Nov 2020 23:24:54 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c042c4cd9b9b1d1123388e4634a6e32a3959a0ff52b1b6f5eb54fdf275f7278`  
		Last Modified: Wed, 25 Nov 2020 23:24:54 GMT  
		Size: 6.9 KB (6894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0481971affd735ee187301b31eb72f31d60212e861b7d7fd56cebe2834e68c4f`  
		Last Modified: Wed, 25 Nov 2020 23:25:07 GMT  
		Size: 113.3 MB (113340348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4269ac39e3eafec3755b539d64a1b93b9a4b258d18161750e03f606fe55fd780`  
		Last Modified: Wed, 25 Nov 2020 23:24:54 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; ppc64le

```console
$ docker pull bonita@sha256:3f963f6aa8d4c2a7e4f63baa1cf4c165dbfa085bd0a7a72d5149af93105ef935
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230218738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ac48a9dbd03d12686924d5884aede6cb6c8613bcc774d905eca7053a6e95b6`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Fri, 06 Nov 2020 21:53:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 06 Nov 2020 21:59:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 06 Nov 2020 22:00:03 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 06 Nov 2020 22:00:30 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 06 Nov 2020 22:00:45 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 06 Nov 2020 22:00:51 GMT
ARG BONITA_VERSION
# Fri, 06 Nov 2020 22:01:03 GMT
ARG BONITA_SHA256
# Fri, 06 Nov 2020 22:01:11 GMT
ARG BASE_URL
# Fri, 06 Nov 2020 22:01:19 GMT
ARG BONITA_URL
# Fri, 06 Nov 2020 22:01:26 GMT
ENV BONITA_VERSION=7.11.3
# Fri, 06 Nov 2020 22:01:31 GMT
ENV BONITA_SHA256=01300373642b7bfcc1fea717e1fd9caf460779ea1f35548d6eed61281f2e6068
# Fri, 06 Nov 2020 22:01:39 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.3.zip
# Fri, 06 Nov 2020 22:01:45 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 06 Nov 2020 22:01:50 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.3/BonitaCommunity-7.11.3.zip
# Fri, 06 Nov 2020 22:02:03 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 06 Nov 2020 22:02:20 GMT
RUN mkdir /opt/files
# Fri, 06 Nov 2020 22:02:24 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 06 Nov 2020 22:02:45 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 06 Nov 2020 22:02:57 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 06 Nov 2020 22:03:04 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 06 Nov 2020 22:03:08 GMT
VOLUME [/opt/bonita]
# Fri, 06 Nov 2020 22:03:11 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 06 Nov 2020 22:03:16 GMT
EXPOSE 8080
# Fri, 06 Nov 2020 22:03:20 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97646347816cc29a9c0edc917938e4c36c0bc216c00bccd71d4d3081847bb16`  
		Last Modified: Fri, 06 Nov 2020 22:04:07 GMT  
		Size: 85.9 MB (85916505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672916f10f4057c27c47fceb6de7be2bf4a17c4eb107341cc604422f0e7a8790`  
		Last Modified: Fri, 06 Nov 2020 22:03:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66096ecc3d12145ffdb754ef87d78ec23f8a93279fd33ebe5f0ca46acd85f479`  
		Last Modified: Fri, 06 Nov 2020 22:03:50 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0834cda6d12e2c7271465126a64b6671c0ad6c5aac4583ce022d5a391ce07af`  
		Last Modified: Fri, 06 Nov 2020 22:03:47 GMT  
		Size: 541.6 KB (541552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0c1d37b78bdc1c038f130c52752aac315c808a806799c76cc0670c368e5aa4`  
		Last Modified: Fri, 06 Nov 2020 22:03:47 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755313b6ecd3fd97b633eef37a140d3bb8577a17168509c4e5fd869f820aed7`  
		Last Modified: Fri, 06 Nov 2020 22:03:47 GMT  
		Size: 6.9 KB (6894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d9ca52ac7f89e66bcb3656eb3ac8d7dffc0b5eefd322c4d7d551826fa76ae5`  
		Last Modified: Fri, 06 Nov 2020 22:03:57 GMT  
		Size: 113.3 MB (113340348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6ba1d904db65b40ef279282190b0c5aeddde0a5c47c42cfbc6a1e6b3b86735`  
		Last Modified: Fri, 06 Nov 2020 22:03:47 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11.3`

```console
$ docker pull bonita@sha256:5c2f8f27b3bc3a288e58d19770eb979734be01331025878384dfb67fe727b9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11.3` - linux; amd64

```console
$ docker pull bonita@sha256:55ca1a9d6556fab9f400b6a0565b3c448001e3e3be78d0c50082535b49e46875
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234283153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f010c6ada2daea1e12693d8443503cd20713a6d814b0ffdac584f9fbee6af60b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Fri, 06 Nov 2020 20:59:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 06 Nov 2020 21:00:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 06 Nov 2020 21:00:28 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 06 Nov 2020 21:00:29 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 06 Nov 2020 21:00:31 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 06 Nov 2020 21:00:31 GMT
ARG BONITA_VERSION
# Fri, 06 Nov 2020 21:00:31 GMT
ARG BONITA_SHA256
# Fri, 06 Nov 2020 21:00:31 GMT
ARG BASE_URL
# Fri, 06 Nov 2020 21:00:31 GMT
ARG BONITA_URL
# Fri, 06 Nov 2020 21:00:32 GMT
ENV BONITA_VERSION=7.11.3
# Fri, 06 Nov 2020 21:00:32 GMT
ENV BONITA_SHA256=01300373642b7bfcc1fea717e1fd9caf460779ea1f35548d6eed61281f2e6068
# Fri, 06 Nov 2020 21:00:32 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.3.zip
# Fri, 06 Nov 2020 21:00:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 06 Nov 2020 21:00:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.3/BonitaCommunity-7.11.3.zip
# Fri, 06 Nov 2020 21:00:33 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 06 Nov 2020 21:00:34 GMT
RUN mkdir /opt/files
# Fri, 06 Nov 2020 21:00:35 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 06 Nov 2020 21:00:39 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 06 Nov 2020 21:00:40 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 06 Nov 2020 21:00:42 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 06 Nov 2020 21:00:42 GMT
VOLUME [/opt/bonita]
# Fri, 06 Nov 2020 21:00:42 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 06 Nov 2020 21:00:42 GMT
EXPOSE 8080
# Fri, 06 Nov 2020 21:00:43 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:74d558549b4f088b12d8d7f40183737f64e2b8b1b581e31b0cf6b7ba33c2a098`  
		Last Modified: Fri, 06 Nov 2020 21:01:16 GMT  
		Size: 93.7 MB (93657145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299279f6c2b963e1562e7f9eb3cfc08844ff4d84495b349a6a8480ab82aecf99`  
		Last Modified: Fri, 06 Nov 2020 21:01:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729af03f489aa47259b29756fe7ac1f4d93e5a96edea681717f708959736293a`  
		Last Modified: Fri, 06 Nov 2020 21:01:00 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a865a4bf2da9c5ec77ebe85db3355479835300324f57ca4192457b8bf80d6b03`  
		Last Modified: Fri, 06 Nov 2020 21:00:59 GMT  
		Size: 572.4 KB (572375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71f3c965e2fe6c75ece21941927f0255357fb223e0daf65e23deb5283a02062`  
		Last Modified: Fri, 06 Nov 2020 21:00:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab813df46746aeb6b728a516026c5a9578c2a73884bf9e386653cc5603844424`  
		Last Modified: Fri, 06 Nov 2020 21:00:59 GMT  
		Size: 6.9 KB (6860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a0d6b79b05f0f06e86b2587159296c4e1d5b1eec758ee885e3d2f1fa3e17fc`  
		Last Modified: Fri, 06 Nov 2020 21:01:05 GMT  
		Size: 113.3 MB (113340348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823aa99640d53270b3a4aa212ea68c84da33931f1acc06fc11db5d7a390aa8c8`  
		Last Modified: Fri, 06 Nov 2020 21:00:59 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.3` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:e1540036a17306fbc9bf5725f28a93bfd4c2fd6d5fc4fe516394ca77b0d793a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222916614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6f7d0940dfaa37734bf3d56eb29c6dd33d354ada87a46fd7084b6fa89f9132`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 25 Nov 2020 22:42:53 GMT
ADD file:e5b221023382c9e42b8558f8887f8317fe7e9759f59feb1799548aed9236e99b in / 
# Wed, 25 Nov 2020 22:42:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:42:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:43:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:43:01 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:22:27 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 25 Nov 2020 23:23:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:23:12 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 25 Nov 2020 23:23:14 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 25 Nov 2020 23:23:17 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 25 Nov 2020 23:23:18 GMT
ARG BONITA_VERSION
# Wed, 25 Nov 2020 23:23:19 GMT
ARG BONITA_SHA256
# Wed, 25 Nov 2020 23:23:20 GMT
ARG BASE_URL
# Wed, 25 Nov 2020 23:23:20 GMT
ARG BONITA_URL
# Wed, 25 Nov 2020 23:23:21 GMT
ENV BONITA_VERSION=7.11.3
# Wed, 25 Nov 2020 23:23:22 GMT
ENV BONITA_SHA256=01300373642b7bfcc1fea717e1fd9caf460779ea1f35548d6eed61281f2e6068
# Wed, 25 Nov 2020 23:23:22 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.3.zip
# Wed, 25 Nov 2020 23:23:23 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 25 Nov 2020 23:23:24 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.3/BonitaCommunity-7.11.3.zip
# Wed, 25 Nov 2020 23:23:26 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 25 Nov 2020 23:23:28 GMT
RUN mkdir /opt/files
# Wed, 25 Nov 2020 23:23:29 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Wed, 25 Nov 2020 23:23:34 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Wed, 25 Nov 2020 23:23:36 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 25 Nov 2020 23:23:39 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 25 Nov 2020 23:23:40 GMT
VOLUME [/opt/bonita]
# Wed, 25 Nov 2020 23:23:41 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 25 Nov 2020 23:23:41 GMT
EXPOSE 8080
# Wed, 25 Nov 2020 23:23:42 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:04da93b342eb651d6b94c74a934a3290697573a907fa0a06067b538095601745`  
		Last Modified: Thu, 19 Nov 2020 16:25:04 GMT  
		Size: 23.7 MB (23733196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b235194751dee33624fc154603f7e25ecdfbb02538fb7d55fa796df9afa95fee`  
		Last Modified: Wed, 25 Nov 2020 22:44:43 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606a67bb8db9a1111022bdc6406442e11c1a66653136c5c777114bf67b61038a`  
		Last Modified: Wed, 25 Nov 2020 22:44:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3335ad1be83802b9f36928a96aa3a203e1f531d22653bdeff056b041e3bc0c`  
		Last Modified: Wed, 25 Nov 2020 23:25:16 GMT  
		Size: 85.3 MB (85289407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d8f8d85c5729d26e222dafc8d445ff4381b1afa3aef91df27ec421dd3490fc`  
		Last Modified: Wed, 25 Nov 2020 23:24:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0fa485948e28ade7253e1e39f15ce35450083f6f490dfa4b16cd16d45b1ae1`  
		Last Modified: Wed, 25 Nov 2020 23:24:56 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da1ea701841366686df534cbdb465cd768dfd42b68dd63782cc0f11f1757c4c`  
		Last Modified: Wed, 25 Nov 2020 23:24:54 GMT  
		Size: 541.8 KB (541828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42f50cf00e70a69ddc0f514891400e5000f417aa34d89a8f1f6cb323f93c160`  
		Last Modified: Wed, 25 Nov 2020 23:24:54 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c042c4cd9b9b1d1123388e4634a6e32a3959a0ff52b1b6f5eb54fdf275f7278`  
		Last Modified: Wed, 25 Nov 2020 23:24:54 GMT  
		Size: 6.9 KB (6894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0481971affd735ee187301b31eb72f31d60212e861b7d7fd56cebe2834e68c4f`  
		Last Modified: Wed, 25 Nov 2020 23:25:07 GMT  
		Size: 113.3 MB (113340348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4269ac39e3eafec3755b539d64a1b93b9a4b258d18161750e03f606fe55fd780`  
		Last Modified: Wed, 25 Nov 2020 23:24:54 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.3` - linux; ppc64le

```console
$ docker pull bonita@sha256:3f963f6aa8d4c2a7e4f63baa1cf4c165dbfa085bd0a7a72d5149af93105ef935
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230218738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ac48a9dbd03d12686924d5884aede6cb6c8613bcc774d905eca7053a6e95b6`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Fri, 06 Nov 2020 21:53:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 06 Nov 2020 21:59:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 06 Nov 2020 22:00:03 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 06 Nov 2020 22:00:30 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 06 Nov 2020 22:00:45 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 06 Nov 2020 22:00:51 GMT
ARG BONITA_VERSION
# Fri, 06 Nov 2020 22:01:03 GMT
ARG BONITA_SHA256
# Fri, 06 Nov 2020 22:01:11 GMT
ARG BASE_URL
# Fri, 06 Nov 2020 22:01:19 GMT
ARG BONITA_URL
# Fri, 06 Nov 2020 22:01:26 GMT
ENV BONITA_VERSION=7.11.3
# Fri, 06 Nov 2020 22:01:31 GMT
ENV BONITA_SHA256=01300373642b7bfcc1fea717e1fd9caf460779ea1f35548d6eed61281f2e6068
# Fri, 06 Nov 2020 22:01:39 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.3.zip
# Fri, 06 Nov 2020 22:01:45 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 06 Nov 2020 22:01:50 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.3/BonitaCommunity-7.11.3.zip
# Fri, 06 Nov 2020 22:02:03 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 06 Nov 2020 22:02:20 GMT
RUN mkdir /opt/files
# Fri, 06 Nov 2020 22:02:24 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 06 Nov 2020 22:02:45 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 06 Nov 2020 22:02:57 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 06 Nov 2020 22:03:04 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 06 Nov 2020 22:03:08 GMT
VOLUME [/opt/bonita]
# Fri, 06 Nov 2020 22:03:11 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 06 Nov 2020 22:03:16 GMT
EXPOSE 8080
# Fri, 06 Nov 2020 22:03:20 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97646347816cc29a9c0edc917938e4c36c0bc216c00bccd71d4d3081847bb16`  
		Last Modified: Fri, 06 Nov 2020 22:04:07 GMT  
		Size: 85.9 MB (85916505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672916f10f4057c27c47fceb6de7be2bf4a17c4eb107341cc604422f0e7a8790`  
		Last Modified: Fri, 06 Nov 2020 22:03:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66096ecc3d12145ffdb754ef87d78ec23f8a93279fd33ebe5f0ca46acd85f479`  
		Last Modified: Fri, 06 Nov 2020 22:03:50 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0834cda6d12e2c7271465126a64b6671c0ad6c5aac4583ce022d5a391ce07af`  
		Last Modified: Fri, 06 Nov 2020 22:03:47 GMT  
		Size: 541.6 KB (541552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0c1d37b78bdc1c038f130c52752aac315c808a806799c76cc0670c368e5aa4`  
		Last Modified: Fri, 06 Nov 2020 22:03:47 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755313b6ecd3fd97b633eef37a140d3bb8577a17168509c4e5fd869f820aed7`  
		Last Modified: Fri, 06 Nov 2020 22:03:47 GMT  
		Size: 6.9 KB (6894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d9ca52ac7f89e66bcb3656eb3ac8d7dffc0b5eefd322c4d7d551826fa76ae5`  
		Last Modified: Fri, 06 Nov 2020 22:03:57 GMT  
		Size: 113.3 MB (113340348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6ba1d904db65b40ef279282190b0c5aeddde0a5c47c42cfbc6a1e6b3b86735`  
		Last Modified: Fri, 06 Nov 2020 22:03:47 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.9`

```console
$ docker pull bonita@sha256:9b3a3f014ccabdc70b33a57efdd1dc875fb5af110fc96726d3db4eb05836a519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.9` - linux; amd64

```console
$ docker pull bonita@sha256:6dd7434048c6ce0d7cf65765c2ef6536533574903972e74aaacaa548913d924a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.3 MB (229309326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ba5fb2960dd0440f3128c99af425d16d930666ab8d578eb2e7dd17518bc77c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Fri, 25 Sep 2020 23:41:10 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 25 Sep 2020 23:41:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:41:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 25 Sep 2020 23:41:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 25 Sep 2020 23:41:50 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 25 Sep 2020 23:41:50 GMT
ARG BONITA_VERSION
# Fri, 25 Sep 2020 23:41:51 GMT
ARG BONITA_SHA256
# Fri, 25 Sep 2020 23:41:51 GMT
ARG BONITA_URL
# Fri, 25 Sep 2020 23:41:51 GMT
ENV BONITA_VERSION=7.9.5
# Fri, 25 Sep 2020 23:41:51 GMT
ENV BONITA_SHA256=49620e505f072a4f20ebb936c9391e8665d441df9f650749a61a19a5c52e2932
# Fri, 25 Sep 2020 23:41:51 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.9.5-tomcat.zip
# Fri, 25 Sep 2020 23:42:01 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 25 Sep 2020 23:42:02 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 25 Sep 2020 23:42:04 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip | sha256sum -c -
# Fri, 25 Sep 2020 23:42:04 GMT
VOLUME [/opt/bonita]
# Fri, 25 Sep 2020 23:42:04 GMT
COPY dir:ef58daa6df201fe2eac6b87ad183ec81a5dbb212d47f61a3244b65faca8cb3c6 in /opt/files 
# Fri, 25 Sep 2020 23:42:04 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 25 Sep 2020 23:42:04 GMT
EXPOSE 8080
# Fri, 25 Sep 2020 23:42:05 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:16b26225e2399009e0af570eebb768bfcbe84cb6c29b1904acdde559aa23f5ea`  
		Last Modified: Fri, 25 Sep 2020 23:43:07 GMT  
		Size: 102.0 MB (101998153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a756bb5a69747c3a85260b46c657b99989e66e321215246e71037a10243f35`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2a72327f28ef87b1a7d940367fe2bd4bde9b327a8efe0d35fd44b7d5c19ab6`  
		Last Modified: Fri, 25 Sep 2020 23:42:49 GMT  
		Size: 1.9 KB (1913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf8ca91d922430c6fecd7439843b96ee71b8d1116fcf27a619ef4ff6b5b5f8e`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 572.4 KB (572374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76df12a7f39d6849f5acbf70ea4ca165fc6b0f07477eddf53ae0b1207ab03245`  
		Last Modified: Fri, 25 Sep 2020 23:42:56 GMT  
		Size: 100.0 MB (100024954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e92a2e89fe94010b0cdad922da1433fbeb2b714f1ea82d598a6bf82bec2b28`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 7.6 KB (7557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf3e10066052f2a8c3180843296f3faecef55cce051176c6ab2194862c974f7`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 1.6 KB (1627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.9` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2df65ddc14f0b59ddd3daa16ef74136abe520a528584f679b811698afbaabc7c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217830939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e1801d9dbeb730cbcd5d2192eef48924ccb97920b723d52230b711702ab7baf`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 25 Nov 2020 22:42:53 GMT
ADD file:e5b221023382c9e42b8558f8887f8317fe7e9759f59feb1799548aed9236e99b in / 
# Wed, 25 Nov 2020 22:42:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:42:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:43:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:43:01 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:19:52 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Wed, 25 Nov 2020 23:21:00 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:21:05 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 25 Nov 2020 23:21:09 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 25 Nov 2020 23:21:12 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 25 Nov 2020 23:21:13 GMT
ARG BONITA_VERSION
# Wed, 25 Nov 2020 23:21:13 GMT
ARG BONITA_SHA256
# Wed, 25 Nov 2020 23:21:14 GMT
ARG BONITA_URL
# Wed, 25 Nov 2020 23:21:15 GMT
ENV BONITA_VERSION=7.9.5
# Wed, 25 Nov 2020 23:21:16 GMT
ENV BONITA_SHA256=49620e505f072a4f20ebb936c9391e8665d441df9f650749a61a19a5c52e2932
# Wed, 25 Nov 2020 23:21:17 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.9.5-tomcat.zip
# Wed, 25 Nov 2020 23:21:26 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Wed, 25 Nov 2020 23:21:30 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Wed, 25 Nov 2020 23:21:33 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip | sha256sum -c -
# Wed, 25 Nov 2020 23:21:35 GMT
VOLUME [/opt/bonita]
# Wed, 25 Nov 2020 23:21:36 GMT
COPY dir:ef58daa6df201fe2eac6b87ad183ec81a5dbb212d47f61a3244b65faca8cb3c6 in /opt/files 
# Wed, 25 Nov 2020 23:21:36 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Wed, 25 Nov 2020 23:21:38 GMT
EXPOSE 8080
# Wed, 25 Nov 2020 23:21:38 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:04da93b342eb651d6b94c74a934a3290697573a907fa0a06067b538095601745`  
		Last Modified: Thu, 19 Nov 2020 16:25:04 GMT  
		Size: 23.7 MB (23733196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b235194751dee33624fc154603f7e25ecdfbb02538fb7d55fa796df9afa95fee`  
		Last Modified: Wed, 25 Nov 2020 22:44:43 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606a67bb8db9a1111022bdc6406442e11c1a66653136c5c777114bf67b61038a`  
		Last Modified: Wed, 25 Nov 2020 22:44:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963a3771da753196019b9ec7438846e332077edafc8fbb958d4b9875a6f8c08c`  
		Last Modified: Wed, 25 Nov 2020 23:24:30 GMT  
		Size: 93.5 MB (93518573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa886be96ef436069e063cfc38c29e97e791aac74a2de17827a9037938c81ecc`  
		Last Modified: Wed, 25 Nov 2020 23:24:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c7801c8831c3bfa0f34a65087747d59edc5c1bb2ef08800eb9c011f9397951`  
		Last Modified: Wed, 25 Nov 2020 23:24:06 GMT  
		Size: 1.9 KB (1915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1dd9294d182f0450f4cb8a4bfb1337db0fd360fcad0286b5868fa2872e8512c`  
		Last Modified: Wed, 25 Nov 2020 23:24:06 GMT  
		Size: 541.8 KB (541821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020b24b2f3d6c58040ad9f371d95f71a31dd83e95a93efaba95f49aa30a772ff`  
		Last Modified: Wed, 25 Nov 2020 23:24:16 GMT  
		Size: 100.0 MB (100025000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30cecf4a2f351c7b4239d29923fe66cf68d57c76d9b9cfea865de3ca2f1f89c`  
		Last Modified: Wed, 25 Nov 2020 23:24:06 GMT  
		Size: 7.6 KB (7587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89dfe83118e5155e381ffab0dd98a84bf71cba036d7d8c884436430edcf66760`  
		Last Modified: Wed, 25 Nov 2020 23:24:06 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.9` - linux; ppc64le

```console
$ docker pull bonita@sha256:fb96dcdef70970a0c3e0ab5901cf885c9ba983a23e7568e0e71098c23b2463dc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (226005453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41738009cf190898409332797a8509227b6a5983c82c0d73f8068b054f6b0449`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 03:25:11 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Sat, 26 Sep 2020 03:29:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 03:30:04 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 26 Sep 2020 03:30:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 26 Sep 2020 03:30:33 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 26 Sep 2020 03:30:41 GMT
ARG BONITA_VERSION
# Sat, 26 Sep 2020 03:30:48 GMT
ARG BONITA_SHA256
# Sat, 26 Sep 2020 03:30:56 GMT
ARG BONITA_URL
# Sat, 26 Sep 2020 03:31:03 GMT
ENV BONITA_VERSION=7.9.5
# Sat, 26 Sep 2020 03:31:08 GMT
ENV BONITA_SHA256=49620e505f072a4f20ebb936c9391e8665d441df9f650749a61a19a5c52e2932
# Sat, 26 Sep 2020 03:31:14 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.9.5-tomcat.zip
# Sat, 26 Sep 2020 03:31:45 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Sat, 26 Sep 2020 03:31:55 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Sat, 26 Sep 2020 03:32:03 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip | sha256sum -c -
# Sat, 26 Sep 2020 03:32:07 GMT
VOLUME [/opt/bonita]
# Sat, 26 Sep 2020 03:32:08 GMT
COPY dir:ef58daa6df201fe2eac6b87ad183ec81a5dbb212d47f61a3244b65faca8cb3c6 in /opt/files 
# Sat, 26 Sep 2020 03:32:09 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Sat, 26 Sep 2020 03:32:12 GMT
EXPOSE 8080
# Sat, 26 Sep 2020 03:32:18 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36f615abc241aa46a9f641088be9733489aa54ecdd7656aabbebc59e8babff4`  
		Last Modified: Sat, 26 Sep 2020 03:36:32 GMT  
		Size: 95.0 MB (95018057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7815598247ab5a7495520c70706e93222c19f009b14fa035185abb72878b65fb`  
		Last Modified: Sat, 26 Sep 2020 03:36:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b957f0e55214fe990421d5d9157a1e2b99678772069be9e9b93204567ce98e8`  
		Last Modified: Sat, 26 Sep 2020 03:36:09 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55cf6fc034ce3ae81db3086f9f903bad18df306e4078a9c4a542cf09dcf0773`  
		Last Modified: Sat, 26 Sep 2020 03:36:10 GMT  
		Size: 541.5 KB (541548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f13d3f9382602b6be6714234d241fc55503d84bd44510f2079b3780d407f12`  
		Last Modified: Sat, 26 Sep 2020 03:36:18 GMT  
		Size: 100.0 MB (100025000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e37c9bee6801e902a0424a33961cfa7f9a3d831242d28de47136f492f26f8d`  
		Last Modified: Sat, 26 Sep 2020 03:36:10 GMT  
		Size: 7.6 KB (7588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9afe094faae2bb36b5cf8883854120c3003a2059e9fbe5401cd6de59fbbf2df4`  
		Last Modified: Sat, 26 Sep 2020 03:36:09 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.9.5`

```console
$ docker pull bonita@sha256:9b3a3f014ccabdc70b33a57efdd1dc875fb5af110fc96726d3db4eb05836a519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.9.5` - linux; amd64

```console
$ docker pull bonita@sha256:6dd7434048c6ce0d7cf65765c2ef6536533574903972e74aaacaa548913d924a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.3 MB (229309326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ba5fb2960dd0440f3128c99af425d16d930666ab8d578eb2e7dd17518bc77c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Fri, 25 Sep 2020 23:41:10 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 25 Sep 2020 23:41:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:41:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 25 Sep 2020 23:41:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 25 Sep 2020 23:41:50 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 25 Sep 2020 23:41:50 GMT
ARG BONITA_VERSION
# Fri, 25 Sep 2020 23:41:51 GMT
ARG BONITA_SHA256
# Fri, 25 Sep 2020 23:41:51 GMT
ARG BONITA_URL
# Fri, 25 Sep 2020 23:41:51 GMT
ENV BONITA_VERSION=7.9.5
# Fri, 25 Sep 2020 23:41:51 GMT
ENV BONITA_SHA256=49620e505f072a4f20ebb936c9391e8665d441df9f650749a61a19a5c52e2932
# Fri, 25 Sep 2020 23:41:51 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.9.5-tomcat.zip
# Fri, 25 Sep 2020 23:42:01 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 25 Sep 2020 23:42:02 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 25 Sep 2020 23:42:04 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip | sha256sum -c -
# Fri, 25 Sep 2020 23:42:04 GMT
VOLUME [/opt/bonita]
# Fri, 25 Sep 2020 23:42:04 GMT
COPY dir:ef58daa6df201fe2eac6b87ad183ec81a5dbb212d47f61a3244b65faca8cb3c6 in /opt/files 
# Fri, 25 Sep 2020 23:42:04 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 25 Sep 2020 23:42:04 GMT
EXPOSE 8080
# Fri, 25 Sep 2020 23:42:05 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:16b26225e2399009e0af570eebb768bfcbe84cb6c29b1904acdde559aa23f5ea`  
		Last Modified: Fri, 25 Sep 2020 23:43:07 GMT  
		Size: 102.0 MB (101998153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a756bb5a69747c3a85260b46c657b99989e66e321215246e71037a10243f35`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2a72327f28ef87b1a7d940367fe2bd4bde9b327a8efe0d35fd44b7d5c19ab6`  
		Last Modified: Fri, 25 Sep 2020 23:42:49 GMT  
		Size: 1.9 KB (1913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf8ca91d922430c6fecd7439843b96ee71b8d1116fcf27a619ef4ff6b5b5f8e`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 572.4 KB (572374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76df12a7f39d6849f5acbf70ea4ca165fc6b0f07477eddf53ae0b1207ab03245`  
		Last Modified: Fri, 25 Sep 2020 23:42:56 GMT  
		Size: 100.0 MB (100024954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e92a2e89fe94010b0cdad922da1433fbeb2b714f1ea82d598a6bf82bec2b28`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 7.6 KB (7557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf3e10066052f2a8c3180843296f3faecef55cce051176c6ab2194862c974f7`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 1.6 KB (1627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.9.5` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2df65ddc14f0b59ddd3daa16ef74136abe520a528584f679b811698afbaabc7c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217830939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e1801d9dbeb730cbcd5d2192eef48924ccb97920b723d52230b711702ab7baf`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 25 Nov 2020 22:42:53 GMT
ADD file:e5b221023382c9e42b8558f8887f8317fe7e9759f59feb1799548aed9236e99b in / 
# Wed, 25 Nov 2020 22:42:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:42:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:43:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:43:01 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:19:52 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Wed, 25 Nov 2020 23:21:00 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:21:05 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 25 Nov 2020 23:21:09 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 25 Nov 2020 23:21:12 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 25 Nov 2020 23:21:13 GMT
ARG BONITA_VERSION
# Wed, 25 Nov 2020 23:21:13 GMT
ARG BONITA_SHA256
# Wed, 25 Nov 2020 23:21:14 GMT
ARG BONITA_URL
# Wed, 25 Nov 2020 23:21:15 GMT
ENV BONITA_VERSION=7.9.5
# Wed, 25 Nov 2020 23:21:16 GMT
ENV BONITA_SHA256=49620e505f072a4f20ebb936c9391e8665d441df9f650749a61a19a5c52e2932
# Wed, 25 Nov 2020 23:21:17 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.9.5-tomcat.zip
# Wed, 25 Nov 2020 23:21:26 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Wed, 25 Nov 2020 23:21:30 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Wed, 25 Nov 2020 23:21:33 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip | sha256sum -c -
# Wed, 25 Nov 2020 23:21:35 GMT
VOLUME [/opt/bonita]
# Wed, 25 Nov 2020 23:21:36 GMT
COPY dir:ef58daa6df201fe2eac6b87ad183ec81a5dbb212d47f61a3244b65faca8cb3c6 in /opt/files 
# Wed, 25 Nov 2020 23:21:36 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Wed, 25 Nov 2020 23:21:38 GMT
EXPOSE 8080
# Wed, 25 Nov 2020 23:21:38 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:04da93b342eb651d6b94c74a934a3290697573a907fa0a06067b538095601745`  
		Last Modified: Thu, 19 Nov 2020 16:25:04 GMT  
		Size: 23.7 MB (23733196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b235194751dee33624fc154603f7e25ecdfbb02538fb7d55fa796df9afa95fee`  
		Last Modified: Wed, 25 Nov 2020 22:44:43 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606a67bb8db9a1111022bdc6406442e11c1a66653136c5c777114bf67b61038a`  
		Last Modified: Wed, 25 Nov 2020 22:44:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963a3771da753196019b9ec7438846e332077edafc8fbb958d4b9875a6f8c08c`  
		Last Modified: Wed, 25 Nov 2020 23:24:30 GMT  
		Size: 93.5 MB (93518573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa886be96ef436069e063cfc38c29e97e791aac74a2de17827a9037938c81ecc`  
		Last Modified: Wed, 25 Nov 2020 23:24:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c7801c8831c3bfa0f34a65087747d59edc5c1bb2ef08800eb9c011f9397951`  
		Last Modified: Wed, 25 Nov 2020 23:24:06 GMT  
		Size: 1.9 KB (1915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1dd9294d182f0450f4cb8a4bfb1337db0fd360fcad0286b5868fa2872e8512c`  
		Last Modified: Wed, 25 Nov 2020 23:24:06 GMT  
		Size: 541.8 KB (541821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020b24b2f3d6c58040ad9f371d95f71a31dd83e95a93efaba95f49aa30a772ff`  
		Last Modified: Wed, 25 Nov 2020 23:24:16 GMT  
		Size: 100.0 MB (100025000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30cecf4a2f351c7b4239d29923fe66cf68d57c76d9b9cfea865de3ca2f1f89c`  
		Last Modified: Wed, 25 Nov 2020 23:24:06 GMT  
		Size: 7.6 KB (7587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89dfe83118e5155e381ffab0dd98a84bf71cba036d7d8c884436430edcf66760`  
		Last Modified: Wed, 25 Nov 2020 23:24:06 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.9.5` - linux; ppc64le

```console
$ docker pull bonita@sha256:fb96dcdef70970a0c3e0ab5901cf885c9ba983a23e7568e0e71098c23b2463dc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (226005453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41738009cf190898409332797a8509227b6a5983c82c0d73f8068b054f6b0449`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 03:25:11 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Sat, 26 Sep 2020 03:29:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 03:30:04 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 26 Sep 2020 03:30:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 26 Sep 2020 03:30:33 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 26 Sep 2020 03:30:41 GMT
ARG BONITA_VERSION
# Sat, 26 Sep 2020 03:30:48 GMT
ARG BONITA_SHA256
# Sat, 26 Sep 2020 03:30:56 GMT
ARG BONITA_URL
# Sat, 26 Sep 2020 03:31:03 GMT
ENV BONITA_VERSION=7.9.5
# Sat, 26 Sep 2020 03:31:08 GMT
ENV BONITA_SHA256=49620e505f072a4f20ebb936c9391e8665d441df9f650749a61a19a5c52e2932
# Sat, 26 Sep 2020 03:31:14 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.9.5-tomcat.zip
# Sat, 26 Sep 2020 03:31:45 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Sat, 26 Sep 2020 03:31:55 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Sat, 26 Sep 2020 03:32:03 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip | sha256sum -c -
# Sat, 26 Sep 2020 03:32:07 GMT
VOLUME [/opt/bonita]
# Sat, 26 Sep 2020 03:32:08 GMT
COPY dir:ef58daa6df201fe2eac6b87ad183ec81a5dbb212d47f61a3244b65faca8cb3c6 in /opt/files 
# Sat, 26 Sep 2020 03:32:09 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Sat, 26 Sep 2020 03:32:12 GMT
EXPOSE 8080
# Sat, 26 Sep 2020 03:32:18 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36f615abc241aa46a9f641088be9733489aa54ecdd7656aabbebc59e8babff4`  
		Last Modified: Sat, 26 Sep 2020 03:36:32 GMT  
		Size: 95.0 MB (95018057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7815598247ab5a7495520c70706e93222c19f009b14fa035185abb72878b65fb`  
		Last Modified: Sat, 26 Sep 2020 03:36:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b957f0e55214fe990421d5d9157a1e2b99678772069be9e9b93204567ce98e8`  
		Last Modified: Sat, 26 Sep 2020 03:36:09 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55cf6fc034ce3ae81db3086f9f903bad18df306e4078a9c4a542cf09dcf0773`  
		Last Modified: Sat, 26 Sep 2020 03:36:10 GMT  
		Size: 541.5 KB (541548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f13d3f9382602b6be6714234d241fc55503d84bd44510f2079b3780d407f12`  
		Last Modified: Sat, 26 Sep 2020 03:36:18 GMT  
		Size: 100.0 MB (100025000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e37c9bee6801e902a0424a33961cfa7f9a3d831242d28de47136f492f26f8d`  
		Last Modified: Sat, 26 Sep 2020 03:36:10 GMT  
		Size: 7.6 KB (7588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9afe094faae2bb36b5cf8883854120c3003a2059e9fbe5401cd6de59fbbf2df4`  
		Last Modified: Sat, 26 Sep 2020 03:36:09 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:5c2f8f27b3bc3a288e58d19770eb979734be01331025878384dfb67fe727b9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:55ca1a9d6556fab9f400b6a0565b3c448001e3e3be78d0c50082535b49e46875
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234283153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f010c6ada2daea1e12693d8443503cd20713a6d814b0ffdac584f9fbee6af60b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Fri, 06 Nov 2020 20:59:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 06 Nov 2020 21:00:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 06 Nov 2020 21:00:28 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 06 Nov 2020 21:00:29 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 06 Nov 2020 21:00:31 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 06 Nov 2020 21:00:31 GMT
ARG BONITA_VERSION
# Fri, 06 Nov 2020 21:00:31 GMT
ARG BONITA_SHA256
# Fri, 06 Nov 2020 21:00:31 GMT
ARG BASE_URL
# Fri, 06 Nov 2020 21:00:31 GMT
ARG BONITA_URL
# Fri, 06 Nov 2020 21:00:32 GMT
ENV BONITA_VERSION=7.11.3
# Fri, 06 Nov 2020 21:00:32 GMT
ENV BONITA_SHA256=01300373642b7bfcc1fea717e1fd9caf460779ea1f35548d6eed61281f2e6068
# Fri, 06 Nov 2020 21:00:32 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.3.zip
# Fri, 06 Nov 2020 21:00:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 06 Nov 2020 21:00:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.3/BonitaCommunity-7.11.3.zip
# Fri, 06 Nov 2020 21:00:33 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 06 Nov 2020 21:00:34 GMT
RUN mkdir /opt/files
# Fri, 06 Nov 2020 21:00:35 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 06 Nov 2020 21:00:39 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 06 Nov 2020 21:00:40 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 06 Nov 2020 21:00:42 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 06 Nov 2020 21:00:42 GMT
VOLUME [/opt/bonita]
# Fri, 06 Nov 2020 21:00:42 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 06 Nov 2020 21:00:42 GMT
EXPOSE 8080
# Fri, 06 Nov 2020 21:00:43 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:74d558549b4f088b12d8d7f40183737f64e2b8b1b581e31b0cf6b7ba33c2a098`  
		Last Modified: Fri, 06 Nov 2020 21:01:16 GMT  
		Size: 93.7 MB (93657145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299279f6c2b963e1562e7f9eb3cfc08844ff4d84495b349a6a8480ab82aecf99`  
		Last Modified: Fri, 06 Nov 2020 21:01:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729af03f489aa47259b29756fe7ac1f4d93e5a96edea681717f708959736293a`  
		Last Modified: Fri, 06 Nov 2020 21:01:00 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a865a4bf2da9c5ec77ebe85db3355479835300324f57ca4192457b8bf80d6b03`  
		Last Modified: Fri, 06 Nov 2020 21:00:59 GMT  
		Size: 572.4 KB (572375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71f3c965e2fe6c75ece21941927f0255357fb223e0daf65e23deb5283a02062`  
		Last Modified: Fri, 06 Nov 2020 21:00:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab813df46746aeb6b728a516026c5a9578c2a73884bf9e386653cc5603844424`  
		Last Modified: Fri, 06 Nov 2020 21:00:59 GMT  
		Size: 6.9 KB (6860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a0d6b79b05f0f06e86b2587159296c4e1d5b1eec758ee885e3d2f1fa3e17fc`  
		Last Modified: Fri, 06 Nov 2020 21:01:05 GMT  
		Size: 113.3 MB (113340348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823aa99640d53270b3a4aa212ea68c84da33931f1acc06fc11db5d7a390aa8c8`  
		Last Modified: Fri, 06 Nov 2020 21:00:59 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:e1540036a17306fbc9bf5725f28a93bfd4c2fd6d5fc4fe516394ca77b0d793a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222916614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6f7d0940dfaa37734bf3d56eb29c6dd33d354ada87a46fd7084b6fa89f9132`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 25 Nov 2020 22:42:53 GMT
ADD file:e5b221023382c9e42b8558f8887f8317fe7e9759f59feb1799548aed9236e99b in / 
# Wed, 25 Nov 2020 22:42:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:42:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:43:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:43:01 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:22:27 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 25 Nov 2020 23:23:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:23:12 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 25 Nov 2020 23:23:14 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 25 Nov 2020 23:23:17 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 25 Nov 2020 23:23:18 GMT
ARG BONITA_VERSION
# Wed, 25 Nov 2020 23:23:19 GMT
ARG BONITA_SHA256
# Wed, 25 Nov 2020 23:23:20 GMT
ARG BASE_URL
# Wed, 25 Nov 2020 23:23:20 GMT
ARG BONITA_URL
# Wed, 25 Nov 2020 23:23:21 GMT
ENV BONITA_VERSION=7.11.3
# Wed, 25 Nov 2020 23:23:22 GMT
ENV BONITA_SHA256=01300373642b7bfcc1fea717e1fd9caf460779ea1f35548d6eed61281f2e6068
# Wed, 25 Nov 2020 23:23:22 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.3.zip
# Wed, 25 Nov 2020 23:23:23 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 25 Nov 2020 23:23:24 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.3/BonitaCommunity-7.11.3.zip
# Wed, 25 Nov 2020 23:23:26 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 25 Nov 2020 23:23:28 GMT
RUN mkdir /opt/files
# Wed, 25 Nov 2020 23:23:29 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Wed, 25 Nov 2020 23:23:34 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Wed, 25 Nov 2020 23:23:36 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 25 Nov 2020 23:23:39 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 25 Nov 2020 23:23:40 GMT
VOLUME [/opt/bonita]
# Wed, 25 Nov 2020 23:23:41 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 25 Nov 2020 23:23:41 GMT
EXPOSE 8080
# Wed, 25 Nov 2020 23:23:42 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:04da93b342eb651d6b94c74a934a3290697573a907fa0a06067b538095601745`  
		Last Modified: Thu, 19 Nov 2020 16:25:04 GMT  
		Size: 23.7 MB (23733196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b235194751dee33624fc154603f7e25ecdfbb02538fb7d55fa796df9afa95fee`  
		Last Modified: Wed, 25 Nov 2020 22:44:43 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606a67bb8db9a1111022bdc6406442e11c1a66653136c5c777114bf67b61038a`  
		Last Modified: Wed, 25 Nov 2020 22:44:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3335ad1be83802b9f36928a96aa3a203e1f531d22653bdeff056b041e3bc0c`  
		Last Modified: Wed, 25 Nov 2020 23:25:16 GMT  
		Size: 85.3 MB (85289407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d8f8d85c5729d26e222dafc8d445ff4381b1afa3aef91df27ec421dd3490fc`  
		Last Modified: Wed, 25 Nov 2020 23:24:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0fa485948e28ade7253e1e39f15ce35450083f6f490dfa4b16cd16d45b1ae1`  
		Last Modified: Wed, 25 Nov 2020 23:24:56 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da1ea701841366686df534cbdb465cd768dfd42b68dd63782cc0f11f1757c4c`  
		Last Modified: Wed, 25 Nov 2020 23:24:54 GMT  
		Size: 541.8 KB (541828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42f50cf00e70a69ddc0f514891400e5000f417aa34d89a8f1f6cb323f93c160`  
		Last Modified: Wed, 25 Nov 2020 23:24:54 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c042c4cd9b9b1d1123388e4634a6e32a3959a0ff52b1b6f5eb54fdf275f7278`  
		Last Modified: Wed, 25 Nov 2020 23:24:54 GMT  
		Size: 6.9 KB (6894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0481971affd735ee187301b31eb72f31d60212e861b7d7fd56cebe2834e68c4f`  
		Last Modified: Wed, 25 Nov 2020 23:25:07 GMT  
		Size: 113.3 MB (113340348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4269ac39e3eafec3755b539d64a1b93b9a4b258d18161750e03f606fe55fd780`  
		Last Modified: Wed, 25 Nov 2020 23:24:54 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:3f963f6aa8d4c2a7e4f63baa1cf4c165dbfa085bd0a7a72d5149af93105ef935
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230218738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ac48a9dbd03d12686924d5884aede6cb6c8613bcc774d905eca7053a6e95b6`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Fri, 06 Nov 2020 21:53:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 06 Nov 2020 21:59:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 06 Nov 2020 22:00:03 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 06 Nov 2020 22:00:30 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 06 Nov 2020 22:00:45 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 06 Nov 2020 22:00:51 GMT
ARG BONITA_VERSION
# Fri, 06 Nov 2020 22:01:03 GMT
ARG BONITA_SHA256
# Fri, 06 Nov 2020 22:01:11 GMT
ARG BASE_URL
# Fri, 06 Nov 2020 22:01:19 GMT
ARG BONITA_URL
# Fri, 06 Nov 2020 22:01:26 GMT
ENV BONITA_VERSION=7.11.3
# Fri, 06 Nov 2020 22:01:31 GMT
ENV BONITA_SHA256=01300373642b7bfcc1fea717e1fd9caf460779ea1f35548d6eed61281f2e6068
# Fri, 06 Nov 2020 22:01:39 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.3.zip
# Fri, 06 Nov 2020 22:01:45 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 06 Nov 2020 22:01:50 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.3/BonitaCommunity-7.11.3.zip
# Fri, 06 Nov 2020 22:02:03 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 06 Nov 2020 22:02:20 GMT
RUN mkdir /opt/files
# Fri, 06 Nov 2020 22:02:24 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 06 Nov 2020 22:02:45 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 06 Nov 2020 22:02:57 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 06 Nov 2020 22:03:04 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 06 Nov 2020 22:03:08 GMT
VOLUME [/opt/bonita]
# Fri, 06 Nov 2020 22:03:11 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 06 Nov 2020 22:03:16 GMT
EXPOSE 8080
# Fri, 06 Nov 2020 22:03:20 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97646347816cc29a9c0edc917938e4c36c0bc216c00bccd71d4d3081847bb16`  
		Last Modified: Fri, 06 Nov 2020 22:04:07 GMT  
		Size: 85.9 MB (85916505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672916f10f4057c27c47fceb6de7be2bf4a17c4eb107341cc604422f0e7a8790`  
		Last Modified: Fri, 06 Nov 2020 22:03:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66096ecc3d12145ffdb754ef87d78ec23f8a93279fd33ebe5f0ca46acd85f479`  
		Last Modified: Fri, 06 Nov 2020 22:03:50 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0834cda6d12e2c7271465126a64b6671c0ad6c5aac4583ce022d5a391ce07af`  
		Last Modified: Fri, 06 Nov 2020 22:03:47 GMT  
		Size: 541.6 KB (541552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0c1d37b78bdc1c038f130c52752aac315c808a806799c76cc0670c368e5aa4`  
		Last Modified: Fri, 06 Nov 2020 22:03:47 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755313b6ecd3fd97b633eef37a140d3bb8577a17168509c4e5fd869f820aed7`  
		Last Modified: Fri, 06 Nov 2020 22:03:47 GMT  
		Size: 6.9 KB (6894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d9ca52ac7f89e66bcb3656eb3ac8d7dffc0b5eefd322c4d7d551826fa76ae5`  
		Last Modified: Fri, 06 Nov 2020 22:03:57 GMT  
		Size: 113.3 MB (113340348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6ba1d904db65b40ef279282190b0c5aeddde0a5c47c42cfbc6a1e6b3b86735`  
		Last Modified: Fri, 06 Nov 2020 22:03:47 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
