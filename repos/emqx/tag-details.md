<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:4`](#emqx4)
-	[`emqx:4.3`](#emqx43)
-	[`emqx:4.3.15`](#emqx4315)
-	[`emqx:4.4`](#emqx44)
-	[`emqx:4.4.4`](#emqx444)
-	[`emqx:latest`](#emqxlatest)

## `emqx:4`

```console
$ docker pull emqx@sha256:cdce1403e0fee48b827129479775d37302f0e22cfc41b8c71da75ff82e5291be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4` - linux; amd64

```console
$ docker pull emqx@sha256:96aaa084ede72e2f7063825961b9d4c33c7de7070a3eda430420f1aef1705d7d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124813883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05d42000605d355acff3be7bd2e91561b4d0a782bebfabd01d3d03810209333`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:50 GMT
ADD file:7726efb0e0eb5003dbcf2967ec29364479eec8b41f2569ff189372153115b54b in / 
# Tue, 23 Aug 2022 00:20:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:05:55 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:05:56 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 23 Aug 2022 01:05:56 GMT
ENV OTP=otp24.1.5-3
# Tue, 23 Aug 2022 01:06:01 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 Aug 2022 01:06:08 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 23 Aug 2022 01:06:08 GMT
WORKDIR /opt/emqx
# Tue, 23 Aug 2022 01:06:08 GMT
USER emqx
# Tue, 23 Aug 2022 01:06:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 Aug 2022 01:06:08 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 Aug 2022 01:06:08 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 23 Aug 2022 01:06:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 01:06:09 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:7a6db449b51b92eac5c81cdbd82917785343f1664b2be57b22337b0a40c5b29d`  
		Last Modified: Tue, 23 Aug 2022 00:24:59 GMT  
		Size: 31.4 MB (31381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffe4803a256fc338d2725fd4a931050eb43f5804176597d989565411f39c0ba`  
		Last Modified: Tue, 23 Aug 2022 01:06:37 GMT  
		Size: 2.6 MB (2569463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8158f546cdbbf53444243363ab3ad5ffb0d011f3609b02f3e76f388262324cf`  
		Last Modified: Tue, 23 Aug 2022 01:06:42 GMT  
		Size: 45.4 MB (45424512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573b89c93de2f74dcf9490f92cbbf4e6ce0d5cf3a36113621de60cb5f14c606d`  
		Last Modified: Tue, 23 Aug 2022 01:06:42 GMT  
		Size: 45.4 MB (45437317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efae4ef2c4c3e4f2858b9437a6dc47120ff2cd5821967db6f10e8ecb32d33cb1`  
		Last Modified: Tue, 23 Aug 2022 01:06:37 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b9b2be320c2a2469aa9c8de01a47db24c4b11d7d8980a59e39259a4976cfc49c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110033038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcabc472c20703152f5e87f687372023f66139abb5c82b7bdecb205d4139962f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:48:22 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:48:22 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 23 Aug 2022 02:48:23 GMT
ENV OTP=otp24.1.5-3
# Tue, 23 Aug 2022 02:48:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 Aug 2022 02:48:30 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 23 Aug 2022 02:48:30 GMT
WORKDIR /opt/emqx
# Tue, 23 Aug 2022 02:48:31 GMT
USER emqx
# Tue, 23 Aug 2022 02:48:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 Aug 2022 02:48:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 Aug 2022 02:48:35 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 23 Aug 2022 02:48:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:48:36 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76875b2a2774be642d6a500995cffb336dc0b7fce71c6554e4415cc6df01a4b2`  
		Last Modified: Tue, 23 Aug 2022 02:49:14 GMT  
		Size: 2.4 MB (2353690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bd6d30cd6371bb62afaacfb03fb3dd2ea33d16d25087af221e21d238febfc9`  
		Last Modified: Tue, 23 Aug 2022 02:49:18 GMT  
		Size: 38.8 MB (38806760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cf00ca63decf520e5ab938da78a25d9ad2816babd18a8e5594cc877a2d4791`  
		Last Modified: Tue, 23 Aug 2022 02:49:18 GMT  
		Size: 38.8 MB (38807691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c5c2a2bac240c35e3c2ef46b56552e483b7324b2c74c09c78bc86d2a7e7b0b`  
		Last Modified: Tue, 23 Aug 2022 02:49:13 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3`

```console
$ docker pull emqx@sha256:b55e60556e2fbb77cdd9b5b77712d330f57c0edc4da46c26184fcbe10c8bf593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.3` - linux; amd64

```console
$ docker pull emqx@sha256:f29b7e63cad4da4acdb4a42066b107758a6be7e6e221d7e5fb6df158915ea2b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103862512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feced5ed4320bee6a4c980e1d7807203f0dd0bcb9f40ade339ec3eb2b6fbfeef`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:10 GMT
ADD file:baca493d7744d12304f6d9c7b6ec0800453a0ba02cbf4005ec35c7b921adf0c4 in / 
# Tue, 23 Aug 2022 00:21:10 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:05:33 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:05:33 GMT
ENV EMQX_VERSION=4.3.15
# Tue, 23 Aug 2022 01:05:38 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 Aug 2022 01:05:44 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 23 Aug 2022 01:05:44 GMT
WORKDIR /opt/emqx
# Tue, 23 Aug 2022 01:05:44 GMT
USER emqx
# Tue, 23 Aug 2022 01:05:44 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 Aug 2022 01:05:45 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 Aug 2022 01:05:45 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Tue, 23 Aug 2022 01:05:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 01:05:45 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:2238450926aa858e592e60bb5d68dd26eeab8a984eee45505ca89d2022e3b450`  
		Last Modified: Tue, 23 Aug 2022 00:25:43 GMT  
		Size: 27.1 MB (27138330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fc000e6c6f87d5970bb32934528b67bd477dd1f5b55750bacff840ca9afa16`  
		Last Modified: Tue, 23 Aug 2022 01:06:24 GMT  
		Size: 4.6 MB (4610293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dfcce166ea2a4d49761e69fa4301ac76c2ffbce971391faf1f7b3847f965d2`  
		Last Modified: Tue, 23 Aug 2022 01:06:28 GMT  
		Size: 36.1 MB (36056943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac686cd8804af39d2959b821282da48d5fcfb7b8e6338a9c689c28b5ecf22bf`  
		Last Modified: Tue, 23 Aug 2022 01:06:28 GMT  
		Size: 36.1 MB (36055904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1aa5f6638a70fdc86e8f2423e702510595c42488ffe301df20abb03590fdfb`  
		Last Modified: Tue, 23 Aug 2022 01:06:23 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:3ac92e082f78f6c79436d92a8bc0b02b223dc6e51f3362475630f57557b8256d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101934052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653d6bc567df59282c0e919f8da05ed6944db4c1dd664b56f0276722f1c7e4f4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:58 GMT
ADD file:4c5bca2d158b11314fb47a6d4b34239575621c2f00f92e77870f23aa02913fac in / 
# Tue, 23 Aug 2022 01:52:59 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:47:57 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:47:57 GMT
ENV EMQX_VERSION=4.3.15
# Tue, 23 Aug 2022 02:48:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 Aug 2022 02:48:04 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 23 Aug 2022 02:48:05 GMT
WORKDIR /opt/emqx
# Tue, 23 Aug 2022 02:48:05 GMT
USER emqx
# Tue, 23 Aug 2022 02:48:06 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 Aug 2022 02:48:07 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 Aug 2022 02:48:09 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Tue, 23 Aug 2022 02:48:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:48:10 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:a84b81edbdb892b3702892bbb01c240695b0b9d619fda43a9b951c9d2df1443c`  
		Last Modified: Tue, 23 Aug 2022 01:58:50 GMT  
		Size: 25.9 MB (25912515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4cfd2f8a927d82ae5d26d82ed5148ad6a2a04e77a07b7a8b09510f39a69d0b3`  
		Last Modified: Tue, 23 Aug 2022 02:48:59 GMT  
		Size: 4.5 MB (4485521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850adcf8056d1b068f8f7c9c4ac1bf58621a291060fffbcf0c53d16fd5ff690a`  
		Last Modified: Tue, 23 Aug 2022 02:49:02 GMT  
		Size: 35.8 MB (35761707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0121fab99e6fd1a8eef8c52ec64255cf4b03c04c6836e7d1bef8bc080d74a300`  
		Last Modified: Tue, 23 Aug 2022 02:49:02 GMT  
		Size: 35.8 MB (35773268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79194c5998efc0a6588755f766dae727b0bce61d7ee1c6ec94657fa7de17ae4`  
		Last Modified: Tue, 23 Aug 2022 02:48:58 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3.15`

```console
$ docker pull emqx@sha256:b55e60556e2fbb77cdd9b5b77712d330f57c0edc4da46c26184fcbe10c8bf593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.3.15` - linux; amd64

```console
$ docker pull emqx@sha256:f29b7e63cad4da4acdb4a42066b107758a6be7e6e221d7e5fb6df158915ea2b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103862512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feced5ed4320bee6a4c980e1d7807203f0dd0bcb9f40ade339ec3eb2b6fbfeef`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:10 GMT
ADD file:baca493d7744d12304f6d9c7b6ec0800453a0ba02cbf4005ec35c7b921adf0c4 in / 
# Tue, 23 Aug 2022 00:21:10 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:05:33 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:05:33 GMT
ENV EMQX_VERSION=4.3.15
# Tue, 23 Aug 2022 01:05:38 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 Aug 2022 01:05:44 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 23 Aug 2022 01:05:44 GMT
WORKDIR /opt/emqx
# Tue, 23 Aug 2022 01:05:44 GMT
USER emqx
# Tue, 23 Aug 2022 01:05:44 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 Aug 2022 01:05:45 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 Aug 2022 01:05:45 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Tue, 23 Aug 2022 01:05:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 01:05:45 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:2238450926aa858e592e60bb5d68dd26eeab8a984eee45505ca89d2022e3b450`  
		Last Modified: Tue, 23 Aug 2022 00:25:43 GMT  
		Size: 27.1 MB (27138330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fc000e6c6f87d5970bb32934528b67bd477dd1f5b55750bacff840ca9afa16`  
		Last Modified: Tue, 23 Aug 2022 01:06:24 GMT  
		Size: 4.6 MB (4610293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dfcce166ea2a4d49761e69fa4301ac76c2ffbce971391faf1f7b3847f965d2`  
		Last Modified: Tue, 23 Aug 2022 01:06:28 GMT  
		Size: 36.1 MB (36056943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac686cd8804af39d2959b821282da48d5fcfb7b8e6338a9c689c28b5ecf22bf`  
		Last Modified: Tue, 23 Aug 2022 01:06:28 GMT  
		Size: 36.1 MB (36055904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1aa5f6638a70fdc86e8f2423e702510595c42488ffe301df20abb03590fdfb`  
		Last Modified: Tue, 23 Aug 2022 01:06:23 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.3.15` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:3ac92e082f78f6c79436d92a8bc0b02b223dc6e51f3362475630f57557b8256d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101934052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653d6bc567df59282c0e919f8da05ed6944db4c1dd664b56f0276722f1c7e4f4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:58 GMT
ADD file:4c5bca2d158b11314fb47a6d4b34239575621c2f00f92e77870f23aa02913fac in / 
# Tue, 23 Aug 2022 01:52:59 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:47:57 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:47:57 GMT
ENV EMQX_VERSION=4.3.15
# Tue, 23 Aug 2022 02:48:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 Aug 2022 02:48:04 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 23 Aug 2022 02:48:05 GMT
WORKDIR /opt/emqx
# Tue, 23 Aug 2022 02:48:05 GMT
USER emqx
# Tue, 23 Aug 2022 02:48:06 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 Aug 2022 02:48:07 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 Aug 2022 02:48:09 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Tue, 23 Aug 2022 02:48:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:48:10 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:a84b81edbdb892b3702892bbb01c240695b0b9d619fda43a9b951c9d2df1443c`  
		Last Modified: Tue, 23 Aug 2022 01:58:50 GMT  
		Size: 25.9 MB (25912515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4cfd2f8a927d82ae5d26d82ed5148ad6a2a04e77a07b7a8b09510f39a69d0b3`  
		Last Modified: Tue, 23 Aug 2022 02:48:59 GMT  
		Size: 4.5 MB (4485521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850adcf8056d1b068f8f7c9c4ac1bf58621a291060fffbcf0c53d16fd5ff690a`  
		Last Modified: Tue, 23 Aug 2022 02:49:02 GMT  
		Size: 35.8 MB (35761707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0121fab99e6fd1a8eef8c52ec64255cf4b03c04c6836e7d1bef8bc080d74a300`  
		Last Modified: Tue, 23 Aug 2022 02:49:02 GMT  
		Size: 35.8 MB (35773268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79194c5998efc0a6588755f766dae727b0bce61d7ee1c6ec94657fa7de17ae4`  
		Last Modified: Tue, 23 Aug 2022 02:48:58 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:cdce1403e0fee48b827129479775d37302f0e22cfc41b8c71da75ff82e5291be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4` - linux; amd64

```console
$ docker pull emqx@sha256:96aaa084ede72e2f7063825961b9d4c33c7de7070a3eda430420f1aef1705d7d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124813883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05d42000605d355acff3be7bd2e91561b4d0a782bebfabd01d3d03810209333`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:50 GMT
ADD file:7726efb0e0eb5003dbcf2967ec29364479eec8b41f2569ff189372153115b54b in / 
# Tue, 23 Aug 2022 00:20:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:05:55 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:05:56 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 23 Aug 2022 01:05:56 GMT
ENV OTP=otp24.1.5-3
# Tue, 23 Aug 2022 01:06:01 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 Aug 2022 01:06:08 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 23 Aug 2022 01:06:08 GMT
WORKDIR /opt/emqx
# Tue, 23 Aug 2022 01:06:08 GMT
USER emqx
# Tue, 23 Aug 2022 01:06:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 Aug 2022 01:06:08 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 Aug 2022 01:06:08 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 23 Aug 2022 01:06:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 01:06:09 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:7a6db449b51b92eac5c81cdbd82917785343f1664b2be57b22337b0a40c5b29d`  
		Last Modified: Tue, 23 Aug 2022 00:24:59 GMT  
		Size: 31.4 MB (31381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffe4803a256fc338d2725fd4a931050eb43f5804176597d989565411f39c0ba`  
		Last Modified: Tue, 23 Aug 2022 01:06:37 GMT  
		Size: 2.6 MB (2569463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8158f546cdbbf53444243363ab3ad5ffb0d011f3609b02f3e76f388262324cf`  
		Last Modified: Tue, 23 Aug 2022 01:06:42 GMT  
		Size: 45.4 MB (45424512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573b89c93de2f74dcf9490f92cbbf4e6ce0d5cf3a36113621de60cb5f14c606d`  
		Last Modified: Tue, 23 Aug 2022 01:06:42 GMT  
		Size: 45.4 MB (45437317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efae4ef2c4c3e4f2858b9437a6dc47120ff2cd5821967db6f10e8ecb32d33cb1`  
		Last Modified: Tue, 23 Aug 2022 01:06:37 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b9b2be320c2a2469aa9c8de01a47db24c4b11d7d8980a59e39259a4976cfc49c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110033038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcabc472c20703152f5e87f687372023f66139abb5c82b7bdecb205d4139962f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:48:22 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:48:22 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 23 Aug 2022 02:48:23 GMT
ENV OTP=otp24.1.5-3
# Tue, 23 Aug 2022 02:48:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 Aug 2022 02:48:30 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 23 Aug 2022 02:48:30 GMT
WORKDIR /opt/emqx
# Tue, 23 Aug 2022 02:48:31 GMT
USER emqx
# Tue, 23 Aug 2022 02:48:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 Aug 2022 02:48:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 Aug 2022 02:48:35 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 23 Aug 2022 02:48:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:48:36 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76875b2a2774be642d6a500995cffb336dc0b7fce71c6554e4415cc6df01a4b2`  
		Last Modified: Tue, 23 Aug 2022 02:49:14 GMT  
		Size: 2.4 MB (2353690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bd6d30cd6371bb62afaacfb03fb3dd2ea33d16d25087af221e21d238febfc9`  
		Last Modified: Tue, 23 Aug 2022 02:49:18 GMT  
		Size: 38.8 MB (38806760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cf00ca63decf520e5ab938da78a25d9ad2816babd18a8e5594cc877a2d4791`  
		Last Modified: Tue, 23 Aug 2022 02:49:18 GMT  
		Size: 38.8 MB (38807691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c5c2a2bac240c35e3c2ef46b56552e483b7324b2c74c09c78bc86d2a7e7b0b`  
		Last Modified: Tue, 23 Aug 2022 02:49:13 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.4`

```console
$ docker pull emqx@sha256:cdce1403e0fee48b827129479775d37302f0e22cfc41b8c71da75ff82e5291be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4.4` - linux; amd64

```console
$ docker pull emqx@sha256:96aaa084ede72e2f7063825961b9d4c33c7de7070a3eda430420f1aef1705d7d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124813883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05d42000605d355acff3be7bd2e91561b4d0a782bebfabd01d3d03810209333`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:50 GMT
ADD file:7726efb0e0eb5003dbcf2967ec29364479eec8b41f2569ff189372153115b54b in / 
# Tue, 23 Aug 2022 00:20:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:05:55 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:05:56 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 23 Aug 2022 01:05:56 GMT
ENV OTP=otp24.1.5-3
# Tue, 23 Aug 2022 01:06:01 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 Aug 2022 01:06:08 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 23 Aug 2022 01:06:08 GMT
WORKDIR /opt/emqx
# Tue, 23 Aug 2022 01:06:08 GMT
USER emqx
# Tue, 23 Aug 2022 01:06:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 Aug 2022 01:06:08 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 Aug 2022 01:06:08 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 23 Aug 2022 01:06:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 01:06:09 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:7a6db449b51b92eac5c81cdbd82917785343f1664b2be57b22337b0a40c5b29d`  
		Last Modified: Tue, 23 Aug 2022 00:24:59 GMT  
		Size: 31.4 MB (31381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffe4803a256fc338d2725fd4a931050eb43f5804176597d989565411f39c0ba`  
		Last Modified: Tue, 23 Aug 2022 01:06:37 GMT  
		Size: 2.6 MB (2569463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8158f546cdbbf53444243363ab3ad5ffb0d011f3609b02f3e76f388262324cf`  
		Last Modified: Tue, 23 Aug 2022 01:06:42 GMT  
		Size: 45.4 MB (45424512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573b89c93de2f74dcf9490f92cbbf4e6ce0d5cf3a36113621de60cb5f14c606d`  
		Last Modified: Tue, 23 Aug 2022 01:06:42 GMT  
		Size: 45.4 MB (45437317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efae4ef2c4c3e4f2858b9437a6dc47120ff2cd5821967db6f10e8ecb32d33cb1`  
		Last Modified: Tue, 23 Aug 2022 01:06:37 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b9b2be320c2a2469aa9c8de01a47db24c4b11d7d8980a59e39259a4976cfc49c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110033038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcabc472c20703152f5e87f687372023f66139abb5c82b7bdecb205d4139962f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:48:22 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:48:22 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 23 Aug 2022 02:48:23 GMT
ENV OTP=otp24.1.5-3
# Tue, 23 Aug 2022 02:48:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 Aug 2022 02:48:30 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 23 Aug 2022 02:48:30 GMT
WORKDIR /opt/emqx
# Tue, 23 Aug 2022 02:48:31 GMT
USER emqx
# Tue, 23 Aug 2022 02:48:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 Aug 2022 02:48:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 Aug 2022 02:48:35 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 23 Aug 2022 02:48:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:48:36 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76875b2a2774be642d6a500995cffb336dc0b7fce71c6554e4415cc6df01a4b2`  
		Last Modified: Tue, 23 Aug 2022 02:49:14 GMT  
		Size: 2.4 MB (2353690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bd6d30cd6371bb62afaacfb03fb3dd2ea33d16d25087af221e21d238febfc9`  
		Last Modified: Tue, 23 Aug 2022 02:49:18 GMT  
		Size: 38.8 MB (38806760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cf00ca63decf520e5ab938da78a25d9ad2816babd18a8e5594cc877a2d4791`  
		Last Modified: Tue, 23 Aug 2022 02:49:18 GMT  
		Size: 38.8 MB (38807691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c5c2a2bac240c35e3c2ef46b56552e483b7324b2c74c09c78bc86d2a7e7b0b`  
		Last Modified: Tue, 23 Aug 2022 02:49:13 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:cdce1403e0fee48b827129479775d37302f0e22cfc41b8c71da75ff82e5291be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:96aaa084ede72e2f7063825961b9d4c33c7de7070a3eda430420f1aef1705d7d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124813883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05d42000605d355acff3be7bd2e91561b4d0a782bebfabd01d3d03810209333`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:50 GMT
ADD file:7726efb0e0eb5003dbcf2967ec29364479eec8b41f2569ff189372153115b54b in / 
# Tue, 23 Aug 2022 00:20:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:05:55 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:05:56 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 23 Aug 2022 01:05:56 GMT
ENV OTP=otp24.1.5-3
# Tue, 23 Aug 2022 01:06:01 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 Aug 2022 01:06:08 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 23 Aug 2022 01:06:08 GMT
WORKDIR /opt/emqx
# Tue, 23 Aug 2022 01:06:08 GMT
USER emqx
# Tue, 23 Aug 2022 01:06:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 Aug 2022 01:06:08 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 Aug 2022 01:06:08 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 23 Aug 2022 01:06:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 01:06:09 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:7a6db449b51b92eac5c81cdbd82917785343f1664b2be57b22337b0a40c5b29d`  
		Last Modified: Tue, 23 Aug 2022 00:24:59 GMT  
		Size: 31.4 MB (31381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffe4803a256fc338d2725fd4a931050eb43f5804176597d989565411f39c0ba`  
		Last Modified: Tue, 23 Aug 2022 01:06:37 GMT  
		Size: 2.6 MB (2569463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8158f546cdbbf53444243363ab3ad5ffb0d011f3609b02f3e76f388262324cf`  
		Last Modified: Tue, 23 Aug 2022 01:06:42 GMT  
		Size: 45.4 MB (45424512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573b89c93de2f74dcf9490f92cbbf4e6ce0d5cf3a36113621de60cb5f14c606d`  
		Last Modified: Tue, 23 Aug 2022 01:06:42 GMT  
		Size: 45.4 MB (45437317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efae4ef2c4c3e4f2858b9437a6dc47120ff2cd5821967db6f10e8ecb32d33cb1`  
		Last Modified: Tue, 23 Aug 2022 01:06:37 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b9b2be320c2a2469aa9c8de01a47db24c4b11d7d8980a59e39259a4976cfc49c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110033038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcabc472c20703152f5e87f687372023f66139abb5c82b7bdecb205d4139962f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:48:22 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:48:22 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 23 Aug 2022 02:48:23 GMT
ENV OTP=otp24.1.5-3
# Tue, 23 Aug 2022 02:48:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 Aug 2022 02:48:30 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 23 Aug 2022 02:48:30 GMT
WORKDIR /opt/emqx
# Tue, 23 Aug 2022 02:48:31 GMT
USER emqx
# Tue, 23 Aug 2022 02:48:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 Aug 2022 02:48:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 Aug 2022 02:48:35 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 23 Aug 2022 02:48:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:48:36 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76875b2a2774be642d6a500995cffb336dc0b7fce71c6554e4415cc6df01a4b2`  
		Last Modified: Tue, 23 Aug 2022 02:49:14 GMT  
		Size: 2.4 MB (2353690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bd6d30cd6371bb62afaacfb03fb3dd2ea33d16d25087af221e21d238febfc9`  
		Last Modified: Tue, 23 Aug 2022 02:49:18 GMT  
		Size: 38.8 MB (38806760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cf00ca63decf520e5ab938da78a25d9ad2816babd18a8e5594cc877a2d4791`  
		Last Modified: Tue, 23 Aug 2022 02:49:18 GMT  
		Size: 38.8 MB (38807691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c5c2a2bac240c35e3c2ef46b56552e483b7324b2c74c09c78bc86d2a7e7b0b`  
		Last Modified: Tue, 23 Aug 2022 02:49:13 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
