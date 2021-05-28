## `buildpack-deps:groovy`

```console
$ docker pull buildpack-deps@sha256:ddb2e201077aad808c74597d106f0d4f21fd4febb528b3920e66b2160a142e9d
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
$ docker pull buildpack-deps@sha256:9c548506f9b1ceb61f3b2d708671c7ed2f156e94bac1f8c7bfef68d691eb93ca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246117309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5c2f76e33b815b2800a0f6ea8e3a3fc270bc4d0a801c83a77601730f84f24b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 May 2021 00:28:11 GMT
ADD file:5582a76cd73639bd7b5f941762801034fe6d3297d63d8333085c79c31b5e777a in / 
# Wed, 26 May 2021 00:28:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 26 May 2021 00:28:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 26 May 2021 00:28:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 26 May 2021 00:28:15 GMT
CMD ["/bin/bash"]
# Wed, 26 May 2021 00:49:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 May 2021 00:49:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 May 2021 00:50:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 May 2021 00:53:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0dfa4d6d32846900cdf518b31b7420c8e3bee78df56f061347f079b085e55eed`  
		Last Modified: Wed, 26 May 2021 00:29:22 GMT  
		Size: 31.3 MB (31339605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ba66a34e9b2cf96e7958749a4fdd29a90699b6cd7eb67976c266a8277a26b`  
		Last Modified: Wed, 26 May 2021 00:29:18 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6382425bb0d013b4122cc28ffc63f8bce680a6562260cb6fa715f6f16a59db`  
		Last Modified: Wed, 26 May 2021 00:29:17 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2855a438bbdf35b205c11cda343e79b366b32de44c66547fce2c6eef2ef7687b`  
		Last Modified: Wed, 26 May 2021 00:55:21 GMT  
		Size: 5.4 MB (5404036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c480a4de53ba6cd27f663db2d65a56c0919c0842d6b514480024ac528f40ea4b`  
		Last Modified: Wed, 26 May 2021 00:55:21 GMT  
		Size: 3.7 MB (3663044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f157cd28d7a119da3297972404c8ad1c208e53297bb28166922bb5e90578acd`  
		Last Modified: Wed, 26 May 2021 00:55:40 GMT  
		Size: 55.5 MB (55473629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef86475df853907b414475c6523466175dc1fa03f88c24ebc07525548c749e90`  
		Last Modified: Wed, 26 May 2021 00:56:12 GMT  
		Size: 150.2 MB (150235961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7976fe104ec00a2dff2d62e00a247b047f7bebaf5a75ce10db2e53ee16d30dbc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210518577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b921e83ebcde2e516dc51051f89a7a61ca0d77c62766e3278bc90b1ccf1933`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 May 2021 17:00:48 GMT
ADD file:64ff5c201737094749a157eeb3e4907949b36f17c0e8c4d4b2b7ac9633fe776c in / 
# Wed, 26 May 2021 17:00:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 26 May 2021 17:00:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 26 May 2021 17:00:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 26 May 2021 17:00:51 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 00:53:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 May 2021 00:54:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 00:55:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0e120224dfb47b00043c7e4077e526b2e311c86bb064631d6405bd428892c3c4`  
		Last Modified: Wed, 26 May 2021 17:03:50 GMT  
		Size: 26.3 MB (26313179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c256fbca870ac2acbc49bfa8e307393013f9593e0623e4ce9b0fd12c73c61c7`  
		Last Modified: Wed, 26 May 2021 17:03:45 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78179aa140f91b4c62e4a8a0c00c0f80a39f112b766c4e88be615f421c9d13d9`  
		Last Modified: Wed, 26 May 2021 17:03:45 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c31b2d3a6bdd8d0276daceeeb3d1cdc698234eb896fc1a371ec2c72d5a2ec2f`  
		Last Modified: Thu, 27 May 2021 01:11:43 GMT  
		Size: 4.8 MB (4840293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e366c83e8a1f0d1255ddaa8ddc08b77b5b167f35e730ab61d4847ccf2b6a1d`  
		Last Modified: Thu, 27 May 2021 01:11:42 GMT  
		Size: 3.1 MB (3140115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c02b5a9b863b150cb958e512330f378ef54bf2566b0135f9a37293005a2509`  
		Last Modified: Thu, 27 May 2021 01:12:12 GMT  
		Size: 50.3 MB (50288208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09f705600c064953f31da646fb2a494e0495e3027e2ab6bd8d557e211fa7f44`  
		Last Modified: Thu, 27 May 2021 01:12:57 GMT  
		Size: 125.9 MB (125935743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cf369efa756c9fd82f55eca0b11b004b13f73d375da203893f0d81bd13176243
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.1 MB (237085550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea0cc115241e93019cfd9a8d86c98ad1e48a2e13e96cdbd51153074b0def530`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 May 2021 12:30:07 GMT
ADD file:9f38584e54932330e111128e5969008e1d92aa7ee1b7f3af0622ee11a30ef661 in / 
# Thu, 27 May 2021 12:30:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:30:08 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 27 May 2021 12:30:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:30:09 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:59:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 May 2021 20:59:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 21:00:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:67cef43ca337885b5e8a4dc8a670b30651b42874b8fcf384957f2b016bbee3b7`  
		Last Modified: Thu, 27 May 2021 12:32:19 GMT  
		Size: 29.9 MB (29875040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93db328fd29467d3c5333c2f202b25c4d50c45cb5980d8f02fea273bb32bf310`  
		Last Modified: Thu, 27 May 2021 12:32:15 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4818fcf480a4c3442f1bf3dfb05adec183af6b462b89783fa8ad4c8493cd8746`  
		Last Modified: Thu, 27 May 2021 12:32:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296ddaeecce03790530b283e70ec6fe9c5132e608d6b3d208de7adb676d0b7ca`  
		Last Modified: Thu, 27 May 2021 21:11:38 GMT  
		Size: 5.4 MB (5372324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d297176d9ea581c24c19136bb30f276c603bbccba48803760cf2935aa5b318`  
		Last Modified: Thu, 27 May 2021 21:11:37 GMT  
		Size: 3.6 MB (3634689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7948ad65e37cccf41570a27421a5926356e2e77603466b33f25fe1a937eb9634`  
		Last Modified: Thu, 27 May 2021 21:11:59 GMT  
		Size: 55.5 MB (55452352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dea221397c39e2101a0284c1e1e5395e14a6cc4b762d907382e902eea8440d1`  
		Last Modified: Thu, 27 May 2021 21:12:36 GMT  
		Size: 142.8 MB (142750112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:047560279fb5ab3c3f9d5c8baa565aef5d681f3886f8c075b53053f02a3829da
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269456639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bef2ff0e30629ea249cb3be38161be600d3cbab5e5c6d46a3ece52930d4fb9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 May 2021 00:50:59 GMT
ADD file:417e85e230e48984b1cc0db245a092e51901fd8cf010070a82fd06ccaec211df in / 
# Wed, 26 May 2021 00:51:09 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 26 May 2021 00:51:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 26 May 2021 00:51:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 26 May 2021 00:51:36 GMT
CMD ["/bin/bash"]
# Wed, 26 May 2021 01:12:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 May 2021 01:14:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 May 2021 01:18:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 May 2021 01:38:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f7501b08507a493babfe9a7a361950a90febd51f598365c8c72a27438e176910`  
		Last Modified: Wed, 26 May 2021 00:54:09 GMT  
		Size: 36.5 MB (36545421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039b1bdfb29d855647202d2d86b6473a9b637d7edaafa7d199fe951071b946c0`  
		Last Modified: Wed, 26 May 2021 00:54:01 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63192a9aec9ad98562f0c79212fe107a71c90d1b3f55488cb16ca414d1d6853f`  
		Last Modified: Wed, 26 May 2021 00:54:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296ee47b5f35b125a133ce4bff94c000b52b76e704739c5a0d46be38f7deca42`  
		Last Modified: Wed, 26 May 2021 01:40:49 GMT  
		Size: 6.0 MB (6040577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfe4cc2db417d1a39f70a65a7e940e02096578289517774312678ebf9ab77b2`  
		Last Modified: Wed, 26 May 2021 01:40:49 GMT  
		Size: 4.5 MB (4521657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5fdfcf857c37dcd7a8b761b7e50458b2d139b48b06b5e115612d53ad928195`  
		Last Modified: Wed, 26 May 2021 01:41:14 GMT  
		Size: 63.7 MB (63742924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6e6f82937d1c66166673e73289233efabcca65f6e33608f78f0b54c303285b`  
		Last Modified: Wed, 26 May 2021 01:41:57 GMT  
		Size: 158.6 MB (158605022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ac11f64457dbd39c145478349240cf15aa313d4bf2bc8c86225c40d8822e25a1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246094738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ded3a841ae453bcdb0c2f58bf4a5543f8cd73a83a445685099bc81e1461349f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 May 2021 00:50:49 GMT
ADD file:953040401ce401194c7939af20d4b65872f29c9f1c9e9411f5b04fbd299161d6 in / 
# Wed, 26 May 2021 00:50:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 26 May 2021 00:50:55 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 26 May 2021 00:50:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 26 May 2021 00:50:56 GMT
CMD ["/bin/bash"]
# Wed, 26 May 2021 01:14:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 May 2021 01:14:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 May 2021 01:15:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 May 2021 01:17:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a86f368f271868bec872a3e420550decf4fa2f153ca0ebcec9ab48b642f129b1`  
		Last Modified: Wed, 26 May 2021 00:52:15 GMT  
		Size: 31.6 MB (31563545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf527448b6952fd5c7da27d42ed151c11bafb569d579a96ce879307419f0970`  
		Last Modified: Wed, 26 May 2021 00:52:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d46e2e6002b01a57ea745988830c3950a2aa33250abe3ebcd67891351feba1f`  
		Last Modified: Wed, 26 May 2021 00:52:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039f58efad91acfba39b19901da37ac258ccb25fb301301dfd989ca742b01940`  
		Last Modified: Wed, 26 May 2021 01:19:29 GMT  
		Size: 5.6 MB (5629719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294f314beb8886b2a3ca040687069cef7b938d4da9642e8ebc5ca6d4f575bf2d`  
		Last Modified: Wed, 26 May 2021 01:19:29 GMT  
		Size: 4.2 MB (4156537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e77438315d9c7860234768a2fb85a9c1b0fda9006148ff1ba5d1539c89e4d2`  
		Last Modified: Wed, 26 May 2021 01:19:46 GMT  
		Size: 60.7 MB (60650009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7fadeb804e8e3317362c194e8633afa06af49e545705920f8faf054c2061fa`  
		Last Modified: Wed, 26 May 2021 01:20:13 GMT  
		Size: 144.1 MB (144093892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
