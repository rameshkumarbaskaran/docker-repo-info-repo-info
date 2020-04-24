## `spiped:alpine`

```console
$ docker pull spiped@sha256:2c6fe00e5c68d782286286f5ce6e67c5b5d182cdf886ea4fc8e85f1ff5af38e8
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

### `spiped:alpine` - linux; amd64

```console
$ docker pull spiped@sha256:1670c0bedf4cde29b471b07e37cf2ecac7572eab7390e6f319e99a9d518d6c64
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2892533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7388fe097949fecec27fc47569b9454e25d605fa8b3bbad998579bb56613405`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 19:24:41 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 Apr 2020 19:24:42 GMT
RUN apk add --no-cache libssl1.1
# Fri, 24 Apr 2020 19:24:42 GMT
ENV SPIPED_VERSION=1.6.1
# Fri, 24 Apr 2020 19:24:42 GMT
ENV SPIPED_DOWNLOAD_URL=https://www.tarsnap.com/spiped/spiped-1.6.1.tgz
# Fri, 24 Apr 2020 19:24:42 GMT
ENV SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 24 Apr 2020 19:24:58 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "$SPIPED_DOWNLOAD_URL" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 24 Apr 2020 19:24:58 GMT
VOLUME [/spiped]
# Fri, 24 Apr 2020 19:24:58 GMT
WORKDIR /spiped
# Fri, 24 Apr 2020 19:24:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 Apr 2020 19:24:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 19:24:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89008d600e9081fb81d2d7e8e6aa8507c9687b3dd3e56b2a17403caf42853ce7`  
		Last Modified: Fri, 24 Apr 2020 19:25:11 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646675b599220309e2ada934f30d0d976b4cd958316483de7cc5991e055ce61b`  
		Last Modified: Fri, 24 Apr 2020 19:25:12 GMT  
		Size: 6.3 KB (6334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87611a6ca8113a67cc77df7f11722a5925c0fa06ded08127f386d921e262d47d`  
		Last Modified: Fri, 24 Apr 2020 19:25:11 GMT  
		Size: 88.9 KB (88917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6389f58338eae962a77c80f2c6a0ffd8f52eb490cd1902c8b333da59a1c46faa`  
		Last Modified: Fri, 24 Apr 2020 19:25:11 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b86813460026159fc213df32cdfda9c6bbdcc1e832029ce95c99f30f247e676`  
		Last Modified: Fri, 24 Apr 2020 19:25:12 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3c0350ac5d5cd7aaf3d93d8f3f7d1e9d1c0888b16731da96a22ccb20b49b531f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2d7b34485f1998f41c45c273be804816dae86f4496e8528867fe3784159e7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:35 GMT
ADD file:ef75120295e25a8e67c5ef378df2cf4ce9f7b83b44709452fcaf247b54fabd16 in / 
# Thu, 23 Apr 2020 15:51:36 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:35:07 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 23 Apr 2020 22:35:09 GMT
RUN apk add --no-cache libssl1.1
# Thu, 23 Apr 2020 22:35:10 GMT
ENV SPIPED_VERSION=1.6.1
# Thu, 23 Apr 2020 22:35:10 GMT
ENV SPIPED_DOWNLOAD_URL=https://www.tarsnap.com/spiped/spiped-1.6.1.tgz
# Thu, 23 Apr 2020 22:35:11 GMT
ENV SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Thu, 23 Apr 2020 22:35:37 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "$SPIPED_DOWNLOAD_URL" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Thu, 23 Apr 2020 22:35:37 GMT
VOLUME [/spiped]
# Thu, 23 Apr 2020 22:35:38 GMT
WORKDIR /spiped
# Thu, 23 Apr 2020 22:35:39 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 23 Apr 2020 22:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 22:35:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e745d1dc1c9e0be26166278da7632765ca98fa1be8179a7cc440b3bdc5671860`  
		Last Modified: Thu, 23 Apr 2020 15:52:15 GMT  
		Size: 2.6 MB (2572512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1b8c67b45978a638cfe09240ed99c3f92f6ec5ed90fdc3228be33d65aba65e`  
		Last Modified: Thu, 23 Apr 2020 22:35:50 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc5b5c9a3c98738e9c97f8a355f660e8b630466790fce376b6fa394efa65762`  
		Last Modified: Thu, 23 Apr 2020 22:35:51 GMT  
		Size: 6.3 KB (6326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13e59f61c9a8509e3813070d46870440778325c0855dfd63a22bd87813428e1`  
		Last Modified: Thu, 23 Apr 2020 22:35:51 GMT  
		Size: 74.9 KB (74941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9a0727cd4b0cd75dd888a9ca44cd03adc1969d7e1861ed490045780002ac44`  
		Last Modified: Thu, 23 Apr 2020 22:35:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857bf6c5552222716711317624492f63113effd58dc10e975f74f275444b8baa`  
		Last Modified: Thu, 23 Apr 2020 22:35:50 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:a75d2b4c484e71a83bd1752e91d1d25f30799c3ee1430494e83268154edc9b4f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa554807a467b5e96447049fcb13bc6e7fee126058733f0cc24172beb312732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:44 GMT
ADD file:dabd2c1328a46961a58e93557d1039d6b98775cbdfe48ce875c109bb74615cb1 in / 
# Thu, 23 Apr 2020 22:04:45 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:14:59 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 Apr 2020 04:15:02 GMT
RUN apk add --no-cache libssl1.1
# Fri, 24 Apr 2020 04:15:02 GMT
ENV SPIPED_VERSION=1.6.1
# Fri, 24 Apr 2020 04:15:03 GMT
ENV SPIPED_DOWNLOAD_URL=https://www.tarsnap.com/spiped/spiped-1.6.1.tgz
# Fri, 24 Apr 2020 04:15:04 GMT
ENV SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 24 Apr 2020 04:15:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "$SPIPED_DOWNLOAD_URL" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 24 Apr 2020 04:15:30 GMT
VOLUME [/spiped]
# Fri, 24 Apr 2020 04:15:31 GMT
WORKDIR /spiped
# Fri, 24 Apr 2020 04:15:32 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 Apr 2020 04:15:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 04:15:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ad20c94522902b824bd9ea4e65dc1cba24dca4fdadd5728ed7446c0f4550d1ff`  
		Last Modified: Thu, 23 Apr 2020 22:05:22 GMT  
		Size: 2.4 MB (2378640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb1adea1516ec3f4e151236f979a79b04121d2b8fab476668918b0c680a98aa`  
		Last Modified: Fri, 24 Apr 2020 04:15:49 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72db7e58e30a264f15b4593c5ff6af5481ad577f3da660d4dc16c83b72e77176`  
		Last Modified: Fri, 24 Apr 2020 04:15:49 GMT  
		Size: 6.3 KB (6340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e868fb481151f8f3f73d24c647733c3ecf7b413ced859c1a8fd7a819cc2fdd3`  
		Last Modified: Fri, 24 Apr 2020 04:15:49 GMT  
		Size: 68.1 KB (68094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a80e3146db25b624154d0900194778383ebdf35898331c684fefe3222eaa9f8`  
		Last Modified: Fri, 24 Apr 2020 04:15:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31aa835c2e31ed87aff90e07c38109e24a4e822a0676b4aba91d60519cc17de6`  
		Last Modified: Fri, 24 Apr 2020 04:15:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:8f2a62b811f84b08b1fe7e18a3fb6dcd379bfca73eda2eee53048c7bc3d3553e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2808833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bccfc824137404361e6033e1ef17ffc282e128ab855d4f22a8eecf2794b77701`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:52 GMT
ADD file:75529f7e83edb6d0457a3b8bbfe33d4e3a12f339c5ace517d0f52dbedd9a146b in / 
# Fri, 24 Apr 2020 00:14:53 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:13:10 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 Apr 2020 12:13:12 GMT
RUN apk add --no-cache libssl1.1
# Fri, 24 Apr 2020 12:13:13 GMT
ENV SPIPED_VERSION=1.6.1
# Fri, 24 Apr 2020 12:13:14 GMT
ENV SPIPED_DOWNLOAD_URL=https://www.tarsnap.com/spiped/spiped-1.6.1.tgz
# Fri, 24 Apr 2020 12:13:14 GMT
ENV SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 24 Apr 2020 12:13:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "$SPIPED_DOWNLOAD_URL" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 24 Apr 2020 12:13:40 GMT
VOLUME [/spiped]
# Fri, 24 Apr 2020 12:13:41 GMT
WORKDIR /spiped
# Fri, 24 Apr 2020 12:13:42 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 Apr 2020 12:13:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 12:13:43 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b038bcb63e9c8905cc879c957302f686a9b43f24a18dcfc4186ab236ddf04cad`  
		Last Modified: Fri, 24 Apr 2020 00:15:54 GMT  
		Size: 2.7 MB (2718734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbef55dc97b2b7a21b6bf9cf83b991c58c86ad0fe3e1a6f6050253f067e037cc`  
		Last Modified: Fri, 24 Apr 2020 12:14:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7369917525ab29de34f65c7ffb1499470aa078dcb46d280d67175d5693154b5b`  
		Last Modified: Fri, 24 Apr 2020 12:14:02 GMT  
		Size: 6.3 KB (6348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa4d0a88d2835e26bd5ba1f10e9c032d68f55a971f203ccbb3f95803f0ce216`  
		Last Modified: Fri, 24 Apr 2020 12:14:01 GMT  
		Size: 82.0 KB (81996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a1a60fac416a4bcf7dcdc29c6831b93f88e6d89fb9bd982f96f0a8601e14ae`  
		Last Modified: Fri, 24 Apr 2020 12:14:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06089ea6b11c1b6c92b6d10715efa2417f03c765cc262a88d1209e14c4eb2790`  
		Last Modified: Fri, 24 Apr 2020 12:14:01 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:78999cb8561c2caff3c5846fe237439af72fba5288eed0845c4ce1bad191094c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2893567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b06cf71914272266c98138b1dddfe0971d0e4314ed3f295e8e498c80ab2db9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:11 GMT
ADD file:2e9fb162fdd20e7ac6e9edcb9e1ce9ece750f125c93824c5709a2800ae397f89 in / 
# Thu, 23 Apr 2020 21:16:11 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 08:56:34 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 Apr 2020 08:56:35 GMT
RUN apk add --no-cache libssl1.1
# Fri, 24 Apr 2020 08:56:35 GMT
ENV SPIPED_VERSION=1.6.1
# Fri, 24 Apr 2020 08:56:35 GMT
ENV SPIPED_DOWNLOAD_URL=https://www.tarsnap.com/spiped/spiped-1.6.1.tgz
# Fri, 24 Apr 2020 08:56:35 GMT
ENV SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 24 Apr 2020 08:56:52 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "$SPIPED_DOWNLOAD_URL" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 24 Apr 2020 08:56:52 GMT
VOLUME [/spiped]
# Fri, 24 Apr 2020 08:56:52 GMT
WORKDIR /spiped
# Fri, 24 Apr 2020 08:56:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 Apr 2020 08:56:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 08:56:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:294658c31053f36b08a64158e37d4fb84478e6fe8f4d5127c51a6334c8a3c36d`  
		Last Modified: Thu, 23 Apr 2020 21:16:37 GMT  
		Size: 2.8 MB (2787128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99115e03ce3c950e46d67227979c778c7628cde48083cb2af971981006bf941`  
		Last Modified: Fri, 24 Apr 2020 08:57:05 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31b4b31c02617aa39baede00c19c62ea202856ecbac0cd402d02254ac730492`  
		Last Modified: Fri, 24 Apr 2020 08:57:05 GMT  
		Size: 6.3 KB (6347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2763a1020ba1dc39a2fe63a92c2a7d3d3db450b78c0003f74c3abd88d2a8690`  
		Last Modified: Fri, 24 Apr 2020 08:57:05 GMT  
		Size: 98.4 KB (98394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfc6e4f386ed41e9ad01c0e5b3e5932a75ad7682805e4aa0799c3415a80ec73a`  
		Last Modified: Fri, 24 Apr 2020 08:57:05 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7579e851392e7efa6fbe6a6a56b04fc171183c31ec1a1f72c1f27658e21286b`  
		Last Modified: Fri, 24 Apr 2020 08:57:05 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:9cfed93592b7fe82e50479c7a0822a48b1b5ab400a40cc2f1389ff26010e2411
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2915588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3490b3150b3b9ab6e3a99426c43e465e9bc6270b4eb8b13f9853fcb2b5b6930`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 Apr 2020 20:40:45 GMT
ADD file:2b585d18d1fcebf3ed725468d8f9642d2e6e32af8770f87b36d4601cc3a55316 in / 
# Thu, 23 Apr 2020 20:40:47 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:08:31 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 Apr 2020 09:08:37 GMT
RUN apk add --no-cache libssl1.1
# Fri, 24 Apr 2020 09:08:40 GMT
ENV SPIPED_VERSION=1.6.1
# Fri, 24 Apr 2020 09:08:44 GMT
ENV SPIPED_DOWNLOAD_URL=https://www.tarsnap.com/spiped/spiped-1.6.1.tgz
# Fri, 24 Apr 2020 09:08:46 GMT
ENV SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 24 Apr 2020 09:09:11 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "$SPIPED_DOWNLOAD_URL" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 24 Apr 2020 09:09:14 GMT
VOLUME [/spiped]
# Fri, 24 Apr 2020 09:09:18 GMT
WORKDIR /spiped
# Fri, 24 Apr 2020 09:09:19 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 Apr 2020 09:09:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 09:09:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6694fcf3186b2073b4f09e0a2a753df9c8bcd31083e89a8a8f9a7001ad295328`  
		Last Modified: Thu, 23 Apr 2020 20:41:47 GMT  
		Size: 2.8 MB (2809956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85914d3a008a1f444b38165ce3fc56d3aa520d88133fdfdf654791a1de71f1a`  
		Last Modified: Fri, 24 Apr 2020 09:09:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec06a3c07a43eaf655e1f2a0e8576ada754f9af29c18bf3aa94950c92a799a1`  
		Last Modified: Fri, 24 Apr 2020 09:09:47 GMT  
		Size: 6.4 KB (6355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c1753650b9ad92aea131b35a681afa866570eb644d3bf8d47c5e2852e6efff`  
		Last Modified: Fri, 24 Apr 2020 09:09:47 GMT  
		Size: 97.5 KB (97519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7e018c97ddc33d44c99d11c34b2d1601296151ec6f87cdc80cee41bbb6d294`  
		Last Modified: Fri, 24 Apr 2020 09:09:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9dc529e21e37a4f215c5335a3b2a298697829328261d7a279e8dd9f1735fff`  
		Last Modified: Fri, 24 Apr 2020 09:09:47 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:5b9c1d41dd39f4984e651ea4535f43f4100936e674d6c3ae153f21b586a3c16d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2663578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de69b324a894fbaf9b08ddc70f1ea37eef4e0b5eb83a102ed1689aba74076abe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 Apr 2020 17:51:08 GMT
ADD file:53e1d2e5396547a2d7109e4b73078911bd069ae5d762f816d90e89ec9731ab13 in / 
# Thu, 23 Apr 2020 17:51:08 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 07:33:50 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 Apr 2020 07:33:51 GMT
RUN apk add --no-cache libssl1.1
# Fri, 24 Apr 2020 07:33:51 GMT
ENV SPIPED_VERSION=1.6.1
# Fri, 24 Apr 2020 07:33:52 GMT
ENV SPIPED_DOWNLOAD_URL=https://www.tarsnap.com/spiped/spiped-1.6.1.tgz
# Fri, 24 Apr 2020 07:33:52 GMT
ENV SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 24 Apr 2020 07:34:01 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "$SPIPED_DOWNLOAD_URL" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 24 Apr 2020 07:34:01 GMT
VOLUME [/spiped]
# Fri, 24 Apr 2020 07:34:01 GMT
WORKDIR /spiped
# Fri, 24 Apr 2020 07:34:02 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 Apr 2020 07:34:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 07:34:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ab92bebeb6027138cd65f1f6658fd3428e21c60c95bdc978e0c57bf0b2a53970`  
		Last Modified: Thu, 23 Apr 2020 17:51:46 GMT  
		Size: 2.6 MB (2574478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3feb176fd2b09952c3679317f0be3a9a74423b300047dcb4dc4115d02775dc8`  
		Last Modified: Fri, 24 Apr 2020 07:34:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0701f42154bd44f03411750273dbc7f43f557ad52deb5aa079179b76140f5d4`  
		Last Modified: Fri, 24 Apr 2020 07:34:18 GMT  
		Size: 6.3 KB (6344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bcb5dd25d4a0e2547fb965eb04d708124eb3754eaf7fa0fe3a4cfd77ccd1fe3`  
		Last Modified: Fri, 24 Apr 2020 07:34:18 GMT  
		Size: 81.0 KB (80998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d7e19bd791bc8c8db467add1c84d489de9b8c5c2b2f5b6013c495c35597b8b`  
		Last Modified: Fri, 24 Apr 2020 07:34:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427d930f454293093665a4d2a97377fec8eae8a043e3c5cc97a84a1ec5ce23d5`  
		Last Modified: Fri, 24 Apr 2020 07:34:24 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
