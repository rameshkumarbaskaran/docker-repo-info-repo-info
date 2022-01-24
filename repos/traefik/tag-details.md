<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:1.7`](#traefik17)
-	[`traefik:1.7-alpine`](#traefik17-alpine)
-	[`traefik:1.7-windowsservercore-1809`](#traefik17-windowsservercore-1809)
-	[`traefik:1.7.34`](#traefik1734)
-	[`traefik:1.7.34-alpine`](#traefik1734-alpine)
-	[`traefik:1.7.34-windowsservercore-1809`](#traefik1734-windowsservercore-1809)
-	[`traefik:2.6`](#traefik26)
-	[`traefik:2.6-windowsservercore-1809`](#traefik26-windowsservercore-1809)
-	[`traefik:2.6.0`](#traefik260)
-	[`traefik:2.6.0-windowsservercore-1809`](#traefik260-windowsservercore-1809)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:maroilles`](#traefikmaroilles)
-	[`traefik:maroilles-alpine`](#traefikmaroilles-alpine)
-	[`traefik:maroilles-windowsservercore-1809`](#traefikmaroilles-windowsservercore-1809)
-	[`traefik:rocamadour`](#traefikrocamadour)
-	[`traefik:rocamadour-windowsservercore-1809`](#traefikrocamadour-windowsservercore-1809)
-	[`traefik:v1.7`](#traefikv17)
-	[`traefik:v1.7-alpine`](#traefikv17-alpine)
-	[`traefik:v1.7-windowsservercore-1809`](#traefikv17-windowsservercore-1809)
-	[`traefik:v1.7.34`](#traefikv1734)
-	[`traefik:v1.7.34-alpine`](#traefikv1734-alpine)
-	[`traefik:v1.7.34-windowsservercore-1809`](#traefikv1734-windowsservercore-1809)
-	[`traefik:v2.6`](#traefikv26)
-	[`traefik:v2.6-windowsservercore-1809`](#traefikv26-windowsservercore-1809)
-	[`traefik:v2.6.0`](#traefikv260)
-	[`traefik:v2.6.0-windowsservercore-1809`](#traefikv260-windowsservercore-1809)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)

## `traefik:1.7`

```console
$ docker pull traefik@sha256:16ab8f1f8facbfa34f11411735be42ca09cc207f4f607f874c0951659aeac258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7` - linux; amd64

```console
$ docker pull traefik@sha256:316eeccf5b0e15c7557194096f1b75b8f3ce3de0052c6ebe7c45b005bd53b366
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22612937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7608bd808d08bc0d844935c654371ee6693c80e036ed2c11c4a5ad3178d8e553`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 17:58:25 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Sat, 13 Nov 2021 07:23:46 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 21:32:47 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 10 Dec 2021 21:32:48 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:48 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 21:32:48 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 21:32:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:13e52be55f8d958b3ebb4e73685de5dd10ff4b4af613c4d23424519693aa01e0`  
		Last Modified: Tue, 05 Oct 2021 17:59:12 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a918f6229a44912f657372ae3d390880a3bf6c27e51417a093520abf943f47`  
		Last Modified: Sat, 13 Nov 2021 07:25:13 GMT  
		Size: 328.6 KB (328578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51ca2df8b1b62bfda71acdff9512e649432f7669c2b4f58f50db456c5fa7b5b`  
		Last Modified: Fri, 10 Dec 2021 21:34:00 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4ae8110451cd8b856050c0519b9106085bf2fb213c1810b559effa377cc9176b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21074267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5d0502d4402e86fa35987d85b84ae56e01f0b4054937aea39094c4be01ea6a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 00:02:38 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Sat, 13 Nov 2021 06:52:39 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 21:50:42 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Fri, 10 Dec 2021 21:50:43 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:43 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 21:50:44 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 21:50:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:611185932e68f8b41b94235c966a6c2d26bb4a0f053993c6e49edc01123213f9`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81282f8b9fcf1f821d7dab2ed1f6addbda565118cc5ee95d9de4ae8ff91333f`  
		Last Modified: Sat, 13 Nov 2021 06:55:43 GMT  
		Size: 328.6 KB (328578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3730ee17455103047e8a361f9e99218a36fcfc41b26fb92516fd9be41ba39c`  
		Last Modified: Fri, 10 Dec 2021 21:53:45 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:adc574c52a5b551c4d5ad2be0d2840be3053c2ea51530325497ea3b12cb9f585
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20582290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a34f8b1feaaf314ac5500fe3f4d71ab33659cc44ca8e5389b8eb36d344b19`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 08 Nov 2021 20:23:04 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Mon, 08 Nov 2021 20:23:05 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 22:10:54 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Fri, 10 Dec 2021 22:10:54 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:55 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 22:10:56 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 22:10:57 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:078e101c84a7a75069b9c18efdfc2b24c9840aa136b34eb6e3a0ebe1b74d0a94`  
		Last Modified: Mon, 08 Nov 2021 20:24:37 GMT  
		Size: 122.4 KB (122399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7a624fda7cabc945cc9d9f610f256d933b121fdafa2052d617cf3144bbe2aa`  
		Last Modified: Mon, 08 Nov 2021 20:24:37 GMT  
		Size: 328.5 KB (328545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3ecfc2ff53e207251e72b68f2570d2a5dae382ad897f8ad4c2811e482770d6`  
		Last Modified: Fri, 10 Dec 2021 22:12:29 GMT  
		Size: 20.1 MB (20131346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-alpine`

```console
$ docker pull traefik@sha256:36645215a2367d25d1aa9d82a00a3d55b78da3a77f5a742a354c3eee6ca9696e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:26057fa675bf46c770691d54fa06179744a268643d6d9265a100b33f7616a7fe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25663227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0385562c2ca638c3e56fc5e368e0d760861501c3acb1be07b1ec2ff5f4ec8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:32:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:32:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:32:17 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:32:18 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:32:18 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8fccde93889bb45e3ec014080674609715442d77a83c4e22aed842c54aa320`  
		Last Modified: Fri, 10 Dec 2021 21:33:40 GMT  
		Size: 22.2 MB (22162054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5edab535d879083fbb7bc0569dd3b1588e3ad6549c4ba201eecf74820ad66aa`  
		Last Modified: Fri, 10 Dec 2021 21:33:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d6148854489f78aa02ad57c0ffdf49690f1df5e8419adb2677d1bac979a6b58c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23942165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e476d9b470f0d848b51a66f192af4d51464443367916280dfffa10d7c00efec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:50:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:50:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:50:20 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:50:21 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:50:21 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3379812682fc7d134d4c61b4dc36cfa6924cd554bfed9e11a2ce6927d111484`  
		Last Modified: Fri, 10 Dec 2021 21:53:07 GMT  
		Size: 20.6 MB (20623432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae87b8d30f43743051ca67a1de1aae50831617389e950c804f7267fa8d100ef`  
		Last Modified: Fri, 10 Dec 2021 21:52:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:32a677053c58d48c9176bad0f34a4c615d3f56aa02d5227d6a6bf4405197095d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23529454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968d2aabeb48500d4f5cd1417d792e3589d251ffdffa051738ed4465ca5dedec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 22:10:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 22:10:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 22:10:41 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 22:10:43 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 22:10:44 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2cdc6d798fd61d5f7a4c0530d3cec221698500c821c7c43d03b7ba1956b8ad`  
		Last Modified: Fri, 10 Dec 2021 22:12:07 GMT  
		Size: 20.1 MB (20131378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c1839484effd5cd9538632a7a114e155d1dfa9c0acc3db51242271af684434`  
		Last Modified: Fri, 10 Dec 2021 22:12:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:6b11bad47b82c2ce735972715400a7436f7db75ed9d702bd4d34d6457621d382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `traefik:1.7-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull traefik@sha256:6dc156b3fc1fcc1652afb67e7c266f9a96b5edbdf88120cd860afcd03a80d7b3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2736173799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4231ea3f1edf8127f1127d1bdfeffaec3ea5d3c9806a5fb0ec85ba1d7712c78f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Jan 2022 20:20:12 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Thu, 20 Jan 2022 20:20:13 GMT
EXPOSE 80
# Thu, 20 Jan 2022 20:20:14 GMT
ENTRYPOINT ["/traefik"]
# Thu, 20 Jan 2022 20:20:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086785254069d57d991fb33221dcdbddc1bf5ab2f6130b06969c5d28d4b3154c`  
		Last Modified: Thu, 20 Jan 2022 20:21:35 GMT  
		Size: 22.8 MB (22846646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc1bb22ab8ce95752191c8ef1f3fcf32eebda933b25acf756be02d092b83778`  
		Last Modified: Thu, 20 Jan 2022 20:21:29 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37af60424ba83807daa1c78e417c2a0c8f23500bb7b0d7277fef45b1b2203f2e`  
		Last Modified: Thu, 20 Jan 2022 20:21:29 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fbbd099df5a89905425a50883a2d467142413ca693c8e826cfddffa86d6bc5`  
		Last Modified: Thu, 20 Jan 2022 20:21:29 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.34`

```console
$ docker pull traefik@sha256:16ab8f1f8facbfa34f11411735be42ca09cc207f4f607f874c0951659aeac258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.34` - linux; amd64

```console
$ docker pull traefik@sha256:316eeccf5b0e15c7557194096f1b75b8f3ce3de0052c6ebe7c45b005bd53b366
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22612937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7608bd808d08bc0d844935c654371ee6693c80e036ed2c11c4a5ad3178d8e553`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 17:58:25 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Sat, 13 Nov 2021 07:23:46 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 21:32:47 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 10 Dec 2021 21:32:48 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:48 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 21:32:48 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 21:32:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:13e52be55f8d958b3ebb4e73685de5dd10ff4b4af613c4d23424519693aa01e0`  
		Last Modified: Tue, 05 Oct 2021 17:59:12 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a918f6229a44912f657372ae3d390880a3bf6c27e51417a093520abf943f47`  
		Last Modified: Sat, 13 Nov 2021 07:25:13 GMT  
		Size: 328.6 KB (328578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51ca2df8b1b62bfda71acdff9512e649432f7669c2b4f58f50db456c5fa7b5b`  
		Last Modified: Fri, 10 Dec 2021 21:34:00 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4ae8110451cd8b856050c0519b9106085bf2fb213c1810b559effa377cc9176b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21074267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5d0502d4402e86fa35987d85b84ae56e01f0b4054937aea39094c4be01ea6a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 00:02:38 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Sat, 13 Nov 2021 06:52:39 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 21:50:42 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Fri, 10 Dec 2021 21:50:43 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:43 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 21:50:44 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 21:50:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:611185932e68f8b41b94235c966a6c2d26bb4a0f053993c6e49edc01123213f9`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81282f8b9fcf1f821d7dab2ed1f6addbda565118cc5ee95d9de4ae8ff91333f`  
		Last Modified: Sat, 13 Nov 2021 06:55:43 GMT  
		Size: 328.6 KB (328578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3730ee17455103047e8a361f9e99218a36fcfc41b26fb92516fd9be41ba39c`  
		Last Modified: Fri, 10 Dec 2021 21:53:45 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:adc574c52a5b551c4d5ad2be0d2840be3053c2ea51530325497ea3b12cb9f585
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20582290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a34f8b1feaaf314ac5500fe3f4d71ab33659cc44ca8e5389b8eb36d344b19`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 08 Nov 2021 20:23:04 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Mon, 08 Nov 2021 20:23:05 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 22:10:54 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Fri, 10 Dec 2021 22:10:54 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:55 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 22:10:56 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 22:10:57 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:078e101c84a7a75069b9c18efdfc2b24c9840aa136b34eb6e3a0ebe1b74d0a94`  
		Last Modified: Mon, 08 Nov 2021 20:24:37 GMT  
		Size: 122.4 KB (122399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7a624fda7cabc945cc9d9f610f256d933b121fdafa2052d617cf3144bbe2aa`  
		Last Modified: Mon, 08 Nov 2021 20:24:37 GMT  
		Size: 328.5 KB (328545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3ecfc2ff53e207251e72b68f2570d2a5dae382ad897f8ad4c2811e482770d6`  
		Last Modified: Fri, 10 Dec 2021 22:12:29 GMT  
		Size: 20.1 MB (20131346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.34-alpine`

```console
$ docker pull traefik@sha256:36645215a2367d25d1aa9d82a00a3d55b78da3a77f5a742a354c3eee6ca9696e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.34-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:26057fa675bf46c770691d54fa06179744a268643d6d9265a100b33f7616a7fe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25663227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0385562c2ca638c3e56fc5e368e0d760861501c3acb1be07b1ec2ff5f4ec8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:32:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:32:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:32:17 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:32:18 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:32:18 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8fccde93889bb45e3ec014080674609715442d77a83c4e22aed842c54aa320`  
		Last Modified: Fri, 10 Dec 2021 21:33:40 GMT  
		Size: 22.2 MB (22162054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5edab535d879083fbb7bc0569dd3b1588e3ad6549c4ba201eecf74820ad66aa`  
		Last Modified: Fri, 10 Dec 2021 21:33:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d6148854489f78aa02ad57c0ffdf49690f1df5e8419adb2677d1bac979a6b58c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23942165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e476d9b470f0d848b51a66f192af4d51464443367916280dfffa10d7c00efec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:50:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:50:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:50:20 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:50:21 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:50:21 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3379812682fc7d134d4c61b4dc36cfa6924cd554bfed9e11a2ce6927d111484`  
		Last Modified: Fri, 10 Dec 2021 21:53:07 GMT  
		Size: 20.6 MB (20623432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae87b8d30f43743051ca67a1de1aae50831617389e950c804f7267fa8d100ef`  
		Last Modified: Fri, 10 Dec 2021 21:52:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:32a677053c58d48c9176bad0f34a4c615d3f56aa02d5227d6a6bf4405197095d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23529454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968d2aabeb48500d4f5cd1417d792e3589d251ffdffa051738ed4465ca5dedec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 22:10:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 22:10:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 22:10:41 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 22:10:43 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 22:10:44 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2cdc6d798fd61d5f7a4c0530d3cec221698500c821c7c43d03b7ba1956b8ad`  
		Last Modified: Fri, 10 Dec 2021 22:12:07 GMT  
		Size: 20.1 MB (20131378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c1839484effd5cd9538632a7a114e155d1dfa9c0acc3db51242271af684434`  
		Last Modified: Fri, 10 Dec 2021 22:12:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.34-windowsservercore-1809`

```console
$ docker pull traefik@sha256:6b11bad47b82c2ce735972715400a7436f7db75ed9d702bd4d34d6457621d382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `traefik:1.7.34-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull traefik@sha256:6dc156b3fc1fcc1652afb67e7c266f9a96b5edbdf88120cd860afcd03a80d7b3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2736173799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4231ea3f1edf8127f1127d1bdfeffaec3ea5d3c9806a5fb0ec85ba1d7712c78f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Jan 2022 20:20:12 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Thu, 20 Jan 2022 20:20:13 GMT
EXPOSE 80
# Thu, 20 Jan 2022 20:20:14 GMT
ENTRYPOINT ["/traefik"]
# Thu, 20 Jan 2022 20:20:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086785254069d57d991fb33221dcdbddc1bf5ab2f6130b06969c5d28d4b3154c`  
		Last Modified: Thu, 20 Jan 2022 20:21:35 GMT  
		Size: 22.8 MB (22846646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc1bb22ab8ce95752191c8ef1f3fcf32eebda933b25acf756be02d092b83778`  
		Last Modified: Thu, 20 Jan 2022 20:21:29 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37af60424ba83807daa1c78e417c2a0c8f23500bb7b0d7277fef45b1b2203f2e`  
		Last Modified: Thu, 20 Jan 2022 20:21:29 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fbbd099df5a89905425a50883a2d467142413ca693c8e826cfddffa86d6bc5`  
		Last Modified: Thu, 20 Jan 2022 20:21:29 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.6`

```console
$ docker pull traefik@sha256:425fdedf3b76cd6f8a532889cfd2b949225210bf6dff19c6f7aa9306e11754a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.6` - linux; amd64

```console
$ docker pull traefik@sha256:3540454a0ee471351dc8f874642afbba07ae0eb387c30ca9b57027409bc377ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30340722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb72e139c3d3963f217bf16e6cb197af821ce187a96a16452d0e0bad80861a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 20 Jan 2022 21:55:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc3/traefik_v2.6.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 20 Jan 2022 21:55:32 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 20 Jan 2022 21:55:33 GMT
EXPOSE 80
# Thu, 20 Jan 2022 21:55:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Jan 2022 21:55:33 GMT
CMD ["traefik"]
# Thu, 20 Jan 2022 21:55:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2d15e40ed08c50672c2820538c9dcad4eae1566976b868a66c983230303c14`  
		Last Modified: Thu, 20 Jan 2022 21:56:18 GMT  
		Size: 26.8 MB (26839549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6138b06ac528688b2cf203650e459f6038cf060dcb83aa47168748bc2281751`  
		Last Modified: Thu, 20 Jan 2022 21:56:13 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:34f6e6627e0a0f9a737ee26c4011d53717c2ccd5a93e4536226b26bbea25ee11
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28509493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9b895b4223d0c9b2bbe5f33d94bbd61560d74ed24840ea909f16965cff29d1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 20 Jan 2022 21:14:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc3/traefik_v2.6.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 20 Jan 2022 21:14:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 20 Jan 2022 21:14:40 GMT
EXPOSE 80
# Thu, 20 Jan 2022 21:14:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Jan 2022 21:14:41 GMT
CMD ["traefik"]
# Thu, 20 Jan 2022 21:14:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777ccc4d94ad04ea4b2d8ea281daa48a0b6dfc459a1cb28abb6b1e8e89315865`  
		Last Modified: Thu, 20 Jan 2022 21:17:32 GMT  
		Size: 25.2 MB (25190760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7ab33ace6417d443e7a6d8e494d98c1c2815e761a23365ca6ec3ce2829c31c`  
		Last Modified: Thu, 20 Jan 2022 21:17:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:55fe42ad5db4842e72dc5f4ef11c6b8e9d5c9098d843d363b8198a9aafa5007b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27883145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad74a7e4206e20366bbe215d9a513a1ed5d4a8d6fa048f174ad4e404d92ec2b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 20 Jan 2022 20:41:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc3/traefik_v2.6.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 20 Jan 2022 20:41:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 20 Jan 2022 20:41:46 GMT
EXPOSE 80
# Thu, 20 Jan 2022 20:41:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Jan 2022 20:41:48 GMT
CMD ["traefik"]
# Thu, 20 Jan 2022 20:41:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164cdde581159f519100f7672af7f721fa6214bb8af19b72d9dccdfba81e47cb`  
		Last Modified: Thu, 20 Jan 2022 20:43:02 GMT  
		Size: 24.5 MB (24485069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7f2efbda48f2d261412124526127c9b4315dc85ab5a8e08c92a97c3d7cd066`  
		Last Modified: Thu, 20 Jan 2022 20:42:58 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.6-windowsservercore-1809`

```console
$ docker pull traefik@sha256:56a39e3e1a6fe5fd550a8a1336c25894872c0dc34839db81da2663e6cb1566b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `traefik:2.6-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull traefik@sha256:1a39c429ce030ea8b2139589b4ba8ac04394df6e6d9535315767e5aaa9385a71
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2740729297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed534d21b80ab2daaaa126d6bee462576099b88189f1832b09461528629f5ab9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Jan 2022 20:17:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.6.0/traefik_v2.6.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 24 Jan 2022 20:17:03 GMT
EXPOSE 80
# Mon, 24 Jan 2022 20:17:04 GMT
ENTRYPOINT ["/traefik"]
# Mon, 24 Jan 2022 20:17:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616132a37689aebcffad1ee520d0c1b885896cbbd641ac3a6657f10102dea775`  
		Last Modified: Mon, 24 Jan 2022 20:17:55 GMT  
		Size: 27.4 MB (27402109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f21934cfc92e23f4ae5fcd28c678568ac61272fcb9926372a431c411f29707`  
		Last Modified: Mon, 24 Jan 2022 20:17:47 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3c1c2283ebd964f4dc8cdee2dd6d9cfd9249714e6a4632c87473bab0cc3c30`  
		Last Modified: Mon, 24 Jan 2022 20:17:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcc3aea18c6fd8c60605fd9add226a7c5b80ded6db1d2605bc5cc2b8b21df0e`  
		Last Modified: Mon, 24 Jan 2022 20:17:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.6.0`

```console
$ docker pull traefik@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `traefik:2.6.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:56a39e3e1a6fe5fd550a8a1336c25894872c0dc34839db81da2663e6cb1566b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `traefik:2.6.0-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull traefik@sha256:1a39c429ce030ea8b2139589b4ba8ac04394df6e6d9535315767e5aaa9385a71
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2740729297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed534d21b80ab2daaaa126d6bee462576099b88189f1832b09461528629f5ab9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Jan 2022 20:17:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.6.0/traefik_v2.6.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 24 Jan 2022 20:17:03 GMT
EXPOSE 80
# Mon, 24 Jan 2022 20:17:04 GMT
ENTRYPOINT ["/traefik"]
# Mon, 24 Jan 2022 20:17:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616132a37689aebcffad1ee520d0c1b885896cbbd641ac3a6657f10102dea775`  
		Last Modified: Mon, 24 Jan 2022 20:17:55 GMT  
		Size: 27.4 MB (27402109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f21934cfc92e23f4ae5fcd28c678568ac61272fcb9926372a431c411f29707`  
		Last Modified: Mon, 24 Jan 2022 20:17:47 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3c1c2283ebd964f4dc8cdee2dd6d9cfd9249714e6a4632c87473bab0cc3c30`  
		Last Modified: Mon, 24 Jan 2022 20:17:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcc3aea18c6fd8c60605fd9add226a7c5b80ded6db1d2605bc5cc2b8b21df0e`  
		Last Modified: Mon, 24 Jan 2022 20:17:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:7d5a6ae66572b27afe1059ce893b59acb28de70f4ce298385e153d0a398ce7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:64e13dc2f241f9d021eda736f5a7c3dc81c113554dd611a9c52340a5e3b7843b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 MB (30112526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865923368a9fd63e7dd1f422e62eda3ef56b005a366eeb5ce90e6603b48a14e6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 20 Jan 2022 21:55:41 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.7/traefik_v2.5.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 20 Jan 2022 21:55:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 20 Jan 2022 21:55:41 GMT
EXPOSE 80
# Thu, 20 Jan 2022 21:55:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Jan 2022 21:55:42 GMT
CMD ["traefik"]
# Thu, 20 Jan 2022 21:55:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd589cd7ab3083a41c8f8d911282899c2d4faefbe1bc7922963283b62f0989ee`  
		Last Modified: Thu, 20 Jan 2022 21:56:40 GMT  
		Size: 26.6 MB (26611353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d201bdb744b3d125df4ce42bd584419646faf55ef2e5f17c257ea92b8e09fe`  
		Last Modified: Thu, 20 Jan 2022 21:56:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:6604b7ad35a0c17ba6da3d4b92f5cd74817ddda4df37ed554c6c50e12fe7c9ce
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28303032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20161d4cde6b5ab7fc5eefc45a234210d903379663d7d06b844c8c6d30fe3b94`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 20 Jan 2022 21:15:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.7/traefik_v2.5.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 20 Jan 2022 21:15:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 20 Jan 2022 21:15:04 GMT
EXPOSE 80
# Thu, 20 Jan 2022 21:15:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Jan 2022 21:15:05 GMT
CMD ["traefik"]
# Thu, 20 Jan 2022 21:15:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d60297a7348e37cf87a8df5921a0a70fdb73710e47482791fed22dfebebbc42`  
		Last Modified: Thu, 20 Jan 2022 21:18:13 GMT  
		Size: 25.0 MB (24984300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09068b7071722c0f0a367ef0bbca2b6d6de0b9eac12d973390a3aeacc06709b4`  
		Last Modified: Thu, 20 Jan 2022 21:17:56 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a2e170cefb82b6f9622375a138f74a58f9276c93c001b9584ab0e050589f452f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27679943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bdb197fc5db12b3367fba943964ffdb0262a1e31194a595048bd06b204f129`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 20 Jan 2022 20:41:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.7/traefik_v2.5.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 20 Jan 2022 20:42:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 20 Jan 2022 20:42:00 GMT
EXPOSE 80
# Thu, 20 Jan 2022 20:42:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Jan 2022 20:42:02 GMT
CMD ["traefik"]
# Thu, 20 Jan 2022 20:42:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b00c8b717648ebe8c3705dfae83cef5398254b781490df86ec17a9d5a756be5`  
		Last Modified: Thu, 20 Jan 2022 20:43:26 GMT  
		Size: 24.3 MB (24281867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a1694dfaf88d33f2831e63ea685e183efd0f37dff664f387b22dd5b17670ff`  
		Last Modified: Thu, 20 Jan 2022 20:43:22 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles`

```console
$ docker pull traefik@sha256:16ab8f1f8facbfa34f11411735be42ca09cc207f4f607f874c0951659aeac258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:316eeccf5b0e15c7557194096f1b75b8f3ce3de0052c6ebe7c45b005bd53b366
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22612937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7608bd808d08bc0d844935c654371ee6693c80e036ed2c11c4a5ad3178d8e553`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 17:58:25 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Sat, 13 Nov 2021 07:23:46 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 21:32:47 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 10 Dec 2021 21:32:48 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:48 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 21:32:48 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 21:32:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:13e52be55f8d958b3ebb4e73685de5dd10ff4b4af613c4d23424519693aa01e0`  
		Last Modified: Tue, 05 Oct 2021 17:59:12 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a918f6229a44912f657372ae3d390880a3bf6c27e51417a093520abf943f47`  
		Last Modified: Sat, 13 Nov 2021 07:25:13 GMT  
		Size: 328.6 KB (328578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51ca2df8b1b62bfda71acdff9512e649432f7669c2b4f58f50db456c5fa7b5b`  
		Last Modified: Fri, 10 Dec 2021 21:34:00 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4ae8110451cd8b856050c0519b9106085bf2fb213c1810b559effa377cc9176b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21074267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5d0502d4402e86fa35987d85b84ae56e01f0b4054937aea39094c4be01ea6a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 00:02:38 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Sat, 13 Nov 2021 06:52:39 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 21:50:42 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Fri, 10 Dec 2021 21:50:43 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:43 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 21:50:44 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 21:50:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:611185932e68f8b41b94235c966a6c2d26bb4a0f053993c6e49edc01123213f9`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81282f8b9fcf1f821d7dab2ed1f6addbda565118cc5ee95d9de4ae8ff91333f`  
		Last Modified: Sat, 13 Nov 2021 06:55:43 GMT  
		Size: 328.6 KB (328578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3730ee17455103047e8a361f9e99218a36fcfc41b26fb92516fd9be41ba39c`  
		Last Modified: Fri, 10 Dec 2021 21:53:45 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:adc574c52a5b551c4d5ad2be0d2840be3053c2ea51530325497ea3b12cb9f585
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20582290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a34f8b1feaaf314ac5500fe3f4d71ab33659cc44ca8e5389b8eb36d344b19`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 08 Nov 2021 20:23:04 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Mon, 08 Nov 2021 20:23:05 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 22:10:54 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Fri, 10 Dec 2021 22:10:54 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:55 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 22:10:56 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 22:10:57 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:078e101c84a7a75069b9c18efdfc2b24c9840aa136b34eb6e3a0ebe1b74d0a94`  
		Last Modified: Mon, 08 Nov 2021 20:24:37 GMT  
		Size: 122.4 KB (122399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7a624fda7cabc945cc9d9f610f256d933b121fdafa2052d617cf3144bbe2aa`  
		Last Modified: Mon, 08 Nov 2021 20:24:37 GMT  
		Size: 328.5 KB (328545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3ecfc2ff53e207251e72b68f2570d2a5dae382ad897f8ad4c2811e482770d6`  
		Last Modified: Fri, 10 Dec 2021 22:12:29 GMT  
		Size: 20.1 MB (20131346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-alpine`

```console
$ docker pull traefik@sha256:36645215a2367d25d1aa9d82a00a3d55b78da3a77f5a742a354c3eee6ca9696e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:26057fa675bf46c770691d54fa06179744a268643d6d9265a100b33f7616a7fe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25663227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0385562c2ca638c3e56fc5e368e0d760861501c3acb1be07b1ec2ff5f4ec8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:32:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:32:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:32:17 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:32:18 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:32:18 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8fccde93889bb45e3ec014080674609715442d77a83c4e22aed842c54aa320`  
		Last Modified: Fri, 10 Dec 2021 21:33:40 GMT  
		Size: 22.2 MB (22162054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5edab535d879083fbb7bc0569dd3b1588e3ad6549c4ba201eecf74820ad66aa`  
		Last Modified: Fri, 10 Dec 2021 21:33:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d6148854489f78aa02ad57c0ffdf49690f1df5e8419adb2677d1bac979a6b58c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23942165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e476d9b470f0d848b51a66f192af4d51464443367916280dfffa10d7c00efec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:50:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:50:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:50:20 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:50:21 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:50:21 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3379812682fc7d134d4c61b4dc36cfa6924cd554bfed9e11a2ce6927d111484`  
		Last Modified: Fri, 10 Dec 2021 21:53:07 GMT  
		Size: 20.6 MB (20623432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae87b8d30f43743051ca67a1de1aae50831617389e950c804f7267fa8d100ef`  
		Last Modified: Fri, 10 Dec 2021 21:52:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:32a677053c58d48c9176bad0f34a4c615d3f56aa02d5227d6a6bf4405197095d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23529454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968d2aabeb48500d4f5cd1417d792e3589d251ffdffa051738ed4465ca5dedec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 22:10:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 22:10:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 22:10:41 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 22:10:43 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 22:10:44 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2cdc6d798fd61d5f7a4c0530d3cec221698500c821c7c43d03b7ba1956b8ad`  
		Last Modified: Fri, 10 Dec 2021 22:12:07 GMT  
		Size: 20.1 MB (20131378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c1839484effd5cd9538632a7a114e155d1dfa9c0acc3db51242271af684434`  
		Last Modified: Fri, 10 Dec 2021 22:12:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-windowsservercore-1809`

```console
$ docker pull traefik@sha256:6b11bad47b82c2ce735972715400a7436f7db75ed9d702bd4d34d6457621d382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull traefik@sha256:6dc156b3fc1fcc1652afb67e7c266f9a96b5edbdf88120cd860afcd03a80d7b3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2736173799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4231ea3f1edf8127f1127d1bdfeffaec3ea5d3c9806a5fb0ec85ba1d7712c78f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Jan 2022 20:20:12 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Thu, 20 Jan 2022 20:20:13 GMT
EXPOSE 80
# Thu, 20 Jan 2022 20:20:14 GMT
ENTRYPOINT ["/traefik"]
# Thu, 20 Jan 2022 20:20:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086785254069d57d991fb33221dcdbddc1bf5ab2f6130b06969c5d28d4b3154c`  
		Last Modified: Thu, 20 Jan 2022 20:21:35 GMT  
		Size: 22.8 MB (22846646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc1bb22ab8ce95752191c8ef1f3fcf32eebda933b25acf756be02d092b83778`  
		Last Modified: Thu, 20 Jan 2022 20:21:29 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37af60424ba83807daa1c78e417c2a0c8f23500bb7b0d7277fef45b1b2203f2e`  
		Last Modified: Thu, 20 Jan 2022 20:21:29 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fbbd099df5a89905425a50883a2d467142413ca693c8e826cfddffa86d6bc5`  
		Last Modified: Thu, 20 Jan 2022 20:21:29 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:rocamadour`

```console
$ docker pull traefik@sha256:425fdedf3b76cd6f8a532889cfd2b949225210bf6dff19c6f7aa9306e11754a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:rocamadour` - linux; amd64

```console
$ docker pull traefik@sha256:3540454a0ee471351dc8f874642afbba07ae0eb387c30ca9b57027409bc377ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30340722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb72e139c3d3963f217bf16e6cb197af821ce187a96a16452d0e0bad80861a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 20 Jan 2022 21:55:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc3/traefik_v2.6.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 20 Jan 2022 21:55:32 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 20 Jan 2022 21:55:33 GMT
EXPOSE 80
# Thu, 20 Jan 2022 21:55:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Jan 2022 21:55:33 GMT
CMD ["traefik"]
# Thu, 20 Jan 2022 21:55:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2d15e40ed08c50672c2820538c9dcad4eae1566976b868a66c983230303c14`  
		Last Modified: Thu, 20 Jan 2022 21:56:18 GMT  
		Size: 26.8 MB (26839549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6138b06ac528688b2cf203650e459f6038cf060dcb83aa47168748bc2281751`  
		Last Modified: Thu, 20 Jan 2022 21:56:13 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:rocamadour` - linux; arm variant v6

```console
$ docker pull traefik@sha256:34f6e6627e0a0f9a737ee26c4011d53717c2ccd5a93e4536226b26bbea25ee11
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28509493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9b895b4223d0c9b2bbe5f33d94bbd61560d74ed24840ea909f16965cff29d1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 20 Jan 2022 21:14:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc3/traefik_v2.6.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 20 Jan 2022 21:14:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 20 Jan 2022 21:14:40 GMT
EXPOSE 80
# Thu, 20 Jan 2022 21:14:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Jan 2022 21:14:41 GMT
CMD ["traefik"]
# Thu, 20 Jan 2022 21:14:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777ccc4d94ad04ea4b2d8ea281daa48a0b6dfc459a1cb28abb6b1e8e89315865`  
		Last Modified: Thu, 20 Jan 2022 21:17:32 GMT  
		Size: 25.2 MB (25190760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7ab33ace6417d443e7a6d8e494d98c1c2815e761a23365ca6ec3ce2829c31c`  
		Last Modified: Thu, 20 Jan 2022 21:17:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:rocamadour` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:55fe42ad5db4842e72dc5f4ef11c6b8e9d5c9098d843d363b8198a9aafa5007b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27883145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad74a7e4206e20366bbe215d9a513a1ed5d4a8d6fa048f174ad4e404d92ec2b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 20 Jan 2022 20:41:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc3/traefik_v2.6.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 20 Jan 2022 20:41:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 20 Jan 2022 20:41:46 GMT
EXPOSE 80
# Thu, 20 Jan 2022 20:41:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Jan 2022 20:41:48 GMT
CMD ["traefik"]
# Thu, 20 Jan 2022 20:41:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164cdde581159f519100f7672af7f721fa6214bb8af19b72d9dccdfba81e47cb`  
		Last Modified: Thu, 20 Jan 2022 20:43:02 GMT  
		Size: 24.5 MB (24485069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7f2efbda48f2d261412124526127c9b4315dc85ab5a8e08c92a97c3d7cd066`  
		Last Modified: Thu, 20 Jan 2022 20:42:58 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:rocamadour-windowsservercore-1809`

```console
$ docker pull traefik@sha256:56a39e3e1a6fe5fd550a8a1336c25894872c0dc34839db81da2663e6cb1566b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `traefik:rocamadour-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull traefik@sha256:1a39c429ce030ea8b2139589b4ba8ac04394df6e6d9535315767e5aaa9385a71
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2740729297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed534d21b80ab2daaaa126d6bee462576099b88189f1832b09461528629f5ab9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Jan 2022 20:17:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.6.0/traefik_v2.6.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 24 Jan 2022 20:17:03 GMT
EXPOSE 80
# Mon, 24 Jan 2022 20:17:04 GMT
ENTRYPOINT ["/traefik"]
# Mon, 24 Jan 2022 20:17:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616132a37689aebcffad1ee520d0c1b885896cbbd641ac3a6657f10102dea775`  
		Last Modified: Mon, 24 Jan 2022 20:17:55 GMT  
		Size: 27.4 MB (27402109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f21934cfc92e23f4ae5fcd28c678568ac61272fcb9926372a431c411f29707`  
		Last Modified: Mon, 24 Jan 2022 20:17:47 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3c1c2283ebd964f4dc8cdee2dd6d9cfd9249714e6a4632c87473bab0cc3c30`  
		Last Modified: Mon, 24 Jan 2022 20:17:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcc3aea18c6fd8c60605fd9add226a7c5b80ded6db1d2605bc5cc2b8b21df0e`  
		Last Modified: Mon, 24 Jan 2022 20:17:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7`

```console
$ docker pull traefik@sha256:16ab8f1f8facbfa34f11411735be42ca09cc207f4f607f874c0951659aeac258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7` - linux; amd64

```console
$ docker pull traefik@sha256:316eeccf5b0e15c7557194096f1b75b8f3ce3de0052c6ebe7c45b005bd53b366
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22612937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7608bd808d08bc0d844935c654371ee6693c80e036ed2c11c4a5ad3178d8e553`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 17:58:25 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Sat, 13 Nov 2021 07:23:46 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 21:32:47 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 10 Dec 2021 21:32:48 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:48 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 21:32:48 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 21:32:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:13e52be55f8d958b3ebb4e73685de5dd10ff4b4af613c4d23424519693aa01e0`  
		Last Modified: Tue, 05 Oct 2021 17:59:12 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a918f6229a44912f657372ae3d390880a3bf6c27e51417a093520abf943f47`  
		Last Modified: Sat, 13 Nov 2021 07:25:13 GMT  
		Size: 328.6 KB (328578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51ca2df8b1b62bfda71acdff9512e649432f7669c2b4f58f50db456c5fa7b5b`  
		Last Modified: Fri, 10 Dec 2021 21:34:00 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4ae8110451cd8b856050c0519b9106085bf2fb213c1810b559effa377cc9176b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21074267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5d0502d4402e86fa35987d85b84ae56e01f0b4054937aea39094c4be01ea6a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 00:02:38 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Sat, 13 Nov 2021 06:52:39 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 21:50:42 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Fri, 10 Dec 2021 21:50:43 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:43 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 21:50:44 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 21:50:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:611185932e68f8b41b94235c966a6c2d26bb4a0f053993c6e49edc01123213f9`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81282f8b9fcf1f821d7dab2ed1f6addbda565118cc5ee95d9de4ae8ff91333f`  
		Last Modified: Sat, 13 Nov 2021 06:55:43 GMT  
		Size: 328.6 KB (328578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3730ee17455103047e8a361f9e99218a36fcfc41b26fb92516fd9be41ba39c`  
		Last Modified: Fri, 10 Dec 2021 21:53:45 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:adc574c52a5b551c4d5ad2be0d2840be3053c2ea51530325497ea3b12cb9f585
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20582290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a34f8b1feaaf314ac5500fe3f4d71ab33659cc44ca8e5389b8eb36d344b19`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 08 Nov 2021 20:23:04 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Mon, 08 Nov 2021 20:23:05 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 22:10:54 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Fri, 10 Dec 2021 22:10:54 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:55 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 22:10:56 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 22:10:57 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:078e101c84a7a75069b9c18efdfc2b24c9840aa136b34eb6e3a0ebe1b74d0a94`  
		Last Modified: Mon, 08 Nov 2021 20:24:37 GMT  
		Size: 122.4 KB (122399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7a624fda7cabc945cc9d9f610f256d933b121fdafa2052d617cf3144bbe2aa`  
		Last Modified: Mon, 08 Nov 2021 20:24:37 GMT  
		Size: 328.5 KB (328545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3ecfc2ff53e207251e72b68f2570d2a5dae382ad897f8ad4c2811e482770d6`  
		Last Modified: Fri, 10 Dec 2021 22:12:29 GMT  
		Size: 20.1 MB (20131346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-alpine`

```console
$ docker pull traefik@sha256:36645215a2367d25d1aa9d82a00a3d55b78da3a77f5a742a354c3eee6ca9696e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:26057fa675bf46c770691d54fa06179744a268643d6d9265a100b33f7616a7fe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25663227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0385562c2ca638c3e56fc5e368e0d760861501c3acb1be07b1ec2ff5f4ec8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:32:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:32:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:32:17 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:32:18 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:32:18 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8fccde93889bb45e3ec014080674609715442d77a83c4e22aed842c54aa320`  
		Last Modified: Fri, 10 Dec 2021 21:33:40 GMT  
		Size: 22.2 MB (22162054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5edab535d879083fbb7bc0569dd3b1588e3ad6549c4ba201eecf74820ad66aa`  
		Last Modified: Fri, 10 Dec 2021 21:33:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d6148854489f78aa02ad57c0ffdf49690f1df5e8419adb2677d1bac979a6b58c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23942165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e476d9b470f0d848b51a66f192af4d51464443367916280dfffa10d7c00efec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:50:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:50:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:50:20 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:50:21 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:50:21 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3379812682fc7d134d4c61b4dc36cfa6924cd554bfed9e11a2ce6927d111484`  
		Last Modified: Fri, 10 Dec 2021 21:53:07 GMT  
		Size: 20.6 MB (20623432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae87b8d30f43743051ca67a1de1aae50831617389e950c804f7267fa8d100ef`  
		Last Modified: Fri, 10 Dec 2021 21:52:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:32a677053c58d48c9176bad0f34a4c615d3f56aa02d5227d6a6bf4405197095d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23529454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968d2aabeb48500d4f5cd1417d792e3589d251ffdffa051738ed4465ca5dedec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 22:10:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 22:10:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 22:10:41 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 22:10:43 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 22:10:44 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2cdc6d798fd61d5f7a4c0530d3cec221698500c821c7c43d03b7ba1956b8ad`  
		Last Modified: Fri, 10 Dec 2021 22:12:07 GMT  
		Size: 20.1 MB (20131378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c1839484effd5cd9538632a7a114e155d1dfa9c0acc3db51242271af684434`  
		Last Modified: Fri, 10 Dec 2021 22:12:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:6b11bad47b82c2ce735972715400a7436f7db75ed9d702bd4d34d6457621d382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `traefik:v1.7-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull traefik@sha256:6dc156b3fc1fcc1652afb67e7c266f9a96b5edbdf88120cd860afcd03a80d7b3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2736173799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4231ea3f1edf8127f1127d1bdfeffaec3ea5d3c9806a5fb0ec85ba1d7712c78f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Jan 2022 20:20:12 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Thu, 20 Jan 2022 20:20:13 GMT
EXPOSE 80
# Thu, 20 Jan 2022 20:20:14 GMT
ENTRYPOINT ["/traefik"]
# Thu, 20 Jan 2022 20:20:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086785254069d57d991fb33221dcdbddc1bf5ab2f6130b06969c5d28d4b3154c`  
		Last Modified: Thu, 20 Jan 2022 20:21:35 GMT  
		Size: 22.8 MB (22846646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc1bb22ab8ce95752191c8ef1f3fcf32eebda933b25acf756be02d092b83778`  
		Last Modified: Thu, 20 Jan 2022 20:21:29 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37af60424ba83807daa1c78e417c2a0c8f23500bb7b0d7277fef45b1b2203f2e`  
		Last Modified: Thu, 20 Jan 2022 20:21:29 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fbbd099df5a89905425a50883a2d467142413ca693c8e826cfddffa86d6bc5`  
		Last Modified: Thu, 20 Jan 2022 20:21:29 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.34`

```console
$ docker pull traefik@sha256:16ab8f1f8facbfa34f11411735be42ca09cc207f4f607f874c0951659aeac258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.34` - linux; amd64

```console
$ docker pull traefik@sha256:316eeccf5b0e15c7557194096f1b75b8f3ce3de0052c6ebe7c45b005bd53b366
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22612937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7608bd808d08bc0d844935c654371ee6693c80e036ed2c11c4a5ad3178d8e553`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 17:58:25 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Sat, 13 Nov 2021 07:23:46 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 21:32:47 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 10 Dec 2021 21:32:48 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:48 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 21:32:48 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 21:32:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:13e52be55f8d958b3ebb4e73685de5dd10ff4b4af613c4d23424519693aa01e0`  
		Last Modified: Tue, 05 Oct 2021 17:59:12 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a918f6229a44912f657372ae3d390880a3bf6c27e51417a093520abf943f47`  
		Last Modified: Sat, 13 Nov 2021 07:25:13 GMT  
		Size: 328.6 KB (328578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51ca2df8b1b62bfda71acdff9512e649432f7669c2b4f58f50db456c5fa7b5b`  
		Last Modified: Fri, 10 Dec 2021 21:34:00 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4ae8110451cd8b856050c0519b9106085bf2fb213c1810b559effa377cc9176b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21074267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5d0502d4402e86fa35987d85b84ae56e01f0b4054937aea39094c4be01ea6a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 00:02:38 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Sat, 13 Nov 2021 06:52:39 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 21:50:42 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Fri, 10 Dec 2021 21:50:43 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:43 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 21:50:44 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 21:50:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:611185932e68f8b41b94235c966a6c2d26bb4a0f053993c6e49edc01123213f9`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81282f8b9fcf1f821d7dab2ed1f6addbda565118cc5ee95d9de4ae8ff91333f`  
		Last Modified: Sat, 13 Nov 2021 06:55:43 GMT  
		Size: 328.6 KB (328578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3730ee17455103047e8a361f9e99218a36fcfc41b26fb92516fd9be41ba39c`  
		Last Modified: Fri, 10 Dec 2021 21:53:45 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:adc574c52a5b551c4d5ad2be0d2840be3053c2ea51530325497ea3b12cb9f585
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20582290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a34f8b1feaaf314ac5500fe3f4d71ab33659cc44ca8e5389b8eb36d344b19`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 08 Nov 2021 20:23:04 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Mon, 08 Nov 2021 20:23:05 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 22:10:54 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Fri, 10 Dec 2021 22:10:54 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:55 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 22:10:56 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 22:10:57 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:078e101c84a7a75069b9c18efdfc2b24c9840aa136b34eb6e3a0ebe1b74d0a94`  
		Last Modified: Mon, 08 Nov 2021 20:24:37 GMT  
		Size: 122.4 KB (122399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7a624fda7cabc945cc9d9f610f256d933b121fdafa2052d617cf3144bbe2aa`  
		Last Modified: Mon, 08 Nov 2021 20:24:37 GMT  
		Size: 328.5 KB (328545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3ecfc2ff53e207251e72b68f2570d2a5dae382ad897f8ad4c2811e482770d6`  
		Last Modified: Fri, 10 Dec 2021 22:12:29 GMT  
		Size: 20.1 MB (20131346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.34-alpine`

```console
$ docker pull traefik@sha256:36645215a2367d25d1aa9d82a00a3d55b78da3a77f5a742a354c3eee6ca9696e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.34-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:26057fa675bf46c770691d54fa06179744a268643d6d9265a100b33f7616a7fe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25663227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0385562c2ca638c3e56fc5e368e0d760861501c3acb1be07b1ec2ff5f4ec8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:32:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:32:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:32:17 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:32:18 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:32:18 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8fccde93889bb45e3ec014080674609715442d77a83c4e22aed842c54aa320`  
		Last Modified: Fri, 10 Dec 2021 21:33:40 GMT  
		Size: 22.2 MB (22162054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5edab535d879083fbb7bc0569dd3b1588e3ad6549c4ba201eecf74820ad66aa`  
		Last Modified: Fri, 10 Dec 2021 21:33:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d6148854489f78aa02ad57c0ffdf49690f1df5e8419adb2677d1bac979a6b58c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23942165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e476d9b470f0d848b51a66f192af4d51464443367916280dfffa10d7c00efec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:50:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:50:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:50:20 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:50:21 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:50:21 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3379812682fc7d134d4c61b4dc36cfa6924cd554bfed9e11a2ce6927d111484`  
		Last Modified: Fri, 10 Dec 2021 21:53:07 GMT  
		Size: 20.6 MB (20623432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae87b8d30f43743051ca67a1de1aae50831617389e950c804f7267fa8d100ef`  
		Last Modified: Fri, 10 Dec 2021 21:52:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:32a677053c58d48c9176bad0f34a4c615d3f56aa02d5227d6a6bf4405197095d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23529454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968d2aabeb48500d4f5cd1417d792e3589d251ffdffa051738ed4465ca5dedec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 22:10:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 22:10:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 22:10:41 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 22:10:43 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 22:10:44 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2cdc6d798fd61d5f7a4c0530d3cec221698500c821c7c43d03b7ba1956b8ad`  
		Last Modified: Fri, 10 Dec 2021 22:12:07 GMT  
		Size: 20.1 MB (20131378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c1839484effd5cd9538632a7a114e155d1dfa9c0acc3db51242271af684434`  
		Last Modified: Fri, 10 Dec 2021 22:12:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.34-windowsservercore-1809`

```console
$ docker pull traefik@sha256:6b11bad47b82c2ce735972715400a7436f7db75ed9d702bd4d34d6457621d382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `traefik:v1.7.34-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull traefik@sha256:6dc156b3fc1fcc1652afb67e7c266f9a96b5edbdf88120cd860afcd03a80d7b3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2736173799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4231ea3f1edf8127f1127d1bdfeffaec3ea5d3c9806a5fb0ec85ba1d7712c78f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Jan 2022 20:20:12 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Thu, 20 Jan 2022 20:20:13 GMT
EXPOSE 80
# Thu, 20 Jan 2022 20:20:14 GMT
ENTRYPOINT ["/traefik"]
# Thu, 20 Jan 2022 20:20:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086785254069d57d991fb33221dcdbddc1bf5ab2f6130b06969c5d28d4b3154c`  
		Last Modified: Thu, 20 Jan 2022 20:21:35 GMT  
		Size: 22.8 MB (22846646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc1bb22ab8ce95752191c8ef1f3fcf32eebda933b25acf756be02d092b83778`  
		Last Modified: Thu, 20 Jan 2022 20:21:29 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37af60424ba83807daa1c78e417c2a0c8f23500bb7b0d7277fef45b1b2203f2e`  
		Last Modified: Thu, 20 Jan 2022 20:21:29 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fbbd099df5a89905425a50883a2d467142413ca693c8e826cfddffa86d6bc5`  
		Last Modified: Thu, 20 Jan 2022 20:21:29 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.6`

```console
$ docker pull traefik@sha256:425fdedf3b76cd6f8a532889cfd2b949225210bf6dff19c6f7aa9306e11754a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.6` - linux; amd64

```console
$ docker pull traefik@sha256:3540454a0ee471351dc8f874642afbba07ae0eb387c30ca9b57027409bc377ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30340722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb72e139c3d3963f217bf16e6cb197af821ce187a96a16452d0e0bad80861a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 20 Jan 2022 21:55:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc3/traefik_v2.6.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 20 Jan 2022 21:55:32 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 20 Jan 2022 21:55:33 GMT
EXPOSE 80
# Thu, 20 Jan 2022 21:55:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Jan 2022 21:55:33 GMT
CMD ["traefik"]
# Thu, 20 Jan 2022 21:55:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2d15e40ed08c50672c2820538c9dcad4eae1566976b868a66c983230303c14`  
		Last Modified: Thu, 20 Jan 2022 21:56:18 GMT  
		Size: 26.8 MB (26839549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6138b06ac528688b2cf203650e459f6038cf060dcb83aa47168748bc2281751`  
		Last Modified: Thu, 20 Jan 2022 21:56:13 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:34f6e6627e0a0f9a737ee26c4011d53717c2ccd5a93e4536226b26bbea25ee11
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28509493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9b895b4223d0c9b2bbe5f33d94bbd61560d74ed24840ea909f16965cff29d1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 20 Jan 2022 21:14:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc3/traefik_v2.6.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 20 Jan 2022 21:14:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 20 Jan 2022 21:14:40 GMT
EXPOSE 80
# Thu, 20 Jan 2022 21:14:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Jan 2022 21:14:41 GMT
CMD ["traefik"]
# Thu, 20 Jan 2022 21:14:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777ccc4d94ad04ea4b2d8ea281daa48a0b6dfc459a1cb28abb6b1e8e89315865`  
		Last Modified: Thu, 20 Jan 2022 21:17:32 GMT  
		Size: 25.2 MB (25190760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7ab33ace6417d443e7a6d8e494d98c1c2815e761a23365ca6ec3ce2829c31c`  
		Last Modified: Thu, 20 Jan 2022 21:17:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:55fe42ad5db4842e72dc5f4ef11c6b8e9d5c9098d843d363b8198a9aafa5007b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27883145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad74a7e4206e20366bbe215d9a513a1ed5d4a8d6fa048f174ad4e404d92ec2b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 20 Jan 2022 20:41:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc3/traefik_v2.6.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 20 Jan 2022 20:41:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 20 Jan 2022 20:41:46 GMT
EXPOSE 80
# Thu, 20 Jan 2022 20:41:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Jan 2022 20:41:48 GMT
CMD ["traefik"]
# Thu, 20 Jan 2022 20:41:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164cdde581159f519100f7672af7f721fa6214bb8af19b72d9dccdfba81e47cb`  
		Last Modified: Thu, 20 Jan 2022 20:43:02 GMT  
		Size: 24.5 MB (24485069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7f2efbda48f2d261412124526127c9b4315dc85ab5a8e08c92a97c3d7cd066`  
		Last Modified: Thu, 20 Jan 2022 20:42:58 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.6-windowsservercore-1809`

```console
$ docker pull traefik@sha256:56a39e3e1a6fe5fd550a8a1336c25894872c0dc34839db81da2663e6cb1566b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `traefik:v2.6-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull traefik@sha256:1a39c429ce030ea8b2139589b4ba8ac04394df6e6d9535315767e5aaa9385a71
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2740729297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed534d21b80ab2daaaa126d6bee462576099b88189f1832b09461528629f5ab9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Jan 2022 20:17:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.6.0/traefik_v2.6.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 24 Jan 2022 20:17:03 GMT
EXPOSE 80
# Mon, 24 Jan 2022 20:17:04 GMT
ENTRYPOINT ["/traefik"]
# Mon, 24 Jan 2022 20:17:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616132a37689aebcffad1ee520d0c1b885896cbbd641ac3a6657f10102dea775`  
		Last Modified: Mon, 24 Jan 2022 20:17:55 GMT  
		Size: 27.4 MB (27402109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f21934cfc92e23f4ae5fcd28c678568ac61272fcb9926372a431c411f29707`  
		Last Modified: Mon, 24 Jan 2022 20:17:47 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3c1c2283ebd964f4dc8cdee2dd6d9cfd9249714e6a4632c87473bab0cc3c30`  
		Last Modified: Mon, 24 Jan 2022 20:17:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcc3aea18c6fd8c60605fd9add226a7c5b80ded6db1d2605bc5cc2b8b21df0e`  
		Last Modified: Mon, 24 Jan 2022 20:17:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.6.0`

```console
$ docker pull traefik@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `traefik:v2.6.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:56a39e3e1a6fe5fd550a8a1336c25894872c0dc34839db81da2663e6cb1566b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `traefik:v2.6.0-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull traefik@sha256:1a39c429ce030ea8b2139589b4ba8ac04394df6e6d9535315767e5aaa9385a71
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2740729297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed534d21b80ab2daaaa126d6bee462576099b88189f1832b09461528629f5ab9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Jan 2022 20:17:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.6.0/traefik_v2.6.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 24 Jan 2022 20:17:03 GMT
EXPOSE 80
# Mon, 24 Jan 2022 20:17:04 GMT
ENTRYPOINT ["/traefik"]
# Mon, 24 Jan 2022 20:17:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616132a37689aebcffad1ee520d0c1b885896cbbd641ac3a6657f10102dea775`  
		Last Modified: Mon, 24 Jan 2022 20:17:55 GMT  
		Size: 27.4 MB (27402109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f21934cfc92e23f4ae5fcd28c678568ac61272fcb9926372a431c411f29707`  
		Last Modified: Mon, 24 Jan 2022 20:17:47 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3c1c2283ebd964f4dc8cdee2dd6d9cfd9249714e6a4632c87473bab0cc3c30`  
		Last Modified: Mon, 24 Jan 2022 20:17:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcc3aea18c6fd8c60605fd9add226a7c5b80ded6db1d2605bc5cc2b8b21df0e`  
		Last Modified: Mon, 24 Jan 2022 20:17:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:56a39e3e1a6fe5fd550a8a1336c25894872c0dc34839db81da2663e6cb1566b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull traefik@sha256:1a39c429ce030ea8b2139589b4ba8ac04394df6e6d9535315767e5aaa9385a71
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2740729297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed534d21b80ab2daaaa126d6bee462576099b88189f1832b09461528629f5ab9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Jan 2022 20:17:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.6.0/traefik_v2.6.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 24 Jan 2022 20:17:03 GMT
EXPOSE 80
# Mon, 24 Jan 2022 20:17:04 GMT
ENTRYPOINT ["/traefik"]
# Mon, 24 Jan 2022 20:17:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616132a37689aebcffad1ee520d0c1b885896cbbd641ac3a6657f10102dea775`  
		Last Modified: Mon, 24 Jan 2022 20:17:55 GMT  
		Size: 27.4 MB (27402109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f21934cfc92e23f4ae5fcd28c678568ac61272fcb9926372a431c411f29707`  
		Last Modified: Mon, 24 Jan 2022 20:17:47 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3c1c2283ebd964f4dc8cdee2dd6d9cfd9249714e6a4632c87473bab0cc3c30`  
		Last Modified: Mon, 24 Jan 2022 20:17:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcc3aea18c6fd8c60605fd9add226a7c5b80ded6db1d2605bc5cc2b8b21df0e`  
		Last Modified: Mon, 24 Jan 2022 20:17:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
