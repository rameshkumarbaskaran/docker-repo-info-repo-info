## `znc:slim`

```console
$ docker pull znc@sha256:6bab4aa32f37fd9d5ef810d9d3b547d6a64b17bb2a450b04d0d0bc2a2e107b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:slim` - linux; amd64

```console
$ docker pull znc@sha256:0bf60c073b319d5cc592bf59b77650f51b8dd8c0eb72a2e76b75ee80b5a06fca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49942612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d140c5a315f3aa2af96be5d7bf2ef780da53a55518f5759bb83c04d88f42e3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 21:22:10 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Mon, 09 Jan 2023 21:22:10 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Mon, 09 Jan 2023 21:22:10 GMT
ARG MAKEFLAGS=
# Mon, 09 Jan 2023 21:22:10 GMT
ENV ZNC_VERSION=1.8.2
# Mon, 09 Jan 2023 21:26:08 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Mon, 09 Jan 2023 21:26:09 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Mon, 09 Jan 2023 21:26:09 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Mon, 09 Jan 2023 21:26:09 GMT
VOLUME [/znc-data]
# Mon, 09 Jan 2023 21:26:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5d8b6b37f44d57259bb006f9b65889c6ea03ea64b4b515a3118d3a41bc8aa5`  
		Last Modified: Mon, 09 Jan 2023 21:26:46 GMT  
		Size: 46.6 MB (46571031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db57db500d6df1351587e84950e21dc0dc36ebf2be1bcfaa4704180210b8b068`  
		Last Modified: Mon, 09 Jan 2023 21:26:38 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291cbdb197592e1d29922f57158268e6c93a82af8f492030b50259afbec70fa3`  
		Last Modified: Mon, 09 Jan 2023 21:26:38 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:6af40c9e744dc2cdd371b2058409d618844e8fea832ed62502ab476a24163568
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47903598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16c272fad6f85350300c57df766f0637565d94f07fef111882b8b715365e5ed`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 03:38:07 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 11 Feb 2023 03:38:07 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 11 Feb 2023 03:38:07 GMT
ARG MAKEFLAGS=
# Sat, 11 Feb 2023 03:38:08 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 11 Feb 2023 03:42:39 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 11 Feb 2023 03:42:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 11 Feb 2023 03:42:40 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 11 Feb 2023 03:42:40 GMT
VOLUME [/znc-data]
# Sat, 11 Feb 2023 03:42:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0d99e5fbf0d5bbc554790b9b6f8139ad8a5c2d439cf8ada388c4dc07f3ef49`  
		Last Modified: Sat, 11 Feb 2023 03:43:35 GMT  
		Size: 44.8 MB (44791788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be077d44b9b301689f79ab3664eb481753d39da8082dfdf8c543c566a80c8fa9`  
		Last Modified: Sat, 11 Feb 2023 03:43:26 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6b389aac55b7e2893117b933180c7e49e5e8b6350871f05c581583d2266a57`  
		Last Modified: Sat, 11 Feb 2023 03:43:26 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:415a89b0777d8316ca723de45208f48bf3317ad2c1d466b90d18c8eeda2becd7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49412848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d43ae36d65c17bd479af78052f10e80faf1e6a8f920d4031d549d03dcbac76`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 09 Jan 2023 17:04:48 GMT
ADD file:3080f19f39259a4b77cc53975de0184c78d4335ceb9ffb77a2838d0539ad6f85 in / 
# Mon, 09 Jan 2023 17:04:49 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 19:16:16 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Mon, 09 Jan 2023 19:16:16 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Mon, 09 Jan 2023 19:16:17 GMT
ARG MAKEFLAGS=
# Mon, 09 Jan 2023 19:16:17 GMT
ENV ZNC_VERSION=1.8.2
# Mon, 09 Jan 2023 19:19:39 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Mon, 09 Jan 2023 19:19:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Mon, 09 Jan 2023 19:19:40 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Mon, 09 Jan 2023 19:19:40 GMT
VOLUME [/znc-data]
# Mon, 09 Jan 2023 19:19:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a9eaa45ef418e883481a13c7d84fa9904f2ec56789c52a87ba5a9e6483f2b74f`  
		Last Modified: Mon, 09 Jan 2023 17:05:12 GMT  
		Size: 3.3 MB (3259241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1a7bf78ba8488ffcb8e702347e8d353e09c6f5b2752202e35038fcfc6a072d`  
		Last Modified: Mon, 09 Jan 2023 19:20:21 GMT  
		Size: 46.2 MB (46152657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036cf60fd34df0dac5ae84e25a8425f8f867c8688e3525fca09e7fa1fd802951`  
		Last Modified: Mon, 09 Jan 2023 19:20:15 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f67a6235f0e6a1e32fd72b1a91ec221405124b966ed6753e49e48b1d5143b3`  
		Last Modified: Mon, 09 Jan 2023 19:20:15 GMT  
		Size: 778.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
