## `traefik:livarot`

```console
$ docker pull traefik@sha256:062dff1b5c54845f34147e04a251a645f3a5318c42da7127bf25a6e0d3c6e4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:livarot` - linux; amd64

```console
$ docker pull traefik@sha256:0cba9ff0d0fafa592f96d0ef0de2c1591bbce7c40fabb57dde2038c0ab3f2b73
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29071840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4c4921aee8ad7a7f66870bb726a8fa4d18f9b0b927ab1ef572e06be5241d65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 03:23:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 25 Feb 2021 03:23:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.5/traefik_v2.4.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 25 Feb 2021 03:23:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 25 Feb 2021 03:23:46 GMT
EXPOSE 80
# Thu, 25 Feb 2021 03:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 03:23:47 GMT
CMD ["traefik"]
# Thu, 25 Feb 2021 03:23:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7caf618c71a94b64d99880ac96da93c76a3931b35dffe57842d5baa964afbb3`  
		Last Modified: Thu, 25 Feb 2021 03:24:54 GMT  
		Size: 674.1 KB (674094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2d603874139eacbf2d7e18cdfa7eabd27a958eed533d7897ca97e176e2098`  
		Last Modified: Thu, 25 Feb 2021 03:25:00 GMT  
		Size: 25.6 MB (25582065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae52e7c5a84ee094d3d4cadb9254fe582fb3bf5ee4459db8e0296ed4a7589fd`  
		Last Modified: Thu, 25 Feb 2021 03:24:53 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:livarot` - linux; arm variant v6

```console
$ docker pull traefik@sha256:51e6acb6b11a005142df938a5c8364906bf46bfc72b336a25816da84a1f97b3f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27118958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e41e625833706e636d407ac328f8f6f0a458c3665c50e921be02c2246900373`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 24 Feb 2021 20:50:45 GMT
ADD file:72743cfd9913f13553e700f9d9cfdc17b9dc793ebeeb337fd5fe02dc962d4b63 in / 
# Wed, 24 Feb 2021 20:50:46 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:33:31 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 24 Feb 2021 23:33:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.5/traefik_v2.4.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 24 Feb 2021 23:33:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 24 Feb 2021 23:33:39 GMT
EXPOSE 80
# Wed, 24 Feb 2021 23:33:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 23:33:41 GMT
CMD ["traefik"]
# Wed, 24 Feb 2021 23:33:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:10e3bc1a9288f315752811ab2f438cb080f27de72c30375566135a542c8e03a1`  
		Last Modified: Wed, 24 Feb 2021 20:51:26 GMT  
		Size: 2.6 MB (2621066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95c78170691d118707d7ee1e0fde756aca169be42fe54416c614386b5d73e82`  
		Last Modified: Wed, 24 Feb 2021 23:35:10 GMT  
		Size: 677.0 KB (677008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e8de7d15c4484a563097a94cbab858afe450985c4b372f94b522b5ea1d8fa6`  
		Last Modified: Wed, 24 Feb 2021 23:35:25 GMT  
		Size: 23.8 MB (23820517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f48c4b827d0213635a8cc7951840f4390b222dc4556e5e471dfc6f190f71dce`  
		Last Modified: Wed, 24 Feb 2021 23:35:10 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:livarot` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:cb015f1dd60e184906c74e18791a4672de286e68d420a1c69f7b6aef3b9e4c16
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26735582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1dc0a165876c6732f35991df0b6ee44a94aee162782d0e65f09d5de023af29`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 04:18:27 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 25 Feb 2021 04:18:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.5/traefik_v2.4.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 25 Feb 2021 04:18:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 25 Feb 2021 04:18:33 GMT
EXPOSE 80
# Thu, 25 Feb 2021 04:18:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 04:18:34 GMT
CMD ["traefik"]
# Thu, 25 Feb 2021 04:18:35 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4961a79823a93d7b581d0d755b544c7ad8e44d35dec7296a3663c7815c9b8e5`  
		Last Modified: Thu, 25 Feb 2021 04:24:33 GMT  
		Size: 675.5 KB (675506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ab8ff4ffc015f2784025d016e57f87c58b493791912f6032182a23930a4312`  
		Last Modified: Thu, 25 Feb 2021 04:24:40 GMT  
		Size: 23.3 MB (23333893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dceb3bdde5806885fd1ee30d061aaf77bc9abcdff7d0a5cef10797211738765f`  
		Last Modified: Thu, 25 Feb 2021 04:24:33 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
