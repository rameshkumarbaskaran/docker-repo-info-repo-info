## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:103d4e5c0095942e3b6a58aef5e9a5f753b8a07315a2ed551557358ab9f32107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:7e99fb5a4c0843e7be220318fe39c1204762f7038738be585f693b62a27e4cf4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44260211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e6615552a7e973ae360e0c9341ec7a36a43984c494fafe4a87d518d6fd15db`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:46 GMT
ADD file:a2ef39a587aac85256b55bee81f17d73aaa7154b2a32a31527c7803fb889f2e7 in / 
# Tue, 29 Mar 2022 00:19:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 16:27:30 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Tue, 29 Mar 2022 16:27:30 GMT
ARG rakudo_version=2021.04
# Tue, 29 Mar 2022 16:27:30 GMT
ENV rakudo_version=2021.04
# Tue, 29 Mar 2022 16:38:18 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps
# Tue, 29 Mar 2022 16:38:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 29 Mar 2022 16:38:18 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:b9c05db88786fd3c89b78787631257301391f898c03ba50553b556630046a741`  
		Last Modified: Tue, 29 Mar 2022 00:20:43 GMT  
		Size: 2.8 MB (2819223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be43853149918db3a48ec21a02aa5f36b61f20e617e3276b94ac579fde8c637c`  
		Last Modified: Tue, 29 Mar 2022 16:38:31 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e90d819e0af0890d0d0b8c18c6fba285f77c7d5d62c2c2d0d8d15fa56fd088`  
		Last Modified: Tue, 29 Mar 2022 16:38:39 GMT  
		Size: 41.4 MB (41439734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:89285bdb42fbe5a00b7bfcc1c79854ad9a5668def09c24a884808f2f77ea69e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43724021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbae01f78e6deb54b411310056ad9caf18d77351041de54c8c0d3d7a906b783`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:46 GMT
ADD file:535e6f58c2cf7520c1824c8a290dc38c5519485470ed49587748a27c0113d586 in / 
# Mon, 04 Apr 2022 23:39:46 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:53:42 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Tue, 05 Apr 2022 06:53:43 GMT
ARG rakudo_version=2021.04
# Tue, 05 Apr 2022 06:53:44 GMT
ENV rakudo_version=2021.04
# Tue, 05 Apr 2022 07:09:02 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps
# Tue, 05 Apr 2022 07:09:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 05 Apr 2022 07:09:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:edd30f0f17040c7b292e0960fa771cf3ea45f994d7a2577a14fe02ae7ce727e9`  
		Last Modified: Mon, 04 Apr 2022 23:40:51 GMT  
		Size: 2.7 MB (2720895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ca547acb27a3e0ccb1f06ea97957818c98bc358320f3de43237b95aa6cece3`  
		Last Modified: Tue, 05 Apr 2022 07:09:20 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a11e7da66aa9e1db5cda79dafa1698ba42753a5251f0d3fc738eed05696b`  
		Last Modified: Tue, 05 Apr 2022 07:09:29 GMT  
		Size: 41.0 MB (41001899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
