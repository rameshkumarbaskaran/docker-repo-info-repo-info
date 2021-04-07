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
$ docker pull varnish@sha256:cddbcb4ba52c5037631b525e495397695c4b143756c1040076ab827b4b5c7416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6` - linux; amd64

```console
$ docker pull varnish@sha256:925dc8a8b3ad6d915f62ff18c3875fc0bc36e14b663251e0fa8fe4de6ec34f66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77060117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6d1830aeff7ebacff08a9963ca64cea177c874ec32fe169ac769c155960ef4`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:51:39 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Wed, 31 Mar 2021 14:51:39 GMT
ENV VARNISH_SIZE=100M
# Wed, 31 Mar 2021 14:51:58 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:51:59 GMT
WORKDIR /etc/varnish
# Tue, 06 Apr 2021 19:36:52 GMT
COPY file:9aaa50c9659d4d213c8c91d6b2b20db18172b64d4b8485112a4b97157ef1eb9e in /usr/local/bin/ 
# Tue, 06 Apr 2021 19:36:52 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 06 Apr 2021 19:36:52 GMT
EXPOSE 80 8443
# Tue, 06 Apr 2021 19:36:53 GMT
CMD []
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c112696cbcf76aafbed649fd17dbfa0f080e4d359e61aaf1ddcf827383495c48`  
		Last Modified: Wed, 31 Mar 2021 14:53:23 GMT  
		Size: 49.9 MB (49920031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce038168b768f628dffd1cf70737cba16dd151efcb0f5d7611fdca37d90b20ce`  
		Last Modified: Tue, 06 Apr 2021 19:37:24 GMT  
		Size: 793.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0`

```console
$ docker pull varnish@sha256:9f99115f0aca4a22ca9ede3afb01b6f09414ee4ca78c2bd88b4fdc2dfaabcd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:ff5d8aa64267bf9f6e1328e159e8589d0476c344361883561ea65fd444fe2d77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76475487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be569bf666a1b9a763abd6d89cf6cfb82c8263525fedd61d4812dc4945c6180c`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:51:09 GMT
ENV VARNISH_VERSION=6.0.7-1~buster
# Wed, 31 Mar 2021 14:51:09 GMT
ENV VARNISH_SIZE=100M
# Wed, 31 Mar 2021 14:51:32 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:51:33 GMT
WORKDIR /etc/varnish
# Tue, 06 Apr 2021 19:36:48 GMT
COPY file:9aaa50c9659d4d213c8c91d6b2b20db18172b64d4b8485112a4b97157ef1eb9e in /usr/local/bin/ 
# Tue, 06 Apr 2021 19:36:48 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 06 Apr 2021 19:36:48 GMT
EXPOSE 80 8443
# Tue, 06 Apr 2021 19:36:49 GMT
CMD []
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83aa58409cf19198895096d632959a96f0d681a94bb34765b872de0770863954`  
		Last Modified: Wed, 31 Mar 2021 14:52:57 GMT  
		Size: 49.3 MB (49335404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4887376c816817119d27db82800774166daf6e236f0d92b269d670f146af20d`  
		Last Modified: Tue, 06 Apr 2021 19:37:10 GMT  
		Size: 790.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.7`

```console
$ docker pull varnish@sha256:9f99115f0aca4a22ca9ede3afb01b6f09414ee4ca78c2bd88b4fdc2dfaabcd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0.7` - linux; amd64

```console
$ docker pull varnish@sha256:ff5d8aa64267bf9f6e1328e159e8589d0476c344361883561ea65fd444fe2d77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76475487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be569bf666a1b9a763abd6d89cf6cfb82c8263525fedd61d4812dc4945c6180c`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:51:09 GMT
ENV VARNISH_VERSION=6.0.7-1~buster
# Wed, 31 Mar 2021 14:51:09 GMT
ENV VARNISH_SIZE=100M
# Wed, 31 Mar 2021 14:51:32 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:51:33 GMT
WORKDIR /etc/varnish
# Tue, 06 Apr 2021 19:36:48 GMT
COPY file:9aaa50c9659d4d213c8c91d6b2b20db18172b64d4b8485112a4b97157ef1eb9e in /usr/local/bin/ 
# Tue, 06 Apr 2021 19:36:48 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 06 Apr 2021 19:36:48 GMT
EXPOSE 80 8443
# Tue, 06 Apr 2021 19:36:49 GMT
CMD []
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83aa58409cf19198895096d632959a96f0d681a94bb34765b872de0770863954`  
		Last Modified: Wed, 31 Mar 2021 14:52:57 GMT  
		Size: 49.3 MB (49335404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4887376c816817119d27db82800774166daf6e236f0d92b269d670f146af20d`  
		Last Modified: Tue, 06 Apr 2021 19:37:10 GMT  
		Size: 790.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.7-1`

```console
$ docker pull varnish@sha256:9f99115f0aca4a22ca9ede3afb01b6f09414ee4ca78c2bd88b4fdc2dfaabcd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0.7-1` - linux; amd64

```console
$ docker pull varnish@sha256:ff5d8aa64267bf9f6e1328e159e8589d0476c344361883561ea65fd444fe2d77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76475487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be569bf666a1b9a763abd6d89cf6cfb82c8263525fedd61d4812dc4945c6180c`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:51:09 GMT
ENV VARNISH_VERSION=6.0.7-1~buster
# Wed, 31 Mar 2021 14:51:09 GMT
ENV VARNISH_SIZE=100M
# Wed, 31 Mar 2021 14:51:32 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:51:33 GMT
WORKDIR /etc/varnish
# Tue, 06 Apr 2021 19:36:48 GMT
COPY file:9aaa50c9659d4d213c8c91d6b2b20db18172b64d4b8485112a4b97157ef1eb9e in /usr/local/bin/ 
# Tue, 06 Apr 2021 19:36:48 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 06 Apr 2021 19:36:48 GMT
EXPOSE 80 8443
# Tue, 06 Apr 2021 19:36:49 GMT
CMD []
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83aa58409cf19198895096d632959a96f0d681a94bb34765b872de0770863954`  
		Last Modified: Wed, 31 Mar 2021 14:52:57 GMT  
		Size: 49.3 MB (49335404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4887376c816817119d27db82800774166daf6e236f0d92b269d670f146af20d`  
		Last Modified: Tue, 06 Apr 2021 19:37:10 GMT  
		Size: 790.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.6`

```console
$ docker pull varnish@sha256:cddbcb4ba52c5037631b525e495397695c4b143756c1040076ab827b4b5c7416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.6` - linux; amd64

```console
$ docker pull varnish@sha256:925dc8a8b3ad6d915f62ff18c3875fc0bc36e14b663251e0fa8fe4de6ec34f66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77060117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6d1830aeff7ebacff08a9963ca64cea177c874ec32fe169ac769c155960ef4`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:51:39 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Wed, 31 Mar 2021 14:51:39 GMT
ENV VARNISH_SIZE=100M
# Wed, 31 Mar 2021 14:51:58 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:51:59 GMT
WORKDIR /etc/varnish
# Tue, 06 Apr 2021 19:36:52 GMT
COPY file:9aaa50c9659d4d213c8c91d6b2b20db18172b64d4b8485112a4b97157ef1eb9e in /usr/local/bin/ 
# Tue, 06 Apr 2021 19:36:52 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 06 Apr 2021 19:36:52 GMT
EXPOSE 80 8443
# Tue, 06 Apr 2021 19:36:53 GMT
CMD []
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c112696cbcf76aafbed649fd17dbfa0f080e4d359e61aaf1ddcf827383495c48`  
		Last Modified: Wed, 31 Mar 2021 14:53:23 GMT  
		Size: 49.9 MB (49920031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce038168b768f628dffd1cf70737cba16dd151efcb0f5d7611fdca37d90b20ce`  
		Last Modified: Tue, 06 Apr 2021 19:37:24 GMT  
		Size: 793.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.6.0`

```console
$ docker pull varnish@sha256:cddbcb4ba52c5037631b525e495397695c4b143756c1040076ab827b4b5c7416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.6.0` - linux; amd64

```console
$ docker pull varnish@sha256:925dc8a8b3ad6d915f62ff18c3875fc0bc36e14b663251e0fa8fe4de6ec34f66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77060117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6d1830aeff7ebacff08a9963ca64cea177c874ec32fe169ac769c155960ef4`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:51:39 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Wed, 31 Mar 2021 14:51:39 GMT
ENV VARNISH_SIZE=100M
# Wed, 31 Mar 2021 14:51:58 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:51:59 GMT
WORKDIR /etc/varnish
# Tue, 06 Apr 2021 19:36:52 GMT
COPY file:9aaa50c9659d4d213c8c91d6b2b20db18172b64d4b8485112a4b97157ef1eb9e in /usr/local/bin/ 
# Tue, 06 Apr 2021 19:36:52 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 06 Apr 2021 19:36:52 GMT
EXPOSE 80 8443
# Tue, 06 Apr 2021 19:36:53 GMT
CMD []
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c112696cbcf76aafbed649fd17dbfa0f080e4d359e61aaf1ddcf827383495c48`  
		Last Modified: Wed, 31 Mar 2021 14:53:23 GMT  
		Size: 49.9 MB (49920031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce038168b768f628dffd1cf70737cba16dd151efcb0f5d7611fdca37d90b20ce`  
		Last Modified: Tue, 06 Apr 2021 19:37:24 GMT  
		Size: 793.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.6.0-1`

```console
$ docker pull varnish@sha256:cddbcb4ba52c5037631b525e495397695c4b143756c1040076ab827b4b5c7416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.6.0-1` - linux; amd64

```console
$ docker pull varnish@sha256:925dc8a8b3ad6d915f62ff18c3875fc0bc36e14b663251e0fa8fe4de6ec34f66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77060117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6d1830aeff7ebacff08a9963ca64cea177c874ec32fe169ac769c155960ef4`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:51:39 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Wed, 31 Mar 2021 14:51:39 GMT
ENV VARNISH_SIZE=100M
# Wed, 31 Mar 2021 14:51:58 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:51:59 GMT
WORKDIR /etc/varnish
# Tue, 06 Apr 2021 19:36:52 GMT
COPY file:9aaa50c9659d4d213c8c91d6b2b20db18172b64d4b8485112a4b97157ef1eb9e in /usr/local/bin/ 
# Tue, 06 Apr 2021 19:36:52 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 06 Apr 2021 19:36:52 GMT
EXPOSE 80 8443
# Tue, 06 Apr 2021 19:36:53 GMT
CMD []
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c112696cbcf76aafbed649fd17dbfa0f080e4d359e61aaf1ddcf827383495c48`  
		Last Modified: Wed, 31 Mar 2021 14:53:23 GMT  
		Size: 49.9 MB (49920031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce038168b768f628dffd1cf70737cba16dd151efcb0f5d7611fdca37d90b20ce`  
		Last Modified: Tue, 06 Apr 2021 19:37:24 GMT  
		Size: 793.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh`

```console
$ docker pull varnish@sha256:cddbcb4ba52c5037631b525e495397695c4b143756c1040076ab827b4b5c7416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:925dc8a8b3ad6d915f62ff18c3875fc0bc36e14b663251e0fa8fe4de6ec34f66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77060117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6d1830aeff7ebacff08a9963ca64cea177c874ec32fe169ac769c155960ef4`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:51:39 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Wed, 31 Mar 2021 14:51:39 GMT
ENV VARNISH_SIZE=100M
# Wed, 31 Mar 2021 14:51:58 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:51:59 GMT
WORKDIR /etc/varnish
# Tue, 06 Apr 2021 19:36:52 GMT
COPY file:9aaa50c9659d4d213c8c91d6b2b20db18172b64d4b8485112a4b97157ef1eb9e in /usr/local/bin/ 
# Tue, 06 Apr 2021 19:36:52 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 06 Apr 2021 19:36:52 GMT
EXPOSE 80 8443
# Tue, 06 Apr 2021 19:36:53 GMT
CMD []
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c112696cbcf76aafbed649fd17dbfa0f080e4d359e61aaf1ddcf827383495c48`  
		Last Modified: Wed, 31 Mar 2021 14:53:23 GMT  
		Size: 49.9 MB (49920031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce038168b768f628dffd1cf70737cba16dd151efcb0f5d7611fdca37d90b20ce`  
		Last Modified: Tue, 06 Apr 2021 19:37:24 GMT  
		Size: 793.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:latest`

```console
$ docker pull varnish@sha256:cddbcb4ba52c5037631b525e495397695c4b143756c1040076ab827b4b5c7416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:925dc8a8b3ad6d915f62ff18c3875fc0bc36e14b663251e0fa8fe4de6ec34f66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77060117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6d1830aeff7ebacff08a9963ca64cea177c874ec32fe169ac769c155960ef4`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:51:39 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Wed, 31 Mar 2021 14:51:39 GMT
ENV VARNISH_SIZE=100M
# Wed, 31 Mar 2021 14:51:58 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:51:59 GMT
WORKDIR /etc/varnish
# Tue, 06 Apr 2021 19:36:52 GMT
COPY file:9aaa50c9659d4d213c8c91d6b2b20db18172b64d4b8485112a4b97157ef1eb9e in /usr/local/bin/ 
# Tue, 06 Apr 2021 19:36:52 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 06 Apr 2021 19:36:52 GMT
EXPOSE 80 8443
# Tue, 06 Apr 2021 19:36:53 GMT
CMD []
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c112696cbcf76aafbed649fd17dbfa0f080e4d359e61aaf1ddcf827383495c48`  
		Last Modified: Wed, 31 Mar 2021 14:53:23 GMT  
		Size: 49.9 MB (49920031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce038168b768f628dffd1cf70737cba16dd151efcb0f5d7611fdca37d90b20ce`  
		Last Modified: Tue, 06 Apr 2021 19:37:24 GMT  
		Size: 793.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:stable`

```console
$ docker pull varnish@sha256:9f99115f0aca4a22ca9ede3afb01b6f09414ee4ca78c2bd88b4fdc2dfaabcd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:ff5d8aa64267bf9f6e1328e159e8589d0476c344361883561ea65fd444fe2d77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76475487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be569bf666a1b9a763abd6d89cf6cfb82c8263525fedd61d4812dc4945c6180c`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 14:51:09 GMT
ENV VARNISH_VERSION=6.0.7-1~buster
# Wed, 31 Mar 2021 14:51:09 GMT
ENV VARNISH_SIZE=100M
# Wed, 31 Mar 2021 14:51:32 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 14:51:33 GMT
WORKDIR /etc/varnish
# Tue, 06 Apr 2021 19:36:48 GMT
COPY file:9aaa50c9659d4d213c8c91d6b2b20db18172b64d4b8485112a4b97157ef1eb9e in /usr/local/bin/ 
# Tue, 06 Apr 2021 19:36:48 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 06 Apr 2021 19:36:48 GMT
EXPOSE 80 8443
# Tue, 06 Apr 2021 19:36:49 GMT
CMD []
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83aa58409cf19198895096d632959a96f0d681a94bb34765b872de0770863954`  
		Last Modified: Wed, 31 Mar 2021 14:52:57 GMT  
		Size: 49.3 MB (49335404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4887376c816817119d27db82800774166daf6e236f0d92b269d670f146af20d`  
		Last Modified: Tue, 06 Apr 2021 19:37:10 GMT  
		Size: 790.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
