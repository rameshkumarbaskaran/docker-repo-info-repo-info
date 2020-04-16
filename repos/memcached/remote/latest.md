## `memcached:latest`

```console
$ docker pull memcached@sha256:6df2f148599be997ef7184ad972786847f6f88c31961367f3bbad0525333caab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `memcached:latest` - linux; amd64

```console
$ docker pull memcached@sha256:9eddbead7cb3e16a4acfc24160524eaa6b4d6b399e229d53e21ac3ca988be86c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30492322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683b58b6465dc45d04feef9004e16bfe0281495f5331419ec65872923b988553`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:01:47 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Thu, 16 Apr 2020 09:01:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 09:01:52 GMT
ENV MEMCACHED_VERSION=1.6.5
# Thu, 16 Apr 2020 09:01:52 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Thu, 16 Apr 2020 09:10:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 16 Apr 2020 09:10:55 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 16 Apr 2020 09:10:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 16 Apr 2020 09:10:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2020 09:10:56 GMT
USER memcache
# Thu, 16 Apr 2020 09:10:57 GMT
EXPOSE 11211
# Thu, 16 Apr 2020 09:10:57 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd5009273ce372e945eff9d465c3b9483feafbe19f9dc6e1f158b184b4e112a`  
		Last Modified: Thu, 16 Apr 2020 09:11:23 GMT  
		Size: 5.0 KB (4982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eaadb451d5774749b9f23e4acd4354848a513f3222fc10fc45f19e7f431b8fe`  
		Last Modified: Thu, 16 Apr 2020 09:11:24 GMT  
		Size: 2.2 MB (2196543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68eb9be399922992c4a03a30b64a2b49e357dd09e695a4baf86e2692d2221dd`  
		Last Modified: Thu, 16 Apr 2020 09:11:24 GMT  
		Size: 1.2 MB (1192241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21bced5496d960c3f0117e3a0025b8af1e4cd1a8539fea1e26405385a513d09c`  
		Last Modified: Thu, 16 Apr 2020 09:11:24 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e88f202390fc25200b44fa925889d3821279298543f224be8f98210dc33be6`  
		Last Modified: Thu, 16 Apr 2020 09:11:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:1f4935dd0107cf9cdb6e9164e41ada5092ddac93d048167c94e3611a3db32175
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27895602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050184fb78c6e102b8c4f58464d01aeb5b2f00cc2c4a6368ae78cda9f16fac32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 16 Apr 2020 00:50:14 GMT
ADD file:761a556ec2a7d8c742c860e429c9b9ba3f7abfcd9383c6b3767499de6dcad4bc in / 
# Thu, 16 Apr 2020 00:50:15 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 01:20:06 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Thu, 16 Apr 2020 01:21:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:21:39 GMT
ENV MEMCACHED_VERSION=1.6.5
# Thu, 16 Apr 2020 01:21:41 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Thu, 16 Apr 2020 01:52:48 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 16 Apr 2020 01:52:52 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 16 Apr 2020 01:53:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 16 Apr 2020 01:53:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2020 01:53:06 GMT
USER memcache
# Thu, 16 Apr 2020 01:53:09 GMT
EXPOSE 11211
# Thu, 16 Apr 2020 01:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:600369660a591bc9594fcf333a847fe997901785f7032d3ad2822b2812c13243`  
		Last Modified: Thu, 16 Apr 2020 00:58:26 GMT  
		Size: 24.8 MB (24836437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b28efba0bcc6fbfeccf6561801abdbc28d2b64d489f76ee8191a0e4b10e37d`  
		Last Modified: Thu, 16 Apr 2020 01:53:20 GMT  
		Size: 4.9 KB (4891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc33a1fa2e0b9f8c854ee94cd9adb7ef5ffb735c0a70cc01ccabe5908c4a9d8`  
		Last Modified: Thu, 16 Apr 2020 01:53:23 GMT  
		Size: 1.9 MB (1896808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ace54d112c6a1b7877ddb9dd0d888fc77035cc99c3c294c69d5154ac2cfc4b4`  
		Last Modified: Thu, 16 Apr 2020 01:53:28 GMT  
		Size: 1.2 MB (1157058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fb24ae48dfbd7b3cb65e78556275a263ddb0964a8761b181efaf5a4075082c`  
		Last Modified: Thu, 16 Apr 2020 01:53:37 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d567aeaee62d3bcefc4ecc969a2ef321a2b67bcb144dea02783037b035fffad2`  
		Last Modified: Thu, 16 Apr 2020 01:53:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:54bcd309e2f20393d4697e22b71344137d3f1fdeb447078522a5a2d6a464117e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25646504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1835a38d745cc54481b86a3603e5fe1771df287e08d6061cb35577ce92b735`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 31 Mar 2020 01:48:12 GMT
ADD file:8c3ed0df404a6bcaf7583e71796cb4c1f40e87288953a21d4ee5946079c3274f in / 
# Tue, 31 Mar 2020 01:48:13 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:27:08 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Tue, 31 Mar 2020 03:28:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Apr 2020 01:21:52 GMT
ENV MEMCACHED_VERSION=1.6.5
# Tue, 14 Apr 2020 01:21:54 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Tue, 14 Apr 2020 01:50:54 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Tue, 14 Apr 2020 01:50:57 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Tue, 14 Apr 2020 01:51:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 14 Apr 2020 01:51:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2020 01:51:11 GMT
USER memcache
# Tue, 14 Apr 2020 01:51:12 GMT
EXPOSE 11211
# Tue, 14 Apr 2020 01:51:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:98098fa10651fdba12c848231b7428536a120e17637f1f9e0d25c63880483fcc`  
		Last Modified: Tue, 31 Mar 2020 01:56:24 GMT  
		Size: 22.7 MB (22699731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7a42e48b851419bcd11506631a8d336fb394d979dcea8feb4830f38ba7cfd7`  
		Last Modified: Tue, 31 Mar 2020 04:39:27 GMT  
		Size: 4.9 KB (4899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc96c4fde110b7a8691d85cf0523cd326fbfd1bcbf928719f6173cd292c91305`  
		Last Modified: Tue, 31 Mar 2020 04:39:35 GMT  
		Size: 1.8 MB (1811551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca1ebe9584513d346175a7b8dc24e8a0e1f282079ab035f21745b1efb49aee2`  
		Last Modified: Tue, 14 Apr 2020 03:14:41 GMT  
		Size: 1.1 MB (1129915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3670b9b896bea4402ae6cf76d7c5690c7be94b8712a6ba9bdbc5162c478c3f4a`  
		Last Modified: Tue, 14 Apr 2020 03:14:40 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13fc7c30db064f3e3c4355aa5316e9ee78fc6d5727ba346d8289b531a5244235`  
		Last Modified: Tue, 14 Apr 2020 03:14:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:282789d4892f98749f2cfdd2e9faa8d7b7ff3fca2d470f4550e7c2dd06a8581c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29100906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9310bf5c2a6c872480bed757e37e694bde6d4c42543a1525509e551d384503`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 16 Apr 2020 02:41:52 GMT
ADD file:1aab17002a9095c31dd6928277a045cb26846ac58c3d2d63316332c99a5f90bd in / 
# Thu, 16 Apr 2020 02:41:57 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:36:45 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Thu, 16 Apr 2020 06:36:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 06:36:54 GMT
ENV MEMCACHED_VERSION=1.6.5
# Thu, 16 Apr 2020 06:36:55 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Thu, 16 Apr 2020 06:46:03 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 16 Apr 2020 06:46:04 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 16 Apr 2020 06:46:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 16 Apr 2020 06:46:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2020 06:46:09 GMT
USER memcache
# Thu, 16 Apr 2020 06:46:11 GMT
EXPOSE 11211
# Thu, 16 Apr 2020 06:46:14 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:3d48095d71a365b5910cea98e5566c152a3f9aa11657560568259bf93ff2f4cb`  
		Last Modified: Thu, 16 Apr 2020 02:48:58 GMT  
		Size: 25.9 MB (25857715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee64d56b93c52fef777d45155f9f4cabeeb795f03110196a04e93440b0083302`  
		Last Modified: Thu, 16 Apr 2020 06:46:35 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ed997b739f188931d6ee976a4119bcdec2d6217f0f22c2d85d0f60fc6c16ff`  
		Last Modified: Thu, 16 Apr 2020 06:46:35 GMT  
		Size: 2.1 MB (2074893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f9a34cd70b75b155763818cb1986f3cc9a0520c4402a0a0a21fc83644a1659`  
		Last Modified: Thu, 16 Apr 2020 06:46:36 GMT  
		Size: 1.2 MB (1162864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed30d41929c1ca6b70e33c6aa1a15465f52384fe6dc68010606c0424a2b3198f`  
		Last Modified: Thu, 16 Apr 2020 06:46:35 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351949e9981f8ae13ba5432ba8b8ac9a77c2e01594cc1dc90127592aabb76f12`  
		Last Modified: Thu, 16 Apr 2020 06:46:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:a1af45df58b704f728b0aaa7317c4abc5eeb0e79549fa19dd8c0dcff1c290014
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31163087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac26f7b25f20a9d5e756364bded9d350398d55828d326f11267f98d4e543d492`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 16 Apr 2020 01:39:55 GMT
ADD file:ab0bbfba6c4b56420ffffc6cdddcc4592fff018f0cd07578c7dc0a5faa49df2f in / 
# Thu, 16 Apr 2020 01:39:56 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:07:59 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Thu, 16 Apr 2020 06:08:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 06:08:07 GMT
ENV MEMCACHED_VERSION=1.6.5
# Thu, 16 Apr 2020 06:08:08 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Thu, 16 Apr 2020 06:17:36 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 16 Apr 2020 06:17:36 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 16 Apr 2020 06:17:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 16 Apr 2020 06:17:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2020 06:17:38 GMT
USER memcache
# Thu, 16 Apr 2020 06:17:38 GMT
EXPOSE 11211
# Thu, 16 Apr 2020 06:17:38 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:75bc60a98e6523be3fadd9128c1a630cb5cbd2d2d813ee5e99dc146a3de22254`  
		Last Modified: Thu, 16 Apr 2020 01:46:20 GMT  
		Size: 27.8 MB (27753976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10acbb49c3daa870154eefb461ab6e93acce27feda350106ed4c9aad7dd9420`  
		Last Modified: Thu, 16 Apr 2020 06:18:04 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54de75798c5d7f4609bf5e8905817ae541c8f25184df211967a49df409e18f7f`  
		Last Modified: Thu, 16 Apr 2020 06:18:05 GMT  
		Size: 2.2 MB (2208096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8a9ca0239e982accb9e0a7db5740f0b2ee3ca13a1c1e34d1865efd63906acc`  
		Last Modified: Thu, 16 Apr 2020 06:18:04 GMT  
		Size: 1.2 MB (1195713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8067be63998d1928867ad1ccf9f848a877a9ce544a2b15f0f9980174550586fa`  
		Last Modified: Thu, 16 Apr 2020 06:18:04 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e8df9011315a5eccd12838319a44e93e4ff3302e888e1872a56a3b3072316a`  
		Last Modified: Thu, 16 Apr 2020 06:18:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; mips64le

```console
$ docker pull memcached@sha256:37443af1d21860af4e933db9c5901eb2334d29a83ba221ac01c9a77298ec38f8
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.7 MB (28725217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a54bd34452343aa3a8f6e631804252b62cdf1fb36e95356f304eebac4ca028`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 16 Apr 2020 03:30:32 GMT
ADD file:1324f1b90326c771ad3fbeba783010d46ba465c130b2b400ff60232e52bc4bbb in / 
# Thu, 16 Apr 2020 03:30:33 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:48:56 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Thu, 16 Apr 2020 06:49:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 06:49:10 GMT
ENV MEMCACHED_VERSION=1.6.5
# Thu, 16 Apr 2020 06:49:11 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Thu, 16 Apr 2020 07:00:08 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 16 Apr 2020 07:00:09 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 16 Apr 2020 07:00:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 16 Apr 2020 07:00:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2020 07:00:12 GMT
USER memcache
# Thu, 16 Apr 2020 07:00:12 GMT
EXPOSE 11211
# Thu, 16 Apr 2020 07:00:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:9d68bbb6bb3e325311e23872a0324580a3e32aea907701fa94bab81e80ff88c4`  
		Last Modified: Thu, 16 Apr 2020 03:56:50 GMT  
		Size: 25.8 MB (25762172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785715caab3f56abc177362b8199fd005f80b317c038df3a45c5bd1403c44ad4`  
		Last Modified: Thu, 16 Apr 2020 07:00:29 GMT  
		Size: 5.0 KB (4983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7f59cac83da5b1ac93cef4097b98628adff0484596ed417e3ec37182291062`  
		Last Modified: Thu, 16 Apr 2020 07:00:31 GMT  
		Size: 1.8 MB (1775990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ff54829cc31369ac9b0e95e0689f6fc93229eec69c55c0d7e975e2937cdc84`  
		Last Modified: Thu, 16 Apr 2020 07:00:31 GMT  
		Size: 1.2 MB (1181663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58a488b9bf07f7fcb8988ab4c67c47cc46f3e4bae17572806460fbe03a380eb`  
		Last Modified: Thu, 16 Apr 2020 07:00:30 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9534a0c87d7e09580b6f25e662699f34a06a9e545c58950262cebcefbb118d5e`  
		Last Modified: Thu, 16 Apr 2020 07:00:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:276923dcc9e512c2f1c08118d810f65debcec9b6687c842faf1d3eec94306030
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34070732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757225c0b9a3b4adb4ce9c18b375416ef9c481aa42e85bc7542e0dbd4ae0cec5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 16 Apr 2020 01:38:30 GMT
ADD file:9beea54416432abbd09d26b965c3c8e5bea8e233113f9bc308294c0008ee886f in / 
# Thu, 16 Apr 2020 01:38:39 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:51:43 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Thu, 16 Apr 2020 02:52:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 02:52:16 GMT
ENV MEMCACHED_VERSION=1.6.5
# Thu, 16 Apr 2020 02:52:26 GMT
ENV MEMCACHED_SHA1=1ddb5f37f69946b63512ad0f89dc448ff7ba5713
# Thu, 16 Apr 2020 03:07:11 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Thu, 16 Apr 2020 03:07:14 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Thu, 16 Apr 2020 03:07:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 16 Apr 2020 03:07:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2020 03:07:29 GMT
USER memcache
# Thu, 16 Apr 2020 03:07:34 GMT
EXPOSE 11211
# Thu, 16 Apr 2020 03:07:39 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f268991f8af64097bbfefa3f01dd3fdb7f715051a3681f352504a3ecaa9d3596`  
		Last Modified: Thu, 16 Apr 2020 01:54:39 GMT  
		Size: 30.5 MB (30524651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f54728ddf3d5bb9060696766575c26ec0bb229622818d0e5dd8a5ab0553926`  
		Last Modified: Thu, 16 Apr 2020 03:08:14 GMT  
		Size: 5.0 KB (4984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac80ca64d3e34a34f53513e845287c7a5bdf39f59d0bb72678a8081c97176068`  
		Last Modified: Thu, 16 Apr 2020 03:08:14 GMT  
		Size: 2.3 MB (2322683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e5e36550d8e4f020336d5d1dab133cf1465839cba3f2c78d91d55b68ff2c3e`  
		Last Modified: Thu, 16 Apr 2020 03:08:14 GMT  
		Size: 1.2 MB (1218011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2baec843adb884a462036750346dcb278d276ef643b2cf4f3db9fa55c9fadc`  
		Last Modified: Thu, 16 Apr 2020 03:08:13 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe0a71e5ce63dce2c34dd1bcaa4198872841b8d7f50911091a547d527f80108`  
		Last Modified: Thu, 16 Apr 2020 03:08:13 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:057b9567b3c01a5b0dbf1c7dba5b89d88df721093c01da5c6a1425c1f8ad6265
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.7 MB (28694839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2378496a97259729a8423d4b14be0ea1db6e01b3f9aa9e34431ef824d655e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:03 GMT
ADD file:eec6c56f8680753860198c3af0d94aabb87018ca30f6f6e346621a6bffe0e4b8 in / 
# Sat, 28 Dec 2019 04:42:04 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 09:52:58 GMT
RUN groupadd --system --gid 11211 memcache && useradd --system --gid memcache --uid 11211 memcache
# Sat, 28 Dec 2019 09:53:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libsasl2-modules 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 09:53:02 GMT
ENV MEMCACHED_VERSION=1.5.20
# Sat, 28 Dec 2019 09:53:02 GMT
ENV MEMCACHED_SHA1=5d3b5af3ce0a1483d655017db7228bcaeff10d47
# Sat, 28 Dec 2019 09:57:41 GMT
RUN set -x 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libio-socket-ssl-perl 		libsasl2-dev 		libssl-dev 		make 		perl 		wget 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& enableExtstore="$( 		case "$gnuArch" in 			s390x-*) ;; 			*) echo '--enable-extstore' ;; 		esac 	)" 	&& ./configure 		--build="$gnuArch" 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 		$enableExtstore 	&& make -j "$(nproc)" 		&& sed -i.bak 's/SECLEVEL=2/SECLEVEL=1/g' /etc/ssl/openssl.cnf 	&& make test 	&& mv /etc/ssl/openssl.cnf.bak /etc/ssl/openssl.cnf 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark > /dev/null 	&& find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 		&& memcached -V
# Sat, 28 Dec 2019 09:57:41 GMT
COPY file:bf641b13ea5b37f5830b299ebe9d72f194ee5d897db14faf8b133dc7a66a48ad in /usr/local/bin/ 
# Sat, 28 Dec 2019 09:57:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 Dec 2019 09:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Dec 2019 09:57:42 GMT
USER memcache
# Sat, 28 Dec 2019 09:57:42 GMT
EXPOSE 11211
# Sat, 28 Dec 2019 09:57:42 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f7542f43e95fb32a870ee38d7f0e7bb23267ac8dcf709e3944311b0a30d7a479`  
		Last Modified: Sat, 28 Dec 2019 04:45:08 GMT  
		Size: 25.7 MB (25705315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10233ccd3a1a569a8ec38365e560732bbd6adbbe1646b79cee3569d59f7cef73`  
		Last Modified: Sat, 28 Dec 2019 09:57:55 GMT  
		Size: 5.0 KB (5022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3e3dfd06ace4d055f1539e38c0fb68e4d1866043a1ba372c8c2f0fec48315d`  
		Last Modified: Sat, 28 Dec 2019 09:57:55 GMT  
		Size: 1.9 MB (1885865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cce4b30798653a4fcf3fd9160a90374e103d5c1e877e69645d033c0f916e67`  
		Last Modified: Sat, 28 Dec 2019 09:57:55 GMT  
		Size: 1.1 MB (1098229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982ba8604e516e190f19469aa238d4197aa0000182cbc54d57345a029b765600`  
		Last Modified: Sat, 28 Dec 2019 09:57:55 GMT  
		Size: 287.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabfe12e62b1d54d9dce449f2dc85f703ade5574f14eadfa54a601a86cc96e54`  
		Last Modified: Sat, 28 Dec 2019 09:57:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
