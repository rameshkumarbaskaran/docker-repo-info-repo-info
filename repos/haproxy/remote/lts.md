## `haproxy:lts`

```console
$ docker pull haproxy@sha256:996b7f46bac11d75766454f7a7efcfd4d196b598a6ca3435b7442c4f48a53ba0
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
$ docker pull haproxy@sha256:dcc5a8eb08d72ffb88141486c12f3e5d1bc54910b42baad9f81301b6b674f029
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39148033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f8d94144772e39abbc3d8a460247e2e159057c8ad7fb742888c28a27aabe9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:29:06 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Thu, 02 Dec 2021 09:31:29 GMT
ENV HAPROXY_VERSION=2.4.9
# Thu, 02 Dec 2021 09:31:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.9.tar.gz
# Thu, 02 Dec 2021 09:31:29 GMT
ENV HAPROXY_SHA256=d56c7fe3c5afedd1b9a19e1b7f8f954feaf50a9c2f205f99891043858b72a763
# Thu, 02 Dec 2021 09:32:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Thu, 02 Dec 2021 09:32:24 GMT
STOPSIGNAL SIGUSR1
# Thu, 02 Dec 2021 09:32:25 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 02 Dec 2021 09:32:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 09:32:25 GMT
USER haproxy
# Thu, 02 Dec 2021 09:32:25 GMT
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
	-	`sha256:0168dba37fb52ad4c44ecd21e95d0d62da4d6e583c03e0a1e8f6874aa1612524`  
		Last Modified: Thu, 02 Dec 2021 09:39:49 GMT  
		Size: 7.8 MB (7775926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593e75abaf10c9b3a50a17a70581e45688888df49770d137ccb4ef08a8f437c2`  
		Last Modified: Thu, 02 Dec 2021 09:39:48 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:5be6a9780a7f2c2a5d93bc06bbe24d7f4f2080eae4a2da90dd102684e8a989c3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36601463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dd5d02afc63bb70e12cc0a94731241fecc3758f483a0c8930b83d86459069c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 02 Dec 2021 02:50:37 GMT
