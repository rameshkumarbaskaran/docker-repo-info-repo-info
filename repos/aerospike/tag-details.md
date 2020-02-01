<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:4.6.0.12`](#aerospike46012)
-	[`aerospike:4.7.0.10`](#aerospike47010)
-	[`aerospike:4.8.0.5`](#aerospike4805)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:4.6.0.12`

```console
$ docker pull aerospike@sha256:e02bb446d0617bcb4c507acc1582fb9ea23838e0605e3b844dcb5a947d04fee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.6.0.12` - linux; amd64

```console
$ docker pull aerospike@sha256:c19e16beefcea13039fdb655630e04c1a2efb06fa9c5da9cf4f3cfb1c9484735
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51656087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bafe6d62895445307304c697adb98f3f05fe2c67cfc68f21d51e948b1e4a7bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:57 GMT
ADD file:003d2bac85e72555ed93f77a2b1d595a7fe51c4a9a2401496a82fc673a863fd6 in / 
# Sat, 01 Feb 2020 17:23:58 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:45:24 GMT
ENV AEROSPIKE_VERSION=4.6.0.12
# Sat, 01 Feb 2020 17:45:24 GMT
ENV AEROSPIKE_SHA256=3e4cfc8c3681091e5ba56042ad4d6a9fc1a69c6f732d08e917c4df05e5eb8d96
# Sat, 01 Feb 2020 17:45:43 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Sat, 01 Feb 2020 17:45:44 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Sat, 01 Feb 2020 17:45:44 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Sat, 01 Feb 2020 17:45:44 GMT
VOLUME [/opt/aerospike/data]
# Sat, 01 Feb 2020 17:45:44 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 01 Feb 2020 17:45:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 17:45:45 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:619014d83c026bca3d21f5eb42a629ac2dbe15bdb37b77f25fc1ac5fbada68e5`  
		Last Modified: Sat, 01 Feb 2020 17:29:01 GMT  
		Size: 22.5 MB (22524713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020656b2ed273a2c21cd21b99d35d642c2006b345138cb1297eeed2dc96bd0d7`  
		Last Modified: Sat, 01 Feb 2020 17:46:53 GMT  
		Size: 29.1 MB (29129357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe9a6ecc64a950425aca05a9a98a1724a88a5f3e6565876db7f88ef49dd60c5`  
		Last Modified: Sat, 01 Feb 2020 17:46:47 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d3bd02393921c02d6baf7c16257b8b8d2a8eb5dacd70d0802d34060ce4def0`  
		Last Modified: Sat, 01 Feb 2020 17:46:47 GMT  
		Size: 884.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:4.7.0.10`

```console
$ docker pull aerospike@sha256:ec43998928c7bbf5e24fbe74b8a162e04869b6a34724b41bef2e92c0dd911571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.7.0.10` - linux; amd64

```console
$ docker pull aerospike@sha256:26631be1ef2233be7c6d0c3a79c1d9788abea91e1e432e4e8edefbcb170f28f2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51778769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e22702945d90f01c26a6c034f8ca0b527ec6853bc2bd25d06b0728381b749b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:57 GMT
ADD file:003d2bac85e72555ed93f77a2b1d595a7fe51c4a9a2401496a82fc673a863fd6 in / 
# Sat, 01 Feb 2020 17:23:58 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:45:52 GMT
ENV AEROSPIKE_VERSION=4.7.0.10
# Sat, 01 Feb 2020 17:45:52 GMT
ENV AEROSPIKE_SHA256=cf96bf6e8dd85b57e0a2bba4446ae3a66b12f753c9d95af69e97f2ec0eea210d
# Sat, 01 Feb 2020 17:46:10 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Sat, 01 Feb 2020 17:46:10 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Sat, 01 Feb 2020 17:46:11 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Sat, 01 Feb 2020 17:46:11 GMT
VOLUME [/opt/aerospike/data]
# Sat, 01 Feb 2020 17:46:11 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 01 Feb 2020 17:46:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 17:46:11 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:619014d83c026bca3d21f5eb42a629ac2dbe15bdb37b77f25fc1ac5fbada68e5`  
		Last Modified: Sat, 01 Feb 2020 17:29:01 GMT  
		Size: 22.5 MB (22524713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbecd3a8a12321e39e0e43511a69c517332254b00999e180017c88122c763a57`  
		Last Modified: Sat, 01 Feb 2020 17:47:02 GMT  
		Size: 29.3 MB (29252038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7299f7b8b387ef0e8aa3cef49dbaeebc6a08e76c6bcacf88212cbdeb3546c17e`  
		Last Modified: Sat, 01 Feb 2020 17:46:56 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd98594a55521df0ab4b9a2afbbfc4e364824bb543f02ab71c93ce0648b4964`  
		Last Modified: Sat, 01 Feb 2020 17:46:56 GMT  
		Size: 884.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:4.8.0.5`

```console
$ docker pull aerospike@sha256:d907d3c6fe52d1d9396ab0824c76fae1c469903e205a02c03cce42691fedaabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.8.0.5` - linux; amd64

```console
$ docker pull aerospike@sha256:e1e98189a037991290238555b122aa8d47a8b3a398a5821b2831cccce5f82524
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51855707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434fd2ff640de6b11979fa7004584a3c49e50e04ee08757fcb215764b30d37d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:57 GMT
ADD file:003d2bac85e72555ed93f77a2b1d595a7fe51c4a9a2401496a82fc673a863fd6 in / 
# Sat, 01 Feb 2020 17:23:58 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:46:16 GMT
ENV AEROSPIKE_VERSION=4.8.0.5
# Sat, 01 Feb 2020 17:46:16 GMT
ENV AEROSPIKE_SHA256=b7082c51eee268992a55c5f0751b3de006cda857d93ed9d3e14624ca7118a1e8
# Sat, 01 Feb 2020 17:46:35 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Sat, 01 Feb 2020 17:46:35 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Sat, 01 Feb 2020 17:46:36 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Sat, 01 Feb 2020 17:46:36 GMT
VOLUME [/opt/aerospike/data]
# Sat, 01 Feb 2020 17:46:36 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 01 Feb 2020 17:46:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 17:46:37 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:619014d83c026bca3d21f5eb42a629ac2dbe15bdb37b77f25fc1ac5fbada68e5`  
		Last Modified: Sat, 01 Feb 2020 17:29:01 GMT  
		Size: 22.5 MB (22524713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6a63677c0f79c1bbc9605ec0526fd17412cac847d86878e9e5bdd94f650a84`  
		Last Modified: Sat, 01 Feb 2020 17:47:09 GMT  
		Size: 29.3 MB (29328975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9380f2d6d9f47066fb21c2e9f03e1a56fd2bb7dd4e0b85e52a2398675eeb1a1`  
		Last Modified: Sat, 01 Feb 2020 17:47:04 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b789a976b746ff2837bcc56105cb7f3a5c074e670d46eaa087a0dd0d917350`  
		Last Modified: Sat, 01 Feb 2020 17:47:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:d907d3c6fe52d1d9396ab0824c76fae1c469903e205a02c03cce42691fedaabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:e1e98189a037991290238555b122aa8d47a8b3a398a5821b2831cccce5f82524
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51855707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434fd2ff640de6b11979fa7004584a3c49e50e04ee08757fcb215764b30d37d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:57 GMT
ADD file:003d2bac85e72555ed93f77a2b1d595a7fe51c4a9a2401496a82fc673a863fd6 in / 
# Sat, 01 Feb 2020 17:23:58 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:46:16 GMT
ENV AEROSPIKE_VERSION=4.8.0.5
# Sat, 01 Feb 2020 17:46:16 GMT
ENV AEROSPIKE_SHA256=b7082c51eee268992a55c5f0751b3de006cda857d93ed9d3e14624ca7118a1e8
# Sat, 01 Feb 2020 17:46:35 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Sat, 01 Feb 2020 17:46:35 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Sat, 01 Feb 2020 17:46:36 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Sat, 01 Feb 2020 17:46:36 GMT
VOLUME [/opt/aerospike/data]
# Sat, 01 Feb 2020 17:46:36 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 01 Feb 2020 17:46:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 17:46:37 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:619014d83c026bca3d21f5eb42a629ac2dbe15bdb37b77f25fc1ac5fbada68e5`  
		Last Modified: Sat, 01 Feb 2020 17:29:01 GMT  
		Size: 22.5 MB (22524713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6a63677c0f79c1bbc9605ec0526fd17412cac847d86878e9e5bdd94f650a84`  
		Last Modified: Sat, 01 Feb 2020 17:47:09 GMT  
		Size: 29.3 MB (29328975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9380f2d6d9f47066fb21c2e9f03e1a56fd2bb7dd4e0b85e52a2398675eeb1a1`  
		Last Modified: Sat, 01 Feb 2020 17:47:04 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b789a976b746ff2837bcc56105cb7f3a5c074e670d46eaa087a0dd0d917350`  
		Last Modified: Sat, 01 Feb 2020 17:47:05 GMT  
		Size: 884.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
