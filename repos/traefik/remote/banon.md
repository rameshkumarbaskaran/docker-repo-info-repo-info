## `traefik:banon`

```console
$ docker pull traefik@sha256:8d81a9df1435f9f3d36ac9398465ef2d5d61e671059974db753faaed14b627de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:banon` - linux; amd64

```console
$ docker pull traefik@sha256:6dee6938b5ebfc511a82ef4e09c80268835a2f67393e5c06c3e4ef9a14d1817b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39613072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e26b5f8193d713eb8f39d0ab0e3d513278f86e41644b07e189e1aef536b335`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 02:37:38 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 06 Apr 2023 18:24:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.10/traefik_v2.9.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 06 Apr 2023 18:24:44 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 06 Apr 2023 18:24:44 GMT
EXPOSE 80
# Thu, 06 Apr 2023 18:24:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Apr 2023 18:24:44 GMT
CMD ["traefik"]
# Thu, 06 Apr 2023 18:24:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d055169f9c6f7e08b88a6ef90eba203750fcc51761ecb994e40aa2aaa640ff72`  
		Last Modified: Thu, 30 Mar 2023 02:38:35 GMT  
		Size: 622.2 KB (622239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afaddc85d79e665b30c4ee7ce9fc12425532f4695c6888b052086589f12aa687`  
		Last Modified: Thu, 06 Apr 2023 18:25:11 GMT  
		Size: 35.6 MB (35615902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff733a62a1272d7fe4817f1b3a8faf56c8a7f0e3808baec593378d274c1d081`  
		Last Modified: Thu, 06 Apr 2023 18:25:06 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:banon` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f76a8f0c2b54429df275eb7e842171230994dc28924cb17f65ca41a3c5cb94fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37257635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c077549480f6828d39797ca3855e6299d0c1e7daf08d67cd62320c07515ff0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 00:39:39 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 06 Apr 2023 18:49:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.10/traefik_v2.9.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 06 Apr 2023 18:49:31 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 06 Apr 2023 18:49:31 GMT
EXPOSE 80
# Thu, 06 Apr 2023 18:49:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Apr 2023 18:49:31 GMT
CMD ["traefik"]
# Thu, 06 Apr 2023 18:49:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bd7901efecc8425b6d98584a9ee5d091a238a8936fb50b8aa4654afb90d05d`  
		Last Modified: Thu, 30 Mar 2023 00:41:05 GMT  
		Size: 624.4 KB (624425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658599efc3390617789f600a87686c808ae0c26e3a0a310ca9ad50944f5061f2`  
		Last Modified: Thu, 06 Apr 2023 18:49:58 GMT  
		Size: 33.5 MB (33522040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39827a939bd6089039662bd6dc0237923c0b6b7d177fcf7f37bdcb9dcaf831ee`  
		Last Modified: Thu, 06 Apr 2023 18:49:52 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:banon` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:7b1ecf3dcf9d504f037e14d060c7bfcb87ebde442eaf3c1d89e0c2e2f180a987
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36503424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fa39db0cea458044cad085ee32cf6bb615ccff2f3f7bbbc5e57f9b36984afb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:18 GMT
ADD file:e51d4089e73ad6dee52b31f0c8059a00c17df6e23f6741fe11b43bd84cc99008 in / 
# Wed, 29 Mar 2023 17:39:18 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 03:26:37 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 06 Apr 2023 18:51:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.10/traefik_v2.9.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 06 Apr 2023 18:51:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 06 Apr 2023 18:51:04 GMT
EXPOSE 80
# Thu, 06 Apr 2023 18:51:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Apr 2023 18:51:04 GMT
CMD ["traefik"]
# Thu, 06 Apr 2023 18:51:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c41833b44d910632b415cd89a9cdaa4d62c9725dc56c99a7ddadafd6719960f9`  
		Last Modified: Wed, 29 Mar 2023 17:39:44 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4336eee5b1b811f9668d2251fb67e6099c4089ef7b26ade14aacd2f5f0982e06`  
		Last Modified: Thu, 30 Mar 2023 03:27:34 GMT  
		Size: 624.2 KB (624204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9cadb05aa1b060d980fd3437917259c39ca7d9fb914fccd2d05ba2c3ac9d1e`  
		Last Modified: Thu, 06 Apr 2023 18:51:28 GMT  
		Size: 32.6 MB (32616998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1371d2d81d70ec646fa25de2ef0e1ecbf8a73448a75536cdae53906746ee2605`  
		Last Modified: Thu, 06 Apr 2023 18:51:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:banon` - linux; s390x

```console
$ docker pull traefik@sha256:40c157efc3aeb2a68be807c7bd9c56058b039f5dc04ea99a2d207f5694ba3498
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38337898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed3cb8277e480dbe2a03868fd3de6e86d2381cb25b7d4cf62ca5209a4a8f36f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 29 Mar 2023 17:41:57 GMT
ADD file:675ad8acf4b076e34aeeba26dd482be7640df5912b1ec5e3183b7eb69c01e83e in / 
# Wed, 29 Mar 2023 17:41:57 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:38:21 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 06 Apr 2023 18:46:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.10/traefik_v2.9.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 06 Apr 2023 18:46:16 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 06 Apr 2023 18:46:16 GMT
EXPOSE 80
# Thu, 06 Apr 2023 18:46:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Apr 2023 18:46:16 GMT
CMD ["traefik"]
# Thu, 06 Apr 2023 18:46:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a76f78d8854217635d8049ec8501edb806f961e72989cfff8503982e6ff2579d`  
		Last Modified: Wed, 29 Mar 2023 17:42:31 GMT  
		Size: 3.2 MB (3175187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096a495bd82a55e97c5be084787578b5b5af0321a33c70ccf19bca0dc260a981`  
		Last Modified: Wed, 29 Mar 2023 22:39:11 GMT  
		Size: 622.6 KB (622584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ff0e0742f027721acb6e403cfd9c33f5035562626412821cf440ee0a0d4bd6`  
		Last Modified: Thu, 06 Apr 2023 18:46:41 GMT  
		Size: 34.5 MB (34539759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566cf6a3c532656d496f8fab7a8822e11cef4dd8c1dab24cdf229bbf359101eb`  
		Last Modified: Thu, 06 Apr 2023 18:46:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
