## `nats:2-alpine`

```console
$ docker pull nats@sha256:d6c6ae7df4a0c5f7aa5ec8035501b7a594d065216aa227265c89909a3c31df96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:89314efbfded0bd51e0b70966ebb7ad753245d6b680d4d999c25904838954a84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8810293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5f3a7141f662bd0bab1c885fe0237733c81118613c3e2a1f041bf7d1cab81d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 22:29:16 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 22:29:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 22:29:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 22:29:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 22:29:18 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 22:29:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688e12de30012d849a08c4b3a056bf9462831be6349fedb514a9b943c5d3b038`  
		Last Modified: Thu, 13 Jul 2023 22:29:51 GMT  
		Size: 5.4 MB (5411416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcb04c9ced60dff0180f5da5e6f033545ec0a56faed6b9ea1f00c88a9ed3847`  
		Last Modified: Thu, 13 Jul 2023 22:29:50 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086da10bd35caa5abb0061f428f619d8dd071a2fb7c760eead2ceb0bb7536e58`  
		Last Modified: Thu, 13 Jul 2023 22:29:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:c1cb16ffa939bd8f1601f657d500e3bd5c45005c28c448b68ec5b4b996fe430e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8318264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83f1c1fe0f07fee40eabe8e9253b5ac08578d588938045575e96a038b76964f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:20 GMT
ADD file:4213782693bf27a9a6de23bc924ef0c4fb6b2d56010fc07b25f81edeba83b0d4 in / 
# Wed, 14 Jun 2023 18:49:20 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 21:49:19 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 21:49:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 21:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 21:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 21:49:22 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 21:49:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:7836be94d3024e2042069c1095caba0b391f70c4b3d34a0475a503239d73dfba`  
		Last Modified: Wed, 14 Jun 2023 18:49:46 GMT  
		Size: 3.1 MB (3143353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbd7a095ebb0cf47214d570aaa6e8beb1144d038098b2cc64526b8119b7a072`  
		Last Modified: Thu, 13 Jul 2023 21:49:46 GMT  
		Size: 5.2 MB (5173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc62259aed8a302b7cb52adf9701c763fb05897f5965d7873f6e27e88d4e07e`  
		Last Modified: Thu, 13 Jul 2023 21:49:45 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3f8be8762d1cac21e849032e638a3ebf9bbb3957511eba1b7321783b83f23c`  
		Last Modified: Thu, 13 Jul 2023 21:49:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:05b3018971114ff61d10e947e304f35c7bbc0abee425911c0fd58e23f7ae74e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8068141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4043b810630b65430ae04fb007b13c892d5e16ae40ea86b45712575d54868208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 22:36:15 GMT
ADD file:082f034323c559f3cb9feb6422c88b1ec8017f436d6109e238a5c5384a32a90a in / 
# Wed, 14 Jun 2023 22:36:15 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 22:52:54 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 22:52:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 22:52:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 22:52:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 22:52:57 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:52:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 22:52:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:633ba29fd335042456b6e2c073636f6fa30de56f1331c442914739b92a479974`  
		Last Modified: Wed, 14 Jun 2023 22:36:49 GMT  
		Size: 2.9 MB (2898508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b240facc4a312dbc41a0d9d2b5f34f26188edc082396407147566f4670a7bd`  
		Last Modified: Thu, 13 Jul 2023 22:53:30 GMT  
		Size: 5.2 MB (5168636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c49f0e2539269574bfe0565b74747b67dc174076c7d3b2b2c8064b2af71a80`  
		Last Modified: Thu, 13 Jul 2023 22:53:28 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f69564b85401d79f11d3d0dd7775aa0dfa3d09c58f3daedcbe1f3fe676eea`  
		Last Modified: Thu, 13 Jul 2023 22:53:28 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:aa93c00cb94a9cf48edbefb3fbb029b8d8187ccf4735f2eff181906d0e869854
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8309359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc0605733abd9e160812417dd92d5c4812e0640ef2a71568b2f2aed85eb6685`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 23:11:00 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 23:11:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 23:11:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 23:11:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 23:11:03 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 23:11:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8d12353ca807b3f28a178dcf6ddfe80ac709c12b0da6364e48db96ab06e400`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 5.0 MB (4979109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7977030405ec12383b1b2033bc0fceb08f5c959b13d57ba18f74f11efee542ed`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041d1130902bd23c5b39754ecf01c19ed66a35c6e60064301df126b0f52259ad`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
