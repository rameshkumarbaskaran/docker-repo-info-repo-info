## `nats:2-alpine`

```console
$ docker pull nats@sha256:7e3c4071cebc4749b3913b42481fbcd7d90f2c3b5bd61a9e06839f2b11acde10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:4e7d4fe05ce93c6c712e1789435da0c99e1bf3ef74db43eaeaef6ca272397766
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7668256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23d872d0d10133874978b8503e1da0a875478f9c36d18274df90f4499c03019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:22:11 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:22:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:22:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:22:13 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:22:13 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:22:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:22:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e0d861b124a1ab454d3802b3afed8c07d3ec1392b2b86e1dfd9d0d5d6a1f11`  
		Last Modified: Fri, 22 Apr 2022 16:22:48 GMT  
		Size: 4.9 MB (4852697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0473f2dce7bc79ef8358c50e032d4fdf17e3cc1b93deb8a87ba3085118feb4`  
		Last Modified: Fri, 22 Apr 2022 16:22:47 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0efed31ac2d8993794bd5b44f6e003ec74ea05fb15e0385ef8b1048c904f60`  
		Last Modified: Fri, 22 Apr 2022 16:22:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:7091220455f290bada50edec48a24908cbbe489e0aac009ddafe3e9d540fb036
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7133695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd13715b15026d21466ab186bb33954a7a9df237fce3098e994c544a0d58f606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:49:33 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:49:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:49:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:49:38 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:49:38 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:49:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:49:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6250a52fe67317e7257391e6c81cf0ea21e47617fd095740a0d3607da4130de7`  
		Last Modified: Fri, 22 Apr 2022 16:51:45 GMT  
		Size: 4.5 MB (4510720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26bd4087b8ffb0f3db8c2e503ba7fb78bceadf9db85e703ebe84ed37074a6df`  
		Last Modified: Fri, 22 Apr 2022 16:51:42 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fdd060af20879eea02ac88ca5a8585f86f5a55e2cd469952ede5eec778a11e`  
		Last Modified: Fri, 22 Apr 2022 16:51:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:ff4d00c43ccc00a0582b1dbc17b5bc28e4ef6545f61b3c6be485e002fae45c4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6928061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fc5f4cb0a6e2b6652822c274f5e6bd051757dc7e24c5be03af50467d4ea670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 19 Apr 2022 05:26:38 GMT
ENV NATS_SERVER=2.8.0
# Tue, 19 Apr 2022 05:26:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6964e92e5d15c1efa29a05f0dd410750c2cf2789097e1391440d7a425108a273' ;; 		armhf) natsArch='arm6'; sha256='4ba6a1fe17fa6d4d65d428ad22afc0cb8aa56ed5486806d179f86ec726c51697' ;; 		armv7) natsArch='arm7'; sha256='3f2d7a38d3d9ea26abda5509177782fc425f79e5d77112093d617904f35663e6' ;; 		x86_64) natsArch='amd64'; sha256='9a6df1121c17dc5537ccb193c2d153b8f3cd1de60a181a41792ea397facce3af' ;; 		x86) natsArch='386'; sha256='d860f618a507124cfb12e5fd0cb42c54513632d004d4d03b3af29c83294d766a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 19 Apr 2022 05:26:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 19 Apr 2022 05:26:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 19 Apr 2022 05:26:43 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Apr 2022 05:26:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Apr 2022 05:26:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7bcb96bb0f2694c2c3650393794ab8ab1fa8467a8822b1b09ae77d69337c5f`  
		Last Modified: Tue, 19 Apr 2022 05:28:54 GMT  
		Size: 4.5 MB (4502736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526c1a645aeb39ecd91ca84623e21480cad2b868cb28fefc907827db0a6f5ca0`  
		Last Modified: Tue, 19 Apr 2022 05:28:51 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ab0dd3f1cfd48ae336e6ce8fecfd8b004df2828e2e87e0c6ca7c13ef658640`  
		Last Modified: Tue, 19 Apr 2022 05:28:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:01abf8e1249f3267774047ec264d815aa57af333eecb3558e40bf86924f3c7b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7207790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb5bc49254cd7eb6d816b2d62ecd8a1052ce0be9a8fbe0c89cd81ecc053de8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Fri, 22 Apr 2022 16:40:04 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:40:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fa1226c8821c0487817ae3738112678d44f4b30a179acdf4ac6edb4b9e630a3d' ;; 		armhf) natsArch='arm6'; sha256='9ff38ac7e93a993112a0a518935cfe2c41a3a19cab6c5920673e1f67bd550348' ;; 		armv7) natsArch='arm7'; sha256='08acef43ae912954cf7b908487bc5d8a61985dab9ada2779b602c5d1176efd98' ;; 		x86_64) natsArch='amd64'; sha256='7fa8300afa29afb0432abbb7455dc8517549b3cf1a32de8f4dc3617cca8e70a5' ;; 		x86) natsArch='386'; sha256='e9c9a110aaf7113959659217bd976d7227e81cda6b74fe04f9649e7c57eb523e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 22 Apr 2022 16:40:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 22 Apr 2022 16:40:10 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 22 Apr 2022 16:40:10 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:40:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Apr 2022 16:40:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2ab5ff26c46d1d386429d02952195bc7699ceedb0288794e9b35e45c82a117`  
		Last Modified: Fri, 22 Apr 2022 16:41:17 GMT  
		Size: 4.5 MB (4490338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e92c2bb8c325e21d94887f856d4590cf00b7a236989ce3f58f00e0e4bd400ea`  
		Last Modified: Fri, 22 Apr 2022 16:41:16 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203649ff8695131a6ebe7b59382b10c48667e76e75bdff0fd07cf378d45aad00`  
		Last Modified: Fri, 22 Apr 2022 16:41:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
