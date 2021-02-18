## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:28e5512902fff95574d6297dfde921d98543a103c04b6fcabbae742f24ee6996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `spiped:1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:835d7b06f38b14f3497dfa8ef3a3387976759c1d4da641bee7b66ab2614327e7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3032332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883c5cce06c38a0f7a19e769ba33df23b5104eae4f2f2529c4b6c7d2540dd71a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 28 Jan 2021 23:19:38 GMT
ADD file:0e2d487cd80773e947c8aae6daad3d565b7bb019a954af2b8bff188681c00d81 in / 
# Thu, 28 Jan 2021 23:19:38 GMT
CMD ["/bin/sh"]
# Sat, 13 Feb 2021 00:10:20 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 13 Feb 2021 00:10:23 GMT
RUN apk add --no-cache libssl1.1
# Sat, 13 Feb 2021 00:10:23 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 00:11:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 13 Feb 2021 00:11:03 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 00:11:03 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 00:11:04 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 00:11:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 00:11:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4c0d98bf9879488e0407f897d9dd4bf758555a78e39675e72b5124ccf12c2580`  
		Last Modified: Thu, 28 Jan 2021 23:20:08 GMT  
		Size: 2.8 MB (2811321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ada2cbdd62e07ee40d2f05c48cbb06a172e5cde247cb27defa9146e342ee24`  
		Last Modified: Sat, 13 Feb 2021 00:11:39 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0809851ee6dd7d72995918c73439754a4ff183f0aa0f142407150e9c75130e`  
		Last Modified: Sat, 13 Feb 2021 00:11:39 GMT  
		Size: 7.0 KB (7049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814bb6e0e86dd762b94f3a86fe4ea3dcac961064cb970ae9852a2389eab5bc72`  
		Last Modified: Sat, 13 Feb 2021 00:11:39 GMT  
		Size: 212.3 KB (212296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a22052f5d37047c574696d71e90ee4fc969f40189329fc130b69fd39cd39ab`  
		Last Modified: Sat, 13 Feb 2021 00:11:39 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db107fe5f9add27475633bd978bdbc7404ae29a7f594d3a2e5aaff7ac44b63db`  
		Last Modified: Sat, 13 Feb 2021 00:11:39 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:a4eae04b6b59fa1465464612d582ab381eae7d0fd508089e99a2d9642d83d589
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2833085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa0d64ae65bd0aed1fae629f2219ead07f2df4d55520aa67fa73701725be6a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:08:57 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 01:09:00 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 01:09:00 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 01:09:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 01:09:29 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 01:09:30 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 01:09:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 01:09:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 01:09:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56478beef0e3bf335b5084e01725a07c247a0df1c2ae4d79a9b37d8d7c1d8c6b`  
		Last Modified: Thu, 18 Feb 2021 01:09:52 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09965b504ec1fcd372f0f74e2de05a28c8cfc7546e5f9abac13b9969308fffc7`  
		Last Modified: Thu, 18 Feb 2021 01:09:52 GMT  
		Size: 7.1 KB (7053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca4d95213096352ef307626e2b9b743cd56d9e041d9bad475b082bdda7cd8fb`  
		Last Modified: Thu, 18 Feb 2021 01:09:52 GMT  
		Size: 202.3 KB (202264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448a184417c9c40109716c2bf6eb26c63873720e7d14b4e852ffe5da738e4871`  
		Last Modified: Thu, 18 Feb 2021 01:09:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb506bcaf6432a313382d4600f3ae27df33c73cfc17f1d9615fee63b17b95c3`  
		Last Modified: Thu, 18 Feb 2021 01:09:51 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e91e8dfd1379e2029d929ab8d21b5b7cacda7a1ac496cecd8c37417d9d48e708
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8d028bc188683c4af6ec6c0afa9cf33c5e88a0569d98c54eebd1e02b4b78b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:11:51 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 01:11:53 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 01:11:55 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 01:12:23 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 01:12:24 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 01:12:25 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 01:12:26 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 01:12:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 01:12:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdfb8a36c4de90dba3240099eb1d0348f8627ed1bc968f7e4271d75b265ccf2`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ab61a202577acd7159b1a345fcb97d20c63e42a6a170dfe22345caa4af688f`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374409fe6217df96932998b712912ebad072a21d4d4e7817b70b6dbb23d0f0a3`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 195.5 KB (195539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592de5c2b9cc50ddf43d871cb052d160ae2dc235c136a1731e45e1cf529b7b80`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562929d72557b487b48b0dcc0ca66188d993a95431efb6ba6e82ecece7035616`  
		Last Modified: Thu, 18 Feb 2021 01:12:49 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b0ca7cbad488b0fcb44506f1c6c65ae77f5573dc072c30c390b75e29a9d2c64c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2924800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffde3212b34beb453841e58f5ca6bcdbd5dee1c658ff1861926718f1f9c5499`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:23:27 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 01:23:30 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 01:23:31 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 01:24:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 01:24:05 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 01:24:06 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 01:24:07 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 01:24:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 01:24:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991947bc8299281c0212c4f9312423d52074ad210f1eab639db0f6df247937b2`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a8e0ee83f949ca3f11000f9df3c4b551cff205fc9d645ed6aa3c13d4b41a14`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 7.1 KB (7059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da8757762737713d5ff919736307c7a18ea61e4e68e7a6f051974461de14f8a`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 204.4 KB (204440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a12b508a6a8ce19fd3eee0367c035a60aebd09e422b169e7e3acb5ec2cc376`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd46a081f7acce468799a1512f765f8f304e396d48824de8d10a33c1e6416619`  
		Last Modified: Thu, 18 Feb 2021 01:24:34 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:4960ec29bb9ef335500e75f0083cd0266fe301739478d22c7eac9fd71a2a0ab3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3049596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4479a0b49914c6027a4470086fafeec21241b4ec58e6a9b2c913d6bca2d22ae3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 28 Jan 2021 23:38:31 GMT
ADD file:c0e9ea135d66ad6504c77915a7a48b3bead60892d155d3258b746cb4945981c0 in / 
# Thu, 28 Jan 2021 23:38:31 GMT
CMD ["/bin/sh"]
# Sat, 13 Feb 2021 00:59:25 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 13 Feb 2021 00:59:26 GMT
RUN apk add --no-cache libssl1.1
# Sat, 13 Feb 2021 00:59:26 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 00:59:50 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 13 Feb 2021 00:59:50 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 00:59:50 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 00:59:51 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 00:59:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 00:59:51 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3fea00a81341ce917db671eb3ad24ef5750cb6928b7f760e3ce4dab619eeb1fa`  
		Last Modified: Thu, 28 Jan 2021 23:39:02 GMT  
		Size: 2.8 MB (2817627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7723c1203294add77f79b9f3aafc10eda8572905ac503c7f5a0b2d49e488ed`  
		Last Modified: Sat, 13 Feb 2021 01:00:17 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ce806478241c0f699afc38824da58e636c67df1e42986b00e0984769077c20`  
		Last Modified: Sat, 13 Feb 2021 01:00:18 GMT  
		Size: 7.0 KB (7042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85bd8240d52bc7724188c29d5ef4610ea463be9b970b707886910547d6edbf85`  
		Last Modified: Sat, 13 Feb 2021 01:00:18 GMT  
		Size: 223.3 KB (223257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9209f92f3e8326cecdb9a9e84435c267898cd9258f7a6ab104632b2653a905c9`  
		Last Modified: Sat, 13 Feb 2021 01:00:18 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40d0142f6f8ec7c14fc1fbc2ea71a8ccf3e8f67ba870450c9b5601ea7a710ca`  
		Last Modified: Sat, 13 Feb 2021 01:00:18 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:33c381176119d7660214d2991cb4a2ccfa254db448220f4df615870f3a84fc66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3042301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50abb8300ea994b3e481699c0929ed73d9007f8f85432f87cc74afeda4045cf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 28 Jan 2021 23:55:50 GMT
ADD file:b14fd5f3f7fcd16e2b4ec6932d3e9c07c7400c577cee5fdcb88b0795a70a7bfb in / 
# Thu, 28 Jan 2021 23:55:52 GMT
CMD ["/bin/sh"]
# Sat, 13 Feb 2021 02:34:34 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 13 Feb 2021 02:34:44 GMT
RUN apk add --no-cache libssl1.1
# Sat, 13 Feb 2021 02:34:49 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 13 Feb 2021 02:35:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 13 Feb 2021 02:35:24 GMT
VOLUME [/spiped]
# Sat, 13 Feb 2021 02:35:28 GMT
WORKDIR /spiped
# Sat, 13 Feb 2021 02:35:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 13 Feb 2021 02:35:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Feb 2021 02:35:43 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f3b94a1d8d591af02f1b419642bee91066ecbb9c65099d6903deed310fd1c2ff`  
		Last Modified: Thu, 28 Jan 2021 23:56:32 GMT  
		Size: 2.8 MB (2812517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e118e9785a8eefb11035770ba3f016fd6735fff79024dddf90bd04b98150410`  
		Last Modified: Sat, 13 Feb 2021 02:36:23 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c02326e8246063ab1916219ed81aa1f954ca993bc3590ef06d7b6748d815977`  
		Last Modified: Sat, 13 Feb 2021 02:36:23 GMT  
		Size: 7.1 KB (7059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc9abddce71df5b7d8a16936252ae190e82033deb046797cf5341fff77f026e`  
		Last Modified: Sat, 13 Feb 2021 02:36:23 GMT  
		Size: 221.0 KB (220996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d1ec7b1f9be796457a3f27e5d1d7644cac7c122fd210e179931e04dbc0e7ad`  
		Last Modified: Sat, 13 Feb 2021 02:36:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce293f6c247be36cea3048f53a9ad45fe1640112b6b234e232b79e69a9f1efae`  
		Last Modified: Sat, 13 Feb 2021 02:36:23 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:84eb47cc2762f89ced7dac3994d19fd866beb6d7edf1ce8ab89075b9e965894d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2816196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931664821077383b17442b73db19b44e519072a6c656d5d071fb35e73856df97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:38:50 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 18 Feb 2021 00:38:52 GMT
RUN apk add --no-cache libssl1.1
# Thu, 18 Feb 2021 00:38:53 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 18 Feb 2021 00:39:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 18 Feb 2021 00:39:08 GMT
VOLUME [/spiped]
# Thu, 18 Feb 2021 00:39:08 GMT
WORKDIR /spiped
# Thu, 18 Feb 2021 00:39:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 18 Feb 2021 00:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 00:39:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e67382afc352947106dc6c166d812d215925da3b965c062a036336a3b0aa2eb`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c645ec8297a3a8a63091e1f2c1a83b18b9649d25e3a0c009ce595fa0f9ab2d01`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 7.0 KB (7048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7ec4619ba6c3e05a4793024f6fc431995072c29d096c87ef92b93acf2fe0ff`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 205.0 KB (205040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c09c00004fe0ea62d74d7d3cd3c7252e1586cb457fbd2d87147cc88c27d799`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8302a33625b439acc9b2f489b57ea79b1d58f06bf3ae086534f499d28e4f951`  
		Last Modified: Thu, 18 Feb 2021 00:39:28 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
