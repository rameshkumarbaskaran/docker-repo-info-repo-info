## `znc:slim`

```console
$ docker pull znc@sha256:34ce86e57d2ca0b5b24b64f71f6fed4070e137467b475a2e68394bb8505bb8ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:slim` - linux; amd64

```console
$ docker pull znc@sha256:4303ffe84845e4386c18f084a7100f391b9e71311400d623391d17e7195ddb29
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47591773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f27eae3fac4ef84586b44f4ca6e780dafaae50dbe4bf6c460ec7125dedcdf3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:38 GMT
ADD file:b2c067f4304d00c91fc9fd92f2e58853412cc705dfda4d1cf658fab965d5802c in / 
# Thu, 25 Mar 2021 22:19:38 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:49:36 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 26 Mar 2021 02:49:37 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 26 Mar 2021 02:49:37 GMT
ARG MAKEFLAGS=
# Fri, 26 Mar 2021 02:49:37 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 26 Mar 2021 02:55:28 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 26 Mar 2021 02:55:28 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 26 Mar 2021 02:55:28 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Fri, 26 Mar 2021 02:55:29 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Fri, 26 Mar 2021 02:55:29 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Fri, 26 Mar 2021 02:55:29 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Fri, 26 Mar 2021 02:55:29 GMT
VOLUME [/znc-data]
# Fri, 26 Mar 2021 02:55:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:22599d3e9e25e799b87521b94e20d20a601ffad16cf676274fdf94b089e4b979`  
		Last Modified: Thu, 25 Mar 2021 22:20:35 GMT  
		Size: 2.8 MB (2799762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef753c00beaf06a3ee7647f2da37af968d3c33b9655927a8d6aca2d1d995e28c`  
		Last Modified: Fri, 26 Mar 2021 02:56:04 GMT  
		Size: 44.8 MB (44790585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9739f8a41ed5c01a8660fa107743ba3fb79709cdf9fd584ea4298252afa54a14`  
		Last Modified: Fri, 26 Mar 2021 02:55:52 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f021d06d531c1dbf7b87991e227094bb17ed380b2aeac36c819c64fad6cf9cc`  
		Last Modified: Fri, 26 Mar 2021 02:55:53 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db01e30df5558a3c24faf6d409e32758133a06c2e2145417d83e1cbeb3e4aee`  
		Last Modified: Fri, 26 Mar 2021 02:55:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afac7b001b7aa8a0b0dbd7c72ca4b057cf50099234a4751ab06b4e33b5a17f10`  
		Last Modified: Fri, 26 Mar 2021 02:55:52 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee18e3181ce87afeaaadc596532013194e9cc8132f0c58f8d235f7f9295e734`  
		Last Modified: Fri, 26 Mar 2021 02:55:52 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:dee2ae871d5ba90dc393e1814e4e70a5bc881ce1031c64a6dcca0060403b7dcd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45419269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9f3f5d0441548bfa2c5d9a8ba74c8b233d7730181b69aa19fc7225d0e05b64`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 24 Feb 2021 20:50:34 GMT
ADD file:8bbb59eeaad0cbcf11559bc6e2b4492aadf6822d1935ed50c710f8bed858b7b5 in / 
# Wed, 24 Feb 2021 20:50:35 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 00:05:52 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Thu, 25 Feb 2021 00:05:54 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Thu, 25 Feb 2021 00:05:55 GMT
ARG MAKEFLAGS=
# Thu, 25 Feb 2021 00:05:56 GMT
ENV ZNC_VERSION=1.8.2
# Thu, 25 Feb 2021 00:16:45 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Thu, 25 Feb 2021 00:16:49 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Thu, 25 Feb 2021 00:16:50 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Thu, 25 Feb 2021 00:16:52 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Thu, 25 Feb 2021 00:16:53 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Thu, 25 Feb 2021 00:16:55 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Thu, 25 Feb 2021 00:16:57 GMT
VOLUME [/znc-data]
# Thu, 25 Feb 2021 00:16:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:55242616b0494f68f44470d864da746cd2a8f8f2d1ffca698114de64032247ef`  
		Last Modified: Wed, 24 Feb 2021 20:51:17 GMT  
		Size: 2.6 MB (2604518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5382eb529edc8827223b1e771b71b9ec4246903d8932a72af4cbbede2862c273`  
		Last Modified: Thu, 25 Feb 2021 00:18:35 GMT  
		Size: 42.8 MB (42813329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c84d00487acf56156df7e0d7b62b65086bcf6bbe1464729445a97d2a82d48b0`  
		Last Modified: Thu, 25 Feb 2021 00:18:07 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ee44f878022162e611df75d3dc8be576fafeedc5fd645f088d3340b63dda95`  
		Last Modified: Thu, 25 Feb 2021 00:18:07 GMT  
		Size: 303.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93257e4598aba884a5ef9132f06d1dce454f3cc46f9fee09e29d7438a920240`  
		Last Modified: Thu, 25 Feb 2021 00:18:07 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd674f1f6e1fb31fabb64453592d639500decc1669e867d1507b9d84ec7a311`  
		Last Modified: Thu, 25 Feb 2021 00:18:07 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b0254f213f32fb94783d0eb98ec6a9448f28dfe95faf0f41b516e65372dada`  
		Last Modified: Thu, 25 Feb 2021 00:18:07 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:b2c8bb3fb1e9afe5258235cc3c9d3f4d6901d1252257dd61ebd2d03621344885
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47345578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9b88dc147bf333fbb832cb8f42a88497233062db2848c50687f14fe28d1180`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:00 GMT
ADD file:97aac29a9ffbba2c76441891035010395614dc3115c4710d58932205b604308f in / 
# Thu, 25 Mar 2021 22:41:10 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:50:00 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 26 Mar 2021 08:50:01 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Fri, 26 Mar 2021 08:50:01 GMT
ARG MAKEFLAGS=
# Fri, 26 Mar 2021 08:50:02 GMT
ENV ZNC_VERSION=1.8.2
# Fri, 26 Mar 2021 08:58:39 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 26 Mar 2021 08:58:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 26 Mar 2021 08:58:41 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Fri, 26 Mar 2021 08:58:43 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Fri, 26 Mar 2021 08:58:44 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Fri, 26 Mar 2021 08:58:45 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Fri, 26 Mar 2021 08:58:46 GMT
VOLUME [/znc-data]
# Fri, 26 Mar 2021 08:58:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:95dec6db372224fc1909f0d0c0a9a9d5767ec6b78d066ff6a7d5723160037828`  
		Last Modified: Thu, 25 Mar 2021 22:45:23 GMT  
		Size: 2.7 MB (2709692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261b1493d1cb2458295caac1ef25dd52633a9918efc444ba17cc51219d26a8d9`  
		Last Modified: Fri, 26 Mar 2021 08:59:40 GMT  
		Size: 44.6 MB (44634463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2281c6206ad9e01aeba3f087c93c093edf03b65b013c1e5f30f1c1cc74e9d4d`  
		Last Modified: Fri, 26 Mar 2021 08:59:27 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6757db4ee2933909c092344b92ea6da1ae5f0cb9dc22909417c149a6c7230e6`  
		Last Modified: Fri, 26 Mar 2021 08:59:27 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1812d97bc4f8773fb4157ee1040400c92ba44a0f4cb42ee1d3968738f711d30`  
		Last Modified: Fri, 26 Mar 2021 08:59:26 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ed828033ac4f4536b200687724afd662cadc3cadab7be191836076e23b0a8`  
		Last Modified: Fri, 26 Mar 2021 08:59:26 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351579885da0be0c3e00c76b547db0e55bdeeba9d93a2a5bc221e79e44d1cdb`  
		Last Modified: Fri, 26 Mar 2021 08:59:26 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
