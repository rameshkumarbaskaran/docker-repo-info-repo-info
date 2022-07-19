## `spiped:alpine`

```console
$ docker pull spiped@sha256:cfbbfd8ad1afbfc582473b1e7390b61b4f09963deb60c3e0beeebd159f04fec4
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
$ docker pull spiped@sha256:960558dde1fffd85012e80768bb5fb6b5ce16f56a6d8ba36c4eb4871b3d7ad20
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3022913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f255584cbbb67f7dca6e7842e9ba534deb82bcc7d271ddb94d37ca749d4143`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 02:58:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 19 Jul 2022 02:58:45 GMT
RUN apk add --no-cache libssl1.1
# Tue, 19 Jul 2022 02:58:45 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 19 Jul 2022 02:58:56 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 19 Jul 2022 02:58:56 GMT
VOLUME [/spiped]
# Tue, 19 Jul 2022 02:58:56 GMT
WORKDIR /spiped
# Tue, 19 Jul 2022 02:58:56 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 19 Jul 2022 02:58:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 02:58:56 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ccfd605bd789873358dddbc12507c07697196241ef12b229daede89fede305`  
		Last Modified: Tue, 19 Jul 2022 02:59:13 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91eb30e4056e3cf1d260026125f2c0969702f9eda398caa33c77fcc1efb6da0f`  
		Last Modified: Tue, 19 Jul 2022 02:59:13 GMT  
		Size: 7.7 KB (7739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeedfc703c38a2268ccf7afedcb792b89f9b7d7ff21f541ba671f04052a7f654`  
		Last Modified: Tue, 19 Jul 2022 02:59:13 GMT  
		Size: 214.6 KB (214629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e96340c6dfa203988333004e74c69a13274414e98de4322ea0c789ad7df42c9`  
		Last Modified: Tue, 19 Jul 2022 02:59:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383211380910b0d4fcc33212392f07b13de80297232cd9da3c25f3a80b67dd34`  
		Last Modified: Tue, 19 Jul 2022 02:59:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:78d7c6b26405f2ccec387dbd5f5f8380bfac8922c0cde017bf83199a7c93de3f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2815244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0975d891cb5d986fa371064357d538cff8e162c0dbcbeb412b87e765eea2bee6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 04:28:52 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 19 Jul 2022 04:28:54 GMT
RUN apk add --no-cache libssl1.1
# Tue, 19 Jul 2022 04:28:55 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 19 Jul 2022 04:29:15 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 19 Jul 2022 04:29:16 GMT
VOLUME [/spiped]
# Tue, 19 Jul 2022 04:29:16 GMT
WORKDIR /spiped
# Tue, 19 Jul 2022 04:29:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 19 Jul 2022 04:29:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 04:29:18 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7794ac6005a3d1042ca428fddd078ac26956535628f13a1901b8aaf3986288d`  
		Last Modified: Tue, 19 Jul 2022 04:29:51 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a8bbac389bb4b97ec5a6d16185ce572d9e89d45f67d819d9eee81fee855e51`  
		Last Modified: Tue, 19 Jul 2022 04:29:51 GMT  
		Size: 7.7 KB (7735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382b8ab18f4e21efbd2668e38088fe5d0a5e016a65d8f3845cfa386c1d974999`  
		Last Modified: Tue, 19 Jul 2022 04:29:51 GMT  
		Size: 199.3 KB (199338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940073d33e787162c6aa336ae5ef93efdd6641a3dc59e5d4a0eb01f0c24aeecf`  
		Last Modified: Tue, 19 Jul 2022 04:29:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf4811d369ed3ed91ee23a134ab53b91888e93efc80c38c6c15d44a1ec8e9de`  
		Last Modified: Tue, 19 Jul 2022 04:29:51 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:acc8ca060038077aa20644d95dfd50f3a9faa59990d2318895033343f94456eb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2614203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa4570c887e85e41ae28860d1797be642647270341c2b31a2d07268170d3d18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 May 2022 18:57:46 GMT
ADD file:72698cc08524b911ebaacf992490707e5a951ddd2fe6edb3fb598e9dc7155049 in / 
# Mon, 23 May 2022 18:57:47 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 23:57:01 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 24 May 2022 23:57:03 GMT
RUN apk add --no-cache libssl1.1
# Tue, 24 May 2022 23:57:03 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 24 May 2022 23:57:23 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 24 May 2022 23:57:24 GMT
VOLUME [/spiped]
# Tue, 24 May 2022 23:57:24 GMT
WORKDIR /spiped
# Tue, 24 May 2022 23:57:25 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 24 May 2022 23:57:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 May 2022 23:57:26 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6366ba92f08e2418e90171f1e34bd86ecd50fdc95953b3f33b8943c143518eca`  
		Last Modified: Mon, 23 May 2022 18:59:17 GMT  
		Size: 2.4 MB (2411648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744a106e187f9790be6dbdde860ada60aab7e95bae779540c813da16ce184ea7`  
		Last Modified: Tue, 24 May 2022 23:58:19 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8f51295340b65e165fffa3de719118e625ca751a7c465a96dee14a0441de72`  
		Last Modified: Tue, 24 May 2022 23:58:19 GMT  
		Size: 7.7 KB (7717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1da9fdb3c39499af6413db4aeed00e8577a949c49968ffd86c20f438118a88`  
		Last Modified: Tue, 24 May 2022 23:58:19 GMT  
		Size: 193.1 KB (193098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b416966b1e14463ce73c56ecba5fd804f4c565b4d781199f3b02247ffdf8e7`  
		Last Modified: Tue, 24 May 2022 23:58:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1016107cea29ba85ecc25a6bba5c5c3494ef9ed31194cc5e7b6ea8add7ef4a`  
		Last Modified: Tue, 24 May 2022 23:58:19 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b4e4831c1382ba6191159248fbf92a052b843dd76ffb3e5ab9590a9b50033a72
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2911791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fa91c14a7ba129a596b0eaffb3c321c3d4c509db24ecf103535d7fb2bd6598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 03:11:40 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 19 Jul 2022 03:11:41 GMT
RUN apk add --no-cache libssl1.1
# Tue, 19 Jul 2022 03:11:42 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 19 Jul 2022 03:11:53 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 19 Jul 2022 03:11:54 GMT
VOLUME [/spiped]
# Tue, 19 Jul 2022 03:11:55 GMT
WORKDIR /spiped
# Tue, 19 Jul 2022 03:11:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 19 Jul 2022 03:11:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 03:11:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a8e96b71a119a7753279fa24fc1b097b559f365c0d74c928ec0827108be3ac`  
		Last Modified: Tue, 19 Jul 2022 03:12:25 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5b7ffd6e7e16898220160e758a91b7ae6e5fa7763e22b1f929570b0e877432`  
		Last Modified: Tue, 19 Jul 2022 03:12:25 GMT  
		Size: 7.7 KB (7708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54764cd29a52b45365923ab1e756750d07330c69ea57b318f8f4b2660940a1fa`  
		Last Modified: Tue, 19 Jul 2022 03:12:25 GMT  
		Size: 207.7 KB (207685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2841c7d2c1268e60c21c01e69c10868bef688cc32f57dbe883e975040d003f`  
		Last Modified: Tue, 19 Jul 2022 03:12:25 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b456f54f4f08db25a2b70f3ecd5b9a2273937e824ae2e3d919c7f3d8b31102a2`  
		Last Modified: Tue, 19 Jul 2022 03:12:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:bd3d4904f8e1d52ce4a28eb847bc57f54248490fc15e9ac6e88cca4566f2bbec
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc7cf0e554fe461e7d95534758c990b4c5f507ac6912d08de0ab5c7192d5a4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 18 Jul 2022 20:38:19 GMT
ADD file:be69b7550bf861d8fb12bdbe1edf3a0d2519a6a4da61bd04858b6258ffbf48a7 in / 
# Mon, 18 Jul 2022 20:38:19 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 00:52:10 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 19 Jul 2022 00:52:11 GMT
RUN apk add --no-cache libssl1.1
# Tue, 19 Jul 2022 00:52:12 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 19 Jul 2022 00:52:24 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 19 Jul 2022 00:52:25 GMT
VOLUME [/spiped]
# Tue, 19 Jul 2022 00:52:26 GMT
WORKDIR /spiped
# Tue, 19 Jul 2022 00:52:28 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 19 Jul 2022 00:52:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 00:52:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5d7f927419794ebb7496ac38b0659686317b2d2fac7252a4a0d40d43d5fdd662`  
		Last Modified: Mon, 18 Jul 2022 19:09:22 GMT  
		Size: 2.8 MB (2802334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8be475f4c97c2b6a50a82b2cda5d04dcf3be627667431e283146f5ef2467cf2`  
		Last Modified: Tue, 19 Jul 2022 00:52:57 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccf382b13c23a3fe33bbd2b36efca3ac3493d37bbda16a50f5df1a18b997e00`  
		Last Modified: Tue, 19 Jul 2022 00:52:57 GMT  
		Size: 7.7 KB (7711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7cd3baa7c17abca3fa3c456474f8fe1b0aa45d19cba81de21b85554722608e`  
		Last Modified: Tue, 19 Jul 2022 00:52:58 GMT  
		Size: 225.1 KB (225138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1a6c9df0a41f62802eec16036b66a1513b5b158004c13839da1b3ba266ac38`  
		Last Modified: Tue, 19 Jul 2022 00:52:57 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f06336cb65e863eccc316001a0037fbb6fc5dd05ff03301c9a513d42af9128`  
		Last Modified: Tue, 19 Jul 2022 00:52:58 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:394770c1c3e52c18b2e060896dc946a7de8c0581c1691fe3a2458c6442d51071
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45dd65bd18433f8227345eb1bc628c92fb777cc4d5e9e790835ba272eaadec4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 23 May 2022 19:16:51 GMT
ADD file:6a5450c8a7cee3ceda59e7cb350c54df4139b0f7b7cf49c8b31bb9c01646c3cd in / 
# Mon, 23 May 2022 19:16:53 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 19:50:10 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 24 May 2022 19:50:18 GMT
RUN apk add --no-cache libssl1.1
# Tue, 24 May 2022 19:50:20 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 24 May 2022 19:50:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 24 May 2022 19:50:42 GMT
VOLUME [/spiped]
# Tue, 24 May 2022 19:50:47 GMT
WORKDIR /spiped
# Tue, 24 May 2022 19:50:48 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 24 May 2022 19:50:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 May 2022 19:50:56 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d3deabf2a506ef6f5fa7c2a68bf27047574cef9908b30a97ff2d01ae539b089a`  
		Last Modified: Mon, 23 May 2022 19:09:13 GMT  
		Size: 2.8 MB (2789745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d245add1998dabc480629fde1ae678cfbb96f740737e4acede363c37eda348`  
		Last Modified: Tue, 24 May 2022 19:51:36 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea94be815996b73043903da4f60b4ea3573e9689c5b3b1b0348ef5ef54fe25b`  
		Last Modified: Tue, 24 May 2022 19:51:36 GMT  
		Size: 7.7 KB (7727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25cc9d25fe567c300c07c50cb1d341544a9751b92d44874cef5399d1beee0aa`  
		Last Modified: Tue, 24 May 2022 19:51:36 GMT  
		Size: 213.7 KB (213687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b003e2ac252266dcd49f568ddc62ed5a04668bc0655e7cd74521a21c0089eb`  
		Last Modified: Tue, 24 May 2022 19:51:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed434cd18f8048c2624c1d26c27721d4ce3e46b39d5d9adcbeec4733e3954ff`  
		Last Modified: Tue, 24 May 2022 19:51:36 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:5abc9d546636b6670ca2c300303d57c59e066f9b42af71ffc12fce775274b2b8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2792283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9891884c555841cd06fd9c1a3608fcb75e6ab6cdb389c07e53fed03b6bb500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 18 Jul 2022 20:41:35 GMT
ADD file:deaa573cd61e07709846a5300fb627a8610e9754129c085ed483ff8897d0c002 in / 
# Mon, 18 Jul 2022 20:41:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 05:40:59 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 19 Jul 2022 05:41:01 GMT
RUN apk add --no-cache libssl1.1
# Tue, 19 Jul 2022 05:41:02 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 19 Jul 2022 05:41:11 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 19 Jul 2022 05:41:11 GMT
VOLUME [/spiped]
# Tue, 19 Jul 2022 05:41:12 GMT
WORKDIR /spiped
# Tue, 19 Jul 2022 05:41:13 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 19 Jul 2022 05:41:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 05:41:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5f1840d5bacf4162a87f497e22d94bce946e660bdfce8eeefcbf7bd0beb193f3`  
		Last Modified: Mon, 18 Jul 2022 20:42:36 GMT  
		Size: 2.6 MB (2580798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6993821da2e7957193713709542cca3a229ed17d3d859ca823a7ef4e38b011`  
		Last Modified: Tue, 19 Jul 2022 05:41:47 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09df37c5f8ac9a24ba5f55d4d545b4835141a55e5f9ecd71f8b936809f8fddd3`  
		Last Modified: Tue, 19 Jul 2022 05:41:47 GMT  
		Size: 7.7 KB (7742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c64cd2f7e97c8f03ec8ef34a7ba77e455842217cfcc3e9c6816f56ea8108b6`  
		Last Modified: Tue, 19 Jul 2022 05:41:47 GMT  
		Size: 202.0 KB (202009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ec9f775174ce04ae9cf626a975e42a1f50926f1d9f9cdecf513cdb1514809b`  
		Last Modified: Tue, 19 Jul 2022 05:41:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b76904392c2be02eeefc2c55db23094f8f3578806838b317aec9d39ec86abd`  
		Last Modified: Tue, 19 Jul 2022 05:41:47 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
