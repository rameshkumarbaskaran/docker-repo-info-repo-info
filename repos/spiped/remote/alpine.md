## `spiped:alpine`

```console
$ docker pull spiped@sha256:2a9b17d34333efdc72a05a909b3ce4208aa6b6676df21b8bc1f61d9a4431a2ef
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
$ docker pull spiped@sha256:d6e6dcfa6086494057f5f26469b25640bf3a9218b6cc4e845e510f611ffa60f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3038919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfeba803d4f72b630a199361799d83475c4f2faaf4727b042f4dae3eab17cc54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:06:12 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 29 Mar 2022 12:06:13 GMT
RUN apk add --no-cache libssl1.1
# Tue, 29 Mar 2022 12:06:13 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 12:06:23 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 29 Mar 2022 12:06:23 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 12:06:23 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 12:06:23 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 12:06:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 12:06:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e2f649ba68890eb48b23f0629d3f0bebfad8591eededff7d1bebbea5d2c299`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b9d24f2037910ca67089823983115eada5364357a69d3debbb44877fa797d9`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 7.8 KB (7787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dbbc9dfedadaeb9831ec97ca27a4c042f24c707f35418fcb5e658ac718d4b2`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 214.9 KB (214880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca650d236223d767382cf22a1841bc16d8b4d27ac027dff84b481bd8b1f3ed09`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901204d6acb74fe11b3b5004cdfd8be4d3e9d9cbab4ceeeb099898ff581d0388`  
		Last Modified: Tue, 29 Mar 2022 12:06:52 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:ae66fb10272b529530524084a214a11e65777dff6517d5a90d71357e60416246
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2830615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae9a0570520cf722d24d3a84685d936a04a06d1b8e35de44be52daca29219ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:24:39 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 29 Mar 2022 08:24:41 GMT
RUN apk add --no-cache libssl1.1
# Tue, 29 Mar 2022 08:24:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 08:25:01 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 29 Mar 2022 08:25:01 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 08:25:02 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 08:25:03 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:25:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:25:04 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc4ea1012b3262fa7706463586c4d41a0cf0a329238cbe52ea6d03bfbc07fae`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5659ae5d68adc8e4012f07c665ea352c4068ee821e83350f8bc165b6aea5583`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 7.8 KB (7774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf4925cebf49f63997a8c7389e423c3623dc4cd2e6c701e4282c664293e789b`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 199.2 KB (199158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eac1b140b33266f585c96310939c5cdbac7bde1fcbc0bd4e8cde9f9f0dd5171`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b13e602bdbc874391ee6aee0f8abffe1e74ee57061d9e1faed46aa76ad44a0`  
		Last Modified: Tue, 29 Mar 2022 08:25:35 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:189afc1c68703cff284e0c131d8d15c9c681d14a4542ddaf2c94693f232decc1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2629275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ea0583224ba3af43c489fca633bcb591704ff4ee8d4cc17c4c606062389b00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 03:14:52 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 24 Mar 2022 03:14:54 GMT
RUN apk add --no-cache libssl1.1
# Thu, 24 Mar 2022 03:14:55 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 24 Mar 2022 03:15:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 24 Mar 2022 03:15:13 GMT
VOLUME [/spiped]
# Thu, 24 Mar 2022 03:15:14 GMT
WORKDIR /spiped
# Thu, 24 Mar 2022 03:15:14 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 24 Mar 2022 03:15:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Mar 2022 03:15:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf5bdaf7a39a22f20503724a23944505c99126d9af994be53508ccc71c16eef`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b40ed26b860753759abe491128ce51dbc0afdbc0cef72b3008dd2e524328df6`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 7.8 KB (7780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae99502b872eb38bf1f4dfc80216174c88c1d79d9cfb8c5abbc39917c0302aad`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 192.7 KB (192697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe098a5d357775ae0a8f18cb457fc9fd6b78d74aa6a76cee1416c0e170ccbacb`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5c27b0616f94be998b0bc78862d22586f0954d06bd7b91579d0d4b0358b624`  
		Last Modified: Thu, 24 Mar 2022 03:16:10 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:c0d28956af21c9ad7d0e3d4cf972b301ea28efa0c8755d1ee62841b09754b0ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2933013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a11675ed63f0f0f4c5e2d5175c06bade440268d204f7a4b104eba50db3f998da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Wed, 30 Mar 2022 01:02:13 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 30 Mar 2022 01:02:15 GMT
RUN apk add --no-cache libssl1.1
# Wed, 30 Mar 2022 01:02:16 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 01:02:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 30 Mar 2022 01:02:35 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 01:02:36 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 01:02:38 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 01:02:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 01:02:39 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef7ee2c7f3dc7bcaf9752a844248d8127145ffd675ae5de72b4be177fc37cd5`  
		Last Modified: Wed, 30 Mar 2022 01:03:39 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c53830f06d1a108ac255dbff68c71fabc58723d0a42943fec7681cbebe653a`  
		Last Modified: Wed, 30 Mar 2022 01:03:38 GMT  
		Size: 7.8 KB (7751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1f94f19caf7b781c37e261530b5861447ecd5ab33d55ad4d2f12a932db1cf8`  
		Last Modified: Wed, 30 Mar 2022 01:03:39 GMT  
		Size: 207.2 KB (207237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b259955a7b787ff533a05f42050e5172ba829db902cac41506236e30a45be04e`  
		Last Modified: Wed, 30 Mar 2022 01:03:38 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29db0547b8fb18568f5c6616a8622211952741a2a93da0e86cb506b1ee4c941c`  
		Last Modified: Wed, 30 Mar 2022 01:03:39 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:768b79c1223f706478b3a0032c22112401fed0957e0cf316ba94683ee1ca7f36
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a79e381a48f0dd00366b8a561ef5f702f1a5b4d8602eb791f1546c342911984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:38:32 GMT
ADD file:8d3b249cd4cd9b2fb1888f3efcc06d39c2f56b4c25257ecee645c1be0146f7fd in / 
# Tue, 29 Mar 2022 00:38:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 10:44:36 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 29 Mar 2022 10:44:37 GMT
RUN apk add --no-cache libssl1.1
# Tue, 29 Mar 2022 10:44:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 29 Mar 2022 10:44:48 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 29 Mar 2022 10:44:49 GMT
VOLUME [/spiped]
# Tue, 29 Mar 2022 10:44:50 GMT
WORKDIR /spiped
# Tue, 29 Mar 2022 10:44:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 29 Mar 2022 10:44:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 10:44:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:134f45dc6b904419acf27b9807970f271117691bc67b963b86de8965db932175`  
		Last Modified: Tue, 29 Mar 2022 00:39:35 GMT  
		Size: 2.8 MB (2818926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b625a1ed487cfd98e806f31bc703a892a97d07f2a33c1657ad981d1072ba7f`  
		Last Modified: Tue, 29 Mar 2022 10:45:37 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02845a45e1b2d5e8e499c956acc9795a048bca98576e02146f9eff14e6cecadf`  
		Last Modified: Tue, 29 Mar 2022 10:45:37 GMT  
		Size: 7.8 KB (7750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8cfab4e949c3e8dd9bcd7085b355b7ffd0167d5edfeffb931188144796b6b3`  
		Last Modified: Tue, 29 Mar 2022 10:45:38 GMT  
		Size: 225.4 KB (225419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7240d8e736fdc883bfc41a6ac79d6b16dbf424902f57637e76a57fc498daac`  
		Last Modified: Tue, 29 Mar 2022 10:45:37 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5efcabfa8c561598869530135704b6302072794ecaaefe3cd2dff77e472af47`  
		Last Modified: Tue, 29 Mar 2022 10:45:37 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:d27c5eb0ad348fe2a50b65e808e4b825f0f479572187d81757b9a82ce2ad9e50
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3033662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1853309ab0785a26d0b48053b424c5b8c4ffd6367504032c68e3377b9fc92eba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:16:52 GMT
ADD file:9e7b65a431d59070abaadae56d9c3fc59c899af881939e4353b1f524b2bd5185 in / 
# Tue, 29 Mar 2022 00:16:55 GMT
CMD ["/bin/sh"]
# Wed, 30 Mar 2022 05:25:40 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 30 Mar 2022 05:25:50 GMT
RUN apk add --no-cache libssl1.1
# Wed, 30 Mar 2022 05:25:53 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 05:26:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 30 Mar 2022 05:26:24 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 05:26:28 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 05:26:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 05:26:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 05:26:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1c611bca4fa49cac5bc1e3826ad53fee85ed659d24bffcccd86c3f04be07339a`  
		Last Modified: Tue, 29 Mar 2022 00:18:26 GMT  
		Size: 2.8 MB (2811009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61e9d70cfabe50a7554945008b067920fffa673936b1b8c50f29cdbc07fad93`  
		Last Modified: Wed, 30 Mar 2022 05:27:51 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9a458bb0005f54d005e938aa01a6aeeb1d7c48486de6811d1c16a9846b1239`  
		Last Modified: Wed, 30 Mar 2022 05:27:51 GMT  
		Size: 7.8 KB (7774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8c858ba1f6886855b0312ec6b3618c916bea4577c858d028e6709d67f05939`  
		Last Modified: Wed, 30 Mar 2022 05:27:51 GMT  
		Size: 213.1 KB (213149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d4e4cb20d1bd858c134eae12aac2cab24001fbae386ee7f84b1e8dc6c6ef76`  
		Last Modified: Wed, 30 Mar 2022 05:27:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cb5033835d271b66d87c37a113ae41ee09c6b1c5b462196462cb06687e3352`  
		Last Modified: Wed, 30 Mar 2022 05:27:51 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:c25c47af1a6bc11637de15ec17dad117ad78343cf7347c265f1e56f0e4b3a414
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2811657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97239b742fae078cff3e290263aa752534ee95461d5f5a32fd585ee92dcdf5e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 29 Mar 2022 00:41:32 GMT
ADD file:75e6f1cb0cdf63de14d99f8419ce47d61e295300299c18b08bd484dff0da4e93 in / 
# Tue, 29 Mar 2022 00:41:32 GMT
CMD ["/bin/sh"]
# Wed, 30 Mar 2022 02:17:37 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 30 Mar 2022 02:17:37 GMT
RUN apk add --no-cache libssl1.1
# Wed, 30 Mar 2022 02:17:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 30 Mar 2022 02:17:43 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 30 Mar 2022 02:17:43 GMT
VOLUME [/spiped]
# Wed, 30 Mar 2022 02:17:43 GMT
WORKDIR /spiped
# Wed, 30 Mar 2022 02:17:43 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 30 Mar 2022 02:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 02:17:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2c33ece150b7a4954636e49b807bdf240c422de7a78f45728d2fcdb7c96d14a3`  
		Last Modified: Tue, 29 Mar 2022 00:44:03 GMT  
		Size: 2.6 MB (2600441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e144ceffef75cc7c2c1c03a85a5beb968414bdf4a4c7bf32a7e80bb4867085`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd8228374fcc60d9ce3f830403b582c951b61d5f290da2cdc5d46470960e122`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 7.8 KB (7785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7189dcfd4895b30653e04d921ea51db9d3cf616a80caef0b9eb4b2a478a0a0`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 201.7 KB (201697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24add8a228de11738a6e3ffc4d1659680ba2a1ea46ecd69f23ae7d8cfb62cc17`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925172ba0226c4330bc068f3815476dbdb5a96c19ef9cdf4f7a51be59fd06c63`  
		Last Modified: Wed, 30 Mar 2022 02:18:20 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
