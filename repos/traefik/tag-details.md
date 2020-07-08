<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2.2`](#traefik22)
-	[`traefik:2.2.2`](#traefik222)
-	[`traefik:2.2.2-windowsservercore-1809`](#traefik222-windowsservercore-1809)
-	[`traefik:2.2-windowsservercore-1809`](#traefik22-windowsservercore-1809)
-	[`traefik:chevrotin`](#traefikchevrotin)
-	[`traefik:chevrotin-windowsservercore-1809`](#traefikchevrotin-windowsservercore-1809)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:v2.2`](#traefikv22)
-	[`traefik:v2.2.2`](#traefikv222)
-	[`traefik:v2.2.2-windowsservercore-1809`](#traefikv222-windowsservercore-1809)
-	[`traefik:v2.2-windowsservercore-1809`](#traefikv22-windowsservercore-1809)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)

## `traefik:2.2`

```console
$ docker pull traefik@sha256:ad4442a6f88cf35266542588f13ae9984aa058a55a518a87876e48c160d19ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.2` - linux; amd64

```console
$ docker pull traefik@sha256:8945fdecf9d6534fd1093b67e11a31f717810b187a93696fd6f496e3fb3b053f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24900388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0acfd4b50041a38c624a3ee2fca2b609675b18b142237032d892f3247a2bca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Apr 2020 20:20:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.1/traefik_v2.2.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Apr 2020 20:20:57 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Apr 2020 20:20:57 GMT
EXPOSE 80
# Wed, 29 Apr 2020 20:20:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Apr 2020 20:20:57 GMT
CMD ["traefik"]
# Wed, 29 Apr 2020 20:20:57 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16506d32a25436b458a7f443ec1ca0d096d99d3479523c92c247856fc6148c0`  
		Last Modified: Fri, 24 Apr 2020 17:34:15 GMT  
		Size: 694.1 KB (694148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be216d464d00a618f74560d4fa5236a194a2c4f8e86e8a92b2985c365bfa90d`  
		Last Modified: Wed, 29 Apr 2020 20:21:21 GMT  
		Size: 21.4 MB (21392555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed51f08b6109033a8e1566d7fd9047e1c9f7aa8271aea315a05aef28646e2e1`  
		Last Modified: Wed, 29 Apr 2020 20:21:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ab72481ca0c8007e98ef5e4aaad8248af42db11c62ebd79698c216dec9554b05
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23404448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ef3e8178d9bbc25f09ebd9d4089b759f0eebf7b7a513311cd95c9b73d1aa38`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Apr 2020 20:49:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.1/traefik_v2.2.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Apr 2020 20:49:45 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Apr 2020 20:49:45 GMT
EXPOSE 80
# Wed, 29 Apr 2020 20:49:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Apr 2020 20:49:46 GMT
CMD ["traefik"]
# Wed, 29 Apr 2020 20:49:47 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a36cf46e6cb6a8028db7cb68482816e710935254a7d463897840713066cf5ba`  
		Last Modified: Thu, 23 Apr 2020 22:39:24 GMT  
		Size: 698.1 KB (698086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b89231f57a4cb735421ab5b257ea157d32d271d84bfcbc1b48417269296decb`  
		Last Modified: Wed, 29 Apr 2020 20:50:18 GMT  
		Size: 20.1 MB (20086057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f194d9ba07ff2bd514ce008851411e43a45fd8322bb9586547c54a5820942ed`  
		Last Modified: Wed, 29 Apr 2020 20:50:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a3522a757a2694610347a5ac23e7491e8df3385d70860c656df4d66bcf941319
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23159864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be195c3c2ee158c763c56381c8d67480ad37250f4e4ef0a96416e2ead0f25ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Apr 2020 20:43:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.1/traefik_v2.2.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Apr 2020 20:43:13 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Apr 2020 20:43:14 GMT
EXPOSE 80
# Wed, 29 Apr 2020 20:43:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Apr 2020 20:43:15 GMT
CMD ["traefik"]
# Wed, 29 Apr 2020 20:43:15 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff968af61b86e34dc2412293ade430f77b7db53f7f4adb925fec30d3ccbb2876`  
		Last Modified: Fri, 24 Apr 2020 12:43:42 GMT  
		Size: 696.1 KB (696058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40b9b46aad1a33555712955aef0d36cba98b0ca83cbdf9f7c2afa05420883f1`  
		Last Modified: Wed, 29 Apr 2020 20:43:47 GMT  
		Size: 19.7 MB (19739013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5780fa41084316b7bd9812d4366a66d210c0c7e6892b1eafbbbcba36239ce094`  
		Last Modified: Wed, 29 Apr 2020 20:43:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.2.2`

```console
$ docker pull traefik@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `traefik:2.2.2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `traefik:2.2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:c4e50a891bf031306cb9f81627057a8a06e1b2985072c08aa680f9e755348d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `traefik:2.2-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull traefik@sha256:555a060ae73021ef89a81c842881ca46b1db626223843497342f59486b3b3074
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2320038676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a6a339334e1388a71632a085f64793f0571e70a54d6334dd56a0239f82b9c97`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jun 2020 20:42:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.1/traefik_v2.2.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Jun 2020 20:42:12 GMT
EXPOSE 80
# Wed, 10 Jun 2020 20:42:14 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Jun 2020 20:42:15 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f841c6a0c622cd36b5b2688011a224ac3e8e96273758f4a2804f2f3f099f267d`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63decd7d0d596e3f5a3c22bce3ac69de0bdca5cdebab6717ea8da68fc9bc55d3`  
		Last Modified: Wed, 10 Jun 2020 20:44:05 GMT  
		Size: 26.1 MB (26119829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f02d2cf6bc9ef4533088a9d976fd8434f7a400831d5aa2446434c9a19bda34a`  
		Last Modified: Wed, 10 Jun 2020 20:43:50 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabd3ad07810767b2e3ad9c427ed7ec367c6a22b7e246236a1d3b53676b7060b`  
		Last Modified: Wed, 10 Jun 2020 20:43:50 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b996e6c1470c3d2b04117319579324ef932e051653e457eec5e581b00c7db4`  
		Last Modified: Wed, 10 Jun 2020 20:43:50 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chevrotin`

```console
$ docker pull traefik@sha256:ad4442a6f88cf35266542588f13ae9984aa058a55a518a87876e48c160d19ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:chevrotin` - linux; amd64

```console
$ docker pull traefik@sha256:8945fdecf9d6534fd1093b67e11a31f717810b187a93696fd6f496e3fb3b053f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24900388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0acfd4b50041a38c624a3ee2fca2b609675b18b142237032d892f3247a2bca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Apr 2020 20:20:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.1/traefik_v2.2.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Apr 2020 20:20:57 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Apr 2020 20:20:57 GMT
EXPOSE 80
# Wed, 29 Apr 2020 20:20:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Apr 2020 20:20:57 GMT
CMD ["traefik"]
# Wed, 29 Apr 2020 20:20:57 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16506d32a25436b458a7f443ec1ca0d096d99d3479523c92c247856fc6148c0`  
		Last Modified: Fri, 24 Apr 2020 17:34:15 GMT  
		Size: 694.1 KB (694148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be216d464d00a618f74560d4fa5236a194a2c4f8e86e8a92b2985c365bfa90d`  
		Last Modified: Wed, 29 Apr 2020 20:21:21 GMT  
		Size: 21.4 MB (21392555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed51f08b6109033a8e1566d7fd9047e1c9f7aa8271aea315a05aef28646e2e1`  
		Last Modified: Wed, 29 Apr 2020 20:21:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:chevrotin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ab72481ca0c8007e98ef5e4aaad8248af42db11c62ebd79698c216dec9554b05
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23404448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ef3e8178d9bbc25f09ebd9d4089b759f0eebf7b7a513311cd95c9b73d1aa38`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Apr 2020 20:49:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.1/traefik_v2.2.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Apr 2020 20:49:45 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Apr 2020 20:49:45 GMT
EXPOSE 80
# Wed, 29 Apr 2020 20:49:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Apr 2020 20:49:46 GMT
CMD ["traefik"]
# Wed, 29 Apr 2020 20:49:47 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a36cf46e6cb6a8028db7cb68482816e710935254a7d463897840713066cf5ba`  
		Last Modified: Thu, 23 Apr 2020 22:39:24 GMT  
		Size: 698.1 KB (698086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b89231f57a4cb735421ab5b257ea157d32d271d84bfcbc1b48417269296decb`  
		Last Modified: Wed, 29 Apr 2020 20:50:18 GMT  
		Size: 20.1 MB (20086057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f194d9ba07ff2bd514ce008851411e43a45fd8322bb9586547c54a5820942ed`  
		Last Modified: Wed, 29 Apr 2020 20:50:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:chevrotin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a3522a757a2694610347a5ac23e7491e8df3385d70860c656df4d66bcf941319
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23159864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be195c3c2ee158c763c56381c8d67480ad37250f4e4ef0a96416e2ead0f25ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Apr 2020 20:43:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.1/traefik_v2.2.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Apr 2020 20:43:13 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Apr 2020 20:43:14 GMT
EXPOSE 80
# Wed, 29 Apr 2020 20:43:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Apr 2020 20:43:15 GMT
CMD ["traefik"]
# Wed, 29 Apr 2020 20:43:15 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff968af61b86e34dc2412293ade430f77b7db53f7f4adb925fec30d3ccbb2876`  
		Last Modified: Fri, 24 Apr 2020 12:43:42 GMT  
		Size: 696.1 KB (696058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40b9b46aad1a33555712955aef0d36cba98b0ca83cbdf9f7c2afa05420883f1`  
		Last Modified: Wed, 29 Apr 2020 20:43:47 GMT  
		Size: 19.7 MB (19739013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5780fa41084316b7bd9812d4366a66d210c0c7e6892b1eafbbbcba36239ce094`  
		Last Modified: Wed, 29 Apr 2020 20:43:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chevrotin-windowsservercore-1809`

```console
$ docker pull traefik@sha256:c4e50a891bf031306cb9f81627057a8a06e1b2985072c08aa680f9e755348d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `traefik:chevrotin-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull traefik@sha256:555a060ae73021ef89a81c842881ca46b1db626223843497342f59486b3b3074
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2320038676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a6a339334e1388a71632a085f64793f0571e70a54d6334dd56a0239f82b9c97`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jun 2020 20:42:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.1/traefik_v2.2.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Jun 2020 20:42:12 GMT
EXPOSE 80
# Wed, 10 Jun 2020 20:42:14 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Jun 2020 20:42:15 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f841c6a0c622cd36b5b2688011a224ac3e8e96273758f4a2804f2f3f099f267d`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63decd7d0d596e3f5a3c22bce3ac69de0bdca5cdebab6717ea8da68fc9bc55d3`  
		Last Modified: Wed, 10 Jun 2020 20:44:05 GMT  
		Size: 26.1 MB (26119829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f02d2cf6bc9ef4533088a9d976fd8434f7a400831d5aa2446434c9a19bda34a`  
		Last Modified: Wed, 10 Jun 2020 20:43:50 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabd3ad07810767b2e3ad9c427ed7ec367c6a22b7e246236a1d3b53676b7060b`  
		Last Modified: Wed, 10 Jun 2020 20:43:50 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b996e6c1470c3d2b04117319579324ef932e051653e457eec5e581b00c7db4`  
		Last Modified: Wed, 10 Jun 2020 20:43:50 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:ad4442a6f88cf35266542588f13ae9984aa058a55a518a87876e48c160d19ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:8945fdecf9d6534fd1093b67e11a31f717810b187a93696fd6f496e3fb3b053f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24900388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0acfd4b50041a38c624a3ee2fca2b609675b18b142237032d892f3247a2bca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Apr 2020 20:20:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.1/traefik_v2.2.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Apr 2020 20:20:57 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Apr 2020 20:20:57 GMT
EXPOSE 80
# Wed, 29 Apr 2020 20:20:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Apr 2020 20:20:57 GMT
CMD ["traefik"]
# Wed, 29 Apr 2020 20:20:57 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16506d32a25436b458a7f443ec1ca0d096d99d3479523c92c247856fc6148c0`  
		Last Modified: Fri, 24 Apr 2020 17:34:15 GMT  
		Size: 694.1 KB (694148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be216d464d00a618f74560d4fa5236a194a2c4f8e86e8a92b2985c365bfa90d`  
		Last Modified: Wed, 29 Apr 2020 20:21:21 GMT  
		Size: 21.4 MB (21392555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed51f08b6109033a8e1566d7fd9047e1c9f7aa8271aea315a05aef28646e2e1`  
		Last Modified: Wed, 29 Apr 2020 20:21:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ab72481ca0c8007e98ef5e4aaad8248af42db11c62ebd79698c216dec9554b05
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23404448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ef3e8178d9bbc25f09ebd9d4089b759f0eebf7b7a513311cd95c9b73d1aa38`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Apr 2020 20:49:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.1/traefik_v2.2.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Apr 2020 20:49:45 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Apr 2020 20:49:45 GMT
EXPOSE 80
# Wed, 29 Apr 2020 20:49:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Apr 2020 20:49:46 GMT
CMD ["traefik"]
# Wed, 29 Apr 2020 20:49:47 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a36cf46e6cb6a8028db7cb68482816e710935254a7d463897840713066cf5ba`  
		Last Modified: Thu, 23 Apr 2020 22:39:24 GMT  
		Size: 698.1 KB (698086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b89231f57a4cb735421ab5b257ea157d32d271d84bfcbc1b48417269296decb`  
		Last Modified: Wed, 29 Apr 2020 20:50:18 GMT  
		Size: 20.1 MB (20086057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f194d9ba07ff2bd514ce008851411e43a45fd8322bb9586547c54a5820942ed`  
		Last Modified: Wed, 29 Apr 2020 20:50:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a3522a757a2694610347a5ac23e7491e8df3385d70860c656df4d66bcf941319
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23159864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be195c3c2ee158c763c56381c8d67480ad37250f4e4ef0a96416e2ead0f25ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Apr 2020 20:43:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.1/traefik_v2.2.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Apr 2020 20:43:13 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Apr 2020 20:43:14 GMT
EXPOSE 80
# Wed, 29 Apr 2020 20:43:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Apr 2020 20:43:15 GMT
CMD ["traefik"]
# Wed, 29 Apr 2020 20:43:15 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff968af61b86e34dc2412293ade430f77b7db53f7f4adb925fec30d3ccbb2876`  
		Last Modified: Fri, 24 Apr 2020 12:43:42 GMT  
		Size: 696.1 KB (696058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40b9b46aad1a33555712955aef0d36cba98b0ca83cbdf9f7c2afa05420883f1`  
		Last Modified: Wed, 29 Apr 2020 20:43:47 GMT  
		Size: 19.7 MB (19739013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5780fa41084316b7bd9812d4366a66d210c0c7e6892b1eafbbbcba36239ce094`  
		Last Modified: Wed, 29 Apr 2020 20:43:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.2`

```console
$ docker pull traefik@sha256:ad4442a6f88cf35266542588f13ae9984aa058a55a518a87876e48c160d19ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.2` - linux; amd64

```console
$ docker pull traefik@sha256:8945fdecf9d6534fd1093b67e11a31f717810b187a93696fd6f496e3fb3b053f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24900388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0acfd4b50041a38c624a3ee2fca2b609675b18b142237032d892f3247a2bca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 17:33:28 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Apr 2020 20:20:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.1/traefik_v2.2.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Apr 2020 20:20:57 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Apr 2020 20:20:57 GMT
EXPOSE 80
# Wed, 29 Apr 2020 20:20:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Apr 2020 20:20:57 GMT
CMD ["traefik"]
# Wed, 29 Apr 2020 20:20:57 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16506d32a25436b458a7f443ec1ca0d096d99d3479523c92c247856fc6148c0`  
		Last Modified: Fri, 24 Apr 2020 17:34:15 GMT  
		Size: 694.1 KB (694148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be216d464d00a618f74560d4fa5236a194a2c4f8e86e8a92b2985c365bfa90d`  
		Last Modified: Wed, 29 Apr 2020 20:21:21 GMT  
		Size: 21.4 MB (21392555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed51f08b6109033a8e1566d7fd9047e1c9f7aa8271aea315a05aef28646e2e1`  
		Last Modified: Wed, 29 Apr 2020 20:21:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ab72481ca0c8007e98ef5e4aaad8248af42db11c62ebd79698c216dec9554b05
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23404448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ef3e8178d9bbc25f09ebd9d4089b759f0eebf7b7a513311cd95c9b73d1aa38`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:36:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Apr 2020 20:49:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.1/traefik_v2.2.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Apr 2020 20:49:45 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Apr 2020 20:49:45 GMT
EXPOSE 80
# Wed, 29 Apr 2020 20:49:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Apr 2020 20:49:46 GMT
CMD ["traefik"]
# Wed, 29 Apr 2020 20:49:47 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a36cf46e6cb6a8028db7cb68482816e710935254a7d463897840713066cf5ba`  
		Last Modified: Thu, 23 Apr 2020 22:39:24 GMT  
		Size: 698.1 KB (698086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b89231f57a4cb735421ab5b257ea157d32d271d84bfcbc1b48417269296decb`  
		Last Modified: Wed, 29 Apr 2020 20:50:18 GMT  
		Size: 20.1 MB (20086057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f194d9ba07ff2bd514ce008851411e43a45fd8322bb9586547c54a5820942ed`  
		Last Modified: Wed, 29 Apr 2020 20:50:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a3522a757a2694610347a5ac23e7491e8df3385d70860c656df4d66bcf941319
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23159864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be195c3c2ee158c763c56381c8d67480ad37250f4e4ef0a96416e2ead0f25ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:14:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Apr 2020 20:43:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.2.1/traefik_v2.2.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Apr 2020 20:43:13 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Apr 2020 20:43:14 GMT
EXPOSE 80
# Wed, 29 Apr 2020 20:43:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Apr 2020 20:43:15 GMT
CMD ["traefik"]
# Wed, 29 Apr 2020 20:43:15 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff968af61b86e34dc2412293ade430f77b7db53f7f4adb925fec30d3ccbb2876`  
		Last Modified: Fri, 24 Apr 2020 12:43:42 GMT  
		Size: 696.1 KB (696058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40b9b46aad1a33555712955aef0d36cba98b0ca83cbdf9f7c2afa05420883f1`  
		Last Modified: Wed, 29 Apr 2020 20:43:47 GMT  
		Size: 19.7 MB (19739013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5780fa41084316b7bd9812d4366a66d210c0c7e6892b1eafbbbcba36239ce094`  
		Last Modified: Wed, 29 Apr 2020 20:43:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.2.2`

```console
$ docker pull traefik@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `traefik:v2.2.2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `traefik:v2.2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:c4e50a891bf031306cb9f81627057a8a06e1b2985072c08aa680f9e755348d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `traefik:v2.2-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull traefik@sha256:555a060ae73021ef89a81c842881ca46b1db626223843497342f59486b3b3074
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2320038676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a6a339334e1388a71632a085f64793f0571e70a54d6334dd56a0239f82b9c97`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jun 2020 20:42:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.1/traefik_v2.2.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Jun 2020 20:42:12 GMT
EXPOSE 80
# Wed, 10 Jun 2020 20:42:14 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Jun 2020 20:42:15 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f841c6a0c622cd36b5b2688011a224ac3e8e96273758f4a2804f2f3f099f267d`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63decd7d0d596e3f5a3c22bce3ac69de0bdca5cdebab6717ea8da68fc9bc55d3`  
		Last Modified: Wed, 10 Jun 2020 20:44:05 GMT  
		Size: 26.1 MB (26119829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f02d2cf6bc9ef4533088a9d976fd8434f7a400831d5aa2446434c9a19bda34a`  
		Last Modified: Wed, 10 Jun 2020 20:43:50 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabd3ad07810767b2e3ad9c427ed7ec367c6a22b7e246236a1d3b53676b7060b`  
		Last Modified: Wed, 10 Jun 2020 20:43:50 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b996e6c1470c3d2b04117319579324ef932e051653e457eec5e581b00c7db4`  
		Last Modified: Wed, 10 Jun 2020 20:43:50 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:c4e50a891bf031306cb9f81627057a8a06e1b2985072c08aa680f9e755348d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull traefik@sha256:555a060ae73021ef89a81c842881ca46b1db626223843497342f59486b3b3074
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2320038676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a6a339334e1388a71632a085f64793f0571e70a54d6334dd56a0239f82b9c97`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jun 2020 20:42:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.2.1/traefik_v2.2.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Jun 2020 20:42:12 GMT
EXPOSE 80
# Wed, 10 Jun 2020 20:42:14 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Jun 2020 20:42:15 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.2.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f841c6a0c622cd36b5b2688011a224ac3e8e96273758f4a2804f2f3f099f267d`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63decd7d0d596e3f5a3c22bce3ac69de0bdca5cdebab6717ea8da68fc9bc55d3`  
		Last Modified: Wed, 10 Jun 2020 20:44:05 GMT  
		Size: 26.1 MB (26119829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f02d2cf6bc9ef4533088a9d976fd8434f7a400831d5aa2446434c9a19bda34a`  
		Last Modified: Wed, 10 Jun 2020 20:43:50 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabd3ad07810767b2e3ad9c427ed7ec367c6a22b7e246236a1d3b53676b7060b`  
		Last Modified: Wed, 10 Jun 2020 20:43:50 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b996e6c1470c3d2b04117319579324ef932e051653e457eec5e581b00c7db4`  
		Last Modified: Wed, 10 Jun 2020 20:43:50 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
