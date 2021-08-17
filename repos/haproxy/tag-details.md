<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `haproxy`

-	[`haproxy:1.7`](#haproxy17)
-	[`haproxy:1.7-alpine`](#haproxy17-alpine)
-	[`haproxy:1.7.14`](#haproxy1714)
-	[`haproxy:1.7.14-alpine`](#haproxy1714-alpine)
-	[`haproxy:1.8`](#haproxy18)
-	[`haproxy:1.8-alpine`](#haproxy18-alpine)
-	[`haproxy:1.8.30`](#haproxy1830)
-	[`haproxy:1.8.30-alpine`](#haproxy1830-alpine)
-	[`haproxy:2.0`](#haproxy20)
-	[`haproxy:2.0-alpine`](#haproxy20-alpine)
-	[`haproxy:2.0.24`](#haproxy2024)
-	[`haproxy:2.0.24-alpine`](#haproxy2024-alpine)
-	[`haproxy:2.2`](#haproxy22)
-	[`haproxy:2.2-alpine`](#haproxy22-alpine)
-	[`haproxy:2.2.16`](#haproxy2216)
-	[`haproxy:2.2.16-alpine`](#haproxy2216-alpine)
-	[`haproxy:2.3`](#haproxy23)
-	[`haproxy:2.3-alpine`](#haproxy23-alpine)
-	[`haproxy:2.3.13`](#haproxy2313)
-	[`haproxy:2.3.13-alpine`](#haproxy2313-alpine)
-	[`haproxy:2.4`](#haproxy24)
-	[`haproxy:2.4-alpine`](#haproxy24-alpine)
-	[`haproxy:2.4.3`](#haproxy243)
-	[`haproxy:2.4.3-alpine`](#haproxy243-alpine)
-	[`haproxy:2.5-dev`](#haproxy25-dev)
-	[`haproxy:2.5-dev-alpine`](#haproxy25-dev-alpine)
-	[`haproxy:2.5-dev4`](#haproxy25-dev4)
-	[`haproxy:2.5-dev4-alpine`](#haproxy25-dev4-alpine)
-	[`haproxy:alpine`](#haproxyalpine)
-	[`haproxy:latest`](#haproxylatest)
-	[`haproxy:lts`](#haproxylts)
-	[`haproxy:lts-alpine`](#haproxylts-alpine)

## `haproxy:1.7`

```console
$ docker pull haproxy@sha256:b6c1b71662c55b2c3401d7b0741737a1a26ad3cce273adcb95702e11782ca169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:1.7` - linux; amd64

```console
$ docker pull haproxy@sha256:f40e8a82e9a7583baa6a0f7209c02dc738685cb2eca03bc60641114d0b19291c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32541417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab9d7a65ad83bce27e523ad6340deb3386f1931abf666ead6b5d615b51f8a88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 10:43:34 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 10:51:51 GMT
ENV HAPROXY_VERSION=1.7.14
# Tue, 17 Aug 2021 10:51:52 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Tue, 17 Aug 2021 10:51:52 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Tue, 17 Aug 2021 10:52:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 10:52:46 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 10:52:46 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 10:52:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 10:52:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 10:52:48 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd06683556254cbe06dad4624837c2dcbd2fec67c7fbdd057251f0a207a9315`  
		Last Modified: Tue, 17 Aug 2021 10:53:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a8907733b2e1814f58567544fa320f9fee50f7c2ae6e68c7943f738f4fb40f`  
		Last Modified: Tue, 17 Aug 2021 10:55:15 GMT  
		Size: 5.4 MB (5393465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e858a054a2e23fd834beed9f3ddbb4d672760a1f19f511239d49bbb48235895`  
		Last Modified: Tue, 17 Aug 2021 10:55:13 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2ce652dfe1bd2b640e28045d3d47697eed2a0e11580262fd8358e6c3bd4d9a`  
		Last Modified: Tue, 17 Aug 2021 10:55:13 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:e5a26fa3795089132ec501d5d25515c7fc9814f19dbbfb491f8ac063f48ce1e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 MB (29901243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d387022ed5cd3bc3c2e34c0ab06a6de79cd1fdcfddcf7b452ee78922090e60dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:56:50 GMT
ADD file:f29260935f1f8b3eef5eb0d5e49dd4cf5370e8731a3f4006d6023724bce09601 in / 
# Tue, 17 Aug 2021 01:56:51 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:39:10 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:45:53 GMT
ENV HAPROXY_VERSION=1.7.14
# Tue, 17 Aug 2021 08:45:53 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Tue, 17 Aug 2021 08:45:54 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Tue, 17 Aug 2021 08:46:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:46:43 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:46:44 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:46:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 08:46:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:46:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3dfab4a5b2accf2d709d8c7d14a42715948ecf2d6da4943a6e2c0de8ae7536a0`  
		Last Modified: Tue, 17 Aug 2021 02:12:42 GMT  
		Size: 24.9 MB (24879063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeabbf4f2af3ef66d78a317a4b3a0704a061a5de2611c57b0bfc47b775c2ed8b`  
		Last Modified: Tue, 17 Aug 2021 08:48:10 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a177a63e39c847952d5d0e2d07ae73e6130eee594bd15f916a760b972ff3ba8f`  
		Last Modified: Tue, 17 Aug 2021 08:50:04 GMT  
		Size: 5.0 MB (5020210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d4bf7aa089a841b638c3983b8543bd4830c622950d8c1a8baff2da1412e6f5`  
		Last Modified: Tue, 17 Aug 2021 08:50:01 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9ed403e2cf4aa127414ca59a2eac19c502f349bde7735c4267cd307d908e52`  
		Last Modified: Tue, 17 Aug 2021 08:50:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:723e5f94bb63059b4978bde52e07b8022a901d5a9c70c862490362dc46f5a4cf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27640424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099ed80319e59967d48ffd6565919f9b792d439fa9f731f362078eaaee4bb6db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 02:14:25 GMT
ADD file:ca8cc4b509e305fa07662fbf2234ed78f0056569f6ca047305dc02bcd60f1558 in / 
# Tue, 17 Aug 2021 02:14:26 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 16:10:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:18:08 GMT
ENV HAPROXY_VERSION=1.7.14
# Tue, 17 Aug 2021 16:18:08 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Tue, 17 Aug 2021 16:18:09 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Tue, 17 Aug 2021 16:18:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:18:54 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:18:55 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:18:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:18:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:18:57 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:13e3f03410ff211945a725435c13065288d48a8cb740f0530e7588012c2679a4`  
		Last Modified: Tue, 17 Aug 2021 02:30:58 GMT  
		Size: 22.7 MB (22746254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb366ce7907325b732435009125848fb9596a1afdb0f87a8703cdf4342e91a4e`  
		Last Modified: Tue, 17 Aug 2021 16:21:35 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d1a9728625ebf90c638ef880a54b4b4efde83a5a7a2e382669193bd936e0f9`  
		Last Modified: Tue, 17 Aug 2021 16:23:55 GMT  
		Size: 4.9 MB (4892202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d947d1197b8278af3f1ef17a3ef2a0589b092c81199e1a4e9b4531fa5ec7b7`  
		Last Modified: Tue, 17 Aug 2021 16:23:52 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d1a1744cdff50b71fd1ed4ee9ed6ba4e9d24640421370b4f234dff03c9d6ae`  
		Last Modified: Tue, 17 Aug 2021 16:23:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:b4adf9fe01dd3abda42c56d278586cfd311660c69860e0f70b3aaa11c7e23185
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31198000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddca6c423e16f76864ba1b61792d012e27e97d20a07bc61240e1304c850745b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:12:02 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:17:24 GMT
ENV HAPROXY_VERSION=1.7.14
# Tue, 17 Aug 2021 08:17:24 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Tue, 17 Aug 2021 08:17:25 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Tue, 17 Aug 2021 08:17:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:17:55 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:17:55 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:17:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 08:17:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:17:56 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc63cf29191f59ddbc41452b9edbe5f8145c4370cd74d3981d50a862173029b`  
		Last Modified: Tue, 17 Aug 2021 08:19:14 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90103053f41007e54898ca5581e39ccae7389e64df4d8271f7c1cb8cb765977b`  
		Last Modified: Tue, 17 Aug 2021 08:20:46 GMT  
		Size: 5.3 MB (5280957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586fb707d52466ad852d767549c530d7de019464d4db6861ae7961ffab783696`  
		Last Modified: Tue, 17 Aug 2021 08:20:45 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d0897ef657c46f8192ae262113034ba62e27d9e5238874311a7affc117583d`  
		Last Modified: Tue, 17 Aug 2021 08:20:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7` - linux; 386

```console
$ docker pull haproxy@sha256:e53d785c8857fd60d26e0199682e320df9c81ef22a126a63abc84a15ba137e5b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 MB (33123623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c975d7d58fea1bddf93ab0737a2a5c43d68cb2361aec6b2b6825b75066202b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:41:16 GMT
ADD file:0418032b55cd0a6dd515ac277fb9f92354397503cab212d446d3a3d8c647a60f in / 
# Tue, 17 Aug 2021 01:41:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 12:14:55 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 12:23:43 GMT
ENV HAPROXY_VERSION=1.7.14
# Tue, 17 Aug 2021 12:23:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Tue, 17 Aug 2021 12:23:43 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Tue, 17 Aug 2021 12:24:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 12:24:20 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 12:24:20 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 12:24:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 12:24:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 12:24:22 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c1c94e1f2523d69effaa463d64fc9962cfc67e2a956f0476c94200e7cf19edf0`  
		Last Modified: Tue, 17 Aug 2021 01:50:57 GMT  
		Size: 27.8 MB (27797627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f804b7c921abcc2fb2904ad2092beefd0224c9bd4cb1cf6477727e6f2bbd7599`  
		Last Modified: Tue, 17 Aug 2021 12:26:22 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e968d632b7ecdca9d50f86e34b80dcf8bc93e2f92c9f6f62559f75a448020b`  
		Last Modified: Tue, 17 Aug 2021 12:28:17 GMT  
		Size: 5.3 MB (5324030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2063a2c5abcf07a4bc200fcd196e03db383f995ef2d02f8be547b2fe4b81b98d`  
		Last Modified: Tue, 17 Aug 2021 12:28:16 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b887b2e8700fb445227f0cfd511782554827370db6073f4f8f7213772e9ea1`  
		Last Modified: Tue, 17 Aug 2021 12:28:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7` - linux; mips64le

```console
$ docker pull haproxy@sha256:e6d3ab1a1c4319e2df4c4a3473da744774aba55b218bfcc4ce15704ab376e28d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 MB (30842800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920c22be6fc8222e82661d19944ed834018aa1497442d0e2423c98d67011e56d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:12:26 GMT
ADD file:8bd279803ead4ddce8db90b65e89c423f84fbf6042bfbeae8c09486b2e884cde in / 
# Tue, 17 Aug 2021 01:12:27 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:10:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 14:25:28 GMT
ENV HAPROXY_VERSION=1.7.14
# Tue, 17 Aug 2021 14:25:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Tue, 17 Aug 2021 14:25:28 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Tue, 17 Aug 2021 14:26:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 14:26:53 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 14:26:54 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 14:26:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 14:26:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:26:56 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a711e3e37b88ef77496c07ed663bb4270ecba9057eba452a91cc9be0bafb9c32`  
		Last Modified: Tue, 17 Aug 2021 01:21:44 GMT  
		Size: 25.8 MB (25813007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac33edc8b81dffec584b1a7ca6a8abea967f70259323fc62ff423b9c01642e`  
		Last Modified: Tue, 17 Aug 2021 14:27:23 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddda091f7f46634f77e5cd53b439482e105729a0a15555462e3b444be20d2ac`  
		Last Modified: Tue, 17 Aug 2021 14:29:10 GMT  
		Size: 5.0 MB (5027822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3053b3229d607030b1143168534283604b72feb411368145a86986da2e2304`  
		Last Modified: Tue, 17 Aug 2021 14:29:07 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73071e325ceb87c5540533797edf78d802018193a6743953340aa353bf6651a7`  
		Last Modified: Tue, 17 Aug 2021 14:29:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7` - linux; ppc64le

```console
$ docker pull haproxy@sha256:8475ee3509f16bcfb2eaf7436f016735de26df74d868625788f74fd8dd897db6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36266635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6124622e0285d0dc28f6a0efcf26dea91ef3b97e3532fbb017fdbe339d904b14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:34:13 GMT
ADD file:8b9b12a994a2519f725d1ed1f4ab5a444665262678fd8e6c42cf78f32dacb7fa in / 
# Tue, 17 Aug 2021 01:34:20 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 13:36:19 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 14:17:12 GMT
ENV HAPROXY_VERSION=1.7.14
# Tue, 17 Aug 2021 14:17:20 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Tue, 17 Aug 2021 14:17:24 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Tue, 17 Aug 2021 14:22:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 14:22:45 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 14:22:49 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 14:22:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 14:23:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:23:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c3e09f0e3e7f6fcb741a4c9214b63e341e1d9b53d7689a5ad6ff640b61a82541`  
		Last Modified: Tue, 17 Aug 2021 01:48:22 GMT  
		Size: 30.6 MB (30553721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb7833dc31cf72935b478f7bf90e34f0f2a22d8260da177e4648ac973af1f9c`  
		Last Modified: Tue, 17 Aug 2021 14:24:41 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867889f7912d7d0fee8c07df97a20c80d5000f06e27cf631dd0766eb2447f2ec`  
		Last Modified: Tue, 17 Aug 2021 14:26:27 GMT  
		Size: 5.7 MB (5710929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4d672ce7e9ae8d89f638de3f292411dd33bc87c7db4c438552651130404959`  
		Last Modified: Tue, 17 Aug 2021 14:26:26 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be2439b3af33effe4d2ca5e2591e968eb1f78e5ed63d01d79488c2972654521`  
		Last Modified: Tue, 17 Aug 2021 14:26:26 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7` - linux; s390x

```console
$ docker pull haproxy@sha256:0166679a3e5b69d94b2599ede49deccc58383a56943e64ee89993ec2e9aea36b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30892015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d78fee778d753c2974dea370009222be4148044c03f8beab87f13698a755fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 07:18:12 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 07:26:33 GMT
ENV HAPROXY_VERSION=1.7.14
# Tue, 17 Aug 2021 07:26:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Tue, 17 Aug 2021 07:26:34 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Tue, 17 Aug 2021 07:26:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 07:27:00 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 07:27:00 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 07:27:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 07:27:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 07:27:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16a2f2a1452470a1d818d8d16934d08d2a57b312ceabcce8c1cfad6c99f00a2`  
		Last Modified: Tue, 17 Aug 2021 07:28:00 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7584ed9c9eebac5bbcca1b1155267a49755d5f13a4b984247ec17cba4415d58c`  
		Last Modified: Tue, 17 Aug 2021 07:29:00 GMT  
		Size: 5.1 MB (5129187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b378b86781f56ce622911bf77656081f2f43b515f52e0a88b643320334435eeb`  
		Last Modified: Tue, 17 Aug 2021 07:29:00 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4502dda560feafee62dfc6f27a87713a3ecc1a3f96af1e86317fba693153296e`  
		Last Modified: Tue, 17 Aug 2021 07:29:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:1.7-alpine`

```console
$ docker pull haproxy@sha256:c61e140064cd6af938e49315547b854fa843509ad4e2660e31e259df40bc3d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:1.7-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:585430cbbec0b6df064587170ed3ac0104e263290ffc6f6d63dfeb3d263437f7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f57f9af8fae5238962a097fdf78d150e3d0cc1160c1495149e0011cdd22cf77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:42:45 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 14 Apr 2021 21:42:45 GMT
ENV HAPROXY_VERSION=1.7.14
# Wed, 14 Apr 2021 21:42:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Wed, 14 Apr 2021 21:42:46 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Wed, 14 Apr 2021 21:42:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Wed, 14 Apr 2021 21:42:57 GMT
STOPSIGNAL SIGUSR1
# Wed, 14 Apr 2021 21:42:57 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Wed, 14 Apr 2021 21:42:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Apr 2021 21:42:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 21:42:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79a8d3da5b7b8e6a180e6fa428bf4a36b8f8bc0e3675927aeb0860a92747561`  
		Last Modified: Wed, 14 Apr 2021 21:44:42 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ba53b9604ae0a19fc162eca377f3de4c0deb844929aa614806d7566b55d42e`  
		Last Modified: Wed, 14 Apr 2021 21:44:43 GMT  
		Size: 745.2 KB (745185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8509370c0a2bc5abc5c0de684ae960d3917ef4fae3de452c52e6a83619de90`  
		Last Modified: Wed, 14 Apr 2021 21:44:42 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bf7494a1e4cf18a66f609c0be15d90d5ec36c6eeb05c116acbd0f00ae4cc08`  
		Last Modified: Wed, 14 Apr 2021 21:44:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:d9ff50855955ad01ade2d0e83cb6d3d6a994d6049cc9edd1f64650eb7fd698c0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3326555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bcb5faeb1698442b56c6ea311daa325d67ecb81cb9a1931e874635a3f160b8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:06 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Fri, 30 Jul 2021 17:50:06 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 00:30:05 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Sat, 31 Jul 2021 00:30:05 GMT
ENV HAPROXY_VERSION=1.7.14
# Sat, 31 Jul 2021 00:30:06 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Sat, 31 Jul 2021 00:30:06 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Sat, 31 Jul 2021 00:30:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Sat, 31 Jul 2021 00:30:17 GMT
STOPSIGNAL SIGUSR1
# Sat, 31 Jul 2021 00:30:18 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Sat, 31 Jul 2021 00:30:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 31 Jul 2021 00:30:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 00:30:20 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaea6ecc8ad8ce34c42ee33d6a25372030df44fcb5dd4b736b87e3b718cc619`  
		Last Modified: Sat, 31 Jul 2021 00:33:24 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db252eaa32a5aac393c01ed64470b2b7f2a3df47ba86803942758b4d5a809300`  
		Last Modified: Sat, 31 Jul 2021 00:33:25 GMT  
		Size: 719.5 KB (719521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95d64a0377ffd186a356094dfaf8cbe18e9993820009646f5e174d0d34732eb`  
		Last Modified: Sat, 31 Jul 2021 00:33:24 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e4bb2bd95eb603a18b475e125fff31ee5ec9e969869d3f9c84f7fadb49f9fb`  
		Last Modified: Sat, 31 Jul 2021 00:33:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:7bfc48ff3ec1730f879bd4a49c025b42dba3ee04d65cb03e3b2f3fd50090a52c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3087784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5b8d65105f15362cb07fc1551f0a7bb949f93dceaf1e40a77dc21f60881a2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:56 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Fri, 30 Jul 2021 18:36:57 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 03:04:47 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Sat, 31 Jul 2021 03:04:48 GMT
ENV HAPROXY_VERSION=1.7.14
# Sat, 31 Jul 2021 03:04:48 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Sat, 31 Jul 2021 03:04:49 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Sat, 31 Jul 2021 03:05:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Sat, 31 Jul 2021 03:05:00 GMT
STOPSIGNAL SIGUSR1
# Sat, 31 Jul 2021 03:05:01 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Sat, 31 Jul 2021 03:05:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 31 Jul 2021 03:05:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 03:05:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40480e974ec7691b9ad0cf86021ed79282f1dfc05c894312797f92546a3a261`  
		Last Modified: Sat, 31 Jul 2021 03:09:33 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55c185ac54a57fb8bf09b10548fa933e0d23ec0c52395bcd1a0f5a18d671cce`  
		Last Modified: Sat, 31 Jul 2021 03:09:33 GMT  
		Size: 676.8 KB (676826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5f4ce1d6cdb2ef48b7186781bfe279f6dc736d5afc0ef16943c878cadb7d91`  
		Last Modified: Sat, 31 Jul 2021 03:09:32 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af907aef58447749664874b5454fc4f9bd665a8c4c1edd4a8de7f651b677d5e8`  
		Last Modified: Sat, 31 Jul 2021 03:09:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:3b4ac8f17466e2cf4a7004feafd5b7cee86b6e30087536f50a9b12d55be267f7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3433872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f64a229633dc7acec39aef12cd9f9c41584d983324089e445db79138c64072`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:09 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Tue, 15 Jun 2021 21:45:09 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 00:43:10 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 16 Jun 2021 00:43:11 GMT
ENV HAPROXY_VERSION=1.7.14
# Wed, 16 Jun 2021 00:43:11 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Wed, 16 Jun 2021 00:43:11 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Wed, 16 Jun 2021 00:43:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Wed, 16 Jun 2021 00:43:21 GMT
STOPSIGNAL SIGUSR1
# Wed, 16 Jun 2021 00:43:21 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Wed, 16 Jun 2021 00:43:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 16 Jun 2021 00:43:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Jun 2021 00:43:22 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb4bfb14121f961d3230a88ceb1a660109674eb24f1088819024b4bd0f8cc7f`  
		Last Modified: Wed, 16 Jun 2021 00:47:43 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef801df0b3ae859e0088c74f1a65addffad28b7c01a66c68d847d5d61204a19d`  
		Last Modified: Wed, 16 Jun 2021 00:47:43 GMT  
		Size: 721.4 KB (721396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68775e45e48621557a43d77a6338d9bb9d0d51b9c6615395c680db228871a5c`  
		Last Modified: Wed, 16 Jun 2021 00:47:43 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387532a80388b0ddbb57e419c705ff30e5864b36174a19124199c509b2d702db`  
		Last Modified: Wed, 16 Jun 2021 00:47:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:7dc566502e4e5dbea0dad303fdc2db644d953f649231265c88f7cbdfa60917d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3554460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690a2df6ec30f31b2a79bdb3b11ff3c1c9e023e4aa2686f5a23e75dc0768be2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 01:58:28 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Thu, 15 Apr 2021 01:58:28 GMT
ENV HAPROXY_VERSION=1.7.14
# Thu, 15 Apr 2021 01:58:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Thu, 15 Apr 2021 01:58:29 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Thu, 15 Apr 2021 01:58:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Thu, 15 Apr 2021 01:58:48 GMT
STOPSIGNAL SIGUSR1
# Thu, 15 Apr 2021 01:58:49 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Thu, 15 Apr 2021 01:58:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 15 Apr 2021 01:58:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 01:58:51 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db648b1d7e93e227e16c4834283e47159a9936ec09ac5b9780d187cb637ad929`  
		Last Modified: Thu, 15 Apr 2021 02:02:01 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6787122459115456ff00e91ee6135f1f51626400da66666caa0d4cb3eb27f2f4`  
		Last Modified: Thu, 15 Apr 2021 02:02:02 GMT  
		Size: 756.9 KB (756887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcb198f7789a97df234ecbc39c81d894b8dfa1d442612d05a674847be086f20`  
		Last Modified: Thu, 15 Apr 2021 02:02:01 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdc70581f273a2514b63c4f025e6c0c6c47a03f53e17515e7c9c87ab1ba177c`  
		Last Modified: Thu, 15 Apr 2021 02:02:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:df37043818310c3477893d9ac0b7b95effcc555926e9259edd8bd86e2c5ebef0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b361ef9535a0475cc56acddfa6e343e0bb00e2ae03c2f5c7adafa76653ee68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 30 Jul 2021 17:25:05 GMT
ADD file:f8b081207f6d35f8ebd06aa471e350644151d183801f678def586d8f37e81366 in / 
# Fri, 30 Jul 2021 17:25:11 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 01:48:58 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Sat, 31 Jul 2021 01:48:59 GMT
ENV HAPROXY_VERSION=1.7.14
# Sat, 31 Jul 2021 01:49:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Sat, 31 Jul 2021 01:49:03 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Sat, 31 Jul 2021 01:49:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Sat, 31 Jul 2021 01:49:20 GMT
STOPSIGNAL SIGUSR1
# Sat, 31 Jul 2021 01:49:21 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Sat, 31 Jul 2021 01:49:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 31 Jul 2021 01:49:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 01:49:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:45707b9629c4ab8c6046680737229218fe844f38d08e5458b24605e1dbfd2709`  
		Last Modified: Wed, 14 Apr 2021 19:32:50 GMT  
		Size: 2.8 MB (2806750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d717e9cbe56630b5ebc48af0076bfbcd23a6e13cd7c411e10fd5af8f6e1ca76a`  
		Last Modified: Sat, 31 Jul 2021 01:52:10 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a461c5e975238263cbadfa3520fce81ccd269097d3a87026c795e20929b974a1`  
		Last Modified: Sat, 31 Jul 2021 01:52:11 GMT  
		Size: 765.4 KB (765351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66333e1221ef508353b13cdc4882f4cd27ec0155ab3b5901e33077e58b8d4e8`  
		Last Modified: Sat, 31 Jul 2021 01:52:10 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cf04caf3a372e6d40dde71d19d7744fa7cb2854b46deb672f61efd2c3c0e0e`  
		Last Modified: Sat, 31 Jul 2021 01:52:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:1a7fd8d305392b12a375a8462cf30fd170cf7ee5c61adbcdea06f538149a7716
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caebb853ea12deddfd890e5e462f0184689e8b73a1dca21f45df5f993b48ab46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 30 Jul 2021 17:41:48 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Fri, 30 Jul 2021 17:41:48 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 23:57:05 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 30 Jul 2021 23:57:05 GMT
ENV HAPROXY_VERSION=1.7.14
# Fri, 30 Jul 2021 23:57:06 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Fri, 30 Jul 2021 23:57:06 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Fri, 30 Jul 2021 23:57:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 30 Jul 2021 23:57:13 GMT
STOPSIGNAL SIGUSR1
# Fri, 30 Jul 2021 23:57:14 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Fri, 30 Jul 2021 23:57:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 30 Jul 2021 23:57:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 Jul 2021 23:57:15 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2427cd91fda616c1d20019a3054ea18500073ee3553bf8ae1d8465d55b7a1eb`  
		Last Modified: Fri, 30 Jul 2021 23:58:16 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff6e498f29a057bddf31486cbb3bf7285c9e47c8ac192e2811542ba6fc3dbc2`  
		Last Modified: Fri, 30 Jul 2021 23:58:16 GMT  
		Size: 775.9 KB (775870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48009381db36161f1e88510b1a32a1aa2ea6992c5e1c5723944da9ea79ace50b`  
		Last Modified: Fri, 30 Jul 2021 23:58:16 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5fbe25bf5c3ad7b060b8c040c89010bf3b39249ea46c2a3ae101dcefc74abf`  
		Last Modified: Fri, 30 Jul 2021 23:58:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:1.7.14`

```console
$ docker pull haproxy@sha256:b6c1b71662c55b2c3401d7b0741737a1a26ad3cce273adcb95702e11782ca169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:1.7.14` - linux; amd64

```console
$ docker pull haproxy@sha256:f40e8a82e9a7583baa6a0f7209c02dc738685cb2eca03bc60641114d0b19291c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32541417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab9d7a65ad83bce27e523ad6340deb3386f1931abf666ead6b5d615b51f8a88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 10:43:34 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 10:51:51 GMT
ENV HAPROXY_VERSION=1.7.14
# Tue, 17 Aug 2021 10:51:52 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Tue, 17 Aug 2021 10:51:52 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Tue, 17 Aug 2021 10:52:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 10:52:46 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 10:52:46 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 10:52:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 10:52:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 10:52:48 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd06683556254cbe06dad4624837c2dcbd2fec67c7fbdd057251f0a207a9315`  
		Last Modified: Tue, 17 Aug 2021 10:53:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a8907733b2e1814f58567544fa320f9fee50f7c2ae6e68c7943f738f4fb40f`  
		Last Modified: Tue, 17 Aug 2021 10:55:15 GMT  
		Size: 5.4 MB (5393465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e858a054a2e23fd834beed9f3ddbb4d672760a1f19f511239d49bbb48235895`  
		Last Modified: Tue, 17 Aug 2021 10:55:13 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2ce652dfe1bd2b640e28045d3d47697eed2a0e11580262fd8358e6c3bd4d9a`  
		Last Modified: Tue, 17 Aug 2021 10:55:13 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.14` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:e5a26fa3795089132ec501d5d25515c7fc9814f19dbbfb491f8ac063f48ce1e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 MB (29901243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d387022ed5cd3bc3c2e34c0ab06a6de79cd1fdcfddcf7b452ee78922090e60dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:56:50 GMT
ADD file:f29260935f1f8b3eef5eb0d5e49dd4cf5370e8731a3f4006d6023724bce09601 in / 
# Tue, 17 Aug 2021 01:56:51 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:39:10 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:45:53 GMT
ENV HAPROXY_VERSION=1.7.14
# Tue, 17 Aug 2021 08:45:53 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Tue, 17 Aug 2021 08:45:54 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Tue, 17 Aug 2021 08:46:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:46:43 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:46:44 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:46:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 08:46:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:46:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3dfab4a5b2accf2d709d8c7d14a42715948ecf2d6da4943a6e2c0de8ae7536a0`  
		Last Modified: Tue, 17 Aug 2021 02:12:42 GMT  
		Size: 24.9 MB (24879063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeabbf4f2af3ef66d78a317a4b3a0704a061a5de2611c57b0bfc47b775c2ed8b`  
		Last Modified: Tue, 17 Aug 2021 08:48:10 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a177a63e39c847952d5d0e2d07ae73e6130eee594bd15f916a760b972ff3ba8f`  
		Last Modified: Tue, 17 Aug 2021 08:50:04 GMT  
		Size: 5.0 MB (5020210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d4bf7aa089a841b638c3983b8543bd4830c622950d8c1a8baff2da1412e6f5`  
		Last Modified: Tue, 17 Aug 2021 08:50:01 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9ed403e2cf4aa127414ca59a2eac19c502f349bde7735c4267cd307d908e52`  
		Last Modified: Tue, 17 Aug 2021 08:50:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.14` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:723e5f94bb63059b4978bde52e07b8022a901d5a9c70c862490362dc46f5a4cf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27640424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099ed80319e59967d48ffd6565919f9b792d439fa9f731f362078eaaee4bb6db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 02:14:25 GMT
ADD file:ca8cc4b509e305fa07662fbf2234ed78f0056569f6ca047305dc02bcd60f1558 in / 
# Tue, 17 Aug 2021 02:14:26 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 16:10:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:18:08 GMT
ENV HAPROXY_VERSION=1.7.14
# Tue, 17 Aug 2021 16:18:08 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Tue, 17 Aug 2021 16:18:09 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Tue, 17 Aug 2021 16:18:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:18:54 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:18:55 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:18:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:18:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:18:57 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:13e3f03410ff211945a725435c13065288d48a8cb740f0530e7588012c2679a4`  
		Last Modified: Tue, 17 Aug 2021 02:30:58 GMT  
		Size: 22.7 MB (22746254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb366ce7907325b732435009125848fb9596a1afdb0f87a8703cdf4342e91a4e`  
		Last Modified: Tue, 17 Aug 2021 16:21:35 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d1a9728625ebf90c638ef880a54b4b4efde83a5a7a2e382669193bd936e0f9`  
		Last Modified: Tue, 17 Aug 2021 16:23:55 GMT  
		Size: 4.9 MB (4892202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d947d1197b8278af3f1ef17a3ef2a0589b092c81199e1a4e9b4531fa5ec7b7`  
		Last Modified: Tue, 17 Aug 2021 16:23:52 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d1a1744cdff50b71fd1ed4ee9ed6ba4e9d24640421370b4f234dff03c9d6ae`  
		Last Modified: Tue, 17 Aug 2021 16:23:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.14` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:b4adf9fe01dd3abda42c56d278586cfd311660c69860e0f70b3aaa11c7e23185
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31198000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddca6c423e16f76864ba1b61792d012e27e97d20a07bc61240e1304c850745b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:12:02 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:17:24 GMT
ENV HAPROXY_VERSION=1.7.14
# Tue, 17 Aug 2021 08:17:24 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Tue, 17 Aug 2021 08:17:25 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Tue, 17 Aug 2021 08:17:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:17:55 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:17:55 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:17:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 08:17:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:17:56 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc63cf29191f59ddbc41452b9edbe5f8145c4370cd74d3981d50a862173029b`  
		Last Modified: Tue, 17 Aug 2021 08:19:14 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90103053f41007e54898ca5581e39ccae7389e64df4d8271f7c1cb8cb765977b`  
		Last Modified: Tue, 17 Aug 2021 08:20:46 GMT  
		Size: 5.3 MB (5280957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586fb707d52466ad852d767549c530d7de019464d4db6861ae7961ffab783696`  
		Last Modified: Tue, 17 Aug 2021 08:20:45 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d0897ef657c46f8192ae262113034ba62e27d9e5238874311a7affc117583d`  
		Last Modified: Tue, 17 Aug 2021 08:20:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.14` - linux; 386

```console
$ docker pull haproxy@sha256:e53d785c8857fd60d26e0199682e320df9c81ef22a126a63abc84a15ba137e5b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 MB (33123623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c975d7d58fea1bddf93ab0737a2a5c43d68cb2361aec6b2b6825b75066202b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:41:16 GMT
ADD file:0418032b55cd0a6dd515ac277fb9f92354397503cab212d446d3a3d8c647a60f in / 
# Tue, 17 Aug 2021 01:41:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 12:14:55 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 12:23:43 GMT
ENV HAPROXY_VERSION=1.7.14
# Tue, 17 Aug 2021 12:23:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Tue, 17 Aug 2021 12:23:43 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Tue, 17 Aug 2021 12:24:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 12:24:20 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 12:24:20 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 12:24:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 12:24:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 12:24:22 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c1c94e1f2523d69effaa463d64fc9962cfc67e2a956f0476c94200e7cf19edf0`  
		Last Modified: Tue, 17 Aug 2021 01:50:57 GMT  
		Size: 27.8 MB (27797627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f804b7c921abcc2fb2904ad2092beefd0224c9bd4cb1cf6477727e6f2bbd7599`  
		Last Modified: Tue, 17 Aug 2021 12:26:22 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e968d632b7ecdca9d50f86e34b80dcf8bc93e2f92c9f6f62559f75a448020b`  
		Last Modified: Tue, 17 Aug 2021 12:28:17 GMT  
		Size: 5.3 MB (5324030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2063a2c5abcf07a4bc200fcd196e03db383f995ef2d02f8be547b2fe4b81b98d`  
		Last Modified: Tue, 17 Aug 2021 12:28:16 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b887b2e8700fb445227f0cfd511782554827370db6073f4f8f7213772e9ea1`  
		Last Modified: Tue, 17 Aug 2021 12:28:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.14` - linux; mips64le

```console
$ docker pull haproxy@sha256:e6d3ab1a1c4319e2df4c4a3473da744774aba55b218bfcc4ce15704ab376e28d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 MB (30842800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920c22be6fc8222e82661d19944ed834018aa1497442d0e2423c98d67011e56d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:12:26 GMT
ADD file:8bd279803ead4ddce8db90b65e89c423f84fbf6042bfbeae8c09486b2e884cde in / 
# Tue, 17 Aug 2021 01:12:27 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:10:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 14:25:28 GMT
ENV HAPROXY_VERSION=1.7.14
# Tue, 17 Aug 2021 14:25:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Tue, 17 Aug 2021 14:25:28 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Tue, 17 Aug 2021 14:26:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 14:26:53 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 14:26:54 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 14:26:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 14:26:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:26:56 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a711e3e37b88ef77496c07ed663bb4270ecba9057eba452a91cc9be0bafb9c32`  
		Last Modified: Tue, 17 Aug 2021 01:21:44 GMT  
		Size: 25.8 MB (25813007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac33edc8b81dffec584b1a7ca6a8abea967f70259323fc62ff423b9c01642e`  
		Last Modified: Tue, 17 Aug 2021 14:27:23 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddda091f7f46634f77e5cd53b439482e105729a0a15555462e3b444be20d2ac`  
		Last Modified: Tue, 17 Aug 2021 14:29:10 GMT  
		Size: 5.0 MB (5027822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3053b3229d607030b1143168534283604b72feb411368145a86986da2e2304`  
		Last Modified: Tue, 17 Aug 2021 14:29:07 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73071e325ceb87c5540533797edf78d802018193a6743953340aa353bf6651a7`  
		Last Modified: Tue, 17 Aug 2021 14:29:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.14` - linux; ppc64le

```console
$ docker pull haproxy@sha256:8475ee3509f16bcfb2eaf7436f016735de26df74d868625788f74fd8dd897db6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36266635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6124622e0285d0dc28f6a0efcf26dea91ef3b97e3532fbb017fdbe339d904b14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:34:13 GMT
ADD file:8b9b12a994a2519f725d1ed1f4ab5a444665262678fd8e6c42cf78f32dacb7fa in / 
# Tue, 17 Aug 2021 01:34:20 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 13:36:19 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 14:17:12 GMT
ENV HAPROXY_VERSION=1.7.14
# Tue, 17 Aug 2021 14:17:20 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Tue, 17 Aug 2021 14:17:24 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Tue, 17 Aug 2021 14:22:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 14:22:45 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 14:22:49 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 14:22:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 14:23:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:23:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c3e09f0e3e7f6fcb741a4c9214b63e341e1d9b53d7689a5ad6ff640b61a82541`  
		Last Modified: Tue, 17 Aug 2021 01:48:22 GMT  
		Size: 30.6 MB (30553721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb7833dc31cf72935b478f7bf90e34f0f2a22d8260da177e4648ac973af1f9c`  
		Last Modified: Tue, 17 Aug 2021 14:24:41 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867889f7912d7d0fee8c07df97a20c80d5000f06e27cf631dd0766eb2447f2ec`  
		Last Modified: Tue, 17 Aug 2021 14:26:27 GMT  
		Size: 5.7 MB (5710929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4d672ce7e9ae8d89f638de3f292411dd33bc87c7db4c438552651130404959`  
		Last Modified: Tue, 17 Aug 2021 14:26:26 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be2439b3af33effe4d2ca5e2591e968eb1f78e5ed63d01d79488c2972654521`  
		Last Modified: Tue, 17 Aug 2021 14:26:26 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.14` - linux; s390x

```console
$ docker pull haproxy@sha256:0166679a3e5b69d94b2599ede49deccc58383a56943e64ee89993ec2e9aea36b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30892015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d78fee778d753c2974dea370009222be4148044c03f8beab87f13698a755fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 07:18:12 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 07:26:33 GMT
ENV HAPROXY_VERSION=1.7.14
# Tue, 17 Aug 2021 07:26:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Tue, 17 Aug 2021 07:26:34 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Tue, 17 Aug 2021 07:26:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 07:27:00 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 07:27:00 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 07:27:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 07:27:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 07:27:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16a2f2a1452470a1d818d8d16934d08d2a57b312ceabcce8c1cfad6c99f00a2`  
		Last Modified: Tue, 17 Aug 2021 07:28:00 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7584ed9c9eebac5bbcca1b1155267a49755d5f13a4b984247ec17cba4415d58c`  
		Last Modified: Tue, 17 Aug 2021 07:29:00 GMT  
		Size: 5.1 MB (5129187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b378b86781f56ce622911bf77656081f2f43b515f52e0a88b643320334435eeb`  
		Last Modified: Tue, 17 Aug 2021 07:29:00 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4502dda560feafee62dfc6f27a87713a3ecc1a3f96af1e86317fba693153296e`  
		Last Modified: Tue, 17 Aug 2021 07:29:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:1.7.14-alpine`

```console
$ docker pull haproxy@sha256:c61e140064cd6af938e49315547b854fa843509ad4e2660e31e259df40bc3d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:1.7.14-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:585430cbbec0b6df064587170ed3ac0104e263290ffc6f6d63dfeb3d263437f7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f57f9af8fae5238962a097fdf78d150e3d0cc1160c1495149e0011cdd22cf77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:42:45 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 14 Apr 2021 21:42:45 GMT
ENV HAPROXY_VERSION=1.7.14
# Wed, 14 Apr 2021 21:42:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Wed, 14 Apr 2021 21:42:46 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Wed, 14 Apr 2021 21:42:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Wed, 14 Apr 2021 21:42:57 GMT
STOPSIGNAL SIGUSR1
# Wed, 14 Apr 2021 21:42:57 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Wed, 14 Apr 2021 21:42:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Apr 2021 21:42:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 21:42:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79a8d3da5b7b8e6a180e6fa428bf4a36b8f8bc0e3675927aeb0860a92747561`  
		Last Modified: Wed, 14 Apr 2021 21:44:42 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ba53b9604ae0a19fc162eca377f3de4c0deb844929aa614806d7566b55d42e`  
		Last Modified: Wed, 14 Apr 2021 21:44:43 GMT  
		Size: 745.2 KB (745185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8509370c0a2bc5abc5c0de684ae960d3917ef4fae3de452c52e6a83619de90`  
		Last Modified: Wed, 14 Apr 2021 21:44:42 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bf7494a1e4cf18a66f609c0be15d90d5ec36c6eeb05c116acbd0f00ae4cc08`  
		Last Modified: Wed, 14 Apr 2021 21:44:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.14-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:d9ff50855955ad01ade2d0e83cb6d3d6a994d6049cc9edd1f64650eb7fd698c0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3326555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bcb5faeb1698442b56c6ea311daa325d67ecb81cb9a1931e874635a3f160b8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:06 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Fri, 30 Jul 2021 17:50:06 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 00:30:05 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Sat, 31 Jul 2021 00:30:05 GMT
ENV HAPROXY_VERSION=1.7.14
# Sat, 31 Jul 2021 00:30:06 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Sat, 31 Jul 2021 00:30:06 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Sat, 31 Jul 2021 00:30:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Sat, 31 Jul 2021 00:30:17 GMT
STOPSIGNAL SIGUSR1
# Sat, 31 Jul 2021 00:30:18 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Sat, 31 Jul 2021 00:30:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 31 Jul 2021 00:30:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 00:30:20 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaea6ecc8ad8ce34c42ee33d6a25372030df44fcb5dd4b736b87e3b718cc619`  
		Last Modified: Sat, 31 Jul 2021 00:33:24 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db252eaa32a5aac393c01ed64470b2b7f2a3df47ba86803942758b4d5a809300`  
		Last Modified: Sat, 31 Jul 2021 00:33:25 GMT  
		Size: 719.5 KB (719521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95d64a0377ffd186a356094dfaf8cbe18e9993820009646f5e174d0d34732eb`  
		Last Modified: Sat, 31 Jul 2021 00:33:24 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e4bb2bd95eb603a18b475e125fff31ee5ec9e969869d3f9c84f7fadb49f9fb`  
		Last Modified: Sat, 31 Jul 2021 00:33:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.14-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:7bfc48ff3ec1730f879bd4a49c025b42dba3ee04d65cb03e3b2f3fd50090a52c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3087784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5b8d65105f15362cb07fc1551f0a7bb949f93dceaf1e40a77dc21f60881a2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:56 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Fri, 30 Jul 2021 18:36:57 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 03:04:47 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Sat, 31 Jul 2021 03:04:48 GMT
ENV HAPROXY_VERSION=1.7.14
# Sat, 31 Jul 2021 03:04:48 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Sat, 31 Jul 2021 03:04:49 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Sat, 31 Jul 2021 03:05:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Sat, 31 Jul 2021 03:05:00 GMT
STOPSIGNAL SIGUSR1
# Sat, 31 Jul 2021 03:05:01 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Sat, 31 Jul 2021 03:05:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 31 Jul 2021 03:05:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 03:05:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40480e974ec7691b9ad0cf86021ed79282f1dfc05c894312797f92546a3a261`  
		Last Modified: Sat, 31 Jul 2021 03:09:33 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55c185ac54a57fb8bf09b10548fa933e0d23ec0c52395bcd1a0f5a18d671cce`  
		Last Modified: Sat, 31 Jul 2021 03:09:33 GMT  
		Size: 676.8 KB (676826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5f4ce1d6cdb2ef48b7186781bfe279f6dc736d5afc0ef16943c878cadb7d91`  
		Last Modified: Sat, 31 Jul 2021 03:09:32 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af907aef58447749664874b5454fc4f9bd665a8c4c1edd4a8de7f651b677d5e8`  
		Last Modified: Sat, 31 Jul 2021 03:09:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.14-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:3b4ac8f17466e2cf4a7004feafd5b7cee86b6e30087536f50a9b12d55be267f7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3433872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f64a229633dc7acec39aef12cd9f9c41584d983324089e445db79138c64072`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:09 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Tue, 15 Jun 2021 21:45:09 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 00:43:10 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 16 Jun 2021 00:43:11 GMT
ENV HAPROXY_VERSION=1.7.14
# Wed, 16 Jun 2021 00:43:11 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Wed, 16 Jun 2021 00:43:11 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Wed, 16 Jun 2021 00:43:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Wed, 16 Jun 2021 00:43:21 GMT
STOPSIGNAL SIGUSR1
# Wed, 16 Jun 2021 00:43:21 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Wed, 16 Jun 2021 00:43:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 16 Jun 2021 00:43:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Jun 2021 00:43:22 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb4bfb14121f961d3230a88ceb1a660109674eb24f1088819024b4bd0f8cc7f`  
		Last Modified: Wed, 16 Jun 2021 00:47:43 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef801df0b3ae859e0088c74f1a65addffad28b7c01a66c68d847d5d61204a19d`  
		Last Modified: Wed, 16 Jun 2021 00:47:43 GMT  
		Size: 721.4 KB (721396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68775e45e48621557a43d77a6338d9bb9d0d51b9c6615395c680db228871a5c`  
		Last Modified: Wed, 16 Jun 2021 00:47:43 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387532a80388b0ddbb57e419c705ff30e5864b36174a19124199c509b2d702db`  
		Last Modified: Wed, 16 Jun 2021 00:47:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.14-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:7dc566502e4e5dbea0dad303fdc2db644d953f649231265c88f7cbdfa60917d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3554460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690a2df6ec30f31b2a79bdb3b11ff3c1c9e023e4aa2686f5a23e75dc0768be2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 01:58:28 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Thu, 15 Apr 2021 01:58:28 GMT
ENV HAPROXY_VERSION=1.7.14
# Thu, 15 Apr 2021 01:58:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Thu, 15 Apr 2021 01:58:29 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Thu, 15 Apr 2021 01:58:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Thu, 15 Apr 2021 01:58:48 GMT
STOPSIGNAL SIGUSR1
# Thu, 15 Apr 2021 01:58:49 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Thu, 15 Apr 2021 01:58:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 15 Apr 2021 01:58:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 01:58:51 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db648b1d7e93e227e16c4834283e47159a9936ec09ac5b9780d187cb637ad929`  
		Last Modified: Thu, 15 Apr 2021 02:02:01 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6787122459115456ff00e91ee6135f1f51626400da66666caa0d4cb3eb27f2f4`  
		Last Modified: Thu, 15 Apr 2021 02:02:02 GMT  
		Size: 756.9 KB (756887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcb198f7789a97df234ecbc39c81d894b8dfa1d442612d05a674847be086f20`  
		Last Modified: Thu, 15 Apr 2021 02:02:01 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdc70581f273a2514b63c4f025e6c0c6c47a03f53e17515e7c9c87ab1ba177c`  
		Last Modified: Thu, 15 Apr 2021 02:02:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.14-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:df37043818310c3477893d9ac0b7b95effcc555926e9259edd8bd86e2c5ebef0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b361ef9535a0475cc56acddfa6e343e0bb00e2ae03c2f5c7adafa76653ee68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 30 Jul 2021 17:25:05 GMT
ADD file:f8b081207f6d35f8ebd06aa471e350644151d183801f678def586d8f37e81366 in / 
# Fri, 30 Jul 2021 17:25:11 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 01:48:58 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Sat, 31 Jul 2021 01:48:59 GMT
ENV HAPROXY_VERSION=1.7.14
# Sat, 31 Jul 2021 01:49:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Sat, 31 Jul 2021 01:49:03 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Sat, 31 Jul 2021 01:49:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Sat, 31 Jul 2021 01:49:20 GMT
STOPSIGNAL SIGUSR1
# Sat, 31 Jul 2021 01:49:21 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Sat, 31 Jul 2021 01:49:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 31 Jul 2021 01:49:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 01:49:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:45707b9629c4ab8c6046680737229218fe844f38d08e5458b24605e1dbfd2709`  
		Last Modified: Wed, 14 Apr 2021 19:32:50 GMT  
		Size: 2.8 MB (2806750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d717e9cbe56630b5ebc48af0076bfbcd23a6e13cd7c411e10fd5af8f6e1ca76a`  
		Last Modified: Sat, 31 Jul 2021 01:52:10 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a461c5e975238263cbadfa3520fce81ccd269097d3a87026c795e20929b974a1`  
		Last Modified: Sat, 31 Jul 2021 01:52:11 GMT  
		Size: 765.4 KB (765351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66333e1221ef508353b13cdc4882f4cd27ec0155ab3b5901e33077e58b8d4e8`  
		Last Modified: Sat, 31 Jul 2021 01:52:10 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cf04caf3a372e6d40dde71d19d7744fa7cb2854b46deb672f61efd2c3c0e0e`  
		Last Modified: Sat, 31 Jul 2021 01:52:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.7.14-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:1a7fd8d305392b12a375a8462cf30fd170cf7ee5c61adbcdea06f538149a7716
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caebb853ea12deddfd890e5e462f0184689e8b73a1dca21f45df5f993b48ab46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 30 Jul 2021 17:41:48 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Fri, 30 Jul 2021 17:41:48 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 23:57:05 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 30 Jul 2021 23:57:05 GMT
ENV HAPROXY_VERSION=1.7.14
# Fri, 30 Jul 2021 23:57:06 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.7/src/haproxy-1.7.14.tar.gz
# Fri, 30 Jul 2021 23:57:06 GMT
ENV HAPROXY_SHA256=1f9fb6c5a342803037a622c7dd04702b0d010a88b5c3922cd3da71a34f3377a4
# Fri, 30 Jul 2021 23:57:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		CFLAGS+="-Wno-address-of-packed-member" 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 30 Jul 2021 23:57:13 GMT
STOPSIGNAL SIGUSR1
# Fri, 30 Jul 2021 23:57:14 GMT
COPY file:9a05f2c8b43e780abf69d813f7c45613cced5481a65611bf8127c6f222dff4e3 in /usr/local/bin/ 
# Fri, 30 Jul 2021 23:57:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 30 Jul 2021 23:57:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 Jul 2021 23:57:15 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2427cd91fda616c1d20019a3054ea18500073ee3553bf8ae1d8465d55b7a1eb`  
		Last Modified: Fri, 30 Jul 2021 23:58:16 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff6e498f29a057bddf31486cbb3bf7285c9e47c8ac192e2811542ba6fc3dbc2`  
		Last Modified: Fri, 30 Jul 2021 23:58:16 GMT  
		Size: 775.9 KB (775870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48009381db36161f1e88510b1a32a1aa2ea6992c5e1c5723944da9ea79ace50b`  
		Last Modified: Fri, 30 Jul 2021 23:58:16 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5fbe25bf5c3ad7b060b8c040c89010bf3b39249ea46c2a3ae101dcefc74abf`  
		Last Modified: Fri, 30 Jul 2021 23:58:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:1.8`

```console
$ docker pull haproxy@sha256:10405165016bbdf5040aa5d762710ba8767c42cc19d85be7f624645e10668f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:1.8` - linux; amd64

```console
$ docker pull haproxy@sha256:49c9bcdebd55fc3cd37805770fc8fa36a32585091ac3d20c4882ab18cd8e923d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33800249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2afa0f4378c8c2836da31aec9f2cd769bcc456028a1d70780a241037fc70250`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 10:43:34 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 10:50:35 GMT
ENV HAPROXY_VERSION=1.8.30
# Tue, 17 Aug 2021 10:50:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Tue, 17 Aug 2021 10:50:36 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Tue, 17 Aug 2021 10:51:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 10:51:41 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 10:51:41 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 10:51:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 10:51:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 10:51:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd06683556254cbe06dad4624837c2dcbd2fec67c7fbdd057251f0a207a9315`  
		Last Modified: Tue, 17 Aug 2021 10:53:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a6f7a10fa32e0c44f1bfa1c0eb9be0023745ce71c715b8bca2bf9b1fcc5396`  
		Last Modified: Tue, 17 Aug 2021 10:55:02 GMT  
		Size: 6.7 MB (6652316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b5103e466612c2c86ccbc1dc089e4e43ed2f5255bc36d05251e1c9de2a230c`  
		Last Modified: Tue, 17 Aug 2021 10:55:01 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a6d55663076df62c72b8edb76440e5dc67903125476b7a1c7d7cfd2e052fa8`  
		Last Modified: Tue, 17 Aug 2021 10:55:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:e2406cf33141a98310092840566a6636250301da49d64bab0119ecb32ab6bc0f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31112236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fbd0c97aee6de1014d7327adf932afc0671dfd92cd44e78a1ab9623bf7cca9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:56:50 GMT
ADD file:f29260935f1f8b3eef5eb0d5e49dd4cf5370e8731a3f4006d6023724bce09601 in / 
# Tue, 17 Aug 2021 01:56:51 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:39:10 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:44:46 GMT
ENV HAPROXY_VERSION=1.8.30
# Tue, 17 Aug 2021 08:44:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Tue, 17 Aug 2021 08:44:47 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Tue, 17 Aug 2021 08:45:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:45:39 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:45:39 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:45:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 08:45:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:45:42 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3dfab4a5b2accf2d709d8c7d14a42715948ecf2d6da4943a6e2c0de8ae7536a0`  
		Last Modified: Tue, 17 Aug 2021 02:12:42 GMT  
		Size: 24.9 MB (24879063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeabbf4f2af3ef66d78a317a4b3a0704a061a5de2611c57b0bfc47b775c2ed8b`  
		Last Modified: Tue, 17 Aug 2021 08:48:10 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6332b82bbe433e45e063bc46fb662f4595f0f89b32319e7192f14c7608beaa`  
		Last Modified: Tue, 17 Aug 2021 08:49:50 GMT  
		Size: 6.2 MB (6231227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b099ab28cce251961e4a2d9aa9bcd175436d533aaf95f981817add79a0bb89af`  
		Last Modified: Tue, 17 Aug 2021 08:49:46 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112180ec06b41530f9b1c5e4f958d9d4ff0877c75a34b9b2be728dc3c9a0e491`  
		Last Modified: Tue, 17 Aug 2021 08:49:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:8a2aaa4c43ad9e63d2b0e10c13a62053e935851099f99fa73ce0458108317de2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28819094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a839724d329d9a91c106368c118749676f1523e54e78dae55403d8ce7a36df5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 02:14:25 GMT
ADD file:ca8cc4b509e305fa07662fbf2234ed78f0056569f6ca047305dc02bcd60f1558 in / 
# Tue, 17 Aug 2021 02:14:26 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 16:10:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:16:53 GMT
ENV HAPROXY_VERSION=1.8.30
# Tue, 17 Aug 2021 16:16:53 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Tue, 17 Aug 2021 16:16:54 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Tue, 17 Aug 2021 16:17:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:17:41 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:17:42 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:17:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:17:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:17:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:13e3f03410ff211945a725435c13065288d48a8cb740f0530e7588012c2679a4`  
		Last Modified: Tue, 17 Aug 2021 02:30:58 GMT  
		Size: 22.7 MB (22746254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb366ce7907325b732435009125848fb9596a1afdb0f87a8703cdf4342e91a4e`  
		Last Modified: Tue, 17 Aug 2021 16:21:35 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d7703e699ab32fa41edeee749507d138ee19957ce1cdaf38d22911f1912220`  
		Last Modified: Tue, 17 Aug 2021 16:23:33 GMT  
		Size: 6.1 MB (6070894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e83ad3304ad9c9faa5dc77cf668fcbdb7f36293fbba2114795617e98d5a6e3`  
		Last Modified: Tue, 17 Aug 2021 16:23:30 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5581cbf3515ace3827998b3992d7c18ca2aeb3e434650ae060583d7dda7675c1`  
		Last Modified: Tue, 17 Aug 2021 16:23:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:b3443efc642e9fbd8ba7f286f134e77c75684cb9d3f9c5deeea65d099408d938
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32370800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac150f16c650d71b54354d78ae5ac2692148ad8214cc671bdcebd3e07a5723c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:12:02 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:16:43 GMT
ENV HAPROXY_VERSION=1.8.30
# Tue, 17 Aug 2021 08:16:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Tue, 17 Aug 2021 08:16:43 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Tue, 17 Aug 2021 08:17:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:17:12 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:17:12 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:17:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 08:17:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:17:13 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc63cf29191f59ddbc41452b9edbe5f8145c4370cd74d3981d50a862173029b`  
		Last Modified: Tue, 17 Aug 2021 08:19:14 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f30e617b2ec3b128522709a5ef45fb8511720085bb9f56408de746dc69219e`  
		Last Modified: Tue, 17 Aug 2021 08:20:33 GMT  
		Size: 6.5 MB (6453782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae49d2e8fb6c082bfe198ad028053fc47460c9b56350d41bb1fd302fd579b1a`  
		Last Modified: Tue, 17 Aug 2021 08:20:31 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69fc5fcb63ad9c06b0360077809d3750efa2ade439a8d97df35539eee1685b9`  
		Last Modified: Tue, 17 Aug 2021 08:20:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8` - linux; 386

```console
$ docker pull haproxy@sha256:bbc52d41708f0d296625cbf528e18c0d32c113bf4ac5fa5824c097dc91c6ae7c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34376383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f94955774be42d24f66b61400de0e20575ad77ac657232733b44f076b2ddaa3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:41:16 GMT
ADD file:0418032b55cd0a6dd515ac277fb9f92354397503cab212d446d3a3d8c647a60f in / 
# Tue, 17 Aug 2021 01:41:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 12:14:55 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 12:22:46 GMT
ENV HAPROXY_VERSION=1.8.30
# Tue, 17 Aug 2021 12:22:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Tue, 17 Aug 2021 12:22:47 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Tue, 17 Aug 2021 12:23:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 12:23:29 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 12:23:30 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 12:23:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 12:23:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 12:23:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c1c94e1f2523d69effaa463d64fc9962cfc67e2a956f0476c94200e7cf19edf0`  
		Last Modified: Tue, 17 Aug 2021 01:50:57 GMT  
		Size: 27.8 MB (27797627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f804b7c921abcc2fb2904ad2092beefd0224c9bd4cb1cf6477727e6f2bbd7599`  
		Last Modified: Tue, 17 Aug 2021 12:26:22 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc90821ea3e08a6b2ffacf914890b8f22d9dcec1ad5850a77813a1c9c4fd6993`  
		Last Modified: Tue, 17 Aug 2021 12:28:03 GMT  
		Size: 6.6 MB (6576813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5acf8fa1f5b6cf4a91fddf31c61af95f657da3d834d36f4e32f0d46f282f69`  
		Last Modified: Tue, 17 Aug 2021 12:28:01 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b866b133478c5ddea5b0789b99a0d185158cbb285f2f533fd50becd510daea5`  
		Last Modified: Tue, 17 Aug 2021 12:28:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8` - linux; mips64le

```console
$ docker pull haproxy@sha256:40c5886a502b4d8dee4231cc3f163ad34e299d82a13b59e651e9f88d99369f3a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31958357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05cb64bfcd11f6dc654becb8cf265c82a452a342afc1638ece8387c3f9943de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:12:26 GMT
ADD file:8bd279803ead4ddce8db90b65e89c423f84fbf6042bfbeae8c09486b2e884cde in / 
# Tue, 17 Aug 2021 01:12:27 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:10:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 14:23:32 GMT
ENV HAPROXY_VERSION=1.8.30
# Tue, 17 Aug 2021 14:23:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Tue, 17 Aug 2021 14:23:32 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Tue, 17 Aug 2021 14:25:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 14:25:13 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 14:25:13 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 14:25:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 14:25:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:25:15 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a711e3e37b88ef77496c07ed663bb4270ecba9057eba452a91cc9be0bafb9c32`  
		Last Modified: Tue, 17 Aug 2021 01:21:44 GMT  
		Size: 25.8 MB (25813007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac33edc8b81dffec584b1a7ca6a8abea967f70259323fc62ff423b9c01642e`  
		Last Modified: Tue, 17 Aug 2021 14:27:23 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a482badf4699073b1e8016fb3736e273192234996c698dcd8d531acb55a1c8e0`  
		Last Modified: Tue, 17 Aug 2021 14:28:57 GMT  
		Size: 6.1 MB (6143401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3863c167bb424ef17263655e8f88117f2e43c4d4fca90a26519c9e590ee11159`  
		Last Modified: Tue, 17 Aug 2021 14:28:52 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01538b4844c786d24cf3e2d63bafa653999614a8571c3fde53dc8eda4e568920`  
		Last Modified: Tue, 17 Aug 2021 14:28:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8` - linux; ppc64le

```console
$ docker pull haproxy@sha256:713c08f78ccc1a48bf579bef9a085f632ec039d8947802e487172db0e6523d2c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37499315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a265f2b9f939709c00f838a0e96dae95e2406d9e27c436797a03732fd409b79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:34:13 GMT
ADD file:8b9b12a994a2519f725d1ed1f4ab5a444665262678fd8e6c42cf78f32dacb7fa in / 
# Tue, 17 Aug 2021 01:34:20 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 13:36:19 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 14:11:10 GMT
ENV HAPROXY_VERSION=1.8.30
# Tue, 17 Aug 2021 14:11:15 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Tue, 17 Aug 2021 14:11:23 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Tue, 17 Aug 2021 14:16:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 14:16:37 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 14:16:40 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 14:16:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 14:16:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:16:59 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c3e09f0e3e7f6fcb741a4c9214b63e341e1d9b53d7689a5ad6ff640b61a82541`  
		Last Modified: Tue, 17 Aug 2021 01:48:22 GMT  
		Size: 30.6 MB (30553721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb7833dc31cf72935b478f7bf90e34f0f2a22d8260da177e4648ac973af1f9c`  
		Last Modified: Tue, 17 Aug 2021 14:24:41 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f9e0316e0cf9c9bd723c914436cbbf3d4eef9b5fedb8bc2e38b9e23947e67d`  
		Last Modified: Tue, 17 Aug 2021 14:26:11 GMT  
		Size: 6.9 MB (6943631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3641a78876a225e627c2f80a5fdfc466e2dd5180bd6bbddd138a1c86d5eed129`  
		Last Modified: Tue, 17 Aug 2021 14:26:09 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eccd50492e1cd0ea05b7f336c7b9ce367cc1dd2baa388e61a27c5f8deab9948e`  
		Last Modified: Tue, 17 Aug 2021 14:26:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8` - linux; s390x

```console
$ docker pull haproxy@sha256:230713a8d26f462a8ab023c0ce0f7aec8394284ff39fb2a9038e6dd7d0df8cb5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31995544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c26efac7113a88d93ceec256d9051a59eb4d5774ce3bb2359f84080a7e48f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 07:18:12 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 07:25:15 GMT
ENV HAPROXY_VERSION=1.8.30
# Tue, 17 Aug 2021 07:25:16 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Tue, 17 Aug 2021 07:25:16 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Tue, 17 Aug 2021 07:25:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 07:25:50 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 07:25:50 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 07:25:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 07:25:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 07:25:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16a2f2a1452470a1d818d8d16934d08d2a57b312ceabcce8c1cfad6c99f00a2`  
		Last Modified: Tue, 17 Aug 2021 07:28:00 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde815120b599af00d27bc664e5f337b839d6a1b90488f887b4f7e9d7272e9b0`  
		Last Modified: Tue, 17 Aug 2021 07:28:51 GMT  
		Size: 6.2 MB (6232742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13cf0f8cd42be7e7a1d3b0d8d98ed182fc83dc5b16c0b91a44958e182ea1687`  
		Last Modified: Tue, 17 Aug 2021 07:28:50 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2789f33d279538ab7c218ca54178c2b5202a5b1e2c1c5b286410edc4fb90f15f`  
		Last Modified: Tue, 17 Aug 2021 07:28:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:1.8-alpine`

```console
$ docker pull haproxy@sha256:e636afbecc760b34bb1cff2d2d9f47f0fe87f2a1cf77ffbd25a6605b80d3005b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:1.8-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:f5e1be9d9be0348431e67f17ce6206b50a24f903233337ede36f70f21546f6d0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6786701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a904a6a2f1c1ffb16601be820758da6a3b0cf1fa0142fae0f5b5822c061b7d6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:43:18 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 19:49:57 GMT
ENV HAPROXY_VERSION=1.8.30
# Fri, 06 Aug 2021 19:49:57 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Fri, 06 Aug 2021 19:49:57 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Fri, 06 Aug 2021 19:50:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 19:50:38 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 19:50:38 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 19:50:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 19:50:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 19:50:40 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22138861da3ab6ae8583cf62942545e1bb75874501f4a8d45d13a38c848a908`  
		Last Modified: Fri, 06 Aug 2021 19:51:27 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a5fd354d11cc818598bf04ae789dcabc3ee2c1b39cc2ccf6042385707c251c`  
		Last Modified: Fri, 06 Aug 2021 19:52:33 GMT  
		Size: 4.0 MB (3971927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106d5a39ebd3941a4b1cad55a15b928bde429faadf690a9a6b8ba68cf8971895`  
		Last Modified: Fri, 06 Aug 2021 19:52:32 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c577c5149c37ac2f2880fc88a1d896b8c0adf4df7f4adc596f2b3962517348d`  
		Last Modified: Fri, 06 Aug 2021 19:52:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:ff198c5e30af586cfb08a1637cf80c53935feace64fc6175b1b64dc369a5b105
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6473485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a374b30833a3cc5cf22e553da0a343c7a3be75c418cdb28145f582a144d9e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:49:32 GMT
ADD file:7f2c7deda009eabdcbbdccb11e854043d32c498e64e7e1ca02165d7bb4261d39 in / 
# Fri, 06 Aug 2021 17:49:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:15:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 18:18:59 GMT
ENV HAPROXY_VERSION=1.8.30
# Fri, 06 Aug 2021 18:18:59 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Fri, 06 Aug 2021 18:19:00 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Fri, 06 Aug 2021 18:19:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 18:19:24 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 18:19:25 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 18:19:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 18:19:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 18:19:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f465bb3e9fcd0c42f936ecc566c6e40353c00f3089b2b2c2ea1663c30f89d3ab`  
		Last Modified: Fri, 06 Aug 2021 17:51:00 GMT  
		Size: 2.6 MB (2626350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332ccafb58fe1d8ed3d3d5ad9c01adba33d922f28a398285d2eb67fed7c8bee8`  
		Last Modified: Fri, 06 Aug 2021 18:20:57 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acb590fd7a3d2c22e077debe0adb8f59ab5aa312316fa35de06be3db4b05014`  
		Last Modified: Fri, 06 Aug 2021 18:22:29 GMT  
		Size: 3.8 MB (3845364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53099ed6f8a71dcad7b991ee6e92f63a621385d0ab79af696504ac4bdd47874a`  
		Last Modified: Fri, 06 Aug 2021 18:22:26 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c5e9bb4fe6f965d657fc527e9030a83cd9e5af5a8292d86a81aa099a0bed5e`  
		Last Modified: Fri, 06 Aug 2021 18:22:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:48cc927b413bd1ecc7dcf2b186e0398a64a787c749c568f3bf781a92f4a48e07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6214143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ac9ef4d97188e723c9ab285ee1c7d85a4d7ad4585056b8fe23887048eea17f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:57:32 GMT
ADD file:3a35ff3ac0d80289d419a4d6d8319610c38e1936d296addafb9aaf506946230f in / 
# Fri, 06 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:54:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 19:59:36 GMT
ENV HAPROXY_VERSION=1.8.30
# Fri, 06 Aug 2021 19:59:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Fri, 06 Aug 2021 19:59:37 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Fri, 06 Aug 2021 20:00:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 20:00:01 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 20:00:02 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 20:00:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 20:00:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 20:00:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4ee0caa23b369b04827640a4be298bf4ff7bacd030c77e915f5d7fb8f987594a`  
		Last Modified: Fri, 06 Aug 2021 17:58:57 GMT  
		Size: 2.4 MB (2429359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548ff9918828f96cb9a5e5656ea589d79e6fb1d7b9f0d693feff2dbefc6929fe`  
		Last Modified: Fri, 06 Aug 2021 20:02:54 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2421cef4cbe218a8caf6b18f05d5f404c64d5ac5b4d714edee3d891eb1bd2cda`  
		Last Modified: Fri, 06 Aug 2021 20:04:40 GMT  
		Size: 3.8 MB (3783012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa8f52f106be61ce21271232331a5c4ddba088b395131da38bf197c816f6040`  
		Last Modified: Fri, 06 Aug 2021 20:04:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a88386f3a5a10c726e32652dd04876b4bfb2ae5c47f20e6b764a0358ca68ebe`  
		Last Modified: Fri, 06 Aug 2021 20:04:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:2e269c0dd8f2ded7deb5b3da0ff486fc90fe8a02fb058bab4d0c2a7f1c788f51
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6641612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d198bfd1dfe729ae77344af23d756b7a521da2d2bb3d67e095d7cb0cd45a86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:39:26 GMT
ADD file:1a8fd1066485e1261462e689c1a072f010c1d3be904b73ef2b84128fac652951 in / 
# Fri, 06 Aug 2021 17:39:27 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:38:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 18:44:10 GMT
ENV HAPROXY_VERSION=1.8.30
# Fri, 06 Aug 2021 18:44:10 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Fri, 06 Aug 2021 18:44:11 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Fri, 06 Aug 2021 18:44:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 18:44:40 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 18:44:41 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 18:44:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 18:44:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 18:44:42 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fd3acdcea5682abced546ec19fb6ebee725c5184e5d91614c469c0a79e67f2d0`  
		Last Modified: Fri, 06 Aug 2021 17:40:12 GMT  
		Size: 2.7 MB (2710613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a23793c1bba0796c0f469305ee92dd0f1cb8299963e4da4249d0f5aa2fcea0`  
		Last Modified: Fri, 06 Aug 2021 18:46:06 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5464479783659679ddef52252cfff218a3ea00eb47d4144096c54145fb7b8f7`  
		Last Modified: Fri, 06 Aug 2021 18:47:26 GMT  
		Size: 3.9 MB (3929233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0ba81491a27348f40013accce5be9bb9104f5484daab1d36939911b9f22d06`  
		Last Modified: Fri, 06 Aug 2021 18:47:25 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915431d67be340c0c7abab56573dd4dfa9cd05201106bbe98dcb3460b0955726`  
		Last Modified: Fri, 06 Aug 2021 18:47:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:f07aac88939a1ff7fa8b26caeacd68aaab432800759c1eeff4ca3008e7b49c0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6709098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd5fce8a83efa395dca43758a79741513231dd11d532788473425ccedaf1d90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:38:26 GMT
ADD file:bafaec4a54d6cef99b5f3660d074a3d2251e4d4bd09df9ea65f33e9bffb7d88d in / 
# Fri, 06 Aug 2021 17:38:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:19:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 19:29:15 GMT
ENV HAPROXY_VERSION=1.8.30
# Fri, 06 Aug 2021 19:29:15 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Fri, 06 Aug 2021 19:29:16 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Fri, 06 Aug 2021 19:30:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 19:30:21 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 19:30:21 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 19:30:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 19:30:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 19:30:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:935703e1179e32e201e4a36d5664d58299dc8e7bcac197b70c295c0a59216db1`  
		Last Modified: Fri, 06 Aug 2021 17:39:15 GMT  
		Size: 2.8 MB (2821910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695b2822110160b402b8f359bb19d954a46a6ead94f868feba7d00f5a10e50e`  
		Last Modified: Fri, 06 Aug 2021 19:32:18 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7df0172c1b292c4823dc8f07519e1ff946b807f6710a7f09dcc0fbc921243f3`  
		Last Modified: Fri, 06 Aug 2021 19:33:50 GMT  
		Size: 3.9 MB (3885421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8eae33ef2ea20ba682bf22f964f3e28f00fbf2dc7e90339bfcfd922e418a77`  
		Last Modified: Fri, 06 Aug 2021 19:33:49 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccddaa60700d05d4ed03cb4cb69dbfe91bb86ece69442eac025203e2e395b67`  
		Last Modified: Fri, 06 Aug 2021 19:33:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:be483e473840a03cb4ab5ec93f46ed662bad8cae560762ea3533ec45e52763b3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6949175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8c165c9006f0ae0092b6cd8f0d4d44c43fe8ddda7e5e7e4c1b32e37d16c928`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:17:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 21:24:57 GMT
ENV HAPROXY_VERSION=1.8.30
# Fri, 06 Aug 2021 21:24:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Fri, 06 Aug 2021 21:25:02 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Fri, 06 Aug 2021 21:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 21:25:38 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 21:25:41 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 21:25:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 21:25:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 21:26:02 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d374dad070e00fdb493e29a3aa64b375dbec801497e01d3b8ddbf7cc967634cb`  
		Last Modified: Fri, 06 Aug 2021 21:27:30 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926fac922b7f30c135d54663b5fef5947ec8e3bbefddc68cf05b2718933137de`  
		Last Modified: Fri, 06 Aug 2021 21:28:51 GMT  
		Size: 4.1 MB (4136257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1643c103dd6aef93e4cdd049b1199fb99749ec01077f3d7f23ff22c53c33864`  
		Last Modified: Fri, 06 Aug 2021 21:28:50 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d6dc7b43bfb8be4890b7c4d4ad687056a7cc893e94e42dd70bb227eea868ce`  
		Last Modified: Fri, 06 Aug 2021 21:28:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:56ab7dd8abed67c02b519cf7e49892f4b44431d493327f3aa9c26dd80841daa9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6469626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8e380d640dae4d7b5e8eda393c2992736478cf6bda09d77675c7938d34db2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:54:24 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 14 Apr 2021 20:57:46 GMT
ENV HAPROXY_VERSION=1.8.30
# Wed, 14 Apr 2021 20:57:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Wed, 14 Apr 2021 20:57:46 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Wed, 14 Apr 2021 20:58:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Wed, 14 Apr 2021 20:58:10 GMT
STOPSIGNAL SIGUSR1
# Wed, 14 Apr 2021 20:58:10 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 14 Apr 2021 20:58:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Apr 2021 20:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 20:58:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267275aba58470c82626189a59be76cd169bd245568e2f2545ed1ee64ff8a8ff`  
		Last Modified: Wed, 14 Apr 2021 20:59:06 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba85d625d72596824b2a38b34880512b279ac65dacc4bb0255d3a8ba92ec8d1`  
		Last Modified: Wed, 14 Apr 2021 20:59:45 GMT  
		Size: 3.9 MB (3865222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6192a99188bab50360cf865945eb38832403ea8911957b387dd76876c1cf394`  
		Last Modified: Wed, 14 Apr 2021 20:59:44 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bf0cbbc7f550f9e866f9b903fc73a259f80d6f6847435c4168a8af0e5c5987`  
		Last Modified: Wed, 14 Apr 2021 20:59:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:1.8.30`

```console
$ docker pull haproxy@sha256:10405165016bbdf5040aa5d762710ba8767c42cc19d85be7f624645e10668f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:1.8.30` - linux; amd64

```console
$ docker pull haproxy@sha256:49c9bcdebd55fc3cd37805770fc8fa36a32585091ac3d20c4882ab18cd8e923d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33800249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2afa0f4378c8c2836da31aec9f2cd769bcc456028a1d70780a241037fc70250`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 10:43:34 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 10:50:35 GMT
ENV HAPROXY_VERSION=1.8.30
# Tue, 17 Aug 2021 10:50:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Tue, 17 Aug 2021 10:50:36 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Tue, 17 Aug 2021 10:51:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 10:51:41 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 10:51:41 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 10:51:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 10:51:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 10:51:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd06683556254cbe06dad4624837c2dcbd2fec67c7fbdd057251f0a207a9315`  
		Last Modified: Tue, 17 Aug 2021 10:53:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a6f7a10fa32e0c44f1bfa1c0eb9be0023745ce71c715b8bca2bf9b1fcc5396`  
		Last Modified: Tue, 17 Aug 2021 10:55:02 GMT  
		Size: 6.7 MB (6652316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b5103e466612c2c86ccbc1dc089e4e43ed2f5255bc36d05251e1c9de2a230c`  
		Last Modified: Tue, 17 Aug 2021 10:55:01 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a6d55663076df62c72b8edb76440e5dc67903125476b7a1c7d7cfd2e052fa8`  
		Last Modified: Tue, 17 Aug 2021 10:55:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.30` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:e2406cf33141a98310092840566a6636250301da49d64bab0119ecb32ab6bc0f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31112236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fbd0c97aee6de1014d7327adf932afc0671dfd92cd44e78a1ab9623bf7cca9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:56:50 GMT
ADD file:f29260935f1f8b3eef5eb0d5e49dd4cf5370e8731a3f4006d6023724bce09601 in / 
# Tue, 17 Aug 2021 01:56:51 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:39:10 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:44:46 GMT
ENV HAPROXY_VERSION=1.8.30
# Tue, 17 Aug 2021 08:44:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Tue, 17 Aug 2021 08:44:47 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Tue, 17 Aug 2021 08:45:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:45:39 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:45:39 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:45:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 08:45:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:45:42 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3dfab4a5b2accf2d709d8c7d14a42715948ecf2d6da4943a6e2c0de8ae7536a0`  
		Last Modified: Tue, 17 Aug 2021 02:12:42 GMT  
		Size: 24.9 MB (24879063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeabbf4f2af3ef66d78a317a4b3a0704a061a5de2611c57b0bfc47b775c2ed8b`  
		Last Modified: Tue, 17 Aug 2021 08:48:10 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6332b82bbe433e45e063bc46fb662f4595f0f89b32319e7192f14c7608beaa`  
		Last Modified: Tue, 17 Aug 2021 08:49:50 GMT  
		Size: 6.2 MB (6231227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b099ab28cce251961e4a2d9aa9bcd175436d533aaf95f981817add79a0bb89af`  
		Last Modified: Tue, 17 Aug 2021 08:49:46 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112180ec06b41530f9b1c5e4f958d9d4ff0877c75a34b9b2be728dc3c9a0e491`  
		Last Modified: Tue, 17 Aug 2021 08:49:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.30` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:8a2aaa4c43ad9e63d2b0e10c13a62053e935851099f99fa73ce0458108317de2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28819094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a839724d329d9a91c106368c118749676f1523e54e78dae55403d8ce7a36df5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 02:14:25 GMT
ADD file:ca8cc4b509e305fa07662fbf2234ed78f0056569f6ca047305dc02bcd60f1558 in / 
# Tue, 17 Aug 2021 02:14:26 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 16:10:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:16:53 GMT
ENV HAPROXY_VERSION=1.8.30
# Tue, 17 Aug 2021 16:16:53 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Tue, 17 Aug 2021 16:16:54 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Tue, 17 Aug 2021 16:17:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:17:41 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:17:42 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:17:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:17:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:17:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:13e3f03410ff211945a725435c13065288d48a8cb740f0530e7588012c2679a4`  
		Last Modified: Tue, 17 Aug 2021 02:30:58 GMT  
		Size: 22.7 MB (22746254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb366ce7907325b732435009125848fb9596a1afdb0f87a8703cdf4342e91a4e`  
		Last Modified: Tue, 17 Aug 2021 16:21:35 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d7703e699ab32fa41edeee749507d138ee19957ce1cdaf38d22911f1912220`  
		Last Modified: Tue, 17 Aug 2021 16:23:33 GMT  
		Size: 6.1 MB (6070894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e83ad3304ad9c9faa5dc77cf668fcbdb7f36293fbba2114795617e98d5a6e3`  
		Last Modified: Tue, 17 Aug 2021 16:23:30 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5581cbf3515ace3827998b3992d7c18ca2aeb3e434650ae060583d7dda7675c1`  
		Last Modified: Tue, 17 Aug 2021 16:23:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.30` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:b3443efc642e9fbd8ba7f286f134e77c75684cb9d3f9c5deeea65d099408d938
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32370800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac150f16c650d71b54354d78ae5ac2692148ad8214cc671bdcebd3e07a5723c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:12:02 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:16:43 GMT
ENV HAPROXY_VERSION=1.8.30
# Tue, 17 Aug 2021 08:16:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Tue, 17 Aug 2021 08:16:43 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Tue, 17 Aug 2021 08:17:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:17:12 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:17:12 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:17:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 08:17:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:17:13 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc63cf29191f59ddbc41452b9edbe5f8145c4370cd74d3981d50a862173029b`  
		Last Modified: Tue, 17 Aug 2021 08:19:14 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f30e617b2ec3b128522709a5ef45fb8511720085bb9f56408de746dc69219e`  
		Last Modified: Tue, 17 Aug 2021 08:20:33 GMT  
		Size: 6.5 MB (6453782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae49d2e8fb6c082bfe198ad028053fc47460c9b56350d41bb1fd302fd579b1a`  
		Last Modified: Tue, 17 Aug 2021 08:20:31 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69fc5fcb63ad9c06b0360077809d3750efa2ade439a8d97df35539eee1685b9`  
		Last Modified: Tue, 17 Aug 2021 08:20:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.30` - linux; 386

```console
$ docker pull haproxy@sha256:bbc52d41708f0d296625cbf528e18c0d32c113bf4ac5fa5824c097dc91c6ae7c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34376383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f94955774be42d24f66b61400de0e20575ad77ac657232733b44f076b2ddaa3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:41:16 GMT
ADD file:0418032b55cd0a6dd515ac277fb9f92354397503cab212d446d3a3d8c647a60f in / 
# Tue, 17 Aug 2021 01:41:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 12:14:55 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 12:22:46 GMT
ENV HAPROXY_VERSION=1.8.30
# Tue, 17 Aug 2021 12:22:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Tue, 17 Aug 2021 12:22:47 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Tue, 17 Aug 2021 12:23:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 12:23:29 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 12:23:30 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 12:23:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 12:23:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 12:23:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c1c94e1f2523d69effaa463d64fc9962cfc67e2a956f0476c94200e7cf19edf0`  
		Last Modified: Tue, 17 Aug 2021 01:50:57 GMT  
		Size: 27.8 MB (27797627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f804b7c921abcc2fb2904ad2092beefd0224c9bd4cb1cf6477727e6f2bbd7599`  
		Last Modified: Tue, 17 Aug 2021 12:26:22 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc90821ea3e08a6b2ffacf914890b8f22d9dcec1ad5850a77813a1c9c4fd6993`  
		Last Modified: Tue, 17 Aug 2021 12:28:03 GMT  
		Size: 6.6 MB (6576813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5acf8fa1f5b6cf4a91fddf31c61af95f657da3d834d36f4e32f0d46f282f69`  
		Last Modified: Tue, 17 Aug 2021 12:28:01 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b866b133478c5ddea5b0789b99a0d185158cbb285f2f533fd50becd510daea5`  
		Last Modified: Tue, 17 Aug 2021 12:28:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.30` - linux; mips64le

```console
$ docker pull haproxy@sha256:40c5886a502b4d8dee4231cc3f163ad34e299d82a13b59e651e9f88d99369f3a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31958357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05cb64bfcd11f6dc654becb8cf265c82a452a342afc1638ece8387c3f9943de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:12:26 GMT
ADD file:8bd279803ead4ddce8db90b65e89c423f84fbf6042bfbeae8c09486b2e884cde in / 
# Tue, 17 Aug 2021 01:12:27 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:10:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 14:23:32 GMT
ENV HAPROXY_VERSION=1.8.30
# Tue, 17 Aug 2021 14:23:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Tue, 17 Aug 2021 14:23:32 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Tue, 17 Aug 2021 14:25:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 14:25:13 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 14:25:13 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 14:25:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 14:25:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:25:15 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a711e3e37b88ef77496c07ed663bb4270ecba9057eba452a91cc9be0bafb9c32`  
		Last Modified: Tue, 17 Aug 2021 01:21:44 GMT  
		Size: 25.8 MB (25813007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac33edc8b81dffec584b1a7ca6a8abea967f70259323fc62ff423b9c01642e`  
		Last Modified: Tue, 17 Aug 2021 14:27:23 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a482badf4699073b1e8016fb3736e273192234996c698dcd8d531acb55a1c8e0`  
		Last Modified: Tue, 17 Aug 2021 14:28:57 GMT  
		Size: 6.1 MB (6143401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3863c167bb424ef17263655e8f88117f2e43c4d4fca90a26519c9e590ee11159`  
		Last Modified: Tue, 17 Aug 2021 14:28:52 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01538b4844c786d24cf3e2d63bafa653999614a8571c3fde53dc8eda4e568920`  
		Last Modified: Tue, 17 Aug 2021 14:28:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.30` - linux; ppc64le

```console
$ docker pull haproxy@sha256:713c08f78ccc1a48bf579bef9a085f632ec039d8947802e487172db0e6523d2c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37499315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a265f2b9f939709c00f838a0e96dae95e2406d9e27c436797a03732fd409b79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:34:13 GMT
ADD file:8b9b12a994a2519f725d1ed1f4ab5a444665262678fd8e6c42cf78f32dacb7fa in / 
# Tue, 17 Aug 2021 01:34:20 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 13:36:19 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 14:11:10 GMT
ENV HAPROXY_VERSION=1.8.30
# Tue, 17 Aug 2021 14:11:15 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Tue, 17 Aug 2021 14:11:23 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Tue, 17 Aug 2021 14:16:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 14:16:37 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 14:16:40 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 14:16:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 14:16:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:16:59 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c3e09f0e3e7f6fcb741a4c9214b63e341e1d9b53d7689a5ad6ff640b61a82541`  
		Last Modified: Tue, 17 Aug 2021 01:48:22 GMT  
		Size: 30.6 MB (30553721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb7833dc31cf72935b478f7bf90e34f0f2a22d8260da177e4648ac973af1f9c`  
		Last Modified: Tue, 17 Aug 2021 14:24:41 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f9e0316e0cf9c9bd723c914436cbbf3d4eef9b5fedb8bc2e38b9e23947e67d`  
		Last Modified: Tue, 17 Aug 2021 14:26:11 GMT  
		Size: 6.9 MB (6943631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3641a78876a225e627c2f80a5fdfc466e2dd5180bd6bbddd138a1c86d5eed129`  
		Last Modified: Tue, 17 Aug 2021 14:26:09 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eccd50492e1cd0ea05b7f336c7b9ce367cc1dd2baa388e61a27c5f8deab9948e`  
		Last Modified: Tue, 17 Aug 2021 14:26:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.30` - linux; s390x

```console
$ docker pull haproxy@sha256:230713a8d26f462a8ab023c0ce0f7aec8394284ff39fb2a9038e6dd7d0df8cb5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31995544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c26efac7113a88d93ceec256d9051a59eb4d5774ce3bb2359f84080a7e48f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 07:18:12 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 07:25:15 GMT
ENV HAPROXY_VERSION=1.8.30
# Tue, 17 Aug 2021 07:25:16 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Tue, 17 Aug 2021 07:25:16 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Tue, 17 Aug 2021 07:25:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 07:25:50 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 07:25:50 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 07:25:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 07:25:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 07:25:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16a2f2a1452470a1d818d8d16934d08d2a57b312ceabcce8c1cfad6c99f00a2`  
		Last Modified: Tue, 17 Aug 2021 07:28:00 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde815120b599af00d27bc664e5f337b839d6a1b90488f887b4f7e9d7272e9b0`  
		Last Modified: Tue, 17 Aug 2021 07:28:51 GMT  
		Size: 6.2 MB (6232742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13cf0f8cd42be7e7a1d3b0d8d98ed182fc83dc5b16c0b91a44958e182ea1687`  
		Last Modified: Tue, 17 Aug 2021 07:28:50 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2789f33d279538ab7c218ca54178c2b5202a5b1e2c1c5b286410edc4fb90f15f`  
		Last Modified: Tue, 17 Aug 2021 07:28:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:1.8.30-alpine`

```console
$ docker pull haproxy@sha256:e636afbecc760b34bb1cff2d2d9f47f0fe87f2a1cf77ffbd25a6605b80d3005b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:1.8.30-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:f5e1be9d9be0348431e67f17ce6206b50a24f903233337ede36f70f21546f6d0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6786701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a904a6a2f1c1ffb16601be820758da6a3b0cf1fa0142fae0f5b5822c061b7d6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:43:18 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 19:49:57 GMT
ENV HAPROXY_VERSION=1.8.30
# Fri, 06 Aug 2021 19:49:57 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Fri, 06 Aug 2021 19:49:57 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Fri, 06 Aug 2021 19:50:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 19:50:38 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 19:50:38 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 19:50:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 19:50:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 19:50:40 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22138861da3ab6ae8583cf62942545e1bb75874501f4a8d45d13a38c848a908`  
		Last Modified: Fri, 06 Aug 2021 19:51:27 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a5fd354d11cc818598bf04ae789dcabc3ee2c1b39cc2ccf6042385707c251c`  
		Last Modified: Fri, 06 Aug 2021 19:52:33 GMT  
		Size: 4.0 MB (3971927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106d5a39ebd3941a4b1cad55a15b928bde429faadf690a9a6b8ba68cf8971895`  
		Last Modified: Fri, 06 Aug 2021 19:52:32 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c577c5149c37ac2f2880fc88a1d896b8c0adf4df7f4adc596f2b3962517348d`  
		Last Modified: Fri, 06 Aug 2021 19:52:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.30-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:ff198c5e30af586cfb08a1637cf80c53935feace64fc6175b1b64dc369a5b105
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6473485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a374b30833a3cc5cf22e553da0a343c7a3be75c418cdb28145f582a144d9e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:49:32 GMT
ADD file:7f2c7deda009eabdcbbdccb11e854043d32c498e64e7e1ca02165d7bb4261d39 in / 
# Fri, 06 Aug 2021 17:49:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:15:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 18:18:59 GMT
ENV HAPROXY_VERSION=1.8.30
# Fri, 06 Aug 2021 18:18:59 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Fri, 06 Aug 2021 18:19:00 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Fri, 06 Aug 2021 18:19:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 18:19:24 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 18:19:25 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 18:19:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 18:19:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 18:19:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f465bb3e9fcd0c42f936ecc566c6e40353c00f3089b2b2c2ea1663c30f89d3ab`  
		Last Modified: Fri, 06 Aug 2021 17:51:00 GMT  
		Size: 2.6 MB (2626350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332ccafb58fe1d8ed3d3d5ad9c01adba33d922f28a398285d2eb67fed7c8bee8`  
		Last Modified: Fri, 06 Aug 2021 18:20:57 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acb590fd7a3d2c22e077debe0adb8f59ab5aa312316fa35de06be3db4b05014`  
		Last Modified: Fri, 06 Aug 2021 18:22:29 GMT  
		Size: 3.8 MB (3845364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53099ed6f8a71dcad7b991ee6e92f63a621385d0ab79af696504ac4bdd47874a`  
		Last Modified: Fri, 06 Aug 2021 18:22:26 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c5e9bb4fe6f965d657fc527e9030a83cd9e5af5a8292d86a81aa099a0bed5e`  
		Last Modified: Fri, 06 Aug 2021 18:22:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.30-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:48cc927b413bd1ecc7dcf2b186e0398a64a787c749c568f3bf781a92f4a48e07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6214143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ac9ef4d97188e723c9ab285ee1c7d85a4d7ad4585056b8fe23887048eea17f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:57:32 GMT
ADD file:3a35ff3ac0d80289d419a4d6d8319610c38e1936d296addafb9aaf506946230f in / 
# Fri, 06 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:54:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 19:59:36 GMT
ENV HAPROXY_VERSION=1.8.30
# Fri, 06 Aug 2021 19:59:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Fri, 06 Aug 2021 19:59:37 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Fri, 06 Aug 2021 20:00:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 20:00:01 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 20:00:02 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 20:00:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 20:00:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 20:00:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4ee0caa23b369b04827640a4be298bf4ff7bacd030c77e915f5d7fb8f987594a`  
		Last Modified: Fri, 06 Aug 2021 17:58:57 GMT  
		Size: 2.4 MB (2429359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548ff9918828f96cb9a5e5656ea589d79e6fb1d7b9f0d693feff2dbefc6929fe`  
		Last Modified: Fri, 06 Aug 2021 20:02:54 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2421cef4cbe218a8caf6b18f05d5f404c64d5ac5b4d714edee3d891eb1bd2cda`  
		Last Modified: Fri, 06 Aug 2021 20:04:40 GMT  
		Size: 3.8 MB (3783012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa8f52f106be61ce21271232331a5c4ddba088b395131da38bf197c816f6040`  
		Last Modified: Fri, 06 Aug 2021 20:04:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a88386f3a5a10c726e32652dd04876b4bfb2ae5c47f20e6b764a0358ca68ebe`  
		Last Modified: Fri, 06 Aug 2021 20:04:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.30-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:2e269c0dd8f2ded7deb5b3da0ff486fc90fe8a02fb058bab4d0c2a7f1c788f51
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6641612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d198bfd1dfe729ae77344af23d756b7a521da2d2bb3d67e095d7cb0cd45a86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:39:26 GMT
ADD file:1a8fd1066485e1261462e689c1a072f010c1d3be904b73ef2b84128fac652951 in / 
# Fri, 06 Aug 2021 17:39:27 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:38:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 18:44:10 GMT
ENV HAPROXY_VERSION=1.8.30
# Fri, 06 Aug 2021 18:44:10 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Fri, 06 Aug 2021 18:44:11 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Fri, 06 Aug 2021 18:44:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 18:44:40 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 18:44:41 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 18:44:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 18:44:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 18:44:42 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fd3acdcea5682abced546ec19fb6ebee725c5184e5d91614c469c0a79e67f2d0`  
		Last Modified: Fri, 06 Aug 2021 17:40:12 GMT  
		Size: 2.7 MB (2710613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a23793c1bba0796c0f469305ee92dd0f1cb8299963e4da4249d0f5aa2fcea0`  
		Last Modified: Fri, 06 Aug 2021 18:46:06 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5464479783659679ddef52252cfff218a3ea00eb47d4144096c54145fb7b8f7`  
		Last Modified: Fri, 06 Aug 2021 18:47:26 GMT  
		Size: 3.9 MB (3929233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0ba81491a27348f40013accce5be9bb9104f5484daab1d36939911b9f22d06`  
		Last Modified: Fri, 06 Aug 2021 18:47:25 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915431d67be340c0c7abab56573dd4dfa9cd05201106bbe98dcb3460b0955726`  
		Last Modified: Fri, 06 Aug 2021 18:47:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.30-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:f07aac88939a1ff7fa8b26caeacd68aaab432800759c1eeff4ca3008e7b49c0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6709098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd5fce8a83efa395dca43758a79741513231dd11d532788473425ccedaf1d90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:38:26 GMT
ADD file:bafaec4a54d6cef99b5f3660d074a3d2251e4d4bd09df9ea65f33e9bffb7d88d in / 
# Fri, 06 Aug 2021 17:38:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:19:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 19:29:15 GMT
ENV HAPROXY_VERSION=1.8.30
# Fri, 06 Aug 2021 19:29:15 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Fri, 06 Aug 2021 19:29:16 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Fri, 06 Aug 2021 19:30:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 19:30:21 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 19:30:21 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 19:30:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 19:30:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 19:30:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:935703e1179e32e201e4a36d5664d58299dc8e7bcac197b70c295c0a59216db1`  
		Last Modified: Fri, 06 Aug 2021 17:39:15 GMT  
		Size: 2.8 MB (2821910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695b2822110160b402b8f359bb19d954a46a6ead94f868feba7d00f5a10e50e`  
		Last Modified: Fri, 06 Aug 2021 19:32:18 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7df0172c1b292c4823dc8f07519e1ff946b807f6710a7f09dcc0fbc921243f3`  
		Last Modified: Fri, 06 Aug 2021 19:33:50 GMT  
		Size: 3.9 MB (3885421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8eae33ef2ea20ba682bf22f964f3e28f00fbf2dc7e90339bfcfd922e418a77`  
		Last Modified: Fri, 06 Aug 2021 19:33:49 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccddaa60700d05d4ed03cb4cb69dbfe91bb86ece69442eac025203e2e395b67`  
		Last Modified: Fri, 06 Aug 2021 19:33:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.30-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:be483e473840a03cb4ab5ec93f46ed662bad8cae560762ea3533ec45e52763b3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6949175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8c165c9006f0ae0092b6cd8f0d4d44c43fe8ddda7e5e7e4c1b32e37d16c928`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:17:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 21:24:57 GMT
ENV HAPROXY_VERSION=1.8.30
# Fri, 06 Aug 2021 21:24:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Fri, 06 Aug 2021 21:25:02 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Fri, 06 Aug 2021 21:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 21:25:38 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 21:25:41 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 21:25:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 21:25:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 21:26:02 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d374dad070e00fdb493e29a3aa64b375dbec801497e01d3b8ddbf7cc967634cb`  
		Last Modified: Fri, 06 Aug 2021 21:27:30 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926fac922b7f30c135d54663b5fef5947ec8e3bbefddc68cf05b2718933137de`  
		Last Modified: Fri, 06 Aug 2021 21:28:51 GMT  
		Size: 4.1 MB (4136257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1643c103dd6aef93e4cdd049b1199fb99749ec01077f3d7f23ff22c53c33864`  
		Last Modified: Fri, 06 Aug 2021 21:28:50 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d6dc7b43bfb8be4890b7c4d4ad687056a7cc893e94e42dd70bb227eea868ce`  
		Last Modified: Fri, 06 Aug 2021 21:28:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:1.8.30-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:56ab7dd8abed67c02b519cf7e49892f4b44431d493327f3aa9c26dd80841daa9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6469626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8e380d640dae4d7b5e8eda393c2992736478cf6bda09d77675c7938d34db2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:54:24 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 14 Apr 2021 20:57:46 GMT
ENV HAPROXY_VERSION=1.8.30
# Wed, 14 Apr 2021 20:57:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/1.8/src/haproxy-1.8.30.tar.gz
# Wed, 14 Apr 2021 20:57:46 GMT
ENV HAPROXY_SHA256=066bfd9a0e5a3550fa621886a132379e5331d0c377e11f38bb6e8dfbec92be42
# Wed, 14 Apr 2021 20:58:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux2628 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Wed, 14 Apr 2021 20:58:10 GMT
STOPSIGNAL SIGUSR1
# Wed, 14 Apr 2021 20:58:10 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 14 Apr 2021 20:58:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Apr 2021 20:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 20:58:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267275aba58470c82626189a59be76cd169bd245568e2f2545ed1ee64ff8a8ff`  
		Last Modified: Wed, 14 Apr 2021 20:59:06 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba85d625d72596824b2a38b34880512b279ac65dacc4bb0255d3a8ba92ec8d1`  
		Last Modified: Wed, 14 Apr 2021 20:59:45 GMT  
		Size: 3.9 MB (3865222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6192a99188bab50360cf865945eb38832403ea8911957b387dd76876c1cf394`  
		Last Modified: Wed, 14 Apr 2021 20:59:44 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bf0cbbc7f550f9e866f9b903fc73a259f80d6f6847435c4168a8af0e5c5987`  
		Last Modified: Wed, 14 Apr 2021 20:59:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.0`

```console
$ docker pull haproxy@sha256:37f0aa9be954b1c4c3e17dd5a9e311415c40b710c3ad0786aa834a643c107d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.0` - linux; amd64

```console
$ docker pull haproxy@sha256:a1c5f9ff2b359c49088bbc6b9cb0b4f554bbec209755037d635583572b603384
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35808441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12715ed5fcbdbbe585156fdce74f719c514ef1e768f61fb3b19958fae8c81ff9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 10:43:34 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:57:22 GMT
ENV HAPROXY_VERSION=2.0.24
# Tue, 17 Aug 2021 16:57:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.24.tar.gz
# Tue, 17 Aug 2021 16:57:22 GMT
ENV HAPROXY_SHA256=210e39599966e4ece6d431d51309c261b1ab5237a329a7a9f089426b0ceeea13
# Tue, 17 Aug 2021 16:58:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:58:09 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:58:09 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:58:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:58:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:58:10 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd06683556254cbe06dad4624837c2dcbd2fec67c7fbdd057251f0a207a9315`  
		Last Modified: Tue, 17 Aug 2021 10:53:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935dfd58b9fe509e6fe45ae00f5ad6fc439b2999e85c4c83c5f21129fe9a0d1c`  
		Last Modified: Tue, 17 Aug 2021 17:01:53 GMT  
		Size: 8.7 MB (8660509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21701f6d2099052e62c9d07c10f1fb9b75706930e3d80c74a0b304e0175c1e0`  
		Last Modified: Tue, 17 Aug 2021 17:01:51 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9615fc6254a11de1b80774aec6ccd1c914601ca6b8eb06239b903e75a1d2f7ad`  
		Last Modified: Tue, 17 Aug 2021 17:01:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:2aa21b3951bac479494476e48b51fb3bfdd22fc38f9104b4467121e4240b8420
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 MB (33069473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2827fea4d9d5a4c6fc23792ce53b54d376e90103db29bc015897620c4e5e3b19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:56:50 GMT
ADD file:f29260935f1f8b3eef5eb0d5e49dd4cf5370e8731a3f4006d6023724bce09601 in / 
# Tue, 17 Aug 2021 01:56:51 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:39:10 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:43:39 GMT
ENV HAPROXY_VERSION=2.0.23
# Tue, 17 Aug 2021 08:43:40 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.23.tar.gz
# Tue, 17 Aug 2021 08:43:40 GMT
ENV HAPROXY_SHA256=5ddc04e9040a07c647fa4b68fc9da6ec36063d56e12824b356e770dcf677c87a
# Tue, 17 Aug 2021 08:44:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:44:30 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:44:30 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:44:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 08:44:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:44:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3dfab4a5b2accf2d709d8c7d14a42715948ecf2d6da4943a6e2c0de8ae7536a0`  
		Last Modified: Tue, 17 Aug 2021 02:12:42 GMT  
		Size: 24.9 MB (24879063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeabbf4f2af3ef66d78a317a4b3a0704a061a5de2611c57b0bfc47b775c2ed8b`  
		Last Modified: Tue, 17 Aug 2021 08:48:10 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f833a0fdef59cf427f03b2bf63d5afc66e9e1d056951b1ea387262f236e55b0c`  
		Last Modified: Tue, 17 Aug 2021 08:49:34 GMT  
		Size: 8.2 MB (8188463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0d0088cdf7f79bb3887aa9c134a183d1f3b49459e08f13120048cf2cc5ed69`  
		Last Modified: Tue, 17 Aug 2021 08:49:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1d0e942000a04a54d5e0aa9856e7ab5e815faba76c1b08566023fedcbee567`  
		Last Modified: Tue, 17 Aug 2021 08:49:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:6eba009dfb69426b7f794130df244abe4ecb8962ef7980b41d54157dd561b45f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30861750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e15b975f14ba7e9047d255f8b6d01bf0aec69dfa3f293b07569d99b706e72be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 02:14:25 GMT
ADD file:ca8cc4b509e305fa07662fbf2234ed78f0056569f6ca047305dc02bcd60f1558 in / 
# Tue, 17 Aug 2021 02:14:26 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 16:10:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:15:37 GMT
ENV HAPROXY_VERSION=2.0.23
# Tue, 17 Aug 2021 16:15:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.23.tar.gz
# Tue, 17 Aug 2021 16:15:38 GMT
ENV HAPROXY_SHA256=5ddc04e9040a07c647fa4b68fc9da6ec36063d56e12824b356e770dcf677c87a
# Tue, 17 Aug 2021 16:16:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:16:23 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:16:24 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:16:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:16:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:16:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:13e3f03410ff211945a725435c13065288d48a8cb740f0530e7588012c2679a4`  
		Last Modified: Tue, 17 Aug 2021 02:30:58 GMT  
		Size: 22.7 MB (22746254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb366ce7907325b732435009125848fb9596a1afdb0f87a8703cdf4342e91a4e`  
		Last Modified: Tue, 17 Aug 2021 16:21:35 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4fde1fb4402eff4758e032affdde62690e26fc668a8a051fd4eb3a92289209`  
		Last Modified: Tue, 17 Aug 2021 16:23:14 GMT  
		Size: 8.1 MB (8113549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8c87165a917db31e63f6e90c9438a81f750847f6f93858ce6b556ab367d12d`  
		Last Modified: Tue, 17 Aug 2021 16:23:10 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bed1ea4ed60ed8f5ad2435dcc710866c6141ec4a9a56c653d23aa386ecca075`  
		Last Modified: Tue, 17 Aug 2021 16:23:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:bc0d18c18c0e56c53a7e580681f3a86b972a951c3874662d8fd9457512a1acfb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34439149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0206f592f95879243443316d91d5ceb90f7c0723a1df118ada38869d9d4779`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:12:02 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:15:47 GMT
ENV HAPROXY_VERSION=2.0.23
# Tue, 17 Aug 2021 08:15:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.23.tar.gz
# Tue, 17 Aug 2021 08:15:47 GMT
ENV HAPROXY_SHA256=5ddc04e9040a07c647fa4b68fc9da6ec36063d56e12824b356e770dcf677c87a
# Tue, 17 Aug 2021 08:16:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:16:28 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:16:29 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:16:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 08:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:16:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc63cf29191f59ddbc41452b9edbe5f8145c4370cd74d3981d50a862173029b`  
		Last Modified: Tue, 17 Aug 2021 08:19:14 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b5b23551f69db3cb4d38814fbf4a2d907c4939236d4da4921e60d1be333b63`  
		Last Modified: Tue, 17 Aug 2021 08:20:19 GMT  
		Size: 8.5 MB (8522129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d736ceff9053d0f898956f51fa0590c345c0eaa50a78c83ea44807fb620eb084`  
		Last Modified: Tue, 17 Aug 2021 08:20:18 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128289658c292ae505aaa53279af1313f7a50d2037a19f63004dc0e28bc614d5`  
		Last Modified: Tue, 17 Aug 2021 08:20:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0` - linux; 386

```console
$ docker pull haproxy@sha256:a49464ab5202942e380c8dd5b47b1666b3e03b2f9c53406e5da5a552d2ed8006
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36299478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd0cd80ffa3f0c9ceddf17d6d4b889ea9b60c36eac0fe413a7d1dd75743d1f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:41:16 GMT
ADD file:0418032b55cd0a6dd515ac277fb9f92354397503cab212d446d3a3d8c647a60f in / 
# Tue, 17 Aug 2021 01:41:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 12:14:55 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:11:09 GMT
ENV HAPROXY_VERSION=2.0.24
# Tue, 17 Aug 2021 17:11:10 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.24.tar.gz
# Tue, 17 Aug 2021 17:11:10 GMT
ENV HAPROXY_SHA256=210e39599966e4ece6d431d51309c261b1ab5237a329a7a9f089426b0ceeea13
# Tue, 17 Aug 2021 17:12:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 17:12:04 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:12:05 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:12:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 17:12:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:12:06 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c1c94e1f2523d69effaa463d64fc9962cfc67e2a956f0476c94200e7cf19edf0`  
		Last Modified: Tue, 17 Aug 2021 01:50:57 GMT  
		Size: 27.8 MB (27797627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f804b7c921abcc2fb2904ad2092beefd0224c9bd4cb1cf6477727e6f2bbd7599`  
		Last Modified: Tue, 17 Aug 2021 12:26:22 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1455615c6c79d1422fdf4658f1ed39f2a10e21d3508282d434465a8bcb88f140`  
		Last Modified: Tue, 17 Aug 2021 17:17:18 GMT  
		Size: 8.5 MB (8499907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d3f8b1ac409f7ee3ebc4c145b1d2f625ded65dcf1f5d6b794f238daf9946f6`  
		Last Modified: Tue, 17 Aug 2021 17:17:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e39d60b102d3195da834b27f2250dfc71c1259e01e67e796c39d74c18e213ef`  
		Last Modified: Tue, 17 Aug 2021 17:17:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0` - linux; mips64le

```console
$ docker pull haproxy@sha256:a12c1a525c1cf4458fbcc565ec149f95542ada13f9d882d4cd7f228a9babb2af
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33981194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b745cc0989d109caa84a223346dd78423ca342dcb2bf3a402625e98821dfd60a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:12:26 GMT
ADD file:8bd279803ead4ddce8db90b65e89c423f84fbf6042bfbeae8c09486b2e884cde in / 
# Tue, 17 Aug 2021 01:12:27 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:10:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 14:21:05 GMT
ENV HAPROXY_VERSION=2.0.23
# Tue, 17 Aug 2021 14:21:05 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.23.tar.gz
# Tue, 17 Aug 2021 14:21:06 GMT
ENV HAPROXY_SHA256=5ddc04e9040a07c647fa4b68fc9da6ec36063d56e12824b356e770dcf677c87a
# Tue, 17 Aug 2021 14:23:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 14:23:16 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 14:23:16 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 14:23:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 14:23:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:23:19 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a711e3e37b88ef77496c07ed663bb4270ecba9057eba452a91cc9be0bafb9c32`  
		Last Modified: Tue, 17 Aug 2021 01:21:44 GMT  
		Size: 25.8 MB (25813007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac33edc8b81dffec584b1a7ca6a8abea967f70259323fc62ff423b9c01642e`  
		Last Modified: Tue, 17 Aug 2021 14:27:23 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c62527a8ee27118429fabe755d0f79d6e30ee1f53b24f8b8ce7bd1bab32cc38`  
		Last Modified: Tue, 17 Aug 2021 14:28:42 GMT  
		Size: 8.2 MB (8166237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71c83be903b95166191c7fb709701e8986e5ba59b183fbd478943552b2695c7`  
		Last Modified: Tue, 17 Aug 2021 14:28:36 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560c079d560aa162413e097cf4fc5e1cbda0938dd60981915318b15c5ab404d9`  
		Last Modified: Tue, 17 Aug 2021 14:28:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0` - linux; ppc64le

```console
$ docker pull haproxy@sha256:8f152d991f98bdc57af8eea6d255d57a9caceb4950b2c651762664fb231e8072
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39531122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807ec85efc811fa92ea3843dda8a6f515d03ef397011b572bac1f8f5cc68ee3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:34:13 GMT
ADD file:8b9b12a994a2519f725d1ed1f4ab5a444665262678fd8e6c42cf78f32dacb7fa in / 
# Tue, 17 Aug 2021 01:34:20 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 13:36:19 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:57:56 GMT
ENV HAPROXY_VERSION=2.0.24
# Tue, 17 Aug 2021 16:57:59 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.24.tar.gz
# Tue, 17 Aug 2021 16:58:02 GMT
ENV HAPROXY_SHA256=210e39599966e4ece6d431d51309c261b1ab5237a329a7a9f089426b0ceeea13
# Tue, 17 Aug 2021 17:00:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 17:00:22 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:00:25 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:00:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 17:00:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:00:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c3e09f0e3e7f6fcb741a4c9214b63e341e1d9b53d7689a5ad6ff640b61a82541`  
		Last Modified: Tue, 17 Aug 2021 01:48:22 GMT  
		Size: 30.6 MB (30553721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb7833dc31cf72935b478f7bf90e34f0f2a22d8260da177e4648ac973af1f9c`  
		Last Modified: Tue, 17 Aug 2021 14:24:41 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f16b85495df89c40effab3516c1a1a4b0dff3138bebad6ed20f16573a37797`  
		Last Modified: Tue, 17 Aug 2021 17:05:54 GMT  
		Size: 9.0 MB (8975439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62650b31a259db4f499ebfcd267ce8dee98cb9611eaa086abef084222d5891f6`  
		Last Modified: Tue, 17 Aug 2021 17:05:52 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674a62f49984c78fd2fe84a59e3ce3d4fb548a787b2db37b9cde94b008fef727`  
		Last Modified: Tue, 17 Aug 2021 17:05:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0` - linux; s390x

```console
$ docker pull haproxy@sha256:5ca87c7fd413103aa1b6721d3f23bb713b690d4f6b40e505adce95908d07064d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34024770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0fc22fe52c289d0b85d0956df7cfe5e78fa783163c745c3b03527ac89e72a6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 07:18:12 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 07:23:55 GMT
ENV HAPROXY_VERSION=2.0.23
# Tue, 17 Aug 2021 07:23:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.23.tar.gz
# Tue, 17 Aug 2021 07:23:56 GMT
ENV HAPROXY_SHA256=5ddc04e9040a07c647fa4b68fc9da6ec36063d56e12824b356e770dcf677c87a
# Tue, 17 Aug 2021 07:24:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 07:24:32 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 07:24:32 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 07:24:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 07:24:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 07:24:34 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16a2f2a1452470a1d818d8d16934d08d2a57b312ceabcce8c1cfad6c99f00a2`  
		Last Modified: Tue, 17 Aug 2021 07:28:00 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2873e28242d53f0f71e2d5126f2f9f7e2b67e80288307f44d2bac4fb5a71da63`  
		Last Modified: Tue, 17 Aug 2021 07:28:43 GMT  
		Size: 8.3 MB (8261968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3239a8133e0576e408240d3d2c122cf0548d8c855ff051099b1e8689e97f82`  
		Last Modified: Tue, 17 Aug 2021 07:28:42 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595697bb5999b99bead8aa5eb55a082d7dc8ccfacdb767a6fb509d1a7843353d`  
		Last Modified: Tue, 17 Aug 2021 07:28:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.0-alpine`

```console
$ docker pull haproxy@sha256:140e1802526bed8f19dbbed03133056829942d43c6a4889f65abb9e658f66e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.0-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:884b6d5135211a189ad603aae1281d96d6f6109650a50c428a5fa8c92c34e767
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8672186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec64e5b2295f57e626d74e44adb59bcc3d6e6e903132022ae362301f4dde8e8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:43:18 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:58:22 GMT
ENV HAPROXY_VERSION=2.0.24
# Tue, 17 Aug 2021 16:58:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.24.tar.gz
# Tue, 17 Aug 2021 16:58:22 GMT
ENV HAPROXY_SHA256=210e39599966e4ece6d431d51309c261b1ab5237a329a7a9f089426b0ceeea13
# Tue, 17 Aug 2021 16:59:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:59:17 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:59:18 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:59:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:59:19 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22138861da3ab6ae8583cf62942545e1bb75874501f4a8d45d13a38c848a908`  
		Last Modified: Fri, 06 Aug 2021 19:51:27 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47e280bd219e1f95360ef417f4e0196802abf0cd04a53541bd03f967a134936`  
		Last Modified: Tue, 17 Aug 2021 17:02:05 GMT  
		Size: 5.9 MB (5857418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f241956a81b70c5b84edc5a7070e5debacd85b1e875740188247b65ca7e67e09`  
		Last Modified: Tue, 17 Aug 2021 17:02:03 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f984f4d7c2134b1a0328b10b06465f61cbfb97038f75d24eeba690c27bed0c2`  
		Last Modified: Tue, 17 Aug 2021 17:02:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:fbaef985b8f7ff3bd7b298cdf3c78354866c1ff03467a96cc88300bf6ee3ec4d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8331654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c92957205eb96e7ae15522eb8310389baded85a67351e209e6d51cdeb4d9fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:49:32 GMT
ADD file:7f2c7deda009eabdcbbdccb11e854043d32c498e64e7e1ca02165d7bb4261d39 in / 
# Fri, 06 Aug 2021 17:49:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:15:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:39:03 GMT
ENV HAPROXY_VERSION=2.0.24
# Tue, 17 Aug 2021 16:39:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.24.tar.gz
# Tue, 17 Aug 2021 16:39:04 GMT
ENV HAPROXY_SHA256=210e39599966e4ece6d431d51309c261b1ab5237a329a7a9f089426b0ceeea13
# Tue, 17 Aug 2021 16:39:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:39:27 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:39:28 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:39:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:39:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:39:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f465bb3e9fcd0c42f936ecc566c6e40353c00f3089b2b2c2ea1663c30f89d3ab`  
		Last Modified: Fri, 06 Aug 2021 17:51:00 GMT  
		Size: 2.6 MB (2626350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332ccafb58fe1d8ed3d3d5ad9c01adba33d922f28a398285d2eb67fed7c8bee8`  
		Last Modified: Fri, 06 Aug 2021 18:20:57 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f04114dc0b073aea02e8ae5c98b1e7a9873eab7b89b12dd77d6e0f6b9c16e73`  
		Last Modified: Tue, 17 Aug 2021 16:42:22 GMT  
		Size: 5.7 MB (5703536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2976a39edd1b3719db70e49c3ccecf657ae05d367114678fbe9cd1e45ca01e92`  
		Last Modified: Tue, 17 Aug 2021 16:42:19 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e145ae037e98a0899f2281d00ce7a4b7c2d87b1f5e8f2f88ab6304fc5cc636`  
		Last Modified: Tue, 17 Aug 2021 16:42:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:92705a0f1a49b1451a930244ede40c6308dc1f74d4d82495c4f39612933952f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8109556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8210472178fd4d60205f3637900b515583a7251af1f671b17b7f245b18b82228`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:57:32 GMT
ADD file:3a35ff3ac0d80289d419a4d6d8319610c38e1936d296addafb9aaf506946230f in / 
# Fri, 06 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:54:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 19:58:51 GMT
ENV HAPROXY_VERSION=2.0.23
# Fri, 06 Aug 2021 19:58:51 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.23.tar.gz
# Fri, 06 Aug 2021 19:58:51 GMT
ENV HAPROXY_SHA256=5ddc04e9040a07c647fa4b68fc9da6ec36063d56e12824b356e770dcf677c87a
# Fri, 06 Aug 2021 19:59:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 19:59:13 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 19:59:14 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 19:59:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 19:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 19:59:17 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4ee0caa23b369b04827640a4be298bf4ff7bacd030c77e915f5d7fb8f987594a`  
		Last Modified: Fri, 06 Aug 2021 17:58:57 GMT  
		Size: 2.4 MB (2429359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548ff9918828f96cb9a5e5656ea589d79e6fb1d7b9f0d693feff2dbefc6929fe`  
		Last Modified: Fri, 06 Aug 2021 20:02:54 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a688887174359c25dca68653173337b263e5221c5fe8115e3dc8ab403de6536`  
		Last Modified: Fri, 06 Aug 2021 20:04:21 GMT  
		Size: 5.7 MB (5678428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c31fbdd8796798e4e9b3d9f6c75ba1ff45f0b03c001f1164678c300842a5420`  
		Last Modified: Fri, 06 Aug 2021 20:04:18 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0938a8c84118747ee5e06be158091274ea1248c34581ea2b71022bbe412ac87b`  
		Last Modified: Fri, 06 Aug 2021 20:04:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:1cd5fe5c8a3a3acab7ddcfda34c36720959927c008ac67a6defa1f54315ead72
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8566068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb34978515b378f392c57e8e43f15e6af97f7e489abb5589e56e127e0b00e64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:39:26 GMT
ADD file:1a8fd1066485e1261462e689c1a072f010c1d3be904b73ef2b84128fac652951 in / 
# Fri, 06 Aug 2021 17:39:27 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:38:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 18:43:14 GMT
ENV HAPROXY_VERSION=2.0.23
# Fri, 06 Aug 2021 18:43:15 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.23.tar.gz
# Fri, 06 Aug 2021 18:43:15 GMT
ENV HAPROXY_SHA256=5ddc04e9040a07c647fa4b68fc9da6ec36063d56e12824b356e770dcf677c87a
# Fri, 06 Aug 2021 18:43:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 18:43:57 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 18:43:57 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 18:43:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 18:43:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 18:43:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fd3acdcea5682abced546ec19fb6ebee725c5184e5d91614c469c0a79e67f2d0`  
		Last Modified: Fri, 06 Aug 2021 17:40:12 GMT  
		Size: 2.7 MB (2710613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a23793c1bba0796c0f469305ee92dd0f1cb8299963e4da4249d0f5aa2fcea0`  
		Last Modified: Fri, 06 Aug 2021 18:46:06 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241f53ab5a4acdd3e2aed049c05d98291adbb4986416dabd1128c360472ac7be`  
		Last Modified: Fri, 06 Aug 2021 18:47:13 GMT  
		Size: 5.9 MB (5853688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c284b1144818b614fc43a7125f04cf5ee382305a5f7b6641e4e0a027bbe034`  
		Last Modified: Fri, 06 Aug 2021 18:47:11 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef13b521ed639a32657723d0d1724d01afdd24c4de67c6efcf508b8919fbc51c`  
		Last Modified: Fri, 06 Aug 2021 18:47:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:faa78743a4070ce601b85945359f08749c320724374a053bcbc78984f1d776aa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8532738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6217994fec122c4fd122c28d5d29e4826eafa9d5de88acc3d7d83ad97f3799ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:38:26 GMT
ADD file:bafaec4a54d6cef99b5f3660d074a3d2251e4d4bd09df9ea65f33e9bffb7d88d in / 
# Fri, 06 Aug 2021 17:38:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:19:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:12:12 GMT
ENV HAPROXY_VERSION=2.0.24
# Tue, 17 Aug 2021 17:12:12 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.24.tar.gz
# Tue, 17 Aug 2021 17:12:12 GMT
ENV HAPROXY_SHA256=210e39599966e4ece6d431d51309c261b1ab5237a329a7a9f089426b0ceeea13
# Tue, 17 Aug 2021 17:13:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 17:13:24 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:13:24 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:13:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 17:13:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:13:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:935703e1179e32e201e4a36d5664d58299dc8e7bcac197b70c295c0a59216db1`  
		Last Modified: Fri, 06 Aug 2021 17:39:15 GMT  
		Size: 2.8 MB (2821910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695b2822110160b402b8f359bb19d954a46a6ead94f868feba7d00f5a10e50e`  
		Last Modified: Fri, 06 Aug 2021 19:32:18 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93143feacf5a8155c3dcb40e44ad1c04979daf28a29bd3dbbdfd4230f6f14f8e`  
		Last Modified: Tue, 17 Aug 2021 17:17:30 GMT  
		Size: 5.7 MB (5709058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334c1e13e9e8da1012e3b0af8bd18b3da45e79365cc8060f873897396348e0fa`  
		Last Modified: Tue, 17 Aug 2021 17:17:29 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46d1878faa667b0b9ebf5b23e9e2a4f0b8fb6ee0f769e804fde66d96172f578`  
		Last Modified: Tue, 17 Aug 2021 17:17:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:00c749396fb7351d2240c1cfa0214899269f36ec409e18b971e6196950290a9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8878659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f4230e11b4f73c21d1721c05660b08deaa3b0e6cf2f728e5419ad735dda762`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:17:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:00:55 GMT
ENV HAPROXY_VERSION=2.0.24
# Tue, 17 Aug 2021 17:00:57 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.24.tar.gz
# Tue, 17 Aug 2021 17:00:59 GMT
ENV HAPROXY_SHA256=210e39599966e4ece6d431d51309c261b1ab5237a329a7a9f089426b0ceeea13
# Tue, 17 Aug 2021 17:01:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 17:01:45 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:01:45 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:01:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 17:02:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:02:08 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d374dad070e00fdb493e29a3aa64b375dbec801497e01d3b8ddbf7cc967634cb`  
		Last Modified: Fri, 06 Aug 2021 21:27:30 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc7270f46bb83656e786c31b3f0a8f79749dd9da4ea56b1d73403043e6bddc0`  
		Last Modified: Tue, 17 Aug 2021 17:06:07 GMT  
		Size: 6.1 MB (6065746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a697865ec90745cdcaf14019a2c71edf6cb298fc902be04324ecacec9c2887`  
		Last Modified: Tue, 17 Aug 2021 17:06:06 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11956179b46ff9c655e91e517885f354fbab8c5389930ed0315b200a06589a93`  
		Last Modified: Tue, 17 Aug 2021 17:06:06 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:293442e60508fc935ff391348a5996d64d6eeda811861ef39184f61e5b817aed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8381609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1c50e6367e0814cb0b7d2a9f4ce26225facb71c39faa887f22019cf419cfa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:54:24 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 14 Apr 2021 20:56:58 GMT
ENV HAPROXY_VERSION=2.0.22
# Wed, 14 Apr 2021 20:56:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.22.tar.gz
# Wed, 14 Apr 2021 20:56:58 GMT
ENV HAPROXY_SHA256=5e1dccf30a3ad782d1e3298cc4e4955b168e4aa06cad4e3ea1c0334cdc0f966d
# Wed, 14 Apr 2021 20:57:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Wed, 14 Apr 2021 20:57:33 GMT
STOPSIGNAL SIGUSR1
# Wed, 14 Apr 2021 20:57:33 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 14 Apr 2021 20:57:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Apr 2021 20:57:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 20:57:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267275aba58470c82626189a59be76cd169bd245568e2f2545ed1ee64ff8a8ff`  
		Last Modified: Wed, 14 Apr 2021 20:59:06 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5baa4dad803c789741ebc1f7cb61771b5c89417dcac880e1dc0f0eddb342ded`  
		Last Modified: Wed, 14 Apr 2021 20:59:38 GMT  
		Size: 5.8 MB (5777204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b272d803c3aad18ee76c50db0627de49c115d046c0acafc910571f0ea8e08578`  
		Last Modified: Wed, 14 Apr 2021 20:59:37 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1eb67bc4c1cfcab424bfc0385b8c9c97507568646d815a5511c42c82b4250a`  
		Last Modified: Wed, 14 Apr 2021 20:59:37 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.0.24`

```console
$ docker pull haproxy@sha256:d30af22f28fb266c3c256200497f08071631becaf37e3b567272f8456f6a09a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le

### `haproxy:2.0.24` - linux; amd64

```console
$ docker pull haproxy@sha256:a1c5f9ff2b359c49088bbc6b9cb0b4f554bbec209755037d635583572b603384
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35808441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12715ed5fcbdbbe585156fdce74f719c514ef1e768f61fb3b19958fae8c81ff9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 10:43:34 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:57:22 GMT
ENV HAPROXY_VERSION=2.0.24
# Tue, 17 Aug 2021 16:57:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.24.tar.gz
# Tue, 17 Aug 2021 16:57:22 GMT
ENV HAPROXY_SHA256=210e39599966e4ece6d431d51309c261b1ab5237a329a7a9f089426b0ceeea13
# Tue, 17 Aug 2021 16:58:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:58:09 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:58:09 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:58:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:58:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:58:10 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd06683556254cbe06dad4624837c2dcbd2fec67c7fbdd057251f0a207a9315`  
		Last Modified: Tue, 17 Aug 2021 10:53:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935dfd58b9fe509e6fe45ae00f5ad6fc439b2999e85c4c83c5f21129fe9a0d1c`  
		Last Modified: Tue, 17 Aug 2021 17:01:53 GMT  
		Size: 8.7 MB (8660509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21701f6d2099052e62c9d07c10f1fb9b75706930e3d80c74a0b304e0175c1e0`  
		Last Modified: Tue, 17 Aug 2021 17:01:51 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9615fc6254a11de1b80774aec6ccd1c914601ca6b8eb06239b903e75a1d2f7ad`  
		Last Modified: Tue, 17 Aug 2021 17:01:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0.24` - linux; 386

```console
$ docker pull haproxy@sha256:a49464ab5202942e380c8dd5b47b1666b3e03b2f9c53406e5da5a552d2ed8006
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36299478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd0cd80ffa3f0c9ceddf17d6d4b889ea9b60c36eac0fe413a7d1dd75743d1f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:41:16 GMT
ADD file:0418032b55cd0a6dd515ac277fb9f92354397503cab212d446d3a3d8c647a60f in / 
# Tue, 17 Aug 2021 01:41:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 12:14:55 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:11:09 GMT
ENV HAPROXY_VERSION=2.0.24
# Tue, 17 Aug 2021 17:11:10 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.24.tar.gz
# Tue, 17 Aug 2021 17:11:10 GMT
ENV HAPROXY_SHA256=210e39599966e4ece6d431d51309c261b1ab5237a329a7a9f089426b0ceeea13
# Tue, 17 Aug 2021 17:12:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 17:12:04 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:12:05 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:12:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 17:12:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:12:06 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c1c94e1f2523d69effaa463d64fc9962cfc67e2a956f0476c94200e7cf19edf0`  
		Last Modified: Tue, 17 Aug 2021 01:50:57 GMT  
		Size: 27.8 MB (27797627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f804b7c921abcc2fb2904ad2092beefd0224c9bd4cb1cf6477727e6f2bbd7599`  
		Last Modified: Tue, 17 Aug 2021 12:26:22 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1455615c6c79d1422fdf4658f1ed39f2a10e21d3508282d434465a8bcb88f140`  
		Last Modified: Tue, 17 Aug 2021 17:17:18 GMT  
		Size: 8.5 MB (8499907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d3f8b1ac409f7ee3ebc4c145b1d2f625ded65dcf1f5d6b794f238daf9946f6`  
		Last Modified: Tue, 17 Aug 2021 17:17:15 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e39d60b102d3195da834b27f2250dfc71c1259e01e67e796c39d74c18e213ef`  
		Last Modified: Tue, 17 Aug 2021 17:17:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0.24` - linux; ppc64le

```console
$ docker pull haproxy@sha256:8f152d991f98bdc57af8eea6d255d57a9caceb4950b2c651762664fb231e8072
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39531122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807ec85efc811fa92ea3843dda8a6f515d03ef397011b572bac1f8f5cc68ee3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:34:13 GMT
ADD file:8b9b12a994a2519f725d1ed1f4ab5a444665262678fd8e6c42cf78f32dacb7fa in / 
# Tue, 17 Aug 2021 01:34:20 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 13:36:19 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:57:56 GMT
ENV HAPROXY_VERSION=2.0.24
# Tue, 17 Aug 2021 16:57:59 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.24.tar.gz
# Tue, 17 Aug 2021 16:58:02 GMT
ENV HAPROXY_SHA256=210e39599966e4ece6d431d51309c261b1ab5237a329a7a9f089426b0ceeea13
# Tue, 17 Aug 2021 17:00:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 17:00:22 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:00:25 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:00:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 17:00:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:00:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c3e09f0e3e7f6fcb741a4c9214b63e341e1d9b53d7689a5ad6ff640b61a82541`  
		Last Modified: Tue, 17 Aug 2021 01:48:22 GMT  
		Size: 30.6 MB (30553721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb7833dc31cf72935b478f7bf90e34f0f2a22d8260da177e4648ac973af1f9c`  
		Last Modified: Tue, 17 Aug 2021 14:24:41 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f16b85495df89c40effab3516c1a1a4b0dff3138bebad6ed20f16573a37797`  
		Last Modified: Tue, 17 Aug 2021 17:05:54 GMT  
		Size: 9.0 MB (8975439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62650b31a259db4f499ebfcd267ce8dee98cb9611eaa086abef084222d5891f6`  
		Last Modified: Tue, 17 Aug 2021 17:05:52 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674a62f49984c78fd2fe84a59e3ce3d4fb548a787b2db37b9cde94b008fef727`  
		Last Modified: Tue, 17 Aug 2021 17:05:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.0.24-alpine`

```console
$ docker pull haproxy@sha256:2e8bfd949953f9331dca107bab41093c9e8e2d07cf8234e557b7467b5d1dfb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; 386
	-	linux; ppc64le

### `haproxy:2.0.24-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:884b6d5135211a189ad603aae1281d96d6f6109650a50c428a5fa8c92c34e767
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8672186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec64e5b2295f57e626d74e44adb59bcc3d6e6e903132022ae362301f4dde8e8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:43:18 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:58:22 GMT
ENV HAPROXY_VERSION=2.0.24
# Tue, 17 Aug 2021 16:58:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.24.tar.gz
# Tue, 17 Aug 2021 16:58:22 GMT
ENV HAPROXY_SHA256=210e39599966e4ece6d431d51309c261b1ab5237a329a7a9f089426b0ceeea13
# Tue, 17 Aug 2021 16:59:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:59:17 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:59:18 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:59:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:59:19 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22138861da3ab6ae8583cf62942545e1bb75874501f4a8d45d13a38c848a908`  
		Last Modified: Fri, 06 Aug 2021 19:51:27 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47e280bd219e1f95360ef417f4e0196802abf0cd04a53541bd03f967a134936`  
		Last Modified: Tue, 17 Aug 2021 17:02:05 GMT  
		Size: 5.9 MB (5857418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f241956a81b70c5b84edc5a7070e5debacd85b1e875740188247b65ca7e67e09`  
		Last Modified: Tue, 17 Aug 2021 17:02:03 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f984f4d7c2134b1a0328b10b06465f61cbfb97038f75d24eeba690c27bed0c2`  
		Last Modified: Tue, 17 Aug 2021 17:02:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0.24-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:fbaef985b8f7ff3bd7b298cdf3c78354866c1ff03467a96cc88300bf6ee3ec4d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8331654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c92957205eb96e7ae15522eb8310389baded85a67351e209e6d51cdeb4d9fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:49:32 GMT
ADD file:7f2c7deda009eabdcbbdccb11e854043d32c498e64e7e1ca02165d7bb4261d39 in / 
# Fri, 06 Aug 2021 17:49:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:15:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:39:03 GMT
ENV HAPROXY_VERSION=2.0.24
# Tue, 17 Aug 2021 16:39:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.24.tar.gz
# Tue, 17 Aug 2021 16:39:04 GMT
ENV HAPROXY_SHA256=210e39599966e4ece6d431d51309c261b1ab5237a329a7a9f089426b0ceeea13
# Tue, 17 Aug 2021 16:39:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:39:27 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:39:28 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:39:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:39:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:39:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f465bb3e9fcd0c42f936ecc566c6e40353c00f3089b2b2c2ea1663c30f89d3ab`  
		Last Modified: Fri, 06 Aug 2021 17:51:00 GMT  
		Size: 2.6 MB (2626350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332ccafb58fe1d8ed3d3d5ad9c01adba33d922f28a398285d2eb67fed7c8bee8`  
		Last Modified: Fri, 06 Aug 2021 18:20:57 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f04114dc0b073aea02e8ae5c98b1e7a9873eab7b89b12dd77d6e0f6b9c16e73`  
		Last Modified: Tue, 17 Aug 2021 16:42:22 GMT  
		Size: 5.7 MB (5703536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2976a39edd1b3719db70e49c3ccecf657ae05d367114678fbe9cd1e45ca01e92`  
		Last Modified: Tue, 17 Aug 2021 16:42:19 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e145ae037e98a0899f2281d00ce7a4b7c2d87b1f5e8f2f88ab6304fc5cc636`  
		Last Modified: Tue, 17 Aug 2021 16:42:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0.24-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:faa78743a4070ce601b85945359f08749c320724374a053bcbc78984f1d776aa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8532738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6217994fec122c4fd122c28d5d29e4826eafa9d5de88acc3d7d83ad97f3799ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:38:26 GMT
ADD file:bafaec4a54d6cef99b5f3660d074a3d2251e4d4bd09df9ea65f33e9bffb7d88d in / 
# Fri, 06 Aug 2021 17:38:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:19:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:12:12 GMT
ENV HAPROXY_VERSION=2.0.24
# Tue, 17 Aug 2021 17:12:12 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.24.tar.gz
# Tue, 17 Aug 2021 17:12:12 GMT
ENV HAPROXY_SHA256=210e39599966e4ece6d431d51309c261b1ab5237a329a7a9f089426b0ceeea13
# Tue, 17 Aug 2021 17:13:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 17:13:24 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:13:24 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:13:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 17:13:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:13:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:935703e1179e32e201e4a36d5664d58299dc8e7bcac197b70c295c0a59216db1`  
		Last Modified: Fri, 06 Aug 2021 17:39:15 GMT  
		Size: 2.8 MB (2821910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695b2822110160b402b8f359bb19d954a46a6ead94f868feba7d00f5a10e50e`  
		Last Modified: Fri, 06 Aug 2021 19:32:18 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93143feacf5a8155c3dcb40e44ad1c04979daf28a29bd3dbbdfd4230f6f14f8e`  
		Last Modified: Tue, 17 Aug 2021 17:17:30 GMT  
		Size: 5.7 MB (5709058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334c1e13e9e8da1012e3b0af8bd18b3da45e79365cc8060f873897396348e0fa`  
		Last Modified: Tue, 17 Aug 2021 17:17:29 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46d1878faa667b0b9ebf5b23e9e2a4f0b8fb6ee0f769e804fde66d96172f578`  
		Last Modified: Tue, 17 Aug 2021 17:17:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.0.24-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:00c749396fb7351d2240c1cfa0214899269f36ec409e18b971e6196950290a9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8878659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f4230e11b4f73c21d1721c05660b08deaa3b0e6cf2f728e5419ad735dda762`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:17:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:00:55 GMT
ENV HAPROXY_VERSION=2.0.24
# Tue, 17 Aug 2021 17:00:57 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.0/src/haproxy-2.0.24.tar.gz
# Tue, 17 Aug 2021 17:00:59 GMT
ENV HAPROXY_SHA256=210e39599966e4ece6d431d51309c261b1ab5237a329a7a9f089426b0ceeea13
# Tue, 17 Aug 2021 17:01:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 17:01:45 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:01:45 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:01:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 17:02:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:02:08 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d374dad070e00fdb493e29a3aa64b375dbec801497e01d3b8ddbf7cc967634cb`  
		Last Modified: Fri, 06 Aug 2021 21:27:30 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc7270f46bb83656e786c31b3f0a8f79749dd9da4ea56b1d73403043e6bddc0`  
		Last Modified: Tue, 17 Aug 2021 17:06:07 GMT  
		Size: 6.1 MB (6065746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a697865ec90745cdcaf14019a2c71edf6cb298fc902be04324ecacec9c2887`  
		Last Modified: Tue, 17 Aug 2021 17:06:06 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11956179b46ff9c655e91e517885f354fbab8c5389930ed0315b200a06589a93`  
		Last Modified: Tue, 17 Aug 2021 17:06:06 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.2`

```console
$ docker pull haproxy@sha256:f1d2a8ce163777b8c2b9cf7ce493737d996f4b10b1158e210204dd999077697d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.2` - linux; amd64

```console
$ docker pull haproxy@sha256:cc763768ad30569fe20614c7f37655959de9eb93d027ab47bd8fcb1c6ab70e10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36424212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c28c2993780b4d4b592367c2c103f3e07220f9b78d67e667fe880b5b2ac912`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 10:43:34 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:55:10 GMT
ENV HAPROXY_VERSION=2.2.16
# Tue, 17 Aug 2021 16:55:10 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.16.tar.gz
# Tue, 17 Aug 2021 16:55:10 GMT
ENV HAPROXY_SHA256=b81e03a181070d1f7bcdaeec9f09af701fb1ab015c3c9c997a881f4773e29375
# Tue, 17 Aug 2021 16:56:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:56:00 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:56:01 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:56:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:56:02 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd06683556254cbe06dad4624837c2dcbd2fec67c7fbdd057251f0a207a9315`  
		Last Modified: Tue, 17 Aug 2021 10:53:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b229167a1afcd43f8c6ce16dbcc014a1d2016031e595d680d27287d0f2ee04`  
		Last Modified: Tue, 17 Aug 2021 17:01:29 GMT  
		Size: 9.3 MB (9276279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d71598d745f25388160dd2b4a6d59f127d928ebf3a99f02b0c87642233d5a96`  
		Last Modified: Tue, 17 Aug 2021 17:01:26 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44da4a39c0f8f2e761d03e4a367aff8cc37623b27d1cbbcf498a7121e0327287`  
		Last Modified: Tue, 17 Aug 2021 17:01:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:596c6aacbbe2f61d9a5aa5dfade6ca62dbda46fc57fd868b525d8c77e244e289
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33823730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5cd379c6517c8c2ec70750abee0b761468be97d294e79af0f31387108ec576`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:56:50 GMT
ADD file:f29260935f1f8b3eef5eb0d5e49dd4cf5370e8731a3f4006d6023724bce09601 in / 
# Tue, 17 Aug 2021 01:56:51 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:39:10 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:42:32 GMT
ENV HAPROXY_VERSION=2.2.15
# Tue, 17 Aug 2021 08:42:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.15.tar.gz
# Tue, 17 Aug 2021 08:42:33 GMT
ENV HAPROXY_SHA256=48cd0e1cb5de889657cd080fe66cc2ada8198cfece55d63f3a0c011553384cd9
# Tue, 17 Aug 2021 08:43:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:43:26 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:43:26 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:43:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 08:43:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:43:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3dfab4a5b2accf2d709d8c7d14a42715948ecf2d6da4943a6e2c0de8ae7536a0`  
		Last Modified: Tue, 17 Aug 2021 02:12:42 GMT  
		Size: 24.9 MB (24879063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeabbf4f2af3ef66d78a317a4b3a0704a061a5de2611c57b0bfc47b775c2ed8b`  
		Last Modified: Tue, 17 Aug 2021 08:48:10 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d35076922a474c5d83849c27a51d0ab330db7866afd6862a95c151067a7a450`  
		Last Modified: Tue, 17 Aug 2021 08:49:17 GMT  
		Size: 8.9 MB (8942721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23217138469743a20edde3b03ce843e94ff9094eea19d81b6ed6de5a89375290`  
		Last Modified: Tue, 17 Aug 2021 08:49:12 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3895fe1be87a0e3a0ddbb7d605731e2dc1300daa91cf089c93bf3d893f98221c`  
		Last Modified: Tue, 17 Aug 2021 08:49:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:70426a7e8699a65eb6b0ad86f1ba2a6d2402b5487f5547889bb3ca59a6f4ea3b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31471102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88276f03072f8e05464906098bb57967cf988134d67d34db13824b7b969a93e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 02:14:25 GMT
ADD file:ca8cc4b509e305fa07662fbf2234ed78f0056569f6ca047305dc02bcd60f1558 in / 
# Tue, 17 Aug 2021 02:14:26 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 16:10:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:14:22 GMT
ENV HAPROXY_VERSION=2.2.15
# Tue, 17 Aug 2021 16:14:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.15.tar.gz
# Tue, 17 Aug 2021 16:14:23 GMT
ENV HAPROXY_SHA256=48cd0e1cb5de889657cd080fe66cc2ada8198cfece55d63f3a0c011553384cd9
# Tue, 17 Aug 2021 16:15:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:15:11 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:15:11 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:15:14 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:13e3f03410ff211945a725435c13065288d48a8cb740f0530e7588012c2679a4`  
		Last Modified: Tue, 17 Aug 2021 02:30:58 GMT  
		Size: 22.7 MB (22746254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb366ce7907325b732435009125848fb9596a1afdb0f87a8703cdf4342e91a4e`  
		Last Modified: Tue, 17 Aug 2021 16:21:35 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d6220cc046546092b3278831e6378a28c51d3b82178a7ef7e0ee87c6450cff`  
		Last Modified: Tue, 17 Aug 2021 16:22:54 GMT  
		Size: 8.7 MB (8722902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0446e685e5aadb9e112a651c90c128ca7ce2d302c4fd84d0d935ee25f50887`  
		Last Modified: Tue, 17 Aug 2021 16:22:49 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246353e4e7e0c38a196ce576f28f4642f7d8efc1ff4af68e1209e0fc032e5b67`  
		Last Modified: Tue, 17 Aug 2021 16:22:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:7a260be1dd3bb32c75bba2a8c4430a01bf49d0bf0e487a5c12d56ebede019f6c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35049380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a404555dd0b5f8c75715801386bcbc457edad2200a351fbee75b5978e5442f25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:12:02 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:14:51 GMT
ENV HAPROXY_VERSION=2.2.15
# Tue, 17 Aug 2021 08:14:51 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.15.tar.gz
# Tue, 17 Aug 2021 08:14:51 GMT
ENV HAPROXY_SHA256=48cd0e1cb5de889657cd080fe66cc2ada8198cfece55d63f3a0c011553384cd9
# Tue, 17 Aug 2021 08:15:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:15:35 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:15:35 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:15:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 08:15:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:15:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc63cf29191f59ddbc41452b9edbe5f8145c4370cd74d3981d50a862173029b`  
		Last Modified: Tue, 17 Aug 2021 08:19:14 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94fb43dc53b5907e378a0e4d9c20050bce08a32d86eaab396edade1523305ad`  
		Last Modified: Tue, 17 Aug 2021 08:20:05 GMT  
		Size: 9.1 MB (9132357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbdddf6d5b649cc33d41a240a0cb893f334c0435cc52953432f2a6a1ea8c502`  
		Last Modified: Tue, 17 Aug 2021 08:20:04 GMT  
		Size: 456.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1139c013c33a681de0bd1ce4c1f6dde8ab084ab5a25abbc98e606d1094acdb`  
		Last Modified: Tue, 17 Aug 2021 08:20:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2` - linux; 386

```console
$ docker pull haproxy@sha256:8b46c6fd393aca59b28af3be323a590a5a092b485acecf19624c64af4fbcd1f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (37022292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1ef64460ac5f0f59202914725f286a66e25a29ed12783a4417e452620c38f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:41:16 GMT
ADD file:0418032b55cd0a6dd515ac277fb9f92354397503cab212d446d3a3d8c647a60f in / 
# Tue, 17 Aug 2021 01:41:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 12:14:55 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:08:30 GMT
ENV HAPROXY_VERSION=2.2.16
# Tue, 17 Aug 2021 17:08:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.16.tar.gz
# Tue, 17 Aug 2021 17:08:30 GMT
ENV HAPROXY_SHA256=b81e03a181070d1f7bcdaeec9f09af701fb1ab015c3c9c997a881f4773e29375
# Tue, 17 Aug 2021 17:09:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 17:09:26 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:09:26 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:09:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 17:09:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:09:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c1c94e1f2523d69effaa463d64fc9962cfc67e2a956f0476c94200e7cf19edf0`  
		Last Modified: Tue, 17 Aug 2021 01:50:57 GMT  
		Size: 27.8 MB (27797627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f804b7c921abcc2fb2904ad2092beefd0224c9bd4cb1cf6477727e6f2bbd7599`  
		Last Modified: Tue, 17 Aug 2021 12:26:22 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3b02767eebad041dfe0c42b5b8416ed112171b7cdb1123d79ef36824c5d3fb`  
		Last Modified: Tue, 17 Aug 2021 17:16:51 GMT  
		Size: 9.2 MB (9222721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf970afa5e264fbd96ab8731b56e5f41579ab28de48193abecb3ceed9b9ac79`  
		Last Modified: Tue, 17 Aug 2021 17:16:49 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2e57356c93c63179b68c20e987e009b9316f67c7cb19ae6a7a752e906459be`  
		Last Modified: Tue, 17 Aug 2021 17:16:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2` - linux; mips64le

```console
$ docker pull haproxy@sha256:73e3a666c11c04e4e7339cd809257facc097509b0c2d2a33e73bc941036cae1c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34716856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb76cac5d320ef0c4559ccccbf073611c0e5ca84379a70e8d044fd9dc0c34b63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:12:26 GMT
ADD file:8bd279803ead4ddce8db90b65e89c423f84fbf6042bfbeae8c09486b2e884cde in / 
# Tue, 17 Aug 2021 01:12:27 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:10:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 14:18:23 GMT
ENV HAPROXY_VERSION=2.2.15
# Tue, 17 Aug 2021 14:18:24 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.15.tar.gz
# Tue, 17 Aug 2021 14:18:24 GMT
ENV HAPROXY_SHA256=48cd0e1cb5de889657cd080fe66cc2ada8198cfece55d63f3a0c011553384cd9
# Tue, 17 Aug 2021 14:20:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 14:20:47 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 14:20:47 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 14:20:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 14:20:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:20:49 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a711e3e37b88ef77496c07ed663bb4270ecba9057eba452a91cc9be0bafb9c32`  
		Last Modified: Tue, 17 Aug 2021 01:21:44 GMT  
		Size: 25.8 MB (25813007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac33edc8b81dffec584b1a7ca6a8abea967f70259323fc62ff423b9c01642e`  
		Last Modified: Tue, 17 Aug 2021 14:27:23 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce78ff61307347a67ad3e567f723e150acc735ca46e35fc426c4e9449d04cb9`  
		Last Modified: Tue, 17 Aug 2021 14:28:26 GMT  
		Size: 8.9 MB (8901905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319926763df6e4d66f265428750bbcd69996a54a81927207690d1b375fb644c2`  
		Last Modified: Tue, 17 Aug 2021 14:28:19 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb67f56e105c01b2b690d79263fba62c53adc5c3b792d0d8962a9fd073bb8da`  
		Last Modified: Tue, 17 Aug 2021 14:28:19 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2` - linux; ppc64le

```console
$ docker pull haproxy@sha256:88c996e4fc2f076f19a32c21b19d35e13b542270d5b9483ce1f92106a8c17f52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40367607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cede20e43d3726fd325da7676ec24a0e3dc9138200c2db519452cf329aeefdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:34:13 GMT
ADD file:8b9b12a994a2519f725d1ed1f4ab5a444665262678fd8e6c42cf78f32dacb7fa in / 
# Tue, 17 Aug 2021 01:34:20 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 13:36:19 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:53:33 GMT
ENV HAPROXY_VERSION=2.2.16
# Tue, 17 Aug 2021 16:53:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.16.tar.gz
# Tue, 17 Aug 2021 16:53:43 GMT
ENV HAPROXY_SHA256=b81e03a181070d1f7bcdaeec9f09af701fb1ab015c3c9c997a881f4773e29375
# Tue, 17 Aug 2021 16:56:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:56:17 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:56:20 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:56:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:56:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:56:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c3e09f0e3e7f6fcb741a4c9214b63e341e1d9b53d7689a5ad6ff640b61a82541`  
		Last Modified: Tue, 17 Aug 2021 01:48:22 GMT  
		Size: 30.6 MB (30553721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb7833dc31cf72935b478f7bf90e34f0f2a22d8260da177e4648ac973af1f9c`  
		Last Modified: Tue, 17 Aug 2021 14:24:41 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d84879de24af9f70426c09557aac4f384f4a9e786ded7d0b01a343a253e9256`  
		Last Modified: Tue, 17 Aug 2021 17:05:27 GMT  
		Size: 9.8 MB (9811923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d02b729e8d9310f593bcec05d440c04dd071d292a4cb96ff5d252572c451606`  
		Last Modified: Tue, 17 Aug 2021 17:05:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309d324b251b7b105d34f2bd437a334ec8460d1067f48e35bc51b5f70b7b9ede`  
		Last Modified: Tue, 17 Aug 2021 17:05:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2` - linux; s390x

```console
$ docker pull haproxy@sha256:21fed401c5e656f7028655495b5ba02b94dc91a908a8c13cf22b67f25c0418b9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34803562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b6d8bfef54d0341d243fbbe87474ea91266b061d4cdb624cb5c7d6fd5774d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 07:18:12 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 07:22:34 GMT
ENV HAPROXY_VERSION=2.2.15
# Tue, 17 Aug 2021 07:22:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.15.tar.gz
# Tue, 17 Aug 2021 07:22:35 GMT
ENV HAPROXY_SHA256=48cd0e1cb5de889657cd080fe66cc2ada8198cfece55d63f3a0c011553384cd9
# Tue, 17 Aug 2021 07:23:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 07:23:15 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 07:23:15 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 07:23:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 07:23:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 07:23:17 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16a2f2a1452470a1d818d8d16934d08d2a57b312ceabcce8c1cfad6c99f00a2`  
		Last Modified: Tue, 17 Aug 2021 07:28:00 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d88d8db096ad2bcd6304e4d412a29b28685e39ce4aa244c1b9b21982110a475`  
		Last Modified: Tue, 17 Aug 2021 07:28:34 GMT  
		Size: 9.0 MB (9040756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d042c59536af9e3a2d96de6be63053ddf6eaed69cf5b0f543cc4ece1ca5dcb86`  
		Last Modified: Tue, 17 Aug 2021 07:28:33 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0806cf6f5a66872eb61979cc842ebade80b7b0e29fb7098dd9416ecca535ee57`  
		Last Modified: Tue, 17 Aug 2021 07:28:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.2-alpine`

```console
$ docker pull haproxy@sha256:e1fcbd4b021593186c6afb463d10411b3e2fdc5d596ee3581088368df0191579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.2-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:56bc50a702e5310218e08f581dbbe928101b6c083a85090f707d2d1d6ea7b5a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9185780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd85c2ced7c2e0a0f8386522864ac67e3081b0e4bcec4989f762cd1429ea21d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:43:18 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:56:10 GMT
ENV HAPROXY_VERSION=2.2.16
# Tue, 17 Aug 2021 16:56:10 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.16.tar.gz
# Tue, 17 Aug 2021 16:56:10 GMT
ENV HAPROXY_SHA256=b81e03a181070d1f7bcdaeec9f09af701fb1ab015c3c9c997a881f4773e29375
# Tue, 17 Aug 2021 16:57:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:57:08 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:57:08 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:57:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:57:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:57:09 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22138861da3ab6ae8583cf62942545e1bb75874501f4a8d45d13a38c848a908`  
		Last Modified: Fri, 06 Aug 2021 19:51:27 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3f929d929bb9e45a3f18e89c5334f254fa343aa2bf355e46c53059439db33d`  
		Last Modified: Tue, 17 Aug 2021 17:01:40 GMT  
		Size: 6.4 MB (6371009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ab04e8d365d0e9a64e5c66520b901d3ef4ef1544c78b77ae82f3ad3db34d87`  
		Last Modified: Tue, 17 Aug 2021 17:01:39 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ba9ae244af88f2626bffcd2963ffcae650ba499e91d500bf9f34059a9ddf70`  
		Last Modified: Tue, 17 Aug 2021 17:01:39 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:50602b8c10dabe847bbb359b30e4aa80d7b4091d948045aa0f4a49390486c83b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8897553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af081a4d7f70aa6da2a8ace73978df041f5fbb6ccdcca518a8da076d0afccfa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:49:32 GMT
ADD file:7f2c7deda009eabdcbbdccb11e854043d32c498e64e7e1ca02165d7bb4261d39 in / 
# Fri, 06 Aug 2021 17:49:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:15:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:38:20 GMT
ENV HAPROXY_VERSION=2.2.16
# Tue, 17 Aug 2021 16:38:21 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.16.tar.gz
# Tue, 17 Aug 2021 16:38:21 GMT
ENV HAPROXY_SHA256=b81e03a181070d1f7bcdaeec9f09af701fb1ab015c3c9c997a881f4773e29375
# Tue, 17 Aug 2021 16:38:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:38:49 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:38:49 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:38:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:38:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f465bb3e9fcd0c42f936ecc566c6e40353c00f3089b2b2c2ea1663c30f89d3ab`  
		Last Modified: Fri, 06 Aug 2021 17:51:00 GMT  
		Size: 2.6 MB (2626350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332ccafb58fe1d8ed3d3d5ad9c01adba33d922f28a398285d2eb67fed7c8bee8`  
		Last Modified: Fri, 06 Aug 2021 18:20:57 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4cba68dd4f3bce350901a2cd42e506ace778145f33252c653828174c8565b6`  
		Last Modified: Tue, 17 Aug 2021 16:42:06 GMT  
		Size: 6.3 MB (6269434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e454f1eae153ff572a78e69b8aeaf0def78e5640f460e5b8221a6a6cbcdaa295`  
		Last Modified: Tue, 17 Aug 2021 16:42:03 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397049d890a662fe6f939322ac8ccabc83e4095886c2c784afd5a7e7ae1c86b4`  
		Last Modified: Tue, 17 Aug 2021 16:42:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:0014f4fc0904a70de59dec4405b9b56408fd1578fb2cf6a894df4895f5284c69
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8600315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2aa1b2025183736b5844c13d1478fb2629c4d784746cd30de6180b0fe98137`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:57:32 GMT
ADD file:3a35ff3ac0d80289d419a4d6d8319610c38e1936d296addafb9aaf506946230f in / 
# Fri, 06 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:54:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 19:57:46 GMT
ENV HAPROXY_VERSION=2.2.15
# Fri, 06 Aug 2021 19:57:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.15.tar.gz
# Fri, 06 Aug 2021 19:57:48 GMT
ENV HAPROXY_SHA256=48cd0e1cb5de889657cd080fe66cc2ada8198cfece55d63f3a0c011553384cd9
# Fri, 06 Aug 2021 19:58:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 19:58:25 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 19:58:26 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 19:58:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 19:58:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 19:58:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4ee0caa23b369b04827640a4be298bf4ff7bacd030c77e915f5d7fb8f987594a`  
		Last Modified: Fri, 06 Aug 2021 17:58:57 GMT  
		Size: 2.4 MB (2429359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548ff9918828f96cb9a5e5656ea589d79e6fb1d7b9f0d693feff2dbefc6929fe`  
		Last Modified: Fri, 06 Aug 2021 20:02:54 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddf5af9d70d7a9d5384e764a7aa2833e521512b909177ec9e02f09bb02aecac`  
		Last Modified: Fri, 06 Aug 2021 20:04:02 GMT  
		Size: 6.2 MB (6169189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b769ef387a8f204bad604f8a382db517f65817904c245715d2582f5e9ecaf489`  
		Last Modified: Fri, 06 Aug 2021 20:04:00 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3d7a3d035423010c517ee9d41d2a6ac34e18b9b35c515cee507dcf0d31928d`  
		Last Modified: Fri, 06 Aug 2021 20:04:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:11505d6576345f1fe34d36c793bc0d1bb86ae685e91d5ecb6787098c9cbc5f4b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9101366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45bca9e79d00a7a244207ab4fcb68d88df1cb3c1400ade77f43abee0314f6c10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:39:26 GMT
ADD file:1a8fd1066485e1261462e689c1a072f010c1d3be904b73ef2b84128fac652951 in / 
# Fri, 06 Aug 2021 17:39:27 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:38:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 18:42:19 GMT
ENV HAPROXY_VERSION=2.2.15
# Fri, 06 Aug 2021 18:42:19 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.15.tar.gz
# Fri, 06 Aug 2021 18:42:19 GMT
ENV HAPROXY_SHA256=48cd0e1cb5de889657cd080fe66cc2ada8198cfece55d63f3a0c011553384cd9
# Fri, 06 Aug 2021 18:43:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 18:43:03 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 18:43:03 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 18:43:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 18:43:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 18:43:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fd3acdcea5682abced546ec19fb6ebee725c5184e5d91614c469c0a79e67f2d0`  
		Last Modified: Fri, 06 Aug 2021 17:40:12 GMT  
		Size: 2.7 MB (2710613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a23793c1bba0796c0f469305ee92dd0f1cb8299963e4da4249d0f5aa2fcea0`  
		Last Modified: Fri, 06 Aug 2021 18:46:06 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f448012a08bb13f87665b4485ea76a8fa07795306cddef93bed57e360298c0`  
		Last Modified: Fri, 06 Aug 2021 18:46:58 GMT  
		Size: 6.4 MB (6388990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976fd38855f0ae3ce20a1b26d4ea2f0c149dfcafe5e1b1ec6c0f46d4f530ffb3`  
		Last Modified: Fri, 06 Aug 2021 18:46:57 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b33b031163e780b7939a2d972d4fe4707793a35c516db90a926bd26d2b4e91c`  
		Last Modified: Fri, 06 Aug 2021 18:46:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:e19131c9982c9af0b47a25e200095a92ab87ae9f8dca1fe4aed26ae0e90ced54
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9050001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868780f890b28ae16dc54c895cb97d1e4dda0e437e0bfa48442a66b949ef767f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:38:26 GMT
ADD file:bafaec4a54d6cef99b5f3660d074a3d2251e4d4bd09df9ea65f33e9bffb7d88d in / 
# Fri, 06 Aug 2021 17:38:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:19:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:09:43 GMT
ENV HAPROXY_VERSION=2.2.16
# Tue, 17 Aug 2021 17:09:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.16.tar.gz
# Tue, 17 Aug 2021 17:09:43 GMT
ENV HAPROXY_SHA256=b81e03a181070d1f7bcdaeec9f09af701fb1ab015c3c9c997a881f4773e29375
# Tue, 17 Aug 2021 17:10:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 17:10:55 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:10:55 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:10:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 17:10:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:10:56 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:935703e1179e32e201e4a36d5664d58299dc8e7bcac197b70c295c0a59216db1`  
		Last Modified: Fri, 06 Aug 2021 17:39:15 GMT  
		Size: 2.8 MB (2821910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695b2822110160b402b8f359bb19d954a46a6ead94f868feba7d00f5a10e50e`  
		Last Modified: Fri, 06 Aug 2021 19:32:18 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05d77252a068be24ed30adc7a41d564e73ba2c4dc7f792f5c4d7b11473cce07`  
		Last Modified: Tue, 17 Aug 2021 17:17:04 GMT  
		Size: 6.2 MB (6226324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55f27d6215ce8aa788bc4fc340e39ac86fa2207594a0a955709fc7699dca208`  
		Last Modified: Tue, 17 Aug 2021 17:17:02 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb3310368ff204641a1be872c924e2053d4a423898977f83120b7b4e3357d98`  
		Last Modified: Tue, 17 Aug 2021 17:17:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:175bc701c960c871408a5601c110b22be001331f5c504205ca8c08b137e6ff07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9521499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6d32dbb24bbd5e29c43ed7e3e0ce8ba9dd3a010c44bc023182036444134ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:17:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:56:44 GMT
ENV HAPROXY_VERSION=2.2.16
# Tue, 17 Aug 2021 16:56:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.16.tar.gz
# Tue, 17 Aug 2021 16:56:48 GMT
ENV HAPROXY_SHA256=b81e03a181070d1f7bcdaeec9f09af701fb1ab015c3c9c997a881f4773e29375
# Tue, 17 Aug 2021 16:57:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:57:30 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:57:31 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:57:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:57:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:57:42 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d374dad070e00fdb493e29a3aa64b375dbec801497e01d3b8ddbf7cc967634cb`  
		Last Modified: Fri, 06 Aug 2021 21:27:30 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6860d80855c25358d091d20f18a9c35876c87b1e04a90b034437223d18bde93b`  
		Last Modified: Tue, 17 Aug 2021 17:05:40 GMT  
		Size: 6.7 MB (6708583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be759e2ed68dc74dd6ce0fdf47303c51d6517675bbc73e073a70491c6bfb9c2`  
		Last Modified: Tue, 17 Aug 2021 17:05:39 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1657f0ace1a0107268cecd3945096e7c9f35d07d8bb37def7a8865982f4b6ed`  
		Last Modified: Tue, 17 Aug 2021 17:05:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:46c26b096b2727e54bd284ce787acdf250105eef2499a26ad3c781ee07ddea65
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8944856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b011e7b2da4973daf7d6c3188e86cb22d4bde3bbfb56281369bc18ac0b7ad66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:54:24 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Thu, 29 Apr 2021 17:43:14 GMT
ENV HAPROXY_VERSION=2.2.14
# Thu, 29 Apr 2021 17:43:14 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.14.tar.gz
# Thu, 29 Apr 2021 17:43:14 GMT
ENV HAPROXY_SHA256=6a9b702f04b07786f3e5878de8172a727acfdfdbc1cefe1c7a438df372f2fb61
# Thu, 29 Apr 2021 17:43:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Thu, 29 Apr 2021 17:43:58 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 Apr 2021 17:43:58 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 29 Apr 2021 17:43:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 29 Apr 2021 17:44:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Apr 2021 17:44:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267275aba58470c82626189a59be76cd169bd245568e2f2545ed1ee64ff8a8ff`  
		Last Modified: Wed, 14 Apr 2021 20:59:06 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bd90fedbb3ad8d7ce19548b2051961aba93878bb770199538eb7d77b84c615`  
		Last Modified: Thu, 29 Apr 2021 17:45:16 GMT  
		Size: 6.3 MB (6340449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b7746ababb0b63330117e707635f5d6f4bb1d0a1641718dc1c4c49af72d0f0`  
		Last Modified: Thu, 29 Apr 2021 17:45:16 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b76e05f6e27ece4bdcb064a2e1f70ce99db1fd371bdb31de6f2a4ad604fd2f`  
		Last Modified: Thu, 29 Apr 2021 17:45:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.2.16`

```console
$ docker pull haproxy@sha256:0c5c3a0c7fd74cb500f601b017dd9021c5b153e3c8676bfceff5ad2fc3dd98be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le

### `haproxy:2.2.16` - linux; amd64

```console
$ docker pull haproxy@sha256:cc763768ad30569fe20614c7f37655959de9eb93d027ab47bd8fcb1c6ab70e10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36424212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c28c2993780b4d4b592367c2c103f3e07220f9b78d67e667fe880b5b2ac912`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 10:43:34 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:55:10 GMT
ENV HAPROXY_VERSION=2.2.16
# Tue, 17 Aug 2021 16:55:10 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.16.tar.gz
# Tue, 17 Aug 2021 16:55:10 GMT
ENV HAPROXY_SHA256=b81e03a181070d1f7bcdaeec9f09af701fb1ab015c3c9c997a881f4773e29375
# Tue, 17 Aug 2021 16:56:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:56:00 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:56:01 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:56:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:56:02 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd06683556254cbe06dad4624837c2dcbd2fec67c7fbdd057251f0a207a9315`  
		Last Modified: Tue, 17 Aug 2021 10:53:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b229167a1afcd43f8c6ce16dbcc014a1d2016031e595d680d27287d0f2ee04`  
		Last Modified: Tue, 17 Aug 2021 17:01:29 GMT  
		Size: 9.3 MB (9276279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d71598d745f25388160dd2b4a6d59f127d928ebf3a99f02b0c87642233d5a96`  
		Last Modified: Tue, 17 Aug 2021 17:01:26 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44da4a39c0f8f2e761d03e4a367aff8cc37623b27d1cbbcf498a7121e0327287`  
		Last Modified: Tue, 17 Aug 2021 17:01:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2.16` - linux; 386

```console
$ docker pull haproxy@sha256:8b46c6fd393aca59b28af3be323a590a5a092b485acecf19624c64af4fbcd1f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (37022292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1ef64460ac5f0f59202914725f286a66e25a29ed12783a4417e452620c38f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:41:16 GMT
ADD file:0418032b55cd0a6dd515ac277fb9f92354397503cab212d446d3a3d8c647a60f in / 
# Tue, 17 Aug 2021 01:41:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 12:14:55 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:08:30 GMT
ENV HAPROXY_VERSION=2.2.16
# Tue, 17 Aug 2021 17:08:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.16.tar.gz
# Tue, 17 Aug 2021 17:08:30 GMT
ENV HAPROXY_SHA256=b81e03a181070d1f7bcdaeec9f09af701fb1ab015c3c9c997a881f4773e29375
# Tue, 17 Aug 2021 17:09:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 17:09:26 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:09:26 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:09:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 17:09:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:09:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c1c94e1f2523d69effaa463d64fc9962cfc67e2a956f0476c94200e7cf19edf0`  
		Last Modified: Tue, 17 Aug 2021 01:50:57 GMT  
		Size: 27.8 MB (27797627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f804b7c921abcc2fb2904ad2092beefd0224c9bd4cb1cf6477727e6f2bbd7599`  
		Last Modified: Tue, 17 Aug 2021 12:26:22 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3b02767eebad041dfe0c42b5b8416ed112171b7cdb1123d79ef36824c5d3fb`  
		Last Modified: Tue, 17 Aug 2021 17:16:51 GMT  
		Size: 9.2 MB (9222721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf970afa5e264fbd96ab8731b56e5f41579ab28de48193abecb3ceed9b9ac79`  
		Last Modified: Tue, 17 Aug 2021 17:16:49 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2e57356c93c63179b68c20e987e009b9316f67c7cb19ae6a7a752e906459be`  
		Last Modified: Tue, 17 Aug 2021 17:16:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2.16` - linux; ppc64le

```console
$ docker pull haproxy@sha256:88c996e4fc2f076f19a32c21b19d35e13b542270d5b9483ce1f92106a8c17f52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40367607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cede20e43d3726fd325da7676ec24a0e3dc9138200c2db519452cf329aeefdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:34:13 GMT
ADD file:8b9b12a994a2519f725d1ed1f4ab5a444665262678fd8e6c42cf78f32dacb7fa in / 
# Tue, 17 Aug 2021 01:34:20 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 13:36:19 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:53:33 GMT
ENV HAPROXY_VERSION=2.2.16
# Tue, 17 Aug 2021 16:53:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.16.tar.gz
# Tue, 17 Aug 2021 16:53:43 GMT
ENV HAPROXY_SHA256=b81e03a181070d1f7bcdaeec9f09af701fb1ab015c3c9c997a881f4773e29375
# Tue, 17 Aug 2021 16:56:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:56:17 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:56:20 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:56:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:56:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:56:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c3e09f0e3e7f6fcb741a4c9214b63e341e1d9b53d7689a5ad6ff640b61a82541`  
		Last Modified: Tue, 17 Aug 2021 01:48:22 GMT  
		Size: 30.6 MB (30553721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb7833dc31cf72935b478f7bf90e34f0f2a22d8260da177e4648ac973af1f9c`  
		Last Modified: Tue, 17 Aug 2021 14:24:41 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d84879de24af9f70426c09557aac4f384f4a9e786ded7d0b01a343a253e9256`  
		Last Modified: Tue, 17 Aug 2021 17:05:27 GMT  
		Size: 9.8 MB (9811923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d02b729e8d9310f593bcec05d440c04dd071d292a4cb96ff5d252572c451606`  
		Last Modified: Tue, 17 Aug 2021 17:05:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309d324b251b7b105d34f2bd437a334ec8460d1067f48e35bc51b5f70b7b9ede`  
		Last Modified: Tue, 17 Aug 2021 17:05:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.2.16-alpine`

```console
$ docker pull haproxy@sha256:84e7078ca97288607a9d2b07c8476dd969b35b5584a9b3a9e2e22ff0c67c6932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; 386
	-	linux; ppc64le

### `haproxy:2.2.16-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:56bc50a702e5310218e08f581dbbe928101b6c083a85090f707d2d1d6ea7b5a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9185780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd85c2ced7c2e0a0f8386522864ac67e3081b0e4bcec4989f762cd1429ea21d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:43:18 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:56:10 GMT
ENV HAPROXY_VERSION=2.2.16
# Tue, 17 Aug 2021 16:56:10 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.16.tar.gz
# Tue, 17 Aug 2021 16:56:10 GMT
ENV HAPROXY_SHA256=b81e03a181070d1f7bcdaeec9f09af701fb1ab015c3c9c997a881f4773e29375
# Tue, 17 Aug 2021 16:57:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:57:08 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:57:08 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:57:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:57:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:57:09 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22138861da3ab6ae8583cf62942545e1bb75874501f4a8d45d13a38c848a908`  
		Last Modified: Fri, 06 Aug 2021 19:51:27 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3f929d929bb9e45a3f18e89c5334f254fa343aa2bf355e46c53059439db33d`  
		Last Modified: Tue, 17 Aug 2021 17:01:40 GMT  
		Size: 6.4 MB (6371009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ab04e8d365d0e9a64e5c66520b901d3ef4ef1544c78b77ae82f3ad3db34d87`  
		Last Modified: Tue, 17 Aug 2021 17:01:39 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ba9ae244af88f2626bffcd2963ffcae650ba499e91d500bf9f34059a9ddf70`  
		Last Modified: Tue, 17 Aug 2021 17:01:39 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2.16-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:50602b8c10dabe847bbb359b30e4aa80d7b4091d948045aa0f4a49390486c83b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8897553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af081a4d7f70aa6da2a8ace73978df041f5fbb6ccdcca518a8da076d0afccfa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:49:32 GMT
ADD file:7f2c7deda009eabdcbbdccb11e854043d32c498e64e7e1ca02165d7bb4261d39 in / 
# Fri, 06 Aug 2021 17:49:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:15:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:38:20 GMT
ENV HAPROXY_VERSION=2.2.16
# Tue, 17 Aug 2021 16:38:21 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.16.tar.gz
# Tue, 17 Aug 2021 16:38:21 GMT
ENV HAPROXY_SHA256=b81e03a181070d1f7bcdaeec9f09af701fb1ab015c3c9c997a881f4773e29375
# Tue, 17 Aug 2021 16:38:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:38:49 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:38:49 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:38:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:38:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:38:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f465bb3e9fcd0c42f936ecc566c6e40353c00f3089b2b2c2ea1663c30f89d3ab`  
		Last Modified: Fri, 06 Aug 2021 17:51:00 GMT  
		Size: 2.6 MB (2626350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332ccafb58fe1d8ed3d3d5ad9c01adba33d922f28a398285d2eb67fed7c8bee8`  
		Last Modified: Fri, 06 Aug 2021 18:20:57 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4cba68dd4f3bce350901a2cd42e506ace778145f33252c653828174c8565b6`  
		Last Modified: Tue, 17 Aug 2021 16:42:06 GMT  
		Size: 6.3 MB (6269434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e454f1eae153ff572a78e69b8aeaf0def78e5640f460e5b8221a6a6cbcdaa295`  
		Last Modified: Tue, 17 Aug 2021 16:42:03 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397049d890a662fe6f939322ac8ccabc83e4095886c2c784afd5a7e7ae1c86b4`  
		Last Modified: Tue, 17 Aug 2021 16:42:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2.16-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:e19131c9982c9af0b47a25e200095a92ab87ae9f8dca1fe4aed26ae0e90ced54
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9050001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868780f890b28ae16dc54c895cb97d1e4dda0e437e0bfa48442a66b949ef767f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:38:26 GMT
ADD file:bafaec4a54d6cef99b5f3660d074a3d2251e4d4bd09df9ea65f33e9bffb7d88d in / 
# Fri, 06 Aug 2021 17:38:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:19:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:09:43 GMT
ENV HAPROXY_VERSION=2.2.16
# Tue, 17 Aug 2021 17:09:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.16.tar.gz
# Tue, 17 Aug 2021 17:09:43 GMT
ENV HAPROXY_SHA256=b81e03a181070d1f7bcdaeec9f09af701fb1ab015c3c9c997a881f4773e29375
# Tue, 17 Aug 2021 17:10:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 17:10:55 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:10:55 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:10:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 17:10:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:10:56 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:935703e1179e32e201e4a36d5664d58299dc8e7bcac197b70c295c0a59216db1`  
		Last Modified: Fri, 06 Aug 2021 17:39:15 GMT  
		Size: 2.8 MB (2821910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695b2822110160b402b8f359bb19d954a46a6ead94f868feba7d00f5a10e50e`  
		Last Modified: Fri, 06 Aug 2021 19:32:18 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05d77252a068be24ed30adc7a41d564e73ba2c4dc7f792f5c4d7b11473cce07`  
		Last Modified: Tue, 17 Aug 2021 17:17:04 GMT  
		Size: 6.2 MB (6226324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55f27d6215ce8aa788bc4fc340e39ac86fa2207594a0a955709fc7699dca208`  
		Last Modified: Tue, 17 Aug 2021 17:17:02 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb3310368ff204641a1be872c924e2053d4a423898977f83120b7b4e3357d98`  
		Last Modified: Tue, 17 Aug 2021 17:17:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.2.16-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:175bc701c960c871408a5601c110b22be001331f5c504205ca8c08b137e6ff07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9521499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6d32dbb24bbd5e29c43ed7e3e0ce8ba9dd3a010c44bc023182036444134ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:17:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:56:44 GMT
ENV HAPROXY_VERSION=2.2.16
# Tue, 17 Aug 2021 16:56:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.2/src/haproxy-2.2.16.tar.gz
# Tue, 17 Aug 2021 16:56:48 GMT
ENV HAPROXY_SHA256=b81e03a181070d1f7bcdaeec9f09af701fb1ab015c3c9c997a881f4773e29375
# Tue, 17 Aug 2021 16:57:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:57:30 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:57:31 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:57:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:57:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:57:42 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d374dad070e00fdb493e29a3aa64b375dbec801497e01d3b8ddbf7cc967634cb`  
		Last Modified: Fri, 06 Aug 2021 21:27:30 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6860d80855c25358d091d20f18a9c35876c87b1e04a90b034437223d18bde93b`  
		Last Modified: Tue, 17 Aug 2021 17:05:40 GMT  
		Size: 6.7 MB (6708583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be759e2ed68dc74dd6ce0fdf47303c51d6517675bbc73e073a70491c6bfb9c2`  
		Last Modified: Tue, 17 Aug 2021 17:05:39 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1657f0ace1a0107268cecd3945096e7c9f35d07d8bb37def7a8865982f4b6ed`  
		Last Modified: Tue, 17 Aug 2021 17:05:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.3`

```console
$ docker pull haproxy@sha256:cef33a90b6c72bea3a85ade98ccc2f4436694104e8d575186e1fad36c76fb319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.3` - linux; amd64

```console
$ docker pull haproxy@sha256:c1b75498e58c16ab5cba899adf47f05ab48e484fe20c9194c379fa43a979eceb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36742170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d6af8c4b4300247ec846e21974fb1cb5b18a3f25a651de2cc30379d2f0b6b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 10:43:34 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:52:58 GMT
ENV HAPROXY_VERSION=2.3.13
# Tue, 17 Aug 2021 16:52:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.13.tar.gz
# Tue, 17 Aug 2021 16:52:58 GMT
ENV HAPROXY_SHA256=c651a44f1a1158085962ea64852ab163e0d21c5ef0ea4b2c5218728ed4dbe257
# Tue, 17 Aug 2021 16:53:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:53:47 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:53:47 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:53:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:53:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:53:48 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd06683556254cbe06dad4624837c2dcbd2fec67c7fbdd057251f0a207a9315`  
		Last Modified: Tue, 17 Aug 2021 10:53:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f0dad8861f0925e83d6071623211c43a8c8bf7d5aace3564a8c8a6a6f0731b`  
		Last Modified: Tue, 17 Aug 2021 17:01:04 GMT  
		Size: 9.6 MB (9594235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fd973566a052b1666dff339fb6c2a4f776c224284f1f68ac560783fc5c8a0c`  
		Last Modified: Tue, 17 Aug 2021 17:01:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad4723e4f29ad02c79786dc6b1a32e358967d6a66fd6b30da0ea49eed84c343`  
		Last Modified: Tue, 17 Aug 2021 17:01:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:8e114d89e91483ad5c959bb2ca76deb621d98ff73978e97844e0236965d99e09
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34085916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618e12cbcc1f2dde820c5942a0683fd4927a4f0cadf9e57f1964f295e1b12c14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:56:50 GMT
ADD file:f29260935f1f8b3eef5eb0d5e49dd4cf5370e8731a3f4006d6023724bce09601 in / 
# Tue, 17 Aug 2021 01:56:51 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:39:10 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:41:26 GMT
ENV HAPROXY_VERSION=2.3.12
# Tue, 17 Aug 2021 08:41:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.12.tar.gz
# Tue, 17 Aug 2021 08:41:27 GMT
ENV HAPROXY_SHA256=684670d71ffe1ab3f0bfd1be0e55ea9d932732081dd01858b9e351c1a909be3e
# Tue, 17 Aug 2021 08:42:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:42:19 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:42:20 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:42:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 08:42:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:42:22 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3dfab4a5b2accf2d709d8c7d14a42715948ecf2d6da4943a6e2c0de8ae7536a0`  
		Last Modified: Tue, 17 Aug 2021 02:12:42 GMT  
		Size: 24.9 MB (24879063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeabbf4f2af3ef66d78a317a4b3a0704a061a5de2611c57b0bfc47b775c2ed8b`  
		Last Modified: Tue, 17 Aug 2021 08:48:10 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea18ffaca34010c7ed58e5e5e7eaf99a2f1b269e47ea6f857e3651e62f07410`  
		Last Modified: Tue, 17 Aug 2021 08:49:00 GMT  
		Size: 9.2 MB (9204908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d306e81c3997372f98023395abcf6485ceba4b4c6cba6bbc5309d25a3fa022a`  
		Last Modified: Tue, 17 Aug 2021 08:48:54 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf012914debbb9a9184db4bf515729b6e89e35fd5617d7a62294ec14504a83ea`  
		Last Modified: Tue, 17 Aug 2021 08:48:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:8ad58e8e0398aaa2012896906cb7026a11ee4e369be290b112b35755b05d19c7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31814383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9049399a09f61c6bce8749cfbf2e6809c467544d3da631270a5175b73540761a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 02:14:25 GMT
ADD file:ca8cc4b509e305fa07662fbf2234ed78f0056569f6ca047305dc02bcd60f1558 in / 
# Tue, 17 Aug 2021 02:14:26 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 16:10:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:13:07 GMT
ENV HAPROXY_VERSION=2.3.12
# Tue, 17 Aug 2021 16:13:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.12.tar.gz
# Tue, 17 Aug 2021 16:13:08 GMT
ENV HAPROXY_SHA256=684670d71ffe1ab3f0bfd1be0e55ea9d932732081dd01858b9e351c1a909be3e
# Tue, 17 Aug 2021 16:13:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:13:55 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:13:55 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:13:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:13:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:13:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:13e3f03410ff211945a725435c13065288d48a8cb740f0530e7588012c2679a4`  
		Last Modified: Tue, 17 Aug 2021 02:30:58 GMT  
		Size: 22.7 MB (22746254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb366ce7907325b732435009125848fb9596a1afdb0f87a8703cdf4342e91a4e`  
		Last Modified: Tue, 17 Aug 2021 16:21:35 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd29312f48a9d79f7701244bd74881cee76cb3c477f2a7b69056f859c55fd84`  
		Last Modified: Tue, 17 Aug 2021 16:22:34 GMT  
		Size: 9.1 MB (9066182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3bae1251e580176f453ca1ff63bde3ad37862b7f8e18e4701b1b1588670e44`  
		Last Modified: Tue, 17 Aug 2021 16:22:29 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b9eda9ef40af960ea02bdd1518a08291c73edb923a9879474d279f09c5e066`  
		Last Modified: Tue, 17 Aug 2021 16:22:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:9feec693b880e7383b592454eb049c0f302e0e29234a19f3eb0b6f6d5f857e6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35397178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150f975e2d61b76252986445da8a1220335145e164f4533e18c64ad5b7290a15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:12:02 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:13:55 GMT
ENV HAPROXY_VERSION=2.3.12
# Tue, 17 Aug 2021 08:13:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.12.tar.gz
# Tue, 17 Aug 2021 08:13:55 GMT
ENV HAPROXY_SHA256=684670d71ffe1ab3f0bfd1be0e55ea9d932732081dd01858b9e351c1a909be3e
# Tue, 17 Aug 2021 08:14:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:14:38 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:14:38 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:14:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 08:14:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:14:39 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc63cf29191f59ddbc41452b9edbe5f8145c4370cd74d3981d50a862173029b`  
		Last Modified: Tue, 17 Aug 2021 08:19:14 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b742b3efa4397fb2a5ce3d1829a5b47197062d58fb7190ebb6d76f19e409f090`  
		Last Modified: Tue, 17 Aug 2021 08:19:51 GMT  
		Size: 9.5 MB (9480158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e325ec10aaa39800881321a941fe3ecb39b26c02128c70eaf8d5e369c9549545`  
		Last Modified: Tue, 17 Aug 2021 08:19:49 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1ba9f01ad73ef4ce0f65a933311310cf2f745fd4833eb65d7c593fef40184e`  
		Last Modified: Tue, 17 Aug 2021 08:19:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3` - linux; 386

```console
$ docker pull haproxy@sha256:4a04f9553522bccbee19a4a68a759a43dc7bf8d43970296a048c4de66f1c9a63
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37255666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1ebb79506f29a0319871c7cd063f86b3a7607a41fb8d15cfdd5c4b01575813`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:41:16 GMT
ADD file:0418032b55cd0a6dd515ac277fb9f92354397503cab212d446d3a3d8c647a60f in / 
# Tue, 17 Aug 2021 01:41:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 12:14:55 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:06:15 GMT
ENV HAPROXY_VERSION=2.3.13
# Tue, 17 Aug 2021 17:06:15 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.13.tar.gz
# Tue, 17 Aug 2021 17:06:16 GMT
ENV HAPROXY_SHA256=c651a44f1a1158085962ea64852ab163e0d21c5ef0ea4b2c5218728ed4dbe257
# Tue, 17 Aug 2021 17:07:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 17:07:09 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:07:09 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:07:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 17:07:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:07:11 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c1c94e1f2523d69effaa463d64fc9962cfc67e2a956f0476c94200e7cf19edf0`  
		Last Modified: Tue, 17 Aug 2021 01:50:57 GMT  
		Size: 27.8 MB (27797627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f804b7c921abcc2fb2904ad2092beefd0224c9bd4cb1cf6477727e6f2bbd7599`  
		Last Modified: Tue, 17 Aug 2021 12:26:22 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0922d477c6ffb741267b29774f481c304959ee41b9306649a822ad163c31eb79`  
		Last Modified: Tue, 17 Aug 2021 17:16:24 GMT  
		Size: 9.5 MB (9456096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97716a71f2da6065c1fa6f0f63210548327a1d0e187ba62409b5be31224dda68`  
		Last Modified: Tue, 17 Aug 2021 17:16:22 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcde26b543976d669aeb15a63facf31e99a60bfb7b1b90bf3b283883d1a048c5`  
		Last Modified: Tue, 17 Aug 2021 17:16:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3` - linux; mips64le

```console
$ docker pull haproxy@sha256:7734dabeacba20dab6c04d8fb24ee3b118a5641e33e6c413539bbf46ad0550ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (34984786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc42ebff3a8c863553c8be88fecf5a2c4339cb727e57b68504633f449bf3cde7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:12:26 GMT
ADD file:8bd279803ead4ddce8db90b65e89c423f84fbf6042bfbeae8c09486b2e884cde in / 
# Tue, 17 Aug 2021 01:12:27 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:10:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 14:15:57 GMT
ENV HAPROXY_VERSION=2.3.12
# Tue, 17 Aug 2021 14:15:57 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.12.tar.gz
# Tue, 17 Aug 2021 14:15:58 GMT
ENV HAPROXY_SHA256=684670d71ffe1ab3f0bfd1be0e55ea9d932732081dd01858b9e351c1a909be3e
# Tue, 17 Aug 2021 14:18:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 14:18:17 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 14:18:17 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 14:18:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 14:18:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:18:20 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a711e3e37b88ef77496c07ed663bb4270ecba9057eba452a91cc9be0bafb9c32`  
		Last Modified: Tue, 17 Aug 2021 01:21:44 GMT  
		Size: 25.8 MB (25813007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac33edc8b81dffec584b1a7ca6a8abea967f70259323fc62ff423b9c01642e`  
		Last Modified: Tue, 17 Aug 2021 14:27:23 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e535f06885d454bcafd3cf76edb05a38d5f14fb5cfa874119319cc8701ffb3d0`  
		Last Modified: Tue, 17 Aug 2021 14:28:09 GMT  
		Size: 9.2 MB (9169830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b593e988a8002e225969bfa7ced796f33d9ed923559547acd20828a41db8fcdd`  
		Last Modified: Tue, 17 Aug 2021 14:28:02 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a06067368b3afc3e61aa7e4709662a4cd30d00979f51a68446341c747e3cffb`  
		Last Modified: Tue, 17 Aug 2021 14:28:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3` - linux; ppc64le

```console
$ docker pull haproxy@sha256:d28865908cd6b88ff6858cdab7ac86f1fddeea1477bc4b81ef894a2b10cc71f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40639782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722c4fe866b20411777a8dc9ee85df0474162264bf76d40d0ad1e3e7c0b95f54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:34:13 GMT
ADD file:8b9b12a994a2519f725d1ed1f4ab5a444665262678fd8e6c42cf78f32dacb7fa in / 
# Tue, 17 Aug 2021 01:34:20 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 13:36:19 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:49:17 GMT
ENV HAPROXY_VERSION=2.3.13
# Tue, 17 Aug 2021 16:49:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.13.tar.gz
# Tue, 17 Aug 2021 16:49:24 GMT
ENV HAPROXY_SHA256=c651a44f1a1158085962ea64852ab163e0d21c5ef0ea4b2c5218728ed4dbe257
# Tue, 17 Aug 2021 16:51:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:52:00 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:52:02 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:52:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:52:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:52:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c3e09f0e3e7f6fcb741a4c9214b63e341e1d9b53d7689a5ad6ff640b61a82541`  
		Last Modified: Tue, 17 Aug 2021 01:48:22 GMT  
		Size: 30.6 MB (30553721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb7833dc31cf72935b478f7bf90e34f0f2a22d8260da177e4648ac973af1f9c`  
		Last Modified: Tue, 17 Aug 2021 14:24:41 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03196f253f2f647dfbfbf2602b60a6aa351008e244898d17d53f05a2b58a9e5c`  
		Last Modified: Tue, 17 Aug 2021 17:04:58 GMT  
		Size: 10.1 MB (10084097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993d83bd5f30c14b937b5efd15fd92c3b2f06efbf56df3e2dec16b8f29d7e731`  
		Last Modified: Tue, 17 Aug 2021 17:04:56 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4ab460ff1c6573147c7d276ac4ff88efe5fab6e33a56d121049c1658a7fdbc`  
		Last Modified: Tue, 17 Aug 2021 17:04:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3` - linux; s390x

```console
$ docker pull haproxy@sha256:9b680124c569f6f0bdf53a85619cc87b1d8a80d56534b2bc666935bcdf8c6439
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35091314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6ccea5ff1c07c6bf27c7f96ca15723b8e23f55afc5f923c57b567cadd41cb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 07:18:12 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 07:21:12 GMT
ENV HAPROXY_VERSION=2.3.12
# Tue, 17 Aug 2021 07:21:12 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.12.tar.gz
# Tue, 17 Aug 2021 07:21:12 GMT
ENV HAPROXY_SHA256=684670d71ffe1ab3f0bfd1be0e55ea9d932732081dd01858b9e351c1a909be3e
# Tue, 17 Aug 2021 07:21:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 07:21:55 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 07:21:55 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 07:21:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 07:21:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 07:21:57 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16a2f2a1452470a1d818d8d16934d08d2a57b312ceabcce8c1cfad6c99f00a2`  
		Last Modified: Tue, 17 Aug 2021 07:28:00 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e2da2d01a213aab879b81b23ccaa3e1d018f572b33e2f38b7f97e50a88627d`  
		Last Modified: Tue, 17 Aug 2021 07:28:25 GMT  
		Size: 9.3 MB (9328508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf9241220d8143820449ca100f541883d66bf279825da36fe20ce7e7fcae987`  
		Last Modified: Tue, 17 Aug 2021 07:28:24 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63a37aba5185b35337ddd522ceaf2984e1582c2ceae091a19c9c76a6725a179`  
		Last Modified: Tue, 17 Aug 2021 07:28:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.3-alpine`

```console
$ docker pull haproxy@sha256:324255077581c10bbd600c440a98c39d2878d12e2f7bac3223e5724da52ab376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.3-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:b17faf3c22f84ca23d8a5232c8ab3ceaf37aa84ed1e4e8c7af4d9ddb77dcb9b2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9505158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e52bb877a244d9b450c5991577d2280f87a0464b993d70bc176f181d78b04a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:43:18 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:53:58 GMT
ENV HAPROXY_VERSION=2.3.13
# Tue, 17 Aug 2021 16:53:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.13.tar.gz
# Tue, 17 Aug 2021 16:53:58 GMT
ENV HAPROXY_SHA256=c651a44f1a1158085962ea64852ab163e0d21c5ef0ea4b2c5218728ed4dbe257
# Tue, 17 Aug 2021 16:54:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:54:56 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:54:56 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:54:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:54:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:54:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22138861da3ab6ae8583cf62942545e1bb75874501f4a8d45d13a38c848a908`  
		Last Modified: Fri, 06 Aug 2021 19:51:27 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5c7c5b2307537ce7640e591232c10089d63cf8f9b161b8c94c7b1309c42ef3`  
		Last Modified: Tue, 17 Aug 2021 17:01:16 GMT  
		Size: 6.7 MB (6690384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6de148c203e31708d6804c0bae85a0138413403e172b6d451e8a7906189776`  
		Last Modified: Tue, 17 Aug 2021 17:01:15 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa05b194879226f7ef7183040f2297e7c4614a85b9cdbf3857312e9f354a61af`  
		Last Modified: Tue, 17 Aug 2021 17:01:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:a195ed35c7bb9b11eb7c0b4d29e8ef87cf24b28d978d8c611a6287ded303e07d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9241692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca9eb2eb0914a313120eb8211fba1ec40385e723a7154b88786f6f1dc067319`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:49:32 GMT
ADD file:7f2c7deda009eabdcbbdccb11e854043d32c498e64e7e1ca02165d7bb4261d39 in / 
# Fri, 06 Aug 2021 17:49:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:15:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:37:39 GMT
ENV HAPROXY_VERSION=2.3.13
# Tue, 17 Aug 2021 16:37:39 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.13.tar.gz
# Tue, 17 Aug 2021 16:37:39 GMT
ENV HAPROXY_SHA256=c651a44f1a1158085962ea64852ab163e0d21c5ef0ea4b2c5218728ed4dbe257
# Tue, 17 Aug 2021 16:38:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:38:06 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:38:06 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:38:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:38:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:38:09 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f465bb3e9fcd0c42f936ecc566c6e40353c00f3089b2b2c2ea1663c30f89d3ab`  
		Last Modified: Fri, 06 Aug 2021 17:51:00 GMT  
		Size: 2.6 MB (2626350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332ccafb58fe1d8ed3d3d5ad9c01adba33d922f28a398285d2eb67fed7c8bee8`  
		Last Modified: Fri, 06 Aug 2021 18:20:57 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8ac30455a624da8fe662e7d0ca76afbf5ca7b46943986fb0924cf2df1e583b`  
		Last Modified: Tue, 17 Aug 2021 16:41:50 GMT  
		Size: 6.6 MB (6613577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b420d0d6686c3ff92e66f88a2ebd243d78b13983cb34753b2d9d67fdc03ac602`  
		Last Modified: Tue, 17 Aug 2021 16:41:46 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1838943ad5638afa907831759ea9453d6b4858bc6391b9820eab40ed846d54`  
		Last Modified: Tue, 17 Aug 2021 16:41:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:ae28316c38a33fd6cc78ba193e3804fcbe92f68f93509d749ff540cb909bd39d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8940621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1a0ccc35f1d40e3299ae67be76705bc80b34a2d21d3fc7b7a55734197f7179`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:57:32 GMT
ADD file:3a35ff3ac0d80289d419a4d6d8319610c38e1936d296addafb9aaf506946230f in / 
# Fri, 06 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:54:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 19:56:37 GMT
ENV HAPROXY_VERSION=2.3.12
# Fri, 06 Aug 2021 19:56:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.12.tar.gz
# Fri, 06 Aug 2021 19:56:38 GMT
ENV HAPROXY_SHA256=684670d71ffe1ab3f0bfd1be0e55ea9d932732081dd01858b9e351c1a909be3e
# Fri, 06 Aug 2021 19:57:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 19:57:18 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 19:57:19 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 19:57:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 19:57:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 19:57:25 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4ee0caa23b369b04827640a4be298bf4ff7bacd030c77e915f5d7fb8f987594a`  
		Last Modified: Fri, 06 Aug 2021 17:58:57 GMT  
		Size: 2.4 MB (2429359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548ff9918828f96cb9a5e5656ea589d79e6fb1d7b9f0d693feff2dbefc6929fe`  
		Last Modified: Fri, 06 Aug 2021 20:02:54 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b447ed4b6db89c115a92e95692d84e81a8d4b6ad7784042a0a8c053b9649a5`  
		Last Modified: Fri, 06 Aug 2021 20:03:44 GMT  
		Size: 6.5 MB (6509495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fded175e1d5b5d545a267ffd089ffaaccb367bc5a8ad5fd3e4a8e8b9109375`  
		Last Modified: Fri, 06 Aug 2021 20:03:42 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcc70659725c00764b6a44a78f0c58b38817b02c057e5a0b6dc7d910d1b004a`  
		Last Modified: Fri, 06 Aug 2021 20:03:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:d2914783d6c5f76a6a9419a505fabf213890c53ebaded5e758542e47f20da936
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9424894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d0717cc841646466a08f701cdc279656c81e79806d0bd5589ff666cd549d45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:39:26 GMT
ADD file:1a8fd1066485e1261462e689c1a072f010c1d3be904b73ef2b84128fac652951 in / 
# Fri, 06 Aug 2021 17:39:27 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:38:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 18:41:23 GMT
ENV HAPROXY_VERSION=2.3.12
# Fri, 06 Aug 2021 18:41:23 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.12.tar.gz
# Fri, 06 Aug 2021 18:41:23 GMT
ENV HAPROXY_SHA256=684670d71ffe1ab3f0bfd1be0e55ea9d932732081dd01858b9e351c1a909be3e
# Fri, 06 Aug 2021 18:42:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 18:42:08 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 18:42:08 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 18:42:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 18:42:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 18:42:09 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fd3acdcea5682abced546ec19fb6ebee725c5184e5d91614c469c0a79e67f2d0`  
		Last Modified: Fri, 06 Aug 2021 17:40:12 GMT  
		Size: 2.7 MB (2710613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a23793c1bba0796c0f469305ee92dd0f1cb8299963e4da4249d0f5aa2fcea0`  
		Last Modified: Fri, 06 Aug 2021 18:46:06 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7770287949306d5888f0619cb57da2e59d0be604df63a20223e77eca0a15fd1d`  
		Last Modified: Fri, 06 Aug 2021 18:46:44 GMT  
		Size: 6.7 MB (6712514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a6eda265667f4478a9c4f4b14ecfc0f3b8d395761719cc6633a5df960fb718`  
		Last Modified: Fri, 06 Aug 2021 18:46:43 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ad4e8f87ba9dea048491ace1fbcff03f10bc70fd2e5dd83be5e632c6f8cd10`  
		Last Modified: Fri, 06 Aug 2021 18:46:43 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:43ad92ddfc6495af382a83862c8d393fdcf1695b8e7e03fdc5002c6e23b81697
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9381238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794cf6c103d0d8a670350855b510dece6493f5e20960327725feaf73563e9cbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:38:26 GMT
ADD file:bafaec4a54d6cef99b5f3660d074a3d2251e4d4bd09df9ea65f33e9bffb7d88d in / 
# Fri, 06 Aug 2021 17:38:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:19:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:07:16 GMT
ENV HAPROXY_VERSION=2.3.13
# Tue, 17 Aug 2021 17:07:17 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.13.tar.gz
# Tue, 17 Aug 2021 17:07:17 GMT
ENV HAPROXY_SHA256=c651a44f1a1158085962ea64852ab163e0d21c5ef0ea4b2c5218728ed4dbe257
# Tue, 17 Aug 2021 17:08:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 17:08:22 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:08:23 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:08:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 17:08:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:08:24 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:935703e1179e32e201e4a36d5664d58299dc8e7bcac197b70c295c0a59216db1`  
		Last Modified: Fri, 06 Aug 2021 17:39:15 GMT  
		Size: 2.8 MB (2821910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695b2822110160b402b8f359bb19d954a46a6ead94f868feba7d00f5a10e50e`  
		Last Modified: Fri, 06 Aug 2021 19:32:18 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dab220ab47be5663a1ec734e0d157b9fc7ba37441e0b52b6d4d3959c7faeb6c`  
		Last Modified: Tue, 17 Aug 2021 17:16:37 GMT  
		Size: 6.6 MB (6557566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140390af18ca7d66906544e27ecde891d2b1bce059896c62c3333d2e6760678e`  
		Last Modified: Tue, 17 Aug 2021 17:16:36 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac25d796e496d79382a39358f8dbaf85a4dcfd66a114e901d7c7c77f82305b6`  
		Last Modified: Tue, 17 Aug 2021 17:16:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:adf81920677fbfe6068c49a34232b6b007561721bf61a3616277559a8942a4a3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9861170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5d2df7629c3e699ce3bf058fca99af93d97700d1a043bb01cec03c6371c920`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:17:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:52:29 GMT
ENV HAPROXY_VERSION=2.3.13
# Tue, 17 Aug 2021 16:52:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.13.tar.gz
# Tue, 17 Aug 2021 16:52:33 GMT
ENV HAPROXY_SHA256=c651a44f1a1158085962ea64852ab163e0d21c5ef0ea4b2c5218728ed4dbe257
# Tue, 17 Aug 2021 16:53:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:53:10 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:53:11 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:53:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:53:22 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d374dad070e00fdb493e29a3aa64b375dbec801497e01d3b8ddbf7cc967634cb`  
		Last Modified: Fri, 06 Aug 2021 21:27:30 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5809a11beb3b89bebdc0ff21560fb63ff7de9c90ef0bd65732d73733a8bdbe9a`  
		Last Modified: Tue, 17 Aug 2021 17:05:12 GMT  
		Size: 7.0 MB (7048254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd11b5af8340104180120ae6d8bb136d5297921f01e83192a0a6b963857ac5d`  
		Last Modified: Tue, 17 Aug 2021 17:05:10 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c371d7b728611836ae93960b47ebabf659defd3407eac3d6e24ab64a9bae73`  
		Last Modified: Tue, 17 Aug 2021 17:05:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:d8002e556915178004debf14488aa6b7e820edbbc4e51471336ba90925a46971
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9259665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35ad497512239f4a077e815769908cf9d12f272fb7d41abae65c31d78fd5e02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:54:24 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 23 Apr 2021 20:43:09 GMT
ENV HAPROXY_VERSION=2.3.10
# Fri, 23 Apr 2021 20:43:10 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.10.tar.gz
# Fri, 23 Apr 2021 20:43:11 GMT
ENV HAPROXY_SHA256=9946e0cfc83f29072b3431e37246221cf9d4a9d28a158c075714d345266f4f35
# Fri, 23 Apr 2021 20:43:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 23 Apr 2021 20:43:58 GMT
STOPSIGNAL SIGUSR1
# Fri, 23 Apr 2021 20:43:58 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 23 Apr 2021 20:43:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 23 Apr 2021 20:43:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Apr 2021 20:43:59 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267275aba58470c82626189a59be76cd169bd245568e2f2545ed1ee64ff8a8ff`  
		Last Modified: Wed, 14 Apr 2021 20:59:06 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aac9cf42616b874dc26fc410c1d0b7ddd5b5acdc32829cab01df78d6a831e01`  
		Last Modified: Fri, 23 Apr 2021 20:45:18 GMT  
		Size: 6.7 MB (6655259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13309a7e4b19e568f7683f6a8dbc48ce6d73e5f6e8ee693c8bd979a4a5774956`  
		Last Modified: Fri, 23 Apr 2021 20:45:17 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59770393e0a5b1867600ef163090de4e39b9733dcaea56ae6d84ebce64f759f`  
		Last Modified: Fri, 23 Apr 2021 20:45:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.3.13`

```console
$ docker pull haproxy@sha256:0ad9fd7dfc484db5218085ced6fc4449144b6b65f9714a4ba0d27a39eebbeb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le

### `haproxy:2.3.13` - linux; amd64

```console
$ docker pull haproxy@sha256:c1b75498e58c16ab5cba899adf47f05ab48e484fe20c9194c379fa43a979eceb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36742170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d6af8c4b4300247ec846e21974fb1cb5b18a3f25a651de2cc30379d2f0b6b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 10:43:34 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:52:58 GMT
ENV HAPROXY_VERSION=2.3.13
# Tue, 17 Aug 2021 16:52:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.13.tar.gz
# Tue, 17 Aug 2021 16:52:58 GMT
ENV HAPROXY_SHA256=c651a44f1a1158085962ea64852ab163e0d21c5ef0ea4b2c5218728ed4dbe257
# Tue, 17 Aug 2021 16:53:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:53:47 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:53:47 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:53:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:53:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:53:48 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd06683556254cbe06dad4624837c2dcbd2fec67c7fbdd057251f0a207a9315`  
		Last Modified: Tue, 17 Aug 2021 10:53:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f0dad8861f0925e83d6071623211c43a8c8bf7d5aace3564a8c8a6a6f0731b`  
		Last Modified: Tue, 17 Aug 2021 17:01:04 GMT  
		Size: 9.6 MB (9594235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fd973566a052b1666dff339fb6c2a4f776c224284f1f68ac560783fc5c8a0c`  
		Last Modified: Tue, 17 Aug 2021 17:01:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad4723e4f29ad02c79786dc6b1a32e358967d6a66fd6b30da0ea49eed84c343`  
		Last Modified: Tue, 17 Aug 2021 17:01:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3.13` - linux; 386

```console
$ docker pull haproxy@sha256:4a04f9553522bccbee19a4a68a759a43dc7bf8d43970296a048c4de66f1c9a63
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37255666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1ebb79506f29a0319871c7cd063f86b3a7607a41fb8d15cfdd5c4b01575813`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:41:16 GMT
ADD file:0418032b55cd0a6dd515ac277fb9f92354397503cab212d446d3a3d8c647a60f in / 
# Tue, 17 Aug 2021 01:41:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 12:14:55 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:06:15 GMT
ENV HAPROXY_VERSION=2.3.13
# Tue, 17 Aug 2021 17:06:15 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.13.tar.gz
# Tue, 17 Aug 2021 17:06:16 GMT
ENV HAPROXY_SHA256=c651a44f1a1158085962ea64852ab163e0d21c5ef0ea4b2c5218728ed4dbe257
# Tue, 17 Aug 2021 17:07:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 17:07:09 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:07:09 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:07:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 17:07:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:07:11 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c1c94e1f2523d69effaa463d64fc9962cfc67e2a956f0476c94200e7cf19edf0`  
		Last Modified: Tue, 17 Aug 2021 01:50:57 GMT  
		Size: 27.8 MB (27797627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f804b7c921abcc2fb2904ad2092beefd0224c9bd4cb1cf6477727e6f2bbd7599`  
		Last Modified: Tue, 17 Aug 2021 12:26:22 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0922d477c6ffb741267b29774f481c304959ee41b9306649a822ad163c31eb79`  
		Last Modified: Tue, 17 Aug 2021 17:16:24 GMT  
		Size: 9.5 MB (9456096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97716a71f2da6065c1fa6f0f63210548327a1d0e187ba62409b5be31224dda68`  
		Last Modified: Tue, 17 Aug 2021 17:16:22 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcde26b543976d669aeb15a63facf31e99a60bfb7b1b90bf3b283883d1a048c5`  
		Last Modified: Tue, 17 Aug 2021 17:16:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3.13` - linux; ppc64le

```console
$ docker pull haproxy@sha256:d28865908cd6b88ff6858cdab7ac86f1fddeea1477bc4b81ef894a2b10cc71f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40639782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722c4fe866b20411777a8dc9ee85df0474162264bf76d40d0ad1e3e7c0b95f54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:34:13 GMT
ADD file:8b9b12a994a2519f725d1ed1f4ab5a444665262678fd8e6c42cf78f32dacb7fa in / 
# Tue, 17 Aug 2021 01:34:20 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 13:36:19 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:49:17 GMT
ENV HAPROXY_VERSION=2.3.13
# Tue, 17 Aug 2021 16:49:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.13.tar.gz
# Tue, 17 Aug 2021 16:49:24 GMT
ENV HAPROXY_SHA256=c651a44f1a1158085962ea64852ab163e0d21c5ef0ea4b2c5218728ed4dbe257
# Tue, 17 Aug 2021 16:51:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:52:00 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:52:02 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:52:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:52:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:52:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c3e09f0e3e7f6fcb741a4c9214b63e341e1d9b53d7689a5ad6ff640b61a82541`  
		Last Modified: Tue, 17 Aug 2021 01:48:22 GMT  
		Size: 30.6 MB (30553721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb7833dc31cf72935b478f7bf90e34f0f2a22d8260da177e4648ac973af1f9c`  
		Last Modified: Tue, 17 Aug 2021 14:24:41 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03196f253f2f647dfbfbf2602b60a6aa351008e244898d17d53f05a2b58a9e5c`  
		Last Modified: Tue, 17 Aug 2021 17:04:58 GMT  
		Size: 10.1 MB (10084097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993d83bd5f30c14b937b5efd15fd92c3b2f06efbf56df3e2dec16b8f29d7e731`  
		Last Modified: Tue, 17 Aug 2021 17:04:56 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4ab460ff1c6573147c7d276ac4ff88efe5fab6e33a56d121049c1658a7fdbc`  
		Last Modified: Tue, 17 Aug 2021 17:04:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.3.13-alpine`

```console
$ docker pull haproxy@sha256:b563136f71424c512d13dd54036c7dfb72d8995514297d700b58137cbbdaa59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; 386
	-	linux; ppc64le

### `haproxy:2.3.13-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:b17faf3c22f84ca23d8a5232c8ab3ceaf37aa84ed1e4e8c7af4d9ddb77dcb9b2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9505158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e52bb877a244d9b450c5991577d2280f87a0464b993d70bc176f181d78b04a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:43:18 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:53:58 GMT
ENV HAPROXY_VERSION=2.3.13
# Tue, 17 Aug 2021 16:53:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.13.tar.gz
# Tue, 17 Aug 2021 16:53:58 GMT
ENV HAPROXY_SHA256=c651a44f1a1158085962ea64852ab163e0d21c5ef0ea4b2c5218728ed4dbe257
# Tue, 17 Aug 2021 16:54:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:54:56 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:54:56 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:54:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:54:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:54:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22138861da3ab6ae8583cf62942545e1bb75874501f4a8d45d13a38c848a908`  
		Last Modified: Fri, 06 Aug 2021 19:51:27 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5c7c5b2307537ce7640e591232c10089d63cf8f9b161b8c94c7b1309c42ef3`  
		Last Modified: Tue, 17 Aug 2021 17:01:16 GMT  
		Size: 6.7 MB (6690384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6de148c203e31708d6804c0bae85a0138413403e172b6d451e8a7906189776`  
		Last Modified: Tue, 17 Aug 2021 17:01:15 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa05b194879226f7ef7183040f2297e7c4614a85b9cdbf3857312e9f354a61af`  
		Last Modified: Tue, 17 Aug 2021 17:01:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3.13-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:a195ed35c7bb9b11eb7c0b4d29e8ef87cf24b28d978d8c611a6287ded303e07d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9241692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca9eb2eb0914a313120eb8211fba1ec40385e723a7154b88786f6f1dc067319`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:49:32 GMT
ADD file:7f2c7deda009eabdcbbdccb11e854043d32c498e64e7e1ca02165d7bb4261d39 in / 
# Fri, 06 Aug 2021 17:49:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:15:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:37:39 GMT
ENV HAPROXY_VERSION=2.3.13
# Tue, 17 Aug 2021 16:37:39 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.13.tar.gz
# Tue, 17 Aug 2021 16:37:39 GMT
ENV HAPROXY_SHA256=c651a44f1a1158085962ea64852ab163e0d21c5ef0ea4b2c5218728ed4dbe257
# Tue, 17 Aug 2021 16:38:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:38:06 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:38:06 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:38:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:38:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:38:09 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f465bb3e9fcd0c42f936ecc566c6e40353c00f3089b2b2c2ea1663c30f89d3ab`  
		Last Modified: Fri, 06 Aug 2021 17:51:00 GMT  
		Size: 2.6 MB (2626350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332ccafb58fe1d8ed3d3d5ad9c01adba33d922f28a398285d2eb67fed7c8bee8`  
		Last Modified: Fri, 06 Aug 2021 18:20:57 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8ac30455a624da8fe662e7d0ca76afbf5ca7b46943986fb0924cf2df1e583b`  
		Last Modified: Tue, 17 Aug 2021 16:41:50 GMT  
		Size: 6.6 MB (6613577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b420d0d6686c3ff92e66f88a2ebd243d78b13983cb34753b2d9d67fdc03ac602`  
		Last Modified: Tue, 17 Aug 2021 16:41:46 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1838943ad5638afa907831759ea9453d6b4858bc6391b9820eab40ed846d54`  
		Last Modified: Tue, 17 Aug 2021 16:41:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3.13-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:43ad92ddfc6495af382a83862c8d393fdcf1695b8e7e03fdc5002c6e23b81697
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9381238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794cf6c103d0d8a670350855b510dece6493f5e20960327725feaf73563e9cbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:38:26 GMT
ADD file:bafaec4a54d6cef99b5f3660d074a3d2251e4d4bd09df9ea65f33e9bffb7d88d in / 
# Fri, 06 Aug 2021 17:38:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:19:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:07:16 GMT
ENV HAPROXY_VERSION=2.3.13
# Tue, 17 Aug 2021 17:07:17 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.13.tar.gz
# Tue, 17 Aug 2021 17:07:17 GMT
ENV HAPROXY_SHA256=c651a44f1a1158085962ea64852ab163e0d21c5ef0ea4b2c5218728ed4dbe257
# Tue, 17 Aug 2021 17:08:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 17:08:22 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:08:23 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:08:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 17:08:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:08:24 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:935703e1179e32e201e4a36d5664d58299dc8e7bcac197b70c295c0a59216db1`  
		Last Modified: Fri, 06 Aug 2021 17:39:15 GMT  
		Size: 2.8 MB (2821910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695b2822110160b402b8f359bb19d954a46a6ead94f868feba7d00f5a10e50e`  
		Last Modified: Fri, 06 Aug 2021 19:32:18 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dab220ab47be5663a1ec734e0d157b9fc7ba37441e0b52b6d4d3959c7faeb6c`  
		Last Modified: Tue, 17 Aug 2021 17:16:37 GMT  
		Size: 6.6 MB (6557566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140390af18ca7d66906544e27ecde891d2b1bce059896c62c3333d2e6760678e`  
		Last Modified: Tue, 17 Aug 2021 17:16:36 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac25d796e496d79382a39358f8dbaf85a4dcfd66a114e901d7c7c77f82305b6`  
		Last Modified: Tue, 17 Aug 2021 17:16:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.3.13-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:adf81920677fbfe6068c49a34232b6b007561721bf61a3616277559a8942a4a3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9861170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5d2df7629c3e699ce3bf058fca99af93d97700d1a043bb01cec03c6371c920`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:17:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:52:29 GMT
ENV HAPROXY_VERSION=2.3.13
# Tue, 17 Aug 2021 16:52:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.13.tar.gz
# Tue, 17 Aug 2021 16:52:33 GMT
ENV HAPROXY_SHA256=c651a44f1a1158085962ea64852ab163e0d21c5ef0ea4b2c5218728ed4dbe257
# Tue, 17 Aug 2021 16:53:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 		zlib-dev 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:53:10 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:53:11 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:53:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 16:53:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:53:22 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d374dad070e00fdb493e29a3aa64b375dbec801497e01d3b8ddbf7cc967634cb`  
		Last Modified: Fri, 06 Aug 2021 21:27:30 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5809a11beb3b89bebdc0ff21560fb63ff7de9c90ef0bd65732d73733a8bdbe9a`  
		Last Modified: Tue, 17 Aug 2021 17:05:12 GMT  
		Size: 7.0 MB (7048254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd11b5af8340104180120ae6d8bb136d5297921f01e83192a0a6b963857ac5d`  
		Last Modified: Tue, 17 Aug 2021 17:05:10 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c371d7b728611836ae93960b47ebabf659defd3407eac3d6e24ab64a9bae73`  
		Last Modified: Tue, 17 Aug 2021 17:05:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.4`

```console
$ docker pull haproxy@sha256:cecd35804d56a8a939975969fbc3ee9c37c193e083d8cc8ee4daeb1817685fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.4` - linux; amd64

```console
$ docker pull haproxy@sha256:be84aa6aa3e60de3ce38adeac6e6d0e01c428e0c02b0a0e7b6d1b42d0bf36a29
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37304052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06340012d09399fd0be90a29f16bc2b8041b9322e9095c6fceeed1aa2f6280cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 10:43:34 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:50:46 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 16:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 16:50:47 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 16:51:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:51:38 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:51:38 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:51:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:51:38 GMT
USER haproxy
# Tue, 17 Aug 2021 16:51:39 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd06683556254cbe06dad4624837c2dcbd2fec67c7fbdd057251f0a207a9315`  
		Last Modified: Tue, 17 Aug 2021 10:53:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341a1a625c8fa0015a85b943c2bc17495fb26b105d5b07b3911a65b0967ea4be`  
		Last Modified: Tue, 17 Aug 2021 17:00:29 GMT  
		Size: 10.2 MB (10156239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63116b577243ee3d88e09a144ffe2122ebb8f78d3ce8b3517e1d39116a9c876a`  
		Last Modified: Tue, 17 Aug 2021 17:00:27 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:97e3c0ac88ed687f305efc5594b62d705816eacfc4f020dc227b7fd597eaea97
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34665658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806dea6cff7a221452cd5f560e5d1868285d8bad11828f9829aaae3321769004`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:56:50 GMT
ADD file:f29260935f1f8b3eef5eb0d5e49dd4cf5370e8731a3f4006d6023724bce09601 in / 
# Tue, 17 Aug 2021 01:56:51 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:39:10 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:40:18 GMT
ENV HAPROXY_VERSION=2.4.2
# Tue, 17 Aug 2021 08:40:18 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Tue, 17 Aug 2021 08:40:18 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Tue, 17 Aug 2021 08:41:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:41:11 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:41:11 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:41:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:41:12 GMT
USER haproxy
# Tue, 17 Aug 2021 08:41:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3dfab4a5b2accf2d709d8c7d14a42715948ecf2d6da4943a6e2c0de8ae7536a0`  
		Last Modified: Tue, 17 Aug 2021 02:12:42 GMT  
		Size: 24.9 MB (24879063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeabbf4f2af3ef66d78a317a4b3a0704a061a5de2611c57b0bfc47b775c2ed8b`  
		Last Modified: Tue, 17 Aug 2021 08:48:10 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9334963a75defcb3be49971cfc877b033ec3d2bf1de44e045c275c0d073eaca`  
		Last Modified: Tue, 17 Aug 2021 08:48:34 GMT  
		Size: 9.8 MB (9784770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddb2411e6120b22278ec6af6dffa64c6a09ed8003d944d6cb75617adb49bb2b`  
		Last Modified: Tue, 17 Aug 2021 08:48:28 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:b6f52164624551033e34146068b12ad46dc5f50521597edf54fa63420d743bea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32372273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beacbf459983020fe4247401d4865851e217e32a61f750547345d46291811e89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 02:14:25 GMT
ADD file:ca8cc4b509e305fa07662fbf2234ed78f0056569f6ca047305dc02bcd60f1558 in / 
# Tue, 17 Aug 2021 02:14:26 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 16:10:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:11:49 GMT
ENV HAPROXY_VERSION=2.4.2
# Tue, 17 Aug 2021 16:11:49 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Tue, 17 Aug 2021 16:11:50 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Tue, 17 Aug 2021 16:12:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:12:38 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:12:38 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:12:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:12:39 GMT
USER haproxy
# Tue, 17 Aug 2021 16:12:40 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:13e3f03410ff211945a725435c13065288d48a8cb740f0530e7588012c2679a4`  
		Last Modified: Tue, 17 Aug 2021 02:30:58 GMT  
		Size: 22.7 MB (22746254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb366ce7907325b732435009125848fb9596a1afdb0f87a8703cdf4342e91a4e`  
		Last Modified: Tue, 17 Aug 2021 16:21:35 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d48315f84cbc9b259be6ccc1d3f0cdabd9261d5ce4839e9f76f5c2ce598320`  
		Last Modified: Tue, 17 Aug 2021 16:22:03 GMT  
		Size: 9.6 MB (9624194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977b73ceb84201298d39d7cf916f4f71ab6c67de8d72d2b2f16875ec8d53e664`  
		Last Modified: Tue, 17 Aug 2021 16:21:57 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:aa0d55c9008fbec2ae69f6d19cb2fe2635cc98db24e6c176f254a3bc600a414b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35942317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707f81868db5f80d178b0eacd35631c9921a4fc03eead614ef818c0a4f53264f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:12:02 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:12:58 GMT
ENV HAPROXY_VERSION=2.4.2
# Tue, 17 Aug 2021 08:12:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Tue, 17 Aug 2021 08:12:58 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Tue, 17 Aug 2021 08:13:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:13:41 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:13:41 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:13:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:13:41 GMT
USER haproxy
# Tue, 17 Aug 2021 08:13:41 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc63cf29191f59ddbc41452b9edbe5f8145c4370cd74d3981d50a862173029b`  
		Last Modified: Tue, 17 Aug 2021 08:19:14 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e000ae73340a93669fb008ccf0dc4d556cfe9a0890b24255a0579eac5309fea4`  
		Last Modified: Tue, 17 Aug 2021 08:19:30 GMT  
		Size: 10.0 MB (10025421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e374ae1b0bcaf5e3cb1c612705c13b7d3a6ea8415d2fe4d55432a771b4c402f`  
		Last Modified: Tue, 17 Aug 2021 08:19:28 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4` - linux; 386

```console
$ docker pull haproxy@sha256:306a0b4ee5470c1cd79c83f83cb29aa61237f55d57a59b746b5df2d2c6ffb037
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37794662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc46e642c5ab3fe5dce635c0ce63dceab31a3f647517798a00710df71a57b80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:41:16 GMT
ADD file:0418032b55cd0a6dd515ac277fb9f92354397503cab212d446d3a3d8c647a60f in / 
# Tue, 17 Aug 2021 01:41:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 12:14:55 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:03:20 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 17:03:21 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 17:03:21 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 17:04:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 17:04:22 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:04:23 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:04:23 GMT
USER haproxy
# Tue, 17 Aug 2021 17:04:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c1c94e1f2523d69effaa463d64fc9962cfc67e2a956f0476c94200e7cf19edf0`  
		Last Modified: Tue, 17 Aug 2021 01:50:57 GMT  
		Size: 27.8 MB (27797627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f804b7c921abcc2fb2904ad2092beefd0224c9bd4cb1cf6477727e6f2bbd7599`  
		Last Modified: Tue, 17 Aug 2021 12:26:22 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439c6e37b7d0414cb74b21e0c06ffef78e3cfd0c5e80979da92ac57ba05eb3d2`  
		Last Modified: Tue, 17 Aug 2021 17:15:45 GMT  
		Size: 10.0 MB (9995212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4919e3d48d2fec06a9fd5cbd2be5dccd1863e31181aaf7fd52cb74e5e75526e4`  
		Last Modified: Tue, 17 Aug 2021 17:15:42 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4` - linux; mips64le

```console
$ docker pull haproxy@sha256:25becba2c50de125a20ca6c807ca1144ae10be6a6a9158dca0bd72593b571e0b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35582885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffc7ee854b5982782d23d6545603aedf6f7f6cd813daae1401c39a4dcdcf88d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:12:26 GMT
ADD file:8bd279803ead4ddce8db90b65e89c423f84fbf6042bfbeae8c09486b2e884cde in / 
# Tue, 17 Aug 2021 01:12:27 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:10:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 14:13:15 GMT
ENV HAPROXY_VERSION=2.4.2
# Tue, 17 Aug 2021 14:13:16 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Tue, 17 Aug 2021 14:13:16 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Tue, 17 Aug 2021 14:15:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 14:15:44 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 14:15:45 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 14:15:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:15:45 GMT
USER haproxy
# Tue, 17 Aug 2021 14:15:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a711e3e37b88ef77496c07ed663bb4270ecba9057eba452a91cc9be0bafb9c32`  
		Last Modified: Tue, 17 Aug 2021 01:21:44 GMT  
		Size: 25.8 MB (25813007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac33edc8b81dffec584b1a7ca6a8abea967f70259323fc62ff423b9c01642e`  
		Last Modified: Tue, 17 Aug 2021 14:27:23 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d2df5d6eb229d0c56111f4ba8be6edc422b3933094da75e75da6adbe915d4b`  
		Last Modified: Tue, 17 Aug 2021 14:27:47 GMT  
		Size: 9.8 MB (9768050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6e2dc937ddf621c5676ff4261041f8e9916e2305e110856dac40b16ea69c93`  
		Last Modified: Tue, 17 Aug 2021 14:27:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4` - linux; ppc64le

```console
$ docker pull haproxy@sha256:005c8f2d6acfbf16e77e74ba888f43c5d95d5382e6e421ac5bb2d3820ed267b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41217675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b559f13fdafa1906fb0123fa75d8350827717db10409d2860d0c3db414312e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:34:13 GMT
ADD file:8b9b12a994a2519f725d1ed1f4ab5a444665262678fd8e6c42cf78f32dacb7fa in / 
# Tue, 17 Aug 2021 01:34:20 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 13:36:19 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:43:54 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 16:44:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 16:44:07 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 16:47:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:47:30 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:47:34 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:47:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:47:41 GMT
USER haproxy
# Tue, 17 Aug 2021 16:47:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c3e09f0e3e7f6fcb741a4c9214b63e341e1d9b53d7689a5ad6ff640b61a82541`  
		Last Modified: Tue, 17 Aug 2021 01:48:22 GMT  
		Size: 30.6 MB (30553721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb7833dc31cf72935b478f7bf90e34f0f2a22d8260da177e4648ac973af1f9c`  
		Last Modified: Tue, 17 Aug 2021 14:24:41 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84b036d99ad375fba8e2862f8eecba0672b2addce066456d8f0af3d9dce36d2`  
		Last Modified: Tue, 17 Aug 2021 17:04:19 GMT  
		Size: 10.7 MB (10662112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec7ca3be675051e451993a6916eac7da569020d428bcf5f04ee244d006878a4`  
		Last Modified: Tue, 17 Aug 2021 17:04:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4` - linux; s390x

```console
$ docker pull haproxy@sha256:3fa33eb62f823be6cff266718be3d9cf7e878075bc429c40d020ff51ca806a62
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35587952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b048110fe88e7fedfb39c5067e23dabd5387a4a39e2f07225995322b8333b434`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 07:18:12 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 07:19:41 GMT
ENV HAPROXY_VERSION=2.4.2
# Tue, 17 Aug 2021 07:19:42 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Tue, 17 Aug 2021 07:19:42 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Tue, 17 Aug 2021 07:20:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 07:20:28 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 07:20:29 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 07:20:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 07:20:30 GMT
USER haproxy
# Tue, 17 Aug 2021 07:20:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16a2f2a1452470a1d818d8d16934d08d2a57b312ceabcce8c1cfad6c99f00a2`  
		Last Modified: Tue, 17 Aug 2021 07:28:00 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc2a7c361fe340d5b70919c5991c098506bb6dd4e2ff6c8696c0135074b51fc`  
		Last Modified: Tue, 17 Aug 2021 07:28:12 GMT  
		Size: 9.8 MB (9825271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6304b5ba716e53c4d88c06c0d3564da13d2ab9cf06cb9ec72e3f70c902a5bb`  
		Last Modified: Tue, 17 Aug 2021 07:28:11 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.4-alpine`

```console
$ docker pull haproxy@sha256:4456ce96d7a1a0f0db94739071949bbf9f1daaf7eabaaecf220599be5284e447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.4-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:2b51b9f7b11fd789be82b17272b8d50c03286b07533abdd2917b4f67b6c551b9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10134063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d615f803d0602d65618848a61a788ec68a0ade7335d9f67dcbc60a003f5a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:43:18 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:51:46 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 16:51:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 16:51:47 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 16:52:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:52:50 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:52:51 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:52:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:52:51 GMT
USER haproxy
# Tue, 17 Aug 2021 16:52:51 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22138861da3ab6ae8583cf62942545e1bb75874501f4a8d45d13a38c848a908`  
		Last Modified: Fri, 06 Aug 2021 19:51:27 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084a6fa47ea6c62e03b343daa72870da70e747dd19b31aa2cd7378f9cf6a0fd9`  
		Last Modified: Tue, 17 Aug 2021 17:00:45 GMT  
		Size: 7.3 MB (7319417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f71cfe692953ce9359c70a04664d75052fc519bcc90a2c5cb96123a9e55e35`  
		Last Modified: Tue, 17 Aug 2021 17:00:44 GMT  
		Size: 444.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:5858c663bfb65657c6aabc6688d710f0aa1924b0476411989f1b8265e1b030fe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9919310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697f662af8e6d0dcb3ef652dbbbae30b74994995f5964d3e2f9491ee980510c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:49:32 GMT
ADD file:7f2c7deda009eabdcbbdccb11e854043d32c498e64e7e1ca02165d7bb4261d39 in / 
# Fri, 06 Aug 2021 17:49:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:15:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:36:55 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 16:36:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 16:36:56 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 16:37:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:37:24 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:37:24 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:37:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:37:25 GMT
USER haproxy
# Tue, 17 Aug 2021 16:37:25 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f465bb3e9fcd0c42f936ecc566c6e40353c00f3089b2b2c2ea1663c30f89d3ab`  
		Last Modified: Fri, 06 Aug 2021 17:51:00 GMT  
		Size: 2.6 MB (2626350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332ccafb58fe1d8ed3d3d5ad9c01adba33d922f28a398285d2eb67fed7c8bee8`  
		Last Modified: Fri, 06 Aug 2021 18:20:57 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405b6f9f13b134ed6de3cf66afffe633c706556bc16fd88ef74043d17a48c54`  
		Last Modified: Tue, 17 Aug 2021 16:41:26 GMT  
		Size: 7.3 MB (7291312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a5b0fa7ec3ddc3c829f96564fdd519c09a290910b48469cc5fe28cc476ab21`  
		Last Modified: Tue, 17 Aug 2021 16:41:22 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:a95a2208dbe0d98814a817cc18b5f3a68422b64b02106d1ec761949d196b7b3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9632801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da47331a3ac424edd35992104629f17383106bda6b4bfd8f913f755a7a700ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:57:32 GMT
ADD file:3a35ff3ac0d80289d419a4d6d8319610c38e1936d296addafb9aaf506946230f in / 
# Fri, 06 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:54:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 19:55:20 GMT
ENV HAPROXY_VERSION=2.4.2
# Fri, 06 Aug 2021 19:55:20 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Fri, 06 Aug 2021 19:55:21 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Fri, 06 Aug 2021 19:56:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 19:56:04 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 19:56:05 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 19:56:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 19:56:07 GMT
USER haproxy
# Fri, 06 Aug 2021 19:56:08 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4ee0caa23b369b04827640a4be298bf4ff7bacd030c77e915f5d7fb8f987594a`  
		Last Modified: Fri, 06 Aug 2021 17:58:57 GMT  
		Size: 2.4 MB (2429359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548ff9918828f96cb9a5e5656ea589d79e6fb1d7b9f0d693feff2dbefc6929fe`  
		Last Modified: Fri, 06 Aug 2021 20:02:54 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b4da96d470a19a8480afc1577eca661b82235d415ce7acee35780bfdbed1b`  
		Last Modified: Fri, 06 Aug 2021 20:03:17 GMT  
		Size: 7.2 MB (7201797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2bf593e46ec3d6ef735a051c2da655872e82e7c811a9be8a9f4127f2d45ffbe`  
		Last Modified: Fri, 06 Aug 2021 20:03:15 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:d8f5c33bebd1828228ca0f3ec81f9cd2f27f44c9179694732e90e9ed533720bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10134877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f5d862f5f50a3173fd52922695ff763bd507483fc29cbe1b10d480f3cba710`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:39:26 GMT
ADD file:1a8fd1066485e1261462e689c1a072f010c1d3be904b73ef2b84128fac652951 in / 
# Fri, 06 Aug 2021 17:39:27 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:38:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 18:40:06 GMT
ENV HAPROXY_VERSION=2.4.2
# Fri, 06 Aug 2021 18:40:06 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Fri, 06 Aug 2021 18:40:06 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Fri, 06 Aug 2021 18:41:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 18:41:05 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 18:41:05 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 18:41:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 18:41:06 GMT
USER haproxy
# Fri, 06 Aug 2021 18:41:06 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fd3acdcea5682abced546ec19fb6ebee725c5184e5d91614c469c0a79e67f2d0`  
		Last Modified: Fri, 06 Aug 2021 17:40:12 GMT  
		Size: 2.7 MB (2710613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a23793c1bba0796c0f469305ee92dd0f1cb8299963e4da4249d0f5aa2fcea0`  
		Last Modified: Fri, 06 Aug 2021 18:46:06 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0169a9e4faea9eebd85152cc75662780750a945ac1632d8f332980a081224555`  
		Last Modified: Fri, 06 Aug 2021 18:46:23 GMT  
		Size: 7.4 MB (7422621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179faf353137636acdb95b716a1e9825d02900a111a3a742e6499b7b753a5bf3`  
		Last Modified: Fri, 06 Aug 2021 18:46:22 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:27057e7fc931ea635e2ca78a31c85fae8c7a5cae3f2a3011b1fe64a47d8408ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10003948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a803ff7d44673ff6a4fd6e673048cdcee2ac921b6bc8639ce0e46572eb09f90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:38:26 GMT
ADD file:bafaec4a54d6cef99b5f3660d074a3d2251e4d4bd09df9ea65f33e9bffb7d88d in / 
# Fri, 06 Aug 2021 17:38:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:19:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:04:33 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 17:04:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 17:04:34 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 17:05:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 17:05:57 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:05:57 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:05:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:05:57 GMT
USER haproxy
# Tue, 17 Aug 2021 17:05:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:935703e1179e32e201e4a36d5664d58299dc8e7bcac197b70c295c0a59216db1`  
		Last Modified: Fri, 06 Aug 2021 17:39:15 GMT  
		Size: 2.8 MB (2821910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695b2822110160b402b8f359bb19d954a46a6ead94f868feba7d00f5a10e50e`  
		Last Modified: Fri, 06 Aug 2021 19:32:18 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d209c067bdfff48477adac6f34b7786f8d8f1d13d1a4b8dd7d70cf7d67ce246`  
		Last Modified: Tue, 17 Aug 2021 17:16:05 GMT  
		Size: 7.2 MB (7180394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb4e0881c29decc18e87cfb212fab9c4066e818a6ad45d14a818e82df909d3f`  
		Last Modified: Tue, 17 Aug 2021 17:16:03 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:875275a0ea30ad381d79d3af91d8046a2e262886b3c89f568b9733e5fbb200b8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10559704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893d2d1de6e4528ad75aa23fbe6fdc87edb44098071fb262cd4dbe51f32c4898`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:17:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:48:04 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 16:48:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 16:48:09 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 16:48:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:48:54 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:48:55 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:48:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:48:58 GMT
USER haproxy
# Tue, 17 Aug 2021 16:49:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d374dad070e00fdb493e29a3aa64b375dbec801497e01d3b8ddbf7cc967634cb`  
		Last Modified: Fri, 06 Aug 2021 21:27:30 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6b7fbbf87c5c7cc03966a6a0c19b891ca8a793a9a70ac80066e9d1240b2943`  
		Last Modified: Tue, 17 Aug 2021 17:04:38 GMT  
		Size: 7.7 MB (7746906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d439e35aac99cbbb58f67662da81ed697e00d547171fc923ea5d472e85334c1b`  
		Last Modified: Tue, 17 Aug 2021 17:04:36 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:67c77b2f75cda356f4462fa8c7cfe05d80b220bb7e3ddff6782557ca308381e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9899025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8353b377710bdcc56a8dd1fcdf4213b83d4378a795634015c8ec0817188591f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:54:24 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 14 May 2021 19:45:22 GMT
ENV HAPROXY_VERSION=2.4.0
# Fri, 14 May 2021 19:45:23 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.0.tar.gz
# Fri, 14 May 2021 19:45:23 GMT
ENV HAPROXY_SHA256=0a6962adaf5a1291db87e3eb4ddf906a72fed535dbd2255b164b7d8394a53640
# Fri, 14 May 2021 19:46:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 14 May 2021 19:46:14 GMT
STOPSIGNAL SIGUSR1
# Fri, 14 May 2021 19:46:14 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 14 May 2021 19:46:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 May 2021 19:46:15 GMT
USER haproxy
# Fri, 14 May 2021 19:46:15 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267275aba58470c82626189a59be76cd169bd245568e2f2545ed1ee64ff8a8ff`  
		Last Modified: Wed, 14 Apr 2021 20:59:06 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1af9bde57dd624c224ba02793a7568cd9f00874c978ff5ab4d6bc0c32fdb81f`  
		Last Modified: Fri, 14 May 2021 19:48:00 GMT  
		Size: 7.3 MB (7294741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68dd09d54ba9406459ae1956173c0df96676de52e5a01f9392966e3493acae68`  
		Last Modified: Fri, 14 May 2021 19:47:59 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.4.3`

```console
$ docker pull haproxy@sha256:0314cccc560d50d85119f3a8195464f435ad3e2c8409984aed8a554c656a8443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le

### `haproxy:2.4.3` - linux; amd64

```console
$ docker pull haproxy@sha256:be84aa6aa3e60de3ce38adeac6e6d0e01c428e0c02b0a0e7b6d1b42d0bf36a29
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37304052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06340012d09399fd0be90a29f16bc2b8041b9322e9095c6fceeed1aa2f6280cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 10:43:34 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:50:46 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 16:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 16:50:47 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 16:51:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:51:38 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:51:38 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:51:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:51:38 GMT
USER haproxy
# Tue, 17 Aug 2021 16:51:39 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd06683556254cbe06dad4624837c2dcbd2fec67c7fbdd057251f0a207a9315`  
		Last Modified: Tue, 17 Aug 2021 10:53:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341a1a625c8fa0015a85b943c2bc17495fb26b105d5b07b3911a65b0967ea4be`  
		Last Modified: Tue, 17 Aug 2021 17:00:29 GMT  
		Size: 10.2 MB (10156239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63116b577243ee3d88e09a144ffe2122ebb8f78d3ce8b3517e1d39116a9c876a`  
		Last Modified: Tue, 17 Aug 2021 17:00:27 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4.3` - linux; 386

```console
$ docker pull haproxy@sha256:306a0b4ee5470c1cd79c83f83cb29aa61237f55d57a59b746b5df2d2c6ffb037
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37794662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc46e642c5ab3fe5dce635c0ce63dceab31a3f647517798a00710df71a57b80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:41:16 GMT
ADD file:0418032b55cd0a6dd515ac277fb9f92354397503cab212d446d3a3d8c647a60f in / 
# Tue, 17 Aug 2021 01:41:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 12:14:55 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:03:20 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 17:03:21 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 17:03:21 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 17:04:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 17:04:22 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:04:23 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:04:23 GMT
USER haproxy
# Tue, 17 Aug 2021 17:04:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c1c94e1f2523d69effaa463d64fc9962cfc67e2a956f0476c94200e7cf19edf0`  
		Last Modified: Tue, 17 Aug 2021 01:50:57 GMT  
		Size: 27.8 MB (27797627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f804b7c921abcc2fb2904ad2092beefd0224c9bd4cb1cf6477727e6f2bbd7599`  
		Last Modified: Tue, 17 Aug 2021 12:26:22 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439c6e37b7d0414cb74b21e0c06ffef78e3cfd0c5e80979da92ac57ba05eb3d2`  
		Last Modified: Tue, 17 Aug 2021 17:15:45 GMT  
		Size: 10.0 MB (9995212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4919e3d48d2fec06a9fd5cbd2be5dccd1863e31181aaf7fd52cb74e5e75526e4`  
		Last Modified: Tue, 17 Aug 2021 17:15:42 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4.3` - linux; ppc64le

```console
$ docker pull haproxy@sha256:005c8f2d6acfbf16e77e74ba888f43c5d95d5382e6e421ac5bb2d3820ed267b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41217675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b559f13fdafa1906fb0123fa75d8350827717db10409d2860d0c3db414312e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:34:13 GMT
ADD file:8b9b12a994a2519f725d1ed1f4ab5a444665262678fd8e6c42cf78f32dacb7fa in / 
# Tue, 17 Aug 2021 01:34:20 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 13:36:19 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:43:54 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 16:44:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 16:44:07 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 16:47:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:47:30 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:47:34 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:47:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:47:41 GMT
USER haproxy
# Tue, 17 Aug 2021 16:47:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c3e09f0e3e7f6fcb741a4c9214b63e341e1d9b53d7689a5ad6ff640b61a82541`  
		Last Modified: Tue, 17 Aug 2021 01:48:22 GMT  
		Size: 30.6 MB (30553721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb7833dc31cf72935b478f7bf90e34f0f2a22d8260da177e4648ac973af1f9c`  
		Last Modified: Tue, 17 Aug 2021 14:24:41 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84b036d99ad375fba8e2862f8eecba0672b2addce066456d8f0af3d9dce36d2`  
		Last Modified: Tue, 17 Aug 2021 17:04:19 GMT  
		Size: 10.7 MB (10662112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec7ca3be675051e451993a6916eac7da569020d428bcf5f04ee244d006878a4`  
		Last Modified: Tue, 17 Aug 2021 17:04:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.4.3-alpine`

```console
$ docker pull haproxy@sha256:5e9bde2e8b581c01461c091ddc1987664f8f5ec6d574ca6f14b85d59a65024e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; 386
	-	linux; ppc64le

### `haproxy:2.4.3-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:2b51b9f7b11fd789be82b17272b8d50c03286b07533abdd2917b4f67b6c551b9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10134063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d615f803d0602d65618848a61a788ec68a0ade7335d9f67dcbc60a003f5a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:43:18 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:51:46 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 16:51:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 16:51:47 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 16:52:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:52:50 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:52:51 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:52:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:52:51 GMT
USER haproxy
# Tue, 17 Aug 2021 16:52:51 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22138861da3ab6ae8583cf62942545e1bb75874501f4a8d45d13a38c848a908`  
		Last Modified: Fri, 06 Aug 2021 19:51:27 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084a6fa47ea6c62e03b343daa72870da70e747dd19b31aa2cd7378f9cf6a0fd9`  
		Last Modified: Tue, 17 Aug 2021 17:00:45 GMT  
		Size: 7.3 MB (7319417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f71cfe692953ce9359c70a04664d75052fc519bcc90a2c5cb96123a9e55e35`  
		Last Modified: Tue, 17 Aug 2021 17:00:44 GMT  
		Size: 444.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4.3-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:5858c663bfb65657c6aabc6688d710f0aa1924b0476411989f1b8265e1b030fe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9919310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697f662af8e6d0dcb3ef652dbbbae30b74994995f5964d3e2f9491ee980510c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:49:32 GMT
ADD file:7f2c7deda009eabdcbbdccb11e854043d32c498e64e7e1ca02165d7bb4261d39 in / 
# Fri, 06 Aug 2021 17:49:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:15:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:36:55 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 16:36:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 16:36:56 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 16:37:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:37:24 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:37:24 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:37:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:37:25 GMT
USER haproxy
# Tue, 17 Aug 2021 16:37:25 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f465bb3e9fcd0c42f936ecc566c6e40353c00f3089b2b2c2ea1663c30f89d3ab`  
		Last Modified: Fri, 06 Aug 2021 17:51:00 GMT  
		Size: 2.6 MB (2626350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332ccafb58fe1d8ed3d3d5ad9c01adba33d922f28a398285d2eb67fed7c8bee8`  
		Last Modified: Fri, 06 Aug 2021 18:20:57 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405b6f9f13b134ed6de3cf66afffe633c706556bc16fd88ef74043d17a48c54`  
		Last Modified: Tue, 17 Aug 2021 16:41:26 GMT  
		Size: 7.3 MB (7291312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a5b0fa7ec3ddc3c829f96564fdd519c09a290910b48469cc5fe28cc476ab21`  
		Last Modified: Tue, 17 Aug 2021 16:41:22 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4.3-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:27057e7fc931ea635e2ca78a31c85fae8c7a5cae3f2a3011b1fe64a47d8408ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10003948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a803ff7d44673ff6a4fd6e673048cdcee2ac921b6bc8639ce0e46572eb09f90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:38:26 GMT
ADD file:bafaec4a54d6cef99b5f3660d074a3d2251e4d4bd09df9ea65f33e9bffb7d88d in / 
# Fri, 06 Aug 2021 17:38:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:19:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:04:33 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 17:04:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 17:04:34 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 17:05:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 17:05:57 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:05:57 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:05:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:05:57 GMT
USER haproxy
# Tue, 17 Aug 2021 17:05:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:935703e1179e32e201e4a36d5664d58299dc8e7bcac197b70c295c0a59216db1`  
		Last Modified: Fri, 06 Aug 2021 17:39:15 GMT  
		Size: 2.8 MB (2821910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695b2822110160b402b8f359bb19d954a46a6ead94f868feba7d00f5a10e50e`  
		Last Modified: Fri, 06 Aug 2021 19:32:18 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d209c067bdfff48477adac6f34b7786f8d8f1d13d1a4b8dd7d70cf7d67ce246`  
		Last Modified: Tue, 17 Aug 2021 17:16:05 GMT  
		Size: 7.2 MB (7180394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb4e0881c29decc18e87cfb212fab9c4066e818a6ad45d14a818e82df909d3f`  
		Last Modified: Tue, 17 Aug 2021 17:16:03 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.4.3-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:875275a0ea30ad381d79d3af91d8046a2e262886b3c89f568b9733e5fbb200b8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10559704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893d2d1de6e4528ad75aa23fbe6fdc87edb44098071fb262cd4dbe51f32c4898`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:17:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:48:04 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 16:48:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 16:48:09 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 16:48:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:48:54 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:48:55 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:48:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:48:58 GMT
USER haproxy
# Tue, 17 Aug 2021 16:49:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d374dad070e00fdb493e29a3aa64b375dbec801497e01d3b8ddbf7cc967634cb`  
		Last Modified: Fri, 06 Aug 2021 21:27:30 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6b7fbbf87c5c7cc03966a6a0c19b891ca8a793a9a70ac80066e9d1240b2943`  
		Last Modified: Tue, 17 Aug 2021 17:04:38 GMT  
		Size: 7.7 MB (7746906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d439e35aac99cbbb58f67662da81ed697e00d547171fc923ea5d472e85334c1b`  
		Last Modified: Tue, 17 Aug 2021 17:04:36 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.5-dev`

```console
$ docker pull haproxy@sha256:612a4a559acc23758c0f7522420db641d6ec94a4885318d63d639cb0c1e7ecb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.5-dev` - linux; amd64

```console
$ docker pull haproxy@sha256:8331a9fda117416fcdaf09c5d2eefd4cee0e8b2379b38472e40d036f6bd2e78f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37486116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2eaccbe4c9c8b2ef5edfb5e6e8da6788182948341e98e841e5b132f5a4db4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 10:43:34 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:48:09 GMT
ENV HAPROXY_VERSION=2.5-dev4
# Tue, 17 Aug 2021 16:48:09 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev4.tar.gz
# Tue, 17 Aug 2021 16:48:09 GMT
ENV HAPROXY_SHA256=9ca0bff5255ccadb42834785097cd380694dc087af6f6556585a979ddf470966
# Tue, 17 Aug 2021 16:49:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:49:07 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:49:07 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:49:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:49:07 GMT
USER haproxy
# Tue, 17 Aug 2021 16:49:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd06683556254cbe06dad4624837c2dcbd2fec67c7fbdd057251f0a207a9315`  
		Last Modified: Tue, 17 Aug 2021 10:53:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92493dc602276088b8fb3304dae6649a52b726417b9dd6e697f9e8a6a644acc4`  
		Last Modified: Tue, 17 Aug 2021 17:00:05 GMT  
		Size: 10.3 MB (10338303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158cb2201f0691d9017fa2ddeb87fc7d70e46ce4ec8870ed6f9b0aa49e519366`  
		Last Modified: Tue, 17 Aug 2021 17:00:03 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.5-dev` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:00ff6ffe7f59a443fddb0bac46bfa4434d3d6ef93585b0c4f532902dbd318ed1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34783090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781cded835fd627e3d7c2d8d0c680b7dc36aeb09ab5969a9d5bc4d276ec60028`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:56:50 GMT
ADD file:f29260935f1f8b3eef5eb0d5e49dd4cf5370e8731a3f4006d6023724bce09601 in / 
# Tue, 17 Aug 2021 01:56:51 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:39:10 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:39:10 GMT
ENV HAPROXY_VERSION=2.5-dev3
# Tue, 17 Aug 2021 08:39:11 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev3.tar.gz
# Tue, 17 Aug 2021 08:39:11 GMT
ENV HAPROXY_SHA256=519343d7304f14701f6c1f7b1f56f1f0acadaf2e7ee21872bca2949ba669fb58
# Tue, 17 Aug 2021 08:40:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:40:05 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:40:06 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:40:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:40:06 GMT
USER haproxy
# Tue, 17 Aug 2021 08:40:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3dfab4a5b2accf2d709d8c7d14a42715948ecf2d6da4943a6e2c0de8ae7536a0`  
		Last Modified: Tue, 17 Aug 2021 02:12:42 GMT  
		Size: 24.9 MB (24879063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeabbf4f2af3ef66d78a317a4b3a0704a061a5de2611c57b0bfc47b775c2ed8b`  
		Last Modified: Tue, 17 Aug 2021 08:48:10 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79631849baffd3251e858de46edbef6e989d0d82251eaab3358d9d5a803e0e1`  
		Last Modified: Tue, 17 Aug 2021 08:48:16 GMT  
		Size: 9.9 MB (9902201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f220380e232f0eb3a4c19b51bb8783c562ededf13e596099e750ef5dd1360955`  
		Last Modified: Tue, 17 Aug 2021 08:48:10 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.5-dev` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:9c795c5ec594ab7e5fc830b4cbcb728b6936a36710a61383861882626902d23c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32486503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de146fe89553b8ba7ce59ed52ae531e847c860d047e1d137b8400271de52a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 02:14:25 GMT
ADD file:ca8cc4b509e305fa07662fbf2234ed78f0056569f6ca047305dc02bcd60f1558 in / 
# Tue, 17 Aug 2021 02:14:26 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 16:10:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:10:36 GMT
ENV HAPROXY_VERSION=2.5-dev3
# Tue, 17 Aug 2021 16:10:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev3.tar.gz
# Tue, 17 Aug 2021 16:10:37 GMT
ENV HAPROXY_SHA256=519343d7304f14701f6c1f7b1f56f1f0acadaf2e7ee21872bca2949ba669fb58
# Tue, 17 Aug 2021 16:11:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:11:25 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:11:26 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:11:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:11:26 GMT
USER haproxy
# Tue, 17 Aug 2021 16:11:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:13e3f03410ff211945a725435c13065288d48a8cb740f0530e7588012c2679a4`  
		Last Modified: Tue, 17 Aug 2021 02:30:58 GMT  
		Size: 22.7 MB (22746254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb366ce7907325b732435009125848fb9596a1afdb0f87a8703cdf4342e91a4e`  
		Last Modified: Tue, 17 Aug 2021 16:21:35 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9bde3d929319adb798bd6ef8f7e7813f5d263642dc0bebe32e2b192f416abd`  
		Last Modified: Tue, 17 Aug 2021 16:21:42 GMT  
		Size: 9.7 MB (9738424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e5f1cdabee1aba1fe64e4d49de9d0e61fa48a6c2e6e8dd2830451357d5e7dc`  
		Last Modified: Tue, 17 Aug 2021 16:21:35 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.5-dev` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:13424c8927504c4b05d3d1a7d04a8f0ede5a5f9e3073e6af793581558ae39ecd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36060747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905fe33b28e6afb94e6fadb571afcc5ee6e9482b59c34657a5ac089211414e6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:12:02 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:12:02 GMT
ENV HAPROXY_VERSION=2.5-dev3
# Tue, 17 Aug 2021 08:12:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev3.tar.gz
# Tue, 17 Aug 2021 08:12:03 GMT
ENV HAPROXY_SHA256=519343d7304f14701f6c1f7b1f56f1f0acadaf2e7ee21872bca2949ba669fb58
# Tue, 17 Aug 2021 08:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:12:46 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:12:46 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:12:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:12:46 GMT
USER haproxy
# Tue, 17 Aug 2021 08:12:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc63cf29191f59ddbc41452b9edbe5f8145c4370cd74d3981d50a862173029b`  
		Last Modified: Tue, 17 Aug 2021 08:19:14 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04139e768baf0a4c44a963935b3c309c61de4774b9a0b71077aa849f9a4a2e0`  
		Last Modified: Tue, 17 Aug 2021 08:19:15 GMT  
		Size: 10.1 MB (10143849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e873ced006b0f3541eba47c8762c1044a0652a44535ca9258b9618544db3ff`  
		Last Modified: Tue, 17 Aug 2021 08:19:14 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.5-dev` - linux; 386

```console
$ docker pull haproxy@sha256:8d4c68400cb20e02bd055c72ec551b3ab7beaff34eeee187228b02fea6dc93b2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37969826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f4ce7e1985625ae007420eaee2c186ed709fdacd0095c27847f19a040bb16c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:41:16 GMT
ADD file:0418032b55cd0a6dd515ac277fb9f92354397503cab212d446d3a3d8c647a60f in / 
# Tue, 17 Aug 2021 01:41:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 12:14:55 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:00:41 GMT
ENV HAPROXY_VERSION=2.5-dev4
# Tue, 17 Aug 2021 17:00:41 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev4.tar.gz
# Tue, 17 Aug 2021 17:00:41 GMT
ENV HAPROXY_SHA256=9ca0bff5255ccadb42834785097cd380694dc087af6f6556585a979ddf470966
# Tue, 17 Aug 2021 17:01:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 17:01:39 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:01:39 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:01:39 GMT
USER haproxy
# Tue, 17 Aug 2021 17:01:40 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c1c94e1f2523d69effaa463d64fc9962cfc67e2a956f0476c94200e7cf19edf0`  
		Last Modified: Tue, 17 Aug 2021 01:50:57 GMT  
		Size: 27.8 MB (27797627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f804b7c921abcc2fb2904ad2092beefd0224c9bd4cb1cf6477727e6f2bbd7599`  
		Last Modified: Tue, 17 Aug 2021 12:26:22 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81cbed7fc459541b845ad80b3aecadc67bf9d2fd9657eb35a6a54a7755ceb6b6`  
		Last Modified: Tue, 17 Aug 2021 17:15:14 GMT  
		Size: 10.2 MB (10170376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba8d74eedc7b3f631df44fa80b40eb4ea92dee537d14dc96f225161dc8139bd`  
		Last Modified: Tue, 17 Aug 2021 17:15:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.5-dev` - linux; mips64le

```console
$ docker pull haproxy@sha256:173aaf09d23eb6f09ec944e7368bbd38ad2bdd2d1809259db67a76b11eedb5d4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35711938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38df953da7052235cd74a01664a2e33e8a97c977cee20e431f145e343489151`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:12:26 GMT
ADD file:8bd279803ead4ddce8db90b65e89c423f84fbf6042bfbeae8c09486b2e884cde in / 
# Tue, 17 Aug 2021 01:12:27 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:10:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 14:10:36 GMT
ENV HAPROXY_VERSION=2.5-dev3
# Tue, 17 Aug 2021 14:10:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev3.tar.gz
# Tue, 17 Aug 2021 14:10:37 GMT
ENV HAPROXY_SHA256=519343d7304f14701f6c1f7b1f56f1f0acadaf2e7ee21872bca2949ba669fb58
# Tue, 17 Aug 2021 14:13:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 14:13:08 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 14:13:08 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 14:13:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:13:09 GMT
USER haproxy
# Tue, 17 Aug 2021 14:13:09 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a711e3e37b88ef77496c07ed663bb4270ecba9057eba452a91cc9be0bafb9c32`  
		Last Modified: Tue, 17 Aug 2021 01:21:44 GMT  
		Size: 25.8 MB (25813007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac33edc8b81dffec584b1a7ca6a8abea967f70259323fc62ff423b9c01642e`  
		Last Modified: Tue, 17 Aug 2021 14:27:23 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4672a20b0e55ffb044da84273b0dbabc2ce0281cd848bb5a538189eb056b5e55`  
		Last Modified: Tue, 17 Aug 2021 14:27:30 GMT  
		Size: 9.9 MB (9897102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326cf76dc5211614a6a6a9200ce574315789f0d6b74cac8709b867c0c6554591`  
		Last Modified: Tue, 17 Aug 2021 14:27:23 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.5-dev` - linux; ppc64le

```console
$ docker pull haproxy@sha256:e70f6c7f808e6bc828fe716dd12ffdb3b5d4e1227368a0752b94cbe1b2f322ca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41419960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007076dc75f1416fb4689c0609533936e1165c881018c7668f33b6fa8f2aebe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:34:13 GMT
ADD file:8b9b12a994a2519f725d1ed1f4ab5a444665262678fd8e6c42cf78f32dacb7fa in / 
# Tue, 17 Aug 2021 01:34:20 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 13:36:19 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:38:31 GMT
ENV HAPROXY_VERSION=2.5-dev4
# Tue, 17 Aug 2021 16:38:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev4.tar.gz
# Tue, 17 Aug 2021 16:38:38 GMT
ENV HAPROXY_SHA256=9ca0bff5255ccadb42834785097cd380694dc087af6f6556585a979ddf470966
# Tue, 17 Aug 2021 16:41:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:41:59 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:42:02 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:42:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:42:07 GMT
USER haproxy
# Tue, 17 Aug 2021 16:42:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c3e09f0e3e7f6fcb741a4c9214b63e341e1d9b53d7689a5ad6ff640b61a82541`  
		Last Modified: Tue, 17 Aug 2021 01:48:22 GMT  
		Size: 30.6 MB (30553721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb7833dc31cf72935b478f7bf90e34f0f2a22d8260da177e4648ac973af1f9c`  
		Last Modified: Tue, 17 Aug 2021 14:24:41 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cbbd501c39cced7a73e666c66609762c53b6b9566703d6a9b703ccef228443`  
		Last Modified: Tue, 17 Aug 2021 17:03:51 GMT  
		Size: 10.9 MB (10864396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2105b9725ffa84427ffb73cd8482b1f3ff30b15d524f8b9426c561e05f0a4934`  
		Last Modified: Tue, 17 Aug 2021 17:03:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.5-dev` - linux; s390x

```console
$ docker pull haproxy@sha256:b3854fe1ef89c6926be76b55769cd7cb0db1cb3ab1980de4cedf497a2e90ab12
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35711566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285975ae5a097f5043d0b6d7c2b33147727634a94d26ff26681240fe0630d1e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 07:18:12 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 07:18:12 GMT
ENV HAPROXY_VERSION=2.5-dev3
# Tue, 17 Aug 2021 07:18:12 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev3.tar.gz
# Tue, 17 Aug 2021 07:18:13 GMT
ENV HAPROXY_SHA256=519343d7304f14701f6c1f7b1f56f1f0acadaf2e7ee21872bca2949ba669fb58
# Tue, 17 Aug 2021 07:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 07:18:56 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 07:18:56 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 07:18:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 07:18:57 GMT
USER haproxy
# Tue, 17 Aug 2021 07:18:57 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16a2f2a1452470a1d818d8d16934d08d2a57b312ceabcce8c1cfad6c99f00a2`  
		Last Modified: Tue, 17 Aug 2021 07:28:00 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3edc6da6e2d32e27214d00a626cf2f3a9ed0168013f18edef2150ade5da647e`  
		Last Modified: Tue, 17 Aug 2021 07:28:02 GMT  
		Size: 9.9 MB (9948884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae9d1b35a9058565a50c04a4eb387b63c4098310c48c1f3da136d9de7ec4059`  
		Last Modified: Tue, 17 Aug 2021 07:28:00 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.5-dev-alpine`

```console
$ docker pull haproxy@sha256:7a8e1a16a6036ff57e53030c115185a701352d87d7ec7eb0e8534ea5e86e4239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:2.5-dev-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:bb251766affec40e2cfcfa235aea22333e099e4ee0718105bd5a876d4908ea71
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c590cbef1ffd2647227e6c3b66fb761ae70743d676dce8b51d13e9e911cdd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:43:18 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:49:21 GMT
ENV HAPROXY_VERSION=2.5-dev4
# Tue, 17 Aug 2021 16:49:21 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev4.tar.gz
# Tue, 17 Aug 2021 16:49:21 GMT
ENV HAPROXY_SHA256=9ca0bff5255ccadb42834785097cd380694dc087af6f6556585a979ddf470966
# Tue, 17 Aug 2021 16:50:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:50:29 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:50:29 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:50:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:50:30 GMT
USER haproxy
# Tue, 17 Aug 2021 16:50:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22138861da3ab6ae8583cf62942545e1bb75874501f4a8d45d13a38c848a908`  
		Last Modified: Fri, 06 Aug 2021 19:51:27 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85446614356ec7bbcfbab89e23cfb3f3d9126325656da0426138d1098a6b5a02`  
		Last Modified: Tue, 17 Aug 2021 17:00:17 GMT  
		Size: 7.5 MB (7507193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a548f5b0d4b9592bf62f380b142326a1d5f667d495b33fa30da479067cdee2f`  
		Last Modified: Tue, 17 Aug 2021 17:00:15 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.5-dev-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:ddfb376632d66f06de40f97d42dfa21a9baecb80b9a40251d70d11c995b7aa1b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10095130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8076668261692627f5e3a1191e24487ff2c571cc249ce6ab7525aca88e5a1801`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:49:32 GMT
ADD file:7f2c7deda009eabdcbbdccb11e854043d32c498e64e7e1ca02165d7bb4261d39 in / 
# Fri, 06 Aug 2021 17:49:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:15:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:36:13 GMT
ENV HAPROXY_VERSION=2.5-dev4
# Tue, 17 Aug 2021 16:36:13 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev4.tar.gz
# Tue, 17 Aug 2021 16:36:14 GMT
ENV HAPROXY_SHA256=9ca0bff5255ccadb42834785097cd380694dc087af6f6556585a979ddf470966
# Tue, 17 Aug 2021 16:36:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:36:42 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:36:43 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:36:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:36:44 GMT
USER haproxy
# Tue, 17 Aug 2021 16:36:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f465bb3e9fcd0c42f936ecc566c6e40353c00f3089b2b2c2ea1663c30f89d3ab`  
		Last Modified: Fri, 06 Aug 2021 17:51:00 GMT  
		Size: 2.6 MB (2626350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332ccafb58fe1d8ed3d3d5ad9c01adba33d922f28a398285d2eb67fed7c8bee8`  
		Last Modified: Fri, 06 Aug 2021 18:20:57 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8510845bd2c94130060bc6615c872643f4301e963871f5e78e2b993018a40ee`  
		Last Modified: Tue, 17 Aug 2021 16:41:09 GMT  
		Size: 7.5 MB (7467134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a12d2254dcc32b20bea441a3772db0a9153d270455e862a1675e572f95df03b`  
		Last Modified: Tue, 17 Aug 2021 16:41:04 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.5-dev-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:54fa4aa34f71a0bca76665f306af4962b15497c1d0c32c5f11562ee7bbf737a3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9754896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f36cde1c33042cab69b986520611f7d0994b2f6bdfd1e7f4f92342baa2cca93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:57:32 GMT
ADD file:3a35ff3ac0d80289d419a4d6d8319610c38e1936d296addafb9aaf506946230f in / 
# Fri, 06 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:54:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 19:54:04 GMT
ENV HAPROXY_VERSION=2.5-dev3
# Fri, 06 Aug 2021 19:54:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev3.tar.gz
# Fri, 06 Aug 2021 19:54:05 GMT
ENV HAPROXY_SHA256=519343d7304f14701f6c1f7b1f56f1f0acadaf2e7ee21872bca2949ba669fb58
# Fri, 06 Aug 2021 19:54:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 19:54:48 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 19:54:49 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 19:54:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 19:54:50 GMT
USER haproxy
# Fri, 06 Aug 2021 19:54:50 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4ee0caa23b369b04827640a4be298bf4ff7bacd030c77e915f5d7fb8f987594a`  
		Last Modified: Fri, 06 Aug 2021 17:58:57 GMT  
		Size: 2.4 MB (2429359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548ff9918828f96cb9a5e5656ea589d79e6fb1d7b9f0d693feff2dbefc6929fe`  
		Last Modified: Fri, 06 Aug 2021 20:02:54 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3bdbccca052e226dbca2ad02ee174526e5507d8dcf197f6a72e755edd9e54c`  
		Last Modified: Fri, 06 Aug 2021 20:02:56 GMT  
		Size: 7.3 MB (7323888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04ef04986dda2aff0285ebdf1b1488621c619bc498e9848261c8264ab4fb248`  
		Last Modified: Fri, 06 Aug 2021 20:02:54 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.5-dev-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:d62ea64ae628d64590a9e8744416e80d9a570e634913d2aaac9a2aac8b2cc349
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10253110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8758d0cd9ef1393ec56f31648cedef4b7cf8a6bb2c5b7ba045d0df0f80be64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:39:26 GMT
ADD file:1a8fd1066485e1261462e689c1a072f010c1d3be904b73ef2b84128fac652951 in / 
# Fri, 06 Aug 2021 17:39:27 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:38:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 18:38:48 GMT
ENV HAPROXY_VERSION=2.5-dev3
# Fri, 06 Aug 2021 18:38:48 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev3.tar.gz
# Fri, 06 Aug 2021 18:38:48 GMT
ENV HAPROXY_SHA256=519343d7304f14701f6c1f7b1f56f1f0acadaf2e7ee21872bca2949ba669fb58
# Fri, 06 Aug 2021 18:39:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 18:39:48 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 18:39:49 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 18:39:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 18:39:49 GMT
USER haproxy
# Fri, 06 Aug 2021 18:39:49 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fd3acdcea5682abced546ec19fb6ebee725c5184e5d91614c469c0a79e67f2d0`  
		Last Modified: Fri, 06 Aug 2021 17:40:12 GMT  
		Size: 2.7 MB (2710613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a23793c1bba0796c0f469305ee92dd0f1cb8299963e4da4249d0f5aa2fcea0`  
		Last Modified: Fri, 06 Aug 2021 18:46:06 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67429a2ef77e845ec568db1e48bbb6b0809d95b52dbd4e142a946a31a947aaa5`  
		Last Modified: Fri, 06 Aug 2021 18:46:08 GMT  
		Size: 7.5 MB (7540854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30017115c5ac5bd4b280e4e103ac2ef38d7a31e1df6e8a49872e22ef8c80af10`  
		Last Modified: Fri, 06 Aug 2021 18:46:06 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.5-dev-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:cfeff4d341c21ccf18528aa5658d6283e91f5ccc59457f7f1faecaba0f4e88e8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10174385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3008d40e0ec4e2c1e6f59c3f0ae79003b03ef13ba90e34251fab55d9356230e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:38:26 GMT
ADD file:bafaec4a54d6cef99b5f3660d074a3d2251e4d4bd09df9ea65f33e9bffb7d88d in / 
# Fri, 06 Aug 2021 17:38:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:19:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:01:53 GMT
ENV HAPROXY_VERSION=2.5-dev4
# Tue, 17 Aug 2021 17:01:54 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev4.tar.gz
# Tue, 17 Aug 2021 17:01:54 GMT
ENV HAPROXY_SHA256=9ca0bff5255ccadb42834785097cd380694dc087af6f6556585a979ddf470966
# Tue, 17 Aug 2021 17:03:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 17:03:13 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:03:13 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:03:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:03:13 GMT
USER haproxy
# Tue, 17 Aug 2021 17:03:14 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:935703e1179e32e201e4a36d5664d58299dc8e7bcac197b70c295c0a59216db1`  
		Last Modified: Fri, 06 Aug 2021 17:39:15 GMT  
		Size: 2.8 MB (2821910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695b2822110160b402b8f359bb19d954a46a6ead94f868feba7d00f5a10e50e`  
		Last Modified: Fri, 06 Aug 2021 19:32:18 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd580785ea1e0addd0e97e48efae36397c70f72a3a2c1b98c71403db6bd970c0`  
		Last Modified: Tue, 17 Aug 2021 17:15:31 GMT  
		Size: 7.4 MB (7350830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3547da641f96b797d13a10d4fd37695081f64f4e80749aa314466f36a606fb25`  
		Last Modified: Tue, 17 Aug 2021 17:15:29 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.5-dev-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:a950426ef6638a2555b545cadbd9a911b4330377a1b63060dbb531dcc21c9c5c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10750856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff5846bf1179be59ec5c805a3789842d18fe1a64801f7d3f83003bdaeb7b0fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:17:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:42:27 GMT
ENV HAPROXY_VERSION=2.5-dev4
# Tue, 17 Aug 2021 16:42:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev4.tar.gz
# Tue, 17 Aug 2021 16:42:35 GMT
ENV HAPROXY_SHA256=9ca0bff5255ccadb42834785097cd380694dc087af6f6556585a979ddf470966
# Tue, 17 Aug 2021 16:43:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:43:20 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:43:22 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:43:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:43:29 GMT
USER haproxy
# Tue, 17 Aug 2021 16:43:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d374dad070e00fdb493e29a3aa64b375dbec801497e01d3b8ddbf7cc967634cb`  
		Last Modified: Fri, 06 Aug 2021 21:27:30 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095baff08b9d9c6c84330c36cd986846b91882fc2137f6cb4db9ba3ab72df6df`  
		Last Modified: Tue, 17 Aug 2021 17:04:04 GMT  
		Size: 7.9 MB (7938059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81ebad019d97bf2dca9500f25746e21adf6e31b6c0f7e82c79bac404b6bf23d`  
		Last Modified: Tue, 17 Aug 2021 17:04:02 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.5-dev-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:e72417786e6b2cd712168a5e7f30765f0d43c08862b357d56a5d89b9d6c8d552
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9899016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f7571e36d5cd7a81877a3a147bc540bab5011e63a020b3cbaa0d239961cc4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:54:24 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 14 May 2021 19:42:56 GMT
ENV HAPROXY_VERSION=2.5-dev0
# Fri, 14 May 2021 19:42:57 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev0.tar.gz
# Fri, 14 May 2021 19:42:57 GMT
ENV HAPROXY_SHA256=6ee45b5047649b2df3fd48f6659860e8845d970bd4e0c1764490a54c3047bd23
# Fri, 14 May 2021 19:43:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 14 May 2021 19:43:53 GMT
STOPSIGNAL SIGUSR1
# Fri, 14 May 2021 19:43:53 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 14 May 2021 19:43:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 May 2021 19:43:54 GMT
USER haproxy
# Fri, 14 May 2021 19:43:55 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267275aba58470c82626189a59be76cd169bd245568e2f2545ed1ee64ff8a8ff`  
		Last Modified: Wed, 14 Apr 2021 20:59:06 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b79e3a1c3d9c059731828093ca4846dfff4ba8ad68671e62fa5d5df56590563`  
		Last Modified: Fri, 14 May 2021 19:47:45 GMT  
		Size: 7.3 MB (7294732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9093b846e5e13ecfca4b82d2d45fd7bdc1c0d026e4fbc93faf64e9d450f9b485`  
		Last Modified: Fri, 14 May 2021 19:47:43 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.5-dev4`

```console
$ docker pull haproxy@sha256:a04e4bd6a47a08e6d157066813ff9debb0268296dd03a8124288262314fdbb0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le

### `haproxy:2.5-dev4` - linux; amd64

```console
$ docker pull haproxy@sha256:8331a9fda117416fcdaf09c5d2eefd4cee0e8b2379b38472e40d036f6bd2e78f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37486116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2eaccbe4c9c8b2ef5edfb5e6e8da6788182948341e98e841e5b132f5a4db4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 10:43:34 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:48:09 GMT
ENV HAPROXY_VERSION=2.5-dev4
# Tue, 17 Aug 2021 16:48:09 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev4.tar.gz
# Tue, 17 Aug 2021 16:48:09 GMT
ENV HAPROXY_SHA256=9ca0bff5255ccadb42834785097cd380694dc087af6f6556585a979ddf470966
# Tue, 17 Aug 2021 16:49:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:49:07 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:49:07 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:49:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:49:07 GMT
USER haproxy
# Tue, 17 Aug 2021 16:49:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd06683556254cbe06dad4624837c2dcbd2fec67c7fbdd057251f0a207a9315`  
		Last Modified: Tue, 17 Aug 2021 10:53:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92493dc602276088b8fb3304dae6649a52b726417b9dd6e697f9e8a6a644acc4`  
		Last Modified: Tue, 17 Aug 2021 17:00:05 GMT  
		Size: 10.3 MB (10338303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158cb2201f0691d9017fa2ddeb87fc7d70e46ce4ec8870ed6f9b0aa49e519366`  
		Last Modified: Tue, 17 Aug 2021 17:00:03 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.5-dev4` - linux; 386

```console
$ docker pull haproxy@sha256:8d4c68400cb20e02bd055c72ec551b3ab7beaff34eeee187228b02fea6dc93b2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37969826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f4ce7e1985625ae007420eaee2c186ed709fdacd0095c27847f19a040bb16c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:41:16 GMT
ADD file:0418032b55cd0a6dd515ac277fb9f92354397503cab212d446d3a3d8c647a60f in / 
# Tue, 17 Aug 2021 01:41:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 12:14:55 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:00:41 GMT
ENV HAPROXY_VERSION=2.5-dev4
# Tue, 17 Aug 2021 17:00:41 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev4.tar.gz
# Tue, 17 Aug 2021 17:00:41 GMT
ENV HAPROXY_SHA256=9ca0bff5255ccadb42834785097cd380694dc087af6f6556585a979ddf470966
# Tue, 17 Aug 2021 17:01:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 17:01:39 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:01:39 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:01:39 GMT
USER haproxy
# Tue, 17 Aug 2021 17:01:40 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c1c94e1f2523d69effaa463d64fc9962cfc67e2a956f0476c94200e7cf19edf0`  
		Last Modified: Tue, 17 Aug 2021 01:50:57 GMT  
		Size: 27.8 MB (27797627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f804b7c921abcc2fb2904ad2092beefd0224c9bd4cb1cf6477727e6f2bbd7599`  
		Last Modified: Tue, 17 Aug 2021 12:26:22 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81cbed7fc459541b845ad80b3aecadc67bf9d2fd9657eb35a6a54a7755ceb6b6`  
		Last Modified: Tue, 17 Aug 2021 17:15:14 GMT  
		Size: 10.2 MB (10170376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba8d74eedc7b3f631df44fa80b40eb4ea92dee537d14dc96f225161dc8139bd`  
		Last Modified: Tue, 17 Aug 2021 17:15:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.5-dev4` - linux; ppc64le

```console
$ docker pull haproxy@sha256:e70f6c7f808e6bc828fe716dd12ffdb3b5d4e1227368a0752b94cbe1b2f322ca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41419960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007076dc75f1416fb4689c0609533936e1165c881018c7668f33b6fa8f2aebe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:34:13 GMT
ADD file:8b9b12a994a2519f725d1ed1f4ab5a444665262678fd8e6c42cf78f32dacb7fa in / 
# Tue, 17 Aug 2021 01:34:20 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 13:36:19 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:38:31 GMT
ENV HAPROXY_VERSION=2.5-dev4
# Tue, 17 Aug 2021 16:38:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev4.tar.gz
# Tue, 17 Aug 2021 16:38:38 GMT
ENV HAPROXY_SHA256=9ca0bff5255ccadb42834785097cd380694dc087af6f6556585a979ddf470966
# Tue, 17 Aug 2021 16:41:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:41:59 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:42:02 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:42:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:42:07 GMT
USER haproxy
# Tue, 17 Aug 2021 16:42:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c3e09f0e3e7f6fcb741a4c9214b63e341e1d9b53d7689a5ad6ff640b61a82541`  
		Last Modified: Tue, 17 Aug 2021 01:48:22 GMT  
		Size: 30.6 MB (30553721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb7833dc31cf72935b478f7bf90e34f0f2a22d8260da177e4648ac973af1f9c`  
		Last Modified: Tue, 17 Aug 2021 14:24:41 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cbbd501c39cced7a73e666c66609762c53b6b9566703d6a9b703ccef228443`  
		Last Modified: Tue, 17 Aug 2021 17:03:51 GMT  
		Size: 10.9 MB (10864396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2105b9725ffa84427ffb73cd8482b1f3ff30b15d524f8b9426c561e05f0a4934`  
		Last Modified: Tue, 17 Aug 2021 17:03:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:2.5-dev4-alpine`

```console
$ docker pull haproxy@sha256:f171722075ccd1954b07f9a770c5e2f44df19828f4f8283adaad7243dc8a7f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; 386
	-	linux; ppc64le

### `haproxy:2.5-dev4-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:bb251766affec40e2cfcfa235aea22333e099e4ee0718105bd5a876d4908ea71
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c590cbef1ffd2647227e6c3b66fb761ae70743d676dce8b51d13e9e911cdd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:43:18 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:49:21 GMT
ENV HAPROXY_VERSION=2.5-dev4
# Tue, 17 Aug 2021 16:49:21 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev4.tar.gz
# Tue, 17 Aug 2021 16:49:21 GMT
ENV HAPROXY_SHA256=9ca0bff5255ccadb42834785097cd380694dc087af6f6556585a979ddf470966
# Tue, 17 Aug 2021 16:50:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:50:29 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:50:29 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:50:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:50:30 GMT
USER haproxy
# Tue, 17 Aug 2021 16:50:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22138861da3ab6ae8583cf62942545e1bb75874501f4a8d45d13a38c848a908`  
		Last Modified: Fri, 06 Aug 2021 19:51:27 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85446614356ec7bbcfbab89e23cfb3f3d9126325656da0426138d1098a6b5a02`  
		Last Modified: Tue, 17 Aug 2021 17:00:17 GMT  
		Size: 7.5 MB (7507193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a548f5b0d4b9592bf62f380b142326a1d5f667d495b33fa30da479067cdee2f`  
		Last Modified: Tue, 17 Aug 2021 17:00:15 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.5-dev4-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:ddfb376632d66f06de40f97d42dfa21a9baecb80b9a40251d70d11c995b7aa1b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10095130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8076668261692627f5e3a1191e24487ff2c571cc249ce6ab7525aca88e5a1801`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:49:32 GMT
ADD file:7f2c7deda009eabdcbbdccb11e854043d32c498e64e7e1ca02165d7bb4261d39 in / 
# Fri, 06 Aug 2021 17:49:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:15:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:36:13 GMT
ENV HAPROXY_VERSION=2.5-dev4
# Tue, 17 Aug 2021 16:36:13 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev4.tar.gz
# Tue, 17 Aug 2021 16:36:14 GMT
ENV HAPROXY_SHA256=9ca0bff5255ccadb42834785097cd380694dc087af6f6556585a979ddf470966
# Tue, 17 Aug 2021 16:36:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:36:42 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:36:43 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:36:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:36:44 GMT
USER haproxy
# Tue, 17 Aug 2021 16:36:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f465bb3e9fcd0c42f936ecc566c6e40353c00f3089b2b2c2ea1663c30f89d3ab`  
		Last Modified: Fri, 06 Aug 2021 17:51:00 GMT  
		Size: 2.6 MB (2626350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332ccafb58fe1d8ed3d3d5ad9c01adba33d922f28a398285d2eb67fed7c8bee8`  
		Last Modified: Fri, 06 Aug 2021 18:20:57 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8510845bd2c94130060bc6615c872643f4301e963871f5e78e2b993018a40ee`  
		Last Modified: Tue, 17 Aug 2021 16:41:09 GMT  
		Size: 7.5 MB (7467134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a12d2254dcc32b20bea441a3772db0a9153d270455e862a1675e572f95df03b`  
		Last Modified: Tue, 17 Aug 2021 16:41:04 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.5-dev4-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:cfeff4d341c21ccf18528aa5658d6283e91f5ccc59457f7f1faecaba0f4e88e8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10174385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3008d40e0ec4e2c1e6f59c3f0ae79003b03ef13ba90e34251fab55d9356230e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:38:26 GMT
ADD file:bafaec4a54d6cef99b5f3660d074a3d2251e4d4bd09df9ea65f33e9bffb7d88d in / 
# Fri, 06 Aug 2021 17:38:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:19:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:01:53 GMT
ENV HAPROXY_VERSION=2.5-dev4
# Tue, 17 Aug 2021 17:01:54 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev4.tar.gz
# Tue, 17 Aug 2021 17:01:54 GMT
ENV HAPROXY_SHA256=9ca0bff5255ccadb42834785097cd380694dc087af6f6556585a979ddf470966
# Tue, 17 Aug 2021 17:03:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 17:03:13 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:03:13 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:03:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:03:13 GMT
USER haproxy
# Tue, 17 Aug 2021 17:03:14 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:935703e1179e32e201e4a36d5664d58299dc8e7bcac197b70c295c0a59216db1`  
		Last Modified: Fri, 06 Aug 2021 17:39:15 GMT  
		Size: 2.8 MB (2821910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695b2822110160b402b8f359bb19d954a46a6ead94f868feba7d00f5a10e50e`  
		Last Modified: Fri, 06 Aug 2021 19:32:18 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd580785ea1e0addd0e97e48efae36397c70f72a3a2c1b98c71403db6bd970c0`  
		Last Modified: Tue, 17 Aug 2021 17:15:31 GMT  
		Size: 7.4 MB (7350830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3547da641f96b797d13a10d4fd37695081f64f4e80749aa314466f36a606fb25`  
		Last Modified: Tue, 17 Aug 2021 17:15:29 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:2.5-dev4-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:a950426ef6638a2555b545cadbd9a911b4330377a1b63060dbb531dcc21c9c5c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10750856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff5846bf1179be59ec5c805a3789842d18fe1a64801f7d3f83003bdaeb7b0fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:17:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:42:27 GMT
ENV HAPROXY_VERSION=2.5-dev4
# Tue, 17 Aug 2021 16:42:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/devel/haproxy-2.5-dev4.tar.gz
# Tue, 17 Aug 2021 16:42:35 GMT
ENV HAPROXY_SHA256=9ca0bff5255ccadb42834785097cd380694dc087af6f6556585a979ddf470966
# Tue, 17 Aug 2021 16:43:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:43:20 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:43:22 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:43:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:43:29 GMT
USER haproxy
# Tue, 17 Aug 2021 16:43:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d374dad070e00fdb493e29a3aa64b375dbec801497e01d3b8ddbf7cc967634cb`  
		Last Modified: Fri, 06 Aug 2021 21:27:30 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095baff08b9d9c6c84330c36cd986846b91882fc2137f6cb4db9ba3ab72df6df`  
		Last Modified: Tue, 17 Aug 2021 17:04:04 GMT  
		Size: 7.9 MB (7938059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81ebad019d97bf2dca9500f25746e21adf6e31b6c0f7e82c79bac404b6bf23d`  
		Last Modified: Tue, 17 Aug 2021 17:04:02 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:alpine`

```console
$ docker pull haproxy@sha256:4456ce96d7a1a0f0db94739071949bbf9f1daaf7eabaaecf220599be5284e447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:2b51b9f7b11fd789be82b17272b8d50c03286b07533abdd2917b4f67b6c551b9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10134063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d615f803d0602d65618848a61a788ec68a0ade7335d9f67dcbc60a003f5a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:43:18 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:51:46 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 16:51:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 16:51:47 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 16:52:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:52:50 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:52:51 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:52:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:52:51 GMT
USER haproxy
# Tue, 17 Aug 2021 16:52:51 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22138861da3ab6ae8583cf62942545e1bb75874501f4a8d45d13a38c848a908`  
		Last Modified: Fri, 06 Aug 2021 19:51:27 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084a6fa47ea6c62e03b343daa72870da70e747dd19b31aa2cd7378f9cf6a0fd9`  
		Last Modified: Tue, 17 Aug 2021 17:00:45 GMT  
		Size: 7.3 MB (7319417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f71cfe692953ce9359c70a04664d75052fc519bcc90a2c5cb96123a9e55e35`  
		Last Modified: Tue, 17 Aug 2021 17:00:44 GMT  
		Size: 444.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:5858c663bfb65657c6aabc6688d710f0aa1924b0476411989f1b8265e1b030fe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9919310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697f662af8e6d0dcb3ef652dbbbae30b74994995f5964d3e2f9491ee980510c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:49:32 GMT
ADD file:7f2c7deda009eabdcbbdccb11e854043d32c498e64e7e1ca02165d7bb4261d39 in / 
# Fri, 06 Aug 2021 17:49:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:15:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:36:55 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 16:36:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 16:36:56 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 16:37:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:37:24 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:37:24 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:37:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:37:25 GMT
USER haproxy
# Tue, 17 Aug 2021 16:37:25 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f465bb3e9fcd0c42f936ecc566c6e40353c00f3089b2b2c2ea1663c30f89d3ab`  
		Last Modified: Fri, 06 Aug 2021 17:51:00 GMT  
		Size: 2.6 MB (2626350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332ccafb58fe1d8ed3d3d5ad9c01adba33d922f28a398285d2eb67fed7c8bee8`  
		Last Modified: Fri, 06 Aug 2021 18:20:57 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405b6f9f13b134ed6de3cf66afffe633c706556bc16fd88ef74043d17a48c54`  
		Last Modified: Tue, 17 Aug 2021 16:41:26 GMT  
		Size: 7.3 MB (7291312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a5b0fa7ec3ddc3c829f96564fdd519c09a290910b48469cc5fe28cc476ab21`  
		Last Modified: Tue, 17 Aug 2021 16:41:22 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:a95a2208dbe0d98814a817cc18b5f3a68422b64b02106d1ec761949d196b7b3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9632801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da47331a3ac424edd35992104629f17383106bda6b4bfd8f913f755a7a700ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:57:32 GMT
ADD file:3a35ff3ac0d80289d419a4d6d8319610c38e1936d296addafb9aaf506946230f in / 
# Fri, 06 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:54:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 19:55:20 GMT
ENV HAPROXY_VERSION=2.4.2
# Fri, 06 Aug 2021 19:55:20 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Fri, 06 Aug 2021 19:55:21 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Fri, 06 Aug 2021 19:56:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 19:56:04 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 19:56:05 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 19:56:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 19:56:07 GMT
USER haproxy
# Fri, 06 Aug 2021 19:56:08 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4ee0caa23b369b04827640a4be298bf4ff7bacd030c77e915f5d7fb8f987594a`  
		Last Modified: Fri, 06 Aug 2021 17:58:57 GMT  
		Size: 2.4 MB (2429359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548ff9918828f96cb9a5e5656ea589d79e6fb1d7b9f0d693feff2dbefc6929fe`  
		Last Modified: Fri, 06 Aug 2021 20:02:54 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b4da96d470a19a8480afc1577eca661b82235d415ce7acee35780bfdbed1b`  
		Last Modified: Fri, 06 Aug 2021 20:03:17 GMT  
		Size: 7.2 MB (7201797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2bf593e46ec3d6ef735a051c2da655872e82e7c811a9be8a9f4127f2d45ffbe`  
		Last Modified: Fri, 06 Aug 2021 20:03:15 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:d8f5c33bebd1828228ca0f3ec81f9cd2f27f44c9179694732e90e9ed533720bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10134877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f5d862f5f50a3173fd52922695ff763bd507483fc29cbe1b10d480f3cba710`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:39:26 GMT
ADD file:1a8fd1066485e1261462e689c1a072f010c1d3be904b73ef2b84128fac652951 in / 
# Fri, 06 Aug 2021 17:39:27 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:38:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 18:40:06 GMT
ENV HAPROXY_VERSION=2.4.2
# Fri, 06 Aug 2021 18:40:06 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Fri, 06 Aug 2021 18:40:06 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Fri, 06 Aug 2021 18:41:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 18:41:05 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 18:41:05 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 18:41:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 18:41:06 GMT
USER haproxy
# Fri, 06 Aug 2021 18:41:06 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fd3acdcea5682abced546ec19fb6ebee725c5184e5d91614c469c0a79e67f2d0`  
		Last Modified: Fri, 06 Aug 2021 17:40:12 GMT  
		Size: 2.7 MB (2710613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a23793c1bba0796c0f469305ee92dd0f1cb8299963e4da4249d0f5aa2fcea0`  
		Last Modified: Fri, 06 Aug 2021 18:46:06 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0169a9e4faea9eebd85152cc75662780750a945ac1632d8f332980a081224555`  
		Last Modified: Fri, 06 Aug 2021 18:46:23 GMT  
		Size: 7.4 MB (7422621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179faf353137636acdb95b716a1e9825d02900a111a3a742e6499b7b753a5bf3`  
		Last Modified: Fri, 06 Aug 2021 18:46:22 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine` - linux; 386

```console
$ docker pull haproxy@sha256:27057e7fc931ea635e2ca78a31c85fae8c7a5cae3f2a3011b1fe64a47d8408ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10003948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a803ff7d44673ff6a4fd6e673048cdcee2ac921b6bc8639ce0e46572eb09f90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:38:26 GMT
ADD file:bafaec4a54d6cef99b5f3660d074a3d2251e4d4bd09df9ea65f33e9bffb7d88d in / 
# Fri, 06 Aug 2021 17:38:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:19:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:04:33 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 17:04:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 17:04:34 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 17:05:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 17:05:57 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:05:57 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:05:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:05:57 GMT
USER haproxy
# Tue, 17 Aug 2021 17:05:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:935703e1179e32e201e4a36d5664d58299dc8e7bcac197b70c295c0a59216db1`  
		Last Modified: Fri, 06 Aug 2021 17:39:15 GMT  
		Size: 2.8 MB (2821910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695b2822110160b402b8f359bb19d954a46a6ead94f868feba7d00f5a10e50e`  
		Last Modified: Fri, 06 Aug 2021 19:32:18 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d209c067bdfff48477adac6f34b7786f8d8f1d13d1a4b8dd7d70cf7d67ce246`  
		Last Modified: Tue, 17 Aug 2021 17:16:05 GMT  
		Size: 7.2 MB (7180394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb4e0881c29decc18e87cfb212fab9c4066e818a6ad45d14a818e82df909d3f`  
		Last Modified: Tue, 17 Aug 2021 17:16:03 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:875275a0ea30ad381d79d3af91d8046a2e262886b3c89f568b9733e5fbb200b8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10559704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893d2d1de6e4528ad75aa23fbe6fdc87edb44098071fb262cd4dbe51f32c4898`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:17:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:48:04 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 16:48:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 16:48:09 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 16:48:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:48:54 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:48:55 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:48:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:48:58 GMT
USER haproxy
# Tue, 17 Aug 2021 16:49:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d374dad070e00fdb493e29a3aa64b375dbec801497e01d3b8ddbf7cc967634cb`  
		Last Modified: Fri, 06 Aug 2021 21:27:30 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6b7fbbf87c5c7cc03966a6a0c19b891ca8a793a9a70ac80066e9d1240b2943`  
		Last Modified: Tue, 17 Aug 2021 17:04:38 GMT  
		Size: 7.7 MB (7746906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d439e35aac99cbbb58f67662da81ed697e00d547171fc923ea5d472e85334c1b`  
		Last Modified: Tue, 17 Aug 2021 17:04:36 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:67c77b2f75cda356f4462fa8c7cfe05d80b220bb7e3ddff6782557ca308381e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9899025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8353b377710bdcc56a8dd1fcdf4213b83d4378a795634015c8ec0817188591f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:54:24 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 14 May 2021 19:45:22 GMT
ENV HAPROXY_VERSION=2.4.0
# Fri, 14 May 2021 19:45:23 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.0.tar.gz
# Fri, 14 May 2021 19:45:23 GMT
ENV HAPROXY_SHA256=0a6962adaf5a1291db87e3eb4ddf906a72fed535dbd2255b164b7d8394a53640
# Fri, 14 May 2021 19:46:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 14 May 2021 19:46:14 GMT
STOPSIGNAL SIGUSR1
# Fri, 14 May 2021 19:46:14 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 14 May 2021 19:46:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 May 2021 19:46:15 GMT
USER haproxy
# Fri, 14 May 2021 19:46:15 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267275aba58470c82626189a59be76cd169bd245568e2f2545ed1ee64ff8a8ff`  
		Last Modified: Wed, 14 Apr 2021 20:59:06 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1af9bde57dd624c224ba02793a7568cd9f00874c978ff5ab4d6bc0c32fdb81f`  
		Last Modified: Fri, 14 May 2021 19:48:00 GMT  
		Size: 7.3 MB (7294741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68dd09d54ba9406459ae1956173c0df96676de52e5a01f9392966e3493acae68`  
		Last Modified: Fri, 14 May 2021 19:47:59 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:latest`

```console
$ docker pull haproxy@sha256:cecd35804d56a8a939975969fbc3ee9c37c193e083d8cc8ee4daeb1817685fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:latest` - linux; amd64

```console
$ docker pull haproxy@sha256:be84aa6aa3e60de3ce38adeac6e6d0e01c428e0c02b0a0e7b6d1b42d0bf36a29
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37304052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06340012d09399fd0be90a29f16bc2b8041b9322e9095c6fceeed1aa2f6280cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 10:43:34 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:50:46 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 16:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 16:50:47 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 16:51:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:51:38 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:51:38 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:51:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:51:38 GMT
USER haproxy
# Tue, 17 Aug 2021 16:51:39 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd06683556254cbe06dad4624837c2dcbd2fec67c7fbdd057251f0a207a9315`  
		Last Modified: Tue, 17 Aug 2021 10:53:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341a1a625c8fa0015a85b943c2bc17495fb26b105d5b07b3911a65b0967ea4be`  
		Last Modified: Tue, 17 Aug 2021 17:00:29 GMT  
		Size: 10.2 MB (10156239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63116b577243ee3d88e09a144ffe2122ebb8f78d3ce8b3517e1d39116a9c876a`  
		Last Modified: Tue, 17 Aug 2021 17:00:27 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:97e3c0ac88ed687f305efc5594b62d705816eacfc4f020dc227b7fd597eaea97
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34665658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806dea6cff7a221452cd5f560e5d1868285d8bad11828f9829aaae3321769004`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:56:50 GMT
ADD file:f29260935f1f8b3eef5eb0d5e49dd4cf5370e8731a3f4006d6023724bce09601 in / 
# Tue, 17 Aug 2021 01:56:51 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:39:10 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:40:18 GMT
ENV HAPROXY_VERSION=2.4.2
# Tue, 17 Aug 2021 08:40:18 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Tue, 17 Aug 2021 08:40:18 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Tue, 17 Aug 2021 08:41:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:41:11 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:41:11 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:41:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:41:12 GMT
USER haproxy
# Tue, 17 Aug 2021 08:41:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3dfab4a5b2accf2d709d8c7d14a42715948ecf2d6da4943a6e2c0de8ae7536a0`  
		Last Modified: Tue, 17 Aug 2021 02:12:42 GMT  
		Size: 24.9 MB (24879063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeabbf4f2af3ef66d78a317a4b3a0704a061a5de2611c57b0bfc47b775c2ed8b`  
		Last Modified: Tue, 17 Aug 2021 08:48:10 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9334963a75defcb3be49971cfc877b033ec3d2bf1de44e045c275c0d073eaca`  
		Last Modified: Tue, 17 Aug 2021 08:48:34 GMT  
		Size: 9.8 MB (9784770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddb2411e6120b22278ec6af6dffa64c6a09ed8003d944d6cb75617adb49bb2b`  
		Last Modified: Tue, 17 Aug 2021 08:48:28 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:b6f52164624551033e34146068b12ad46dc5f50521597edf54fa63420d743bea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32372273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beacbf459983020fe4247401d4865851e217e32a61f750547345d46291811e89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 02:14:25 GMT
ADD file:ca8cc4b509e305fa07662fbf2234ed78f0056569f6ca047305dc02bcd60f1558 in / 
# Tue, 17 Aug 2021 02:14:26 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 16:10:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:11:49 GMT
ENV HAPROXY_VERSION=2.4.2
# Tue, 17 Aug 2021 16:11:49 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Tue, 17 Aug 2021 16:11:50 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Tue, 17 Aug 2021 16:12:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:12:38 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:12:38 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:12:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:12:39 GMT
USER haproxy
# Tue, 17 Aug 2021 16:12:40 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:13e3f03410ff211945a725435c13065288d48a8cb740f0530e7588012c2679a4`  
		Last Modified: Tue, 17 Aug 2021 02:30:58 GMT  
		Size: 22.7 MB (22746254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb366ce7907325b732435009125848fb9596a1afdb0f87a8703cdf4342e91a4e`  
		Last Modified: Tue, 17 Aug 2021 16:21:35 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d48315f84cbc9b259be6ccc1d3f0cdabd9261d5ce4839e9f76f5c2ce598320`  
		Last Modified: Tue, 17 Aug 2021 16:22:03 GMT  
		Size: 9.6 MB (9624194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977b73ceb84201298d39d7cf916f4f71ab6c67de8d72d2b2f16875ec8d53e664`  
		Last Modified: Tue, 17 Aug 2021 16:21:57 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:aa0d55c9008fbec2ae69f6d19cb2fe2635cc98db24e6c176f254a3bc600a414b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35942317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707f81868db5f80d178b0eacd35631c9921a4fc03eead614ef818c0a4f53264f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:12:02 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:12:58 GMT
ENV HAPROXY_VERSION=2.4.2
# Tue, 17 Aug 2021 08:12:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Tue, 17 Aug 2021 08:12:58 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Tue, 17 Aug 2021 08:13:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:13:41 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:13:41 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:13:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:13:41 GMT
USER haproxy
# Tue, 17 Aug 2021 08:13:41 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc63cf29191f59ddbc41452b9edbe5f8145c4370cd74d3981d50a862173029b`  
		Last Modified: Tue, 17 Aug 2021 08:19:14 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e000ae73340a93669fb008ccf0dc4d556cfe9a0890b24255a0579eac5309fea4`  
		Last Modified: Tue, 17 Aug 2021 08:19:30 GMT  
		Size: 10.0 MB (10025421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e374ae1b0bcaf5e3cb1c612705c13b7d3a6ea8415d2fe4d55432a771b4c402f`  
		Last Modified: Tue, 17 Aug 2021 08:19:28 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; 386

```console
$ docker pull haproxy@sha256:306a0b4ee5470c1cd79c83f83cb29aa61237f55d57a59b746b5df2d2c6ffb037
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37794662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc46e642c5ab3fe5dce635c0ce63dceab31a3f647517798a00710df71a57b80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:41:16 GMT
ADD file:0418032b55cd0a6dd515ac277fb9f92354397503cab212d446d3a3d8c647a60f in / 
# Tue, 17 Aug 2021 01:41:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 12:14:55 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:03:20 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 17:03:21 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 17:03:21 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 17:04:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 17:04:22 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:04:23 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:04:23 GMT
USER haproxy
# Tue, 17 Aug 2021 17:04:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c1c94e1f2523d69effaa463d64fc9962cfc67e2a956f0476c94200e7cf19edf0`  
		Last Modified: Tue, 17 Aug 2021 01:50:57 GMT  
		Size: 27.8 MB (27797627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f804b7c921abcc2fb2904ad2092beefd0224c9bd4cb1cf6477727e6f2bbd7599`  
		Last Modified: Tue, 17 Aug 2021 12:26:22 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439c6e37b7d0414cb74b21e0c06ffef78e3cfd0c5e80979da92ac57ba05eb3d2`  
		Last Modified: Tue, 17 Aug 2021 17:15:45 GMT  
		Size: 10.0 MB (9995212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4919e3d48d2fec06a9fd5cbd2be5dccd1863e31181aaf7fd52cb74e5e75526e4`  
		Last Modified: Tue, 17 Aug 2021 17:15:42 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; mips64le

```console
$ docker pull haproxy@sha256:25becba2c50de125a20ca6c807ca1144ae10be6a6a9158dca0bd72593b571e0b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35582885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffc7ee854b5982782d23d6545603aedf6f7f6cd813daae1401c39a4dcdcf88d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:12:26 GMT
ADD file:8bd279803ead4ddce8db90b65e89c423f84fbf6042bfbeae8c09486b2e884cde in / 
# Tue, 17 Aug 2021 01:12:27 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:10:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 14:13:15 GMT
ENV HAPROXY_VERSION=2.4.2
# Tue, 17 Aug 2021 14:13:16 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Tue, 17 Aug 2021 14:13:16 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Tue, 17 Aug 2021 14:15:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 14:15:44 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 14:15:45 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 14:15:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:15:45 GMT
USER haproxy
# Tue, 17 Aug 2021 14:15:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a711e3e37b88ef77496c07ed663bb4270ecba9057eba452a91cc9be0bafb9c32`  
		Last Modified: Tue, 17 Aug 2021 01:21:44 GMT  
		Size: 25.8 MB (25813007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac33edc8b81dffec584b1a7ca6a8abea967f70259323fc62ff423b9c01642e`  
		Last Modified: Tue, 17 Aug 2021 14:27:23 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d2df5d6eb229d0c56111f4ba8be6edc422b3933094da75e75da6adbe915d4b`  
		Last Modified: Tue, 17 Aug 2021 14:27:47 GMT  
		Size: 9.8 MB (9768050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6e2dc937ddf621c5676ff4261041f8e9916e2305e110856dac40b16ea69c93`  
		Last Modified: Tue, 17 Aug 2021 14:27:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; ppc64le

```console
$ docker pull haproxy@sha256:005c8f2d6acfbf16e77e74ba888f43c5d95d5382e6e421ac5bb2d3820ed267b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41217675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b559f13fdafa1906fb0123fa75d8350827717db10409d2860d0c3db414312e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:34:13 GMT
ADD file:8b9b12a994a2519f725d1ed1f4ab5a444665262678fd8e6c42cf78f32dacb7fa in / 
# Tue, 17 Aug 2021 01:34:20 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 13:36:19 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:43:54 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 16:44:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 16:44:07 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 16:47:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:47:30 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:47:34 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:47:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:47:41 GMT
USER haproxy
# Tue, 17 Aug 2021 16:47:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c3e09f0e3e7f6fcb741a4c9214b63e341e1d9b53d7689a5ad6ff640b61a82541`  
		Last Modified: Tue, 17 Aug 2021 01:48:22 GMT  
		Size: 30.6 MB (30553721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb7833dc31cf72935b478f7bf90e34f0f2a22d8260da177e4648ac973af1f9c`  
		Last Modified: Tue, 17 Aug 2021 14:24:41 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84b036d99ad375fba8e2862f8eecba0672b2addce066456d8f0af3d9dce36d2`  
		Last Modified: Tue, 17 Aug 2021 17:04:19 GMT  
		Size: 10.7 MB (10662112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec7ca3be675051e451993a6916eac7da569020d428bcf5f04ee244d006878a4`  
		Last Modified: Tue, 17 Aug 2021 17:04:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; s390x

```console
$ docker pull haproxy@sha256:3fa33eb62f823be6cff266718be3d9cf7e878075bc429c40d020ff51ca806a62
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35587952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b048110fe88e7fedfb39c5067e23dabd5387a4a39e2f07225995322b8333b434`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 07:18:12 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 07:19:41 GMT
ENV HAPROXY_VERSION=2.4.2
# Tue, 17 Aug 2021 07:19:42 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Tue, 17 Aug 2021 07:19:42 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Tue, 17 Aug 2021 07:20:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 07:20:28 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 07:20:29 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 07:20:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 07:20:30 GMT
USER haproxy
# Tue, 17 Aug 2021 07:20:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16a2f2a1452470a1d818d8d16934d08d2a57b312ceabcce8c1cfad6c99f00a2`  
		Last Modified: Tue, 17 Aug 2021 07:28:00 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc2a7c361fe340d5b70919c5991c098506bb6dd4e2ff6c8696c0135074b51fc`  
		Last Modified: Tue, 17 Aug 2021 07:28:12 GMT  
		Size: 9.8 MB (9825271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6304b5ba716e53c4d88c06c0d3564da13d2ab9cf06cb9ec72e3f70c902a5bb`  
		Last Modified: Tue, 17 Aug 2021 07:28:11 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:lts`

```console
$ docker pull haproxy@sha256:cecd35804d56a8a939975969fbc3ee9c37c193e083d8cc8ee4daeb1817685fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:lts` - linux; amd64

```console
$ docker pull haproxy@sha256:be84aa6aa3e60de3ce38adeac6e6d0e01c428e0c02b0a0e7b6d1b42d0bf36a29
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37304052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06340012d09399fd0be90a29f16bc2b8041b9322e9095c6fceeed1aa2f6280cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 10:43:34 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:50:46 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 16:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 16:50:47 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 16:51:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:51:38 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:51:38 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:51:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:51:38 GMT
USER haproxy
# Tue, 17 Aug 2021 16:51:39 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd06683556254cbe06dad4624837c2dcbd2fec67c7fbdd057251f0a207a9315`  
		Last Modified: Tue, 17 Aug 2021 10:53:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341a1a625c8fa0015a85b943c2bc17495fb26b105d5b07b3911a65b0967ea4be`  
		Last Modified: Tue, 17 Aug 2021 17:00:29 GMT  
		Size: 10.2 MB (10156239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63116b577243ee3d88e09a144ffe2122ebb8f78d3ce8b3517e1d39116a9c876a`  
		Last Modified: Tue, 17 Aug 2021 17:00:27 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:97e3c0ac88ed687f305efc5594b62d705816eacfc4f020dc227b7fd597eaea97
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34665658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806dea6cff7a221452cd5f560e5d1868285d8bad11828f9829aaae3321769004`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:56:50 GMT
ADD file:f29260935f1f8b3eef5eb0d5e49dd4cf5370e8731a3f4006d6023724bce09601 in / 
# Tue, 17 Aug 2021 01:56:51 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:39:10 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:40:18 GMT
ENV HAPROXY_VERSION=2.4.2
# Tue, 17 Aug 2021 08:40:18 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Tue, 17 Aug 2021 08:40:18 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Tue, 17 Aug 2021 08:41:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:41:11 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:41:11 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:41:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:41:12 GMT
USER haproxy
# Tue, 17 Aug 2021 08:41:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3dfab4a5b2accf2d709d8c7d14a42715948ecf2d6da4943a6e2c0de8ae7536a0`  
		Last Modified: Tue, 17 Aug 2021 02:12:42 GMT  
		Size: 24.9 MB (24879063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeabbf4f2af3ef66d78a317a4b3a0704a061a5de2611c57b0bfc47b775c2ed8b`  
		Last Modified: Tue, 17 Aug 2021 08:48:10 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9334963a75defcb3be49971cfc877b033ec3d2bf1de44e045c275c0d073eaca`  
		Last Modified: Tue, 17 Aug 2021 08:48:34 GMT  
		Size: 9.8 MB (9784770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddb2411e6120b22278ec6af6dffa64c6a09ed8003d944d6cb75617adb49bb2b`  
		Last Modified: Tue, 17 Aug 2021 08:48:28 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:b6f52164624551033e34146068b12ad46dc5f50521597edf54fa63420d743bea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32372273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beacbf459983020fe4247401d4865851e217e32a61f750547345d46291811e89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 02:14:25 GMT
ADD file:ca8cc4b509e305fa07662fbf2234ed78f0056569f6ca047305dc02bcd60f1558 in / 
# Tue, 17 Aug 2021 02:14:26 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 16:10:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:11:49 GMT
ENV HAPROXY_VERSION=2.4.2
# Tue, 17 Aug 2021 16:11:49 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Tue, 17 Aug 2021 16:11:50 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Tue, 17 Aug 2021 16:12:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:12:38 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:12:38 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:12:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:12:39 GMT
USER haproxy
# Tue, 17 Aug 2021 16:12:40 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:13e3f03410ff211945a725435c13065288d48a8cb740f0530e7588012c2679a4`  
		Last Modified: Tue, 17 Aug 2021 02:30:58 GMT  
		Size: 22.7 MB (22746254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb366ce7907325b732435009125848fb9596a1afdb0f87a8703cdf4342e91a4e`  
		Last Modified: Tue, 17 Aug 2021 16:21:35 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d48315f84cbc9b259be6ccc1d3f0cdabd9261d5ce4839e9f76f5c2ce598320`  
		Last Modified: Tue, 17 Aug 2021 16:22:03 GMT  
		Size: 9.6 MB (9624194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977b73ceb84201298d39d7cf916f4f71ab6c67de8d72d2b2f16875ec8d53e664`  
		Last Modified: Tue, 17 Aug 2021 16:21:57 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:aa0d55c9008fbec2ae69f6d19cb2fe2635cc98db24e6c176f254a3bc600a414b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35942317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707f81868db5f80d178b0eacd35631c9921a4fc03eead614ef818c0a4f53264f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:12:02 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 08:12:58 GMT
ENV HAPROXY_VERSION=2.4.2
# Tue, 17 Aug 2021 08:12:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Tue, 17 Aug 2021 08:12:58 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Tue, 17 Aug 2021 08:13:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 08:13:41 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 08:13:41 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 08:13:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 08:13:41 GMT
USER haproxy
# Tue, 17 Aug 2021 08:13:41 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc63cf29191f59ddbc41452b9edbe5f8145c4370cd74d3981d50a862173029b`  
		Last Modified: Tue, 17 Aug 2021 08:19:14 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e000ae73340a93669fb008ccf0dc4d556cfe9a0890b24255a0579eac5309fea4`  
		Last Modified: Tue, 17 Aug 2021 08:19:30 GMT  
		Size: 10.0 MB (10025421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e374ae1b0bcaf5e3cb1c612705c13b7d3a6ea8415d2fe4d55432a771b4c402f`  
		Last Modified: Tue, 17 Aug 2021 08:19:28 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; 386

```console
$ docker pull haproxy@sha256:306a0b4ee5470c1cd79c83f83cb29aa61237f55d57a59b746b5df2d2c6ffb037
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37794662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc46e642c5ab3fe5dce635c0ce63dceab31a3f647517798a00710df71a57b80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:41:16 GMT
ADD file:0418032b55cd0a6dd515ac277fb9f92354397503cab212d446d3a3d8c647a60f in / 
# Tue, 17 Aug 2021 01:41:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 12:14:55 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:03:20 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 17:03:21 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 17:03:21 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 17:04:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 17:04:22 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:04:23 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:04:23 GMT
USER haproxy
# Tue, 17 Aug 2021 17:04:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c1c94e1f2523d69effaa463d64fc9962cfc67e2a956f0476c94200e7cf19edf0`  
		Last Modified: Tue, 17 Aug 2021 01:50:57 GMT  
		Size: 27.8 MB (27797627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f804b7c921abcc2fb2904ad2092beefd0224c9bd4cb1cf6477727e6f2bbd7599`  
		Last Modified: Tue, 17 Aug 2021 12:26:22 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439c6e37b7d0414cb74b21e0c06ffef78e3cfd0c5e80979da92ac57ba05eb3d2`  
		Last Modified: Tue, 17 Aug 2021 17:15:45 GMT  
		Size: 10.0 MB (9995212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4919e3d48d2fec06a9fd5cbd2be5dccd1863e31181aaf7fd52cb74e5e75526e4`  
		Last Modified: Tue, 17 Aug 2021 17:15:42 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; mips64le

```console
$ docker pull haproxy@sha256:25becba2c50de125a20ca6c807ca1144ae10be6a6a9158dca0bd72593b571e0b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35582885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffc7ee854b5982782d23d6545603aedf6f7f6cd813daae1401c39a4dcdcf88d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:12:26 GMT
ADD file:8bd279803ead4ddce8db90b65e89c423f84fbf6042bfbeae8c09486b2e884cde in / 
# Tue, 17 Aug 2021 01:12:27 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:10:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 14:13:15 GMT
ENV HAPROXY_VERSION=2.4.2
# Tue, 17 Aug 2021 14:13:16 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Tue, 17 Aug 2021 14:13:16 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Tue, 17 Aug 2021 14:15:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 14:15:44 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 14:15:45 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 14:15:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:15:45 GMT
USER haproxy
# Tue, 17 Aug 2021 14:15:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a711e3e37b88ef77496c07ed663bb4270ecba9057eba452a91cc9be0bafb9c32`  
		Last Modified: Tue, 17 Aug 2021 01:21:44 GMT  
		Size: 25.8 MB (25813007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac33edc8b81dffec584b1a7ca6a8abea967f70259323fc62ff423b9c01642e`  
		Last Modified: Tue, 17 Aug 2021 14:27:23 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d2df5d6eb229d0c56111f4ba8be6edc422b3933094da75e75da6adbe915d4b`  
		Last Modified: Tue, 17 Aug 2021 14:27:47 GMT  
		Size: 9.8 MB (9768050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6e2dc937ddf621c5676ff4261041f8e9916e2305e110856dac40b16ea69c93`  
		Last Modified: Tue, 17 Aug 2021 14:27:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; ppc64le

```console
$ docker pull haproxy@sha256:005c8f2d6acfbf16e77e74ba888f43c5d95d5382e6e421ac5bb2d3820ed267b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41217675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b559f13fdafa1906fb0123fa75d8350827717db10409d2860d0c3db414312e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:34:13 GMT
ADD file:8b9b12a994a2519f725d1ed1f4ab5a444665262678fd8e6c42cf78f32dacb7fa in / 
# Tue, 17 Aug 2021 01:34:20 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 13:36:19 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:43:54 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 16:44:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 16:44:07 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 16:47:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 16:47:30 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:47:34 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:47:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:47:41 GMT
USER haproxy
# Tue, 17 Aug 2021 16:47:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c3e09f0e3e7f6fcb741a4c9214b63e341e1d9b53d7689a5ad6ff640b61a82541`  
		Last Modified: Tue, 17 Aug 2021 01:48:22 GMT  
		Size: 30.6 MB (30553721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb7833dc31cf72935b478f7bf90e34f0f2a22d8260da177e4648ac973af1f9c`  
		Last Modified: Tue, 17 Aug 2021 14:24:41 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84b036d99ad375fba8e2862f8eecba0672b2addce066456d8f0af3d9dce36d2`  
		Last Modified: Tue, 17 Aug 2021 17:04:19 GMT  
		Size: 10.7 MB (10662112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec7ca3be675051e451993a6916eac7da569020d428bcf5f04ee244d006878a4`  
		Last Modified: Tue, 17 Aug 2021 17:04:17 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; s390x

```console
$ docker pull haproxy@sha256:3fa33eb62f823be6cff266718be3d9cf7e878075bc429c40d020ff51ca806a62
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35587952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b048110fe88e7fedfb39c5067e23dabd5387a4a39e2f07225995322b8333b434`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 07:18:12 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 07:19:41 GMT
ENV HAPROXY_VERSION=2.4.2
# Tue, 17 Aug 2021 07:19:42 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Tue, 17 Aug 2021 07:19:42 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Tue, 17 Aug 2021 07:20:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 17 Aug 2021 07:20:28 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 07:20:29 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 07:20:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 07:20:30 GMT
USER haproxy
# Tue, 17 Aug 2021 07:20:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16a2f2a1452470a1d818d8d16934d08d2a57b312ceabcce8c1cfad6c99f00a2`  
		Last Modified: Tue, 17 Aug 2021 07:28:00 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc2a7c361fe340d5b70919c5991c098506bb6dd4e2ff6c8696c0135074b51fc`  
		Last Modified: Tue, 17 Aug 2021 07:28:12 GMT  
		Size: 9.8 MB (9825271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6304b5ba716e53c4d88c06c0d3564da13d2ab9cf06cb9ec72e3f70c902a5bb`  
		Last Modified: Tue, 17 Aug 2021 07:28:11 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haproxy:lts-alpine`

```console
$ docker pull haproxy@sha256:4456ce96d7a1a0f0db94739071949bbf9f1daaf7eabaaecf220599be5284e447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:lts-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:2b51b9f7b11fd789be82b17272b8d50c03286b07533abdd2917b4f67b6c551b9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10134063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d615f803d0602d65618848a61a788ec68a0ade7335d9f67dcbc60a003f5a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:43:18 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:51:46 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 16:51:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 16:51:47 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 16:52:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:52:50 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:52:51 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:52:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:52:51 GMT
USER haproxy
# Tue, 17 Aug 2021 16:52:51 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22138861da3ab6ae8583cf62942545e1bb75874501f4a8d45d13a38c848a908`  
		Last Modified: Fri, 06 Aug 2021 19:51:27 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084a6fa47ea6c62e03b343daa72870da70e747dd19b31aa2cd7378f9cf6a0fd9`  
		Last Modified: Tue, 17 Aug 2021 17:00:45 GMT  
		Size: 7.3 MB (7319417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f71cfe692953ce9359c70a04664d75052fc519bcc90a2c5cb96123a9e55e35`  
		Last Modified: Tue, 17 Aug 2021 17:00:44 GMT  
		Size: 444.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:5858c663bfb65657c6aabc6688d710f0aa1924b0476411989f1b8265e1b030fe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9919310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697f662af8e6d0dcb3ef652dbbbae30b74994995f5964d3e2f9491ee980510c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:49:32 GMT
ADD file:7f2c7deda009eabdcbbdccb11e854043d32c498e64e7e1ca02165d7bb4261d39 in / 
# Fri, 06 Aug 2021 17:49:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:15:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:36:55 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 16:36:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 16:36:56 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 16:37:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:37:24 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:37:24 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:37:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:37:25 GMT
USER haproxy
# Tue, 17 Aug 2021 16:37:25 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f465bb3e9fcd0c42f936ecc566c6e40353c00f3089b2b2c2ea1663c30f89d3ab`  
		Last Modified: Fri, 06 Aug 2021 17:51:00 GMT  
		Size: 2.6 MB (2626350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332ccafb58fe1d8ed3d3d5ad9c01adba33d922f28a398285d2eb67fed7c8bee8`  
		Last Modified: Fri, 06 Aug 2021 18:20:57 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405b6f9f13b134ed6de3cf66afffe633c706556bc16fd88ef74043d17a48c54`  
		Last Modified: Tue, 17 Aug 2021 16:41:26 GMT  
		Size: 7.3 MB (7291312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a5b0fa7ec3ddc3c829f96564fdd519c09a290910b48469cc5fe28cc476ab21`  
		Last Modified: Tue, 17 Aug 2021 16:41:22 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:a95a2208dbe0d98814a817cc18b5f3a68422b64b02106d1ec761949d196b7b3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9632801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da47331a3ac424edd35992104629f17383106bda6b4bfd8f913f755a7a700ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:57:32 GMT
ADD file:3a35ff3ac0d80289d419a4d6d8319610c38e1936d296addafb9aaf506946230f in / 
# Fri, 06 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:54:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 19:55:20 GMT
ENV HAPROXY_VERSION=2.4.2
# Fri, 06 Aug 2021 19:55:20 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Fri, 06 Aug 2021 19:55:21 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Fri, 06 Aug 2021 19:56:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 19:56:04 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 19:56:05 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 19:56:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 19:56:07 GMT
USER haproxy
# Fri, 06 Aug 2021 19:56:08 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4ee0caa23b369b04827640a4be298bf4ff7bacd030c77e915f5d7fb8f987594a`  
		Last Modified: Fri, 06 Aug 2021 17:58:57 GMT  
		Size: 2.4 MB (2429359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548ff9918828f96cb9a5e5656ea589d79e6fb1d7b9f0d693feff2dbefc6929fe`  
		Last Modified: Fri, 06 Aug 2021 20:02:54 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b4da96d470a19a8480afc1577eca661b82235d415ce7acee35780bfdbed1b`  
		Last Modified: Fri, 06 Aug 2021 20:03:17 GMT  
		Size: 7.2 MB (7201797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2bf593e46ec3d6ef735a051c2da655872e82e7c811a9be8a9f4127f2d45ffbe`  
		Last Modified: Fri, 06 Aug 2021 20:03:15 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:d8f5c33bebd1828228ca0f3ec81f9cd2f27f44c9179694732e90e9ed533720bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10134877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f5d862f5f50a3173fd52922695ff763bd507483fc29cbe1b10d480f3cba710`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:39:26 GMT
ADD file:1a8fd1066485e1261462e689c1a072f010c1d3be904b73ef2b84128fac652951 in / 
# Fri, 06 Aug 2021 17:39:27 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 18:38:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 06 Aug 2021 18:40:06 GMT
ENV HAPROXY_VERSION=2.4.2
# Fri, 06 Aug 2021 18:40:06 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.2.tar.gz
# Fri, 06 Aug 2021 18:40:06 GMT
ENV HAPROXY_SHA256=edf9788f7f3411498e3d7b21777036b4dc14183e95c8e2ce7577baa0ea4ea2aa
# Fri, 06 Aug 2021 18:41:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 06 Aug 2021 18:41:05 GMT
STOPSIGNAL SIGUSR1
# Fri, 06 Aug 2021 18:41:05 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 06 Aug 2021 18:41:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 18:41:06 GMT
USER haproxy
# Fri, 06 Aug 2021 18:41:06 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fd3acdcea5682abced546ec19fb6ebee725c5184e5d91614c469c0a79e67f2d0`  
		Last Modified: Fri, 06 Aug 2021 17:40:12 GMT  
		Size: 2.7 MB (2710613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a23793c1bba0796c0f469305ee92dd0f1cb8299963e4da4249d0f5aa2fcea0`  
		Last Modified: Fri, 06 Aug 2021 18:46:06 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0169a9e4faea9eebd85152cc75662780750a945ac1632d8f332980a081224555`  
		Last Modified: Fri, 06 Aug 2021 18:46:23 GMT  
		Size: 7.4 MB (7422621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179faf353137636acdb95b716a1e9825d02900a111a3a742e6499b7b753a5bf3`  
		Last Modified: Fri, 06 Aug 2021 18:46:22 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:27057e7fc931ea635e2ca78a31c85fae8c7a5cae3f2a3011b1fe64a47d8408ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10003948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a803ff7d44673ff6a4fd6e673048cdcee2ac921b6bc8639ce0e46572eb09f90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 17:38:26 GMT
ADD file:bafaec4a54d6cef99b5f3660d074a3d2251e4d4bd09df9ea65f33e9bffb7d88d in / 
# Fri, 06 Aug 2021 17:38:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:19:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 17:04:33 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 17:04:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 17:04:34 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 17:05:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 17:05:57 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 17:05:57 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 17:05:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 17:05:57 GMT
USER haproxy
# Tue, 17 Aug 2021 17:05:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:935703e1179e32e201e4a36d5664d58299dc8e7bcac197b70c295c0a59216db1`  
		Last Modified: Fri, 06 Aug 2021 17:39:15 GMT  
		Size: 2.8 MB (2821910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695b2822110160b402b8f359bb19d954a46a6ead94f868feba7d00f5a10e50e`  
		Last Modified: Fri, 06 Aug 2021 19:32:18 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d209c067bdfff48477adac6f34b7786f8d8f1d13d1a4b8dd7d70cf7d67ce246`  
		Last Modified: Tue, 17 Aug 2021 17:16:05 GMT  
		Size: 7.2 MB (7180394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb4e0881c29decc18e87cfb212fab9c4066e818a6ad45d14a818e82df909d3f`  
		Last Modified: Tue, 17 Aug 2021 17:16:03 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:875275a0ea30ad381d79d3af91d8046a2e262886b3c89f568b9733e5fbb200b8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10559704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893d2d1de6e4528ad75aa23fbe6fdc87edb44098071fb262cd4dbe51f32c4898`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:17:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Tue, 17 Aug 2021 16:48:04 GMT
ENV HAPROXY_VERSION=2.4.3
# Tue, 17 Aug 2021 16:48:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.3.tar.gz
# Tue, 17 Aug 2021 16:48:09 GMT
ENV HAPROXY_SHA256=ce479380be5464faa881dcd829618931b60130ffeb01c88bc2bf95e230046405
# Tue, 17 Aug 2021 16:48:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Tue, 17 Aug 2021 16:48:54 GMT
STOPSIGNAL SIGUSR1
# Tue, 17 Aug 2021 16:48:55 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 17 Aug 2021 16:48:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 16:48:58 GMT
USER haproxy
# Tue, 17 Aug 2021 16:49:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d374dad070e00fdb493e29a3aa64b375dbec801497e01d3b8ddbf7cc967634cb`  
		Last Modified: Fri, 06 Aug 2021 21:27:30 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6b7fbbf87c5c7cc03966a6a0c19b891ca8a793a9a70ac80066e9d1240b2943`  
		Last Modified: Tue, 17 Aug 2021 17:04:38 GMT  
		Size: 7.7 MB (7746906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d439e35aac99cbbb58f67662da81ed697e00d547171fc923ea5d472e85334c1b`  
		Last Modified: Tue, 17 Aug 2021 17:04:36 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:67c77b2f75cda356f4462fa8c7cfe05d80b220bb7e3ddff6782557ca308381e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9899025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8353b377710bdcc56a8dd1fcdf4213b83d4378a795634015c8ec0817188591f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:54:24 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Fri, 14 May 2021 19:45:22 GMT
ENV HAPROXY_VERSION=2.4.0
# Fri, 14 May 2021 19:45:23 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.0.tar.gz
# Fri, 14 May 2021 19:45:23 GMT
ENV HAPROXY_SHA256=0a6962adaf5a1291db87e3eb4ddf906a72fed535dbd2255b164b7d8394a53640
# Fri, 14 May 2021 19:46:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.3-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 LUA_LIB=/usr/lib/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v
# Fri, 14 May 2021 19:46:14 GMT
STOPSIGNAL SIGUSR1
# Fri, 14 May 2021 19:46:14 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 14 May 2021 19:46:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 May 2021 19:46:15 GMT
USER haproxy
# Fri, 14 May 2021 19:46:15 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267275aba58470c82626189a59be76cd169bd245568e2f2545ed1ee64ff8a8ff`  
		Last Modified: Wed, 14 Apr 2021 20:59:06 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1af9bde57dd624c224ba02793a7568cd9f00874c978ff5ab4d6bc0c32fdb81f`  
		Last Modified: Fri, 14 May 2021 19:48:00 GMT  
		Size: 7.3 MB (7294741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68dd09d54ba9406459ae1956173c0df96676de52e5a01f9392966e3493acae68`  
		Last Modified: Fri, 14 May 2021 19:47:59 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
