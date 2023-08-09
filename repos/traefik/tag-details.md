<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2.10`](#traefik210)
-	[`traefik:2.10-windowsservercore-1809`](#traefik210-windowsservercore-1809)
-	[`traefik:2.10.4`](#traefik2104)
-	[`traefik:2.10.4-windowsservercore-1809`](#traefik2104-windowsservercore-1809)
-	[`traefik:3.0`](#traefik30)
-	[`traefik:3.0-windowsservercore-1809`](#traefik30-windowsservercore-1809)
-	[`traefik:3.0.0-beta3`](#traefik300-beta3)
-	[`traefik:3.0.0-beta3-windowsservercore-1809`](#traefik300-beta3-windowsservercore-1809)
-	[`traefik:beaufort`](#traefikbeaufort)
-	[`traefik:beaufort-windowsservercore-1809`](#traefikbeaufort-windowsservercore-1809)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:saintmarcelin`](#traefiksaintmarcelin)
-	[`traefik:saintmarcelin-windowsservercore-1809`](#traefiksaintmarcelin-windowsservercore-1809)
-	[`traefik:v2.10`](#traefikv210)
-	[`traefik:v2.10-windowsservercore-1809`](#traefikv210-windowsservercore-1809)
-	[`traefik:v2.10.4`](#traefikv2104)
-	[`traefik:v2.10.4-windowsservercore-1809`](#traefikv2104-windowsservercore-1809)
-	[`traefik:v3.0`](#traefikv30)
-	[`traefik:v3.0-windowsservercore-1809`](#traefikv30-windowsservercore-1809)
-	[`traefik:v3.0.0-beta3`](#traefikv300-beta3)
-	[`traefik:v3.0.0-beta3-windowsservercore-1809`](#traefikv300-beta3-windowsservercore-1809)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)

## `traefik:2.10`

```console
$ docker pull traefik@sha256:d557ab50ff51de06b60c528ed670d8c73f21cebb2195b3eecddf7aefcad628c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:2.10` - linux; amd64

```console
$ docker pull traefik@sha256:cda187e491fd290c16c972a7c2bba6dd20a3ffa8af101d84992f8f863ca0fa75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42380871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7adf08e6ff58c711a928da451587ef96dad977ea2dc85eef98fd4b551108b562`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 21 Jun 2023 00:26:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 25 Jul 2023 00:19:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 25 Jul 2023 00:19:42 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 25 Jul 2023 00:19:42 GMT
EXPOSE 80
# Tue, 25 Jul 2023 00:19:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Jul 2023 00:19:42 GMT
CMD ["traefik"]
# Tue, 25 Jul 2023 00:19:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a9b499d7ae3ed84aef77186cbd2b1ae5418ddc653e721702ec1a35fa324a3`  
		Last Modified: Wed, 21 Jun 2023 00:26:31 GMT  
		Size: 622.2 KB (622241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed0f8d1a10693b01ee2a3083246af8e1fb9f634539a0addcb433dce31535498`  
		Last Modified: Tue, 25 Jul 2023 00:20:05 GMT  
		Size: 38.4 MB (38360382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a842830f041aa03d92468d4e29754239f50a645960826ef46124a1efbc6c5386`  
		Last Modified: Tue, 25 Jul 2023 00:19:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.10` - linux; arm variant v6

```console
$ docker pull traefik@sha256:bcf37f90bb3c148ecc6c642f0a5ef7ecca69c107f5055a24e94de6b178038ee3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39897744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b470a25273a17965c4195798705c8c434dec9e1dcb8bed0e25cd4afd15e5a1df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:36:43 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 08 Aug 2023 23:36:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 08 Aug 2023 23:36:56 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 08 Aug 2023 23:36:56 GMT
EXPOSE 80
# Tue, 08 Aug 2023 23:36:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Aug 2023 23:36:56 GMT
CMD ["traefik"]
# Tue, 08 Aug 2023 23:36:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8cc6c7cf0fb882727ce9bdded1e9477cf9f51f27f262ddd2837ce010c75546`  
		Last Modified: Tue, 08 Aug 2023 23:37:08 GMT  
		Size: 622.7 KB (622688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f350ea2c1577d6f498d27752f1efc8de8aea15ad9cc2c8ac411a406fc06474`  
		Last Modified: Tue, 08 Aug 2023 23:37:34 GMT  
		Size: 36.1 MB (36129878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc4c23d6ff9206d00fa66fef11f0d9010dd364ced1cff33b54909008c2add1a`  
		Last Modified: Tue, 08 Aug 2023 23:37:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.10` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:464822209fa79cf4290dd21b9efdca0a28c72f8dc1fc2d1b7a01e80290a219c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39135061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a46b9a293dcb8a9cc4a0ec58acb1ff9a887e5ae62982750ad592a2ca7883209`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 23:21:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 25 Jul 2023 00:43:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 25 Jul 2023 00:43:29 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 25 Jul 2023 00:43:29 GMT
EXPOSE 80
# Tue, 25 Jul 2023 00:43:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Jul 2023 00:43:29 GMT
CMD ["traefik"]
# Tue, 25 Jul 2023 00:43:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b960a271861d2b8bee110ab4afb7ec842665bbbd31f1bb9c1c279cd78d925fc`  
		Last Modified: Tue, 20 Jun 2023 23:22:04 GMT  
		Size: 624.5 KB (624502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc8f7c18018a36bd99487bf04502db826e024f451a6a8a65f63b14f9f12587e`  
		Last Modified: Tue, 25 Jul 2023 00:43:45 GMT  
		Size: 35.2 MB (35180940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7c3aabffd24552b932f17694ea955ca9767427c4d7d6aede5be245758328c1`  
		Last Modified: Tue, 25 Jul 2023 00:43:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.10` - linux; s390x

```console
$ docker pull traefik@sha256:53453d8365bce00f1d0fc9db847c5d0b9c7a49be32342b0bd083b7a894a3e578
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41033110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cafb27a3280df3e588ad32633b3fd03ff4def053e356151a9bbb636a754a3a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 22:49:13 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 25 Jul 2023 00:03:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 25 Jul 2023 00:03:36 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 25 Jul 2023 00:03:37 GMT
EXPOSE 80
# Tue, 25 Jul 2023 00:03:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Jul 2023 00:03:37 GMT
CMD ["traefik"]
# Tue, 25 Jul 2023 00:03:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6fdd3c34275458c3ea0a8688ec24b8c7698ce5a31715673ae57aa8dd5b0844`  
		Last Modified: Tue, 20 Jun 2023 22:49:39 GMT  
		Size: 622.8 KB (622821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6158db5bbbb90d5afe7f56e0eec15dea136038213b9ab2f9a478924bf671802`  
		Last Modified: Tue, 25 Jul 2023 00:04:04 GMT  
		Size: 37.2 MB (37196424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be121cfc0faefca1a55460f6f2a4f500fcb355e64c8458a91c213c890c2f8df1`  
		Last Modified: Tue, 25 Jul 2023 00:03:58 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.10-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7b1d7933d34be8cb94a98c21e2012d094aacf7588f986e2c44ab1ac23e58c8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `traefik:2.10-windowsservercore-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull traefik@sha256:fdb540f2c6a721b012defd44bd25dde874a55f609fc3b880d67db28f424cf9a7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1978644570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab3df456f37590d20edb73827d45b4c85cf4b13b906310b855eb98f6cfcbbb2`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Jul 2023 22:45:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 24 Jul 2023 22:45:10 GMT
EXPOSE 80
# Mon, 24 Jul 2023 22:45:10 GMT
ENTRYPOINT ["/traefik"]
# Mon, 24 Jul 2023 22:45:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5aca5a8f07b6697cf4ed1b44c7cd6c3a737387a3303978a503bd9cf0c3623f`  
		Last Modified: Mon, 24 Jul 2023 22:45:49 GMT  
		Size: 38.9 MB (38949881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba21efd5ef6c3fc2fb79d8b27d9db2ed4a703d85260d8d42b81f17cc8441cf2`  
		Last Modified: Mon, 24 Jul 2023 22:45:41 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c979aa71e159870dc2fa120e7446a3ace60f72788635511544790363c89637`  
		Last Modified: Mon, 24 Jul 2023 22:45:41 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1476200a7b3fbc5f2081c68313f321e5e2dbf3ca2f5fa8b6fc146a47729ff7f`  
		Last Modified: Mon, 24 Jul 2023 22:45:41 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.10.4`

```console
$ docker pull traefik@sha256:d557ab50ff51de06b60c528ed670d8c73f21cebb2195b3eecddf7aefcad628c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:2.10.4` - linux; amd64

```console
$ docker pull traefik@sha256:cda187e491fd290c16c972a7c2bba6dd20a3ffa8af101d84992f8f863ca0fa75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42380871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7adf08e6ff58c711a928da451587ef96dad977ea2dc85eef98fd4b551108b562`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 21 Jun 2023 00:26:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 25 Jul 2023 00:19:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 25 Jul 2023 00:19:42 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 25 Jul 2023 00:19:42 GMT
EXPOSE 80
# Tue, 25 Jul 2023 00:19:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Jul 2023 00:19:42 GMT
CMD ["traefik"]
# Tue, 25 Jul 2023 00:19:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a9b499d7ae3ed84aef77186cbd2b1ae5418ddc653e721702ec1a35fa324a3`  
		Last Modified: Wed, 21 Jun 2023 00:26:31 GMT  
		Size: 622.2 KB (622241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed0f8d1a10693b01ee2a3083246af8e1fb9f634539a0addcb433dce31535498`  
		Last Modified: Tue, 25 Jul 2023 00:20:05 GMT  
		Size: 38.4 MB (38360382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a842830f041aa03d92468d4e29754239f50a645960826ef46124a1efbc6c5386`  
		Last Modified: Tue, 25 Jul 2023 00:19:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.10.4` - linux; arm variant v6

```console
$ docker pull traefik@sha256:bcf37f90bb3c148ecc6c642f0a5ef7ecca69c107f5055a24e94de6b178038ee3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39897744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b470a25273a17965c4195798705c8c434dec9e1dcb8bed0e25cd4afd15e5a1df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:36:43 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 08 Aug 2023 23:36:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 08 Aug 2023 23:36:56 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 08 Aug 2023 23:36:56 GMT
EXPOSE 80
# Tue, 08 Aug 2023 23:36:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Aug 2023 23:36:56 GMT
CMD ["traefik"]
# Tue, 08 Aug 2023 23:36:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8cc6c7cf0fb882727ce9bdded1e9477cf9f51f27f262ddd2837ce010c75546`  
		Last Modified: Tue, 08 Aug 2023 23:37:08 GMT  
		Size: 622.7 KB (622688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f350ea2c1577d6f498d27752f1efc8de8aea15ad9cc2c8ac411a406fc06474`  
		Last Modified: Tue, 08 Aug 2023 23:37:34 GMT  
		Size: 36.1 MB (36129878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc4c23d6ff9206d00fa66fef11f0d9010dd364ced1cff33b54909008c2add1a`  
		Last Modified: Tue, 08 Aug 2023 23:37:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.10.4` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:464822209fa79cf4290dd21b9efdca0a28c72f8dc1fc2d1b7a01e80290a219c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39135061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a46b9a293dcb8a9cc4a0ec58acb1ff9a887e5ae62982750ad592a2ca7883209`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 23:21:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 25 Jul 2023 00:43:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 25 Jul 2023 00:43:29 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 25 Jul 2023 00:43:29 GMT
EXPOSE 80
# Tue, 25 Jul 2023 00:43:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Jul 2023 00:43:29 GMT
CMD ["traefik"]
# Tue, 25 Jul 2023 00:43:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b960a271861d2b8bee110ab4afb7ec842665bbbd31f1bb9c1c279cd78d925fc`  
		Last Modified: Tue, 20 Jun 2023 23:22:04 GMT  
		Size: 624.5 KB (624502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc8f7c18018a36bd99487bf04502db826e024f451a6a8a65f63b14f9f12587e`  
		Last Modified: Tue, 25 Jul 2023 00:43:45 GMT  
		Size: 35.2 MB (35180940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7c3aabffd24552b932f17694ea955ca9767427c4d7d6aede5be245758328c1`  
		Last Modified: Tue, 25 Jul 2023 00:43:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.10.4` - linux; s390x

```console
$ docker pull traefik@sha256:53453d8365bce00f1d0fc9db847c5d0b9c7a49be32342b0bd083b7a894a3e578
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41033110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cafb27a3280df3e588ad32633b3fd03ff4def053e356151a9bbb636a754a3a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 22:49:13 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 25 Jul 2023 00:03:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 25 Jul 2023 00:03:36 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 25 Jul 2023 00:03:37 GMT
EXPOSE 80
# Tue, 25 Jul 2023 00:03:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Jul 2023 00:03:37 GMT
CMD ["traefik"]
# Tue, 25 Jul 2023 00:03:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6fdd3c34275458c3ea0a8688ec24b8c7698ce5a31715673ae57aa8dd5b0844`  
		Last Modified: Tue, 20 Jun 2023 22:49:39 GMT  
		Size: 622.8 KB (622821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6158db5bbbb90d5afe7f56e0eec15dea136038213b9ab2f9a478924bf671802`  
		Last Modified: Tue, 25 Jul 2023 00:04:04 GMT  
		Size: 37.2 MB (37196424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be121cfc0faefca1a55460f6f2a4f500fcb355e64c8458a91c213c890c2f8df1`  
		Last Modified: Tue, 25 Jul 2023 00:03:58 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.10.4-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7b1d7933d34be8cb94a98c21e2012d094aacf7588f986e2c44ab1ac23e58c8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `traefik:2.10.4-windowsservercore-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull traefik@sha256:fdb540f2c6a721b012defd44bd25dde874a55f609fc3b880d67db28f424cf9a7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1978644570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab3df456f37590d20edb73827d45b4c85cf4b13b906310b855eb98f6cfcbbb2`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Jul 2023 22:45:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 24 Jul 2023 22:45:10 GMT
EXPOSE 80
# Mon, 24 Jul 2023 22:45:10 GMT
ENTRYPOINT ["/traefik"]
# Mon, 24 Jul 2023 22:45:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5aca5a8f07b6697cf4ed1b44c7cd6c3a737387a3303978a503bd9cf0c3623f`  
		Last Modified: Mon, 24 Jul 2023 22:45:49 GMT  
		Size: 38.9 MB (38949881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba21efd5ef6c3fc2fb79d8b27d9db2ed4a703d85260d8d42b81f17cc8441cf2`  
		Last Modified: Mon, 24 Jul 2023 22:45:41 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c979aa71e159870dc2fa120e7446a3ace60f72788635511544790363c89637`  
		Last Modified: Mon, 24 Jul 2023 22:45:41 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1476200a7b3fbc5f2081c68313f321e5e2dbf3ca2f5fa8b6fc146a47729ff7f`  
		Last Modified: Mon, 24 Jul 2023 22:45:41 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0`

```console
$ docker pull traefik@sha256:85e386ea5aa2bfb2cebc7111540f9da53d84dc4e38848339a9fc479bd942c860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:3.0` - linux; amd64

```console
$ docker pull traefik@sha256:e5d4d00b48c51509c5b7fe051688e3d5254ae32459d822b04e845721f18f01b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42335491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60a5464b41e9a0fa02ad5c08069c9d61c3820b69ddb7539cda1ffbe66c36034`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 21 Jun 2023 00:26:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 20:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 20:20:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 20:20:11 GMT
EXPOSE 80
# Thu, 22 Jun 2023 20:20:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 20:20:11 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 20:20:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a9b499d7ae3ed84aef77186cbd2b1ae5418ddc653e721702ec1a35fa324a3`  
		Last Modified: Wed, 21 Jun 2023 00:26:31 GMT  
		Size: 622.2 KB (622241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8de7a217c34522d58e5296d7481baf74ca19f272f764c99614230fdfb6614d8`  
		Last Modified: Thu, 22 Jun 2023 20:20:30 GMT  
		Size: 38.3 MB (38315002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7429dc1ef43cddca6161c8b5989c8407cf8a2d9d8ffc38382d61b27cf27a3a69`  
		Last Modified: Thu, 22 Jun 2023 20:20:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4610ad0a08abfd441d5efea592fc370ab772915d5d62a4fe1b6ad57f5b1f7a17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39834746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c7857053ace4e793ccb85ef5e4f7039d5b2d69ef3bba2091533f1eac50eb57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:36:43 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 08 Aug 2023 23:36:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 08 Aug 2023 23:36:48 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 08 Aug 2023 23:36:48 GMT
EXPOSE 80
# Tue, 08 Aug 2023 23:36:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Aug 2023 23:36:48 GMT
CMD ["traefik"]
# Tue, 08 Aug 2023 23:36:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8cc6c7cf0fb882727ce9bdded1e9477cf9f51f27f262ddd2837ce010c75546`  
		Last Modified: Tue, 08 Aug 2023 23:37:08 GMT  
		Size: 622.7 KB (622688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a56f8f3e28824e8aeed3179006a8bacb5ea8697429ecdcf4b3313a11531872`  
		Last Modified: Tue, 08 Aug 2023 23:37:14 GMT  
		Size: 36.1 MB (36066881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4c24374a077bea1e909f5b61e43515993be1be29aacd3aef10a445d1447b70`  
		Last Modified: Tue, 08 Aug 2023 23:37:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:efaf29c610c2c375ca040a7082a4e2d1070f6637656e4a8690bda7e0b6d87242
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39096640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37fe55cab162059f692a67908c2664d867103ddf7274c54454a328ddcfc2ab5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 23:21:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 21:03:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 21:03:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 21:03:40 GMT
EXPOSE 80
# Thu, 22 Jun 2023 21:03:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 21:03:40 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 21:03:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b960a271861d2b8bee110ab4afb7ec842665bbbd31f1bb9c1c279cd78d925fc`  
		Last Modified: Tue, 20 Jun 2023 23:22:04 GMT  
		Size: 624.5 KB (624502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76382258b6f8e99baf32705e376a293bc7ed29e7bd383735c51c6dec2089dc3`  
		Last Modified: Thu, 22 Jun 2023 21:03:57 GMT  
		Size: 35.1 MB (35142519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596c4d06a06800876a536dcc687884fa9aa6312a4a6d69883bf10d2a02842040`  
		Last Modified: Thu, 22 Jun 2023 21:03:53 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; s390x

```console
$ docker pull traefik@sha256:9524d85b440d108c8641a51639b18fe27525d764a76327bfe2056ccf1f53f742
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40949702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5245200a97de3f0132729144c7ad3ec05bff569700b534486980a5d5139f063e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 22:49:13 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 19:43:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 19:43:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 19:43:18 GMT
EXPOSE 80
# Thu, 22 Jun 2023 19:43:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 19:43:19 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 19:43:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6fdd3c34275458c3ea0a8688ec24b8c7698ce5a31715673ae57aa8dd5b0844`  
		Last Modified: Tue, 20 Jun 2023 22:49:39 GMT  
		Size: 622.8 KB (622821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf960d6667a0be4844e96e2d1289b0e0220f968f717a8deaa46a4b97a2fe84ad`  
		Last Modified: Thu, 22 Jun 2023 19:43:56 GMT  
		Size: 37.1 MB (37113016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ec02b13b7d2100602de0b81f0e2f099162042d9fd9e2eddacc5f7c75313ded`  
		Last Modified: Thu, 22 Jun 2023 19:43:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:39223bfb0ad32d6f75222fc15bb3485e0dee016185f90671b4afbb6d79fa18f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `traefik:3.0-windowsservercore-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull traefik@sha256:d6862812720c532b092c2de682c892bdac8c0c67e6bec2b77e7323df968c4292
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1978586286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014bfe48eda2b324b4732f9a0d88fb8a0ccc6fd914fbd507568926f604439357`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jul 2023 03:41:59 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 14 Jul 2023 03:42:00 GMT
EXPOSE 80
# Fri, 14 Jul 2023 03:42:00 GMT
ENTRYPOINT ["/traefik"]
# Fri, 14 Jul 2023 03:42:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466207745a644fe73ff5acf6f1b26f0d899b68952dbe6eea34df2c8f1bc39878`  
		Last Modified: Fri, 14 Jul 2023 03:44:03 GMT  
		Size: 38.9 MB (38891610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb6b841b8c3783f4f2334cae29b1d2b8a2fc18cc0a556b277758166ba732b3b`  
		Last Modified: Fri, 14 Jul 2023 03:43:55 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950fbe16c05cf58dc8fc972ce6594dbab92250b58dcc21698f2476df0bfeaa39`  
		Last Modified: Fri, 14 Jul 2023 03:43:55 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390ea4373b029353b0cc8ec920b6d4067e1284e318edea2d82957de0fa9b853a`  
		Last Modified: Fri, 14 Jul 2023 03:43:55 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-beta3`

```console
$ docker pull traefik@sha256:85e386ea5aa2bfb2cebc7111540f9da53d84dc4e38848339a9fc479bd942c860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:3.0.0-beta3` - linux; amd64

```console
$ docker pull traefik@sha256:e5d4d00b48c51509c5b7fe051688e3d5254ae32459d822b04e845721f18f01b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42335491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60a5464b41e9a0fa02ad5c08069c9d61c3820b69ddb7539cda1ffbe66c36034`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 21 Jun 2023 00:26:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 20:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 20:20:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 20:20:11 GMT
EXPOSE 80
# Thu, 22 Jun 2023 20:20:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 20:20:11 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 20:20:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a9b499d7ae3ed84aef77186cbd2b1ae5418ddc653e721702ec1a35fa324a3`  
		Last Modified: Wed, 21 Jun 2023 00:26:31 GMT  
		Size: 622.2 KB (622241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8de7a217c34522d58e5296d7481baf74ca19f272f764c99614230fdfb6614d8`  
		Last Modified: Thu, 22 Jun 2023 20:20:30 GMT  
		Size: 38.3 MB (38315002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7429dc1ef43cddca6161c8b5989c8407cf8a2d9d8ffc38382d61b27cf27a3a69`  
		Last Modified: Thu, 22 Jun 2023 20:20:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-beta3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4610ad0a08abfd441d5efea592fc370ab772915d5d62a4fe1b6ad57f5b1f7a17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39834746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c7857053ace4e793ccb85ef5e4f7039d5b2d69ef3bba2091533f1eac50eb57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:36:43 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 08 Aug 2023 23:36:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 08 Aug 2023 23:36:48 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 08 Aug 2023 23:36:48 GMT
EXPOSE 80
# Tue, 08 Aug 2023 23:36:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Aug 2023 23:36:48 GMT
CMD ["traefik"]
# Tue, 08 Aug 2023 23:36:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8cc6c7cf0fb882727ce9bdded1e9477cf9f51f27f262ddd2837ce010c75546`  
		Last Modified: Tue, 08 Aug 2023 23:37:08 GMT  
		Size: 622.7 KB (622688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a56f8f3e28824e8aeed3179006a8bacb5ea8697429ecdcf4b3313a11531872`  
		Last Modified: Tue, 08 Aug 2023 23:37:14 GMT  
		Size: 36.1 MB (36066881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4c24374a077bea1e909f5b61e43515993be1be29aacd3aef10a445d1447b70`  
		Last Modified: Tue, 08 Aug 2023 23:37:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-beta3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:efaf29c610c2c375ca040a7082a4e2d1070f6637656e4a8690bda7e0b6d87242
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39096640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37fe55cab162059f692a67908c2664d867103ddf7274c54454a328ddcfc2ab5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 23:21:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 21:03:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 21:03:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 21:03:40 GMT
EXPOSE 80
# Thu, 22 Jun 2023 21:03:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 21:03:40 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 21:03:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b960a271861d2b8bee110ab4afb7ec842665bbbd31f1bb9c1c279cd78d925fc`  
		Last Modified: Tue, 20 Jun 2023 23:22:04 GMT  
		Size: 624.5 KB (624502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76382258b6f8e99baf32705e376a293bc7ed29e7bd383735c51c6dec2089dc3`  
		Last Modified: Thu, 22 Jun 2023 21:03:57 GMT  
		Size: 35.1 MB (35142519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596c4d06a06800876a536dcc687884fa9aa6312a4a6d69883bf10d2a02842040`  
		Last Modified: Thu, 22 Jun 2023 21:03:53 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-beta3` - linux; s390x

```console
$ docker pull traefik@sha256:9524d85b440d108c8641a51639b18fe27525d764a76327bfe2056ccf1f53f742
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40949702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5245200a97de3f0132729144c7ad3ec05bff569700b534486980a5d5139f063e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 22:49:13 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 19:43:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 19:43:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 19:43:18 GMT
EXPOSE 80
# Thu, 22 Jun 2023 19:43:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 19:43:19 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 19:43:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6fdd3c34275458c3ea0a8688ec24b8c7698ce5a31715673ae57aa8dd5b0844`  
		Last Modified: Tue, 20 Jun 2023 22:49:39 GMT  
		Size: 622.8 KB (622821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf960d6667a0be4844e96e2d1289b0e0220f968f717a8deaa46a4b97a2fe84ad`  
		Last Modified: Thu, 22 Jun 2023 19:43:56 GMT  
		Size: 37.1 MB (37113016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ec02b13b7d2100602de0b81f0e2f099162042d9fd9e2eddacc5f7c75313ded`  
		Last Modified: Thu, 22 Jun 2023 19:43:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-beta3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:39223bfb0ad32d6f75222fc15bb3485e0dee016185f90671b4afbb6d79fa18f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `traefik:3.0.0-beta3-windowsservercore-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull traefik@sha256:d6862812720c532b092c2de682c892bdac8c0c67e6bec2b77e7323df968c4292
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1978586286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014bfe48eda2b324b4732f9a0d88fb8a0ccc6fd914fbd507568926f604439357`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jul 2023 03:41:59 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 14 Jul 2023 03:42:00 GMT
EXPOSE 80
# Fri, 14 Jul 2023 03:42:00 GMT
ENTRYPOINT ["/traefik"]
# Fri, 14 Jul 2023 03:42:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466207745a644fe73ff5acf6f1b26f0d899b68952dbe6eea34df2c8f1bc39878`  
		Last Modified: Fri, 14 Jul 2023 03:44:03 GMT  
		Size: 38.9 MB (38891610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb6b841b8c3783f4f2334cae29b1d2b8a2fc18cc0a556b277758166ba732b3b`  
		Last Modified: Fri, 14 Jul 2023 03:43:55 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950fbe16c05cf58dc8fc972ce6594dbab92250b58dcc21698f2476df0bfeaa39`  
		Last Modified: Fri, 14 Jul 2023 03:43:55 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390ea4373b029353b0cc8ec920b6d4067e1284e318edea2d82957de0fa9b853a`  
		Last Modified: Fri, 14 Jul 2023 03:43:55 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort`

```console
$ docker pull traefik@sha256:85e386ea5aa2bfb2cebc7111540f9da53d84dc4e38848339a9fc479bd942c860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:beaufort` - linux; amd64

```console
$ docker pull traefik@sha256:e5d4d00b48c51509c5b7fe051688e3d5254ae32459d822b04e845721f18f01b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42335491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60a5464b41e9a0fa02ad5c08069c9d61c3820b69ddb7539cda1ffbe66c36034`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 21 Jun 2023 00:26:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 20:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 20:20:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 20:20:11 GMT
EXPOSE 80
# Thu, 22 Jun 2023 20:20:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 20:20:11 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 20:20:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a9b499d7ae3ed84aef77186cbd2b1ae5418ddc653e721702ec1a35fa324a3`  
		Last Modified: Wed, 21 Jun 2023 00:26:31 GMT  
		Size: 622.2 KB (622241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8de7a217c34522d58e5296d7481baf74ca19f272f764c99614230fdfb6614d8`  
		Last Modified: Thu, 22 Jun 2023 20:20:30 GMT  
		Size: 38.3 MB (38315002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7429dc1ef43cddca6161c8b5989c8407cf8a2d9d8ffc38382d61b27cf27a3a69`  
		Last Modified: Thu, 22 Jun 2023 20:20:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4610ad0a08abfd441d5efea592fc370ab772915d5d62a4fe1b6ad57f5b1f7a17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39834746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c7857053ace4e793ccb85ef5e4f7039d5b2d69ef3bba2091533f1eac50eb57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:36:43 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 08 Aug 2023 23:36:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 08 Aug 2023 23:36:48 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 08 Aug 2023 23:36:48 GMT
EXPOSE 80
# Tue, 08 Aug 2023 23:36:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Aug 2023 23:36:48 GMT
CMD ["traefik"]
# Tue, 08 Aug 2023 23:36:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8cc6c7cf0fb882727ce9bdded1e9477cf9f51f27f262ddd2837ce010c75546`  
		Last Modified: Tue, 08 Aug 2023 23:37:08 GMT  
		Size: 622.7 KB (622688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a56f8f3e28824e8aeed3179006a8bacb5ea8697429ecdcf4b3313a11531872`  
		Last Modified: Tue, 08 Aug 2023 23:37:14 GMT  
		Size: 36.1 MB (36066881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4c24374a077bea1e909f5b61e43515993be1be29aacd3aef10a445d1447b70`  
		Last Modified: Tue, 08 Aug 2023 23:37:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:efaf29c610c2c375ca040a7082a4e2d1070f6637656e4a8690bda7e0b6d87242
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39096640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37fe55cab162059f692a67908c2664d867103ddf7274c54454a328ddcfc2ab5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 23:21:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 21:03:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 21:03:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 21:03:40 GMT
EXPOSE 80
# Thu, 22 Jun 2023 21:03:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 21:03:40 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 21:03:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b960a271861d2b8bee110ab4afb7ec842665bbbd31f1bb9c1c279cd78d925fc`  
		Last Modified: Tue, 20 Jun 2023 23:22:04 GMT  
		Size: 624.5 KB (624502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76382258b6f8e99baf32705e376a293bc7ed29e7bd383735c51c6dec2089dc3`  
		Last Modified: Thu, 22 Jun 2023 21:03:57 GMT  
		Size: 35.1 MB (35142519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596c4d06a06800876a536dcc687884fa9aa6312a4a6d69883bf10d2a02842040`  
		Last Modified: Thu, 22 Jun 2023 21:03:53 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; s390x

```console
$ docker pull traefik@sha256:9524d85b440d108c8641a51639b18fe27525d764a76327bfe2056ccf1f53f742
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40949702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5245200a97de3f0132729144c7ad3ec05bff569700b534486980a5d5139f063e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 22:49:13 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 19:43:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 19:43:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 19:43:18 GMT
EXPOSE 80
# Thu, 22 Jun 2023 19:43:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 19:43:19 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 19:43:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6fdd3c34275458c3ea0a8688ec24b8c7698ce5a31715673ae57aa8dd5b0844`  
		Last Modified: Tue, 20 Jun 2023 22:49:39 GMT  
		Size: 622.8 KB (622821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf960d6667a0be4844e96e2d1289b0e0220f968f717a8deaa46a4b97a2fe84ad`  
		Last Modified: Thu, 22 Jun 2023 19:43:56 GMT  
		Size: 37.1 MB (37113016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ec02b13b7d2100602de0b81f0e2f099162042d9fd9e2eddacc5f7c75313ded`  
		Last Modified: Thu, 22 Jun 2023 19:43:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort-windowsservercore-1809`

```console
$ docker pull traefik@sha256:39223bfb0ad32d6f75222fc15bb3485e0dee016185f90671b4afbb6d79fa18f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `traefik:beaufort-windowsservercore-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull traefik@sha256:d6862812720c532b092c2de682c892bdac8c0c67e6bec2b77e7323df968c4292
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1978586286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014bfe48eda2b324b4732f9a0d88fb8a0ccc6fd914fbd507568926f604439357`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jul 2023 03:41:59 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 14 Jul 2023 03:42:00 GMT
EXPOSE 80
# Fri, 14 Jul 2023 03:42:00 GMT
ENTRYPOINT ["/traefik"]
# Fri, 14 Jul 2023 03:42:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466207745a644fe73ff5acf6f1b26f0d899b68952dbe6eea34df2c8f1bc39878`  
		Last Modified: Fri, 14 Jul 2023 03:44:03 GMT  
		Size: 38.9 MB (38891610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb6b841b8c3783f4f2334cae29b1d2b8a2fc18cc0a556b277758166ba732b3b`  
		Last Modified: Fri, 14 Jul 2023 03:43:55 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950fbe16c05cf58dc8fc972ce6594dbab92250b58dcc21698f2476df0bfeaa39`  
		Last Modified: Fri, 14 Jul 2023 03:43:55 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390ea4373b029353b0cc8ec920b6d4067e1284e318edea2d82957de0fa9b853a`  
		Last Modified: Fri, 14 Jul 2023 03:43:55 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:d557ab50ff51de06b60c528ed670d8c73f21cebb2195b3eecddf7aefcad628c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:cda187e491fd290c16c972a7c2bba6dd20a3ffa8af101d84992f8f863ca0fa75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42380871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7adf08e6ff58c711a928da451587ef96dad977ea2dc85eef98fd4b551108b562`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 21 Jun 2023 00:26:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 25 Jul 2023 00:19:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 25 Jul 2023 00:19:42 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 25 Jul 2023 00:19:42 GMT
EXPOSE 80
# Tue, 25 Jul 2023 00:19:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Jul 2023 00:19:42 GMT
CMD ["traefik"]
# Tue, 25 Jul 2023 00:19:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a9b499d7ae3ed84aef77186cbd2b1ae5418ddc653e721702ec1a35fa324a3`  
		Last Modified: Wed, 21 Jun 2023 00:26:31 GMT  
		Size: 622.2 KB (622241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed0f8d1a10693b01ee2a3083246af8e1fb9f634539a0addcb433dce31535498`  
		Last Modified: Tue, 25 Jul 2023 00:20:05 GMT  
		Size: 38.4 MB (38360382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a842830f041aa03d92468d4e29754239f50a645960826ef46124a1efbc6c5386`  
		Last Modified: Tue, 25 Jul 2023 00:19:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:bcf37f90bb3c148ecc6c642f0a5ef7ecca69c107f5055a24e94de6b178038ee3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39897744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b470a25273a17965c4195798705c8c434dec9e1dcb8bed0e25cd4afd15e5a1df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:36:43 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 08 Aug 2023 23:36:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 08 Aug 2023 23:36:56 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 08 Aug 2023 23:36:56 GMT
EXPOSE 80
# Tue, 08 Aug 2023 23:36:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Aug 2023 23:36:56 GMT
CMD ["traefik"]
# Tue, 08 Aug 2023 23:36:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8cc6c7cf0fb882727ce9bdded1e9477cf9f51f27f262ddd2837ce010c75546`  
		Last Modified: Tue, 08 Aug 2023 23:37:08 GMT  
		Size: 622.7 KB (622688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f350ea2c1577d6f498d27752f1efc8de8aea15ad9cc2c8ac411a406fc06474`  
		Last Modified: Tue, 08 Aug 2023 23:37:34 GMT  
		Size: 36.1 MB (36129878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc4c23d6ff9206d00fa66fef11f0d9010dd364ced1cff33b54909008c2add1a`  
		Last Modified: Tue, 08 Aug 2023 23:37:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:464822209fa79cf4290dd21b9efdca0a28c72f8dc1fc2d1b7a01e80290a219c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39135061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a46b9a293dcb8a9cc4a0ec58acb1ff9a887e5ae62982750ad592a2ca7883209`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 23:21:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 25 Jul 2023 00:43:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 25 Jul 2023 00:43:29 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 25 Jul 2023 00:43:29 GMT
EXPOSE 80
# Tue, 25 Jul 2023 00:43:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Jul 2023 00:43:29 GMT
CMD ["traefik"]
# Tue, 25 Jul 2023 00:43:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b960a271861d2b8bee110ab4afb7ec842665bbbd31f1bb9c1c279cd78d925fc`  
		Last Modified: Tue, 20 Jun 2023 23:22:04 GMT  
		Size: 624.5 KB (624502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc8f7c18018a36bd99487bf04502db826e024f451a6a8a65f63b14f9f12587e`  
		Last Modified: Tue, 25 Jul 2023 00:43:45 GMT  
		Size: 35.2 MB (35180940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7c3aabffd24552b932f17694ea955ca9767427c4d7d6aede5be245758328c1`  
		Last Modified: Tue, 25 Jul 2023 00:43:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:53453d8365bce00f1d0fc9db847c5d0b9c7a49be32342b0bd083b7a894a3e578
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41033110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cafb27a3280df3e588ad32633b3fd03ff4def053e356151a9bbb636a754a3a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 22:49:13 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 25 Jul 2023 00:03:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 25 Jul 2023 00:03:36 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 25 Jul 2023 00:03:37 GMT
EXPOSE 80
# Tue, 25 Jul 2023 00:03:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Jul 2023 00:03:37 GMT
CMD ["traefik"]
# Tue, 25 Jul 2023 00:03:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6fdd3c34275458c3ea0a8688ec24b8c7698ce5a31715673ae57aa8dd5b0844`  
		Last Modified: Tue, 20 Jun 2023 22:49:39 GMT  
		Size: 622.8 KB (622821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6158db5bbbb90d5afe7f56e0eec15dea136038213b9ab2f9a478924bf671802`  
		Last Modified: Tue, 25 Jul 2023 00:04:04 GMT  
		Size: 37.2 MB (37196424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be121cfc0faefca1a55460f6f2a4f500fcb355e64c8458a91c213c890c2f8df1`  
		Last Modified: Tue, 25 Jul 2023 00:03:58 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:saintmarcelin`

```console
$ docker pull traefik@sha256:d557ab50ff51de06b60c528ed670d8c73f21cebb2195b3eecddf7aefcad628c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:saintmarcelin` - linux; amd64

```console
$ docker pull traefik@sha256:cda187e491fd290c16c972a7c2bba6dd20a3ffa8af101d84992f8f863ca0fa75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42380871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7adf08e6ff58c711a928da451587ef96dad977ea2dc85eef98fd4b551108b562`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 21 Jun 2023 00:26:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 25 Jul 2023 00:19:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 25 Jul 2023 00:19:42 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 25 Jul 2023 00:19:42 GMT
EXPOSE 80
# Tue, 25 Jul 2023 00:19:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Jul 2023 00:19:42 GMT
CMD ["traefik"]
# Tue, 25 Jul 2023 00:19:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a9b499d7ae3ed84aef77186cbd2b1ae5418ddc653e721702ec1a35fa324a3`  
		Last Modified: Wed, 21 Jun 2023 00:26:31 GMT  
		Size: 622.2 KB (622241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed0f8d1a10693b01ee2a3083246af8e1fb9f634539a0addcb433dce31535498`  
		Last Modified: Tue, 25 Jul 2023 00:20:05 GMT  
		Size: 38.4 MB (38360382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a842830f041aa03d92468d4e29754239f50a645960826ef46124a1efbc6c5386`  
		Last Modified: Tue, 25 Jul 2023 00:19:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:saintmarcelin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:bcf37f90bb3c148ecc6c642f0a5ef7ecca69c107f5055a24e94de6b178038ee3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39897744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b470a25273a17965c4195798705c8c434dec9e1dcb8bed0e25cd4afd15e5a1df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:36:43 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 08 Aug 2023 23:36:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 08 Aug 2023 23:36:56 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 08 Aug 2023 23:36:56 GMT
EXPOSE 80
# Tue, 08 Aug 2023 23:36:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Aug 2023 23:36:56 GMT
CMD ["traefik"]
# Tue, 08 Aug 2023 23:36:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8cc6c7cf0fb882727ce9bdded1e9477cf9f51f27f262ddd2837ce010c75546`  
		Last Modified: Tue, 08 Aug 2023 23:37:08 GMT  
		Size: 622.7 KB (622688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f350ea2c1577d6f498d27752f1efc8de8aea15ad9cc2c8ac411a406fc06474`  
		Last Modified: Tue, 08 Aug 2023 23:37:34 GMT  
		Size: 36.1 MB (36129878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc4c23d6ff9206d00fa66fef11f0d9010dd364ced1cff33b54909008c2add1a`  
		Last Modified: Tue, 08 Aug 2023 23:37:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:saintmarcelin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:464822209fa79cf4290dd21b9efdca0a28c72f8dc1fc2d1b7a01e80290a219c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39135061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a46b9a293dcb8a9cc4a0ec58acb1ff9a887e5ae62982750ad592a2ca7883209`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 23:21:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 25 Jul 2023 00:43:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 25 Jul 2023 00:43:29 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 25 Jul 2023 00:43:29 GMT
EXPOSE 80
# Tue, 25 Jul 2023 00:43:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Jul 2023 00:43:29 GMT
CMD ["traefik"]
# Tue, 25 Jul 2023 00:43:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b960a271861d2b8bee110ab4afb7ec842665bbbd31f1bb9c1c279cd78d925fc`  
		Last Modified: Tue, 20 Jun 2023 23:22:04 GMT  
		Size: 624.5 KB (624502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc8f7c18018a36bd99487bf04502db826e024f451a6a8a65f63b14f9f12587e`  
		Last Modified: Tue, 25 Jul 2023 00:43:45 GMT  
		Size: 35.2 MB (35180940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7c3aabffd24552b932f17694ea955ca9767427c4d7d6aede5be245758328c1`  
		Last Modified: Tue, 25 Jul 2023 00:43:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:saintmarcelin` - linux; s390x

```console
$ docker pull traefik@sha256:53453d8365bce00f1d0fc9db847c5d0b9c7a49be32342b0bd083b7a894a3e578
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41033110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cafb27a3280df3e588ad32633b3fd03ff4def053e356151a9bbb636a754a3a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 22:49:13 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 25 Jul 2023 00:03:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 25 Jul 2023 00:03:36 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 25 Jul 2023 00:03:37 GMT
EXPOSE 80
# Tue, 25 Jul 2023 00:03:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Jul 2023 00:03:37 GMT
CMD ["traefik"]
# Tue, 25 Jul 2023 00:03:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6fdd3c34275458c3ea0a8688ec24b8c7698ce5a31715673ae57aa8dd5b0844`  
		Last Modified: Tue, 20 Jun 2023 22:49:39 GMT  
		Size: 622.8 KB (622821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6158db5bbbb90d5afe7f56e0eec15dea136038213b9ab2f9a478924bf671802`  
		Last Modified: Tue, 25 Jul 2023 00:04:04 GMT  
		Size: 37.2 MB (37196424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be121cfc0faefca1a55460f6f2a4f500fcb355e64c8458a91c213c890c2f8df1`  
		Last Modified: Tue, 25 Jul 2023 00:03:58 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:saintmarcelin-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7b1d7933d34be8cb94a98c21e2012d094aacf7588f986e2c44ab1ac23e58c8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `traefik:saintmarcelin-windowsservercore-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull traefik@sha256:fdb540f2c6a721b012defd44bd25dde874a55f609fc3b880d67db28f424cf9a7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1978644570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab3df456f37590d20edb73827d45b4c85cf4b13b906310b855eb98f6cfcbbb2`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Jul 2023 22:45:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 24 Jul 2023 22:45:10 GMT
EXPOSE 80
# Mon, 24 Jul 2023 22:45:10 GMT
ENTRYPOINT ["/traefik"]
# Mon, 24 Jul 2023 22:45:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5aca5a8f07b6697cf4ed1b44c7cd6c3a737387a3303978a503bd9cf0c3623f`  
		Last Modified: Mon, 24 Jul 2023 22:45:49 GMT  
		Size: 38.9 MB (38949881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba21efd5ef6c3fc2fb79d8b27d9db2ed4a703d85260d8d42b81f17cc8441cf2`  
		Last Modified: Mon, 24 Jul 2023 22:45:41 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c979aa71e159870dc2fa120e7446a3ace60f72788635511544790363c89637`  
		Last Modified: Mon, 24 Jul 2023 22:45:41 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1476200a7b3fbc5f2081c68313f321e5e2dbf3ca2f5fa8b6fc146a47729ff7f`  
		Last Modified: Mon, 24 Jul 2023 22:45:41 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.10`

```console
$ docker pull traefik@sha256:d557ab50ff51de06b60c528ed670d8c73f21cebb2195b3eecddf7aefcad628c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v2.10` - linux; amd64

```console
$ docker pull traefik@sha256:cda187e491fd290c16c972a7c2bba6dd20a3ffa8af101d84992f8f863ca0fa75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42380871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7adf08e6ff58c711a928da451587ef96dad977ea2dc85eef98fd4b551108b562`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 21 Jun 2023 00:26:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 25 Jul 2023 00:19:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 25 Jul 2023 00:19:42 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 25 Jul 2023 00:19:42 GMT
EXPOSE 80
# Tue, 25 Jul 2023 00:19:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Jul 2023 00:19:42 GMT
CMD ["traefik"]
# Tue, 25 Jul 2023 00:19:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a9b499d7ae3ed84aef77186cbd2b1ae5418ddc653e721702ec1a35fa324a3`  
		Last Modified: Wed, 21 Jun 2023 00:26:31 GMT  
		Size: 622.2 KB (622241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed0f8d1a10693b01ee2a3083246af8e1fb9f634539a0addcb433dce31535498`  
		Last Modified: Tue, 25 Jul 2023 00:20:05 GMT  
		Size: 38.4 MB (38360382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a842830f041aa03d92468d4e29754239f50a645960826ef46124a1efbc6c5386`  
		Last Modified: Tue, 25 Jul 2023 00:19:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.10` - linux; arm variant v6

```console
$ docker pull traefik@sha256:bcf37f90bb3c148ecc6c642f0a5ef7ecca69c107f5055a24e94de6b178038ee3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39897744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b470a25273a17965c4195798705c8c434dec9e1dcb8bed0e25cd4afd15e5a1df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:36:43 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 08 Aug 2023 23:36:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 08 Aug 2023 23:36:56 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 08 Aug 2023 23:36:56 GMT
EXPOSE 80
# Tue, 08 Aug 2023 23:36:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Aug 2023 23:36:56 GMT
CMD ["traefik"]
# Tue, 08 Aug 2023 23:36:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8cc6c7cf0fb882727ce9bdded1e9477cf9f51f27f262ddd2837ce010c75546`  
		Last Modified: Tue, 08 Aug 2023 23:37:08 GMT  
		Size: 622.7 KB (622688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f350ea2c1577d6f498d27752f1efc8de8aea15ad9cc2c8ac411a406fc06474`  
		Last Modified: Tue, 08 Aug 2023 23:37:34 GMT  
		Size: 36.1 MB (36129878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc4c23d6ff9206d00fa66fef11f0d9010dd364ced1cff33b54909008c2add1a`  
		Last Modified: Tue, 08 Aug 2023 23:37:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.10` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:464822209fa79cf4290dd21b9efdca0a28c72f8dc1fc2d1b7a01e80290a219c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39135061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a46b9a293dcb8a9cc4a0ec58acb1ff9a887e5ae62982750ad592a2ca7883209`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 23:21:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 25 Jul 2023 00:43:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 25 Jul 2023 00:43:29 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 25 Jul 2023 00:43:29 GMT
EXPOSE 80
# Tue, 25 Jul 2023 00:43:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Jul 2023 00:43:29 GMT
CMD ["traefik"]
# Tue, 25 Jul 2023 00:43:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b960a271861d2b8bee110ab4afb7ec842665bbbd31f1bb9c1c279cd78d925fc`  
		Last Modified: Tue, 20 Jun 2023 23:22:04 GMT  
		Size: 624.5 KB (624502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc8f7c18018a36bd99487bf04502db826e024f451a6a8a65f63b14f9f12587e`  
		Last Modified: Tue, 25 Jul 2023 00:43:45 GMT  
		Size: 35.2 MB (35180940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7c3aabffd24552b932f17694ea955ca9767427c4d7d6aede5be245758328c1`  
		Last Modified: Tue, 25 Jul 2023 00:43:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.10` - linux; s390x

```console
$ docker pull traefik@sha256:53453d8365bce00f1d0fc9db847c5d0b9c7a49be32342b0bd083b7a894a3e578
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41033110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cafb27a3280df3e588ad32633b3fd03ff4def053e356151a9bbb636a754a3a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 22:49:13 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 25 Jul 2023 00:03:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 25 Jul 2023 00:03:36 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 25 Jul 2023 00:03:37 GMT
EXPOSE 80
# Tue, 25 Jul 2023 00:03:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Jul 2023 00:03:37 GMT
CMD ["traefik"]
# Tue, 25 Jul 2023 00:03:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6fdd3c34275458c3ea0a8688ec24b8c7698ce5a31715673ae57aa8dd5b0844`  
		Last Modified: Tue, 20 Jun 2023 22:49:39 GMT  
		Size: 622.8 KB (622821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6158db5bbbb90d5afe7f56e0eec15dea136038213b9ab2f9a478924bf671802`  
		Last Modified: Tue, 25 Jul 2023 00:04:04 GMT  
		Size: 37.2 MB (37196424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be121cfc0faefca1a55460f6f2a4f500fcb355e64c8458a91c213c890c2f8df1`  
		Last Modified: Tue, 25 Jul 2023 00:03:58 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.10-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7b1d7933d34be8cb94a98c21e2012d094aacf7588f986e2c44ab1ac23e58c8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `traefik:v2.10-windowsservercore-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull traefik@sha256:fdb540f2c6a721b012defd44bd25dde874a55f609fc3b880d67db28f424cf9a7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1978644570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab3df456f37590d20edb73827d45b4c85cf4b13b906310b855eb98f6cfcbbb2`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Jul 2023 22:45:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 24 Jul 2023 22:45:10 GMT
EXPOSE 80
# Mon, 24 Jul 2023 22:45:10 GMT
ENTRYPOINT ["/traefik"]
# Mon, 24 Jul 2023 22:45:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5aca5a8f07b6697cf4ed1b44c7cd6c3a737387a3303978a503bd9cf0c3623f`  
		Last Modified: Mon, 24 Jul 2023 22:45:49 GMT  
		Size: 38.9 MB (38949881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba21efd5ef6c3fc2fb79d8b27d9db2ed4a703d85260d8d42b81f17cc8441cf2`  
		Last Modified: Mon, 24 Jul 2023 22:45:41 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c979aa71e159870dc2fa120e7446a3ace60f72788635511544790363c89637`  
		Last Modified: Mon, 24 Jul 2023 22:45:41 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1476200a7b3fbc5f2081c68313f321e5e2dbf3ca2f5fa8b6fc146a47729ff7f`  
		Last Modified: Mon, 24 Jul 2023 22:45:41 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.10.4`

```console
$ docker pull traefik@sha256:d557ab50ff51de06b60c528ed670d8c73f21cebb2195b3eecddf7aefcad628c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v2.10.4` - linux; amd64

```console
$ docker pull traefik@sha256:cda187e491fd290c16c972a7c2bba6dd20a3ffa8af101d84992f8f863ca0fa75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42380871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7adf08e6ff58c711a928da451587ef96dad977ea2dc85eef98fd4b551108b562`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 21 Jun 2023 00:26:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 25 Jul 2023 00:19:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 25 Jul 2023 00:19:42 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 25 Jul 2023 00:19:42 GMT
EXPOSE 80
# Tue, 25 Jul 2023 00:19:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Jul 2023 00:19:42 GMT
CMD ["traefik"]
# Tue, 25 Jul 2023 00:19:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a9b499d7ae3ed84aef77186cbd2b1ae5418ddc653e721702ec1a35fa324a3`  
		Last Modified: Wed, 21 Jun 2023 00:26:31 GMT  
		Size: 622.2 KB (622241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed0f8d1a10693b01ee2a3083246af8e1fb9f634539a0addcb433dce31535498`  
		Last Modified: Tue, 25 Jul 2023 00:20:05 GMT  
		Size: 38.4 MB (38360382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a842830f041aa03d92468d4e29754239f50a645960826ef46124a1efbc6c5386`  
		Last Modified: Tue, 25 Jul 2023 00:19:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.10.4` - linux; arm variant v6

```console
$ docker pull traefik@sha256:bcf37f90bb3c148ecc6c642f0a5ef7ecca69c107f5055a24e94de6b178038ee3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39897744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b470a25273a17965c4195798705c8c434dec9e1dcb8bed0e25cd4afd15e5a1df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:36:43 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 08 Aug 2023 23:36:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 08 Aug 2023 23:36:56 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 08 Aug 2023 23:36:56 GMT
EXPOSE 80
# Tue, 08 Aug 2023 23:36:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Aug 2023 23:36:56 GMT
CMD ["traefik"]
# Tue, 08 Aug 2023 23:36:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8cc6c7cf0fb882727ce9bdded1e9477cf9f51f27f262ddd2837ce010c75546`  
		Last Modified: Tue, 08 Aug 2023 23:37:08 GMT  
		Size: 622.7 KB (622688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f350ea2c1577d6f498d27752f1efc8de8aea15ad9cc2c8ac411a406fc06474`  
		Last Modified: Tue, 08 Aug 2023 23:37:34 GMT  
		Size: 36.1 MB (36129878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc4c23d6ff9206d00fa66fef11f0d9010dd364ced1cff33b54909008c2add1a`  
		Last Modified: Tue, 08 Aug 2023 23:37:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.10.4` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:464822209fa79cf4290dd21b9efdca0a28c72f8dc1fc2d1b7a01e80290a219c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39135061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a46b9a293dcb8a9cc4a0ec58acb1ff9a887e5ae62982750ad592a2ca7883209`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 23:21:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 25 Jul 2023 00:43:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 25 Jul 2023 00:43:29 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 25 Jul 2023 00:43:29 GMT
EXPOSE 80
# Tue, 25 Jul 2023 00:43:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Jul 2023 00:43:29 GMT
CMD ["traefik"]
# Tue, 25 Jul 2023 00:43:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b960a271861d2b8bee110ab4afb7ec842665bbbd31f1bb9c1c279cd78d925fc`  
		Last Modified: Tue, 20 Jun 2023 23:22:04 GMT  
		Size: 624.5 KB (624502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc8f7c18018a36bd99487bf04502db826e024f451a6a8a65f63b14f9f12587e`  
		Last Modified: Tue, 25 Jul 2023 00:43:45 GMT  
		Size: 35.2 MB (35180940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7c3aabffd24552b932f17694ea955ca9767427c4d7d6aede5be245758328c1`  
		Last Modified: Tue, 25 Jul 2023 00:43:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.10.4` - linux; s390x

```console
$ docker pull traefik@sha256:53453d8365bce00f1d0fc9db847c5d0b9c7a49be32342b0bd083b7a894a3e578
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41033110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cafb27a3280df3e588ad32633b3fd03ff4def053e356151a9bbb636a754a3a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 22:49:13 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 25 Jul 2023 00:03:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 25 Jul 2023 00:03:36 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 25 Jul 2023 00:03:37 GMT
EXPOSE 80
# Tue, 25 Jul 2023 00:03:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Jul 2023 00:03:37 GMT
CMD ["traefik"]
# Tue, 25 Jul 2023 00:03:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6fdd3c34275458c3ea0a8688ec24b8c7698ce5a31715673ae57aa8dd5b0844`  
		Last Modified: Tue, 20 Jun 2023 22:49:39 GMT  
		Size: 622.8 KB (622821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6158db5bbbb90d5afe7f56e0eec15dea136038213b9ab2f9a478924bf671802`  
		Last Modified: Tue, 25 Jul 2023 00:04:04 GMT  
		Size: 37.2 MB (37196424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be121cfc0faefca1a55460f6f2a4f500fcb355e64c8458a91c213c890c2f8df1`  
		Last Modified: Tue, 25 Jul 2023 00:03:58 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.10.4-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7b1d7933d34be8cb94a98c21e2012d094aacf7588f986e2c44ab1ac23e58c8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `traefik:v2.10.4-windowsservercore-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull traefik@sha256:fdb540f2c6a721b012defd44bd25dde874a55f609fc3b880d67db28f424cf9a7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1978644570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab3df456f37590d20edb73827d45b4c85cf4b13b906310b855eb98f6cfcbbb2`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Jul 2023 22:45:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 24 Jul 2023 22:45:10 GMT
EXPOSE 80
# Mon, 24 Jul 2023 22:45:10 GMT
ENTRYPOINT ["/traefik"]
# Mon, 24 Jul 2023 22:45:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5aca5a8f07b6697cf4ed1b44c7cd6c3a737387a3303978a503bd9cf0c3623f`  
		Last Modified: Mon, 24 Jul 2023 22:45:49 GMT  
		Size: 38.9 MB (38949881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba21efd5ef6c3fc2fb79d8b27d9db2ed4a703d85260d8d42b81f17cc8441cf2`  
		Last Modified: Mon, 24 Jul 2023 22:45:41 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c979aa71e159870dc2fa120e7446a3ace60f72788635511544790363c89637`  
		Last Modified: Mon, 24 Jul 2023 22:45:41 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1476200a7b3fbc5f2081c68313f321e5e2dbf3ca2f5fa8b6fc146a47729ff7f`  
		Last Modified: Mon, 24 Jul 2023 22:45:41 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0`

```console
$ docker pull traefik@sha256:85e386ea5aa2bfb2cebc7111540f9da53d84dc4e38848339a9fc479bd942c860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v3.0` - linux; amd64

```console
$ docker pull traefik@sha256:e5d4d00b48c51509c5b7fe051688e3d5254ae32459d822b04e845721f18f01b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42335491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60a5464b41e9a0fa02ad5c08069c9d61c3820b69ddb7539cda1ffbe66c36034`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 21 Jun 2023 00:26:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 20:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 20:20:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 20:20:11 GMT
EXPOSE 80
# Thu, 22 Jun 2023 20:20:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 20:20:11 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 20:20:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a9b499d7ae3ed84aef77186cbd2b1ae5418ddc653e721702ec1a35fa324a3`  
		Last Modified: Wed, 21 Jun 2023 00:26:31 GMT  
		Size: 622.2 KB (622241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8de7a217c34522d58e5296d7481baf74ca19f272f764c99614230fdfb6614d8`  
		Last Modified: Thu, 22 Jun 2023 20:20:30 GMT  
		Size: 38.3 MB (38315002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7429dc1ef43cddca6161c8b5989c8407cf8a2d9d8ffc38382d61b27cf27a3a69`  
		Last Modified: Thu, 22 Jun 2023 20:20:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4610ad0a08abfd441d5efea592fc370ab772915d5d62a4fe1b6ad57f5b1f7a17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39834746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c7857053ace4e793ccb85ef5e4f7039d5b2d69ef3bba2091533f1eac50eb57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:36:43 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 08 Aug 2023 23:36:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 08 Aug 2023 23:36:48 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 08 Aug 2023 23:36:48 GMT
EXPOSE 80
# Tue, 08 Aug 2023 23:36:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Aug 2023 23:36:48 GMT
CMD ["traefik"]
# Tue, 08 Aug 2023 23:36:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8cc6c7cf0fb882727ce9bdded1e9477cf9f51f27f262ddd2837ce010c75546`  
		Last Modified: Tue, 08 Aug 2023 23:37:08 GMT  
		Size: 622.7 KB (622688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a56f8f3e28824e8aeed3179006a8bacb5ea8697429ecdcf4b3313a11531872`  
		Last Modified: Tue, 08 Aug 2023 23:37:14 GMT  
		Size: 36.1 MB (36066881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4c24374a077bea1e909f5b61e43515993be1be29aacd3aef10a445d1447b70`  
		Last Modified: Tue, 08 Aug 2023 23:37:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:efaf29c610c2c375ca040a7082a4e2d1070f6637656e4a8690bda7e0b6d87242
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39096640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37fe55cab162059f692a67908c2664d867103ddf7274c54454a328ddcfc2ab5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 23:21:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 21:03:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 21:03:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 21:03:40 GMT
EXPOSE 80
# Thu, 22 Jun 2023 21:03:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 21:03:40 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 21:03:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b960a271861d2b8bee110ab4afb7ec842665bbbd31f1bb9c1c279cd78d925fc`  
		Last Modified: Tue, 20 Jun 2023 23:22:04 GMT  
		Size: 624.5 KB (624502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76382258b6f8e99baf32705e376a293bc7ed29e7bd383735c51c6dec2089dc3`  
		Last Modified: Thu, 22 Jun 2023 21:03:57 GMT  
		Size: 35.1 MB (35142519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596c4d06a06800876a536dcc687884fa9aa6312a4a6d69883bf10d2a02842040`  
		Last Modified: Thu, 22 Jun 2023 21:03:53 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; s390x

```console
$ docker pull traefik@sha256:9524d85b440d108c8641a51639b18fe27525d764a76327bfe2056ccf1f53f742
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40949702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5245200a97de3f0132729144c7ad3ec05bff569700b534486980a5d5139f063e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 22:49:13 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 19:43:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 19:43:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 19:43:18 GMT
EXPOSE 80
# Thu, 22 Jun 2023 19:43:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 19:43:19 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 19:43:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6fdd3c34275458c3ea0a8688ec24b8c7698ce5a31715673ae57aa8dd5b0844`  
		Last Modified: Tue, 20 Jun 2023 22:49:39 GMT  
		Size: 622.8 KB (622821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf960d6667a0be4844e96e2d1289b0e0220f968f717a8deaa46a4b97a2fe84ad`  
		Last Modified: Thu, 22 Jun 2023 19:43:56 GMT  
		Size: 37.1 MB (37113016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ec02b13b7d2100602de0b81f0e2f099162042d9fd9e2eddacc5f7c75313ded`  
		Last Modified: Thu, 22 Jun 2023 19:43:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:39223bfb0ad32d6f75222fc15bb3485e0dee016185f90671b4afbb6d79fa18f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `traefik:v3.0-windowsservercore-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull traefik@sha256:d6862812720c532b092c2de682c892bdac8c0c67e6bec2b77e7323df968c4292
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1978586286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014bfe48eda2b324b4732f9a0d88fb8a0ccc6fd914fbd507568926f604439357`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jul 2023 03:41:59 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 14 Jul 2023 03:42:00 GMT
EXPOSE 80
# Fri, 14 Jul 2023 03:42:00 GMT
ENTRYPOINT ["/traefik"]
# Fri, 14 Jul 2023 03:42:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466207745a644fe73ff5acf6f1b26f0d899b68952dbe6eea34df2c8f1bc39878`  
		Last Modified: Fri, 14 Jul 2023 03:44:03 GMT  
		Size: 38.9 MB (38891610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb6b841b8c3783f4f2334cae29b1d2b8a2fc18cc0a556b277758166ba732b3b`  
		Last Modified: Fri, 14 Jul 2023 03:43:55 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950fbe16c05cf58dc8fc972ce6594dbab92250b58dcc21698f2476df0bfeaa39`  
		Last Modified: Fri, 14 Jul 2023 03:43:55 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390ea4373b029353b0cc8ec920b6d4067e1284e318edea2d82957de0fa9b853a`  
		Last Modified: Fri, 14 Jul 2023 03:43:55 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-beta3`

```console
$ docker pull traefik@sha256:85e386ea5aa2bfb2cebc7111540f9da53d84dc4e38848339a9fc479bd942c860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v3.0.0-beta3` - linux; amd64

```console
$ docker pull traefik@sha256:e5d4d00b48c51509c5b7fe051688e3d5254ae32459d822b04e845721f18f01b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42335491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60a5464b41e9a0fa02ad5c08069c9d61c3820b69ddb7539cda1ffbe66c36034`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 21 Jun 2023 00:26:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 20:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 20:20:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 20:20:11 GMT
EXPOSE 80
# Thu, 22 Jun 2023 20:20:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 20:20:11 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 20:20:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a9b499d7ae3ed84aef77186cbd2b1ae5418ddc653e721702ec1a35fa324a3`  
		Last Modified: Wed, 21 Jun 2023 00:26:31 GMT  
		Size: 622.2 KB (622241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8de7a217c34522d58e5296d7481baf74ca19f272f764c99614230fdfb6614d8`  
		Last Modified: Thu, 22 Jun 2023 20:20:30 GMT  
		Size: 38.3 MB (38315002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7429dc1ef43cddca6161c8b5989c8407cf8a2d9d8ffc38382d61b27cf27a3a69`  
		Last Modified: Thu, 22 Jun 2023 20:20:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-beta3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4610ad0a08abfd441d5efea592fc370ab772915d5d62a4fe1b6ad57f5b1f7a17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39834746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c7857053ace4e793ccb85ef5e4f7039d5b2d69ef3bba2091533f1eac50eb57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:36:43 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 08 Aug 2023 23:36:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 08 Aug 2023 23:36:48 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 08 Aug 2023 23:36:48 GMT
EXPOSE 80
# Tue, 08 Aug 2023 23:36:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Aug 2023 23:36:48 GMT
CMD ["traefik"]
# Tue, 08 Aug 2023 23:36:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8cc6c7cf0fb882727ce9bdded1e9477cf9f51f27f262ddd2837ce010c75546`  
		Last Modified: Tue, 08 Aug 2023 23:37:08 GMT  
		Size: 622.7 KB (622688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a56f8f3e28824e8aeed3179006a8bacb5ea8697429ecdcf4b3313a11531872`  
		Last Modified: Tue, 08 Aug 2023 23:37:14 GMT  
		Size: 36.1 MB (36066881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4c24374a077bea1e909f5b61e43515993be1be29aacd3aef10a445d1447b70`  
		Last Modified: Tue, 08 Aug 2023 23:37:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-beta3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:efaf29c610c2c375ca040a7082a4e2d1070f6637656e4a8690bda7e0b6d87242
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39096640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37fe55cab162059f692a67908c2664d867103ddf7274c54454a328ddcfc2ab5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 23:21:47 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 21:03:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 21:03:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 21:03:40 GMT
EXPOSE 80
# Thu, 22 Jun 2023 21:03:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 21:03:40 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 21:03:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b960a271861d2b8bee110ab4afb7ec842665bbbd31f1bb9c1c279cd78d925fc`  
		Last Modified: Tue, 20 Jun 2023 23:22:04 GMT  
		Size: 624.5 KB (624502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76382258b6f8e99baf32705e376a293bc7ed29e7bd383735c51c6dec2089dc3`  
		Last Modified: Thu, 22 Jun 2023 21:03:57 GMT  
		Size: 35.1 MB (35142519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596c4d06a06800876a536dcc687884fa9aa6312a4a6d69883bf10d2a02842040`  
		Last Modified: Thu, 22 Jun 2023 21:03:53 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-beta3` - linux; s390x

```console
$ docker pull traefik@sha256:9524d85b440d108c8641a51639b18fe27525d764a76327bfe2056ccf1f53f742
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40949702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5245200a97de3f0132729144c7ad3ec05bff569700b534486980a5d5139f063e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Tue, 20 Jun 2023 22:49:13 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 22 Jun 2023 19:43:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 22 Jun 2023 19:43:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 22 Jun 2023 19:43:18 GMT
EXPOSE 80
# Thu, 22 Jun 2023 19:43:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jun 2023 19:43:19 GMT
CMD ["traefik"]
# Thu, 22 Jun 2023 19:43:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6fdd3c34275458c3ea0a8688ec24b8c7698ce5a31715673ae57aa8dd5b0844`  
		Last Modified: Tue, 20 Jun 2023 22:49:39 GMT  
		Size: 622.8 KB (622821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf960d6667a0be4844e96e2d1289b0e0220f968f717a8deaa46a4b97a2fe84ad`  
		Last Modified: Thu, 22 Jun 2023 19:43:56 GMT  
		Size: 37.1 MB (37113016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ec02b13b7d2100602de0b81f0e2f099162042d9fd9e2eddacc5f7c75313ded`  
		Last Modified: Thu, 22 Jun 2023 19:43:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-beta3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:39223bfb0ad32d6f75222fc15bb3485e0dee016185f90671b4afbb6d79fa18f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `traefik:v3.0.0-beta3-windowsservercore-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull traefik@sha256:d6862812720c532b092c2de682c892bdac8c0c67e6bec2b77e7323df968c4292
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1978586286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014bfe48eda2b324b4732f9a0d88fb8a0ccc6fd914fbd507568926f604439357`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jul 2023 03:41:59 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta3/traefik_v3.0.0-beta3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 14 Jul 2023 03:42:00 GMT
EXPOSE 80
# Fri, 14 Jul 2023 03:42:00 GMT
ENTRYPOINT ["/traefik"]
# Fri, 14 Jul 2023 03:42:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466207745a644fe73ff5acf6f1b26f0d899b68952dbe6eea34df2c8f1bc39878`  
		Last Modified: Fri, 14 Jul 2023 03:44:03 GMT  
		Size: 38.9 MB (38891610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb6b841b8c3783f4f2334cae29b1d2b8a2fc18cc0a556b277758166ba732b3b`  
		Last Modified: Fri, 14 Jul 2023 03:43:55 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950fbe16c05cf58dc8fc972ce6594dbab92250b58dcc21698f2476df0bfeaa39`  
		Last Modified: Fri, 14 Jul 2023 03:43:55 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390ea4373b029353b0cc8ec920b6d4067e1284e318edea2d82957de0fa9b853a`  
		Last Modified: Fri, 14 Jul 2023 03:43:55 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:7b1d7933d34be8cb94a98c21e2012d094aacf7588f986e2c44ab1ac23e58c8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull traefik@sha256:fdb540f2c6a721b012defd44bd25dde874a55f609fc3b880d67db28f424cf9a7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1978644570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab3df456f37590d20edb73827d45b4c85cf4b13b906310b855eb98f6cfcbbb2`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Jul 2023 22:45:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 24 Jul 2023 22:45:10 GMT
EXPOSE 80
# Mon, 24 Jul 2023 22:45:10 GMT
ENTRYPOINT ["/traefik"]
# Mon, 24 Jul 2023 22:45:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5aca5a8f07b6697cf4ed1b44c7cd6c3a737387a3303978a503bd9cf0c3623f`  
		Last Modified: Mon, 24 Jul 2023 22:45:49 GMT  
		Size: 38.9 MB (38949881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba21efd5ef6c3fc2fb79d8b27d9db2ed4a703d85260d8d42b81f17cc8441cf2`  
		Last Modified: Mon, 24 Jul 2023 22:45:41 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c979aa71e159870dc2fa120e7446a3ace60f72788635511544790363c89637`  
		Last Modified: Mon, 24 Jul 2023 22:45:41 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1476200a7b3fbc5f2081c68313f321e5e2dbf3ca2f5fa8b6fc146a47729ff7f`  
		Last Modified: Mon, 24 Jul 2023 22:45:41 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
