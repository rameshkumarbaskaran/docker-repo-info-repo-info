## `buildpack-deps:bookworm`

```console
$ docker pull buildpack-deps@sha256:6f29420a8d7ee5a3455f18da2c139975ab72f9bc2d243921a2a19a8ebd816208
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

### `buildpack-deps:bookworm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0b77ec844ff095ee6ca73bc3fa862687eb6568b8fa04ad169235470db37175b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.7 MB (348740165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7d79b2a55e0ab1155cae2f0b0b90ecf92699dbbb895f91c4dd9c8d8cb45382`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:26 GMT
ADD file:ce04d6a354feaef93795269c859f36667fce9efda23c61b37d7060263b66ed4e in / 
# Wed, 20 Sep 2023 04:55:26 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:20:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:21:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:21:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:167b8a53ca4504bc6aa3182e336fa96f4ef76875d158c1933d3e2fa19c57e0c3`  
		Last Modified: Wed, 20 Sep 2023 04:59:55 GMT  
		Size: 49.6 MB (49557601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47a222d28fa95680198398973d0a29b82a968f03e7ef361cc8ded562e4d84a3`  
		Last Modified: Wed, 20 Sep 2023 09:29:57 GMT  
		Size: 24.0 MB (24030522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debce5f9f3a9709885f7f2ad3cf41f036a3b57b406b27ba3a883928315787042`  
		Last Modified: Wed, 20 Sep 2023 09:30:18 GMT  
		Size: 64.1 MB (64112257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7ca7cd2e066ae77ac6284a9d027f72a31a02a18bfc2a249ef2e7b01074338b`  
		Last Modified: Wed, 20 Sep 2023 09:30:55 GMT  
		Size: 211.0 MB (211039785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:86d28c1e87df6d4e3309e403a9ced8594ad1380ffb29db3cbb99ee65245d77e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316030711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61c441d8080fa400d21357cb9170445e8b0e150d15c350be1e20d0849837a84`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:37:30 GMT
ADD file:c07cf5c750a3e3c7ff84a3a3b8fc6087c9c5e0639d7bf638f0556d0a94309919 in / 
# Wed, 11 Oct 2023 17:37:35 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:04:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:05:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:06:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b7ec6536594e6c45ab234eecb51aacd85440ddc0e6da5873de23938ff146b5ec`  
		Last Modified: Wed, 11 Oct 2023 17:40:19 GMT  
		Size: 47.4 MB (47355749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ec943df1872e82ab3efa51bd5b2d7aac598550123e6db67156283ade7509d1`  
		Last Modified: Wed, 11 Oct 2023 18:14:31 GMT  
		Size: 22.7 MB (22729282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9f5c18924658cf6e03e52e00ddbf230cb1925aa017edb92b3cd508ec76293f`  
		Last Modified: Wed, 11 Oct 2023 18:14:54 GMT  
		Size: 61.6 MB (61561678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7670741713d795c2814eacfe8b75187f28e3485379b6fb2770c71d163e26127`  
		Last Modified: Wed, 11 Oct 2023 18:15:37 GMT  
		Size: 184.4 MB (184384002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:712fc02e2b27d8c0f2f491bad1a5ec106832bb703ee3764fdbf533ea79ae16c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301450257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45a3b495c3b78d28b8530d72e5c1f46a85d3fcf223cbf2e181055b763046cde`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:57:08 GMT
ADD file:e8c98b19a39772b96a8bfa0f38abfc620498f040012f9b9906640975ac01ce0d in / 
# Wed, 20 Sep 2023 04:57:09 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 15:24:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 15:24:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 15:26:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:013e3017888216ce95d0ffe3d0fb039c509402dc99800465157f56e7520abd4a`  
		Last Modified: Wed, 20 Sep 2023 05:00:53 GMT  
		Size: 45.2 MB (45232576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b45aaa3d8d542a2281410c108a016f367f050793bb029d35cca677cc0d500f1`  
		Last Modified: Wed, 20 Sep 2023 15:35:12 GMT  
		Size: 21.9 MB (21936768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecb66b8eee4d1eb823c09a41799c3f25f6ef9f31c3ef273c3b37419d8c39606`  
		Last Modified: Wed, 20 Sep 2023 15:35:36 GMT  
		Size: 59.3 MB (59262478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72dc52e910dd753d54c6e3c960b1d79d8719a60eff848e822cee998e217615e0`  
		Last Modified: Wed, 20 Sep 2023 15:36:12 GMT  
		Size: 175.0 MB (175018435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1217daf5693bf080affa2383e80682e4ed80fa25c7b6889924e21e401abfef07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339643434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13543f9c2ab23caf4e23f3900fa93f86e7a0d57bbfb3dfb296c3985b777511b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 19:44:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 19:45:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 19:46:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7541d83e7b8c0f5f6cacacddfcf5fdd942793f13418bc4645203b4ab4f3de3`  
		Last Modified: Wed, 11 Oct 2023 19:53:48 GMT  
		Size: 23.6 MB (23588086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a653d69b7b96df6835b157d043d7b926f776531e96c9263f4c7dae0033514d`  
		Last Modified: Wed, 11 Oct 2023 19:54:07 GMT  
		Size: 64.0 MB (63994319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02d5d50082e4632f070b715dfd5d3a3680e35e0434a1281edbcfdc3cdff52dc`  
		Last Modified: Wed, 11 Oct 2023 19:54:39 GMT  
		Size: 202.4 MB (202448451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1a6a219086627846d966e869a8d56fd78994fb747da91f49e6a46a674ef778c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351462994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4402f88a53734d262ec398d9da3786d89072972edfbbc52175a078d23b80d0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:40:29 GMT
ADD file:0b6fc66d778d0cd8ae8b17b92945d98cc34f9c7008cda864ed0a54b5e40b9cb0 in / 
# Wed, 11 Oct 2023 17:40:32 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:09:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:10:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:11:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:501a599c15b6def048b2e00cfdf6c658061c00a504305ef2075fb1009a62c1e2`  
		Last Modified: Wed, 11 Oct 2023 17:45:01 GMT  
		Size: 50.6 MB (50600791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf9d6abbf47f32cac71cefb6f7233e5f700d4f6f941ca631e29947c5f1df955`  
		Last Modified: Wed, 11 Oct 2023 18:21:57 GMT  
		Size: 24.9 MB (24887201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1693c4d42b110c48ad84138aa8c91e1aeffbed6ca630f12495f711b89609823`  
		Last Modified: Wed, 11 Oct 2023 18:22:27 GMT  
		Size: 66.0 MB (65984002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d61ba44e3cf60d5c6195ef4448de7160aff21051156b51d78755d19cb401055`  
		Last Modified: Wed, 11 Oct 2023 18:23:24 GMT  
		Size: 210.0 MB (209991000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b585c2f0cfabe530c3905bb95c637eb6339c7663273b893ede5b4d8cacd9233b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325624324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ae125d4ffa592dfd3716595bf2806c88e2b3b84e7cdc94482338771a440d1c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:48:50 GMT
ADD file:b081db8d48290ef5b5f477edb85d8f04d62a6995ec09bdb516d66dbe19b98137 in / 
# Wed, 11 Oct 2023 17:48:55 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 23:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 23:20:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 23:26:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:54dda4e4d31846b7324172a7fda3d0bdc7d8a2105ab27e9a92c2db43f35f9e5d`  
		Last Modified: Wed, 11 Oct 2023 17:59:53 GMT  
		Size: 49.6 MB (49569257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370a64ae3420fd85a23128ef46431df034f9038821764a14bb436272a1345505`  
		Last Modified: Wed, 11 Oct 2023 23:55:20 GMT  
		Size: 23.4 MB (23439567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19b06553268b2cbcf576e075fdb1ac8c430154167258bcd4f925d5938117659`  
		Last Modified: Wed, 11 Oct 2023 23:56:13 GMT  
		Size: 63.0 MB (62962779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe7e7187a4f54c6c9e49f439f18fe1ae7a7f06894b24eae29001a71e03340c5`  
		Last Modified: Wed, 11 Oct 2023 23:58:22 GMT  
		Size: 189.7 MB (189652721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:12b9dc56603f357d0e68e2cd0927be121561f588bc3f728ed3a1fb3dc0ec9ded
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.0 MB (362953503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7467ffe1bf70430528cbbee8f716bd707ff747ee7ff42c2f77578884a1c214d6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:44:01 GMT
ADD file:ed515e1aef8321271c6544e30cbeb31257e9640979e8f68a9e490cb25d3525fd in / 
# Wed, 11 Oct 2023 17:44:04 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:14:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:15:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:19:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f137383853e717724a59e86aa526d31eabb4a5d45a259cd1ade68d93b3f45ae9`  
		Last Modified: Wed, 11 Oct 2023 17:49:27 GMT  
		Size: 53.6 MB (53575984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da754908592cac64ca75d9cdc8c43a4a396901108de4adae61bd92937de4f65`  
		Last Modified: Wed, 11 Oct 2023 18:36:14 GMT  
		Size: 25.7 MB (25700026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524b67dc97fb52dd33f61fe12da424874443bb200789c7cfde14425f85938f54`  
		Last Modified: Wed, 11 Oct 2023 18:36:46 GMT  
		Size: 69.6 MB (69584544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7449a547606da3836fd2405c85ed15e48ed96b7936fe9dfcbb8c69e21475738e`  
		Last Modified: Wed, 11 Oct 2023 18:37:46 GMT  
		Size: 214.1 MB (214092949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:eb83643215e451aa8409fe1fec979764362831916fa9a2955baa57c263d6631f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.2 MB (318222519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42abbfd998057c2e0c5d1c31d39f5a383b5ce7201d011ae9066f0214cd94321c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:50:07 GMT
ADD file:2dc117136732884ad4b058065700dd66cc49d6ce56b0fdbb672915e3ad8adb84 in / 
# Wed, 11 Oct 2023 17:50:10 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 23:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 23:52:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 23:58:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ad5e374600bf40a929dfe51e52737e4ca04aba83f499656760ba938841fb6552`  
		Last Modified: Wed, 11 Oct 2023 17:55:18 GMT  
		Size: 47.9 MB (47942934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6344f505670ce139b1b3f472749240f33304ec7535daae4a72913a6da08f304f`  
		Last Modified: Thu, 12 Oct 2023 00:33:20 GMT  
		Size: 24.0 MB (24046768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf2b4ce0798e7985dd88d10311ea2a2730812d4e10c9a8f24f564875c6cb617`  
		Last Modified: Thu, 12 Oct 2023 00:33:56 GMT  
		Size: 63.1 MB (63132898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317490e394e1c9331e54c7c33215628d4d08a8cd9d2191cb3d294d0b021a18f9`  
		Last Modified: Thu, 12 Oct 2023 00:34:47 GMT  
		Size: 183.1 MB (183099919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
