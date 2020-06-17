## `buildpack-deps:eoan`

```console
$ docker pull buildpack-deps@sha256:0d4ec89762d9ae7c1bc293464374fb2bcbdfa2a83c97cfe022c22cdee55d275e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:eoan` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:88f296e573b9c954c5237a8f7f407bbc1901c7206c095e8b28181a703f8d5b5f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234026657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d68c825a44e64a1e49c7cb980dff67db31d942a5639928adf60b3955afbcf2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:20:42 GMT
ADD file:f7e262b5b83427ba392961a76f015b60b140c12e8313ec3a5764b9829926a687 in / 
# Wed, 17 Jun 2020 01:20:43 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:20:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:20:44 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 01:59:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:59:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Jun 2020 02:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:02:36 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3f2411103a12c8e169df7a9ea00ff26ab07501858e3eff315a2e11c219e78ce1`  
		Last Modified: Tue, 09 Jun 2020 20:51:11 GMT  
		Size: 28.3 MB (28261433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da04088b2c299c17ae8a78858846c6fd4a6c36717baa816974cc75bef632871`  
		Last Modified: Wed, 17 Jun 2020 01:21:53 GMT  
		Size: 30.6 KB (30640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1184837b6f6f4a130c8b4eb72f576b86c4c46b3e33dada4740a966948d98e6`  
		Last Modified: Wed, 17 Jun 2020 01:21:53 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354c6da61dcc176c5b363ded571bea1de41b718131658fa0e563f2a749028cd1`  
		Last Modified: Wed, 17 Jun 2020 01:21:53 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a9187cd317f7b194fecbc5f1650c2c058a745867f75de00303ca6164f84d9d`  
		Last Modified: Wed, 17 Jun 2020 02:13:26 GMT  
		Size: 6.5 MB (6513812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4357e28c21183158d80ed73cb61a69c0a4de0643f020f19c7985fd99939f89`  
		Last Modified: Wed, 17 Jun 2020 02:13:25 GMT  
		Size: 3.5 MB (3517039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f18c86d98f6cb29a334c878b09cbcf9f20b080b566bec12a661631e38e6867`  
		Last Modified: Wed, 17 Jun 2020 02:13:41 GMT  
		Size: 47.4 MB (47412549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ead06469d8ab8f71317b3907a3a8b76bd639c3f913341812df05fa5e2d7355`  
		Last Modified: Wed, 17 Jun 2020 02:14:15 GMT  
		Size: 148.3 MB (148290174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:af838d81c766cd5ae52095aa557dc645a4aec1ba26d3aa48f7b09a8132116b75
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201770904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77346b1f3f933945450700767a4659dbebf9d88edc13bf6419098dc196e09106`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 02:02:31 GMT
ADD file:d43571d8ec3b0f10a1b242ded17304c8d0c67defd774479adc96b4919bb2a6fd in / 
# Wed, 17 Jun 2020 02:02:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 02:02:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 02:02:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 02:02:39 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:36:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:37:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Jun 2020 02:37:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:39:58 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ed534548814ba68388f69f6c9ebc41b3ba49406d1e3e47b6c8a7f232476505af`  
		Last Modified: Tue, 09 Jun 2020 20:51:36 GMT  
		Size: 23.7 MB (23724447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ae6c0ab304c4d5ecb78eee3114741bcd30b6c59f1e7a2a4b43c53c96d770d8`  
		Last Modified: Wed, 17 Jun 2020 02:05:40 GMT  
		Size: 30.6 KB (30615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9248b2a96ff45670a37617caa588330c35dde2dd20d637d82e8731e6e1095a8d`  
		Last Modified: Wed, 17 Jun 2020 02:05:40 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710b589714e81fef09237ff29abe689babbb3bc4e07749ff2728e96523bbaf08`  
		Last Modified: Wed, 17 Jun 2020 02:05:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70b606b2a386c3d69aaf3f31e9814f295789a510b8411709222e6d7236f6f5b`  
		Last Modified: Wed, 17 Jun 2020 02:49:17 GMT  
		Size: 5.5 MB (5531763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c648b4a1c3422be6b9ecdb415cf25414bc5ec38f462e12251149f46bddfea9a8`  
		Last Modified: Wed, 17 Jun 2020 02:49:17 GMT  
		Size: 3.0 MB (2983001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a7c5a18de18f72fe11d489b76020751195bc78672d613abcad77a25b7ed912`  
		Last Modified: Wed, 17 Jun 2020 02:49:38 GMT  
		Size: 43.1 MB (43132226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa047293586dad817112dec5ec048200f06403210be575c765c9e17314a8e56`  
		Last Modified: Wed, 17 Jun 2020 02:50:20 GMT  
		Size: 126.4 MB (126367812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:51c57785d2fc108047f1ac5abcf441ece41867d5f7ff12ed51dcaf90cd7c8de1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229423440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3a79514b8a7a0d033a86c702ebec0dd38bf15e034381affb6e9267b5903b23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:43:02 GMT
ADD file:afbae8593c2a310485f9ac20a2133d643aa78f1f287db87e1087832b0ea18b1e in / 
# Wed, 17 Jun 2020 01:43:06 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:43:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:43:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:43:10 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:16:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:16:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Jun 2020 02:17:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:19:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1afa64cae883b0ec934e8fbc2f830e304f115308af38eaf523297c4f609d268`  
		Last Modified: Tue, 09 Jun 2020 20:52:04 GMT  
		Size: 26.9 MB (26856827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bf5c9b0975d3d817466789f94fcfcc93d62ab7b6d979a9aa142836b712b047`  
		Last Modified: Wed, 17 Jun 2020 01:45:00 GMT  
		Size: 30.5 KB (30454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:522f9d93dd776c07db2beae6d659ea57f4129e53d53995f5b39925911ac873c8`  
		Last Modified: Wed, 17 Jun 2020 01:45:00 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87211bb3d9b9ceb47475623e94327d188e9a61a929af9908773d610bc4da51a0`  
		Last Modified: Wed, 17 Jun 2020 01:45:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fd4bdf0856ce4ef79c137ebd9daa48e62b5ade607c3227cf1ba5bf264a8d17`  
		Last Modified: Wed, 17 Jun 2020 02:35:01 GMT  
		Size: 6.4 MB (6370589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c2dc4fa12cb39c777fb38247574583a980ae89bf17ccc90d27f0ab3d3aa69d`  
		Last Modified: Wed, 17 Jun 2020 02:35:00 GMT  
		Size: 3.5 MB (3511857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4dcca8c6b1b84bea9f76e6b9d93106b22a69768033ad91ea8944efd3ba248a`  
		Last Modified: Wed, 17 Jun 2020 02:35:24 GMT  
		Size: 47.4 MB (47416802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd5532d2bcbfe98e95d58ba77489ddd1a24e7b8b66dc72900d4167992a6b576`  
		Last Modified: Wed, 17 Jun 2020 02:36:13 GMT  
		Size: 145.2 MB (145235870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f83f84e3d44c59a9b22383a313218f50c73655593ab317e1603cf7514568ab31
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.5 MB (238502589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be68b31eaf29eb22e5908ba4a23b7414a685526a5132cd7ec31a0d88d16ffb7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:39:02 GMT
ADD file:40320578d00c1821c8821f38e2a57315d599aed7b8fc7d9802b43c61a68f542c in / 
# Wed, 17 Jun 2020 01:39:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:39:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:39:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:39:04 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:00:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:00:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Jun 2020 02:01:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:03:20 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8c36fa2111ce9dcde83dd801ec64601f6c2b3c088bdcc38e9b6e1ccb6309b7f1`  
		Last Modified: Tue, 09 Jun 2020 20:51:41 GMT  
		Size: 29.0 MB (29035230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fa8cf01bad05acfd29371595c17cde6b9391303a29ac2ec1f6eb6841aef676`  
		Last Modified: Wed, 17 Jun 2020 01:39:49 GMT  
		Size: 30.7 KB (30719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19249f6bd8f71396680b10c2143643495fca3f6366bf9aec8520fd0190be7072`  
		Last Modified: Wed, 17 Jun 2020 01:39:49 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0944949ff614b039740df9433ab1d4992a6c0bf629dbcffe5795305c3b8898`  
		Last Modified: Wed, 17 Jun 2020 01:39:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bbc19c077e82d808d2be92c96e0b006d38de91a3f98a2d7f6397d5c537e59c`  
		Last Modified: Wed, 17 Jun 2020 02:08:53 GMT  
		Size: 6.8 MB (6843100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09935cd525a610ed6f45f15d31f8b6d63ab85b522334543d9fbc4865137b37d1`  
		Last Modified: Wed, 17 Jun 2020 02:08:52 GMT  
		Size: 3.8 MB (3810677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38de4fc219f6916b746f086f957651ecc0199c4a2d7897f16335f904c22324b`  
		Last Modified: Wed, 17 Jun 2020 02:09:11 GMT  
		Size: 49.0 MB (49018441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9147e90268e6fafe43ee2f9ed3c8e486768449be322c8c558ef6ff1ad5a1b90e`  
		Last Modified: Wed, 17 Jun 2020 02:09:53 GMT  
		Size: 149.8 MB (149763413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4f12b75f6c36e34c1a59de1da63fd3771e02ef21efea840b1d82e917a02e201e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260705502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a07a0e295c23716f2efe8c3b22aaf8fc2a6e34656d500104080fc7042130ef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:24:16 GMT
ADD file:b0e87075c5ec316f18389b20c0c211f819ef926d4b7d296772d1d647cdf28749 in / 
# Wed, 17 Jun 2020 01:24:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:24:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:24:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:24:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:16:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:17:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Jun 2020 02:20:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:30:19 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:760e28c7fe2c4974ed9f1ecefc9aebeb7ff99297aab78b2faf337a81f712d94a`  
		Last Modified: Mon, 15 Jun 2020 15:47:09 GMT  
		Size: 33.0 MB (32974436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba63d394568f664672606269aaafcd06adc7d7e715ff81c4c8fb027461d3b98`  
		Last Modified: Wed, 17 Jun 2020 01:28:35 GMT  
		Size: 30.5 KB (30484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8788fdf41b7effd6e7c13ee062e1896ae05d8efd7a658cca8b2ae2b2a13317e`  
		Last Modified: Wed, 17 Jun 2020 01:28:34 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f61bf6be23a47edee95c64efd8ce249f8154e352cfb567a1197ac559e59333`  
		Last Modified: Wed, 17 Jun 2020 01:28:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337e009a7e5b31958faf88280152cf8d3c2222e2052cdf0d95e4d33ea1a85aa4`  
		Last Modified: Wed, 17 Jun 2020 03:19:21 GMT  
		Size: 7.4 MB (7420723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3187264767c614c53e17669d015c43a9c6e1cd27c481eb7d7db7bfadca0b93`  
		Last Modified: Wed, 17 Jun 2020 03:19:21 GMT  
		Size: 4.5 MB (4463533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c2a553d7666755ad150a750ef59481c1631a0c37e077f9fbf1a2b2e06af2c8`  
		Last Modified: Wed, 17 Jun 2020 03:19:46 GMT  
		Size: 54.8 MB (54847906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c320a2a4229856491c78bbfe4bfef11c68a6a39a2a53382b79ce7afe58329df`  
		Last Modified: Wed, 17 Jun 2020 03:20:36 GMT  
		Size: 161.0 MB (160967380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2c6565216b1f4fa4fa322a1cbc0e4ddca21740f205141fd126ee4dc963f21f63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218436427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35a11517e5b45d1cc25494052cb2720d3d71362f9417b4a1eb1756b012e5c7b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:00 GMT
ADD file:de2223a9d367b5144964ef4803706aa5f0ce3c9da016847943d22ed84093c778 in / 
# Wed, 17 Jun 2020 01:42:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:04 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:10:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:10:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Jun 2020 02:11:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 02:25:46 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1347f68b26b409dd65f7ac87018777a80b9265c8e73f4bec19d61d3e01530e42`  
		Last Modified: Mon, 15 Jun 2020 15:47:23 GMT  
		Size: 26.7 MB (26672199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0f5e4e1faa13756ccb5717dc63e2fac83bab4340ec04ac2f235cc51244f7e2`  
		Last Modified: Wed, 17 Jun 2020 01:43:05 GMT  
		Size: 31.1 KB (31106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e64d224f0888ae8021041126daa2bf94c395927aabe3c5bc9bc2608e110089`  
		Last Modified: Wed, 17 Jun 2020 01:43:10 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019af11f3dc8756cf6f996afe32163d43c06949f160ab2d269e5520ecdee3b9b`  
		Last Modified: Wed, 17 Jun 2020 01:43:05 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0487f249704dc3a5d7fc50d8d8fb4cdc6a1ed85fc31733838cc41e2500af3e87`  
		Last Modified: Wed, 17 Jun 2020 02:54:19 GMT  
		Size: 6.1 MB (6140212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8578e2c6a1916f3cb047eb6e484057cdf50a06c389ae7f6b3461c7a73c2ac2`  
		Last Modified: Wed, 17 Jun 2020 02:54:25 GMT  
		Size: 3.4 MB (3433881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8307b8714c5c6f661cc8de6fc81cc82298b501bee323f310a171d9f1c29f97`  
		Last Modified: Wed, 17 Jun 2020 02:54:38 GMT  
		Size: 47.0 MB (47002160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f69cb8d084a151dc3989d54d69acf40a3c4f64690648fc92f7ffa6510ef082`  
		Last Modified: Wed, 17 Jun 2020 02:55:05 GMT  
		Size: 135.2 MB (135155830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
