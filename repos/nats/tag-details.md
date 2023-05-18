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
$ docker pull nats@sha256:f6a7ae625804d5d66e403dc36d331797d47a5c2570b393a380136c03b04babb8
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
$ docker pull nats@sha256:6b63ca13550920e16ac8d1d383dc58df9d072c4c3fd4e511281d202dbe38c0bc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109468515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4679dd016bef3c8ed79c3b2d31d2c63a3476cd23995815bd0f30f6861672beef`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:43:58 GMT
RUN cmd /S /C #(nop) COPY file:097c54a43536c2c00c5d7ab4ca42531dfa5623331b43597ffed4871d2f7f7d72 in C:\nats-server.exe 
# Wed, 10 May 2023 02:43:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 May 2023 02:44:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 May 2023 02:44:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 May 2023 02:44:03 GMT
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
	-	`sha256:b1d85a51b6ad0c0fa41d8acd3c2343413b08e446c0e8285547dc0f823bc8c79f`  
		Last Modified: Wed, 10 May 2023 07:09:52 GMT  
		Size: 5.1 MB (5078084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52698a3efa93904b0f9e31143300d218ee09e1094c4750deee936722a434c9f0`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354b5f484857495c910fe4f837972933f33fd6843557455f4bdf4f353ef6128f`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c06258e4387dc50c2c887507689557c15c1676fa0c66e537b7d0dd4d052267`  
		Last Modified: Wed, 10 May 2023 07:09:51 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1975391c3359e794cc1f15388c47f08ef7f9587a8f1ba4cf78d70a6586eaafd6`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.1 KB (1141 bytes)  
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
$ docker pull nats@sha256:1507f0f2963897740a12da7508fd1bc6ebea7ebdad76eb111d235fb15a1a7f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:6b63ca13550920e16ac8d1d383dc58df9d072c4c3fd4e511281d202dbe38c0bc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109468515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4679dd016bef3c8ed79c3b2d31d2c63a3476cd23995815bd0f30f6861672beef`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:43:58 GMT
RUN cmd /S /C #(nop) COPY file:097c54a43536c2c00c5d7ab4ca42531dfa5623331b43597ffed4871d2f7f7d72 in C:\nats-server.exe 
# Wed, 10 May 2023 02:43:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 May 2023 02:44:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 May 2023 02:44:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 May 2023 02:44:03 GMT
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
	-	`sha256:b1d85a51b6ad0c0fa41d8acd3c2343413b08e446c0e8285547dc0f823bc8c79f`  
		Last Modified: Wed, 10 May 2023 07:09:52 GMT  
		Size: 5.1 MB (5078084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52698a3efa93904b0f9e31143300d218ee09e1094c4750deee936722a434c9f0`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354b5f484857495c910fe4f837972933f33fd6843557455f4bdf4f353ef6128f`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c06258e4387dc50c2c887507689557c15c1676fa0c66e537b7d0dd4d052267`  
		Last Modified: Wed, 10 May 2023 07:09:51 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1975391c3359e794cc1f15388c47f08ef7f9587a8f1ba4cf78d70a6586eaafd6`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:1507f0f2963897740a12da7508fd1bc6ebea7ebdad76eb111d235fb15a1a7f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:6b63ca13550920e16ac8d1d383dc58df9d072c4c3fd4e511281d202dbe38c0bc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109468515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4679dd016bef3c8ed79c3b2d31d2c63a3476cd23995815bd0f30f6861672beef`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:43:58 GMT
RUN cmd /S /C #(nop) COPY file:097c54a43536c2c00c5d7ab4ca42531dfa5623331b43597ffed4871d2f7f7d72 in C:\nats-server.exe 
# Wed, 10 May 2023 02:43:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 May 2023 02:44:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 May 2023 02:44:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 May 2023 02:44:03 GMT
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
	-	`sha256:b1d85a51b6ad0c0fa41d8acd3c2343413b08e446c0e8285547dc0f823bc8c79f`  
		Last Modified: Wed, 10 May 2023 07:09:52 GMT  
		Size: 5.1 MB (5078084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52698a3efa93904b0f9e31143300d218ee09e1094c4750deee936722a434c9f0`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354b5f484857495c910fe4f837972933f33fd6843557455f4bdf4f353ef6128f`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c06258e4387dc50c2c887507689557c15c1676fa0c66e537b7d0dd4d052267`  
		Last Modified: Wed, 10 May 2023 07:09:51 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1975391c3359e794cc1f15388c47f08ef7f9587a8f1ba4cf78d70a6586eaafd6`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.1 KB (1141 bytes)  
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
$ docker pull nats@sha256:f7cb4ed36f2be5c7be9a7b08d8c1b22e645f58ba4991dfa459e74577d9f4b615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:1732bbcb34375aafeac01e77ce6e7aa2dbba27278ba12958bb3aed917f0c1dc0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077822911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8bfcb2ac53edf941120e941b4913e75121f8f7849d6c69cd234724ac1354311`
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
# Wed, 10 May 2023 02:40:27 GMT
ENV NATS_SERVER=2.9.16
# Wed, 10 May 2023 02:40:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.16/nats-server-v2.9.16-windows-amd64.zip
# Wed, 10 May 2023 02:40:29 GMT
ENV NATS_SERVER_SHASUM=293013cd810f35f2a3dd25b0d850da248bc45af46b854a805383f848db3e9fa0
# Wed, 10 May 2023 02:41:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 May 2023 02:43:41 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 May 2023 02:43:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 May 2023 02:43:43 GMT
EXPOSE 4222 6222 8222
# Wed, 10 May 2023 02:43:44 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 May 2023 02:43:44 GMT
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
	-	`sha256:1de33925544fc248e0ffac22a06e9727c7ba90ba2cb7db16eeaaff706776402b`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7135feb8500e9833370ec21c3622cf7fbba7424afcac727b61e304376265d4be`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5271c6f8ccb837e1ce744ad44305a94c606b0be8b8485718313913c90315cd`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bcd42cac1942260a2fe8430628f8d0f792cc8361dd67fab848150d01b97657`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 426.3 KB (426266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a398f7862050ef8d8f732aef1986f5db3a45557b30ba2a17c22f482c023b9f`  
		Last Modified: Wed, 10 May 2023 07:09:35 GMT  
		Size: 5.3 MB (5348225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d534b19d5fbf3dd2d41d8086faca3ddedf186adbb103979e6d76101e3eec78d`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 2.0 KB (1968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fd8189adda36aa8738fc9e85d0a25701a5a0e38a451afa5af1700e7e79d67e`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78173f06e168d48cc7aa1d4654204d98d914ae854728a118131ffe8d9181a82f`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cd778f6318ee8c3823680bf429cf481faec2f6f7e714cde79309dfc917345a`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:f7cb4ed36f2be5c7be9a7b08d8c1b22e645f58ba4991dfa459e74577d9f4b615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:1732bbcb34375aafeac01e77ce6e7aa2dbba27278ba12958bb3aed917f0c1dc0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077822911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8bfcb2ac53edf941120e941b4913e75121f8f7849d6c69cd234724ac1354311`
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
# Wed, 10 May 2023 02:40:27 GMT
ENV NATS_SERVER=2.9.16
# Wed, 10 May 2023 02:40:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.16/nats-server-v2.9.16-windows-amd64.zip
# Wed, 10 May 2023 02:40:29 GMT
ENV NATS_SERVER_SHASUM=293013cd810f35f2a3dd25b0d850da248bc45af46b854a805383f848db3e9fa0
# Wed, 10 May 2023 02:41:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 May 2023 02:43:41 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 May 2023 02:43:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 May 2023 02:43:43 GMT
EXPOSE 4222 6222 8222
# Wed, 10 May 2023 02:43:44 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 May 2023 02:43:44 GMT
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
	-	`sha256:1de33925544fc248e0ffac22a06e9727c7ba90ba2cb7db16eeaaff706776402b`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7135feb8500e9833370ec21c3622cf7fbba7424afcac727b61e304376265d4be`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5271c6f8ccb837e1ce744ad44305a94c606b0be8b8485718313913c90315cd`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bcd42cac1942260a2fe8430628f8d0f792cc8361dd67fab848150d01b97657`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 426.3 KB (426266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a398f7862050ef8d8f732aef1986f5db3a45557b30ba2a17c22f482c023b9f`  
		Last Modified: Wed, 10 May 2023 07:09:35 GMT  
		Size: 5.3 MB (5348225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d534b19d5fbf3dd2d41d8086faca3ddedf186adbb103979e6d76101e3eec78d`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 2.0 KB (1968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fd8189adda36aa8738fc9e85d0a25701a5a0e38a451afa5af1700e7e79d67e`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78173f06e168d48cc7aa1d4654204d98d914ae854728a118131ffe8d9181a82f`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cd778f6318ee8c3823680bf429cf481faec2f6f7e714cde79309dfc917345a`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:f6a7ae625804d5d66e403dc36d331797d47a5c2570b393a380136c03b04babb8
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
$ docker pull nats@sha256:6b63ca13550920e16ac8d1d383dc58df9d072c4c3fd4e511281d202dbe38c0bc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109468515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4679dd016bef3c8ed79c3b2d31d2c63a3476cd23995815bd0f30f6861672beef`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:43:58 GMT
RUN cmd /S /C #(nop) COPY file:097c54a43536c2c00c5d7ab4ca42531dfa5623331b43597ffed4871d2f7f7d72 in C:\nats-server.exe 
# Wed, 10 May 2023 02:43:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 May 2023 02:44:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 May 2023 02:44:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 May 2023 02:44:03 GMT
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
	-	`sha256:b1d85a51b6ad0c0fa41d8acd3c2343413b08e446c0e8285547dc0f823bc8c79f`  
		Last Modified: Wed, 10 May 2023 07:09:52 GMT  
		Size: 5.1 MB (5078084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52698a3efa93904b0f9e31143300d218ee09e1094c4750deee936722a434c9f0`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354b5f484857495c910fe4f837972933f33fd6843557455f4bdf4f353ef6128f`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c06258e4387dc50c2c887507689557c15c1676fa0c66e537b7d0dd4d052267`  
		Last Modified: Wed, 10 May 2023 07:09:51 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1975391c3359e794cc1f15388c47f08ef7f9587a8f1ba4cf78d70a6586eaafd6`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.1 KB (1141 bytes)  
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
$ docker pull nats@sha256:1507f0f2963897740a12da7508fd1bc6ebea7ebdad76eb111d235fb15a1a7f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:6b63ca13550920e16ac8d1d383dc58df9d072c4c3fd4e511281d202dbe38c0bc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109468515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4679dd016bef3c8ed79c3b2d31d2c63a3476cd23995815bd0f30f6861672beef`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:43:58 GMT
RUN cmd /S /C #(nop) COPY file:097c54a43536c2c00c5d7ab4ca42531dfa5623331b43597ffed4871d2f7f7d72 in C:\nats-server.exe 
# Wed, 10 May 2023 02:43:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 May 2023 02:44:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 May 2023 02:44:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 May 2023 02:44:03 GMT
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
	-	`sha256:b1d85a51b6ad0c0fa41d8acd3c2343413b08e446c0e8285547dc0f823bc8c79f`  
		Last Modified: Wed, 10 May 2023 07:09:52 GMT  
		Size: 5.1 MB (5078084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52698a3efa93904b0f9e31143300d218ee09e1094c4750deee936722a434c9f0`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354b5f484857495c910fe4f837972933f33fd6843557455f4bdf4f353ef6128f`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c06258e4387dc50c2c887507689557c15c1676fa0c66e537b7d0dd4d052267`  
		Last Modified: Wed, 10 May 2023 07:09:51 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1975391c3359e794cc1f15388c47f08ef7f9587a8f1ba4cf78d70a6586eaafd6`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:1507f0f2963897740a12da7508fd1bc6ebea7ebdad76eb111d235fb15a1a7f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:6b63ca13550920e16ac8d1d383dc58df9d072c4c3fd4e511281d202dbe38c0bc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109468515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4679dd016bef3c8ed79c3b2d31d2c63a3476cd23995815bd0f30f6861672beef`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:43:58 GMT
RUN cmd /S /C #(nop) COPY file:097c54a43536c2c00c5d7ab4ca42531dfa5623331b43597ffed4871d2f7f7d72 in C:\nats-server.exe 
# Wed, 10 May 2023 02:43:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 May 2023 02:44:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 May 2023 02:44:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 May 2023 02:44:03 GMT
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
	-	`sha256:b1d85a51b6ad0c0fa41d8acd3c2343413b08e446c0e8285547dc0f823bc8c79f`  
		Last Modified: Wed, 10 May 2023 07:09:52 GMT  
		Size: 5.1 MB (5078084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52698a3efa93904b0f9e31143300d218ee09e1094c4750deee936722a434c9f0`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354b5f484857495c910fe4f837972933f33fd6843557455f4bdf4f353ef6128f`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c06258e4387dc50c2c887507689557c15c1676fa0c66e537b7d0dd4d052267`  
		Last Modified: Wed, 10 May 2023 07:09:51 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1975391c3359e794cc1f15388c47f08ef7f9587a8f1ba4cf78d70a6586eaafd6`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.1 KB (1141 bytes)  
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
$ docker pull nats@sha256:f7cb4ed36f2be5c7be9a7b08d8c1b22e645f58ba4991dfa459e74577d9f4b615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:1732bbcb34375aafeac01e77ce6e7aa2dbba27278ba12958bb3aed917f0c1dc0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077822911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8bfcb2ac53edf941120e941b4913e75121f8f7849d6c69cd234724ac1354311`
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
# Wed, 10 May 2023 02:40:27 GMT
ENV NATS_SERVER=2.9.16
# Wed, 10 May 2023 02:40:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.16/nats-server-v2.9.16-windows-amd64.zip
# Wed, 10 May 2023 02:40:29 GMT
ENV NATS_SERVER_SHASUM=293013cd810f35f2a3dd25b0d850da248bc45af46b854a805383f848db3e9fa0
# Wed, 10 May 2023 02:41:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 May 2023 02:43:41 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 May 2023 02:43:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 May 2023 02:43:43 GMT
EXPOSE 4222 6222 8222
# Wed, 10 May 2023 02:43:44 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 May 2023 02:43:44 GMT
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
	-	`sha256:1de33925544fc248e0ffac22a06e9727c7ba90ba2cb7db16eeaaff706776402b`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7135feb8500e9833370ec21c3622cf7fbba7424afcac727b61e304376265d4be`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5271c6f8ccb837e1ce744ad44305a94c606b0be8b8485718313913c90315cd`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bcd42cac1942260a2fe8430628f8d0f792cc8361dd67fab848150d01b97657`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 426.3 KB (426266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a398f7862050ef8d8f732aef1986f5db3a45557b30ba2a17c22f482c023b9f`  
		Last Modified: Wed, 10 May 2023 07:09:35 GMT  
		Size: 5.3 MB (5348225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d534b19d5fbf3dd2d41d8086faca3ddedf186adbb103979e6d76101e3eec78d`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 2.0 KB (1968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fd8189adda36aa8738fc9e85d0a25701a5a0e38a451afa5af1700e7e79d67e`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78173f06e168d48cc7aa1d4654204d98d914ae854728a118131ffe8d9181a82f`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cd778f6318ee8c3823680bf429cf481faec2f6f7e714cde79309dfc917345a`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:f7cb4ed36f2be5c7be9a7b08d8c1b22e645f58ba4991dfa459e74577d9f4b615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:1732bbcb34375aafeac01e77ce6e7aa2dbba27278ba12958bb3aed917f0c1dc0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077822911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8bfcb2ac53edf941120e941b4913e75121f8f7849d6c69cd234724ac1354311`
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
# Wed, 10 May 2023 02:40:27 GMT
ENV NATS_SERVER=2.9.16
# Wed, 10 May 2023 02:40:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.16/nats-server-v2.9.16-windows-amd64.zip
# Wed, 10 May 2023 02:40:29 GMT
ENV NATS_SERVER_SHASUM=293013cd810f35f2a3dd25b0d850da248bc45af46b854a805383f848db3e9fa0
# Wed, 10 May 2023 02:41:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 May 2023 02:43:41 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 May 2023 02:43:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 May 2023 02:43:43 GMT
EXPOSE 4222 6222 8222
# Wed, 10 May 2023 02:43:44 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 May 2023 02:43:44 GMT
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
	-	`sha256:1de33925544fc248e0ffac22a06e9727c7ba90ba2cb7db16eeaaff706776402b`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7135feb8500e9833370ec21c3622cf7fbba7424afcac727b61e304376265d4be`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5271c6f8ccb837e1ce744ad44305a94c606b0be8b8485718313913c90315cd`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bcd42cac1942260a2fe8430628f8d0f792cc8361dd67fab848150d01b97657`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 426.3 KB (426266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a398f7862050ef8d8f732aef1986f5db3a45557b30ba2a17c22f482c023b9f`  
		Last Modified: Wed, 10 May 2023 07:09:35 GMT  
		Size: 5.3 MB (5348225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d534b19d5fbf3dd2d41d8086faca3ddedf186adbb103979e6d76101e3eec78d`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 2.0 KB (1968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fd8189adda36aa8738fc9e85d0a25701a5a0e38a451afa5af1700e7e79d67e`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78173f06e168d48cc7aa1d4654204d98d914ae854728a118131ffe8d9181a82f`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cd778f6318ee8c3823680bf429cf481faec2f6f7e714cde79309dfc917345a`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.17`

```console
$ docker pull nats@sha256:8371b3bfc468a2294efb247531c2252c592398a98b574c2e81268d8c7f865d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

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
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.9.17-nanoserver-1809`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

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
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.9.17-windowsservercore-1809`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

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
$ docker pull nats@sha256:f6a7ae625804d5d66e403dc36d331797d47a5c2570b393a380136c03b04babb8
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
$ docker pull nats@sha256:6b63ca13550920e16ac8d1d383dc58df9d072c4c3fd4e511281d202dbe38c0bc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109468515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4679dd016bef3c8ed79c3b2d31d2c63a3476cd23995815bd0f30f6861672beef`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:43:58 GMT
RUN cmd /S /C #(nop) COPY file:097c54a43536c2c00c5d7ab4ca42531dfa5623331b43597ffed4871d2f7f7d72 in C:\nats-server.exe 
# Wed, 10 May 2023 02:43:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 May 2023 02:44:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 May 2023 02:44:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 May 2023 02:44:03 GMT
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
	-	`sha256:b1d85a51b6ad0c0fa41d8acd3c2343413b08e446c0e8285547dc0f823bc8c79f`  
		Last Modified: Wed, 10 May 2023 07:09:52 GMT  
		Size: 5.1 MB (5078084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52698a3efa93904b0f9e31143300d218ee09e1094c4750deee936722a434c9f0`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354b5f484857495c910fe4f837972933f33fd6843557455f4bdf4f353ef6128f`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c06258e4387dc50c2c887507689557c15c1676fa0c66e537b7d0dd4d052267`  
		Last Modified: Wed, 10 May 2023 07:09:51 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1975391c3359e794cc1f15388c47f08ef7f9587a8f1ba4cf78d70a6586eaafd6`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.1 KB (1141 bytes)  
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
$ docker pull nats@sha256:1507f0f2963897740a12da7508fd1bc6ebea7ebdad76eb111d235fb15a1a7f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:nanoserver` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:6b63ca13550920e16ac8d1d383dc58df9d072c4c3fd4e511281d202dbe38c0bc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109468515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4679dd016bef3c8ed79c3b2d31d2c63a3476cd23995815bd0f30f6861672beef`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:43:58 GMT
RUN cmd /S /C #(nop) COPY file:097c54a43536c2c00c5d7ab4ca42531dfa5623331b43597ffed4871d2f7f7d72 in C:\nats-server.exe 
# Wed, 10 May 2023 02:43:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 May 2023 02:44:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 May 2023 02:44:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 May 2023 02:44:03 GMT
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
	-	`sha256:b1d85a51b6ad0c0fa41d8acd3c2343413b08e446c0e8285547dc0f823bc8c79f`  
		Last Modified: Wed, 10 May 2023 07:09:52 GMT  
		Size: 5.1 MB (5078084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52698a3efa93904b0f9e31143300d218ee09e1094c4750deee936722a434c9f0`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354b5f484857495c910fe4f837972933f33fd6843557455f4bdf4f353ef6128f`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c06258e4387dc50c2c887507689557c15c1676fa0c66e537b7d0dd4d052267`  
		Last Modified: Wed, 10 May 2023 07:09:51 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1975391c3359e794cc1f15388c47f08ef7f9587a8f1ba4cf78d70a6586eaafd6`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:1507f0f2963897740a12da7508fd1bc6ebea7ebdad76eb111d235fb15a1a7f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:6b63ca13550920e16ac8d1d383dc58df9d072c4c3fd4e511281d202dbe38c0bc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109468515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4679dd016bef3c8ed79c3b2d31d2c63a3476cd23995815bd0f30f6861672beef`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:43:58 GMT
RUN cmd /S /C #(nop) COPY file:097c54a43536c2c00c5d7ab4ca42531dfa5623331b43597ffed4871d2f7f7d72 in C:\nats-server.exe 
# Wed, 10 May 2023 02:43:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 May 2023 02:44:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 May 2023 02:44:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 May 2023 02:44:03 GMT
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
	-	`sha256:b1d85a51b6ad0c0fa41d8acd3c2343413b08e446c0e8285547dc0f823bc8c79f`  
		Last Modified: Wed, 10 May 2023 07:09:52 GMT  
		Size: 5.1 MB (5078084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52698a3efa93904b0f9e31143300d218ee09e1094c4750deee936722a434c9f0`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354b5f484857495c910fe4f837972933f33fd6843557455f4bdf4f353ef6128f`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c06258e4387dc50c2c887507689557c15c1676fa0c66e537b7d0dd4d052267`  
		Last Modified: Wed, 10 May 2023 07:09:51 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1975391c3359e794cc1f15388c47f08ef7f9587a8f1ba4cf78d70a6586eaafd6`  
		Last Modified: Wed, 10 May 2023 07:09:50 GMT  
		Size: 1.1 KB (1141 bytes)  
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
$ docker pull nats@sha256:f7cb4ed36f2be5c7be9a7b08d8c1b22e645f58ba4991dfa459e74577d9f4b615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:windowsservercore` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:1732bbcb34375aafeac01e77ce6e7aa2dbba27278ba12958bb3aed917f0c1dc0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077822911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8bfcb2ac53edf941120e941b4913e75121f8f7849d6c69cd234724ac1354311`
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
# Wed, 10 May 2023 02:40:27 GMT
ENV NATS_SERVER=2.9.16
# Wed, 10 May 2023 02:40:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.16/nats-server-v2.9.16-windows-amd64.zip
# Wed, 10 May 2023 02:40:29 GMT
ENV NATS_SERVER_SHASUM=293013cd810f35f2a3dd25b0d850da248bc45af46b854a805383f848db3e9fa0
# Wed, 10 May 2023 02:41:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 May 2023 02:43:41 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 May 2023 02:43:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 May 2023 02:43:43 GMT
EXPOSE 4222 6222 8222
# Wed, 10 May 2023 02:43:44 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 May 2023 02:43:44 GMT
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
	-	`sha256:1de33925544fc248e0ffac22a06e9727c7ba90ba2cb7db16eeaaff706776402b`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7135feb8500e9833370ec21c3622cf7fbba7424afcac727b61e304376265d4be`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5271c6f8ccb837e1ce744ad44305a94c606b0be8b8485718313913c90315cd`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bcd42cac1942260a2fe8430628f8d0f792cc8361dd67fab848150d01b97657`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 426.3 KB (426266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a398f7862050ef8d8f732aef1986f5db3a45557b30ba2a17c22f482c023b9f`  
		Last Modified: Wed, 10 May 2023 07:09:35 GMT  
		Size: 5.3 MB (5348225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d534b19d5fbf3dd2d41d8086faca3ddedf186adbb103979e6d76101e3eec78d`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 2.0 KB (1968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fd8189adda36aa8738fc9e85d0a25701a5a0e38a451afa5af1700e7e79d67e`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78173f06e168d48cc7aa1d4654204d98d914ae854728a118131ffe8d9181a82f`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cd778f6318ee8c3823680bf429cf481faec2f6f7e714cde79309dfc917345a`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:f7cb4ed36f2be5c7be9a7b08d8c1b22e645f58ba4991dfa459e74577d9f4b615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:1732bbcb34375aafeac01e77ce6e7aa2dbba27278ba12958bb3aed917f0c1dc0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077822911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8bfcb2ac53edf941120e941b4913e75121f8f7849d6c69cd234724ac1354311`
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
# Wed, 10 May 2023 02:40:27 GMT
ENV NATS_SERVER=2.9.16
# Wed, 10 May 2023 02:40:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.16/nats-server-v2.9.16-windows-amd64.zip
# Wed, 10 May 2023 02:40:29 GMT
ENV NATS_SERVER_SHASUM=293013cd810f35f2a3dd25b0d850da248bc45af46b854a805383f848db3e9fa0
# Wed, 10 May 2023 02:41:47 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 May 2023 02:43:41 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 May 2023 02:43:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 May 2023 02:43:43 GMT
EXPOSE 4222 6222 8222
# Wed, 10 May 2023 02:43:44 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 May 2023 02:43:44 GMT
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
	-	`sha256:1de33925544fc248e0ffac22a06e9727c7ba90ba2cb7db16eeaaff706776402b`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7135feb8500e9833370ec21c3622cf7fbba7424afcac727b61e304376265d4be`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5271c6f8ccb837e1ce744ad44305a94c606b0be8b8485718313913c90315cd`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bcd42cac1942260a2fe8430628f8d0f792cc8361dd67fab848150d01b97657`  
		Last Modified: Wed, 10 May 2023 07:09:36 GMT  
		Size: 426.3 KB (426266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a398f7862050ef8d8f732aef1986f5db3a45557b30ba2a17c22f482c023b9f`  
		Last Modified: Wed, 10 May 2023 07:09:35 GMT  
		Size: 5.3 MB (5348225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d534b19d5fbf3dd2d41d8086faca3ddedf186adbb103979e6d76101e3eec78d`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 2.0 KB (1968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fd8189adda36aa8738fc9e85d0a25701a5a0e38a451afa5af1700e7e79d67e`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78173f06e168d48cc7aa1d4654204d98d914ae854728a118131ffe8d9181a82f`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cd778f6318ee8c3823680bf429cf481faec2f6f7e714cde79309dfc917345a`  
		Last Modified: Wed, 10 May 2023 07:09:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
