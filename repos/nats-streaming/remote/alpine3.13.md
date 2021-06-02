## `nats-streaming:alpine3.13`

```console
$ docker pull nats-streaming@sha256:b9260f10e34219360acaac608ce39811e675351a762abdc3ce286183df11de01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.13` - linux; amd64

```console
$ docker pull nats-streaming@sha256:402dacbb78f9bf5e9ea249c730f7905caa085ca665782e1cb4c6e7004f597689
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8774780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7ad70b17b46627026163460cce06023868f24d36a50cd9c261e7c6cba86e29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 21:25:11 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:25:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 21:25:14 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 21:25:15 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:25:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:25:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269577e93d92e9e558c3607d8b5e74978c939fc643895de15fd70ef06b811323`  
		Last Modified: Fri, 16 Apr 2021 21:25:54 GMT  
		Size: 6.0 MB (5962389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fa1ca69a5dc5f7aecbfca382d45ab09423bb9d103c6567abc37af7b842073a`  
		Last Modified: Fri, 16 Apr 2021 21:25:54 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.13` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:8f5fec9c3508cacdf96a48dccfda3cb07ba922cc31faefcd9b82981ece64b14c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9175700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6654e93452d6f1e430cf9500177e35f139504b0058910421ad055b18d8bb2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Tue, 01 Jun 2021 23:54:27 GMT
ENV NATS_STREAMING_SERVER=0.22.0
# Tue, 01 Jun 2021 23:54:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3ffc4b74f469b97a8ce0edff8b645baf89d9f9f3debdfa7088a0ceac3ed6c37b' ;; 		armhf) natsArch='arm6'; sha256='abe201b1a90cd2e8db39989c81a2c76d3956035745c68d0c7e090fc8c5a138c8' ;; 		armv7) natsArch='arm7'; sha256='d218edd395f980ea91a54624b4cc1fe0220268171ee596a24d7c01c15a7dbb7f' ;; 		x86_64) natsArch='amd64'; sha256='72f5b899167a8866d4b82d1bf9bc14b5d047e6b1ab127dd0085e9eb91a89f097' ;; 		x86) natsArch='386'; sha256='d87bb204228c5e820747e1682dbfb56289e3ddadcfe129b9c9fcf1ad7c0ba053' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 01 Jun 2021 23:54:31 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 01 Jun 2021 23:54:32 GMT
EXPOSE 4222 8222
# Tue, 01 Jun 2021 23:54:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jun 2021 23:54:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef7b36a5eb9baa587c0c795817923d783258f4ec2d50d157bc548fb861282c6`  
		Last Modified: Tue, 01 Jun 2021 23:55:55 GMT  
		Size: 6.6 MB (6553148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02404618fe373dc7f314135fe9ad25f49fe83b972a776fda8ef5562833d9b7fd`  
		Last Modified: Tue, 01 Jun 2021 23:55:53 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.13` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ea133d32e6510a0d1822a1ea1cfcca41e3cbd747a3d69491aee62319937e892d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc13824ee86fb9d0c1609b885378ba366f3883903bfe990fb27464bce6c02686`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 20:59:08 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 20:59:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 20:59:13 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 20:59:14 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 20:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 20:59:16 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b86c52fd84fa988d60547be09b11af6fcac2dffa6b340e92b776a0fc89a298`  
		Last Modified: Fri, 16 Apr 2021 21:00:42 GMT  
		Size: 5.5 MB (5527039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b279e3ce6e5cfc3967a4acbf6dc2563f1715817b059d6f320b53cbc21b74e1`  
		Last Modified: Fri, 16 Apr 2021 21:00:40 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:febf36c660fc36bcbf3da9945707f541e81665b0d21a0f1c6c8220543697a757
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8165113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd79dce90e049636e2513bd55a0b3178cb59197d3dfc53cbed474dbbd5de0f1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Fri, 16 Apr 2021 21:44:03 GMT
ENV NATS_STREAMING_SERVER=0.21.2
# Fri, 16 Apr 2021 21:44:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='56bcfea3c3d7a232dab93ad280ce8f8df87959ac000c7d24ce03dbab2f4c4d2b' ;; 		armhf) natsArch='arm6'; sha256='34d7032ba61724ec55d78cb94a5ed244754509b8b957e1e7e4f0579292c35a7f' ;; 		armv7) natsArch='arm7'; sha256='b4869711408e3823c8818e934bf90d07ed51f350147702b80831fb4fe5a390d2' ;; 		x86_64) natsArch='amd64'; sha256='7a401a3af7eb56a0d1d3b207dc517222697b48cb7e9e524848e62bd13393d23a' ;; 		x86) natsArch='386'; sha256='58aa4cad4c75920522ec0457b79d889f9c740c248647b875254cd1313517620c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.zip "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-streaming-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-streaming-server.zip "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server"; 	rm nats-streaming-server.zip; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rmdir "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 16 Apr 2021 21:44:08 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 16 Apr 2021 21:44:09 GMT
EXPOSE 4222 8222
# Fri, 16 Apr 2021 21:44:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:44:10 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a1a4dae3b1b310f0231f28f4db383d7605066343274881c5be1300ebe64f51`  
		Last Modified: Fri, 16 Apr 2021 21:48:37 GMT  
		Size: 5.5 MB (5452665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a06774842e75925d8884fc1ea5a3e83c2c8054d4fb443ad11021c5866b0617`  
		Last Modified: Fri, 16 Apr 2021 21:48:36 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
