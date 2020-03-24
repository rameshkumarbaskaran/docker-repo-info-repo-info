<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:1.7`](#traefik17)
-	[`traefik:1.7.23`](#traefik1723)
-	[`traefik:1.7.23-alpine`](#traefik1723-alpine)
-	[`traefik:1.7.23-windowsservercore-1809`](#traefik1723-windowsservercore-1809)
-	[`traefik:1.7-alpine`](#traefik17-alpine)
-	[`traefik:1.7-windowsservercore-1809`](#traefik17-windowsservercore-1809)
-	[`traefik:2.1`](#traefik21)
-	[`traefik:2.1.9`](#traefik219)
-	[`traefik:2.1.9-windowsservercore-1809`](#traefik219-windowsservercore-1809)
-	[`traefik:2.1-windowsservercore-1809`](#traefik21-windowsservercore-1809)
-	[`traefik:2.2`](#traefik22)
-	[`traefik:2.2.0-rc4`](#traefik220-rc4)
-	[`traefik:2.2.0-rc4-windowsservercore-1809`](#traefik220-rc4-windowsservercore-1809)
-	[`traefik:2.2-windowsservercore-1809`](#traefik22-windowsservercore-1809)
-	[`traefik:cantal`](#traefikcantal)
-	[`traefik:cantal-windowsservercore-1809`](#traefikcantal-windowsservercore-1809)
-	[`traefik:chevrotin`](#traefikchevrotin)
-	[`traefik:chevrotin-windowsservercore-1809`](#traefikchevrotin-windowsservercore-1809)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:maroilles`](#traefikmaroilles)
-	[`traefik:maroilles-alpine`](#traefikmaroilles-alpine)
-	[`traefik:maroilles-windowsservercore-1809`](#traefikmaroilles-windowsservercore-1809)
-	[`traefik:v1.7`](#traefikv17)
-	[`traefik:v1.7.23`](#traefikv1723)
-	[`traefik:v1.7.23-alpine`](#traefikv1723-alpine)
-	[`traefik:v1.7.23-windowsservercore-1809`](#traefikv1723-windowsservercore-1809)
-	[`traefik:v1.7-alpine`](#traefikv17-alpine)
-	[`traefik:v1.7-windowsservercore-1809`](#traefikv17-windowsservercore-1809)
-	[`traefik:v2.1`](#traefikv21)
-	[`traefik:v2.1.9`](#traefikv219)
-	[`traefik:v2.1.9-windowsservercore-1809`](#traefikv219-windowsservercore-1809)
-	[`traefik:v2.1-windowsservercore-1809`](#traefikv21-windowsservercore-1809)
-	[`traefik:v2.2`](#traefikv22)
-	[`traefik:v2.2.0-rc4`](#traefikv220-rc4)
-	[`traefik:v2.2.0-rc4-windowsservercore-1809`](#traefikv220-rc4-windowsservercore-1809)
-	[`traefik:v2.2-windowsservercore-1809`](#traefikv22-windowsservercore-1809)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)

## `traefik:1.7`

```console
$ docker pull traefik@sha256:d8d07854fc8123227b916460903ae368a27146108df96a696b08656e5a47b52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7` - linux; amd64

```console
$ docker pull traefik@sha256:3dd7053eaef5072de87162644d4c14b4c6d6f10baa00e9714b9959480c3a8ba2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21578577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d3e8a9c33887f506e928881e765eccd48b8535e63cf04178f8e78c1351b6c8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:27:01 GMT
COPY file:977e3eca412036b63f1f1b09d8388d4e5d6b3535c7af5df64ba18886ed8efd6f in / 
# Mon, 23 Mar 2020 20:27:01 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:27:01 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:27:02 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:27:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e40d0b92fe2d2ef50c6f43f32c33dc117ab26d69a29d74ae15725a379dbde0c2`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 131.7 KB (131682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c068c5049677b6879089396aa0d2d162ac9697e25bacf333c0596a248bae8a5`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 327.4 KB (327376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d33f083e50ccd3f0b3af53d0e2a2c2dca2898906a953c1e2e4b14c530aefe1`  
		Last Modified: Mon, 23 Mar 2020 20:27:37 GMT  
		Size: 21.1 MB (21119519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ad05498d1d177ef22566fa16d1e9256adce71af86013d7eb9b082c1294249899
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20230021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156c24891f895dbc51607c824d2e299ff2ea302df9fc2b8962f5fdd2e4f8b1fb`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 03:46:16 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 03:46:17 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 24 Mar 2020 03:46:21 GMT
COPY file:0a84c8de85d7e943231603655ccecf108fb25302c6ed1f9c6cb4f9e90c926dfb in / 
# Tue, 24 Mar 2020 03:46:22 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:46:23 GMT
VOLUME [/tmp]
# Tue, 24 Mar 2020 03:46:24 GMT
ENTRYPOINT ["/traefik"]
# Tue, 24 Mar 2020 03:46:24 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3ea78b0360c0223e83ecbb7336ab0de873d099e2aa889216bc3622c7dc315adc`  
		Last Modified: Tue, 24 Mar 2020 03:47:54 GMT  
		Size: 131.7 KB (131681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd374e140760994a9274b43e4cbf314b61a77acb227eca705d35780bb33a6a07`  
		Last Modified: Tue, 24 Mar 2020 03:47:55 GMT  
		Size: 327.4 KB (327405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e556ef2bd973f47fadf08d98f358fd091604a1de5409cf4a7cc8d3187623d3`  
		Last Modified: Tue, 24 Mar 2020 03:48:03 GMT  
		Size: 19.8 MB (19770935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f6a41eb9ec2b3294c6a1a65cd25e440c6f2b07a4af0b644d08c73045ae9c821c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19950885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9fd16d96e8adc131956fc884a01f9e45e2adafad71b15083c3ae764b799ee9c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 05:55:25 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 05:55:26 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 24 Mar 2020 05:55:28 GMT
COPY file:a3694a993cf25306aff467c03d4f70f02c07bff1afad394515f87b732cdab043 in / 
# Tue, 24 Mar 2020 05:55:29 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:55:29 GMT
VOLUME [/tmp]
# Tue, 24 Mar 2020 05:55:30 GMT
ENTRYPOINT ["/traefik"]
# Tue, 24 Mar 2020 05:55:31 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:58ceb9a2a8ba9dd83eef0c2cf887c175911b301df486d142f7d09293605add22`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 131.7 KB (131676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b9edf48787b0368bb1af04734041d3b374acefa70417bdf0090919056c874d`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 327.4 KB (327402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8802a35e2e74e1dcf82490548042848f15ea48357d7f9c232231f94cda68ef`  
		Last Modified: Tue, 24 Mar 2020 05:56:49 GMT  
		Size: 19.5 MB (19491807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.23`

```console
$ docker pull traefik@sha256:d8d07854fc8123227b916460903ae368a27146108df96a696b08656e5a47b52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.23` - linux; amd64

```console
$ docker pull traefik@sha256:3dd7053eaef5072de87162644d4c14b4c6d6f10baa00e9714b9959480c3a8ba2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21578577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d3e8a9c33887f506e928881e765eccd48b8535e63cf04178f8e78c1351b6c8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:27:01 GMT
COPY file:977e3eca412036b63f1f1b09d8388d4e5d6b3535c7af5df64ba18886ed8efd6f in / 
# Mon, 23 Mar 2020 20:27:01 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:27:01 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:27:02 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:27:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e40d0b92fe2d2ef50c6f43f32c33dc117ab26d69a29d74ae15725a379dbde0c2`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 131.7 KB (131682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c068c5049677b6879089396aa0d2d162ac9697e25bacf333c0596a248bae8a5`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 327.4 KB (327376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d33f083e50ccd3f0b3af53d0e2a2c2dca2898906a953c1e2e4b14c530aefe1`  
		Last Modified: Mon, 23 Mar 2020 20:27:37 GMT  
		Size: 21.1 MB (21119519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.23` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ad05498d1d177ef22566fa16d1e9256adce71af86013d7eb9b082c1294249899
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20230021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156c24891f895dbc51607c824d2e299ff2ea302df9fc2b8962f5fdd2e4f8b1fb`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 03:46:16 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 03:46:17 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 24 Mar 2020 03:46:21 GMT
COPY file:0a84c8de85d7e943231603655ccecf108fb25302c6ed1f9c6cb4f9e90c926dfb in / 
# Tue, 24 Mar 2020 03:46:22 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:46:23 GMT
VOLUME [/tmp]
# Tue, 24 Mar 2020 03:46:24 GMT
ENTRYPOINT ["/traefik"]
# Tue, 24 Mar 2020 03:46:24 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3ea78b0360c0223e83ecbb7336ab0de873d099e2aa889216bc3622c7dc315adc`  
		Last Modified: Tue, 24 Mar 2020 03:47:54 GMT  
		Size: 131.7 KB (131681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd374e140760994a9274b43e4cbf314b61a77acb227eca705d35780bb33a6a07`  
		Last Modified: Tue, 24 Mar 2020 03:47:55 GMT  
		Size: 327.4 KB (327405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e556ef2bd973f47fadf08d98f358fd091604a1de5409cf4a7cc8d3187623d3`  
		Last Modified: Tue, 24 Mar 2020 03:48:03 GMT  
		Size: 19.8 MB (19770935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.23` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f6a41eb9ec2b3294c6a1a65cd25e440c6f2b07a4af0b644d08c73045ae9c821c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19950885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9fd16d96e8adc131956fc884a01f9e45e2adafad71b15083c3ae764b799ee9c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 05:55:25 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 05:55:26 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 24 Mar 2020 05:55:28 GMT
COPY file:a3694a993cf25306aff467c03d4f70f02c07bff1afad394515f87b732cdab043 in / 
# Tue, 24 Mar 2020 05:55:29 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:55:29 GMT
VOLUME [/tmp]
# Tue, 24 Mar 2020 05:55:30 GMT
ENTRYPOINT ["/traefik"]
# Tue, 24 Mar 2020 05:55:31 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:58ceb9a2a8ba9dd83eef0c2cf887c175911b301df486d142f7d09293605add22`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 131.7 KB (131676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b9edf48787b0368bb1af04734041d3b374acefa70417bdf0090919056c874d`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 327.4 KB (327402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8802a35e2e74e1dcf82490548042848f15ea48357d7f9c232231f94cda68ef`  
		Last Modified: Tue, 24 Mar 2020 05:56:49 GMT  
		Size: 19.5 MB (19491807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.23-alpine`

```console
$ docker pull traefik@sha256:87ec78321c9af542f8bd0b58299d7bad96740e24fb3fab8e50a146b2952f283f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.23-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:46c4281b4bb6882eff0d972b7c2c9cbaba69c6fc66074058b660268404a27c7a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24617484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afc1d9db6d8fa6572e0313edb7e41f57a5ba4ec2d2322b2934e25eb81b7417b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:19 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:20 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:21 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41bdc4cb62d692fefe850ea163c318db37fbba75755b78932d1e43492d0b29d`  
		Last Modified: Mon, 23 Mar 2020 23:47:34 GMT  
		Size: 21.1 MB (21119717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a70748d348ef256993ee5cffc84cf0f40f2b1e1713952299e986d373d12811`  
		Last Modified: Mon, 23 Mar 2020 23:47:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.23-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:9708bb38140b19e258179c0e7886e6b8551a1cc1f6507d0899505fa573b8a3a1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23088000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30bf0f95111027bbafdf5e4e1359007f64b69883b904adefa37a0ee515ac8a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 03:43:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 03:44:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 03:44:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 03:44:34 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:44:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 03:44:35 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 03:44:36 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b73c299e24e9aa32bbbec493b7588c3a6592d11b52ccb01c156037b819aef46`  
		Last Modified: Tue, 24 Mar 2020 03:47:03 GMT  
		Size: 698.1 KB (698067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80eaea1c33d2ec522e729ccc1f058ccfba9d7e66158f435004d333626b62e79`  
		Last Modified: Tue, 24 Mar 2020 03:47:45 GMT  
		Size: 19.8 MB (19770986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d46bd54705ee81f39ce737c02dbc6ba461ebf69507a39aea7592a29250dd7ac`  
		Last Modified: Tue, 24 Mar 2020 03:47:43 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.23-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:0d134b143eec517177fdd9df79aaa4a11e7fe98283b502ff4eb73097f710d786
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22911680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004d9bce1ce8133ee2ed61502f6db556dd1d485b479e7c6ba6a7b6881ce7fae3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 05:53:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 05:53:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 05:53:16 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:53:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 05:53:17 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 05:53:17 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba236ca9140213ef04f6289ffeb9778d10fe5a35cb7fa09ec3b67581e9dd31d`  
		Last Modified: Tue, 24 Mar 2020 05:56:32 GMT  
		Size: 19.5 MB (19491989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfb55492bb3451bea3761bd98a63749a7a3f6fed739d7949c9967c3d5b5d386`  
		Last Modified: Tue, 24 Mar 2020 05:56:25 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.23-windowsservercore-1809`

```console
$ docker pull traefik@sha256:28a158cbb1f498399673e62f4b77b5fc6abf59324564397ef0b7c19430ca8cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:1.7.23-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:44fc6778ad6b2ddb0bdcddb9561019c5fc9595c265060a07291a12f4cbe49b44
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291142670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4919c09dd96ca89d1f3b47d479f9bf17813c7f78fa7762a1a58b29b97ed5375`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:32:24 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Mon, 23 Mar 2020 21:32:28 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:32:29 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:32:30 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b00e8e040906f3d887b30e678e40efb35c177517d3ab7885312a259fc4cd60`  
		Last Modified: Mon, 23 Mar 2020 21:33:27 GMT  
		Size: 25.8 MB (25801749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b74468fd780764620b22dd13d3c2ad380a2f4b8038f52ed9bea45b29c3e5b`  
		Last Modified: Mon, 23 Mar 2020 21:33:22 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac07893895096293dc66362aaef0ba3fa38751d015265b3c1df0cd9122d7531`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3023a9d8dd0513c3a0f98d6ff8af04fad6fb178de50458b5a9c75acf3963721`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-alpine`

```console
$ docker pull traefik@sha256:87ec78321c9af542f8bd0b58299d7bad96740e24fb3fab8e50a146b2952f283f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:46c4281b4bb6882eff0d972b7c2c9cbaba69c6fc66074058b660268404a27c7a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24617484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afc1d9db6d8fa6572e0313edb7e41f57a5ba4ec2d2322b2934e25eb81b7417b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:19 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:20 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:21 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41bdc4cb62d692fefe850ea163c318db37fbba75755b78932d1e43492d0b29d`  
		Last Modified: Mon, 23 Mar 2020 23:47:34 GMT  
		Size: 21.1 MB (21119717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a70748d348ef256993ee5cffc84cf0f40f2b1e1713952299e986d373d12811`  
		Last Modified: Mon, 23 Mar 2020 23:47:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:9708bb38140b19e258179c0e7886e6b8551a1cc1f6507d0899505fa573b8a3a1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23088000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30bf0f95111027bbafdf5e4e1359007f64b69883b904adefa37a0ee515ac8a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 03:43:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 03:44:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 03:44:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 03:44:34 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:44:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 03:44:35 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 03:44:36 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b73c299e24e9aa32bbbec493b7588c3a6592d11b52ccb01c156037b819aef46`  
		Last Modified: Tue, 24 Mar 2020 03:47:03 GMT  
		Size: 698.1 KB (698067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80eaea1c33d2ec522e729ccc1f058ccfba9d7e66158f435004d333626b62e79`  
		Last Modified: Tue, 24 Mar 2020 03:47:45 GMT  
		Size: 19.8 MB (19770986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d46bd54705ee81f39ce737c02dbc6ba461ebf69507a39aea7592a29250dd7ac`  
		Last Modified: Tue, 24 Mar 2020 03:47:43 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:0d134b143eec517177fdd9df79aaa4a11e7fe98283b502ff4eb73097f710d786
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22911680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004d9bce1ce8133ee2ed61502f6db556dd1d485b479e7c6ba6a7b6881ce7fae3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 05:53:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 05:53:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 05:53:16 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:53:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 05:53:17 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 05:53:17 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba236ca9140213ef04f6289ffeb9778d10fe5a35cb7fa09ec3b67581e9dd31d`  
		Last Modified: Tue, 24 Mar 2020 05:56:32 GMT  
		Size: 19.5 MB (19491989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfb55492bb3451bea3761bd98a63749a7a3f6fed739d7949c9967c3d5b5d386`  
		Last Modified: Tue, 24 Mar 2020 05:56:25 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:28a158cbb1f498399673e62f4b77b5fc6abf59324564397ef0b7c19430ca8cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:1.7-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:44fc6778ad6b2ddb0bdcddb9561019c5fc9595c265060a07291a12f4cbe49b44
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291142670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4919c09dd96ca89d1f3b47d479f9bf17813c7f78fa7762a1a58b29b97ed5375`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:32:24 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Mon, 23 Mar 2020 21:32:28 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:32:29 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:32:30 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b00e8e040906f3d887b30e678e40efb35c177517d3ab7885312a259fc4cd60`  
		Last Modified: Mon, 23 Mar 2020 21:33:27 GMT  
		Size: 25.8 MB (25801749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b74468fd780764620b22dd13d3c2ad380a2f4b8038f52ed9bea45b29c3e5b`  
		Last Modified: Mon, 23 Mar 2020 21:33:22 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac07893895096293dc66362aaef0ba3fa38751d015265b3c1df0cd9122d7531`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3023a9d8dd0513c3a0f98d6ff8af04fad6fb178de50458b5a9c75acf3963721`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.1`

```console
$ docker pull traefik@sha256:ab83baa3d198ee5a2fd685bed96417055a2bdd271efe11a0b831d6c02436aabd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.1` - linux; amd64

```console
$ docker pull traefik@sha256:0f877111f469c6843a3e18d181dc2eaeecaca5cf4dfa8538cb534be2e2806ce1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22719782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bfc37343a47ef437767e7f10ec6c47b5dfb7d5a7fde99a78063f0217b6edfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:07 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:08 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780c440cb354cd104d66dca36ad5f5e924dbbf0baacd588406f7635c48569fab`  
		Last Modified: Mon, 23 Mar 2020 23:47:22 GMT  
		Size: 19.2 MB (19222015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89f3c2e369bd1b3dbdfb399a0d6c9f5e8d9b595ab26c6ad4d3ec5cee06cc771`  
		Last Modified: Mon, 23 Mar 2020 23:47:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:c6a38950d8f392d4ccedea121fb6b59f79e3468f04fe005b2946da8d7d33a95a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21362283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7ab131d970b368d0b6c84a678dae3dd68d40e3fbffdc27ce055270e82377fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 03:43:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 03:44:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 03:44:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 03:44:19 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:44:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 03:44:21 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 03:44:21 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b73c299e24e9aa32bbbec493b7588c3a6592d11b52ccb01c156037b819aef46`  
		Last Modified: Tue, 24 Mar 2020 03:47:03 GMT  
		Size: 698.1 KB (698067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0faaabb70feaf46fc30c623ca581dd5a603309378073aefb34021408fbaeca27`  
		Last Modified: Tue, 24 Mar 2020 03:47:27 GMT  
		Size: 18.0 MB (18045269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96986412029c005a604e02811ee63c2972698683e34ba39979d6b483b33fe185`  
		Last Modified: Tue, 24 Mar 2020 03:47:20 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e303a3b44ed8884b51de268bd4c990087cbc08139e0be4d4d139032083706b01
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21167159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d182f8822a3701b3c590176311bd202687d1dee46b684a850f05bc25f9780e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 05:53:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 05:53:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 05:53:04 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:53:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 05:53:05 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 05:53:06 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb068a5ae768db846d4cffd6d8a07b00341712cc95b28925ffd386be29ad6da5`  
		Last Modified: Tue, 24 Mar 2020 05:56:14 GMT  
		Size: 17.7 MB (17747468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de178e83d0b4ec78b825872546d5376d07eb016394af195f7322b609c2c84c2a`  
		Last Modified: Tue, 24 Mar 2020 05:56:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.1.9`

```console
$ docker pull traefik@sha256:ab83baa3d198ee5a2fd685bed96417055a2bdd271efe11a0b831d6c02436aabd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.1.9` - linux; amd64

```console
$ docker pull traefik@sha256:0f877111f469c6843a3e18d181dc2eaeecaca5cf4dfa8538cb534be2e2806ce1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22719782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bfc37343a47ef437767e7f10ec6c47b5dfb7d5a7fde99a78063f0217b6edfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:07 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:08 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780c440cb354cd104d66dca36ad5f5e924dbbf0baacd588406f7635c48569fab`  
		Last Modified: Mon, 23 Mar 2020 23:47:22 GMT  
		Size: 19.2 MB (19222015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89f3c2e369bd1b3dbdfb399a0d6c9f5e8d9b595ab26c6ad4d3ec5cee06cc771`  
		Last Modified: Mon, 23 Mar 2020 23:47:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.1.9` - linux; arm variant v6

```console
$ docker pull traefik@sha256:c6a38950d8f392d4ccedea121fb6b59f79e3468f04fe005b2946da8d7d33a95a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21362283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7ab131d970b368d0b6c84a678dae3dd68d40e3fbffdc27ce055270e82377fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 03:43:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 03:44:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 03:44:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 03:44:19 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:44:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 03:44:21 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 03:44:21 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b73c299e24e9aa32bbbec493b7588c3a6592d11b52ccb01c156037b819aef46`  
		Last Modified: Tue, 24 Mar 2020 03:47:03 GMT  
		Size: 698.1 KB (698067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0faaabb70feaf46fc30c623ca581dd5a603309378073aefb34021408fbaeca27`  
		Last Modified: Tue, 24 Mar 2020 03:47:27 GMT  
		Size: 18.0 MB (18045269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96986412029c005a604e02811ee63c2972698683e34ba39979d6b483b33fe185`  
		Last Modified: Tue, 24 Mar 2020 03:47:20 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.1.9` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e303a3b44ed8884b51de268bd4c990087cbc08139e0be4d4d139032083706b01
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21167159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d182f8822a3701b3c590176311bd202687d1dee46b684a850f05bc25f9780e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 05:53:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 05:53:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 05:53:04 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:53:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 05:53:05 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 05:53:06 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb068a5ae768db846d4cffd6d8a07b00341712cc95b28925ffd386be29ad6da5`  
		Last Modified: Tue, 24 Mar 2020 05:56:14 GMT  
		Size: 17.7 MB (17747468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de178e83d0b4ec78b825872546d5376d07eb016394af195f7322b609c2c84c2a`  
		Last Modified: Tue, 24 Mar 2020 05:56:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.1.9-windowsservercore-1809`

```console
$ docker pull traefik@sha256:426da4e134080b1ad724038a856a4cafabaff316e490d221f898d3c6a3584a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:2.1.9-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:85934211df41d1946d9277304658f788ce4fdaa568bb130cd5978c9a7128aa00
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289298644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991a23a2835a6c3a3b9c9308404203c7a48eb7c61127bc0d08404f6ea6fcac0b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:31:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Mar 2020 21:31:26 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:31:27 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:31:28 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f80b3ae1536653ce370f049d76fd558fc18a69697f5c9a0208ed8dbdfd30475`  
		Last Modified: Mon, 23 Mar 2020 21:33:03 GMT  
		Size: 24.0 MB (23957752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e3dbb3d1da32a0307e35df54c13379b326d3f966599877c8192ffc10c444d3`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe22549283bca4c11332825e6dae34e308420cd54afadaec8140e55183cc763`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9cd238ed825cbc292541dd9f8cfb82f9ee5ba2999bede775a3f051ed89733`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.1-windowsservercore-1809`

```console
$ docker pull traefik@sha256:426da4e134080b1ad724038a856a4cafabaff316e490d221f898d3c6a3584a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:2.1-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:85934211df41d1946d9277304658f788ce4fdaa568bb130cd5978c9a7128aa00
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289298644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991a23a2835a6c3a3b9c9308404203c7a48eb7c61127bc0d08404f6ea6fcac0b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:31:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Mar 2020 21:31:26 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:31:27 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:31:28 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f80b3ae1536653ce370f049d76fd558fc18a69697f5c9a0208ed8dbdfd30475`  
		Last Modified: Mon, 23 Mar 2020 21:33:03 GMT  
		Size: 24.0 MB (23957752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e3dbb3d1da32a0307e35df54c13379b326d3f966599877c8192ffc10c444d3`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe22549283bca4c11332825e6dae34e308420cd54afadaec8140e55183cc763`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9cd238ed825cbc292541dd9f8cfb82f9ee5ba2999bede775a3f051ed89733`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.2`

```console
$ docker pull traefik@sha256:723fc9db3de3432ad5f7d9596074cc47080e960ba81e7d8181bb1c682b564f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.2` - linux; amd64

```console
$ docker pull traefik@sha256:ea85c9c3a5d1c1e5b84769e14f17bf9e505cc8f0719cce800b61e10cd67d4101
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24780053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b552cb4ae6598187cd5353e0db70314afe2dc07f7596120f3a99a884f1fe76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:45:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:45:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:45:55 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:45:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:45:56 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:45:56 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f368fd862d907340d21e551d6fa5d97176b88b2ae3c92c28af55d8d7dc0a316`  
		Last Modified: Mon, 23 Mar 2020 23:47:09 GMT  
		Size: 21.3 MB (21282286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5b29ae28cf739aec30a2128fa715c59ac327ae5b127a2b270ab73141ca1b6f`  
		Last Modified: Mon, 23 Mar 2020 23:47:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fd374b0c80939d157f7d87f913715e2329b4acc5f97f4157f985403baed0b97f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23305628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7442444ce9e74ba3c02660c7be76ddcee26f9df3d7987214d171783c899705f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 03:43:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 03:44:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 03:44:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 03:44:05 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:44:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 03:44:07 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 03:44:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b73c299e24e9aa32bbbec493b7588c3a6592d11b52ccb01c156037b819aef46`  
		Last Modified: Tue, 24 Mar 2020 03:47:03 GMT  
		Size: 698.1 KB (698067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a54d3a262f9749f5dd0e62870a09217792ce6fe6d332fccbe96e75eac720a05`  
		Last Modified: Tue, 24 Mar 2020 03:47:10 GMT  
		Size: 20.0 MB (19988615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc68d67aafd345f029a6469144e76ad9b015c017cffa21e4cc27a31a961b943`  
		Last Modified: Tue, 24 Mar 2020 03:47:04 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:810c80e42a51505b352fa40c49fc6f47d18daa15a9a06a037b2c77c4a1da909d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23052200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31574eaabcda934879fd354a8aaaad034b96cb836bcb385f3eaba8e00ef68e50`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 05:52:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 05:52:52 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 05:52:53 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:52:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 05:52:54 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 05:52:54 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5601e5e68ec3f28b097b71055aad3c3b78a6c2a1748e218c6547797917153671`  
		Last Modified: Tue, 24 Mar 2020 05:55:59 GMT  
		Size: 19.6 MB (19632509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681e03de8125baca253f2686a970056c714325b611de9769dcd1829ef9e77b8f`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.2.0-rc4`

```console
$ docker pull traefik@sha256:723fc9db3de3432ad5f7d9596074cc47080e960ba81e7d8181bb1c682b564f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.2.0-rc4` - linux; amd64

```console
$ docker pull traefik@sha256:ea85c9c3a5d1c1e5b84769e14f17bf9e505cc8f0719cce800b61e10cd67d4101
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24780053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b552cb4ae6598187cd5353e0db70314afe2dc07f7596120f3a99a884f1fe76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:45:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:45:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:45:55 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:45:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:45:56 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:45:56 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f368fd862d907340d21e551d6fa5d97176b88b2ae3c92c28af55d8d7dc0a316`  
		Last Modified: Mon, 23 Mar 2020 23:47:09 GMT  
		Size: 21.3 MB (21282286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5b29ae28cf739aec30a2128fa715c59ac327ae5b127a2b270ab73141ca1b6f`  
		Last Modified: Mon, 23 Mar 2020 23:47:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.2.0-rc4` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fd374b0c80939d157f7d87f913715e2329b4acc5f97f4157f985403baed0b97f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23305628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7442444ce9e74ba3c02660c7be76ddcee26f9df3d7987214d171783c899705f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 03:43:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 03:44:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 03:44:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 03:44:05 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:44:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 03:44:07 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 03:44:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b73c299e24e9aa32bbbec493b7588c3a6592d11b52ccb01c156037b819aef46`  
		Last Modified: Tue, 24 Mar 2020 03:47:03 GMT  
		Size: 698.1 KB (698067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a54d3a262f9749f5dd0e62870a09217792ce6fe6d332fccbe96e75eac720a05`  
		Last Modified: Tue, 24 Mar 2020 03:47:10 GMT  
		Size: 20.0 MB (19988615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc68d67aafd345f029a6469144e76ad9b015c017cffa21e4cc27a31a961b943`  
		Last Modified: Tue, 24 Mar 2020 03:47:04 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.2.0-rc4` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:810c80e42a51505b352fa40c49fc6f47d18daa15a9a06a037b2c77c4a1da909d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23052200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31574eaabcda934879fd354a8aaaad034b96cb836bcb385f3eaba8e00ef68e50`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 05:52:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 05:52:52 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 05:52:53 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:52:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 05:52:54 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 05:52:54 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5601e5e68ec3f28b097b71055aad3c3b78a6c2a1748e218c6547797917153671`  
		Last Modified: Tue, 24 Mar 2020 05:55:59 GMT  
		Size: 19.6 MB (19632509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681e03de8125baca253f2686a970056c714325b611de9769dcd1829ef9e77b8f`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.2.0-rc4-windowsservercore-1809`

```console
$ docker pull traefik@sha256:10b613c0d809a2f32e3f1f05a4d1bf8948740b300edc48c0db647d89ded615a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:2.2.0-rc4-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:be5249e8a1f004bc3b704f5f678a716baeb1e02cbabf159eb439b82457d3cadf
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291275576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e276e79ace0d8ef3779cc569768475cf7763dcb4753b2da424149790667851c1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Mar 2020 23:40:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 19 Mar 2020 23:41:01 GMT
EXPOSE 80
# Thu, 19 Mar 2020 23:41:02 GMT
ENTRYPOINT ["/traefik"]
# Thu, 19 Mar 2020 23:41:03 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549f06fe79c6ff9fe97ad90025e8fa1f62dc9cc3b2d1a223c2be32e8e944ff9e`  
		Last Modified: Thu, 19 Mar 2020 23:42:30 GMT  
		Size: 25.9 MB (25934473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465d2f7acd904d7ca8da43eb4cdd73475b80ccce5ba79a88d9968266c4bad07f`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809f97326d00cd242ff10557bd548b8db16c340fd5d7fc274f3282623f542bbb`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e27a6ecc6db484f65e2587cb61e379ddb398f17469e292905230bc60e36fc04`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:10b613c0d809a2f32e3f1f05a4d1bf8948740b300edc48c0db647d89ded615a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:2.2-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:be5249e8a1f004bc3b704f5f678a716baeb1e02cbabf159eb439b82457d3cadf
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291275576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e276e79ace0d8ef3779cc569768475cf7763dcb4753b2da424149790667851c1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Mar 2020 23:40:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 19 Mar 2020 23:41:01 GMT
EXPOSE 80
# Thu, 19 Mar 2020 23:41:02 GMT
ENTRYPOINT ["/traefik"]
# Thu, 19 Mar 2020 23:41:03 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549f06fe79c6ff9fe97ad90025e8fa1f62dc9cc3b2d1a223c2be32e8e944ff9e`  
		Last Modified: Thu, 19 Mar 2020 23:42:30 GMT  
		Size: 25.9 MB (25934473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465d2f7acd904d7ca8da43eb4cdd73475b80ccce5ba79a88d9968266c4bad07f`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809f97326d00cd242ff10557bd548b8db16c340fd5d7fc274f3282623f542bbb`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e27a6ecc6db484f65e2587cb61e379ddb398f17469e292905230bc60e36fc04`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:cantal`

```console
$ docker pull traefik@sha256:ab83baa3d198ee5a2fd685bed96417055a2bdd271efe11a0b831d6c02436aabd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:cantal` - linux; amd64

```console
$ docker pull traefik@sha256:0f877111f469c6843a3e18d181dc2eaeecaca5cf4dfa8538cb534be2e2806ce1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22719782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bfc37343a47ef437767e7f10ec6c47b5dfb7d5a7fde99a78063f0217b6edfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:07 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:08 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780c440cb354cd104d66dca36ad5f5e924dbbf0baacd588406f7635c48569fab`  
		Last Modified: Mon, 23 Mar 2020 23:47:22 GMT  
		Size: 19.2 MB (19222015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89f3c2e369bd1b3dbdfb399a0d6c9f5e8d9b595ab26c6ad4d3ec5cee06cc771`  
		Last Modified: Mon, 23 Mar 2020 23:47:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:cantal` - linux; arm variant v6

```console
$ docker pull traefik@sha256:c6a38950d8f392d4ccedea121fb6b59f79e3468f04fe005b2946da8d7d33a95a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21362283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7ab131d970b368d0b6c84a678dae3dd68d40e3fbffdc27ce055270e82377fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 03:43:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 03:44:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 03:44:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 03:44:19 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:44:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 03:44:21 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 03:44:21 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b73c299e24e9aa32bbbec493b7588c3a6592d11b52ccb01c156037b819aef46`  
		Last Modified: Tue, 24 Mar 2020 03:47:03 GMT  
		Size: 698.1 KB (698067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0faaabb70feaf46fc30c623ca581dd5a603309378073aefb34021408fbaeca27`  
		Last Modified: Tue, 24 Mar 2020 03:47:27 GMT  
		Size: 18.0 MB (18045269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96986412029c005a604e02811ee63c2972698683e34ba39979d6b483b33fe185`  
		Last Modified: Tue, 24 Mar 2020 03:47:20 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:cantal` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e303a3b44ed8884b51de268bd4c990087cbc08139e0be4d4d139032083706b01
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21167159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d182f8822a3701b3c590176311bd202687d1dee46b684a850f05bc25f9780e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 05:53:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 05:53:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 05:53:04 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:53:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 05:53:05 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 05:53:06 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb068a5ae768db846d4cffd6d8a07b00341712cc95b28925ffd386be29ad6da5`  
		Last Modified: Tue, 24 Mar 2020 05:56:14 GMT  
		Size: 17.7 MB (17747468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de178e83d0b4ec78b825872546d5376d07eb016394af195f7322b609c2c84c2a`  
		Last Modified: Tue, 24 Mar 2020 05:56:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:cantal-windowsservercore-1809`

```console
$ docker pull traefik@sha256:426da4e134080b1ad724038a856a4cafabaff316e490d221f898d3c6a3584a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:cantal-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:85934211df41d1946d9277304658f788ce4fdaa568bb130cd5978c9a7128aa00
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289298644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991a23a2835a6c3a3b9c9308404203c7a48eb7c61127bc0d08404f6ea6fcac0b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:31:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Mar 2020 21:31:26 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:31:27 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:31:28 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f80b3ae1536653ce370f049d76fd558fc18a69697f5c9a0208ed8dbdfd30475`  
		Last Modified: Mon, 23 Mar 2020 21:33:03 GMT  
		Size: 24.0 MB (23957752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e3dbb3d1da32a0307e35df54c13379b326d3f966599877c8192ffc10c444d3`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe22549283bca4c11332825e6dae34e308420cd54afadaec8140e55183cc763`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9cd238ed825cbc292541dd9f8cfb82f9ee5ba2999bede775a3f051ed89733`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chevrotin`

```console
$ docker pull traefik@sha256:723fc9db3de3432ad5f7d9596074cc47080e960ba81e7d8181bb1c682b564f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:chevrotin` - linux; amd64

```console
$ docker pull traefik@sha256:ea85c9c3a5d1c1e5b84769e14f17bf9e505cc8f0719cce800b61e10cd67d4101
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24780053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b552cb4ae6598187cd5353e0db70314afe2dc07f7596120f3a99a884f1fe76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:45:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:45:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:45:55 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:45:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:45:56 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:45:56 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f368fd862d907340d21e551d6fa5d97176b88b2ae3c92c28af55d8d7dc0a316`  
		Last Modified: Mon, 23 Mar 2020 23:47:09 GMT  
		Size: 21.3 MB (21282286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5b29ae28cf739aec30a2128fa715c59ac327ae5b127a2b270ab73141ca1b6f`  
		Last Modified: Mon, 23 Mar 2020 23:47:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:chevrotin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fd374b0c80939d157f7d87f913715e2329b4acc5f97f4157f985403baed0b97f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23305628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7442444ce9e74ba3c02660c7be76ddcee26f9df3d7987214d171783c899705f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 03:43:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 03:44:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 03:44:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 03:44:05 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:44:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 03:44:07 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 03:44:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b73c299e24e9aa32bbbec493b7588c3a6592d11b52ccb01c156037b819aef46`  
		Last Modified: Tue, 24 Mar 2020 03:47:03 GMT  
		Size: 698.1 KB (698067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a54d3a262f9749f5dd0e62870a09217792ce6fe6d332fccbe96e75eac720a05`  
		Last Modified: Tue, 24 Mar 2020 03:47:10 GMT  
		Size: 20.0 MB (19988615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc68d67aafd345f029a6469144e76ad9b015c017cffa21e4cc27a31a961b943`  
		Last Modified: Tue, 24 Mar 2020 03:47:04 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:chevrotin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:810c80e42a51505b352fa40c49fc6f47d18daa15a9a06a037b2c77c4a1da909d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23052200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31574eaabcda934879fd354a8aaaad034b96cb836bcb385f3eaba8e00ef68e50`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 05:52:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 05:52:52 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 05:52:53 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:52:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 05:52:54 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 05:52:54 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5601e5e68ec3f28b097b71055aad3c3b78a6c2a1748e218c6547797917153671`  
		Last Modified: Tue, 24 Mar 2020 05:55:59 GMT  
		Size: 19.6 MB (19632509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681e03de8125baca253f2686a970056c714325b611de9769dcd1829ef9e77b8f`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chevrotin-windowsservercore-1809`

```console
$ docker pull traefik@sha256:10b613c0d809a2f32e3f1f05a4d1bf8948740b300edc48c0db647d89ded615a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:chevrotin-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:be5249e8a1f004bc3b704f5f678a716baeb1e02cbabf159eb439b82457d3cadf
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291275576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e276e79ace0d8ef3779cc569768475cf7763dcb4753b2da424149790667851c1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Mar 2020 23:40:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 19 Mar 2020 23:41:01 GMT
EXPOSE 80
# Thu, 19 Mar 2020 23:41:02 GMT
ENTRYPOINT ["/traefik"]
# Thu, 19 Mar 2020 23:41:03 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549f06fe79c6ff9fe97ad90025e8fa1f62dc9cc3b2d1a223c2be32e8e944ff9e`  
		Last Modified: Thu, 19 Mar 2020 23:42:30 GMT  
		Size: 25.9 MB (25934473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465d2f7acd904d7ca8da43eb4cdd73475b80ccce5ba79a88d9968266c4bad07f`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809f97326d00cd242ff10557bd548b8db16c340fd5d7fc274f3282623f542bbb`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e27a6ecc6db484f65e2587cb61e379ddb398f17469e292905230bc60e36fc04`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:ab83baa3d198ee5a2fd685bed96417055a2bdd271efe11a0b831d6c02436aabd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:0f877111f469c6843a3e18d181dc2eaeecaca5cf4dfa8538cb534be2e2806ce1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22719782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bfc37343a47ef437767e7f10ec6c47b5dfb7d5a7fde99a78063f0217b6edfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:07 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:08 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780c440cb354cd104d66dca36ad5f5e924dbbf0baacd588406f7635c48569fab`  
		Last Modified: Mon, 23 Mar 2020 23:47:22 GMT  
		Size: 19.2 MB (19222015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89f3c2e369bd1b3dbdfb399a0d6c9f5e8d9b595ab26c6ad4d3ec5cee06cc771`  
		Last Modified: Mon, 23 Mar 2020 23:47:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:c6a38950d8f392d4ccedea121fb6b59f79e3468f04fe005b2946da8d7d33a95a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21362283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7ab131d970b368d0b6c84a678dae3dd68d40e3fbffdc27ce055270e82377fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 03:43:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 03:44:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 03:44:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 03:44:19 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:44:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 03:44:21 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 03:44:21 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b73c299e24e9aa32bbbec493b7588c3a6592d11b52ccb01c156037b819aef46`  
		Last Modified: Tue, 24 Mar 2020 03:47:03 GMT  
		Size: 698.1 KB (698067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0faaabb70feaf46fc30c623ca581dd5a603309378073aefb34021408fbaeca27`  
		Last Modified: Tue, 24 Mar 2020 03:47:27 GMT  
		Size: 18.0 MB (18045269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96986412029c005a604e02811ee63c2972698683e34ba39979d6b483b33fe185`  
		Last Modified: Tue, 24 Mar 2020 03:47:20 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e303a3b44ed8884b51de268bd4c990087cbc08139e0be4d4d139032083706b01
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21167159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d182f8822a3701b3c590176311bd202687d1dee46b684a850f05bc25f9780e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 05:53:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 05:53:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 05:53:04 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:53:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 05:53:05 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 05:53:06 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb068a5ae768db846d4cffd6d8a07b00341712cc95b28925ffd386be29ad6da5`  
		Last Modified: Tue, 24 Mar 2020 05:56:14 GMT  
		Size: 17.7 MB (17747468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de178e83d0b4ec78b825872546d5376d07eb016394af195f7322b609c2c84c2a`  
		Last Modified: Tue, 24 Mar 2020 05:56:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles`

```console
$ docker pull traefik@sha256:d8d07854fc8123227b916460903ae368a27146108df96a696b08656e5a47b52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:3dd7053eaef5072de87162644d4c14b4c6d6f10baa00e9714b9959480c3a8ba2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21578577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d3e8a9c33887f506e928881e765eccd48b8535e63cf04178f8e78c1351b6c8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:27:01 GMT
COPY file:977e3eca412036b63f1f1b09d8388d4e5d6b3535c7af5df64ba18886ed8efd6f in / 
# Mon, 23 Mar 2020 20:27:01 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:27:01 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:27:02 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:27:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e40d0b92fe2d2ef50c6f43f32c33dc117ab26d69a29d74ae15725a379dbde0c2`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 131.7 KB (131682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c068c5049677b6879089396aa0d2d162ac9697e25bacf333c0596a248bae8a5`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 327.4 KB (327376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d33f083e50ccd3f0b3af53d0e2a2c2dca2898906a953c1e2e4b14c530aefe1`  
		Last Modified: Mon, 23 Mar 2020 20:27:37 GMT  
		Size: 21.1 MB (21119519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ad05498d1d177ef22566fa16d1e9256adce71af86013d7eb9b082c1294249899
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20230021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156c24891f895dbc51607c824d2e299ff2ea302df9fc2b8962f5fdd2e4f8b1fb`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 03:46:16 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 03:46:17 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 24 Mar 2020 03:46:21 GMT
COPY file:0a84c8de85d7e943231603655ccecf108fb25302c6ed1f9c6cb4f9e90c926dfb in / 
# Tue, 24 Mar 2020 03:46:22 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:46:23 GMT
VOLUME [/tmp]
# Tue, 24 Mar 2020 03:46:24 GMT
ENTRYPOINT ["/traefik"]
# Tue, 24 Mar 2020 03:46:24 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3ea78b0360c0223e83ecbb7336ab0de873d099e2aa889216bc3622c7dc315adc`  
		Last Modified: Tue, 24 Mar 2020 03:47:54 GMT  
		Size: 131.7 KB (131681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd374e140760994a9274b43e4cbf314b61a77acb227eca705d35780bb33a6a07`  
		Last Modified: Tue, 24 Mar 2020 03:47:55 GMT  
		Size: 327.4 KB (327405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e556ef2bd973f47fadf08d98f358fd091604a1de5409cf4a7cc8d3187623d3`  
		Last Modified: Tue, 24 Mar 2020 03:48:03 GMT  
		Size: 19.8 MB (19770935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f6a41eb9ec2b3294c6a1a65cd25e440c6f2b07a4af0b644d08c73045ae9c821c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19950885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9fd16d96e8adc131956fc884a01f9e45e2adafad71b15083c3ae764b799ee9c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 05:55:25 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 05:55:26 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 24 Mar 2020 05:55:28 GMT
COPY file:a3694a993cf25306aff467c03d4f70f02c07bff1afad394515f87b732cdab043 in / 
# Tue, 24 Mar 2020 05:55:29 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:55:29 GMT
VOLUME [/tmp]
# Tue, 24 Mar 2020 05:55:30 GMT
ENTRYPOINT ["/traefik"]
# Tue, 24 Mar 2020 05:55:31 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:58ceb9a2a8ba9dd83eef0c2cf887c175911b301df486d142f7d09293605add22`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 131.7 KB (131676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b9edf48787b0368bb1af04734041d3b374acefa70417bdf0090919056c874d`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 327.4 KB (327402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8802a35e2e74e1dcf82490548042848f15ea48357d7f9c232231f94cda68ef`  
		Last Modified: Tue, 24 Mar 2020 05:56:49 GMT  
		Size: 19.5 MB (19491807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-alpine`

```console
$ docker pull traefik@sha256:87ec78321c9af542f8bd0b58299d7bad96740e24fb3fab8e50a146b2952f283f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:46c4281b4bb6882eff0d972b7c2c9cbaba69c6fc66074058b660268404a27c7a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24617484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afc1d9db6d8fa6572e0313edb7e41f57a5ba4ec2d2322b2934e25eb81b7417b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:19 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:20 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:21 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41bdc4cb62d692fefe850ea163c318db37fbba75755b78932d1e43492d0b29d`  
		Last Modified: Mon, 23 Mar 2020 23:47:34 GMT  
		Size: 21.1 MB (21119717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a70748d348ef256993ee5cffc84cf0f40f2b1e1713952299e986d373d12811`  
		Last Modified: Mon, 23 Mar 2020 23:47:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:9708bb38140b19e258179c0e7886e6b8551a1cc1f6507d0899505fa573b8a3a1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23088000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30bf0f95111027bbafdf5e4e1359007f64b69883b904adefa37a0ee515ac8a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 03:43:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 03:44:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 03:44:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 03:44:34 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:44:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 03:44:35 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 03:44:36 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b73c299e24e9aa32bbbec493b7588c3a6592d11b52ccb01c156037b819aef46`  
		Last Modified: Tue, 24 Mar 2020 03:47:03 GMT  
		Size: 698.1 KB (698067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80eaea1c33d2ec522e729ccc1f058ccfba9d7e66158f435004d333626b62e79`  
		Last Modified: Tue, 24 Mar 2020 03:47:45 GMT  
		Size: 19.8 MB (19770986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d46bd54705ee81f39ce737c02dbc6ba461ebf69507a39aea7592a29250dd7ac`  
		Last Modified: Tue, 24 Mar 2020 03:47:43 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:0d134b143eec517177fdd9df79aaa4a11e7fe98283b502ff4eb73097f710d786
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22911680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004d9bce1ce8133ee2ed61502f6db556dd1d485b479e7c6ba6a7b6881ce7fae3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 05:53:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 05:53:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 05:53:16 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:53:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 05:53:17 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 05:53:17 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba236ca9140213ef04f6289ffeb9778d10fe5a35cb7fa09ec3b67581e9dd31d`  
		Last Modified: Tue, 24 Mar 2020 05:56:32 GMT  
		Size: 19.5 MB (19491989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfb55492bb3451bea3761bd98a63749a7a3f6fed739d7949c9967c3d5b5d386`  
		Last Modified: Tue, 24 Mar 2020 05:56:25 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-windowsservercore-1809`

```console
$ docker pull traefik@sha256:28a158cbb1f498399673e62f4b77b5fc6abf59324564397ef0b7c19430ca8cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:44fc6778ad6b2ddb0bdcddb9561019c5fc9595c265060a07291a12f4cbe49b44
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291142670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4919c09dd96ca89d1f3b47d479f9bf17813c7f78fa7762a1a58b29b97ed5375`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:32:24 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Mon, 23 Mar 2020 21:32:28 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:32:29 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:32:30 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b00e8e040906f3d887b30e678e40efb35c177517d3ab7885312a259fc4cd60`  
		Last Modified: Mon, 23 Mar 2020 21:33:27 GMT  
		Size: 25.8 MB (25801749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b74468fd780764620b22dd13d3c2ad380a2f4b8038f52ed9bea45b29c3e5b`  
		Last Modified: Mon, 23 Mar 2020 21:33:22 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac07893895096293dc66362aaef0ba3fa38751d015265b3c1df0cd9122d7531`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3023a9d8dd0513c3a0f98d6ff8af04fad6fb178de50458b5a9c75acf3963721`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7`

```console
$ docker pull traefik@sha256:d8d07854fc8123227b916460903ae368a27146108df96a696b08656e5a47b52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7` - linux; amd64

```console
$ docker pull traefik@sha256:3dd7053eaef5072de87162644d4c14b4c6d6f10baa00e9714b9959480c3a8ba2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21578577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d3e8a9c33887f506e928881e765eccd48b8535e63cf04178f8e78c1351b6c8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:27:01 GMT
COPY file:977e3eca412036b63f1f1b09d8388d4e5d6b3535c7af5df64ba18886ed8efd6f in / 
# Mon, 23 Mar 2020 20:27:01 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:27:01 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:27:02 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:27:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e40d0b92fe2d2ef50c6f43f32c33dc117ab26d69a29d74ae15725a379dbde0c2`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 131.7 KB (131682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c068c5049677b6879089396aa0d2d162ac9697e25bacf333c0596a248bae8a5`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 327.4 KB (327376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d33f083e50ccd3f0b3af53d0e2a2c2dca2898906a953c1e2e4b14c530aefe1`  
		Last Modified: Mon, 23 Mar 2020 20:27:37 GMT  
		Size: 21.1 MB (21119519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ad05498d1d177ef22566fa16d1e9256adce71af86013d7eb9b082c1294249899
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20230021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156c24891f895dbc51607c824d2e299ff2ea302df9fc2b8962f5fdd2e4f8b1fb`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 03:46:16 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 03:46:17 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 24 Mar 2020 03:46:21 GMT
COPY file:0a84c8de85d7e943231603655ccecf108fb25302c6ed1f9c6cb4f9e90c926dfb in / 
# Tue, 24 Mar 2020 03:46:22 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:46:23 GMT
VOLUME [/tmp]
# Tue, 24 Mar 2020 03:46:24 GMT
ENTRYPOINT ["/traefik"]
# Tue, 24 Mar 2020 03:46:24 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3ea78b0360c0223e83ecbb7336ab0de873d099e2aa889216bc3622c7dc315adc`  
		Last Modified: Tue, 24 Mar 2020 03:47:54 GMT  
		Size: 131.7 KB (131681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd374e140760994a9274b43e4cbf314b61a77acb227eca705d35780bb33a6a07`  
		Last Modified: Tue, 24 Mar 2020 03:47:55 GMT  
		Size: 327.4 KB (327405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e556ef2bd973f47fadf08d98f358fd091604a1de5409cf4a7cc8d3187623d3`  
		Last Modified: Tue, 24 Mar 2020 03:48:03 GMT  
		Size: 19.8 MB (19770935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f6a41eb9ec2b3294c6a1a65cd25e440c6f2b07a4af0b644d08c73045ae9c821c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19950885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9fd16d96e8adc131956fc884a01f9e45e2adafad71b15083c3ae764b799ee9c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 05:55:25 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 05:55:26 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 24 Mar 2020 05:55:28 GMT
COPY file:a3694a993cf25306aff467c03d4f70f02c07bff1afad394515f87b732cdab043 in / 
# Tue, 24 Mar 2020 05:55:29 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:55:29 GMT
VOLUME [/tmp]
# Tue, 24 Mar 2020 05:55:30 GMT
ENTRYPOINT ["/traefik"]
# Tue, 24 Mar 2020 05:55:31 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:58ceb9a2a8ba9dd83eef0c2cf887c175911b301df486d142f7d09293605add22`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 131.7 KB (131676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b9edf48787b0368bb1af04734041d3b374acefa70417bdf0090919056c874d`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 327.4 KB (327402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8802a35e2e74e1dcf82490548042848f15ea48357d7f9c232231f94cda68ef`  
		Last Modified: Tue, 24 Mar 2020 05:56:49 GMT  
		Size: 19.5 MB (19491807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.23`

```console
$ docker pull traefik@sha256:d8d07854fc8123227b916460903ae368a27146108df96a696b08656e5a47b52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.23` - linux; amd64

```console
$ docker pull traefik@sha256:3dd7053eaef5072de87162644d4c14b4c6d6f10baa00e9714b9959480c3a8ba2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21578577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d3e8a9c33887f506e928881e765eccd48b8535e63cf04178f8e78c1351b6c8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:27:01 GMT
COPY file:977e3eca412036b63f1f1b09d8388d4e5d6b3535c7af5df64ba18886ed8efd6f in / 
# Mon, 23 Mar 2020 20:27:01 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:27:01 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:27:02 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:27:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e40d0b92fe2d2ef50c6f43f32c33dc117ab26d69a29d74ae15725a379dbde0c2`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 131.7 KB (131682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c068c5049677b6879089396aa0d2d162ac9697e25bacf333c0596a248bae8a5`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 327.4 KB (327376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d33f083e50ccd3f0b3af53d0e2a2c2dca2898906a953c1e2e4b14c530aefe1`  
		Last Modified: Mon, 23 Mar 2020 20:27:37 GMT  
		Size: 21.1 MB (21119519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.23` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ad05498d1d177ef22566fa16d1e9256adce71af86013d7eb9b082c1294249899
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20230021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156c24891f895dbc51607c824d2e299ff2ea302df9fc2b8962f5fdd2e4f8b1fb`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 03:46:16 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 03:46:17 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 24 Mar 2020 03:46:21 GMT
COPY file:0a84c8de85d7e943231603655ccecf108fb25302c6ed1f9c6cb4f9e90c926dfb in / 
# Tue, 24 Mar 2020 03:46:22 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:46:23 GMT
VOLUME [/tmp]
# Tue, 24 Mar 2020 03:46:24 GMT
ENTRYPOINT ["/traefik"]
# Tue, 24 Mar 2020 03:46:24 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3ea78b0360c0223e83ecbb7336ab0de873d099e2aa889216bc3622c7dc315adc`  
		Last Modified: Tue, 24 Mar 2020 03:47:54 GMT  
		Size: 131.7 KB (131681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd374e140760994a9274b43e4cbf314b61a77acb227eca705d35780bb33a6a07`  
		Last Modified: Tue, 24 Mar 2020 03:47:55 GMT  
		Size: 327.4 KB (327405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e556ef2bd973f47fadf08d98f358fd091604a1de5409cf4a7cc8d3187623d3`  
		Last Modified: Tue, 24 Mar 2020 03:48:03 GMT  
		Size: 19.8 MB (19770935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.23` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f6a41eb9ec2b3294c6a1a65cd25e440c6f2b07a4af0b644d08c73045ae9c821c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19950885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9fd16d96e8adc131956fc884a01f9e45e2adafad71b15083c3ae764b799ee9c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 05:55:25 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 05:55:26 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 24 Mar 2020 05:55:28 GMT
COPY file:a3694a993cf25306aff467c03d4f70f02c07bff1afad394515f87b732cdab043 in / 
# Tue, 24 Mar 2020 05:55:29 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:55:29 GMT
VOLUME [/tmp]
# Tue, 24 Mar 2020 05:55:30 GMT
ENTRYPOINT ["/traefik"]
# Tue, 24 Mar 2020 05:55:31 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:58ceb9a2a8ba9dd83eef0c2cf887c175911b301df486d142f7d09293605add22`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 131.7 KB (131676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b9edf48787b0368bb1af04734041d3b374acefa70417bdf0090919056c874d`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 327.4 KB (327402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8802a35e2e74e1dcf82490548042848f15ea48357d7f9c232231f94cda68ef`  
		Last Modified: Tue, 24 Mar 2020 05:56:49 GMT  
		Size: 19.5 MB (19491807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.23-alpine`

```console
$ docker pull traefik@sha256:87ec78321c9af542f8bd0b58299d7bad96740e24fb3fab8e50a146b2952f283f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.23-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:46c4281b4bb6882eff0d972b7c2c9cbaba69c6fc66074058b660268404a27c7a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24617484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afc1d9db6d8fa6572e0313edb7e41f57a5ba4ec2d2322b2934e25eb81b7417b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:19 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:20 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:21 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41bdc4cb62d692fefe850ea163c318db37fbba75755b78932d1e43492d0b29d`  
		Last Modified: Mon, 23 Mar 2020 23:47:34 GMT  
		Size: 21.1 MB (21119717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a70748d348ef256993ee5cffc84cf0f40f2b1e1713952299e986d373d12811`  
		Last Modified: Mon, 23 Mar 2020 23:47:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.23-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:9708bb38140b19e258179c0e7886e6b8551a1cc1f6507d0899505fa573b8a3a1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23088000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30bf0f95111027bbafdf5e4e1359007f64b69883b904adefa37a0ee515ac8a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 03:43:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 03:44:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 03:44:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 03:44:34 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:44:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 03:44:35 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 03:44:36 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b73c299e24e9aa32bbbec493b7588c3a6592d11b52ccb01c156037b819aef46`  
		Last Modified: Tue, 24 Mar 2020 03:47:03 GMT  
		Size: 698.1 KB (698067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80eaea1c33d2ec522e729ccc1f058ccfba9d7e66158f435004d333626b62e79`  
		Last Modified: Tue, 24 Mar 2020 03:47:45 GMT  
		Size: 19.8 MB (19770986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d46bd54705ee81f39ce737c02dbc6ba461ebf69507a39aea7592a29250dd7ac`  
		Last Modified: Tue, 24 Mar 2020 03:47:43 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.23-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:0d134b143eec517177fdd9df79aaa4a11e7fe98283b502ff4eb73097f710d786
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22911680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004d9bce1ce8133ee2ed61502f6db556dd1d485b479e7c6ba6a7b6881ce7fae3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 05:53:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 05:53:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 05:53:16 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:53:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 05:53:17 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 05:53:17 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba236ca9140213ef04f6289ffeb9778d10fe5a35cb7fa09ec3b67581e9dd31d`  
		Last Modified: Tue, 24 Mar 2020 05:56:32 GMT  
		Size: 19.5 MB (19491989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfb55492bb3451bea3761bd98a63749a7a3f6fed739d7949c9967c3d5b5d386`  
		Last Modified: Tue, 24 Mar 2020 05:56:25 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.23-windowsservercore-1809`

```console
$ docker pull traefik@sha256:28a158cbb1f498399673e62f4b77b5fc6abf59324564397ef0b7c19430ca8cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:v1.7.23-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:44fc6778ad6b2ddb0bdcddb9561019c5fc9595c265060a07291a12f4cbe49b44
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291142670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4919c09dd96ca89d1f3b47d479f9bf17813c7f78fa7762a1a58b29b97ed5375`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:32:24 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Mon, 23 Mar 2020 21:32:28 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:32:29 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:32:30 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b00e8e040906f3d887b30e678e40efb35c177517d3ab7885312a259fc4cd60`  
		Last Modified: Mon, 23 Mar 2020 21:33:27 GMT  
		Size: 25.8 MB (25801749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b74468fd780764620b22dd13d3c2ad380a2f4b8038f52ed9bea45b29c3e5b`  
		Last Modified: Mon, 23 Mar 2020 21:33:22 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac07893895096293dc66362aaef0ba3fa38751d015265b3c1df0cd9122d7531`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3023a9d8dd0513c3a0f98d6ff8af04fad6fb178de50458b5a9c75acf3963721`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-alpine`

```console
$ docker pull traefik@sha256:87ec78321c9af542f8bd0b58299d7bad96740e24fb3fab8e50a146b2952f283f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:46c4281b4bb6882eff0d972b7c2c9cbaba69c6fc66074058b660268404a27c7a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24617484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afc1d9db6d8fa6572e0313edb7e41f57a5ba4ec2d2322b2934e25eb81b7417b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:19 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:20 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:21 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41bdc4cb62d692fefe850ea163c318db37fbba75755b78932d1e43492d0b29d`  
		Last Modified: Mon, 23 Mar 2020 23:47:34 GMT  
		Size: 21.1 MB (21119717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a70748d348ef256993ee5cffc84cf0f40f2b1e1713952299e986d373d12811`  
		Last Modified: Mon, 23 Mar 2020 23:47:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:9708bb38140b19e258179c0e7886e6b8551a1cc1f6507d0899505fa573b8a3a1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23088000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30bf0f95111027bbafdf5e4e1359007f64b69883b904adefa37a0ee515ac8a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 03:43:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 03:44:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 03:44:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 03:44:34 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:44:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 03:44:35 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 03:44:36 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b73c299e24e9aa32bbbec493b7588c3a6592d11b52ccb01c156037b819aef46`  
		Last Modified: Tue, 24 Mar 2020 03:47:03 GMT  
		Size: 698.1 KB (698067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80eaea1c33d2ec522e729ccc1f058ccfba9d7e66158f435004d333626b62e79`  
		Last Modified: Tue, 24 Mar 2020 03:47:45 GMT  
		Size: 19.8 MB (19770986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d46bd54705ee81f39ce737c02dbc6ba461ebf69507a39aea7592a29250dd7ac`  
		Last Modified: Tue, 24 Mar 2020 03:47:43 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:0d134b143eec517177fdd9df79aaa4a11e7fe98283b502ff4eb73097f710d786
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22911680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004d9bce1ce8133ee2ed61502f6db556dd1d485b479e7c6ba6a7b6881ce7fae3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 05:53:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 05:53:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 05:53:16 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:53:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 05:53:17 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 05:53:17 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba236ca9140213ef04f6289ffeb9778d10fe5a35cb7fa09ec3b67581e9dd31d`  
		Last Modified: Tue, 24 Mar 2020 05:56:32 GMT  
		Size: 19.5 MB (19491989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfb55492bb3451bea3761bd98a63749a7a3f6fed739d7949c9967c3d5b5d386`  
		Last Modified: Tue, 24 Mar 2020 05:56:25 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:28a158cbb1f498399673e62f4b77b5fc6abf59324564397ef0b7c19430ca8cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:v1.7-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:44fc6778ad6b2ddb0bdcddb9561019c5fc9595c265060a07291a12f4cbe49b44
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291142670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4919c09dd96ca89d1f3b47d479f9bf17813c7f78fa7762a1a58b29b97ed5375`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:32:24 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Mon, 23 Mar 2020 21:32:28 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:32:29 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:32:30 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b00e8e040906f3d887b30e678e40efb35c177517d3ab7885312a259fc4cd60`  
		Last Modified: Mon, 23 Mar 2020 21:33:27 GMT  
		Size: 25.8 MB (25801749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b74468fd780764620b22dd13d3c2ad380a2f4b8038f52ed9bea45b29c3e5b`  
		Last Modified: Mon, 23 Mar 2020 21:33:22 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac07893895096293dc66362aaef0ba3fa38751d015265b3c1df0cd9122d7531`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3023a9d8dd0513c3a0f98d6ff8af04fad6fb178de50458b5a9c75acf3963721`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.1`

```console
$ docker pull traefik@sha256:ab83baa3d198ee5a2fd685bed96417055a2bdd271efe11a0b831d6c02436aabd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.1` - linux; amd64

```console
$ docker pull traefik@sha256:0f877111f469c6843a3e18d181dc2eaeecaca5cf4dfa8538cb534be2e2806ce1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22719782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bfc37343a47ef437767e7f10ec6c47b5dfb7d5a7fde99a78063f0217b6edfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:07 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:08 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780c440cb354cd104d66dca36ad5f5e924dbbf0baacd588406f7635c48569fab`  
		Last Modified: Mon, 23 Mar 2020 23:47:22 GMT  
		Size: 19.2 MB (19222015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89f3c2e369bd1b3dbdfb399a0d6c9f5e8d9b595ab26c6ad4d3ec5cee06cc771`  
		Last Modified: Mon, 23 Mar 2020 23:47:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:c6a38950d8f392d4ccedea121fb6b59f79e3468f04fe005b2946da8d7d33a95a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21362283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7ab131d970b368d0b6c84a678dae3dd68d40e3fbffdc27ce055270e82377fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 03:43:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 03:44:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 03:44:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 03:44:19 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:44:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 03:44:21 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 03:44:21 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b73c299e24e9aa32bbbec493b7588c3a6592d11b52ccb01c156037b819aef46`  
		Last Modified: Tue, 24 Mar 2020 03:47:03 GMT  
		Size: 698.1 KB (698067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0faaabb70feaf46fc30c623ca581dd5a603309378073aefb34021408fbaeca27`  
		Last Modified: Tue, 24 Mar 2020 03:47:27 GMT  
		Size: 18.0 MB (18045269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96986412029c005a604e02811ee63c2972698683e34ba39979d6b483b33fe185`  
		Last Modified: Tue, 24 Mar 2020 03:47:20 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e303a3b44ed8884b51de268bd4c990087cbc08139e0be4d4d139032083706b01
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21167159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d182f8822a3701b3c590176311bd202687d1dee46b684a850f05bc25f9780e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 05:53:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 05:53:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 05:53:04 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:53:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 05:53:05 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 05:53:06 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb068a5ae768db846d4cffd6d8a07b00341712cc95b28925ffd386be29ad6da5`  
		Last Modified: Tue, 24 Mar 2020 05:56:14 GMT  
		Size: 17.7 MB (17747468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de178e83d0b4ec78b825872546d5376d07eb016394af195f7322b609c2c84c2a`  
		Last Modified: Tue, 24 Mar 2020 05:56:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.1.9`

```console
$ docker pull traefik@sha256:ab83baa3d198ee5a2fd685bed96417055a2bdd271efe11a0b831d6c02436aabd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.1.9` - linux; amd64

```console
$ docker pull traefik@sha256:0f877111f469c6843a3e18d181dc2eaeecaca5cf4dfa8538cb534be2e2806ce1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22719782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bfc37343a47ef437767e7f10ec6c47b5dfb7d5a7fde99a78063f0217b6edfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:46:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:46:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:46:07 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:46:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:46:08 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:46:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780c440cb354cd104d66dca36ad5f5e924dbbf0baacd588406f7635c48569fab`  
		Last Modified: Mon, 23 Mar 2020 23:47:22 GMT  
		Size: 19.2 MB (19222015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89f3c2e369bd1b3dbdfb399a0d6c9f5e8d9b595ab26c6ad4d3ec5cee06cc771`  
		Last Modified: Mon, 23 Mar 2020 23:47:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.1.9` - linux; arm variant v6

```console
$ docker pull traefik@sha256:c6a38950d8f392d4ccedea121fb6b59f79e3468f04fe005b2946da8d7d33a95a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21362283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7ab131d970b368d0b6c84a678dae3dd68d40e3fbffdc27ce055270e82377fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 03:43:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 03:44:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 03:44:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 03:44:19 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:44:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 03:44:21 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 03:44:21 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b73c299e24e9aa32bbbec493b7588c3a6592d11b52ccb01c156037b819aef46`  
		Last Modified: Tue, 24 Mar 2020 03:47:03 GMT  
		Size: 698.1 KB (698067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0faaabb70feaf46fc30c623ca581dd5a603309378073aefb34021408fbaeca27`  
		Last Modified: Tue, 24 Mar 2020 03:47:27 GMT  
		Size: 18.0 MB (18045269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96986412029c005a604e02811ee63c2972698683e34ba39979d6b483b33fe185`  
		Last Modified: Tue, 24 Mar 2020 03:47:20 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.1.9` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e303a3b44ed8884b51de268bd4c990087cbc08139e0be4d4d139032083706b01
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21167159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d182f8822a3701b3c590176311bd202687d1dee46b684a850f05bc25f9780e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 05:53:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 05:53:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 05:53:04 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:53:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 05:53:05 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 05:53:06 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb068a5ae768db846d4cffd6d8a07b00341712cc95b28925ffd386be29ad6da5`  
		Last Modified: Tue, 24 Mar 2020 05:56:14 GMT  
		Size: 17.7 MB (17747468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de178e83d0b4ec78b825872546d5376d07eb016394af195f7322b609c2c84c2a`  
		Last Modified: Tue, 24 Mar 2020 05:56:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.1.9-windowsservercore-1809`

```console
$ docker pull traefik@sha256:426da4e134080b1ad724038a856a4cafabaff316e490d221f898d3c6a3584a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:v2.1.9-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:85934211df41d1946d9277304658f788ce4fdaa568bb130cd5978c9a7128aa00
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289298644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991a23a2835a6c3a3b9c9308404203c7a48eb7c61127bc0d08404f6ea6fcac0b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:31:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Mar 2020 21:31:26 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:31:27 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:31:28 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f80b3ae1536653ce370f049d76fd558fc18a69697f5c9a0208ed8dbdfd30475`  
		Last Modified: Mon, 23 Mar 2020 21:33:03 GMT  
		Size: 24.0 MB (23957752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e3dbb3d1da32a0307e35df54c13379b326d3f966599877c8192ffc10c444d3`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe22549283bca4c11332825e6dae34e308420cd54afadaec8140e55183cc763`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9cd238ed825cbc292541dd9f8cfb82f9ee5ba2999bede775a3f051ed89733`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.1-windowsservercore-1809`

```console
$ docker pull traefik@sha256:426da4e134080b1ad724038a856a4cafabaff316e490d221f898d3c6a3584a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:v2.1-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:85934211df41d1946d9277304658f788ce4fdaa568bb130cd5978c9a7128aa00
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289298644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991a23a2835a6c3a3b9c9308404203c7a48eb7c61127bc0d08404f6ea6fcac0b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:31:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Mar 2020 21:31:26 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:31:27 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:31:28 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f80b3ae1536653ce370f049d76fd558fc18a69697f5c9a0208ed8dbdfd30475`  
		Last Modified: Mon, 23 Mar 2020 21:33:03 GMT  
		Size: 24.0 MB (23957752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e3dbb3d1da32a0307e35df54c13379b326d3f966599877c8192ffc10c444d3`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe22549283bca4c11332825e6dae34e308420cd54afadaec8140e55183cc763`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9cd238ed825cbc292541dd9f8cfb82f9ee5ba2999bede775a3f051ed89733`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.2`

```console
$ docker pull traefik@sha256:723fc9db3de3432ad5f7d9596074cc47080e960ba81e7d8181bb1c682b564f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.2` - linux; amd64

```console
$ docker pull traefik@sha256:ea85c9c3a5d1c1e5b84769e14f17bf9e505cc8f0719cce800b61e10cd67d4101
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24780053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b552cb4ae6598187cd5353e0db70314afe2dc07f7596120f3a99a884f1fe76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:45:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:45:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:45:55 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:45:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:45:56 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:45:56 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f368fd862d907340d21e551d6fa5d97176b88b2ae3c92c28af55d8d7dc0a316`  
		Last Modified: Mon, 23 Mar 2020 23:47:09 GMT  
		Size: 21.3 MB (21282286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5b29ae28cf739aec30a2128fa715c59ac327ae5b127a2b270ab73141ca1b6f`  
		Last Modified: Mon, 23 Mar 2020 23:47:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fd374b0c80939d157f7d87f913715e2329b4acc5f97f4157f985403baed0b97f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23305628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7442444ce9e74ba3c02660c7be76ddcee26f9df3d7987214d171783c899705f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 03:43:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 03:44:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 03:44:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 03:44:05 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:44:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 03:44:07 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 03:44:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b73c299e24e9aa32bbbec493b7588c3a6592d11b52ccb01c156037b819aef46`  
		Last Modified: Tue, 24 Mar 2020 03:47:03 GMT  
		Size: 698.1 KB (698067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a54d3a262f9749f5dd0e62870a09217792ce6fe6d332fccbe96e75eac720a05`  
		Last Modified: Tue, 24 Mar 2020 03:47:10 GMT  
		Size: 20.0 MB (19988615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc68d67aafd345f029a6469144e76ad9b015c017cffa21e4cc27a31a961b943`  
		Last Modified: Tue, 24 Mar 2020 03:47:04 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:810c80e42a51505b352fa40c49fc6f47d18daa15a9a06a037b2c77c4a1da909d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23052200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31574eaabcda934879fd354a8aaaad034b96cb836bcb385f3eaba8e00ef68e50`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 05:52:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 05:52:52 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 05:52:53 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:52:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 05:52:54 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 05:52:54 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5601e5e68ec3f28b097b71055aad3c3b78a6c2a1748e218c6547797917153671`  
		Last Modified: Tue, 24 Mar 2020 05:55:59 GMT  
		Size: 19.6 MB (19632509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681e03de8125baca253f2686a970056c714325b611de9769dcd1829ef9e77b8f`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.2.0-rc4`

```console
$ docker pull traefik@sha256:723fc9db3de3432ad5f7d9596074cc47080e960ba81e7d8181bb1c682b564f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.2.0-rc4` - linux; amd64

```console
$ docker pull traefik@sha256:ea85c9c3a5d1c1e5b84769e14f17bf9e505cc8f0719cce800b61e10cd67d4101
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24780053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b552cb4ae6598187cd5353e0db70314afe2dc07f7596120f3a99a884f1fe76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:45:50 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 23 Mar 2020 23:45:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 23 Mar 2020 23:45:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 23 Mar 2020 23:45:55 GMT
EXPOSE 80
# Mon, 23 Mar 2020 23:45:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Mar 2020 23:45:56 GMT
CMD ["traefik"]
# Mon, 23 Mar 2020 23:45:56 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f365f1b91ebb32c62c3856cd602b14702103c16ede6873855d0c5a5faa874810`  
		Last Modified: Mon, 23 Mar 2020 23:47:03 GMT  
		Size: 694.1 KB (694143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f368fd862d907340d21e551d6fa5d97176b88b2ae3c92c28af55d8d7dc0a316`  
		Last Modified: Mon, 23 Mar 2020 23:47:09 GMT  
		Size: 21.3 MB (21282286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5b29ae28cf739aec30a2128fa715c59ac327ae5b127a2b270ab73141ca1b6f`  
		Last Modified: Mon, 23 Mar 2020 23:47:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.2.0-rc4` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fd374b0c80939d157f7d87f913715e2329b4acc5f97f4157f985403baed0b97f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23305628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7442444ce9e74ba3c02660c7be76ddcee26f9df3d7987214d171783c899705f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 03:43:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 03:44:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 03:44:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 03:44:05 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:44:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 03:44:07 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 03:44:08 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b73c299e24e9aa32bbbec493b7588c3a6592d11b52ccb01c156037b819aef46`  
		Last Modified: Tue, 24 Mar 2020 03:47:03 GMT  
		Size: 698.1 KB (698067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a54d3a262f9749f5dd0e62870a09217792ce6fe6d332fccbe96e75eac720a05`  
		Last Modified: Tue, 24 Mar 2020 03:47:10 GMT  
		Size: 20.0 MB (19988615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc68d67aafd345f029a6469144e76ad9b015c017cffa21e4cc27a31a961b943`  
		Last Modified: Tue, 24 Mar 2020 03:47:04 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.2.0-rc4` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:810c80e42a51505b352fa40c49fc6f47d18daa15a9a06a037b2c77c4a1da909d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23052200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31574eaabcda934879fd354a8aaaad034b96cb836bcb385f3eaba8e00ef68e50`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:52:48 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 24 Mar 2020 05:52:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 24 Mar 2020 05:52:52 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 24 Mar 2020 05:52:53 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:52:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2020 05:52:54 GMT
CMD ["traefik"]
# Tue, 24 Mar 2020 05:52:54 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc893b889cb9ecb596775296ec01901b5ffcd52efc8691a608afb27fc5be6e6`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 696.2 KB (696184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5601e5e68ec3f28b097b71055aad3c3b78a6c2a1748e218c6547797917153671`  
		Last Modified: Tue, 24 Mar 2020 05:55:59 GMT  
		Size: 19.6 MB (19632509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681e03de8125baca253f2686a970056c714325b611de9769dcd1829ef9e77b8f`  
		Last Modified: Tue, 24 Mar 2020 05:55:52 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.2.0-rc4-windowsservercore-1809`

```console
$ docker pull traefik@sha256:10b613c0d809a2f32e3f1f05a4d1bf8948740b300edc48c0db647d89ded615a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:v2.2.0-rc4-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:be5249e8a1f004bc3b704f5f678a716baeb1e02cbabf159eb439b82457d3cadf
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291275576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e276e79ace0d8ef3779cc569768475cf7763dcb4753b2da424149790667851c1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Mar 2020 23:40:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 19 Mar 2020 23:41:01 GMT
EXPOSE 80
# Thu, 19 Mar 2020 23:41:02 GMT
ENTRYPOINT ["/traefik"]
# Thu, 19 Mar 2020 23:41:03 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549f06fe79c6ff9fe97ad90025e8fa1f62dc9cc3b2d1a223c2be32e8e944ff9e`  
		Last Modified: Thu, 19 Mar 2020 23:42:30 GMT  
		Size: 25.9 MB (25934473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465d2f7acd904d7ca8da43eb4cdd73475b80ccce5ba79a88d9968266c4bad07f`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809f97326d00cd242ff10557bd548b8db16c340fd5d7fc274f3282623f542bbb`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e27a6ecc6db484f65e2587cb61e379ddb398f17469e292905230bc60e36fc04`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:10b613c0d809a2f32e3f1f05a4d1bf8948740b300edc48c0db647d89ded615a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:v2.2-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:be5249e8a1f004bc3b704f5f678a716baeb1e02cbabf159eb439b82457d3cadf
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291275576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e276e79ace0d8ef3779cc569768475cf7763dcb4753b2da424149790667851c1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Mar 2020 23:40:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.0-rc4/traefik_v2.2.0-rc4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 19 Mar 2020 23:41:01 GMT
EXPOSE 80
# Thu, 19 Mar 2020 23:41:02 GMT
ENTRYPOINT ["/traefik"]
# Thu, 19 Mar 2020 23:41:03 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.0-rc4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549f06fe79c6ff9fe97ad90025e8fa1f62dc9cc3b2d1a223c2be32e8e944ff9e`  
		Last Modified: Thu, 19 Mar 2020 23:42:30 GMT  
		Size: 25.9 MB (25934473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465d2f7acd904d7ca8da43eb4cdd73475b80ccce5ba79a88d9968266c4bad07f`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809f97326d00cd242ff10557bd548b8db16c340fd5d7fc274f3282623f542bbb`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e27a6ecc6db484f65e2587cb61e379ddb398f17469e292905230bc60e36fc04`  
		Last Modified: Thu, 19 Mar 2020 23:42:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:426da4e134080b1ad724038a856a4cafabaff316e490d221f898d3c6a3584a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:85934211df41d1946d9277304658f788ce4fdaa568bb130cd5978c9a7128aa00
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289298644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991a23a2835a6c3a3b9c9308404203c7a48eb7c61127bc0d08404f6ea6fcac0b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:31:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.9/traefik_v2.1.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 23 Mar 2020 21:31:26 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:31:27 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:31:28 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f80b3ae1536653ce370f049d76fd558fc18a69697f5c9a0208ed8dbdfd30475`  
		Last Modified: Mon, 23 Mar 2020 21:33:03 GMT  
		Size: 24.0 MB (23957752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e3dbb3d1da32a0307e35df54c13379b326d3f966599877c8192ffc10c444d3`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe22549283bca4c11332825e6dae34e308420cd54afadaec8140e55183cc763`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9cd238ed825cbc292541dd9f8cfb82f9ee5ba2999bede775a3f051ed89733`  
		Last Modified: Mon, 23 Mar 2020 21:32:58 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
