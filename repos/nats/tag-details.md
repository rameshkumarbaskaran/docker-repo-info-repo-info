<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.18`](#nats2-alpine318)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.9`](#nats29)
-	[`nats:2.9-alpine`](#nats29-alpine)
-	[`nats:2.9-alpine3.18`](#nats29-alpine318)
-	[`nats:2.9-linux`](#nats29-linux)
-	[`nats:2.9-nanoserver`](#nats29-nanoserver)
-	[`nats:2.9-nanoserver-1809`](#nats29-nanoserver-1809)
-	[`nats:2.9-scratch`](#nats29-scratch)
-	[`nats:2.9-windowsservercore`](#nats29-windowsservercore)
-	[`nats:2.9-windowsservercore-1809`](#nats29-windowsservercore-1809)
-	[`nats:2.9.17`](#nats2917)
-	[`nats:2.9.17-alpine`](#nats2917-alpine)
-	[`nats:2.9.17-alpine3.18`](#nats2917-alpine318)
-	[`nats:2.9.17-linux`](#nats2917-linux)
-	[`nats:2.9.17-nanoserver`](#nats2917-nanoserver)
-	[`nats:2.9.17-nanoserver-1809`](#nats2917-nanoserver-1809)
-	[`nats:2.9.17-scratch`](#nats2917-scratch)
-	[`nats:2.9.17-windowsservercore`](#nats2917-windowsservercore)
-	[`nats:2.9.17-windowsservercore-1809`](#nats2917-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.18`](#natsalpine318)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:c366591c44da44fe1180ca3aaee4f18b959d2d8ab5170c5ebec98eda2d0cb390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4377; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:d7a57514cf7a0949ab8e63985f040f1fbaa01aa70aa50d8485f796a9a8dead08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd1a8b681814e86af7f1b07aa7178abd74163b5101ad1f855420c25d4afae5e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:19:59 GMT
COPY file:a3e4cfa40e3f87cbc1a2427fe9e77a182eed251b7a2f3037b894ac919acda56d in /nats-server 
# Thu, 18 May 2023 21:19:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:19:59 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:19:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:19:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e7f86c5b152db9b1815749cb2d298d36014c2905070ae66128b67029b4b31780`  
		Last Modified: Thu, 18 May 2023 21:20:38 GMT  
		Size: 5.1 MB (5116621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ce2c40f365197112db5bf1e3ed9b09b631da2058b456f99a50a5890fdda44`  
		Last Modified: Thu, 18 May 2023 21:20:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:b93fec72f4aff1d673fd6ead1e244e694e4919368e246cc29e0d7d120e59ed77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4881364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab660f64e3aad0f8f74d3a08909fe9013543eb07b61a9f8c6862b5db7d457d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:49:31 GMT
COPY file:6e54deb4ba87d6bff1f230123320fc7c9eee49d9a7456888efc872a22b9bd9ba in /nats-server 
# Thu, 18 May 2023 21:49:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:49:32 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:49:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41da3c5a1624a52c52a67beaa7b94c8c85a26f53b81e82e6dc05ae661adfebc1`  
		Last Modified: Thu, 18 May 2023 21:50:09 GMT  
		Size: 4.9 MB (4880856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df51ab38f5ab934d23f3b5429532106ef6baa2f64572f07ce9e5718e3f27374b`  
		Last Modified: Thu, 18 May 2023 21:50:08 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:94bf4a62f52fd647adb621d2d584e9c48aea06b124fb81cd59afed50252071bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4874864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8b8de1397d0af96648a1d02610dc54a066633c75eb548fc6be7e0d15497c3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:57:50 GMT
COPY file:31e26234e2abf1c16cd5869033f07320118e6dc458af341f37a27a3d12ffbc65 in /nats-server 
# Thu, 18 May 2023 21:57:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b6209c6f59228d4816baef6c05a38f68693937e6c86969581c57a1c7b68ccb40`  
		Last Modified: Thu, 18 May 2023 21:58:28 GMT  
		Size: 4.9 MB (4874355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69c5a4696da201d78c2dae749a6bce01c3a924afbdfa7e87c6797b8db238d4d`  
		Last Modified: Thu, 18 May 2023 21:58:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c4a7f923864c688cb5cc324df620960febd829b8d1f7074e4af3805caf5d5ceb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4685324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c4d84878abd37db0a2ba71386d26a2aaea2e989b4c3fc5f5930194da2e95c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:39:47 GMT
COPY file:b639df8cca07607378826468450a651a2cab9fb1be759ac266bf356bbfa2ac8c in /nats-server 
# Thu, 18 May 2023 21:39:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:39:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:39:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:39:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8e3bc385de2fea9fcd87e3f5b9809c6c133578671c906d0c1df657657c34664`  
		Last Modified: Thu, 18 May 2023 21:40:23 GMT  
		Size: 4.7 MB (4684816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d538df43ba01d77f25e465d3cce0829b2fbcf2a5ff131e1a42fda47b5c6c64`  
		Last Modified: Thu, 18 May 2023 21:40:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:992902adab2316f4e0f1a0e7edbddad09cb2659bb7e26ed498ef39ebc86b5e20
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109563244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38a2aebef90db7b99751a2c93b984e1f7ca5acabedc0f61f40e08a00a740585`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:18:08 GMT
RUN cmd /S /C #(nop) COPY file:af4b677614d535ef3af8025256146a8f3389c5c6a4397c848e25544ea858eace in C:\nats-server.exe 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b004c7f9a3834a96e986a89e27e23aa329db101d8f291c2b5a3cdc913a1c57de`  
		Last Modified: Thu, 18 May 2023 22:18:56 GMT  
		Size: 5.2 MB (5172869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3456f5dbcfcadd4157124d47dec0661e9812e4db874cb74cb8e95be4c4ff246`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663f7b2aab72f936cdb391d59c87f99e0154634854724380b4f54daf05d300cc`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12ae8aa52c42d91abbe9fd8cd449efbcb465ac7b718d50e0589caa7436aebee`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f224e7b1c5810b30e107368e877ea6b7ca699eb4bcc4b27003aae49658d6f25`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:1a7b320b294218d11b48ddcd1552a18a74ae8790c80ba5372726c58d0a5ee295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:7544f1dfe4b270789a68e2056135467d525da411f331f43640150b0642dee693
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8802768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ada7bbdb360a5406551ced3593bc48e57c6cea5ee5d502e1a0df2437156d06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:19:49 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:19:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:19:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:19:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:19:52 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:19:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba69a821f226517d8763fd5007b51eeb8a68e40f7fb32dec75e13297ea1cb49`  
		Last Modified: Thu, 18 May 2023 21:20:19 GMT  
		Size: 5.4 MB (5404276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ad2f9c9076c4ccedf3a056bf6e996a658fa5ece8cc35913e4728d58617e8b3`  
		Last Modified: Thu, 18 May 2023 21:20:18 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb3c123b7bd114e7897ddf602c16bcd18f034abda3ee53d91a108b71c624faa`  
		Last Modified: Thu, 18 May 2023 21:20:18 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:08b7d50259bf79d1f0cc5476da2707cbe3723f8b25ececd27b4e20f5c3ba036e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8325871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676517e73baa5d6c0a13a665dcf0412659d93274c96643829ff67835d5e4905d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:04 GMT
ADD file:f87a991e2e9f185fd4a88569d86a9b8e5bc07182e7fa613b95acab25986f2a6c in / 
# Tue, 09 May 2023 23:11:04 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:49:22 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:49:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:49:24 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:49:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:015ee8d9fb3dca1b18815f1e4ee0d325d1f40cde6f2df4dd307918f7b69167d7`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.2 MB (3155679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06976c3bb336d8c3936e2bbb8d27dbd5b805054e1064aaf7c651d6fd5523aa71`  
		Last Modified: Thu, 18 May 2023 21:49:48 GMT  
		Size: 5.2 MB (5169192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c85a9f3b4246d93c82583c9d4336cb58688e4b311be41f752bc0c9456a2135`  
		Last Modified: Thu, 18 May 2023 21:49:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6d307fb0f80f02bb15dbdbb0eba31d3a463afa38dca28f6cd0e913798ebf62`  
		Last Modified: Thu, 18 May 2023 21:49:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:882066add3894dc13cfadaeec8af9f9fce5b9c3fee92e377a13f0997a88a121f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8071388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574536f22d8de67b2c2f0962d9e7d108bb4b41d07cb13a05ebab5e3b82fe6d63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 22:57:32 GMT
ADD file:eb6b6a885e8ac9bccbf44a5c673b8542c8144bba927376688240446c2f413b10 in / 
# Tue, 09 May 2023 22:57:32 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:57:27 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:57:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:57:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:57:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:57:29 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:57:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e14425cf8fb9304b9ad4a9d1250e0d4c22e507a334ff747fa69b804500afc113`  
		Last Modified: Tue, 09 May 2023 22:57:50 GMT  
		Size: 2.9 MB (2911117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213de106e11b3e7261faf48da426167af8702e8a56ab0237f786ba0eb864a38d`  
		Last Modified: Thu, 18 May 2023 21:58:08 GMT  
		Size: 5.2 MB (5159272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5535f74851ba24bbb57849b9f7085eb8441d584ea938b19bdd027f5ccf52a193`  
		Last Modified: Thu, 18 May 2023 21:58:07 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2518eda2d1b2ce9ae4c75acdccc0d3bbe028cfbdf30d7e173dfa82e489af6ec`  
		Last Modified: Thu, 18 May 2023 21:58:08 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:36980286981e9058cd3f3a1f58fb92741d5ba73ff1a66d3b8ef7b98e23ab8377
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8313998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1348d24d9abc62396994637b0c3153212850856ce4ab5c1cc49194dd4ef4872e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:39:41 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:39:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:39:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:39:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:39:43 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:39:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8409748378eca62a6e13533d1f6fef38e6b40a7ad726dff04ad548a63ae20313`  
		Last Modified: Thu, 18 May 2023 21:40:03 GMT  
		Size: 5.0 MB (4970150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a822f2037d3c235b73c5f9924d54c4de71f06b2ba22757fc2a059c4f33d5c6`  
		Last Modified: Thu, 18 May 2023 21:40:02 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94f121392ee621f9e3f1aaa44685e70de92e169d23c2c547ba2d5172904b49d`  
		Last Modified: Thu, 18 May 2023 21:40:02 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.18`

```console
$ docker pull nats@sha256:1a7b320b294218d11b48ddcd1552a18a74ae8790c80ba5372726c58d0a5ee295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:7544f1dfe4b270789a68e2056135467d525da411f331f43640150b0642dee693
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8802768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ada7bbdb360a5406551ced3593bc48e57c6cea5ee5d502e1a0df2437156d06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:19:49 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:19:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:19:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:19:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:19:52 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:19:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba69a821f226517d8763fd5007b51eeb8a68e40f7fb32dec75e13297ea1cb49`  
		Last Modified: Thu, 18 May 2023 21:20:19 GMT  
		Size: 5.4 MB (5404276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ad2f9c9076c4ccedf3a056bf6e996a658fa5ece8cc35913e4728d58617e8b3`  
		Last Modified: Thu, 18 May 2023 21:20:18 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb3c123b7bd114e7897ddf602c16bcd18f034abda3ee53d91a108b71c624faa`  
		Last Modified: Thu, 18 May 2023 21:20:18 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:08b7d50259bf79d1f0cc5476da2707cbe3723f8b25ececd27b4e20f5c3ba036e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8325871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676517e73baa5d6c0a13a665dcf0412659d93274c96643829ff67835d5e4905d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:04 GMT
ADD file:f87a991e2e9f185fd4a88569d86a9b8e5bc07182e7fa613b95acab25986f2a6c in / 
# Tue, 09 May 2023 23:11:04 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:49:22 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:49:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:49:24 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:49:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:015ee8d9fb3dca1b18815f1e4ee0d325d1f40cde6f2df4dd307918f7b69167d7`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.2 MB (3155679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06976c3bb336d8c3936e2bbb8d27dbd5b805054e1064aaf7c651d6fd5523aa71`  
		Last Modified: Thu, 18 May 2023 21:49:48 GMT  
		Size: 5.2 MB (5169192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c85a9f3b4246d93c82583c9d4336cb58688e4b311be41f752bc0c9456a2135`  
		Last Modified: Thu, 18 May 2023 21:49:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6d307fb0f80f02bb15dbdbb0eba31d3a463afa38dca28f6cd0e913798ebf62`  
		Last Modified: Thu, 18 May 2023 21:49:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:882066add3894dc13cfadaeec8af9f9fce5b9c3fee92e377a13f0997a88a121f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8071388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574536f22d8de67b2c2f0962d9e7d108bb4b41d07cb13a05ebab5e3b82fe6d63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 22:57:32 GMT
ADD file:eb6b6a885e8ac9bccbf44a5c673b8542c8144bba927376688240446c2f413b10 in / 
# Tue, 09 May 2023 22:57:32 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:57:27 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:57:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:57:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:57:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:57:29 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:57:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e14425cf8fb9304b9ad4a9d1250e0d4c22e507a334ff747fa69b804500afc113`  
		Last Modified: Tue, 09 May 2023 22:57:50 GMT  
		Size: 2.9 MB (2911117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213de106e11b3e7261faf48da426167af8702e8a56ab0237f786ba0eb864a38d`  
		Last Modified: Thu, 18 May 2023 21:58:08 GMT  
		Size: 5.2 MB (5159272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5535f74851ba24bbb57849b9f7085eb8441d584ea938b19bdd027f5ccf52a193`  
		Last Modified: Thu, 18 May 2023 21:58:07 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2518eda2d1b2ce9ae4c75acdccc0d3bbe028cfbdf30d7e173dfa82e489af6ec`  
		Last Modified: Thu, 18 May 2023 21:58:08 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:36980286981e9058cd3f3a1f58fb92741d5ba73ff1a66d3b8ef7b98e23ab8377
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8313998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1348d24d9abc62396994637b0c3153212850856ce4ab5c1cc49194dd4ef4872e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:39:41 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:39:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:39:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:39:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:39:43 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:39:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8409748378eca62a6e13533d1f6fef38e6b40a7ad726dff04ad548a63ae20313`  
		Last Modified: Thu, 18 May 2023 21:40:03 GMT  
		Size: 5.0 MB (4970150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a822f2037d3c235b73c5f9924d54c4de71f06b2ba22757fc2a059c4f33d5c6`  
		Last Modified: Thu, 18 May 2023 21:40:02 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94f121392ee621f9e3f1aaa44685e70de92e169d23c2c547ba2d5172904b49d`  
		Last Modified: Thu, 18 May 2023 21:40:02 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:8371b3bfc468a2294efb247531c2252c592398a98b574c2e81268d8c7f865d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:d7a57514cf7a0949ab8e63985f040f1fbaa01aa70aa50d8485f796a9a8dead08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd1a8b681814e86af7f1b07aa7178abd74163b5101ad1f855420c25d4afae5e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:19:59 GMT
COPY file:a3e4cfa40e3f87cbc1a2427fe9e77a182eed251b7a2f3037b894ac919acda56d in /nats-server 
# Thu, 18 May 2023 21:19:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:19:59 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:19:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:19:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e7f86c5b152db9b1815749cb2d298d36014c2905070ae66128b67029b4b31780`  
		Last Modified: Thu, 18 May 2023 21:20:38 GMT  
		Size: 5.1 MB (5116621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ce2c40f365197112db5bf1e3ed9b09b631da2058b456f99a50a5890fdda44`  
		Last Modified: Thu, 18 May 2023 21:20:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:b93fec72f4aff1d673fd6ead1e244e694e4919368e246cc29e0d7d120e59ed77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4881364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab660f64e3aad0f8f74d3a08909fe9013543eb07b61a9f8c6862b5db7d457d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:49:31 GMT
COPY file:6e54deb4ba87d6bff1f230123320fc7c9eee49d9a7456888efc872a22b9bd9ba in /nats-server 
# Thu, 18 May 2023 21:49:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:49:32 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:49:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41da3c5a1624a52c52a67beaa7b94c8c85a26f53b81e82e6dc05ae661adfebc1`  
		Last Modified: Thu, 18 May 2023 21:50:09 GMT  
		Size: 4.9 MB (4880856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df51ab38f5ab934d23f3b5429532106ef6baa2f64572f07ce9e5718e3f27374b`  
		Last Modified: Thu, 18 May 2023 21:50:08 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:94bf4a62f52fd647adb621d2d584e9c48aea06b124fb81cd59afed50252071bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4874864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8b8de1397d0af96648a1d02610dc54a066633c75eb548fc6be7e0d15497c3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:57:50 GMT
COPY file:31e26234e2abf1c16cd5869033f07320118e6dc458af341f37a27a3d12ffbc65 in /nats-server 
# Thu, 18 May 2023 21:57:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b6209c6f59228d4816baef6c05a38f68693937e6c86969581c57a1c7b68ccb40`  
		Last Modified: Thu, 18 May 2023 21:58:28 GMT  
		Size: 4.9 MB (4874355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69c5a4696da201d78c2dae749a6bce01c3a924afbdfa7e87c6797b8db238d4d`  
		Last Modified: Thu, 18 May 2023 21:58:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c4a7f923864c688cb5cc324df620960febd829b8d1f7074e4af3805caf5d5ceb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4685324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c4d84878abd37db0a2ba71386d26a2aaea2e989b4c3fc5f5930194da2e95c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:39:47 GMT
COPY file:b639df8cca07607378826468450a651a2cab9fb1be759ac266bf356bbfa2ac8c in /nats-server 
# Thu, 18 May 2023 21:39:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:39:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:39:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:39:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8e3bc385de2fea9fcd87e3f5b9809c6c133578671c906d0c1df657657c34664`  
		Last Modified: Thu, 18 May 2023 21:40:23 GMT  
		Size: 4.7 MB (4684816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d538df43ba01d77f25e465d3cce0829b2fbcf2a5ff131e1a42fda47b5c6c64`  
		Last Modified: Thu, 18 May 2023 21:40:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:d69e0d7dcf49ef2b8018b6dc2e7a751e91f3908ea7a3dab55fda01cda28b6a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:992902adab2316f4e0f1a0e7edbddad09cb2659bb7e26ed498ef39ebc86b5e20
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109563244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38a2aebef90db7b99751a2c93b984e1f7ca5acabedc0f61f40e08a00a740585`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:18:08 GMT
RUN cmd /S /C #(nop) COPY file:af4b677614d535ef3af8025256146a8f3389c5c6a4397c848e25544ea858eace in C:\nats-server.exe 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b004c7f9a3834a96e986a89e27e23aa329db101d8f291c2b5a3cdc913a1c57de`  
		Last Modified: Thu, 18 May 2023 22:18:56 GMT  
		Size: 5.2 MB (5172869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3456f5dbcfcadd4157124d47dec0661e9812e4db874cb74cb8e95be4c4ff246`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663f7b2aab72f936cdb391d59c87f99e0154634854724380b4f54daf05d300cc`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12ae8aa52c42d91abbe9fd8cd449efbcb465ac7b718d50e0589caa7436aebee`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f224e7b1c5810b30e107368e877ea6b7ca699eb4bcc4b27003aae49658d6f25`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:d69e0d7dcf49ef2b8018b6dc2e7a751e91f3908ea7a3dab55fda01cda28b6a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:992902adab2316f4e0f1a0e7edbddad09cb2659bb7e26ed498ef39ebc86b5e20
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109563244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38a2aebef90db7b99751a2c93b984e1f7ca5acabedc0f61f40e08a00a740585`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:18:08 GMT
RUN cmd /S /C #(nop) COPY file:af4b677614d535ef3af8025256146a8f3389c5c6a4397c848e25544ea858eace in C:\nats-server.exe 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b004c7f9a3834a96e986a89e27e23aa329db101d8f291c2b5a3cdc913a1c57de`  
		Last Modified: Thu, 18 May 2023 22:18:56 GMT  
		Size: 5.2 MB (5172869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3456f5dbcfcadd4157124d47dec0661e9812e4db874cb74cb8e95be4c4ff246`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663f7b2aab72f936cdb391d59c87f99e0154634854724380b4f54daf05d300cc`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12ae8aa52c42d91abbe9fd8cd449efbcb465ac7b718d50e0589caa7436aebee`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f224e7b1c5810b30e107368e877ea6b7ca699eb4bcc4b27003aae49658d6f25`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:8371b3bfc468a2294efb247531c2252c592398a98b574c2e81268d8c7f865d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:d7a57514cf7a0949ab8e63985f040f1fbaa01aa70aa50d8485f796a9a8dead08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd1a8b681814e86af7f1b07aa7178abd74163b5101ad1f855420c25d4afae5e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:19:59 GMT
COPY file:a3e4cfa40e3f87cbc1a2427fe9e77a182eed251b7a2f3037b894ac919acda56d in /nats-server 
# Thu, 18 May 2023 21:19:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:19:59 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:19:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:19:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e7f86c5b152db9b1815749cb2d298d36014c2905070ae66128b67029b4b31780`  
		Last Modified: Thu, 18 May 2023 21:20:38 GMT  
		Size: 5.1 MB (5116621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ce2c40f365197112db5bf1e3ed9b09b631da2058b456f99a50a5890fdda44`  
		Last Modified: Thu, 18 May 2023 21:20:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b93fec72f4aff1d673fd6ead1e244e694e4919368e246cc29e0d7d120e59ed77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4881364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab660f64e3aad0f8f74d3a08909fe9013543eb07b61a9f8c6862b5db7d457d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:49:31 GMT
COPY file:6e54deb4ba87d6bff1f230123320fc7c9eee49d9a7456888efc872a22b9bd9ba in /nats-server 
# Thu, 18 May 2023 21:49:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:49:32 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:49:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41da3c5a1624a52c52a67beaa7b94c8c85a26f53b81e82e6dc05ae661adfebc1`  
		Last Modified: Thu, 18 May 2023 21:50:09 GMT  
		Size: 4.9 MB (4880856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df51ab38f5ab934d23f3b5429532106ef6baa2f64572f07ce9e5718e3f27374b`  
		Last Modified: Thu, 18 May 2023 21:50:08 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:94bf4a62f52fd647adb621d2d584e9c48aea06b124fb81cd59afed50252071bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4874864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8b8de1397d0af96648a1d02610dc54a066633c75eb548fc6be7e0d15497c3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:57:50 GMT
COPY file:31e26234e2abf1c16cd5869033f07320118e6dc458af341f37a27a3d12ffbc65 in /nats-server 
# Thu, 18 May 2023 21:57:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b6209c6f59228d4816baef6c05a38f68693937e6c86969581c57a1c7b68ccb40`  
		Last Modified: Thu, 18 May 2023 21:58:28 GMT  
		Size: 4.9 MB (4874355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69c5a4696da201d78c2dae749a6bce01c3a924afbdfa7e87c6797b8db238d4d`  
		Last Modified: Thu, 18 May 2023 21:58:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c4a7f923864c688cb5cc324df620960febd829b8d1f7074e4af3805caf5d5ceb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4685324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c4d84878abd37db0a2ba71386d26a2aaea2e989b4c3fc5f5930194da2e95c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:39:47 GMT
COPY file:b639df8cca07607378826468450a651a2cab9fb1be759ac266bf356bbfa2ac8c in /nats-server 
# Thu, 18 May 2023 21:39:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:39:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:39:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:39:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8e3bc385de2fea9fcd87e3f5b9809c6c133578671c906d0c1df657657c34664`  
		Last Modified: Thu, 18 May 2023 21:40:23 GMT  
		Size: 4.7 MB (4684816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d538df43ba01d77f25e465d3cce0829b2fbcf2a5ff131e1a42fda47b5c6c64`  
		Last Modified: Thu, 18 May 2023 21:40:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:b66bd38321dbc1f4988181be5367eac0ddbcba3dd178ce291a1a01bc7ea11ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:7806ba994a1a25a836b54b8653c5e46d2a0237e0584f8f0e5d7bcf507a0102f0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077968206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d965773e9d5a5ab8056ef67b4ea971e23a0a74f14c81cf73f1676388001a7a61`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 01:56:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 May 2023 02:40:26 GMT
ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:15:10 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 22:15:10 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.17/nats-server-v2.9.17-windows-amd64.zip
# Thu, 18 May 2023 22:15:11 GMT
ENV NATS_SERVER_SHASUM=5648a1feb86600d6634fdc405a3b08b77ac8ee7695248c10587e9809a07baae8
# Thu, 18 May 2023 22:16:10 GMT
RUN Set-PSDebug -Trace 2
# Thu, 18 May 2023 22:17:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 18 May 2023 22:17:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:17:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:17:48 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:17:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a89be60a77cd8d520ec5f03d703ddbc15675dd1df4d95e041032cf08960af5`  
		Last Modified: Wed, 10 May 2023 02:23:36 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446cee93ab2781cfc08e135a3a7ab166e5342ee6817c34fb47e0662c085bbc29`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16b2ca8cf0615f148ab3c039e2da3946c641b998fa5342e0a86b86ef80497d5`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68aa5081f892e224d628f283c6eed1d4e424761f2ae3063fedacbc566aa10c75`  
		Last Modified: Thu, 18 May 2023 22:18:41 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e024e49e7a422a94a25d1d9af6e592192c04eb7c608b17ff1af3e93529c8a35e`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b22f5baa9cb4548ac8e10267dd54d7033e3ab44ad6a770205dc734933edfbdb`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 451.2 KB (451175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956556c3c6e7691c7107a0b6dcf1c63af3f8eb15efde6c70830a2e163cbbc171`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 5.5 MB (5468496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9da5547ee8802f531d1653edb8624b8b7f62423c2b007a3f28b211233fb598a`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f66377b577951e073ab005cd4b038ad3d581aed123c6e23df40968cae80056`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0008781bdc119b24b9cc4edb26bca6a3b72efae4f6931c96f2dff965fc1ccf`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b2a25b19d19214628ae2dff527abe8becb02247e0838187f5e2d679d87bffb`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:b66bd38321dbc1f4988181be5367eac0ddbcba3dd178ce291a1a01bc7ea11ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:7806ba994a1a25a836b54b8653c5e46d2a0237e0584f8f0e5d7bcf507a0102f0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077968206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d965773e9d5a5ab8056ef67b4ea971e23a0a74f14c81cf73f1676388001a7a61`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 01:56:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 May 2023 02:40:26 GMT
ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:15:10 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 22:15:10 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.17/nats-server-v2.9.17-windows-amd64.zip
# Thu, 18 May 2023 22:15:11 GMT
ENV NATS_SERVER_SHASUM=5648a1feb86600d6634fdc405a3b08b77ac8ee7695248c10587e9809a07baae8
# Thu, 18 May 2023 22:16:10 GMT
RUN Set-PSDebug -Trace 2
# Thu, 18 May 2023 22:17:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 18 May 2023 22:17:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:17:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:17:48 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:17:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a89be60a77cd8d520ec5f03d703ddbc15675dd1df4d95e041032cf08960af5`  
		Last Modified: Wed, 10 May 2023 02:23:36 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446cee93ab2781cfc08e135a3a7ab166e5342ee6817c34fb47e0662c085bbc29`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16b2ca8cf0615f148ab3c039e2da3946c641b998fa5342e0a86b86ef80497d5`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68aa5081f892e224d628f283c6eed1d4e424761f2ae3063fedacbc566aa10c75`  
		Last Modified: Thu, 18 May 2023 22:18:41 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e024e49e7a422a94a25d1d9af6e592192c04eb7c608b17ff1af3e93529c8a35e`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b22f5baa9cb4548ac8e10267dd54d7033e3ab44ad6a770205dc734933edfbdb`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 451.2 KB (451175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956556c3c6e7691c7107a0b6dcf1c63af3f8eb15efde6c70830a2e163cbbc171`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 5.5 MB (5468496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9da5547ee8802f531d1653edb8624b8b7f62423c2b007a3f28b211233fb598a`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f66377b577951e073ab005cd4b038ad3d581aed123c6e23df40968cae80056`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0008781bdc119b24b9cc4edb26bca6a3b72efae4f6931c96f2dff965fc1ccf`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b2a25b19d19214628ae2dff527abe8becb02247e0838187f5e2d679d87bffb`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:c366591c44da44fe1180ca3aaee4f18b959d2d8ab5170c5ebec98eda2d0cb390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4377; amd64

### `nats:2.9` - linux; amd64

```console
$ docker pull nats@sha256:d7a57514cf7a0949ab8e63985f040f1fbaa01aa70aa50d8485f796a9a8dead08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd1a8b681814e86af7f1b07aa7178abd74163b5101ad1f855420c25d4afae5e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:19:59 GMT
COPY file:a3e4cfa40e3f87cbc1a2427fe9e77a182eed251b7a2f3037b894ac919acda56d in /nats-server 
# Thu, 18 May 2023 21:19:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:19:59 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:19:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:19:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e7f86c5b152db9b1815749cb2d298d36014c2905070ae66128b67029b4b31780`  
		Last Modified: Thu, 18 May 2023 21:20:38 GMT  
		Size: 5.1 MB (5116621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ce2c40f365197112db5bf1e3ed9b09b631da2058b456f99a50a5890fdda44`  
		Last Modified: Thu, 18 May 2023 21:20:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:b93fec72f4aff1d673fd6ead1e244e694e4919368e246cc29e0d7d120e59ed77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4881364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab660f64e3aad0f8f74d3a08909fe9013543eb07b61a9f8c6862b5db7d457d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:49:31 GMT
COPY file:6e54deb4ba87d6bff1f230123320fc7c9eee49d9a7456888efc872a22b9bd9ba in /nats-server 
# Thu, 18 May 2023 21:49:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:49:32 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:49:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41da3c5a1624a52c52a67beaa7b94c8c85a26f53b81e82e6dc05ae661adfebc1`  
		Last Modified: Thu, 18 May 2023 21:50:09 GMT  
		Size: 4.9 MB (4880856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df51ab38f5ab934d23f3b5429532106ef6baa2f64572f07ce9e5718e3f27374b`  
		Last Modified: Thu, 18 May 2023 21:50:08 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:94bf4a62f52fd647adb621d2d584e9c48aea06b124fb81cd59afed50252071bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4874864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8b8de1397d0af96648a1d02610dc54a066633c75eb548fc6be7e0d15497c3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:57:50 GMT
COPY file:31e26234e2abf1c16cd5869033f07320118e6dc458af341f37a27a3d12ffbc65 in /nats-server 
# Thu, 18 May 2023 21:57:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b6209c6f59228d4816baef6c05a38f68693937e6c86969581c57a1c7b68ccb40`  
		Last Modified: Thu, 18 May 2023 21:58:28 GMT  
		Size: 4.9 MB (4874355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69c5a4696da201d78c2dae749a6bce01c3a924afbdfa7e87c6797b8db238d4d`  
		Last Modified: Thu, 18 May 2023 21:58:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c4a7f923864c688cb5cc324df620960febd829b8d1f7074e4af3805caf5d5ceb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4685324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c4d84878abd37db0a2ba71386d26a2aaea2e989b4c3fc5f5930194da2e95c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:39:47 GMT
COPY file:b639df8cca07607378826468450a651a2cab9fb1be759ac266bf356bbfa2ac8c in /nats-server 
# Thu, 18 May 2023 21:39:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:39:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:39:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:39:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8e3bc385de2fea9fcd87e3f5b9809c6c133578671c906d0c1df657657c34664`  
		Last Modified: Thu, 18 May 2023 21:40:23 GMT  
		Size: 4.7 MB (4684816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d538df43ba01d77f25e465d3cce0829b2fbcf2a5ff131e1a42fda47b5c6c64`  
		Last Modified: Thu, 18 May 2023 21:40:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:992902adab2316f4e0f1a0e7edbddad09cb2659bb7e26ed498ef39ebc86b5e20
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109563244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38a2aebef90db7b99751a2c93b984e1f7ca5acabedc0f61f40e08a00a740585`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:18:08 GMT
RUN cmd /S /C #(nop) COPY file:af4b677614d535ef3af8025256146a8f3389c5c6a4397c848e25544ea858eace in C:\nats-server.exe 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b004c7f9a3834a96e986a89e27e23aa329db101d8f291c2b5a3cdc913a1c57de`  
		Last Modified: Thu, 18 May 2023 22:18:56 GMT  
		Size: 5.2 MB (5172869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3456f5dbcfcadd4157124d47dec0661e9812e4db874cb74cb8e95be4c4ff246`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663f7b2aab72f936cdb391d59c87f99e0154634854724380b4f54daf05d300cc`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12ae8aa52c42d91abbe9fd8cd449efbcb465ac7b718d50e0589caa7436aebee`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f224e7b1c5810b30e107368e877ea6b7ca699eb4bcc4b27003aae49658d6f25`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine`

```console
$ docker pull nats@sha256:1a7b320b294218d11b48ddcd1552a18a74ae8790c80ba5372726c58d0a5ee295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:7544f1dfe4b270789a68e2056135467d525da411f331f43640150b0642dee693
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8802768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ada7bbdb360a5406551ced3593bc48e57c6cea5ee5d502e1a0df2437156d06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:19:49 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:19:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:19:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:19:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:19:52 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:19:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba69a821f226517d8763fd5007b51eeb8a68e40f7fb32dec75e13297ea1cb49`  
		Last Modified: Thu, 18 May 2023 21:20:19 GMT  
		Size: 5.4 MB (5404276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ad2f9c9076c4ccedf3a056bf6e996a658fa5ece8cc35913e4728d58617e8b3`  
		Last Modified: Thu, 18 May 2023 21:20:18 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb3c123b7bd114e7897ddf602c16bcd18f034abda3ee53d91a108b71c624faa`  
		Last Modified: Thu, 18 May 2023 21:20:18 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:08b7d50259bf79d1f0cc5476da2707cbe3723f8b25ececd27b4e20f5c3ba036e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8325871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676517e73baa5d6c0a13a665dcf0412659d93274c96643829ff67835d5e4905d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:04 GMT
ADD file:f87a991e2e9f185fd4a88569d86a9b8e5bc07182e7fa613b95acab25986f2a6c in / 
# Tue, 09 May 2023 23:11:04 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:49:22 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:49:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:49:24 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:49:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:015ee8d9fb3dca1b18815f1e4ee0d325d1f40cde6f2df4dd307918f7b69167d7`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.2 MB (3155679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06976c3bb336d8c3936e2bbb8d27dbd5b805054e1064aaf7c651d6fd5523aa71`  
		Last Modified: Thu, 18 May 2023 21:49:48 GMT  
		Size: 5.2 MB (5169192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c85a9f3b4246d93c82583c9d4336cb58688e4b311be41f752bc0c9456a2135`  
		Last Modified: Thu, 18 May 2023 21:49:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6d307fb0f80f02bb15dbdbb0eba31d3a463afa38dca28f6cd0e913798ebf62`  
		Last Modified: Thu, 18 May 2023 21:49:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:882066add3894dc13cfadaeec8af9f9fce5b9c3fee92e377a13f0997a88a121f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8071388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574536f22d8de67b2c2f0962d9e7d108bb4b41d07cb13a05ebab5e3b82fe6d63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 22:57:32 GMT
ADD file:eb6b6a885e8ac9bccbf44a5c673b8542c8144bba927376688240446c2f413b10 in / 
# Tue, 09 May 2023 22:57:32 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:57:27 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:57:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:57:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:57:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:57:29 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:57:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e14425cf8fb9304b9ad4a9d1250e0d4c22e507a334ff747fa69b804500afc113`  
		Last Modified: Tue, 09 May 2023 22:57:50 GMT  
		Size: 2.9 MB (2911117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213de106e11b3e7261faf48da426167af8702e8a56ab0237f786ba0eb864a38d`  
		Last Modified: Thu, 18 May 2023 21:58:08 GMT  
		Size: 5.2 MB (5159272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5535f74851ba24bbb57849b9f7085eb8441d584ea938b19bdd027f5ccf52a193`  
		Last Modified: Thu, 18 May 2023 21:58:07 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2518eda2d1b2ce9ae4c75acdccc0d3bbe028cfbdf30d7e173dfa82e489af6ec`  
		Last Modified: Thu, 18 May 2023 21:58:08 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:36980286981e9058cd3f3a1f58fb92741d5ba73ff1a66d3b8ef7b98e23ab8377
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8313998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1348d24d9abc62396994637b0c3153212850856ce4ab5c1cc49194dd4ef4872e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:39:41 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:39:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:39:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:39:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:39:43 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:39:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8409748378eca62a6e13533d1f6fef38e6b40a7ad726dff04ad548a63ae20313`  
		Last Modified: Thu, 18 May 2023 21:40:03 GMT  
		Size: 5.0 MB (4970150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a822f2037d3c235b73c5f9924d54c4de71f06b2ba22757fc2a059c4f33d5c6`  
		Last Modified: Thu, 18 May 2023 21:40:02 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94f121392ee621f9e3f1aaa44685e70de92e169d23c2c547ba2d5172904b49d`  
		Last Modified: Thu, 18 May 2023 21:40:02 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.18`

```console
$ docker pull nats@sha256:1a7b320b294218d11b48ddcd1552a18a74ae8790c80ba5372726c58d0a5ee295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:7544f1dfe4b270789a68e2056135467d525da411f331f43640150b0642dee693
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8802768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ada7bbdb360a5406551ced3593bc48e57c6cea5ee5d502e1a0df2437156d06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:19:49 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:19:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:19:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:19:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:19:52 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:19:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba69a821f226517d8763fd5007b51eeb8a68e40f7fb32dec75e13297ea1cb49`  
		Last Modified: Thu, 18 May 2023 21:20:19 GMT  
		Size: 5.4 MB (5404276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ad2f9c9076c4ccedf3a056bf6e996a658fa5ece8cc35913e4728d58617e8b3`  
		Last Modified: Thu, 18 May 2023 21:20:18 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb3c123b7bd114e7897ddf602c16bcd18f034abda3ee53d91a108b71c624faa`  
		Last Modified: Thu, 18 May 2023 21:20:18 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:08b7d50259bf79d1f0cc5476da2707cbe3723f8b25ececd27b4e20f5c3ba036e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8325871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676517e73baa5d6c0a13a665dcf0412659d93274c96643829ff67835d5e4905d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:04 GMT
ADD file:f87a991e2e9f185fd4a88569d86a9b8e5bc07182e7fa613b95acab25986f2a6c in / 
# Tue, 09 May 2023 23:11:04 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:49:22 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:49:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:49:24 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:49:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:015ee8d9fb3dca1b18815f1e4ee0d325d1f40cde6f2df4dd307918f7b69167d7`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.2 MB (3155679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06976c3bb336d8c3936e2bbb8d27dbd5b805054e1064aaf7c651d6fd5523aa71`  
		Last Modified: Thu, 18 May 2023 21:49:48 GMT  
		Size: 5.2 MB (5169192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c85a9f3b4246d93c82583c9d4336cb58688e4b311be41f752bc0c9456a2135`  
		Last Modified: Thu, 18 May 2023 21:49:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6d307fb0f80f02bb15dbdbb0eba31d3a463afa38dca28f6cd0e913798ebf62`  
		Last Modified: Thu, 18 May 2023 21:49:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:882066add3894dc13cfadaeec8af9f9fce5b9c3fee92e377a13f0997a88a121f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8071388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574536f22d8de67b2c2f0962d9e7d108bb4b41d07cb13a05ebab5e3b82fe6d63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 22:57:32 GMT
ADD file:eb6b6a885e8ac9bccbf44a5c673b8542c8144bba927376688240446c2f413b10 in / 
# Tue, 09 May 2023 22:57:32 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:57:27 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:57:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:57:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:57:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:57:29 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:57:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e14425cf8fb9304b9ad4a9d1250e0d4c22e507a334ff747fa69b804500afc113`  
		Last Modified: Tue, 09 May 2023 22:57:50 GMT  
		Size: 2.9 MB (2911117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213de106e11b3e7261faf48da426167af8702e8a56ab0237f786ba0eb864a38d`  
		Last Modified: Thu, 18 May 2023 21:58:08 GMT  
		Size: 5.2 MB (5159272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5535f74851ba24bbb57849b9f7085eb8441d584ea938b19bdd027f5ccf52a193`  
		Last Modified: Thu, 18 May 2023 21:58:07 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2518eda2d1b2ce9ae4c75acdccc0d3bbe028cfbdf30d7e173dfa82e489af6ec`  
		Last Modified: Thu, 18 May 2023 21:58:08 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:36980286981e9058cd3f3a1f58fb92741d5ba73ff1a66d3b8ef7b98e23ab8377
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8313998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1348d24d9abc62396994637b0c3153212850856ce4ab5c1cc49194dd4ef4872e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:39:41 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:39:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:39:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:39:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:39:43 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:39:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8409748378eca62a6e13533d1f6fef38e6b40a7ad726dff04ad548a63ae20313`  
		Last Modified: Thu, 18 May 2023 21:40:03 GMT  
		Size: 5.0 MB (4970150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a822f2037d3c235b73c5f9924d54c4de71f06b2ba22757fc2a059c4f33d5c6`  
		Last Modified: Thu, 18 May 2023 21:40:02 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94f121392ee621f9e3f1aaa44685e70de92e169d23c2c547ba2d5172904b49d`  
		Last Modified: Thu, 18 May 2023 21:40:02 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-linux`

```console
$ docker pull nats@sha256:8371b3bfc468a2294efb247531c2252c592398a98b574c2e81268d8c7f865d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:d7a57514cf7a0949ab8e63985f040f1fbaa01aa70aa50d8485f796a9a8dead08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd1a8b681814e86af7f1b07aa7178abd74163b5101ad1f855420c25d4afae5e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:19:59 GMT
COPY file:a3e4cfa40e3f87cbc1a2427fe9e77a182eed251b7a2f3037b894ac919acda56d in /nats-server 
# Thu, 18 May 2023 21:19:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:19:59 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:19:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:19:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e7f86c5b152db9b1815749cb2d298d36014c2905070ae66128b67029b4b31780`  
		Last Modified: Thu, 18 May 2023 21:20:38 GMT  
		Size: 5.1 MB (5116621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ce2c40f365197112db5bf1e3ed9b09b631da2058b456f99a50a5890fdda44`  
		Last Modified: Thu, 18 May 2023 21:20:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:b93fec72f4aff1d673fd6ead1e244e694e4919368e246cc29e0d7d120e59ed77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4881364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab660f64e3aad0f8f74d3a08909fe9013543eb07b61a9f8c6862b5db7d457d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:49:31 GMT
COPY file:6e54deb4ba87d6bff1f230123320fc7c9eee49d9a7456888efc872a22b9bd9ba in /nats-server 
# Thu, 18 May 2023 21:49:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:49:32 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:49:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41da3c5a1624a52c52a67beaa7b94c8c85a26f53b81e82e6dc05ae661adfebc1`  
		Last Modified: Thu, 18 May 2023 21:50:09 GMT  
		Size: 4.9 MB (4880856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df51ab38f5ab934d23f3b5429532106ef6baa2f64572f07ce9e5718e3f27374b`  
		Last Modified: Thu, 18 May 2023 21:50:08 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:94bf4a62f52fd647adb621d2d584e9c48aea06b124fb81cd59afed50252071bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4874864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8b8de1397d0af96648a1d02610dc54a066633c75eb548fc6be7e0d15497c3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:57:50 GMT
COPY file:31e26234e2abf1c16cd5869033f07320118e6dc458af341f37a27a3d12ffbc65 in /nats-server 
# Thu, 18 May 2023 21:57:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b6209c6f59228d4816baef6c05a38f68693937e6c86969581c57a1c7b68ccb40`  
		Last Modified: Thu, 18 May 2023 21:58:28 GMT  
		Size: 4.9 MB (4874355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69c5a4696da201d78c2dae749a6bce01c3a924afbdfa7e87c6797b8db238d4d`  
		Last Modified: Thu, 18 May 2023 21:58:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c4a7f923864c688cb5cc324df620960febd829b8d1f7074e4af3805caf5d5ceb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4685324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c4d84878abd37db0a2ba71386d26a2aaea2e989b4c3fc5f5930194da2e95c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:39:47 GMT
COPY file:b639df8cca07607378826468450a651a2cab9fb1be759ac266bf356bbfa2ac8c in /nats-server 
# Thu, 18 May 2023 21:39:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:39:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:39:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:39:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8e3bc385de2fea9fcd87e3f5b9809c6c133578671c906d0c1df657657c34664`  
		Last Modified: Thu, 18 May 2023 21:40:23 GMT  
		Size: 4.7 MB (4684816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d538df43ba01d77f25e465d3cce0829b2fbcf2a5ff131e1a42fda47b5c6c64`  
		Last Modified: Thu, 18 May 2023 21:40:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver`

```console
$ docker pull nats@sha256:d69e0d7dcf49ef2b8018b6dc2e7a751e91f3908ea7a3dab55fda01cda28b6a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:992902adab2316f4e0f1a0e7edbddad09cb2659bb7e26ed498ef39ebc86b5e20
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109563244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38a2aebef90db7b99751a2c93b984e1f7ca5acabedc0f61f40e08a00a740585`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:18:08 GMT
RUN cmd /S /C #(nop) COPY file:af4b677614d535ef3af8025256146a8f3389c5c6a4397c848e25544ea858eace in C:\nats-server.exe 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b004c7f9a3834a96e986a89e27e23aa329db101d8f291c2b5a3cdc913a1c57de`  
		Last Modified: Thu, 18 May 2023 22:18:56 GMT  
		Size: 5.2 MB (5172869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3456f5dbcfcadd4157124d47dec0661e9812e4db874cb74cb8e95be4c4ff246`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663f7b2aab72f936cdb391d59c87f99e0154634854724380b4f54daf05d300cc`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12ae8aa52c42d91abbe9fd8cd449efbcb465ac7b718d50e0589caa7436aebee`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f224e7b1c5810b30e107368e877ea6b7ca699eb4bcc4b27003aae49658d6f25`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:d69e0d7dcf49ef2b8018b6dc2e7a751e91f3908ea7a3dab55fda01cda28b6a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:992902adab2316f4e0f1a0e7edbddad09cb2659bb7e26ed498ef39ebc86b5e20
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109563244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38a2aebef90db7b99751a2c93b984e1f7ca5acabedc0f61f40e08a00a740585`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:18:08 GMT
RUN cmd /S /C #(nop) COPY file:af4b677614d535ef3af8025256146a8f3389c5c6a4397c848e25544ea858eace in C:\nats-server.exe 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b004c7f9a3834a96e986a89e27e23aa329db101d8f291c2b5a3cdc913a1c57de`  
		Last Modified: Thu, 18 May 2023 22:18:56 GMT  
		Size: 5.2 MB (5172869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3456f5dbcfcadd4157124d47dec0661e9812e4db874cb74cb8e95be4c4ff246`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663f7b2aab72f936cdb391d59c87f99e0154634854724380b4f54daf05d300cc`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12ae8aa52c42d91abbe9fd8cd449efbcb465ac7b718d50e0589caa7436aebee`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f224e7b1c5810b30e107368e877ea6b7ca699eb4bcc4b27003aae49658d6f25`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:8371b3bfc468a2294efb247531c2252c592398a98b574c2e81268d8c7f865d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:d7a57514cf7a0949ab8e63985f040f1fbaa01aa70aa50d8485f796a9a8dead08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd1a8b681814e86af7f1b07aa7178abd74163b5101ad1f855420c25d4afae5e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:19:59 GMT
COPY file:a3e4cfa40e3f87cbc1a2427fe9e77a182eed251b7a2f3037b894ac919acda56d in /nats-server 
# Thu, 18 May 2023 21:19:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:19:59 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:19:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:19:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e7f86c5b152db9b1815749cb2d298d36014c2905070ae66128b67029b4b31780`  
		Last Modified: Thu, 18 May 2023 21:20:38 GMT  
		Size: 5.1 MB (5116621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ce2c40f365197112db5bf1e3ed9b09b631da2058b456f99a50a5890fdda44`  
		Last Modified: Thu, 18 May 2023 21:20:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b93fec72f4aff1d673fd6ead1e244e694e4919368e246cc29e0d7d120e59ed77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4881364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab660f64e3aad0f8f74d3a08909fe9013543eb07b61a9f8c6862b5db7d457d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:49:31 GMT
COPY file:6e54deb4ba87d6bff1f230123320fc7c9eee49d9a7456888efc872a22b9bd9ba in /nats-server 
# Thu, 18 May 2023 21:49:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:49:32 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:49:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41da3c5a1624a52c52a67beaa7b94c8c85a26f53b81e82e6dc05ae661adfebc1`  
		Last Modified: Thu, 18 May 2023 21:50:09 GMT  
		Size: 4.9 MB (4880856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df51ab38f5ab934d23f3b5429532106ef6baa2f64572f07ce9e5718e3f27374b`  
		Last Modified: Thu, 18 May 2023 21:50:08 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:94bf4a62f52fd647adb621d2d584e9c48aea06b124fb81cd59afed50252071bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4874864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8b8de1397d0af96648a1d02610dc54a066633c75eb548fc6be7e0d15497c3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:57:50 GMT
COPY file:31e26234e2abf1c16cd5869033f07320118e6dc458af341f37a27a3d12ffbc65 in /nats-server 
# Thu, 18 May 2023 21:57:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b6209c6f59228d4816baef6c05a38f68693937e6c86969581c57a1c7b68ccb40`  
		Last Modified: Thu, 18 May 2023 21:58:28 GMT  
		Size: 4.9 MB (4874355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69c5a4696da201d78c2dae749a6bce01c3a924afbdfa7e87c6797b8db238d4d`  
		Last Modified: Thu, 18 May 2023 21:58:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c4a7f923864c688cb5cc324df620960febd829b8d1f7074e4af3805caf5d5ceb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4685324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c4d84878abd37db0a2ba71386d26a2aaea2e989b4c3fc5f5930194da2e95c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:39:47 GMT
COPY file:b639df8cca07607378826468450a651a2cab9fb1be759ac266bf356bbfa2ac8c in /nats-server 
# Thu, 18 May 2023 21:39:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:39:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:39:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:39:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8e3bc385de2fea9fcd87e3f5b9809c6c133578671c906d0c1df657657c34664`  
		Last Modified: Thu, 18 May 2023 21:40:23 GMT  
		Size: 4.7 MB (4684816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d538df43ba01d77f25e465d3cce0829b2fbcf2a5ff131e1a42fda47b5c6c64`  
		Last Modified: Thu, 18 May 2023 21:40:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore`

```console
$ docker pull nats@sha256:b66bd38321dbc1f4988181be5367eac0ddbcba3dd178ce291a1a01bc7ea11ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:7806ba994a1a25a836b54b8653c5e46d2a0237e0584f8f0e5d7bcf507a0102f0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077968206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d965773e9d5a5ab8056ef67b4ea971e23a0a74f14c81cf73f1676388001a7a61`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 01:56:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 May 2023 02:40:26 GMT
ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:15:10 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 22:15:10 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.17/nats-server-v2.9.17-windows-amd64.zip
# Thu, 18 May 2023 22:15:11 GMT
ENV NATS_SERVER_SHASUM=5648a1feb86600d6634fdc405a3b08b77ac8ee7695248c10587e9809a07baae8
# Thu, 18 May 2023 22:16:10 GMT
RUN Set-PSDebug -Trace 2
# Thu, 18 May 2023 22:17:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 18 May 2023 22:17:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:17:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:17:48 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:17:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a89be60a77cd8d520ec5f03d703ddbc15675dd1df4d95e041032cf08960af5`  
		Last Modified: Wed, 10 May 2023 02:23:36 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446cee93ab2781cfc08e135a3a7ab166e5342ee6817c34fb47e0662c085bbc29`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16b2ca8cf0615f148ab3c039e2da3946c641b998fa5342e0a86b86ef80497d5`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68aa5081f892e224d628f283c6eed1d4e424761f2ae3063fedacbc566aa10c75`  
		Last Modified: Thu, 18 May 2023 22:18:41 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e024e49e7a422a94a25d1d9af6e592192c04eb7c608b17ff1af3e93529c8a35e`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b22f5baa9cb4548ac8e10267dd54d7033e3ab44ad6a770205dc734933edfbdb`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 451.2 KB (451175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956556c3c6e7691c7107a0b6dcf1c63af3f8eb15efde6c70830a2e163cbbc171`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 5.5 MB (5468496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9da5547ee8802f531d1653edb8624b8b7f62423c2b007a3f28b211233fb598a`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f66377b577951e073ab005cd4b038ad3d581aed123c6e23df40968cae80056`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0008781bdc119b24b9cc4edb26bca6a3b72efae4f6931c96f2dff965fc1ccf`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b2a25b19d19214628ae2dff527abe8becb02247e0838187f5e2d679d87bffb`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:b66bd38321dbc1f4988181be5367eac0ddbcba3dd178ce291a1a01bc7ea11ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:7806ba994a1a25a836b54b8653c5e46d2a0237e0584f8f0e5d7bcf507a0102f0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077968206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d965773e9d5a5ab8056ef67b4ea971e23a0a74f14c81cf73f1676388001a7a61`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 01:56:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 May 2023 02:40:26 GMT
ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:15:10 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 22:15:10 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.17/nats-server-v2.9.17-windows-amd64.zip
# Thu, 18 May 2023 22:15:11 GMT
ENV NATS_SERVER_SHASUM=5648a1feb86600d6634fdc405a3b08b77ac8ee7695248c10587e9809a07baae8
# Thu, 18 May 2023 22:16:10 GMT
RUN Set-PSDebug -Trace 2
# Thu, 18 May 2023 22:17:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 18 May 2023 22:17:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:17:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:17:48 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:17:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a89be60a77cd8d520ec5f03d703ddbc15675dd1df4d95e041032cf08960af5`  
		Last Modified: Wed, 10 May 2023 02:23:36 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446cee93ab2781cfc08e135a3a7ab166e5342ee6817c34fb47e0662c085bbc29`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16b2ca8cf0615f148ab3c039e2da3946c641b998fa5342e0a86b86ef80497d5`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68aa5081f892e224d628f283c6eed1d4e424761f2ae3063fedacbc566aa10c75`  
		Last Modified: Thu, 18 May 2023 22:18:41 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e024e49e7a422a94a25d1d9af6e592192c04eb7c608b17ff1af3e93529c8a35e`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b22f5baa9cb4548ac8e10267dd54d7033e3ab44ad6a770205dc734933edfbdb`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 451.2 KB (451175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956556c3c6e7691c7107a0b6dcf1c63af3f8eb15efde6c70830a2e163cbbc171`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 5.5 MB (5468496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9da5547ee8802f531d1653edb8624b8b7f62423c2b007a3f28b211233fb598a`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f66377b577951e073ab005cd4b038ad3d581aed123c6e23df40968cae80056`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0008781bdc119b24b9cc4edb26bca6a3b72efae4f6931c96f2dff965fc1ccf`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b2a25b19d19214628ae2dff527abe8becb02247e0838187f5e2d679d87bffb`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.17`

```console
$ docker pull nats@sha256:c366591c44da44fe1180ca3aaee4f18b959d2d8ab5170c5ebec98eda2d0cb390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4377; amd64

### `nats:2.9.17` - linux; amd64

```console
$ docker pull nats@sha256:d7a57514cf7a0949ab8e63985f040f1fbaa01aa70aa50d8485f796a9a8dead08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd1a8b681814e86af7f1b07aa7178abd74163b5101ad1f855420c25d4afae5e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:19:59 GMT
COPY file:a3e4cfa40e3f87cbc1a2427fe9e77a182eed251b7a2f3037b894ac919acda56d in /nats-server 
# Thu, 18 May 2023 21:19:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:19:59 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:19:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:19:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e7f86c5b152db9b1815749cb2d298d36014c2905070ae66128b67029b4b31780`  
		Last Modified: Thu, 18 May 2023 21:20:38 GMT  
		Size: 5.1 MB (5116621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ce2c40f365197112db5bf1e3ed9b09b631da2058b456f99a50a5890fdda44`  
		Last Modified: Thu, 18 May 2023 21:20:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.17` - linux; arm variant v6

```console
$ docker pull nats@sha256:b93fec72f4aff1d673fd6ead1e244e694e4919368e246cc29e0d7d120e59ed77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4881364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab660f64e3aad0f8f74d3a08909fe9013543eb07b61a9f8c6862b5db7d457d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:49:31 GMT
COPY file:6e54deb4ba87d6bff1f230123320fc7c9eee49d9a7456888efc872a22b9bd9ba in /nats-server 
# Thu, 18 May 2023 21:49:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:49:32 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:49:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41da3c5a1624a52c52a67beaa7b94c8c85a26f53b81e82e6dc05ae661adfebc1`  
		Last Modified: Thu, 18 May 2023 21:50:09 GMT  
		Size: 4.9 MB (4880856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df51ab38f5ab934d23f3b5429532106ef6baa2f64572f07ce9e5718e3f27374b`  
		Last Modified: Thu, 18 May 2023 21:50:08 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.17` - linux; arm variant v7

```console
$ docker pull nats@sha256:94bf4a62f52fd647adb621d2d584e9c48aea06b124fb81cd59afed50252071bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4874864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8b8de1397d0af96648a1d02610dc54a066633c75eb548fc6be7e0d15497c3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:57:50 GMT
COPY file:31e26234e2abf1c16cd5869033f07320118e6dc458af341f37a27a3d12ffbc65 in /nats-server 
# Thu, 18 May 2023 21:57:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b6209c6f59228d4816baef6c05a38f68693937e6c86969581c57a1c7b68ccb40`  
		Last Modified: Thu, 18 May 2023 21:58:28 GMT  
		Size: 4.9 MB (4874355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69c5a4696da201d78c2dae749a6bce01c3a924afbdfa7e87c6797b8db238d4d`  
		Last Modified: Thu, 18 May 2023 21:58:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.17` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c4a7f923864c688cb5cc324df620960febd829b8d1f7074e4af3805caf5d5ceb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4685324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c4d84878abd37db0a2ba71386d26a2aaea2e989b4c3fc5f5930194da2e95c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:39:47 GMT
COPY file:b639df8cca07607378826468450a651a2cab9fb1be759ac266bf356bbfa2ac8c in /nats-server 
# Thu, 18 May 2023 21:39:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:39:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:39:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:39:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8e3bc385de2fea9fcd87e3f5b9809c6c133578671c906d0c1df657657c34664`  
		Last Modified: Thu, 18 May 2023 21:40:23 GMT  
		Size: 4.7 MB (4684816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d538df43ba01d77f25e465d3cce0829b2fbcf2a5ff131e1a42fda47b5c6c64`  
		Last Modified: Thu, 18 May 2023 21:40:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.17` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:992902adab2316f4e0f1a0e7edbddad09cb2659bb7e26ed498ef39ebc86b5e20
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109563244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38a2aebef90db7b99751a2c93b984e1f7ca5acabedc0f61f40e08a00a740585`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:18:08 GMT
RUN cmd /S /C #(nop) COPY file:af4b677614d535ef3af8025256146a8f3389c5c6a4397c848e25544ea858eace in C:\nats-server.exe 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b004c7f9a3834a96e986a89e27e23aa329db101d8f291c2b5a3cdc913a1c57de`  
		Last Modified: Thu, 18 May 2023 22:18:56 GMT  
		Size: 5.2 MB (5172869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3456f5dbcfcadd4157124d47dec0661e9812e4db874cb74cb8e95be4c4ff246`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663f7b2aab72f936cdb391d59c87f99e0154634854724380b4f54daf05d300cc`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12ae8aa52c42d91abbe9fd8cd449efbcb465ac7b718d50e0589caa7436aebee`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f224e7b1c5810b30e107368e877ea6b7ca699eb4bcc4b27003aae49658d6f25`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.17-alpine`

```console
$ docker pull nats@sha256:1a7b320b294218d11b48ddcd1552a18a74ae8790c80ba5372726c58d0a5ee295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.17-alpine` - linux; amd64

```console
$ docker pull nats@sha256:7544f1dfe4b270789a68e2056135467d525da411f331f43640150b0642dee693
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8802768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ada7bbdb360a5406551ced3593bc48e57c6cea5ee5d502e1a0df2437156d06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:19:49 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:19:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:19:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:19:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:19:52 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:19:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba69a821f226517d8763fd5007b51eeb8a68e40f7fb32dec75e13297ea1cb49`  
		Last Modified: Thu, 18 May 2023 21:20:19 GMT  
		Size: 5.4 MB (5404276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ad2f9c9076c4ccedf3a056bf6e996a658fa5ece8cc35913e4728d58617e8b3`  
		Last Modified: Thu, 18 May 2023 21:20:18 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb3c123b7bd114e7897ddf602c16bcd18f034abda3ee53d91a108b71c624faa`  
		Last Modified: Thu, 18 May 2023 21:20:18 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.17-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:08b7d50259bf79d1f0cc5476da2707cbe3723f8b25ececd27b4e20f5c3ba036e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8325871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676517e73baa5d6c0a13a665dcf0412659d93274c96643829ff67835d5e4905d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:04 GMT
ADD file:f87a991e2e9f185fd4a88569d86a9b8e5bc07182e7fa613b95acab25986f2a6c in / 
# Tue, 09 May 2023 23:11:04 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:49:22 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:49:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:49:24 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:49:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:015ee8d9fb3dca1b18815f1e4ee0d325d1f40cde6f2df4dd307918f7b69167d7`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.2 MB (3155679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06976c3bb336d8c3936e2bbb8d27dbd5b805054e1064aaf7c651d6fd5523aa71`  
		Last Modified: Thu, 18 May 2023 21:49:48 GMT  
		Size: 5.2 MB (5169192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c85a9f3b4246d93c82583c9d4336cb58688e4b311be41f752bc0c9456a2135`  
		Last Modified: Thu, 18 May 2023 21:49:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6d307fb0f80f02bb15dbdbb0eba31d3a463afa38dca28f6cd0e913798ebf62`  
		Last Modified: Thu, 18 May 2023 21:49:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.17-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:882066add3894dc13cfadaeec8af9f9fce5b9c3fee92e377a13f0997a88a121f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8071388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574536f22d8de67b2c2f0962d9e7d108bb4b41d07cb13a05ebab5e3b82fe6d63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 22:57:32 GMT
ADD file:eb6b6a885e8ac9bccbf44a5c673b8542c8144bba927376688240446c2f413b10 in / 
# Tue, 09 May 2023 22:57:32 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:57:27 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:57:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:57:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:57:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:57:29 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:57:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e14425cf8fb9304b9ad4a9d1250e0d4c22e507a334ff747fa69b804500afc113`  
		Last Modified: Tue, 09 May 2023 22:57:50 GMT  
		Size: 2.9 MB (2911117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213de106e11b3e7261faf48da426167af8702e8a56ab0237f786ba0eb864a38d`  
		Last Modified: Thu, 18 May 2023 21:58:08 GMT  
		Size: 5.2 MB (5159272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5535f74851ba24bbb57849b9f7085eb8441d584ea938b19bdd027f5ccf52a193`  
		Last Modified: Thu, 18 May 2023 21:58:07 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2518eda2d1b2ce9ae4c75acdccc0d3bbe028cfbdf30d7e173dfa82e489af6ec`  
		Last Modified: Thu, 18 May 2023 21:58:08 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.17-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:36980286981e9058cd3f3a1f58fb92741d5ba73ff1a66d3b8ef7b98e23ab8377
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8313998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1348d24d9abc62396994637b0c3153212850856ce4ab5c1cc49194dd4ef4872e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:39:41 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:39:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:39:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:39:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:39:43 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:39:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8409748378eca62a6e13533d1f6fef38e6b40a7ad726dff04ad548a63ae20313`  
		Last Modified: Thu, 18 May 2023 21:40:03 GMT  
		Size: 5.0 MB (4970150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a822f2037d3c235b73c5f9924d54c4de71f06b2ba22757fc2a059c4f33d5c6`  
		Last Modified: Thu, 18 May 2023 21:40:02 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94f121392ee621f9e3f1aaa44685e70de92e169d23c2c547ba2d5172904b49d`  
		Last Modified: Thu, 18 May 2023 21:40:02 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.17-alpine3.18`

```console
$ docker pull nats@sha256:1a7b320b294218d11b48ddcd1552a18a74ae8790c80ba5372726c58d0a5ee295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.17-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:7544f1dfe4b270789a68e2056135467d525da411f331f43640150b0642dee693
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8802768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ada7bbdb360a5406551ced3593bc48e57c6cea5ee5d502e1a0df2437156d06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:19:49 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:19:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:19:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:19:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:19:52 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:19:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba69a821f226517d8763fd5007b51eeb8a68e40f7fb32dec75e13297ea1cb49`  
		Last Modified: Thu, 18 May 2023 21:20:19 GMT  
		Size: 5.4 MB (5404276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ad2f9c9076c4ccedf3a056bf6e996a658fa5ece8cc35913e4728d58617e8b3`  
		Last Modified: Thu, 18 May 2023 21:20:18 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb3c123b7bd114e7897ddf602c16bcd18f034abda3ee53d91a108b71c624faa`  
		Last Modified: Thu, 18 May 2023 21:20:18 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.17-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:08b7d50259bf79d1f0cc5476da2707cbe3723f8b25ececd27b4e20f5c3ba036e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8325871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676517e73baa5d6c0a13a665dcf0412659d93274c96643829ff67835d5e4905d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:04 GMT
ADD file:f87a991e2e9f185fd4a88569d86a9b8e5bc07182e7fa613b95acab25986f2a6c in / 
# Tue, 09 May 2023 23:11:04 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:49:22 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:49:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:49:24 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:49:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:015ee8d9fb3dca1b18815f1e4ee0d325d1f40cde6f2df4dd307918f7b69167d7`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.2 MB (3155679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06976c3bb336d8c3936e2bbb8d27dbd5b805054e1064aaf7c651d6fd5523aa71`  
		Last Modified: Thu, 18 May 2023 21:49:48 GMT  
		Size: 5.2 MB (5169192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c85a9f3b4246d93c82583c9d4336cb58688e4b311be41f752bc0c9456a2135`  
		Last Modified: Thu, 18 May 2023 21:49:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6d307fb0f80f02bb15dbdbb0eba31d3a463afa38dca28f6cd0e913798ebf62`  
		Last Modified: Thu, 18 May 2023 21:49:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.17-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:882066add3894dc13cfadaeec8af9f9fce5b9c3fee92e377a13f0997a88a121f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8071388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574536f22d8de67b2c2f0962d9e7d108bb4b41d07cb13a05ebab5e3b82fe6d63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 22:57:32 GMT
ADD file:eb6b6a885e8ac9bccbf44a5c673b8542c8144bba927376688240446c2f413b10 in / 
# Tue, 09 May 2023 22:57:32 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:57:27 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:57:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:57:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:57:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:57:29 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:57:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e14425cf8fb9304b9ad4a9d1250e0d4c22e507a334ff747fa69b804500afc113`  
		Last Modified: Tue, 09 May 2023 22:57:50 GMT  
		Size: 2.9 MB (2911117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213de106e11b3e7261faf48da426167af8702e8a56ab0237f786ba0eb864a38d`  
		Last Modified: Thu, 18 May 2023 21:58:08 GMT  
		Size: 5.2 MB (5159272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5535f74851ba24bbb57849b9f7085eb8441d584ea938b19bdd027f5ccf52a193`  
		Last Modified: Thu, 18 May 2023 21:58:07 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2518eda2d1b2ce9ae4c75acdccc0d3bbe028cfbdf30d7e173dfa82e489af6ec`  
		Last Modified: Thu, 18 May 2023 21:58:08 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.17-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:36980286981e9058cd3f3a1f58fb92741d5ba73ff1a66d3b8ef7b98e23ab8377
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8313998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1348d24d9abc62396994637b0c3153212850856ce4ab5c1cc49194dd4ef4872e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:39:41 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:39:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:39:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:39:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:39:43 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:39:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8409748378eca62a6e13533d1f6fef38e6b40a7ad726dff04ad548a63ae20313`  
		Last Modified: Thu, 18 May 2023 21:40:03 GMT  
		Size: 5.0 MB (4970150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a822f2037d3c235b73c5f9924d54c4de71f06b2ba22757fc2a059c4f33d5c6`  
		Last Modified: Thu, 18 May 2023 21:40:02 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94f121392ee621f9e3f1aaa44685e70de92e169d23c2c547ba2d5172904b49d`  
		Last Modified: Thu, 18 May 2023 21:40:02 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.17-linux`

```console
$ docker pull nats@sha256:8371b3bfc468a2294efb247531c2252c592398a98b574c2e81268d8c7f865d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.17-linux` - linux; amd64

```console
$ docker pull nats@sha256:d7a57514cf7a0949ab8e63985f040f1fbaa01aa70aa50d8485f796a9a8dead08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd1a8b681814e86af7f1b07aa7178abd74163b5101ad1f855420c25d4afae5e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:19:59 GMT
COPY file:a3e4cfa40e3f87cbc1a2427fe9e77a182eed251b7a2f3037b894ac919acda56d in /nats-server 
# Thu, 18 May 2023 21:19:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:19:59 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:19:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:19:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e7f86c5b152db9b1815749cb2d298d36014c2905070ae66128b67029b4b31780`  
		Last Modified: Thu, 18 May 2023 21:20:38 GMT  
		Size: 5.1 MB (5116621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ce2c40f365197112db5bf1e3ed9b09b631da2058b456f99a50a5890fdda44`  
		Last Modified: Thu, 18 May 2023 21:20:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.17-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:b93fec72f4aff1d673fd6ead1e244e694e4919368e246cc29e0d7d120e59ed77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4881364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab660f64e3aad0f8f74d3a08909fe9013543eb07b61a9f8c6862b5db7d457d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:49:31 GMT
COPY file:6e54deb4ba87d6bff1f230123320fc7c9eee49d9a7456888efc872a22b9bd9ba in /nats-server 
# Thu, 18 May 2023 21:49:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:49:32 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:49:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41da3c5a1624a52c52a67beaa7b94c8c85a26f53b81e82e6dc05ae661adfebc1`  
		Last Modified: Thu, 18 May 2023 21:50:09 GMT  
		Size: 4.9 MB (4880856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df51ab38f5ab934d23f3b5429532106ef6baa2f64572f07ce9e5718e3f27374b`  
		Last Modified: Thu, 18 May 2023 21:50:08 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.17-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:94bf4a62f52fd647adb621d2d584e9c48aea06b124fb81cd59afed50252071bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4874864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8b8de1397d0af96648a1d02610dc54a066633c75eb548fc6be7e0d15497c3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:57:50 GMT
COPY file:31e26234e2abf1c16cd5869033f07320118e6dc458af341f37a27a3d12ffbc65 in /nats-server 
# Thu, 18 May 2023 21:57:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b6209c6f59228d4816baef6c05a38f68693937e6c86969581c57a1c7b68ccb40`  
		Last Modified: Thu, 18 May 2023 21:58:28 GMT  
		Size: 4.9 MB (4874355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69c5a4696da201d78c2dae749a6bce01c3a924afbdfa7e87c6797b8db238d4d`  
		Last Modified: Thu, 18 May 2023 21:58:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.17-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c4a7f923864c688cb5cc324df620960febd829b8d1f7074e4af3805caf5d5ceb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4685324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c4d84878abd37db0a2ba71386d26a2aaea2e989b4c3fc5f5930194da2e95c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:39:47 GMT
COPY file:b639df8cca07607378826468450a651a2cab9fb1be759ac266bf356bbfa2ac8c in /nats-server 
# Thu, 18 May 2023 21:39:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:39:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:39:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:39:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8e3bc385de2fea9fcd87e3f5b9809c6c133578671c906d0c1df657657c34664`  
		Last Modified: Thu, 18 May 2023 21:40:23 GMT  
		Size: 4.7 MB (4684816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d538df43ba01d77f25e465d3cce0829b2fbcf2a5ff131e1a42fda47b5c6c64`  
		Last Modified: Thu, 18 May 2023 21:40:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.17-nanoserver`

```console
$ docker pull nats@sha256:d69e0d7dcf49ef2b8018b6dc2e7a751e91f3908ea7a3dab55fda01cda28b6a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2.9.17-nanoserver` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:992902adab2316f4e0f1a0e7edbddad09cb2659bb7e26ed498ef39ebc86b5e20
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109563244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38a2aebef90db7b99751a2c93b984e1f7ca5acabedc0f61f40e08a00a740585`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:18:08 GMT
RUN cmd /S /C #(nop) COPY file:af4b677614d535ef3af8025256146a8f3389c5c6a4397c848e25544ea858eace in C:\nats-server.exe 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b004c7f9a3834a96e986a89e27e23aa329db101d8f291c2b5a3cdc913a1c57de`  
		Last Modified: Thu, 18 May 2023 22:18:56 GMT  
		Size: 5.2 MB (5172869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3456f5dbcfcadd4157124d47dec0661e9812e4db874cb74cb8e95be4c4ff246`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663f7b2aab72f936cdb391d59c87f99e0154634854724380b4f54daf05d300cc`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12ae8aa52c42d91abbe9fd8cd449efbcb465ac7b718d50e0589caa7436aebee`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f224e7b1c5810b30e107368e877ea6b7ca699eb4bcc4b27003aae49658d6f25`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.17-nanoserver-1809`

```console
$ docker pull nats@sha256:d69e0d7dcf49ef2b8018b6dc2e7a751e91f3908ea7a3dab55fda01cda28b6a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2.9.17-nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:992902adab2316f4e0f1a0e7edbddad09cb2659bb7e26ed498ef39ebc86b5e20
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109563244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38a2aebef90db7b99751a2c93b984e1f7ca5acabedc0f61f40e08a00a740585`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:18:08 GMT
RUN cmd /S /C #(nop) COPY file:af4b677614d535ef3af8025256146a8f3389c5c6a4397c848e25544ea858eace in C:\nats-server.exe 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b004c7f9a3834a96e986a89e27e23aa329db101d8f291c2b5a3cdc913a1c57de`  
		Last Modified: Thu, 18 May 2023 22:18:56 GMT  
		Size: 5.2 MB (5172869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3456f5dbcfcadd4157124d47dec0661e9812e4db874cb74cb8e95be4c4ff246`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663f7b2aab72f936cdb391d59c87f99e0154634854724380b4f54daf05d300cc`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12ae8aa52c42d91abbe9fd8cd449efbcb465ac7b718d50e0589caa7436aebee`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f224e7b1c5810b30e107368e877ea6b7ca699eb4bcc4b27003aae49658d6f25`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.17-scratch`

```console
$ docker pull nats@sha256:8371b3bfc468a2294efb247531c2252c592398a98b574c2e81268d8c7f865d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.17-scratch` - linux; amd64

```console
$ docker pull nats@sha256:d7a57514cf7a0949ab8e63985f040f1fbaa01aa70aa50d8485f796a9a8dead08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd1a8b681814e86af7f1b07aa7178abd74163b5101ad1f855420c25d4afae5e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:19:59 GMT
COPY file:a3e4cfa40e3f87cbc1a2427fe9e77a182eed251b7a2f3037b894ac919acda56d in /nats-server 
# Thu, 18 May 2023 21:19:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:19:59 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:19:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:19:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e7f86c5b152db9b1815749cb2d298d36014c2905070ae66128b67029b4b31780`  
		Last Modified: Thu, 18 May 2023 21:20:38 GMT  
		Size: 5.1 MB (5116621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ce2c40f365197112db5bf1e3ed9b09b631da2058b456f99a50a5890fdda44`  
		Last Modified: Thu, 18 May 2023 21:20:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.17-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b93fec72f4aff1d673fd6ead1e244e694e4919368e246cc29e0d7d120e59ed77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4881364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab660f64e3aad0f8f74d3a08909fe9013543eb07b61a9f8c6862b5db7d457d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:49:31 GMT
COPY file:6e54deb4ba87d6bff1f230123320fc7c9eee49d9a7456888efc872a22b9bd9ba in /nats-server 
# Thu, 18 May 2023 21:49:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:49:32 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:49:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41da3c5a1624a52c52a67beaa7b94c8c85a26f53b81e82e6dc05ae661adfebc1`  
		Last Modified: Thu, 18 May 2023 21:50:09 GMT  
		Size: 4.9 MB (4880856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df51ab38f5ab934d23f3b5429532106ef6baa2f64572f07ce9e5718e3f27374b`  
		Last Modified: Thu, 18 May 2023 21:50:08 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.17-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:94bf4a62f52fd647adb621d2d584e9c48aea06b124fb81cd59afed50252071bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4874864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8b8de1397d0af96648a1d02610dc54a066633c75eb548fc6be7e0d15497c3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:57:50 GMT
COPY file:31e26234e2abf1c16cd5869033f07320118e6dc458af341f37a27a3d12ffbc65 in /nats-server 
# Thu, 18 May 2023 21:57:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b6209c6f59228d4816baef6c05a38f68693937e6c86969581c57a1c7b68ccb40`  
		Last Modified: Thu, 18 May 2023 21:58:28 GMT  
		Size: 4.9 MB (4874355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69c5a4696da201d78c2dae749a6bce01c3a924afbdfa7e87c6797b8db238d4d`  
		Last Modified: Thu, 18 May 2023 21:58:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.17-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c4a7f923864c688cb5cc324df620960febd829b8d1f7074e4af3805caf5d5ceb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4685324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c4d84878abd37db0a2ba71386d26a2aaea2e989b4c3fc5f5930194da2e95c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:39:47 GMT
COPY file:b639df8cca07607378826468450a651a2cab9fb1be759ac266bf356bbfa2ac8c in /nats-server 
# Thu, 18 May 2023 21:39:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:39:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:39:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:39:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8e3bc385de2fea9fcd87e3f5b9809c6c133578671c906d0c1df657657c34664`  
		Last Modified: Thu, 18 May 2023 21:40:23 GMT  
		Size: 4.7 MB (4684816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d538df43ba01d77f25e465d3cce0829b2fbcf2a5ff131e1a42fda47b5c6c64`  
		Last Modified: Thu, 18 May 2023 21:40:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.17-windowsservercore`

```console
$ docker pull nats@sha256:b66bd38321dbc1f4988181be5367eac0ddbcba3dd178ce291a1a01bc7ea11ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2.9.17-windowsservercore` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:7806ba994a1a25a836b54b8653c5e46d2a0237e0584f8f0e5d7bcf507a0102f0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077968206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d965773e9d5a5ab8056ef67b4ea971e23a0a74f14c81cf73f1676388001a7a61`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 01:56:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 May 2023 02:40:26 GMT
ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:15:10 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 22:15:10 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.17/nats-server-v2.9.17-windows-amd64.zip
# Thu, 18 May 2023 22:15:11 GMT
ENV NATS_SERVER_SHASUM=5648a1feb86600d6634fdc405a3b08b77ac8ee7695248c10587e9809a07baae8
# Thu, 18 May 2023 22:16:10 GMT
RUN Set-PSDebug -Trace 2
# Thu, 18 May 2023 22:17:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 18 May 2023 22:17:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:17:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:17:48 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:17:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a89be60a77cd8d520ec5f03d703ddbc15675dd1df4d95e041032cf08960af5`  
		Last Modified: Wed, 10 May 2023 02:23:36 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446cee93ab2781cfc08e135a3a7ab166e5342ee6817c34fb47e0662c085bbc29`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16b2ca8cf0615f148ab3c039e2da3946c641b998fa5342e0a86b86ef80497d5`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68aa5081f892e224d628f283c6eed1d4e424761f2ae3063fedacbc566aa10c75`  
		Last Modified: Thu, 18 May 2023 22:18:41 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e024e49e7a422a94a25d1d9af6e592192c04eb7c608b17ff1af3e93529c8a35e`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b22f5baa9cb4548ac8e10267dd54d7033e3ab44ad6a770205dc734933edfbdb`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 451.2 KB (451175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956556c3c6e7691c7107a0b6dcf1c63af3f8eb15efde6c70830a2e163cbbc171`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 5.5 MB (5468496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9da5547ee8802f531d1653edb8624b8b7f62423c2b007a3f28b211233fb598a`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f66377b577951e073ab005cd4b038ad3d581aed123c6e23df40968cae80056`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0008781bdc119b24b9cc4edb26bca6a3b72efae4f6931c96f2dff965fc1ccf`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b2a25b19d19214628ae2dff527abe8becb02247e0838187f5e2d679d87bffb`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.17-windowsservercore-1809`

```console
$ docker pull nats@sha256:b66bd38321dbc1f4988181be5367eac0ddbcba3dd178ce291a1a01bc7ea11ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2.9.17-windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:7806ba994a1a25a836b54b8653c5e46d2a0237e0584f8f0e5d7bcf507a0102f0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077968206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d965773e9d5a5ab8056ef67b4ea971e23a0a74f14c81cf73f1676388001a7a61`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 01:56:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 May 2023 02:40:26 GMT
ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:15:10 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 22:15:10 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.17/nats-server-v2.9.17-windows-amd64.zip
# Thu, 18 May 2023 22:15:11 GMT
ENV NATS_SERVER_SHASUM=5648a1feb86600d6634fdc405a3b08b77ac8ee7695248c10587e9809a07baae8
# Thu, 18 May 2023 22:16:10 GMT
RUN Set-PSDebug -Trace 2
# Thu, 18 May 2023 22:17:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 18 May 2023 22:17:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:17:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:17:48 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:17:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a89be60a77cd8d520ec5f03d703ddbc15675dd1df4d95e041032cf08960af5`  
		Last Modified: Wed, 10 May 2023 02:23:36 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446cee93ab2781cfc08e135a3a7ab166e5342ee6817c34fb47e0662c085bbc29`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16b2ca8cf0615f148ab3c039e2da3946c641b998fa5342e0a86b86ef80497d5`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68aa5081f892e224d628f283c6eed1d4e424761f2ae3063fedacbc566aa10c75`  
		Last Modified: Thu, 18 May 2023 22:18:41 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e024e49e7a422a94a25d1d9af6e592192c04eb7c608b17ff1af3e93529c8a35e`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b22f5baa9cb4548ac8e10267dd54d7033e3ab44ad6a770205dc734933edfbdb`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 451.2 KB (451175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956556c3c6e7691c7107a0b6dcf1c63af3f8eb15efde6c70830a2e163cbbc171`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 5.5 MB (5468496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9da5547ee8802f531d1653edb8624b8b7f62423c2b007a3f28b211233fb598a`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f66377b577951e073ab005cd4b038ad3d581aed123c6e23df40968cae80056`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0008781bdc119b24b9cc4edb26bca6a3b72efae4f6931c96f2dff965fc1ccf`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b2a25b19d19214628ae2dff527abe8becb02247e0838187f5e2d679d87bffb`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:1a7b320b294218d11b48ddcd1552a18a74ae8790c80ba5372726c58d0a5ee295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:7544f1dfe4b270789a68e2056135467d525da411f331f43640150b0642dee693
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8802768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ada7bbdb360a5406551ced3593bc48e57c6cea5ee5d502e1a0df2437156d06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:19:49 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:19:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:19:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:19:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:19:52 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:19:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba69a821f226517d8763fd5007b51eeb8a68e40f7fb32dec75e13297ea1cb49`  
		Last Modified: Thu, 18 May 2023 21:20:19 GMT  
		Size: 5.4 MB (5404276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ad2f9c9076c4ccedf3a056bf6e996a658fa5ece8cc35913e4728d58617e8b3`  
		Last Modified: Thu, 18 May 2023 21:20:18 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb3c123b7bd114e7897ddf602c16bcd18f034abda3ee53d91a108b71c624faa`  
		Last Modified: Thu, 18 May 2023 21:20:18 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:08b7d50259bf79d1f0cc5476da2707cbe3723f8b25ececd27b4e20f5c3ba036e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8325871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676517e73baa5d6c0a13a665dcf0412659d93274c96643829ff67835d5e4905d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:04 GMT
ADD file:f87a991e2e9f185fd4a88569d86a9b8e5bc07182e7fa613b95acab25986f2a6c in / 
# Tue, 09 May 2023 23:11:04 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:49:22 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:49:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:49:24 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:49:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:015ee8d9fb3dca1b18815f1e4ee0d325d1f40cde6f2df4dd307918f7b69167d7`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.2 MB (3155679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06976c3bb336d8c3936e2bbb8d27dbd5b805054e1064aaf7c651d6fd5523aa71`  
		Last Modified: Thu, 18 May 2023 21:49:48 GMT  
		Size: 5.2 MB (5169192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c85a9f3b4246d93c82583c9d4336cb58688e4b311be41f752bc0c9456a2135`  
		Last Modified: Thu, 18 May 2023 21:49:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6d307fb0f80f02bb15dbdbb0eba31d3a463afa38dca28f6cd0e913798ebf62`  
		Last Modified: Thu, 18 May 2023 21:49:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:882066add3894dc13cfadaeec8af9f9fce5b9c3fee92e377a13f0997a88a121f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8071388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574536f22d8de67b2c2f0962d9e7d108bb4b41d07cb13a05ebab5e3b82fe6d63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 22:57:32 GMT
ADD file:eb6b6a885e8ac9bccbf44a5c673b8542c8144bba927376688240446c2f413b10 in / 
# Tue, 09 May 2023 22:57:32 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:57:27 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:57:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:57:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:57:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:57:29 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:57:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e14425cf8fb9304b9ad4a9d1250e0d4c22e507a334ff747fa69b804500afc113`  
		Last Modified: Tue, 09 May 2023 22:57:50 GMT  
		Size: 2.9 MB (2911117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213de106e11b3e7261faf48da426167af8702e8a56ab0237f786ba0eb864a38d`  
		Last Modified: Thu, 18 May 2023 21:58:08 GMT  
		Size: 5.2 MB (5159272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5535f74851ba24bbb57849b9f7085eb8441d584ea938b19bdd027f5ccf52a193`  
		Last Modified: Thu, 18 May 2023 21:58:07 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2518eda2d1b2ce9ae4c75acdccc0d3bbe028cfbdf30d7e173dfa82e489af6ec`  
		Last Modified: Thu, 18 May 2023 21:58:08 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:36980286981e9058cd3f3a1f58fb92741d5ba73ff1a66d3b8ef7b98e23ab8377
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8313998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1348d24d9abc62396994637b0c3153212850856ce4ab5c1cc49194dd4ef4872e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:39:41 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:39:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:39:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:39:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:39:43 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:39:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8409748378eca62a6e13533d1f6fef38e6b40a7ad726dff04ad548a63ae20313`  
		Last Modified: Thu, 18 May 2023 21:40:03 GMT  
		Size: 5.0 MB (4970150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a822f2037d3c235b73c5f9924d54c4de71f06b2ba22757fc2a059c4f33d5c6`  
		Last Modified: Thu, 18 May 2023 21:40:02 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94f121392ee621f9e3f1aaa44685e70de92e169d23c2c547ba2d5172904b49d`  
		Last Modified: Thu, 18 May 2023 21:40:02 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.18`

```console
$ docker pull nats@sha256:1a7b320b294218d11b48ddcd1552a18a74ae8790c80ba5372726c58d0a5ee295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:7544f1dfe4b270789a68e2056135467d525da411f331f43640150b0642dee693
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8802768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ada7bbdb360a5406551ced3593bc48e57c6cea5ee5d502e1a0df2437156d06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:19:49 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:19:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:19:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:19:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:19:52 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:19:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba69a821f226517d8763fd5007b51eeb8a68e40f7fb32dec75e13297ea1cb49`  
		Last Modified: Thu, 18 May 2023 21:20:19 GMT  
		Size: 5.4 MB (5404276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ad2f9c9076c4ccedf3a056bf6e996a658fa5ece8cc35913e4728d58617e8b3`  
		Last Modified: Thu, 18 May 2023 21:20:18 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb3c123b7bd114e7897ddf602c16bcd18f034abda3ee53d91a108b71c624faa`  
		Last Modified: Thu, 18 May 2023 21:20:18 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:08b7d50259bf79d1f0cc5476da2707cbe3723f8b25ececd27b4e20f5c3ba036e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8325871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676517e73baa5d6c0a13a665dcf0412659d93274c96643829ff67835d5e4905d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:04 GMT
ADD file:f87a991e2e9f185fd4a88569d86a9b8e5bc07182e7fa613b95acab25986f2a6c in / 
# Tue, 09 May 2023 23:11:04 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:49:22 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:49:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:49:24 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:49:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:015ee8d9fb3dca1b18815f1e4ee0d325d1f40cde6f2df4dd307918f7b69167d7`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.2 MB (3155679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06976c3bb336d8c3936e2bbb8d27dbd5b805054e1064aaf7c651d6fd5523aa71`  
		Last Modified: Thu, 18 May 2023 21:49:48 GMT  
		Size: 5.2 MB (5169192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c85a9f3b4246d93c82583c9d4336cb58688e4b311be41f752bc0c9456a2135`  
		Last Modified: Thu, 18 May 2023 21:49:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6d307fb0f80f02bb15dbdbb0eba31d3a463afa38dca28f6cd0e913798ebf62`  
		Last Modified: Thu, 18 May 2023 21:49:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:882066add3894dc13cfadaeec8af9f9fce5b9c3fee92e377a13f0997a88a121f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8071388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574536f22d8de67b2c2f0962d9e7d108bb4b41d07cb13a05ebab5e3b82fe6d63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 22:57:32 GMT
ADD file:eb6b6a885e8ac9bccbf44a5c673b8542c8144bba927376688240446c2f413b10 in / 
# Tue, 09 May 2023 22:57:32 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:57:27 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:57:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:57:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:57:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:57:29 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:57:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e14425cf8fb9304b9ad4a9d1250e0d4c22e507a334ff747fa69b804500afc113`  
		Last Modified: Tue, 09 May 2023 22:57:50 GMT  
		Size: 2.9 MB (2911117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213de106e11b3e7261faf48da426167af8702e8a56ab0237f786ba0eb864a38d`  
		Last Modified: Thu, 18 May 2023 21:58:08 GMT  
		Size: 5.2 MB (5159272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5535f74851ba24bbb57849b9f7085eb8441d584ea938b19bdd027f5ccf52a193`  
		Last Modified: Thu, 18 May 2023 21:58:07 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2518eda2d1b2ce9ae4c75acdccc0d3bbe028cfbdf30d7e173dfa82e489af6ec`  
		Last Modified: Thu, 18 May 2023 21:58:08 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:36980286981e9058cd3f3a1f58fb92741d5ba73ff1a66d3b8ef7b98e23ab8377
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8313998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1348d24d9abc62396994637b0c3153212850856ce4ab5c1cc49194dd4ef4872e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:39:41 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:39:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:39:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:39:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:39:43 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:39:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8409748378eca62a6e13533d1f6fef38e6b40a7ad726dff04ad548a63ae20313`  
		Last Modified: Thu, 18 May 2023 21:40:03 GMT  
		Size: 5.0 MB (4970150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a822f2037d3c235b73c5f9924d54c4de71f06b2ba22757fc2a059c4f33d5c6`  
		Last Modified: Thu, 18 May 2023 21:40:02 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94f121392ee621f9e3f1aaa44685e70de92e169d23c2c547ba2d5172904b49d`  
		Last Modified: Thu, 18 May 2023 21:40:02 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:c366591c44da44fe1180ca3aaee4f18b959d2d8ab5170c5ebec98eda2d0cb390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4377; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:d7a57514cf7a0949ab8e63985f040f1fbaa01aa70aa50d8485f796a9a8dead08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd1a8b681814e86af7f1b07aa7178abd74163b5101ad1f855420c25d4afae5e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:19:59 GMT
COPY file:a3e4cfa40e3f87cbc1a2427fe9e77a182eed251b7a2f3037b894ac919acda56d in /nats-server 
# Thu, 18 May 2023 21:19:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:19:59 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:19:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:19:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e7f86c5b152db9b1815749cb2d298d36014c2905070ae66128b67029b4b31780`  
		Last Modified: Thu, 18 May 2023 21:20:38 GMT  
		Size: 5.1 MB (5116621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ce2c40f365197112db5bf1e3ed9b09b631da2058b456f99a50a5890fdda44`  
		Last Modified: Thu, 18 May 2023 21:20:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:b93fec72f4aff1d673fd6ead1e244e694e4919368e246cc29e0d7d120e59ed77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4881364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab660f64e3aad0f8f74d3a08909fe9013543eb07b61a9f8c6862b5db7d457d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:49:31 GMT
COPY file:6e54deb4ba87d6bff1f230123320fc7c9eee49d9a7456888efc872a22b9bd9ba in /nats-server 
# Thu, 18 May 2023 21:49:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:49:32 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:49:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41da3c5a1624a52c52a67beaa7b94c8c85a26f53b81e82e6dc05ae661adfebc1`  
		Last Modified: Thu, 18 May 2023 21:50:09 GMT  
		Size: 4.9 MB (4880856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df51ab38f5ab934d23f3b5429532106ef6baa2f64572f07ce9e5718e3f27374b`  
		Last Modified: Thu, 18 May 2023 21:50:08 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:94bf4a62f52fd647adb621d2d584e9c48aea06b124fb81cd59afed50252071bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4874864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8b8de1397d0af96648a1d02610dc54a066633c75eb548fc6be7e0d15497c3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:57:50 GMT
COPY file:31e26234e2abf1c16cd5869033f07320118e6dc458af341f37a27a3d12ffbc65 in /nats-server 
# Thu, 18 May 2023 21:57:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b6209c6f59228d4816baef6c05a38f68693937e6c86969581c57a1c7b68ccb40`  
		Last Modified: Thu, 18 May 2023 21:58:28 GMT  
		Size: 4.9 MB (4874355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69c5a4696da201d78c2dae749a6bce01c3a924afbdfa7e87c6797b8db238d4d`  
		Last Modified: Thu, 18 May 2023 21:58:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c4a7f923864c688cb5cc324df620960febd829b8d1f7074e4af3805caf5d5ceb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4685324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c4d84878abd37db0a2ba71386d26a2aaea2e989b4c3fc5f5930194da2e95c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:39:47 GMT
COPY file:b639df8cca07607378826468450a651a2cab9fb1be759ac266bf356bbfa2ac8c in /nats-server 
# Thu, 18 May 2023 21:39:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:39:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:39:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:39:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8e3bc385de2fea9fcd87e3f5b9809c6c133578671c906d0c1df657657c34664`  
		Last Modified: Thu, 18 May 2023 21:40:23 GMT  
		Size: 4.7 MB (4684816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d538df43ba01d77f25e465d3cce0829b2fbcf2a5ff131e1a42fda47b5c6c64`  
		Last Modified: Thu, 18 May 2023 21:40:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:992902adab2316f4e0f1a0e7edbddad09cb2659bb7e26ed498ef39ebc86b5e20
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109563244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38a2aebef90db7b99751a2c93b984e1f7ca5acabedc0f61f40e08a00a740585`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:18:08 GMT
RUN cmd /S /C #(nop) COPY file:af4b677614d535ef3af8025256146a8f3389c5c6a4397c848e25544ea858eace in C:\nats-server.exe 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b004c7f9a3834a96e986a89e27e23aa329db101d8f291c2b5a3cdc913a1c57de`  
		Last Modified: Thu, 18 May 2023 22:18:56 GMT  
		Size: 5.2 MB (5172869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3456f5dbcfcadd4157124d47dec0661e9812e4db874cb74cb8e95be4c4ff246`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663f7b2aab72f936cdb391d59c87f99e0154634854724380b4f54daf05d300cc`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12ae8aa52c42d91abbe9fd8cd449efbcb465ac7b718d50e0589caa7436aebee`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f224e7b1c5810b30e107368e877ea6b7ca699eb4bcc4b27003aae49658d6f25`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:8371b3bfc468a2294efb247531c2252c592398a98b574c2e81268d8c7f865d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:d7a57514cf7a0949ab8e63985f040f1fbaa01aa70aa50d8485f796a9a8dead08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd1a8b681814e86af7f1b07aa7178abd74163b5101ad1f855420c25d4afae5e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:19:59 GMT
COPY file:a3e4cfa40e3f87cbc1a2427fe9e77a182eed251b7a2f3037b894ac919acda56d in /nats-server 
# Thu, 18 May 2023 21:19:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:19:59 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:19:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:19:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e7f86c5b152db9b1815749cb2d298d36014c2905070ae66128b67029b4b31780`  
		Last Modified: Thu, 18 May 2023 21:20:38 GMT  
		Size: 5.1 MB (5116621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ce2c40f365197112db5bf1e3ed9b09b631da2058b456f99a50a5890fdda44`  
		Last Modified: Thu, 18 May 2023 21:20:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:b93fec72f4aff1d673fd6ead1e244e694e4919368e246cc29e0d7d120e59ed77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4881364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab660f64e3aad0f8f74d3a08909fe9013543eb07b61a9f8c6862b5db7d457d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:49:31 GMT
COPY file:6e54deb4ba87d6bff1f230123320fc7c9eee49d9a7456888efc872a22b9bd9ba in /nats-server 
# Thu, 18 May 2023 21:49:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:49:32 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:49:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41da3c5a1624a52c52a67beaa7b94c8c85a26f53b81e82e6dc05ae661adfebc1`  
		Last Modified: Thu, 18 May 2023 21:50:09 GMT  
		Size: 4.9 MB (4880856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df51ab38f5ab934d23f3b5429532106ef6baa2f64572f07ce9e5718e3f27374b`  
		Last Modified: Thu, 18 May 2023 21:50:08 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:94bf4a62f52fd647adb621d2d584e9c48aea06b124fb81cd59afed50252071bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4874864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8b8de1397d0af96648a1d02610dc54a066633c75eb548fc6be7e0d15497c3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:57:50 GMT
COPY file:31e26234e2abf1c16cd5869033f07320118e6dc458af341f37a27a3d12ffbc65 in /nats-server 
# Thu, 18 May 2023 21:57:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b6209c6f59228d4816baef6c05a38f68693937e6c86969581c57a1c7b68ccb40`  
		Last Modified: Thu, 18 May 2023 21:58:28 GMT  
		Size: 4.9 MB (4874355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69c5a4696da201d78c2dae749a6bce01c3a924afbdfa7e87c6797b8db238d4d`  
		Last Modified: Thu, 18 May 2023 21:58:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c4a7f923864c688cb5cc324df620960febd829b8d1f7074e4af3805caf5d5ceb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4685324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c4d84878abd37db0a2ba71386d26a2aaea2e989b4c3fc5f5930194da2e95c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:39:47 GMT
COPY file:b639df8cca07607378826468450a651a2cab9fb1be759ac266bf356bbfa2ac8c in /nats-server 
# Thu, 18 May 2023 21:39:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:39:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:39:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:39:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8e3bc385de2fea9fcd87e3f5b9809c6c133578671c906d0c1df657657c34664`  
		Last Modified: Thu, 18 May 2023 21:40:23 GMT  
		Size: 4.7 MB (4684816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d538df43ba01d77f25e465d3cce0829b2fbcf2a5ff131e1a42fda47b5c6c64`  
		Last Modified: Thu, 18 May 2023 21:40:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:d69e0d7dcf49ef2b8018b6dc2e7a751e91f3908ea7a3dab55fda01cda28b6a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:nanoserver` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:992902adab2316f4e0f1a0e7edbddad09cb2659bb7e26ed498ef39ebc86b5e20
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109563244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38a2aebef90db7b99751a2c93b984e1f7ca5acabedc0f61f40e08a00a740585`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:18:08 GMT
RUN cmd /S /C #(nop) COPY file:af4b677614d535ef3af8025256146a8f3389c5c6a4397c848e25544ea858eace in C:\nats-server.exe 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b004c7f9a3834a96e986a89e27e23aa329db101d8f291c2b5a3cdc913a1c57de`  
		Last Modified: Thu, 18 May 2023 22:18:56 GMT  
		Size: 5.2 MB (5172869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3456f5dbcfcadd4157124d47dec0661e9812e4db874cb74cb8e95be4c4ff246`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663f7b2aab72f936cdb391d59c87f99e0154634854724380b4f54daf05d300cc`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12ae8aa52c42d91abbe9fd8cd449efbcb465ac7b718d50e0589caa7436aebee`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f224e7b1c5810b30e107368e877ea6b7ca699eb4bcc4b27003aae49658d6f25`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:d69e0d7dcf49ef2b8018b6dc2e7a751e91f3908ea7a3dab55fda01cda28b6a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:992902adab2316f4e0f1a0e7edbddad09cb2659bb7e26ed498ef39ebc86b5e20
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109563244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38a2aebef90db7b99751a2c93b984e1f7ca5acabedc0f61f40e08a00a740585`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:18:08 GMT
RUN cmd /S /C #(nop) COPY file:af4b677614d535ef3af8025256146a8f3389c5c6a4397c848e25544ea858eace in C:\nats-server.exe 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:18:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:18:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b004c7f9a3834a96e986a89e27e23aa329db101d8f291c2b5a3cdc913a1c57de`  
		Last Modified: Thu, 18 May 2023 22:18:56 GMT  
		Size: 5.2 MB (5172869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3456f5dbcfcadd4157124d47dec0661e9812e4db874cb74cb8e95be4c4ff246`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663f7b2aab72f936cdb391d59c87f99e0154634854724380b4f54daf05d300cc`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12ae8aa52c42d91abbe9fd8cd449efbcb465ac7b718d50e0589caa7436aebee`  
		Last Modified: Thu, 18 May 2023 22:18:54 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f224e7b1c5810b30e107368e877ea6b7ca699eb4bcc4b27003aae49658d6f25`  
		Last Modified: Thu, 18 May 2023 22:18:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:8371b3bfc468a2294efb247531c2252c592398a98b574c2e81268d8c7f865d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:d7a57514cf7a0949ab8e63985f040f1fbaa01aa70aa50d8485f796a9a8dead08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd1a8b681814e86af7f1b07aa7178abd74163b5101ad1f855420c25d4afae5e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:19:59 GMT
COPY file:a3e4cfa40e3f87cbc1a2427fe9e77a182eed251b7a2f3037b894ac919acda56d in /nats-server 
# Thu, 18 May 2023 21:19:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:19:59 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:19:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:19:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e7f86c5b152db9b1815749cb2d298d36014c2905070ae66128b67029b4b31780`  
		Last Modified: Thu, 18 May 2023 21:20:38 GMT  
		Size: 5.1 MB (5116621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ce2c40f365197112db5bf1e3ed9b09b631da2058b456f99a50a5890fdda44`  
		Last Modified: Thu, 18 May 2023 21:20:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b93fec72f4aff1d673fd6ead1e244e694e4919368e246cc29e0d7d120e59ed77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4881364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab660f64e3aad0f8f74d3a08909fe9013543eb07b61a9f8c6862b5db7d457d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:49:31 GMT
COPY file:6e54deb4ba87d6bff1f230123320fc7c9eee49d9a7456888efc872a22b9bd9ba in /nats-server 
# Thu, 18 May 2023 21:49:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:49:32 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:49:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41da3c5a1624a52c52a67beaa7b94c8c85a26f53b81e82e6dc05ae661adfebc1`  
		Last Modified: Thu, 18 May 2023 21:50:09 GMT  
		Size: 4.9 MB (4880856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df51ab38f5ab934d23f3b5429532106ef6baa2f64572f07ce9e5718e3f27374b`  
		Last Modified: Thu, 18 May 2023 21:50:08 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:94bf4a62f52fd647adb621d2d584e9c48aea06b124fb81cd59afed50252071bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4874864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8b8de1397d0af96648a1d02610dc54a066633c75eb548fc6be7e0d15497c3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:57:50 GMT
COPY file:31e26234e2abf1c16cd5869033f07320118e6dc458af341f37a27a3d12ffbc65 in /nats-server 
# Thu, 18 May 2023 21:57:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:57:51 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:57:51 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:57:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b6209c6f59228d4816baef6c05a38f68693937e6c86969581c57a1c7b68ccb40`  
		Last Modified: Thu, 18 May 2023 21:58:28 GMT  
		Size: 4.9 MB (4874355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69c5a4696da201d78c2dae749a6bce01c3a924afbdfa7e87c6797b8db238d4d`  
		Last Modified: Thu, 18 May 2023 21:58:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c4a7f923864c688cb5cc324df620960febd829b8d1f7074e4af3805caf5d5ceb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4685324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c4d84878abd37db0a2ba71386d26a2aaea2e989b4c3fc5f5930194da2e95c3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 18 May 2023 21:39:47 GMT
COPY file:b639df8cca07607378826468450a651a2cab9fb1be759ac266bf356bbfa2ac8c in /nats-server 
# Thu, 18 May 2023 21:39:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 18 May 2023 21:39:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 18 May 2023 21:39:48 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 18 May 2023 21:39:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8e3bc385de2fea9fcd87e3f5b9809c6c133578671c906d0c1df657657c34664`  
		Last Modified: Thu, 18 May 2023 21:40:23 GMT  
		Size: 4.7 MB (4684816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d538df43ba01d77f25e465d3cce0829b2fbcf2a5ff131e1a42fda47b5c6c64`  
		Last Modified: Thu, 18 May 2023 21:40:22 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:b66bd38321dbc1f4988181be5367eac0ddbcba3dd178ce291a1a01bc7ea11ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:windowsservercore` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:7806ba994a1a25a836b54b8653c5e46d2a0237e0584f8f0e5d7bcf507a0102f0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077968206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d965773e9d5a5ab8056ef67b4ea971e23a0a74f14c81cf73f1676388001a7a61`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 01:56:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 May 2023 02:40:26 GMT
ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:15:10 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 22:15:10 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.17/nats-server-v2.9.17-windows-amd64.zip
# Thu, 18 May 2023 22:15:11 GMT
ENV NATS_SERVER_SHASUM=5648a1feb86600d6634fdc405a3b08b77ac8ee7695248c10587e9809a07baae8
# Thu, 18 May 2023 22:16:10 GMT
RUN Set-PSDebug -Trace 2
# Thu, 18 May 2023 22:17:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 18 May 2023 22:17:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:17:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:17:48 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:17:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a89be60a77cd8d520ec5f03d703ddbc15675dd1df4d95e041032cf08960af5`  
		Last Modified: Wed, 10 May 2023 02:23:36 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446cee93ab2781cfc08e135a3a7ab166e5342ee6817c34fb47e0662c085bbc29`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16b2ca8cf0615f148ab3c039e2da3946c641b998fa5342e0a86b86ef80497d5`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68aa5081f892e224d628f283c6eed1d4e424761f2ae3063fedacbc566aa10c75`  
		Last Modified: Thu, 18 May 2023 22:18:41 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e024e49e7a422a94a25d1d9af6e592192c04eb7c608b17ff1af3e93529c8a35e`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b22f5baa9cb4548ac8e10267dd54d7033e3ab44ad6a770205dc734933edfbdb`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 451.2 KB (451175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956556c3c6e7691c7107a0b6dcf1c63af3f8eb15efde6c70830a2e163cbbc171`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 5.5 MB (5468496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9da5547ee8802f531d1653edb8624b8b7f62423c2b007a3f28b211233fb598a`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f66377b577951e073ab005cd4b038ad3d581aed123c6e23df40968cae80056`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0008781bdc119b24b9cc4edb26bca6a3b72efae4f6931c96f2dff965fc1ccf`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b2a25b19d19214628ae2dff527abe8becb02247e0838187f5e2d679d87bffb`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:b66bd38321dbc1f4988181be5367eac0ddbcba3dd178ce291a1a01bc7ea11ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:7806ba994a1a25a836b54b8653c5e46d2a0237e0584f8f0e5d7bcf507a0102f0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077968206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d965773e9d5a5ab8056ef67b4ea971e23a0a74f14c81cf73f1676388001a7a61`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 01:56:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 May 2023 02:40:26 GMT
ENV NATS_DOCKERIZED=1
# Thu, 18 May 2023 22:15:10 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 22:15:10 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.17/nats-server-v2.9.17-windows-amd64.zip
# Thu, 18 May 2023 22:15:11 GMT
ENV NATS_SERVER_SHASUM=5648a1feb86600d6634fdc405a3b08b77ac8ee7695248c10587e9809a07baae8
# Thu, 18 May 2023 22:16:10 GMT
RUN Set-PSDebug -Trace 2
# Thu, 18 May 2023 22:17:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 18 May 2023 22:17:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 18 May 2023 22:17:48 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 22:17:48 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 18 May 2023 22:17:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a89be60a77cd8d520ec5f03d703ddbc15675dd1df4d95e041032cf08960af5`  
		Last Modified: Wed, 10 May 2023 02:23:36 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446cee93ab2781cfc08e135a3a7ab166e5342ee6817c34fb47e0662c085bbc29`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16b2ca8cf0615f148ab3c039e2da3946c641b998fa5342e0a86b86ef80497d5`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68aa5081f892e224d628f283c6eed1d4e424761f2ae3063fedacbc566aa10c75`  
		Last Modified: Thu, 18 May 2023 22:18:41 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e024e49e7a422a94a25d1d9af6e592192c04eb7c608b17ff1af3e93529c8a35e`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b22f5baa9cb4548ac8e10267dd54d7033e3ab44ad6a770205dc734933edfbdb`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 451.2 KB (451175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956556c3c6e7691c7107a0b6dcf1c63af3f8eb15efde6c70830a2e163cbbc171`  
		Last Modified: Thu, 18 May 2023 22:18:40 GMT  
		Size: 5.5 MB (5468496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9da5547ee8802f531d1653edb8624b8b7f62423c2b007a3f28b211233fb598a`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f66377b577951e073ab005cd4b038ad3d581aed123c6e23df40968cae80056`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0008781bdc119b24b9cc4edb26bca6a3b72efae4f6931c96f2dff965fc1ccf`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b2a25b19d19214628ae2dff527abe8becb02247e0838187f5e2d679d87bffb`  
		Last Modified: Thu, 18 May 2023 22:18:38 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
