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
$ docker pull znc@sha256:35a5cd90f00926e424261485f9a4293792b688b3c3cc7135b762828ec49fbc29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8` - linux; amd64

```console
$ docker pull znc@sha256:9666a4cc083c3a69ba589d9d3d281ff1e289029f5f78cf0cb8226fa98a4ddc4e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138547570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82de5c6341c02822af90820d98d694244ef1beb5d8ef9c6cf270a5d6cf003bd0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 06:18:17 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 01 Sep 2021 06:18:17 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 01 Sep 2021 06:18:17 GMT
ARG MAKEFLAGS=
# Wed, 01 Sep 2021 06:18:17 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Oct 2021 23:08:55 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Oct 2021 23:08:56 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Oct 2021 23:08:56 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Oct 2021 23:08:56 GMT
VOLUME [/znc-data]
# Fri, 01 Oct 2021 23:08:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 23:09:17 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 01 Oct 2021 23:09:18 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a73afbe56e6d9a30ec82d815877acf0aed072948e9bc3a36b0ad9c094ddb53`  
		Last Modified: Fri, 01 Oct 2021 23:09:41 GMT  
		Size: 43.4 MB (43381636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63a2c0b7d6f98c822c562fff7958533862ac4067eb74b73631483e0dd56f233`  
		Last Modified: Fri, 01 Oct 2021 23:09:32 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95be7798fda8e3c01dc73ad2cb976f3ed92a657c8628e45388365f95d49269e`  
		Last Modified: Fri, 01 Oct 2021 23:09:32 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e8fb0fdd0ded9e7c89855fecdc8f411eabf480cbc4a437f64e1a94cbc176bb`  
		Last Modified: Fri, 01 Oct 2021 23:10:07 GMT  
		Size: 92.4 MB (92350573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d9ab4cb345e80038df0ecb07e296c8452b70ce1e6d4bab4deb06b7f0ee6bbe`  
		Last Modified: Fri, 01 Oct 2021 23:09:53 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8` - linux; arm variant v6

```console
$ docker pull znc@sha256:26f8843b164895a859ea39130cbdb5f74395745e7b4fb9c712e0b19976b604fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122189311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254c9d8d7309227f5ae2a80fcbb2b4912cb86d424932380be6c8fa93f5f306b8`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:31:42 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 12 Nov 2021 17:31:42 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 12 Nov 2021 17:31:43 GMT
ARG MAKEFLAGS=
# Fri, 12 Nov 2021 17:31:43 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 12 Nov 2021 17:43:48 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 12 Nov 2021 17:43:49 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 12 Nov 2021 17:43:49 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 12 Nov 2021 17:43:50 GMT
VOLUME [/znc-data]
# Fri, 12 Nov 2021 17:43:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 17:44:33 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 12 Nov 2021 17:44:34 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bce9787b2291d0748e856d82bcdc801c8d620fd853c9fea6f82c35635cfca0b`  
		Last Modified: Fri, 12 Nov 2021 17:45:51 GMT  
		Size: 41.7 MB (41652596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ec6a9aea035f3998644c219b10f4f43da8002e52a526673274617185ab870f`  
		Last Modified: Fri, 12 Nov 2021 17:45:22 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1d06f09b7c54f8ec35ed87b144db269c1d97ae31dc4144777a4ee0206b446`  
		Last Modified: Fri, 12 Nov 2021 17:45:22 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5485254bd3be6cee3450da77bc70775858229108f438df3cc13be47ee396134`  
		Last Modified: Fri, 12 Nov 2021 17:47:01 GMT  
		Size: 77.9 MB (77902086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d1d92e84261b512e195c458ce10a8bb396b65d86025d6a72eeb3c4602f00c5`  
		Last Modified: Fri, 12 Nov 2021 17:46:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:b322a403e9ac017c9cc7d6014132a2721ebf8e67638ff35041d243c2cd047dbd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129831813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01cb753070d0ef97b8a7d96a93b53aa832ecd804b3fa37a527abfec8f2cd87ea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 11:30:01 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 01 Sep 2021 11:30:01 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 01 Sep 2021 11:30:01 GMT
ARG MAKEFLAGS=
# Wed, 01 Sep 2021 11:30:02 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Oct 2021 21:47:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Oct 2021 21:47:44 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Oct 2021 21:47:44 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Oct 2021 21:47:44 GMT
VOLUME [/znc-data]
# Fri, 01 Oct 2021 21:47:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 21:48:03 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 01 Oct 2021 21:48:03 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7483ab13bd967aa38dd59edd4d43509af1ee92998db0f60fe00acaa7bca7cab`  
		Last Modified: Fri, 01 Oct 2021 21:48:33 GMT  
		Size: 43.2 MB (43227495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846a634441e53d991dcfeb3e2e0040b60271e306e2e21c2f5a90b9950b91e9a5`  
		Last Modified: Fri, 01 Oct 2021 21:48:25 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97ce6959ea02c7cf78772bc2a7f9f451701a02fc59df2e2a4b900654b48bc1e`  
		Last Modified: Fri, 01 Oct 2021 21:48:25 GMT  
		Size: 777.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06929df4d3659431dda0ce829b55d578aa3a756e2b9cfb8ea4b5b154cd9f7ceb`  
		Last Modified: Fri, 01 Oct 2021 21:49:02 GMT  
		Size: 83.9 MB (83890032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020eddac6c8ca78e6f77c3311501d51a83db997bd31e0ffe8bf744187f1f7cc3`  
		Last Modified: Fri, 01 Oct 2021 21:48:47 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8-slim`

```console
$ docker pull znc@sha256:96aad272912cf191d3a7a23b0974c46db472dd8c0dbea38e955b76d48ba0ecf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8-slim` - linux; amd64

```console
$ docker pull znc@sha256:ba8fb0b48d1738dbfc366e70a2f20587e2b70f1f9fecea1b53f7b156a0a0fc0b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46196666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b40d52e48014894c304f1b6add593df7fecdae270697fb87898b5e8c522bf0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 06:18:17 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 01 Sep 2021 06:18:17 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 01 Sep 2021 06:18:17 GMT
ARG MAKEFLAGS=
# Wed, 01 Sep 2021 06:18:17 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Oct 2021 23:08:55 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Oct 2021 23:08:56 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Oct 2021 23:08:56 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Oct 2021 23:08:56 GMT
VOLUME [/znc-data]
# Fri, 01 Oct 2021 23:08:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a73afbe56e6d9a30ec82d815877acf0aed072948e9bc3a36b0ad9c094ddb53`  
		Last Modified: Fri, 01 Oct 2021 23:09:41 GMT  
		Size: 43.4 MB (43381636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63a2c0b7d6f98c822c562fff7958533862ac4067eb74b73631483e0dd56f233`  
		Last Modified: Fri, 01 Oct 2021 23:09:32 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95be7798fda8e3c01dc73ad2cb976f3ed92a657c8628e45388365f95d49269e`  
		Last Modified: Fri, 01 Oct 2021 23:09:32 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:368ce5d9175f8d71dc16dc4804766e6e6c6bbe2f833e91d25b392fe665f3b56e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44286892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67570c1f1f3bc95dcd53221836cb0b8a0179ece8fb06d9e7f534def1a6e3890`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:31:42 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 12 Nov 2021 17:31:42 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 12 Nov 2021 17:31:43 GMT
ARG MAKEFLAGS=
# Fri, 12 Nov 2021 17:31:43 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 12 Nov 2021 17:43:48 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 12 Nov 2021 17:43:49 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 12 Nov 2021 17:43:49 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 12 Nov 2021 17:43:50 GMT
VOLUME [/znc-data]
# Fri, 12 Nov 2021 17:43:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bce9787b2291d0748e856d82bcdc801c8d620fd853c9fea6f82c35635cfca0b`  
		Last Modified: Fri, 12 Nov 2021 17:45:51 GMT  
		Size: 41.7 MB (41652596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ec6a9aea035f3998644c219b10f4f43da8002e52a526673274617185ab870f`  
		Last Modified: Fri, 12 Nov 2021 17:45:22 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1d06f09b7c54f8ec35ed87b144db269c1d97ae31dc4144777a4ee0206b446`  
		Last Modified: Fri, 12 Nov 2021 17:45:22 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:56cf76aa7bc8e26cbab88d54f78b3cc2d03f7cf6ccbdd475b6d4aac93af73d72
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45941450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75911e04d496f2d31c2d93053d71b0db2e27a95af61c1a4b9ee04e94fe3463db`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 11:30:01 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 01 Sep 2021 11:30:01 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 01 Sep 2021 11:30:01 GMT
ARG MAKEFLAGS=
# Wed, 01 Sep 2021 11:30:02 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Oct 2021 21:47:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Oct 2021 21:47:44 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Oct 2021 21:47:44 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Oct 2021 21:47:44 GMT
VOLUME [/znc-data]
# Fri, 01 Oct 2021 21:47:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7483ab13bd967aa38dd59edd4d43509af1ee92998db0f60fe00acaa7bca7cab`  
		Last Modified: Fri, 01 Oct 2021 21:48:33 GMT  
		Size: 43.2 MB (43227495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846a634441e53d991dcfeb3e2e0040b60271e306e2e21c2f5a90b9950b91e9a5`  
		Last Modified: Fri, 01 Oct 2021 21:48:25 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97ce6959ea02c7cf78772bc2a7f9f451701a02fc59df2e2a4b900654b48bc1e`  
		Last Modified: Fri, 01 Oct 2021 21:48:25 GMT  
		Size: 777.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8.2`

```console
$ docker pull znc@sha256:35a5cd90f00926e424261485f9a4293792b688b3c3cc7135b762828ec49fbc29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8.2` - linux; amd64

```console
$ docker pull znc@sha256:9666a4cc083c3a69ba589d9d3d281ff1e289029f5f78cf0cb8226fa98a4ddc4e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138547570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82de5c6341c02822af90820d98d694244ef1beb5d8ef9c6cf270a5d6cf003bd0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 06:18:17 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 01 Sep 2021 06:18:17 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 01 Sep 2021 06:18:17 GMT
ARG MAKEFLAGS=
# Wed, 01 Sep 2021 06:18:17 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Oct 2021 23:08:55 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Oct 2021 23:08:56 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Oct 2021 23:08:56 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Oct 2021 23:08:56 GMT
VOLUME [/znc-data]
# Fri, 01 Oct 2021 23:08:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 23:09:17 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 01 Oct 2021 23:09:18 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a73afbe56e6d9a30ec82d815877acf0aed072948e9bc3a36b0ad9c094ddb53`  
		Last Modified: Fri, 01 Oct 2021 23:09:41 GMT  
		Size: 43.4 MB (43381636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63a2c0b7d6f98c822c562fff7958533862ac4067eb74b73631483e0dd56f233`  
		Last Modified: Fri, 01 Oct 2021 23:09:32 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95be7798fda8e3c01dc73ad2cb976f3ed92a657c8628e45388365f95d49269e`  
		Last Modified: Fri, 01 Oct 2021 23:09:32 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e8fb0fdd0ded9e7c89855fecdc8f411eabf480cbc4a437f64e1a94cbc176bb`  
		Last Modified: Fri, 01 Oct 2021 23:10:07 GMT  
		Size: 92.4 MB (92350573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d9ab4cb345e80038df0ecb07e296c8452b70ce1e6d4bab4deb06b7f0ee6bbe`  
		Last Modified: Fri, 01 Oct 2021 23:09:53 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2` - linux; arm variant v6

```console
$ docker pull znc@sha256:26f8843b164895a859ea39130cbdb5f74395745e7b4fb9c712e0b19976b604fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122189311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254c9d8d7309227f5ae2a80fcbb2b4912cb86d424932380be6c8fa93f5f306b8`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:31:42 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 12 Nov 2021 17:31:42 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 12 Nov 2021 17:31:43 GMT
ARG MAKEFLAGS=
# Fri, 12 Nov 2021 17:31:43 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 12 Nov 2021 17:43:48 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 12 Nov 2021 17:43:49 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 12 Nov 2021 17:43:49 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 12 Nov 2021 17:43:50 GMT
VOLUME [/znc-data]
# Fri, 12 Nov 2021 17:43:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 17:44:33 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 12 Nov 2021 17:44:34 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bce9787b2291d0748e856d82bcdc801c8d620fd853c9fea6f82c35635cfca0b`  
		Last Modified: Fri, 12 Nov 2021 17:45:51 GMT  
		Size: 41.7 MB (41652596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ec6a9aea035f3998644c219b10f4f43da8002e52a526673274617185ab870f`  
		Last Modified: Fri, 12 Nov 2021 17:45:22 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1d06f09b7c54f8ec35ed87b144db269c1d97ae31dc4144777a4ee0206b446`  
		Last Modified: Fri, 12 Nov 2021 17:45:22 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5485254bd3be6cee3450da77bc70775858229108f438df3cc13be47ee396134`  
		Last Modified: Fri, 12 Nov 2021 17:47:01 GMT  
		Size: 77.9 MB (77902086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d1d92e84261b512e195c458ce10a8bb396b65d86025d6a72eeb3c4602f00c5`  
		Last Modified: Fri, 12 Nov 2021 17:46:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:b322a403e9ac017c9cc7d6014132a2721ebf8e67638ff35041d243c2cd047dbd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129831813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01cb753070d0ef97b8a7d96a93b53aa832ecd804b3fa37a527abfec8f2cd87ea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 11:30:01 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 01 Sep 2021 11:30:01 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 01 Sep 2021 11:30:01 GMT
ARG MAKEFLAGS=
# Wed, 01 Sep 2021 11:30:02 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Oct 2021 21:47:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Oct 2021 21:47:44 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Oct 2021 21:47:44 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Oct 2021 21:47:44 GMT
VOLUME [/znc-data]
# Fri, 01 Oct 2021 21:47:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 21:48:03 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 01 Oct 2021 21:48:03 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7483ab13bd967aa38dd59edd4d43509af1ee92998db0f60fe00acaa7bca7cab`  
		Last Modified: Fri, 01 Oct 2021 21:48:33 GMT  
		Size: 43.2 MB (43227495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846a634441e53d991dcfeb3e2e0040b60271e306e2e21c2f5a90b9950b91e9a5`  
		Last Modified: Fri, 01 Oct 2021 21:48:25 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97ce6959ea02c7cf78772bc2a7f9f451701a02fc59df2e2a4b900654b48bc1e`  
		Last Modified: Fri, 01 Oct 2021 21:48:25 GMT  
		Size: 777.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06929df4d3659431dda0ce829b55d578aa3a756e2b9cfb8ea4b5b154cd9f7ceb`  
		Last Modified: Fri, 01 Oct 2021 21:49:02 GMT  
		Size: 83.9 MB (83890032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020eddac6c8ca78e6f77c3311501d51a83db997bd31e0ffe8bf744187f1f7cc3`  
		Last Modified: Fri, 01 Oct 2021 21:48:47 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8.2-slim`

```console
$ docker pull znc@sha256:96aad272912cf191d3a7a23b0974c46db472dd8c0dbea38e955b76d48ba0ecf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8.2-slim` - linux; amd64

```console
$ docker pull znc@sha256:ba8fb0b48d1738dbfc366e70a2f20587e2b70f1f9fecea1b53f7b156a0a0fc0b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46196666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b40d52e48014894c304f1b6add593df7fecdae270697fb87898b5e8c522bf0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 06:18:17 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 01 Sep 2021 06:18:17 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 01 Sep 2021 06:18:17 GMT
ARG MAKEFLAGS=
# Wed, 01 Sep 2021 06:18:17 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Oct 2021 23:08:55 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Oct 2021 23:08:56 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Oct 2021 23:08:56 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Oct 2021 23:08:56 GMT
VOLUME [/znc-data]
# Fri, 01 Oct 2021 23:08:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a73afbe56e6d9a30ec82d815877acf0aed072948e9bc3a36b0ad9c094ddb53`  
		Last Modified: Fri, 01 Oct 2021 23:09:41 GMT  
		Size: 43.4 MB (43381636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63a2c0b7d6f98c822c562fff7958533862ac4067eb74b73631483e0dd56f233`  
		Last Modified: Fri, 01 Oct 2021 23:09:32 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95be7798fda8e3c01dc73ad2cb976f3ed92a657c8628e45388365f95d49269e`  
		Last Modified: Fri, 01 Oct 2021 23:09:32 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:368ce5d9175f8d71dc16dc4804766e6e6c6bbe2f833e91d25b392fe665f3b56e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44286892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67570c1f1f3bc95dcd53221836cb0b8a0179ece8fb06d9e7f534def1a6e3890`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:31:42 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 12 Nov 2021 17:31:42 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 12 Nov 2021 17:31:43 GMT
ARG MAKEFLAGS=
# Fri, 12 Nov 2021 17:31:43 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 12 Nov 2021 17:43:48 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 12 Nov 2021 17:43:49 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 12 Nov 2021 17:43:49 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 12 Nov 2021 17:43:50 GMT
VOLUME [/znc-data]
# Fri, 12 Nov 2021 17:43:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bce9787b2291d0748e856d82bcdc801c8d620fd853c9fea6f82c35635cfca0b`  
		Last Modified: Fri, 12 Nov 2021 17:45:51 GMT  
		Size: 41.7 MB (41652596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ec6a9aea035f3998644c219b10f4f43da8002e52a526673274617185ab870f`  
		Last Modified: Fri, 12 Nov 2021 17:45:22 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1d06f09b7c54f8ec35ed87b144db269c1d97ae31dc4144777a4ee0206b446`  
		Last Modified: Fri, 12 Nov 2021 17:45:22 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:56cf76aa7bc8e26cbab88d54f78b3cc2d03f7cf6ccbdd475b6d4aac93af73d72
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45941450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75911e04d496f2d31c2d93053d71b0db2e27a95af61c1a4b9ee04e94fe3463db`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 11:30:01 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 01 Sep 2021 11:30:01 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 01 Sep 2021 11:30:01 GMT
ARG MAKEFLAGS=
# Wed, 01 Sep 2021 11:30:02 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Oct 2021 21:47:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Oct 2021 21:47:44 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Oct 2021 21:47:44 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Oct 2021 21:47:44 GMT
VOLUME [/znc-data]
# Fri, 01 Oct 2021 21:47:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7483ab13bd967aa38dd59edd4d43509af1ee92998db0f60fe00acaa7bca7cab`  
		Last Modified: Fri, 01 Oct 2021 21:48:33 GMT  
		Size: 43.2 MB (43227495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846a634441e53d991dcfeb3e2e0040b60271e306e2e21c2f5a90b9950b91e9a5`  
		Last Modified: Fri, 01 Oct 2021 21:48:25 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97ce6959ea02c7cf78772bc2a7f9f451701a02fc59df2e2a4b900654b48bc1e`  
		Last Modified: Fri, 01 Oct 2021 21:48:25 GMT  
		Size: 777.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:latest`

```console
$ docker pull znc@sha256:35a5cd90f00926e424261485f9a4293792b688b3c3cc7135b762828ec49fbc29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:latest` - linux; amd64

```console
$ docker pull znc@sha256:9666a4cc083c3a69ba589d9d3d281ff1e289029f5f78cf0cb8226fa98a4ddc4e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138547570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82de5c6341c02822af90820d98d694244ef1beb5d8ef9c6cf270a5d6cf003bd0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 06:18:17 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 01 Sep 2021 06:18:17 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 01 Sep 2021 06:18:17 GMT
ARG MAKEFLAGS=
# Wed, 01 Sep 2021 06:18:17 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Oct 2021 23:08:55 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Oct 2021 23:08:56 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Oct 2021 23:08:56 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Oct 2021 23:08:56 GMT
VOLUME [/znc-data]
# Fri, 01 Oct 2021 23:08:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 23:09:17 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 01 Oct 2021 23:09:18 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a73afbe56e6d9a30ec82d815877acf0aed072948e9bc3a36b0ad9c094ddb53`  
		Last Modified: Fri, 01 Oct 2021 23:09:41 GMT  
		Size: 43.4 MB (43381636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63a2c0b7d6f98c822c562fff7958533862ac4067eb74b73631483e0dd56f233`  
		Last Modified: Fri, 01 Oct 2021 23:09:32 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95be7798fda8e3c01dc73ad2cb976f3ed92a657c8628e45388365f95d49269e`  
		Last Modified: Fri, 01 Oct 2021 23:09:32 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e8fb0fdd0ded9e7c89855fecdc8f411eabf480cbc4a437f64e1a94cbc176bb`  
		Last Modified: Fri, 01 Oct 2021 23:10:07 GMT  
		Size: 92.4 MB (92350573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d9ab4cb345e80038df0ecb07e296c8452b70ce1e6d4bab4deb06b7f0ee6bbe`  
		Last Modified: Fri, 01 Oct 2021 23:09:53 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:26f8843b164895a859ea39130cbdb5f74395745e7b4fb9c712e0b19976b604fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122189311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254c9d8d7309227f5ae2a80fcbb2b4912cb86d424932380be6c8fa93f5f306b8`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:31:42 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 12 Nov 2021 17:31:42 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 12 Nov 2021 17:31:43 GMT
ARG MAKEFLAGS=
# Fri, 12 Nov 2021 17:31:43 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 12 Nov 2021 17:43:48 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 12 Nov 2021 17:43:49 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 12 Nov 2021 17:43:49 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 12 Nov 2021 17:43:50 GMT
VOLUME [/znc-data]
# Fri, 12 Nov 2021 17:43:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 17:44:33 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 12 Nov 2021 17:44:34 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bce9787b2291d0748e856d82bcdc801c8d620fd853c9fea6f82c35635cfca0b`  
		Last Modified: Fri, 12 Nov 2021 17:45:51 GMT  
		Size: 41.7 MB (41652596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ec6a9aea035f3998644c219b10f4f43da8002e52a526673274617185ab870f`  
		Last Modified: Fri, 12 Nov 2021 17:45:22 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1d06f09b7c54f8ec35ed87b144db269c1d97ae31dc4144777a4ee0206b446`  
		Last Modified: Fri, 12 Nov 2021 17:45:22 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5485254bd3be6cee3450da77bc70775858229108f438df3cc13be47ee396134`  
		Last Modified: Fri, 12 Nov 2021 17:47:01 GMT  
		Size: 77.9 MB (77902086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d1d92e84261b512e195c458ce10a8bb396b65d86025d6a72eeb3c4602f00c5`  
		Last Modified: Fri, 12 Nov 2021 17:46:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:b322a403e9ac017c9cc7d6014132a2721ebf8e67638ff35041d243c2cd047dbd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129831813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01cb753070d0ef97b8a7d96a93b53aa832ecd804b3fa37a527abfec8f2cd87ea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 11:30:01 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 01 Sep 2021 11:30:01 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 01 Sep 2021 11:30:01 GMT
ARG MAKEFLAGS=
# Wed, 01 Sep 2021 11:30:02 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Oct 2021 21:47:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Oct 2021 21:47:44 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Oct 2021 21:47:44 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Oct 2021 21:47:44 GMT
VOLUME [/znc-data]
# Fri, 01 Oct 2021 21:47:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 21:48:03 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 01 Oct 2021 21:48:03 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7483ab13bd967aa38dd59edd4d43509af1ee92998db0f60fe00acaa7bca7cab`  
		Last Modified: Fri, 01 Oct 2021 21:48:33 GMT  
		Size: 43.2 MB (43227495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846a634441e53d991dcfeb3e2e0040b60271e306e2e21c2f5a90b9950b91e9a5`  
		Last Modified: Fri, 01 Oct 2021 21:48:25 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97ce6959ea02c7cf78772bc2a7f9f451701a02fc59df2e2a4b900654b48bc1e`  
		Last Modified: Fri, 01 Oct 2021 21:48:25 GMT  
		Size: 777.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06929df4d3659431dda0ce829b55d578aa3a756e2b9cfb8ea4b5b154cd9f7ceb`  
		Last Modified: Fri, 01 Oct 2021 21:49:02 GMT  
		Size: 83.9 MB (83890032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020eddac6c8ca78e6f77c3311501d51a83db997bd31e0ffe8bf744187f1f7cc3`  
		Last Modified: Fri, 01 Oct 2021 21:48:47 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:slim`

```console
$ docker pull znc@sha256:96aad272912cf191d3a7a23b0974c46db472dd8c0dbea38e955b76d48ba0ecf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:slim` - linux; amd64

```console
$ docker pull znc@sha256:ba8fb0b48d1738dbfc366e70a2f20587e2b70f1f9fecea1b53f7b156a0a0fc0b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46196666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b40d52e48014894c304f1b6add593df7fecdae270697fb87898b5e8c522bf0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 06:18:17 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 01 Sep 2021 06:18:17 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 01 Sep 2021 06:18:17 GMT
ARG MAKEFLAGS=
# Wed, 01 Sep 2021 06:18:17 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Oct 2021 23:08:55 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Oct 2021 23:08:56 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Oct 2021 23:08:56 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Oct 2021 23:08:56 GMT
VOLUME [/znc-data]
# Fri, 01 Oct 2021 23:08:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a73afbe56e6d9a30ec82d815877acf0aed072948e9bc3a36b0ad9c094ddb53`  
		Last Modified: Fri, 01 Oct 2021 23:09:41 GMT  
		Size: 43.4 MB (43381636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63a2c0b7d6f98c822c562fff7958533862ac4067eb74b73631483e0dd56f233`  
		Last Modified: Fri, 01 Oct 2021 23:09:32 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95be7798fda8e3c01dc73ad2cb976f3ed92a657c8628e45388365f95d49269e`  
		Last Modified: Fri, 01 Oct 2021 23:09:32 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:368ce5d9175f8d71dc16dc4804766e6e6c6bbe2f833e91d25b392fe665f3b56e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44286892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67570c1f1f3bc95dcd53221836cb0b8a0179ece8fb06d9e7f534def1a6e3890`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:31:42 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 12 Nov 2021 17:31:42 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 12 Nov 2021 17:31:43 GMT
ARG MAKEFLAGS=
# Fri, 12 Nov 2021 17:31:43 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 12 Nov 2021 17:43:48 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 12 Nov 2021 17:43:49 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 12 Nov 2021 17:43:49 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 12 Nov 2021 17:43:50 GMT
VOLUME [/znc-data]
# Fri, 12 Nov 2021 17:43:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bce9787b2291d0748e856d82bcdc801c8d620fd853c9fea6f82c35635cfca0b`  
		Last Modified: Fri, 12 Nov 2021 17:45:51 GMT  
		Size: 41.7 MB (41652596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ec6a9aea035f3998644c219b10f4f43da8002e52a526673274617185ab870f`  
		Last Modified: Fri, 12 Nov 2021 17:45:22 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1d06f09b7c54f8ec35ed87b144db269c1d97ae31dc4144777a4ee0206b446`  
		Last Modified: Fri, 12 Nov 2021 17:45:22 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:56cf76aa7bc8e26cbab88d54f78b3cc2d03f7cf6ccbdd475b6d4aac93af73d72
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45941450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75911e04d496f2d31c2d93053d71b0db2e27a95af61c1a4b9ee04e94fe3463db`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 11:30:01 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 01 Sep 2021 11:30:01 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 01 Sep 2021 11:30:01 GMT
ARG MAKEFLAGS=
# Wed, 01 Sep 2021 11:30:02 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 01 Oct 2021 21:47:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 01 Oct 2021 21:47:44 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 01 Oct 2021 21:47:44 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 01 Oct 2021 21:47:44 GMT
VOLUME [/znc-data]
# Fri, 01 Oct 2021 21:47:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7483ab13bd967aa38dd59edd4d43509af1ee92998db0f60fe00acaa7bca7cab`  
		Last Modified: Fri, 01 Oct 2021 21:48:33 GMT  
		Size: 43.2 MB (43227495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846a634441e53d991dcfeb3e2e0040b60271e306e2e21c2f5a90b9950b91e9a5`  
		Last Modified: Fri, 01 Oct 2021 21:48:25 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97ce6959ea02c7cf78772bc2a7f9f451701a02fc59df2e2a4b900654b48bc1e`  
		Last Modified: Fri, 01 Oct 2021 21:48:25 GMT  
		Size: 777.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
