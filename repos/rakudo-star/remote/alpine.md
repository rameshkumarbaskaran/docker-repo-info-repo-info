## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:701a8429edbec4d2075e303198a450e251004b56db808449ce3d0f9f6fa22397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:b15e93d85b042ff1edbeb2991957eb1511db3dbb5a81a518b8c2fcaa0f8aa483
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30054034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a272458d9eccb35ca3b03d8f9e3a84f145a3eb483c9fd00ef273afdfa5b7e9`
-	Default Command: `["perl6"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 16:45:11 GMT
RUN addgroup -S perl6 && adduser -S perl6 -G perl6
# Fri, 24 Apr 2020 16:45:11 GMT
ARG rakudo_version=2019.03
# Fri, 24 Apr 2020 16:45:11 GMT
ENV rakudo_version=2019.03
# Fri, 24 Apr 2020 17:02:13 GMT
RUN buildDeps='         gnupg         perl         perl-encode         gcc         libc-dev         make     '         url="https://rakudostar.com/files/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apk del .build-deps
# Fri, 24 Apr 2020 17:02:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Fri, 24 Apr 2020 17:02:14 GMT
CMD ["perl6"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7042ee37afa2192c2d0a0b305dfabaf184dacb621adee078904c9e78ca592c58`  
		Last Modified: Fri, 24 Apr 2020 17:02:31 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e862742ec50cac92c806c64ea4cf7c41e1ad8ca3895da9f5145b115559bbb2e3`  
		Last Modified: Fri, 24 Apr 2020 17:02:37 GMT  
		Size: 27.3 MB (27257196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:34841b8c9668d35628597a4da051522dbda2ed4831efe64205280c15a1c71633
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29776589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235d3c53343db51e99a8b82d44c7e94b5dc40a52413dad480611bf52f06dbe37`
-	Default Command: `["perl6"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:52 GMT
ADD file:75529f7e83edb6d0457a3b8bbfe33d4e3a12f339c5ace517d0f52dbedd9a146b in / 
# Fri, 24 Apr 2020 00:14:53 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 11:32:29 GMT
RUN addgroup -S perl6 && adduser -S perl6 -G perl6
# Fri, 24 Apr 2020 11:32:29 GMT
ARG rakudo_version=2019.03
# Fri, 24 Apr 2020 11:32:31 GMT
ENV rakudo_version=2019.03
# Fri, 24 Apr 2020 12:09:14 GMT
RUN buildDeps='         gnupg         perl         perl-encode         gcc         libc-dev         make     '         url="https://rakudostar.com/files/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apk del .build-deps
# Fri, 24 Apr 2020 12:09:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Fri, 24 Apr 2020 12:09:17 GMT
CMD ["perl6"]
```

-	Layers:
	-	`sha256:b038bcb63e9c8905cc879c957302f686a9b43f24a18dcfc4186ab236ddf04cad`  
		Last Modified: Fri, 24 Apr 2020 00:15:54 GMT  
		Size: 2.7 MB (2718734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69d6710ca1b98ac4cfcb667f1d9dea827f2c2444bea5cf10fd2af03517a1b74`  
		Last Modified: Fri, 24 Apr 2020 12:09:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f397d48d5416d526560ad61a55d85db1f049a3b221f3e865085c934dbb85f`  
		Last Modified: Fri, 24 Apr 2020 12:09:48 GMT  
		Size: 27.1 MB (27056569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
