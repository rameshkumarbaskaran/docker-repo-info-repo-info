## `spiped:alpine`

```console
$ docker pull spiped@sha256:d49d33b3ae9e7b92ec9b4b11e07e3463e76dc493f0a388cb580c5440c8328e94
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

### `spiped:alpine` - linux; amd64

```console
$ docker pull spiped@sha256:d50ba6a73229914485b07e034308874110b29ff4248bbcd662f55717c0fa55ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7507918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ec3311c4035c9336c868279b0d420cc09b44cb5b9d93a813ed0c85d27304f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 03 Aug 2023 21:20:53 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 03 Aug 2023 21:20:54 GMT
RUN apk add --no-cache libssl1.1
# Thu, 03 Aug 2023 21:20:54 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 03 Aug 2023 21:21:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 03 Aug 2023 21:21:05 GMT
VOLUME [/spiped]
# Thu, 03 Aug 2023 21:21:05 GMT
WORKDIR /spiped
# Thu, 03 Aug 2023 21:21:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 03 Aug 2023 21:21:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 21:21:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68caf666f4bb5f440531a0253294f702094d48f8694afeb159c3bee3a955928f`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56cc31d2500b156ae258f8cc835c039611b28a7fc664f9b5bec635f26a165f1`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 1.4 MB (1433005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0f60cfc992e735eab6827e81ef8ab9410faa8bb5a3aa95bcccd8324b6982b9`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 2.7 MB (2675293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfca5f8c6c25a4d506776dd84d3a716ba26161c5b53d23200c2131ad7abf8c5`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5512defaf613253867bb293bce40f0f1572c7b5909bc313ff20891f7fdf3e5`  
		Last Modified: Thu, 03 Aug 2023 21:21:20 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:b5410a81169549aa8d98776d528c0809dee1c5a5b3d5e034caebd79fa05f9c9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6723797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2bafbe8d36e3352cee4207bd67aecc89e91c95885e66e8b3c91915a5db90f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:20 GMT