ADD file:7debbdb237139cb08189976f79cfa64cfd71f5cc98dfb2f560b558acb5f7cec9 in / 
# Thu, 02 Dec 2021 02:50:38 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 04:09:50 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Thu, 02 Dec 2021 04:14:15 GMT
ENV HAPROXY_VERSION=2.4.9
# Thu, 02 Dec 2021 04:14:17 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.9.tar.gz
# Thu, 02 Dec 2021 04:14:18 GMT
ENV HAPROXY_SHA256=d56c7fe3c5afedd1b9a19e1b7f8f954feaf50a9c2f205f99891043858b72a763
# Thu, 02 Dec 2021 04:15:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Thu, 02 Dec 2021 04:16:00 GMT
STOPSIGNAL SIGUSR1
# Thu, 02 Dec 2021 04:16:01 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 02 Dec 2021 04:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 04:16:04 GMT
USER haproxy
# Thu, 02 Dec 2021 04:16:05 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c5e429166894878430c39748965935f89ffa957667340c3c8bd872418dbce663`  
		Last Modified: Thu, 02 Dec 2021 03:09:28 GMT  
		Size: 28.9 MB (28910824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f07c503385be22857dba85dad3dcb8bfa2ee5d137a7b048606b4e055aaa7251`  
		Last Modified: Thu, 02 Dec 2021 04:29:29 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c614fa56733fa7ccf6e6979c6297e221b8a4519a798eee66fcf9d158b4d37fb`  
		Last Modified: Thu, 02 Dec 2021 04:30:30 GMT  
		Size: 7.7 MB (7688752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f2cff0dec202d3368648d1a60a90cc0adf8a19f86b3ba31f28b34b04c35143`  
		Last Modified: Thu, 02 Dec 2021 04:30:25 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:06c3b1d7c11b252f4db349aac69de8964aa5a091a69446bf8b73d065a90cf63d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34126188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70eb6ad57c44c7b86d615baed65e2259ed77c59ac64a5de1384d149276b7f31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 02 Dec 2021 09:05:17 GMT
ADD file:97ce5af9ff4fb4002733d5c402ddc01a13e765d31b85bb6525a7fa797b698e10 in / 
# Thu, 02 Dec 2021 09:05:17 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 15:20:08 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Thu, 02 Dec 2021 15:22:54 GMT
ENV HAPROXY_VERSION=2.4.9
# Thu, 02 Dec 2021 15:22:54 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.9.tar.gz
# Thu, 02 Dec 2021 15:22:55 GMT
ENV HAPROXY_SHA256=d56c7fe3c5afedd1b9a19e1b7f8f954feaf50a9c2f205f99891043858b72a763
# Thu, 02 Dec 2021 15:23:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Thu, 02 Dec 2021 15:23:46 GMT
STOPSIGNAL SIGUSR1
# Thu, 02 Dec 2021 15:23:46 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 02 Dec 2021 15:23:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 15:23:47 GMT
USER haproxy
# Thu, 02 Dec 2021 15:23:47 GMT
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
	-	`sha256:6826efff394bbb5afff9d7e710c813a6e6b49b03fdcaed3cea3cb15cddd91e91`  
		Last Modified: Thu, 02 Dec 2021 15:37:05 GMT  
		Size: 7.6 MB (7551111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4836af058e1d4b126427d03862c155bfd53f9150f28483f13ab094e567845022`  
		Last Modified: Thu, 02 Dec 2021 15:37:01 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:43702f4caae041cb4d64b7102d1ae651e7d6835b0c5e95f0a9238a0c6fb1b6cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37897574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2c2c81111d761b695666cbeeee461da412b5d06c2758812cb44e0516651434`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:09 GMT
ADD file:002f2f7c6dc806b24b6c365882acd59d2b3d3fcec46d8fd99130b07a4575c88c in / 
# Thu, 02 Dec 2021 08:08:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 17:49:49 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Thu, 02 Dec 2021 17:51:27 GMT
ENV HAPROXY_VERSION=2.4.9
# Thu, 02 Dec 2021 17:51:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.9.tar.gz
# Thu, 02 Dec 2021 17:51:29 GMT
ENV HAPROXY_SHA256=d56c7fe3c5afedd1b9a19e1b7f8f954feaf50a9c2f205f99891043858b72a763
# Thu, 02 Dec 2021 17:51:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Thu, 02 Dec 2021 17:52:00 GMT
STOPSIGNAL SIGUSR1
# Thu, 02 Dec 2021 17:52:02 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 02 Dec 2021 17:52:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 17:52:03 GMT
USER haproxy
# Thu, 02 Dec 2021 17:52:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:968621624b326084ed82349252b333e649eaab39f71866edb2b9a4f847283680`  
		Last Modified: Thu, 02 Dec 2021 08:40:45 GMT  
		Size: 30.1 MB (30056536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8defed3fac34156bfc8181ec3596d070ea1a0759292a47b2fb5db4931f7c993`  
		Last Modified: Thu, 02 Dec 2021 17:58:03 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f7f46e9e7136ddfaf0ddb7c7eee4dc72441ba3e28af61b94d0e8e209f53d5e`  
		Last Modified: Thu, 02 Dec 2021 17:58:51 GMT  
		Size: 7.8 MB (7839295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42003e96c2b09dbd12ee1a20a7b47c3afdc91bd53b67db6ccc759b2cefbb03d9`  
		Last Modified: Thu, 02 Dec 2021 17:58:50 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; 386

```console
$ docker pull haproxy@sha256:a0314f6766ae8abefb03170b34f00d07afd0801a407eea40cad9edb6246b6fcc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39936823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b71044da5a122866a5057bda711053d340beb65a47a3c4340729886e7ae0611`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 02 Dec 2021 02:39:54 GMT
ADD file:0284c10b06ba22560408e1e14c1147887f4302c79dba143277ece2e333d6dcbc in / 
# Thu, 02 Dec 2021 02:39:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 08:49:13 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Thu, 02 Dec 2021 08:53:18 GMT
ENV HAPROXY_VERSION=2.4.9
# Thu, 02 Dec 2021 08:53:18 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.9.tar.gz
# Thu, 02 Dec 2021 08:53:18 GMT
ENV HAPROXY_SHA256=d56c7fe3c5afedd1b9a19e1b7f8f954feaf50a9c2f205f99891043858b72a763
# Thu, 02 Dec 2021 08:54:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Thu, 02 Dec 2021 08:54:25 GMT
STOPSIGNAL SIGUSR1
# Thu, 02 Dec 2021 08:54:26 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 02 Dec 2021 08:54:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 08:54:26 GMT
USER haproxy
# Thu, 02 Dec 2021 08:54:27 GMT
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
	-	`sha256:57e86ba9143c46bf44776dcaf76276d30421ec63dab3253f0131fdb2fb39ec5c`  
		Last Modified: Thu, 02 Dec 2021 09:06:41 GMT  
		Size: 7.6 MB (7554127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2753bc6a6b57339d110d62c2c6d3ea23f622eaa2133fde7416aed9f2fc67ac3a`  
		Last Modified: Thu, 02 Dec 2021 09:06:39 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; mips64le

```console
$ docker pull haproxy@sha256:9d7d526d10554548f33e8ce275545dbb77f836c03d43ee86beb461356e1c97be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37547407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d60f6b2629b21a6403fc353fef550046389a149338d37321f23357dfe5a0c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 02 Dec 2021 03:09:10 GMT
ADD file:419aff162077eb16923c3ede6455ca86756a929a5a837bc6ac6b8dc67913503a in / 
# Thu, 02 Dec 2021 03:09:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 04:35:11 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Thu, 02 Dec 2021 04:40:39 GMT
ENV HAPROXY_VERSION=2.4.9
# Thu, 02 Dec 2021 04:40:39 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.9.tar.gz
# Thu, 02 Dec 2021 04:40:40 GMT
ENV HAPROXY_SHA256=d56c7fe3c5afedd1b9a19e1b7f8f954feaf50a9c2f205f99891043858b72a763
# Thu, 02 Dec 2021 04:43:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Thu, 02 Dec 2021 04:43:14 GMT
STOPSIGNAL SIGUSR1
# Thu, 02 Dec 2021 04:43:15 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 02 Dec 2021 04:43:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 04:43:15 GMT
USER haproxy
# Thu, 02 Dec 2021 04:43:16 GMT
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
	-	`sha256:1fddc8f62c7e371b510ec5c50a7e9dfb409c810ceff7d690d17a9f4c2c98dfaf`  
		Last Modified: Thu, 02 Dec 2021 04:55:58 GMT  
		Size: 7.9 MB (7915051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891d597ff343aafb93ad33f1bff4c6895846d1502ab948acea85842f628cc573`  
		Last Modified: Thu, 02 Dec 2021 04:55:53 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; ppc64le

```console
$ docker pull haproxy@sha256:1d028cb3c5f081b5436675160afab73d5bc10352491b9e03fed646b97b9d705c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43445040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4b460db470e494371d3556c803c2e56252042bf6970867abf6444bd51e6915`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 02 Dec 2021 07:21:21 GMT
ADD file:81a93de7f5dcdbb9397c05b9b6bb7dc5a4742119d46faf929b4c6277b02be7a5 in / 
# Thu, 02 Dec 2021 07:21:25 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 13:00:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Thu, 02 Dec 2021 13:07:17 GMT
ENV HAPROXY_VERSION=2.4.9
# Thu, 02 Dec 2021 13:07:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.9.tar.gz
# Thu, 02 Dec 2021 13:07:30 GMT
ENV HAPROXY_SHA256=d56c7fe3c5afedd1b9a19e1b7f8f954feaf50a9c2f205f99891043858b72a763
# Thu, 02 Dec 2021 13:10:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Thu, 02 Dec 2021 13:10:49 GMT
STOPSIGNAL SIGUSR1
# Thu, 02 Dec 2021 13:10:50 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 02 Dec 2021 13:10:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 13:10:54 GMT
USER haproxy
# Thu, 02 Dec 2021 13:10:56 GMT
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
	-	`sha256:fb7c53143a417cfba258d59bcab63cf3d16fc2b418532ea15c13ca114b031bd0`  
		Last Modified: Thu, 02 Dec 2021 13:33:03 GMT  
		Size: 8.2 MB (8171769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6daf5d96344f7d5167a160d089643da42ee60e64481ab7ca0e0827bb50869c19`  
		Last Modified: Thu, 02 Dec 2021 13:33:00 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; s390x

```console
$ docker pull haproxy@sha256:3661dd2b76280544b7b7b4df7321d32881e57021b805f40c28e2c046bf814f12
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37475599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd1553ad233765c69d9575756b7482b02dfe80bdded4f5421b8259d11d0e115`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 02 Dec 2021 07:19:07 GMT
ADD file:9303def035f391c14bdca007751c5061f36fe929d5b3f4d725ce376e25f7dd36 in / 
# Thu, 02 Dec 2021 07:19:09 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 08:31:46 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Thu, 02 Dec 2021 08:33:18 GMT
ENV HAPROXY_VERSION=2.4.9
# Thu, 02 Dec 2021 08:33:18 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.9.tar.gz
# Thu, 02 Dec 2021 08:33:19 GMT
ENV HAPROXY_SHA256=d56c7fe3c5afedd1b9a19e1b7f8f954feaf50a9c2f205f99891043858b72a763
# Thu, 02 Dec 2021 08:33:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Thu, 02 Dec 2021 08:33:48 GMT
STOPSIGNAL SIGUSR1
# Thu, 02 Dec 2021 08:33:48 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 02 Dec 2021 08:33:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 08:33:49 GMT
USER haproxy
# Thu, 02 Dec 2021 08:33:49 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bf2c280d82ca10801fb58bfc3f73029eef17592cbe00e94875cb189bdbac0c5f`  
		Last Modified: Thu, 02 Dec 2021 07:25:12 GMT  
		Size: 29.7 MB (29650954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb82bca4c942b46974a0c6c7f6b09c985591598102323bc9ccaaf483587723b2`  
		Last Modified: Thu, 02 Dec 2021 08:39:46 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294653ef56394ede982e9a5d583d78676180dd04cd7c9dbb60a8770d61ad16a2`  
		Last Modified: Thu, 02 Dec 2021 08:40:22 GMT  
		Size: 7.8 MB (7822757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d0aaa858741f1c522101edfa3a473b4a1ef3d450cce63b654ddc726bbf14c5`  
		Last Modified: Thu, 02 Dec 2021 08:40:21 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
