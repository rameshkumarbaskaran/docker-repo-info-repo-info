## `haproxy:bullseye`

```console
$ docker pull haproxy@sha256:8ea670f54141216570d33b91f8b59aa734ac26d1d39893afe8e532b02d817718
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

### `haproxy:bullseye` - linux; amd64

```console
$ docker pull haproxy@sha256:7500ec5f2288a855154b05f63262a832a52f52050f469c41b3a06fab29cbed80
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39262604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f62cf2dd2c9c3fbedf11c3986b4c2506e538822053d1e215c15f2e0d8e18838`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:29:06 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Thu, 02 Dec 2021 09:30:17 GMT
ENV HAPROXY_VERSION=2.5.0
# Thu, 02 Dec 2021 09:30:17 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/haproxy-2.5.0.tar.gz
# Thu, 02 Dec 2021 09:30:17 GMT
ENV HAPROXY_SHA256=16a5ed6256ca3670e41b76366a892b08485643204a3ce72b6e7a2d9a313aa225
# Thu, 02 Dec 2021 09:31:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Thu, 02 Dec 2021 09:31:12 GMT
STOPSIGNAL SIGUSR1
# Thu, 02 Dec 2021 09:31:12 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 02 Dec 2021 09:31:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 09:31:13 GMT
USER haproxy
# Thu, 02 Dec 2021 09:31:13 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59cb091950d0df66637a73f5f5b3ecabbbd01435710a2708c23919ddfdb155a5`  
		Last Modified: Thu, 02 Dec 2021 09:39:04 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5215a4b62398454a7c7f11ec32c9a0f2d6d76df288eaeaef5beb744bf820721a`  
		Last Modified: Thu, 02 Dec 2021 09:39:24 GMT  
		Size: 7.9 MB (7890499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d793bfb7e4cb376dd62388ad06a1f34b6f8788f3efe735a5b961fdf28787d19`  
		Last Modified: Thu, 02 Dec 2021 09:39:23 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:bullseye` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:808a22b4f0476f8e709382186bc12e306654e50a6e10a63dea5913047de79e02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36711335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85def0c52b8cb86cf3cc2ae297b30549aa86d2b2f98bec35a144f49c9d2f6c1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Dec 2021 01:50:31 GMT
ADD file:a3023f71bd93966e7db1419adda3ccde4fcc5e2e8cf58e7b13c51036ed5ff796 in / 
# Tue, 21 Dec 2021 01:50:32 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:32:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Tue, 21 Dec 2021 02:33:52 GMT
ENV HAPROXY_VERSION=2.5.0
# Tue, 21 Dec 2021 02:33:53 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/haproxy-2.5.0.tar.gz
# Tue, 21 Dec 2021 02:33:53 GMT
ENV HAPROXY_SHA256=16a5ed6256ca3670e41b76366a892b08485643204a3ce72b6e7a2d9a313aa225
# Tue, 21 Dec 2021 02:34:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 21 Dec 2021 02:34:50 GMT
STOPSIGNAL SIGUSR1
# Tue, 21 Dec 2021 02:34:50 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 21 Dec 2021 02:34:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Dec 2021 02:34:51 GMT
USER haproxy
# Tue, 21 Dec 2021 02:34:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:054429d0cf4038fef39a3b5eb6ce52f600f9a2cbb71a4fb3e95ecf9b2da62581`  
		Last Modified: Tue, 21 Dec 2021 02:05:52 GMT  
		Size: 28.9 MB (28900253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a82e188ee0a10f2ac52989c97a8fb79da2dd6539fc7cdac21779ebfa019702`  
		Last Modified: Tue, 21 Dec 2021 02:44:57 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db03b6ab5acd0ad74b1ea35b21cab1c311b09d0d69844ec90775b6f42dec3cc1`  
		Last Modified: Tue, 21 Dec 2021 02:45:26 GMT  
		Size: 7.8 MB (7809192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65dd57c006e5cca2d6a851ea34f4f41b078a07b404f2307dae02b18bbf348c8`  
		Last Modified: Tue, 21 Dec 2021 02:45:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:bullseye` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:eb3b026117be2ab29267e33c26c439a8dd97710b2e3c06b21b99da6fa18a7233
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34248518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fcbf2df2104d5c1eabf69f41dce7f43c4d9feba1e742a95212ecc070b97600c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 02 Dec 2021 09:05:17 GMT
ADD file:97ce5af9ff4fb4002733d5c402ddc01a13e765d31b85bb6525a7fa797b698e10 in / 
# Thu, 02 Dec 2021 09:05:17 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 15:20:08 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Thu, 02 Dec 2021 15:21:29 GMT
ENV HAPROXY_VERSION=2.5.0
# Thu, 02 Dec 2021 15:21:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/haproxy-2.5.0.tar.gz
# Thu, 02 Dec 2021 15:21:30 GMT
ENV HAPROXY_SHA256=16a5ed6256ca3670e41b76366a892b08485643204a3ce72b6e7a2d9a313aa225
# Thu, 02 Dec 2021 15:22:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Thu, 02 Dec 2021 15:22:22 GMT
STOPSIGNAL SIGUSR1
# Thu, 02 Dec 2021 15:22:22 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 02 Dec 2021 15:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 15:22:23 GMT
USER haproxy
# Thu, 02 Dec 2021 15:22:24 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ba82a1312e1efdcd1cc6eb31cd40358dcec180da31779dac399cba31bf3dc206`  
		Last Modified: Thu, 02 Dec 2021 09:21:03 GMT  
		Size: 26.6 MB (26573192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c792706ad7c9232a9ffa186bab6ef3ed426485ea33020c34fafb35a89beda1`  
		Last Modified: Thu, 02 Dec 2021 15:35:49 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e68a03a8642e2e38b6041555d4e260b4be07074f5e1539e3a8be5077c27952`  
		Last Modified: Thu, 02 Dec 2021 15:36:24 GMT  
		Size: 7.7 MB (7673441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad54ff43f5503007454c91dab56437f423f93a71e78b032cd31af6a20293b0f2`  
		Last Modified: Thu, 02 Dec 2021 15:36:20 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:bullseye` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:f3daa6397a101222805cc6f7c75fa7464c7af44a27162e426567d91da9aa9552
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37989281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478fc672c4d6da59ef4d92a1375eb48f11633d14e3d9e8d97d6fce7ba48816e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:23 GMT
ADD file:986f91febed4aa8e2072081ff8419d52ba2060510822e717086d3b3d9469e4d7 in / 
# Tue, 21 Dec 2021 01:42:24 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:28:02 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Tue, 21 Dec 2021 02:28:50 GMT
ENV HAPROXY_VERSION=2.5.0
# Tue, 21 Dec 2021 02:28:51 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/haproxy-2.5.0.tar.gz
# Tue, 21 Dec 2021 02:28:52 GMT
ENV HAPROXY_SHA256=16a5ed6256ca3670e41b76366a892b08485643204a3ce72b6e7a2d9a313aa225
# Tue, 21 Dec 2021 02:29:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 21 Dec 2021 02:29:20 GMT
STOPSIGNAL SIGUSR1
# Tue, 21 Dec 2021 02:29:22 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 21 Dec 2021 02:29:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Dec 2021 02:29:23 GMT
USER haproxy
# Tue, 21 Dec 2021 02:29:24 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:927a35006d93ea08499b57046904046d7926cd76fb17be193e3e74f56d634a08`  
		Last Modified: Tue, 21 Dec 2021 01:48:54 GMT  
		Size: 30.0 MB (30043793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56dbc5e4c8a6cbecec9e828908817a3a1d54a633cad6966e025afa3c66b06281`  
		Last Modified: Tue, 21 Dec 2021 02:36:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f177892cc2486cb408aa24dbcf85056339081b79f7c7a6b149fb21246ca3ae46`  
		Last Modified: Tue, 21 Dec 2021 02:36:37 GMT  
		Size: 7.9 MB (7943745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba86e74cb50b1cb22e62a9e5d06a8997bb0d9f7bc9c1f83be5cdc8c288a164bc`  
		Last Modified: Tue, 21 Dec 2021 02:36:35 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:bullseye` - linux; 386

```console
$ docker pull haproxy@sha256:c4a8afc207927d6a8248472681439e7eefa62c5e20ea9737dc19d963a3b448d7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (40046314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7840bd706f4deab0abac5386e5e512d2458c69cfa4ded9de3533f39d90efa36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 02 Dec 2021 02:39:54 GMT
ADD file:0284c10b06ba22560408e1e14c1147887f4302c79dba143277ece2e333d6dcbc in / 
# Thu, 02 Dec 2021 02:39:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 08:49:13 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Thu, 02 Dec 2021 08:51:31 GMT
ENV HAPROXY_VERSION=2.5.0
# Thu, 02 Dec 2021 08:51:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/haproxy-2.5.0.tar.gz
# Thu, 02 Dec 2021 08:51:32 GMT
ENV HAPROXY_SHA256=16a5ed6256ca3670e41b76366a892b08485643204a3ce72b6e7a2d9a313aa225
# Thu, 02 Dec 2021 08:52:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Thu, 02 Dec 2021 08:52:50 GMT
STOPSIGNAL SIGUSR1
# Thu, 02 Dec 2021 08:52:51 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 02 Dec 2021 08:52:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 08:52:51 GMT
USER haproxy
# Thu, 02 Dec 2021 08:52:51 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2df7932f17d752876c686aa22054692a38e88e182dd7b6a5cca7ffce4ffe6f84`  
		Last Modified: Thu, 02 Dec 2021 02:47:59 GMT  
		Size: 32.4 MB (32380814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a1028ff52ffee9271a8fb1e0ca56420454f6ee695939cadc916da9bdc09d5c`  
		Last Modified: Thu, 02 Dec 2021 09:05:42 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ed6552bbe9bbcc67a8653b1e2503ef368194d83ee8b9b69119c7f1d7af0143`  
		Last Modified: Thu, 02 Dec 2021 09:06:11 GMT  
		Size: 7.7 MB (7663619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f3b822cdd66cedd72b93cbb96f944a997497a5e59ae517293b898df6fd159c`  
		Last Modified: Thu, 02 Dec 2021 09:06:09 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:bullseye` - linux; mips64le

```console
$ docker pull haproxy@sha256:0976eb6969e7441b3edbbcbe20833921ab6ec7aa6690457401d54c32b33d1a6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37675524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a712f2fbf5542189f5892a6c54f7be4ea9648fa227558d932ce4272c412f55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 02 Dec 2021 03:09:10 GMT
ADD file:419aff162077eb16923c3ede6455ca86756a929a5a837bc6ac6b8dc67913503a in / 
# Thu, 02 Dec 2021 03:09:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 04:35:11 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Thu, 02 Dec 2021 04:37:54 GMT
ENV HAPROXY_VERSION=2.5.0
# Thu, 02 Dec 2021 04:37:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/haproxy-2.5.0.tar.gz
# Thu, 02 Dec 2021 04:37:55 GMT
ENV HAPROXY_SHA256=16a5ed6256ca3670e41b76366a892b08485643204a3ce72b6e7a2d9a313aa225
# Thu, 02 Dec 2021 04:40:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Thu, 02 Dec 2021 04:40:21 GMT
STOPSIGNAL SIGUSR1
# Thu, 02 Dec 2021 04:40:22 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 02 Dec 2021 04:40:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 04:40:22 GMT
USER haproxy
# Thu, 02 Dec 2021 04:40:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:df61fb15db6391af55d70bc3c0db3e9014438c81bf802619fb527221adf5e8a8`  
		Last Modified: Thu, 02 Dec 2021 03:17:58 GMT  
		Size: 29.6 MB (29630496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7b5307dd1d7b7b0bc1e2dbefc9cca068a4018f0063a7c9137b806da74938d1`  
		Last Modified: Thu, 02 Dec 2021 04:55:06 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971f656e4f6badcdd3c9b394ca8377a9c64c44e3d0784368d1cd9de363195524`  
		Last Modified: Thu, 02 Dec 2021 04:55:34 GMT  
		Size: 8.0 MB (8043167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79c056937f7ad736d49b682c8345ad54f46ad739abfc8d67020e0b59d05691f`  
		Last Modified: Thu, 02 Dec 2021 04:55:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:bullseye` - linux; ppc64le

```console
$ docker pull haproxy@sha256:ad40dc64617fdf3cbda1e37a6b39e37f65c528a06646e0d0bb22ca1246d7578a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43586679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cde2bbc6d90b8c721a2e30d4e5cd081da7d3e7654d92c95549e3971819c1a16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 02 Dec 2021 07:21:21 GMT
ADD file:81a93de7f5dcdbb9397c05b9b6bb7dc5a4742119d46faf929b4c6277b02be7a5 in / 
# Thu, 02 Dec 2021 07:21:25 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 13:00:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Thu, 02 Dec 2021 13:03:59 GMT
ENV HAPROXY_VERSION=2.5.0
# Thu, 02 Dec 2021 13:04:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/haproxy-2.5.0.tar.gz
# Thu, 02 Dec 2021 13:04:05 GMT
ENV HAPROXY_SHA256=16a5ed6256ca3670e41b76366a892b08485643204a3ce72b6e7a2d9a313aa225
# Thu, 02 Dec 2021 13:06:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Thu, 02 Dec 2021 13:06:47 GMT
STOPSIGNAL SIGUSR1
# Thu, 02 Dec 2021 13:06:48 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 02 Dec 2021 13:06:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 13:06:51 GMT
USER haproxy
# Thu, 02 Dec 2021 13:06:54 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8d46978b233ccedeaa1cbef7248b214991469fa922cc4fbf9916f9d0711d2d2e`  
		Last Modified: Thu, 02 Dec 2021 07:31:43 GMT  
		Size: 35.3 MB (35271379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2509fcb678201769c1c3a5c94a7023ebd77996fbe6ad55a72fb9bbf55de82a`  
		Last Modified: Thu, 02 Dec 2021 13:32:12 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0293aabdfb9c0e997bce1ebd8c49b892d0331390dc90428065c015e52d3565`  
		Last Modified: Thu, 02 Dec 2021 13:32:35 GMT  
		Size: 8.3 MB (8313409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9187cd6c644d7a80d6b16da696d2ca3fe7d4309daca87869f2e9131528f0ce0`  
		Last Modified: Thu, 02 Dec 2021 13:32:33 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:bullseye` - linux; s390x

```console
$ docker pull haproxy@sha256:3810310fb66db632ca5e63ffe44e0ada0a3404fb0bc4fafb67b5ff8738a4e9c0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37591081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a999eb9f84ee2e1bda10b6d4948d91e2f4525ef0de30ab1df614ad1ef2538`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:27 GMT
ADD file:c8a482d41bf09dfb6484bf2a6e38535bf0594d26dd6eedd5abde4e3cc811fa6c in / 
# Tue, 21 Dec 2021 01:42:29 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:58:50 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Tue, 21 Dec 2021 02:59:39 GMT
ENV HAPROXY_VERSION=2.5.0
# Tue, 21 Dec 2021 02:59:39 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.5/src/haproxy-2.5.0.tar.gz
# Tue, 21 Dec 2021 02:59:40 GMT
ENV HAPROXY_SHA256=16a5ed6256ca3670e41b76366a892b08485643204a3ce72b6e7a2d9a313aa225
# Tue, 21 Dec 2021 03:00:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 21 Dec 2021 03:00:09 GMT
STOPSIGNAL SIGUSR1
# Tue, 21 Dec 2021 03:00:09 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 21 Dec 2021 03:00:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Dec 2021 03:00:10 GMT
USER haproxy
# Tue, 21 Dec 2021 03:00:10 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:12562551722a758d23ceea9abcdc2bee737e38c8f62a0f3d3afb2cc2626c28b1`  
		Last Modified: Tue, 21 Dec 2021 01:48:15 GMT  
		Size: 29.6 MB (29641636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7e79e149705e44e56049543f2ba9d2b399145c3aad2c76b8e3ecdb94b39a2e`  
		Last Modified: Tue, 21 Dec 2021 03:06:58 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5df8540d3ee8e718721f573bacb19738bc4b82f5ca17ac0b58aef5a495f13d3`  
		Last Modified: Tue, 21 Dec 2021 03:07:15 GMT  
		Size: 7.9 MB (7947556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf7e94315bf406f98cfca6af5085c10381d0196ba2b0c3e40556d23340e460a`  
		Last Modified: Tue, 21 Dec 2021 03:07:14 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
