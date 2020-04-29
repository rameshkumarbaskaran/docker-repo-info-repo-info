## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:e85ed451f30167a2163809ce35270f82f711f53f487ef479092f36a0f166f4b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:7582bde23313a17fe3f6c1959b46bbc3622432a8780530c2c4a2d7f5816e70df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32447489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad4d6fbb74669b5b30726c2d599070fa83ba4868e262437469085efb6b3a0ea`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Wed, 29 Apr 2020 02:47:29 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Wed, 29 Apr 2020 02:47:29 GMT
ARG rakudo_version=2020.01
# Wed, 29 Apr 2020 02:47:29 GMT
ENV rakudo_version=2020.01
# Wed, 29 Apr 2020 03:11:59 GMT
RUN buildDeps='         gnupg         perl         perl-encode         gcc         libc-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apk del .build-deps
# Wed, 29 Apr 2020 03:11:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Wed, 29 Apr 2020 03:11:59 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1309bc98d8d6bdf032bd788330f6a9b9829fae2ad0f22bfb0c70ccaa8cfa1f`  
		Last Modified: Wed, 29 Apr 2020 03:12:25 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ea977c03cd2ea114dada822df05948d13976d63d5f6c534a493927a71e64a8`  
		Last Modified: Wed, 29 Apr 2020 03:12:35 GMT  
		Size: 29.7 MB (29650653 bytes)  
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
