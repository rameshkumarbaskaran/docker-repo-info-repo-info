## `znc:latest`

```console
$ docker pull znc@sha256:6cb18aaa5697c84c5654a5ca953c1101e70b74cff73b666cc9f9f89d1182a9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:latest` - linux; amd64

```console
$ docker pull znc@sha256:35164b10f47970b0059f74dda1ab6e6dc828004ff11aa65bbdac249c7ce6fa0d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138548287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b1acee2da36b45e41bccf8ad06cfea9a255fda8532ffb3fa37160416b40220`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:14 GMT
ADD file:7fd90c097e2c4587dee91726d71abc02fa1aa6a3a3395c862206a4e14e0c299c in / 
# Tue, 09 Aug 2022 17:20:14 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:29:24 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 07 Oct 2022 04:29:24 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 07 Oct 2022 04:29:24 GMT
ARG MAKEFLAGS=
# Fri, 07 Oct 2022 04:29:24 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 07 Oct 2022 04:33:38 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 07 Oct 2022 04:33:39 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 07 Oct 2022 04:33:39 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 07 Oct 2022 04:33:39 GMT
VOLUME [/znc-data]
# Fri, 07 Oct 2022 04:33:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 04:33:53 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 07 Oct 2022 04:33:54 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:72cfd02ff4d01b1f319eed108b53120dea0185b916d2abeb4e6121879cbf7a65`  
		Last Modified: Tue, 09 Aug 2022 17:21:16 GMT  
		Size: 2.8 MB (2827571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0f22044f90ae2a77eb095f28b9428f87de8918f228f9f85339e4cd8aad8850`  
		Last Modified: Fri, 07 Oct 2022 04:34:13 GMT  
		Size: 43.4 MB (43368543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bbd3936fe6a3a35579af2243d727780a9862256c761a2bf141b62fd6d9999e`  
		Last Modified: Fri, 07 Oct 2022 04:34:07 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071b7456cd68899b3f3ec4ab1b6e9e124fb1ea95840688aef6c72bade3d9a4f3`  
		Last Modified: Fri, 07 Oct 2022 04:34:07 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7816457a4059b0065bf58cb940a11bdd7067e636b4976c855f9c8ce40c2134`  
		Last Modified: Fri, 07 Oct 2022 04:34:39 GMT  
		Size: 92.4 MB (92350891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5ad7123205b7247668526fa597cc4a8dabd73cd3ca1e8cc11ad96cca2549c3`  
		Last Modified: Fri, 07 Oct 2022 04:34:26 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:e4238f74b00aae7929ab287c3e81bd10a93b86c62b91f647e24c46c75adfe248
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122179534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73037de035f20c95d0c5d45adf8d44305736624b1703f194954a11d7b7431c70`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:40 GMT
ADD file:541b767b21b9e0c4dab118d5e000990da3dbb81b547c1ee9941e2cf7edc5edd6 in / 
# Tue, 09 Aug 2022 17:49:40 GMT
CMD ["/bin/sh"]
# Sat, 08 Oct 2022 04:03:40 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 08 Oct 2022 04:03:40 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 08 Oct 2022 04:03:40 GMT
ARG MAKEFLAGS=
# Sat, 08 Oct 2022 04:03:40 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 08 Oct 2022 04:08:13 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 08 Oct 2022 04:08:13 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 08 Oct 2022 04:08:14 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 08 Oct 2022 04:08:14 GMT
VOLUME [/znc-data]
# Sat, 08 Oct 2022 04:08:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Oct 2022 04:08:27 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Sat, 08 Oct 2022 04:08:27 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:b423ab447fbb66b194458908339addbb5dd52e4aa7d04a42b387cdc07bbd92a1`  
		Last Modified: Tue, 09 Aug 2022 17:51:16 GMT  
		Size: 2.6 MB (2633535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c3894384c0844f622deea88b6ab05596a1f565d2aa4557a96f6c419b1f1f36`  
		Last Modified: Sat, 08 Oct 2022 04:09:02 GMT  
		Size: 41.6 MB (41645409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f517206166b2d7cf5ddfc516816d145adedb4dd826d180c09c3386dc90672d03`  
		Last Modified: Sat, 08 Oct 2022 04:08:54 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518985203fd479fde2eb5e1634be50637fe4b7f21097fc69daf24a0084dcc0d6`  
		Last Modified: Sat, 08 Oct 2022 04:08:54 GMT  
		Size: 779.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc92e96ac941e3ccc08b584c754017964834febaff714e5aeaa91a62038468c`  
		Last Modified: Sat, 08 Oct 2022 04:09:33 GMT  
		Size: 77.9 MB (77899310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed48f7663283fb5db909d8f8be9be0849b3096e68fc228c752e63f352e4ab01`  
		Last Modified: Sat, 08 Oct 2022 04:09:17 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:e2c1ca8fb245b32c193cde4cba45a214955c13b198398cee31b9b023115fd562
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129852238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4384148afc7b4901bb5e385427b859c694e3bd1b3d923d6493c0855e2bdfb6dc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:40:07 GMT
ADD file:f23c059b4312458fbf0fc018d4695f36157a3eb6e5a83167912a39f9a738f4eb in / 
# Tue, 09 Aug 2022 17:40:07 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 07:54:22 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 07 Oct 2022 07:54:22 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 07 Oct 2022 07:54:23 GMT
ARG MAKEFLAGS=
# Fri, 07 Oct 2022 07:54:24 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 07 Oct 2022 07:59:14 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 07 Oct 2022 07:59:15 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 07 Oct 2022 07:59:16 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 07 Oct 2022 07:59:16 GMT
VOLUME [/znc-data]
# Fri, 07 Oct 2022 07:59:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 07:59:40 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 07 Oct 2022 07:59:41 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:25f523f0e93b2b5fa676c15d91b90f08ee4de7a160874e6c52ea452929d5a7cc`  
		Last Modified: Tue, 09 Aug 2022 17:41:17 GMT  
		Size: 2.7 MB (2722126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6206569e0bdb06e4044b58e956b7facaeece22358eeb2bc15332d098eb7bed`  
		Last Modified: Fri, 07 Oct 2022 08:00:07 GMT  
		Size: 43.2 MB (43228832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98e2c61a6ae4486ffaeda8b0cfa960364e77f2f8ffd9267ec89baa6bbe108e0`  
		Last Modified: Fri, 07 Oct 2022 08:00:01 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e6141e45205c561f503bc9336c56ec0a572893f00f7ae560fb5fc2ac9bbbad`  
		Last Modified: Fri, 07 Oct 2022 08:00:01 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c42699e6d37cec092d37838442b35351ac132944022455bc15a30300893f5e4`  
		Last Modified: Fri, 07 Oct 2022 08:00:34 GMT  
		Size: 83.9 MB (83900021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8ff8262c2b0304ff2ebeeef3c65bb6f039ba208bb0e7d9a1a5f234a5a01be8`  
		Last Modified: Fri, 07 Oct 2022 08:00:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
