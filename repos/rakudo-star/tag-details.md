<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2019.03`](#rakudo-star201903)
-	[`rakudo-star:2019.03-alpine`](#rakudo-star201903-alpine)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:latest`](#rakudo-starlatest)

## `rakudo-star:2019.03`

```console
$ docker pull rakudo-star@sha256:71645467ce76559fea7036552d091b860bcd8a23f37e07198480f67aa3868a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:2019.03` - linux; amd64

```console
$ docker pull rakudo-star@sha256:940e7a0ab194ac8a394199ef9bddcbfd071271a3ffcd7ab0d0fe672f8537614b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138201712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c522d8d49d585aa5fa94bf8a5a3d72e3dfa1d143553e1a913dc835a56b3ba1`
-	Default Command: `["perl6"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:41 GMT
ADD file:8a9218592e5d736a05a1821a6dd38b205cdd8197c26a5aa33f6fc22fbfaa1c4d in / 
# Sat, 01 Feb 2020 17:23:41 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 00:33:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 00:34:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 02 Feb 2020 00:34:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 20:34:16 GMT
MAINTAINER Rob Hoelz
# Sun, 02 Feb 2020 20:34:17 GMT
RUN groupadd -r perl6 && useradd -r -g perl6 perl6
# Sun, 02 Feb 2020 20:34:17 GMT
ARG rakudo_version=2019.03
# Sun, 02 Feb 2020 20:34:18 GMT
ENV rakudo_version=2019.03
# Sun, 02 Feb 2020 20:49:51 GMT
RUN buildDeps='         gcc         libc6-dev         libencode-perl         make     '         url="https://rakudostar.com/files/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apt-get update     && apt-get --yes install --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Sun, 02 Feb 2020 20:49:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Sun, 02 Feb 2020 20:49:52 GMT
CMD ["perl6"]
```

-	Layers:
	-	`sha256:3192219afd04f93d90f0af7f89cb527d1af2a16975ea391ea8517c602ad6ddb6`  
		Last Modified: Sat, 01 Feb 2020 17:28:49 GMT  
		Size: 45.4 MB (45380658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c160265e75550c2ed099aa7d3906b3fef0bf046a2aeead136f8e587a015159`  
		Last Modified: Sun, 02 Feb 2020 00:42:04 GMT  
		Size: 10.8 MB (10797219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4fe40d0e618e3319afb689c3570bb87e8e8cf51bca080364d1552317bc66c2`  
		Last Modified: Sun, 02 Feb 2020 00:42:02 GMT  
		Size: 4.3 MB (4340216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d647f502a07e6daaee43c23cfac9399501b1d7f55fb4c60d56307e23f0ed5a5`  
		Last Modified: Sun, 02 Feb 2020 00:42:26 GMT  
		Size: 50.1 MB (50073989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a50f9d701f4346f7c03c29251980be15b01be0aeaf9f6cfd9380332655c3e16`  
		Last Modified: Sun, 02 Feb 2020 20:50:04 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c3b3e330974725772db3f8414a294ea43a99313ffe98e817b3c142e00e49a1`  
		Last Modified: Sun, 02 Feb 2020 20:50:10 GMT  
		Size: 27.6 MB (27607866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:2019.03` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:aaf2182cd9f969e295013be07257fc6bad79edd6ef4922c6e027829b0406f180
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132303361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06205f32b34eeb7c90e0c964a7f68752a3b75836ea52854a1f9b190c8ccb98b5`
-	Default Command: `["perl6"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:03 GMT
ADD file:c82c7dc82c2eb3b50218c35e1b848f707b134d2df957f57125408f69aaeb9b96 in / 
# Wed, 26 Feb 2020 00:50:15 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:59:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:59:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 23:11:41 GMT
MAINTAINER Rob Hoelz
# Wed, 26 Feb 2020 23:11:42 GMT
RUN groupadd -r perl6 && useradd -r -g perl6 perl6
# Wed, 26 Feb 2020 23:11:43 GMT
ARG rakudo_version=2019.03
# Wed, 26 Feb 2020 23:11:44 GMT
ENV rakudo_version=2019.03
# Wed, 26 Feb 2020 23:45:46 GMT
RUN buildDeps='         gcc         libc6-dev         libencode-perl         make     '         url="https://rakudostar.com/files/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apt-get update     && apt-get --yes install --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Wed, 26 Feb 2020 23:45:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Wed, 26 Feb 2020 23:45:48 GMT
CMD ["perl6"]
```

-	Layers:
	-	`sha256:668c278237ef972312df4979c8fb1a927b38db5da09f094ae4fcc84a061dedf8`  
		Last Modified: Wed, 26 Feb 2020 00:58:30 GMT  
		Size: 43.2 MB (43158146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b41cac09012800692bd13a1238260bfb293c18c7864536c494809f2983ad770`  
		Last Modified: Wed, 26 Feb 2020 04:08:32 GMT  
		Size: 9.7 MB (9748511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b353938273b0bbc576a8a80a232614ca2d9bfe48769641eee7055f3db6a5e`  
		Last Modified: Wed, 26 Feb 2020 04:08:31 GMT  
		Size: 4.1 MB (4094435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fba2538bf9e06bc84462d53d1effc13ecb38f026a6bc0df91cb9da3ffc0fb1`  
		Last Modified: Wed, 26 Feb 2020 04:08:53 GMT  
		Size: 48.0 MB (48024341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b0a29b6a44242e9ab4c883b2890ba5bf018c1f18f0578b7141f45c303d8c76`  
		Last Modified: Wed, 26 Feb 2020 23:46:04 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f5fb1f0820c319aa04ce54511e44371baf9a847ed4dd88de1e132f48374200`  
		Last Modified: Wed, 26 Feb 2020 23:46:15 GMT  
		Size: 27.3 MB (27276165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rakudo-star:2019.03-alpine`

```console
$ docker pull rakudo-star@sha256:5f04312a8e5805414aee67ddc4e61fd9ac3bccd9f68635410994dbbd16dee3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:2019.03-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:f455ce97de76478b475915eec6015157f91de4f8dd460efaee855bfa6abd6452
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30053992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae6daca675b8efb6ebf8eb66736153b061e05b70fa06c98452183afb7d98e71`
-	Default Command: `["perl6"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:19:53 GMT
RUN addgroup -S perl6 && adduser -S perl6 -G perl6
# Thu, 23 Jan 2020 22:19:53 GMT
ARG rakudo_version=2019.03
# Thu, 23 Jan 2020 22:19:53 GMT
ENV rakudo_version=2019.03
# Thu, 23 Jan 2020 22:42:29 GMT
RUN buildDeps='         gnupg         perl         perl-encode         gcc         libc-dev         make     '         url="https://rakudostar.com/files/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apk del .build-deps
# Thu, 23 Jan 2020 22:42:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Thu, 23 Jan 2020 22:42:29 GMT
CMD ["perl6"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd1b886c5caeb9c93e822b4e5d00d482308c2da8170e1fba4668dae85670843`  
		Last Modified: Thu, 23 Jan 2020 22:42:41 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ec5e1f0e6dd884dfb59272800d2d689125b3b40246cefa48b1ef0018b5b752`  
		Last Modified: Thu, 23 Jan 2020 22:43:03 GMT  
		Size: 27.3 MB (27265770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:2019.03-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:04d70f918da5d405ebe3cbc0d1a027d1e71c0bab07d76bf69c1fad978c90e2a7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 MB (29610759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759165c83e3b8566c465cd83c1e5eb0931b32a9b71b9bcf152d440df1f19bcee`
-	Default Command: `["perl6"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:39 GMT
ADD file:bdfbd4b0dfb53eecc80bac65894d1e2fcfafb27dcf24ab019176e2c9f60b9a39 in / 
# Thu, 23 Jan 2020 16:54:40 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:23:24 GMT
RUN addgroup -S perl6 && adduser -S perl6 -G perl6
# Thu, 23 Jan 2020 22:23:24 GMT
ARG rakudo_version=2019.03
# Thu, 23 Jan 2020 22:23:25 GMT
ENV rakudo_version=2019.03
# Thu, 23 Jan 2020 23:00:31 GMT
RUN buildDeps='         gnupg         perl         perl-encode         gcc         libc-dev         make     '         url="https://rakudostar.com/files/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apk del .build-deps
# Thu, 23 Jan 2020 23:00:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Thu, 23 Jan 2020 23:00:36 GMT
CMD ["perl6"]
```

-	Layers:
	-	`sha256:f07e4bcf42b862c240f4c00f2f7ed362d7d93ca15151de547beda593f3b669e5`  
		Last Modified: Thu, 23 Jan 2020 16:55:24 GMT  
		Size: 2.7 MB (2717732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f1177d01116b50429bddd1a67f102e1267c9a241e437f07bcf06a8bef85092`  
		Last Modified: Thu, 23 Jan 2020 23:00:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b6b0cda86e0b249946b6e684d6e31b3780d49932c1360129c3b693316bfad9`  
		Last Modified: Thu, 23 Jan 2020 23:00:58 GMT  
		Size: 26.9 MB (26891740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:5f04312a8e5805414aee67ddc4e61fd9ac3bccd9f68635410994dbbd16dee3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:f455ce97de76478b475915eec6015157f91de4f8dd460efaee855bfa6abd6452
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30053992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae6daca675b8efb6ebf8eb66736153b061e05b70fa06c98452183afb7d98e71`
-	Default Command: `["perl6"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:19:53 GMT
RUN addgroup -S perl6 && adduser -S perl6 -G perl6
# Thu, 23 Jan 2020 22:19:53 GMT
ARG rakudo_version=2019.03
# Thu, 23 Jan 2020 22:19:53 GMT
ENV rakudo_version=2019.03
# Thu, 23 Jan 2020 22:42:29 GMT
RUN buildDeps='         gnupg         perl         perl-encode         gcc         libc-dev         make     '         url="https://rakudostar.com/files/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apk del .build-deps
# Thu, 23 Jan 2020 22:42:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Thu, 23 Jan 2020 22:42:29 GMT
CMD ["perl6"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd1b886c5caeb9c93e822b4e5d00d482308c2da8170e1fba4668dae85670843`  
		Last Modified: Thu, 23 Jan 2020 22:42:41 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ec5e1f0e6dd884dfb59272800d2d689125b3b40246cefa48b1ef0018b5b752`  
		Last Modified: Thu, 23 Jan 2020 22:43:03 GMT  
		Size: 27.3 MB (27265770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:04d70f918da5d405ebe3cbc0d1a027d1e71c0bab07d76bf69c1fad978c90e2a7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 MB (29610759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759165c83e3b8566c465cd83c1e5eb0931b32a9b71b9bcf152d440df1f19bcee`
-	Default Command: `["perl6"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:39 GMT
ADD file:bdfbd4b0dfb53eecc80bac65894d1e2fcfafb27dcf24ab019176e2c9f60b9a39 in / 
# Thu, 23 Jan 2020 16:54:40 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:23:24 GMT
RUN addgroup -S perl6 && adduser -S perl6 -G perl6
# Thu, 23 Jan 2020 22:23:24 GMT
ARG rakudo_version=2019.03
# Thu, 23 Jan 2020 22:23:25 GMT
ENV rakudo_version=2019.03
# Thu, 23 Jan 2020 23:00:31 GMT
RUN buildDeps='         gnupg         perl         perl-encode         gcc         libc-dev         make     '         url="https://rakudostar.com/files/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apk del .build-deps
# Thu, 23 Jan 2020 23:00:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Thu, 23 Jan 2020 23:00:36 GMT
CMD ["perl6"]
```

-	Layers:
	-	`sha256:f07e4bcf42b862c240f4c00f2f7ed362d7d93ca15151de547beda593f3b669e5`  
		Last Modified: Thu, 23 Jan 2020 16:55:24 GMT  
		Size: 2.7 MB (2717732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f1177d01116b50429bddd1a67f102e1267c9a241e437f07bcf06a8bef85092`  
		Last Modified: Thu, 23 Jan 2020 23:00:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b6b0cda86e0b249946b6e684d6e31b3780d49932c1360129c3b693316bfad9`  
		Last Modified: Thu, 23 Jan 2020 23:00:58 GMT  
		Size: 26.9 MB (26891740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:71645467ce76559fea7036552d091b860bcd8a23f37e07198480f67aa3868a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:940e7a0ab194ac8a394199ef9bddcbfd071271a3ffcd7ab0d0fe672f8537614b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138201712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c522d8d49d585aa5fa94bf8a5a3d72e3dfa1d143553e1a913dc835a56b3ba1`
-	Default Command: `["perl6"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:41 GMT
ADD file:8a9218592e5d736a05a1821a6dd38b205cdd8197c26a5aa33f6fc22fbfaa1c4d in / 
# Sat, 01 Feb 2020 17:23:41 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 00:33:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 00:34:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 02 Feb 2020 00:34:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 20:34:16 GMT
MAINTAINER Rob Hoelz
# Sun, 02 Feb 2020 20:34:17 GMT
RUN groupadd -r perl6 && useradd -r -g perl6 perl6
# Sun, 02 Feb 2020 20:34:17 GMT
ARG rakudo_version=2019.03
# Sun, 02 Feb 2020 20:34:18 GMT
ENV rakudo_version=2019.03
# Sun, 02 Feb 2020 20:49:51 GMT
RUN buildDeps='         gcc         libc6-dev         libencode-perl         make     '         url="https://rakudostar.com/files/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apt-get update     && apt-get --yes install --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Sun, 02 Feb 2020 20:49:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Sun, 02 Feb 2020 20:49:52 GMT
CMD ["perl6"]
```

-	Layers:
	-	`sha256:3192219afd04f93d90f0af7f89cb527d1af2a16975ea391ea8517c602ad6ddb6`  
		Last Modified: Sat, 01 Feb 2020 17:28:49 GMT  
		Size: 45.4 MB (45380658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c160265e75550c2ed099aa7d3906b3fef0bf046a2aeead136f8e587a015159`  
		Last Modified: Sun, 02 Feb 2020 00:42:04 GMT  
		Size: 10.8 MB (10797219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4fe40d0e618e3319afb689c3570bb87e8e8cf51bca080364d1552317bc66c2`  
		Last Modified: Sun, 02 Feb 2020 00:42:02 GMT  
		Size: 4.3 MB (4340216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d647f502a07e6daaee43c23cfac9399501b1d7f55fb4c60d56307e23f0ed5a5`  
		Last Modified: Sun, 02 Feb 2020 00:42:26 GMT  
		Size: 50.1 MB (50073989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a50f9d701f4346f7c03c29251980be15b01be0aeaf9f6cfd9380332655c3e16`  
		Last Modified: Sun, 02 Feb 2020 20:50:04 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c3b3e330974725772db3f8414a294ea43a99313ffe98e817b3c142e00e49a1`  
		Last Modified: Sun, 02 Feb 2020 20:50:10 GMT  
		Size: 27.6 MB (27607866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:aaf2182cd9f969e295013be07257fc6bad79edd6ef4922c6e027829b0406f180
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132303361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06205f32b34eeb7c90e0c964a7f68752a3b75836ea52854a1f9b190c8ccb98b5`
-	Default Command: `["perl6"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:03 GMT
ADD file:c82c7dc82c2eb3b50218c35e1b848f707b134d2df957f57125408f69aaeb9b96 in / 
# Wed, 26 Feb 2020 00:50:15 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:59:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:59:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 23:11:41 GMT
MAINTAINER Rob Hoelz
# Wed, 26 Feb 2020 23:11:42 GMT
RUN groupadd -r perl6 && useradd -r -g perl6 perl6
# Wed, 26 Feb 2020 23:11:43 GMT
ARG rakudo_version=2019.03
# Wed, 26 Feb 2020 23:11:44 GMT
ENV rakudo_version=2019.03
# Wed, 26 Feb 2020 23:45:46 GMT
RUN buildDeps='         gcc         libc6-dev         libencode-perl         make     '         url="https://rakudostar.com/files/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apt-get update     && apt-get --yes install --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Wed, 26 Feb 2020 23:45:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Wed, 26 Feb 2020 23:45:48 GMT
CMD ["perl6"]
```

-	Layers:
	-	`sha256:668c278237ef972312df4979c8fb1a927b38db5da09f094ae4fcc84a061dedf8`  
		Last Modified: Wed, 26 Feb 2020 00:58:30 GMT  
		Size: 43.2 MB (43158146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b41cac09012800692bd13a1238260bfb293c18c7864536c494809f2983ad770`  
		Last Modified: Wed, 26 Feb 2020 04:08:32 GMT  
		Size: 9.7 MB (9748511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b353938273b0bbc576a8a80a232614ca2d9bfe48769641eee7055f3db6a5e`  
		Last Modified: Wed, 26 Feb 2020 04:08:31 GMT  
		Size: 4.1 MB (4094435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fba2538bf9e06bc84462d53d1effc13ecb38f026a6bc0df91cb9da3ffc0fb1`  
		Last Modified: Wed, 26 Feb 2020 04:08:53 GMT  
		Size: 48.0 MB (48024341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b0a29b6a44242e9ab4c883b2890ba5bf018c1f18f0578b7141f45c303d8c76`  
		Last Modified: Wed, 26 Feb 2020 23:46:04 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f5fb1f0820c319aa04ce54511e44371baf9a847ed4dd88de1e132f48374200`  
		Last Modified: Wed, 26 Feb 2020 23:46:15 GMT  
		Size: 27.3 MB (27276165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
