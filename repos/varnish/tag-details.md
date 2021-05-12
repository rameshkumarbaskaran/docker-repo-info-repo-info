<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6`](#varnish6)
-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.7`](#varnish607)
-	[`varnish:6.0.7-1`](#varnish607-1)
-	[`varnish:6.6`](#varnish66)
-	[`varnish:6.6.0`](#varnish660)
-	[`varnish:6.6.0-1`](#varnish660-1)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:stable`](#varnishstable)

## `varnish:6`

```console
$ docker pull varnish@sha256:5b41623edd338ef6bb3b456fdfb79a1b60aba64d6d07b9ca5daeb2210f2dc03c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6` - linux; amd64

```console
$ docker pull varnish@sha256:6c62ea95b142a9edc53f1ded46db96e5f20545c45d0229c922ac63369bf53a29
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77066494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30e85f5f69a863438e951dee58348e40e869baf7f39fd8383af29ec4133b679`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 14:43:33 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Wed, 12 May 2021 14:43:34 GMT
ENV VARNISH_SIZE=100M
# Wed, 12 May 2021 14:44:03 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 14:44:04 GMT
WORKDIR /etc/varnish
# Wed, 12 May 2021 14:44:04 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 12 May 2021 14:44:05 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 12 May 2021 14:44:05 GMT
EXPOSE 80 8443
# Wed, 12 May 2021 14:44:05 GMT
CMD []
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224ea214330d2e152e48627cea86bd9428d64d20c1f8849f762cb47bfa9bdf56`  
		Last Modified: Wed, 12 May 2021 14:44:57 GMT  
		Size: 49.9 MB (49919878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0344adcc19d810ad7826bcf920f21337390c5bab0ca7dea8cc5aac8e88c6c8`  
		Last Modified: Wed, 12 May 2021 14:44:49 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0`

```console
$ docker pull varnish@sha256:cbb313ec5f23e267f4a9f799932a7bf7cb09b3ca4ad4d78eedd028428fc166a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:1b4e10411daa864617852eff5c7e82600c7cf77210b843fe6c96eb4b274bab20
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76482037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ea4085b4075a9050244ec84214287054281eac6f5fee664ee539426173c81d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 14:42:57 GMT
ENV VARNISH_VERSION=6.0.7-1~buster
# Wed, 12 May 2021 14:42:57 GMT
ENV VARNISH_SIZE=100M
# Wed, 12 May 2021 14:43:25 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 14:43:26 GMT
WORKDIR /etc/varnish
# Wed, 12 May 2021 14:43:26 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 12 May 2021 14:43:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 12 May 2021 14:43:26 GMT
EXPOSE 80 8443
# Wed, 12 May 2021 14:43:27 GMT
CMD []
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0975279306aa45296101bef5ac10167461aa640b37718358c961e584fde6fe14`  
		Last Modified: Wed, 12 May 2021 14:44:33 GMT  
		Size: 49.3 MB (49335423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4329d731c9b4d5a6558c7c08f4d08d036a75a4114d3207d169d7a6020fa59a0b`  
		Last Modified: Wed, 12 May 2021 14:44:25 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.7`

```console
$ docker pull varnish@sha256:cbb313ec5f23e267f4a9f799932a7bf7cb09b3ca4ad4d78eedd028428fc166a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0.7` - linux; amd64

```console
$ docker pull varnish@sha256:1b4e10411daa864617852eff5c7e82600c7cf77210b843fe6c96eb4b274bab20
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76482037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ea4085b4075a9050244ec84214287054281eac6f5fee664ee539426173c81d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 14:42:57 GMT
ENV VARNISH_VERSION=6.0.7-1~buster
# Wed, 12 May 2021 14:42:57 GMT
ENV VARNISH_SIZE=100M
# Wed, 12 May 2021 14:43:25 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 14:43:26 GMT
WORKDIR /etc/varnish
# Wed, 12 May 2021 14:43:26 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 12 May 2021 14:43:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 12 May 2021 14:43:26 GMT
EXPOSE 80 8443
# Wed, 12 May 2021 14:43:27 GMT
CMD []
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0975279306aa45296101bef5ac10167461aa640b37718358c961e584fde6fe14`  
		Last Modified: Wed, 12 May 2021 14:44:33 GMT  
		Size: 49.3 MB (49335423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4329d731c9b4d5a6558c7c08f4d08d036a75a4114d3207d169d7a6020fa59a0b`  
		Last Modified: Wed, 12 May 2021 14:44:25 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.7-1`

```console
$ docker pull varnish@sha256:cbb313ec5f23e267f4a9f799932a7bf7cb09b3ca4ad4d78eedd028428fc166a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0.7-1` - linux; amd64

```console
$ docker pull varnish@sha256:1b4e10411daa864617852eff5c7e82600c7cf77210b843fe6c96eb4b274bab20
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76482037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ea4085b4075a9050244ec84214287054281eac6f5fee664ee539426173c81d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 14:42:57 GMT
ENV VARNISH_VERSION=6.0.7-1~buster
# Wed, 12 May 2021 14:42:57 GMT
ENV VARNISH_SIZE=100M
# Wed, 12 May 2021 14:43:25 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 14:43:26 GMT
WORKDIR /etc/varnish
# Wed, 12 May 2021 14:43:26 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 12 May 2021 14:43:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 12 May 2021 14:43:26 GMT
EXPOSE 80 8443
# Wed, 12 May 2021 14:43:27 GMT
CMD []
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0975279306aa45296101bef5ac10167461aa640b37718358c961e584fde6fe14`  
		Last Modified: Wed, 12 May 2021 14:44:33 GMT  
		Size: 49.3 MB (49335423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4329d731c9b4d5a6558c7c08f4d08d036a75a4114d3207d169d7a6020fa59a0b`  
		Last Modified: Wed, 12 May 2021 14:44:25 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.6`

```console
$ docker pull varnish@sha256:5b41623edd338ef6bb3b456fdfb79a1b60aba64d6d07b9ca5daeb2210f2dc03c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.6` - linux; amd64

```console
$ docker pull varnish@sha256:6c62ea95b142a9edc53f1ded46db96e5f20545c45d0229c922ac63369bf53a29
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77066494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30e85f5f69a863438e951dee58348e40e869baf7f39fd8383af29ec4133b679`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 14:43:33 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Wed, 12 May 2021 14:43:34 GMT
ENV VARNISH_SIZE=100M
# Wed, 12 May 2021 14:44:03 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 14:44:04 GMT
WORKDIR /etc/varnish
# Wed, 12 May 2021 14:44:04 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 12 May 2021 14:44:05 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 12 May 2021 14:44:05 GMT
EXPOSE 80 8443
# Wed, 12 May 2021 14:44:05 GMT
CMD []
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224ea214330d2e152e48627cea86bd9428d64d20c1f8849f762cb47bfa9bdf56`  
		Last Modified: Wed, 12 May 2021 14:44:57 GMT  
		Size: 49.9 MB (49919878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0344adcc19d810ad7826bcf920f21337390c5bab0ca7dea8cc5aac8e88c6c8`  
		Last Modified: Wed, 12 May 2021 14:44:49 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.6.0`

```console
$ docker pull varnish@sha256:5b41623edd338ef6bb3b456fdfb79a1b60aba64d6d07b9ca5daeb2210f2dc03c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.6.0` - linux; amd64

```console
$ docker pull varnish@sha256:6c62ea95b142a9edc53f1ded46db96e5f20545c45d0229c922ac63369bf53a29
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77066494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30e85f5f69a863438e951dee58348e40e869baf7f39fd8383af29ec4133b679`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 14:43:33 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Wed, 12 May 2021 14:43:34 GMT
ENV VARNISH_SIZE=100M
# Wed, 12 May 2021 14:44:03 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 14:44:04 GMT
WORKDIR /etc/varnish
# Wed, 12 May 2021 14:44:04 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 12 May 2021 14:44:05 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 12 May 2021 14:44:05 GMT
EXPOSE 80 8443
# Wed, 12 May 2021 14:44:05 GMT
CMD []
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224ea214330d2e152e48627cea86bd9428d64d20c1f8849f762cb47bfa9bdf56`  
		Last Modified: Wed, 12 May 2021 14:44:57 GMT  
		Size: 49.9 MB (49919878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0344adcc19d810ad7826bcf920f21337390c5bab0ca7dea8cc5aac8e88c6c8`  
		Last Modified: Wed, 12 May 2021 14:44:49 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.6.0-1`

```console
$ docker pull varnish@sha256:5b41623edd338ef6bb3b456fdfb79a1b60aba64d6d07b9ca5daeb2210f2dc03c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.6.0-1` - linux; amd64

```console
$ docker pull varnish@sha256:6c62ea95b142a9edc53f1ded46db96e5f20545c45d0229c922ac63369bf53a29
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77066494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30e85f5f69a863438e951dee58348e40e869baf7f39fd8383af29ec4133b679`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 14:43:33 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Wed, 12 May 2021 14:43:34 GMT
ENV VARNISH_SIZE=100M
# Wed, 12 May 2021 14:44:03 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 14:44:04 GMT
WORKDIR /etc/varnish
# Wed, 12 May 2021 14:44:04 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 12 May 2021 14:44:05 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 12 May 2021 14:44:05 GMT
EXPOSE 80 8443
# Wed, 12 May 2021 14:44:05 GMT
CMD []
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224ea214330d2e152e48627cea86bd9428d64d20c1f8849f762cb47bfa9bdf56`  
		Last Modified: Wed, 12 May 2021 14:44:57 GMT  
		Size: 49.9 MB (49919878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0344adcc19d810ad7826bcf920f21337390c5bab0ca7dea8cc5aac8e88c6c8`  
		Last Modified: Wed, 12 May 2021 14:44:49 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh`

```console
$ docker pull varnish@sha256:5b41623edd338ef6bb3b456fdfb79a1b60aba64d6d07b9ca5daeb2210f2dc03c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:6c62ea95b142a9edc53f1ded46db96e5f20545c45d0229c922ac63369bf53a29
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77066494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30e85f5f69a863438e951dee58348e40e869baf7f39fd8383af29ec4133b679`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 14:43:33 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Wed, 12 May 2021 14:43:34 GMT
ENV VARNISH_SIZE=100M
# Wed, 12 May 2021 14:44:03 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 14:44:04 GMT
WORKDIR /etc/varnish
# Wed, 12 May 2021 14:44:04 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 12 May 2021 14:44:05 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 12 May 2021 14:44:05 GMT
EXPOSE 80 8443
# Wed, 12 May 2021 14:44:05 GMT
CMD []
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224ea214330d2e152e48627cea86bd9428d64d20c1f8849f762cb47bfa9bdf56`  
		Last Modified: Wed, 12 May 2021 14:44:57 GMT  
		Size: 49.9 MB (49919878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0344adcc19d810ad7826bcf920f21337390c5bab0ca7dea8cc5aac8e88c6c8`  
		Last Modified: Wed, 12 May 2021 14:44:49 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:latest`

```console
$ docker pull varnish@sha256:5b41623edd338ef6bb3b456fdfb79a1b60aba64d6d07b9ca5daeb2210f2dc03c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:6c62ea95b142a9edc53f1ded46db96e5f20545c45d0229c922ac63369bf53a29
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77066494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30e85f5f69a863438e951dee58348e40e869baf7f39fd8383af29ec4133b679`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 14:43:33 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Wed, 12 May 2021 14:43:34 GMT
ENV VARNISH_SIZE=100M
# Wed, 12 May 2021 14:44:03 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 14:44:04 GMT
WORKDIR /etc/varnish
# Wed, 12 May 2021 14:44:04 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 12 May 2021 14:44:05 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 12 May 2021 14:44:05 GMT
EXPOSE 80 8443
# Wed, 12 May 2021 14:44:05 GMT
CMD []
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224ea214330d2e152e48627cea86bd9428d64d20c1f8849f762cb47bfa9bdf56`  
		Last Modified: Wed, 12 May 2021 14:44:57 GMT  
		Size: 49.9 MB (49919878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0344adcc19d810ad7826bcf920f21337390c5bab0ca7dea8cc5aac8e88c6c8`  
		Last Modified: Wed, 12 May 2021 14:44:49 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:stable`

```console
$ docker pull varnish@sha256:cbb313ec5f23e267f4a9f799932a7bf7cb09b3ca4ad4d78eedd028428fc166a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:1b4e10411daa864617852eff5c7e82600c7cf77210b843fe6c96eb4b274bab20
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76482037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ea4085b4075a9050244ec84214287054281eac6f5fee664ee539426173c81d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 14:42:57 GMT
ENV VARNISH_VERSION=6.0.7-1~buster
# Wed, 12 May 2021 14:42:57 GMT
ENV VARNISH_SIZE=100M
# Wed, 12 May 2021 14:43:25 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 14:43:26 GMT
WORKDIR /etc/varnish
# Wed, 12 May 2021 14:43:26 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Wed, 12 May 2021 14:43:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 12 May 2021 14:43:26 GMT
EXPOSE 80 8443
# Wed, 12 May 2021 14:43:27 GMT
CMD []
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0975279306aa45296101bef5ac10167461aa640b37718358c961e584fde6fe14`  
		Last Modified: Wed, 12 May 2021 14:44:33 GMT  
		Size: 49.3 MB (49335423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4329d731c9b4d5a6558c7c08f4d08d036a75a4114d3207d169d7a6020fa59a0b`  
		Last Modified: Wed, 12 May 2021 14:44:25 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
