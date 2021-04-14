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
$ docker pull znc@sha256:df6784799c7290ddfc38dce5345db11b803b0ee36543dafd9848ba74dcf07f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8` - linux; amd64

```console
$ docker pull znc@sha256:0cccc12e308a5d762b9cbec014d5472450096302610abdceff1542d7a1621280
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150970876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ab11ca8f6374fc1adc2dc533e83e5e048b94095d9b0ed356a5608341d71053`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 17:49:00 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Thu, 01 Apr 2021 17:49:00 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Thu, 01 Apr 2021 17:49:01 GMT
ARG MAKEFLAGS=
# Thu, 01 Apr 2021 17:49:01 GMT
ENV ZNC_VERSION=1.8.2
# Thu, 01 Apr 2021 17:52:47 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Thu, 01 Apr 2021 17:52:47 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
VOLUME [/znc-data]
# Thu, 01 Apr 2021 17:52:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 17:53:03 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Thu, 01 Apr 2021 17:53:03 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1103d376d29954cff3fea6de5480826bc263f3888c64bc57dab67a4ef9cdea`  
		Last Modified: Thu, 01 Apr 2021 17:53:29 GMT  
		Size: 44.8 MB (44792653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc40e0a135454655217450977447b9282013e0751f0434a0001f45292f5497cd`  
		Last Modified: Thu, 01 Apr 2021 17:53:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857bfaea68a2cbe5b808fa821d0ccb1d361c3758d3df34a2366f0b4cb72f8681`  
		Last Modified: Thu, 01 Apr 2021 17:53:19 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f942297ef7eb757f7f04ece23aca503f6f7db401b6d0a55f97f6f6a6463200d1`  
		Last Modified: Thu, 01 Apr 2021 17:53:20 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2634923c8781f93aa89d896f3e6e81eb52b7270c9a910b6848a64ab2af3631a9`  
		Last Modified: Thu, 01 Apr 2021 17:53:18 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eb40a55b0d76878ebe44114be2eccb1346cc6bbf4f56b0f5364a38049f4004`  
		Last Modified: Thu, 01 Apr 2021 17:53:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9988bb148379af77a0e3d6cff7a5b17b96fe6fc365ce48a4b7117686675023`  
		Last Modified: Thu, 01 Apr 2021 17:54:02 GMT  
		Size: 103.4 MB (103376759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae11985415ffff5fdf6801187aec20092b9a1a9430ab364ea11473759970d99`  
		Last Modified: Thu, 01 Apr 2021 17:53:44 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8` - linux; arm variant v6

```console
$ docker pull znc@sha256:637262cf7726596493c9e1b36319cadee4df531ad169e2ab193bfa5c793c606a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132687454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db254ececf401d0f7db47f515c435b080eeccf382db2085cedd9b4df8336259c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:06:24 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 14 Apr 2021 19:06:25 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 14 Apr 2021 19:06:26 GMT
ARG MAKEFLAGS=
# Wed, 14 Apr 2021 19:06:27 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 14 Apr 2021 19:14:38 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 14 Apr 2021 19:14:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 14 Apr 2021 19:14:41 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:42 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:43 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:44 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:45 GMT
VOLUME [/znc-data]
# Wed, 14 Apr 2021 19:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Apr 2021 19:15:07 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Wed, 14 Apr 2021 19:15:10 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a7c2bb5435b1fa5a12ae177d982fedb637c06223b2c701cb90ecd09de64929`  
		Last Modified: Wed, 14 Apr 2021 19:15:45 GMT  
		Size: 43.0 MB (43047705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174b893fee9110b0d361ce6ac762b55def7e783e102df78cfa7de76273c474c2`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cd01900ad296ad09f6b29dc0dbf821432761b6b9771daddbe9077e2ac7bede`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4852ba58f3351dc50f648ff54754f3143c4bc73aff353c8fc44f1ca4b2727e1b`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e2bd3ffa516127012f7dd673a572cff0cc0b3a53555d987507a3f0e697e70d`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc133d3eda0b1cbf3ee429aa42a8babe168097f3490aff7e11bf216e2200ff9`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6f9dc0fc71449c9d6aa086257cdeeccd8c2b27bc1d0912041ec74b9acd1e76`  
		Last Modified: Wed, 14 Apr 2021 19:16:23 GMT  
		Size: 87.0 MB (87032736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773f8f7b9621c6f9898eccd6e54c2229ef68db2240332907412d1c0e7a7bb167`  
		Last Modified: Wed, 14 Apr 2021 19:15:56 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:0a733b42166ea183134133b15d3eb864698e431e36b0b3cec35b03d435e2db5d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138119446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4eeffdf302195ad59ce285311e54882c7431f33635a3bad1164497c7b8243c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:48 GMT
ADD file:dd1db8a59e36aac513488fa97629360c665b6079fb7c6b3cd09065ef993f6675 in / 
# Wed, 31 Mar 2021 17:21:50 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 16:25:22 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Thu, 01 Apr 2021 16:25:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Thu, 01 Apr 2021 16:25:24 GMT
ARG MAKEFLAGS=
# Thu, 01 Apr 2021 16:25:24 GMT
ENV ZNC_VERSION=1.8.2
# Thu, 01 Apr 2021 16:33:35 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Thu, 01 Apr 2021 16:33:37 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Thu, 01 Apr 2021 16:33:38 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:39 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:40 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:41 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:42 GMT
VOLUME [/znc-data]
# Thu, 01 Apr 2021 16:33:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 16:34:13 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Thu, 01 Apr 2021 16:34:16 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:9a219e8acc52b4071b6121a1e4d4ecbce48f38113fbbcfe026c26768ce76bcc0`  
		Last Modified: Wed, 31 Mar 2021 17:22:52 GMT  
		Size: 2.7 MB (2709852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b4a14ad4a95a93c1ec49befe5db8a6c134ef9f688ef91a8a893fcd71f28295`  
		Last Modified: Thu, 01 Apr 2021 16:34:46 GMT  
		Size: 44.6 MB (44634326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecd51a9f27e0a81e979cd79a8c85b9d28404be2276e1fa575ad2b04a45f632d`  
		Last Modified: Thu, 01 Apr 2021 16:34:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6124bb532c242c74f7cfc2997c96d310c1c795fbd1d60db99e23e5979853c0`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c215a41a50553b36c36bb621700ed53bb792aa6fa6c6f8de650bb5283aebd636`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b90612607d4d3ff34f3f99c13cfb3fae6b62f2bc2e16653a33da1648a98099`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4139ba013ae04e155d31c48860248aa044aeaf79d2c14c0ccc788a19da8b24`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4df986b08a57d06eb4aec4f3dad35e381dccabb8e383efdfb6110ef696758a`  
		Last Modified: Thu, 01 Apr 2021 16:35:28 GMT  
		Size: 90.8 MB (90773511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edefd45ea576487b4729c1f530f7a62473c0784a020035e7c492be0d2db78f33`  
		Last Modified: Thu, 01 Apr 2021 16:35:00 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8-slim`

```console
$ docker pull znc@sha256:d76170ef7fd803fd9c72eacd7fa9c166c9172396b8f3ddc265b5024c45454b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8-slim` - linux; amd64

```console
$ docker pull znc@sha256:f6b4ab358a44c0bbd15e36b434fe7d258be74b9766055c965816fffd3624b387
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47593787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9ffdec9a24c864640b5e25ed19f26464c206b5423df96aaed62ccd4becaea5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 17:49:00 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Thu, 01 Apr 2021 17:49:00 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Thu, 01 Apr 2021 17:49:01 GMT
ARG MAKEFLAGS=
# Thu, 01 Apr 2021 17:49:01 GMT
ENV ZNC_VERSION=1.8.2
# Thu, 01 Apr 2021 17:52:47 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Thu, 01 Apr 2021 17:52:47 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
VOLUME [/znc-data]
# Thu, 01 Apr 2021 17:52:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1103d376d29954cff3fea6de5480826bc263f3888c64bc57dab67a4ef9cdea`  
		Last Modified: Thu, 01 Apr 2021 17:53:29 GMT  
		Size: 44.8 MB (44792653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc40e0a135454655217450977447b9282013e0751f0434a0001f45292f5497cd`  
		Last Modified: Thu, 01 Apr 2021 17:53:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857bfaea68a2cbe5b808fa821d0ccb1d361c3758d3df34a2366f0b4cb72f8681`  
		Last Modified: Thu, 01 Apr 2021 17:53:19 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f942297ef7eb757f7f04ece23aca503f6f7db401b6d0a55f97f6f6a6463200d1`  
		Last Modified: Thu, 01 Apr 2021 17:53:20 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2634923c8781f93aa89d896f3e6e81eb52b7270c9a910b6848a64ab2af3631a9`  
		Last Modified: Thu, 01 Apr 2021 17:53:18 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eb40a55b0d76878ebe44114be2eccb1346cc6bbf4f56b0f5364a38049f4004`  
		Last Modified: Thu, 01 Apr 2021 17:53:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:9b761b1992bdda212d16af7b3b2d0d468764d161c88035178ac474f7537a0eb9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2ff69e5ce11a914848b667be0bf0a31b595738cc67565d230d38f15915d641`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:06:24 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 14 Apr 2021 19:06:25 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 14 Apr 2021 19:06:26 GMT
ARG MAKEFLAGS=
# Wed, 14 Apr 2021 19:06:27 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 14 Apr 2021 19:14:38 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 14 Apr 2021 19:14:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 14 Apr 2021 19:14:41 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:42 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:43 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:44 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:45 GMT
VOLUME [/znc-data]
# Wed, 14 Apr 2021 19:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a7c2bb5435b1fa5a12ae177d982fedb637c06223b2c701cb90ecd09de64929`  
		Last Modified: Wed, 14 Apr 2021 19:15:45 GMT  
		Size: 43.0 MB (43047705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174b893fee9110b0d361ce6ac762b55def7e783e102df78cfa7de76273c474c2`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cd01900ad296ad09f6b29dc0dbf821432761b6b9771daddbe9077e2ac7bede`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4852ba58f3351dc50f648ff54754f3143c4bc73aff353c8fc44f1ca4b2727e1b`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e2bd3ffa516127012f7dd673a572cff0cc0b3a53555d987507a3f0e697e70d`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc133d3eda0b1cbf3ee429aa42a8babe168097f3490aff7e11bf216e2200ff9`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:ab0377ddda004ac1e00e310d647774727609814961c5802d587578350592bedd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47345602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90b74d05978dcb1995981bd235bac3d679307b809f82390897cdad29afc6604`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:48 GMT
ADD file:dd1db8a59e36aac513488fa97629360c665b6079fb7c6b3cd09065ef993f6675 in / 
# Wed, 31 Mar 2021 17:21:50 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 16:25:22 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Thu, 01 Apr 2021 16:25:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Thu, 01 Apr 2021 16:25:24 GMT
ARG MAKEFLAGS=
# Thu, 01 Apr 2021 16:25:24 GMT
ENV ZNC_VERSION=1.8.2
# Thu, 01 Apr 2021 16:33:35 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Thu, 01 Apr 2021 16:33:37 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Thu, 01 Apr 2021 16:33:38 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:39 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:40 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:41 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:42 GMT
VOLUME [/znc-data]
# Thu, 01 Apr 2021 16:33:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9a219e8acc52b4071b6121a1e4d4ecbce48f38113fbbcfe026c26768ce76bcc0`  
		Last Modified: Wed, 31 Mar 2021 17:22:52 GMT  
		Size: 2.7 MB (2709852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b4a14ad4a95a93c1ec49befe5db8a6c134ef9f688ef91a8a893fcd71f28295`  
		Last Modified: Thu, 01 Apr 2021 16:34:46 GMT  
		Size: 44.6 MB (44634326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecd51a9f27e0a81e979cd79a8c85b9d28404be2276e1fa575ad2b04a45f632d`  
		Last Modified: Thu, 01 Apr 2021 16:34:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6124bb532c242c74f7cfc2997c96d310c1c795fbd1d60db99e23e5979853c0`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c215a41a50553b36c36bb621700ed53bb792aa6fa6c6f8de650bb5283aebd636`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b90612607d4d3ff34f3f99c13cfb3fae6b62f2bc2e16653a33da1648a98099`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4139ba013ae04e155d31c48860248aa044aeaf79d2c14c0ccc788a19da8b24`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8.2`

```console
$ docker pull znc@sha256:df6784799c7290ddfc38dce5345db11b803b0ee36543dafd9848ba74dcf07f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8.2` - linux; amd64

```console
$ docker pull znc@sha256:0cccc12e308a5d762b9cbec014d5472450096302610abdceff1542d7a1621280
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150970876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ab11ca8f6374fc1adc2dc533e83e5e048b94095d9b0ed356a5608341d71053`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 17:49:00 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Thu, 01 Apr 2021 17:49:00 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Thu, 01 Apr 2021 17:49:01 GMT
ARG MAKEFLAGS=
# Thu, 01 Apr 2021 17:49:01 GMT
ENV ZNC_VERSION=1.8.2
# Thu, 01 Apr 2021 17:52:47 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Thu, 01 Apr 2021 17:52:47 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
VOLUME [/znc-data]
# Thu, 01 Apr 2021 17:52:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 17:53:03 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Thu, 01 Apr 2021 17:53:03 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1103d376d29954cff3fea6de5480826bc263f3888c64bc57dab67a4ef9cdea`  
		Last Modified: Thu, 01 Apr 2021 17:53:29 GMT  
		Size: 44.8 MB (44792653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc40e0a135454655217450977447b9282013e0751f0434a0001f45292f5497cd`  
		Last Modified: Thu, 01 Apr 2021 17:53:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857bfaea68a2cbe5b808fa821d0ccb1d361c3758d3df34a2366f0b4cb72f8681`  
		Last Modified: Thu, 01 Apr 2021 17:53:19 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f942297ef7eb757f7f04ece23aca503f6f7db401b6d0a55f97f6f6a6463200d1`  
		Last Modified: Thu, 01 Apr 2021 17:53:20 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2634923c8781f93aa89d896f3e6e81eb52b7270c9a910b6848a64ab2af3631a9`  
		Last Modified: Thu, 01 Apr 2021 17:53:18 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eb40a55b0d76878ebe44114be2eccb1346cc6bbf4f56b0f5364a38049f4004`  
		Last Modified: Thu, 01 Apr 2021 17:53:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9988bb148379af77a0e3d6cff7a5b17b96fe6fc365ce48a4b7117686675023`  
		Last Modified: Thu, 01 Apr 2021 17:54:02 GMT  
		Size: 103.4 MB (103376759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae11985415ffff5fdf6801187aec20092b9a1a9430ab364ea11473759970d99`  
		Last Modified: Thu, 01 Apr 2021 17:53:44 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2` - linux; arm variant v6

```console
$ docker pull znc@sha256:637262cf7726596493c9e1b36319cadee4df531ad169e2ab193bfa5c793c606a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132687454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db254ececf401d0f7db47f515c435b080eeccf382db2085cedd9b4df8336259c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:06:24 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 14 Apr 2021 19:06:25 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 14 Apr 2021 19:06:26 GMT
ARG MAKEFLAGS=
# Wed, 14 Apr 2021 19:06:27 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 14 Apr 2021 19:14:38 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 14 Apr 2021 19:14:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 14 Apr 2021 19:14:41 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:42 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:43 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:44 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:45 GMT
VOLUME [/znc-data]
# Wed, 14 Apr 2021 19:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Apr 2021 19:15:07 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Wed, 14 Apr 2021 19:15:10 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a7c2bb5435b1fa5a12ae177d982fedb637c06223b2c701cb90ecd09de64929`  
		Last Modified: Wed, 14 Apr 2021 19:15:45 GMT  
		Size: 43.0 MB (43047705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174b893fee9110b0d361ce6ac762b55def7e783e102df78cfa7de76273c474c2`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cd01900ad296ad09f6b29dc0dbf821432761b6b9771daddbe9077e2ac7bede`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4852ba58f3351dc50f648ff54754f3143c4bc73aff353c8fc44f1ca4b2727e1b`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e2bd3ffa516127012f7dd673a572cff0cc0b3a53555d987507a3f0e697e70d`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc133d3eda0b1cbf3ee429aa42a8babe168097f3490aff7e11bf216e2200ff9`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6f9dc0fc71449c9d6aa086257cdeeccd8c2b27bc1d0912041ec74b9acd1e76`  
		Last Modified: Wed, 14 Apr 2021 19:16:23 GMT  
		Size: 87.0 MB (87032736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773f8f7b9621c6f9898eccd6e54c2229ef68db2240332907412d1c0e7a7bb167`  
		Last Modified: Wed, 14 Apr 2021 19:15:56 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:0a733b42166ea183134133b15d3eb864698e431e36b0b3cec35b03d435e2db5d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138119446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4eeffdf302195ad59ce285311e54882c7431f33635a3bad1164497c7b8243c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:48 GMT
ADD file:dd1db8a59e36aac513488fa97629360c665b6079fb7c6b3cd09065ef993f6675 in / 
# Wed, 31 Mar 2021 17:21:50 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 16:25:22 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Thu, 01 Apr 2021 16:25:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Thu, 01 Apr 2021 16:25:24 GMT
ARG MAKEFLAGS=
# Thu, 01 Apr 2021 16:25:24 GMT
ENV ZNC_VERSION=1.8.2
# Thu, 01 Apr 2021 16:33:35 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Thu, 01 Apr 2021 16:33:37 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Thu, 01 Apr 2021 16:33:38 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:39 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:40 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:41 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:42 GMT
VOLUME [/znc-data]
# Thu, 01 Apr 2021 16:33:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 16:34:13 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Thu, 01 Apr 2021 16:34:16 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:9a219e8acc52b4071b6121a1e4d4ecbce48f38113fbbcfe026c26768ce76bcc0`  
		Last Modified: Wed, 31 Mar 2021 17:22:52 GMT  
		Size: 2.7 MB (2709852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b4a14ad4a95a93c1ec49befe5db8a6c134ef9f688ef91a8a893fcd71f28295`  
		Last Modified: Thu, 01 Apr 2021 16:34:46 GMT  
		Size: 44.6 MB (44634326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecd51a9f27e0a81e979cd79a8c85b9d28404be2276e1fa575ad2b04a45f632d`  
		Last Modified: Thu, 01 Apr 2021 16:34:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6124bb532c242c74f7cfc2997c96d310c1c795fbd1d60db99e23e5979853c0`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c215a41a50553b36c36bb621700ed53bb792aa6fa6c6f8de650bb5283aebd636`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b90612607d4d3ff34f3f99c13cfb3fae6b62f2bc2e16653a33da1648a98099`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4139ba013ae04e155d31c48860248aa044aeaf79d2c14c0ccc788a19da8b24`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4df986b08a57d06eb4aec4f3dad35e381dccabb8e383efdfb6110ef696758a`  
		Last Modified: Thu, 01 Apr 2021 16:35:28 GMT  
		Size: 90.8 MB (90773511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edefd45ea576487b4729c1f530f7a62473c0784a020035e7c492be0d2db78f33`  
		Last Modified: Thu, 01 Apr 2021 16:35:00 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8.2-slim`

```console
$ docker pull znc@sha256:d76170ef7fd803fd9c72eacd7fa9c166c9172396b8f3ddc265b5024c45454b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8.2-slim` - linux; amd64

```console
$ docker pull znc@sha256:f6b4ab358a44c0bbd15e36b434fe7d258be74b9766055c965816fffd3624b387
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47593787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9ffdec9a24c864640b5e25ed19f26464c206b5423df96aaed62ccd4becaea5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 17:49:00 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Thu, 01 Apr 2021 17:49:00 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Thu, 01 Apr 2021 17:49:01 GMT
ARG MAKEFLAGS=
# Thu, 01 Apr 2021 17:49:01 GMT
ENV ZNC_VERSION=1.8.2
# Thu, 01 Apr 2021 17:52:47 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Thu, 01 Apr 2021 17:52:47 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
VOLUME [/znc-data]
# Thu, 01 Apr 2021 17:52:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1103d376d29954cff3fea6de5480826bc263f3888c64bc57dab67a4ef9cdea`  
		Last Modified: Thu, 01 Apr 2021 17:53:29 GMT  
		Size: 44.8 MB (44792653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc40e0a135454655217450977447b9282013e0751f0434a0001f45292f5497cd`  
		Last Modified: Thu, 01 Apr 2021 17:53:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857bfaea68a2cbe5b808fa821d0ccb1d361c3758d3df34a2366f0b4cb72f8681`  
		Last Modified: Thu, 01 Apr 2021 17:53:19 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f942297ef7eb757f7f04ece23aca503f6f7db401b6d0a55f97f6f6a6463200d1`  
		Last Modified: Thu, 01 Apr 2021 17:53:20 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2634923c8781f93aa89d896f3e6e81eb52b7270c9a910b6848a64ab2af3631a9`  
		Last Modified: Thu, 01 Apr 2021 17:53:18 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eb40a55b0d76878ebe44114be2eccb1346cc6bbf4f56b0f5364a38049f4004`  
		Last Modified: Thu, 01 Apr 2021 17:53:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:9b761b1992bdda212d16af7b3b2d0d468764d161c88035178ac474f7537a0eb9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2ff69e5ce11a914848b667be0bf0a31b595738cc67565d230d38f15915d641`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:06:24 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 14 Apr 2021 19:06:25 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 14 Apr 2021 19:06:26 GMT
ARG MAKEFLAGS=
# Wed, 14 Apr 2021 19:06:27 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 14 Apr 2021 19:14:38 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 14 Apr 2021 19:14:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 14 Apr 2021 19:14:41 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:42 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:43 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:44 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:45 GMT
VOLUME [/znc-data]
# Wed, 14 Apr 2021 19:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a7c2bb5435b1fa5a12ae177d982fedb637c06223b2c701cb90ecd09de64929`  
		Last Modified: Wed, 14 Apr 2021 19:15:45 GMT  
		Size: 43.0 MB (43047705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174b893fee9110b0d361ce6ac762b55def7e783e102df78cfa7de76273c474c2`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cd01900ad296ad09f6b29dc0dbf821432761b6b9771daddbe9077e2ac7bede`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4852ba58f3351dc50f648ff54754f3143c4bc73aff353c8fc44f1ca4b2727e1b`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e2bd3ffa516127012f7dd673a572cff0cc0b3a53555d987507a3f0e697e70d`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc133d3eda0b1cbf3ee429aa42a8babe168097f3490aff7e11bf216e2200ff9`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:ab0377ddda004ac1e00e310d647774727609814961c5802d587578350592bedd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47345602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90b74d05978dcb1995981bd235bac3d679307b809f82390897cdad29afc6604`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:48 GMT
ADD file:dd1db8a59e36aac513488fa97629360c665b6079fb7c6b3cd09065ef993f6675 in / 
# Wed, 31 Mar 2021 17:21:50 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 16:25:22 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Thu, 01 Apr 2021 16:25:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Thu, 01 Apr 2021 16:25:24 GMT
ARG MAKEFLAGS=
# Thu, 01 Apr 2021 16:25:24 GMT
ENV ZNC_VERSION=1.8.2
# Thu, 01 Apr 2021 16:33:35 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Thu, 01 Apr 2021 16:33:37 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Thu, 01 Apr 2021 16:33:38 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:39 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:40 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:41 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:42 GMT
VOLUME [/znc-data]
# Thu, 01 Apr 2021 16:33:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9a219e8acc52b4071b6121a1e4d4ecbce48f38113fbbcfe026c26768ce76bcc0`  
		Last Modified: Wed, 31 Mar 2021 17:22:52 GMT  
		Size: 2.7 MB (2709852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b4a14ad4a95a93c1ec49befe5db8a6c134ef9f688ef91a8a893fcd71f28295`  
		Last Modified: Thu, 01 Apr 2021 16:34:46 GMT  
		Size: 44.6 MB (44634326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecd51a9f27e0a81e979cd79a8c85b9d28404be2276e1fa575ad2b04a45f632d`  
		Last Modified: Thu, 01 Apr 2021 16:34:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6124bb532c242c74f7cfc2997c96d310c1c795fbd1d60db99e23e5979853c0`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c215a41a50553b36c36bb621700ed53bb792aa6fa6c6f8de650bb5283aebd636`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b90612607d4d3ff34f3f99c13cfb3fae6b62f2bc2e16653a33da1648a98099`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4139ba013ae04e155d31c48860248aa044aeaf79d2c14c0ccc788a19da8b24`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:latest`

```console
$ docker pull znc@sha256:df6784799c7290ddfc38dce5345db11b803b0ee36543dafd9848ba74dcf07f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:latest` - linux; amd64

```console
$ docker pull znc@sha256:0cccc12e308a5d762b9cbec014d5472450096302610abdceff1542d7a1621280
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150970876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ab11ca8f6374fc1adc2dc533e83e5e048b94095d9b0ed356a5608341d71053`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 17:49:00 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Thu, 01 Apr 2021 17:49:00 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Thu, 01 Apr 2021 17:49:01 GMT
ARG MAKEFLAGS=
# Thu, 01 Apr 2021 17:49:01 GMT
ENV ZNC_VERSION=1.8.2
# Thu, 01 Apr 2021 17:52:47 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Thu, 01 Apr 2021 17:52:47 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
VOLUME [/znc-data]
# Thu, 01 Apr 2021 17:52:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 17:53:03 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Thu, 01 Apr 2021 17:53:03 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1103d376d29954cff3fea6de5480826bc263f3888c64bc57dab67a4ef9cdea`  
		Last Modified: Thu, 01 Apr 2021 17:53:29 GMT  
		Size: 44.8 MB (44792653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc40e0a135454655217450977447b9282013e0751f0434a0001f45292f5497cd`  
		Last Modified: Thu, 01 Apr 2021 17:53:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857bfaea68a2cbe5b808fa821d0ccb1d361c3758d3df34a2366f0b4cb72f8681`  
		Last Modified: Thu, 01 Apr 2021 17:53:19 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f942297ef7eb757f7f04ece23aca503f6f7db401b6d0a55f97f6f6a6463200d1`  
		Last Modified: Thu, 01 Apr 2021 17:53:20 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2634923c8781f93aa89d896f3e6e81eb52b7270c9a910b6848a64ab2af3631a9`  
		Last Modified: Thu, 01 Apr 2021 17:53:18 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eb40a55b0d76878ebe44114be2eccb1346cc6bbf4f56b0f5364a38049f4004`  
		Last Modified: Thu, 01 Apr 2021 17:53:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9988bb148379af77a0e3d6cff7a5b17b96fe6fc365ce48a4b7117686675023`  
		Last Modified: Thu, 01 Apr 2021 17:54:02 GMT  
		Size: 103.4 MB (103376759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae11985415ffff5fdf6801187aec20092b9a1a9430ab364ea11473759970d99`  
		Last Modified: Thu, 01 Apr 2021 17:53:44 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:637262cf7726596493c9e1b36319cadee4df531ad169e2ab193bfa5c793c606a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132687454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db254ececf401d0f7db47f515c435b080eeccf382db2085cedd9b4df8336259c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:06:24 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 14 Apr 2021 19:06:25 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 14 Apr 2021 19:06:26 GMT
ARG MAKEFLAGS=
# Wed, 14 Apr 2021 19:06:27 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 14 Apr 2021 19:14:38 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 14 Apr 2021 19:14:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 14 Apr 2021 19:14:41 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:42 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:43 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:44 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:45 GMT
VOLUME [/znc-data]
# Wed, 14 Apr 2021 19:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Apr 2021 19:15:07 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Wed, 14 Apr 2021 19:15:10 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a7c2bb5435b1fa5a12ae177d982fedb637c06223b2c701cb90ecd09de64929`  
		Last Modified: Wed, 14 Apr 2021 19:15:45 GMT  
		Size: 43.0 MB (43047705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174b893fee9110b0d361ce6ac762b55def7e783e102df78cfa7de76273c474c2`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cd01900ad296ad09f6b29dc0dbf821432761b6b9771daddbe9077e2ac7bede`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4852ba58f3351dc50f648ff54754f3143c4bc73aff353c8fc44f1ca4b2727e1b`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e2bd3ffa516127012f7dd673a572cff0cc0b3a53555d987507a3f0e697e70d`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc133d3eda0b1cbf3ee429aa42a8babe168097f3490aff7e11bf216e2200ff9`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6f9dc0fc71449c9d6aa086257cdeeccd8c2b27bc1d0912041ec74b9acd1e76`  
		Last Modified: Wed, 14 Apr 2021 19:16:23 GMT  
		Size: 87.0 MB (87032736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773f8f7b9621c6f9898eccd6e54c2229ef68db2240332907412d1c0e7a7bb167`  
		Last Modified: Wed, 14 Apr 2021 19:15:56 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:0a733b42166ea183134133b15d3eb864698e431e36b0b3cec35b03d435e2db5d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138119446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4eeffdf302195ad59ce285311e54882c7431f33635a3bad1164497c7b8243c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:48 GMT
ADD file:dd1db8a59e36aac513488fa97629360c665b6079fb7c6b3cd09065ef993f6675 in / 
# Wed, 31 Mar 2021 17:21:50 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 16:25:22 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Thu, 01 Apr 2021 16:25:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Thu, 01 Apr 2021 16:25:24 GMT
ARG MAKEFLAGS=
# Thu, 01 Apr 2021 16:25:24 GMT
ENV ZNC_VERSION=1.8.2
# Thu, 01 Apr 2021 16:33:35 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Thu, 01 Apr 2021 16:33:37 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Thu, 01 Apr 2021 16:33:38 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:39 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:40 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:41 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:42 GMT
VOLUME [/znc-data]
# Thu, 01 Apr 2021 16:33:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 16:34:13 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         libressl-dev         perl         python3
# Thu, 01 Apr 2021 16:34:16 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:9a219e8acc52b4071b6121a1e4d4ecbce48f38113fbbcfe026c26768ce76bcc0`  
		Last Modified: Wed, 31 Mar 2021 17:22:52 GMT  
		Size: 2.7 MB (2709852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b4a14ad4a95a93c1ec49befe5db8a6c134ef9f688ef91a8a893fcd71f28295`  
		Last Modified: Thu, 01 Apr 2021 16:34:46 GMT  
		Size: 44.6 MB (44634326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecd51a9f27e0a81e979cd79a8c85b9d28404be2276e1fa575ad2b04a45f632d`  
		Last Modified: Thu, 01 Apr 2021 16:34:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6124bb532c242c74f7cfc2997c96d310c1c795fbd1d60db99e23e5979853c0`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c215a41a50553b36c36bb621700ed53bb792aa6fa6c6f8de650bb5283aebd636`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b90612607d4d3ff34f3f99c13cfb3fae6b62f2bc2e16653a33da1648a98099`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4139ba013ae04e155d31c48860248aa044aeaf79d2c14c0ccc788a19da8b24`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4df986b08a57d06eb4aec4f3dad35e381dccabb8e383efdfb6110ef696758a`  
		Last Modified: Thu, 01 Apr 2021 16:35:28 GMT  
		Size: 90.8 MB (90773511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edefd45ea576487b4729c1f530f7a62473c0784a020035e7c492be0d2db78f33`  
		Last Modified: Thu, 01 Apr 2021 16:35:00 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:slim`

```console
$ docker pull znc@sha256:d76170ef7fd803fd9c72eacd7fa9c166c9172396b8f3ddc265b5024c45454b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:slim` - linux; amd64

```console
$ docker pull znc@sha256:f6b4ab358a44c0bbd15e36b434fe7d258be74b9766055c965816fffd3624b387
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47593787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9ffdec9a24c864640b5e25ed19f26464c206b5423df96aaed62ccd4becaea5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 17:49:00 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Thu, 01 Apr 2021 17:49:00 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Thu, 01 Apr 2021 17:49:01 GMT
ARG MAKEFLAGS=
# Thu, 01 Apr 2021 17:49:01 GMT
ENV ZNC_VERSION=1.8.2
# Thu, 01 Apr 2021 17:52:47 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Thu, 01 Apr 2021 17:52:47 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Thu, 01 Apr 2021 17:52:48 GMT
VOLUME [/znc-data]
# Thu, 01 Apr 2021 17:52:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1103d376d29954cff3fea6de5480826bc263f3888c64bc57dab67a4ef9cdea`  
		Last Modified: Thu, 01 Apr 2021 17:53:29 GMT  
		Size: 44.8 MB (44792653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc40e0a135454655217450977447b9282013e0751f0434a0001f45292f5497cd`  
		Last Modified: Thu, 01 Apr 2021 17:53:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857bfaea68a2cbe5b808fa821d0ccb1d361c3758d3df34a2366f0b4cb72f8681`  
		Last Modified: Thu, 01 Apr 2021 17:53:19 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f942297ef7eb757f7f04ece23aca503f6f7db401b6d0a55f97f6f6a6463200d1`  
		Last Modified: Thu, 01 Apr 2021 17:53:20 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2634923c8781f93aa89d896f3e6e81eb52b7270c9a910b6848a64ab2af3631a9`  
		Last Modified: Thu, 01 Apr 2021 17:53:18 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eb40a55b0d76878ebe44114be2eccb1346cc6bbf4f56b0f5364a38049f4004`  
		Last Modified: Thu, 01 Apr 2021 17:53:20 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:9b761b1992bdda212d16af7b3b2d0d468764d161c88035178ac474f7537a0eb9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2ff69e5ce11a914848b667be0bf0a31b595738cc67565d230d38f15915d641`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:06:24 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 14 Apr 2021 19:06:25 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 14 Apr 2021 19:06:26 GMT
ARG MAKEFLAGS=
# Wed, 14 Apr 2021 19:06:27 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 14 Apr 2021 19:14:38 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 14 Apr 2021 19:14:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 14 Apr 2021 19:14:41 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:42 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:43 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:44 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Wed, 14 Apr 2021 19:14:45 GMT
VOLUME [/znc-data]
# Wed, 14 Apr 2021 19:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a7c2bb5435b1fa5a12ae177d982fedb637c06223b2c701cb90ecd09de64929`  
		Last Modified: Wed, 14 Apr 2021 19:15:45 GMT  
		Size: 43.0 MB (43047705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174b893fee9110b0d361ce6ac762b55def7e783e102df78cfa7de76273c474c2`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cd01900ad296ad09f6b29dc0dbf821432761b6b9771daddbe9077e2ac7bede`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4852ba58f3351dc50f648ff54754f3143c4bc73aff353c8fc44f1ca4b2727e1b`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e2bd3ffa516127012f7dd673a572cff0cc0b3a53555d987507a3f0e697e70d`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc133d3eda0b1cbf3ee429aa42a8babe168097f3490aff7e11bf216e2200ff9`  
		Last Modified: Wed, 14 Apr 2021 19:15:28 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:ab0377ddda004ac1e00e310d647774727609814961c5802d587578350592bedd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47345602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90b74d05978dcb1995981bd235bac3d679307b809f82390897cdad29afc6604`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:48 GMT
ADD file:dd1db8a59e36aac513488fa97629360c665b6079fb7c6b3cd09065ef993f6675 in / 
# Wed, 31 Mar 2021 17:21:50 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 16:25:22 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Thu, 01 Apr 2021 16:25:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Thu, 01 Apr 2021 16:25:24 GMT
ARG MAKEFLAGS=
# Thu, 01 Apr 2021 16:25:24 GMT
ENV ZNC_VERSION=1.8.2
# Thu, 01 Apr 2021 16:33:35 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         libressl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         libressl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Thu, 01 Apr 2021 16:33:37 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Thu, 01 Apr 2021 16:33:38 GMT
COPY file:dfda6761eff5635f2f7a6c1d540b2b14ea67514867578d12226629a780844185 in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:39 GMT
COPY file:809dccdc6a2a9f5e2a058644d9f71b2f167ab0f237913902896fef13b6315814 in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:40 GMT
COPY file:84986dd2ebc690804b4c47eb72d1af3a52ba257c76202478879604756431ff5c in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:41 GMT
COPY file:50e035ea8915a4bc88fd57c8f79152224f23e0c4c4b68ea8469294aedbddd039 in /startup-sequence/ 
# Thu, 01 Apr 2021 16:33:42 GMT
VOLUME [/znc-data]
# Thu, 01 Apr 2021 16:33:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9a219e8acc52b4071b6121a1e4d4ecbce48f38113fbbcfe026c26768ce76bcc0`  
		Last Modified: Wed, 31 Mar 2021 17:22:52 GMT  
		Size: 2.7 MB (2709852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b4a14ad4a95a93c1ec49befe5db8a6c134ef9f688ef91a8a893fcd71f28295`  
		Last Modified: Thu, 01 Apr 2021 16:34:46 GMT  
		Size: 44.6 MB (44634326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecd51a9f27e0a81e979cd79a8c85b9d28404be2276e1fa575ad2b04a45f632d`  
		Last Modified: Thu, 01 Apr 2021 16:34:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6124bb532c242c74f7cfc2997c96d310c1c795fbd1d60db99e23e5979853c0`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 304.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c215a41a50553b36c36bb621700ed53bb792aa6fa6c6f8de650bb5283aebd636`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b90612607d4d3ff34f3f99c13cfb3fae6b62f2bc2e16653a33da1648a98099`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4139ba013ae04e155d31c48860248aa044aeaf79d2c14c0ccc788a19da8b24`  
		Last Modified: Thu, 01 Apr 2021 16:34:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
