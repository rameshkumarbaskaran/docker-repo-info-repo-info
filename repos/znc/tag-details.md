<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `znc`

-	[`znc:1.8`](#znc18)
-	[`znc:1.8-slim`](#znc18-slim)
-	[`znc:1.8.2`](#znc182)
-	[`znc:1.8.2-slim`](#znc182-slim)
-	[`znc:latest`](#znclatest)
-	[`znc:slim`](#zncslim)

## `znc:1.8`

```console
$ docker pull znc@sha256:2ec0eda5107d3399c3088673d1225da7fcc2f34a82421b32a63cd845d6bd4f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8` - linux; amd64

```console
$ docker pull znc@sha256:e33193008470acc438102ec956beb05233d317a51e8052b3c445bd3b6e4d6a84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164514394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c7638026d75882178dce1ed596b1ce1c589d894b6616e1881505e2cbf03ca7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:04:35 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 01 Dec 2023 06:04:35 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 01 Dec 2023 06:04:35 GMT
ARG MAKEFLAGS=
# Fri, 01 Dec 2023 06:04:35 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Dec 2023 06:08:17 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Dec 2023 06:08:18 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Dec 2023 06:08:18 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Dec 2023 06:08:18 GMT
VOLUME [/znc-data]
# Fri, 01 Dec 2023 06:08:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 06:08:35 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 01 Dec 2023 06:08:36 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fdd5a2f8948f451b8cf0195c6b0c8c11fac6cdb0628ea8e2d119c5dc9525b09`  
		Last Modified: Fri, 01 Dec 2023 06:08:52 GMT  
		Size: 46.6 MB (46591052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa334fed6c3c7ccb881fec4ffcb9fee0f6d3e063dcaeeaa1a7614623a64c6b6`  
		Last Modified: Fri, 01 Dec 2023 06:08:45 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede8f33c698c8e9831bdf20e0293486eaefe2896933968bc526a968d6d1c5f99`  
		Last Modified: Fri, 01 Dec 2023 06:08:45 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148d922a90ec0f4837d6abf0a61d81e7a5e16a1e2e0120637a8815a09a34b54`  
		Last Modified: Fri, 01 Dec 2023 06:09:18 GMT  
		Size: 114.5 MB (114542736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878762b26efde2025dbd27c198078c197b112f6d815fb3969cb20e6847782bb5`  
		Last Modified: Fri, 01 Dec 2023 06:09:03 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8` - linux; arm variant v6

```console
$ docker pull znc@sha256:fe5eb38d82c425c2020ee19b3480aa75a6b980017b37c18f044f5b6ffa5642d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145796167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5c14ba30773dd88bad088290630ab11c75d105f90678824766c4dba43be3ad`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 01:06:37 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 21 Oct 2023 01:06:37 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 21 Oct 2023 01:06:37 GMT
ARG MAKEFLAGS=
# Sat, 21 Oct 2023 01:06:37 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 21 Oct 2023 01:10:54 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 21 Oct 2023 01:10:54 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 21 Oct 2023 01:10:54 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 21 Oct 2023 01:10:55 GMT
VOLUME [/znc-data]
# Sat, 21 Oct 2023 01:10:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 01:11:10 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Sat, 21 Oct 2023 01:11:11 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002008a855ea7b373cae0abe4a007131720f5a0ea5b51c1b1f83e74fd3015426`  
		Last Modified: Sat, 21 Oct 2023 01:11:29 GMT  
		Size: 46.5 MB (46517304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24138600d1b287babb74486f5dca7fe0d5d5231a1eb66382237238e125f5509f`  
		Last Modified: Sat, 21 Oct 2023 01:11:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5933e40c262653efef9ec5ce36ba591b17ca9b83fc3370f11c0ba50b739616d`  
		Last Modified: Sat, 21 Oct 2023 01:11:21 GMT  
		Size: 779.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84329bfb09bca7341cdfa9b69c1660f332be6c7eb952b74871cba141477c38c`  
		Last Modified: Sat, 21 Oct 2023 01:11:56 GMT  
		Size: 96.2 MB (96165132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40875873a9609f0879330180aa0c1a53f4a5544705cc2dd2f2521afe296a4022`  
		Last Modified: Sat, 21 Oct 2023 01:11:39 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:9092ef4562b6adffc21590b809284e1c916c65745adcbb2fa805080363466ddb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153354436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865dd3205a6a81290cc843b22cd266ba2e4587ba90dae28397f2bb7cdb59f2f1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:07 GMT
ADD file:e5c66967d6570e36da50c9d42dd8f8f55e6c6a65b92c79601ea9e750c076fa2a in / 
# Thu, 30 Nov 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:38:17 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 01 Dec 2023 09:38:17 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 01 Dec 2023 09:38:17 GMT
ARG MAKEFLAGS=
# Fri, 01 Dec 2023 09:38:18 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Dec 2023 09:41:37 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Dec 2023 09:41:37 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Dec 2023 09:41:37 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Dec 2023 09:41:37 GMT
VOLUME [/znc-data]
# Fri, 01 Dec 2023 09:41:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 09:41:46 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 01 Dec 2023 09:41:48 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:b8180c93b172865af87a7c0e7e3c8bcb139e0d0c92e19c96467ff2cd4c8919ad`  
		Last Modified: Thu, 30 Nov 2023 23:11:45 GMT  
		Size: 3.3 MB (3258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213f7f5b0c180e2d58676c6b4cd4cfd63f6b688bc05b4ab4c4963d75d42f3223`  
		Last Modified: Fri, 01 Dec 2023 09:42:02 GMT  
		Size: 46.2 MB (46178748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9951779961cae64bd54274ec877697c8165153ff31bf352adb7f5cde0689d2e0`  
		Last Modified: Fri, 01 Dec 2023 09:41:56 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968ed58f7f69c0879be206f4043cacbd48705540750e3d093d0acac1cfb52d1f`  
		Last Modified: Fri, 01 Dec 2023 09:41:56 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9690c35e7ba277ffe6f578a6ee4983b644cbbe6609a55f16fb0508bf917fa4d9`  
		Last Modified: Fri, 01 Dec 2023 09:42:24 GMT  
		Size: 103.9 MB (103916054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb864d5d5e773f61b5168ad68d0226138c70854bc55d16969a88d8d64243b451`  
		Last Modified: Fri, 01 Dec 2023 09:42:12 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8-slim`

```console
$ docker pull znc@sha256:6f05006e27f762ef72c0142d4c20e3569b2caf26f44b3806074de3dd51a10137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8-slim` - linux; amd64

```console
$ docker pull znc@sha256:ec346f7322ce7a9a5ef1d9e9d486611452cb4bcc9e42857f4beabdce8c8b031b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49971327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01fb310ed190dae7579746e9d81457877b88a39ee433204ea090299bd92290a8`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:04:35 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 01 Dec 2023 06:04:35 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 01 Dec 2023 06:04:35 GMT
ARG MAKEFLAGS=
# Fri, 01 Dec 2023 06:04:35 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Dec 2023 06:08:17 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Dec 2023 06:08:18 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Dec 2023 06:08:18 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Dec 2023 06:08:18 GMT
VOLUME [/znc-data]
# Fri, 01 Dec 2023 06:08:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fdd5a2f8948f451b8cf0195c6b0c8c11fac6cdb0628ea8e2d119c5dc9525b09`  
		Last Modified: Fri, 01 Dec 2023 06:08:52 GMT  
		Size: 46.6 MB (46591052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa334fed6c3c7ccb881fec4ffcb9fee0f6d3e063dcaeeaa1a7614623a64c6b6`  
		Last Modified: Fri, 01 Dec 2023 06:08:45 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede8f33c698c8e9831bdf20e0293486eaefe2896933968bc526a968d6d1c5f99`  
		Last Modified: Fri, 01 Dec 2023 06:08:45 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:67e4bf0cbf0f131934764211260c79c23c075aa64a8711081c96d0d02c6fc785
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49630703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b142df1f977913b209e5f322704d91bb43d297eba01dd5519878d3bd4ebe227`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 01:06:37 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 21 Oct 2023 01:06:37 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 21 Oct 2023 01:06:37 GMT
ARG MAKEFLAGS=
# Sat, 21 Oct 2023 01:06:37 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 21 Oct 2023 01:10:54 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 21 Oct 2023 01:10:54 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 21 Oct 2023 01:10:54 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 21 Oct 2023 01:10:55 GMT
VOLUME [/znc-data]
# Sat, 21 Oct 2023 01:10:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002008a855ea7b373cae0abe4a007131720f5a0ea5b51c1b1f83e74fd3015426`  
		Last Modified: Sat, 21 Oct 2023 01:11:29 GMT  
		Size: 46.5 MB (46517304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24138600d1b287babb74486f5dca7fe0d5d5231a1eb66382237238e125f5509f`  
		Last Modified: Sat, 21 Oct 2023 01:11:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5933e40c262653efef9ec5ce36ba591b17ca9b83fc3370f11c0ba50b739616d`  
		Last Modified: Sat, 21 Oct 2023 01:11:21 GMT  
		Size: 779.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:6df1daa85f186a3e34632ce6f0d3c2eb803678c35c44fc31d82324c027ccfa39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49438050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed297fd8caae55b2d7f5df31429e2398fe11f9cca92c2d921f584d9dfa2552bf`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:07 GMT
ADD file:e5c66967d6570e36da50c9d42dd8f8f55e6c6a65b92c79601ea9e750c076fa2a in / 
# Thu, 30 Nov 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:38:17 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 01 Dec 2023 09:38:17 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 01 Dec 2023 09:38:17 GMT
ARG MAKEFLAGS=
# Fri, 01 Dec 2023 09:38:18 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Dec 2023 09:41:37 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Dec 2023 09:41:37 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Dec 2023 09:41:37 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Dec 2023 09:41:37 GMT
VOLUME [/znc-data]
# Fri, 01 Dec 2023 09:41:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b8180c93b172865af87a7c0e7e3c8bcb139e0d0c92e19c96467ff2cd4c8919ad`  
		Last Modified: Thu, 30 Nov 2023 23:11:45 GMT  
		Size: 3.3 MB (3258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213f7f5b0c180e2d58676c6b4cd4cfd63f6b688bc05b4ab4c4963d75d42f3223`  
		Last Modified: Fri, 01 Dec 2023 09:42:02 GMT  
		Size: 46.2 MB (46178748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9951779961cae64bd54274ec877697c8165153ff31bf352adb7f5cde0689d2e0`  
		Last Modified: Fri, 01 Dec 2023 09:41:56 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968ed58f7f69c0879be206f4043cacbd48705540750e3d093d0acac1cfb52d1f`  
		Last Modified: Fri, 01 Dec 2023 09:41:56 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8.2`

```console
$ docker pull znc@sha256:2ec0eda5107d3399c3088673d1225da7fcc2f34a82421b32a63cd845d6bd4f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8.2` - linux; amd64

```console
$ docker pull znc@sha256:e33193008470acc438102ec956beb05233d317a51e8052b3c445bd3b6e4d6a84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164514394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c7638026d75882178dce1ed596b1ce1c589d894b6616e1881505e2cbf03ca7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:04:35 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 01 Dec 2023 06:04:35 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 01 Dec 2023 06:04:35 GMT
ARG MAKEFLAGS=
# Fri, 01 Dec 2023 06:04:35 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Dec 2023 06:08:17 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Dec 2023 06:08:18 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Dec 2023 06:08:18 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Dec 2023 06:08:18 GMT
VOLUME [/znc-data]
# Fri, 01 Dec 2023 06:08:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 06:08:35 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 01 Dec 2023 06:08:36 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fdd5a2f8948f451b8cf0195c6b0c8c11fac6cdb0628ea8e2d119c5dc9525b09`  
		Last Modified: Fri, 01 Dec 2023 06:08:52 GMT  
		Size: 46.6 MB (46591052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa334fed6c3c7ccb881fec4ffcb9fee0f6d3e063dcaeeaa1a7614623a64c6b6`  
		Last Modified: Fri, 01 Dec 2023 06:08:45 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede8f33c698c8e9831bdf20e0293486eaefe2896933968bc526a968d6d1c5f99`  
		Last Modified: Fri, 01 Dec 2023 06:08:45 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148d922a90ec0f4837d6abf0a61d81e7a5e16a1e2e0120637a8815a09a34b54`  
		Last Modified: Fri, 01 Dec 2023 06:09:18 GMT  
		Size: 114.5 MB (114542736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878762b26efde2025dbd27c198078c197b112f6d815fb3969cb20e6847782bb5`  
		Last Modified: Fri, 01 Dec 2023 06:09:03 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2` - linux; arm variant v6

```console
$ docker pull znc@sha256:fe5eb38d82c425c2020ee19b3480aa75a6b980017b37c18f044f5b6ffa5642d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145796167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5c14ba30773dd88bad088290630ab11c75d105f90678824766c4dba43be3ad`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 01:06:37 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 21 Oct 2023 01:06:37 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 21 Oct 2023 01:06:37 GMT
ARG MAKEFLAGS=
# Sat, 21 Oct 2023 01:06:37 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 21 Oct 2023 01:10:54 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 21 Oct 2023 01:10:54 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 21 Oct 2023 01:10:54 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 21 Oct 2023 01:10:55 GMT
VOLUME [/znc-data]
# Sat, 21 Oct 2023 01:10:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 01:11:10 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Sat, 21 Oct 2023 01:11:11 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002008a855ea7b373cae0abe4a007131720f5a0ea5b51c1b1f83e74fd3015426`  
		Last Modified: Sat, 21 Oct 2023 01:11:29 GMT  
		Size: 46.5 MB (46517304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24138600d1b287babb74486f5dca7fe0d5d5231a1eb66382237238e125f5509f`  
		Last Modified: Sat, 21 Oct 2023 01:11:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5933e40c262653efef9ec5ce36ba591b17ca9b83fc3370f11c0ba50b739616d`  
		Last Modified: Sat, 21 Oct 2023 01:11:21 GMT  
		Size: 779.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84329bfb09bca7341cdfa9b69c1660f332be6c7eb952b74871cba141477c38c`  
		Last Modified: Sat, 21 Oct 2023 01:11:56 GMT  
		Size: 96.2 MB (96165132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40875873a9609f0879330180aa0c1a53f4a5544705cc2dd2f2521afe296a4022`  
		Last Modified: Sat, 21 Oct 2023 01:11:39 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:9092ef4562b6adffc21590b809284e1c916c65745adcbb2fa805080363466ddb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153354436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865dd3205a6a81290cc843b22cd266ba2e4587ba90dae28397f2bb7cdb59f2f1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:07 GMT
ADD file:e5c66967d6570e36da50c9d42dd8f8f55e6c6a65b92c79601ea9e750c076fa2a in / 
# Thu, 30 Nov 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:38:17 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 01 Dec 2023 09:38:17 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 01 Dec 2023 09:38:17 GMT
ARG MAKEFLAGS=
# Fri, 01 Dec 2023 09:38:18 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Dec 2023 09:41:37 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Dec 2023 09:41:37 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Dec 2023 09:41:37 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Dec 2023 09:41:37 GMT
VOLUME [/znc-data]
# Fri, 01 Dec 2023 09:41:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 09:41:46 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 01 Dec 2023 09:41:48 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:b8180c93b172865af87a7c0e7e3c8bcb139e0d0c92e19c96467ff2cd4c8919ad`  
		Last Modified: Thu, 30 Nov 2023 23:11:45 GMT  
		Size: 3.3 MB (3258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213f7f5b0c180e2d58676c6b4cd4cfd63f6b688bc05b4ab4c4963d75d42f3223`  
		Last Modified: Fri, 01 Dec 2023 09:42:02 GMT  
		Size: 46.2 MB (46178748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9951779961cae64bd54274ec877697c8165153ff31bf352adb7f5cde0689d2e0`  
		Last Modified: Fri, 01 Dec 2023 09:41:56 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968ed58f7f69c0879be206f4043cacbd48705540750e3d093d0acac1cfb52d1f`  
		Last Modified: Fri, 01 Dec 2023 09:41:56 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9690c35e7ba277ffe6f578a6ee4983b644cbbe6609a55f16fb0508bf917fa4d9`  
		Last Modified: Fri, 01 Dec 2023 09:42:24 GMT  
		Size: 103.9 MB (103916054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb864d5d5e773f61b5168ad68d0226138c70854bc55d16969a88d8d64243b451`  
		Last Modified: Fri, 01 Dec 2023 09:42:12 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8.2-slim`

```console
$ docker pull znc@sha256:6f05006e27f762ef72c0142d4c20e3569b2caf26f44b3806074de3dd51a10137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8.2-slim` - linux; amd64

```console
$ docker pull znc@sha256:ec346f7322ce7a9a5ef1d9e9d486611452cb4bcc9e42857f4beabdce8c8b031b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49971327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01fb310ed190dae7579746e9d81457877b88a39ee433204ea090299bd92290a8`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:04:35 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 01 Dec 2023 06:04:35 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 01 Dec 2023 06:04:35 GMT
ARG MAKEFLAGS=
# Fri, 01 Dec 2023 06:04:35 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Dec 2023 06:08:17 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Dec 2023 06:08:18 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Dec 2023 06:08:18 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Dec 2023 06:08:18 GMT
VOLUME [/znc-data]
# Fri, 01 Dec 2023 06:08:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fdd5a2f8948f451b8cf0195c6b0c8c11fac6cdb0628ea8e2d119c5dc9525b09`  
		Last Modified: Fri, 01 Dec 2023 06:08:52 GMT  
		Size: 46.6 MB (46591052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa334fed6c3c7ccb881fec4ffcb9fee0f6d3e063dcaeeaa1a7614623a64c6b6`  
		Last Modified: Fri, 01 Dec 2023 06:08:45 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede8f33c698c8e9831bdf20e0293486eaefe2896933968bc526a968d6d1c5f99`  
		Last Modified: Fri, 01 Dec 2023 06:08:45 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:67e4bf0cbf0f131934764211260c79c23c075aa64a8711081c96d0d02c6fc785
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49630703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b142df1f977913b209e5f322704d91bb43d297eba01dd5519878d3bd4ebe227`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 01:06:37 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 21 Oct 2023 01:06:37 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 21 Oct 2023 01:06:37 GMT
ARG MAKEFLAGS=
# Sat, 21 Oct 2023 01:06:37 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 21 Oct 2023 01:10:54 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 21 Oct 2023 01:10:54 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 21 Oct 2023 01:10:54 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 21 Oct 2023 01:10:55 GMT
VOLUME [/znc-data]
# Sat, 21 Oct 2023 01:10:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002008a855ea7b373cae0abe4a007131720f5a0ea5b51c1b1f83e74fd3015426`  
		Last Modified: Sat, 21 Oct 2023 01:11:29 GMT  
		Size: 46.5 MB (46517304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24138600d1b287babb74486f5dca7fe0d5d5231a1eb66382237238e125f5509f`  
		Last Modified: Sat, 21 Oct 2023 01:11:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5933e40c262653efef9ec5ce36ba591b17ca9b83fc3370f11c0ba50b739616d`  
		Last Modified: Sat, 21 Oct 2023 01:11:21 GMT  
		Size: 779.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:6df1daa85f186a3e34632ce6f0d3c2eb803678c35c44fc31d82324c027ccfa39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49438050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed297fd8caae55b2d7f5df31429e2398fe11f9cca92c2d921f584d9dfa2552bf`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:07 GMT
ADD file:e5c66967d6570e36da50c9d42dd8f8f55e6c6a65b92c79601ea9e750c076fa2a in / 
# Thu, 30 Nov 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:38:17 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 01 Dec 2023 09:38:17 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 01 Dec 2023 09:38:17 GMT
ARG MAKEFLAGS=
# Fri, 01 Dec 2023 09:38:18 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Dec 2023 09:41:37 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Dec 2023 09:41:37 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Dec 2023 09:41:37 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Dec 2023 09:41:37 GMT
VOLUME [/znc-data]
# Fri, 01 Dec 2023 09:41:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b8180c93b172865af87a7c0e7e3c8bcb139e0d0c92e19c96467ff2cd4c8919ad`  
		Last Modified: Thu, 30 Nov 2023 23:11:45 GMT  
		Size: 3.3 MB (3258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213f7f5b0c180e2d58676c6b4cd4cfd63f6b688bc05b4ab4c4963d75d42f3223`  
		Last Modified: Fri, 01 Dec 2023 09:42:02 GMT  
		Size: 46.2 MB (46178748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9951779961cae64bd54274ec877697c8165153ff31bf352adb7f5cde0689d2e0`  
		Last Modified: Fri, 01 Dec 2023 09:41:56 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968ed58f7f69c0879be206f4043cacbd48705540750e3d093d0acac1cfb52d1f`  
		Last Modified: Fri, 01 Dec 2023 09:41:56 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:latest`

```console
$ docker pull znc@sha256:2ec0eda5107d3399c3088673d1225da7fcc2f34a82421b32a63cd845d6bd4f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:latest` - linux; amd64

```console
$ docker pull znc@sha256:e33193008470acc438102ec956beb05233d317a51e8052b3c445bd3b6e4d6a84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164514394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c7638026d75882178dce1ed596b1ce1c589d894b6616e1881505e2cbf03ca7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:04:35 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 01 Dec 2023 06:04:35 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 01 Dec 2023 06:04:35 GMT
ARG MAKEFLAGS=
# Fri, 01 Dec 2023 06:04:35 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Dec 2023 06:08:17 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Dec 2023 06:08:18 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Dec 2023 06:08:18 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Dec 2023 06:08:18 GMT
VOLUME [/znc-data]
# Fri, 01 Dec 2023 06:08:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 06:08:35 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 01 Dec 2023 06:08:36 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fdd5a2f8948f451b8cf0195c6b0c8c11fac6cdb0628ea8e2d119c5dc9525b09`  
		Last Modified: Fri, 01 Dec 2023 06:08:52 GMT  
		Size: 46.6 MB (46591052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa334fed6c3c7ccb881fec4ffcb9fee0f6d3e063dcaeeaa1a7614623a64c6b6`  
		Last Modified: Fri, 01 Dec 2023 06:08:45 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede8f33c698c8e9831bdf20e0293486eaefe2896933968bc526a968d6d1c5f99`  
		Last Modified: Fri, 01 Dec 2023 06:08:45 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148d922a90ec0f4837d6abf0a61d81e7a5e16a1e2e0120637a8815a09a34b54`  
		Last Modified: Fri, 01 Dec 2023 06:09:18 GMT  
		Size: 114.5 MB (114542736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878762b26efde2025dbd27c198078c197b112f6d815fb3969cb20e6847782bb5`  
		Last Modified: Fri, 01 Dec 2023 06:09:03 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:fe5eb38d82c425c2020ee19b3480aa75a6b980017b37c18f044f5b6ffa5642d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145796167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5c14ba30773dd88bad088290630ab11c75d105f90678824766c4dba43be3ad`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 01:06:37 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 21 Oct 2023 01:06:37 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 21 Oct 2023 01:06:37 GMT
ARG MAKEFLAGS=
# Sat, 21 Oct 2023 01:06:37 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 21 Oct 2023 01:10:54 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 21 Oct 2023 01:10:54 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 21 Oct 2023 01:10:54 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 21 Oct 2023 01:10:55 GMT
VOLUME [/znc-data]
# Sat, 21 Oct 2023 01:10:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 01:11:10 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Sat, 21 Oct 2023 01:11:11 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002008a855ea7b373cae0abe4a007131720f5a0ea5b51c1b1f83e74fd3015426`  
		Last Modified: Sat, 21 Oct 2023 01:11:29 GMT  
		Size: 46.5 MB (46517304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24138600d1b287babb74486f5dca7fe0d5d5231a1eb66382237238e125f5509f`  
		Last Modified: Sat, 21 Oct 2023 01:11:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5933e40c262653efef9ec5ce36ba591b17ca9b83fc3370f11c0ba50b739616d`  
		Last Modified: Sat, 21 Oct 2023 01:11:21 GMT  
		Size: 779.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84329bfb09bca7341cdfa9b69c1660f332be6c7eb952b74871cba141477c38c`  
		Last Modified: Sat, 21 Oct 2023 01:11:56 GMT  
		Size: 96.2 MB (96165132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40875873a9609f0879330180aa0c1a53f4a5544705cc2dd2f2521afe296a4022`  
		Last Modified: Sat, 21 Oct 2023 01:11:39 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:9092ef4562b6adffc21590b809284e1c916c65745adcbb2fa805080363466ddb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153354436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865dd3205a6a81290cc843b22cd266ba2e4587ba90dae28397f2bb7cdb59f2f1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:07 GMT
ADD file:e5c66967d6570e36da50c9d42dd8f8f55e6c6a65b92c79601ea9e750c076fa2a in / 
# Thu, 30 Nov 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:38:17 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 01 Dec 2023 09:38:17 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 01 Dec 2023 09:38:17 GMT
ARG MAKEFLAGS=
# Fri, 01 Dec 2023 09:38:18 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Dec 2023 09:41:37 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Dec 2023 09:41:37 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Dec 2023 09:41:37 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Dec 2023 09:41:37 GMT
VOLUME [/znc-data]
# Fri, 01 Dec 2023 09:41:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 09:41:46 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 01 Dec 2023 09:41:48 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:b8180c93b172865af87a7c0e7e3c8bcb139e0d0c92e19c96467ff2cd4c8919ad`  
		Last Modified: Thu, 30 Nov 2023 23:11:45 GMT  
		Size: 3.3 MB (3258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213f7f5b0c180e2d58676c6b4cd4cfd63f6b688bc05b4ab4c4963d75d42f3223`  
		Last Modified: Fri, 01 Dec 2023 09:42:02 GMT  
		Size: 46.2 MB (46178748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9951779961cae64bd54274ec877697c8165153ff31bf352adb7f5cde0689d2e0`  
		Last Modified: Fri, 01 Dec 2023 09:41:56 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968ed58f7f69c0879be206f4043cacbd48705540750e3d093d0acac1cfb52d1f`  
		Last Modified: Fri, 01 Dec 2023 09:41:56 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9690c35e7ba277ffe6f578a6ee4983b644cbbe6609a55f16fb0508bf917fa4d9`  
		Last Modified: Fri, 01 Dec 2023 09:42:24 GMT  
		Size: 103.9 MB (103916054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb864d5d5e773f61b5168ad68d0226138c70854bc55d16969a88d8d64243b451`  
		Last Modified: Fri, 01 Dec 2023 09:42:12 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:slim`

```console
$ docker pull znc@sha256:6f05006e27f762ef72c0142d4c20e3569b2caf26f44b3806074de3dd51a10137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:slim` - linux; amd64

```console
$ docker pull znc@sha256:ec346f7322ce7a9a5ef1d9e9d486611452cb4bcc9e42857f4beabdce8c8b031b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49971327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01fb310ed190dae7579746e9d81457877b88a39ee433204ea090299bd92290a8`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:04:35 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 01 Dec 2023 06:04:35 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 01 Dec 2023 06:04:35 GMT
ARG MAKEFLAGS=
# Fri, 01 Dec 2023 06:04:35 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Dec 2023 06:08:17 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Dec 2023 06:08:18 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Dec 2023 06:08:18 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Dec 2023 06:08:18 GMT
VOLUME [/znc-data]
# Fri, 01 Dec 2023 06:08:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fdd5a2f8948f451b8cf0195c6b0c8c11fac6cdb0628ea8e2d119c5dc9525b09`  
		Last Modified: Fri, 01 Dec 2023 06:08:52 GMT  
		Size: 46.6 MB (46591052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa334fed6c3c7ccb881fec4ffcb9fee0f6d3e063dcaeeaa1a7614623a64c6b6`  
		Last Modified: Fri, 01 Dec 2023 06:08:45 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede8f33c698c8e9831bdf20e0293486eaefe2896933968bc526a968d6d1c5f99`  
		Last Modified: Fri, 01 Dec 2023 06:08:45 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:67e4bf0cbf0f131934764211260c79c23c075aa64a8711081c96d0d02c6fc785
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49630703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b142df1f977913b209e5f322704d91bb43d297eba01dd5519878d3bd4ebe227`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 01:06:37 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 21 Oct 2023 01:06:37 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 21 Oct 2023 01:06:37 GMT
ARG MAKEFLAGS=
# Sat, 21 Oct 2023 01:06:37 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 21 Oct 2023 01:10:54 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 21 Oct 2023 01:10:54 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 21 Oct 2023 01:10:54 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 21 Oct 2023 01:10:55 GMT
VOLUME [/znc-data]
# Sat, 21 Oct 2023 01:10:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002008a855ea7b373cae0abe4a007131720f5a0ea5b51c1b1f83e74fd3015426`  
		Last Modified: Sat, 21 Oct 2023 01:11:29 GMT  
		Size: 46.5 MB (46517304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24138600d1b287babb74486f5dca7fe0d5d5231a1eb66382237238e125f5509f`  
		Last Modified: Sat, 21 Oct 2023 01:11:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5933e40c262653efef9ec5ce36ba591b17ca9b83fc3370f11c0ba50b739616d`  
		Last Modified: Sat, 21 Oct 2023 01:11:21 GMT  
		Size: 779.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:6df1daa85f186a3e34632ce6f0d3c2eb803678c35c44fc31d82324c027ccfa39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49438050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed297fd8caae55b2d7f5df31429e2398fe11f9cca92c2d921f584d9dfa2552bf`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:07 GMT
ADD file:e5c66967d6570e36da50c9d42dd8f8f55e6c6a65b92c79601ea9e750c076fa2a in / 
# Thu, 30 Nov 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:38:17 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 01 Dec 2023 09:38:17 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 01 Dec 2023 09:38:17 GMT
ARG MAKEFLAGS=
# Fri, 01 Dec 2023 09:38:18 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Dec 2023 09:41:37 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Dec 2023 09:41:37 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Dec 2023 09:41:37 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Dec 2023 09:41:37 GMT
VOLUME [/znc-data]
# Fri, 01 Dec 2023 09:41:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b8180c93b172865af87a7c0e7e3c8bcb139e0d0c92e19c96467ff2cd4c8919ad`  
		Last Modified: Thu, 30 Nov 2023 23:11:45 GMT  
		Size: 3.3 MB (3258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213f7f5b0c180e2d58676c6b4cd4cfd63f6b688bc05b4ab4c4963d75d42f3223`  
		Last Modified: Fri, 01 Dec 2023 09:42:02 GMT  
		Size: 46.2 MB (46178748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9951779961cae64bd54274ec877697c8165153ff31bf352adb7f5cde0689d2e0`  
		Last Modified: Fri, 01 Dec 2023 09:41:56 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968ed58f7f69c0879be206f4043cacbd48705540750e3d093d0acac1cfb52d1f`  
		Last Modified: Fri, 01 Dec 2023 09:41:56 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
