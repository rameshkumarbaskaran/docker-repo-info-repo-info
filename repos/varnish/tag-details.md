<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6`](#varnish6)
-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.6`](#varnish606)
-	[`varnish:6.0.6-1`](#varnish606-1)
-	[`varnish:6.4`](#varnish64)
-	[`varnish:6.4.0`](#varnish640)
-	[`varnish:6.4.0-1`](#varnish640-1)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:stable`](#varnishstable)

## `varnish:6`

```console
$ docker pull varnish@sha256:6e563f527878a9c55354039c6f39a156eef1102b1d2aa992398bfd1b80213791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6` - linux; amd64

```console
$ docker pull varnish@sha256:e086d3b5385e0fda78e93af023a1e3fa8486fe0215ab844ceb6847c6f1f807bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76767914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7678ff147b618a786720d6ead2ff7ae19b1f990ff7ef1028a483f7be9a2729d8`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:16:44 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Tue, 31 Mar 2020 02:16:44 GMT
ENV VARNISH_SIZE=100M
# Tue, 31 Mar 2020 02:17:09 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:17:10 GMT
WORKDIR /etc/varnish
# Tue, 31 Mar 2020 02:17:10 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 31 Mar 2020 02:17:11 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 31 Mar 2020 02:17:11 GMT
EXPOSE 80 8443
# Tue, 31 Mar 2020 02:17:12 GMT
CMD []
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709f9e6210227aaf3005681c46399fe85bce3eccfa53ad2e1c14458aa58349cb`  
		Last Modified: Tue, 31 Mar 2020 02:17:44 GMT  
		Size: 49.7 MB (49675601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011a17c03f8f324c8db6a0d6f22d6a6cd03e9d4d3326a158f50b837e2fb25775`  
		Last Modified: Tue, 31 Mar 2020 02:17:35 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0`

```console
$ docker pull varnish@sha256:feed6fb4114d467a63c9f9fed1721b140c986768f157c1709efbdc1fb1c02376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:407b2702fa096bd8a01a651f15de311cef2fb29c594d330ba3e032b2242ed75c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67208420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bd583ef89975a94d9d967e2189fdd02335739a541360e7029480b75a746b45`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:16:11 GMT
ENV VARNISH_VERSION=6.0.6-1~stretch
# Tue, 31 Mar 2020 02:16:11 GMT
ENV VARNISH_SIZE=100M
# Tue, 31 Mar 2020 02:16:37 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:16:37 GMT
WORKDIR /etc/varnish
# Tue, 31 Mar 2020 02:16:38 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 31 Mar 2020 02:16:38 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 31 Mar 2020 02:16:39 GMT
EXPOSE 80 8443
# Tue, 31 Mar 2020 02:16:39 GMT
CMD []
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479160b319e16e3e144876625062c8eba0abe962107f9d3424d843cdec2b92df`  
		Last Modified: Tue, 31 Mar 2020 02:17:30 GMT  
		Size: 44.7 MB (44694582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117f9e5b0e819d9d66639ef00cb69fd9d2aa3bb69340c841c331ac4949d9f0e8`  
		Last Modified: Tue, 31 Mar 2020 02:17:21 GMT  
		Size: 464.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.6`

```console
$ docker pull varnish@sha256:feed6fb4114d467a63c9f9fed1721b140c986768f157c1709efbdc1fb1c02376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0.6` - linux; amd64

```console
$ docker pull varnish@sha256:407b2702fa096bd8a01a651f15de311cef2fb29c594d330ba3e032b2242ed75c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67208420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bd583ef89975a94d9d967e2189fdd02335739a541360e7029480b75a746b45`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:16:11 GMT
ENV VARNISH_VERSION=6.0.6-1~stretch
# Tue, 31 Mar 2020 02:16:11 GMT
ENV VARNISH_SIZE=100M
# Tue, 31 Mar 2020 02:16:37 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:16:37 GMT
WORKDIR /etc/varnish
# Tue, 31 Mar 2020 02:16:38 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 31 Mar 2020 02:16:38 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 31 Mar 2020 02:16:39 GMT
EXPOSE 80 8443
# Tue, 31 Mar 2020 02:16:39 GMT
CMD []
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479160b319e16e3e144876625062c8eba0abe962107f9d3424d843cdec2b92df`  
		Last Modified: Tue, 31 Mar 2020 02:17:30 GMT  
		Size: 44.7 MB (44694582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117f9e5b0e819d9d66639ef00cb69fd9d2aa3bb69340c841c331ac4949d9f0e8`  
		Last Modified: Tue, 31 Mar 2020 02:17:21 GMT  
		Size: 464.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.6-1`

```console
$ docker pull varnish@sha256:feed6fb4114d467a63c9f9fed1721b140c986768f157c1709efbdc1fb1c02376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0.6-1` - linux; amd64

```console
$ docker pull varnish@sha256:407b2702fa096bd8a01a651f15de311cef2fb29c594d330ba3e032b2242ed75c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67208420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bd583ef89975a94d9d967e2189fdd02335739a541360e7029480b75a746b45`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:16:11 GMT
ENV VARNISH_VERSION=6.0.6-1~stretch
# Tue, 31 Mar 2020 02:16:11 GMT
ENV VARNISH_SIZE=100M
# Tue, 31 Mar 2020 02:16:37 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:16:37 GMT
WORKDIR /etc/varnish
# Tue, 31 Mar 2020 02:16:38 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 31 Mar 2020 02:16:38 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 31 Mar 2020 02:16:39 GMT
EXPOSE 80 8443
# Tue, 31 Mar 2020 02:16:39 GMT
CMD []
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479160b319e16e3e144876625062c8eba0abe962107f9d3424d843cdec2b92df`  
		Last Modified: Tue, 31 Mar 2020 02:17:30 GMT  
		Size: 44.7 MB (44694582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117f9e5b0e819d9d66639ef00cb69fd9d2aa3bb69340c841c331ac4949d9f0e8`  
		Last Modified: Tue, 31 Mar 2020 02:17:21 GMT  
		Size: 464.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.4`

```console
$ docker pull varnish@sha256:6e563f527878a9c55354039c6f39a156eef1102b1d2aa992398bfd1b80213791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.4` - linux; amd64

```console
$ docker pull varnish@sha256:e086d3b5385e0fda78e93af023a1e3fa8486fe0215ab844ceb6847c6f1f807bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76767914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7678ff147b618a786720d6ead2ff7ae19b1f990ff7ef1028a483f7be9a2729d8`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:16:44 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Tue, 31 Mar 2020 02:16:44 GMT
ENV VARNISH_SIZE=100M
# Tue, 31 Mar 2020 02:17:09 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:17:10 GMT
WORKDIR /etc/varnish
# Tue, 31 Mar 2020 02:17:10 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 31 Mar 2020 02:17:11 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 31 Mar 2020 02:17:11 GMT
EXPOSE 80 8443
# Tue, 31 Mar 2020 02:17:12 GMT
CMD []
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709f9e6210227aaf3005681c46399fe85bce3eccfa53ad2e1c14458aa58349cb`  
		Last Modified: Tue, 31 Mar 2020 02:17:44 GMT  
		Size: 49.7 MB (49675601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011a17c03f8f324c8db6a0d6f22d6a6cd03e9d4d3326a158f50b837e2fb25775`  
		Last Modified: Tue, 31 Mar 2020 02:17:35 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.4.0`

```console
$ docker pull varnish@sha256:6e563f527878a9c55354039c6f39a156eef1102b1d2aa992398bfd1b80213791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.4.0` - linux; amd64

```console
$ docker pull varnish@sha256:e086d3b5385e0fda78e93af023a1e3fa8486fe0215ab844ceb6847c6f1f807bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76767914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7678ff147b618a786720d6ead2ff7ae19b1f990ff7ef1028a483f7be9a2729d8`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:16:44 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Tue, 31 Mar 2020 02:16:44 GMT
ENV VARNISH_SIZE=100M
# Tue, 31 Mar 2020 02:17:09 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:17:10 GMT
WORKDIR /etc/varnish
# Tue, 31 Mar 2020 02:17:10 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 31 Mar 2020 02:17:11 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 31 Mar 2020 02:17:11 GMT
EXPOSE 80 8443
# Tue, 31 Mar 2020 02:17:12 GMT
CMD []
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709f9e6210227aaf3005681c46399fe85bce3eccfa53ad2e1c14458aa58349cb`  
		Last Modified: Tue, 31 Mar 2020 02:17:44 GMT  
		Size: 49.7 MB (49675601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011a17c03f8f324c8db6a0d6f22d6a6cd03e9d4d3326a158f50b837e2fb25775`  
		Last Modified: Tue, 31 Mar 2020 02:17:35 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.4.0-1`

```console
$ docker pull varnish@sha256:6e563f527878a9c55354039c6f39a156eef1102b1d2aa992398bfd1b80213791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.4.0-1` - linux; amd64

```console
$ docker pull varnish@sha256:e086d3b5385e0fda78e93af023a1e3fa8486fe0215ab844ceb6847c6f1f807bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76767914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7678ff147b618a786720d6ead2ff7ae19b1f990ff7ef1028a483f7be9a2729d8`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:16:44 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Tue, 31 Mar 2020 02:16:44 GMT
ENV VARNISH_SIZE=100M
# Tue, 31 Mar 2020 02:17:09 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:17:10 GMT
WORKDIR /etc/varnish
# Tue, 31 Mar 2020 02:17:10 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 31 Mar 2020 02:17:11 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 31 Mar 2020 02:17:11 GMT
EXPOSE 80 8443
# Tue, 31 Mar 2020 02:17:12 GMT
CMD []
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709f9e6210227aaf3005681c46399fe85bce3eccfa53ad2e1c14458aa58349cb`  
		Last Modified: Tue, 31 Mar 2020 02:17:44 GMT  
		Size: 49.7 MB (49675601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011a17c03f8f324c8db6a0d6f22d6a6cd03e9d4d3326a158f50b837e2fb25775`  
		Last Modified: Tue, 31 Mar 2020 02:17:35 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh`

```console
$ docker pull varnish@sha256:6e563f527878a9c55354039c6f39a156eef1102b1d2aa992398bfd1b80213791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:e086d3b5385e0fda78e93af023a1e3fa8486fe0215ab844ceb6847c6f1f807bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76767914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7678ff147b618a786720d6ead2ff7ae19b1f990ff7ef1028a483f7be9a2729d8`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:16:44 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Tue, 31 Mar 2020 02:16:44 GMT
ENV VARNISH_SIZE=100M
# Tue, 31 Mar 2020 02:17:09 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:17:10 GMT
WORKDIR /etc/varnish
# Tue, 31 Mar 2020 02:17:10 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 31 Mar 2020 02:17:11 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 31 Mar 2020 02:17:11 GMT
EXPOSE 80 8443
# Tue, 31 Mar 2020 02:17:12 GMT
CMD []
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709f9e6210227aaf3005681c46399fe85bce3eccfa53ad2e1c14458aa58349cb`  
		Last Modified: Tue, 31 Mar 2020 02:17:44 GMT  
		Size: 49.7 MB (49675601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011a17c03f8f324c8db6a0d6f22d6a6cd03e9d4d3326a158f50b837e2fb25775`  
		Last Modified: Tue, 31 Mar 2020 02:17:35 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:latest`

```console
$ docker pull varnish@sha256:6e563f527878a9c55354039c6f39a156eef1102b1d2aa992398bfd1b80213791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:e086d3b5385e0fda78e93af023a1e3fa8486fe0215ab844ceb6847c6f1f807bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76767914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7678ff147b618a786720d6ead2ff7ae19b1f990ff7ef1028a483f7be9a2729d8`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:16:44 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Tue, 31 Mar 2020 02:16:44 GMT
ENV VARNISH_SIZE=100M
# Tue, 31 Mar 2020 02:17:09 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:17:10 GMT
WORKDIR /etc/varnish
# Tue, 31 Mar 2020 02:17:10 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 31 Mar 2020 02:17:11 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 31 Mar 2020 02:17:11 GMT
EXPOSE 80 8443
# Tue, 31 Mar 2020 02:17:12 GMT
CMD []
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709f9e6210227aaf3005681c46399fe85bce3eccfa53ad2e1c14458aa58349cb`  
		Last Modified: Tue, 31 Mar 2020 02:17:44 GMT  
		Size: 49.7 MB (49675601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011a17c03f8f324c8db6a0d6f22d6a6cd03e9d4d3326a158f50b837e2fb25775`  
		Last Modified: Tue, 31 Mar 2020 02:17:35 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:stable`

```console
$ docker pull varnish@sha256:feed6fb4114d467a63c9f9fed1721b140c986768f157c1709efbdc1fb1c02376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:407b2702fa096bd8a01a651f15de311cef2fb29c594d330ba3e032b2242ed75c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67208420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bd583ef89975a94d9d967e2189fdd02335739a541360e7029480b75a746b45`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:16:11 GMT
ENV VARNISH_VERSION=6.0.6-1~stretch
# Tue, 31 Mar 2020 02:16:11 GMT
ENV VARNISH_SIZE=100M
# Tue, 31 Mar 2020 02:16:37 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:16:37 GMT
WORKDIR /etc/varnish
# Tue, 31 Mar 2020 02:16:38 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 31 Mar 2020 02:16:38 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 31 Mar 2020 02:16:39 GMT
EXPOSE 80 8443
# Tue, 31 Mar 2020 02:16:39 GMT
CMD []
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479160b319e16e3e144876625062c8eba0abe962107f9d3424d843cdec2b92df`  
		Last Modified: Tue, 31 Mar 2020 02:17:30 GMT  
		Size: 44.7 MB (44694582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117f9e5b0e819d9d66639ef00cb69fd9d2aa3bb69340c841c331ac4949d9f0e8`  
		Last Modified: Tue, 31 Mar 2020 02:17:21 GMT  
		Size: 464.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
