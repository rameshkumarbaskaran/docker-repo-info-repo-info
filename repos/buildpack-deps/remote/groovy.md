## `buildpack-deps:groovy`

```console
$ docker pull buildpack-deps@sha256:bc101e4a47623c0ea185a19c95d607f03f46f004fad7f2dacd4a826c5870852c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:groovy` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1e34730d0a550f41d2feaa453eb656a6de0d622dfa132ef96127818fd03db774
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244551245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a14461d832f5045285939ca3ba06f6461510e40fe18a96b754fc23ae44634b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Oct 2020 17:32:46 GMT
ADD file:6099585856c27a9f8dd40d7e679184a6d1bb58133acf73d5d3c9904932def005 in / 
# Fri, 23 Oct 2020 17:32:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 17:32:47 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 17:32:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 17:32:48 GMT
CMD ["/bin/bash"]
# Fri, 23 Oct 2020 18:01:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 18:01:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Oct 2020 18:02:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 18:03:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7a14fb4cd302ea60d4b208f17bb50098b52a17183a2137c08299a3b915d7cbae`  
		Last Modified: Fri, 23 Oct 2020 17:33:40 GMT  
		Size: 31.3 MB (31337938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b1fecc905c746712dc231f73c5d630927892af991ce140673eb77dd9b697cd`  
		Last Modified: Fri, 23 Oct 2020 17:33:35 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ac8019c9736cea870759cf87bf752344fd3fb2dbf7a3921e9c60e140213900`  
		Last Modified: Fri, 23 Oct 2020 17:33:35 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b137add616873c756cd3a60d7de3e8ac2ad471a32a8d7e7fba112082ac32f5`  
		Last Modified: Fri, 23 Oct 2020 18:08:23 GMT  
		Size: 4.5 MB (4515029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee9baeffa76ee358acf2e9423b3bd03ff13ef4361cda101c57242f87268fc7e`  
		Last Modified: Fri, 23 Oct 2020 18:08:24 GMT  
		Size: 3.6 MB (3587545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9a37c16661daea48912319bcac62ebc465498b050a168b140e35fdedb5ab5e`  
		Last Modified: Fri, 23 Oct 2020 18:08:42 GMT  
		Size: 55.0 MB (55013337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b4316385454a48bc9998e88339aef9ecbe25ba68206d852d936820329727c4`  
		Last Modified: Fri, 23 Oct 2020 18:09:19 GMT  
		Size: 150.1 MB (150096389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:862c3b2ec1a3d003495309dc88d8a4140944eafec0671bd23b73298f96d13ec6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.0 MB (209010016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550dfb9ab7bce2e8adb1f5e8a31ef9a2c7133e6399be2560168eed3a8fab446c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Oct 2020 18:16:42 GMT
ADD file:0eeb4202bc0d9b7d0c78bff294ff6015f21c8fb8e9ca0ff983ff6c78d5897235 in / 
# Fri, 23 Oct 2020 18:16:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 18:16:46 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 18:16:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 18:16:48 GMT
CMD ["/bin/bash"]
# Fri, 23 Oct 2020 18:42:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 18:42:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Oct 2020 18:43:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 18:44:59 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f17eabb5dfcad75fa1be363632f687064e41500f8c6fe95ae2ef3bcdf7c32c0c`  
		Last Modified: Fri, 23 Oct 2020 18:18:04 GMT  
		Size: 26.3 MB (26298569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d196182becee925f94a0471151ee4e042efe951ee13958f732f1b7c094aa6619`  
		Last Modified: Fri, 23 Oct 2020 18:17:57 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06172a7b7f85373b7794e70e99b64be5361635df132bbde4a4773b41f054659f`  
		Last Modified: Fri, 23 Oct 2020 18:17:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43db61c8d962a4885826b1982ab535ffd6828cea2acbe0981ca260f11727cfd0`  
		Last Modified: Fri, 23 Oct 2020 18:51:02 GMT  
		Size: 4.0 MB (3953516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09266347ab8142f8237419749bbdc85ef3334e9e808fb7da9b93b594b5acd745`  
		Last Modified: Fri, 23 Oct 2020 18:51:01 GMT  
		Size: 3.1 MB (3061341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d547e331855d6a3010db77fb2b3f9ff8a012fa9ec112eb8354d64e4009c138`  
		Last Modified: Fri, 23 Oct 2020 18:51:26 GMT  
		Size: 49.9 MB (49892332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3bb71705385661fc002b36f8c44265a940ef6a4f17361b1a5b4f25e04147066`  
		Last Modified: Fri, 23 Oct 2020 18:52:12 GMT  
		Size: 125.8 MB (125803221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3ac223345610de52a09bd5b620cd34c6be7ec9ce550c9207af52c4fce3c1c68b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235630176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40907eea848842a4909d7393c173a335a1541bde725cd02c45478a58a9480624`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Oct 2020 18:19:57 GMT
ADD file:eba1bf343f462dff24cd8570c557a24680d651c0accfaed36f4d3845e30f92de in / 
# Fri, 23 Oct 2020 18:19:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 18:20:01 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 18:20:03 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 18:20:03 GMT
CMD ["/bin/bash"]
# Fri, 23 Oct 2020 18:47:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 18:47:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Oct 2020 18:48:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 18:50:29 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:52b0f1f415e4765da3991a8d5e5c3d6bdf45adde4a31fe000210c37e09281ad4`  
		Last Modified: Fri, 23 Oct 2020 18:21:16 GMT  
		Size: 29.9 MB (29884705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7b4c42c4aa2ad2610ea0264f0a465ac8caecaebf3f6126595042adb7ab1616`  
		Last Modified: Fri, 23 Oct 2020 18:21:09 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566e53edfb1c98cf8ccea2ad6fdf8e3c67d3876df1d842cc33b5e373551af235`  
		Last Modified: Fri, 23 Oct 2020 18:21:09 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d138e6b088e2167ac9411cba16ccb3f2a1e8b3f982d39cd3b5f067a8777195`  
		Last Modified: Fri, 23 Oct 2020 18:55:52 GMT  
		Size: 4.5 MB (4493043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4072107c812c1ddbe9e3f9c03c04c93f931c8a135ebcce053be48d66dbb2ae`  
		Last Modified: Fri, 23 Oct 2020 18:55:51 GMT  
		Size: 3.6 MB (3572808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3209e1daa43b546f73c91211d5397d25eba069311f490288a49e6802a9b8599d`  
		Last Modified: Fri, 23 Oct 2020 18:56:13 GMT  
		Size: 55.1 MB (55051623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c264dfd5e66ed4af081c0c2236b8c95febf588dd2aad7c2eee92f7654a89ebb6`  
		Last Modified: Fri, 23 Oct 2020 18:57:30 GMT  
		Size: 142.6 MB (142626961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b6d0059d4afc9da3b9446bb38c495d96380725657e9d2d96e38914528f69cd81
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.9 MB (270939178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08b530f571f8cc1e15a325fbe37adb30689cfba9c0bcf0e74e4ce5b2e994bf2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 23:57:16 GMT
ADD file:1d127c60d27e61fed1bc05efcd1e053216bd515f25e598f2bd2192798a432b38 in / 
# Fri, 25 Sep 2020 23:57:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:57:49 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:58:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:58:15 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 02:19:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 02:20:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 26 Sep 2020 02:25:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 02:43:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fa412f0e85b1faf347e6f09ddf91451a53108addc78add28b908a3d945af88c8`  
		Last Modified: Mon, 21 Sep 2020 15:56:56 GMT  
		Size: 36.6 MB (36564503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f869fda62abc9fccaeb5e79724beec764d6fa02d1d2accb759a271979311dbd1`  
		Last Modified: Sat, 26 Sep 2020 00:07:16 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1f0fbca858631e5429a6e9c42dc3c15284957004c30d7965889e5ad5a116f9`  
		Last Modified: Sat, 26 Sep 2020 00:07:16 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6d0dd3850e8dd7f0d083a2c986d6e35878df4ca17d5876d543cb15e37dc32d`  
		Last Modified: Sat, 26 Sep 2020 03:16:10 GMT  
		Size: 5.2 MB (5151317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049532e919fc17854e7574f3c91163ed72cafb6d1a60996045223ccef96adcde`  
		Last Modified: Sat, 26 Sep 2020 03:16:10 GMT  
		Size: 4.4 MB (4449846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8739f4c812b9cac8b015392febb466060da99a0802d18cefbf4ec03a132619e8`  
		Last Modified: Sat, 26 Sep 2020 03:18:04 GMT  
		Size: 63.4 MB (63432199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60ca924810df22784a2976b1a0ee8b45db56e4b1b9663b07b7c91bcfc9b142d`  
		Last Modified: Sat, 26 Sep 2020 03:20:11 GMT  
		Size: 161.3 MB (161340275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3bd732352162ddbcd56692f6d7351244ff271de87546fdd5524b84f9a3c8be51
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240800291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd65f5d3f2ab0b686e0519396f4e4064bf8781c4915c538b141b0f966f89d6e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 22:45:17 GMT
ADD file:89492d6e96925fde151f47721bb76d3d3497e248deebfcd8470c53e9b16a8037 in / 
# Fri, 25 Sep 2020 22:45:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:45:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:45:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:45:21 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:22:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:22:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 25 Sep 2020 23:22:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:23:22 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b91259bd471bf4c457bc7a08c109ddb2d7e96dd9a3c2a2fe6efbf8fb94cfbda1`  
		Last Modified: Mon, 21 Sep 2020 15:57:23 GMT  
		Size: 31.2 MB (31186236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f77b06dfaa40a67e6b37fcec76245eebcdecaf6b93a73c88f74352b36294417`  
		Last Modified: Fri, 25 Sep 2020 22:46:10 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168e47b5b6ebe06b0c93b79e3350cfba27d0ef79386c2859df93ba66c8083e28`  
		Last Modified: Fri, 25 Sep 2020 22:46:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452def7cd68695a7e737dc1860047132f164c6de0fb09b2cd1fb0f40f2bebe58`  
		Last Modified: Fri, 25 Sep 2020 23:26:52 GMT  
		Size: 4.7 MB (4709178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ffc553793ba56a9a6403e2cac0dde3c1428211510febadc0a6f28b0000b8b7`  
		Last Modified: Fri, 25 Sep 2020 23:26:52 GMT  
		Size: 3.6 MB (3582294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9c1f4bac14267b1c4178a5e8a6f6e99f1897a60ca3a05901c05895a60f5e2e`  
		Last Modified: Fri, 25 Sep 2020 23:27:06 GMT  
		Size: 55.2 MB (55184795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c182d7d840fbee64c7067093fab8c3bb5b96ab2a7c21c2c2b19bf5d415e9a2fd`  
		Last Modified: Fri, 25 Sep 2020 23:27:32 GMT  
		Size: 146.1 MB (146136755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