ADD file:4213782693bf27a9a6de23bc924ef0c4fb6b2d56010fc07b25f81edeba83b0d4 in / 
# Wed, 14 Jun 2023 18:49:20 GMT
CMD ["/bin/sh"]
# Thu, 03 Aug 2023 20:49:29 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 03 Aug 2023 20:49:32 GMT
RUN apk add --no-cache libssl1.1
# Thu, 03 Aug 2023 20:49:32 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 03 Aug 2023 20:49:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 03 Aug 2023 20:49:41 GMT
VOLUME [/spiped]
# Thu, 03 Aug 2023 20:49:41 GMT
WORKDIR /spiped
# Thu, 03 Aug 2023 20:49:41 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 03 Aug 2023 20:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 20:49:41 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7836be94d3024e2042069c1095caba0b391f70c4b3d34a0475a503239d73dfba`  
		Last Modified: Wed, 14 Jun 2023 18:49:46 GMT  
		Size: 3.1 MB (3143353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8086b266566791667f947a1086634fd914926220dd004f29444af89daf5f3605`  
		Last Modified: Thu, 03 Aug 2023 20:49:52 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2846fa6d4f83f5feca4fa9882c2a6520c64c42d834b4f3c032c0015e2a3d87f9`  
		Last Modified: Thu, 03 Aug 2023 20:49:52 GMT  
		Size: 1.2 MB (1236774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4868a63255145133c12391c8ff4abd5d62b935d15e41d00317269bb0bf44ae`  
		Last Modified: Thu, 03 Aug 2023 20:49:52 GMT  
		Size: 2.3 MB (2341927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fff17ab4aa079775bef673d9dfcc34dbf0fa1ac05deb4eaaff60b80969d808b`  
		Last Modified: Thu, 03 Aug 2023 20:49:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ebe2927deba9122396e871560ce0317d588604b1b81d0b3c6a21ad488c0d4c`  
		Last Modified: Thu, 03 Aug 2023 20:49:51 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:1c5dc77314c37cfc1a189c6d82a7df091e12035a2e15c9e5d9c26c297616ed34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537fd9a23cadf89a08fd05d5e7c43810c53e5d287586404061a09d0e1695db8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 22:36:15 GMT
ADD file:082f034323c559f3cb9feb6422c88b1ec8017f436d6109e238a5c5384a32a90a in / 
# Wed, 14 Jun 2023 22:36:15 GMT
CMD ["/bin/sh"]
# Thu, 03 Aug 2023 21:13:14 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 03 Aug 2023 21:13:16 GMT
RUN apk add --no-cache libssl1.1
# Thu, 03 Aug 2023 21:13:16 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 03 Aug 2023 21:13:23 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 03 Aug 2023 21:13:23 GMT
VOLUME [/spiped]
# Thu, 03 Aug 2023 21:13:23 GMT
WORKDIR /spiped
# Thu, 03 Aug 2023 21:13:23 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 03 Aug 2023 21:13:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 21:13:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:633ba29fd335042456b6e2c073636f6fa30de56f1331c442914739b92a479974`  
		Last Modified: Wed, 14 Jun 2023 22:36:49 GMT  
		Size: 2.9 MB (2898508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970821b1d8efee783127a2619083a669216b80273d993fce6f63cc7186cc19c3`  
		Last Modified: Thu, 03 Aug 2023 21:13:36 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c2d2a094a3ebb4cd33e6ed205b8a7806414f9f4d8fcc19cca243861f895c87`  
		Last Modified: Thu, 03 Aug 2023 21:13:36 GMT  
		Size: 1.2 MB (1163890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e795a0f73495ed60755df87924824d54f7f6c3e39e2290a6620b2292052515`  
		Last Modified: Thu, 03 Aug 2023 21:13:36 GMT  
		Size: 2.2 MB (2186719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2faaee2dedf1e580ff7534fb772d1338f4e9d765327fb972789b1b2799e6885b`  
		Last Modified: Thu, 03 Aug 2023 21:13:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cca000c6fef721df038acac5d75af1e5a0b225eeb9f585b656ff77e03bb8b30`  
		Last Modified: Thu, 03 Aug 2023 21:13:36 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:e44e0d5e538f2c9b96c690fff1ddb28d4803c23999f1d454965db93bbd687b6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7264425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91392764bb6d58165d856113b83126cace6414f5457df110974537188a7da7be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 03 Aug 2023 21:03:36 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 03 Aug 2023 21:03:38 GMT
RUN apk add --no-cache libssl1.1
# Thu, 03 Aug 2023 21:03:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 03 Aug 2023 21:03:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 03 Aug 2023 21:03:46 GMT
VOLUME [/spiped]
# Thu, 03 Aug 2023 21:03:46 GMT
WORKDIR /spiped
# Thu, 03 Aug 2023 21:03:46 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 03 Aug 2023 21:03:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 21:03:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29059dc293c00f54da752a558300b577b0437eae0d9b5f256f9a658105ca21ee`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351829a8bd360584cadfe089bec88f0a556d95f7cd39439affae43ea13c8a4b8`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 1.4 MB (1362700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39f438d5a167cd51de9296e034ad6a94ce4848c706dfb163b6d19c35c1c3432`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 2.6 MB (2570731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3702fb444a3ca3cc36e82826eec5dbdc01917e9ff3532bcf06e5f3f4f00e9745`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e20649f92b6732530e48c20749ec1bfc6c47e65b61a2c24d7acde959d9a463`  
		Last Modified: Thu, 03 Aug 2023 21:04:03 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:76e2f5658516698bd2c79af31214cb5e53d37d16e9ca35ab33d572b15e7036a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7111610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18845f8185f0983a9e0afddca9e50674f6617c27b10f8c6c58be257b7db0e1cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 22:33:22 GMT
ADD file:94bec00e2c0c7f47c81ec4355a29ca23a81b439797d037b1a5a455f36a25dab4 in / 
# Wed, 14 Jun 2023 22:33:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Aug 2023 20:38:34 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 03 Aug 2023 20:38:36 GMT
RUN apk add --no-cache libssl1.1
# Thu, 03 Aug 2023 20:38:36 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 03 Aug 2023 20:38:48 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 03 Aug 2023 20:38:48 GMT
VOLUME [/spiped]
# Thu, 03 Aug 2023 20:38:48 GMT
WORKDIR /spiped
# Thu, 03 Aug 2023 20:38:48 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 03 Aug 2023 20:38:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 20:38:49 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b3f50075abd13aad1cb7d8c1427aa59d7fcac88f3690d3f9c3efdbec80fd0856`  
		Last Modified: Wed, 14 Jun 2023 22:33:48 GMT  
		Size: 3.2 MB (3233951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6169fd23fe4cd58ce36a6e19e4d1705e39403046b69581c4beb6df320c50014a`  
		Last Modified: Thu, 03 Aug 2023 20:39:03 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ee2993a4cfc4228c2e41215de349210b7bad73f85a3de3acdfcc2732198893`  
		Last Modified: Thu, 03 Aug 2023 20:39:03 GMT  
		Size: 1.4 MB (1353894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e910bdbdc5fca470d5ebc8b40dd1013d2be9be872247bf70a3c600bc28bc818`  
		Last Modified: Thu, 03 Aug 2023 20:39:03 GMT  
		Size: 2.5 MB (2522029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2446a3a4f48a300a3cf71b09306f075c2c8594095c885c8aee46e5971f4afd9`  
		Last Modified: Thu, 03 Aug 2023 20:39:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debfa23a79889de3ef5d83cb87782630a42e92f5fd7dc4ac439f1f800df403b9`  
		Last Modified: Thu, 03 Aug 2023 20:39:03 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:b65da64e644ffa02fbf72d198f610d1a6c8f4b10bbe5560da5bfd0d1926d1e50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7269613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fa459337bbfd5e8164fa5e38f77829da9cab821842d4dd3c2a69480caf5297`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 15 Jun 2023 00:39:49 GMT
ADD file:694c636c0dd19fd01accbc189e4c1dc4d063952692c6e7eb26dce02a7adba833 in / 
# Thu, 15 Jun 2023 00:39:49 GMT
CMD ["/bin/sh"]
# Thu, 03 Aug 2023 21:18:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 03 Aug 2023 21:18:50 GMT
RUN apk add --no-cache libssl1.1
# Thu, 03 Aug 2023 21:18:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 03 Aug 2023 21:19:05 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 03 Aug 2023 21:19:06 GMT
VOLUME [/spiped]
# Thu, 03 Aug 2023 21:19:06 GMT
WORKDIR /spiped
# Thu, 03 Aug 2023 21:19:07 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 03 Aug 2023 21:19:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 21:19:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ffa4a466dbb8eebd7e7f25590a9df12390de9016abf82279c29c9a64aa76491a`  
		Last Modified: Thu, 15 Jun 2023 00:40:26 GMT  
		Size: 3.3 MB (3344781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66da6dd14e674d632df26db00ba6d390672a77f4cdd5be6234c1236ed71d2eed`  
		Last Modified: Thu, 03 Aug 2023 21:19:29 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513bf2ec7fd3547c8b964240c84d8ef032e8255e4b5fc7743dfd38032d127e39`  
		Last Modified: Thu, 03 Aug 2023 21:19:29 GMT  
		Size: 1.4 MB (1361736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ec5141bf787a8f4c14073100a1489396a1ae17945319a03699f40d9b01178a`  
		Last Modified: Thu, 03 Aug 2023 21:19:29 GMT  
		Size: 2.6 MB (2561358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932ad14b2cc424ab6ff91c42d6a0ed3805c9ebbec11766535e97beaed2426952`  
		Last Modified: Thu, 03 Aug 2023 21:19:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba8bd5b58d1158776b5df5d9fbaa5ecf4018b0a9a5b02c1cd8774681e465a75`  
		Last Modified: Thu, 03 Aug 2023 21:19:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:0c67d19c417d964e0fa15c5d365329a73cd5788e7c19e5f53a5b55fc870bc075
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6868272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d15792a85e1bb890a83d0944741e7eb83b2c5986e752741cfb30fbefc01c73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Thu, 03 Aug 2023 20:42:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 03 Aug 2023 20:42:59 GMT
RUN apk add --no-cache libssl1.1
# Thu, 03 Aug 2023 20:42:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 03 Aug 2023 20:43:08 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 03 Aug 2023 20:43:08 GMT
VOLUME [/spiped]
# Thu, 03 Aug 2023 20:43:08 GMT
WORKDIR /spiped
# Thu, 03 Aug 2023 20:43:08 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 03 Aug 2023 20:43:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 20:43:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc2b61c233457afa4e875ea1072a41c83d8960d39d9aca2b510f19196183762`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f91626c38ef7493a3034539c6f4b3cb05312bc7d9cd68767337fcb080f406f1`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 1.2 MB (1221498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed4c8e4aad25c008e64ac4daeaa49158ce6be40d29a2b375e44b58e884de05b`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 2.4 MB (2431542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a65a1664c27d1527d4df8a094a4579394f4a254569198914d63f38e9cdfb98`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e066b14d5da75b2e61d93352a2d245ef33cea8f6f7a4ef6015667d941a14debd`  
		Last Modified: Thu, 03 Aug 2023 20:43:29 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
