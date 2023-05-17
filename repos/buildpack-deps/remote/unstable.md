## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:470ec0cc2b3a5ea8a7a1aaeb131f4c59bf91f0ceef3a0be584f0f349d4378908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d06b9c9a0b43d5cf9ba185cb98902d5d006604d7ae912e99cc49e2bafacfbcbc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.0 MB (344986510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db522652278aba4050aa04755035020098e12ee7f98d0b89e685ea61d8c582f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:42 GMT
ADD file:6261ecb921e04d2b3f6fd44e5dcb5683154bc0beee4f26913c2be9395a060489 in / 
# Tue, 02 May 2023 23:47:43 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:01:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:02:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:02:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ae396e350f30e1defad1bfa67a84b97389d42cf3442551e39a0e2bab6b53a50c`  
		Last Modified: Tue, 02 May 2023 23:51:56 GMT  
		Size: 49.3 MB (49299270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd17d28808409b147a3bf1ad99b0f7837c93556c98e22adfd32391f10cd514c3`  
		Last Modified: Wed, 03 May 2023 20:15:05 GMT  
		Size: 20.2 MB (20241988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c7fc303564e2f5840c7571b2755251add439e9c918e410cb9101bfa2d3e540`  
		Last Modified: Wed, 03 May 2023 20:15:22 GMT  
		Size: 64.5 MB (64511077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa3739c6e2e043a0c968190dde8dec2ee8d9a1e0a1666a9312f3b1e250f9aeb`  
		Last Modified: Wed, 03 May 2023 20:15:56 GMT  
		Size: 210.9 MB (210934175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:288ece3416492c64e1248ee272ccbef0178d92acca26bc0d426cf3692770c575
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.6 MB (317567457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0131abeadc3caba3acc73222ae0a5422865e85564d3d7fdb6cbac0e16e7c320`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 22:49:00 GMT
ADD file:2228a07c6ec82db1e0719684d77cecf448c3be947c2b1b48347ba5de9e5b57f8 in / 
# Tue, 02 May 2023 22:49:00 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:52:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:52:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:53:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:90d5a5fdc15637fce928afc279fecd9adb82fe3c476f174458fc6bdd7fb4b57e`  
		Last Modified: Tue, 02 May 2023 22:51:47 GMT  
		Size: 47.2 MB (47167062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3aabdf1b5f4fe267ba781854e71260b46210e5625adf002fe5ff5e24865561`  
		Last Modified: Tue, 16 May 2023 23:55:08 GMT  
		Size: 24.0 MB (24009742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5c70d2aaf967c21be93aee1715376be9d7e6080ca3b20e1fce409cbb398017`  
		Last Modified: Tue, 16 May 2023 23:55:27 GMT  
		Size: 62.1 MB (62140663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebcc5c1bf73c642c8f84ac83643aa00abd40f5b52cd4892a91e95084a799f7c`  
		Last Modified: Tue, 16 May 2023 23:56:01 GMT  
		Size: 184.2 MB (184249990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:54e96cc0b444702a2e08116f00f2c5b58d704f39d7d063ba949966d99c3e53ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302905039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4d82fce231bab872e199f0c47c7398de32aac9c7bf10625868625572586fe2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:48:42 GMT
ADD file:17739fc730ad8febc64f53eec61cbf10f8d2c5184cfda5466e89ab423a88f9d6 in / 
# Tue, 02 May 2023 23:48:42 GMT
CMD ["bash"]
# Wed, 17 May 2023 00:02:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 May 2023 00:02:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 May 2023 00:03:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0b827c534260a55126ac3b18c14ea9160a3a3a03448b5c2b4462f9f3f4cf0ab`  
		Last Modified: Tue, 02 May 2023 23:53:05 GMT  
		Size: 45.0 MB (44988077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858686fb647755cfaf9d97846212a8b1056f291d77f962bb8bf7be5d16a5ff60`  
		Last Modified: Wed, 17 May 2023 00:24:35 GMT  
		Size: 23.2 MB (23219225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16fdb017446b11706119bca2906a6b8fa79ccf636d08457981e54be450413bf`  
		Last Modified: Wed, 17 May 2023 00:24:55 GMT  
		Size: 59.8 MB (59773847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05930ecf1b48b63067b8734906c94169606839e7d6c40620dd661cdf4f03308a`  
		Last Modified: Wed, 17 May 2023 00:25:28 GMT  
		Size: 174.9 MB (174923890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:153eeec75f8135d836bbbff8dfcf3bebed936d7e05eadafd9e3f94ca1bfe31a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341082531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd1e95af413f229da5d28234c5f7a5efb0e701e944a0d0ba946a2059cffeb19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:23:28 GMT
ADD file:cb107aa90220a9fc72fe1e3aa26878752691d6e9eb04696738920b5834c6d9e2 in / 
# Wed, 03 May 2023 00:23:29 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:42:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:42:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:43:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:77a3c1a83d83f65ef8fd579d19879f09a4018e384f42cfa55f82d426f32ff840`  
		Last Modified: Wed, 03 May 2023 00:27:15 GMT  
		Size: 49.3 MB (49345262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52781deab323ab07663419dcbd3af52651bfaf9895ae88fa6160c7a78b5c7c0`  
		Last Modified: Tue, 16 May 2023 23:57:13 GMT  
		Size: 24.9 MB (24896432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c9f3ed5b90a971a7d8c99f95aa99252f2fcd3a7fadddd62e9c1b012f89b3b6`  
		Last Modified: Tue, 16 May 2023 23:57:29 GMT  
		Size: 64.5 MB (64497777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bd71f8afc49b877c7eabe5d7816e2ca3c1b93ac5a23f3d04d37f8b90c410f2`  
		Last Modified: Tue, 16 May 2023 23:57:55 GMT  
		Size: 202.3 MB (202343060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f5924fb47db8226d35d969903baa8bb9fd820a0a02d0422cc7c59f9f3d599d10
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.7 MB (352721139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a903a8d39f26734e47ded5ebefa2f94a5b77b6a7cbe80b3c966927874aae2a11`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:01:59 GMT
ADD file:4abf127b0d4037b2d94457a8ef168165ed6946fec0635fdaa845ed4ee8f74681 in / 
# Wed, 03 May 2023 00:02:00 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:44:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:45:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:125509149936f5c9fc010cb99811f5cb23108af74e034fcf0903d3f2cc08d893`  
		Last Modified: Wed, 03 May 2023 00:06:56 GMT  
		Size: 50.3 MB (50321774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4a96d98aebd4e76698b47d9e1a7e5c5b576c22314cb670e159aa6548a7e385`  
		Last Modified: Tue, 16 May 2023 23:47:11 GMT  
		Size: 26.2 MB (26192711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce172b2251db3844f41f864eda3f64f8d4c0141d0557af09d03c8a0725ebd47`  
		Last Modified: Tue, 16 May 2023 23:47:32 GMT  
		Size: 66.3 MB (66340255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac1711fa8697446abb4fae10aeafbe252cba600258a0dd74ffaca859b76bbe4`  
		Last Modified: Tue, 16 May 2023 23:48:18 GMT  
		Size: 209.9 MB (209866399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c39e9ee4e324a29343a4f0295017e16053221a90a88af68f467e5eb6685fbdba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.5 MB (326466979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e511ebccf5d054b0403be92616bd319b8538fc1cc8cfa7bbfc772bcf7e279535`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:50:24 GMT
ADD file:3eff171361a4eb801d0fe38f81ca109a46285fd25a23f84aa338364d49c0591d in / 
# Tue, 02 May 2023 23:50:30 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:54:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:56:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 May 2023 00:02:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6ad09064fad2597f74f486eca3ca74c1f51072bf61093439cd70c0d5735689aa`  
		Last Modified: Tue, 02 May 2023 23:58:51 GMT  
		Size: 49.3 MB (49301428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c533f052cb6f9d390977495e5045e622d198eff3064421eab4a0476cb44dc6`  
		Last Modified: Wed, 17 May 2023 00:06:07 GMT  
		Size: 24.2 MB (24206980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b8dcf757e238ec443e11e6688d2932c5b7fcdd1a6033170446c15b90305e01`  
		Last Modified: Wed, 17 May 2023 00:06:56 GMT  
		Size: 63.4 MB (63421941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5639bd40fccfe0d084a5a6e0eba5b18068126e1cc2399560ec181a8b9f9d11`  
		Last Modified: Wed, 17 May 2023 00:08:58 GMT  
		Size: 189.5 MB (189536630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:077816016367870804b7b5ef40f8597601bc697749315bd898b2ace7f02f1063
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358824159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77634842c2cb762f4280494be8ab4bf9ca10bbcf929e61776172dc1ec526b20a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:32:10 GMT
ADD file:c9bb656a5f751ff13849f6ca569f657cfc8dbe757b270dfa6e9fe2181e699494 in / 
# Wed, 03 May 2023 00:32:13 GMT
CMD ["bash"]
# Wed, 03 May 2023 23:17:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 23:17:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 23:19:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71d18ac463268aeb15f1776de10a379de577489dfb1022fc92adf6187695aeeb`  
		Last Modified: Wed, 03 May 2023 00:37:22 GMT  
		Size: 53.3 MB (53307234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0418f9e193f610de7186baec4f50ba3dfb4d394491ce54a0bbbf54eafb72013c`  
		Last Modified: Wed, 03 May 2023 23:38:43 GMT  
		Size: 21.6 MB (21584485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff34e388dfd0cc4b77ae1014ae05ab11a5f0f26fb3bbfd47f3dd41bcb48bb428`  
		Last Modified: Wed, 03 May 2023 23:39:10 GMT  
		Size: 70.0 MB (69953589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c881e9f43ab9a0bc539e3baae38e777174c80389aef3715ce4c78f3ae43f3ed`  
		Last Modified: Wed, 03 May 2023 23:40:12 GMT  
		Size: 214.0 MB (213978851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:12adeb17b70a35c1c949d02fd340381a96e45f3e1357ae31e6741dc4b203d8a3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.3 MB (356278392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edc6f31938e2300aac23d2456cb5e56e9d5f903b4c676136993b343ebe82932`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:29:17 GMT
ADD file:4e365b380d9cfb77573624c399d3376d19fa5c7028c44b681071b426fb1c6db0 in / 
# Tue, 02 May 2023 23:29:19 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:51:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:54:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 00:02:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:29b183cb384ba20db9a991d4213be72a43fcec3d5fc87f259bd5719d35027d1b`  
		Last Modified: Tue, 02 May 2023 23:32:35 GMT  
		Size: 45.5 MB (45510102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93940bc329d1d971861f44e84f01d2bf1b1b0075644023b2caae44992f0e70cb`  
		Last Modified: Wed, 03 May 2023 00:03:11 GMT  
		Size: 18.7 MB (18656704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d9b13ea8a5a6cc6efb43a7b1b940dbe6a4cf4e6dfd3a66e0d926891398ac6c`  
		Last Modified: Wed, 03 May 2023 00:04:32 GMT  
		Size: 60.0 MB (59957056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65751e6feb8ebfc538ee01d19da0c0de0f28112bf667890c6565039d166b71f3`  
		Last Modified: Wed, 03 May 2023 00:09:49 GMT  
		Size: 232.2 MB (232154530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2f0e211951042f7f1cf40b2862a68399a2ede5730dfb51d144b13bb88289de24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.6 MB (319642888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29609bf90989836428d165180d62b49d8ee1a619abd7efae09463e30410ecaf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 03:42:08 GMT
ADD file:f714218b704bfe42a591f19c2fc0360b178732edfcd6b12687ea572c74b84171 in / 
# Wed, 03 May 2023 03:42:11 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:43:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:43:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:45:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9cad3c2eaf2133414000bf2d83ce6816eb4031d5b81288493af8102df33f2e4c`  
		Last Modified: Wed, 03 May 2023 03:45:13 GMT  
		Size: 47.7 MB (47675884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bab5e47182cd759c84de89b674a6e02b13aef910e9d07d034d7b802c36c2c9`  
		Last Modified: Tue, 16 May 2023 23:55:48 GMT  
		Size: 25.4 MB (25352347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79c5309e9a86c28868504dbce3cd42aab010a6909a28eee8682f5a41cf684d5`  
		Last Modified: Tue, 16 May 2023 23:56:03 GMT  
		Size: 63.6 MB (63605877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af793130316301ffbf3e74da80ce407f623368f63319cbb8b9847f0c32e9cff`  
		Last Modified: Tue, 16 May 2023 23:56:33 GMT  
		Size: 183.0 MB (183008780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
