## `nats:alpine3.18`

```console
$ docker pull nats@sha256:14a077e2c0f9bf8fd02e43e78cf1c3cb38c5ffc7174690fe6fd2ae2098049a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:79f55e1e1ac530428b0f3dbb8447fca8eb73d43b8706ea60041b9150ec9cee4e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8807112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba37671be303876cc9cfaabde62d4cba45e69f890335b8257195f1d6109e6dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 21 Jun 2023 00:17:25 GMT
ENV NATS_SERVER=2.9.19
# Wed, 21 Jun 2023 00:17:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='74d01dff16360fd4187f56005d1ca9783762e6693cc26ab015c73bddf1d02e48' ;; 		armhf) natsArch='arm6'; sha256='b8160af8d6585a97c7c794c1dffaba0429757b51654986d4e64de6b1ca64d457' ;; 		armv7) natsArch='arm7'; sha256='d2062448c98a907af83b2253c42b91a4cc98243f98e70f91a060d5eb94664dfe' ;; 		x86_64) natsArch='amd64'; sha256='e3856357cba44652776ade8de6fd0d6198d484f7b2419e97fbec6a9edfe84c49' ;; 		x86) natsArch='386'; sha256='a368c9f1456447093bc902fa2dffaaa1f282ed52a40cb2c4e015df80461b34a6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 21 Jun 2023 00:17:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 21 Jun 2023 00:17:28 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 21 Jun 2023 00:17:28 GMT
EXPOSE 4222 6222 8222
# Wed, 21 Jun 2023 00:17:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jun 2023 00:17:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c14de251df13ed7d21c47cd279de1e6909afcd92ef08e3e220bd21826ad17c`  
		Last Modified: Wed, 21 Jun 2023 00:17:52 GMT  
		Size: 5.4 MB (5408233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae5c74d1f37b02a1a518849fb5ff1a7392f336d60cc3e120d74cb26088a6d29`  
		Last Modified: Wed, 21 Jun 2023 00:17:51 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59566e38ec7be6b427690697eb98acbd97024ac5167a328a1a9110fd5336e0a`  
		Last Modified: Wed, 21 Jun 2023 00:17:51 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.18` - linux; arm variant v6

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

### `nats:alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:d42b0952c95fca686f67910c9d8a3ff062e23acd1d4c4c9483d76ccd4dd64ece
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8062747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15157ab7b8a856d3975e26cbd3060310e1a35b03d8b71922d703b1881b7c17e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 22:36:15 GMT
ADD file:082f034323c559f3cb9feb6422c88b1ec8017f436d6109e238a5c5384a32a90a in / 
# Wed, 14 Jun 2023 22:36:15 GMT
CMD ["/bin/sh"]
# Wed, 21 Jun 2023 00:09:15 GMT
ENV NATS_SERVER=2.9.19
# Wed, 21 Jun 2023 00:09:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='74d01dff16360fd4187f56005d1ca9783762e6693cc26ab015c73bddf1d02e48' ;; 		armhf) natsArch='arm6'; sha256='b8160af8d6585a97c7c794c1dffaba0429757b51654986d4e64de6b1ca64d457' ;; 		armv7) natsArch='arm7'; sha256='d2062448c98a907af83b2253c42b91a4cc98243f98e70f91a060d5eb94664dfe' ;; 		x86_64) natsArch='amd64'; sha256='e3856357cba44652776ade8de6fd0d6198d484f7b2419e97fbec6a9edfe84c49' ;; 		x86) natsArch='386'; sha256='a368c9f1456447093bc902fa2dffaaa1f282ed52a40cb2c4e015df80461b34a6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 21 Jun 2023 00:09:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 21 Jun 2023 00:09:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 21 Jun 2023 00:09:18 GMT
EXPOSE 4222 6222 8222
# Wed, 21 Jun 2023 00:09:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jun 2023 00:09:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:633ba29fd335042456b6e2c073636f6fa30de56f1331c442914739b92a479974`  
		Last Modified: Wed, 14 Jun 2023 22:36:49 GMT  
		Size: 2.9 MB (2898508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b84fd19835fa4d25a00aefb9a29fa58064bef400cadb46dca4379f51aea9df`  
		Last Modified: Wed, 21 Jun 2023 00:09:52 GMT  
		Size: 5.2 MB (5163241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9babea9cb5c03c0b3ad9c273223967b0c7f601ee8f1266264673cc982ac707`  
		Last Modified: Wed, 21 Jun 2023 00:09:51 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c3febf8d9d1012edf70b3b51d8aee72c564d0623ebb8510a037dfb86bf735a`  
		Last Modified: Wed, 21 Jun 2023 00:09:51 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9d7047e7aa327735a497636a2a565c497ecdab4d39542b36d311378c6e66fa6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8302354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0290494870a431e33a0ddcacc6f8ad9b9ce8b9b4908f16c8e079756ea205ed47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 21 Jun 2023 00:15:29 GMT
ENV NATS_SERVER=2.9.19
# Wed, 21 Jun 2023 00:15:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='74d01dff16360fd4187f56005d1ca9783762e6693cc26ab015c73bddf1d02e48' ;; 		armhf) natsArch='arm6'; sha256='b8160af8d6585a97c7c794c1dffaba0429757b51654986d4e64de6b1ca64d457' ;; 		armv7) natsArch='arm7'; sha256='d2062448c98a907af83b2253c42b91a4cc98243f98e70f91a060d5eb94664dfe' ;; 		x86_64) natsArch='amd64'; sha256='e3856357cba44652776ade8de6fd0d6198d484f7b2419e97fbec6a9edfe84c49' ;; 		x86) natsArch='386'; sha256='a368c9f1456447093bc902fa2dffaaa1f282ed52a40cb2c4e015df80461b34a6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 21 Jun 2023 00:15:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 21 Jun 2023 00:15:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 21 Jun 2023 00:15:31 GMT
EXPOSE 4222 6222 8222
# Wed, 21 Jun 2023 00:15:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Jun 2023 00:15:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb00d7e55df9bba47fe0634e06a979dae0fe0362c1eeac62da7dbc69bcec08c`  
		Last Modified: Wed, 21 Jun 2023 00:15:55 GMT  
		Size: 5.0 MB (4972110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18cbef28284265dd9e570b61ea0613ecd955c0cd58abf12d7b379e0db34eabf`  
		Last Modified: Wed, 21 Jun 2023 00:15:54 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70361c011c7e732ec8545ea9382e6c492f07e92c784a78c9e8b526401dde5de7`  
		Last Modified: Wed, 21 Jun 2023 00:15:54 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
