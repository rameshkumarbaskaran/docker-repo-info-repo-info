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
$ docker pull znc@sha256:7b4179cda13b7e774bd122067a3ba29633f8564951c6435b18e0d019399d4e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8` - linux; amd64

```console
$ docker pull znc@sha256:06f36fd86b43a8e7734f8170934e9d4fa5bbc6a94ce90f965882edf9f6f0f20d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150968904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c803978ff1716d522e2dbb48cf667a2933030683dec6170898f8ea135ffb72e`
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
# Fri, 26 Mar 2021 02:55:39 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Fri, 26 Mar 2021 02:55:39 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
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
	-	`sha256:7585d98d7ae0ca7844e2d481de40ee8bfee40e04d9afa6d3c57a664165d40cc0`  
		Last Modified: Fri, 26 Mar 2021 02:56:35 GMT  
		Size: 103.4 MB (103376800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3bd687d2611b904fa018ddbec55747e33a4ef0747e568c2976c11c595859cc`  
		Last Modified: Fri, 26 Mar 2021 02:56:17 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8` - linux; arm variant v6

```console
$ docker pull znc@sha256:65938c16bbfe1cdb413134c2f6e862bdd5b0848378921bfc57f30aeee62652ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132439554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039511976f980cfdd239067c71473fd5660112a19995a9647abfa9c17d577d20`
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
# Thu, 25 Feb 2021 00:17:35 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Thu, 25 Feb 2021 00:17:40 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
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
	-	`sha256:e86acd3109e1a9d47fc8f46af7f2278815b6151adfc23a51628adcfa6549c79e`  
		Last Modified: Thu, 25 Feb 2021 00:19:16 GMT  
		Size: 87.0 MB (87019954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8f2dc6f184db59b26d687b9f293731eadea5732883397b6edf33153dd32e8e`  
		Last Modified: Thu, 25 Feb 2021 00:18:45 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:3182f96c3b2ec2cbc0f6514ee006154905ec91500e9eaa56ed462130e7bdf005
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137896947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b329db163eeb059a223ebfb32d397dd0d9024e9e9d6e655d65e60f89ba23780`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:39 GMT
ADD file:7e82858ef85f6db90c131ed835a390d736cfdbd1a0cf8bccaeed8f7e30172ddb in / 
# Wed, 24 Feb 2021 20:39:40 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:56:13 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 24 Feb 2021 20:56:14 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 24 Feb 2021 20:56:14 GMT
ARG MAKEFLAGS=
# Wed, 24 Feb 2021 20:56:15 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 24 Feb 2021 21:05:27 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 24 Feb 2021 21:05:28 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 24 Feb 2021 21:05:29 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:30 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:31 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:32 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:33 GMT
VOLUME [/znc-data]
# Wed, 24 Feb 2021 21:05:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 21:06:08 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Wed, 24 Feb 2021 21:06:10 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:dce8679b510e95d136241d02ababff86469dd14220812a7ce9202833c0e32f66`  
		Last Modified: Wed, 24 Feb 2021 20:40:26 GMT  
		Size: 2.7 MB (2709880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7586597cce0f628e5a326548016b1c7814083444b6c00ab8a914e45b5e69684d`  
		Last Modified: Wed, 24 Feb 2021 21:06:45 GMT  
		Size: 44.4 MB (44411904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628ced890f177e09fa6d905bdd7baa9a6f99ae59609213fb66466e7f32b8dba3`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ded50504325c661aa0baefac4f299624b07f97ee423591bfde127fb66e3ee0a`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da080d2a6e219e12175c28ac524d009e2b0aa03fe07dec5916f9cb164c116863`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379b82ee5fd7718bdcb7c5283b68e3dfa948e27dbb22ae496b50b55d394312f9`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e61cd5304d3b84764e960159b05c953bf3ab497f774bdfd8e9ed3a5fa0604f4`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840f906cdd8cfb337e04784a263016b4f67080af7db001ab6c1193637aa327b6`  
		Last Modified: Wed, 24 Feb 2021 21:07:21 GMT  
		Size: 90.8 MB (90773406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dd3ce3b26b878f743ccea44f18ba5e9f70da67dca89fbcc809e329fb0c14bc`  
		Last Modified: Wed, 24 Feb 2021 21:06:57 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8-slim`

```console
$ docker pull znc@sha256:babf34289a5d96e8ebda9bd7227d2f19ab62fe1dd8b2ad4c40ae99db0c27a341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8-slim` - linux; amd64

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

### `znc:1.8-slim` - linux; arm variant v6

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

### `znc:1.8-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:47a4a9d1272d05a9423888ab471af5c253a7367d92ef8a8c6dfd399e36bbae83
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47123209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f935174bfa0f99dfc90a325ac996e64e67c623d978e3c6eba94ecd747d07010`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:39 GMT
ADD file:7e82858ef85f6db90c131ed835a390d736cfdbd1a0cf8bccaeed8f7e30172ddb in / 
# Wed, 24 Feb 2021 20:39:40 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:56:13 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 24 Feb 2021 20:56:14 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 24 Feb 2021 20:56:14 GMT
ARG MAKEFLAGS=
# Wed, 24 Feb 2021 20:56:15 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 24 Feb 2021 21:05:27 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 24 Feb 2021 21:05:28 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 24 Feb 2021 21:05:29 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:30 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:31 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:32 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:33 GMT
VOLUME [/znc-data]
# Wed, 24 Feb 2021 21:05:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:dce8679b510e95d136241d02ababff86469dd14220812a7ce9202833c0e32f66`  
		Last Modified: Wed, 24 Feb 2021 20:40:26 GMT  
		Size: 2.7 MB (2709880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7586597cce0f628e5a326548016b1c7814083444b6c00ab8a914e45b5e69684d`  
		Last Modified: Wed, 24 Feb 2021 21:06:45 GMT  
		Size: 44.4 MB (44411904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628ced890f177e09fa6d905bdd7baa9a6f99ae59609213fb66466e7f32b8dba3`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ded50504325c661aa0baefac4f299624b07f97ee423591bfde127fb66e3ee0a`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da080d2a6e219e12175c28ac524d009e2b0aa03fe07dec5916f9cb164c116863`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379b82ee5fd7718bdcb7c5283b68e3dfa948e27dbb22ae496b50b55d394312f9`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e61cd5304d3b84764e960159b05c953bf3ab497f774bdfd8e9ed3a5fa0604f4`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8.2`

```console
$ docker pull znc@sha256:7b4179cda13b7e774bd122067a3ba29633f8564951c6435b18e0d019399d4e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8.2` - linux; amd64

```console
$ docker pull znc@sha256:06f36fd86b43a8e7734f8170934e9d4fa5bbc6a94ce90f965882edf9f6f0f20d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150968904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c803978ff1716d522e2dbb48cf667a2933030683dec6170898f8ea135ffb72e`
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
# Fri, 26 Mar 2021 02:55:39 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Fri, 26 Mar 2021 02:55:39 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
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
	-	`sha256:7585d98d7ae0ca7844e2d481de40ee8bfee40e04d9afa6d3c57a664165d40cc0`  
		Last Modified: Fri, 26 Mar 2021 02:56:35 GMT  
		Size: 103.4 MB (103376800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3bd687d2611b904fa018ddbec55747e33a4ef0747e568c2976c11c595859cc`  
		Last Modified: Fri, 26 Mar 2021 02:56:17 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2` - linux; arm variant v6

```console
$ docker pull znc@sha256:65938c16bbfe1cdb413134c2f6e862bdd5b0848378921bfc57f30aeee62652ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132439554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039511976f980cfdd239067c71473fd5660112a19995a9647abfa9c17d577d20`
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
# Thu, 25 Feb 2021 00:17:35 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Thu, 25 Feb 2021 00:17:40 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
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
	-	`sha256:e86acd3109e1a9d47fc8f46af7f2278815b6151adfc23a51628adcfa6549c79e`  
		Last Modified: Thu, 25 Feb 2021 00:19:16 GMT  
		Size: 87.0 MB (87019954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8f2dc6f184db59b26d687b9f293731eadea5732883397b6edf33153dd32e8e`  
		Last Modified: Thu, 25 Feb 2021 00:18:45 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:3182f96c3b2ec2cbc0f6514ee006154905ec91500e9eaa56ed462130e7bdf005
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137896947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b329db163eeb059a223ebfb32d397dd0d9024e9e9d6e655d65e60f89ba23780`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:39 GMT
ADD file:7e82858ef85f6db90c131ed835a390d736cfdbd1a0cf8bccaeed8f7e30172ddb in / 
# Wed, 24 Feb 2021 20:39:40 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:56:13 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 24 Feb 2021 20:56:14 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 24 Feb 2021 20:56:14 GMT
ARG MAKEFLAGS=
# Wed, 24 Feb 2021 20:56:15 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 24 Feb 2021 21:05:27 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 24 Feb 2021 21:05:28 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 24 Feb 2021 21:05:29 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:30 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:31 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:32 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:33 GMT
VOLUME [/znc-data]
# Wed, 24 Feb 2021 21:05:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 21:06:08 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Wed, 24 Feb 2021 21:06:10 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:dce8679b510e95d136241d02ababff86469dd14220812a7ce9202833c0e32f66`  
		Last Modified: Wed, 24 Feb 2021 20:40:26 GMT  
		Size: 2.7 MB (2709880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7586597cce0f628e5a326548016b1c7814083444b6c00ab8a914e45b5e69684d`  
		Last Modified: Wed, 24 Feb 2021 21:06:45 GMT  
		Size: 44.4 MB (44411904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628ced890f177e09fa6d905bdd7baa9a6f99ae59609213fb66466e7f32b8dba3`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ded50504325c661aa0baefac4f299624b07f97ee423591bfde127fb66e3ee0a`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da080d2a6e219e12175c28ac524d009e2b0aa03fe07dec5916f9cb164c116863`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379b82ee5fd7718bdcb7c5283b68e3dfa948e27dbb22ae496b50b55d394312f9`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e61cd5304d3b84764e960159b05c953bf3ab497f774bdfd8e9ed3a5fa0604f4`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840f906cdd8cfb337e04784a263016b4f67080af7db001ab6c1193637aa327b6`  
		Last Modified: Wed, 24 Feb 2021 21:07:21 GMT  
		Size: 90.8 MB (90773406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dd3ce3b26b878f743ccea44f18ba5e9f70da67dca89fbcc809e329fb0c14bc`  
		Last Modified: Wed, 24 Feb 2021 21:06:57 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8.2-slim`

```console
$ docker pull znc@sha256:babf34289a5d96e8ebda9bd7227d2f19ab62fe1dd8b2ad4c40ae99db0c27a341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8.2-slim` - linux; amd64

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

### `znc:1.8.2-slim` - linux; arm variant v6

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

### `znc:1.8.2-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:47a4a9d1272d05a9423888ab471af5c253a7367d92ef8a8c6dfd399e36bbae83
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47123209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f935174bfa0f99dfc90a325ac996e64e67c623d978e3c6eba94ecd747d07010`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:39 GMT
ADD file:7e82858ef85f6db90c131ed835a390d736cfdbd1a0cf8bccaeed8f7e30172ddb in / 
# Wed, 24 Feb 2021 20:39:40 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:56:13 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 24 Feb 2021 20:56:14 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 24 Feb 2021 20:56:14 GMT
ARG MAKEFLAGS=
# Wed, 24 Feb 2021 20:56:15 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 24 Feb 2021 21:05:27 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 24 Feb 2021 21:05:28 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 24 Feb 2021 21:05:29 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:30 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:31 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:32 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:33 GMT
VOLUME [/znc-data]
# Wed, 24 Feb 2021 21:05:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:dce8679b510e95d136241d02ababff86469dd14220812a7ce9202833c0e32f66`  
		Last Modified: Wed, 24 Feb 2021 20:40:26 GMT  
		Size: 2.7 MB (2709880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7586597cce0f628e5a326548016b1c7814083444b6c00ab8a914e45b5e69684d`  
		Last Modified: Wed, 24 Feb 2021 21:06:45 GMT  
		Size: 44.4 MB (44411904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628ced890f177e09fa6d905bdd7baa9a6f99ae59609213fb66466e7f32b8dba3`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ded50504325c661aa0baefac4f299624b07f97ee423591bfde127fb66e3ee0a`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da080d2a6e219e12175c28ac524d009e2b0aa03fe07dec5916f9cb164c116863`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379b82ee5fd7718bdcb7c5283b68e3dfa948e27dbb22ae496b50b55d394312f9`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e61cd5304d3b84764e960159b05c953bf3ab497f774bdfd8e9ed3a5fa0604f4`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:latest`

```console
$ docker pull znc@sha256:7b4179cda13b7e774bd122067a3ba29633f8564951c6435b18e0d019399d4e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:latest` - linux; amd64

```console
$ docker pull znc@sha256:06f36fd86b43a8e7734f8170934e9d4fa5bbc6a94ce90f965882edf9f6f0f20d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150968904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c803978ff1716d522e2dbb48cf667a2933030683dec6170898f8ea135ffb72e`
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
# Fri, 26 Mar 2021 02:55:39 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Fri, 26 Mar 2021 02:55:39 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
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
	-	`sha256:7585d98d7ae0ca7844e2d481de40ee8bfee40e04d9afa6d3c57a664165d40cc0`  
		Last Modified: Fri, 26 Mar 2021 02:56:35 GMT  
		Size: 103.4 MB (103376800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3bd687d2611b904fa018ddbec55747e33a4ef0747e568c2976c11c595859cc`  
		Last Modified: Fri, 26 Mar 2021 02:56:17 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:65938c16bbfe1cdb413134c2f6e862bdd5b0848378921bfc57f30aeee62652ff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132439554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039511976f980cfdd239067c71473fd5660112a19995a9647abfa9c17d577d20`
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
# Thu, 25 Feb 2021 00:17:35 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Thu, 25 Feb 2021 00:17:40 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
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
	-	`sha256:e86acd3109e1a9d47fc8f46af7f2278815b6151adfc23a51628adcfa6549c79e`  
		Last Modified: Thu, 25 Feb 2021 00:19:16 GMT  
		Size: 87.0 MB (87019954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8f2dc6f184db59b26d687b9f293731eadea5732883397b6edf33153dd32e8e`  
		Last Modified: Thu, 25 Feb 2021 00:18:45 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:3182f96c3b2ec2cbc0f6514ee006154905ec91500e9eaa56ed462130e7bdf005
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137896947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b329db163eeb059a223ebfb32d397dd0d9024e9e9d6e655d65e60f89ba23780`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:39 GMT
ADD file:7e82858ef85f6db90c131ed835a390d736cfdbd1a0cf8bccaeed8f7e30172ddb in / 
# Wed, 24 Feb 2021 20:39:40 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:56:13 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 24 Feb 2021 20:56:14 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 24 Feb 2021 20:56:14 GMT
ARG MAKEFLAGS=
# Wed, 24 Feb 2021 20:56:15 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 24 Feb 2021 21:05:27 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 24 Feb 2021 21:05:28 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 24 Feb 2021 21:05:29 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:30 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:31 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:32 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:33 GMT
VOLUME [/znc-data]
# Wed, 24 Feb 2021 21:05:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 21:06:08 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Wed, 24 Feb 2021 21:06:10 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:dce8679b510e95d136241d02ababff86469dd14220812a7ce9202833c0e32f66`  
		Last Modified: Wed, 24 Feb 2021 20:40:26 GMT  
		Size: 2.7 MB (2709880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7586597cce0f628e5a326548016b1c7814083444b6c00ab8a914e45b5e69684d`  
		Last Modified: Wed, 24 Feb 2021 21:06:45 GMT  
		Size: 44.4 MB (44411904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628ced890f177e09fa6d905bdd7baa9a6f99ae59609213fb66466e7f32b8dba3`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ded50504325c661aa0baefac4f299624b07f97ee423591bfde127fb66e3ee0a`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da080d2a6e219e12175c28ac524d009e2b0aa03fe07dec5916f9cb164c116863`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379b82ee5fd7718bdcb7c5283b68e3dfa948e27dbb22ae496b50b55d394312f9`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e61cd5304d3b84764e960159b05c953bf3ab497f774bdfd8e9ed3a5fa0604f4`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840f906cdd8cfb337e04784a263016b4f67080af7db001ab6c1193637aa327b6`  
		Last Modified: Wed, 24 Feb 2021 21:07:21 GMT  
		Size: 90.8 MB (90773406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dd3ce3b26b878f743ccea44f18ba5e9f70da67dca89fbcc809e329fb0c14bc`  
		Last Modified: Wed, 24 Feb 2021 21:06:57 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:slim`

```console
$ docker pull znc@sha256:babf34289a5d96e8ebda9bd7227d2f19ab62fe1dd8b2ad4c40ae99db0c27a341
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
$ docker pull znc@sha256:47a4a9d1272d05a9423888ab471af5c253a7367d92ef8a8c6dfd399e36bbae83
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47123209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f935174bfa0f99dfc90a325ac996e64e67c623d978e3c6eba94ecd747d07010`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:39 GMT
ADD file:7e82858ef85f6db90c131ed835a390d736cfdbd1a0cf8bccaeed8f7e30172ddb in / 
# Wed, 24 Feb 2021 20:39:40 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:56:13 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 24 Feb 2021 20:56:14 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 24 Feb 2021 20:56:14 GMT
ARG MAKEFLAGS=
# Wed, 24 Feb 2021 20:56:15 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 24 Feb 2021 21:05:27 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 24 Feb 2021 21:05:28 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 24 Feb 2021 21:05:29 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:30 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:31 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:32 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Wed, 24 Feb 2021 21:05:33 GMT
VOLUME [/znc-data]
# Wed, 24 Feb 2021 21:05:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:dce8679b510e95d136241d02ababff86469dd14220812a7ce9202833c0e32f66`  
		Last Modified: Wed, 24 Feb 2021 20:40:26 GMT  
		Size: 2.7 MB (2709880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7586597cce0f628e5a326548016b1c7814083444b6c00ab8a914e45b5e69684d`  
		Last Modified: Wed, 24 Feb 2021 21:06:45 GMT  
		Size: 44.4 MB (44411904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628ced890f177e09fa6d905bdd7baa9a6f99ae59609213fb66466e7f32b8dba3`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ded50504325c661aa0baefac4f299624b07f97ee423591bfde127fb66e3ee0a`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da080d2a6e219e12175c28ac524d009e2b0aa03fe07dec5916f9cb164c116863`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379b82ee5fd7718bdcb7c5283b68e3dfa948e27dbb22ae496b50b55d394312f9`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e61cd5304d3b84764e960159b05c953bf3ab497f774bdfd8e9ed3a5fa0604f4`  
		Last Modified: Wed, 24 Feb 2021 21:06:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
