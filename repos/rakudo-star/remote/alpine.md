## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:331083d67ca8fc94e055e07a9deb6d262773921d67e5c6d6817f6283e2ef0422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:c17ac60cf1290709c4ccb21feda593b45155334f4f59c7e86b9b092640297675
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42507438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c964effe58208e8e8b7e3a6157951b4dd9ea095771b54da1e8c133df5e17a9d`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Sat, 13 Mar 2021 10:24:46 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Sat, 13 Mar 2021 10:24:47 GMT
ARG rakudo_version=2020.10
# Sat, 13 Mar 2021 10:24:47 GMT
ENV rakudo_version=2020.10
# Sat, 13 Mar 2021 10:34:16 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps
# Sat, 13 Mar 2021 10:34:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Sat, 13 Mar 2021 10:34:17 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88861232df65fd2bd79ca50d1cada6fc417dd5f2afa11cc9c72d1d4c72870f86`  
		Last Modified: Sat, 13 Mar 2021 10:34:57 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4977f0f71fc330d52d468848ac2b8b121b5b2cbb0f995f30fb5a8adf8eb0f702`  
		Last Modified: Sat, 13 Mar 2021 10:35:05 GMT  
		Size: 39.7 MB (39706685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f941ddd6b80f37f038bb134802ffc4785b137647d7e6676bde74148e93cc7852
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42209149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f974c57aa0a942e8494df54917a4df0da6196347d0b020acebf5bda8c0d3f7`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:39 GMT
ADD file:7e82858ef85f6db90c131ed835a390d736cfdbd1a0cf8bccaeed8f7e30172ddb in / 
# Wed, 24 Feb 2021 20:39:40 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 03:50:21 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Thu, 25 Feb 2021 03:50:22 GMT
ARG rakudo_version=2020.10
# Thu, 25 Feb 2021 03:50:23 GMT
ENV rakudo_version=2020.10
# Thu, 25 Feb 2021 04:12:09 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps
# Thu, 25 Feb 2021 04:12:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 25 Feb 2021 04:12:13 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:dce8679b510e95d136241d02ababff86469dd14220812a7ce9202833c0e32f66`  
		Last Modified: Wed, 24 Feb 2021 20:40:26 GMT  
		Size: 2.7 MB (2709880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d993b24eb35af28a879ac677d518272f14fabd25f35cb82b5be875ec8e86f4`  
		Last Modified: Thu, 25 Feb 2021 04:12:26 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70117a8bc8f66a4d5241d1371fc25ab608fab9c49688e61208c134675b687937`  
		Last Modified: Thu, 25 Feb 2021 04:12:42 GMT  
		Size: 39.5 MB (39498013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
