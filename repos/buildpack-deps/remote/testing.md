## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:c779e6b1b1a4a7e030d8717d772d6d0dad7f79d0d956dd58a5d01a2cc5758def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:45fb2ce9799b80ad29e60898a986078d01433cc1c03628788a04b5aee0e090e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339183958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ffee0a8d331521c018b2c3ba07fa67551f46e43c4ad72be79fd2dd9c3fcdac`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 01:19:34 GMT
ADD file:e413c7d61ecdc96ab067e1f8bff6ce03c792c94b9d1f54e80cf633052c5d975a in / 
# Tue, 12 Jul 2022 01:19:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:46:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:46:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 02:46:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:47:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c7a32fcf1e30b18b7a9a032acf892763291bef7159859a35297bf81217bbee4`  
		Last Modified: Tue, 12 Jul 2022 01:23:29 GMT  
		Size: 53.0 MB (53022393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00146b6ba9670f0b5362fb1ea6716d934ae0d1545d85efb6e7d9871f449ed7f`  
		Last Modified: Tue, 12 Jul 2022 02:53:57 GMT  
		Size: 9.3 MB (9292245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed5201b04ed0ec80bf5f970e6e10f4e241d58bfbeff69ec15faa4c6a34f01b6`  
		Last Modified: Tue, 12 Jul 2022 02:53:57 GMT  
		Size: 11.3 MB (11271764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0139c5963d20aff0bb13d34b320b3eae3eb708f57b7e951ad4fc79ed5f036b1d`  
		Last Modified: Tue, 12 Jul 2022 02:54:16 GMT  
		Size: 57.7 MB (57721761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d40908700ad3e88b14faa2f13a4d7bcfb8e3b7037bf8668f6ac034025d8165`  
		Last Modified: Tue, 12 Jul 2022 02:54:52 GMT  
		Size: 207.9 MB (207875795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:19fc78917caa8a50132db22a47247618c90a1640ad957840b2f70d85fda6fd5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310827324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c699f7120025a910e0e60a05330f2d8a92551798d832fbed5d71fd49d31fbc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:48:33 GMT
ADD file:f83bd7c88ccdb8f7b53f9072524438c8262a71b297a007c804923fd6d817479b in / 
# Tue, 02 Aug 2022 00:48:33 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:17:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:18:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:18:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:20:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f721a266d53173a0af0b138649440b41e425660c1bfb8506b479507fa2627c4d`  
		Last Modified: Tue, 02 Aug 2022 00:54:42 GMT  
		Size: 51.8 MB (51812934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6a541c310c2e2f0c838ea71f560b2bf4a91d0e9c4c71ab80c566d34acaae98`  
		Last Modified: Tue, 02 Aug 2022 01:28:50 GMT  
		Size: 8.7 MB (8739729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8928c72f00c51da560bfe1136e59212f70544fcc07732cc6b7156db46dbf7d55`  
		Last Modified: Tue, 02 Aug 2022 01:28:49 GMT  
		Size: 10.9 MB (10946664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd933a4710700cd7753f9558b1a5e9d88dbcb1fec5686f8fe3ad6a4ac1556370`  
		Last Modified: Tue, 02 Aug 2022 01:29:18 GMT  
		Size: 55.5 MB (55479066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ad58f49727106b97231711b8f9a1e17d2ded8fe3f26ba7554a391c8bc4473f`  
		Last Modified: Tue, 02 Aug 2022 01:30:12 GMT  
		Size: 183.8 MB (183848931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9a600d1bd9f374ba63199357fb2b43f0e3d84ff00611579519f7dc7eb4015653
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297698577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49dc73618886f3fd7c4d92c655d62e9893b318f326792a44d4fb294b963702ab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:57:55 GMT
ADD file:359193f5179bfdc5181bda2e05bd0b22ae4a86c638b0bbf09f289d1727fad222 in / 
# Tue, 02 Aug 2022 00:57:55 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:45:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:45:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:45:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:47:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:537407bee93780ba0135c6d74e62d8cee8d32e85ab926669d3cc9bedeef28852`  
		Last Modified: Tue, 02 Aug 2022 01:05:20 GMT  
		Size: 49.5 MB (49527674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21e0c1ecdb66b081e679eaee092b97020507b0a7735843a508a74b1ecb86429`  
		Last Modified: Tue, 02 Aug 2022 02:07:51 GMT  
		Size: 8.4 MB (8417992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2371236f490dda856391359574a3e2e3ecf9d8d39f77649c8c6839a1846326`  
		Last Modified: Tue, 02 Aug 2022 02:07:51 GMT  
		Size: 10.6 MB (10589533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503864111e2b00823bf24541ba248d5caaa84e32bc41634a765833fba8201148`  
		Last Modified: Tue, 02 Aug 2022 02:08:17 GMT  
		Size: 53.4 MB (53402629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b751166610da667d89fe195a173fc7be85f007e70bfb691ca710de49c23cc`  
		Last Modified: Tue, 02 Aug 2022 02:08:56 GMT  
		Size: 175.8 MB (175760749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9d696693f9992c86e6294fbc3036803915696286365cccfd06d9a459efa18cb6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.5 MB (334493472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5a859d9f6f66479159ae04bf8e6b38d4ea96d18292b92ad018e6fd171efc51`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:01 GMT
ADD file:66ffd29b395276f108023b4be1a449714b6fb1fcbcaf770debb7ec6910e84294 in / 
# Tue, 02 Aug 2022 00:40:02 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:22:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:22:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:24:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c76fc726ec0ec853818bf6b42fbe47810086904b89f146d4ccce624e8c5a33e2`  
		Last Modified: Tue, 02 Aug 2022 00:44:53 GMT  
		Size: 53.1 MB (53097492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446351798668b67b250456bd33621fa3f1239a40db1aa52cbae04c3c1524f3b9`  
		Last Modified: Tue, 02 Aug 2022 01:43:23 GMT  
		Size: 9.1 MB (9148571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a6b5eb548691ce9ed80e732c56ffc57a9ff5c14103b158596eb92a0508c44c`  
		Last Modified: Tue, 02 Aug 2022 01:43:23 GMT  
		Size: 11.1 MB (11062330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72738b07767d36266efbb85e749b932d343b20eb6acafb82341aa301f4d3d80d`  
		Last Modified: Tue, 02 Aug 2022 01:43:43 GMT  
		Size: 57.8 MB (57788160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0d20940fbe299ed915f087ef75dfcec3f6935c7f864936038996275345703f`  
		Last Modified: Tue, 02 Aug 2022 01:44:20 GMT  
		Size: 203.4 MB (203396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:dab794abea84650a5cf442c2e08165e58ac8e7519209e9143161b2b41ac2ec41
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343946065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9305d634ca5a5dd0d1d68b655657a4cd8e784540540525218720880cb0246fcc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:38:40 GMT
ADD file:f331e5b0e8626bfcbb682d701943586f63db1ff65d9add0d94759ecaeb8c8269 in / 
# Tue, 02 Aug 2022 00:38:41 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:06:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:08:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f78c3dc38f418186e278713175ef4cfc4bc70d85867d3597da89d03b5b956170`  
		Last Modified: Tue, 02 Aug 2022 00:43:55 GMT  
		Size: 54.0 MB (53974067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d30bb833cd65f6a8dd0078ee5cb794a55e3d1ecfe364e6976104636596e4fd1`  
		Last Modified: Tue, 02 Aug 2022 01:22:56 GMT  
		Size: 9.5 MB (9475285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e544133d2cd6d41cae7bfa63047f55cf4e607b50597b796c9562f4425da665a2`  
		Last Modified: Tue, 02 Aug 2022 01:22:55 GMT  
		Size: 11.5 MB (11473455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca79ad636ab4af17ce2eb8b9a9912b23a92742437fc984077a0f97ece1b9c85`  
		Last Modified: Tue, 02 Aug 2022 01:23:18 GMT  
		Size: 59.2 MB (59190696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d667b568cc30b58686e64c05de511cbae348f44eb28b2d875a80441e24494bef`  
		Last Modified: Tue, 02 Aug 2022 01:24:05 GMT  
		Size: 209.8 MB (209832562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2faa3d004c3d1c0715732c9b36565e3ff015016987b3d39483c7d97e3c4336f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.4 MB (319448185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c9b0582ca66fea6c77870f9fab3f40908382d7b4bf0d83f32d3e6054b3c01d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 04:39:09 GMT
ADD file:a4c1c80b05ba336cf2c87e4c90f5bd31ad9a6952b41985b49461741377bdf82f in / 
# Tue, 12 Jul 2022 04:39:13 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 05:59:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 06:00:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 06:02:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 06:08:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d42ff6e50c127c0849c96192832cf954071e1fe597bc69ae0894999838a3d95b`  
		Last Modified: Tue, 12 Jul 2022 04:49:46 GMT  
		Size: 52.1 MB (52148304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6761aa7c460392eac1c72e9e3d658302ae105a69f107d6b7fb8bce7f988b5b`  
		Last Modified: Tue, 12 Jul 2022 06:37:09 GMT  
		Size: 8.7 MB (8657917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6e4ee7231527a7e9598fb19bb5b34e13789124eaff6a2955f130d363356fb1`  
		Last Modified: Tue, 12 Jul 2022 06:37:09 GMT  
		Size: 11.0 MB (11033071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542574c436d1e1a7fb43145fb5d9e92a5cdb77987eceb090b0ddab0819c83fc3`  
		Last Modified: Tue, 12 Jul 2022 06:37:59 GMT  
		Size: 56.4 MB (56402664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca29d077fa9ead5f96d6f4e59cde30b153b8fa6c131d63cb22db6167fcd1cc8`  
		Last Modified: Tue, 12 Jul 2022 06:40:11 GMT  
		Size: 191.2 MB (191206229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6d4410d5fde13b6aaae133c06589a4a91b6ade1e6e18d38f186262e77e6e258a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.2 MB (357238409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a559dfc980d1962a4ff1c742677b13fe770a1e70be0f0d0e61543260beb7725`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 01:24:07 GMT
ADD file:ae1b00e1c53ca0bbd56262f1d2cd742362c7a02eed6214e944b4b4762dda64ff in / 
# Tue, 12 Jul 2022 01:24:11 GMT
CMD ["bash"]
# Tue, 26 Jul 2022 22:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Jul 2022 22:28:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 26 Jul 2022 22:28:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 26 Jul 2022 22:32:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8000c6ba1eb02ffb5f03a6b7e7d8f71a864844286f05cb8516ff71014b1cb870`  
		Last Modified: Tue, 12 Jul 2022 01:33:34 GMT  
		Size: 57.2 MB (57237580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40aa4d5388d97e0872477cb7660fbd3c341738064717f187dcfc90f0b64e8e89`  
		Last Modified: Tue, 26 Jul 2022 23:45:55 GMT  
		Size: 9.9 MB (9902776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05727228be0751bdf9f161f49f4edda690903161ccbf1593b8a4a16062ad8ce7`  
		Last Modified: Tue, 26 Jul 2022 23:45:54 GMT  
		Size: 12.1 MB (12082979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a298d404e383284543270c337de3d135d6d054da120136936a43e9d452360a`  
		Last Modified: Tue, 26 Jul 2022 23:46:27 GMT  
		Size: 62.4 MB (62430712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7f84da278ace9fc760d418483b0a7ab195c9a89a942f183cb561ae1e8d63e6`  
		Last Modified: Tue, 26 Jul 2022 23:47:39 GMT  
		Size: 215.6 MB (215584362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:57fb9cda7864376befccdba60b0413224dc32ed2b9bff5f027364c801ba026f1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310501027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdfb704283aef4b05b84723b02d390716be945c6a0e085d3c009420045e590ed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:41:38 GMT
ADD file:9364324d9e3e24a6e417365a226c42bac5c3c9589b444096a65d5bf539eec127 in / 
# Tue, 02 Aug 2022 00:41:45 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:07:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:07:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:07:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:08:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1a5bd7c6618b65a5948f8c07805e4109ef4f5aac36711b43d0fabe6f11fe0ec8`  
		Last Modified: Tue, 02 Aug 2022 00:47:13 GMT  
		Size: 51.5 MB (51514530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c61b0b54c9dc1946fb336e5a04c532d39a45e681f19f307f477085013dd8bc`  
		Last Modified: Tue, 02 Aug 2022 01:34:07 GMT  
		Size: 9.0 MB (8952435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1edc88e19b9b0261e01462a1883dcbc8fd4849c5a80450a4659c246ae5188132`  
		Last Modified: Tue, 02 Aug 2022 01:34:07 GMT  
		Size: 11.2 MB (11166761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322fa986d6da7624363b347b0ecc23718b41b493d8ee8b8ff0ff9e1c158ce17e`  
		Last Modified: Tue, 02 Aug 2022 01:34:21 GMT  
		Size: 57.0 MB (57027041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218863b80cd9b0b84378aa603587fa1a63bed8644c193bb83a697b01ddfcac7f`  
		Last Modified: Tue, 02 Aug 2022 01:35:03 GMT  
		Size: 181.8 MB (181840260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
