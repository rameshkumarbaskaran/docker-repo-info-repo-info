<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.16`](#nats2-alpine316)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.9`](#nats29)
-	[`nats:2.9-alpine`](#nats29-alpine)
-	[`nats:2.9-alpine3.16`](#nats29-alpine316)
-	[`nats:2.9-linux`](#nats29-linux)
-	[`nats:2.9-nanoserver`](#nats29-nanoserver)
-	[`nats:2.9-nanoserver-1809`](#nats29-nanoserver-1809)
-	[`nats:2.9-scratch`](#nats29-scratch)
-	[`nats:2.9-windowsservercore`](#nats29-windowsservercore)
-	[`nats:2.9-windowsservercore-1809`](#nats29-windowsservercore-1809)
-	[`nats:2.9.3`](#nats293)
-	[`nats:2.9.3-alpine`](#nats293-alpine)
-	[`nats:2.9.3-alpine3.16`](#nats293-alpine316)
-	[`nats:2.9.3-linux`](#nats293-linux)
-	[`nats:2.9.3-nanoserver`](#nats293-nanoserver)
-	[`nats:2.9.3-nanoserver-1809`](#nats293-nanoserver-1809)
-	[`nats:2.9.3-scratch`](#nats293-scratch)
-	[`nats:2.9.3-windowsservercore`](#nats293-windowsservercore)
-	[`nats:2.9.3-windowsservercore-1809`](#nats293-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.16`](#natsalpine316)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:9ab5a62adfc3057ad67f8d1930e5aacba1669658bb6f4901f1783e31877d17f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3532; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:0008930d6f49b1c3a706f5e751756e25faa913eb0d24a4d1a3cc7111995c2cc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4907907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae8e0e40e5d6a88833150b7613d8c2af98aeeefd0da6dca3100722e12b19571`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:3f7f7d06c5f77e836d502f53de29b2d7a2e80853d13b4d9c75b6bda16857761b in /nats-server 
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:25:42 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:25:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d6d85ead114c982a0357d6002a45433e3f39494cdc0f3cc920d804a45cae35ee`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 4.9 MB (4907400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60865ecae70fb12a59e8579974bc3d65a97b7e84fcd8fe6445d275320879ea5`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:8f0d092d06af2710b06354ee677b81f10f6251a0e8efb0421d8d3f86d1000677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4675550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbbb2f82c0829a2a87cd2ea49c73284638f5861690c6b230951c2b6ca549d06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:65c01e5e1e16c3f3b2d7df9541699c9363f45a0a991482d97d24193d7e1bb29a in /nats-server 
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:49:34 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4db83ef5484b7db61a63b554c60491f4a902ca94cce6b612d3aa32aa92888ec6`  
		Last Modified: Tue, 11 Oct 2022 17:51:01 GMT  
		Size: 4.7 MB (4675041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb93982fc62459387f27a9bde43633a8c758cec8404805cd92613cad4436f4d`  
		Last Modified: Tue, 11 Oct 2022 17:51:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:14a5c2b109967d3adb793cd0ab698648bc10a969bff48575c619a09e6e5ad232
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4664630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7884a65e2ecb2f9f6974f0b17533ba58e8845ff3d4e2f58f62762e8980ddbc5b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:34c532093a5dbef0c1af4a815d6c675cdb6125f12b5f44a7f2b662696b571b90 in /nats-server 
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:58:03 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:58:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:58:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:58:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:03af04ed4c28e4580e7b4c3a5ea1484aae440ba7d2dd4e9a656d77d82dd54b98`  
		Last Modified: Tue, 11 Oct 2022 17:59:30 GMT  
		Size: 4.7 MB (4664122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7148a4d5aff61489f0013cd47ecaf37fcf9a49f79472e42dd389601319be9422`  
		Last Modified: Tue, 11 Oct 2022 17:59:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc4ef43bc1c7b49a3550af75cf1940321e1f5565da18e0f178bde6acd5a36bdd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f962526ab017817241bd3fbee96aff03c8852436cf5bcdc0a58b5e3fe5a09d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:40:23 GMT
COPY file:bc86ca7535653a0512f71a856c462b418bdf59420e8fa4ca2103093ecb5bf96e in /nats-server 
# Tue, 11 Oct 2022 17:40:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:40:24 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:40:26 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:40:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a147f8167144f46b22ee755fdae458d8e5b2fa34cb9a04d5b0393033d9044e08`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 4.5 MB (4497202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e720a4acb8f391823b838f963c0b4de61247a73c4721a3224829968b7b7c0e4c`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:1a1502e9c757eecbb9d40c1795b8aa966bd4c2fab0e557fb56b2db28114f15e1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108344947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821890b5ce167e8d00c7802b4c1b05e6d186a42968f0d0c99b33f0e57d80cbac`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:25:57 GMT
RUN cmd /S /C #(nop) COPY file:ebd16169defae69259e980faeec8d0a781382823c2f6ba62e4124678fe7cd5ff in C:\nats-server.exe 
# Tue, 11 Oct 2022 17:25:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:26:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:26:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f4d5c8d186c8f312a6ae9319e5853518d0fd4d59cf203ad7f21ee572928fb0`  
		Last Modified: Tue, 11 Oct 2022 17:26:54 GMT  
		Size: 5.0 MB (4961254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147afea671cb39b7c3224c41bef90d62a0a4af88ed1d5807480181a613275a6b`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db765622dc1c4a61d8097b7d5c78f046e4111d96704078aa12c8e6af33ef68e5`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a39cb9946d421dff62e99511f125369156430794a031de774db3f5430cfd2ed`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d278ea5c62988b5ad67b51302fdd9bf43d7f72187d576dc0878bac41e162c12`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:e0615d6d59dad37b1eee587e2e89d2feee1d93537c4f5d68a6550685f0d1ab48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:bf9cae35d4496a6557faaaa46222bc55961ffdea0f6d833968a7fe798581a289
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8000982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d664099656e24efd4de4cdc101c35c38e79e635d0fc49a9a5c79774363ea5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:25:33 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:25:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:25:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:25:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:25:35 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:25:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73aeb9277156392c66e1a873af420eca6482f253b894387e7e80883cbdb4249`  
		Last Modified: Tue, 11 Oct 2022 17:26:08 GMT  
		Size: 5.2 MB (5193929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0307d13e86598b08828290bb6740eb65b29f5fdd9ee5bd8b4c8eed473d84bf56`  
		Last Modified: Tue, 11 Oct 2022 17:26:07 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66055fe8b1856a88ca9c9afb0b9bbf6592e9bacb1b170260b235b8e4bf356de`  
		Last Modified: Tue, 11 Oct 2022 17:26:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:45edeee49c18b5594b54054229f8783c0db4ea87cbee5afae59c9984301cfd08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7571449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94b7a3987a9935b4c2d3b4242a054e954088cd7a9625b8913193cb56590f841`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:49:20 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:49:22 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:49:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5485032ca7ba2b0f0c8d9b075d5e1e340c36377267e4b3ae41c4e2f7894e91`  
		Last Modified: Tue, 11 Oct 2022 17:50:29 GMT  
		Size: 5.0 MB (4956483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7900c6c1d0cb325952cdd6ae71490a3e0b941af92e71f22de10187efa837d703`  
		Last Modified: Tue, 11 Oct 2022 17:50:28 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b5305ca20b90d113889b94211f4949a2fffcc5faa2c5844fb1091fec4a866`  
		Last Modified: Tue, 11 Oct 2022 17:50:28 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a5e65b6fa62d1d428e050efe382bbb2005f94464c7818f635f5920bcefb6f106
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7371964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abced2cbd4c41ff1e9075d451f2649984429dc4115edb90e30fe487288cb9155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:57:40 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:57:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:57:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:57:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:57:43 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:57:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:57:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8c3c4b8cb46efedb04498db6fa20cd55763c0418b70a87ca3ec04ae2679149`  
		Last Modified: Tue, 11 Oct 2022 17:58:57 GMT  
		Size: 5.0 MB (4953899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9754b757cf985fb40c2726f1043ee751fdf5c5ceba1b57acd9ac4182d17a14`  
		Last Modified: Tue, 11 Oct 2022 17:58:56 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f195bb3987db93e4b84ec3c227bd96a40f580b48ae1b269d48de5183443d24f3`  
		Last Modified: Tue, 11 Oct 2022 17:58:56 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb4394d1cb68931c388d303a356838d71e8cdd1c35eb7bd1dd0d145fc2a845d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8492b76ba91c73798af6bc47734164369b9bc2a414e2089d076d6541df9c4f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:40:06 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:40:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:40:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:40:11 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:40:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cea947ad70084e9470d551b1b736974de4f3633c4fe3d13eef48b5cb1b08b62`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 4.8 MB (4778601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86247e116e9902a618c7b5998f94f6f0117d8ef407b3e6d7437f59f1a1213057`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582e80d779e2f3e9eeb095bd75ba94437c2b08083ea399361835668c478359e1`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.16`

```console
$ docker pull nats@sha256:e0615d6d59dad37b1eee587e2e89d2feee1d93537c4f5d68a6550685f0d1ab48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.16` - linux; amd64

```console
$ docker pull nats@sha256:bf9cae35d4496a6557faaaa46222bc55961ffdea0f6d833968a7fe798581a289
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8000982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d664099656e24efd4de4cdc101c35c38e79e635d0fc49a9a5c79774363ea5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:25:33 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:25:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:25:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:25:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:25:35 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:25:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73aeb9277156392c66e1a873af420eca6482f253b894387e7e80883cbdb4249`  
		Last Modified: Tue, 11 Oct 2022 17:26:08 GMT  
		Size: 5.2 MB (5193929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0307d13e86598b08828290bb6740eb65b29f5fdd9ee5bd8b4c8eed473d84bf56`  
		Last Modified: Tue, 11 Oct 2022 17:26:07 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66055fe8b1856a88ca9c9afb0b9bbf6592e9bacb1b170260b235b8e4bf356de`  
		Last Modified: Tue, 11 Oct 2022 17:26:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.16` - linux; arm variant v6

```console
$ docker pull nats@sha256:45edeee49c18b5594b54054229f8783c0db4ea87cbee5afae59c9984301cfd08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7571449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94b7a3987a9935b4c2d3b4242a054e954088cd7a9625b8913193cb56590f841`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:49:20 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:49:22 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:49:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5485032ca7ba2b0f0c8d9b075d5e1e340c36377267e4b3ae41c4e2f7894e91`  
		Last Modified: Tue, 11 Oct 2022 17:50:29 GMT  
		Size: 5.0 MB (4956483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7900c6c1d0cb325952cdd6ae71490a3e0b941af92e71f22de10187efa837d703`  
		Last Modified: Tue, 11 Oct 2022 17:50:28 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b5305ca20b90d113889b94211f4949a2fffcc5faa2c5844fb1091fec4a866`  
		Last Modified: Tue, 11 Oct 2022 17:50:28 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.16` - linux; arm variant v7

```console
$ docker pull nats@sha256:a5e65b6fa62d1d428e050efe382bbb2005f94464c7818f635f5920bcefb6f106
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7371964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abced2cbd4c41ff1e9075d451f2649984429dc4115edb90e30fe487288cb9155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:57:40 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:57:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:57:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:57:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:57:43 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:57:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:57:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8c3c4b8cb46efedb04498db6fa20cd55763c0418b70a87ca3ec04ae2679149`  
		Last Modified: Tue, 11 Oct 2022 17:58:57 GMT  
		Size: 5.0 MB (4953899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9754b757cf985fb40c2726f1043ee751fdf5c5ceba1b57acd9ac4182d17a14`  
		Last Modified: Tue, 11 Oct 2022 17:58:56 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f195bb3987db93e4b84ec3c227bd96a40f580b48ae1b269d48de5183443d24f3`  
		Last Modified: Tue, 11 Oct 2022 17:58:56 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb4394d1cb68931c388d303a356838d71e8cdd1c35eb7bd1dd0d145fc2a845d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8492b76ba91c73798af6bc47734164369b9bc2a414e2089d076d6541df9c4f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:40:06 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:40:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:40:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:40:11 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:40:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cea947ad70084e9470d551b1b736974de4f3633c4fe3d13eef48b5cb1b08b62`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 4.8 MB (4778601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86247e116e9902a618c7b5998f94f6f0117d8ef407b3e6d7437f59f1a1213057`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582e80d779e2f3e9eeb095bd75ba94437c2b08083ea399361835668c478359e1`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:464514526a41389cb8eba22f4222d1e44dbfbc570acdb09a32d557c9b9955a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:0008930d6f49b1c3a706f5e751756e25faa913eb0d24a4d1a3cc7111995c2cc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4907907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae8e0e40e5d6a88833150b7613d8c2af98aeeefd0da6dca3100722e12b19571`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:3f7f7d06c5f77e836d502f53de29b2d7a2e80853d13b4d9c75b6bda16857761b in /nats-server 
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:25:42 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:25:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d6d85ead114c982a0357d6002a45433e3f39494cdc0f3cc920d804a45cae35ee`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 4.9 MB (4907400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60865ecae70fb12a59e8579974bc3d65a97b7e84fcd8fe6445d275320879ea5`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:8f0d092d06af2710b06354ee677b81f10f6251a0e8efb0421d8d3f86d1000677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4675550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbbb2f82c0829a2a87cd2ea49c73284638f5861690c6b230951c2b6ca549d06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:65c01e5e1e16c3f3b2d7df9541699c9363f45a0a991482d97d24193d7e1bb29a in /nats-server 
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:49:34 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4db83ef5484b7db61a63b554c60491f4a902ca94cce6b612d3aa32aa92888ec6`  
		Last Modified: Tue, 11 Oct 2022 17:51:01 GMT  
		Size: 4.7 MB (4675041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb93982fc62459387f27a9bde43633a8c758cec8404805cd92613cad4436f4d`  
		Last Modified: Tue, 11 Oct 2022 17:51:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:14a5c2b109967d3adb793cd0ab698648bc10a969bff48575c619a09e6e5ad232
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4664630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7884a65e2ecb2f9f6974f0b17533ba58e8845ff3d4e2f58f62762e8980ddbc5b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:34c532093a5dbef0c1af4a815d6c675cdb6125f12b5f44a7f2b662696b571b90 in /nats-server 
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:58:03 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:58:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:58:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:58:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:03af04ed4c28e4580e7b4c3a5ea1484aae440ba7d2dd4e9a656d77d82dd54b98`  
		Last Modified: Tue, 11 Oct 2022 17:59:30 GMT  
		Size: 4.7 MB (4664122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7148a4d5aff61489f0013cd47ecaf37fcf9a49f79472e42dd389601319be9422`  
		Last Modified: Tue, 11 Oct 2022 17:59:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc4ef43bc1c7b49a3550af75cf1940321e1f5565da18e0f178bde6acd5a36bdd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f962526ab017817241bd3fbee96aff03c8852436cf5bcdc0a58b5e3fe5a09d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:40:23 GMT
COPY file:bc86ca7535653a0512f71a856c462b418bdf59420e8fa4ca2103093ecb5bf96e in /nats-server 
# Tue, 11 Oct 2022 17:40:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:40:24 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:40:26 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:40:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a147f8167144f46b22ee755fdae458d8e5b2fa34cb9a04d5b0393033d9044e08`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 4.5 MB (4497202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e720a4acb8f391823b838f963c0b4de61247a73c4721a3224829968b7b7c0e4c`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:e98b441edfc72745b80116d6ea3b5ebd4e6bb7ef160f06a905150370864838b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:1a1502e9c757eecbb9d40c1795b8aa966bd4c2fab0e557fb56b2db28114f15e1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108344947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821890b5ce167e8d00c7802b4c1b05e6d186a42968f0d0c99b33f0e57d80cbac`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:25:57 GMT
RUN cmd /S /C #(nop) COPY file:ebd16169defae69259e980faeec8d0a781382823c2f6ba62e4124678fe7cd5ff in C:\nats-server.exe 
# Tue, 11 Oct 2022 17:25:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:26:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:26:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f4d5c8d186c8f312a6ae9319e5853518d0fd4d59cf203ad7f21ee572928fb0`  
		Last Modified: Tue, 11 Oct 2022 17:26:54 GMT  
		Size: 5.0 MB (4961254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147afea671cb39b7c3224c41bef90d62a0a4af88ed1d5807480181a613275a6b`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db765622dc1c4a61d8097b7d5c78f046e4111d96704078aa12c8e6af33ef68e5`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a39cb9946d421dff62e99511f125369156430794a031de774db3f5430cfd2ed`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d278ea5c62988b5ad67b51302fdd9bf43d7f72187d576dc0878bac41e162c12`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:e98b441edfc72745b80116d6ea3b5ebd4e6bb7ef160f06a905150370864838b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:1a1502e9c757eecbb9d40c1795b8aa966bd4c2fab0e557fb56b2db28114f15e1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108344947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821890b5ce167e8d00c7802b4c1b05e6d186a42968f0d0c99b33f0e57d80cbac`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:25:57 GMT
RUN cmd /S /C #(nop) COPY file:ebd16169defae69259e980faeec8d0a781382823c2f6ba62e4124678fe7cd5ff in C:\nats-server.exe 
# Tue, 11 Oct 2022 17:25:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:26:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:26:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f4d5c8d186c8f312a6ae9319e5853518d0fd4d59cf203ad7f21ee572928fb0`  
		Last Modified: Tue, 11 Oct 2022 17:26:54 GMT  
		Size: 5.0 MB (4961254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147afea671cb39b7c3224c41bef90d62a0a4af88ed1d5807480181a613275a6b`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db765622dc1c4a61d8097b7d5c78f046e4111d96704078aa12c8e6af33ef68e5`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a39cb9946d421dff62e99511f125369156430794a031de774db3f5430cfd2ed`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d278ea5c62988b5ad67b51302fdd9bf43d7f72187d576dc0878bac41e162c12`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:464514526a41389cb8eba22f4222d1e44dbfbc570acdb09a32d557c9b9955a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:0008930d6f49b1c3a706f5e751756e25faa913eb0d24a4d1a3cc7111995c2cc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4907907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae8e0e40e5d6a88833150b7613d8c2af98aeeefd0da6dca3100722e12b19571`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:3f7f7d06c5f77e836d502f53de29b2d7a2e80853d13b4d9c75b6bda16857761b in /nats-server 
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:25:42 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:25:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d6d85ead114c982a0357d6002a45433e3f39494cdc0f3cc920d804a45cae35ee`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 4.9 MB (4907400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60865ecae70fb12a59e8579974bc3d65a97b7e84fcd8fe6445d275320879ea5`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:8f0d092d06af2710b06354ee677b81f10f6251a0e8efb0421d8d3f86d1000677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4675550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbbb2f82c0829a2a87cd2ea49c73284638f5861690c6b230951c2b6ca549d06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:65c01e5e1e16c3f3b2d7df9541699c9363f45a0a991482d97d24193d7e1bb29a in /nats-server 
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:49:34 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4db83ef5484b7db61a63b554c60491f4a902ca94cce6b612d3aa32aa92888ec6`  
		Last Modified: Tue, 11 Oct 2022 17:51:01 GMT  
		Size: 4.7 MB (4675041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb93982fc62459387f27a9bde43633a8c758cec8404805cd92613cad4436f4d`  
		Last Modified: Tue, 11 Oct 2022 17:51:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:14a5c2b109967d3adb793cd0ab698648bc10a969bff48575c619a09e6e5ad232
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4664630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7884a65e2ecb2f9f6974f0b17533ba58e8845ff3d4e2f58f62762e8980ddbc5b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:34c532093a5dbef0c1af4a815d6c675cdb6125f12b5f44a7f2b662696b571b90 in /nats-server 
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:58:03 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:58:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:58:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:58:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:03af04ed4c28e4580e7b4c3a5ea1484aae440ba7d2dd4e9a656d77d82dd54b98`  
		Last Modified: Tue, 11 Oct 2022 17:59:30 GMT  
		Size: 4.7 MB (4664122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7148a4d5aff61489f0013cd47ecaf37fcf9a49f79472e42dd389601319be9422`  
		Last Modified: Tue, 11 Oct 2022 17:59:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc4ef43bc1c7b49a3550af75cf1940321e1f5565da18e0f178bde6acd5a36bdd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f962526ab017817241bd3fbee96aff03c8852436cf5bcdc0a58b5e3fe5a09d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:40:23 GMT
COPY file:bc86ca7535653a0512f71a856c462b418bdf59420e8fa4ca2103093ecb5bf96e in /nats-server 
# Tue, 11 Oct 2022 17:40:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:40:24 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:40:26 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:40:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a147f8167144f46b22ee755fdae458d8e5b2fa34cb9a04d5b0393033d9044e08`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 4.5 MB (4497202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e720a4acb8f391823b838f963c0b4de61247a73c4721a3224829968b7b7c0e4c`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:fb39a5ed839f11261b832e0dca62197ee21a2ad938138f4cc656a9a52d03d975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:4bddc4dfe1d225cfe86ce8237721abb0c49bd069e8c0bf1ab5c0ba2ec5c6899b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2716818637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ab84e2e207d755fd864c921bfee7744f5f0533ef2a8eb1649486351579db39`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 17:22:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Oct 2022 17:22:08 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:22:09 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:22:10 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.3/nats-server-v2.9.3-windows-amd64.zip
# Tue, 11 Oct 2022 17:22:11 GMT
ENV NATS_SERVER_SHASUM=83b25dad03dee498becb734623ae4d096235b2863be878d5f6d6a32d76f7e85f
# Tue, 11 Oct 2022 17:23:56 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Oct 2022 17:25:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 11 Oct 2022 17:25:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:32 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:25:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c778a0131ae2f1653f1fb703f05998e74365629f70b1a15a0360fb1292182846`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ce79ce85e7eb7d4b12316d81cc8cb3ff2567ee214f4aa0bbf36933fd55891f`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462d88c3de2e572b0d0ee482e3424c3ecb6eae150e8b29e5c8678a3059178bea`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12db35ec0388714c2e4e91a025ad3c010583c420b244c7941d378814da4b414`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61065ad9c7494c241e65c1c1b701828947105c6de39a9a246ef1da83d1967b`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a922f9001668df7166a8c2806eb76dacbac25dfe2a6a6b366546a53ff4a68be`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 350.4 KB (350379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696f9101e75d054c09b2f5086fdb484f298ac859200417dc480c0c95d4db8b79`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 5.3 MB (5290962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063d7a0294a6b35b745dafda4218ac1caccd20c2862af30174e073d25df4240f`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d46f46f65dffc178e8ef8c4d17fc35f23e32db9c2b23028319ab7d51f92b36e`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea87d29a4c3431239148436823825cc53a83211b86daa22eb69df30ff028bde`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245dfbad1025b6c7d6ad15e3336d3a11bd111607ce8db6de8efed6a157cc5872`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:fb39a5ed839f11261b832e0dca62197ee21a2ad938138f4cc656a9a52d03d975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:4bddc4dfe1d225cfe86ce8237721abb0c49bd069e8c0bf1ab5c0ba2ec5c6899b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2716818637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ab84e2e207d755fd864c921bfee7744f5f0533ef2a8eb1649486351579db39`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 17:22:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Oct 2022 17:22:08 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:22:09 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:22:10 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.3/nats-server-v2.9.3-windows-amd64.zip
# Tue, 11 Oct 2022 17:22:11 GMT
ENV NATS_SERVER_SHASUM=83b25dad03dee498becb734623ae4d096235b2863be878d5f6d6a32d76f7e85f
# Tue, 11 Oct 2022 17:23:56 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Oct 2022 17:25:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 11 Oct 2022 17:25:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:32 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:25:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c778a0131ae2f1653f1fb703f05998e74365629f70b1a15a0360fb1292182846`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ce79ce85e7eb7d4b12316d81cc8cb3ff2567ee214f4aa0bbf36933fd55891f`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462d88c3de2e572b0d0ee482e3424c3ecb6eae150e8b29e5c8678a3059178bea`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12db35ec0388714c2e4e91a025ad3c010583c420b244c7941d378814da4b414`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61065ad9c7494c241e65c1c1b701828947105c6de39a9a246ef1da83d1967b`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a922f9001668df7166a8c2806eb76dacbac25dfe2a6a6b366546a53ff4a68be`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 350.4 KB (350379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696f9101e75d054c09b2f5086fdb484f298ac859200417dc480c0c95d4db8b79`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 5.3 MB (5290962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063d7a0294a6b35b745dafda4218ac1caccd20c2862af30174e073d25df4240f`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d46f46f65dffc178e8ef8c4d17fc35f23e32db9c2b23028319ab7d51f92b36e`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea87d29a4c3431239148436823825cc53a83211b86daa22eb69df30ff028bde`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245dfbad1025b6c7d6ad15e3336d3a11bd111607ce8db6de8efed6a157cc5872`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:9ab5a62adfc3057ad67f8d1930e5aacba1669658bb6f4901f1783e31877d17f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3532; amd64

### `nats:2.9` - linux; amd64

```console
$ docker pull nats@sha256:0008930d6f49b1c3a706f5e751756e25faa913eb0d24a4d1a3cc7111995c2cc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4907907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae8e0e40e5d6a88833150b7613d8c2af98aeeefd0da6dca3100722e12b19571`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:3f7f7d06c5f77e836d502f53de29b2d7a2e80853d13b4d9c75b6bda16857761b in /nats-server 
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:25:42 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:25:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d6d85ead114c982a0357d6002a45433e3f39494cdc0f3cc920d804a45cae35ee`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 4.9 MB (4907400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60865ecae70fb12a59e8579974bc3d65a97b7e84fcd8fe6445d275320879ea5`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:8f0d092d06af2710b06354ee677b81f10f6251a0e8efb0421d8d3f86d1000677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4675550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbbb2f82c0829a2a87cd2ea49c73284638f5861690c6b230951c2b6ca549d06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:65c01e5e1e16c3f3b2d7df9541699c9363f45a0a991482d97d24193d7e1bb29a in /nats-server 
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:49:34 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4db83ef5484b7db61a63b554c60491f4a902ca94cce6b612d3aa32aa92888ec6`  
		Last Modified: Tue, 11 Oct 2022 17:51:01 GMT  
		Size: 4.7 MB (4675041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb93982fc62459387f27a9bde43633a8c758cec8404805cd92613cad4436f4d`  
		Last Modified: Tue, 11 Oct 2022 17:51:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:14a5c2b109967d3adb793cd0ab698648bc10a969bff48575c619a09e6e5ad232
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4664630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7884a65e2ecb2f9f6974f0b17533ba58e8845ff3d4e2f58f62762e8980ddbc5b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:34c532093a5dbef0c1af4a815d6c675cdb6125f12b5f44a7f2b662696b571b90 in /nats-server 
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:58:03 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:58:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:58:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:58:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:03af04ed4c28e4580e7b4c3a5ea1484aae440ba7d2dd4e9a656d77d82dd54b98`  
		Last Modified: Tue, 11 Oct 2022 17:59:30 GMT  
		Size: 4.7 MB (4664122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7148a4d5aff61489f0013cd47ecaf37fcf9a49f79472e42dd389601319be9422`  
		Last Modified: Tue, 11 Oct 2022 17:59:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc4ef43bc1c7b49a3550af75cf1940321e1f5565da18e0f178bde6acd5a36bdd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f962526ab017817241bd3fbee96aff03c8852436cf5bcdc0a58b5e3fe5a09d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:40:23 GMT
COPY file:bc86ca7535653a0512f71a856c462b418bdf59420e8fa4ca2103093ecb5bf96e in /nats-server 
# Tue, 11 Oct 2022 17:40:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:40:24 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:40:26 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:40:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a147f8167144f46b22ee755fdae458d8e5b2fa34cb9a04d5b0393033d9044e08`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 4.5 MB (4497202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e720a4acb8f391823b838f963c0b4de61247a73c4721a3224829968b7b7c0e4c`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:1a1502e9c757eecbb9d40c1795b8aa966bd4c2fab0e557fb56b2db28114f15e1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108344947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821890b5ce167e8d00c7802b4c1b05e6d186a42968f0d0c99b33f0e57d80cbac`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:25:57 GMT
RUN cmd /S /C #(nop) COPY file:ebd16169defae69259e980faeec8d0a781382823c2f6ba62e4124678fe7cd5ff in C:\nats-server.exe 
# Tue, 11 Oct 2022 17:25:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:26:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:26:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f4d5c8d186c8f312a6ae9319e5853518d0fd4d59cf203ad7f21ee572928fb0`  
		Last Modified: Tue, 11 Oct 2022 17:26:54 GMT  
		Size: 5.0 MB (4961254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147afea671cb39b7c3224c41bef90d62a0a4af88ed1d5807480181a613275a6b`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db765622dc1c4a61d8097b7d5c78f046e4111d96704078aa12c8e6af33ef68e5`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a39cb9946d421dff62e99511f125369156430794a031de774db3f5430cfd2ed`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d278ea5c62988b5ad67b51302fdd9bf43d7f72187d576dc0878bac41e162c12`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine`

```console
$ docker pull nats@sha256:e0615d6d59dad37b1eee587e2e89d2feee1d93537c4f5d68a6550685f0d1ab48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:bf9cae35d4496a6557faaaa46222bc55961ffdea0f6d833968a7fe798581a289
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8000982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d664099656e24efd4de4cdc101c35c38e79e635d0fc49a9a5c79774363ea5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:25:33 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:25:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:25:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:25:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:25:35 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:25:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73aeb9277156392c66e1a873af420eca6482f253b894387e7e80883cbdb4249`  
		Last Modified: Tue, 11 Oct 2022 17:26:08 GMT  
		Size: 5.2 MB (5193929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0307d13e86598b08828290bb6740eb65b29f5fdd9ee5bd8b4c8eed473d84bf56`  
		Last Modified: Tue, 11 Oct 2022 17:26:07 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66055fe8b1856a88ca9c9afb0b9bbf6592e9bacb1b170260b235b8e4bf356de`  
		Last Modified: Tue, 11 Oct 2022 17:26:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:45edeee49c18b5594b54054229f8783c0db4ea87cbee5afae59c9984301cfd08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7571449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94b7a3987a9935b4c2d3b4242a054e954088cd7a9625b8913193cb56590f841`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:49:20 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:49:22 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:49:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5485032ca7ba2b0f0c8d9b075d5e1e340c36377267e4b3ae41c4e2f7894e91`  
		Last Modified: Tue, 11 Oct 2022 17:50:29 GMT  
		Size: 5.0 MB (4956483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7900c6c1d0cb325952cdd6ae71490a3e0b941af92e71f22de10187efa837d703`  
		Last Modified: Tue, 11 Oct 2022 17:50:28 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b5305ca20b90d113889b94211f4949a2fffcc5faa2c5844fb1091fec4a866`  
		Last Modified: Tue, 11 Oct 2022 17:50:28 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a5e65b6fa62d1d428e050efe382bbb2005f94464c7818f635f5920bcefb6f106
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7371964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abced2cbd4c41ff1e9075d451f2649984429dc4115edb90e30fe487288cb9155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:57:40 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:57:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:57:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:57:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:57:43 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:57:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:57:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8c3c4b8cb46efedb04498db6fa20cd55763c0418b70a87ca3ec04ae2679149`  
		Last Modified: Tue, 11 Oct 2022 17:58:57 GMT  
		Size: 5.0 MB (4953899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9754b757cf985fb40c2726f1043ee751fdf5c5ceba1b57acd9ac4182d17a14`  
		Last Modified: Tue, 11 Oct 2022 17:58:56 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f195bb3987db93e4b84ec3c227bd96a40f580b48ae1b269d48de5183443d24f3`  
		Last Modified: Tue, 11 Oct 2022 17:58:56 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb4394d1cb68931c388d303a356838d71e8cdd1c35eb7bd1dd0d145fc2a845d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8492b76ba91c73798af6bc47734164369b9bc2a414e2089d076d6541df9c4f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:40:06 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:40:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:40:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:40:11 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:40:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cea947ad70084e9470d551b1b736974de4f3633c4fe3d13eef48b5cb1b08b62`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 4.8 MB (4778601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86247e116e9902a618c7b5998f94f6f0117d8ef407b3e6d7437f59f1a1213057`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582e80d779e2f3e9eeb095bd75ba94437c2b08083ea399361835668c478359e1`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.16`

```console
$ docker pull nats@sha256:e0615d6d59dad37b1eee587e2e89d2feee1d93537c4f5d68a6550685f0d1ab48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.16` - linux; amd64

```console
$ docker pull nats@sha256:bf9cae35d4496a6557faaaa46222bc55961ffdea0f6d833968a7fe798581a289
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8000982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d664099656e24efd4de4cdc101c35c38e79e635d0fc49a9a5c79774363ea5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:25:33 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:25:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:25:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:25:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:25:35 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:25:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73aeb9277156392c66e1a873af420eca6482f253b894387e7e80883cbdb4249`  
		Last Modified: Tue, 11 Oct 2022 17:26:08 GMT  
		Size: 5.2 MB (5193929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0307d13e86598b08828290bb6740eb65b29f5fdd9ee5bd8b4c8eed473d84bf56`  
		Last Modified: Tue, 11 Oct 2022 17:26:07 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66055fe8b1856a88ca9c9afb0b9bbf6592e9bacb1b170260b235b8e4bf356de`  
		Last Modified: Tue, 11 Oct 2022 17:26:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.16` - linux; arm variant v6

```console
$ docker pull nats@sha256:45edeee49c18b5594b54054229f8783c0db4ea87cbee5afae59c9984301cfd08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7571449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94b7a3987a9935b4c2d3b4242a054e954088cd7a9625b8913193cb56590f841`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:49:20 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:49:22 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:49:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5485032ca7ba2b0f0c8d9b075d5e1e340c36377267e4b3ae41c4e2f7894e91`  
		Last Modified: Tue, 11 Oct 2022 17:50:29 GMT  
		Size: 5.0 MB (4956483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7900c6c1d0cb325952cdd6ae71490a3e0b941af92e71f22de10187efa837d703`  
		Last Modified: Tue, 11 Oct 2022 17:50:28 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b5305ca20b90d113889b94211f4949a2fffcc5faa2c5844fb1091fec4a866`  
		Last Modified: Tue, 11 Oct 2022 17:50:28 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.16` - linux; arm variant v7

```console
$ docker pull nats@sha256:a5e65b6fa62d1d428e050efe382bbb2005f94464c7818f635f5920bcefb6f106
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7371964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abced2cbd4c41ff1e9075d451f2649984429dc4115edb90e30fe487288cb9155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:57:40 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:57:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:57:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:57:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:57:43 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:57:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:57:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8c3c4b8cb46efedb04498db6fa20cd55763c0418b70a87ca3ec04ae2679149`  
		Last Modified: Tue, 11 Oct 2022 17:58:57 GMT  
		Size: 5.0 MB (4953899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9754b757cf985fb40c2726f1043ee751fdf5c5ceba1b57acd9ac4182d17a14`  
		Last Modified: Tue, 11 Oct 2022 17:58:56 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f195bb3987db93e4b84ec3c227bd96a40f580b48ae1b269d48de5183443d24f3`  
		Last Modified: Tue, 11 Oct 2022 17:58:56 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb4394d1cb68931c388d303a356838d71e8cdd1c35eb7bd1dd0d145fc2a845d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8492b76ba91c73798af6bc47734164369b9bc2a414e2089d076d6541df9c4f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:40:06 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:40:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:40:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:40:11 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:40:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cea947ad70084e9470d551b1b736974de4f3633c4fe3d13eef48b5cb1b08b62`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 4.8 MB (4778601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86247e116e9902a618c7b5998f94f6f0117d8ef407b3e6d7437f59f1a1213057`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582e80d779e2f3e9eeb095bd75ba94437c2b08083ea399361835668c478359e1`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-linux`

```console
$ docker pull nats@sha256:464514526a41389cb8eba22f4222d1e44dbfbc570acdb09a32d557c9b9955a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:0008930d6f49b1c3a706f5e751756e25faa913eb0d24a4d1a3cc7111995c2cc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4907907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae8e0e40e5d6a88833150b7613d8c2af98aeeefd0da6dca3100722e12b19571`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:3f7f7d06c5f77e836d502f53de29b2d7a2e80853d13b4d9c75b6bda16857761b in /nats-server 
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:25:42 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:25:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d6d85ead114c982a0357d6002a45433e3f39494cdc0f3cc920d804a45cae35ee`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 4.9 MB (4907400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60865ecae70fb12a59e8579974bc3d65a97b7e84fcd8fe6445d275320879ea5`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:8f0d092d06af2710b06354ee677b81f10f6251a0e8efb0421d8d3f86d1000677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4675550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbbb2f82c0829a2a87cd2ea49c73284638f5861690c6b230951c2b6ca549d06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:65c01e5e1e16c3f3b2d7df9541699c9363f45a0a991482d97d24193d7e1bb29a in /nats-server 
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:49:34 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4db83ef5484b7db61a63b554c60491f4a902ca94cce6b612d3aa32aa92888ec6`  
		Last Modified: Tue, 11 Oct 2022 17:51:01 GMT  
		Size: 4.7 MB (4675041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb93982fc62459387f27a9bde43633a8c758cec8404805cd92613cad4436f4d`  
		Last Modified: Tue, 11 Oct 2022 17:51:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:14a5c2b109967d3adb793cd0ab698648bc10a969bff48575c619a09e6e5ad232
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4664630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7884a65e2ecb2f9f6974f0b17533ba58e8845ff3d4e2f58f62762e8980ddbc5b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:34c532093a5dbef0c1af4a815d6c675cdb6125f12b5f44a7f2b662696b571b90 in /nats-server 
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:58:03 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:58:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:58:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:58:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:03af04ed4c28e4580e7b4c3a5ea1484aae440ba7d2dd4e9a656d77d82dd54b98`  
		Last Modified: Tue, 11 Oct 2022 17:59:30 GMT  
		Size: 4.7 MB (4664122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7148a4d5aff61489f0013cd47ecaf37fcf9a49f79472e42dd389601319be9422`  
		Last Modified: Tue, 11 Oct 2022 17:59:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc4ef43bc1c7b49a3550af75cf1940321e1f5565da18e0f178bde6acd5a36bdd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f962526ab017817241bd3fbee96aff03c8852436cf5bcdc0a58b5e3fe5a09d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:40:23 GMT
COPY file:bc86ca7535653a0512f71a856c462b418bdf59420e8fa4ca2103093ecb5bf96e in /nats-server 
# Tue, 11 Oct 2022 17:40:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:40:24 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:40:26 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:40:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a147f8167144f46b22ee755fdae458d8e5b2fa34cb9a04d5b0393033d9044e08`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 4.5 MB (4497202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e720a4acb8f391823b838f963c0b4de61247a73c4721a3224829968b7b7c0e4c`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver`

```console
$ docker pull nats@sha256:e98b441edfc72745b80116d6ea3b5ebd4e6bb7ef160f06a905150370864838b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:1a1502e9c757eecbb9d40c1795b8aa966bd4c2fab0e557fb56b2db28114f15e1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108344947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821890b5ce167e8d00c7802b4c1b05e6d186a42968f0d0c99b33f0e57d80cbac`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:25:57 GMT
RUN cmd /S /C #(nop) COPY file:ebd16169defae69259e980faeec8d0a781382823c2f6ba62e4124678fe7cd5ff in C:\nats-server.exe 
# Tue, 11 Oct 2022 17:25:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:26:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:26:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f4d5c8d186c8f312a6ae9319e5853518d0fd4d59cf203ad7f21ee572928fb0`  
		Last Modified: Tue, 11 Oct 2022 17:26:54 GMT  
		Size: 5.0 MB (4961254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147afea671cb39b7c3224c41bef90d62a0a4af88ed1d5807480181a613275a6b`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db765622dc1c4a61d8097b7d5c78f046e4111d96704078aa12c8e6af33ef68e5`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a39cb9946d421dff62e99511f125369156430794a031de774db3f5430cfd2ed`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d278ea5c62988b5ad67b51302fdd9bf43d7f72187d576dc0878bac41e162c12`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:e98b441edfc72745b80116d6ea3b5ebd4e6bb7ef160f06a905150370864838b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:1a1502e9c757eecbb9d40c1795b8aa966bd4c2fab0e557fb56b2db28114f15e1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108344947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821890b5ce167e8d00c7802b4c1b05e6d186a42968f0d0c99b33f0e57d80cbac`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:25:57 GMT
RUN cmd /S /C #(nop) COPY file:ebd16169defae69259e980faeec8d0a781382823c2f6ba62e4124678fe7cd5ff in C:\nats-server.exe 
# Tue, 11 Oct 2022 17:25:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:26:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:26:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f4d5c8d186c8f312a6ae9319e5853518d0fd4d59cf203ad7f21ee572928fb0`  
		Last Modified: Tue, 11 Oct 2022 17:26:54 GMT  
		Size: 5.0 MB (4961254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147afea671cb39b7c3224c41bef90d62a0a4af88ed1d5807480181a613275a6b`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db765622dc1c4a61d8097b7d5c78f046e4111d96704078aa12c8e6af33ef68e5`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a39cb9946d421dff62e99511f125369156430794a031de774db3f5430cfd2ed`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d278ea5c62988b5ad67b51302fdd9bf43d7f72187d576dc0878bac41e162c12`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:464514526a41389cb8eba22f4222d1e44dbfbc570acdb09a32d557c9b9955a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:0008930d6f49b1c3a706f5e751756e25faa913eb0d24a4d1a3cc7111995c2cc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4907907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae8e0e40e5d6a88833150b7613d8c2af98aeeefd0da6dca3100722e12b19571`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:3f7f7d06c5f77e836d502f53de29b2d7a2e80853d13b4d9c75b6bda16857761b in /nats-server 
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:25:42 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:25:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d6d85ead114c982a0357d6002a45433e3f39494cdc0f3cc920d804a45cae35ee`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 4.9 MB (4907400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60865ecae70fb12a59e8579974bc3d65a97b7e84fcd8fe6445d275320879ea5`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:8f0d092d06af2710b06354ee677b81f10f6251a0e8efb0421d8d3f86d1000677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4675550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbbb2f82c0829a2a87cd2ea49c73284638f5861690c6b230951c2b6ca549d06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:65c01e5e1e16c3f3b2d7df9541699c9363f45a0a991482d97d24193d7e1bb29a in /nats-server 
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:49:34 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4db83ef5484b7db61a63b554c60491f4a902ca94cce6b612d3aa32aa92888ec6`  
		Last Modified: Tue, 11 Oct 2022 17:51:01 GMT  
		Size: 4.7 MB (4675041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb93982fc62459387f27a9bde43633a8c758cec8404805cd92613cad4436f4d`  
		Last Modified: Tue, 11 Oct 2022 17:51:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:14a5c2b109967d3adb793cd0ab698648bc10a969bff48575c619a09e6e5ad232
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4664630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7884a65e2ecb2f9f6974f0b17533ba58e8845ff3d4e2f58f62762e8980ddbc5b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:34c532093a5dbef0c1af4a815d6c675cdb6125f12b5f44a7f2b662696b571b90 in /nats-server 
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:58:03 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:58:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:58:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:58:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:03af04ed4c28e4580e7b4c3a5ea1484aae440ba7d2dd4e9a656d77d82dd54b98`  
		Last Modified: Tue, 11 Oct 2022 17:59:30 GMT  
		Size: 4.7 MB (4664122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7148a4d5aff61489f0013cd47ecaf37fcf9a49f79472e42dd389601319be9422`  
		Last Modified: Tue, 11 Oct 2022 17:59:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc4ef43bc1c7b49a3550af75cf1940321e1f5565da18e0f178bde6acd5a36bdd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f962526ab017817241bd3fbee96aff03c8852436cf5bcdc0a58b5e3fe5a09d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:40:23 GMT
COPY file:bc86ca7535653a0512f71a856c462b418bdf59420e8fa4ca2103093ecb5bf96e in /nats-server 
# Tue, 11 Oct 2022 17:40:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:40:24 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:40:26 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:40:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a147f8167144f46b22ee755fdae458d8e5b2fa34cb9a04d5b0393033d9044e08`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 4.5 MB (4497202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e720a4acb8f391823b838f963c0b4de61247a73c4721a3224829968b7b7c0e4c`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore`

```console
$ docker pull nats@sha256:fb39a5ed839f11261b832e0dca62197ee21a2ad938138f4cc656a9a52d03d975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:4bddc4dfe1d225cfe86ce8237721abb0c49bd069e8c0bf1ab5c0ba2ec5c6899b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2716818637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ab84e2e207d755fd864c921bfee7744f5f0533ef2a8eb1649486351579db39`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 17:22:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Oct 2022 17:22:08 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:22:09 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:22:10 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.3/nats-server-v2.9.3-windows-amd64.zip
# Tue, 11 Oct 2022 17:22:11 GMT
ENV NATS_SERVER_SHASUM=83b25dad03dee498becb734623ae4d096235b2863be878d5f6d6a32d76f7e85f
# Tue, 11 Oct 2022 17:23:56 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Oct 2022 17:25:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 11 Oct 2022 17:25:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:32 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:25:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c778a0131ae2f1653f1fb703f05998e74365629f70b1a15a0360fb1292182846`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ce79ce85e7eb7d4b12316d81cc8cb3ff2567ee214f4aa0bbf36933fd55891f`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462d88c3de2e572b0d0ee482e3424c3ecb6eae150e8b29e5c8678a3059178bea`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12db35ec0388714c2e4e91a025ad3c010583c420b244c7941d378814da4b414`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61065ad9c7494c241e65c1c1b701828947105c6de39a9a246ef1da83d1967b`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a922f9001668df7166a8c2806eb76dacbac25dfe2a6a6b366546a53ff4a68be`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 350.4 KB (350379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696f9101e75d054c09b2f5086fdb484f298ac859200417dc480c0c95d4db8b79`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 5.3 MB (5290962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063d7a0294a6b35b745dafda4218ac1caccd20c2862af30174e073d25df4240f`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d46f46f65dffc178e8ef8c4d17fc35f23e32db9c2b23028319ab7d51f92b36e`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea87d29a4c3431239148436823825cc53a83211b86daa22eb69df30ff028bde`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245dfbad1025b6c7d6ad15e3336d3a11bd111607ce8db6de8efed6a157cc5872`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:fb39a5ed839f11261b832e0dca62197ee21a2ad938138f4cc656a9a52d03d975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:4bddc4dfe1d225cfe86ce8237721abb0c49bd069e8c0bf1ab5c0ba2ec5c6899b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2716818637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ab84e2e207d755fd864c921bfee7744f5f0533ef2a8eb1649486351579db39`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 17:22:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Oct 2022 17:22:08 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:22:09 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:22:10 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.3/nats-server-v2.9.3-windows-amd64.zip
# Tue, 11 Oct 2022 17:22:11 GMT
ENV NATS_SERVER_SHASUM=83b25dad03dee498becb734623ae4d096235b2863be878d5f6d6a32d76f7e85f
# Tue, 11 Oct 2022 17:23:56 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Oct 2022 17:25:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 11 Oct 2022 17:25:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:32 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:25:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c778a0131ae2f1653f1fb703f05998e74365629f70b1a15a0360fb1292182846`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ce79ce85e7eb7d4b12316d81cc8cb3ff2567ee214f4aa0bbf36933fd55891f`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462d88c3de2e572b0d0ee482e3424c3ecb6eae150e8b29e5c8678a3059178bea`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12db35ec0388714c2e4e91a025ad3c010583c420b244c7941d378814da4b414`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61065ad9c7494c241e65c1c1b701828947105c6de39a9a246ef1da83d1967b`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a922f9001668df7166a8c2806eb76dacbac25dfe2a6a6b366546a53ff4a68be`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 350.4 KB (350379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696f9101e75d054c09b2f5086fdb484f298ac859200417dc480c0c95d4db8b79`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 5.3 MB (5290962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063d7a0294a6b35b745dafda4218ac1caccd20c2862af30174e073d25df4240f`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d46f46f65dffc178e8ef8c4d17fc35f23e32db9c2b23028319ab7d51f92b36e`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea87d29a4c3431239148436823825cc53a83211b86daa22eb69df30ff028bde`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245dfbad1025b6c7d6ad15e3336d3a11bd111607ce8db6de8efed6a157cc5872`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.3`

```console
$ docker pull nats@sha256:9ab5a62adfc3057ad67f8d1930e5aacba1669658bb6f4901f1783e31877d17f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3532; amd64

### `nats:2.9.3` - linux; amd64

```console
$ docker pull nats@sha256:0008930d6f49b1c3a706f5e751756e25faa913eb0d24a4d1a3cc7111995c2cc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4907907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae8e0e40e5d6a88833150b7613d8c2af98aeeefd0da6dca3100722e12b19571`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:3f7f7d06c5f77e836d502f53de29b2d7a2e80853d13b4d9c75b6bda16857761b in /nats-server 
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:25:42 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:25:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d6d85ead114c982a0357d6002a45433e3f39494cdc0f3cc920d804a45cae35ee`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 4.9 MB (4907400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60865ecae70fb12a59e8579974bc3d65a97b7e84fcd8fe6445d275320879ea5`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.3` - linux; arm variant v6

```console
$ docker pull nats@sha256:8f0d092d06af2710b06354ee677b81f10f6251a0e8efb0421d8d3f86d1000677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4675550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbbb2f82c0829a2a87cd2ea49c73284638f5861690c6b230951c2b6ca549d06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:65c01e5e1e16c3f3b2d7df9541699c9363f45a0a991482d97d24193d7e1bb29a in /nats-server 
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:49:34 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4db83ef5484b7db61a63b554c60491f4a902ca94cce6b612d3aa32aa92888ec6`  
		Last Modified: Tue, 11 Oct 2022 17:51:01 GMT  
		Size: 4.7 MB (4675041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb93982fc62459387f27a9bde43633a8c758cec8404805cd92613cad4436f4d`  
		Last Modified: Tue, 11 Oct 2022 17:51:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.3` - linux; arm variant v7

```console
$ docker pull nats@sha256:14a5c2b109967d3adb793cd0ab698648bc10a969bff48575c619a09e6e5ad232
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4664630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7884a65e2ecb2f9f6974f0b17533ba58e8845ff3d4e2f58f62762e8980ddbc5b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:34c532093a5dbef0c1af4a815d6c675cdb6125f12b5f44a7f2b662696b571b90 in /nats-server 
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:58:03 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:58:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:58:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:58:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:03af04ed4c28e4580e7b4c3a5ea1484aae440ba7d2dd4e9a656d77d82dd54b98`  
		Last Modified: Tue, 11 Oct 2022 17:59:30 GMT  
		Size: 4.7 MB (4664122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7148a4d5aff61489f0013cd47ecaf37fcf9a49f79472e42dd389601319be9422`  
		Last Modified: Tue, 11 Oct 2022 17:59:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.3` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc4ef43bc1c7b49a3550af75cf1940321e1f5565da18e0f178bde6acd5a36bdd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f962526ab017817241bd3fbee96aff03c8852436cf5bcdc0a58b5e3fe5a09d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:40:23 GMT
COPY file:bc86ca7535653a0512f71a856c462b418bdf59420e8fa4ca2103093ecb5bf96e in /nats-server 
# Tue, 11 Oct 2022 17:40:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:40:24 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:40:26 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:40:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a147f8167144f46b22ee755fdae458d8e5b2fa34cb9a04d5b0393033d9044e08`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 4.5 MB (4497202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e720a4acb8f391823b838f963c0b4de61247a73c4721a3224829968b7b7c0e4c`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.3` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:1a1502e9c757eecbb9d40c1795b8aa966bd4c2fab0e557fb56b2db28114f15e1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108344947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821890b5ce167e8d00c7802b4c1b05e6d186a42968f0d0c99b33f0e57d80cbac`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:25:57 GMT
RUN cmd /S /C #(nop) COPY file:ebd16169defae69259e980faeec8d0a781382823c2f6ba62e4124678fe7cd5ff in C:\nats-server.exe 
# Tue, 11 Oct 2022 17:25:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:26:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:26:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f4d5c8d186c8f312a6ae9319e5853518d0fd4d59cf203ad7f21ee572928fb0`  
		Last Modified: Tue, 11 Oct 2022 17:26:54 GMT  
		Size: 5.0 MB (4961254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147afea671cb39b7c3224c41bef90d62a0a4af88ed1d5807480181a613275a6b`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db765622dc1c4a61d8097b7d5c78f046e4111d96704078aa12c8e6af33ef68e5`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a39cb9946d421dff62e99511f125369156430794a031de774db3f5430cfd2ed`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d278ea5c62988b5ad67b51302fdd9bf43d7f72187d576dc0878bac41e162c12`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.3-alpine`

```console
$ docker pull nats@sha256:e0615d6d59dad37b1eee587e2e89d2feee1d93537c4f5d68a6550685f0d1ab48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.3-alpine` - linux; amd64

```console
$ docker pull nats@sha256:bf9cae35d4496a6557faaaa46222bc55961ffdea0f6d833968a7fe798581a289
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8000982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d664099656e24efd4de4cdc101c35c38e79e635d0fc49a9a5c79774363ea5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:25:33 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:25:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:25:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:25:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:25:35 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:25:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73aeb9277156392c66e1a873af420eca6482f253b894387e7e80883cbdb4249`  
		Last Modified: Tue, 11 Oct 2022 17:26:08 GMT  
		Size: 5.2 MB (5193929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0307d13e86598b08828290bb6740eb65b29f5fdd9ee5bd8b4c8eed473d84bf56`  
		Last Modified: Tue, 11 Oct 2022 17:26:07 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66055fe8b1856a88ca9c9afb0b9bbf6592e9bacb1b170260b235b8e4bf356de`  
		Last Modified: Tue, 11 Oct 2022 17:26:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.3-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:45edeee49c18b5594b54054229f8783c0db4ea87cbee5afae59c9984301cfd08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7571449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94b7a3987a9935b4c2d3b4242a054e954088cd7a9625b8913193cb56590f841`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:49:20 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:49:22 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:49:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5485032ca7ba2b0f0c8d9b075d5e1e340c36377267e4b3ae41c4e2f7894e91`  
		Last Modified: Tue, 11 Oct 2022 17:50:29 GMT  
		Size: 5.0 MB (4956483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7900c6c1d0cb325952cdd6ae71490a3e0b941af92e71f22de10187efa837d703`  
		Last Modified: Tue, 11 Oct 2022 17:50:28 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b5305ca20b90d113889b94211f4949a2fffcc5faa2c5844fb1091fec4a866`  
		Last Modified: Tue, 11 Oct 2022 17:50:28 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.3-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a5e65b6fa62d1d428e050efe382bbb2005f94464c7818f635f5920bcefb6f106
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7371964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abced2cbd4c41ff1e9075d451f2649984429dc4115edb90e30fe487288cb9155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:57:40 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:57:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:57:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:57:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:57:43 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:57:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:57:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8c3c4b8cb46efedb04498db6fa20cd55763c0418b70a87ca3ec04ae2679149`  
		Last Modified: Tue, 11 Oct 2022 17:58:57 GMT  
		Size: 5.0 MB (4953899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9754b757cf985fb40c2726f1043ee751fdf5c5ceba1b57acd9ac4182d17a14`  
		Last Modified: Tue, 11 Oct 2022 17:58:56 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f195bb3987db93e4b84ec3c227bd96a40f580b48ae1b269d48de5183443d24f3`  
		Last Modified: Tue, 11 Oct 2022 17:58:56 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.3-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb4394d1cb68931c388d303a356838d71e8cdd1c35eb7bd1dd0d145fc2a845d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8492b76ba91c73798af6bc47734164369b9bc2a414e2089d076d6541df9c4f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:40:06 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:40:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:40:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:40:11 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:40:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cea947ad70084e9470d551b1b736974de4f3633c4fe3d13eef48b5cb1b08b62`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 4.8 MB (4778601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86247e116e9902a618c7b5998f94f6f0117d8ef407b3e6d7437f59f1a1213057`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582e80d779e2f3e9eeb095bd75ba94437c2b08083ea399361835668c478359e1`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.3-alpine3.16`

```console
$ docker pull nats@sha256:e0615d6d59dad37b1eee587e2e89d2feee1d93537c4f5d68a6550685f0d1ab48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.3-alpine3.16` - linux; amd64

```console
$ docker pull nats@sha256:bf9cae35d4496a6557faaaa46222bc55961ffdea0f6d833968a7fe798581a289
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8000982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d664099656e24efd4de4cdc101c35c38e79e635d0fc49a9a5c79774363ea5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:25:33 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:25:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:25:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:25:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:25:35 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:25:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73aeb9277156392c66e1a873af420eca6482f253b894387e7e80883cbdb4249`  
		Last Modified: Tue, 11 Oct 2022 17:26:08 GMT  
		Size: 5.2 MB (5193929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0307d13e86598b08828290bb6740eb65b29f5fdd9ee5bd8b4c8eed473d84bf56`  
		Last Modified: Tue, 11 Oct 2022 17:26:07 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66055fe8b1856a88ca9c9afb0b9bbf6592e9bacb1b170260b235b8e4bf356de`  
		Last Modified: Tue, 11 Oct 2022 17:26:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.3-alpine3.16` - linux; arm variant v6

```console
$ docker pull nats@sha256:45edeee49c18b5594b54054229f8783c0db4ea87cbee5afae59c9984301cfd08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7571449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94b7a3987a9935b4c2d3b4242a054e954088cd7a9625b8913193cb56590f841`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:49:20 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:49:22 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:49:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5485032ca7ba2b0f0c8d9b075d5e1e340c36377267e4b3ae41c4e2f7894e91`  
		Last Modified: Tue, 11 Oct 2022 17:50:29 GMT  
		Size: 5.0 MB (4956483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7900c6c1d0cb325952cdd6ae71490a3e0b941af92e71f22de10187efa837d703`  
		Last Modified: Tue, 11 Oct 2022 17:50:28 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b5305ca20b90d113889b94211f4949a2fffcc5faa2c5844fb1091fec4a866`  
		Last Modified: Tue, 11 Oct 2022 17:50:28 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.3-alpine3.16` - linux; arm variant v7

```console
$ docker pull nats@sha256:a5e65b6fa62d1d428e050efe382bbb2005f94464c7818f635f5920bcefb6f106
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7371964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abced2cbd4c41ff1e9075d451f2649984429dc4115edb90e30fe487288cb9155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:57:40 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:57:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:57:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:57:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:57:43 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:57:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:57:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8c3c4b8cb46efedb04498db6fa20cd55763c0418b70a87ca3ec04ae2679149`  
		Last Modified: Tue, 11 Oct 2022 17:58:57 GMT  
		Size: 5.0 MB (4953899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9754b757cf985fb40c2726f1043ee751fdf5c5ceba1b57acd9ac4182d17a14`  
		Last Modified: Tue, 11 Oct 2022 17:58:56 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f195bb3987db93e4b84ec3c227bd96a40f580b48ae1b269d48de5183443d24f3`  
		Last Modified: Tue, 11 Oct 2022 17:58:56 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.3-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb4394d1cb68931c388d303a356838d71e8cdd1c35eb7bd1dd0d145fc2a845d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8492b76ba91c73798af6bc47734164369b9bc2a414e2089d076d6541df9c4f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:40:06 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:40:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:40:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:40:11 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:40:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cea947ad70084e9470d551b1b736974de4f3633c4fe3d13eef48b5cb1b08b62`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 4.8 MB (4778601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86247e116e9902a618c7b5998f94f6f0117d8ef407b3e6d7437f59f1a1213057`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582e80d779e2f3e9eeb095bd75ba94437c2b08083ea399361835668c478359e1`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.3-linux`

```console
$ docker pull nats@sha256:464514526a41389cb8eba22f4222d1e44dbfbc570acdb09a32d557c9b9955a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.3-linux` - linux; amd64

```console
$ docker pull nats@sha256:0008930d6f49b1c3a706f5e751756e25faa913eb0d24a4d1a3cc7111995c2cc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4907907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae8e0e40e5d6a88833150b7613d8c2af98aeeefd0da6dca3100722e12b19571`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:3f7f7d06c5f77e836d502f53de29b2d7a2e80853d13b4d9c75b6bda16857761b in /nats-server 
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:25:42 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:25:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d6d85ead114c982a0357d6002a45433e3f39494cdc0f3cc920d804a45cae35ee`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 4.9 MB (4907400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60865ecae70fb12a59e8579974bc3d65a97b7e84fcd8fe6445d275320879ea5`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.3-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:8f0d092d06af2710b06354ee677b81f10f6251a0e8efb0421d8d3f86d1000677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4675550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbbb2f82c0829a2a87cd2ea49c73284638f5861690c6b230951c2b6ca549d06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:65c01e5e1e16c3f3b2d7df9541699c9363f45a0a991482d97d24193d7e1bb29a in /nats-server 
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:49:34 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4db83ef5484b7db61a63b554c60491f4a902ca94cce6b612d3aa32aa92888ec6`  
		Last Modified: Tue, 11 Oct 2022 17:51:01 GMT  
		Size: 4.7 MB (4675041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb93982fc62459387f27a9bde43633a8c758cec8404805cd92613cad4436f4d`  
		Last Modified: Tue, 11 Oct 2022 17:51:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.3-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:14a5c2b109967d3adb793cd0ab698648bc10a969bff48575c619a09e6e5ad232
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4664630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7884a65e2ecb2f9f6974f0b17533ba58e8845ff3d4e2f58f62762e8980ddbc5b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:34c532093a5dbef0c1af4a815d6c675cdb6125f12b5f44a7f2b662696b571b90 in /nats-server 
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:58:03 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:58:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:58:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:58:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:03af04ed4c28e4580e7b4c3a5ea1484aae440ba7d2dd4e9a656d77d82dd54b98`  
		Last Modified: Tue, 11 Oct 2022 17:59:30 GMT  
		Size: 4.7 MB (4664122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7148a4d5aff61489f0013cd47ecaf37fcf9a49f79472e42dd389601319be9422`  
		Last Modified: Tue, 11 Oct 2022 17:59:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.3-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc4ef43bc1c7b49a3550af75cf1940321e1f5565da18e0f178bde6acd5a36bdd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f962526ab017817241bd3fbee96aff03c8852436cf5bcdc0a58b5e3fe5a09d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:40:23 GMT
COPY file:bc86ca7535653a0512f71a856c462b418bdf59420e8fa4ca2103093ecb5bf96e in /nats-server 
# Tue, 11 Oct 2022 17:40:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:40:24 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:40:26 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:40:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a147f8167144f46b22ee755fdae458d8e5b2fa34cb9a04d5b0393033d9044e08`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 4.5 MB (4497202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e720a4acb8f391823b838f963c0b4de61247a73c4721a3224829968b7b7c0e4c`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.3-nanoserver`

```console
$ docker pull nats@sha256:e98b441edfc72745b80116d6ea3b5ebd4e6bb7ef160f06a905150370864838b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2.9.3-nanoserver` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:1a1502e9c757eecbb9d40c1795b8aa966bd4c2fab0e557fb56b2db28114f15e1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108344947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821890b5ce167e8d00c7802b4c1b05e6d186a42968f0d0c99b33f0e57d80cbac`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:25:57 GMT
RUN cmd /S /C #(nop) COPY file:ebd16169defae69259e980faeec8d0a781382823c2f6ba62e4124678fe7cd5ff in C:\nats-server.exe 
# Tue, 11 Oct 2022 17:25:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:26:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:26:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f4d5c8d186c8f312a6ae9319e5853518d0fd4d59cf203ad7f21ee572928fb0`  
		Last Modified: Tue, 11 Oct 2022 17:26:54 GMT  
		Size: 5.0 MB (4961254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147afea671cb39b7c3224c41bef90d62a0a4af88ed1d5807480181a613275a6b`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db765622dc1c4a61d8097b7d5c78f046e4111d96704078aa12c8e6af33ef68e5`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a39cb9946d421dff62e99511f125369156430794a031de774db3f5430cfd2ed`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d278ea5c62988b5ad67b51302fdd9bf43d7f72187d576dc0878bac41e162c12`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.3-nanoserver-1809`

```console
$ docker pull nats@sha256:e98b441edfc72745b80116d6ea3b5ebd4e6bb7ef160f06a905150370864838b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2.9.3-nanoserver-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:1a1502e9c757eecbb9d40c1795b8aa966bd4c2fab0e557fb56b2db28114f15e1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108344947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821890b5ce167e8d00c7802b4c1b05e6d186a42968f0d0c99b33f0e57d80cbac`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:25:57 GMT
RUN cmd /S /C #(nop) COPY file:ebd16169defae69259e980faeec8d0a781382823c2f6ba62e4124678fe7cd5ff in C:\nats-server.exe 
# Tue, 11 Oct 2022 17:25:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:26:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:26:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f4d5c8d186c8f312a6ae9319e5853518d0fd4d59cf203ad7f21ee572928fb0`  
		Last Modified: Tue, 11 Oct 2022 17:26:54 GMT  
		Size: 5.0 MB (4961254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147afea671cb39b7c3224c41bef90d62a0a4af88ed1d5807480181a613275a6b`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db765622dc1c4a61d8097b7d5c78f046e4111d96704078aa12c8e6af33ef68e5`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a39cb9946d421dff62e99511f125369156430794a031de774db3f5430cfd2ed`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d278ea5c62988b5ad67b51302fdd9bf43d7f72187d576dc0878bac41e162c12`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.3-scratch`

```console
$ docker pull nats@sha256:464514526a41389cb8eba22f4222d1e44dbfbc570acdb09a32d557c9b9955a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.3-scratch` - linux; amd64

```console
$ docker pull nats@sha256:0008930d6f49b1c3a706f5e751756e25faa913eb0d24a4d1a3cc7111995c2cc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4907907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae8e0e40e5d6a88833150b7613d8c2af98aeeefd0da6dca3100722e12b19571`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:3f7f7d06c5f77e836d502f53de29b2d7a2e80853d13b4d9c75b6bda16857761b in /nats-server 
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:25:42 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:25:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d6d85ead114c982a0357d6002a45433e3f39494cdc0f3cc920d804a45cae35ee`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 4.9 MB (4907400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60865ecae70fb12a59e8579974bc3d65a97b7e84fcd8fe6445d275320879ea5`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.3-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:8f0d092d06af2710b06354ee677b81f10f6251a0e8efb0421d8d3f86d1000677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4675550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbbb2f82c0829a2a87cd2ea49c73284638f5861690c6b230951c2b6ca549d06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:65c01e5e1e16c3f3b2d7df9541699c9363f45a0a991482d97d24193d7e1bb29a in /nats-server 
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:49:34 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4db83ef5484b7db61a63b554c60491f4a902ca94cce6b612d3aa32aa92888ec6`  
		Last Modified: Tue, 11 Oct 2022 17:51:01 GMT  
		Size: 4.7 MB (4675041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb93982fc62459387f27a9bde43633a8c758cec8404805cd92613cad4436f4d`  
		Last Modified: Tue, 11 Oct 2022 17:51:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.3-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:14a5c2b109967d3adb793cd0ab698648bc10a969bff48575c619a09e6e5ad232
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4664630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7884a65e2ecb2f9f6974f0b17533ba58e8845ff3d4e2f58f62762e8980ddbc5b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:34c532093a5dbef0c1af4a815d6c675cdb6125f12b5f44a7f2b662696b571b90 in /nats-server 
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:58:03 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:58:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:58:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:58:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:03af04ed4c28e4580e7b4c3a5ea1484aae440ba7d2dd4e9a656d77d82dd54b98`  
		Last Modified: Tue, 11 Oct 2022 17:59:30 GMT  
		Size: 4.7 MB (4664122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7148a4d5aff61489f0013cd47ecaf37fcf9a49f79472e42dd389601319be9422`  
		Last Modified: Tue, 11 Oct 2022 17:59:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.3-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc4ef43bc1c7b49a3550af75cf1940321e1f5565da18e0f178bde6acd5a36bdd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f962526ab017817241bd3fbee96aff03c8852436cf5bcdc0a58b5e3fe5a09d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:40:23 GMT
COPY file:bc86ca7535653a0512f71a856c462b418bdf59420e8fa4ca2103093ecb5bf96e in /nats-server 
# Tue, 11 Oct 2022 17:40:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:40:24 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:40:26 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:40:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a147f8167144f46b22ee755fdae458d8e5b2fa34cb9a04d5b0393033d9044e08`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 4.5 MB (4497202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e720a4acb8f391823b838f963c0b4de61247a73c4721a3224829968b7b7c0e4c`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.3-windowsservercore`

```console
$ docker pull nats@sha256:fb39a5ed839f11261b832e0dca62197ee21a2ad938138f4cc656a9a52d03d975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2.9.3-windowsservercore` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:4bddc4dfe1d225cfe86ce8237721abb0c49bd069e8c0bf1ab5c0ba2ec5c6899b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2716818637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ab84e2e207d755fd864c921bfee7744f5f0533ef2a8eb1649486351579db39`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 17:22:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Oct 2022 17:22:08 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:22:09 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:22:10 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.3/nats-server-v2.9.3-windows-amd64.zip
# Tue, 11 Oct 2022 17:22:11 GMT
ENV NATS_SERVER_SHASUM=83b25dad03dee498becb734623ae4d096235b2863be878d5f6d6a32d76f7e85f
# Tue, 11 Oct 2022 17:23:56 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Oct 2022 17:25:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 11 Oct 2022 17:25:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:32 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:25:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c778a0131ae2f1653f1fb703f05998e74365629f70b1a15a0360fb1292182846`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ce79ce85e7eb7d4b12316d81cc8cb3ff2567ee214f4aa0bbf36933fd55891f`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462d88c3de2e572b0d0ee482e3424c3ecb6eae150e8b29e5c8678a3059178bea`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12db35ec0388714c2e4e91a025ad3c010583c420b244c7941d378814da4b414`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61065ad9c7494c241e65c1c1b701828947105c6de39a9a246ef1da83d1967b`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a922f9001668df7166a8c2806eb76dacbac25dfe2a6a6b366546a53ff4a68be`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 350.4 KB (350379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696f9101e75d054c09b2f5086fdb484f298ac859200417dc480c0c95d4db8b79`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 5.3 MB (5290962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063d7a0294a6b35b745dafda4218ac1caccd20c2862af30174e073d25df4240f`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d46f46f65dffc178e8ef8c4d17fc35f23e32db9c2b23028319ab7d51f92b36e`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea87d29a4c3431239148436823825cc53a83211b86daa22eb69df30ff028bde`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245dfbad1025b6c7d6ad15e3336d3a11bd111607ce8db6de8efed6a157cc5872`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.3-windowsservercore-1809`

```console
$ docker pull nats@sha256:fb39a5ed839f11261b832e0dca62197ee21a2ad938138f4cc656a9a52d03d975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2.9.3-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:4bddc4dfe1d225cfe86ce8237721abb0c49bd069e8c0bf1ab5c0ba2ec5c6899b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2716818637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ab84e2e207d755fd864c921bfee7744f5f0533ef2a8eb1649486351579db39`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 17:22:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Oct 2022 17:22:08 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:22:09 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:22:10 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.3/nats-server-v2.9.3-windows-amd64.zip
# Tue, 11 Oct 2022 17:22:11 GMT
ENV NATS_SERVER_SHASUM=83b25dad03dee498becb734623ae4d096235b2863be878d5f6d6a32d76f7e85f
# Tue, 11 Oct 2022 17:23:56 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Oct 2022 17:25:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 11 Oct 2022 17:25:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:32 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:25:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c778a0131ae2f1653f1fb703f05998e74365629f70b1a15a0360fb1292182846`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ce79ce85e7eb7d4b12316d81cc8cb3ff2567ee214f4aa0bbf36933fd55891f`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462d88c3de2e572b0d0ee482e3424c3ecb6eae150e8b29e5c8678a3059178bea`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12db35ec0388714c2e4e91a025ad3c010583c420b244c7941d378814da4b414`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61065ad9c7494c241e65c1c1b701828947105c6de39a9a246ef1da83d1967b`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a922f9001668df7166a8c2806eb76dacbac25dfe2a6a6b366546a53ff4a68be`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 350.4 KB (350379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696f9101e75d054c09b2f5086fdb484f298ac859200417dc480c0c95d4db8b79`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 5.3 MB (5290962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063d7a0294a6b35b745dafda4218ac1caccd20c2862af30174e073d25df4240f`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d46f46f65dffc178e8ef8c4d17fc35f23e32db9c2b23028319ab7d51f92b36e`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea87d29a4c3431239148436823825cc53a83211b86daa22eb69df30ff028bde`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245dfbad1025b6c7d6ad15e3336d3a11bd111607ce8db6de8efed6a157cc5872`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:e0615d6d59dad37b1eee587e2e89d2feee1d93537c4f5d68a6550685f0d1ab48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:bf9cae35d4496a6557faaaa46222bc55961ffdea0f6d833968a7fe798581a289
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8000982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d664099656e24efd4de4cdc101c35c38e79e635d0fc49a9a5c79774363ea5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:25:33 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:25:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:25:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:25:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:25:35 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:25:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73aeb9277156392c66e1a873af420eca6482f253b894387e7e80883cbdb4249`  
		Last Modified: Tue, 11 Oct 2022 17:26:08 GMT  
		Size: 5.2 MB (5193929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0307d13e86598b08828290bb6740eb65b29f5fdd9ee5bd8b4c8eed473d84bf56`  
		Last Modified: Tue, 11 Oct 2022 17:26:07 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66055fe8b1856a88ca9c9afb0b9bbf6592e9bacb1b170260b235b8e4bf356de`  
		Last Modified: Tue, 11 Oct 2022 17:26:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:45edeee49c18b5594b54054229f8783c0db4ea87cbee5afae59c9984301cfd08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7571449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94b7a3987a9935b4c2d3b4242a054e954088cd7a9625b8913193cb56590f841`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:49:20 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:49:22 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:49:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5485032ca7ba2b0f0c8d9b075d5e1e340c36377267e4b3ae41c4e2f7894e91`  
		Last Modified: Tue, 11 Oct 2022 17:50:29 GMT  
		Size: 5.0 MB (4956483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7900c6c1d0cb325952cdd6ae71490a3e0b941af92e71f22de10187efa837d703`  
		Last Modified: Tue, 11 Oct 2022 17:50:28 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b5305ca20b90d113889b94211f4949a2fffcc5faa2c5844fb1091fec4a866`  
		Last Modified: Tue, 11 Oct 2022 17:50:28 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a5e65b6fa62d1d428e050efe382bbb2005f94464c7818f635f5920bcefb6f106
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7371964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abced2cbd4c41ff1e9075d451f2649984429dc4115edb90e30fe487288cb9155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:57:40 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:57:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:57:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:57:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:57:43 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:57:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:57:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8c3c4b8cb46efedb04498db6fa20cd55763c0418b70a87ca3ec04ae2679149`  
		Last Modified: Tue, 11 Oct 2022 17:58:57 GMT  
		Size: 5.0 MB (4953899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9754b757cf985fb40c2726f1043ee751fdf5c5ceba1b57acd9ac4182d17a14`  
		Last Modified: Tue, 11 Oct 2022 17:58:56 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f195bb3987db93e4b84ec3c227bd96a40f580b48ae1b269d48de5183443d24f3`  
		Last Modified: Tue, 11 Oct 2022 17:58:56 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb4394d1cb68931c388d303a356838d71e8cdd1c35eb7bd1dd0d145fc2a845d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8492b76ba91c73798af6bc47734164369b9bc2a414e2089d076d6541df9c4f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:40:06 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:40:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:40:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:40:11 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:40:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cea947ad70084e9470d551b1b736974de4f3633c4fe3d13eef48b5cb1b08b62`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 4.8 MB (4778601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86247e116e9902a618c7b5998f94f6f0117d8ef407b3e6d7437f59f1a1213057`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582e80d779e2f3e9eeb095bd75ba94437c2b08083ea399361835668c478359e1`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.16`

```console
$ docker pull nats@sha256:e0615d6d59dad37b1eee587e2e89d2feee1d93537c4f5d68a6550685f0d1ab48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.16` - linux; amd64

```console
$ docker pull nats@sha256:bf9cae35d4496a6557faaaa46222bc55961ffdea0f6d833968a7fe798581a289
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8000982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d664099656e24efd4de4cdc101c35c38e79e635d0fc49a9a5c79774363ea5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:25:33 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:25:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:25:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:25:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:25:35 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:25:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73aeb9277156392c66e1a873af420eca6482f253b894387e7e80883cbdb4249`  
		Last Modified: Tue, 11 Oct 2022 17:26:08 GMT  
		Size: 5.2 MB (5193929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0307d13e86598b08828290bb6740eb65b29f5fdd9ee5bd8b4c8eed473d84bf56`  
		Last Modified: Tue, 11 Oct 2022 17:26:07 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66055fe8b1856a88ca9c9afb0b9bbf6592e9bacb1b170260b235b8e4bf356de`  
		Last Modified: Tue, 11 Oct 2022 17:26:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.16` - linux; arm variant v6

```console
$ docker pull nats@sha256:45edeee49c18b5594b54054229f8783c0db4ea87cbee5afae59c9984301cfd08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7571449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94b7a3987a9935b4c2d3b4242a054e954088cd7a9625b8913193cb56590f841`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:49:20 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:49:22 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:49:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5485032ca7ba2b0f0c8d9b075d5e1e340c36377267e4b3ae41c4e2f7894e91`  
		Last Modified: Tue, 11 Oct 2022 17:50:29 GMT  
		Size: 5.0 MB (4956483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7900c6c1d0cb325952cdd6ae71490a3e0b941af92e71f22de10187efa837d703`  
		Last Modified: Tue, 11 Oct 2022 17:50:28 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b5305ca20b90d113889b94211f4949a2fffcc5faa2c5844fb1091fec4a866`  
		Last Modified: Tue, 11 Oct 2022 17:50:28 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.16` - linux; arm variant v7

```console
$ docker pull nats@sha256:a5e65b6fa62d1d428e050efe382bbb2005f94464c7818f635f5920bcefb6f106
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7371964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abced2cbd4c41ff1e9075d451f2649984429dc4115edb90e30fe487288cb9155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:57:40 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:57:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:57:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:57:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:57:43 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:57:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:57:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8c3c4b8cb46efedb04498db6fa20cd55763c0418b70a87ca3ec04ae2679149`  
		Last Modified: Tue, 11 Oct 2022 17:58:57 GMT  
		Size: 5.0 MB (4953899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9754b757cf985fb40c2726f1043ee751fdf5c5ceba1b57acd9ac4182d17a14`  
		Last Modified: Tue, 11 Oct 2022 17:58:56 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f195bb3987db93e4b84ec3c227bd96a40f580b48ae1b269d48de5183443d24f3`  
		Last Modified: Tue, 11 Oct 2022 17:58:56 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.16` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb4394d1cb68931c388d303a356838d71e8cdd1c35eb7bd1dd0d145fc2a845d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8492b76ba91c73798af6bc47734164369b9bc2a414e2089d076d6541df9c4f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 17:40:06 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:40:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='8d156c27e2702f4e43fcad0ad28f7e6ccf490777b8f78c25aba45125d541dd5b' ;; 		armhf) natsArch='arm6'; sha256='74204a66f8c76637d0e70d91f9ff22e35e4a55d6204d71820ba22a945a782b73' ;; 		armv7) natsArch='arm7'; sha256='280c4de193b2759f8a9c4bd2633b481fdbbfc5b45bda87d7926731e6bfc1ec31' ;; 		x86_64) natsArch='amd64'; sha256='398aa61a5dd74d1bc14a30573a1eb9114e3a92621c350f93baaf453696ec3526' ;; 		x86) natsArch='386'; sha256='297c21a9024f408a63c7b5b7e040e2256eff4f5fd34c7297727a82e223786812' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 11 Oct 2022 17:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 11 Oct 2022 17:40:11 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 11 Oct 2022 17:40:11 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 17:40:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cea947ad70084e9470d551b1b736974de4f3633c4fe3d13eef48b5cb1b08b62`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 4.8 MB (4778601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86247e116e9902a618c7b5998f94f6f0117d8ef407b3e6d7437f59f1a1213057`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582e80d779e2f3e9eeb095bd75ba94437c2b08083ea399361835668c478359e1`  
		Last Modified: Tue, 11 Oct 2022 17:41:14 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:9ab5a62adfc3057ad67f8d1930e5aacba1669658bb6f4901f1783e31877d17f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3532; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:0008930d6f49b1c3a706f5e751756e25faa913eb0d24a4d1a3cc7111995c2cc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4907907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae8e0e40e5d6a88833150b7613d8c2af98aeeefd0da6dca3100722e12b19571`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:3f7f7d06c5f77e836d502f53de29b2d7a2e80853d13b4d9c75b6bda16857761b in /nats-server 
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:25:42 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:25:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d6d85ead114c982a0357d6002a45433e3f39494cdc0f3cc920d804a45cae35ee`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 4.9 MB (4907400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60865ecae70fb12a59e8579974bc3d65a97b7e84fcd8fe6445d275320879ea5`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:8f0d092d06af2710b06354ee677b81f10f6251a0e8efb0421d8d3f86d1000677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4675550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbbb2f82c0829a2a87cd2ea49c73284638f5861690c6b230951c2b6ca549d06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:65c01e5e1e16c3f3b2d7df9541699c9363f45a0a991482d97d24193d7e1bb29a in /nats-server 
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:49:34 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4db83ef5484b7db61a63b554c60491f4a902ca94cce6b612d3aa32aa92888ec6`  
		Last Modified: Tue, 11 Oct 2022 17:51:01 GMT  
		Size: 4.7 MB (4675041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb93982fc62459387f27a9bde43633a8c758cec8404805cd92613cad4436f4d`  
		Last Modified: Tue, 11 Oct 2022 17:51:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:14a5c2b109967d3adb793cd0ab698648bc10a969bff48575c619a09e6e5ad232
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4664630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7884a65e2ecb2f9f6974f0b17533ba58e8845ff3d4e2f58f62762e8980ddbc5b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:34c532093a5dbef0c1af4a815d6c675cdb6125f12b5f44a7f2b662696b571b90 in /nats-server 
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:58:03 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:58:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:58:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:58:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:03af04ed4c28e4580e7b4c3a5ea1484aae440ba7d2dd4e9a656d77d82dd54b98`  
		Last Modified: Tue, 11 Oct 2022 17:59:30 GMT  
		Size: 4.7 MB (4664122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7148a4d5aff61489f0013cd47ecaf37fcf9a49f79472e42dd389601319be9422`  
		Last Modified: Tue, 11 Oct 2022 17:59:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc4ef43bc1c7b49a3550af75cf1940321e1f5565da18e0f178bde6acd5a36bdd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f962526ab017817241bd3fbee96aff03c8852436cf5bcdc0a58b5e3fe5a09d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:40:23 GMT
COPY file:bc86ca7535653a0512f71a856c462b418bdf59420e8fa4ca2103093ecb5bf96e in /nats-server 
# Tue, 11 Oct 2022 17:40:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:40:24 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:40:26 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:40:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a147f8167144f46b22ee755fdae458d8e5b2fa34cb9a04d5b0393033d9044e08`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 4.5 MB (4497202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e720a4acb8f391823b838f963c0b4de61247a73c4721a3224829968b7b7c0e4c`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:1a1502e9c757eecbb9d40c1795b8aa966bd4c2fab0e557fb56b2db28114f15e1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108344947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821890b5ce167e8d00c7802b4c1b05e6d186a42968f0d0c99b33f0e57d80cbac`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:25:57 GMT
RUN cmd /S /C #(nop) COPY file:ebd16169defae69259e980faeec8d0a781382823c2f6ba62e4124678fe7cd5ff in C:\nats-server.exe 
# Tue, 11 Oct 2022 17:25:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:26:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:26:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f4d5c8d186c8f312a6ae9319e5853518d0fd4d59cf203ad7f21ee572928fb0`  
		Last Modified: Tue, 11 Oct 2022 17:26:54 GMT  
		Size: 5.0 MB (4961254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147afea671cb39b7c3224c41bef90d62a0a4af88ed1d5807480181a613275a6b`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db765622dc1c4a61d8097b7d5c78f046e4111d96704078aa12c8e6af33ef68e5`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a39cb9946d421dff62e99511f125369156430794a031de774db3f5430cfd2ed`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d278ea5c62988b5ad67b51302fdd9bf43d7f72187d576dc0878bac41e162c12`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:464514526a41389cb8eba22f4222d1e44dbfbc570acdb09a32d557c9b9955a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:0008930d6f49b1c3a706f5e751756e25faa913eb0d24a4d1a3cc7111995c2cc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4907907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae8e0e40e5d6a88833150b7613d8c2af98aeeefd0da6dca3100722e12b19571`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:3f7f7d06c5f77e836d502f53de29b2d7a2e80853d13b4d9c75b6bda16857761b in /nats-server 
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:25:42 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:25:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d6d85ead114c982a0357d6002a45433e3f39494cdc0f3cc920d804a45cae35ee`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 4.9 MB (4907400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60865ecae70fb12a59e8579974bc3d65a97b7e84fcd8fe6445d275320879ea5`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:8f0d092d06af2710b06354ee677b81f10f6251a0e8efb0421d8d3f86d1000677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4675550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbbb2f82c0829a2a87cd2ea49c73284638f5861690c6b230951c2b6ca549d06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:65c01e5e1e16c3f3b2d7df9541699c9363f45a0a991482d97d24193d7e1bb29a in /nats-server 
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:49:34 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4db83ef5484b7db61a63b554c60491f4a902ca94cce6b612d3aa32aa92888ec6`  
		Last Modified: Tue, 11 Oct 2022 17:51:01 GMT  
		Size: 4.7 MB (4675041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb93982fc62459387f27a9bde43633a8c758cec8404805cd92613cad4436f4d`  
		Last Modified: Tue, 11 Oct 2022 17:51:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:14a5c2b109967d3adb793cd0ab698648bc10a969bff48575c619a09e6e5ad232
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4664630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7884a65e2ecb2f9f6974f0b17533ba58e8845ff3d4e2f58f62762e8980ddbc5b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:34c532093a5dbef0c1af4a815d6c675cdb6125f12b5f44a7f2b662696b571b90 in /nats-server 
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:58:03 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:58:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:58:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:58:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:03af04ed4c28e4580e7b4c3a5ea1484aae440ba7d2dd4e9a656d77d82dd54b98`  
		Last Modified: Tue, 11 Oct 2022 17:59:30 GMT  
		Size: 4.7 MB (4664122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7148a4d5aff61489f0013cd47ecaf37fcf9a49f79472e42dd389601319be9422`  
		Last Modified: Tue, 11 Oct 2022 17:59:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc4ef43bc1c7b49a3550af75cf1940321e1f5565da18e0f178bde6acd5a36bdd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f962526ab017817241bd3fbee96aff03c8852436cf5bcdc0a58b5e3fe5a09d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:40:23 GMT
COPY file:bc86ca7535653a0512f71a856c462b418bdf59420e8fa4ca2103093ecb5bf96e in /nats-server 
# Tue, 11 Oct 2022 17:40:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:40:24 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:40:26 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:40:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a147f8167144f46b22ee755fdae458d8e5b2fa34cb9a04d5b0393033d9044e08`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 4.5 MB (4497202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e720a4acb8f391823b838f963c0b4de61247a73c4721a3224829968b7b7c0e4c`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:e98b441edfc72745b80116d6ea3b5ebd4e6bb7ef160f06a905150370864838b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:nanoserver` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:1a1502e9c757eecbb9d40c1795b8aa966bd4c2fab0e557fb56b2db28114f15e1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108344947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821890b5ce167e8d00c7802b4c1b05e6d186a42968f0d0c99b33f0e57d80cbac`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:25:57 GMT
RUN cmd /S /C #(nop) COPY file:ebd16169defae69259e980faeec8d0a781382823c2f6ba62e4124678fe7cd5ff in C:\nats-server.exe 
# Tue, 11 Oct 2022 17:25:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:26:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:26:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f4d5c8d186c8f312a6ae9319e5853518d0fd4d59cf203ad7f21ee572928fb0`  
		Last Modified: Tue, 11 Oct 2022 17:26:54 GMT  
		Size: 5.0 MB (4961254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147afea671cb39b7c3224c41bef90d62a0a4af88ed1d5807480181a613275a6b`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db765622dc1c4a61d8097b7d5c78f046e4111d96704078aa12c8e6af33ef68e5`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a39cb9946d421dff62e99511f125369156430794a031de774db3f5430cfd2ed`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d278ea5c62988b5ad67b51302fdd9bf43d7f72187d576dc0878bac41e162c12`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:e98b441edfc72745b80116d6ea3b5ebd4e6bb7ef160f06a905150370864838b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:1a1502e9c757eecbb9d40c1795b8aa966bd4c2fab0e557fb56b2db28114f15e1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108344947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821890b5ce167e8d00c7802b4c1b05e6d186a42968f0d0c99b33f0e57d80cbac`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:25:57 GMT
RUN cmd /S /C #(nop) COPY file:ebd16169defae69259e980faeec8d0a781382823c2f6ba62e4124678fe7cd5ff in C:\nats-server.exe 
# Tue, 11 Oct 2022 17:25:58 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:26:00 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:26:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f4d5c8d186c8f312a6ae9319e5853518d0fd4d59cf203ad7f21ee572928fb0`  
		Last Modified: Tue, 11 Oct 2022 17:26:54 GMT  
		Size: 5.0 MB (4961254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147afea671cb39b7c3224c41bef90d62a0a4af88ed1d5807480181a613275a6b`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db765622dc1c4a61d8097b7d5c78f046e4111d96704078aa12c8e6af33ef68e5`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a39cb9946d421dff62e99511f125369156430794a031de774db3f5430cfd2ed`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d278ea5c62988b5ad67b51302fdd9bf43d7f72187d576dc0878bac41e162c12`  
		Last Modified: Tue, 11 Oct 2022 17:26:53 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:464514526a41389cb8eba22f4222d1e44dbfbc570acdb09a32d557c9b9955a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:0008930d6f49b1c3a706f5e751756e25faa913eb0d24a4d1a3cc7111995c2cc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4907907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae8e0e40e5d6a88833150b7613d8c2af98aeeefd0da6dca3100722e12b19571`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:3f7f7d06c5f77e836d502f53de29b2d7a2e80853d13b4d9c75b6bda16857761b in /nats-server 
# Tue, 11 Oct 2022 17:25:41 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:25:42 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:25:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:25:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d6d85ead114c982a0357d6002a45433e3f39494cdc0f3cc920d804a45cae35ee`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 4.9 MB (4907400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60865ecae70fb12a59e8579974bc3d65a97b7e84fcd8fe6445d275320879ea5`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:8f0d092d06af2710b06354ee677b81f10f6251a0e8efb0421d8d3f86d1000677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4675550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbbb2f82c0829a2a87cd2ea49c73284638f5861690c6b230951c2b6ca549d06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:65c01e5e1e16c3f3b2d7df9541699c9363f45a0a991482d97d24193d7e1bb29a in /nats-server 
# Tue, 11 Oct 2022 17:49:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:49:34 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:49:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:49:34 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:49:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4db83ef5484b7db61a63b554c60491f4a902ca94cce6b612d3aa32aa92888ec6`  
		Last Modified: Tue, 11 Oct 2022 17:51:01 GMT  
		Size: 4.7 MB (4675041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb93982fc62459387f27a9bde43633a8c758cec8404805cd92613cad4436f4d`  
		Last Modified: Tue, 11 Oct 2022 17:51:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:14a5c2b109967d3adb793cd0ab698648bc10a969bff48575c619a09e6e5ad232
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4664630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7884a65e2ecb2f9f6974f0b17533ba58e8845ff3d4e2f58f62762e8980ddbc5b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:34c532093a5dbef0c1af4a815d6c675cdb6125f12b5f44a7f2b662696b571b90 in /nats-server 
# Tue, 11 Oct 2022 17:58:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:58:03 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:58:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:58:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:58:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:03af04ed4c28e4580e7b4c3a5ea1484aae440ba7d2dd4e9a656d77d82dd54b98`  
		Last Modified: Tue, 11 Oct 2022 17:59:30 GMT  
		Size: 4.7 MB (4664122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7148a4d5aff61489f0013cd47ecaf37fcf9a49f79472e42dd389601319be9422`  
		Last Modified: Tue, 11 Oct 2022 17:59:29 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc4ef43bc1c7b49a3550af75cf1940321e1f5565da18e0f178bde6acd5a36bdd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f962526ab017817241bd3fbee96aff03c8852436cf5bcdc0a58b5e3fe5a09d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 11 Oct 2022 17:40:23 GMT
COPY file:bc86ca7535653a0512f71a856c462b418bdf59420e8fa4ca2103093ecb5bf96e in /nats-server 
# Tue, 11 Oct 2022 17:40:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 11 Oct 2022 17:40:24 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:40:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 11 Oct 2022 17:40:26 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 11 Oct 2022 17:40:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a147f8167144f46b22ee755fdae458d8e5b2fa34cb9a04d5b0393033d9044e08`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 4.5 MB (4497202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e720a4acb8f391823b838f963c0b4de61247a73c4721a3224829968b7b7c0e4c`  
		Last Modified: Tue, 11 Oct 2022 17:41:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:fb39a5ed839f11261b832e0dca62197ee21a2ad938138f4cc656a9a52d03d975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:windowsservercore` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:4bddc4dfe1d225cfe86ce8237721abb0c49bd069e8c0bf1ab5c0ba2ec5c6899b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2716818637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ab84e2e207d755fd864c921bfee7744f5f0533ef2a8eb1649486351579db39`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 17:22:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Oct 2022 17:22:08 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:22:09 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:22:10 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.3/nats-server-v2.9.3-windows-amd64.zip
# Tue, 11 Oct 2022 17:22:11 GMT
ENV NATS_SERVER_SHASUM=83b25dad03dee498becb734623ae4d096235b2863be878d5f6d6a32d76f7e85f
# Tue, 11 Oct 2022 17:23:56 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Oct 2022 17:25:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 11 Oct 2022 17:25:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:32 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:25:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c778a0131ae2f1653f1fb703f05998e74365629f70b1a15a0360fb1292182846`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ce79ce85e7eb7d4b12316d81cc8cb3ff2567ee214f4aa0bbf36933fd55891f`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462d88c3de2e572b0d0ee482e3424c3ecb6eae150e8b29e5c8678a3059178bea`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12db35ec0388714c2e4e91a025ad3c010583c420b244c7941d378814da4b414`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61065ad9c7494c241e65c1c1b701828947105c6de39a9a246ef1da83d1967b`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a922f9001668df7166a8c2806eb76dacbac25dfe2a6a6b366546a53ff4a68be`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 350.4 KB (350379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696f9101e75d054c09b2f5086fdb484f298ac859200417dc480c0c95d4db8b79`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 5.3 MB (5290962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063d7a0294a6b35b745dafda4218ac1caccd20c2862af30174e073d25df4240f`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d46f46f65dffc178e8ef8c4d17fc35f23e32db9c2b23028319ab7d51f92b36e`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea87d29a4c3431239148436823825cc53a83211b86daa22eb69df30ff028bde`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245dfbad1025b6c7d6ad15e3336d3a11bd111607ce8db6de8efed6a157cc5872`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:fb39a5ed839f11261b832e0dca62197ee21a2ad938138f4cc656a9a52d03d975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:4bddc4dfe1d225cfe86ce8237721abb0c49bd069e8c0bf1ab5c0ba2ec5c6899b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2716818637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ab84e2e207d755fd864c921bfee7744f5f0533ef2a8eb1649486351579db39`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 17:22:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Oct 2022 17:22:08 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 17:22:09 GMT
ENV NATS_SERVER=2.9.3
# Tue, 11 Oct 2022 17:22:10 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.3/nats-server-v2.9.3-windows-amd64.zip
# Tue, 11 Oct 2022 17:22:11 GMT
ENV NATS_SERVER_SHASUM=83b25dad03dee498becb734623ae4d096235b2863be878d5f6d6a32d76f7e85f
# Tue, 11 Oct 2022 17:23:56 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Oct 2022 17:25:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 11 Oct 2022 17:25:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 11 Oct 2022 17:25:32 GMT
EXPOSE 4222 6222 8222
# Tue, 11 Oct 2022 17:25:33 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 11 Oct 2022 17:25:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c778a0131ae2f1653f1fb703f05998e74365629f70b1a15a0360fb1292182846`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ce79ce85e7eb7d4b12316d81cc8cb3ff2567ee214f4aa0bbf36933fd55891f`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462d88c3de2e572b0d0ee482e3424c3ecb6eae150e8b29e5c8678a3059178bea`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12db35ec0388714c2e4e91a025ad3c010583c420b244c7941d378814da4b414`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61065ad9c7494c241e65c1c1b701828947105c6de39a9a246ef1da83d1967b`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a922f9001668df7166a8c2806eb76dacbac25dfe2a6a6b366546a53ff4a68be`  
		Last Modified: Tue, 11 Oct 2022 17:26:35 GMT  
		Size: 350.4 KB (350379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696f9101e75d054c09b2f5086fdb484f298ac859200417dc480c0c95d4db8b79`  
		Last Modified: Tue, 11 Oct 2022 17:26:34 GMT  
		Size: 5.3 MB (5290962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063d7a0294a6b35b745dafda4218ac1caccd20c2862af30174e073d25df4240f`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d46f46f65dffc178e8ef8c4d17fc35f23e32db9c2b23028319ab7d51f92b36e`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea87d29a4c3431239148436823825cc53a83211b86daa22eb69df30ff028bde`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245dfbad1025b6c7d6ad15e3336d3a11bd111607ce8db6de8efed6a157cc5872`  
		Last Modified: Tue, 11 Oct 2022 17:26:33 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
